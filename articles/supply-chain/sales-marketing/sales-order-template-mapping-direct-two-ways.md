---
title: "Myyntitilausten synkronointi suoraan Salesin ja Finance and Operationsin välillä"
description: "Tässä ohjeaiheessa esitellään mallit ja niiden taustalla olevat tehtävät, joita käytetään synkronoitaessa myyntitilaukset suoraan Microsoft Dynamics 365 for Salesin ja Microsoft Dynamics 365 for Finance and Operationsin välillä."
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2018
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
ms.openlocfilehash: e26244ffc380291a40edfbd2c2cb5911b0d8b3cb
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="synchronization-of-sales-orders-directly-between-sales-and-finance-and-operations"></a>Myyntitilausten synkronointi suoraan Salesin ja Finance and Operationsin välillä

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa esitellään mallit ja niiden taustalla olevat tehtävät, joita käytetään synkronoitaessa myyntitilaukset suoraan Microsoft Dynamics 365 for Salesin ja Microsoft Dynamics 365 for Finance and Operationsin välillä.

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Näet käytettävissä olevat mallit avaamalla [PowerApps-hallintakeskuksen](https://preview.admin.powerapps.com/dataintegration). Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.

Seuraavia malleja ja niiden taustalla olevia tehtäviä käytetään synkronoitaessa myyntitilaukset suoraan Salesin ja Finance and Operationsin välillä:

- **Mallien nimet tietojen integroinnissa:** 

    - Myyntitilaukset (Salesista Fin and Opsiin) - suora
    - Myyntitilaukset (Fin and Opsista Salesiin) - suora

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

Myyntitilaukset luodaan Salesissa ja ne synkronoidaan Finance and Operationsiin, kun **Suorita projekti** käynnistetään projektille, joka perustuu **Myyntitilaukset (Salesista Fin and Opsiin) - suora** -malliin. Voit aktivoida ja synkronoida myyntitilaukset Salesista vain, jos **tilaustuotteet** koostuvat vain ulkoisesti ylläpidetyistä tuotteista. Tämän vuoksi käsin lisättyjä tuotteita ei voi olla. Kun tilaus on aktivoitu, myyntitilaus määritetään vain luku -tilaan käyttöliittymässä. Tässä vaiheessa päivitykset tehdään Finance and Operationsissa. Kun myyntitilauksen tila on **Vahvistettu**, **Myyntitilaukset (Fin and Opsista Salesiin) - suora** -malliin perustuvaa projektia voi käyttää Finance and Operationsista Salesiin tapahtuvien päivitysten tai toimitusten tilojen synkronoinnissa.

Sinun ei tarvitse luoda tilauksia Sales-sovelluksessa. Voit luoda uudet myyntitilaukset sen sijaan Finance and Operations -sovelluksessa. Kun myyntitilauksen tilaksi on määritetty **Vahvista**, se synkronoidaan Salesiin edellisessä kappaleessa kuvatulla tavalla.

Finance and Operations -sovelluksen mallin suodattimet auttavat varmistamaan, että synkronointiin sisällytetään vain halutut myyntitilaukset.

- Sekä myyntitilauksen tilaava asiakas että laskutusasiakas on saatava Sales-sovelluksesta, jotta nämä tiedot sisällytetään synkronointiin. Finance and Operations -sovelluksen **OrderingCustomerIsExternallyMaintained**- ja **InvoiceCustomerIsExternallyMaintained**-kenttiä käytetään myyntitilausten suodattamiseen tietoyksiköistä.
- Myyntitilaus on vahvistettava Finance and Operationsissa. Salesiin synkronoidaan vain vahvistetut myyntitilaukset tai myyntitilaukset joilla on ylempi käsittelytila, kuten **Lähetetty** tai **Laskutettu**.
- Kun myyntitilaus on luotu tai kun sitä on muokattu, **Laske kokonaismyynti** -eräajo on suoritettava Finance and Operationsissa. Salesiin synkronoidaan vain myyntitilaukset, joiden loppusummat on laskettu.

## <a name="freight-tax"></a>Rahdin verot

Sales ei tue veroa otsikkotasolla, koska verot tallennetaan rivitasolle. Kun Finance and Operationsin otsikkotason veroja, kuten rahdin veroja, halutaan tukea, järjestelmä synkronoi verot Salesiin käsin lisättynä tuotteena, jonka nimi on **Rahdin vero**. Se synkronoi myös Finance and Operationsin verosumman. Näin Salesin vakiohinnan laskentaa voidaan käyttää kokonaissummissa, vaikka Finance and Operationsissa olisi käytössä otsikkotason vero.

## <a name="discount-calculation-and-rounding"></a>Alennuksen laskeminen ja pyöristäminen

Salesin alennuksen laskentamalli on erilainen kuin Finance and Operationsin alennuksen laskentamalli. Finance and Operationsissa myyntirivin lopullinen alennussumma voi olla alennussummien ja alennusprosenttien yhdistelmän tulos. Jos tämä lopullinen alennussumma jaetaan rivin määrällä, tulos saatetaan pyöristää. Pyöristystä ei kuitenkaan tehdä, jos pyöristetty yksikkökohtainen alennussumma synkronoidaan Salesiin. Voit varmistaa, että Finance and Operations -myyntirivin koko alennussumma synkronoidaan oikein Salesiin, kun koko summa synkronoidaan ilman, että sitä jaetaan rivimäärällä. Tämän vuoksi Salesin **Alennuksen laskutapa** -kohdan arvoksi on määritettävä **Rivinimike**.

Kun myyntitilausrivi synkronoidaan Salesista Finance and Operationsiin, käytetään koko rivin alennussummaa. Koska Finance and Operationsissa ei ole kenttää, johon rivin koko alennussumman voisi tallentaa, summa jaetaan määrällä ja tallennetaan **Rivialennus**-kenttään. Tässä jaossa tapahtuva mahdollinen pyöristys tallennetaan myyntirivin **Myynnin kulut** -kenttään.

### <a name="example"></a>Esimerkki

**Synkronointi Salesista Finance and Operationsiin**

- **Sales:** Määrä = 3, rivikohtainen alennus = 10,00 $
- **Finance and Operations:** Määrä = 3, rivin alennussumma = 3,33 $, myynnin kulut = -0,01 $ 

**Synkronointi Finance and Operationsista Salesiin**

- **Finance and Operations:** Määrä = 3, rivin alennussumma = 3,33 $, myynnin kulut = -0,01 $
- **Sales:** Määrä = 3, rivikohtainen alennus = (3 × 3,33 $) + 0,01 $ = 10,00 $

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

**Tilaus**-yksikköön on lisätty uusia kenttiä, jotka näkyvät sivulla:

- **Ulkoisesti ylläpidetty** – määritä tämän vaihtoehdon arvoksi **Kyllä**, kun tilaus on peräisin Finance and Operationsista.
- **Käsittelytila** – tämä kenttä näyttää tilauksen käsittelytilan Finance and Operationsissa. Käytettävissä ovat seuraavat arvot:

    - **Luonnos** – alkuperäinen tila, jossa tilaus luodaan Salesissa. Vain tässä käsittelytilassa olevia tilauksia voi muokata Salesissa.
    - **Aktiivinen** – tila sen jälkeen, kun tilaus on aktivoitu Salesissa **Aktivoi**-painikkeen avulla.
    - **Vahvistettu**
    - **Pakkausluettelo**
    - **Laskutettu**
    - **Keräilty**
    - **Osittain keräilty**
    - **Osittain pakattu**
    - **Lähetetty**
    - **Osittain lähetetty**
    - **Osittain laskutettu**
    - **Peruutettu**

**Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -asetusta käytetään tilauksen aktivoinnin aikana. Sen avulla seurataan johdonmukaisesti, koostuuko myyntitilaus kokonaan ulkoisesti ylläpidetyistä tuotteista. Jos myyntitilauksessa on vain ulkoisesti ylläpidettyjä tuotteita, tuotteita ylläpidetään Finance and Operationsissa. Tämä asetus auttaa varmistamaan, ettet aktivoi ja yritä synkronoida sellaisia myyntitilausrivejä, joissa on tuotteita, joita Finance and Operations ei tunne.

**Myyntitilaus**-sivun **Luo lasku**, **Peruuta tilaus**, **Laske uudelleen**, **Hae tuotteet** ja **Hae osoite** -painikkeet on piilotettu ulkoisesti ylläpidetyissä tilauksissa, koska laskut luodaan Finance and Operationsissa, josta ne synkronoidaan Salesiin. Näitä tilauksia ei voi muokata, sillä myyntitilaustiedot synkronoidaan Finance and Operationsista aktivoinnin jälkeen.

Myyntitilauksen tila pysyy **aktiivisena**, jotta muutokset Finance and Operationsista siirtyvät Salesin myyntitilaukseen. Voit ohjata tätä toimintaa määrittämällä **Tilakoodi \[tila\]**-arvoksi **Aktiivinen** tietojen integrointiprojektissa.

## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

Seuraavat asetukset tulee päivittää järjestelmissä ennen myyntitilausten synkronointia.

### <a name="setup-in-sales"></a>Asetukset Salesissa

- Varmista, että sen käyttäjän ryhmän käyttöoikeudet on määritetty, jolle Salesissa asetettu yhteys on määritetty. Jos käytät esittelytietoja, käyttäjällä on usein järjestelmänvalvojan käyttöoikeudet, mutta ryhmällä ei. Jos ryhmällä ei ole järjestelmänvalvojan käyttöoikeuksia, kun suoritat projektin tietojen integrointiohjelmasta, saat virheilmoituksen, jossa kerrotaan ensisijaisen ryhmän puuttumisesta.

    Siirry kohtaan **Asetukset** &gt; **Suojaus** &gt; **Ryhmät** ja valitse haluamasi ryhmä. Valitse **Roolien hallinta** ja valitse sitten halutut käyttöoikeudet, kuten **järjestelmänvalvoja**.

- Voit varmistaa alennusten oikean laskennan sekä Salesissa että Finance and Operationsissa valitsemalla **Alennuksen laskentatapa** -asetukseksi **Rivinimike**.
- Siirry kohtaan **Asetukset** &gt; **Hallinto** &gt; **Järjestelmäasetukset** &gt; **Sales** ja varmista, että käytössä ovat seuraavat asetukset:

    - **Käytä järjestelmän hinnanlaskentajärjestelmää** -asetuksen arvoksi on määritetty **Kyllä**.
    - **Alennuksen laskutapa** -kentän arvoksi on määritetty **Rivinimike**.

### <a name="setup-in-finance-and-operations"></a>Asetukset Finance and Operationsissa

- Siirry kohtaan **Myynti ja markkinointi** &gt; **Kausittaiset tehtävät** &gt; **Laske kokonaismyynti**. Määritä sitten erätyönä suoritettava työ. Määritä **Laske myyntitilausten loppusummat** -vaihtoehdon arvoksi **Kyllä**. Tämä vaihe on tärkeä, koska Salesiin synkronoidaan vain myyntitilaukset, joiden loppusummat on laskettu. Erätyön toistovälin tulisi olla sama kuin myyntitilausten synkronoinnin toistoväli.

### <a name="setup-in-the-sales-orders-sales-to-fin-and-ops---direct-data-integration-project"></a>Myyntitilaukset (Salesista Fin and Opsiin) - suora -integrointiprojektin asetukset

- Varmista, että **Shipto\_country**- ja **DeliveryAddressCountryRegionISOCode**-kohdan välinen yhdistämismääritys on tehty. Voit määrittää arvomäärityksessä tyhjän oletusarvon, jos haluat välttää maan syöttämisen kansallisissa tilauksissa. Jätä vasen puoli tyhjäksi ja määritä oikean puolen arvoksi haluamasi maa tai alue.

    Malliarvo on arvomääritys, jossa on yhdistetty useita maita tai alueita. Jos kohta jätetään tyhjäksi, arvo on US.

### <a name="setup-in-the-sales-orders-fin-and-ops-to-sales---direct-data-integration-project"></a>Myyntitilaukset (Fin and Opsista Salesiin) - suora -integrointiprojektin asetukset

#### <a name="salesheader-task"></a>SalesHeader -tehtävä

- Hinnasto on pakollinen Salesissa, jotta tilauksia voidaan luoda. Päivitä **pricelevelid.name \[hinnaston nimi\]**-kohdan arvomääritykseksi Salesissa käytettävä hinnasto. Yhdelle valuutalle voit käyttää oletushinnastoa. Vaihtoehtoisesti voit käyttää arvomääritystä, jos hinnastossa on useita valuuttoja.

    **pricelevelid.name \[hinnaston nimi\]** -kohdan oletusmallin arvo on **CRM Service USA (esimerkki)**.

#### <a name="salesline-task"></a>SalesLine -tehtävä

- Varmista, että Finance and Operationsin **SalesUnitSymbol**-kohdassa on vaadittu arvomääritys.
- Varmista, että Salesissa on määritetty pakolliset yksiköt.

    **SalesUnitSymbol**-kohdan malliarvoksi, jolla on arvomääritys, on määritetty **oumid.name**.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

> [!NOTE]
> **Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin. Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

> [!NOTE]
> Yhdistämismääritys osoittaa, minkä kentän tiedot synkronoidaan Salesista Finance and Operationsiin tai Finance and Operationsista Salesiin.

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderheader"></a>Myyntitilaukset (Fin and Opsista Salesiin) - suora: OrderHeader

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderline"></a>Myyntitilaukset (Fin and Opsista Salesiin) - suora: OrderLine

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderheader"></a>Myyntitilaukset (Salesista Fin and Opsiin) - suora: OrderHeader

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderline"></a>Myyntitilaukset (Salesista Fin and Opsiin) - suora: OrderLine

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Liittyvät aiheet

[Prospektista käteiseksi](prospect-to-cash.md)

