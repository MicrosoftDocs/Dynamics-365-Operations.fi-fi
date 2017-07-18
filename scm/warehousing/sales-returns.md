---
title: Myyntipalautukset
description: "Tässä aiheessa on tietoja palautustilausten prosessista. Se sisältää tietoja asiakaspalautuksista ja niiden vaikutuksesta kustannuslaskentaan ja käytettävissä olevan varaston määriin."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: b66bf79413ad21f12f789eabafe8413af3f58c9c
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="sales-returns"></a>Myyntipalautukset

[!include[banner](../includes/banner.md)]


Tässä aiheessa on tietoja palautustilausten prosessista. Se sisältää tietoja asiakaspalautuksista ja niiden vaikutuksesta kustannuslaskentaan ja käytettävissä olevan varaston määriin.

Asiakas voi palauttaa nimikkeitä useista syistä. Nimike saattaa olla viallinen tai se ei ehkä täytä asiakkaan odotuksia. Palautusprosessi alkaa, kun asiakas lähettää nimikkeen palautuspyynnön. Kun asiakkaan pyyntö on vastaanotettu, palautustilaus luodaan Microsoft Dynamics 365 for Finance and Operations -järjestelmässä.

## <a name="return-order-process"></a>Palautustilausten prosessi
Seuraavassa kuvassa on yhteenveto palautustilausten prosessista.  

