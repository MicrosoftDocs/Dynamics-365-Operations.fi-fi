---
title: Ennakoivat laatupäivitykset
description: Tässä artikkelissa on tietoja laatupäivitysten ennakoivasta toimituksesta.
author: rashmansur
ms.date: 09/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 60f9d84b240016671ff726fc3cca2e02cfd811ca
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689221"
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
- **Näkyvyys** – Ilmoitukset lähetetään hallintakeskuksen, Lifecycle Servicesin (LCS) ja muiden käytettävissä olevien kanavien kautta saapuvia ennakoivia laatupäivityksiä varten. Lisäksi tukiryhmät ja tapahtumaliidit näkevät, missä laatupäivitykset on otettu käyttöön ennakoivasti.
 > [!NOTE]
 > Microsoft Communications -tiimi tutkii meneillään olevaa sähköpostityökalun heikentymistä. Se estää sähköposti-ilmoitusten toimittamisen. Jatka Microsoft 365:n viestikeskuksen seurantaa perehdyttämistä ja ilmoituksia koskevia viestejä varten.
- **Fail Safe -väliversiotestauksen avulla** – Väliversiotestausta käytetään koodimuutosten tallentamiseen laatupäivityksen ohjelmistovirheen ja korjaukseen liittyvän olemassa olevan toiminnon väliversiotestauksen aikana. Jos varmistuksen tai muutoksen poistaminen käytöstä on pakollista ennakoivan käyttöönoton jälkeen, se voidaan tehdä väliversiotestausjärjestelmän avulla muiden virheiden välttämiseksi.
- **Eristysympäristön synkronoinnin määritys** – Alle 20 prosentilla asiakkaista on nykyään useita eristysympäristöjä. Asiakkailla on käytössä yksi eristysympäristö, jossa versio vastaa tuotantoa. Tämä helpottaa vianmääritystä. Jos asiakas käyttää eristysympäristöä tuotantoympäristön versiota uudemman version testaamisessa, eristysympäristö vastaanottaa uuden version laatupäivityksiä.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Mikä on laatupäivitysten toimituksen toteutussuunnitelma?

Eristysympäristöjen ennakoivien laatupäivitysten jakelun odotetaan alkavan vuoden 2022 syyskuun lopulla tai lokakuussa Azuren julkisen pilvipalvelun asiakkaille. Myös kokeiluympäristöt alkavat vastaanottaa ennakoivan päivityksen käyttöönottoja samaan aikaan. Syyskuussa kaikille asiakkaille lähetään ilmoitus heidän ympäristöjensä suunnitellusta aikataulusta. Poikkeuksia ennakoivaan päivitysjakeluprosessiin sallitaan vain FDA:n säännösten alaisille asiakkaille. Selvitämme parhaillaan, miten säänneltyjä ympäristöjä sekä maakohtaisen ja julkishallinnon pilvipalvelun asiakkaita tullaan hallinnoimaan.

Seuraavan kuuden kuukauden jakson aikana lisäämme vähittäin ennakoivia päivityksiä vastaanottavien eristysympäristöjen prosenttiosuutta, kunnes kaikki määritetyt ympäristöt on lisätty. Tämän jälkeen päivitetään tuotantoympäristöt. Koko jakson aikana valvomme, että käyttöönottoprosessi sujuu saumattomasti ja tietopaketit siirtyvät häiriöittä.

Asiakkaat vastaanottavat jatkuvasti pieniä määriä tietoja, joten ajan tasalla pysyminen on todennäköisesti aiempaa helpompaa. Muutamme päivityksen käyttöönoton väliä, kun prosessi voidaan suorittaa ilman keskeytyksiä. Tämä prosessi toimii jo tehokkaasti Dataverse-ympäristössä ja -sovelluksissa. Prosessi tuo toivottuja parannuksia palvelun laatuun. Haluamme toimia samalla tavalla talous- ja toimintosovellusten kanssa.

## <a name="when-will-quality-updates-start-for-production-environments"></a>Milloin tuotantoympäristöjen laatupäivitykset alkavat?
Tällä hetkellä laatupäivitykset koskevat vain eristysympäristöjä. Tähän tilaan päivitetään tuotantoympäristöjen aloituspäivämäärä, kun käytettävissä on eristysympäristöjen ennakoivien päivitysten konkreettisia tietoja ja mittauksia tuotannon valmiusasteen mittaamiseksi.

