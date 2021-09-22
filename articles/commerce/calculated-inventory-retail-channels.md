---
title: Vähittäismyyntikanavien varaston käytettävyyden laskeminen
description: Tässä ohjeaiheessa kerrotaan, miten yritys voi käyttää Microsoft Dynamics 365 Commercea arvioitujen käytettävissä olevan varaston tarkastelussa tuotteille online- ja myymäläkanavissa.
author: hhainesms
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: d3cfd8c2f0b88a4e634cee0398283a51eddf60b2
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472168"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Vähittäismyyntikanavien varaston käytettävyyden laskeminen

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa kerrotaan, miten yritys voi käyttää Microsoft Dynamics 365 Commercea arvioitujen käytettävissä olevan varaston tarkastelussa tuotteille online- ja myymäläkanavissa.

## <a name="accuracy-of-inventory-availability"></a>Varaston käytettävyyden tarkkuus

Commerce käyttää useita palvelimia ja tietokantoja skaalattavuuden ja suorituskyvyn varmistamiseksi. Tämän vuoksi on tärkeä ymmärtää, että myyntipisteen kautta saatavat käytettävissä olevat varastoarvot, sähköisen kaupankäynnin varaston saatavuuden ohjelmointirajapinnat ja käytettävissä olevan varaston sivut Commerce-pääkonttorisovelluksessa eivät ehkä ole reaaliaikaisesti täysin tarkkoja. Jos tuotteille online- tai myymäläkanavassa luotavia tapahtumia ei ole vielä synkronoitu pääkonttorin, käytettävissä olevan varaston sivut pääkonttorissa eivät ehkä näytä näiden tuotteiden tarkkoja reaaliaikaisia varastoarvoja. Vastaavasti jos olet määrittänyt yrityksen siten, että pääkonttorisovelluksen tai muiden integroitujen sovellusten käyttäjät voivat myydä, vastaanottaa, palauttaa tai muuten muuttaa varastoa tai online-varastoa, myyntipiste- tai online-kanava ei välttämättä sisällä kaikkia nimikkeiden tarkan reaaliaikaisen arvon näyttämisessä tarvittavia tietoja.

On tärkeää ymmärtää, että kaikkia työpäivän aikana saatuja käytettävissä olevan varaston tietoja pidetään arvioina. Jos siis yrität vertailla käytettävissä olevan varaston tietoja, jotka sovellus määrittää hyllyjen toteutuneen fyysisen varaston perusteella, tai käytettävissä olevia varastoarvoja, jotka näytetään myyntipisteessä yhdessä käytettävissä olevan varaston tietojen kanssa samassa pääkonttorin varastossa, arvot voivat olla erilaisia. Tämä työpäivän aikainen ero on odotettavissa, eikä sitä tule käsitellä virheenä. Jos haluat tarkistaa tiedot ja varmistaa, että myyntipisteen, ohjelmointirajapintojen ja pääkonttorin annetut arvot vastaavat toteutuneita fyysisiä yksiköitä, jotka löytyvät myymälän tai varaston hyllyiltä, tarkistus kannattaa tehdä sen jälkeen kun kanavatoiminnot on pysäytetty päivän jälkeen ja kaikki tapahtumat on synkronoitu oikein pääkonttorin ja kanavien välillä.

## <a name="channel-side-inventory-calculation"></a>Kanavan puolella oleva varastolaskelma

Kanavanpuoleinen varastolaskenta on mekanismi, jossa Commerce-pääkonttorisovelluksen viimeiset kanavan varastotiedot otetaan lähtökohtana ja huomioidaan lisävarastomuutokset, jotka on tehty kanavan puolella ja jotka eivät sisälly tähän perustasoon käytettävissä olevan varaston lähes reaaliaikaisten arvioitujen laskelmien laskemiseksi. 

Seuraavat varastomuutokset on tällä hetkellä otettu huomioon kanavanpuoleisen varaston laskentalogiikassa:

- Myymälän itsepalvelutukkutilausten kautta myyty varasto
- Myymälän tai verkkokanavan asiakastilausten kautta myyty varasto.
- Myymälälle palautettu varasto
- Täytetty varasto (kerää, pakkaa, lähetä) myymälävarastosta

Kanavapuolen varastonlaskennan käyttämistä varten sinun on otettava **Optimoitu tuotteen saatavuuslaskenta** -ominaisuus käyttöön.

