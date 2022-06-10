---
title: Epäsuoran kustannuksen kirjaus
description: Tässä aiheessa kerrotaan, miten epäsuoria kustannuksia kirjataan, luodaan kustannusryhmiä ja lisätään epäsuorien kustannusten kustannuslaskentalomakkeeseen solmuja.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CostSheetDesigner, BOMCostGroup, ProjCategory, CostingVersion, CostSheetCalculationFactor
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: d7f4753f69d83d172993e1c9b04be2220fdf253f
ms.sourcegitcommit: 1ea145dc606e243c7f51d91a5c0dd9e385bbda4a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/25/2022
ms.locfileid: "8804622"
---
# <a name="indirect-cost-posting"></a>Epäsuoran kustannuksen kirjaus

Epäsuorat kustannukset ovat kustannuksia, jotka eivät liity suoraan mihinkään tuotantoprosessin yksittäiseen toimintoon. Esimerkkejä tällaisista kustannuksista ovat esimerkiksi työntekijöiden palkat, kirjanpito-osastojen kustannukset ja yleiskustannukset, kuten vuokra, sähkö ja konekustannukset.

## <a name="calculating-indirect-costs"></a>Välillisten kustannusten laskenta

Microsoft Dynamics 365 Financessa ei voi laskea automaattisesti epäsuorien kustannusten hintaa. Sinun on määritettävä epäsuorat kustannukset, luotava epäsuorat kustannuskoodit ja ylläpidettävä kunkin epäsuoran kustannuksen hintaa kustannuslaskentalomakkeessa.

Epäsuorien kustannusten laskennassa käytettävä tarkka prosessi voi hieman vaihdella yrityksen mukaan. Yleisesti ottaen prosessi koostuu seuraavista perusvaiheista:

1. Luo epäsuorien kustannusten luettelo, jotka tunnistetaan tuotannossa. Luettelossa voi olla esimerkiksi vuokra-, hallintokuluja, kirjanpitomaksuja ja lakisääteisiä maksuja. Se ei saa sisältää tuotantoreitityksille kirjattuja raaka-ainekustannuksia tai työkustannuksia.
2. Laske kaikkien epäsuorien kustannusten summa. Voit ryhmitellä samantyyppisiä epäsuoria kustannuksia tai pitää ne erillään toisistaan. Jokaisella konfiguroidulla välillisellä kustannuksella voi olla eri päätili, jota käytetään kirjattaessa kirjanpitoon.
3. Vertaa epäsuoria kustannuksia kertoimeen, jota kutsutaan myös kustannusperusteeksi. Kerroin voi olla mikä tahansa. Joitakin yleisiä esimerkkejä:

    - Myyntituotto
    - Tuotettava kokonaismäärä
    - Asetusaika
    - Ajoaika

    Voit valita kauden, jota varten epäsuorat kustannukset lasketaan. Näitä kausia ovat esimerkiksi kuukausi, neljännesvuosi tai vuosi. Epäsuorien kustannusten summan ja kerroinsumman summan tulisi olla yhtä pitkän ajanjakson summa. Epäsuorien kustannusten hinnan laskemiseen käytetään seuraavaa kaavaa:

    *Epäsuoran kustannuksen hinta*  =  *Epäsuoran kustannuksen kokonaiskustannukset* &divide; *Kokonaiskerroin*

4. Epäsuorien kustannusryhmien luonti.
5. Määritä kustannuslaskentalomakkeeseen hintasi.
6. Ylläpidä epäsuorien kustannusten kustannusta kustannuslaskelmaversiossa.

> [!NOTE]
> **Kustannuslaskenta**-moduulin avulla voit kerryttää kustannuksia ja määrittää yleiskustannukset eri lähteistä, kuten tuotannosta, projekteista ja kirjanpidosta. Lisätietoja on kohdassa [Kustannuslaskenta](/cost-accounting/cost-accounting-home-page.md).

> [!IMPORTANT]
> Eri sääntelyviranomaiset ovat julkaisseet ohjeita kustannustyypeistä, jotka voidaan sisällyttää epäsuorina kustannuksina tai valmiiden tuotteiden yleiskustannuksina. Ennen epäsuorien kustannusten konfigurointia on suositeltavaa tarkistaa kirjanpitäjältäsi ja paikallisilta määräyksiltä, että toimit vaatimusten mukaan.