## <a name="what-is-the-schedule-for-sandbox-proactive-quality-updates"></a>Mikä on eristysympäristön ennakoivien laatupäivitysten aikataulu?
Lisätietoja kunkin alueen yöajasta on kohdassa [Mitkä ovat suunnitellut ylläpitoikkunat alueen mukaan?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).

### <a name="proactive-quality-update-release-10028"></a>Ennakoiva laatupäivitysjulkaisu: 10.0.28
**Sovellusversio: 10.0.1265.89**
**Vastaava uusin tietokanta-artikkeli: 745340**

| Asema | Alueet | Valmis aikataulu| Tuleva eristysympäristön aikataulu
|---|---|---|---|
| Asema 1 | Kanada - keskinen, Kanada - itäinen, Ranska - keskinen, Intia - keskinen, Norja - itäinen, Sveitsi - läntinen | 15.-18. syyskuuta 2022, 19.-22. syyskuuta 2022 ja 7.-10. lokakuuta 2022 | 25.–28. lokakuuta 2022 |
| Asema 2 | Ranska - etelä, Intia - etelä, Norja - länsi, Sveitsi - pohjoinen, Etelä-Afrikka - pohjoinen, Australia - itä, Yhdistynyt kuningaskunta - etelä, Yhdistyneet arabiemiirikunnat - pohjoinen, Japani - itä, Australia - koillinen, Kaakkois-Aasia | 25.–28. syyskuuta 2022 ja 7.–10. lokakuuta 2022 | 25.–28. lokakuuta 2022 |
| Asema 3 | Itä-Aasia, Yhdistynyt kuningaskunta - länsi, Japani - länsi, Brasilia - etelä, Länsi-Eurooppa, Itä-Yhdysvallat, keskinen Yhdistyneet arabiemiirikunnat | 26.–29. syyskuuta 2022 ja 7.–10. lokakuuta 2022 | 25.–28. lokakuuta 2022 |
| Asema 4 | Pohjois-Eurooppa, Keski-Yhdysvallat, Länsi-Yhdysvallat | 28. syyskuuta - 1. lokakuuta 2022 ja 7.–10. lokakuuta 2022 | 25.–28. lokakuuta 2022 |
| Asema 5 | DoD, Government Community Cloud , Kiina | Ei suunniteltu | Ei suunniteltu |

### <a name="proactive-quality-update-release-10029"></a><a name="schedule"></a>Ennakoiva laatupäivitysjulkaisu: 10.0.29
**Sovellusversio: 10.0.1326.70**
**Vastaava uusin tietokanta-artikkeli: 748926**

| Asema | Alueet | Tuleva eristysympäristön aikataulu
|---|---|---|
| Asema 1 | Kanada - keskinen, Kanada - itäinen, Ranska - keskinen, Intia - keskinen, Norja - itäinen, Sveitsi - läntinen | 14.–17. lokakuuta 2022 |
| Asema 2 | Ranska - etelä, Intia - etelä, Norja - länsi, Sveitsi - pohjoinen, Etelä-Afrikka - pohjoinen, Australia - itä, Yhdistynyt kuningaskunta - etelä, Yhdistyneet arabiemiirikunnat - pohjoinen, Japani - itä, Australia - koillinen, Kaakkois-Aasia | 15.–18. lokakuuta 2022 |
| Asema 3 | Itä-Aasia, Yhdistynyt kuningaskunta - länsi, Japani - länsi, Brasilia - etelä, Länsi-Eurooppa, Itä-Yhdysvallat, keskinen Yhdistyneet arabiemiirikunnat | 16.–19. lokakuuta 2022 |
| Asema 4 | Pohjois-Eurooppa, Keski-Yhdysvallat, Länsi-Yhdysvallat | 17.–20. lokakuuta 2022 |
| Asema 5 | DoD, Government Community Cloud , Kiina | Ei suunniteltu |