Jos Commerce-ympäristösi versio on **10.0.8–10.0.11**, noudata seuraavia ohjeita.

1. Siirry Commerce-pääkonttorissa kohtaan **Retail ja Commerce** \> **Commercen jaetut parametrit**.
1. Valitse **Varasto**-välilehden **Tuotteen saatavuus -työ** -kentässä **Käytä optimoitua prosessia tuotteen saatavuuden työssä**.

Jos Commerce-ympäristösi versio on **10.0.12 tai uudempi**, noudata seuraavia ohjeita.

1. Siirry Commerce-pääkonttorissa kohtaan **Työtilat \> Ominaisuuksienhallinta** ja ota **Optimoitu tuotteen saatavuuden laskenta** -ominaisuus käyttöön.
1. Jos verkko- ja myymäläkanavissa käytetään samoja toteutusvarastoja, sinun on otettava käyttöön myös **Parannettu sähköisen kaupankäynnin kanavanpuoleinen varaston laskentalogiikka** -ominaisuus. Tällöin ohjelmointirajapinnan kanavanpuoleinen laskentalogiikka ottaa huomioon myymäläkanavassa luodut kirjaamattomat tapahtumat. (Nämä tapahtumat voivat olla itsepalvelutukkutapahtumia, asiakastilauksia ja palautuksia).
1. Suorita **1070** (**Kanavan määritys**) -työ.

Jos Commerce-ympäristö on päivitetty Commerce-versiota 10.0.8 aiemmasta versiosta, sinun on suoritettava myös **Alusta Commerce-ajastus**, kun olet ottanut käyttöön **Optimoitu tuotteen saatavuuslaskenta** -ominaisuus, jotta ominaisuus tulee käyttöön. Suorita alustus menemällä kohtaan **Retail ja Commerce** \> **Pääkonttorina asetukset** \> **Commerce-ajastus**.

Jos kanavanpuoleisen varaston laskentaa halutaan käyttää, **Tuotteen saatavuus** -työn luoma pääkonttorin varastotietojen kausittainen tilannevedos on lähetettävä kanavatietokantoihin. Tilannevedos vastaa tietoja, jotka pääkonttorisovelluksella on varaston saatavuudesta tietylle tuotteen tai tuotevariantin ja varaston yhdistelmälle. Se sisältää vain varastotapahtumat, jotka on käsitelty ja kirjattu pääkonttorissa tilannevedoksen määrityksen yhteydessä, eikä se ole välttämättä 100 prosenttisen tarkka reaaliajassa jaetuissa palvelimissa olevan vakiomyyntikäsittelyn vuoksi.

- Jos tuotteen varasto on myyty myymälässä myyntipistesovelluksen noutotukkumyynnin tai asynkronisen asiakastilausmyynnin avulla, pääkonttorisovelluksessa ei heti ole tietoja myyntiin liittyvästä varasto-ottotapahtumasta. Pääkonttori sisältää tietoja varastosta, joka on myyty tämäntyyppisille myymälämyynneille vain sen jälkeen, kun P-työ on ladannut liittyvän tapahtuman myymälän kanavan tietokannasta pääkonttorisovellukseen ja liittyvät myyntitilaukset on luotu laskelman kirjauksen tai vähittäin suoritettavien kirjausprosessien kautta. Tilausten luontiprosessi pääkonttorisovelluksessa luo liittyvät varastotapahtumat. 
- Pääkonttori sisältää tietoja sähköisen kaupankäynnin kanavan tilauksille varastotapahtumista vasta sen jälkeen, kun tapahtumat on lähetetty pääkonttorisovellukseen P-työn avulla ja tilauksen synkronointiprosessi on valmis.

Voit luoda halutessasi varaston tilannevedoksen pääkonttorisovelluksessa seuraavasti.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Vähittäismyynnin ja kaupan IT \> Tuotteet ja varasto \> Tuotteen saatavuus**.
1. Valitse **OK**, jos haluat suorittaa **Tuotteen saatavuus** -työn. Voit myös ajoittaa tämän työn niin, että se suoritetaan eränä.

Kun **Tuotteen saatavuus** -työ on päättynyt, kerätyt tiedot on siirrettävä kanavan tietokantoihin. Tällöin uusinta pääkonttorivaraston tilannevedosta voidaan pitää käytettävissä olevan varaston arvion kanavanpuoleisena laskelmana.

