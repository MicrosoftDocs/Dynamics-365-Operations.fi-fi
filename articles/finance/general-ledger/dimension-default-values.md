---
title: Talouskirjauskansioiden taloushallinnon oletusdimensiot
description: Tässä artikkelissa kuvataan sääntöjä, jotka määrittävät, miten taloushallinnon dimensioarvot määritetään talouskirjauskansioissa syötettyihin tapahtumiin. Se sisältää myös tietoja skenaarioista, joissa käytetään kiinteitä dimensioita.
author: kweekley
ms.date: 09/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransDaily, LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d0fcf836e22207baae562801fb082d735df0f96
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907919"
---
# <a name="default-financial-dimensions-on-financial-journals"></a>Talouskirjauskansioiden taloushallinnon oletusdimensiot

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan sääntöjä, jotka määrittävät, miten taloushallinnon dimensioarvot määritetään talouskirjauskansioissa (mutta ei varasto- tai projektikirjauskansioissa) syötettyihin tapahtumiin. Se sisältää myös tietoja skenaarioista, joissa käytetään kiinteitä dimensioita.

## <a name="symptom"></a>Oire

Taloushallinnon dimensioarvoja ei ole määritetty odotetulla tavalla tilin tai vastatilin osalta talouskirjauskansiossa. Seuraavissa skenaarioissa esitellään kaksi esimerkkiä:

Tosite lisätään kirjauskansioon yleisessä kirjauskansiossa. Tilinä on toimittajatili, ja vastatilinä on pankkitili. Toimittajan taloushallinnon dimensiot syötetään oletusarvoisesti tilille, mutta pankin taloushallinnon dimensioita ei syötetä oletusarvoisesti vastatilille. Sen sijaan tilin dimensioarvot syötetään oletusarvoisesti vastatilille.

Asiakkaalle on määritetty taloushallinnon dimension oletusarvot, ja osaston taloushallinnon dimensiolle on määritetty kiinteä dimensioarvo tuoton päätilillä. Tosite lisätään yleiseen kirjauskansioon.  Tilinä on asiakas, ja vastatilinä on kirjanpitotili, erityisesti tuottotili, jolla on kiinteä dimensioarvo. Kiinteää dimensiota ei ole määritetty tuoton päätilin vastatilille. Sen sijaan arvoksi määritetään asiakkaalta tullut tilin osastodimensioarvo.  Tositteen kirjaamisen jälkeen kiinteää dimensioarvoa käytetään kirjatussa kirjanpitomerkinnässä, mutta tositteessa näkyy edelleen asiakkaan osastoarvo tuottotilillä. 

Mitä sääntöjä noudatetaan taloushallinnon dimensioarvoissa, jotka on määritetty kirjauskansion tositteille?

## <a name="resolution"></a>Ratkaisu

Seuraavia sääntöjä noudatetaan, kun taloushallinnon dimensioarvoja syötetään oletusarvoisesti talouskirjauskansioiden, kuten yleisen kirjauskansion tai toimittajalaskukirjauskansion, tositteen riveille. 

1. **Kirjauskansion otsikko**

   - Kirjauskansion otsikon dimensiot syötetään oletusarvoisesti kirjauskansion nimidimensioista.

2. **Kirjauskansiorivin tili**

   - Kirjauskansiorivin tilin dimensiot syötetään oletusarvoisesti kirjauskansion otsikon dimensioista.
   - Jos taloushallinnon dimensio on tyhjä, sen arvo syötetään oletusarvoisesti asiakkaan, toimittajan, pankin, käyttöomaisuuserän, projektin tai kirjanpidon dimensioista.

     - Jos tilityyppinä on **Kirjanpito**, kirjanpitotilin kiinteää dimensiota käsitellään oletusdimensiona tapahtumien kirjauksen aikana.
     - Jos tilityyppinä on **Asiakas**, **Toimittaja**, **Pankki**, **Käyttöomaisuus** tai **Projekti**, päätiliä ei voi vielä määrittää. Sen vuoksi tilille ei koskaan syötetä oletusarvoisesti kiinteää dimensiota.

