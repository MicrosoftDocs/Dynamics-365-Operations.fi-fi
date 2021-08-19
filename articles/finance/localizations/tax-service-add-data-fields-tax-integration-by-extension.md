---
title: Vero-integroinnin tietokenttien lisääminen laajennusten avulla
description: Tässä aiheessa kerrotaan, kuinka X++ -laajennuksia käytetään tietokenttien lisäämiseen verointegrointiin.
author: qire
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8bdd56ebdd50c1eae98094725a01bf9c5ec52bb4e689eb282f80631810a65725
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721655"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>Vero-integroinnin tietokenttien lisääminen laajennuksen avulla

[!include [banner](../includes/banner.md)]


Tässä aiheessa kerrotaan, kuinka X++ -laajennuksia käytetään tietokenttien lisäämiseen verointegrointiin. Nämä kentät voidaan laajentaa veropalvelun verotietomalliin, ja niitä voidaan käyttää verokoodien määrittämiseen. Lisätietoja on kohdassa [Tietokenttien lisääminen verokonfiguraatioihin](tax-service-add-data-fields-tax-configurations.md).

## <a name="data-model"></a>Tietomalli

Tietomallin tietoja säilyttävät objektit ja luokat toteuttavat ne.

Seuraavassa on luettelo tärkeimmistä objekteista:

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

Seuraavassa kuvassa kerrotaan, miten nämä objektit liittyvät toisiinsa.

