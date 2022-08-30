---
title: Ennakoivat laatupäivitykset
description: Tässä artikkelissa on tietoja laatupäivitysten ennakoivasta toimituksesta.
author: rashmansur
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9d81cb15e9a127e7bea7ad9b5e0f50a1ee543f71
ms.sourcegitcommit: 78e85ad49634cd31459fdb7325cb273352bf1501
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9338133"
---
# <a name="proactive-quality-updates"></a>Ennakoivat laatupäivitykset

[!include[banner](../includes/banner.md)]

Microsoft on parantanut jatkuvasti [One Versionia](../../dev-itpro/lifecycle-services/oneversion-overview.md) viimeisten seitsemän vuoden aikana. One Versionin toimintaperiaate on yksinkertainen: mitä suurempi osa asiakkaista käyttää samaa ohjelmistoversiota, sitä laadukkaampaa palvelua heille voidaan tarjota. Ongelmat löytyvät ja ne ratkaistaan kerran, ja ratkaisut voidaan toimittaa useille asiakkaille nopeasti.

Tulokset todistavat tämän hyväksi toimintaperiaatteeksi: tuotteissa on aiempaa vähemmän virhetapauksia. Jos asiakkailla on käytössä eri sovellusversioita, sovelluksissa esiintyy ongelmia, joihin on jo olemassa ratkaisut. Dynamics 365 Financea, Dynamics 365 Supply Chainia, Dynamics 365 Project Operationsia ja Dynamics 365 Commercea on jo parannettu. Uusien teknisten toimintojen ansiosta nyt on mahdollista ottaa seuraava askel. Alla on tietoja siitä, mitä Microsoft tulee tekemään jatkossa, mitä on jo tehty ja miten ja milloin uudet, häiriöittä toimivat ominaisuudet esitellään.

## <a name="focus-on-quality-updates"></a>Laatupäivityksiin keskittyminen

Tällä hetkellä [palvelupäivityksiä](public-preview-releases.md) on vuodessa seitsemän. Esimerkiksi versio 10.0.29 on palvelupäivitys. Tätä ennen päivityksiä oli vuodessa kahdeksan. Yksi päivitys kuitenkin jätettiin pois asiakaspalautteen vuoksi. Palautteessa toivottiin, että kalenterivuoden lopussa ei tehtäisi muutoksia.

Palvelupäivitysten väliä ei tulla muuttamaan. Sen sijaan One Version -siirtymän seuraavassa vaiheessa keskitytään *laatupäivityksiin*. Laatupäivitykset ovat kumulatiivisia hotfix-korjausten koontiversioita. Ne eivät sisällä uusia ominaisuuksia. Ajankohdasta riippumatta koko asiakaskunta voi saada kolme tai neljä uusinta palvelupäivitystä. Kaikissa palvelupäivityksissä voidaan käyttää kymmeniä eri laatupäivitysversioita käyttöönottopäivämäärien mukaan ryhmän sisällä. Seuraavassa vaiheessa laatupäivitykset lähetetään ennakoivasti. Tätä mallia käytetään jo Dataverse-perustaisissa sovelluksissa, joissa laatu on parantunut ja tukitapausten määrä vähentynyt.

Virheiden väheneminen voi vähentää laatupäivitysten tarvetta tai poistaa ne kokonaan. Meneillään on useita hankkeita palvelupäivityksiä vaativien virheiden vähentämiseksi. Vaikka palvelupäivitysten tietoja vähennetään, asiakasperustan yhdenmukaisuus parantaa tukea ja asiakkaat saavat parannukset aiempaa nopeammin. Asiakkaat eivät myöskään löydä virheitä niin usein, koska ongelmia on jo ratkaistu.

## <a name="making-proactive-distribution-possible"></a>Ennakoivan jakelun mahdollistaminen

Seuraavia laatupäivitysten ennakoivan toimittamisen mahdollistavia toimintoja on jo otettu käyttöön:

- **Päivittäminen niin, että käyttämättömyysaika on lähes nolla** – Jos haluat toimittaa päivityksiä ympäristöihin säännöllisesti, on tärkeää, että vaikutusta ympäristön käytettävyyteen pienennetään ja noudatetaan näin Dynamics 365:n palvelutasosopimuksia. Päivittäminen niin, että käyttämättömyysaika on lähes nolla, otettiin käyttöön alun perin parantamaan kuukausittaisia järjestelmäkorjauksia. Niissä käytettiin klusterin vikasietoa päivitetyn kuvan aktivoimiseksi ilman suuria häiriöitä. Päivitysten kohdistusmekanismia on parannettu niin, että se aiheuttaa vielä aiempaakin vähemmän häiriöitä ja kattaa sekä käyttöjärjestelmän korjaukset että laatupäivitysten käyttöönoton.

    Vuorovaikutteisten käyttäjien aktiivinen istunto saattaa keskeytyä, joten heidän on kirjauduttava uudelleen päivitettyyn ympäristöön. Uuden, suostumukseen perustuvan [prioriteettiin perustuvan erien ajoituksen](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md) avulla erien ajoitus ja käsittely palautuu ja jatkaa toimintoja heti päivityksen jälkeen. Prioriteettiin perustuva erien ajoitus on asiakkaiden käytettävissä ennen kuin he ottavat osaa tuotantoympäristöjen laatupäivitysten ennakoivaan jakeluun.

- **Yöaika** – Kullekin Azure-alueelle määritetään yöaika, jonka aikana tehdään päivitykset niin, että käyttämättömyysaika on lähes nolla.

## <a name="the-proactive-update-process"></a>Ennakoiva päivitysprosessi

