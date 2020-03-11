---
title: Varaston saatavuuden laskeminen vähittäismyyntikanaville
description: Tässä ohjeaiheessa kerrotaan vaihtoehdot, jotka ovat valittavissa käytettävissä olevan varaston näyttämiseksi myymälä- ja online-kanavissa.
author: hhainesms
manager: annbe
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 8bef8edb46a1942d3efc325e2c437a138ad44839
ms.sourcegitcommit: e1a55b4dc43abedf523c33ba9a8abe7b073f2ec6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/26/2020
ms.locfileid: "3083015"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Varaston saatavuuden laskeminen vähittäismyyntikanaville

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten yritys voi käyttää Microsoft Dynamics 365 Commercea arvioitujen käytettävissä olevan varaston tarkastelussa tuotteille online- ja myymäläkanavissa.

## <a name="accuracy-of-calculation"></a>Laskemisen tarkkuus

Commerce käyttää useita palvelimia ja tietokantoja skaalattavuuden ja suorituskyvyn varmistamiseksi. Tämän vuoksi on tärkeä ymmärtää, että myyntipisteen kautta saatavat käytettävissä olevat varastoarvot, sähköisen kaupankäynnin varaston saatavuuden ohjelmointirajapinnat ja käytettävissä olevan varaston sivut Commerce Headquarters -sovelluksessa eivät ehkä ole reaaliaikaisesti täysin tarkkoja. Jos tuotteille online- tai myymäläkanavassa luotavia tapahtumia ei ole vielä synkronoitu Commerce Headquarters -palvelimen ja -tietokannan kanssa, käytettävissä olevan varaston sivut Commerce Headquarters -sovelluksessa eivät ehkä näytä näiden tuotteiden tarkkoja reaaliaikaisia varastoarvoja. Vastaavasti jos olet määrittänyt yrityksen siten, että Commerce Headquarters -sovelluksen tai muiden integroitujen sovellusten käyttäjät voivat myydä, vastaanottaa, palauttaa tai muuten muuttaa varastoa tai online-varastoa, myyntipiste- tai online-kanava ei välttämättä sisällä kaikkia nimikkeiden tarkan reaaliaikaisen käytettävissä olevan varastoarvon näyttämisessä tarvittavia tietoja.

Tässä ohjeaiheessa kerrotaan tietojen synkronointiprosesseista. Niitä voidaan käyttää usein, ja näin voidaan rajoittaa tietojen viivettä sovellusten tai kanavien välillä. On kuitenkin tärkeää ymmärtää, että kaikkia työpäivän aikana saatuja käytettävissä olevan varaston tietoja pidetään arvioina. Jos siis yrität vertailla käytettävissä olevan varaston tietoja, jotka sovellus määrittää hyllyjen toteutuneen fyysisen varaston perusteella, tai käytettävissä olevia varastoarvoja, jotka näytetään myyntipisteessä yhdessä käytettävissä olevan varaston tietojen kanssa samassa Commerce Headquarters -varastossa, arvot voivat olla erilaisia. Tämä työpäivän aikainen ero on odotettavissa, eikä sitä tule käsitellä virheenä. Jos haluat tarkistaa tiedot ja varmistaa, että varaston saatavuuden ohjelmointirajapintojen ja Commerce Headquarters -sovelluksen annetut arvot vastaavat toteutuneita fyysisiä yksiköitä, jotka löytyvät myymälän tai varaston hyllyiltä, tarkistus kannattaa tehdä sen jälkeen kun kanavatoiminnot on pysäytetty päivän jälkeen ja kaikki tapahtumat on synkronoitu oikein Commerce Headquarters -sovelluksen ja kanavan välillä.

## <a name="use-inventory-lookup-apis-for-e-commerce-inventory-availability-requests"></a>Varastohakujen ohjelmointirajapintojen käyttäminen sähköisen kaupankäynnin varaston saatavuuden pyyntöjä varten

