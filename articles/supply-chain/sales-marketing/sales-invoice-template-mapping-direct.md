---
title: Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin myyntilaskujen otsikot ja rivit synkronoidaan suoraan Microsoft Dynamics 365 for Salesiin."
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: afbf4a24b737cf7221bac4b688b8801b1bcd839c
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin

[!INCLUDE [banner](../includes/banner.md)]

Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin myyntilaskujen otsikot ja rivit synkronoidaan suoraan Microsoft Dynamics 365 for Salesiin.

## <a name="data-flow-in-prospect-to-cash"></a>Prospektista käteiseksi -ratkaisun tiedonkulku

Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Finance and Operations and Sales -esiintymien tietojen synkronoinnissa. Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Finance and Operationsin ja Salesin välillä. Seuraavassa kuvassa kerrotaan, miten tiedot synkronoidaan Finance and Operations- ja Sales-sovelluksen välillä.

[![Prospektista käteiseksi -ratkaisun tiedonkulku](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Näet käytettävissä olevat mallit avaamalla [PowerApps-hallintakeskuksen](https://preview.admin.powerapps.com/dataintegration). Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan myyntilaskujen otsikot ja rivit Finance and Operationsista Salesiin:

- **Mallin nimi tietojen integroinnissa:** Myyntilaskut (Fin and Opsista Salesiin) – suora
- **Tehtävien nimet tietojen integrointiprojektissa:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Seuraavat synkronointitehtävät tarvitaan, ennen kuin myyntilaskujen otsikot ja rivit voidaan synkronoida:

- Tuotteet (Fin and Opsista Salesiin) - suora
- Tilit (Salesista Fin and Opsiin) - suora (jos käytössä)
- Yhteyshenkilöt (Salesista Fin and Opsiin) - suora (jos käytössä)
- Myyntitilauksen otsikko ja rivit (Fin and Opsista Salesiin) - suora

## <a name="entity-set"></a>Yksikköjoukko

| Finance and Operations                               | Myynti          |
|------------------------------------------------------|----------------|
| Ulkoisesti ylläpidettyjen asiakkaiden myyntilaskujen otsikot | Laskut       |
| Ulkoisesti ylläpidettyjen asiakkaiden myyntilaskun rivit   | InvoiceDetails |

## <a name="entity-flow"></a>Yksikön työnkulku

Myyntilaskut luodaan Finance and Operationsissa ja synkronoidaan Salesiin.

> [!NOTE]
> Tällä hetkellä myyntilaskun otsikon kuluihin liittyviä veroja ei synkronoida Finance and Operationsista Salesiin. Sales ei tue verotietoja otsikkotasolla. Sen sijaan rivitason kuluihin liittyvä vero sisällytetään synkronointiin.

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

- **Laskun numero** -kenttä on lisätty **Lasku**-yksikköön. Se näkyy sivulla.
- **Myyntitilaus**-sivun **Luo lasku** -painike on piilotettu, koska laskut luodaan Finance and Operationsissa, josta ne synkronoidaan Salesiin. **Lasku**-sivua ei voi muokata, sillä laskut synkronoidaan Finance and Operationsista.
- **Myyntitilauksen tila** -arvo muuttuu automaattisesti **Laskutettu**-tilaksi, kun liittyvä lasku on synkronoitu Finance and Operationsista Salesiin. Lisäksi laskun omistajaksi määritetään sen myyntitilauksen omistaja, josta lasku on muodostettu. Tämän vuoksi myyntitilauksen omistaja voi tarkastella laskua.

## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

Seuraavat asetukset tulee päivittää järjestelmissä ennen myyntilaskujen synkronointia.

### <a name="setup-in-sales"></a>Asetukset Salesissa

Siirry kohtaan **Asetukset** > **Hallinto** > **Järjestelmäasetukset** > **Sales** ja varmista, että käytössä ovat seuraavat asetukset:

- **Käytä järjestelmän hinnanlaskentajärjestelmää** -asetuksen arvoksi on määritetty **Kyllä**.
- **Alennuksen laskutapa** -kentän arvoksi on määritetty **Rivinimike**.

### <a name="setup-in-the-data-integration-project"></a>Asetukset tietojen integrointiprojektissa

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader -tehtävä

- Varmista, että **InvoiceCountryRegionId**- ja **BillingAddress\_Country** -kohdan välinen yhdistämismääritys on tehty.

    Malliarvo on arvomääritys, jossa on yhdistetty useita maita tai alueita.

- Hinnasto on pakollinen Salesissa, jotta laskuja voidaan luoda. Päivitä **pricelevelid.name \[hinnaston nimi\]**-kohdan arvomääritykseksi Salesissa käytettävä hinnasto. Yhdelle valuutalle voit käyttää oletushinnastoa. Vaihtoehtoisesti voit käyttää arvomääritystä, jos hinnastossa on useita valuuttoja.

    **pricelevelid.name \[Price list name\]**-kohdan mallin arvo on arvomääritys, joka perustuu USD-valuuttaan = CRM Service USA (esimerkki).  
    
#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine -tehtävä

- Varmista, että **Mittayksikkö**-kohdalla on pakollinen yhdistämismääritys.
- Varmista, että Finance and Operationsin **SalesUnitSymbol**-kohdassa on vaadittu arvomääritys.

    **SalesUnitSymbol**-kohdan malliarvoksi, jolla on arvomääritys, on määritetty **Quantity\_UOM**.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

> [!NOTE]
> **Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin. Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä. 

> [!NOTE]
> Yhdistämismääritys osoittaa, minkä kentän tiedot synkronoidaan Salesista Finance and Operationsiin.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Liittyvät aiheet

[Prospektista käteiseksi](prospect-to-cash.md)

[Sales-asiakkaiden synkronointi suoraan Finance and Operations -asiakkaisiin](accounts-template-mapping-direct.md)

[Finance and Operationsin tuotteiden synkronointi suoraan Salesin tuotteisiin](products-template-mapping-direct.md)

[Salesin yhteyshenkilöiden synkronointi suoraan Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin](contacts-template-mapping-direct.md)

[Myyntitilauksien otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin](sales-order-template-mapping-direct-two-ways.md)