3. **Kirjauskansiorivin vastatili**

 - Ensin kirjauskansiorivin vastatilin dimensiot syötetään oletusarvoisesti kirjauskansiorivin tilin dimensioista.

 - Jos taloushallinnon dimensio on tyhjä, seuraava oletusarvo syötetään asiakkaan, toimittajan, pankin, käyttöomaisuuserän, projektin tai kirjanpidon oletusdimensioista.
   1. Jos vastatilityyppinä on **Kirjanpito**, kirjanpitotilin kiinteää dimensiota käsitellään oletusdimensiona tapahtumien kirjauksen aikana. Jos tilistä on jo syötetty dimensioarvo oletusarvoisesti, päätilin oletusdimensioarvo tai kiinteä dimensioarvo ei ohita olemassa olevaa arvoa.
   2. Jos vastatilin tyyppinä on **Asiakas**, **Toimittaja**, **Pankki**, **Käyttöomaisuus** tai **Projekti**, päätiliä ei vielä tiedetä, joten kiinteä dimensio ei ole koskaan vastatilin oletusarvona.

4. **Kirjaus**

    1. Kirjauksen aikana jokaisen kirjanpitotapahtuman rivin (sekä tilin että vastatilin) päätili arvioidaan sen mukaan, onko kiinteä dimensioarvo olemassa. Jos kiinteä dimensio on määritetty, olemassa olevat tai tyhjät arvot korvataan kiinteällä dimensioarvolla.

        Kiinteä dimensioarvo **ei** näy kirjauskansion riveillä kirjauksen jälkeen. Se näkyy sen sijaan kirjanpitomerkinnässä, kun tositetta tarkastellaan sen kirjaamisen jälkeen.

    2. Kirjauksen aikana ei lisätä muita dimensioarvoja, mukaan lukien kirjauksen aikana lisättävät kirjanpitotilit, kuten pyöristystilit ja konsernin sisäiset erääntymiskohteen ja -lähteen tilit. Lisäkirjanpitotilien oletusdimensiomerkinnät ovat peräisin tili- tai vastatileistä.

Kun dimensioarvoja syötetään oletusarvoisesti, kirjauskansion oletusprosessi ei voi määrittää, onko tyhjä dimensioarvo jätetty tarkoituksella tyhjäksi vai eikö oletusmerkintää tehty. Jos dimensioarvo jätetään tarkoituksella tyhjäksi, arvo voidaan silti syöttää oletusarvoisesti käyttämällä aiemmin kuvattua oletusjärjestystä. Jos haluat, että dimensioarvo on tyhjä, sinun on ehkä luotava dimensio, jonka arvo on **0** (nolla) tai **Tyhjä**, jotta sitä voidaan käyttää tyhjän dimension tilalla.

Seuraavissa skenaarioissa on esimerkkejä taloushallinnon dimension oletusjärjestyksen käytöstä.

### <a name="scenario-1"></a>Skenaario 1

Valitse **Kirjanpito \> Kirjauskansion määrittäminen \> Kirjauskansioiden nimet** ja valitse kirjauskansion nimeksi **GenJrn**. Määritä sitten **Taloushallinnon dimensiot** -pikavälilehdessä seuraavat taloushallinnon oletusdimensioiden arvot:

- **BUSINESSUNIT:** 001
- **DEPARTMENT:** 024

[![Kirjauskansioiden nimet -sivu](./media/financial-dimension-defaulting-jrnl-names-01.png)](./media/financial-dimension-defaulting-jrnl-names-01.png)

Valitse **Kirjanpito \> Kirjauskansioviennit \> Yleinen kirjauskansio** ja luo uusi yleinen kirjauskansio, jonka nimenä on **GenJrn**. Dimensiot syötetään oletusarvoisesti kirjauskansion nimestä (LedgerJournalName-taulu) kirjauskansion otsikkoon (LedgerJournalTable-taulu) **Taloushallinnon dimensiot** -välilehden mukaisesti.

[![Taloushallinnon dimensiot -välilehti Yleiset kirjauskansiot -sivulla](./media/financial-dimension-defaulting-genrl-jrnl-02.png)](./media/financial-dimension-defaulting-genrl-jrnl-02.png)

