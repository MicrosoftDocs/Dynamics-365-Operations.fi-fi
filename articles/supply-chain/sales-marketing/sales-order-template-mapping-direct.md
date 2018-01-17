---
title: Myyntitilauksien otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin
description: "Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin myyntitilausten otsikot ja rivit synkronoidaan suoraan Microsoft Dynamics 365 for Salesiin."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Myyntitilauksien otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin myyntitilausten otsikot ja rivit synkronoidaan suoraan Microsoft Dynamics 365 for Salesiin.

## <a name="data-flow-in-prospect-to-cash"></a>Prospektista käteiseksi -ratkaisun tiedonkulku

Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Finance and Operations and Sales -esiintymien tietojen synkronoinnissa. Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Finance and Operationsin ja Salesin välillä. Seuraavassa kuvassa kerrotaan, miten tiedot synkronoidaan Finance and Operations- ja Sales-sovelluksen välillä.

[![Prospektista käteiseksi -ratkaisun tiedonkulku](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Näet käytettävissä olevat mallit avaamalla [PowerApps-hallintakeskuksen](https://preview.admin.powerapps.com/dataintegration). Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan myyntitilausten otsikot ja rivit Finance and Operationsista Salesiin:

- **Mallin nimi tietojen integroinnissa:** Myyntitilaukset (Fin and Opsista Salesiin) – suora
- **Tehtävien nimet tietojen integrointiprojektissa:**

    - OrderHeader
    - OrderLine

Seuraavat synkronointitehtävät tarvitaan, ennen kuin myyntilaskujen otsikot ja rivit voidaan synkronoida:

- Tuotteet (Fin and Opsista Salesiin) - suora
- Tilit (Salesista Fin and Opsiin) - suora (jos käytössä)
- Yhteyshenkilöistä asiakkaisiin (Salesista Fin and Opsiin) - suora (jos käytössä)

## <a name="entity-set"></a>Yksikköjoukko

| Finance and Operations  | Myynti             |
|-------------------------|-------------------|
| CDS myyntitilauksen otsikot | SalesOrders       |
| CDS-myyntitilausrivit   | SalesOrderDetails |

## <a name="entity-flow"></a>Yksikön työnkulku

Myyntitilaukset luodaan Finance and Operationsissa ja synkronoidaan Salesiin.

Mallin suodattimen auttavat varmistamaan, että vain asiaankuuluvat myyntitilaukset synkronoidaan:

- Salesin myyntitilauksen tilaava asiakas ja laskutusasiakas sisällytetään synkronointiin. Finance and Operations -sovelluksen **OrderingCustomerIsExternallyMaintained**- ja **InvoiceCustomerIsExternallyMaintained**-kenttiä käytetään tietoyksiköiden synkronointien seurantaan.
- Myyntitilaus on vahvistettava Finance and Operationsissa. Salesiin synkronoidaan vain vahvistetut myyntitilaukset tai myyntitilaukset joilla on ylempi käsittelytila, kuten **Lähetetty** tai **Laskutettu**.
- Kun myyntitilaus on luotu tai kun sitä on muokattu, **Laske kokonaismyynti** -eräajo on suoritettava Finance and Operationsissa. Salesiin synkronoidaan vain myyntitilaukset, joiden loppusummat on laskettu.

> [!NOTE]
> Tällä hetkellä myyntitilauksen otsikon kuluihin liittyviä veroja ei synkronoida Finance and Operationsista Salesiin. Sales ei tue verotietoja otsikkotasolla. Sen sijaan rivitason kuluihin liittyvä vero sisällytetään synkronointiin.

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

**Tilaus**-yksikköön on lisätty uusia kenttiä, jotka näkyvät sivulla:

- **Ulkoisesti ylläpidetty** – määritä tämän vaihtoehdon arvoksi **Kyllä**, kun tilaus on peräisin Finance and Operationsista.
- **Käsittelytila** – tämä kenttä näyttää tilauksen käsittelytilan Finance and Operationsissa. Käytettävissä ovat seuraavat arvot:

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

**Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -asetusta käytetään muissa myyntitilausskenaarioissa (esimerkiksi synkronointi Salesista Finance and Operationsiin), jotta järjestelmä voi seurata, koostuuko myyntitilaus täysin ulkoisesti ylläpidetyistä tuotteista. Jos myyntitilauksessa on vain ulkoisesti ylläpidettyjä tuotteita, tuotteita ylläpidetään Finance and Operationsissa. Tämä asetus auttaa varmistamaan, ettet yritä synkronoida sellaisia myyntitilausrivejä, joissa on tuotteita, joita Finance and Operations ei tunne.

**Myyntitilaus**-sivun **Luo lasku**, **Peruuta tilaus**, **Laske uudelleen**, **Hae tuotteet** ja **Hae osoite** -painikkeet on piilotettu ulkoisesti ylläpidetyissä tilauksissa, koska laskut luodaan Finance and Operationsissa, josta ne synkronoidaan Salesiin. Tilaussivua ei voi muokata, sillä myyntitilaustiedot synkronoidaan Finance and Operationsista.

Myyntitilauksen tila pysyy **aktiivisena**, jotta muutokset Finance and Operationsista siirtyvät Salesin myyntitilaukseen. Voit ohjata tätä toimintaa määrittämällä **Tilakoodi \[tila\]**-arvoksi **Aktiivinen** tietojen integrointiprojektissa.

## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

Seuraavat asetukset tulee päivittää järjestelmissä ennen myyntitilausten synkronointia.

### <a name="setup-in-sales"></a>Asetukset Salesissa

- Varmista, että sen käyttäjän ryhmän käyttöoikeudet on määritetty, jolle Salesissa asetettu yhteys on määritetty. Jos käytät esittelytietoja, käyttäjällä on usein järjestelmänvalvojan käyttöoikeudet, mutta ryhmällä ei. Jos ryhmällä ei ole myöskään järjestelmänvalvojan käyttöoikeuksia, kun suoritat projektin tietojen integrointiohjelmasta, saat virheilmoituksen, jossa kerrotaan ensisijaisen ryhmän puuttumisesta.

    Siirry kohtaan **Asetukset** > **Suojaus** > **Ryhmät**ja valitse haluamasi ryhmä. Valitse **Roolien hallinta** ja valitse sitten halutut käyttöoikeudet, kuten **järjestelmänvalvoja**.

- Siirry kohtaan **Asetukset** > **Hallinto** > **Järjestelmäasetukset** > **Sales** ja varmista, että käytössä ovat seuraavat asetukset:

    - **Käytä järjestelmän hinnanlaskentajärjestelmää** -asetuksen arvoksi on määritetty **Kyllä**.
    - **Alennuksen laskutapa** -kentän arvoksi on määritetty **Rivinimike**.

### <a name="setup-in-finance-and-operations"></a>Asetukset Finance and Operationsissa

Siirry kohtaan **Myynti ja markkinointi** > **Kausittaiset tehtävät** > **Laske kokonaismyynti**. Määritä sitten erätyönä suoritettava työ. Määritä **Laske myyntitilausten loppusummat** -vaihtoehdon arvoksi **Kyllä**. Tämä vaihe on tärkeä, koska Salesiin synkronoidaan vain myyntitilaukset, joiden loppusummat on laskettu. Erätyön toistovälin tulisi olla sama kuin myyntitilausten synkronoinnin toistoväli.

### <a name="setup-in-the-data-integration-project"></a>Asetukset tietojen integrointiprojektissa

#### <a name="salesheader-task"></a>SalesHeader -tehtävä

- Varmista, että tarvittavat yhdistämismääritykset on tehty **InvoiceCountryRegionId**- ja **BillingAddress\_Country**-kohdalle ja **DeliveryCountryRegionId**- ja **DeliveryAddress\_Country**-kohdalle.

    Malliarvo on arvomääritys, jossa on yhdistetty useita maita tai alueita.

- Hinnasto on pakollinen Salesissa, jotta tilauksia voidaan luoda. Päivitä **pricelevelid.name \[hinnaston nimi\]**-kohdan arvomääritykseksi Salesissa käytettävä hinnasto. Yhdelle valuutalle voit käyttää oletushinnastoa. Vaihtoehtoisesti voit käyttää arvomääritystä, jos hinnastossa on useita valuuttoja.

    **pricelevelid.name \[hinnaston nimi\]** -kohdan oletusmallin arvo on **CRM Service USA (esimerkki)**.

#### <a name="salesline-task"></a>SalesLine -tehtävä

- Varmista, että **DeliveryCountryRegionId**- ja **DeliveryAddress\_Country**-kohdan välinen yhdistämismääritys on tehty.

    Malliarvo on arvomääritys, jossa on yhdistetty useita maita tai alueita.

- Varmista, että Finance and Operationsin **SalesUnitSymbol**-kohdassa on vaadittu arvomääritys.

    **SalesUnitSymbol**-kohdan malliarvoksi, jolla on arvomääritys, on määritetty **Quantity\_UOM**.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

> [!NOTE]
> **Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin. Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä. 

> [!NOTE]
> Yhdistämismääritys osoittaa, minkä kentän tiedot synkronoidaan Salesista Finance and Operationsiin.

### <a name="orderheader"></a>OrderHeader

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a>OrderLine

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Liittyvät aiheet

[Prospektista käteiseksi](prospect-to-cash.md)

[Sales-asiakkaiden synkronointi suoraan Finance and Operations -asiakkaisiin](accounts-template-mapping-direct.md)

[Finance and Operationsin tuotteiden synkronointi suoraan Salesin tuotteisiin](products-template-mapping-direct.md)

[Salesin yhteyshenkilöiden synkronointi suoraan Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin](contacts-template-mapping-direct.md)

[Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin](sales-invoice-template-mapping-direct.md)