> [!IMPORTANT] 
> Microsoft päivittää edellisen aikataulun viisi päivää etukäteen ja lähettää sähköposti-ilmoitukset niille ympäristöille, jotka on ajoitettu vastaanottamaan nämä laatupäivitykset. Edellinen aikataulu koskee vain ympäristöjä, joille on ilmoitettu tulevasta päivityksestä. Lisätietoja kunkin alueen yöajasta on kohdassa [Mitkä ovat suunnitellut ylläpitoikkunat alueen mukaan?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).
>
> Aikataulussa on neljän päivän aikavälejä jokaiselle alueryhmälle tai *asemalle*, jossa laatupäivitys on nyt ajoitettuna käyttöönottoa varten. Laatupäivitykset alkavat ensin eristysympäristöissä. Tämän jälkeen onnistuneiden eristysympäristön käyttöönottojen prosenttiosuuden noustessa aloitetaan käyttöönotot tuotantoympäristöissä. Asiakkaille lähetetään ennakkoilmoitukset.
> 
> Laatupäivitykset tehdään aina niin, että päivitys tehdään halutuissa ympäristöissä aikataulun mukaan. Ympäristöjen päivitykset saadaan valmiiksi kussakin asemassa neljännen päivän lopussa. Tämä ei kuitenkaan tarkoita sitä, että ympäristön päivitys kestää neljä päivää. Tämä tarkoittaa sitä, että etukäteen ei voi määrittää, mikä ympäristöjoukko päivitetään tiettynä päivänä neljän päivän aikavälin aikana. Kaikki päivitykset tehdään yöaikana niin, että käyttämättömyysaika on lähes nolla. Päivitykset päättyvät tietyn alueen yöaikaikkunan aikana.

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Miten yöaikaa käsitellään, jos asiakkailla on yksi talous- ja toimintosovellusten esiintymä, mutta ne ovat aktiivisia useilla aikavyöhykkeillä? 
Yöajan ulkopuolella ei ole erityisiä aikatauluja talous- ja toimintosovellusten esiintymää varten, koska laatupäivitykset tullaan ottamaan käyttöön mahdollisimman vähäisin häiriöin [nZDT:n](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean) avulla.

## <a name="what-is-the-current-rollout-cadence-for-proactive-quality-updates"></a>Mikä on ennakoivien laatupäivitysten nykyinen käyttöönottoväli?
Ennakoivat laatupäivitykset toimitetaan tällä hetkellä kerran kuukaudessa jokaiselle huoltopäivityksen tuetulle versiolle. Valituille eristysympäristöille tehdään kuukaudessa vain yksi päivitys, ellei asiakas siirry uuteen huoltopäivitysversioon. Tällöin he voivat saada esiajoitetun ennakoivan laatupäivityksen uuden huoltopäivityksen olemassa olevana julkaisujonona. Kun maailmanlaajuinen käyttöönotto on valmis vuonna 2023, näiden päivitysten toistumistiheys kasvaa. Ilmoituksia lähetetään aina vähintään yksi kuukaudessa, jos toimitusväliin tulee muutoksia.

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Miten Microsoft varmistaa päivitysten laadun?
Microsoft pyrkii pitämään julkaisuputken riittävän tehokkaana, jotta pienten tietomäärien toimittaminen onnistuu vahvistuskustannusten pitämiseksi alhaisina. Laatupäivityksen jokainen korjaus käsitellään täsmällisessä ja turvallisessa käyttöönottoprosessissa, joka parantaa laatua ja luotettavuutta vähentäen näin asiakkaan järjestelmään tehtäviä muutoksia. Käyttöönotto tapahtuu ensin vaiheissa eristysympäristössä ja sitten tuotantoympäristössä. Vaiheittain tehtävien käyttöönottojen avulla voidaan valvoa, että käyttöönoton jatkaminen on turvallista. Käyttöönotto pysäytetään, jos käyttöönoton asiakasryhmissä havaitaan ongelmia. Näin voidaan myös varmistaa, että käyttöönoton jokaisessa vaiheessa on riittävästi aikaa ongelmien löytymiselle. Jokaisessa tulevassa laatupäivityksessä on näkyvyys aikatauluun julkisissa ohjeissa ja sähköposteissa. Näiden avulla asiakkaat voivat suunnitella tulevaa toimintaa.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Voivatko asiakkaat viivyttää, ajoittaa uudelleen tai keskeyttää laatupäivityksen?
Ei Laatupäivitysten tärkein tavoite on varmistaa, että asiakkaiden käytettävissä olevat perusominaisuudet kuten tietosuoja, yksityisyys, luotettavuus, saatavuus ja suorituskyky paranevat jatkuvasti. Jos päivitystä viivytetään tai jos se keskeytetään, tietosuoja, saatavuus ja luotettavuus voivat olla vaarassa.