Voit käyttää seuraavia ohjelmointirajapintoja, jos haluat näyttää tuotteen varaston saatavuuden asiakkaiden ollessa ostoksilla sähköisen kaupankäynnin sivustossa.

- **GetEstimatedAvailabilty** – Käytä tätä ohjelmointirajapintaa, jos haluat hakea varaston saatavuuden nimikkeelle sähköisen kaupankäynnin kanavan varastossa tai kaikissa varastoissa, jotka on linkitetty sähköisen kaupankäynnin täyttämisryhmän kokoonpanoon. Tätä ohjelmointirajapintaa voi käyttää myös tietyn hakualueen tai -säteen varastoissa pituus- tai leveysastetietojen perusteella.
- **ProductWarehouseInventoryAvailabilities** – Käytä tätä ohjelmointirajapintaa, jos haluat pyytää nimikkeen varastoa tietystä varastosta. Voit käyttää sitä esimerkiksi näyttämään varaston saatavuuden skenaarioissa, joissa käytetään tilauksen noutoa.

> [!NOTE]
> Nämä ohjelmointirajapinnat korvaavat **GetProductAvailabilities**- ja **GetAvailableInventoryNearby**-ohjelmointirajapinnat Dynamics 365 Retailin versiossa 10.0.7 ja vanhemmissa versioissa.

Molemmat ohjelmointirajapinnat hakevat tietoja Commerce-palvelimelta ja antavat arvion käytettävissä olevasta varastosta tietylle tuotteen tai tuotevariantin ja varaston yhdistelmälle. Vaikka Commerce-palvelimen muut ohjelmointirajapinnat voivat siirtyä suoraan Commerce Headquarters -sovellukseen ja hakea käytettävissä olevan varaston määrät tuotteille, tätä ei suositella käytettäväksi sähköisen kaupankäynnin ympäristössä. Tämä johtuu siitä, että nämä toistuvat pyynnöt voivat vaikuttaa Commerce Headquarters -palvelimiin ja aiheuttaa mahdollisia suorituskykyongelmia. Jos lisäksi käytettävissä oleva varasto lasketaan Commerce-palvelimen kautta, laskenta sisältää todennäköisesti myös lähiaikoina sähköisen kaupankäynnin tapahtumissa myytyä varastoa, jota ei ole vielä synkronoitu Commerce Headquarters -sovellukseen. Vaikka Commerce Headquarters ei ehkä sisällä tietoja näistä tapahtumista, Commerce-palvelin ja kanavan tietokanta sisältävät kyseiset tiedot. Tämän vuoksi tiedot otetaan huomioon. Niiden avulla saadaan tarkka arvio tuotteen käytettävissä olevasta varastosta.

### <a name="get-started-with-e-commerce-calculated-inventory-availability"></a>Sähköisen kaupankäynnin lasketun varaston saatavuuden toiminnon aloittaminen

Ennen kuin käytät näitä kahta aiemmin mainittua ohjelmointirajapintaa, Commerce Headquarters -sovelluksessa on tehtävä parametrin muutos. Näin varmistetaan, että varastoarvojen tilannekuvaus, jonka Commerce Headquarters laskee **Tuotteen saatavuus** -työn avulla, syöttää tiedot oikeisiin taulukoihin.

Määritä parametri seuraavien vaiheiden avulla.

1. Valitse **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Kaupan jaetut parametrit**.
1. Valitse **Varasto**-välilehden **Tuotteen saatavuus -työ** -osassa **Käytä optimoitua prosessia tuotteen saatavuuden työssä**. Tämä asetus varmistaa, että kanavan käytettävissä olevan varaston laskennassa käytetään optimaalista toimintojoukkoa Commerce-palvelimessa.