[![Tietomallin objektisuhde.](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

**Document**-objekti voi sisältää useita **Line**-objekteja. Kukin objekti sisältää veropalvelun metatietoja.

- `TaxIntegrationDocumentObject`-kohteessa on `originAddress`-metatieto, jotka sisältävät tietoja lähde-osoitteesta ja `includingTax`-metatieto, joka ilmaisee, sisältääkö rivisumma arvonlisäveron.
- `TaxIntegrationLineObject`-kohteella on `itemId`-, `quantity`- ja `categoryId`-metatiedot.

> [!NOTE]
> `TaxIntegrationLineObject` toteuttaa myös **Charge**-objektit.

## <a name="integration-flow"></a>Integroinnin työnkulku

Toiminnot manipuloivat työnkulun tietoja.

### <a name="key-activities"></a>Tärkeimmät toiminnot

* AxClass/TaxIntegration **Calculation** ActivityOnDocument
* AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument
* AxClass/TaxIntegration **DataPersistence** ActivityOnDocument
* AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument
* AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument

Tehtävät suoritetaan seuraavassa järjestyksessä:

1. Noutamisen määrittäminen
2. Tietojen noutaminen
3. Laskentapalvelu
4. Valuutan vaihto
5. Tietojen säilyvyys

Esimerkiksi laajenna **Tietojen nouto** ennen kuin **Laskentapalvelu**.

#### <a name="data-retrieval-activities"></a>Tietojen noutamisen tehtävät

**Tietojen noutamisen** tehtävät noutavat tietoja tietokannasta. Eri tapahtumien sovittimet ovat käytettävissä tietojen hakemiseen eri tapahtumatauluista:

- AxClass/TaxIntegration **PurchTable** DataRetrieval
- AxClass/TaxIntegration **PurchParmTable** DataRetrieval
- AxClass/TaxIntegration **PurchREQTable** DataRetrieval
- AxClass/TaxIntegration **PurchRFQTable** DataRetrieval
- AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval
- AxClass/TaxIntegration **SalesTable** DataRetrieval
- AxClass/TaxIntegration **SalesParm** DataRetrieval

Näissä **tietojen noutamisen** tehtävissä tiedot kopioidaan tietokannasta `TaxIntegrationDocumentObject`- ja `TaxIntegrationLineObject`-kohteeseen. Koska kaikki nämä tehtävät laajentavat saman abstraktin malliluokan, niillä on yhteisiä metodeita.

#### <a name="calculation-service-activities"></a>Laskentapalvelun tehtävät

**Laskentapalvelun** tehtävä on veropalvelun ja verointegraaton välinen linkki. Tämä tehtävä on vastuussa seuraavista toiminnoista:

1. Muodosta pyyntö.
2. Lähetä pyyntö veropalveluun.
3. Hae vastaus veropalvelusta.
4. Jäsennä vastaus.

Pyyntöön lisättävä tietokenttä lähetetään yhdessä muiden metatietojen kanssa. 

## <a name="extension-implementation"></a>Laajennuksen toteutus

Tässä osassa on yksityiskohtaisia ohjeita laajennuksen toteuttamisesta. Esimerkkejä ovat taloushallinnon dimensiot **Kustannuspaikka** ja **Projekti**.

### <a name="step-1-add-the-data-variable-in-the-object-class"></a>Vaihe 1. Tietomuuttujan lisääminen objektiluokkaan

Objektiluokka sisältää tietomuuttujan sekä tietojen getter-/setter-metodit. Lisää tietokenttä joko `TaxIntegrationDocumentObject`- tai `TaxIntegrationLineObject`-objektiin kentän tason mukaan. Seuraavassa esimerkissä käytetään rivitasoa, ja tiedoston nimi on `TaxIntegrationLineObject_Extension.xpp`.

> [!NOTE]
> Jos lisätty tietokenttä on tiedostotasolla, muuta tiedoston nimeksi `TaxIntegrationDocumentObject_Extension.xpp`.

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

**Kustannuspaikka** ja **Projekti** lisätään yksityisinä muuttujina. Voit käsitellä tietoja luomalla getter- ja setter-metodit näille tietokentille.

### <a name="step-2-retrieve-data-from-the-database"></a>Vaihe 2. Tietojen noutaminen tietokannasta

Määritä tapahtuma ja nouda tiedot laajentamalla asianmukaiset sovitinluokat. Jos käytät esimerkiksi **Ostotilaus**-tapahtumaa, on laajennettava `TaxIntegrationPurchTableDataRetrieval`- ja `TaxIntegrationVendInvoiceInfoTableDataRetrieval`-luokkia. 

> [!NOTE]
> `TaxIntegrationPurchParmTableDataRetrieval` on peritty `TaxIntegrationPurchTableDataRetrieval`-luokasta. Sitä ei saa muuttaa, ellei `purchTable`- ja `purchParmTable`-taulujen logiikka ole erilainen.

Jos tietokenttä on lisättävä kaikille tapahtumille, laajenna kaikki `DataRetrieval`-luokat.

Koska **Tietojen nouto** -tehtävät laajentavat samaa malliluokkaa, luokkarakenteet, muuttujat ja metodit ovat samankaltaisia.

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

Seuraavassa esimerkissä esitetään perusrakenne, kun `PurchTable`-taulua käytetään.

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

Kun `CopyToDocument`-metodia kutsutaan, `this.purchTable`-puskuri on jo olemassa. Tämän metodin avulla voit kopioida kaikki tarvittavat tiedot `this.purchTable`-kohteesta `document`-objektiin käyttämällä `DocumentObject`-luokassa luotua setter-metodia.

Samoin `this.purchLine`-puskuri on jo olemassa `CopyToLine`-metodissa. Tämän metodin avulla voit kopioida kaikki tarvittavat tiedot `this.purchLine`-kohteesta `_line`-objektiin käyttämällä `LineObject`-luokassa luotua setter-metodia.

Kaikkein suoraviivaisin tapa on laajentaa `CopyToDocument`- ja `CopyToLine`-metodeja. On kuitenkin suositeltavaa kokeilla ensin `copyToDocumentFromHeaderTable`- ja `copyToLineFromLineTable`-metodeja. Jos ne eivät toimi niin kuin on tarpeen, toteuta oma metodi ja kutsu sitä `CopyToDocument`- ja `CopyToLine`-metodeissa. Tätä lähestymistapaa voidaan käyttää kolmessa yleisessä tilanteessa:

- Pakollinen kenttä on kohteessa `PurchTable` tai `PurchLine`. Tässä tapauksessa voit laajentaa kohteita `copyToDocumentFromHeaderTable` ja `copyToLineFromLineTable`. Tässä on esimerkkikoodi.

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- Vaadittavat tiedot eivät ole tapahtuman oletustaulussa. Oletustauluun liittyy kuitenkin joitakin liitossuhteita, ja useimmilla riveillä kenttä on pakollinen. Tässä tapauksessa voit korvata `getDocumentQueryObject`- tai `getLineObject`-metodin kyselläksesi taulusta liitossuhteen avulla. Seuraavassa esimerkissä **Toimita nyt** -kenttä integroidaan rivitasolla myyntitilauksen kanssa.

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    Tässä esimerkissä `mcrSalesLineDropShipment`-puskurit määritetään ja kysely määritetään kohdassa `getLineQueryObject`. Kysely käyttää suhdetta `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`. Kun olet laajentamassa tässä tilanteessa, voit korvata `getLineQueryObject`-kohteen omalla luodulla kyselyobjektilla. Ota kuitenkin seuraavat seikat huomioon:

    * Koska `getLineQueryObject`-metodin palautusarvo on `SysDaQueryObject`, sinun on muodostettava tämä objekti SysDa-lähestymistavan avulla.
    * Aiemmin luotua taulua ei voi poistaa.

- Vaadittavat tiedot liittyvät tapahtumatauluun monimutkaisella liitossuhteella, tai suhde ei ole yksi yhteen (1:1) vaan yksi moneen (1:N). Tässä tapauksessa tilanne on hieman monimutkaisempi. Tämä tilanne koskee taloushallinnon dimensioiden esimerkkiä. 

    Tässä tapauksessa voit toteuttaa oman metodin tietojen hakemiseksi. Tässä on esimerkkikoodi `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`-tiedostossa.

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a>Vaihe 3. Tietojen lisääminen pyyntöön

Laajenna `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject`- tai `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine`-metodi lisätäksesi tiedot pyyntöön. Tässä on esimerkkikoodi `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`-tiedostossa.

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```

Tässä koodissa `_destination` on paketointiobjekti, jota käytetään POST-pyynnön luonnissa ja `_source` on `TaxIntegrationLineObject`-objekti. 

> [!NOTE]
> * Määritä avain, jota käytetään pyyntölomakkeessa nimellä `private const str`.
> * Määritä `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine`-metodin kenttä `SetField`-metodin avulla. Toisen parametrin tietotyypin on oltava `string`. Jos tietotyyppi ei ole `string` muunna tietotyypiksi `string`.

## <a name="appendix"></a>Liite

Tästä liitteestä ilmenee taloushallinnon dimensioiden (**Kustannuspaikka** ja **Projekti**) integroinnin koko esimerkkikoodi rivitasolla.

### <a name="taxintegrationlineobject_extensionxpp"></a>TaxIntegrationLineObject_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a>TaxIntegrationPurchTableDataRetrieval_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a>TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
