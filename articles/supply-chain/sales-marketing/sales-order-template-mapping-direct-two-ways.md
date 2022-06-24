---
title: Myyntitilausten synkronointi suoraan Salesin ja Supply Chain Managementin välillä
description: Artikkelissa käsitellään malleja ja niiden taustalla olevia tehtäviä, joita käytetään myyntitilausten synkronointiin suoraan Dynamics 365 Salesin ja Dynamics 365 Supply Chain Managementin välillä.
author: Henrikan
ms.date: 05/09/2019
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
ms.openlocfilehash: 63a9be9bedabe1f15ad8db583151aa7fa480473b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854149"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-supply-chain-management"></a>Myyntitilausten synkronointi suoraan Salesin ja Supply Chain Managementin välillä

[!include [banner](../includes/banner.md)]



Artikkelissa käsitellään malleja ja niiden taustalla olevia tehtäviä, joita käytetään myyntitilausten synkronointiin suoraan Dynamics 365 Salesin ja Dynamics 365 Supply Chain Managementin välillä.

## <a name="data-flow-in-prospect-to-cash"></a>Prospektista käteiseksi -ratkaisun tiedonkulku

Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Supply Chain Managementin and Salesin esiintymien tietojen synkronoinnissa. Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Supply Chain Managementin ja Salesin välillä. Seuraava kuva näyttää, miten tiedot synkronoidaan Supply Chain Managementin ja Salesin välillä.