## <a name="how-do-i-know-what-set-of-changes-went-into-a-quality-update-payload"></a>Miten tiedän, mikä muutosjoukko laatupäivityksen tiedoissa on?
Seuraavat vaiheet ovat tilapäinen ratkaisu, sillä selvitämme jatkamme aiempaa paremman ratkaisun etsimistä määrittääksemme niiden muutosten luettelon, jotka siirtyvät laatupäivityksen tietoihin. 

Käytä laatupäivityksen julkaisujonon tietopankkia numero 745340 ja liittyvää sovellusversiota 10.0.1265.89.

1. Avaa LCS:ssä eristysympäristön **Ympäristön tiedot** -sivu. 
2. Valitse **Käytettävissä olevat päivitykset** -osassa uusimman laatupäivityksen koontiversion **Näytä päivitys** -kohta. 
3. Vie koontiversio CSV- tai Microsoft Excel -tiedostoon.
4. Lajittele viedyn tiedoston tiedot ajan perusteella (vanhin ensimmäisenä) ja hae sitten tietopankin numeroa 745340 **Päivitystunnus**-sarakkeessa. Näkyvissä on nyt tietopankkien deltaluettelo.
 
 > [!NOTE]
 > Vienti CSV- tai Excel-tiedostoon on tehtävä, ennen kuin ympäristö päivitetään. Muussa tapauksessa voit käyttää ympäristöä samanlaisilla määrityksellä, johon ei ole asennettu päivitystä, ja noudattaa yllä olevia ohjeita.

[![Esimerkki ympäristöstä ja laatupäivityksestä.](./media/how-to-get-kb-list-pqu.png)](./media/how-to-get-kb-list-pqu.png)

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Millainen prosessi vaaditaan, jos laatupäivityksen jälkeen löytyy kriittinen ongelma?
Kriittinen ongelma tai regressio on yksi tapahtuma tai useita tapahtumia, jotka yleensä aiheuttavat useille asiakkaille yhden tai usean palvelun käyttökokemuksen heikentymisen. Nämä ongelmat voivat aiheuttaa suunnittelematonta käyttämättömyysaikaa, kuten saatavuuden heikentymistä, suorituskyvyn laskua ja palvelun hallinnan häiriöitä. Jos regressiot aiheuttavat laajoja muutoksia asiakkaiden järjestelmiin, laatupäivityksen käyttöönotto pysäytetään siksi aikaa, kunnes ongelmaa selvitetään ja se korjataan. Yleensä seuraava laatupäivitys sisältää tarvittavat korjaukset käyttöönoton jatkamiseksi.

Jos yksittäinen asiakasympäristö kärsii ongelmista, avaa palvelupyyntö ottamalla yhteyttä Microsoftin tukeen. Perustelluista syistä pysäytämme laatupäivityksen käyttöönoton kaikissa muissa ympäristöissä siihen asti, kunnes ongelma on korjattu.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lcs"></a>Voivatko asiakkaat edelleen ottaa hotfix-korjaukset manuaalisesti käyttöön LCS:stä?
Kyllä. Jotta varmistetaan käynnissä oleva pariteetti hotfix-korjausten käyttämiseksi, hotfix-korjauksia voi yhä ottaa käyttöön asiakasympäristöissä LCS:ssä. Huomaa kuitenkin, että laatupäivityksen osana käyttöön otettavat hotfix-korjaukset käyvät läpi turvallisen vakiokäyttöönottoprosessin ennen päivityksen käyttöönottoa. Tämä vähentää regressioiden riskiä korkean laadun vuoksi. Suosittelemme, että valitset laatupäivityksen hotfix-korjausten manuaalisen käyttöönoton sijaan paremman luotettavuuden vuoksi.

