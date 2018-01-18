---
title: Myyntitilauksien otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin myyntitilausten otsikot ja rivit synkronoidaan Microsoft Dynamics 365 for Salesiin."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c7b2ff6430e99661ee284f65089086df9fa5a1ad
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a>Myyntitilauksien otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin

[!include[banner](../includes/banner.md)]

Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin myyntitilausten otsikot ja rivit synkronoidaan Microsoft Dynamics 365 for Salesiin. 

## <a name="template-and-tasks"></a>Malli ja tehtävät

Seuraavia malleja ja niiden taustalla olevia tehtäviä käytetään synkronoimaan myyntitilausten otsikot ja rivit Finance and Operationsista Salesiin:

- **Mallin nimi Tietojen integroinnissa** 

    - Myyntitilaukset (Fin and Opsista Salesiin)
    
- **Tietojen integrointiprojektin tehtävien nimet**

    - OrderHeader
    - OrderLine

Myyntilaskun otsikon ja rivien synkronointia edeltävät, pakolliset synkronointitehtävät:

- Tuotteet (Fin and Opsista Salesiin)
- Tilit (Salesista Fin and Opsiin) (jos käytössä)
- Yhteyshenkilöstä asiakkaisiin (Salesista Fin and Opsiin) (jos käytössä)

## <a name="entity-set"></a>Yksikköjoukko

| Finance and Operations |    Common Data Service (CDS)         |     Myynti      |
|------------------------|----------------|----------------|
| CDS myyntitilauksen otsikot| SalesOrder     | SalesOrders |
| CDS-myyntitilausrivit  | SalesOrderLine | SalesOrderDetails|

## <a name="entity-flow"></a>Yksikön työnkulku

Myyntitilaukset luodaan Finance and Operationsissa ja synkronoidaan Salesiin.

Mallin suodattimen varmistavat, että vain asiaankuuluvat myyntitilaukset synkronoidaan:

- Salesista synkronoitavaan myyntitilaukseen sisältyvät niin tilaava kuin laskuttava asiakas. Finance and Operationsin kenttiä **OrderingCustomerIsExternallyMaintained** ja **InvoiceCustomerIsExternallyMaintained** käytetään tietoyksiköiden synkronointien seurantaan.

- **Myyntitilaus** on vahvistettava Finance and Operationsissa. Salesiin synkronoidaan vain vahvistetut myyntitilaukset, tai tilaukset joilla on ylempi käsittelytila, kuten Toimitettu tai Laskutettu.

- Luotuasi tai muokattuasi myyntitilauksen, aja **Laske kokonaismyynti** -eräajo Finance and Operationsissa. CDS:ään ja Salesiin synkronoidaan ainoastaan myyntitilaukset, joiden kokonaismyynti on laskettu.

> [!NOTE]
> **Myyntitilauksen otsikon** kuluihin liittyviä veroja ei tällä hetkellä synkronoida Finance and Operationsista Salesiin. Tämä johtuu siitä, että Sales ei tue verotietoja otsikkotasolla. Rivitason kuluihin liittyvät verot ovat tuettuja.

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

**Tilaus**-yksikköön on lisätty uusia kenttiä, jotka näkyvät sivulla:

- **Ulkoisesti ylläpidetty** - aseta arvoksi **Kyllä**, kun tilaus on peräisin Finance and Operationsista.

- **Käsittelytila** - näyttää tilauksen käsittelytilan Finance and Operationsissa. Arvoja ovat

    - Aktiivinen
    - Vahvistettu
    - Pakkausluettelo
    - Laskutettu
    - Keräilty
    - Osittain keräilty
    - Osittain pakattu
    - Lähetetty
    - Osittain lähetetty
    - Osittain laskutettu
    - Peruutettu

**Vain ulkoisesti ylläpidettyjä tuotteita** -asetusta käytetään muissa myyntitilausskenaarioissa (synkronointi Salesista Finance and Operationsiin), jotta järjestelmä voi seurata, koostuuko myyntitilaus täysin **ulkoisesti ylläpidetyistä tuotteista**, jolloin tuotteita ylläpidetään Finance and Operationsissa. Tämä varmistaa, ettet yritä synkronoida myyntitilausrivejä sellaisten tuotteiden kanssa, joita Finance and Operations ei tunne.
 
**Myyntitilaus**-sivun **Luo lasku**, **Peruuta tilaus**, **Laske uudelleen**, **Hae tuotteet** ja **Hae osoite** -painikkeet on piilotettu ulkoisesti ylläpidetyissä tilauksissa, koska laskut luodaan Finance and Operationsissa, josta ne synkronoidaan Salesiin. Tilaussivua ei voi muokata, sillä myyntitilaustiedot synkronoidaan Finance and Operationsista.
 
**Myyntitilauksen tila** pysyy aktiivisena, jotta muutokset Finance and Operationsista siirtyvät Salesin **myyntitilaukseen**. Tämä määräytyy asettamalla **Tilakoodi [Status]** -oletusarvoksi **Aktiivinen** tietojen integrointiprojektissa.

## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset 