Ennen kuin ohjelmointirajapinnat voivat laskea parhaan varaston saatavuuden arvion nimikkeelle, Commerce Headquarters -sovelluksen varaston saatavuuden kausittainen tilannevedos on käsiteltävä ja lähetettävä siihen kanavan tietokantaan, jota sähköisen kaupankäynnin Commerce Scale Unit käyttää. Tilannevedos vastaa tietoja, jotka Commerce Headquarters -sovelluksella on varaston saatavuudesta tietylle tuotteen tai tuotevariantin ja varaston yhdistelmälle. Se voi sisältää varaston oikaisuja tai siirtoja, jotka johtuvat varaston vastaanotoista, lähetyksistä tai muista prosesseista, jotka Commerce Headquarters suorittaa ja joista sähköisen kaupankäynnin kanavalla on tietoja vain synkronisointiprosessin vuoksi.

Tietokannan tilannevedot, jonka **Tuotteen saatavuus** -työ luo, laskee vain Commerce Headquarters -sovelluksessa käsitellyt ja sinne kirjatut varastotapahtumat tilannevedoksen luontiajankohtana. Jos tuotteen varasto on myyty myymälän varastossa myyntipistesovelluksen noutotukkumyynnin tai asynkronisen asiakastilausmyynnin avulla, Commerce Headquarters -sovelluksessa ei heti ole tietoja myyntiin liittyvästä varasto-ottotapahtumasta. Se sisältää tietoja varastosta, joka on myyty tämäntyyppisille myymälämyynneille vain sen jälkeen, kun P-työ on ladannut liittyvän tapahtuman myymälän kanavan tietokannasta Commerce Headquarters -sovellukseen ja liittyvä myyntitilaus on luotu laskelman kirjauksen tai vähittäin suoritettavien kirjausprosessien kautta. Tilauksen luontiprosessi Commerce Headquarters -sovelluksessa luo liittyvät varastotapahtumat. Commerce Headquarters sisältää tietoja sähköisen kaupankäynnin kanavan tilauksille varastotapahtumista vasta sen jälkeen, kun tapahtumat on lähetetty Commerce Headquarters -sovellukseen P-työn avulla ja tilauksen synkronointiprosessi on valmis. Tämän vuoksi on tärkeää ymmärtää, että **Tuotteen saatavuus** -työn varaston tilannevedoksen arvo ei välttämättä ole täysin tarkka ja reaaliaikainen jaetuilla palvelimilla tapahtuvien jatkuvien myyntikäsittelyjen vuoksi.

Voit luoda halutessasi varaston tilannevedoksen Commerce Headquarters -sovelluksessa seuraavasti.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Vähittäismyynnin ja kaupan IT \> Tuotteet ja varasto \> Tuotteen saatavuus**.
1. Valitse **OK**, jos haluat suorittaa **Tuotteen saatavuus** -työn. Voit myös ajoittaa tämän työn niin, että se suoritetaan eränä.

Kun **Tuotteen saatavuus** -työ on päättynyt, kerätyt tiedot on siirrettävä sähköisen kaupankäynnin kanavan tietokantoihin. Tällöin uusinta Commerce Headquarters -varaston tilannevedosta voidaan pitää käytettävissä olevan varaston arvion laskelmana.

1. Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.
1. Suorita **1130** (**Tuotteen saatavuus**) -työ, jolloin **Tuotteen saatavuus** -työn luomat tilannevedoksen tiedot synkronoidaan Commerce Headquarters -sovelluksesta omiin kanavan tietokantoihin.

Kun **GetEstimatedAvailabilty**- tai **ProductWarehouseInventoryAvailabilities**-ohjelmointirajapinnalta pyydetään varaston saatavuutta, suoritetaan laskelma, joka antaa parhaan mahdollisen tuotteen varaston arvion. Laskelma viittaa kaikkiin sähköisen kaupankäynnin asiakastilauksiin, jotka ovat kanavan tietokannassa, mutta joita ei ole sisällytetty 1130-työn antamiin tilannevedoksen tietoihin. Tämä logiikka suoritetaan seuraamalla viimeksi käsiteltyä varastotapahtumaa Commerce Headquarters -sovelluksesta ja vertaamalla sitä kanavan tietokannan tapahtumiin. Se määrittää kanavan peruslaskentalogiikan, jolloin asiakastilauksen myyntitapahtumien varaston lisäsiirrot sähköisen kaupankäynnin kanavan tietokannassa voidaan kohdistaa ohjelmointirajapinnan tarjoamaan arvioituun varastoarvoon.