Valitse **Rivit**. Valitse **Tilityyppi**-kentässä **Kirjanpito** ja syötä sitten **Tili**-kenttään **170150**. Siirry sitten pois kentästä valitsemalla **Välilehti**-avain. Dimensiot syötetään oletusarvoisesti kirjauskansion otsikosta. Siksi **tilin** arvona on **170150-001-024**.

[![Yleisen kirjauskansion rivit Kirjaustosite-sivulla](./media/financial-dimension-defaulting-jrnl-vchr-03.png)](./media/financial-dimension-defaulting-jrnl-vchr-03.png)

Muuta **tilin** arvoksi **170150-001-023**. Syötä joko veloitussumma tai hyvityssumma. Valitse **Vastatilityyppi**-kentässä **Kirjanpito** ja syötä sitten **Vastatili**-kenttään **600150**. Dimensioarvot syötetään oletusarvoisesti tililtä. Siksi **vastatilin** arvona on **600150-001-023**.

### <a name="scenario-2"></a>Skenaario 2

Käytä niitä taloushallinnon dimensioita, jotka määritit kirjauskansion nimelle skenaariossa 1. Valitse seuraavaksi **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat** ja määritä taloushallinnon oletusarvot asiakkaalle US-001. Avaa asiakkaan tiedot valitsemalla asiakas. Säilytä **Taloushallinnon dimensiot** -välilehdessä **BUSINESSUNIT**-dimension oletusarvo (**001**). Lisää **COSTCENTER**-dimensio ja syötä arvoksi **007**.

Luo uusi yleinen kirjauskansio, joka käyttää kirjauskansion nimeä **GenJrn**. Muuta **Taloushallinnon dimensiot** -välilehdessä **BUSINESSUNIT**-oletusarvo arvosta **001** arvoon **002**.

Valitse **Rivit**. Valitse **Tilityyppi**-kentässä **Asiakas** ja syötä sitten **Tili**-kenttään **US-001**. Voit tarkastella muiden kuin kirjanpidon tilityyppien taloushallinnon dimensioita valitsemalla **Taloushallinnon dimensiot \> Tili**. Seuraavat taloushallinnon dimensioarvojen oletusarvot syötetään:

- **BUSINESSUNIT:** 002 – Oletusarvo otetaan kirjauskansion otsikosta. Arvoa **001** ei syötetä oletusarvoisesti asiakkaalta US-001, koska oletusarvo on jo syötetty.
- **COSTCENTER:** 007 – Oletusarvo otetaan asiakkaan US-001 määrityksistä.
- **DEPARTMENT:** 024 – Oletusarvo otetaan kirjauskansion otsikosta.

Valitse rivillä **Vastatilityyppi**-kohdassa **Kirjanpito** ja syötä sitten **Vastatili**-kenttään **600150**. Riville syötetään seuraavat taloushallinnon dimensioarvot:

- **BUSINESSUNIT:** 002 – Oletusarvo otetaan tilin taloushallinnon dimensioista. (Se syötettiin alun perin oletusarvoisesti kirjauskansion otsikosta.)
- **DEPARTMENT:** 024 – Oletusarvo otetaan tilin taloushallinnon dimensioista. (Se syötettiin alun perin oletusarvoisesti kirjauskansion otsikosta.)
- **COSTCENTER:** 007 – Oletusarvo otetaan tilin taloushallinnon dimensioista. (Se syötettiin alun perin oletusarvoisesti asiakkaasta.)

### <a name="scenario-3"></a>Skenaario 3

Lisää uusi rivi samaan kirjauskansioon, jota käytit skenaariossa 2. Valitse **Tilityyppi**-kentässä **Kirjanpito** ja syötä sitten **Tili**-kenttään **170150**. Tyhjennä oletusdimensioarvot niin, että jäljellä on vain päätili 170150. Valitse **Vastatilityyppi**-kentässä **Asiakas** ja syötä sitten **Vastatili**-kenttään **US-001**. Seuraavat taloushallinnon dimensioarvojen oletusarvot syötetään:

- **BUSINESSUNIT:** 002 – Oletusarvo otetaan kirjauskansion otsikosta, koska tilin dimensioarvo on tyhjä. Arvoa **001** ei syötetä oletusarvoisesti asiakkaalta US-001, koska oletusarvo on jo otettu kirjauskansion otsikosta. Jos **BUSINESSUNIT**-arvo on jätetty tarkoituksella tyhjäksi, poista myös vastatilin taloushallinnon dimensio.
- **COSTCENTER:** 007 – Oletusarvo otetaan asiakkaalta US-001, koska tilin dimensioarvo ja kirjauskansion otsikon dimensioarvo ovat tyhjiä. Jos **COSTCENTER**-arvo on jätetty tarkoituksella tyhjäksi, poista myös vastatilin taloushallinnon dimensio.
- **DEPARTMENT:** 024 – Oletusarvo otetaan kirjauskansion otsikosta, koska tilin dimensioarvo on tyhjä. Jos **DEPARTMENT**-arvo on jätetty tarkoituksella tyhjäksi, poista myös vastatilin taloushallinnon dimensio.

### <a name="scenario-4"></a>Skenaario 4

Käytä samoja taloushallinnon dimension oletusarvoja, jotka määritit kirjauskansion nimelle ja asiakkaalle skenaarioissa 1 ja 2. Määritä seuraavaksi kiinteä dimensioarvo **BUSINESSUNIT**-dimensiolle päätilillä 170150. Valitse **Kirjanpito \> Tilikartta \> Tilit \> Päätilit**. Valitse **Päätili**-kentässä **170150** ja valitse sitten **Yrityksen ohitukset** -välilehdessä **Lisää**. Valitse yritykseksi **USMF** ja valitse sitten **Lisää**. Valitse tietue ja valitse sitten **Oletusdimensiot**. Muuta **BUSINESSUNIT**-dimensioksi **Kiinteä arvo** ja määritä arvoksi **003**.

Luo uusi yleinen kirjauskansio, joka käyttää kirjauskansion nimeä **GenJrn**. Poista **Taloushallinnon dimensiot** -välilehdestä kaikki oletusdimensioarvot.

Valitse **Rivit**. Valitse **Tilityyppi**-kentässä **Kirjanpito** ja syötä sitten **Tili**-kenttään **170150**. Siirry sitten pois kentästä valitsemalla **Välilehti**-avain. Dimensioarvot syötetään oletusarvoisesti päätilin määrityksistä tilille 170150. Siksi **tilin** arvona on **170150-003-**.

Muuta **tilin** arvoksi **170150-004-**. **Kirjauskansion toiminnot eivät estä kiinteän dimensioarvon muuttamista.** Syötä joko veloitussumma tai hyvityssumma. Valitse **Vastatilityyppi**-kentässä **Kirjanpito** ja syötä sitten **Vastatili**-kenttään **170250**. Taloushallinnon dimensioarvo 004 syötetään oletusarvoisesti tililtä. Kirjaa sitten asiakirja. Valitse kirjauskansiossa **Tosite**. Huomaa, että **BUSINESSUNIT**-arvo palautettiin kirjauksen aikana kiinteään dimensioarvoon **003**.

Kun palaat kirjauskansion tositteeseen, **BUSINESSUNIT**-dimensio **ei** vastaa kiinteää dimensioarvoa. Sillä on aina arvo, joka näkyi näytössä ennen kirjaamista. Kirjausprosessi ei muuta tositteelle syötettyjä arvoja. Ainoastaan kirjanpitomerkintä muuttuu kirjauksen aikana.

## <a name="developer-notes"></a>Huomautukset kehittäjille

Jos olet kehittäjä ja haluat tarkastella oletustoimintoprosessin koodia, tutustu seuraaviin menetelmiin:

- **LedgerJournalEngine.accountModified()** – Tämä menetelmä on pääaloituskohta ensisijaisen tilin dimension oletusprosessille, joka on vakiona kaikille kirjauskansioille (ja jonka jotkin kirjauskansiotyypit ohittavat).
- **LedgerJournalEngine.offsetAccountModified()** – Tämä menetelmä on pääaloituskohta vastatilin dimension oletusprosessille.