[![Prospektista käteiseksi -ratkaisun tiedonkulku.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Näet käytettävissä olevat mallit avaamalla [Power Apps-hallintakeskuksen](https://preview.admin.powerapps.com/dataintegration). Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.

Seuraavia malleja ja niiden taustalla olevia tehtäviä käytetään synkronoitaessa myyntitilauksia suoraan Salesin ja Supply Chain Managementin välillä.

- **Mallien nimet tietojen integroinnissa:** 

    - Myyntitilaukset (Salesista Supply Chain Managementiin) - suora
    - Myyntitilaukset (Supply Chain Managementista Salesiin) - suora

- **Tehtävien nimet tietojen integrointiprojektissa:**

    - OrderHeader
    - OrderLine

Seuraavat synkronointitehtävät tarvitaan, ennen kuin myyntilaskujen otsikot ja rivit voidaan synkronoida:

- Tuotteet (Supply Chain Managementista Salesiin) - suora
- Tilit (Salesista Supply Chain Managementiin) - Suora (jos käytössä)
- Yhteyshenkilöistä asiakkaisiin (Salesista Supply Chain Managementiin) - Suora (jos käytössä)

## <a name="entity-set"></a>Yksikköjoukko

| Toimitusketjun hallinta  | Myynti             |
|-------------------------|-------------------|
| Dataversen myyntitilauksen otsikot | SalesOrders       |
| Dataversen myyntitilausrivit   | SalesOrderDetails |

## <a name="entity-flow"></a>Yksikön työnkulku

Myyntitilaukset luodaan Salesissa ja ne synkronoidaan Supply Chain Managementiin, kun **Suorita projekti** käynnistetään projektille, joka perustuu **Myyntitilaukset (Salesista Supply Chain Managementiin) - suora** -malliin. Voit aktivoida ja synkronoida myyntitilaukset Salesista vain, jos **tilaustuotteet** koostuvat vain ulkoisesti ylläpidetyistä tuotteista. Tämän vuoksi käsin lisättyjä tuotteita ei voi olla. Kun tilaus on aktivoitu, myyntitilaus määritetään vain luku -tilaan käyttöliittymässä. Tässä vaiheessa päivitykset tehdään Supply Chain Managementissa. Kun myyntitilauksen tila on **Vahvistettu**, **Myyntitilaukset (Supply Chain Managementista Salesiin) - suora** -malliin perustuvaa projektia voi käyttää Supply Chain Managementista Salesiin tapahtuvien päivitysten tai toimitusten tilojen synkronoinnissa.

Sinun ei tarvitse luoda tilauksia Sales-sovelluksessa. Sen sijaan voit luoda uusia myyntitilauksia Supply Chain Managementissa. Kun myyntitilauksen tilaksi on määritetty **Vahvista**, se synkronoidaan Salesiin edellisessä kappaleessa kuvatulla tavalla.

Supply Chain Managementin mallin suodattimet auttavat varmistamaan, että synkronointiin sisällytetään vain halutut myyntitilaukset.

- Sekä myyntitilauksen tilaava asiakas että laskutusasiakas on saatava Sales-sovelluksesta, jotta nämä tiedot sisällytetään synkronointiin. Supply Chain Managementin **OrderingCustomerIsExternallyMaintained**- ja **InvoiceCustomerIsExternallyMaintained**-sarakkeita käytetään myyntitilausten suodattamiseen tietotaulukoista.
- Myyntitilaus on vahvistettava Supply Chain Managementissa. Salesiin synkronoidaan vain vahvistetut myyntitilaukset tai myyntitilaukset joilla on ylempi käsittelytila, kuten **Lähetetty** tai **Laskutettu**.
- Kun myyntitilaus on luotu tai kun sitä on muokattu, **Laske kokonaismyynti** -eräajo on suoritettava Supply Chain Managementissa. Salesiin synkronoidaan vain myyntitilaukset, joiden loppusummat on laskettu.

## <a name="freight-tax"></a>Rahdin verot

Sales ei tue veroa otsikkotasolla, koska verot tallennetaan rivitasolle. Kun Supply Chain Managementin otsikkotason veroja, kuten rahdin veroja, halutaan tukea, järjestelmä synkronoi verot Salesiin käsin lisättynä tuotteena, jonka nimi on **Rahdin vero**. Se synkronoi myös Supply Chain Managementista verosumman. Näin Salesin vakiohinnan laskentaa voidaan käyttää kokonaissummissa, vaikka Supply Chain Managementissa olisi käytössä otsikkotason vero.

## <a name="discount-calculation-and-rounding"></a>Alennuksen laskeminen ja pyöristäminen

Salesin alennuksen laskentamalli on erilainen kuin Supply Chain Managementin alennuksen laskentamalli. Supply Chain Managementissa myyntirivin lopullinen alennussumma voi olla alennussummien ja alennusprosenttien yhdistelmän tulos. Jos tämä lopullinen alennussumma jaetaan rivin määrällä, tulos saatetaan pyöristää. Pyöristystä ei kuitenkaan tehdä, jos pyöristetty yksikkökohtainen alennussumma synkronoidaan Salesiin. Voit varmistaa, että Supply Chain Management -myyntirivin koko alennussumma synkronoidaan oikein Salesiin, kun koko summa synkronoidaan ilman, että sitä jaetaan rivimäärällä. Tämän vuoksi Salesin **Alennuksen laskutapa** -kohdan arvoksi on määritettävä **Rivinimike**.

Kun myyntitilausrivi synkronoidaan Salesista Supply Chain Managementiin, käytetään koko rivin alennussummaa. Koska Supply Chain Managementissa ei ole kenttää, johon rivin koko alennussumman voisi tallentaa, summa jaetaan määrällä ja tallennetaan **Rivialennus**-kenttään. Tässä jaossa tapahtuva mahdollinen pyöristys tallennetaan myyntirivin **Myynnin kulut** -kenttään.

### <a name="example"></a>Esimerkki

**Synkronointi Salesista Supply Chain Managementiin**

- **Sales:** Määrä = 3, rivikohtainen alennus = 10,00 $
- **Supply Chain Management:** Määrä = 3, rivin alennussumma = $3,33, myynnin kulut = -$0,01 

**Synkronointi Supply Chain Managementista Salesiin**

- **Supply Chain Management:** Määrä = 3, rivin alennussumma = $3,33, myynnin kulut = -$0,01
- **Sales:** Määrä = 3, rivikohtainen alennus = (3 × 3,33 $) + 0,01 $ = 10,00 $

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

**Tilaus**-taulukkoon on lisätty uusia sarakkeita, jotka näkyvät sivulla:

- **Ulkoisesti ylläpidetty** – Määritä tämän vaihtoehdon arvoksi **Kyllä**, kun tilaus on peräisin Supply Chain Managementista.
- **Käsittelytila** – Tämä sarake näyttää tilauksen käsittelyn tilan Supply Chain Managementissa. Käytettävissä ovat seuraavat arvot:

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

**Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -asetusta käytetään tilauksen aktivoinnin aikana. Sen avulla seurataan johdonmukaisesti, koostuuko myyntitilaus kokonaan ulkoisesti ylläpidetyistä tuotteista. Jos myyntitilauksessa on vain ulkoisesti ylläpidettyjä tuotteita, tuotteita ylläpidetään Supply Chain Managementissa. Tämä asetus auttaa varmistamaan, ettet aktivoi ja yritä synkronoida sellaisia myyntitilausrivejä, joissa on tuotteita, joita Supply Chain Management ei tunne.

**Myyntitilaus**-sivun **Luo lasku**, **Peruuta tilaus**, **Laske uudelleen**, **Hae tuotteet** ja **Hae osoite** -painikkeet on piilotettu ulkoisesti ylläpidetyissä tilauksissa, koska laskut luodaan Supply Chain Managementissa, josta ne synkronoidaan Salesiin. Näitä tilauksia ei voi muokata, sillä myyntitilaustiedot synkronoidaan Supply Chain Managementista aktivoinnin jälkeen.

Myyntitilauksen tila pysyy **aktiivisena**, jotta muutokset Supply Chain Managementista siirtyvät Salesin myyntitilaukseen. Voit ohjata tätä toimintaa määrittämällä **Tilakoodi \[tila\]**-arvoksi **Aktiivinen** tietojen integrointiprojektissa.

## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

Seuraavat asetukset tulee päivittää järjestelmissä ennen myyntitilausten synkronointia.

### <a name="setup-in-sales"></a>Asetukset Salesissa

- Varmista, että sen käyttäjän ryhmän käyttöoikeudet on määritetty, jolle Salesissa asetettu yhteys on määritetty. Jos käytät esittelytietoja, käyttäjällä on usein järjestelmänvalvojan käyttöoikeudet, mutta ryhmällä ei. Jos ryhmällä ei ole järjestelmänvalvojan käyttöoikeuksia, kun suoritat projektin tietojen integrointiohjelmasta, saat virheilmoituksen, jossa kerrotaan ensisijaisen ryhmän puuttumisesta.

    Siirry kohtaan **Asetukset** &gt; **Suojaus** &gt; **Ryhmät** ja valitse haluamasi ryhmä. Valitse **Roolien hallinta** ja valitse sitten halutut käyttöoikeudet, kuten **järjestelmänvalvoja**.

- Voit varmistaa alennusten oikean laskennan sekä Salesissa että Supply Chain Managementissa valitsemalla **Alennuksen laskentatapa** -asetukseksi **Rivinimike**.
- Siirry kohtaan **Asetukset** &gt; **Hallinto** &gt; **Järjestelmäasetukset** &gt; **Sales** ja varmista, että käytössä ovat seuraavat asetukset:

    - **Käytä järjestelmän hinnanlaskentajärjestelmää** -asetuksen arvoksi on määritetty **Kyllä**.
    - **Alennuksen laskutapa** -sarakkeen arvoksi on määritetty **Rivinimike**.

### <a name="setup-in-supply-chain-management"></a>Määritys Supply Chain Managementissa

- Siirry kohtaan **Myynti ja markkinointi** &gt; **Kausittaiset tehtävät** &gt; **Laske kokonaismyynti**. Määritä sitten erätyönä suoritettava työ. Määritä **Laske myyntitilausten loppusummat** -vaihtoehdon arvoksi **Kyllä**. Tämä vaihe on tärkeä, koska Salesiin synkronoidaan vain myyntitilaukset, joiden loppusummat on laskettu. Erätyön toistovälin tulisi olla sama kuin myyntitilausten synkronoinnin toistoväli.

Jos käytät myös työtilausten integrointia, sinun on määritettävä myynnin alkuperä. Myynnin alkuperän avulla Field Servicen työtilauksista luodut myyntitilaukset voidaan erottaa Supply Chain Managementissa. Kun myyntitilauksen myynnin alkuperätyyppi on **Työtilauksen integrointi**, myyntitilauksen ylätunnisteessa on **Ulkoisen työtilauksen tila** -kenttä. Myynnin alkuperä varmistaa, että Field Servicen työtilauksista luodut myyntitilaukset suodatetaan pois synkronoitaessa myyntitilausta Supply Chain Managementista Field Serviceen.

1. Valitse **Myynti ja markkinointi** \> **Asetukset** \> **Myyntitilaukset** \> **Myynnin alkuperä**.
2. Luo uusi myynnin alkuperä valitsemalla **Uusi**.
3. Anna **Myynnin alkuperä** -sarakkeessa myynnin alkuperän nimi, kuten **SalesOrder**.
4. Anna **Kuvaus**-sarakkeessa kuvaus, kuten **Myyntitilaus Salesista**.
5. Valitse **Alkuperän tyypin määritys** -valintaruutu.
6. Valitse **Myynnin alkuperän tyyppi** -sarakkeessa **Myyntitilauksen integrointi**.
7. Valitse **Tallenna**.

### <a name="setup-in-the-sales-orders-sales-to-supply-chain-management---direct-data-integration-project"></a>Myyntitilaukset (Salesista Supply Chain Managementiin) - suora -integrointiprojektin asetukset

- Varmista, että **Shipto\_country**- ja **DeliveryAddressCountryRegionISOCode**-kohdan välinen yhdistämismääritys on tehty. Voit määrittää arvomäärityksessä tyhjän oletusarvon, jos haluat välttää maan syöttämisen kansallisissa tilauksissa. Jätä vasen puoli tyhjäksi ja määritä oikean puolen arvoksi haluamasi maa tai alue.

    Malliarvo on arvomääritys, jossa on yhdistetty useita maita tai alueita. Jos kohta jätetään tyhjäksi, arvo on US.

### <a name="setup-in-the-sales-orders-supply-chain-management-to-sales---direct-data-integration-project"></a>Myyntitilaukset (Supply Chain Managementista Salesiin) - suora -integrointiprojektin asetukset

#### <a name="salesheader-task"></a>SalesHeader -tehtävä

- Hinnasto on pakollinen Salesissa, jotta tilauksia voidaan luoda. Päivitä **pricelevelid.name \[hinnaston nimi\]**-kohdan arvomääritykseksi Salesissa käytettävä hinnasto. Yhdelle valuutalle voit käyttää oletushinnastoa. Vaihtoehtoisesti voit käyttää arvomääritystä, jos hinnastossa on useita valuuttoja.

    **pricelevelid.name \[hinnaston nimi\]** -kohdan oletusmallin arvo on **CRM Service USA (esimerkki)**.

#### <a name="salesline-task"></a>SalesLine -tehtävä

- Varmista, että Supply Chain Managementin **SalesUnitSymbol**-kohdassa on vaadittu arvomääritys.
- Varmista, että Salesissa on määritetty pakolliset yksiköt.

    **SalesUnitSymbol**-kohdan malliarvoksi, jolla on arvomääritys, on määritetty **oumid.name**.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

> [!NOTE]
> **Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-sarakkeet eivät sisälly oletusarvoisiin yhdistämismäärityksiin. Näiden sarakkeiden määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä taulukko synkronoidaan.

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

> [!NOTE]
> Yhdistämismääritys osoittaa, minkä sarakkeen tiedot synkronoidaan Salesista Supply Chain Managementiin tai Supply Chain Managementista Salesiin.

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderheader"></a>Myyntitilaukset (Supply Chain Managementista Salesiin) - suora: OrderHeader

[![Myyntitilausten tietojen integroinnin mallin yhdistämismääritys (Supply Chain Managementista Salesiin) – suora: OrderHeader](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderline"></a>Myyntitilaukset (Supply Chain Managementista Salesiin) - suora: OrderLine

[![Myyntitilausten tietojen integroinnin mallin yhdistämismääritys (Supply Chain Managementista Salesiin) – suora: OrderLine](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderheader"></a>Myyntitilaukset (Salesista Supply Chain Managementiin) - suora: OrderHeader

[![Myyntitilausten tietojen integroinnin mallin yhdistämismääritys (Salesista Supply Chain Managementiin) – suora: OrderHeader](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderline"></a>Myyntitilaukset (Salesista Supply Chain Managementiin) - suora: OrderLine

[![Myyntitilausten tietojen integroinnin mallin yhdistämismääritys (Salesista Supply Chain Managementiin) – suora: OrderLine](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-articles"></a>Liittyvät artikkelit

[Prospektista käteiseksi](prospect-to-cash.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]