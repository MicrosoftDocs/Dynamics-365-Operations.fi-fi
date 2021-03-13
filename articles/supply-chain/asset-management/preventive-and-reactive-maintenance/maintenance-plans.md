---
title: Ylläpitosuunnitelmat
description: Tässä ohjeaiheessa kerrotaan ylläpitosuunnitelmista resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9ec4929e9ea608318b83a2ae6033c4b25855f4dd
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/28/2021
ms.locfileid: "5077547"
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

Ensin luot huoltosuunnitelmat, joita tarvitset ennaltaehkäiseviin kunnossapitotöihin, ja valitset käyttöomaisuustyypit, resurssit, toiminnalliset sijaintityypit ja toiminnalliset sijainnit, jotka liittyvät kuhunkin huoltosuunnitelmaan. Sen jälkeen voit tarvittaessa lisätä kunnossapitosuunnitelmia käyttöomaisuuserään tai toiminnallisiin paikkoihin kohdassa **Kaikki resurssit** \> valitse resurssi \> **Resurssien ylläpitosuunnitelmat** -pikavälilehti tai **Kaikki toiminnalliset sijainnit** \> valitse toiminnallinen sijainti \> **Ylläpitosuunnitelmat**-pikavälilehti.

Jos lisäät kunnossapitosuunnitelman käyttöomaisuuslajeihin tai toiminnallisiin sijaintityyppeihin, se tarkoittaa, että kun luot uusia resursseja tai toiminnallisia sijainteja näiden käyttöomaisuus tyyppien tai toiminnallisten sijaintien tyyppien avulla, käyttöomaisuus tai toiminnallinen sijainti lisätään automaattisesti huoltosuunnitelmaan. Huoltosuunnitelman suhteen alkamispäivämäärä on kuluva päivämäärä, joka on ehkä oikaistava.

## <a name="set-up-maintenance-plans"></a>Määritä ylläpitosuunnitelmat

Tässä osassa kuvataan huoltosuunnitelmarivien määrittämistä ja esimerkkejä siitä, miten niitä voidaan käyttää.

1. Valitse **Resurssien hallinta \> Asetukset \>Ennalta ehkäisevä ylläpito \>Ylläpitosuunnitelmat**.

1. Luo uusi jakso valitsemalla **Uusi**.

1. Lisää tunnus **Ylläpitojakso**-kenttään ja laskurin nimi **Nimi**-kenttään.

1. Lisää **Suunnitelman päivämäärä** -kenttään aloituspäivämäärä, josta lähtien suunnittelu voidaan tehdä ylläpitosuunnitelmassa. Huomaa, että aikaperusteisissa ylläpitosuunnitelman riveissä voi olla muita suunnitelman päivämääriä.

1. Aktivoi huoltosuunnitelma valitsemalla **Aktiivinen**-vaihtopainikkeessa "kyllä".

    >[!NOTE]
    >Jos huoltosuunnitelma poistetaan käytöstä, ylläpitoaikatauluun ei luoda aikataulumerkintöjä, kun aikataulun ylläpitosuunnitelmatyö suoritetaan.

1. **Toleranssipäivät ennen**- ja **Toleranssipäivät jälkeen** -kentät liittyvät huoltosuunnitelmariveihin, joissa **Piilota päällekkäiset ylläpitotyöt** -valintaruutu on valittuna (katso vaihe 17). "Toleranssi"-kenttiä käytetään pidentämään aikaväliä päivinä, jolloin, jos useat huoltosuunnitelmat menevät päällekkäin, kattavin/suurin työ luodaan ylläpitoaikatauluriviksi ylläpitosuunnitelman ajoituksen aikana, kun taas useammin suoritettavia päällekkäisiä töitä jätetään pois ylläpitosuunnitelman ajoituksessa. Lisää päivien määrä **Toleranssipäiviä ennen** -kenttään, esimerkiksi "2".

1. Jos olet lisännyt arvon **Toleranssipäiviä ennen** -kenttään, lisää päivien lukumäärä myös **Toleranssi päiviä jälkeen** -kenttään, esimerkiksi "2".

    >[!NOTE]
    >Tässä ja edellisessä vaiheessa kuvattu esimerkki tarkoittaa, että jos useat ylläpitosuunnitelman rivit ovat päällekkäisiä ja jos vähintään yhdelle riville on valittu **Piilota päällekkäiset ylläpitotyöt**, kausi, josta on jätetty pois huoltoaikataulu rivit, on pidennetty yhteensä viiteen päivään (ylläpitoaikataulurivin odotettu alkamispäivä *ja* kaksi päivää ennen kyseistä päivämäärää *ja* kaksi päivää sen jälkeen).

1. **Tiedot**-pikavälilehden **Tiedot**-ryhmän kentissä näkyy ylläpitosuunnitelmaan määritettyjen huoltosuunnitelmarivien määrä sekä ylläpitosuunnitelmaan liittyvien käyttökohteiden ja toiminnallisten sijaintien määrä.

1. Luo uusi huoltosuunnitelmarivi valitsemalla **Rivit**-pikavälilehdessä **Lisää aikarivi** tai **Lisää resurssilaskuririvi**.

