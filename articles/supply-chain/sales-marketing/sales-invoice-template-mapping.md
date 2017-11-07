---
title: Myyntilaskujen otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin myyntilaskujen otsikot ja rivit synkronoidaan Microsoft Dynamics 365 for Salesiin."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fb5ba099911deda5308daf92d82cd6b3489995bf
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a>Myyntilaskujen otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin

[!include[banner](../includes/banner.md)]

Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin myyntilaskujen otsikot ja rivit synkronoidaan Microsoft Dynamics 365 for Salesiin. 

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Seuraavia malleja ja niiden taustalla olevia tehtäviä käytetään synkronoimaan myyntilaskujen otsikot ja rivit Finance and Operationsista Salesiin:

- **Mallin nimi Tietojen integroinnissa** 

     - Myyntilaskut (Fin and Opsista Salesiin)

- **Tietojen integrointiprojektin tehtävien nimet**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Myyntilaskun otsikon ja rivien synkronointia edeltävät, pakolliset synkronointitehtävät:
-   Tuotteet (Fin and Opsista Salesiin)
-   Tilit (Salesista Fin and Opsiin) (jos käytössä)
-   Yhteystiedot (Salesista Fin and Opsiin) (jos käytössä)
-   Myyntitilauksen otsikko ja rivit (Fin and Opsista Salesiin)

## <a name="entity-set"></a>Yksikköjoukko

| Finance and Operations                               | Common Data Service (CDS)              | Myynti          |
|------------------------------------------------------|------------------|----------------|
| Ulkoisesti ylläpidettyjen asiakkaiden myyntilaskujen otsikot | SalesInvoice     | Laskut       |
| Ulkoisesti ylläpidettyjen asiakkaiden myyntilaskun rivit   | SalesInvoiceLine | InvoiceDetails |

## <a name="entity-flow"></a>Yksikön työnkulku

Myyntilaskut luodaan Finance and Operationsissa ja synkronoidaan Salesiin.

> [!NOTE]
> **Myyntilaskun otsikon** kuluihin liittyviä veroja ei tällä hetkellä synkronoida Finance and Operationsista Salesiin. Tämä johtuu siitä, että Sales ei tue verotietoja otsikkotasolla. Rivitason kuluihin liittyvät verot ovat tuettuja.

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

-  **Laskun numero -kenttään** lisätään **Lasku**-yksikköön ja se näytetään sivulla.
 
-  **Myyntitilaus**-sivun **Luo lasku** -painike on piilotettu, koska laskut luodaan Finance and Operationsissa, josta ne synkronoidaan Salesiin. **Laskusivua** ei voi muokata, sillä laskut synkronoidaan Finance and Operationsista.
 
-  **Myyntitilauksen tila** muuttuu automaattisesti **Laskutettu**-tilaan, kun liittyvä lasku on synkronoitu Finance and Operationsista Salesiin. Laskun omistajaksi määritetään sen myyntitilauksen omistaja, josta lasku on muodostettu. Näin myyntitilauksen omistaja voi tarkastella laskua.
 
## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

Järjestelmiin tulisi päivittää seuraavat asetukset ennen myyntilaskujen synkronointia:

### <a name="setup-in-sales"></a>Asetukset Salesissa

- Varmista kohdassa **Asetukset** > **Hallinto** > **Järjestelmäasetukset** > **Myynti**, että **Käytä järjestelmän hinnanlaskentajärjestelmää** -asetus on **Kyllä**. 

- Varmista kohdassa **Asetukset** > **Hallinto** > **Järjestelmäasetukset** > **Myynti**, että **Alennuksen laskutapa** -asetus on **Rivinimike**. 

### <a name="setup-in-the-data-integration-project"></a>Asetukset tietojen integrointiprojektissa

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader -tehtävä

- Päivitä yhdistämismääritys **CDS-organisaation tunnukselle** kohdassa **Lähde** > **CDS**. 

    -  **SalesOrder_Organization_OrganizationId**-oletusmalliarvo on ORG001.
    -  **Account_Organization_OrganizationId**-oletusmalliarvo on ORG001.
    -  **Organization_OrganizationId**-oletusmalliarvo on ORG001.

- Varmista, että tarvittava yhdistämismääritys on tehty kohtaan **Lähde** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.

    -  Mallin arvo on **ValueMap**, johon on yhdistetty maiden määrä.

- **Hinnasto** on pakollinen laskujen luontiin Salesissa. Päivitä **CDS**:n **ValueMap** -arvo > **Kohde -kohdasta pricelevelid.name [Hinnaston nimi]** arvoon Salesissa käytettävä valuuttakohtainen **Hinnasto**. Voit käyttää yhden valuutan oletusarvoista **hinnastoa** tai käyttää **ValueMap**-listaa, jos sinulla on useamman valuutan **hinnasto**.

    -  Mallin arvo **pricelevelid.name [Hinta nimi]** -mallille on **ValueMap**, joka perustuu **valuuttaan**.
    -  usd: CRM Service USA (esimerkki). 

#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine -tehtävä

- Varmista, että tarvittava yhdistämismääritys on luotu kohtaan **Lähde** > **CDS mittayksikölle**.

- Varmista, että tarvittava **ValueMap** kohteelle **SalesUnitSymbol** on määritetty Finance and Operationsin kohdassa **Lähde** > **CDS-yhdistämismääritys**. 
    
    - Mallin arvo **ValueMap** on määritetty arvoon **SalesUnitSymbol Quantity_UOM**.
    
-  Päivitä yhdistämismääritys **CDS-organisaation tunnukselle kohdassa Lähde** > **CDS**. 

    -  **SalesInvoicer_Organization_OrganizationId**-oletusmalliarvo on ORG001.
    -  **Product_Organization_OrganizationId**-oletusmalliarvo on ORG001.
 
## <a name="template-mapping-in-data-integrator"></a>Mallin yhdistäminen tietojen integrointiohjelmassa

> [!NOTE]
> **Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila** eivät sisälly oletusarvoisiin yhdistämismäärityksiin. Näiden kenttien yhdistäminen edellyttää arvomäärityksen määrittämistä, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Liittyvät aiheet

[Finance and Operationsin tuotteiden synkronointi Salesin tuotteisiin](products-template-mapping.md)

[Salesin asiakkaiden synkronointi Finance and Operationsin asiakkaisiin](accounts-template-mapping.md)

[Salesin yhteyshenkilöiden synkronointi Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin](contacts-template-mapping.md)

[Myyntitarjouksien otsikoiden ja rivien synkronointi Salesista Finance and Operationsiin](sales-quotation-template-mapping.md)

[Myyntitilauksien otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin](sales-order-template-mapping.md)


