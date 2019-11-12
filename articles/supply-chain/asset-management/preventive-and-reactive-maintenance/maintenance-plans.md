---
title: Ylläpitosuunnitelmat
description: Tässä ohjeaiheessa kerrotaan ylläpitosuunnitelmista resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5f88c681eecbd630902c6087b910bd6880b39673
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571343"
---
# <a name="maintenance-plans"></a>Ylläpitosuunnitelmat

[!include [banner](../../includes/banner.md)]

 

Huoltosuunnitelma määrittää, milloin ennalta suunniteltu ennaltaehkäisevä kunnossapitotyö suoritetaan käyttöomaisuuserälle. Ylläpitosuunnitelmat voivat liittyä käyttöomaisuuseriin, omaisuuslajeihin, toiminnallisiin sijainteihin tai toiminnallisiin sijaintityyppeihin, mutta ensin on luotava huoltosuunnitelmat, joita käytetään yrityksessä.

Ylläpitosuunnitelmassa voi olla useita huoltosuunnitelmarivejä. Kunnossapitotöiden tyyppi ja väli määritetään huoltosuunnitelmarivillä. Ylläpitosuunnitelman rivejä on kahdenlaisia:

- Aika  
- Inventoija  

Huoltosuunnitelmarivejä, joiden tyyppi on "aika", käytetään toistuvassa suunnitellussa kunnossapidossa tietyn aikavälin perusteella. Huolto suunnitelma rivejä, joiden tyyppi on "laskuri", käytetään suunniteltuun kunnossapitoon tai reaktiiviseen ylläpitoon käyttöomaisuuslaskurin merkintöjen perusteella. Ylläpitosuunnitelmaan voi kuulua useita kummankin tyyppisiä huoltosuunnitelmarivejä.

>[!NOTE]
>Jos käyttöomaisuuserän laskurityypille ei ole rekisteröity laskuriarvoja, ylläpitosuunnitelman rivit jätetään pois.

Ensin luot huoltosuunnitelmat, joita tarvitset ennaltaehkäiseviin kunnossapitotöihin, ja valitset käyttöomaisuustyypit, resurssit, toiminnalliset sijaintityypit ja toiminnalliset sijainnit, jotka liittyvät kuhunkin huoltosuunnitelmaan. Sen jälkeen voit tarvittaessa lisätä kunnossapitosuunnitelmia käyttöomaisuuserään tai toiminnallisiin paikkoihin kohdassa **Kaikki resurssit** > valitse resurssi > **Resurssien ylläpitosuunnitelmat** -pikavälilehti tai **Kaikki toiminnalliset sijainnit** > valitse toiminnallinen sijainti > **Ylläpitosuunnitelmat**-pikavälilehti.

Jos lisäät kunnossapitosuunnitelman käyttöomaisuuslajeihin tai toiminnallisiin sijaintityyppeihin, se tarkoittaa, että kun luot uusia resursseja tai toiminnallisia sijainteja näiden käyttöomaisuus tyyppien tai toiminnallisten sijaintien tyyppien avulla, käyttöomaisuus tai toiminnallinen sijainti lisätään automaattisesti huoltosuunnitelmaan. Huoltosuunnitelman suhteen alkamispäivämäärä on kuluva päivämäärä, joka on ehkä oikaistava.

## <a name="set-up-maintenance-plans"></a>Määritä ylläpitosuunnitelmat

Tässä osassa kuvataan huoltosuunnitelmarivien määrittämistä ja esimerkkejä siitä, miten niitä voidaan käyttää.

1. Valitse **Resurssien hallinta** > **Asetukset** > **Ennalta ehkäisevä ylläpito** > **Ylläpitosuunnitelmat**.

2. Luo uusi järjestys valitsemalla **Uusi**.

3. Lisää tunnus **Ylläpitojakso**-kenttään ja laskurin nimi **Nimi**-kenttään.

4. Lisää **Suunnitelman päivämäärä** -kenttään aloituspäivämäärä, josta lähtien suunnittelu voidaan tehdä ylläpitosuunnitelmassa. Huomaa, että aikaperusteisissa ylläpitosuunnitelman riveissä voi olla muita suunnitelman päivämääriä.