## <a name="create-cost-groups-for-indirect-costs"></a>Epäsuorien kustannusten kustannusryhmien luonti

Epäsuorille kustannuksille on luotava vähintään yksi kustannusryhmä. Käytettävissä olevien kustannusryhmien määrää ei ole rajoitettu. Mieti, kuinka kustannukset lasketaan ja onko erityyppisille kustannuksille eri hinnat. Organisaatiossasi voidaan esimerkiksi valmistaa elintarviketuotteita. Jotkin raaka-aineet ja valmiit tavarat ovat kuivatavaroita, ja niiden yksi epäsuora kustannus on varastoinnille. Jotkin raaka-aineet ja valmiit tavarat on säilytettävä jäähdytettynä, joten niiden epäsuorat kustannukset ovat suuremmat. Tässä tapauksessa kannattaa luoda kaksi kustannusryhmää, jotka ovat **kuivamateriaalin yleiskustannukset** ja **jäähdytetyn materiaalin yleiskustannukset**.

Voit luoda kustannusryhmän epäsuorille kustannuksille noudattamalla seuraavia ohjeita.

1. Valitse **Tuotannonhallinta &gt; Asetukset &gt; Reitit &gt; Kustannusryhmät**.
2. Luo ryhmä valitsemalla **Uusi**.
3. Kirjoita **Kustannusryhmä**-kenttään kustannusryhmän yksilöllinen nimi, esimerkiksi **MATOVH**.
4. Kirjoita **Nimi**-kenttään kustannusryhmän kuvaus, esimerkiksi **Materiaalin yleiskustannus**.
5. Valitse **Kustannusryhmän tyyppi** -kentässä **Välillinen**.
6. Valinnainen: Valitse **Toimintatapa**-kentästä **Kiinteä kustannus** tai **Muuttuva kustannus**.

## <a name="configure-the-costing-sheet-for-indirect-costs"></a>Epäsuorien kustannusten kustannuslaskentalomakkeen konfiguroiminen

Kun olet luonut yhden kustannusryhmän tai useita kustannusryhmiä, voit konfiguroida kustannuslaskentalomakkeen epäsuorien kustannusten avulla ja määrittää laskelman. Voit ryhmitellä epäsuorat kustannukset kustannuslaskentalomakkeeseen. Voit ryhmitellä epäsuorat kustannukset luomalla valinnaisen otsikon kustannuslaskentalomakkeeseen. Kustannuslaskentalomakkeen kullekin kustannusryhmälle on luotava vähintään yksi solmu. Voit lisätä lisää epäsuorien kustannusten laskelmia kullekin epäsuorien kustannusten kustannusryhmälle.

### <a name="indirect-cost-node-types"></a>Epäsuorien kustannusten solmujen tyypit

Tässä osassa kuvataan epäsuorien kustannusten erityyppisiä solmuja.

#### <a name="surcharge"></a>Lisämaksu

**Lisämaksu** on yksi yleisimpiä epäsuorien kustannusten tyyppejä. Se laskee prosenttiosuuden kustannuksista tuotantotilauksen kustannusten kustannusperusteesta. Voit määrittää kustannusperusteen valitsemalla kustannuslaskentalomakkeessa materiaali- tai aikakomponentteihin linkitetyt kustannusryhmät.

Esimerkiksi 3 prosentin lisämaksu voidaan lisätä tuotantotilauksen kaikkien raaka-aineiden tuotantokustannuksiin.

#### <a name="rate"></a>Taso

**Hinta**-tyyppistä epäsuoraa kustannusta käytetään, kun tuotantotilauksen kustannusperusteesta voidaan lisätä kiinteä kustannus tuotantotilaukseen. Hinta voi perustua yhteen kolmesta alatyypistä:

- **Prosessi**: Hinta perustuu reitityksen ajoaikaan.
- **Määritys**: Hinta perustuu reitityksen määritysaikaan.
- **Määrä**: Hinta perustuu tuotettavaan määrään.

Voit määrittää kustannusperusteen valitsemalla kustannuslaskentalomakkeessa materiaali- tai aikakomponentteihin linkitetyt kustannusryhmät.

