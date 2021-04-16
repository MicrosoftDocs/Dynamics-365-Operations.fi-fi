---
title: Vero-integroinnin tietokenttien lisääminen laajennusten avulla
description: Tässä aiheessa kerrotaan, kuinka X++ -laajennuksia käytetään tietokenttien lisäämiseen verointegrointiin.
author: qire
ms.date: 03/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: fdf112bbdd5245d19ab1d07cfcf94c58bf8208c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830337"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a><span data-ttu-id="85d46-103">Vero-integroinnin tietokenttien lisääminen laajennuksen avulla</span><span class="sxs-lookup"><span data-stu-id="85d46-103">Add data fields in the tax integration by using extension</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="85d46-104">Tässä aiheessa kerrotaan, kuinka X++ -laajennuksia käytetään tietokenttien lisäämiseen verointegrointiin.</span><span class="sxs-lookup"><span data-stu-id="85d46-104">This topic explains how to use X++ extensions to add data fields in the tax integration.</span></span> <span data-ttu-id="85d46-105">Nämä kentät voidaan laajentaa veropalvelun verotietomalliin, ja niitä voidaan käyttää verokoodien määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="85d46-105">These fields can be extended to the tax data model of the tax service and used to determine tax codes.</span></span> <span data-ttu-id="85d46-106">Lisätietoja on kohdassa [Tietokenttien lisääminen verokonfiguraatioihin](tax-service-add-data-fields-tax-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="85d46-106">For more information, see [Add data fields in tax configurations](tax-service-add-data-fields-tax-configurations.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="85d46-107">Tietomalli</span><span class="sxs-lookup"><span data-stu-id="85d46-107">Data model</span></span>

<span data-ttu-id="85d46-108">Tietomallin tietoja säilyttävät objektit ja luokat toteuttavat ne.</span><span class="sxs-lookup"><span data-stu-id="85d46-108">The data in the data model is carried by objects and implemented by classes.</span></span>

<span data-ttu-id="85d46-109">Seuraavassa on luettelo tärkeimmistä objekteista:</span><span class="sxs-lookup"><span data-stu-id="85d46-109">Here is a list of the major objects:</span></span>

* <span data-ttu-id="85d46-110">AxClass/TaxIntegration **Document** Object</span><span class="sxs-lookup"><span data-stu-id="85d46-110">AxClass/TaxIntegration **Document** Object</span></span>
* <span data-ttu-id="85d46-111">AxClass/TaxIntegration **Line** Object</span><span class="sxs-lookup"><span data-stu-id="85d46-111">AxClass/TaxIntegration **Line** Object</span></span>
* <span data-ttu-id="85d46-112">AxClass/TaxIntegration **TaxLine** Object</span><span class="sxs-lookup"><span data-stu-id="85d46-112">AxClass/TaxIntegration **TaxLine** Object</span></span>

<span data-ttu-id="85d46-113">Seuraavassa kuvassa kerrotaan, miten nämä objektit liittyvät toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="85d46-113">The following illustration shows how these objects are related.</span></span>