Noudattamalla seuraavia ohjeita voit synkronoida tilannevedostietoja pääkonttorista kanavatietokantoihin.

1. Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.
1. Suorita **1130** (**Tuotteen saatavuus**) -työ, jolloin **Tuotteen saatavuus** -työn luomat tilannevedoksen tiedot synkronoidaan pääkonttorisovelluksesta omiin kanavan tietokantoihin.

## <a name="inventory-availability-apis-for-e-commerce"></a>Sähköisen kaupankäynnin varaston käytettävyyden ohjelmointirajapinnat

Commerce toimittaa seuraavat sähköisen kaupan ohjelmointirajapinnat, jotta voidaan tehdä kysely tuotteen varaston saatavuudesta:

- **GetEstimatedAvailability** – Tämän ohjelmointirajapinnan avulla voit tehdä kyselyn tuotteen tai tuotevariantin varastosta online-kanavan varastossa tai varastoissa, jotka on linkitetty online-kanavan täytäntöönpanoryhmään.
- **GetEstimatedProductWarehouseAvailability** – Käytä tätä ohjelmointirajapintaa, jos haluat tehdä kyselyn tuotteesta tai tuotevariantista tietystä varastosta.

> [!NOTE]
> Nämä ohjelmointirajapinnat korvaavat **GetProductAvailabilities**- ja **GetAvailableInventoryNearby**-ohjelmointirajapinnat Commercen versiossa 10.0.7 ja vanhemmissa versioissa.

Molemmat ohjelmointirajapinnat käyttävät sisäisesti kanavanpuoleista laskentalogiikkaa ja palauttavat arvioidun **fyysisen käytettävissä** olevan määrän, **käytettävissä olevan kokonaismäärän**, **mittayksikön (UoM)** ja **varastotason** pyydetylle tuotteelle ja varastolle. Palautetut arvot voidaan näyttää tarvittaessa sähköisen kaupankäynnin sivustossa tai niitä voi käyttää muun liiketoimintalogiikan käynnistämisessä sähköisen kaupankäynnin sivustossa. Voit esimerkiksi estää tuotteiden oston Loppunut varastosta -varastotasolla.

Vaikka Commercen muut ohjelmointirajapinnat voivat siirtyä suoraan pääkonttorisovellukseen ja hakea käytettävissä olevan varaston määrät tuotteille, tätä ei suositella käytettäväksi sähköisen kaupankäynnin ympäristössä. Tämä johtuu siitä, että nämä toistuvat pyynnöt voivat vaikuttaa pääkonttorin palvelimiin ja aiheuttaa mahdollisia suorituskykyongelmia. Lisäksi kanavanpuoleisen laskennan avulla edellä mainitut kaksi ohjelmointirajapintaa voivat antaa tarkemman arvion tuotteen saatavuudesta ottamalla huomioon niiden kanavien tapahtumat, joista ei vielä tiedetä pääkonttorissa.

Seuraavia ohjeita noudattamalla voit määrittää, miten tuotemäärä palautetaan ohjelmointirajapinnan tuotoksessa.

1. Valitse **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Kaupan parametrit**.
1. Valitse **Varasto**-välilehti ja määritä sitten **Sähköisen kaupankäynnin varaston käytettävyyden ohjelmointirajapinnat** -pikavälilehdessä **Ohjelmointirajapinnan tuotoksen määrä** -asetuksen arvo.
1. Synkronoi uusin asetus kanaviin suorittamalla **1070** (**Kanavan määritys**) -työ.

**Ohjelmointirajapinnan tuotoksen määrä** -asetuksessa on kolme vaihtoehtoa:

- **Palauta varastomäärä** – Pyydetyn tuotteen fyysinen käytettävissä oleva määrä ja käytettävissä oleva kokonaismäärä palautetaan ohjelmointirajapinnan tuotoksessa.
- **Palauta varastomäärä vähentämällä varastopuskuri** – Ohjelmointirajapinnan tuotoksen palauttama määrä oikaistaan vähentämällä varastopuskurin arvo. Lisätietoja varastopuskurista on kohdassa [Varastopuskureiden ja varastotasojen konfiguroiminen](inventory-buffers-levels.md).
- **Ei palauta varastomäärää** – Vain varastotaso palautetaan ohjelmointirajapinnan tuotoksessa. Lisätietoja varastotasoista on kohdassa [Varastopuskureiden ja varastotasojen konfiguroiminen](inventory-buffers-levels.md).