Kuhunkin tuotantotilaukseen lisätään esimerkiksi 2,00 Yhdysvaltain dollarin (USD) kiinteä summa, joka perustuu kustannuslaskentalomakkeen työkustannusryhmän reitin suoritusaikaan.

#### <a name="output-unit-based"></a>Tulostusyksikköperusteinen

**Tulostusyksikköperusteinen**-tyypin epäsuora kustannus lasketaan kertomalla kustannuslaskentalomakkeen **Hinta**-pikavälilehdessä määritetty summa valitulla alityypillä. Voit valita valmiin tuotteen määrän, painon tai tilavuuden epäsuorien kustannusten kertoimeksi.

Määrän avulla voit esimerkiksi laskea kullekin tuotantomäärälle 1,50 USD koneen vanhentumisesta. Toisena esimerkkinä voit laskea tilavuuden avulla 2,00 USD jäähdytyskustannuksia tilalle, jonka valmiit tavarat tarvitsevat jäähdytysyksiköissä.

#### <a name="input-unit-based"></a>Syöttöyksikköperusteinen

**Syöttöyksikköperusteinen** -tyypin epäsuora kustannus lasketaan kertomalla tuotantotilauksessa kulutettu raaka-aineiden määrä tilauksen määrällä. Voit käyttää tuotantotilauksen syötteiden painoa tai tilavuutta kokonaissumman laskemiseen. Voit rajoittaa laskennan materiaalien osajoukkoon valitsemalla yhden tai useamman kustannusryhmän kustannuslaskentalomakkeen **Kustannusperuste**-pikavälilehdessä.

Voit esimerkiksi lisätä tuotantotilauksiin 1,00 USD käyttämällä tiettyä jäähdytettyihin tuotteisiin linkitettyä kustannusryhmää syötteiden tilavuudelle.

### <a name="create-a-total-node-for-indirect-costs-in-the-costing-sheet"></a>Epäsuorien kustannusten kokonaissolmun luominen kustannuslaskentalomakkeessa

Toimi seuraavasti, kun haluat luoda epäsuorien kustannusten kokonaissolmun kustannuslaskentalomakkeeseen.

1. Valitse **Kustannusten hallinta &gt; Välillisten kustannusten kirjanpitokäytäntöjen määrittäminen &gt; Kustannuslaskentalomake**.
2. Valitse puusta solmu, joka vastaa valmistettujen tuotteiden kustannuksia.
3. Luo solmu valitsemalla **Uusi**.
4. Valitse **Valitse solmutyyppi** -kentästä **Yhteensä**.
5. Kirjoita **Koodi**-kenttään solmun yksilöivä tunnus, kuten **Tuotannon yleiskustannukset**.
6. Valitse **Otsikko**-valintaruutu.
7. Valitse **Yhteensä**-valintaruutu.
8. Valitse **OK**.

### <a name="create-an-indirect-cost-group-node-in-the-costing-sheet"></a>Epäsuorien kustannusten ryhmän solmun luominen kustannuslaskentalomakkeessa

Toimi seuraavasti, kun haluat luoda epäsuorien kustannusten ryhmän solmun kustannuslaskentalomakkeeseen.

1. Valitse **Kustannusten hallinta &gt; Välillisten kustannusten kirjanpitokäytäntöjen määrittäminen &gt; Kustannuslaskentalomake**.
2. Valitse puusta solmu, jonka alle haluat luoda epäsuoran kustannuksen. Valitse esimerkiksi **Tuotannon yleiskustannukset** -solmun Yhteensä-solmu.
3. Luo solmu valitsemalla **Uusi**.
4. Valitse **Valitse solmutyyppi** -kentässä **Kustannusryhmä**.
5. Kirjoita **Koodi**-kenttään solmun yksilöivä tunnus, kuten **TRANSP**.
6. Kirjoita **Kuvaus**-kenttään lyhyt kuvaus, kuten **Kuljetuksen yleiskustannukset**.
7. Valitse **OK**.
8. Valitse **Kustannusryhmä**-kentästä kustannusryhmä, esimerkiksi **OVH1: Kuljetuksen yleiskustannukset**.

### <a name="create-a-surcharge-indirect-cost"></a>Lisämaksujen epäsuorien kustannusten luominen