Kanavan laskentalogiikka palauttaa arvioidun fyysisen varaston arvon ja saatavissa olevan varaston kokonaisarvon pyydetylle tuotteelle ja varastolle. Arvot voidaan näyttää tarvittaessa sähköisen kaupankäynnin sivustossa tai niitä voi käyttää muun liiketoimintalogiikan käynnistämisessä sähköisen kaupankäynnin sivustossa. Ohjelmointirajapinnan välittämän toteutuneen käytettävissä olevan varastomäärän sijaan voidaan näyttää ei varastossa -sanomaa.

Laskentalogiikka, jota kanavan sähköisen kaupankäynnin ohjelmointirajapinnat käyttävät arvioidussa varastoarvossa, voivat arvioida varaston pelkästään niiden asiakastilausten perusteella, jotka on luotu kanavan tietokannassa, mutta joita ei ole vielä synkronoitu ja kirjattu Commerce Headquarters -sovellukseen. Jos kanavan tietokanta sisältää myös tapahtumatietoja myymäläkohtaisten varastojen noutotukkumyynnille, tätä myyntiä ei oteta huomioon näiden varastojen kanavan sähköisen kaupankäynnin laskennassa.

## <a name="configure-the-inventory-lookup-operation-in-the-pos-channel"></a>Varastohaku-toiminnon määrittäminen myyntipistekanavassa

Retailin versiossa 10.0.9 ja vanhemmissa versioissa myyntipisteen **Varastohaku**-toiminto käytti reaaliaikaista palvelukutsua Commerce Headquarters -sovelluksessa hakiessaan tietyn tuotteen varaston tietoja sekä käyttäjän myymälässä että muissa myymälöissä, jotka on määritetty täyttämisryhmälle osana myymälän kanavan määritystä. Commerce-versiossa 10.0.10 ja uudemmassa versiossa reaaliaikaiset palvelukutsut voidaan poistaa käytöistä Commerce Headquarters -sovelluksessa. Sen sijaan voidaan käyttää kanavan laskentaa Commerce-palvelimessa, kun määritetään myymälässä ja muissa täyttämisryhmän määritetyissä sijainneissa fyysinen käytettävissä oleva varasto. Tämä kanavan laskema varaston määritys on hyödyllinen myös sijainneissa, joissa internet-yhteys ei toimi kunnolla, koska Commerce Headquarters -sovelluksesta voi tehdä varastohakuja myös online-tilan ulkopuolella.

Kun kanavan laskenta on oikein määritetty ja hallittu, se voi tuottaa luotettavia arvioita myymälän nykyisestä varastosta, koska se käyttää Commerce-kanavan tietokannan tapahtumatietoja. Commerce Headquarters ei välttämättä vielä sisällä näitä tietoja. Jos esimerkiksi käytössä on myyntipisteen varastohakujen olemassa oleva reaaliaikainen palvelukutsu, Commerce Headquarters ei ehkä vielä sisällä tietoja tuotteen juuri tapahtuneesta noutotukkumyynnistä. Tämän vuoksi käytettävissä oleva varastoarvo, jonka Commerce Headquarters palauttaa tuotteelle, todennäköisesti ylittää myymälän toteutuneen käytettävissä olevan varaston yhdellä yksiköllä. Jos kuitenkin käytät kanavan laskentaa, noutotukkumyynti voidaan kohdistaa laskentaan ja vähentää näkyvillä olevasta käytettävissä olevasta varastoarvosta. Vaikka sekä kanavan laskennan että reaaliaikaisen palvelukutsun antamat arvot ovat vain arvioita käytettävissä olevasta varastosta, kanavan laskennan arvo on todennäköisemmin oikeassa nykyistä myymälää ajatellen.