## <a name="can-customers-proactively-install-a-quality-update-build-ahead-of-the-schedule"></a>Voivatko asiakkaat asentaa ennakoivasti laatupäivityksen koontiversion etukäteen?
Kyllä. Laatupäivityksen voi asentaa ennakoivasti. Microsoft ohittaa päivityksen, jos ympäristön nykyinen koontiversio on sama tai uudempi kuin kyseinen laatupäivitys.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Jos ympäristössä on tuleva ajoitettu kuukausittainen huoltopäivitys viikon kuluessa, saako ympäristö edelleen laatupäivitykset?
- Laatupäivityksiä ei kohdisteta tuotantoympäristöihin, jos ympäristöllä on odottava huoltopäivitys ajoitettuna viikon ajalle siitä, kun laatupäivitys on tarkoitus tehdä.
- Jos eristysympäristön koontiversio on sama tai uudempi kuin odottava laatupäivitys, se ohitetaan.
- Jos tuotantoympäristön koontiversio on sama tai uudempi kuin odottava laatupäivitys, se ohitetaan.
- Jos eristysympäristön koontiversio on sama tai uudempi tuotannon laatupäivityksen tai manuaalisen päivityksen vuoksi, tuotanto saa yhä kuukausittaisen huoltopäivityksen ajoitetun version. Jos et haluat päivittää ajoitettua tuotantoympäristöä huoltopäivityksen versiolla, voit pysäyttää huoltopäivityksen LCS:ssä. 
- Muutokset kannattaa testata uusimman laatupäivityksen koontiversion avulla. Näin varmistetaan ympäristön vakaus ja tulosten oikeellisuus.

## <a name="if-an-environment-has-an-upcoming-scheduled-action-and-a-scheduled-quality-update-in-the-same-maintenance-window-will-it-still-receive-the-quality-update"></a>Jos ympäristöllä on tuleva ajoitettu toiminto ja ajoitettu laatupäivitys samassa ylläpitoikkunassa, tuleeko laatupäivitys edelleen vastaanottaa?
Jos löytyy ristiriita ennalta ajoitetuissa toiminnoissa, kuten tietyn ajankohdan palautuksessa (PITR), laatupäivitys ajoitetaan uudelleen seuraavaan käytettävissä olevaan huoltoikkunaan seuraavien neljän päivän aikana. Lisätietoja aikataulusta on kohdassa [Mikä on ennakoivien laatupäivitysten aikataulu?](#schedule). 

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Voiko ympäristön tuoda takaisin aiempaan tilaan, jos laatupäivityksen jälkeen on ongelmia?
Kun laatupäivitys on otettu käyttöön, ei voi palata aiempaan tilaan missään olosuhteissa. Käytettävissä ovat vain korjaustiedoston etenemisvalinnat, joiden avulla ongelmia voi pienentää.

## <a name="what-about-fda-regulation-and-gpx"></a>Miten FDA-säännökset ja GPX toimivat?
Suunnitelma niitä asiakkaita varten, joita koskevat FDA-vahvistus ja -säädökset, on yhä kehitettävänä. Ilmoitamme päivityksistä tässä pian. Tällä hetkellä kaikki asiakkaat on vapautettu laatupäivityksistä. Varmista, että asiakas käyttää FDA-säännöksiä, kohdassa [Microsoft Azure GPX -tarjooma](/azure/compliance/offerings/offering-gxp).

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Mitä huoltopäivitysten versioita nämä laatupäivitykset tukevat?
Kaikkien laatupäivitysten huoltopäivitysten tuettujen versioiden asiakkaat. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retailsdk"></a>Talous- ja toimintosovellusten käyttöönotot ja Retail-komponentit edellyttävät yleensä lisätyötä sen lisäksi, että MPOS on otettava käyttöön uudelleen. Miten nämä laatupäivitykset vaikuttavat RetailSDK:n toimintaan? 
Koska hotfix-korjaus ei itsessään muuta laatupäivitysten tietoja, Retail-komponentteihin ei odoteta tulevat muutoksia tällä kertaa.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che"></a>Muuttuvatko pilvipalveluympäristöt (CHE)? 
CHE-ympäristöt eivät saa laatupäivityksiä, koska ne eivät kuulu Microsoft Purview -alueeseen

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Onko Microsoft Dataversen kanssa integrointiongelmia? 
Tiedossa ei ole integrointiongelmia, jotka liittyvät Dataversen laatupäivityksiin.