Toimi seuraavasti, kun haluat luoda lisämaksujen epäsuorien kustannuksen kustannuslaskentalomakkeeseen.

1. Valitse **Kustannusten hallinta &gt; Välillisten kustannusten kirjanpitokäytäntöjen määrittäminen &gt; Kustannuslaskentalomake**.
2. Valitse puusta epäsuoran kustannuksen ryhmän solmu, jonka alle haluat luoda epäsuoran kustannuksen. Valitse esimerkiksi **TRANSP – Kuljetuksen yleiskustannukset** -solmun Yhteensä-solmu.
3. Luo solmu valitsemalla **Uusi**.
4. Valitse **Valitse solmutyyppi** -kentästä **Lisämaksu**.
5. Kirjoita **Koodi**-kenttään solmun yksilöivä tunnus, kuten **Kuljetuksen lisämaksut**.
6. Valitse **OK**.
7. Valitse **Alityyppi**-kentässä **Yhteensä**.
8. Luo kustannuskoodi valitsemalla **Kustannusperuste**-pikavälilehdessä **Uusi**.
9. Valitse **Koodi**-kentästä lisämaksun laskennassa käytettävä kustannusryhmä.
10. Valinnainen: Toista vaiheet 8 - 9 jokaiselle lisättävälle kustannusryhmälle, jota haluat käyttää laskennassa.
11. Luo hinta valitsemalla **Lisämaksu**-pikavälilehdellä **Uusi**.
12. Valitse **Versio**-kentästä kustannuslaskelmaversio, johon lisämaksu lisätään.
13. Valinnainen: Syötä **Toimipaikka**-kenttään toimipaikka, jossa lisämaksua käytetään.
14. Lisää **Prosentti**-kenttään prosenttiosuus, joka lasketaan tuotantotilauksille **Kustannusperuste**-pikavälilehdessä määritetyistä kustannusryhmistä.
15. Valitse **Kirjanpidon kirjaukset** -pikavälilehdessä päätili, jota käytetään seuraaville kentille: **Absorboituneet arvioidut välilliset kustannukset**, **Arvioidut kulutetut välilliset kustannukset, KET**, **Absorboituneet välilliset kustannukset** ja **Epäsuorien toimintojen kustannukset, KET**.
16. Valinnainen: Määritä **Taloushallinnon dimensiot** -pikavälilehdessä taloushallinnon dimensiot, joita käytetään oletusarvon mukaan tapahtumissa kirjattaessa kirjanpitoon.

Edellisten vaiheiden avulla voit luoda **Lisämaksu**-tyyppisen epäsuoran kustannuksen. Samanlaisilla vaiheilla luodaan muuntyyppisiä epäsuoria kustannuksia. Seuraavissa osissa kuvataan kunkin tyypin erot.

#### <a name="rate"></a>Taso

- Valitse vaiheessa 4 **Lisämaksun** asemesta **Hinta**.
- Valitse vaiheessa 7 **Yhteensä**-kentän sijaan **Prosessi**, **Määritys** tai **Määrä**.
- Käytä vaiheessa 11 **Lisämaksu**-pikavälilehden asemesta **Hinta**-pikavälilehteä.
- Kirjoita vaiheessa 14 **Summa**-kenttään summa **Prosentti**-kentän prosenttiosuuden asemesta.

#### <a name="output-unit-based"></a>Tulostusyksikköperusteinen

- Valitse vaiheessa 4 **Lisämaksun** asemesta **Tulostusyksikköperusteinen**.
- Valitse vaiheessa 7 **Yhteensä**-kentän sijaan **Määrä**, **Paino** tai **Tilavuus**.
- Ohita vaiheet 8 – 10.
- Käytä vaiheessa 11 **Lisämaksu**-pikavälilehden asemesta **Hinta**-pikavälilehteä.

#### <a name="input-unit-based"></a>Syöttöyksikköperusteinen

- Valitse vaiheessa 4 **Lisämaksun** asemesta **Syöttöyksikköperusteinen**.
- Valitse vaiheessa 7 **Yhteensä**-kentän sijaan **Paino** tai **Tilavuus**.
- Käytä vaiheessa 11 **Lisämaksu**-pikavälilehden asemesta **Hinta**-pikavälilehteä.
