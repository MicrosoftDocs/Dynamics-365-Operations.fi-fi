---
title: Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Supply Chain Managementista Salesiin
description: Tässä ohjeaiheessa käsitellään malleja ja niiden taustalla olevia tehtäviä, joita käytetään synkronoimaan myyntilaskujen otsikot ja rivit suoraan Dynamics 365 Supply Chain Managementista Dynamics 365 Salesiin.
author: Henrikan
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: c2f988b4f170c027444ba7cf54a55e0bd846cedf
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571638"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja niiden taustalla olevia tehtäviä, joita käytetään synkronoimaan myyntilaskujen otsikot ja rivit suoraan Dynamics 365 Supply Chain Managementista Dynamics 365 Salesiin.

## <a name="data-flow-in-prospect-to-cash"></a>Prospektista käteiseksi -ratkaisun tiedonkulku

Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Supply Chain Managementin and Salesin esiintymien tietojen synkronoinnissa. Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Supply Chain Managementin ja Salesin välillä. Seuraava kuva näyttää, miten tiedot synkronoidaan Supply Chain Managementin ja Salesin välillä.

[![Prospektista käteiseksi -ratkaisun tiedonkulku.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Näet käytettävissä olevat mallit avaamalla [Power Apps-hallintakeskuksen](https://preview.admin.powerapps.com/dataintegration). Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoitaessa myyntilaskujen otsikot ja rivit Supply Chain Managementista Salesiin:

- **Mallin nimi tietojen integroinnissa:** Myyntilaskut (Fin and Opsista Salesiin) – suora
- **Tehtävien nimet tietojen integrointiprojektissa:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Seuraavat synkronointitehtävät tarvitaan, ennen kuin myyntilaskujen otsikot ja rivit voidaan synkronoida:

- Tuotteet (Supply Chain Managementista Salesiin) - suora
- Tilit (Salesista Supply Chain Managementiin) - Suora (jos käytössä)
- Yhteyshenkilöt (Salesista Supply Chain Managementiin) - Suora (jos käytössä)
- Myyntitilauksen otsikko ja rivit (Supply Chain Managementista Salesiin) - Suora

## <a name="entity-set"></a>Yksikköjoukko

| Toimitusketjun hallinta                              | Myynti          |
|------------------------------------------------------|----------------|
| Ulkoisesti ylläpidettyjen asiakkaiden myyntilaskujen otsikot | Laskut       |
| Ulkoisesti ylläpidettyjen asiakkaiden myyntilaskun rivit   | InvoiceDetails |

## <a name="entity-flow"></a>Yksikön työnkulku

Myyntilaskut luodaan Supply Chain Managementissa ja synkronoidaan Salesiin.

> [!NOTE]
> Tällä hetkellä myyntilaskun otsikon kuluihin liittyviä veroja ei synkronoida Supply Chain Managementista Salesiin. Sales ei tue verotietoja otsikkotasolla. Sen sijaan rivitason kuluihin liittyvä vero sisällytetään synkronointiin.

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

- **Laskun numero** -kenttä on lisätty **Lasku**-yksikköön. Se näkyy sivulla.
- **Myyntitilaus**-sivun **Luo lasku** -painike on piilotettu, koska laskut luodaan Supply Chain Managementissa, josta ne synkronoidaan Salesiin. **Lasku**-sivua ei voi muokata, sillä laskut synkronoidaan Supply Chain Managementista.
- **Myyntitilauksen tila** -arvo muuttuu automaattisesti **Laskutettu**-tilaksi, kun liittyvä lasku on synkronoitu Supply Chain Managementista Salesiin. Lisäksi laskun omistajaksi määritetään sen myyntitilauksen omistaja, josta lasku on muodostettu. Tämän vuoksi myyntitilauksen omistaja voi tarkastella laskua.

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
- Varmista, että Supply Chain Managementin **SalesUnitSymbol**-kohdassa on vaadittu arvomääritys.

    **SalesUnitSymbol**-kohdan malliarvoksi, jolla on arvomääritys, on määritetty **Quantity\_UOM**.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

> [!NOTE]
> **Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin. Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä. 

> [!NOTE]
> Yhdistämismääritys osoittaa, minkä kentän tiedot synkronoidaan Salesista Supply Chain Managementiin.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![SalesInvoiceHeaderin tietojen integroinnin mallimääritys.](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![SalesInvoiceLinen tietojen integroinnin mallimääritys.](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Liittyvät aiheet

[Prospektista käteiseksi](prospect-to-cash.md)

[Tilien synkronointi suoraan Salesin tuotteista Supply Chain Managementin asiakkaisiin](accounts-template-mapping-direct.md)

[Supply Chain Managementin tuotteiden synkronointi suoraan Salesin tuotteisiin](products-template-mapping-direct.md)

[Salesin yhteyshenkilöiden synkronointi suoraan Supply Chain Managementin yhteyshenkilöihin tai asiakkaisiin](contacts-template-mapping-direct.md)

[Myyntitilausten synkronointi suoraan Salesin ja Supply Chain Managementin välillä](sales-order-template-mapping-direct-two-ways.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]