1. Kirjoita **Työtilauksen kuvaus** -kenttään rivin kuvaus. Kuvaus siirretään liittyviin työtilauksiin.

1. Valitse työtyyppi, johon kunnossapitosuunnitelmarivi liittyy **Ylläpitotyön tyyppi** -kentässä.

1. Valitse **Ylläpitotyön tyypin variantti**- ja **Toimiala**-kentissä kunnossapitotyön tyypin variantti ja toimiala.

1. Voit lisätä **Päättyminen päivän sisällä**- ja **Päättyminen tunnin sisällä** -kenttiin suunnitellun päätymishetken päivinä tai tunteina. Odotettu päättymispäivämäärä lisätään suhteessa suunniteltuun aloituspäivämäärään, joka lasketaan huoltoaikataulurivien luonnin yhteydessä. Voit esimerkiksi lisätä **Päättyminen päivän sisällä** -kenttään arvon 7, joka ilmaisee, että liittyvä tehtävä on suoritettava viikon kuluessa suunnitellusta aloituspäivämäärästä.

1. Valitse **Välityyppi**-kentässä huoltosuunnitelmarivillä käytettävän välin tyyppi, esimerkiksi "Toistetaan..." tai "Kerran...". Alla olevassa [Välityyppien yleiskatsaus](#interval-types) -taulukossa on välityyppien ja rivityyppien välisen suhteen kuvaus.

1. **Kausi**-kenttä koskee vain aikaperustaisia rivityyppejä. Valitse jakson frekvensiin liittyvä kausityyppi.

1. Lisää **Jakson frekvenssi** -kenttään, kuinka monta kertaa riviä käytetään ennaltaehkäisevien kunnossapitotöiden suunnittelussa. Esimerkki: Jos olet luonut rivin, jonka tyyppi on Laskuri, ja laskuri on tuotantomäärä, ja lisäät tähän kenttään numeron "20000", uudet huoltosarjarivit luodaan ennaltaehkäisevän huollon ajoituksessa aina, kun suunnitellaan 20 000 uuden nimikkeen tuotantoa.

1. **Piilota päällekkäiset ylläpitotyöt** -valintaruutu liittyy aika- ja laskuripohjaisiin rivityyppeihin. Valitse tämä valintaruutu, jos haluat poistaa samana päivänä luodut kunnossapitoaikataulumerkinnät. Tämä on tarpeen, jos olet esimerkiksi luonut 1 kuukauden tarkastusrivin, 6 kuukauden tarkastus rivin ja yhden vuoden tarkastusrivin. Yhden vuoden tarkastuksessa haluat tehdä vain vuoden välein tehtävän tarkistuksen, ei 1 tai 6 kk välein tehtävää tarkastusta. Tämän esimerkin määrittäminen oikein edellyttää, että määrität yhden vuoden tarkastusrivin ensimmäiseksi riviksi, 6 kuukauden rivin toiseksi riviksi ja kolmanneksi riviksi 1 kuukauden rivin ja valitset **Piilota päällekkäiset ylläpitotyöt** -valintaruudun 1 kuukauden ja 6 kuukauden riveillä. Näin varmistat, että kun saavutat yhden vuoden aikavälin, 1 kuukauden ja 6 kuukauden tarkastukset jätetään pois ja huoltoaikataulurivi luodaan vain yhden vuoden tarkastusriville.

    >[!NOTE]
    >Tässä vaiheessa kuvattu esimerkki osoittaa, että kaikkein kattavin työ, joka sisältää suurimman määrän tehtäviä ja jota ei tehdä niin usein, tulee aina lisätä ensimmäiseksi riviksi. Tiheämmin toistuvat työt lisätään sitten erillisinä riveinä esiintymisjärjestyksessä, jolloin useimmin toistuva työ sijoitetaan luettelon alaosaan.

1. **Laskuri**-kenttä koskee vain laskuriperustaisia rivityyppejä. Valitse rivillä käytettävä laskurityyppi. Jos laskurityyppi ei ole aktiivinen liittyvässä käyttöomaisuuskohteessa, huoltosuunnitelmarivi jätetään pois.

1. **Resurssilaskurin aikaraja päivinä** -kenttä liittyy vain laskuripohjaisiin rivityyppeihin. Lisää numero, joka määrittää, kuinka monta päivää taaksepäin laskurien rekisteröinnit tarkistetaan, kun ylläpitosuunnitelman ajoittaminen tehdään. Tämä tarkoittaa, kuinka kauas taaksepäin tietoja (aiemmat laskurirekisteröinnit) käytetään määritettäessä trendiä, joka määrittää, kuinka monta ylläpitoaikatauluriviä luodaan.

    >*Esimerkki:* Jos laskurikirjaus on tarkoitus tehdä kerran kuukaudessa, voit lisätä tähän kenttään numeron 365, koska ylläpitosuunnitelman ajoitus perustuu aina viimeiseen 12 kuukauteen ja siksi se luo kunnossapitoaikataulurivejä, jotka perustuvat kuluneen vuoden trendiin. Jos taas lisäät tähän kenttään numeron 10, oletat, että laskurikirjaukset tehdään useammin, esimerkiksi päivittäin. Tämä tarkoittaa sitä, että kun ajoitat huoltosuunnitelman, kunnossapitoaikataulurivien ajoituksen perustana käytetään viimeisten 10 päivän laskurimerkintöjä.

1. **Suunnitelman päivämäärä** -kenttä koskee vain aikaperustaisia rivityyppejä. Jos huoltosuunnitelman rivillä on toinen suunnittelupäivämäärä kuin koko huoltosuunnitelmalla, valitse rivillä **Suunnitelman päivämäärä** -kentästä päivämäärä.

1. **Palvelutaso**-kentässä voit valitat työtilauksen palvelutason lisärajaukseksi ylläpitosuunnitelman riville, jota käytetään työtilausten palvelutasona.

1. Valitse **Luo automaattisesti** -valintaruutu, jos haluat, että työtilaus luodaan automaattisesti valitun huoltosuunnitelmarivin mukaan huoltosuunnitelmia aikataulutettaessa.

1. Jos olet valinnut **Luo automaattisesti** -valintaruudun, voit valita työtilauksen tyypin automaattisesti luodulle työtilaukselle **Työtilauksen tyyppi** -kentässä. Jos olet valinnut **Luo automaattisesti** -valintaruudun etkä valitse tässä kentässä työtilaustyyppiä, käytetään työtilaustyyppiä, joka on valittu kohdassa **Resurssien hallinta \> Asetukset \> Resurssienhallinnan parametrit \> Työtilaukset** -linkki \> **Ennaltaehkäisevän työtilauksen tyyppi** -kenttä.

1. **Kausi alkaen**- ja **Kausi asti** -kenttien avulla voit luoda toistuvan aikapohjaisen huoltosuunnitelmarivin 12 kuukauden jakson sisällä. *Esimerkki:* Viheralueiden ylläpitämiseen käytettävät laitteet edellyttävät joka kevät huoltoa ennalta määrätyn ajanjakson sisällä. Lisää **Kausi alkaen** -kenttään toistuvan kauden alkamispäivämäärä.

1. Lisää **Kausi asti** -kenttään toistuvan kauden päättymispäivämäärä.

1. **Tuloksena oleva kausi** -kentässä näkyviin tulee toistuva kausi. Kun valittu kausi on kulunut ja aloitat uuden vuoden, tässä kentässä näkyvä kausi päivitetään vastaamaan toistosarjan seuraavaa jaksoa.

1. Valitse **Resurssit**-pikavälilehdessä resurssit, jotka liittyvät ylläpitosuunnitelmaan.

1. Valitse **Resurssityypit**-pikavälilehdessä resurssityypit, jotka liittyvät ylläpitosuunnitelmaan.

1. Valitse **Toiminnalliset sijainnit** -pikavälilehdessä toiminnalliset sijainnit, jotka liittyvät ylläpitosuunnitelmaan. Tarvittaessa voit tehdä asetuksista tarkempia valitsemalla liittyvän käyttöomaisuus tyypin, valmistajan ja mallin.

1. Valitse **Toiminnalliset sijaintityypit** -pikavälilehdessä toiminnalliset sijaintityypit, jotka liittyvät ylläpitosuunnitelmaan.

>[!NOTE]
>Kun työtilaukset luodaan manuaalisesti toimittajan takuun kattamille resursseille, näyttöön tulee valintaikkuna, jonka avulla käyttäjä saa tietää takuun. Työtilauksen luonti voidaan sitten peruuttaa. Takuusuhdetta koskeva tarkistus jätetään pois automaattisesti luoduissa työtilauksissa.

<a id="interval-types"></a>

## <a name="interval-types-overview"></a>Välityyppien yleiskuvaus

| Välin tyyppi ja kuvaus | Rivityyppi: Aika | Rivityyppi: Laskuri |
|---|---|---|
| **Aikavälin tyyppi: Toistetaan suunnitelman päivämäärästä** laskenta alkaa käytetystä suunnitelman päivästä. Kun ajoitat huoltosuunnitelmia, huoltoaikataulurivit luodaan, kun aikaväli saavutetaan. | Käytetään huoltosuunnitelmarivin **Suunnitelman päivämäärä** -arvoa. Jos rivillä ei ole valittu suunnitelmapäivämäärää, käytetään ylläpitosuunnitelman **Suunnitelman päivämäärä** -arvoa. Esimerkki: Jos **Jakson frekvenssi** -kenttään on lisätty numero "3" ja **Kausi** -kentässä on valittuna "Vuosi", uusi huoltoaikataulurivi luodaan kolmen vuoden välein. | Käytetään huoltosuunnitelman **Suunnitelman päivämäärä** -arvoa. Jos laskuri on korvattu, suunnitelman päivämääränä käytetään viimeisintä korvaavaa päivää. |
| **Välin tyyppi: Toistuu aloituspäivämäärästä** – Laskuri alkaa käyttöomaisuussuhteen alkamispäivämäärästä. Päivämäärä valitaan kohdassa **Kaikki resurssit** \> **Resurssien ylläpitosuunnitelmat** -pikavälilehti \> **Aloituspäivämäärä** -kenttä tai kohdassa **Kaikki toiminnalliset sijainnit** \> **Ylläpitosuunnitelmat**-pikavälilehti \> **Aloituspäivämäärä** -kenttä. Kun ajoitat huoltosuunnitelmia, huoltoaikataulurivi luodaan, kun aikaväli saavutetaan. | Käyttöomaisuuserän tai toimipaikan huoltosuunnitelmarivin aloituspäivää käytetään. Jos tämä kenttä on tyhjä, käytetään ylläpitosuunnitelman **Suunnitelman päivämäärä** -päivämäärää. | Käyttöomaisuuserän tai toimipaikan huoltosuunnitelmarivin aloituspäivää käytetään. Jos tämä kenttä on tyhjä, käytetään ylläpitosuunnitelman **Suunnitelman päivämäärä** -päivämäärää. |
| **Välin tyyppi: toistuu viimeisestä työtilauksesta** – Laskuri alkaa viimeisimmän työtilauksen päättymispäivämäärästä ja-ajasta, joka suoritettiin käyttöomaisuuserälle ja tämän tietyn kunnosapitotyön tyypin, kunnossapitotyön tyypin variantin ja toimialan yhdistelmälle. Tämä päivämäärä ja kellonaika näkyvät **Kaikki työtilaukset** -näkymän **Toteutunut lopetus** -kentässä. | Käyttöomaisuuserälle tehdyn työtilauksen todellinen päättymispäivä ja -aika ja tietyn kunnossapitotyön tyypin / kunnossapitotyön tyypin variantin / toimialan yhdistelmä. Jos suoritettua työtilausta ei löydy, käytetään sen sijaan jotakin edellä kuvatun "Toistetään aloituspäivämäärästä" -aikavälityyppiä. | Käyttöomaisuuserälle tehdyn työtilauksen todellinen päättymispäivä ja -aika *ja* kunnossapitotyön tyypin / kunnossapitotyön tyypin variantin / toimialan yhdistelmä. käytetään. Jos työtilauksen loppupäivämäärä ja -aika on jätetty tyhjäksi, käytetään sen sijaan jotakin edellä kuvatun "Toistetään aloituspäivämäärästä" -aikavälityyppiä. |
| **Välin tyyppi: Kerran suunnitelman päivämäärästä** – Katso yllä olevan "Toistetaan suunnitelman päivämäärästä" -välityypin kuvaus. Ainoa ero on se, että tätä aikavälityyppiä käytetään vain kerran. | Katso edellä oleva "Toistetaan suunnitelman päivämäärästä"-välityypin kuvaus. Tätä väliä käytetään yleensä kertaylläpito- tai kertahuoltotöissä. | Katso edellä oleva "Toistetaan suunnitelman päivämäärästä"-välityypin kuvaus. Tätä väliä käytetään yleensä kertaylläpito- tai kertahuoltotöissä. **Huomautus 1:** Tämä välityyppi on merkityksellinen vain, jos laskuri korvataan aina, kun suoritat huoltotyön. Jos laskuri on jostain syystä korvattu ennen suunnitellun aikavälin loppumisaikaa, työlle lasketaan uusi aika laskurin korvaamisen ajalta. **Huomautus 2:** Jos laskuri korvataan huoltotyötä suoritettaessa, tämä aikavälityyppi toimii kuten edellä kuvattu Toistetaan suunnitelman päivämäärästä -tyyppi. |
| **Välin tyyppi: Kerran aloituspäivämäärästä** – Katso yllä olevan "Toistetään aloituspäivämäärästä" -välityypin kuvaus. Ainoa ero on se, että tätä aikavälityyppiä käytetään vain kerran. | Katso edellä oleva "Toistetään aloituspäivämäärästä"-välityypin kuvaus. Tätä väliä käytetään yleensä kertaylläpito- tai kertahuoltotöissä. | Katso edellä oleva "Toistetään aloituspäivämäärästä"-välityypin kuvaus. Tätä väliä käytetään yleensä kertaylläpito- tai kertahuoltotöissä. **Huomautus 1**: yllä oleva koskee myös tätä aikavälin tyyppiä. **Huomautus 3:** Jos laskuri korvataan huoltotyötä suoritettaessa, tämä aikavälityyppi toimii kuten edellä kuvattu Toistetään aloituspäivämäärästä -tyyppi. |
| **Aikavälin tyyppi: Kerran, kun ylittää** – Tämä aikavälityyppi koskee vain laskureita ja sitä käytetään huoltosuunnitelmarivillä määritetyn ylärajan ilmaisemiseen. Ylläpitoaikataulumerkinnöissä on odotettu laskurin alkamispäivämäärä ja -aika, mikä tarkoittaa, että nämä tapahtumat luodaan siten, että odotettu alkamispäivämäärä on sama tai aikaisempi kuin järjestelmän päivämäärä. | Ei käytettävissä | Laskuriväli ilmaisee ylärajan. Jos raja ylittyy, kun luot laskurikirjauksen, huoltoaikataulurivi luodaan, kun ajoitat ennaltaehkäisevän huollon. |
| **Aikavälin tyyppi: Kerran, kun alittaa** – Tämä aikavälityyppi koskee vain laskureita ja sitä käytetään huoltosuunnitelmarivillä määritetyn alarajan ilmaisemiseen. Ylläpitoaikataulumerkinnöissä on odotettu laskurin alkamispäivämäärä ja -aika, mikä tarkoittaa, että nämä tapahtumat luodaan siten, että odotettu alkamispäivämäärä on sama tai aikaisempi kuin järjestelmän päivämäärä. | Ei käytettävissä | Laskuriväli ilmaisee alarajan. Jos raja alittuu, kun luot laskurikirjauksen, huoltoaikataulurivi luodaan, kun ajoitat ennaltaehkäisevän huollon. |
| **Aikavälin tyyppi: Linkitetty aloituspäivämäärästä** tämä aikavälityyppi luo ylläpitoaikataulurivin vain kerran. Huoltosuunnitelma voi sisältää useampia huoltosuunnitelmarivejä käyttäen tätä aikavälityyppiä, ja nämä rivit on linkitetty. Yleensä luodaan huoltosuunnitelma, joka sisältää vain tämän aikavälityypin rivit. Huoltoaikataulurivit luodaan määrittämällä huoltosuunnitelman rivi, jolla on ensimmäinen odotettu alkamispäivämäärä ja -aika. | Katso edellä oleva "Kerran aloituspäivämäärästä"-välityypin kuvaus. Esimerkki: Luot huoltosuunnitelmassa kaksi riviä auton huoltotyötä varten: yksi aika-pohjainen rivi, jossa on 1 vuoden kausi, ja yksi laskuripohjainen rivi, jonka raja on 25 000 km. Huoltoaikataulurivi luodaan ensin saavutettavalle rajalle. Tälle rivityypille luodaan rivi, jolla on 1 vuoden kausi. | Katso edellä oleva "Kerran aloituspäivämäärästä"-välityypin kuvaus. Esimerkki: Luot huoltosuunnitelmassa kaksi riviä auton huoltotyötä varten: yksi aika-pohjainen rivi, jossa on 1 vuoden kausi, ja yksi laskuripohjainen rivi, jonka raja on 25 000 km. Huoltoaikataulurivi luodaan ensin saavutettavalle rajalle. Tälle rivityypille luodaan rivi, jolla on 25 000 kilometrin raja. Esimerkki kahden laskuririvin luomisesta: Voit myös määrittää ylläpitosuunnitelman, jossa on kaksi linkitettyä laskuripohjaista riviä, joilla ensimmäisen rivin raja 10 000 tuotettua nimikettä, ja toinen rivi liittyy koneeseen tai kuormituspaikkaan, joka edellyttää huoltoa 3 000 tunnin käytön jälkeen. |
| **Aikavälin tyyppi: linkitetty viimeisestä työtilauksesta** Tämä välityyppi luo uusia ylläpitoaikataulurivejä jokaisen valmiin työtilauksen jälkeen. Huoltosuunnitelma voi sisältää useampia rivejä käyttäen tätä aikavälityyppiä, ja nämä rivit on linkitetty. Yleensä luodaan huoltosuunnitelma, joka sisältää vain tämän aikavälityypin huoltosuunnitelmarivit. Huoltoaikataulurivit luodaan määrittämällä huoltosuunnitelman rivi, jolla on ensimmäinen odotettu alkamispäivämäärä ja -aika. | Tämä aikaväli tyyppi toimii edellä kuvatulla Linkitetty aloituspäivämäärästä -tyypin tavalla. Ainoa ero on aikavälityypin perustana oleva päivämäärä. Käytettävä päivämäärä on käyttöomaisuuserälle tehdyn viimeisimmän työtilauksen todellinen valmistumispäivä ja -aika *ja* kunnossapitotyön tyypin / kunnossapitotyön tyypin variantin / toimialan yhdistelmä. | Tämä aikaväli tyyppi toimii edellä kuvatulla Linkitetty aloituspäivämäärästä -tyypin tavalla. Ainoa ero on aikavälityypin perustana oleva päivämäärä. Käytettävä päivämäärä on käyttöomaisuuserälle tehdyn viimeisimmän työtilauksen todellinen valmistumispäivä ja -aika *ja* kunnossapitotyön tyypin / kunnossapitotyön tyypin variantin / toimialan yhdistelmä. |
| **Välin tyyppi: toistetaan koostetussa arvossa (vain laskuri)** Kun ylläpitosuunnitelma suoritetaan, aikataulutettu ylläpitorivi luodaan joka kerta, kun resurssilaskuri koostettu arvo saavuttaa kausivälin tai useita kausivälejä. (Kausiväli määritetään ylläpitosuunnitelman rivillä.)<p>Lisätietoja tämän toiminnon käyttöönotosta ja käyttämisestä on myöhemmin tässä aiheessa kohdassa [Laskuripohjaiset ylläpidon parannukset](#counter-based-maintenance). | Ei käytettävissä | **Esimerkki:** Tuntilaskuri on määritetty resurssille AK-101. Resurssille on lisäksi määritetty resurssisuunnitelma. Tämän rivin välin tyyppi on *Toistetaan koostetun arvon mukaan (vain laskuri)* ja kausiväli on *1 000*. Ylläpitosuunnitelmaa suoritettaessa aikataulutettu ylläpitorivi luodaan, kun laskurin koostettu arvo ylittää 1 000 tuntia. Kun laskurin koostettu arvo ylittää 2 000 tuntia, toinen aikataulutettu ylläpitorivi luodaan. Näin jatketaan kunkin seuraavan 1 000 tunnin osalta. |
| **Välin tyyppi: Kerran koostetun arvon perusteella (vain laskuri)** Kun ylläpitosuunnitelma suoritetaan, aikataulutettu ylläpitorivi luodaan, kun resurssilaskurin koostettu arvo saavuttaa ylläpitosuunnitelman rivillä määritetyn kausivälin.<p>Lisätietoja tämän toiminnon käyttöönotosta ja käyttämisestä on kohdassa [Laskuripohjaiset ylläpidon parannukset](#counter-based-maintenance). | Ei käytettävissä | **Esimerkki:** Tuntilaskuri on määritetty resurssille AK-101. Resurssille on lisäksi määritetty resurssisuunnitelma. Tämän rivin välin tyyppi on *Kerran koostetun arvon perusteella (vain laskuri)* ja kausiväli on *1 000*. Ylläpitosuunnitelmaa suoritettaessa aikataulutettu ylläpitorivi luodaan, kun laskurin koostettu arvo ylittää 1 000 tuntia. |

>[!NOTE]
>Kun huoltoaikataulurivit luodaan aikaperustaisille ylläpitosuunnitelmariveille, odotettu aika on aina päivän alussa. Laskuripohjaisille ylläpitosuunnitelmariveille odotettu aika voi olla milloin tahansa päivän aikana.

Alla on esimerkkejä aikapohjaisten ja laskuripohjaisten ylläpitosuunnitelmarivien asetuksista:

**Esimerkki 1 – aikapohjainen huoltosuunnitelma rivi:** Voitelutyö voidaan määrittää säännöllisin kiintein väliajoin, kerran viikossa. Tätä tarkoitusta varten valitse **Välin tyyppi** -kentässä "Toistetaan suunnitelman päivämäärästä". Katso esimerkki seuraavasta kuvasta.

![Määritetyllä palvelutyöllä on kiinteä esiintymisväli kerran viikossa](media/02-preventive-maintenance.png "Määritetyllä palvelutyöllä on kiinteä esiintymisväli kerran viikossa")

**Esimerkki 2 – aikapohjainen huoltosuunnitelmarivi:** Tarkastustyö voidaan määrittää tehtäväksi noin kerran viikossa. Tätä tarkoitusta varten valitse **Välin tyyppi** -kentässä "Toistetaan viimeisestä työtilauksesta". Katso esimerkki seuraavasta kuvasta.

![Noin kerran viikossa tehtäväksi määritetty tarkastustyö](media/03-preventive-maintenance.png "Noin kerran viikossa tehtäväksi määritetty tarkastustyö")

**Esimerkki 3 – laskuripohjainen ylläpitosuunnitelmarivi:** Seuraavassa kuvassa on tuntilaskuri, jolle uusi huoltoaikataulurivi luodaan joka kerta, kun 250 tuntia on kulunut. Tämän laskuripohjaisen rivin välityyppi on "Toistetään aloituspäivämäärästä". Aloituspäivämäärä on liittyvien resurssien aloituspäivämäärä kohdassa **Kaikki resurssit** \> **Resurssien ylläpitosuunnitelmat** -pikavälilehti \> **Aloituspäivämäärä**-kenttä tai kohdassa **Toiminnallinen sijainti** \> **Ylläpitosuunnitelmat** -pikavälilehti \> **Aloituspäivämäärä**-kenttä. Tämä on esimerkki *ennaltaehkäisevästä* huoltosuunnitelmasta, koska huoltoaikataulurivi luodaan automaattisesti aina, kun kynnysarvo (+ 250) saavutetaan.

![Säännöllisesti ylläpitosuunnitelman rivit luova tuntilaskuri](media/04-preventive-maintenance.png "Säännöllisesti ylläpitosuunnitelman rivit luova tuntilaskuri")

**Esimerkki 4 – laskuripohjainen huoltosuunnitelmarivi:** Seuraavassa kuvassa on laskuriarvon vähennys, joka mittaa jarrupalojen kulumista. Huoltoaikataulurivi luodaan, kun jarrupalalle luodaan laskurikirjaus, joka on alle 20 millimetriä. Tämän laskuripohjaisen rivin aikavälityyppi on "Kerran, kun alittaa" tai "Kerran viimeisestä aloituspäivämäärästä". Tämä on esimerkki *reaktiivisesta* huoltosuunnitelmasta, koska huoltoaikatauluriviä ei luoda ennen kuin rekisteröidään alle 20 mm mittaus rekisteröidään.

![Jarrupalojen kulumista mittaava laskuriarvon vähennys](media/05-preventive-maintenance.png "Jarrupalojen kulumista mittaava laskuriarvon vähennys")

**Esimerkki 5 – Laskuripohjainen ylläpitosuunnitelmarivi:** Seuraavassa kuvassa on laskuri, jonka raja on -18°C. Huoltoaikataulu rivi luodaan, kun laskurikirjaus on tehty yli -18 celsiusasteen mittauksesta. Tämän laskuripohjaisen rivin välityyppi on "Kerran, kun ylittää". Tämä on esimerkki *reaktiivisesta* huoltosuunnitelmasta, koska huoltoaikatauluriviä ei luoda ennen kuin rekisteröidään yli -18°C mittaus rekisteröidään.

![Laskuri, jonka raja on –18 °C](media/06-preventive-maintenance.png "Laskuri, jonka raja on –18 °C")

- Kun luot uuden käyttöomaisuuserän ja käyttöomaisuuserä käyttää huoltosuunnitelmaan liittyvää käyttöomaisuustyyppiä, ylläpitosuunnitelma lisätään automaattisesti **Kaikki objektit \> Resurssien ylläpitosuunnitelmat** -pikavälilehteen. **Ylläpitosuunnitelmat**-pikavälilehden **Resurssin oletustyypit** -kohtaan lisätään automaattisesti liittyvät huoltosuunnitelmat.
- Jos lisäät tai poistat käyttöomaisuustyyppejä tai toiminnallisia sijaintityyppejä kohdassa **Ylläpitosuunnitelmat**, muutos vaikuttaa vain uusiin resurssiehin, jotka on luotu muutoksen tekemisen jälkeen.
- Jos lisäät tai poistat käyttöomaisuuseriä tai toiminnallisia sijainteja **Ylläpitosuunnitelmat**-kohdassa, tämä muutos päivitetään automaattisesti **Kaikki resurssit \> Resurssien ylläpitosuunnitelmat** -pikavälilehteen tai **Kaikki toiminnalliset sijainnit \> Ylläpitosuunnitelmat** -pikavälilehteen.

Seuraavassa kuvassa on esimerkki **Ylläpitosuunnitelmat**-sivun "Truck service" -nimisestä huoltosuunnitelmasta.

![Esimerkki kuorma-auton huollon ylläpitosuunnitelmasta](media/07-preventive-maintenance.png "Esimerkki kuorma-auton huollon ylläpitosuunnitelmasta")

## <a name="add-a-maintenance-plan-to-an-asset"></a>Huoltosuunnitelman lisääminen resurssiin

1. Valitse **Resurssien hallinta \> Yhteiset \> Resurssit \> Kaikki resurssit** tai **Aktiiviset resurssit**.

1. Valitse resurssi, jolle haluat määrittää ylläpitosuunnitelman, ja valitse sitten **Muokkaa.**

1. Lisää ylläpitosuunnitelma resurssiin valitsemalla **Resurssien ylläpitosuunnitelmat**-pikavälilehdessä **Lisää rivi**.

1. Valitse asianmukainen kunnossapitosuunnitelma **Ylläpitosuunnitelma** -kentässä.

1. Valitse **Aloituspäivämäärä** -kentässä päivämäärä, josta lähtien ennaltaehkäisevien ylläpitotöiden suunnittelu voidaan tehdä. 

1. Valitse **Tallenna**. **Aktiivinen**-kenttä päivittyy automaattisesti.

Seuraavassa kuvassa on esimerkki **Kaikki resurssit**-sivulla resurssille määritetyistä huoltosuunnitelmista.

![Esimerkki resurssille määritetyistä ylläpitosuunnitelmista](media/08-preventive-maintenance.png "Esimerkki resurssille määritetyistä ylläpitosuunnitelmista")

<a id="counter-based-maintenance"></a>

## <a name="counter-based-maintenance-enhancements"></a>Laskuripohjaiset ylläpidon parannukset

> [!IMPORTANT]
> Tässä osassa kuvatut toiminnot ovat saatavana esiversion osana. Sisältö ja toiminnot voivat muuttua. Lisätietoja ennakkojulkaisusta on kohdassa [One Version -palvelupäivitysten usein kysytyt kysymykset](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).

*Laskuripohjaiset ylläpidon parannukset* -toiminto ottaa käyttöön seuraavat toiminnallisuudet:

- Mahdollisuus lisätä resurssin luonnin yhteydessä automaattisesti laskuri, jonka arvo on *0* (nolla). Tämä vaihtoehto voi olla kätevä, kun käytössä on laskureihin perustuva ennakoiva ylläpito. *Jos Laskuripohjaiset ylläpidon parannukset* -toimintoa ei käytetä ja laskurin arvo on *0* (nolla), se on lisättävä manuaalisesti.
- Mahdollisuus määrittää laskuri siten, että se nollautuu automaattisesti, kun työtilaus on valmis. Tämä toiminto on kätevä, jos ylläpidon aikataulutukseen käytetään viimeisen työtilauksen valmistumisen jälkeistä koostettua arvoa.
- Uuden ylläpitosuunnitelman esiintymisvälin tyyppi on *Toistetaan koostetun arvon mukaan (vain laskuri)*. Tämä tyyppi käynnistää ylläpidon aina, kun koostettu laskuri saavuttaa määritetyn arvon kerrannaisen. Huolto voidaan esimerkiksi käynnistää 10 000 tunnin välein. Lisätietoja on tämän ohjeaiheen edellä olevassa kohdassa [Välityyppien yleiskuvaus](#interval-types).
- Toinen uusi ylläpitosuunnitelman välityyppi on *Kerran koostetun arvon perusteella (vain laskuri)*. Tämä tyyppi käynnistää ylläpidon, kun koostettu laskuri saavuttaa määritetyn arvon, kuten 8 000 tuntia. Lisätietoja on kohdassa [Välityyppien yleiskuvaus](#interval-types).

### <a name="turn-on-the-counter-based-maintenance-enhancements-feature"></a>Laskuripohjaiset ylläpidon parannukset -toiminnon ottamine käyttöön

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Resurssien hallinta*
- **Toiminnon nimi:** *(Esiversio) Laskuripohjaiset ylläpidon parannukset*

### <a name="create-and-initialize-counters-when-an-asset-is-created"></a>Laskurien luominen ja alustaminen resurssia luotaessa

Aina kun resurssi luodaan, liittyvät resurssilaskurit, joiden alustava arvo on *0* (nolla), voidaan luoda automaattisesti, mikäli järjestelmä on määritetty ja resurssi luodaan oikein.

1. Valitse **Resurssien hallinta \> Asetukset \> Resurssityypit**.
1. Varmista, että käytössä on suunniteltuun uuteen resurssiin soveltuva resurssityyppi. Luo resurssityyppi tarvittaessa. Varmista, että kaikki asianmukaiset laskurit valitaan **Laskurit**-pikavälilehdessä.
1. Valitse **Resurssien hallinta \> Asetukset \> Resurssityypit \> Laskurit**.
1. Varmista kussakin liittyvässä laskurissa, että **Yhteenlaskettu summa** -kentän määrityksenä on *Summa*.
1. Luo resurssi **Kaikki resurssit** -sivulla.
1. Määritä **Resurssityyppi**-kenttään resurssityyppi, joka määritettiin tai luotiin vaiheessa 2.
1. Viimeistele uuden resurssin määritys tarpeen mukaan.
1. Valitse **Resurssien hallinta \> Kyselyt \> Resurssit \> Laskurit**. Uudelle resurssille määritettyjen alustettujen laskurien pitäisi olla nyt löydettävissä.

> [!NOTE]
> Alustetuissa resurssilaskureissa oletuksena on, että resurssia ei ole koskaan käytetty ennen sen lisäämistä järjestelmään. Kun ylläpitosuunnitelma suoritetaan ensimmäisen kerran, laskelma käyttää päivämäärään ja laskurin arvoa *0* (nolla) perusarvona tulevan ylläpidon laskemiseen. Jos järjestelmään lisätty resurssi ei ollut uusi, laskurin arvo voidaan säätää manuaalisesti vastaamaan todellista laskurin arvoa. Laskurin arvoa säädetään avaamalla kyseine resurssi **Kaikki resurssit** -sivulla ja valitsemalla sitten toimintoruudun **Resurssi**-välilehden **Ehkäisevä**-ryhmässä **Laskurit**. Säädä valitun resurssin **Resurssilaskurit**-sivulla tarpeen mukaan arvoa, joka on ensimmäisen laskuritietueen **Arvo**-sarakkeessa.

### <a name="automatically-reset-a-counter-value"></a>Laskurin arvon automaattinen nollaus

Järjestelmä voidaan määrittää nollaamaan laskuri automaattisesti aina, kun liittyvä työtilaus saavuttaa valitun tila-arvon.

1. Valitse **Resurssien hallinta \> Asetukset \>Ennalta ehkäisevä ylläpito \>Ylläpitosuunnitelmat**.
1. Valitse luetteloruudussa ylläpitosuunnitelma. Laskurin nollaus koskee kaikkia tätä suunnitelmaa käyttäviä resursseja.
1. Etsi **Rivit**-osassa se resurssilaskurin rivi, jonka laskuri halutaan nollata, ja valitse kyseisen rivin **Nollaa laskuri** -valintaruutu. (Resurssilaskurin rivien arvo on **Laskuri**-sarakkeessa. Kyseisessä sarakkeessa määritetty laskuri on laskuri, joka nollataan liittyvän resurssin osalta.)
1. Valitse **Resurssien hallinta \> Asetukset \> Työtilaukset \> Elinkaaren tilat**.
1. Valitse luetteloruudussa se työtilauksen elinkaaren tila, jonka liittyvä laskuri on nollattava.
1. Määritä **Yleinen**-pikavälilehden **Nollaa laskuri** -asetukseksi *Kyllä*.