`QuantityUnitTypeValue`-ohjelmointirajapinnan parametrin avulla voit määrittää yksikkötyypin, joissa haluat ohjelmointirajapintojen palauttavan määrän. Tämä parametri tukee **Varastoyksikkö**- (oletusarvo), **Ostoyksikkö**- ja **Myyntiyksikkö**-vaihtoehtoja. Palautettu määrä pyöristetään vastaavan mittayksikön määritettyyn tarkkuuteen pääkonttorissa.

**GetEstimatedAvailability**-ohjelmointirajapinta tarjoaa seuraavat syöteparametrit tukemaan erilaisia kyselyskenaarioita:

- `DefaultWarehouseOnly` – Tämän parametrin avulla voit tehdä kyselyn tuotteelle varastosta online-kanavan oletusvarastossa. 
- `FilterByChannelFulfillmentGroup` ja `SearchArea` – Näiden kahden parametrin avulla voit tehdä kyselyn tuotteelle varastosta kaikista tietyn hakualueen noutosijainneista, perustana `longitude`, `latitude` ja `radius`. 
- `FilterByChannelFulfillmentGroup` ja `DeliveryModeTypeFilterValue` – Näiden kahden parametrin avulla voit tehdä kyselyn tuotteelle tietyistä varastoista, jotka on linkitetty online-kanavan täytäntöönpanoryhmään ja jotka on määritetty tukemaan tiettyjä toimitustapoja. `DeliveryModeTypeFilterValue`-parametri tukee **kaikki**- (oletusarvo), **lähetys**- ja **nouto**-vaihtoehtoja. Jos esimerkiksi online-tilaus voidaan täyttää useista lähetysvarastoista, voit tehdä kyselyn tuotteen varaston saatavuudesta näiden kahden parametrin avulla kaikissa lähetysvarastoissa. Tässä tapauksessa ohjelmointirajapinta palauttaa tuotteen käytettävissä olevan määrän ja varaston tason kaikissa lähetysvarastoissa sekä koostetun määrän ja koostetun varastotason kyselyn laajuuden kaikista lähetysvarastoista.
 
Commercen ostoruutu-, myymälän valitsin-, toivelista-, ostoskori- ja ostokorikuvakemoduulit käyttävät yllä mainittuja ohjelmointirajapintoja ja parametreja varastotason sanomien tarkastelemiseksi koko sähköisen kaupan sivustossa. Commercen sivustonmuodostin tarjoaa useita varastoasetuksia myynninedistämisen ja oston toiminnan ohjaamista varten. Lisätietoa kohdassa [Varastoasetusten käyttöönotto](inventory-settings.md).

## <a name="pos-inventory-lookup-with-channel-side-calculation"></a>Myyntipisteen varastohaku ja kanavanpuoleisella laskennalla

Commercen versiossa 10.0.9 ja vanhemmissa versioissa myyntipisteen **Varastohaku**-toiminto käytti reaaliaikaista palvelukutsua pääkonttoriin hakiessaan tietyn tuotteen varaston tietoja sekä käyttäjän myymälässä että muissa myymälöissä, jotka on määritetty täyttämisryhmälle osana myymälän kanavan määritystä. Commerce-versiossa 10.0.10 ja uudemmassa versiossa reaaliaikaiset palvelukutsut voidaan poistaa käytöstä pääkonttoriin. Sen sijaan voidaan käyttää kanavan laskentaa Commerce-palvelimessa, kun määritetään myymälässä ja muissa täyttämisryhmän määritetyissä sijainneissa fyysinen käytettävissä oleva varasto. Tämä kanavan laskema varaston määritys on hyödyllinen myös sijainneissa, joissa internet-yhteys ei toimi kunnolla, koska pääkonttorisovelluksesta voi tehdä varastohakuja myös online-tilan ulkopuolella.