[![salesreturns01](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

Palautustilauksilla on kaksi prosessia: tuotteen fyysinen palautus tai pelkkä hyvitys.

-   **Fyysinen palautus** – Palautustilaus hyväksyy tuotteiden fyysisen palauttamisen.
-   **Vain hyvitys-** – Palautustilauksessa hyväksytään asiakkaan hyvittäminen, mutta tuotteiden palauttamista ei vaadita.

### <a name="physical-return-order-process"></a>Fyysisen palautustilauksen prosessi

1.  **Palautustilauksen luominen.** Dokumentoi asiakkaalle annettava hyväksyntä viallisten tai ei-toivottujen tuotteiden palauttamiseen muodollisesti. Palautustilauksessa ei edellytetä, että yritys hyväksyy palautetut tuotteet tai tarjoaa asiakkaalle hyvityksen. Jos palautus hyväksytään, voit hyväksyä korvaavan nimikkeen lähettämisen ennen, kuin viallinen nimike on palautettu.
2.  **Tuotteen saapuminen varastoon tarkastettavaksi.** Suorita alustava tarkastus ja vahvistus palautustilausasiakirjan mukaisesti. Palautustilaus tukee myös palautettujen nimikkeiden säilyttämistä lisätarkastusta ja laadunvalvontaa varten.
3.  **Määritä käsittely.** Viimeistele tarkastusprosessi ja päätä, mitä palautetuille tuotteille tulee tehdä. Tässä vaiheessa päätät myös, annatko asiakkaalle hyvityksen, hylkäätkö vai hyväksytkö tuotepalautuksen, hävitätkö tuotteen ja lähetätkö asiakkaalle korvaavan tuotteen.
4.  **Pakkausluettelon luominen.** Luo pakkausluettelo ja vahvista vaiheessa 3 tekemäsi käsittelypäätös. Viimeistele logistiikan prosessit.
5.  **Luo lasku.** Sulje palautustilaus.

### <a name="credit-only-process"></a>Vain hyvitys -prosessi

1.  **Palautustilauksen luominen.** Dokumentoi muodollisesti asiakkaalle annettava hyväksyntä hyvityksestä ilman viallisten tai ei-toivottujen tuotteiden palauttamista. **Vain hyvitys** -käsittelykoodi valtuuttaa asiakashyvityspäätöksen ilman tuotteiden fyysistä palauttamista.
2.  **Luo lasku.** Luo hyvityslasku ja sulje palautustilaus.

## <a name="return-material-authorization"></a>Palautus
Palautusten (RMA) käsittely on rakennettu myyntitilaustoiminnon varaan. RMA rekisteröidään palautustilauksena, joka luodaan myyntitilauksena, johon voi liittyä toinen myyntitilaus, eli vaihtotilaus. Molemmat myyntitilaukset on yhdistetty alkuperäiseen palautusnumeroon.

-   **Palautustilaus** – RMA rekisteröidään luomalla palautustilaus, joka on myyntitilaus, jonka määritetty tyyppi on **Palautettu tilaus.** RMA-tietoihin tehtävät muutokset päivitetään automaattisesti myyntitilaukseen. Palautustilaus ei näy myyntitilausten luetteloss, ennen kuin sen tila on **Avoin**. RMA-tilauksia käytetään palautettujen nimikkeiden saapumisen ja vastaanoton käsittelyyn sekä hyväksymään vain hyvitettävät poistotapahtumat (ks. osa **Käsittelykoodit ja poistotapahtumat**). Kaikki muuta seurantaprosessit on käsiteltävä myyntitilauksessa.
-   **Korvaava tilaus** – kun korvaava tilaus on toimitettava asiakkaalle, RMA voi sisältää toisen, siihen liittyvä myyntitilauksen. Voit luoda korvaavan tilauksen RMA:lle, joka tukee välitöntä toimitusta. Korvaava tilaus voidaan vaihtoehtoisesti luoda automaattisesti, kun saapuminen, tarkastus ja vastaanotto ovat valmiit RMA-rivinimikkeelle, jonka käsittelykoodi ilmaisee korvaamista. Korvaavalla tilauksella on samat toiminnallisuudet kuin myyntitilauksilla. Voit esimerkiksi määrittää mukautetun tuotteen korvaavaksi nimikkeeksi, luoda tuotantotilauksen palautetun nimikkeen korjaamiseksi, luoda suoratoimitus-ostotilauksen korvaavan tuotteen toimittamiseksi toimittajalta tai tukea muita tarkoituksia.

## <a name="create-a-return-order"></a>Palautustilauksen luominen
Palautustilauksen käsittely alkaa, kun asiakas ottaa organisaatioosi yhteyttä ja ilmoittaa palauttavansa viallisen tai ei-toivotun tuotteen ja/tai haluaa hyvityksen. Kun organisaatiosi on hyväksynyt palautuksen, se dokumentoidaan palautustilauksena. Tästä palautustilauksesta tulee sitten palautetun tuotteen keskipiste sen sisäisessä käsittelyssä. Seuraavassa kuvassa näytetään palautustilauksen luomisen toimintaohjeet.  

[![Palautustilauksen luomisen toimintaohjeet](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Luo palautustilauksen otsikko

Kun luot palautustilauksen, siihen tulee sisältyä seuraavassa taulukossa olevat tiedot.

| Kenttä              | kuvaus                                              | Huomautukset                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Asiakastili   | Viite Asiakkaat-taulukkoon                       | Sinun on määritettävä olemassa oleva asiakastili.                                                                                                                                                                                                                                                                                                  |
| Toimitusosoite   | Nimikkeen palautusosoite                 | Oletusarvona käytetään organisaation osoitetta. Jos otsikossa on valittu tietty varasto, toimitusosoitteeksi muutetaan kyseisen varaston toimitusosoite. Voit muuttaa tätä osoitetta **Palautustilauksen tiedot** -sivulla.                                                                                                  |
| Sijainti/varasto     | Sijainti tai varasto, joka vastaanottaa palautetun tuotteen | Palautustilauksen toimitusosoite määritetään sijainnin tai varaston toimitusosoitteen perusteella.                                                                                                                                                                                                                                 |
| Palautusnumero         | Palautustilaukseen liitetty tunnus              | Palautustilauksen käsittelyn vaihtoehtoisena avaimena käytetään palautusnumeroa. Määritettävä palautusnumero perustuu **Myyntireskontran parametrit** -sivulla määritettyyn palautusnumeron sarjaan.                                                                                                                              |
| Määräaika           | Viimeinen päivämäärä, jolloin nimike voidaan palauttaa               | Oletusarvo lasketaan kaavalla nykyinen päivämäärä + voimassaoloaika. Jos esimerkiksi palautus on kelvollinen vain 90 päivää palautustilauksen luonnin jälkeen ja kyseinen tilaus on luotu 1. toukokuuta, kentän arvo on **30-Heinä**. Voimassaoloaika määritetään **Myyntireskontran parametrit** -sivulla. |
| Palautuksen syykoodi | Asiakkaan syy tuotteen palauttamiselle          | Syykoodi on valitaan käyttäjän määrittämästä syykoodien luettelosta. Voit päivittää tätä kenttää milloin tahansa.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Luo palautustilauksen rivit

Kun palautuksen otsikko on valmis, voit luoda palautusrivejä jollakin seuraavista tavoista:

-   Anna nimikkeen tiedot, määrä ja muut tiedot kullekin palautusriville manuaalisesti.
-   Luo palautusrivi käyttämällä **Etsi myyntitilaus** -toimintoa. Suosittelemme, että käytät tätä toimintoa, kun luot palautustilauksen. **Etsi myyntitilaus** -toiminto määrittää viitteen palautusriviltä laskutetulle myyntitilausriville ja hakee rivin tiedot, kuten nimiketunnuksen, määrän, hinnan, alennuksen ja kustannusarvot myyntiriviltä. Viittaus takaa, että kun tuote palautetaan yritykselle, se arvostetaan samalle yksikkökustannukselle, jolla se myytiin. Viittaus myös varmistaa, että palautustilauksia ei ole luotu määrälle, joka yrittää laskulla myydyn määrän.

**Huomautus:** palautusrivejä, joilla on viittaus myyntitilaukseen, käsitellään myynnin korjauksina tai peruutuksina. Lisätietoja jäljempänä tämän aiheen osiossa “Kirjaa kirjanpitoon”.

### <a name="charges"></a>Kulut

Maksut voidaan lisätä palautustilaukseen jollain seuraavista tavoista:

-   Voit lisätä kulut manuaalisesti palautustilauksen otsikkotietoihin, palautustilauksen riville tai molempiin.
-   Maksut voidaan lisätä palautustilauksen otsikkotietoihin automaattisesti palautuksen syykoodin funktiona.
-   Maksut voidaan lisätä palautustilauksen rivin tietoihin automaattisesti rivin käsittelykoodin funktiona.

Kulut lisätään automaattisesti, kun riville on määritetty palautuksen syykoodi tai käsittelykoodi. Jos syykoodia muutetaan jälkikäteen, aiemmin lisättyä kulutapahtumaa ei poisteta, mutta riville voidaan lisätä uusi kulutapahtuma uudesta syykoodista riippuen. Kun lisäät palautustilauksen riveille kuluja, rivin tai tilauksen prosenttiosuutena laskettavat kulut muutetaan negatiivisiksi kun rivi tai rivin tilaus on negatiivinen, ellei prosenttiosuus itsessään ole negatiivinen luku. Kulu, jonka arvo on negatiivinen tarkoittaa asiakkaalle tehtävää hyvitystä.

### <a name="return-reason-codes"></a>Palautuksen syykoodit

Voit helpottaa palautusmallien analysointia käyttämällä palautuksissa syykoodeja. Syykoodit sisältävät tietoja siitä, miksi asiakas haluaa palauttaa nimikkeen. Joillakin organisaatioilla on useita syykoodeja. Nämä organisaatiot voivat ryhmitellä syykoodit syykoodiryhmiksi saadakseen paremman yleiskuvan sekä kumulatiivista raportointia varten.

### <a name="disposition-codes-and-disposition-actions"></a>Käsittelykoodit ja käsittelytoimenpiteet

Palautustilauksen prosessissa tärkeä vaihe on käsittelykoodin määrittäminen palautustilauksen riville saapumisrekisteröinnin yhteydessä. Käsittelykoodi määrittää seuraavat tiedot:

-   **Taloudelliset vaikutukset** – Hyvitetäänkö asiakasta palautetuista nimikkeistä, ja tuleeko palautustilauksen riville lisätä kuluja?
-   **Palautetun nimikkeen käsittely** – Lisätäänkö nimike takaisin varastoon, hävitetäänkö nimike vai palautetaanko se asiakkaalle?
-   **Palautetun nimikkeen logistiikka** – Lähetetäänkö asiakkaalle korvaava nimike?

Palautettujen tavaroiden poistamistavan määrittämisen lisäksi käsittelykoodit voivat luoda kustannuksia palautusriveille. Niitä voidaan myös käyttää palautusten ryhmittelyyn tilastollista analyysiä varten. Käsittelykoodit määritellään palautustilausten määrityksen yhteydessä. Jokaisen käsittelykoodin on kuitenkin viitattava yhteen valmiista käsittelytoimenpiteistä. Seuraavassa taulukossa on luettelo valmiista käsittelykoodeista ja niiden toimenpiteistä. **Tärkeää:** jos kohdetta ei tule palauttaa, mutta asiakkaalle annetaan hyvitys, määritä palautusriville **Vain hyvitys** -käsittelykoodi.

<table>
<thead>
<tr class="header">
<th>Käsittelykoodi</th>
<th>Taloudelliset vaikutukset</th>
<th>Logistiikan vaikutukset</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vain hyvitys</td>
<td><ul>
<li>Asiakkaalle hyvitetään myyntihinta vähennettynä maksuilla ja kuluilla.</li>
<li>Nimikkeen hävittämistappio kirjataan kirjanpitoon.</li>
</ul></td>
<td>Nimikettä ei saa palauttaa. Tätä käsittelytoimenpidettä käytetään seuraavissa tapauksissa:
<ul>
<li>Osapuolten välillä on riittävä luottamus.</li>
<li>Viallisen nimikkeen palautuskustannus on kohtuuton.</li>
<li>Nimikkeitä ei voi päästää takaisin varastoon. Fyysistä palautusta ei tarvita muiden olosuhteiden vuoksi.</li>
</ul></td>
</tr>
<tr class="even">
<td>Hyvitys</td>
<td><ul>
<li>Asiakkaalle hyvitetään myyntihinta vähennettynä maksuilla ja kuluilla.</li>
<li>Varaston arvo nousee palautetun nimikkeen kustannuksen mukaisesti.</li>
</ul></td>
<td>Nimike palautetaan ja lisätään takaisin varastoon.</td>
</tr>
<tr class="odd">
<td>Korvaus ja hyvitys</td>
<td><ul>
<li>Asiakkaalle hyvitetään myyntihinta vähennettynä maksuilla ja kuluilla.</li>
<li>Varaston arvo nousee palautetun nimikkeen kustannuksen mukaisesti.</li>
<li>Korvaavalle tuotteelle luodaan erillinen myyntitilaus, joka käsitellään erikseen.</li>
</ul></td>
<td>Nimike palautetaan ja lisätään takaisin varastoon.</td>
</tr>
<tr class="even">
<td>Korvaus ja hävitys</td>
<td><ul>
<li>Asiakkaalle hyvitetään myyntihinta vähennettynä maksuilla ja kuluilla.</li>
<li>Nimikkeen hävittämistappio kirjataan kirjanpitoon.</li>
<li>Korvaavalle tuotteelle luodaan erillinen myyntitilaus, joka käsitellään erikseen.</li>
</ul></td>
<td>Nimike palautetaan ja hävitetään.</td>
</tr>
<tr class="odd">
<td>Palautus asiakkaalle</td>
<td>Ei mitään, paitsi maksut ja kulut.</td>
<td>Nimike palautetaan, mutta lähetetään takaisin asiakkaalle tarkastuksen jälkeen. Tätä käsittelytoimenpidettä voidaan käyttää, jos nimike on tahallisesti vioitettu tai takuu on mitätöity.</td>
</tr>
<tr class="even">
<td>Hävikki</td>
<td><ul>
<li>Asiakkaalle hyvitetään myyntihinta vähennettynä maksuilla ja kuluilla.</li>
<li>Nimikkeen hävittämistappio kirjataan kirjanpitoon.</li>
</ul></td>
<td>Nimike palautetaan tai hävitetään.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Tuotteen saapuminen varastoon tarkastettavaksi.
Ennen kuin voit vastaanottaa palautetut nimikkeet varastoon fyysisesti kirjaamalla pakkausluettelon, nimikkeille on tehtävä saapumisrekisteröinti ja valinnainen tarkastus. Seuraavassa kuvassa on yhteenveto saapumisprosessista. Seuraavat osat kuvaavat kaikki kuvassa näytetyt vaiheet.  

[![Saapumisprosessi](./media/salesreturn03.png)](./media/salesreturn03.png)  

Prosessilla on useita muunnelmia, joita ei käsitellä tässä ohjeaiheessa. Tässä on esimerkkejä kyseisistä muunnelmista:

-   Älä käytä **Saapumisten yhteenveto** -luetteloa Saapumisen kirjauskansion luomiseen. Luo Saapumisen kirjauskansio manuaalisesti sen sijaan. Palautustilausten viitteenä on **Myyntitilaus**.
-   Jos käytät Varastonhallintaa, luo kuormalavakuljetukset. Palautusrivin tila on **Saapunut** kuormalavakuljetuksen aikana.
-   Rekisteröi palautetun nimikkeen saapuminen suoraan palautustilauksen riviltä **Rekisteröinti**-toiminnolla.

Palautusten saapuminen on integroitu yleiseen varastosaapumisten prosessiin. Saapumisprosessi tukee myös palautettujen nimikkeiden sivuun ottamista, jos niille on tehtävä erillinen tarkastus.

### <a name="identify-products-in-the-arrival-overview-list"></a>Tunnista tuotteet Saapumisten yhteenvetoluettelossa

**Saapumisten yhteenveto** -sivulla on lueteltu kaikki suunnitellut saapumiset. **Huomautus:** palautustilauksille saapuvat tuotteet on käsiteltävä erikseen muista saapumistapahtumista. Kun olet tunnistanut saapuvan paketin **Saapumisten yhteenveto** -sivulla (esimerkiksi RMA-saateasiakirjan avulla), napsauta toimintoruudusta **Aloita saapuminen** -painiketta luodaksesi saapumista vastaavan Saapumisen kirjauskansion.

### <a name="edit-the-arrival-journal"></a>Muokkaa saapumisen kirjauskansiota

Määrittämällä **Karanteeninhallinta** asetukseksi **Kyllä**, voit luoda palautusriville karanteenitilauksen. Jos rivi on lähetetty karanteeniin tarkastettavaksi, et voi määrittää käsittelykoodia. **Huomautus:** jos nimikkeen varastomalliryhmän **Karanteeninhallinta** -asetus on **Kyllä**, **Kirjauskansiorivit**-sivun **Karanteeninhallinta**-asetus on merkittynä saapumisten kirjauskansioriveille, eikä sitä voi muuttaa. Jos rivi lähetetään karanteeniin, sille on määritettävä sopiva karanteenivarasto. Jos saapumisriviä ei lähetetä tarkastettavaksi, varaston saapumisvirkailijan on määritettävä käsittelykoodi suoraan saapumisen kirjauskansioriville ja kirjattava sitten saapumisen kirjauskansio. Jos samaa käsittelykoodia ei tule liittää palautusrivin koko määrään tai jos rivin koko määrää ei ole vielä vastaanotettu, rivi on jaettava. Kun jaat saapumisen kirjauskansiorivin, voit myös jakaa palautusrivin (**SalesLine**) ja luoda uuden erätunnuksen. Voit jakaa rivin vähentämällä saapumisen kirjauskansiorivin määrää. Kun kirjauskansio kirjataan, luodaan uusi palautusrivi, jonka tila on **Odotettu** jäljellä olevan määrän osalta. Voit myös jakaa rivin valitsemalla **Toiminnot** &gt; **Jako**.

### <a name="process-the-quarantine-order"></a>Karanteenitilauksen käsittely

Jos palautetut tuotteet lähetetään tarkastettavaksi karanteenivarastossa, muu käsittely suoritetaan karanteenitilauksessa. Kullekin karanteeniin lähetetylle saapumisriville luodaan karanteenitilaus. Käsittelykoodi ilmaisee tarkastusprosessin tuloksen. Voit jakaa karanteenitilauksen samalla tavalla kuin saapumisen kirjauskansion voi jakaa. Jos jaat karanteenitilauksen, vastaava palautusrivi jaetaan myös. Kun olet syöttänyt käsittelykoodin, päätä karanteenitilaus joko **Päätä**-toiminnolla tai **Ilmoita valmiiksi** -toiminnolla. Jos valitset **Ilmoita valmiiksi**, määritettyyn varastoon luodaan uusi saapuminen. Voit sitten käsitellä tämän saapumisen **Saapumisten yhteenveto** -sivulla. Jos saapuminen on peräisin karanteenitilauksesta, et voi muuttaa sille tarkastuksen aikana määritettyä käsittelykoodia. Jos teet karanteenitilauksen valmiiksi **Päätä**-toiminnolla, erä rekisteröidään automaattisesti. Nimike saatetaan joskus lähettää karanteenista takaisin lähetys- ja vastaanotto-osastolle. Esimerkiksi karanteenitarkastaja ei ehkä tiedä, mihin nimike varastoidaan. Tässä tapauksessa vastaava pakkausluettelo on päivitettävä, jotta se rekisteröi ja toimii karanteenin seurauksena määritetyn käsittelykoodin kanssa. Vastaanottokuittaukset voidaan lähettää asiakkaalle, kun palautusrivi rekisteröidään. **Palautuksen kuittaus** -raportti muistuttaa palautustilauksen asiakirjaa. **Palautuksen kuittaus** -raporttia ei kirjata tai rekisteröidä järjestelmään muutoin, eikä se ole palautustilausprosessin pakollinen vaihe.

## <a name="replace-a-product"></a>Tuotteen korvaaminen
Korvaavien tuotteiden hallintaan on kaksi menetelmää:

-   **Ennakolta tehtävä korvaus** – tuotteen korvaaminen ennen, kuin palautettava tuote on vastaanotettu asiakkaalta.
-   **Korvaus käsittelykoodilla** – luo uuden korvaustilauksen rivin automaattisesti.

### <a name="up-front-replacement"></a>Ennakolta tehtävä korvaus

Ennakolta tehtävässä korvauksessa korvaava tuote voidaan toimittaa asiakkaalle ennen, kuin palautus on vastaanotettu. Tämä menetelmä on hyödyllinen, jos nimike on esimerkiksi koneen osa, jota ei voi irrottaa ennen kuin sille on saatavilla varaosa, tai jos haluat, että asiakkaasi saa korvaavan tuotteen niin pian kuin mahdollista. Ennakolta tehtävä korvaustilaus on itsenäinen myyntitilaus. Otsikkotiedot alustetaan asiakkaan perusteella ja rivin tiedot alustetaan palautustilauksesta. Voit muokata, käsitellä ja poistaa korvaustilausta erillään palautustilauksesta. Kun poistat korvaustilauksen, näyttöön tulee sanoma, että tilaus on luotu korvaustilaukseksi. Seuraavassa kuvassa esitellään ennakolta tehtävän korvauksen prosessi.  

[![Ennakolta tehtävän korvauksen prosessi](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)  

Palautustilaus sisältää viittauksen korvaustilaukseen. Jos palautustilaukselle luodaan ennakolta tehtävä korvaustilaus ennen, kuin viallinen tuote on palautettu, et voi valita käsittelykoodeja korvaukselle sen jälkeen, kun viallinen tuote on palautettu.

### <a name="replacement-by-disposition-code"></a>Korvaaminen käsittelykoodin perusteella

Jos toimitat asiakkaalle korvaavan nimikkeen ja käytät palautustilauksessa **Korvaus ja hävitys**- tai **Korvaus ja hyvitys** -käsittelytoimenpidettä, käytä prosessia, joka esitellään seuraavassa kuvassa.  

[![Korvausprosessi, kun käytössä on käsittelykoodi](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)  

Korvaava nimike toimitetaan itsenäisen myyntitilauksen, eli korvaavan myyntitilauksen avulla. Tämä myyntitilaus luodaan, kun palautustilauksen pakkausluettelo muodostetaan. Tilauksen otsikossa käytetään asiakkaan tietoja, joihin viitataan palautustilauksen otsikossa. Rivin tiedot on kerätään tiedoista, jotka on syötetty **Korvaava nimike** -sivulla. **Korvaava nimike** -sivulle on täytettävä rivit, joilla on käsittelytoimenpiteitä, jotka alkavat sanalla "korv". Korvaavan nimikkeen määrää tai tyyppiä ei kuitenkaan vahvisteta tai rajoiteta. Tämä mahdollistaa tapaukset, joissa asiakas haluaa saman nimikkeen eri kokoonpanossa tai koossa, sekä tapaukset, joissa asiakas haluaa täysin eri nimikkeen. Samanlainen nimike syötetään oletuksena **Korvaava nimike** -sivulle. Voit kuitenkin valita toisen nimikkeen, jos kyseinen toiminto on otettu käyttöön. **Huomautus:** voit muokata ja poistaa korvaavan myyntitilauksen, kun se on luotu.

## <a name="generate-a-packing-slip"></a>Pakkausluettelon luominen.
Ennen kuin palautetut nimikkeet voidaan vastaanottaa varastoon, sen tilauksen pakkausluettelo, johon palautetut nimikkeet kuuluvat, on päivitettävä. Samalla tavoin kuin laskun päivitysprosessi kirjanpitotapahtumaksi pakkausluettelon päivitysprosessi on varastotietueen fyysinen päivitys. Toisin sanoen se vahvistaa muutokset varastoon. Kun kyseessä on palautus, käsittelytoimenpiteen vaiheet toteutetaan pakkausluettelon päivityksen aikana. Kun muodostat pakkausluettelon, suoritetaan seuraavat tapahtumat:

-   Varastossa suoritetaan fyysinen vastaanotto vakioprosessin mukaisesti. Kirjanpidon kirjaukset luodaan, jos varastointimallin ryhmä (**Kirjaa varastotilanne**) ja myyntireskontran parametrit (**Kirjaa pakkausluettelo kirjanpitoon**) on määritetty oikein.
-   Nimikkeet, jotka on merkitty käsittelytoimenpiteellä, jonka nimessä on "hävit" hävitetään, ja varastotappio kirjataan kirjanpitoon.
-   Nimikkeet, jotka on merkitty **Palautetaan asiakkaalle** -käsittelytoimenpiteellä vastaanotetaan ja toimitetaan asiakkaalle. Näillä nimikkeillä ei ole nettovaikutusta varastoon.
-   Korvaava myyntitilaus on luotu. Tämä myyntitilaus perustuu **Korvaava nimike** -sivun tietoihin.

Voit luoda pakkausluettelon ainoastaan riveille, joiden palautustila on **Rekisteröity** ja ainoastaan palautusrivin täydelle määrälle. Jos usealla palautustilauksen rivillä on **Rekisteröity**-tila, voit pakkausluettelon rivin osajoukolle poistamalla muut rivit **Kirjaa pakkausluettelo** -sivulta. Osapalautukset määritetään palautustilausrivien, ei palautustilauslähetyksen mukaan. Se tarkoittaa sitä, että jos vastaanotat yhdellä palautustilausrivillä osoitetun koko määrän, mutta et mitään muilla palautustilausriveillä osoitettuja määriä, toimitus ei ole osatoimitus. Jos kuitenkin palautustilausrivi kutsuu palautettavaksi tietyn nimikkeen 10 yksikköä ja vastaanotat vain neljä, kyseessä on osatoimitus. Jos kaikki odotetut palautusnimikkeet eivät ole saapuneet, voit asettaa toimituksen syrjään ja odottaa, että loppu palautettava määrä saapuu. Vaihtoehtoisesti voit rekisteröidä ja kirjata osittaisen määrän. Pakkausluetteloiden kirjaamisprosessin osana on mahdollista liittää pakkausluettelon viitenumero asiakkaan toimitusasiakirjoista tilausriveille. Tämä liitos on valinnainen ja on tarkoitettu vain tiedoksi. Se ei vaikuta tapahtumaan liittyviin päivityksiin. Pakkausluetteloprosessin voi yleensä ohittaa ja siirtyä suoraan laskutukseen. Näissä tapauksissa pakkausluettelon muodostamisen aikana suoritettavat vaiheet tehdään laskutuksen aikana.

## <a name="generate-an-invoice"></a>Luo lasku
Vaikka **Palautustilaus**-sivu sisältääkin tietoja ja toimintoja, joita tarvitaan palautustilauksen erityisten logistiset erityisnäkökohtien käsittelyyn, laskutusprosessi on vietävä loppuun **Myyntitilaus**-sivulla. Organisaatiosi voi sitten laskuttaa palautus- ja myyntitilaukset samanaikaisesti, ja sama henkilö voi saattaa laskutusprosessin loppuun tarpeen mukaan. Voit tarkastella palautustilausta **Myyntitilaus**-sivulla napsauttamalla myyntitilauksen numeron linkkiä, joka avaa liittyvän myyntitilauksen. Palautustilauksen löydät myös **Kaikki myyntitilaukset** -sivulta. Palautustilaukset ovat myyntitilauksia, joiden tilaustyyppi on **Palautettu tilaus**.

### <a name="credit-correction"></a>Hyvityksen oikaisu

Varmista, osana laskutusprosessia, että muut kulut ovat oikein. Jotta kirjauskansion kirjaukset tehdään korjauksina (Storno), harkitse käyttäväsi **Hyvityksen oikaisu** -asetusta **Laskun kirjaus** -sivun **Muu**-välilehdellä kun kirjaat laskun/hyvityslaskun. **Huomautus:** oletusarvon mukaan **Hyvityksen oikaisu** -asetus on aktiivinen, jos **Korjaus hyvityslaskulla** -asetus on otettu käyttöön **Myyntireskontran parametrit** -sivulla. Suosittelemme kuitenkin, että et kirjaa palautuksia Stornolla.

## <a name="create-intercompany-return-orders"></a>Luo konsernin sisäiset palautustilaukset
Palautustilauksia voi suorittaa kahden organisaatiosi sisäisen yrityksen välillä. Seuraavia tilanteita tuetaan:

-   Yksinkertaiset palautukset kahden yrityksen välillä, joilla on konserninsisäinen suhde
-   Konsernin sisäinen ketju, joka määritetään, kun asiakkaan palautustilaus luodaan myyjäyrityksessä
-   Konsernin sisäinen ketju, joka määritetään, kun toimittajan palautustilaus luodaan ostajayrityksessä
-   Suoratoimituspalautukset ulkoisen asiakkaan ja kahden, konsernin sisäisessä suhteessa olevan yrityksen välillä

### <a name="setup"></a>Luo perustiedot

Seuraavassa kuvassa esitellään vähimmäismääritys, joka tarvitaan kahden yrityksen konsernin sisäiseen suhteeseen ja konsernin sisäiseen kaupankäyntiin.  

[![Vähimmäisasetukset](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)  

Seuraavassa tilanteessa CompBuy on ostava yritys, ja CompSell on myyjäyritys. Yleensä myyjäyritys toimittaa tavarat ostavalle yritykselle tai, suoratoimitustapauksissa suoraan loppuasiakkaalle. CompBuy on määritellyt toimittajan IC\_CompSell konsernin sisäiseksi päätepisteeksi, joka on liitetty CompSell-yritykseen. Samanaikaisesti CompSell on määritellyt asiakkaan IC\_CompBuy konsernin sisäiseksi päätepisteeksi, joka on liitetty CompBuy-yritykseen. Molempiin yrityksiin on määritettävä asianmukaiset toimintakäytännöt ja arvon määritykset. Suoratoimitustilanteessa konsernin sisäinen palautustilaus, joka on lisäksi konsernin sisäinen myyntitilaus luodaan myyjäyrityksessä. Konsernin sisäisen palautustilauksen palautusnumeron voi poimia CompSellin RMA-numerosarjasta, tai se voidaan kopioida CompBuyn alkuperäisen palautustilauksen palautusnumerosta. Palautusnumeron asetukset CompBuyn **PurchaseRequisition**-toimintakäytännössä määrittävät nämä toiminnot. Jos palautusnumero synkronoidaan suosittelemme valmistautumaan numeroristiriitariskin lieventämiseen, jos molemmat yritykset käyttävät samaa numerosarjaa.

### <a name="simple-intercompany-returns"></a>Yksinkertainen konsernin sisäinen palautus

Tähän tilanteeseen liittyy kaksi saman organisaation yritystä seuraavan kuvan mukaisesti.  

[![Yksinkertainen konsernin sisäinen palautus](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)  

Tilaus-toimitusketjun voi muodostaa, kun toimittajan palautustilaus luodaan ostavassa yrityksessä tai asiakkaan palautustilaus luodaan myyjäyrityksessä. Finance and Operations luo vastaavan tilauksen toiseen yritykseen ja varmistaa, että toimittajan palautustilauksen otsikko- ja rivitiedot vastaavat asiakkaan palautustilauksen asetuksia. Luotu palautustilaus joko sisältää tai jättää pois viittauksen (**Etsi myyntitilaus**) olemassa olevaan asiakkaan laskuun. Kummankin tilauksen pakkausluettelo ja lasku voidaan käsitellä erikseen. Sinun ei tarvitse luoda pakkausluetteloa toimittajan palautustilaukselle ennen kuin luot pakkausluettelon asiakkaan palautustilaukselle.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Suoratoimitettavat palautukset kolmen osapuolen kesken

Tämä tilanne voidaan luoda, jos edellisen **Suoratoimitus**-tyyppinen myynti on valmis ja asiakkaan kanssa toimivalla yrityksellä on asiakasta koskeva lasku. Seuraavassa kuvassa CompBuy on myynyt ja laskuttanut tuotteita asiakkaalle Extern. Tuotteet on toimitettu suoraan CompSell-yritykseltä asiakkaalle konsernin sisäisen tilausketjun kautta.  

[![Suoratoimitettavat palautukset kolmen osapuolen kesken](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)  

Jos ulkoinen asiakas haluaa palauttaa tuotteet, CompBuy-yritys luo asiakkaalle palautustilauksen (RMA02). Konsernin sisäinen ketju luodaan, kun palautustilaus merkitään suoratoimitettavaksi. Kun käytät **Etsi myyntitilaus** -toimintoa etsiessäsi palautettavan myyntilaskun, luodaan konsernin sisäinen tilausketju, joka koostuu seuraavista asiakirjoista:

-   **Alkuperäinen palautustilaus:** RMA02 (CompBuy)
-   **Ostotilaus:** PO02 (CompBuy)
-   **Konsernin sisäinen palautustilaus:** RMA\_00032 (CompSell)

Kun suoratoimituksen konsernin sisäinen ketju on luotu, kaikki palautuksen fyysiset käsittelytoimet on suoritettava CompSell-yrityksen konsernin sisäisen palautustilauksen RMA\_00032 kontekstissa. CompBuy ei voi vastaanottaa tuotteita. Kun konsernin sisäiselle palautustilaukselle määritetään käsittelykoodi, se synkronoidaan alkuperäiseen palautustilaukseen, jotta alkuperäinen tilaus voidaan laskuttaa oikein.

## <a name="post-to-the-ledger"></a>Kirjaa kirjanpitoon
Kirjanpidon kirjauksiin, jotka luodaan, kun palautustilaus laskutetaan vaikuttavat tietyt tärkeät asetukset ja parametrit:

-   **Palautuksen kustannushinta** – muut kuin **standardikustannus**-varastotuotteet, **Palautuksen kustannushinta** -parametri määrittää nimikkeen kustannuksen, kun se hyväksytään takaisin varastoon tai hävitetään. Jotta varaston arvo lasketaan oikein, **Palautuksen kustannushinta** -parametri on asetettava oikein. Jos käytät **Etsi myyntitilaus** -toimintoa palautustilausrivin luomiseen, joka viittaa myyntilaskuun, **Palautuksen kustannushinta** -arvo on sama kuin myytävän nimikkeen kustannushinta. Muussa tapauksessa kustannushinta-arvo on peräisin nimikkeet määrityksistä, tai se voidaan syöttää manuaalisesti.
-   **Hyvityksen oikaisu/Storno** – **Hyvityksen oikaisu** -parametri **Laskun kirjaus** -sivulla määrittää, tulisiko kirjaukset tehdä positiivisina (DR/CR) tapahtumina vai korjaavina, negatiivisina tapahtumina.

Seuraavissa esimerkeissä palautuksen kustannushinta esitetään **Varastokustannushinta**-arvolla.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Esimerkki 1: Palautustilauksessa ei ole viittausta myyntilaskuun

Palautustilauksessa ei ole viittausta myyntilaskuun. Palautettu nimike hyvitetään. **Hyvityksen korjaus** -parametri ei ole valittuna, kun palautustilauksen laskun tai hyvityslasku muodostetaan.  

[![Palautustilauksessa ei ole viittausta myyntilaskuun](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)  

**Huomautus:** nimikkeen päätietuehintaa käytetään **Palautuksen kustannushinta** -parametrin oletusarvona. Oletushinta eroaa kustannushinnasta varasto-oton hetkellä. Vaikutus on siis, että on syntynyt tappio-arvo on 3. Palautustilaus ei lisäksi sisällä alennusta, joka asiakkaalle oli annettu myyntitilauksessa. Tämän vuoksi ilmenee liian suuri hyvitys.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Esimerkki 2: Hyvityksen korjaus on valittuna palautustilaukselle

Esimerkki 2 on muuten sama kuin esimerkki 1, mutta **Hyvityksen korjaus** -parametri on valittuna, kun palautustilauksen lasku muodostetaan.  

[![Hyvityksen korjaus on valittuna palautustilaukselle ](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)  

**Huomautus:** kirjanpidon kirjaukset syötetään negatiivisina oikaisuina.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Esimerkki 3: Palautustilauksen rivi on luotu Etsi myyntitilaus -toiminnolla

Tässä esimerkissä palautustilauksen rivi on luotu **Etsi myyntitilaus** -toiminnolla. **Hyvityksen korjaus** -parametri ei ole valittuna, kun lasku luodaan.  

[![Palautustilauksen rivi on luotu Etsi myyntitilaus -toiminnolla ](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)  

**Huomautus:** **Alennus** ja **Palautuksen kustannushinta** on määritetty oikein. Tämän vuoksi myyntilasku ilmenee käännettynä.