5. Aktivoi huoltosuunnitelma valitsemalla **Aktiivinen**-vaihtopainikkeessa "kyllä".

>[!NOTE]
>Jos huoltosuunnitelma poistetaan käytöstä, ylläpitoaikatauluun ei luoda aikataulumerkintöjä, kun aikataulun ylläpitosuunnitelmatyö suoritetaan.

6. **Toleranssipäivät ennen**- ja **Toleranssipäivät jälkeen** -kentät liittyvät huoltosuunnitelmariveihin, joissa **Piilota päällekkäiset ylläpitotyöt** -valintaruutu on valittuna (katso vaihe 17). "Toleranssi"-kenttiä käytetään pidentämään aikaväliä päivinä, jolloin, jos useat huoltosuunnitelmat menevät päällekkäin, kattavin/suurin työ luodaan ylläpitoaikatauluriviksi ylläpitosuunnitelman ajoituksen aikana, kun taas useammin suoritettavia päällekkäisiä töitä jätetään pois ylläpitosuunnitelman ajoituksessa. Lisää päivien määrä **Toleranssipäiviä ennen** -kenttään, esimerkiksi "2".

7. Jos olet lisännyt arvon **Toleranssipäiviä ennen** -kenttään, lisää päivien lukumäärä myös **Toleranssi päiviä jälkeen** -kenttään, esimerkiksi "2".

>[!NOTE]
>Tässä ja edellisessä vaiheessa kuvattu esimerkki tarkoittaa, että jos useat ylläpitosuunnitelman rivit ovat päällekkäisiä ja jos vähintään yhdelle riville on valittu **Piilota päällekkäiset ylläpitotyöt**, kausi, josta on jätetty pois huoltoaikataulu rivit, on pidennetty yhteensä viiteen päivään (ylläpitoaikataulurivin odotettu alkamispäivä *ja* kaksi päivää ennen kyseistä päivämäärää *ja* kaksi päivää sen jälkeen).

8. **Tiedot**-pikavälilehden **Tiedot**-ryhmän kentissä näkyy ylläpitosuunnitelmaan määritettyjen huoltosuunnitelmarivien määrä sekä ylläpitosuunnitelmaan liittyvien käyttökohteiden ja toiminnallisten sijaintien määrä.

9. Luo uusi huoltosuunnitelmarivi valitsemalla **Rivit**-pikavälilehdessä **Lisää aikarivi** tai **Lisää resurssilaskuririvi**.

10. Kirjoita **Työtilauksen kuvaus** -kenttään rivin kuvaus. Kuvaus siirretään liittyviin työtilauksiin.

11. Valitse työtyyppi, johon kunnossapitosuunnitelmarivi liittyy **Ylläpitotyön tyyppi** -kentässä.

12. Valitse **Ylläpitotyön tyypin variantti**- ja **Toimiala**-kentissä kunnossapitotyön tyypin variantti ja toimiala.

13. Voit lisätä **Päättyminen päivän sisällä**- ja **Päättyminen tunnin sisällä** -kenttiin suunnitellun päätymishetken päivinä tai tunteina. Odotettu päättymispäivämäärä lisätään suhteessa suunniteltuun aloituspäivämäärään, joka lasketaan huoltoaikataulurivien luonnin yhteydessä. Voit esimerkiksi lisätä **Päättyminen päivän sisällä** -kenttään arvon 7, joka ilmaisee, että liittyvä tehtävä on suoritettava viikon kuluessa suunnitellusta aloituspäivämäärästä.