<span data-ttu-id="85d46-114">[![Tietomallin objektisuhde](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span><span class="sxs-lookup"><span data-stu-id="85d46-114">[![Data model object relationship](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span></span>

<span data-ttu-id="85d46-115">**Document**-objekti voi sisältää useita **Line**-objekteja.</span><span class="sxs-lookup"><span data-stu-id="85d46-115">A **Document** object can contain many **Line** objects.</span></span> <span data-ttu-id="85d46-116">Kukin objekti sisältää veropalvelun metatietoja.</span><span class="sxs-lookup"><span data-stu-id="85d46-116">Each object contains metadata for the tax service.</span></span>

- <span data-ttu-id="85d46-117">`TaxIntegrationDocumentObject`-kohteessa on `originAddress`-metatieto, jotka sisältävät tietoja lähde-osoitteesta ja `includingTax`-metatieto, joka ilmaisee, sisältääkö rivisumma arvonlisäveron.</span><span class="sxs-lookup"><span data-stu-id="85d46-117">`TaxIntegrationDocumentObject` has `originAddress` metadata, which contains information about the source address, and `includingTax` metadata, which indicates whether the line amount includes sales tax.</span></span>
- <span data-ttu-id="85d46-118">`TaxIntegrationLineObject`-kohteella on `itemId`-, `quantity`- ja `categoryId`-metatiedot.</span><span class="sxs-lookup"><span data-stu-id="85d46-118">`TaxIntegrationLineObject` has `itemId`, `quantity`, and `categoryId` metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="85d46-119">`TaxIntegrationLineObject` toteuttaa myös **Charge**-objektit.</span><span class="sxs-lookup"><span data-stu-id="85d46-119">`TaxIntegrationLineObject` also implements **Charge** objects.</span></span>

## <a name="integration-flow"></a><span data-ttu-id="85d46-120">Integroinnin työnkulku</span><span class="sxs-lookup"><span data-stu-id="85d46-120">Integration flow</span></span>

<span data-ttu-id="85d46-121">Toiminnot manipuloivat työnkulun tietoja.</span><span class="sxs-lookup"><span data-stu-id="85d46-121">The data in the flow is manipulated by activities.</span></span>

### <a name="key-activities"></a><span data-ttu-id="85d46-122">Tärkeimmät toiminnot</span><span class="sxs-lookup"><span data-stu-id="85d46-122">Key activities</span></span>

* <span data-ttu-id="85d46-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="85d46-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span></span>
* <span data-ttu-id="85d46-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="85d46-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span></span>
* <span data-ttu-id="85d46-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="85d46-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span></span>
* <span data-ttu-id="85d46-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="85d46-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span></span>
* <span data-ttu-id="85d46-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="85d46-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span></span>

<span data-ttu-id="85d46-128">Tehtävät suoritetaan seuraavassa järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="85d46-128">Activities are run in the following order:</span></span>

1. <span data-ttu-id="85d46-129">Noutamisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="85d46-129">Setting Retrieval</span></span>
2. <span data-ttu-id="85d46-130">Tietojen noutaminen</span><span class="sxs-lookup"><span data-stu-id="85d46-130">Data Retrieval</span></span>
3. <span data-ttu-id="85d46-131">Laskentapalvelu</span><span class="sxs-lookup"><span data-stu-id="85d46-131">Calculation Service</span></span>
4. <span data-ttu-id="85d46-132">Valuutan vaihto</span><span class="sxs-lookup"><span data-stu-id="85d46-132">Currency Exchange</span></span>
5. <span data-ttu-id="85d46-133">Tietojen säilyvyys</span><span class="sxs-lookup"><span data-stu-id="85d46-133">Data Persistence</span></span>

<span data-ttu-id="85d46-134">Esimerkiksi laajenna **Tietojen nouto** ennen kuin **Laskentapalvelu**.</span><span class="sxs-lookup"><span data-stu-id="85d46-134">For example, extend **Data Retrieval** before **Calculation Service**.</span></span>

#### <a name="data-retrieval-activities"></a><span data-ttu-id="85d46-135">Tietojen noutamisen tehtävät</span><span class="sxs-lookup"><span data-stu-id="85d46-135">Data Retrieval activities</span></span>

<span data-ttu-id="85d46-136">**Tietojen noutamisen** tehtävät noutavat tietoja tietokannasta.</span><span class="sxs-lookup"><span data-stu-id="85d46-136">**Data Retrieval** activities retrieve data from the database.</span></span> <span data-ttu-id="85d46-137">Eri tapahtumien sovittimet ovat käytettävissä tietojen hakemiseen eri tapahtumatauluista:</span><span class="sxs-lookup"><span data-stu-id="85d46-137">Adapters for different transactions are available to retrieve data from different transaction tables:</span></span>

- <span data-ttu-id="85d46-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="85d46-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span></span>
- <span data-ttu-id="85d46-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="85d46-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span></span>
- <span data-ttu-id="85d46-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="85d46-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span></span>
- <span data-ttu-id="85d46-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="85d46-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span></span>
- <span data-ttu-id="85d46-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="85d46-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span></span>
- <span data-ttu-id="85d46-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="85d46-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span></span>
- <span data-ttu-id="85d46-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="85d46-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span></span>

<span data-ttu-id="85d46-145">Näissä **tietojen noutamisen** tehtävissä tiedot kopioidaan tietokannasta `TaxIntegrationDocumentObject`- ja `TaxIntegrationLineObject`-kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="85d46-145">In these **Data Retrieval** activities, data is copied from the database to `TaxIntegrationDocumentObject` and `TaxIntegrationLineObject`.</span></span> <span data-ttu-id="85d46-146">Koska kaikki nämä tehtävät laajentavat saman abstraktin malliluokan, niillä on yhteisiä metodeita.</span><span class="sxs-lookup"><span data-stu-id="85d46-146">Because all these activities extend the same abstract template class, they have common methods.</span></span>

#### <a name="calculation-service-activities"></a><span data-ttu-id="85d46-147">Laskentapalvelun tehtävät</span><span class="sxs-lookup"><span data-stu-id="85d46-147">Calculation Service activities</span></span>

<span data-ttu-id="85d46-148">**Laskentapalvelun** tehtävä on veropalvelun ja verointegraaton välinen linkki.</span><span class="sxs-lookup"><span data-stu-id="85d46-148">The **Calculation Service** activity is the link between the tax service and the tax integration.</span></span> <span data-ttu-id="85d46-149">Tämä tehtävä on vastuussa seuraavista toiminnoista:</span><span class="sxs-lookup"><span data-stu-id="85d46-149">This activity is responsible for the following functions:</span></span>

1. <span data-ttu-id="85d46-150">Muodosta pyyntö.</span><span class="sxs-lookup"><span data-stu-id="85d46-150">Construct the request.</span></span>
2. <span data-ttu-id="85d46-151">Lähetä pyyntö veropalveluun.</span><span class="sxs-lookup"><span data-stu-id="85d46-151">Post the request to the tax service.</span></span>
3. <span data-ttu-id="85d46-152">Hae vastaus veropalvelusta.</span><span class="sxs-lookup"><span data-stu-id="85d46-152">Get the response from the tax service.</span></span>
4. <span data-ttu-id="85d46-153">Jäsennä vastaus.</span><span class="sxs-lookup"><span data-stu-id="85d46-153">Parse the response.</span></span>

<span data-ttu-id="85d46-154">Pyyntöön lisättävä tietokenttä lähetetään yhdessä muiden metatietojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="85d46-154">A data field that you add to the request will be posted together with other metadata.</span></span> 

## <a name="extension-implementation"></a><span data-ttu-id="85d46-155">Laajennuksen toteutus</span><span class="sxs-lookup"><span data-stu-id="85d46-155">Extension implementation</span></span>

<span data-ttu-id="85d46-156">Tässä osassa on yksityiskohtaisia ohjeita laajennuksen toteuttamisesta.</span><span class="sxs-lookup"><span data-stu-id="85d46-156">This section provides detailed steps that explain how to implement the extension.</span></span> <span data-ttu-id="85d46-157">Esimerkkejä ovat taloushallinnon dimensiot **Kustannuspaikka** ja **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="85d46-157">It uses the **Cost center** and **Project** financial dimensions as examples.</span></span>

### <a name="step-1-add-the-data-variable-in-the-object-class"></a><span data-ttu-id="85d46-158">Vaihe 1.</span><span class="sxs-lookup"><span data-stu-id="85d46-158">Step 1.</span></span> <span data-ttu-id="85d46-159">Tietomuuttujan lisääminen objektiluokkaan</span><span class="sxs-lookup"><span data-stu-id="85d46-159">Add the data variable in the object class</span></span>

<span data-ttu-id="85d46-160">Objektiluokka sisältää tietomuuttujan sekä tietojen getter-/setter-metodit.</span><span class="sxs-lookup"><span data-stu-id="85d46-160">The object class contains the data variable and getter/setter methods for the data.</span></span> <span data-ttu-id="85d46-161">Lisää tietokenttä joko `TaxIntegrationDocumentObject`- tai `TaxIntegrationLineObject`-objektiin kentän tason mukaan.</span><span class="sxs-lookup"><span data-stu-id="85d46-161">Add the data field to either `TaxIntegrationDocumentObject` or `TaxIntegrationLineObject`, depending on the level of the field.</span></span> <span data-ttu-id="85d46-162">Seuraavassa esimerkissä käytetään rivitasoa, ja tiedoston nimi on `TaxIntegrationLineObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="85d46-162">The following example uses the line level, and the file name is `TaxIntegrationLineObject_Extension.xpp`.</span></span>

> [!NOTE]
> <span data-ttu-id="85d46-163">Jos lisätty tietokenttä on tiedostotasolla, muuta tiedoston nimeksi `TaxIntegrationDocumentObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="85d46-163">If the data field that you're adding is at the document level, change the file name to `TaxIntegrationDocumentObject_Extension.xpp`.</span></span>

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

<span data-ttu-id="85d46-164">**Kustannuspaikka** ja **Projekti** lisätään yksityisinä muuttujina.</span><span class="sxs-lookup"><span data-stu-id="85d46-164">**Cost center** and **Project** are added as private variables.</span></span> <span data-ttu-id="85d46-165">Voit käsitellä tietoja luomalla getter- ja setter-metodit näille tietokentille.</span><span class="sxs-lookup"><span data-stu-id="85d46-165">Create getter and setter methods for these data fields to manipulate the data.</span></span>

### <a name="step-2-retrieve-data-from-the-database"></a><span data-ttu-id="85d46-166">Vaihe 2.</span><span class="sxs-lookup"><span data-stu-id="85d46-166">Step 2.</span></span> <span data-ttu-id="85d46-167">Tietojen noutaminen tietokannasta</span><span class="sxs-lookup"><span data-stu-id="85d46-167">Retrieve data from the database</span></span>

<span data-ttu-id="85d46-168">Määritä tapahtuma ja nouda tiedot laajentamalla asianmukaiset sovitinluokat.</span><span class="sxs-lookup"><span data-stu-id="85d46-168">Specify the transaction, and extend the appropriate adapter classes to retrieve the data.</span></span> <span data-ttu-id="85d46-169">Jos käytät esimerkiksi **Ostotilaus**-tapahtumaa, on laajennettava `TaxIntegrationPurchTableDataRetrieval`- ja `TaxIntegrationVendInvoiceInfoTableDataRetrieval`-luokkia.</span><span class="sxs-lookup"><span data-stu-id="85d46-169">For example, if you use a **Purchase order** transaction, you must extend `TaxIntegrationPurchTableDataRetrieval` and `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span></span> 

> [!NOTE]
> <span data-ttu-id="85d46-170">`TaxIntegrationPurchParmTableDataRetrieval` on peritty `TaxIntegrationPurchTableDataRetrieval`-luokasta.</span><span class="sxs-lookup"><span data-stu-id="85d46-170">`TaxIntegrationPurchParmTableDataRetrieval` is inherited from `TaxIntegrationPurchTableDataRetrieval`.</span></span> <span data-ttu-id="85d46-171">Sitä ei saa muuttaa, ellei `purchTable`- ja `purchParmTable`-taulujen logiikka ole erilainen.</span><span class="sxs-lookup"><span data-stu-id="85d46-171">It should not be changed unless the logic of the `purchTable` and `purchParmTable` tables differs.</span></span>

<span data-ttu-id="85d46-172">Jos tietokenttä on lisättävä kaikille tapahtumille, laajenna kaikki `DataRetrieval`-luokat.</span><span class="sxs-lookup"><span data-stu-id="85d46-172">If the data field should be added for all transactions, extend all `DataRetrieval` classes.</span></span>

<span data-ttu-id="85d46-173">Koska **Tietojen nouto** -tehtävät laajentavat samaa malliluokkaa, luokkarakenteet, muuttujat ja metodit ovat samankaltaisia.</span><span class="sxs-lookup"><span data-stu-id="85d46-173">Because all **Data Retrieval** activities extend the same template class, the class structures, variables, and methods are similar.</span></span>

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

<span data-ttu-id="85d46-174">Seuraavassa esimerkissä esitetään perusrakenne, kun `PurchTable`-taulua käytetään.</span><span class="sxs-lookup"><span data-stu-id="85d46-174">The following example shows the basic structure when the `PurchTable` table is used.</span></span>

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

<span data-ttu-id="85d46-175">Kun `CopyToDocument`-metodia kutsutaan, `this.purchTable`-puskuri on jo olemassa.</span><span class="sxs-lookup"><span data-stu-id="85d46-175">When the `CopyToDocument` method is called, the `this.purchTable` buffer already exists.</span></span> <span data-ttu-id="85d46-176">Tämän metodin avulla voit kopioida kaikki tarvittavat tiedot `this.purchTable`-kohteesta `document`-objektiin käyttämällä `DocumentObject`-luokassa luotua setter-metodia.</span><span class="sxs-lookup"><span data-stu-id="85d46-176">The purpose of this method is to copy all the required data from `this.purchTable` to the `document` object by using the setter method that was created in the `DocumentObject` class.</span></span>

<span data-ttu-id="85d46-177">Samoin `this.purchLine`-puskuri on jo olemassa `CopyToLine`-metodissa.</span><span class="sxs-lookup"><span data-stu-id="85d46-177">Likewise, a `this.purchLine` buffer already exists in the `CopyToLine` method.</span></span> <span data-ttu-id="85d46-178">Tämän metodin avulla voit kopioida kaikki tarvittavat tiedot `this.purchLine`-kohteesta `_line`-objektiin käyttämällä `LineObject`-luokassa luotua setter-metodia.</span><span class="sxs-lookup"><span data-stu-id="85d46-178">The purpose of this method is to copy all the required data from `this.purchLine` to the `_line` object by using the setter method that was created in the `LineObject` class.</span></span>

<span data-ttu-id="85d46-179">Kaikkein suoraviivaisin tapa on laajentaa `CopyToDocument`- ja `CopyToLine`-metodeja.</span><span class="sxs-lookup"><span data-stu-id="85d46-179">The most straightforward approach is to extend the `CopyToDocument` and `CopyToLine` methods.</span></span> <span data-ttu-id="85d46-180">On kuitenkin suositeltavaa kokeilla ensin `copyToDocumentFromHeaderTable`- ja `copyToLineFromLineTable`-metodeja.</span><span class="sxs-lookup"><span data-stu-id="85d46-180">However, we recommend that you try the `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable` methods first.</span></span> <span data-ttu-id="85d46-181">Jos ne eivät toimi niin kuin on tarpeen, toteuta oma metodi ja kutsu sitä `CopyToDocument`- ja `CopyToLine`-metodeissa.</span><span class="sxs-lookup"><span data-stu-id="85d46-181">If they don't work as you require, implement your own method, and call it in `CopyToDocument` and `CopyToLine`.</span></span> <span data-ttu-id="85d46-182">Tätä lähestymistapaa voidaan käyttää kolmessa yleisessä tilanteessa:</span><span class="sxs-lookup"><span data-stu-id="85d46-182">There are three common situations where you might use this approach:</span></span>

- <span data-ttu-id="85d46-183">Pakollinen kenttä on kohteessa `PurchTable` tai `PurchLine`.</span><span class="sxs-lookup"><span data-stu-id="85d46-183">The required field is in `PurchTable` or `PurchLine`.</span></span> <span data-ttu-id="85d46-184">Tässä tapauksessa voit laajentaa kohteita `copyToDocumentFromHeaderTable` ja `copyToLineFromLineTable`.</span><span class="sxs-lookup"><span data-stu-id="85d46-184">In this situation, you can extend `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable`.</span></span> <span data-ttu-id="85d46-185">Tässä on esimerkkikoodi.</span><span class="sxs-lookup"><span data-stu-id="85d46-185">Here is the sample code.</span></span>

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

- <span data-ttu-id="85d46-186">Vaadittavat tiedot eivät ole tapahtuman oletustaulussa.</span><span class="sxs-lookup"><span data-stu-id="85d46-186">The required data isn't in the default table of the transaction.</span></span> <span data-ttu-id="85d46-187">Oletustauluun liittyy kuitenkin joitakin liitossuhteita, ja useimmilla riveillä kenttä on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="85d46-187">However, there are some join relationships with the default table, and the field is required on most lines.</span></span> <span data-ttu-id="85d46-188">Tässä tapauksessa voit korvata `getDocumentQueryObject`- tai `getLineObject`-metodin kyselläksesi taulusta liitossuhteen avulla.</span><span class="sxs-lookup"><span data-stu-id="85d46-188">In this situation, replace `getDocumentQueryObject` or `getLineObject` to query the table by join relationship.</span></span> <span data-ttu-id="85d46-189">Seuraavassa esimerkissä **Toimita nyt** -kenttä integroidaan rivitasolla myyntitilauksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="85d46-189">In the following example, the **Deliver Now** field is integrated with the sales order at the line level.</span></span>

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

    <span data-ttu-id="85d46-190">Tässä esimerkissä `mcrSalesLineDropShipment`-puskurit määritetään ja kysely määritetään kohdassa `getLineQueryObject`.</span><span class="sxs-lookup"><span data-stu-id="85d46-190">In this example, a `mcrSalesLineDropShipment` buffer is declared, and the query is defined in `getLineQueryObject`.</span></span> <span data-ttu-id="85d46-191">Kysely käyttää suhdetta `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span><span class="sxs-lookup"><span data-stu-id="85d46-191">The query uses the relationship `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span></span> <span data-ttu-id="85d46-192">Kun olet laajentamassa tässä tilanteessa, voit korvata `getLineQueryObject`-kohteen omalla luodulla kyselyobjektilla.</span><span class="sxs-lookup"><span data-stu-id="85d46-192">While you're extending in this situation, you can replace `getLineQueryObject` with your own constructed query object.</span></span> <span data-ttu-id="85d46-193">Ota kuitenkin seuraavat seikat huomioon:</span><span class="sxs-lookup"><span data-stu-id="85d46-193">However, note the following points:</span></span>

    * <span data-ttu-id="85d46-194">Koska `getLineQueryObject`-metodin palautusarvo on `SysDaQueryObject`, sinun on muodostettava tämä objekti SysDa-lähestymistavan avulla.</span><span class="sxs-lookup"><span data-stu-id="85d46-194">Because the return value of the `getLineQueryObject` method is `SysDaQueryObject`, you must construct this object by using the SysDa approach.</span></span>
    * <span data-ttu-id="85d46-195">Aiemmin luotua taulua ei voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="85d46-195">Can't remove existed table.</span></span>

- <span data-ttu-id="85d46-196">Vaadittavat tiedot liittyvät tapahtumatauluun monimutkaisella liitossuhteella, tai suhde ei ole yksi yhteen (1:1) vaan yksi moneen (1:N).</span><span class="sxs-lookup"><span data-stu-id="85d46-196">The required data is related to the transaction table by a complicated join relationship, or the relation isn't one to one (1:1) but one to many (1:N).</span></span> <span data-ttu-id="85d46-197">Tässä tapauksessa tilanne on hieman monimutkaisempi.</span><span class="sxs-lookup"><span data-stu-id="85d46-197">In this situation, things become a little complicated.</span></span> <span data-ttu-id="85d46-198">Tämä tilanne koskee taloushallinnon dimensioiden esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="85d46-198">This situation applies to the example of financial dimensions.</span></span> 

    <span data-ttu-id="85d46-199">Tässä tapauksessa voit toteuttaa oman metodin tietojen hakemiseksi.</span><span class="sxs-lookup"><span data-stu-id="85d46-199">In this situation, you can implement your own method to retrieve the data.</span></span> <span data-ttu-id="85d46-200">Tässä on esimerkkikoodi `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`-tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="85d46-200">Here is the sample code in the `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` file.</span></span>

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

### <a name="step-3-add-data-to-the-request"></a><span data-ttu-id="85d46-201">Vaihe 3.</span><span class="sxs-lookup"><span data-stu-id="85d46-201">Step 3.</span></span> <span data-ttu-id="85d46-202">Tietojen lisääminen pyyntöön</span><span class="sxs-lookup"><span data-stu-id="85d46-202">Add data to the request</span></span>

<span data-ttu-id="85d46-203">Laajenna `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject`- tai `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine`-metodi lisätäksesi tiedot pyyntöön.</span><span class="sxs-lookup"><span data-stu-id="85d46-203">Extend the `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` or `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method to add data to the request.</span></span> <span data-ttu-id="85d46-204">Tässä on esimerkkikoodi `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`-tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="85d46-204">Here is the sample code in the `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` file.</span></span>

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

<span data-ttu-id="85d46-205">Tässä koodissa `_destination` on paketointiobjekti, jota käytetään POST-pyynnön luonnissa ja `_source` on `TaxIntegrationLineObject`-objekti.</span><span class="sxs-lookup"><span data-stu-id="85d46-205">In this code, `_destination` is the wrapper object that is used to generate the post request, and `_source` is the `TaxIntegrationLineObject` object.</span></span> 

> [!NOTE]
> * <span data-ttu-id="85d46-206">Määritä avain, jota käytetään pyyntölomakkeessa nimellä `private const str`.</span><span class="sxs-lookup"><span data-stu-id="85d46-206">Define the key that is used in the request form as `private const str`.</span></span>
> * <span data-ttu-id="85d46-207">Määritä `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine`-metodin kenttä `SetField`-metodin avulla.</span><span class="sxs-lookup"><span data-stu-id="85d46-207">Set the field in the `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method by using the `SetField` method.</span></span> <span data-ttu-id="85d46-208">Toisen parametrin tietotyypin on oltava `string`.</span><span class="sxs-lookup"><span data-stu-id="85d46-208">The data type of the second parameter should be `string`.</span></span> <span data-ttu-id="85d46-209">Jos tietotyyppi ei ole `string` muunna tietotyypiksi `string`.</span><span class="sxs-lookup"><span data-stu-id="85d46-209">If the data type isn't `string`, convert it to `string`.</span></span>

## <a name="appendix"></a><span data-ttu-id="85d46-210">Liite</span><span class="sxs-lookup"><span data-stu-id="85d46-210">Appendix</span></span>

<span data-ttu-id="85d46-211">Tästä liitteestä ilmenee taloushallinnon dimensioiden (**Kustannuspaikka** ja **Projekti**) integroinnin koko esimerkkikoodi rivitasolla.</span><span class="sxs-lookup"><span data-stu-id="85d46-211">This appendix shows the complete sample code for the integration of financial dimensions (**Cost center** and **Project**) at the line level.</span></span>

### <a name="taxintegrationlineobject_extensionxpp"></a><span data-ttu-id="85d46-212">TaxIntegrationLineObject_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="85d46-212">TaxIntegrationLineObject_Extension.xpp</span></span>

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

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a><span data-ttu-id="85d46-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="85d46-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span></span>

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

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a><span data-ttu-id="85d46-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="85d46-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span></span>

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
