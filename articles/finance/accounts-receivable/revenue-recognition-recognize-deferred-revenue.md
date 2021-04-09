---
title: Siirretyn tuoton kirjaus
description: Tässä ohjeaiheessa annetaan tietoja tuottojen kirjaamisesta tuottokirjaustoiminnon avulla.
author: kweekley
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 8d9b5e1248497ec74e1c7125b2395c0ed4c825c2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820518"
---
# <a name="recognize-deferred-revenue"></a>Siirretyn tuoton kirjaus

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Tuoton kirjaustoimintoa ei voi ottaa käyttöön ominaisuuksien hallinnan avulla. Tällä hetkellä se on otettava käyttöön konfigurointiavainten avulla.

Tässä ohjeaiheessa kuvataan tuottokirjausaikataulun tuottokirjausprosessi. Kun myyntitilauksen lasku on kirjattu, kullekin myyntitilausriville, jolla on tuottoaikataulu, luodaan tuottokirjausaikataulu. Rivin tuottoaikataulua käytetään sen määrittämiseen, siirretäänkö rivin tuotto.

## <a name="view-revenue-recognition-schedule-details"></a>Tuottokirjausaikataulun tietojen tarkasteleminen

Tuottokirjausaikataulun tietoja voidaan tarkastella kahdella tavalla.

- Voit avata tuottokirjausaikataulun suoraan laskutetusta myyntitilauksesta. Tällöin tuottoaikataulun tiedot suodatetaan näyttämään vain valitun myyntitilauksen tiedot. Tämä on hyödyllistä myyntitilauksen aikataulutietojen tarkistamisessa.
- Tuottokirjausaikataulu voidaan avata **Tuottokirjaus \> Kausittaiset tehtävät** -sivulta. Tätä toimintatapaa käytetään usein, kun tuotto kirjataan kauden lopussa. Kun sivu avataan ensimmäistä kertaa, tietoja ei ole näkyvissä. Ruudukon yläpuolella olevilla suodattimilla voidaan määrittää perusteet näytettäville aikataulutiedoille. Laskutuspäivämääriä voidaan suodattaa määrittämällä päivämääräväli, myyntitilaus, asiakas, projektitunnus tai tila.

[![Kuva Tuottoaikataulut-sivusta](./media/revenue-recognition-schedule-page.png)](./media/revenue-recognition-schedule-page.png)

**Taloushallinnon dimensio** -pikavälilehti ruudukon alla avaa myyntitilausrivin taloushallinnon dimensiot. Nämä dimensiot otettiin huomioon kirjauksessa siirrettyyn tuottoon. Ne otetaan huomioon myös tuoton kirjauksessa. Käytettävät dimensioarvot määräytyvät tuotolle määritetyn tilirakenteen ja siirretyn tuoton päätilien mukaan.

## <a name="recognize-revenue"></a>Tuoton kirjaus

Tuotto kirjataan suorittamalla **Tuoton kirjaus** -sivun **Luo kirjauskansio** -prosessi. Tämä sivu voidaan avata joko myyntitilauksesta tai kohdasta **Kausittaiset tehtävät**. Jos prosessi suoritetaan myyntitilauksesta, se kirjaa vain valitun myyntitilauksen tuoton. Yleensä prosessi suoritetaan kohdasta **Kausittaiset tehtävät**, jotta se kirjaa kaikkien kirjattujen myyntitilausten laskujen tuotot.

Tuoton valitsemisen ja kirjauksen perusteet määritetään valitsemalla **Luo kirjauskansio**, jolloin avautuu **Luo kirjauskansio** -valintaruutu.

[![Luo kirjauskansion parametrivaihtoehdot](./media/revenue-recognition-create-journal.png)](./media/revenue-recognition-create-journal.png)

Määritä tuoton kirjauksessa käytettävä kirjauspäivämäärä valintaikkunan **Käsittelypäivämäärä**-kenttäryhmän asetuksilla. Jos valitset **Valittu päivämäärä**, voit syöttää kirjauspäivämäärän **Tapahtuman päivämäärä** -kenttään. Jos valitset **Tuottoaikataulun päivämäärä**, tapahtuman päivämäärää ei käytetä. Kirjauspäivämääränä käytetään sen sijaan kunkin aikataulun rivin **Kirjauspäivämäärä**-kentän arvoa.

Syötä sitten **Tilannepäivämäärä**-kenttään tuottokirjauksen tilannepäivämäärä. Kaikki rivit, joiden kirjauspäivämäärä on tilannepäivämäärä tai edeltää sitä, kirjataan, jos ne eivät ole pidossa.

Kun päivämäärät on määritetty, luo kirjauskansio valitsemalla valintaikkunassa **OK**. Saat ilmoitusviestin, joka sisältää tiedot luotujen tapahtumien määrästä sekä kirjauskansiosta, jossa ne luotiin. Kirjauskansiota ei kirjata automaattisesti. Siten tuottokirjauksen hallinnalla on aikaa tarkistaa, mitkä aikataulun rivit kirjataan.