14. Valitse **Välityyppi**-kentässä huoltosuunnitelmarivillä käytettävän välin tyyppi, esimerkiksi "Toistetaan..." tai "Kerran...". Alla olevassa [Välityyppien yleiskatsaus](## Interval types overview) -taulukossa on välityyppien ja rivityyppien välisen suhteen kuvaus.

15. **Kausi**-kenttä koskee vain aikaperustaisia rivityyppejä. Valitse jakson frekvensiin liittyvä kausityyppi.

16. Lisää **Jakson frekvenssi** -kenttään, kuinka monta kertaa riviä käytetään ennaltaehkäisevien kunnossapitotöiden suunnittelussa. Esimerkki: Jos olet luonut rivin, jonka tyyppi on Laskuri, ja laskuri on tuotantomäärä, ja lisäät tähän kenttään numeron "20000", uudet huoltosarjarivit luodaan ennaltaehkäisevän huollon ajoituksessa aina, kun suunnitellaan 20 000 uuden nimikkeen tuotantoa.

17. **Piilota päällekkäiset ylläpitotyöt** -valintaruutu liittyy aika- ja laskuripohjaisiin rivityyppeihin. Valitse tämä valintaruutu, jos haluat poistaa samana päivänä luodut kunnossapitoaikataulumerkinnät. Tämä on tarpeen, jos olet esimerkiksi luonut 1 kuukauden tarkastusrivin, 6 kuukauden tarkastus rivin ja yhden vuoden tarkastusrivin. Yhden vuoden tarkastuksessa haluat tehdä vain vuoden välein tehtävän tarkistuksen, ei 1 tai 6 kk välein tehtävää tarkastusta. Tämän esimerkin määrittäminen oikein edellyttää, että määrität yhden vuoden tarkastusrivin ensimmäiseksi riviksi, 6 kuukauden rivin toiseksi riviksi ja kolmanneksi riviksi 1 kuukauden rivin ja valitset **Piilota päällekkäiset ylläpitotyöt** -valintaruudun 1 kuukauden ja 6 kuukauden riveillä. Näin varmistat, että kun saavutat yhden vuoden aikavälin, 1 kuukauden ja 6 kuukauden tarkastukset jätetään pois ja huoltoaikataulurivi luodaan vain yhden vuoden tarkastusriville.

>[!NOTE]
>Tässä vaiheessa kuvattu esimerkki osoittaa, että kaikkein kattavin työ, joka sisältää suurimman määrän tehtäviä ja jota ei tehdä niin usein, tulee aina lisätä ensimmäiseksi riviksi. Tiheämmin toistuvat työt lisätään sitten erillisinä riveinä esiintymisjärjestyksessä, jolloin useimmin toistuva työ sijoitetaan luettelon alaosaan.

18. **Laskuri**-kenttä koskee vain laskuriperustaisia rivityyppejä. Valitse rivillä käytettävä laskurityyppi. Jos laskurityyppi ei ole aktiivinen liittyvässä käyttöomaisuuskohteessa, huoltosuunnitelmarivi jätetään pois.

19. **Resurssilaskurin aikaraja päivinä** -kenttä liittyy vain laskuripohjaisiin rivityyppeihin. Lisää numero, joka määrittää, kuinka monta päivää taaksepäin laskurien rekisteröinnit tarkistetaan, kun ylläpitosuunnitelman ajoittaminen tehdään. Tämä tarkoittaa, kuinka kauas taaksepäin tietoja (aiemmat laskurirekisteröinnit) käytetään määritettäessä trendiä, joka määrittää, kuinka monta ylläpitoaikatauluriviä luodaan.

>*Esimerkki:* Jos laskurikirjaus on tarkoitus tehdä kerran kuukaudessa, voit lisätä tähän kenttään numeron 365, koska ylläpitosuunnitelman ajoitus perustuu aina viimeiseen 12 kuukauteen ja siksi se luo kunnossapitoaikataulurivejä, jotka perustuvat kuluneen vuoden trendiin. Jos taas lisäät tähän kenttään numeron 10, oletat, että laskurikirjaukset tehdään useammin, esimerkiksi päivittäin. Tämä tarkoittaa sitä, että kun ajoitat huoltosuunnitelman, kunnossapitoaikataulurivien ajoituksen perustana käytetään viimeisten 10 päivän laskurimerkintöjä.

20. **Suunnitelman päivämäärä** -kenttä koskee vain aikaperustaisia rivityyppejä. Jos huoltosuunnitelman rivillä on toinen suunnittelupäivämäärä kuin koko huoltosuunnitelmalla, valitse rivillä **Suunnitelman päivämäärä** -kentästä päivämäärä.

21. **Palvelutaso**-kentässä voit valitat työtilauksen palvelutason lisärajaukseksi ylläpitosuunnitelman riville, jota käytetään työtilausten palvelutasona.

22. Valitse **Luo automaattisesti** -valintaruutu, jos haluat, että työtilaus luodaan automaattisesti valitun huoltosuunnitelmarivin mukaan huoltosuunnitelmia aikataulutettaessa.

23. Jos olet valinnut **Luo automaattisesti** -valintaruudun, voit valita työtilauksen tyypin automaattisesti luodulle työtilaukselle **Työtilauksen tyyppi** -kentässä. Jos olet valinnut **Luo automaattisesti** -valintaruudun, etkä valitse tässä kentässä työtilaustyyppiä, käytetään työtilaustyyppiä, joka on valittu kohdassa **Resurssien hallinta** > **Asetukset** > **Resurssienhallinnan parametrit** > **työtilaukset** -linkki > **Ennaltaehkäisevän työtilauksen tyyppi** -kenttä.

24. **Kausi alkaen**- ja **Kausi asti** -kenttien avulla voit luoda toistuvan aikapohjaisen huoltosuunnitelmarivin 12 kuukauden jakson sisällä. *Esimerkki:* Viheralueiden ylläpitämiseen käytettävät laitteet edellyttävät joka kevät huoltoa ennalta määrätyn ajanjakson sisällä. Lisää **Kausi alkaen** -kenttään toistuvan kauden alkamispäivämäärä.

25. Lisää **Kausi asti** -kenttään toistuvan kauden päättymispäivämäärä.

26. **Tuloksena oleva kausi** -kentässä näkyviin tulee toistuva kausi. Kun valittu kausi on kulunut ja aloitat uuden vuoden, tässä kentässä näkyvä kausi päivitetään vastaamaan toistosarjan seuraavaa jaksoa.

27. Valitse **Resurssit**-pikavälilehdessä resurssit, jotka liittyvät ylläpitosuunnitelmaan.

28. Valitse **Resurssityypit**-pikavälilehdessä resurssityypit, jotka liittyvät ylläpitosuunnitelmaan.

29. Valitse **Toiminnalliset sijainnit** -pikavälilehdessä toiminnalliset sijainnit, jotka liittyvät ylläpitosuunnitelmaan. Tarvittaessa voit tehdä asetuksista tarkempia valitsemalla liittyvän käyttöomaisuus tyypin, valmistajan ja mallin.

30. Valitse **Toiminnalliset sijaintityypit** -pikavälilehdessä toiminnalliset sijaintityypit, jotka liittyvät ylläpitosuunnitelmaan.

>[!NOTE]
>Kun työtilaukset luodaan manuaalisesti toimittajan takuun kattamille resursseille, näyttöön tulee valintaikkuna, jonka avulla käyttäjä saa tietää takuun. Työtilauksen luonti voidaan sitten peruuttaa. Takuusuhdetta koskeva tarkistus jätetään pois automaattisesti luoduissa työtilauksissa.

## <a name="interval-types-overview"></a>Välityyppien yleiskuvaus

| Välin tyyppi ja kuvaus                                                                                                                                                                                                                                                                                                                                                                                                       | Rivityyppi: Aika                                                                                                                                                                                                                                                                                                                                                           | Rivityyppi: Laskuri                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aikavälin tyyppi: Toistetaan suunnitelman päivämäärästä** laskenta alkaa käytetystä suunnitelman päivästä. Kun ajoitat huoltosuunnitelmia, huoltoaikataulurivit luodaan, kun aikaväli saavutetaan.                                                                                                                                                                                                                | Käytetään huoltosuunnitelmarivin **Suunnitelman päivämäärä** -arvoa. Jos rivillä ei ole valittu suunnitelmapäivämäärää, käytetään ylläpitosuunnitelman **Suunnitelman päivämäärä** -arvoa. Esimerkki: Jos **Jakson frekvenssi** -kenttään on lisätty numero "3" ja **Kausi** -kentässä on valittuna "Vuosi", uusi huoltoaikataulurivi luodaan kolmen vuoden välein.                             | Käytetään huoltosuunnitelman **Suunnitelman päivämäärä** -arvoa. Jos laskuri on korvattu, suunnitelman päivämääränä käytetään viimeisintä korvaavaa päivää.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Välin tyyppi: Toistuu aloituspäivämäärästä** – Laskuri alkaa käyttöomaisuussuhteen alkamispäivämäärästä. Päivämäärä valitaan kohdassa **Kaikki resurssit** > **Resurssien ylläpitosuunnitelmat** -pikavälilehti > **Aloituspäivämäärä** -kenttä tai kohdassa **Kaikki toiminnalliset sijainnit** > **Ylläpitosuunnitelmat** -pikavälilehti > **Aloituspäivämäärä** -kenttä. Kun ajoitat huoltosuunnitelmia, huoltoaikataulurivi luodaan, kun aikaväli saavutetaan. | Käyttöomaisuuserän tai toimipaikan huoltosuunnitelmarivin aloituspäivää käytetään. Jos tämä kenttä on tyhjä, käytetään ylläpitosuunnitelman **Suunnitelman päivämäärä** -päivämäärää.                                                                                                                                                                                                 | Käyttöomaisuuserän tai toimipaikan huoltosuunnitelmarivin aloituspäivää käytetään. Jos tämä kenttä on tyhjä, käytetään ylläpitosuunnitelman **Suunnitelman päivämäärä** -päivämäärää.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Välin tyyppi: toistuu viimeisestä työtilauksesta** – Laskuri alkaa viimeisimmän työtilauksen päättymispäivämäärästä ja-ajasta, joka suoritettiin käyttöomaisuuserälle ja tämän tietyn kunnosapitotyön tyypin, kunnossapitotyön tyypin variantin ja toimialan yhdistelmälle. Tämä päivämäärä ja kellonaika näkyvät**Kaikki työtilaukset** -näkymän **Toteutunut lopetus** -kentässä.                                                                                                                                 | Käyttöomaisuuserälle tehdyn työtilauksen todellinen päättymispäivä ja -aika ja tietyn kunnossapitotyön tyypin / kunnossapitotyön tyypin variantin / toimialan yhdistelmä. Jos suoritettua työtilausta ei löydy, käytetään sen sijaan jotakin edellä kuvatun "Toistetään aloituspäivämäärästä" -aikavälityyppiä.                                                                                             | Käyttöomaisuuserälle tehdyn työtilauksen todellinen päättymispäivä ja -aika *ja* kunnossapitotyön tyypin / kunnossapitotyön tyypin variantin / toimialan yhdistelmä. käytetään. Jos työtilauksen loppupäivämäärä ja -aika on jätetty tyhjäksi, käytetään sen sijaan jotakin edellä kuvatun "Toistetään aloituspäivämäärästä" -aikavälityyppiä.                                                                                                                                                                                                                                                                                                                                                                           |
| **Välin tyyppi: Kerran suunnitelman päivämäärästä** – Katso yllä olevan "Toistetaan suunnitelman päivämäärästä" -välityypin kuvaus. Ainoa ero on se, että tätä aikavälityyppiä käytetään vain kerran.                                                                                                                                                                                                                                                   | Katso edellä oleva "Toistetaan suunnitelman päivämäärästä"-välityypin kuvaus. Tätä väliä käytetään yleensä kertaylläpito- tai kertahuoltotöissä.                                                                                                                                                                                                                             | Katso edellä oleva "Toistetaan suunnitelman päivämäärästä"-välityypin kuvaus. Tätä väliä käytetään yleensä kertaylläpito- tai kertahuoltotöissä. **Huomautus 1:** Tämä välityyppi on merkityksellinen vain, jos laskuri korvataan aina, kun suoritat huoltotyön. Jos laskuri on jostain syystä korvattu ennen suunnitellun aikavälin loppumisaikaa, työlle lasketaan uusi aika laskurin korvaamisen ajalta. **Huomautus 2:** Jos laskuri korvataan huoltotyötä suoritettaessa, tämä aikavälityyppi toimii kuten edellä kuvattu Toistetaan suunnitelman päivämäärästä -tyyppi.                                             |
| **Välin tyyppi: Kerran aloituspäivämäärästä** – Katso yllä olevan "Toistetään aloituspäivämäärästä" -välityypin kuvaus. Ainoa ero on se, että tätä aikavälityyppiä käytetään vain kerran.                                                                                                                                                                                                                                                 | Katso edellä oleva "Toistetään aloituspäivämäärästä"-välityypin kuvaus. Tätä väliä käytetään yleensä kertaylläpito- tai kertahuoltotöissä.                                                                                                                                                                                                                            | Katso edellä oleva "Toistetään aloituspäivämäärästä"-välityypin kuvaus. Tätä väliä käytetään yleensä kertaylläpito- tai kertahuoltotöissä. **Huomautus 1**: yllä oleva koskee myös tätä aikavälin tyyppiä. **Huomautus 3:** Jos laskuri korvataan huoltotyötä suoritettaessa, tämä aikavälityyppi toimii kuten edellä kuvattu Toistetään aloituspäivämäärästä -tyyppi.                                                                                                                                                                                                                                                                                                |
| **Aikavälin tyyppi: Kerran, kun ylittää** – Tämä aikavälityyppi koskee vain laskureita ja sitä käytetään huoltosuunnitelmarivillä määritetyn ylärajan ilmaisemiseen. Ylläpitoaikataulumerkinnöissä on odotettu laskurin alkamispäivämäärä ja -aika, mikä tarkoittaa, että nämä tapahtumat luodaan siten, että odotettu alkamispäivämäärä on sama tai aikaisempi kuin järjestelmän päivämäärä.                                                | Ei saatavilla                                                                                                                                                                                                                                                                                                                                                                       | Laskuriväli ilmaisee ylärajan. Jos raja ylittyy, kun luot laskurikirjauksen, huoltoaikataulurivi luodaan, kun ajoitat ennaltaehkäisevän huollon.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Aikavälin tyyppi: Kerran, kun alittaa** – Tämä aikavälityyppi koskee vain laskureita ja sitä käytetään huoltosuunnitelmarivillä määritetyn alarajan ilmaisemiseen. Ylläpitoaikataulumerkinnöissä on odotettu laskurin alkamispäivämäärä ja -aika, mikä tarkoittaa, että nämä tapahtumat luodaan siten, että odotettu alkamispäivämäärä on sama tai aikaisempi kuin järjestelmän päivämäärä.                                                 | Ei saatavilla                                                                                                                                                                                                                                                                                                                                                                       | Laskuriväli ilmaisee alarajan. Jos raja alittuu, kun luot laskurikirjauksen, huoltoaikataulurivi luodaan, kun ajoitat ennaltaehkäisevän huollon.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Aikavälin tyyppi: Linkitetty aloituspäivämäärästä** tämä aikavälityyppi luo ylläpitoaikataulurivin vain kerran. Huoltosuunnitelma voi sisältää useampia huoltosuunnitelmarivejä käyttäen tätä aikavälityyppiä, ja nämä rivit on linkitetty. Yleensä luodaan huoltosuunnitelma, joka sisältää vain tämän aikavälityypin rivit. Huoltoaikataulurivit luodaan määrittämällä huoltosuunnitelman rivi, jolla on ensimmäinen odotettu alkamispäivämäärä ja -aika.                                                                                                                                                                                                                                                                                                                                                                                           | Katso edellä oleva "Kerran aloituspäivämäärästä"-välityypin kuvaus. Esimerkki: Luot huoltosuunnitelmassa kaksi riviä auton huoltotyötä varten: yksi aika-pohjainen rivi, jossa on 1 vuoden kausi, ja yksi laskuripohjainen rivi, jonka raja on 25 000 km. Huoltoaikataulurivi luodaan ensin saavutettavalle rajalle. Tälle rivityypille luodaan rivi, jolla on 1 vuoden kausi.                                                                                                                                                                                   | Katso edellä oleva "Kerran aloituspäivämäärästä"-välityypin kuvaus. Esimerkki: Luot huoltosuunnitelmassa kaksi riviä auton huoltotyötä varten: yksi aika-pohjainen rivi, jossa on 1 vuoden kausi, ja yksi laskuripohjainen rivi, jonka raja on 25 000 km. Huoltoaikataulurivi luodaan ensin saavutettavalle rajalle. Tälle rivityypille luodaan rivi, jolla on 25 000 kilometrin raja. Esimerkki kahden laskuririvin luomisesta: Voit myös määrittää ylläpitosuunnitelman, jossa on kaksi linkitettyä laskuripohjaista riviä, joilla ensimmäisen rivin raja 10 000 tuotettua nimikettä, ja toinen rivi liittyy koneeseen tai kuormituspaikkaan, joka edellyttää huoltoa 3 000 tunnin käytön jälkeen.                                                                                                                                                           |
| **Aikavälin tyyppi: linkitetty viimeisestä työtilauksesta** Tämä välityyppi luo uusia ylläpitoaikataulurivejä jokaisen valmiin työtilauksen jälkeen. Huoltosuunnitelma voi sisältää useampia rivejä käyttäen tätä aikavälityyppiä, ja nämä rivit on linkitetty. Yleensä luodaan huoltosuunnitelma, joka sisältää vain tämän aikavälityypin huoltosuunnitelmarivit. Huoltoaikataulurivit luodaan määrittämällä huoltosuunnitelman rivi, jolla on ensimmäinen odotettu alkamispäivämäärä ja -aika.                                                                                                                                                                                                                                                                        | Tämä aikaväli tyyppi toimii edellä kuvatulla Linkitetty aloituspäivämäärästä -tyypin tavalla. Ainoa ero on aikavälityypin perustana oleva päivämäärä. Käytettävä päivämäärä on käyttöomaisuuserälle tehdyn viimeisimmän työtilauksen todellinen valmistumispäivä ja -aika *ja* kunnossapitotyön tyypin / kunnossapitotyön tyypin variantin / toimialan yhdistelmä.                                                                                                                                                                                                                                                           | Tämä aikaväli tyyppi toimii edellä kuvatulla Linkitetty aloituspäivämäärästä -tyypin tavalla. Ainoa ero on aikavälityypin perustana oleva päivämäärä. Käytettävä päivämäärä on käyttöomaisuuserälle tehdyn viimeisimmän työtilauksen todellinen valmistumispäivä ja -aika *ja* kunnossapitotyön tyypin / kunnossapitotyön tyypin variantin / toimialan yhdistelmä.                                                                                                                   |


>[!NOTE]
>Kun huoltoaikataulurivit luodaan aikaperustaisille ylläpitosuunnitelmariveille, odotettu aika on aina päivän alussa. Laskuripohjaisille ylläpitosuunnitelmariveille odotettu aika voi olla milloin tahansa päivän aikana.

Alla on esimerkkejä aikapohjaisten ja laskuripohjaisten ylläpitosuunnitelmarivien asetuksista:

**Esimerkki 1 – aikapohjainen huoltosuunnitelma rivi:** Voitelutyö voidaan määrittää säännöllisin kiintein väliajoin, kerran viikossa. Tätä tarkoitusta varten valitse **Välin tyyppi** -kentässä "Toistetaan suunnitelman päivämäärästä". Katso esimerkki seuraavasta kuvasta.

![Kuva 1](media/02-preventive-maintenance.png)

**Esimerkki 2 – aikapohjainen huoltosuunnitelmarivi:** Tarkastustyö voidaan määrittää tehtäväksi noin kerran viikossa. Tätä tarkoitusta varten valitse **Välin tyyppi** -kentässä "Toistetaan viimeisestä työtilauksesta". Katso esimerkki seuraavasta kuvasta.

![Kuva 2](media/03-preventive-maintenance.png)

**Esimerkki 3 – laskuripohjainen ylläpitosuunnitelmarivi:** Seuraavassa kuvassa on tuntilaskuri, jolle uusi huoltoaikataulurivi luodaan joka kerta, kun 250 tuntia on kulunut. Tämän laskuripohjaisen rivin välityyppi on "Toistetään aloituspäivämäärästä". Aloituspäivämäärä on liittyvien resurssien aloituspäivämäärä kohdassa **Kaikki resurssit** > **Resurssien ylläpitosuunnitelmat** -pikavälilehti > **Aloituspäivämäärä** -kenttä tai kohdassa **Kaikki toiminnalliset sijainnit** > **Ylläpitosuunnitelmat** -pikavälilehti > **Aloituspäivämäärä** -kenttä. Tämä on esimerkki *ennaltaehkäisevästä* huoltosuunnitelmasta, koska huoltoaikataulurivi luodaan automaattisesti aina, kun kynnysarvo (+ 250) saavutetaan.

![Kuva 3](media/04-preventive-maintenance.png)


**Esimerkki 4 – laskuripohjainen huoltosuunnitelmarivi:** Seuraavassa kuvassa on laskuriarvon vähennys, joka mittaa jarrupalojen kulumista. Huoltoaikataulurivi luodaan, kun jarrupalalle luodaan laskurikirjaus, joka on alle 20 millimetriä. Tämän laskuripohjaisen rivin aikavälityyppi on "Kerran, kun alittaa" tai "Kerran viimeisestä aloituspäivämäärästä". Tämä on esimerkki *reaktiivisesta* huoltosuunnitelmasta, koska huoltoaikatauluriviä ei luoda ennen kuin rekisteröidään alle 20 mm mittaus rekisteröidään.

![Kuva 4](media/05-preventive-maintenance.png)


**Esimerkki 5 – Laskuripohjainen ylläpitosuunnitelmarivi:** Seuraavassa kuvassa on laskuri, jonka raja on -18°C. Huoltoaikataulu rivi luodaan, kun laskurikirjaus on tehty yli -18 celsiusasteen mittauksesta. Tämän laskuripohjaisen rivin välityyppi on "Kerran, kun ylittää". Tämä on esimerkki *reaktiivisesta* huoltosuunnitelmasta, koska huoltoaikatauluriviä ei luoda ennen kuin rekisteröidään yli -18°C mittaus rekisteröidään.

![Kuva 5](media/06-preventive-maintenance.png)

- Kun luot uuden käyttöomaisuuserän ja käyttöomaisuuserä käyttää huoltosuunnitelmaan liittyvää käyttöomaisuustyyppiä, ylläpitosuunnitelma lisätään automaattisesti **Kaikki objektit** > **Resurssien ylläpitosuunnitelmat** -pikavälilehteen. **Ylläpitosuunnitelmat**-pikavälilehden **Resurssin oletustyypit** -kohtaan lisätään automaattisesti liittyvät huoltosuunnitelmat.  
- Jos lisäät tai poistat käyttöomaisuustyyppejä tai toiminnallisia sijaintityyppejä kohdassa **Ylläpitosuunnitelmat**, muutos vaikuttaa vain uusiin resurssiehin, jotka on luotu muutoksen tekemisen jälkeen.  
- Jos lisäät tai poistat käyttöomaisuuseriä tai toiminnallisia sijainteja **Ylläpitosuunnitelmat** -kohdassa, tämä muutos päivitetään automaattisesti **Kaikki resurssit** > **Resurssien ylläpitosuunnitelmat** -pikavälilehteen tai **Kaikki toiminnalliset sijainnit** > **Ylläpitosuunnitelmat** -pikavälilehteen.  

Seuraavassa kuvassa on esimerkki **Ylläpitosuunnitelmat**-sivun "Truck service" -nimisestä huoltosuunnitelmasta.

![Kuva 6](media/07-preventive-maintenance.png)


## <a name="add-a-maintenance-plan-to-an-asset"></a>Huoltosuunnitelman lisääminen resurssiin

1. Valitse **Resurssien hallinta** > **Yhteiset** > **Resurssit** > **Kaikki resurssit** tai **Aktiiviset resurssit**.

2. Valitse käyttöomaisuuserä, jolle haluat määrittää ylläpitosuunnitelman, ja valitse sitten **Muokkaa.**

3. Valitse **Resurssien ylläpitosuunnitelmat**-pikavälilehdellä **Lisää rivi** lisätäksesi ylläpitosuunnitelman resurssiin.

4. Valitse asianmukainen kunnossapitosuunnitelma **Ylläpitosuunnitelma** -kentässä.

5. Valitse **Aloituspäivämäärä** -kentässä päivämäärä, josta lähtien ennaltaehkäisevien ylläpitotöiden suunnittelu voidaan tehdä. 

6. Valitse **Tallenna**. **Aktiivinen**-kenttä päivittyy automaattisesti.

Seuraavassa kuvassa on esimerkki **Kaikki resurssit**-sivulla resurssille määritetyistä huoltosuunnitelmista.

![Kuva 7](media/08-preventive-maintenance.png)