Kun kanavan laskenta on oikein määritetty ja hallittu, se voi tuottaa luotettavia arvioita myymälän nykyisestä varastosta, koska se käyttää Commerce-kanavan tietokannan tapahtumatietoja. Pääkonttori ei välttämättä vielä sisällä näitä tietoja. Jos esimerkiksi käytössä on myyntipisteen varastohakujen olemassa oleva reaaliaikainen palvelukutsu, pääkonttori ei ehkä vielä sisällä tietoja tuotteen juuri tapahtuneesta noutotukkumyynnistä. Tämän vuoksi käytettävissä oleva varastoarvo, jonka pääkonttori palauttaa tuotteelle, todennäköisesti ylittää myymälän toteutuneen käytettävissä olevan varaston yhdellä yksiköllä. Jos kuitenkin käytät kanavan laskentaa, noutotukkumyynti voidaan kohdistaa laskentaan ja vähentää näkyvillä olevasta käytettävissä olevasta varastoarvosta. Vaikka sekä kanavan laskennan että reaaliaikaisen palvelukutsun antamat arvot ovat vain arvioita käytettävissä olevasta varastosta, kanavan laskennan arvo on todennäköisemmin oikeassa nykyistä myymälää ajatellen.

Jos haluat määrittää myyntipisteen **Varastohaku**-toiminnon Commerce-pääkonttorisovelluksessa käyttämään kanavanpuoleista laskentalogiikkaa ja poistaa reaaliaikaisen palvelukutsun käytöstä, sinun täytyy ensin ottaa **Optimoitu tuotteen saatavuuden laskenta** -ominaisuus käyttöön Commerce-pääkonttorisovelluksen **Ominaisuuksien hallinta** -työtilasta ja noudattaa sitten seuraavia ohjeita.

1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit**.
1. Valitse toimintoprofiili.
1. Muuta **Toiminnot**-pikavälilehden **Varaston saatavuuden laskenta** -osassa **Varaston saatavuuden laskentatila** -kohdan arvo **Reaaliaikainen palvelu** -arvosta **Kanava**-arvoksi. Oletusarvoisesti kaikki toimintoprofiilit käyttävät reaaliaikaisia palvelukutsuja. Sinun on muutettava tämän kentän arvoa, jos haluat käyttää kanavan laskentalogiikkaa. Tämä muutos vaikuttaa jokaiseen valittuun toimintoprofiiliin linkitettyyn vähittäismyymälään.

Muutokset on sitten synkronoitava kanaviin pääkonttorin jakelun aikataulutusprosessilla seuraavien ohjeiden mukaisesti.

1. Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.
1. Suorita **1070** (**Kanavan määritys**) -työ.

Kun määritys on valmis, fyysisen käytettävissä olevan varaston tiedot eivät enää käytä reaaliaikaista palvelukutsua, kun myyntipistesovelluksen käyttäjä käyttää **Varastohaku**-toimintoa (vakio- ja matriisinäkymät). Sen sijaan nykyisen myymälän ja kaikkien täyttämisryhmän myymälöiden fyysisesti käytettävissä olevan varaston tiedot lasketaan edellisen tunnetun Commerce Headquarters -sovelluksesta kanavan tietokantaan toimitetun tilannevedoksen mukaan. Kanavan laskenta muuttaa tilannevedoksen arvoa niin, että fyysisesti käytettävissä olevan varaston arvo muuttuu kanavan tietokannan sen valitun tuotteen lisämyynnin tai palautustapahtumien perusteella, jota ei sisällytetty edelliseen synkronoituun tilannevedokseen 1130-työstä. Jos kanavan tietokanta ei sisällä tapahtumatietoja mistään täyttämisryhmän varastossa tai myymälässä, se ei sisällä muita tapahtumia arvon uudelleenlaskentaa varten. Tämän vuoksi paras käytettävissä olevan varaston arvio, joka voidaan näyttää varastoille tai myymälöille, on edellisen tunnetun Commerce Headquarters -tilannevedoksesta saatavat tiedot.

**Tilauksen täyttäminen** -näytöt myyntipisteessä hyödyntävät myös kanavan laskentaa nimikkeiden käytettävissä olevan varaston näyttämisessä, kun tilauksen täyttämisen rivi valitaan ja käyttäjä tarkastelee valitun nimikkeen käytettävissä olevan varaston **Tiedot**-paneelia.

## <a name="optimize-your-inventory-data"></a>Varastotietojen optimoiminen

Voit varmistaa varaston parhaan mahdollisen arvion saamisen, jos käytät seuraavia Commerce-erätöitä ja suoritat ne säännöllisesti:

- **P-työ** – P-työ löytyy **Jakeluaikataulut**-sivulta. Se tulee suorittaa säännöllisesti. Tämä työ tuo sähköisen kaupankäynnin tilaukset, myyntipisteen luomat asynkroniset asiakastilaukset ja myyntipisteen kanavan tietokannoista Commerce Headquarters -sovellukseen luomat noutotukkutilaukset, jotta niitä voidaan käsitellä lisää. Commerce Headquarters ei sisällä tietoja näiden tapahtumien aiheuttamista varaston tuotteiden varasto-oikaisuista ennen kuin nämä tiedot on synkronoitu kanavasta Commerce Headquarters -sovellukseen.
- **Synkronoi tilaukset** – Tämä työ käsittelee P-työn määrittämät tapahtuman raakatiedot Commerce Headquarters -sovelluksessa ja muuntaa sähköisen kaupankäynnin ja asynkronisen asiakastilauksen tapahtumat myyntitilauksiksi Commerce Headquarters -sovelluksessa. Varastotapahtumia luodaan vasta sen jälkeen, kun tämä työ on käsitelty ja myyntitilaukset on luotu. Tämän vuoksi Commerce Headquarters -sovelluksen käytettävissä olevaa varastoa ei oteta huomioon tapahtumissa.
- **Laske tapahtumaraportit eräajona** – Myymälässä luotujen noutotukkutapahtumien vähittäin suoritettava kirjausprosessi varmistaa, että myyntiin liittyvä varasto päivitetään tehokkaasti. Noutotukkutilausten varastotapahtumien käsittelyn tehokkuuden varmistamiseksi kannattaa tarkistaa, että järjestelmä on määritetty käyttämään [vähittäin suoritettavaa kirjausta](./trickle-feed.md).
- **Kirjaa tapahtumaraportit eräajona** – Tämä työ on myös pakollinen vähittäin suoritettavassa kirjauksessa. Se seuraa **Laske tapahtumaraportit eräajona** -työtä. Tämä työ kirjaa lasketut laskelmat järjestelmällisesti niin, että noutotukkumyynnin myyntitilaukset luodaan Commerce Headquarters -sovelluksessa. Näin Commerce Headquarters vastaa aiempaa tarkemmin myymälän varastoa.
- **Tuotteen saatavuus** – Tämä työ luo tilannevedoksen Commerce Headquarters -sovelluksen varastosta.
- **1130 (Tuotteen saatavuus)** – Tämä työ löytyy **Jakeluaikataulut**-sivulta. Se tulee suorittaa heti **Tuotteen saatavuus** -työn jälkeen. Tämä työ siirtää varaston tilannevedoksen tiedot Commerce Headquarters -sovelluksesta kanavan tietokantoihin.

> [!NOTE]
> - Hyvänä käytäntönä on käyttää **tuotteiden saatavuutta** ja **1130**-töitä tuntitasolla ja ajoittaa P-työtä, synkronoida tilauksia ja määrittää, että yhtä usein tai tiheämmin toistuviin töihin kirjataan liittyviä töitä.
> - Kun kanavan varaston saatavuuden laskelmia käytetään varaston saatavuuspyynnön luomisessa sähköisen kaupankäynnin ohjelmointirajapintaa tai myyntipisteen kanavan varastointilogiikkaa, suorituskyvyn varmistamiseksi laskelma käyttää välimuistia ja määrittää sen avulla, onko laskentalogiikan suorittamisesta kulunut riittävästi aikaa, jotta sen suorittaminen uudelleen on perusteltua. Välimuistin oletusarvoksi on määritetty 60 sekuntia. Tässä esimerkissä otetaan käyttöön kanavan laskennan myymälässä ja tarkastellaan tuotteen käytettävissä olevaa varastoa **Varastohaku**-sivulla. Jos tuotetta tämän jälkeen myydään yksi yksikkö, **Varastohaku**-sivulla ei näy vähennetty varasto ennen välimuistin tyhjentämistä. Käyttäjien kirjattua tapahtumia myyntipisteeseen, heidän tulee odottaa 60 sekuntia. Tämän jälkeen he voivat tarkistaa, onko käytettävissä olevaa varastoa vähennetty tapahtuman mukaan.

Jos liiketoimintaskenaario edellyttää lyhyempää välimuistin aikaa, ota yhteyttä tuotetuen edustajaan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