Kun prosessi on suoritettu, kirjauskansioon siirretyt aikataulun rivit saavat merkinnän **Käsitelty**. **Käsitelty**-merkintä ilmaisee, että rivit on siirretty kirjauskansioon. Ne voivat kuitenkin olla kirjattuja tai kirjaamattomia. Kun tuottokirjauskansio on kirjattu, **Käsitelty**-merkintä säilyy. Jos tuottokirjauskansio poistetaan tai jos rivi poistetaan, **Käsitelty**-merkintä poistetaan. Tällä tavoin rivi voidaan kirjata, kun **Luo kirjauskansio** -prosessi suoritetaan uudelleen.

[![Tuottokirjausaikataulujen sivu](./media/revenue-recognition-rev-recog-schedule-02.png)](./media/revenue-recognition-rev-recog-schedule-02.png)

Avaa **Tuottokirjauskansio**-sivulla (**Tuottokirjaus \> Kirjauskansioviennit \> Tuottokirjauskansio**) kohta **Rivit** tarkastellaksesi tietoja kirjattavista asioista. Kullekin kirjattavan aikataulun riville luodaan erillinen tapahtuma, vaikka rivit kirjattaisiin samana päivänä samoille kirjanpitotileille.

[![Kirjauskansion tositesivu](./media/revenue-recognition-journal-voucher.png)](./media/revenue-recognition-journal-voucher.png)

**Tili**-sarakkeessa näkyy siirretyn tuoton kirjanpitotili. Tätä kirjanpitotiliä ei voi muokata. Tämä rajoitus auttaa takaamaan, että oikea siirretyn tuoton kirjanpitotili vapautetaan. Tätä kirjanpitotiliä tarkisteta tilirakenteeseen verraten, koska se on saattanut muuttua sen jälkeen, kun viitattuun kirjanpitotiliin tehtiin edellinen kirjaus.

**Vastatili**-sarakkeessa näkyy tuoton kirjanpitotili. Oletusarvoisesti tuoton kirjanpitotili perustuu varaston kirjausprofiileihin, ja taloushallinnon dimensiot perustuvat myyntitilausriviin. Tämä kirjanpitotili tarkistetaan verrattuna nykyiseen tilirakenteeseen. Sitä voidaan kuitenkin muokata, jos tilirakenne on muuttunut ja vaatii lisää taloushallinnon dimensioita.

Oletussumma perustuu vastaavalle aikataulun riville, eikä sitä voi muuttaa.

Myyntitilaus on oletusarvoisesti usean valuutan myyntitilaus. Vaihtokurssiksi merkitään laskun vaihtokurssi. Tämä toimintatapa auttaa sen takaamisessa, kirjanpitovaluutan ja raportointivaluutan summat vapautetaan täysin. Pyöristämisen vuoksi aikataulun viimeisen rivin vaihtokurssi voi poiketa hieman laskun kurssista.

Kun tuottokirjauskansio on kirjattu, tosite lisätään aikatauluun. Jos samalle aikatauluriville on useita tositteita, rivi merkitään asteriskilla (\*). Voit tarkastella kaikkia kyseiselle riville kirjattuja tositteita valitsemalla **Tositetapahtumat**.

## <a name="modify-the-revenue-recognition-schedule-details"></a>Tuottokirjausaikataulun tietojen muokkaaminen

Suurinta osaa tuottoaikataulun tiedoista ei voi muokata. Aikatauluun ei voi lisätä uusia rivejä eikä olemassa olevia rivejä voi poistaa. Kunkin myyntitilausrivin tuottoaikataulun tiedot on ylläpidettävä sen varmistamiseksi, että organisaatio kirjaa siirrettyä summaa vastaavan summan ajan kuluessa.

### <a name="edit-schedule-lines"></a>Aikataulurivien muokkaus

Aikataulun riveihin voi tehdä joitakin muutoksia. Rivien seuraavia kenttiä voidaan muuttaa:

- **Pidossa** – Tämä merkintä voidaan lisätä tai poistaa ennen rivin käsittelyä. Merkintä poistetaan valitsemalla rivi ja sitten **Poista pito**. Tuottoa ei voi muuttaa riveillä, jotka ovat pidossa. Rivejä voidaan laittaa automaattisesti pitoon, jos tuottoaikataulu sallii automaattisen pidon.

    [![Tuottoaikataulut – aikataulurivien muokkaaminen](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)

- **Kirjauspäivämäärä** – Kirjauspäivämäärää voi muuttaa ennen rivin käsittelyä. Kun tuottokirjauskansion luova prosessi suoritetaan, **Tuottokirjauksen tilannepäivämäärä** -kenttään täytetään päivämäärä. Kyseistä päivämäärää verrataan **Kirjauspäivämäärä**-kenttään sen määrittämiseksi, mitkä rivit kirjataan.
- **Vapautettava summa** – Vapautettavaa summa voidaan muuttaa ennen rivin käsittelyä. Kirjattavan tuoton summaa voidaan pienentää, mutta ei suurentaa. Tämän kentän avulla organisaatio voi kirjata osan tuotosta kirjauspäivämääränä. Jos summaa on muutettu, **Jäljellä oleva summa** -kentässä oleva summa ilmaisee, kuinka paljon tuottoa on vielä kirjattava.
- **Vapautettava summa** – Jos tuottoaikataulu on määritetty yhdelle esiintymälle tai yhdelle kuukaudelle, **Vapautettava summa** -kentässä näkyy myyntitilausrivin määrä. Myös tätä kenttää voidaan muuttaa, ja se tarjoaa toisen tavan kirjata osan tuotosta. Jos rivin määrä esimerkiksi on 5, määrä voidaan ohittaa siten, että se on alle 5. **Vapautettava summa** -kentän summa päivitetään vastaavasti.

### <a name="update-contract-terms"></a>Sopimusehtojen päivittäminen

Tuottoaikataulun tiedot luodaan sen tuottoaikataulun perusteella, joka on kohdistettu myyntitilausriville, kun lasku kirjataan. Jos myyntitilausrivin tuottoaikataulu on virheellinen, sitä ei voida muuttaa myyntitilauksessa sen jälkeen, kun myyntitilaus on laskutettu. Tuottoaikataulun muuttamiseen on sen sijaan käytettävä **Päivitä sopimusehdot** -painiketta. Tuottoaikataulua voidaan muuttaa joko ennen tuoton kirjaamista tai sen jälkeen.

Aikataulua voidaan muuttaa valitsemalla mikä tahansa muutettavan nimikkeen aikataulurivi. Seuraavassa kuvassa on valittuna nimikkeen S0008 rivi. Kyseinen nimike on kirjattu käyttäen 12 kuukauden tuottoaikataulua. Kun **Päivitä sopimusehdot** valitaan, valintaikkunassa näytetään sopimuksen alkamis- ja päättymispäivät sekä tuottoaikataulu.

[![Sopimuksen alkamis- ja päättymispäivät.](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)

Sopimuksen alkamis- ja päättymispäivät muutetaan vastaamaan oikeaa aikaväliä. Kun aikaväliä muutetaan, **Esiintymien määrä**-kentän arvon on vastattava järjestelmässä määritettyä tuottoaikataulua. Koska sopimus tässä esimerkissä muutettiin 24 kuukauden kestoiseksi, on määritettävä 24 kuukauden tuottoaikataulu. Koska 24 kuukauden tuottoaikataulu on olemassa, se annetaan oletusarvoisesti, ja sopimusta voidaan muuttaa. Jos olemassa olevaa tuottoaikataulua, jolla on sama määrä esiintymiä, ei ole, sopimusta ei voi muuttaa. Kun sopimusehtoja ja tuottoaikataulua on päivitetty halutulla tavalla, tallenna muutoksesi valitsemalla valintaikkunassa **OK**.

[![Päivitetty sopimuksen aikaväli](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)

Sopimuksen muutoksilla on seuraavat vaikutukset tuottoaikataulutietoihin:

- Jos tuotteen tuotto on kirjattu, kaikki aiemmat aikataulutiedot poistetaan ja korvataan uusilla tuottoaikataulutiedoilla. Esimerkiksi nimikkeellä S0008 oli alun perin aikataulutiedoissa 12 riviä. Nämä 12 riviä poistetaan ja korvataan 24:llä uuteen tuottoaikatauluun perustuvalla rivillä.
- Jos tuotteelle on kirjattu tuottoa, tuottoa on kirjattu väärin, koska kirjaus on perustunut virheelliseen tuottoaikatauluun. Nämä rivit on takaisinkirjattava ja kirjattava uudelleen uuden aikataulun perusteella. Tässä skenaariossa luodaan uusia tuottoaikataulurivejä, joilla on negatiivinen summa alkuperäisenä kirjauspäivänä. Sitten luodaan uusia rivejä, joilla summat kirjataan uuden tuottoaikataulun perusteella. 8.8.2019 esimerkiksi kirjattiin 10,53 dollarin tuotto. 8. syyskuuta 2019 taas kirjattiin 13,16 dollarin tuotto. Siten samoina päivinä luodaan kaksi uutta riviä. Yhden rivin arvo on -10,53 dollaria ja toisen -13,16 dollaria. Sitten luodaan 24 uutta riviä, joille siirretyn tuoton kokonaismäärä eli 160,61 dollaria kohdistetaan. Takaisinkirjausrivit voidaan kirjata suorittamalla **Luo kirjauskansio** -prosessi.

[![Tuottokirjausaikataulu](./media/revenue-recognition-rev-recog-schedule-03.png)](./media/revenue-recognition-rev-recog-schedule-03.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]