Järjestelmiin tulisi päivittää seuraavat asetukset ennen myyntitilausten synkronointia:

### <a name="setup-in-sales"></a>Asetukset Salesissa

- Varmista, että käyttäjän ryhmän käyttöoikeudet (Salesin **Yhteysasetus**) on liitetty. Jos käytät esittelytietoja, käyttäjällä on usein järjestelmänvalvojan käyttöoikeudet, mutta ryhmällä ei. Ilman tätä asetusta näyttöön tulee virhe, Ensisijainen ryhmä puuttuu, kun projekti suoritetaan tietojen integrointitoiminnossa. 

    - Valitse **Asetukset** > **Suojaus** > **Ryhmät** ja sitten haluamasi ryhmän, valitse **Roolien hallinta** ja sitten rooli ja halutut käyttöoikeudet, esim. Järjestelmänvalvoja.

- Varmista kohdassa **Asetukset** > **Hallinto** > **Järjestelmäasetukset** > **Myynti**, että **Käytä järjestelmän hinnanlaskentajärjestelmää** -asetus on **Kyllä**. 

- Varmista kohdassa **Asetukset** > **Hallinto** > **Järjestelmäasetukset** > **Myynti**, että **Alennuksen laskutapa** -asetus on **Rivinimike**. 

### <a name="setup-in-finance-and-operations"></a>Asetukset Finance and Operationsissa

Määritä **Myynti ja markkinointi** > **Kausittaiset tehtävät** > **Laske kokonaismyynti** suoritettavaksi erätyönä, jonka **Laske myyntitilausten loppusummat** -asetukseksi on määritetty **Kyllä**. Tämä on tärkeää, sillä CDS:ään ja Salesiin synkronoidaan ainoastaan myyntitilaukset, joiden kokonaismyynti on laskettu. Erätyön toistovälin tulee olla sama kuin myyntitilausten toistoväli.

### <a name="setup-in-the-data-integration-project"></a>Asetukset tietojen integrointiprojektissa

#### <a name="salesheader-task"></a>SalesHeader -tehtävä

- Päivitä yhdistämismääritys **CDS-organisaation tunnukselle kohdassa Lähde** > **CDS**.

    - **Account_Organization_OrganizationId**-oletusmalliarvo on ORG001.
    - **InvoiceAccount_Organization_OrganizationId**-oletusmalliarvo on ORG001.
    - **Organization_OrganizationId**-oletusmalliarvo on ORG001.

- Varmista, että tarvittavat yhdistämismääritykset on tehty kohtiin **Lähde** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** ja **DeliveryCountryRegionId to DeliveryAddress_Country**.

    - Mallin arvo on **ValueMap**, johon on yhdistetty maiden määrä.

- **Hinnasto** on pakollinen tilausten luontiin Salesissa. Päivitä **CDS**:n **ValueMap** -arvo > **Kohde** -kohdasta **pricelevelid.name [Hinnaston nimi]** arvoon Salesissa käytettävä valuuttakohtainen **Hinnasto**. Voit käyttää yhden valuutan oletusarvoista **hinnastoa** tai käyttää **ValueMap**-listaa, jos sinulla on useamman valuutan **hinnasto**.
    
    - Mallin **pricelevelid.name [Hinnaston nimi]** oletusarvo on CRM Service USA (sample). 

#### <a name="salesline-task"></a>SalesLine -tehtävä

- Päivitä yhdistämismääritys **CDS-organisaation tunnukselle kohdassa Lähde** > **CDS**. 
    
    - **SalesOrder_Organization_OrganizationId**-oletusmalliarvo on ORG001.
    - **Product_Organization_OrganizationId**-oletusmalliarvo on ORG001.

- Varmista, että tarvittava yhdistämismääritys on tehty kohtaan **Lähde** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.

    - Mallin arvo on **ValueMap**, johon on yhdistetty maiden määrä.
    
- Varmista, että tarvittava **ValueMap** kohteelle **SalesUnitSymbol** on määritetty Finance and Operationsin kohdassa **Lähde** > **CDS-yhdistämismääritys**.

    - Mallin arvo **ValueMap** on määritetty arvoon **SalesUnitSymbol Quantity_UOM**.

## <a name="template-mapping-in-data-integrator"></a>Mallin yhdistäminen tietojen integrointiohjelmassa

> [!NOTE]
> **Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin. Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.

### <a name="orderheader"></a>OrderHeader

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-order-template-mapping-data-integrator-1.png)

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a>OrderLine

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-order-template-mapping-data-integrator-3.png)

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Liittyvät aiheet

[Finance and Operationsin tuotteiden synkronointi Salesin tuotteisiin](products-template-mapping.md)

[Salesin asiakkaiden synkronointi Finance and Operationsin asiakkaisiin](accounts-template-mapping.md)

[Salesin yhteyshenkilöiden synkronointi Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin](contacts-template-mapping.md)

[Myyntitarjouksien otsikoiden ja rivien synkronointi Salesista Finance and Operationsiin](sales-quotation-template-mapping.md)

[Myyntilaskujen otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin](sales-invoice-template-mapping.md)