Ennakoivien laatupäivitysten käyttöönotto noudattaa turvallista käyttöönottoprosessia. Turvallisen käyttöönottoprosessin yksityiskohdat muuttuvat, mutta laatupäivitykset otetaan ensin käyttöön eristysympäristöissä. Prosessi alkaa ympäristöistä, joissa on hyväksytty varhainen käyttöönotto. Onnistuneiden eristysympäristön käyttöönottojen prosenttiosuuden noustessa aloitetaan käyttöönotot tuotantoympäristöissä. Prosessi alkaa jälleen ympäristöistä, joissa on hyväksytty varhainen käyttöönotto. Kuuntelujärjestelmät valvovat järjestelmän telemetria- ja live-sivustotapahtumia ja lopettavat tietyn version päivittämisen, jos havaitaan regressiota. Asiakkaat voivat yhä halutessaan hakea laatupäivityksiä ennen ennakoivaa käyttöönottoa.

Nykyiset julkaisujen hallintatiedot kertovat, että vähemmän kuin 3 prosenttia regressioista tapahtuu laatupäivityksissä. Kun keskitytään regressioiden poistamiseen ja turvallisen käyttöönottoprosessin parantamiseen, regressioiden mahdollinen vaikutus on huomattavasti alhaisempi kuin laadun parantumisen aiheuttamat hyödyt, jotka saadaan korjausten nopeasta toimittamisesta asiakkaille laajasti.

## <a name="process-changes"></a>Käsittele muutokset

Prosessimuutosten joukko otetaan käyttöön ennen ennakoivan laatupäivityksen käyttöönoton aktivointia seuraavasti:

- **Rakenne** – Työkalut varmistavat, että laatupäivitysten koontiversiot sisältävät vain rakennemuutoksia, jotka voidaan ottaa käyttöön palvelun ollessa online-tilassa. Tämä menetelmä auttaa säilyttämään päivitysmahdollisuuden niin, että käyttämättömyysaika on lähes nolla.
- **Lisääntynyt muutosten tarkastelu** – Tällä hetkellä käytössä on jo uusi prosessivaihe laatupäivityksen muutosten sisällytyksen hyväksyntää varten. Lisävaiheessa tapahtuvaa sisällytystä lisätään, jotta mahdollisten regressioiden mahdollisuutta voidaan vähentää. Laatupäivitykset eivät sisällä tärkeimpiä muutoksia. Muutosten sisällytysten lisääminen varmistaa, että tämä tavoite saavutetaan.
- **Näkyvyys** – Lähetämme ilmoitukset tulevista ennakoivista laatupäivityksistä sähköpostitse ja Lifecycle Services -palvelun kautta. Lisäksi tukiryhmät ja tapahtumaliidit näkevät, missä laatupäivitykset on otettu käyttöön ennakoivasti.
- **Versiovarmistus** – Väliversiotestausta käytetään ennakoivan laatupäivityksen kaikkien muutosten ryhmittelyssä. Jos varmistusta tarvitaan ennakoivan käyttöönoton jälkeen, se voidaan tehdä väliversiotestausjärjestelmän avulla.
- **Eristysympäristön synkronoinnin määritys** – Alle 20 prosentilla asiakkaista on nykyään useita eristysympäristöjä. Asiakkailla on käytössä yksi eristysympäristö, jossa versio vastaa tuotantoa. Tämä helpottaa vianmääritystä. Lähitulevaisuudessa asiakkaat voivat määrittää eristysympäristön, joka ei vastaanota ennakoivan laatupäivityksen käyttöönottoa yhdessä muiden eristysympäristöjen kanssa, vaan se vastaanotetaan myöhemmin yhdessä tuotantoympäristön kanssa. Ota huomioon, että jos asiakas käyttää eristysympäristöä tuotantoympäristön versiota uudemman version testaamisessa, eristysympäristö vastaanottaa uuden version laatupäivityksiä.
- 
## <a name="when-will-proactive-quality-updates-start"></a>Milloin ennakoivat laatupäivitykset alkavat?

Eristysympäristöjen ennakoivien laatupäivitysten jakelun odotetaan alkavan vuoden 2022 syyskuun lopulla tai lokakuussa Azuren julkisen pilvipalvelun asiakkaille. Myös kokeiluympäristöt alkavat vastaanottaa ennakoivan päivityksen käyttöönottoja samaan aikaan. Syyskuussa kaikille asiakkaille lähetään ilmoitus heidän ympäristöjensä suunnitellusta aikataulusta. Poikkeuksia ennakoivaan päivitysjakeluprosessiin sallitaan vain FDA:n säännösten alaisille asiakkaille. Selvitämme parhaillaan, miten säänneltyjä ympäristöjä sekä maakohtaisen ja julkishallinnon pilvipalvelun asiakkaita tullaan hallinnoimaan.

Seuraavan kuuden kuukauden jakson aikana lisäämme vähittäin ennakoivia päivityksiä vastaanottavien eristysympäristöjen prosenttiosuutta, kunnes kaikki määritetyt ympäristöt on lisätty. Tämän jälkeen päivitetään tuotantoympäristöt. Koko jakson aikana valvomme, että käyttöönottoprosessi sujuu saumattomasti ja tietopaketit siirtyvät häiriöittä.

Asiakkaat vastaanottavat jatkuvasti pieniä määriä tietoja, joten ajan tasalla pysyminen on todennäköisesti aiempaa helpompaa. Muutamme päivityksen käyttöönoton väliä, kun prosessi voidaan suorittaa ilman keskeytyksiä. Tämä prosessi toimii jo tehokkaasti Dataverse-ympäristössä ja -sovelluksissa. Prosessi tuo toivottuja parannuksia palvelun laatuun. Haluamme toimia samalla tavalla talous- ja toimintosovellusten kanssa.