### <a name="get-started-with-pos-channel-side-calculated-inventory-availability"></a>Myyntipisteen kanavan lasketun varaston saatavuuden toiminnon aloittaminen

Voit käyttää kanavan laskentalogiikkaa ja ottaa reaaliaikaiset palvelukutsut pois käytöstä varastohauissa myyntipistesovelluksessa, jos teet ensin kaksi parametrimuutosta. Tämän jälkeen muutokset synkronoidaan kanavassa jakeluaikatauluprosessin kautta.

Määritä ensimmäinen parametri seuraavien vaiheiden avulla.

1. Valitse **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Kaupan jaetut parametrit**.
1. Valitse **Varasto**-välilehden **Tuotteen saatavuus -työ** -osassa **Käytä optimoitua prosessia tuotteen saatavuuden työssä**. Tämä asetus varmistaa, että kanavan käytettävissä olevan varaston laskennassa käytetään optimaalista toimintojoukkoa Commerce-palvelimessa.

Määritä toinen parametri seuraavien vaiheiden avulla.

1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit**.
1. Valitse toimintoprofiili.
1. Muuta **Toiminnot**-pikavälilehden **Varaston saatavuuden laskenta** -osassa **Varaston saatavuuden laskentatila** -kentän arvo **Reaaliaikainen palvelu** -arvosta **Kanava**-arvoksi. Oletusarvoisesti kaikki toimintoprofiilit käyttävät reaaliaikaisia palvelukutsuja. Tämän vuoksi sinun on muutettava tämän kentän arvoa, jos haluat käyttää kanavan laskentalogiikkaa. Tämä muutos vaikuttaa jokaiseen valittuun toimintoprofiiliin linkitettyyn vähittäismyymälään.

Päivitä palvelimet seuraavien vaiheiden avulla.

1. Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.
1. Suorita **1070** (**Kanavan määritys**) -työ.

Kun määritys on valmis, fyysisen käytettävissä olevan varaston tiedot eivät enää käytä reaaliaikaista palvelukutsua, kun myyntipistesovelluksen käyttäjä käyttää **Varastohaku**-toimintoa (vakio- ja matriisinäkymät). Sen sijaan nykyisen myymälän ja kaikkien täyttämisryhmän myymälöiden fyysisesti käytettävissä olevan varaston tiedot lasketaan edellisen tunnetun Commerce Headquarters -sovelluksesta kanavan tietokantaan toimitetun tilannevedoksen mukaan. Kanavan laskenta muuttaa tilannevedoksen arvoa niin, että fyysisesti käytettävissä olevan varaston arvo muuttuu kanavan tietokannan sen valitun tuotteen lisämyynnin tai palautustapahtumien perusteella, jota ei sisällytetty edelliseen synkronoituun tilannevedokseen 1130-työstä. Jos kanavan tietokanta ei sisällä tapahtumatietoja mistään täyttämisryhmän varastossa tai myymälässä, se ei sisällä muita tapahtumia arvon uudelleenlaskentaa varten. Tämän vuoksi paras käytettävissä olevan varaston arvio, joka voidaan näyttää varastoille tai myymälöille, on edellisen tunnetun Commerce Headquarters -tilannevedoksesta saatavat tiedot.

**Tilauksen täyttäminen** -näytöt myyntipisteessä hyödyntävät myös kanavan laskentaa nimikkeiden käytettävissä olevan varaston näyttämisessä, kun tilauksen täyttämisen rivi valitaan ja käyttäjä tarkastelee valitun nimikkeen käytettävissä olevan varaston **Tiedot**-paneelia.

## <a name="optimize-your-inventory-data"></a>Varastotietojen optimoiminen

Voit varmistaa varaston parhaan mahdollisen arvion saamisen, jos käytät seuraavia Commerce-erätöitä ja suoritat ne säännöllisesti:

- **P-työ** – P-työ löytyy **Jakeluaikataulut**-sivulta. Se tulee suorittaa säännöllisesti. Tämä työ tuo sähköisen kaupankäynnin tilaukset, myyntipisteen luomat asynkroniset asiakastilaukset ja myyntipisteen kanavan tietokannoista Commerce Headquarters -sovellukseen luomat noutotukkutilaukset, jotta niitä voidaan käsitellä lisää. Commerce Headquarters ei sisällä tietoja näiden tapahtumien aiheuttamista varaston tuotteiden varasto-oikaisuista ennen kuin nämä tiedot on synkronoitu kanavasta Commerce Headquarters -sovellukseen.
- **Synkronoi tilaukset** – Tämä työ käsittelee P-työn määrittämät tapahtuman raakatiedot Commerce Headquarters -sovelluksessa ja muuntaa sähköisen kaupankäynnin ja asynkronisen asiakastilauksen tapahtumat myyntitilauksiksi Commerce Headquarters -sovelluksessa. Varastotapahtumia luodaan vasta sen jälkeen, kun tämä työ on käsitelty ja myyntitilaukset on luotu. Tämän vuoksi Commerce Headquarters -sovelluksen käytettävissä olevaa varastoa ei oteta huomioon tapahtumissa.
- **Laske tapahtumaraportit eräajona** – Myymälässä luotujen noutotukkutapahtumien vähittäin suoritettava kirjausprosessi varmistaa, että myyntiin liittyvä varasto päivitetään tehokkaasti. Noutotukkutilausten varastotapahtumien käsittelyn tehokkuuden varmistamiseksi kannattaa tarkistaa, että järjestelmä on määritetty käyttämään [vähittäin suoritettavaa kirjausta](https://docs.microsoft.com/dynamics365/commerce/trickle-feed).
- **Kirjaa tapahtumaraportit eräajona** – Tämä työ on myös pakollinen vähittäin suoritettavassa kirjauksessa. Se seuraa **Laske tapahtumaraportit eräajona** -työtä. Tämä työ kirjaa lasketut laskelmat järjestelmällisesti niin, että noutotukkumyynnin myyntitilaukset luodaan Commerce Headquarters -sovelluksessa. Näin Commerce Headquarters vastaa aiempaa tarkemmin myymälän varastoa.
- **Tuotteen saatavuus** – Tämä työ luo tilannevedoksen Commerce Headquarters -sovelluksen varastosta.
- **1130 (Tuotteen saatavuus)** – Tämä työ löytyy **Jakeluaikataulut**-sivulta. Se tulee suorittaa heti **Tuotteen saatavuus** -työn jälkeen. Tämä työ siirtää varaston tilannevedoksen tiedot Commerce Headquarters -sovelluksesta kanavan tietokantoihin.

> [!NOTE]
> Kun kanavan varaston saatavuuden laskelmia käytetään varaston saatavuuspyynnön luomisessa sähköisen kaupankäynnin ohjelmointirajapintaa tai uutta myyntipisteen kanavan varastointilogiikkaa, suorituskyvyn varmistamiseksi laskelma käyttää välimuistia ja määrittää sen avulla, onko laskentalogiikan suorittamisesta kulunut riittävästi aikaa, jotta sen suorittaminen uudelleen on perusteltua. Välimuistin oletusarvoksi on määritetty 60 sekuntia. Tässä esimerkissä otetaan käyttöön kanavan laskennan myymälässä ja tarkastellaan tuotteen käytettävissä olevaa varastoa **Varastohaku**-sivulla. Jos tuotetta tämän jälkeen myydään yksi yksikkö, **Varastohaku**-sivulla ei näy vähennetty varasto ennen välimuistin tyhjentämistä. Käyttäjien kirjattua tapahtumia myyntipisteeseen, heidän tulee odottaa 60 sekuntia. Tämän jälkeen he voivat tarkistaa, onko käytettävissä olevaa varastoa vähennetty tapahtuman mukaan.

Jos liiketoimintaskenaario edellyttää lyhyempää välimuistin aikaa, ota yhteyttä tuotetuen edustajaan.
