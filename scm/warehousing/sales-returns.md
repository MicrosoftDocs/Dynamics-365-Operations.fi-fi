---
title: Myyntipalautukset
description: "Tässä aiheessa on tietoja palautustilausten prosessista. Se sisältää tietoja asiakaspalautukset ja niiden vaikutus kustannuslaskennan ja käytettävissä olevan varaston määrien."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3d02a15387231160f5b8a237aa11008b91ef1223
ms.openlocfilehash: b265a20a271230de5dba6df93900a24aad642885
ms.lasthandoff: 03/31/2017


---

# <a name="sales-returns"></a>Myyntipalautukset

Tässä aiheessa on tietoja palautustilausten prosessista. Se sisältää tietoja asiakaspalautukset ja niiden vaikutus kustannuslaskennan ja käytettävissä olevan varaston määrien.

Asiakkaille voi palauttaa kohteita eri syistä. Kohde saattaa olla viallinen, tai se ei täytä asiakkaan odotuksia. Palaa prosessi alkaa, kun asiakas palauttaa nimikkeen pyynnön. Kun asiakkaan pyyntö on vastaanotettu, palautustilaus luodaan Microsoft Dynamics-365 operaatioille.

## <a name="return-order-process"></a>Palautustilauksen käsittely
Seuraavassa kuvassa on yleiskuvaus palautustilauksen käsittely.  

[![salesreturns01](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

Palautustilauksen käsittely on kahdenlaisia: fyysinen palaa ja hyvittää vain.

-   **Fyysinen tuotto** – palautustilauksen valtuuttaa tuotteiden fyysistä palauttamista.
-   **Vain kredit-** – palautustilauksen valtuuttaa asiakkaan luotto mutta ei edellytä, että asiakas palauttaa tuotteet fyysisesti.

### <a name="physical-return-order-process"></a>Fyysinen palautustilauksen käsittely

1.  **Luo palautustilaus.** Muodollisesti asiakirjan palauttaa viallinen tai ei-toivottuja tuotteita asiakkaan lupa. Palautustilausta ei edellytä yhtiön Hyväksy palautettuja tuotteita tai antaa hyvityksen asiakkaalle. Jos palautus on hyväksytty, voit antaa korvaavan nimikkeen viallinen nimike on palautettu ennen lähettämistä.
2.  **Saapuvat varastosta tarkastusta varten.** Alustava tarkastus- ja vastaan asiakirjan palautustilauksen vahvistus loppuun. Palautustilauksen tukee myös muita tarkastuksen ja laadunvalvonnan palautetut nimikkeet karanteenissa.
3.  **Määrittää poistamisen.** Viimeistele tarkastusprosessi ja päättää mitä tulee tehdä palautetut tuotteet. Osana tässä vaiheessa päättää, onko haluat hyvittää asiakkaan, tuotteen palautus, Hylkää tai hyväksy tuotteen palauttamista, hävittää tuotteen ja lähettää asiakkaalle korvaavan tuotteen.
4.  **Luo pakkausluettelo.** Luo pakkausluettelo ja vahvista poistamisen, vaiheessa 3 tekemäsi päätös. Viimeistele Logistiikka-prosessit.
5.  **Luo lasku.** Sulje palautustilauksen.

### <a name="credit-only-process"></a>Käsittele vain kredit

1.  **Luo palautustilaus.** Muodollisesti asiakirjan vastaanottamaan kreditin palaamatta viallinen tai ei-toivottujen tuotteiden asiakkaan lupa. **Vain kredit-** käsittelykoodi valtuuttaa päätös hyvittää asiakkaalle ilman fyysistä palauttamista.
2.  **Luo lasku.** Luo hyvityslasku ja suljet palautustilauksen.

## <a name="return-material-authorization"></a>Palauttaa materiaalin luvan
Materiaalin luvan (RMA) palautuksen käsittely perustuu myyntitilaukseen toimintoja. Palautustilaus, johon myyntitilaus luodaan, ja niillä voi olla toiseen myyntitilaukseen liitetty kutsutaan korvaava tilaus on rekisteröity RMA. Sekä myyntitilauksissa linkittää alkuperäisen palautusnumero.

-   **Palautustilausten** – Rekisteröi RMA Luo palautustilaus, joka on myyntitilauksen, joka on määritetty tyyppi, **palauttaa järjestys.** RMA-tietoihin tekemäsi muutokset päivitetään automaattisesti myyntitilaukseen. Palautustilauksen tila on vasta **avoin**, se ei tule myyntitilausten luettelo. Käytät RMA saapumisen ja palautettujen nimikkeiden vastaanoton sekä sallia vain kredit-poistotehtävänä (kohdassa **käsittelykoodit ja poistotapahtumia**). Kaikki seuranta prosessit on käsiteltävä myyntitilauksen.
-   **Korvaava tilaus** – kun korvaava tilaus on toimitettu asiakkaalle RMA voi olla toinen liittyvä myyntitilaus. Välitön toimitus tukemaan RMA korvaavan tilauksen voi luoda manuaalisesti. Vaihtoehtoisesti korvaava tilaus voidaan luoda automaattisesti kun RMA rivinimikkeen käsittelykoodi, joka ilmaisee korvaaminen on suoritettu saapumisen, tarkastus ja vastaanotto. Korvaava tilaus on samalla tavalla, joka on liitetty myyntitilaukseen. Esimerkiksi voit määrittää mukautetun tuotteen korvaavaa nimikettä, luoda tuotantotilauksen korjaa palautettua nimikettä, Luo suoratoimitus ostotilaus korvaaminen lähettää toimittajalta tai tukea muihin tarkoituksiin.

## <a name="create-a-return-order"></a>Palautustilauksen luominen
Palautustilauksen käsittely alkaa, kun asiakas ottaa organisaatioon palauttaa viallinen tai ei-toivottujen tuotteiden ja/tai hyvitetty. Kun organisaatio on hyväksynyt palautuksen, palautustilauksen dokumentoitu palauttamista. Tämän palautustilauksen tulee sisäiseen käsittelyyn palautetun tuotteen yhteysyksikön. Seuraavassa kuvassa näkyy palautustilauksen luomisen toimintaohjeita.  

[![Palautustilauksen luomisen toimintaohjeita](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Luo palautustilaus-otsikko

Kun luot palautustilauksen, seuraavassa taulukossa tiedot on sisällytettävä.

| Kenttä              | kuvaus                                              | Huomautukset                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Asiakastili   | Asiakkaat-taulukko viittaa                       | Olemassa oleva asiakastili on määritettävä.                                                                                                                                                                                                                                                                                                  |
| Toimitusosoite   | Osoite, joka on palautettu nimike                 | Käytetään oletusarvon mukaan yrityksen osoite. Otsikon on valittu tietty varasto, jos toimitusosoite muutetaan varasto toimitusosoite. Voit muuttaa tätä osoitetta **palauttaa tiedot** sivulla.                                                                                                  |
| Toimipisteen ja varaston     | Sivuston tai varaston, joka vastaanottaa palautetun tuotteen | Palautustilauksen toimitusosoite määritetään sivuston tai varastoinnin toimitusosoitteen perusteella.                                                                                                                                                                                                                                 |
| Palautusnumero         | Tunnus, joka liittyy palautustilaukseen              | Palautustilauksen käsittely koko vaihtoehtoisella käytetään palautusnumero. RMA-numero, joka määritetään perustuu RMA numerosarja on määritetty **Myyntireskontran parametrit** sivulla.                                                                                                                              |
| Määräaika           | Viimeinen päivämäärä, jolloin nimike voidaan palauttaa               | Oletusarvo lasketaan nykyinen päivämäärä plus voimassaoloajan. Esimerkiksi palauttaa on kelvollinen vain 90 päivää palautustilauksen luonnin, jolloin palautustilaus luotiin toukokuussa 1, jos-kentän arvo on **30-heinäkuun**. Voimassaoloaika määritetään **Myyntireskontran parametrit** sivulla. |
| Palautuksen syykoodi | Asiakkaan syy nimikkeen tuotteen          | Syykoodi on valittu käyttäjän määrittämä syykoodien luettelo. Kenttää voi päivittää milloin tahansa.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Luoda palautustilauksen rivit

Jälkeen palaa otsikon, voit luoda palautusrivit jollakin seuraavista tavoista:

-   Anna kohteen tiedot ja muut tiedot saat palautuksen jokaisella rivillä määrä manuaalisesti.
-   Luo palautuksen rivi käyttämällä **Etsi myyntitilaus** funktio. Suosittelemme, että käytät tätä toimintoa, kun luot palautustilausta. **Etsi myyntitilaus** toteaa palautusrivi laskutettu myyntitilausrivi viittaus funktion ja rivi hakee tietoja, esimerkiksi nimikenumero, määrä, hinta, alennus ja kustannusarvot myyntiriviltä. Viittaus auttaa takaamaan, että tuote palautetaan yritykselle, kun se on arvostettuna yksikkö samoin kustannuksin, että se oli myydä. Viittaus tarkistaa, jotka palauttavat tilaukset eivät ole luotu, määrä, joka ylittää määrän, joka on myyty laskun.

**Huomautus:** korjaukset tai myyntiä, palautukset käsitellään palautusrivit, joiden viittaa myyntitilaukseen. Lisätietoja on kohdassa "Post-kirjanpidon" jäljempänä tässä ohjeaiheessa olevassa.

### <a name="charges"></a>Kulut

Maksut voidaan lisätä palautustilaukseen kautta yksi tai useampi seuraavista toimista:

-   Voit lisätä kulut manuaalisesti palautustilauksen otsikkotiedoissa tai palautustilauksen riville.
-   Maksuja voidaan automaattisesti lisätä palautustilauksen otsikkotiedoissa palautuksen syykoodin funktiona.
-   Maksuja voidaan automaattisesti lisätä palautustilausrivi rivin käsittelykoodi perusteella.

Kulujen jälkeen Palautuksen syykoodi lisätään automaattisesti tai määritetään rivin käsittelykoodi. Jos myöhemmin muuttaa syykoodin, ei voi poistaa aiemmin Kulu-tapahtuman, mutta saatetaan lisätä uuden tapahtuman kulun, mukaan uusi syykoodi. Kun lisäät palautustilauksen rivit kulut, kulut, jotka lasketaan prosenttiosuutena rivin tai tilauksen arvo tulee negatiivinen, kun rivi tai rivin tilaus on negatiivinen, ellei prosenttiosuus on myös negatiivinen. Varausta, jolla on negatiivinen arvo edustaa hyvityksen asiakkaalle.

### <a name="return-reason-codes"></a>Palautuksen syykoodit

Soveltamalla palautusten syykoodit, voit auttaa parantamaan palaa kuviot helpompi analysoida. Syykoodit on tietoja siitä, miksi asiakas haluaa palauttaa nimikkeitä. Joillakin organisaatioilla on useita syykoodeja. Nämä organisaation ryhmittää syykoodit syykoodiryhmät saada yleiskuvan selkeyttämiseksi ja kertynyt raportointia varten.

### <a name="disposition-codes-and-disposition-actions"></a>Käsittelykoodit ja poistotapahtumia

Palautustilauksen käsittely tärkeä vaihe on Saapumisrekisteröinti osana käsittelykoodi palautustilauksen riviin määrittelyä. Käsittelykoodin määrittää seuraavat tiedot:

-   **Taloudellisia vaikutuksia** – asiakkaalle hyvitetään palautetuille nimikkeille ja kulut lisätään palautustilauksen riville?
-   **Palautetun nimikkeen käsittelyn** – kohteen voidaan lisätä varastoon olisi sen menevän hukkaan tai se palautetaan asiakkaalle?
-   **Palautetun nimikkeen Logistiikka** – korvaavan nimikkeen myönnettävä asiakkaalle?

Lisäksi määritetään kuinka palautetut tavarat on myyty, käsittelykoodien voi aiheuttaa kuluja, jotka kohdistetaan palautusrivi. Ne voidaan myös ryhmitellä palauttaa tilastollista analyysiä varten. Käsittelykoodit määritellään osa palautustilaukset. Kuitenkin jokainen käsittelykoodi on viitattava jonkin valmiin poistamisen toimista. Seuraavassa taulukossa on lueteltu sisäiset käsittelykoodit ja niiden toiminnot. **Tärkeää:** Jos kohdetta ei voi palauttaa, mutta silti hyvitetään asiakkaalle, **vain kredit-** käsittelykoodi niin palautusrivi.

<table>
<thead>
<tr class="header">
<th>Käsittelykoodi</th>
<th>Rahoitusvaikutusten</th>
<th>Logistiikan vaikutukset</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vain hyvitys</td>
<td><ul>
<li>Asiakkaalle hyvitetään myyntihinta vähennettynä mitään maksuja ja veroja.</li>
<li>Tappio nimike kirjataan kirjanpitoon.</li>
</ul></td>
<td>Sitä ei tule palauttaa. Tämä poistotehtävänä käytetään seuraavissa tapauksissa:
<ul>
<li>On riittävä luottamus osapuolten kesken.</li>
<li>Palauttaa viallisen nimikkeen kustannus on kohtuuttoman kallis.</li>
<li>Kohteet voi poistaa takaisin varastoon. Koska muita ehtoja ei tarvita fyysistä palauttamista.</li>
</ul></td>
</tr>
<tr class="even">
<td>Hyvitys</td>
<td><ul>
<li>Asiakkaalle hyvitetään myyntihinta vähennettynä mitään maksuja ja veroja.</li>
<li>Palautetun nimikkeen kustannuksen arvo nousi varastoarvon.</li>
</ul></td>
<td>Kohde palautetaan ja lisätään takaisin varastoon.</td>
</tr>
<tr class="odd">
<td>Korvaus ja hyvitys</td>
<td><ul>
<li>Asiakkaalle hyvitetään myyntihinta vähennettynä mitään maksuja ja veroja.</li>
<li>Palautetun nimikkeen kustannuksen arvo nousi varastoarvon.</li>
<li>Korvaa erillisen myyntitilaus luodaan ja käsitellään erikseen.</li>
</ul></td>
<td>Kohde palautetaan ja lisätään takaisin varastoon.</td>
</tr>
<tr class="even">
<td>Korvaus ja hävitys</td>
<td><ul>
<li>Asiakkaalle hyvitetään myyntihinta vähennettynä mitään maksuja ja veroja.</li>
<li>Tappio nimike kirjataan kirjanpitoon.</li>
<li>Korvaa erillisen myyntitilaus luodaan ja käsitellään erikseen.</li>
</ul></td>
<td>Kohde palautetaan ja hukkaan.</td>
</tr>
<tr class="odd">
<td>Palautus asiakkaalle</td>
<td>Ei mitään, paitsi mitään maksuja ja veroja.</td>
<td>Kohde palautetaan, mutta tarkastuksen jälkeen lähetetään takaisin asiakkaalle. Tämä poistotehtävänä voidaan kohteen vioittunut tahallisesti tai takuu on mitätöity.</td>
</tr>
<tr class="even">
<td>Hävikki</td>
<td><ul>
<li>Asiakkaalle hyvitetään myyntihinta vähennettynä mitään maksuja ja veroja.</li>
<li>Tappio nimike kirjataan kirjanpitoon.</li>
</ul></td>
<td>Kohde palautti tai Romutettu.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Tarkastusta varten varastoon saapumisen
Ennen kuin voit vastaanottaa palautetut nimikkeet varastoon fyysisesti kirjaamalla pakkausluettelon, nimikkeet täytyy mennä Saapumisrekisteröinti ja valinnaisen tarkastuksen kautta. Seuraavassa kuvassa on yleiskuvaus saapumisen yhteydessä. Tapoja, joilla kuvataan kunkin vaiheen, joka näkyy kuvassa.  

[![Saapumisprosessi](./media/salesreturn03.png)](./media/salesreturn03.png)  

On useita muita muunnoksia, jotka eivät ole tämän ohjeaiheen piiriin. Tässä muutamia näihin muutoksiin:

-   Älä käytä **Saapumisten yhteenveto** -luettelosta Luo saapumiskirjauskansio. Sen sijaan manuaalisesti luo saapumisen kirjauskansio. Palauttaa Tilaukset on **myynti** viitteenä.
-   Jos käytät varastonhallintaa, Luo kuormalavakuljetukset. Palautusrivi tilan olla **saapunut** aikana kuormalavakuljetus.
-   Rekisteröidä suoraan ostopalautuksen tilausrivin palautetun nimikkeen saapumisen avulla **rekisteröinti** funktio.

Saapumisen aikana palauttaa on integroitu varaston saapuvien yleinen prosessi. Saapumisprosessi tukee myös perustamista varten palautetut nimikkeet, jotka on suoritettava erillisessä tarkastus karanteenitilaukset.

### <a name="identify-products-in-the-arrival-overview-list"></a>Määritä tuotteiden saapumista yleistä luettelosta

**Saapumisten yhteenveto** sivulla on lueteltu kaikki suunnitellut saapuvat saapuneiden. **Huomautus:** saapuvat palautustilauksista on käsiteltävä erikseen muita tapahtumatyyppejä saapumista. Kun olet tunnistanut saapuva paketti **Saapumisten yhteenveto** -sivulla (esimerkiksi käyttämällä RMA saateasiakirja), toimintoruudun **Aloita Saapuminen** luoda ja alustaa, joka saapumisen vastaa saapumisen kirjauskansioon.

### <a name="edit-the-arrival-journal"></a>Muokkaa saapumisen kirjauskansio

Määrittämällä **Karanteeni hallinta** asetukseksi **Kyllä**, voit luoda karanteenitilauksen palautusrivi varten. Jos rivi on lähetetty karanteeniin tarkastettavaksi, et voi määrittää käsittelykoodi. **Huomautus:** Jos **Karanteeni hallinta** asetuksella **Kyllä** nimikkeen varastomalliryhmässä **Karanteeni hallinta** asetus **kirjauskansiorivit** sivun saapumisen kirjauskansion riville merkitään, eikä sitä voi muuttaa. Jos rivi lähetetään karanteeniin, sopiva Karanteenivarasto on määritettävä. Jos saapumisen riviä ei ole lähetetty tarkastettavaksi, varastoon saapumisen virkailija on määrittää käsittelykoodin suoraan saapumisen kirjauskansiorivin ja kirjaa saapumisen kirjauskansio. Jos samaa käsittelykoodia ei liitetä palautusrivi koko määrä tai jos rivin koko määrä ei ole vielä vastaanotettu, rivi on jaettava. Kun jaat, saapumisen kirjauskansiorivin, voit myös jakaa palautusrivi (**SalesLine**) ja luo uuden erän tunnus. Voit jakaa rivin vähentämällä saapumisen kirjauskansiorivin määrä. Kun kirjauskansio kirjataan, palauta uusi rivi luodaan, tila on **odotettu** jäljellä olevan määrän osalta. Voit myös jakaa rivin valitsemalla **toimintojen**&gt;**Jaa**.

### <a name="process-the-quarantine-order"></a>Prosessin karanteenitilaus

Palautetut tuotteet lähetetään karanteenivarastossa tarkastusta varten, jos muut käsittely on valmis karanteenitilaus. Yksi karanteenitilaus luodaan saapumisen kullekin riville, joka lähetetään karanteeniin. Käsittelykoodin ilmaisee tuloksen tarkastuksen prosessi. Voit jakaa karanteenitilaus, aivan kuten voit jakaa saapumisen kirjauskansio. Karanteenitilaus on jaettava, jos aiheuttaa palautusrivin vastaavan jaon. Täytä karanteenitilauksen käsittelykoodin kirjoitetut käyttämällä joko **pään** funktio tai **valmiiksi** funktio. Jos valitset **valmiiksi**, uudet toimijat on luotu määritettyyn varastoon. Voit käsitellä tämän saapumisen jälkeen avulla **Saapumisten yhteenveto** sivulla. Jos saapumisen peräisin karanteenitilaus, et voi muuttaa käsittelykoodi, joka on määritelty tarkastuksen aikana. Jos avulla tekemään karanteenitilausten **pään** funktion, erä on automaattisesti rekisteröity. Joskus kohde saattaa lähetetään takaisin karanteenista lähetys- ja vastaanotto-osastolle. Esimerkiksi karanteenitarkastaja ehkä tiedä, mihin nimike varastoidaan varasto. Tässä tapauksessa vastaavat pakkausluettelo on päivitettävä oikein rekisteröityä ja käsittelykoodi, joka on määritetty Karanteeni vuoksi. Asiakkaalle voidaan lähettää kuittauksen vastaanottamisesta palautusrivi rekisteröitäessä. **Palautuksen kuittaus** raportti muistuttaa asiakirjan palautustilaukseen. **Palautuksen kuittaus** raportti ei ole kirjattu tai muuten rekisteröity järjestelmään, ja se ei ole pakollinen vaihe, palautustilaus.

## <a name="replace-a-product"></a>Korvaa tuotteen
Hallintaan tuotteen korvaamisen kahdella tavalla:

-   **Etukäteiskustannukset korvaavan** – korvaa tuotteen ennen palautettu tuote on vastaanotettu asiakkaalta.
-   **Käsittelykoodi korvaaminen** – automaattisesti luoda korvaava uusi tilausrivi.

### <a name="up-front-replacement"></a>Ennakolta tehtävä korvaus

-Etukäteiskustannukset korvaavan korvaavaa nimikettä voidaan toimittaa asiakkaalle ennen kuin kohde palautetaan. Tämä menetelmä on hyödyllinen, jos kohde on esimerkiksi koneen osaa ei voi poistaa, ellei ole varaosa on saatavilla sen tapahtua, tai jos haluat asiakkaasi on korvaava tuote mahdollisimman pian. Etukäteiskustannukset korvaava tilaus on riippumaton myyntitilauksen. Otsikkotiedot alustetaan asiakkaan ja rivin tiedot alustetaan palautustilauksesta. Voit muokata, käsitellä ja poistaa korvaavan tilauksen palautustilauksen erikseen. Kun poistat korvaava tilaus, näyttöön tulee sanoma, että tilaus on luotu korvaava tilaus. Seuraavassa kuvassa näkyy etukäteiskustannukset korvaavan prosessin.  

[![Etukäteiskustannukset korvaava prosessi](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)  

Palautustilaus on viittaus korvaavaan tilaukseen. Etukäteiskustannukset korvaava tilaus on luotu palautustilaus ennen kuin viallinen nimike palautetaan, jos et voi valita käsittelykoodien korvaamiseen kun viallinen nimike on palautettu.

### <a name="replacement-by-disposition-code"></a>Korvaaminen käsittelykoodi

Voit toimittaa asiakkaalle korvaavaa nimikettä, ja käyttää **korvaus ja hävitys** tai **korvaus ja hyvitys** poistotehtävänä palautustilauksessa, käytä prosessi, joka näkyy seuraavassa kuvassa.  

[![Korvaavan prosessin käytettynä käsittelykoodi](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)  

Korvaava nimike toimitetaan riippumaton myyntitilauksen korvaavan myyntitilauksen avulla. Tämä myyntitilaus luodaan, kun palautustilauksen pakkausluettelo luodaan. Tilausotsikon tiedot asiakkaalta, johon viitataan käyttää palautustilauksen otsikkotiedoissa. Rivin tiedot on kerätty tiedot, jotka on syötetty **korvaava nimike** sivulla. **Korvaava nimike** sivun täytyy täyttää rivit, joiden käsittelyn toiminnot, jotka alkavat sanalla "Korvaa". Kuitenkin määrä eikä korvaavaa nimikettä henkilöllisyys on vahvistettu tai rajoitettu. Tämä mahdollistaa mutta tapauksissa, joissa asiakas haluaa saman nimikkeen eri kokoonpano tai koko ja myös tapauksissa joissa asiakkaista haluaa kokonaan eri nimike. Samanlainen nimike syötetään- **korvaava nimike** sivulla. Voit valita toinen kohde, kuitenkin sillä edellytyksellä, että funktio on määritetty. **Huomautus:** voit muokata ja poistaa korvaavan myyntitilauksen luonnin jälkeen.

## <a name="generate-a-packing-slip"></a>Luo pakkausluettelo
Ennen kuin palautetut nimikkeet voidaan vastaanottaa varastoon, jotka kuuluvat nimikkeet tilauksen pakkausluettelo on päivitettävä. Samalla tavalla kuin laskun päivitysprosessi on Kirjanpitotapahtuman päivitys, pakkausluettelon päivitys prosessi on Varastotietueen fyysinen päivitys. Toisin sanoen tämä prosessi vahvistaa muutokset varastoon. Kun kyseessä vaiheet, jotka on määritetty poistamisen toimenpide toteutetaan aikana pakkausluettelon päivityksen. Kun pakkausluettelo, seuraavat tapahtumat toteutuvat:

-   Varasto-standardi prosessi käytetään suorittamaan fyysisen vastaanoton. Kirjanpidon kirjaukset luodaan, jos varaston malli ryhmän (**Kirjaa varastotilanne**) ja Accounts receivable parameters (**Kirjaa pakkausluettelo kirjanpitoon**) on määritetty oikein.
-   Jotka on merkitty poistotehtävänä, joka sisältää sanan "romu-nimikkeet on merkitty hävikiksi ja varastotappio kirjataan kirjanpitoon.
-   Kohteet, jotka on merkitty **asiakas palaa** poistotehtävänä on vastaanotettu ja toimitettu asiakkaalle. Nämä kohteet ole mitään nettovaikutusta varaston.
-   Korvaavan myyntitilauksen luomisen yhteydessä. Tälle myyntitilaukselle perustuu tietoihin **korvaava nimike** sivulla.

Voit luoda vain rivit, joiden tila on palautettu, pakkausluettelon **rekisteröity**, ja vain palautusrivi koko määrä. Jos on useita palautustilauksen rivit **rekisteröity** tila, voit luoda poistamalla siitä rivit pakkausluettelon rivin osajoukko **Kirjaa pakkausluettelo** sivun. Osittainen palauttaa on määritetty palautustilauksen rivit eivät palautustilauksen toimitusten osalta. Siis jos koko määrä, joka ilmaistaan palautustilauksen rivillä tulee, mutta mitään vastaanottaa palautustilauksen muut rivit, toimitus ei ole osittainen toimitus. Jos ostopalautustilauksen riville edellyttää 10 yksikön, joka palautetaan, mutta saat vain neljä yksikköä, toimitus on osatoimitus. Jos oletettu palautetut nimikkeet ovat Saapuneet, voit kesannoitujen toimitus ja odottaa loput saapuvat määrän. Vaihtoehtoisesti voit rekisteröidä ja palautustilausrivin. Osana prosessia pakkausluetteloiden kirjausta varten voit liittää tilausrivit pakkausluettelon viitenumero asiakkaan toimittamista asiakirjoista. Tämä kytkentä on valinnainen ja on tarkoitettu vain tiedoksi. Se ei luo tapahtumiin liittyviä päivityksiä. Yleensä voit ohittaa pakkausluettelon prosessin viivästyä ja siirtyä suoraan laskutukseen. Vaiheet, jotka olet tehnyt pakkausluettelon luomisen yhteydessä on tehty tässä tapauksessa laskutuksen aikana.

## <a name="generate-an-invoice"></a>Luo lasku
Vaikka **palautustilauksen** sivu sisältää tietoja ja toimintoja, joita tarvitaan käsitellä logistiset erityisnäkökohdat palautustilauksen, on käytettävä **myynti** sivun laskutuskauden loppuun. Organisaatio voi sitten laskun palautustilaukset ja myyntitilauksen on päätetty samaan aikaan ja sama henkilö voi suorittaa tarvittaessa laskutusprosessiin. Voit tarkastella palautustilaus **myynti** -sivulla linkkiä, avaa siihen liittyvä myyntitilaus myyntitilauksen numero. Myös löydät palautustilauksen **kaikki myyntitilaukset** sivulla. Palauttaa tilaukset ovat myyntitilaukset, joiden tilauksen tyyppi **tilaus palautetaan**.

### <a name="credit-correction"></a>Hyvityksen oikaisu

Osana laskutusprosessiin Varmista, että muita kuluja ovat oikein. Aiheuttaa kirjanpitokirjaukset tulla korjauksia (Storno), harkitse **luotto-korjaus** asetus **muita** -välilehdessä **lasku** sivulle silloin, kun kirjaat laskun tai hyvityslaskun. **Huomautus:** oletusarvon mukaan **luotto-korjaus** vaihtoehto on aktiivinen, jos **korjaus hyvityslaskulla** asetus **Myyntireskontran parametrit** sivu on otettu käyttöön. Suosittelemme kuitenkin, että voit palauttaa ei kirjaa Storno kanssa.

## <a name="create-intercompany-return-orders"></a>Konserniyritysten väliset palautustilaukset luodaan Luo
Palautustilausten voi suorittaa kahdella organisaatioon kuuluvien yritysten välillä. Tuetaan seuraavissa tilanteissa:

-   Yksinkertainen konserniyritysten välisiä palautuksia, jotka osallistuvat konserniyritysten välisen suhteen kahden yrityksen välinen
-   Konsernin sisäisen ketjun, joka määritetään, kun asiakkaan palautustilaus on luotu myyntiyhtiön
-   Konsernin sisäisen ketjun, joka määritetään, kun toimittajalle ostopalautustilaus luodaan ostava yritys-
-   Toimitus: Suoratoimitus palauttaa ulkoiselle asiakkaalle ja kaksi yritystä, jotka osallistuvat konserniyritysten välisen suhteen

### <a name="setup"></a>Luo perustiedot

Seuraavassa kuvassa vähimmäisasetuksista, tarvitaan kaksi yritystä osallistumaan konsernin sisäisen suhteen ja hyödyntää konserniyritysten välisessä kaupassa.  

[![Minimum setup](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)  

Seuraavassa tilanteessa CompBuy on ostava yritys, ja CompSell on myyvä yritys. Yleensä myyvä yritys toimittaa tavaroiden ostava yritys tai, Suoratoimitus toimitus tilanteissa suoraan loppuasiakkaalle. -CompBuy toimittajan Konsernin\_CompSell määritellään yrityksen sisäinen päätepiste, joka liittyy yrityksen CompSell. Samaan aikaan CompSell, asiakkaan Konsernin\_CompBuy määritellään yrityksen sisäinen päätepiste, joka liittyy yrityksen CompBuy. Molempien yritysten on määritettävä tarvittavat toimenpiteet käytännön tiedot ja arvojen määritykset. Konsernin sisäisen palautustilauksen, joka on myös konsernin sisäiseen myyntitilaukseen, luodaan suoratoimitus toimitus-skenaariossa myyvä yritys. Konsernin sisäisen palautustilauksen palautusnumero voi keräillä numerosarjasta RMA-CompSell, tai se voidaan kopioida RMA-numero alkuperäisestä palautustilauksesta CompBuy on liitetty. RMA-numeron asetuksia **PurchaseRequisition** selvittää nämä toiminnot CompBuy käytännön toimia. Palautusnumero synkronoidaan, jos aiot pitäisi lieventää riskiä luku ristiriidassa Jos kaksi yritykset käyttävät samaa numerojärjestystä.

### <a name="simple-intercompany-returns"></a>Yksinkertainen konserniyritysten palautusten

Tämä tilanne liittyy saman organisaation kaksi yritystä kuvassa esitetyllä tavalla.  

[![Konsernin palautus yksinkertaiset](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)  

Tilaus-toimitusketjun voi muodostaa, kun toimittajalle ostopalautustilaus luodaan ostava yritys- tai asiakkaan palautustilaus luodaan myyvä yritys. Työvaiheiden 365 Dynamics luo vastaavan huoltotilauksen toisessa yrityksessä ja varmistaa, että ylä- ja riviä tietoja toimittajan palauttaa kuvastaa tilauksen asetukset asiakkaan palautustilaus. Palautustilaus on sijoittautunut voit sisällyttää tai jättää pois viittaus (**Etsi myyntitilaus**) aiemmin asiakkaan laskuun. Pakkausluetteloista ja laskuista kahden tilauksista voidaan käsitellä erikseen. Esimerkiksi sinun ei tarvitse luoda toimittajan palautustilauksen pakkausluettelo ennen pakkausluettelon asiakkaan palautustilaus luo.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Toimitus: Suoratoimitus palauttaa osapuolten kolmen kesken

Tässä tilanteessa voidaan vahvistaa, jos edellisen myynnistä **suorat toimitukset** tyyppi on valmis, ja jos laskua vastaan asiakas on yritys, joka on vuorovaikutuksessa asiakkaan kanssa. Seuraavassa kuvassa yrityksen CompBuy on aiemmin myyty ja laskutettu asiakas Extern tuotteiden. Tuotteet on lastattu suoraan yritykseltä CompSell asiakkaan konsernin välisen tilausketjun kautta.  

[![Toimitus: Suoratoimitus palauttaa kolme osapuolten välillä](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)  

Ulkoinen asiakas haluaa palauttaa tuotteen, jos asiakkaan yrityksen CompBuy on luotu palautustilaus (RMA02). Vahvistaa konsernin sisäisessä ketjussa, palautustilaus on merkittävä suoratoimitusta varten. Kun käytät **Etsi myyntitilaus** asiakkaan laskuun palauttaa, valitse funktio on perustettu konsernin sisäistä tilausketjua, joka sisältää seuraavat asiakirjat:

-   **Alkuperäinen palautustilaus:** RMA02 (yrityksen CompBuy)
-   **Ostotilaus:** PO02 (yrityksen CompBuy)
-   **Konsernin sisäinen palautustilaus:** RMA\_00032 (yrityksen CompSell)

Suoratoimituksen konsernin sisäisessä ketjussa luonnin jälkeen kaikki fyysisen käsittelyn ja palauttaa käsittely voi esiintyä konsernin sisäisen palautustilauksen, RMA yhteydessä\_00032 yrityksen CompSell. Yrityksen CompBuy ei voi vastaanottaa tuotteet. Käsittelykoodi määritetään konsernin palautustilauksen, kun tiedot synkronoidaan, jotta asianmukainen Laskutus alkuperäisen alkuperäiseen palautustilaukseen.

## <a name="post-to-the-ledger"></a>Kirjaa kirjanpitoon
Kirjanpidon kirjaukset, jotka on luotu palautustilaus laskutetaan vaikuttaa joitakin tärkeitä asetuksia ja parametreja:

-   **Palautuksen kustannushinta** – osalta varasto mallit, muut kuin **standardikustannusten**, **Palautuksen kustannushinta** parametri määrittää nimikkeen kustannuksen, kun se on hyväksytty takaisin varastoon tai Romutettu. Oikean varaston arvostuksen laskemiseen, on tärkeää, että **Palautuksen kustannushinta** parametria oikein. Jos käytät **Etsi myyntitilaus** -funktio Luo palautustilaus-rivi, joka viittaa asiakkaan laskun, **Palautuksen kustannushinta** arvo on yhtä kuin kustannushinta, joka myydään osa. Muussa tapauksessa hinta-arvo on peräisin nimikkeiden asetukset tai voidaan syöttää manuaalisesti.
-   **Luotto korjaus/Storno** – **luotto-korjaus** -parametrin **lasku** sivulla määrittää, tulisiko kirjaukset olla tallennettu (DR/CR) Positiiviset tapahtumat tai korjaaminen, negatiivinen tiedot.

Seuraavat esimerkit, palautuksen kustannushinnan esitetään **laskun hinta**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Esimerkki 1: Palautustilauksen ei viitata myyntilasku

Palautustilausta ei viitata asiakkaan laskuun. Palautetun nimikkeen hyvitetään. **Luotto-korjaus** parametri ei ole valittuna, kun palautustilauksen, laskun tai hyvityslaskun.  

[![Palautustilausta ei viittaa asiakkaan invoic](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)  

**Huomautus:** master hinta käytetty on oletusarvo **Palautuksen kustannushinta** parametri. Oletus hinnan kustannushinta eroaa, kun varasto-otto. Antaakseen siis 3 menetys syntynyt. Lisäksi palautustilauksen ei sisälly alennuksen, joka on annettu asiakkaan myyntitilauksen. Tämän vuoksi ilmenee liiallinen luotto.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Esimerkki 2: Luotto korjaus valitaan palautustilaukselle

Esimerkki 2 on sama kuin Esimerkki 1, mutta **luotto-korjaus** parametri on valittuna, kun palautustilauksen lasku luodaan.  

[![Palautustilauksen, jossa luotto korjaus on valittuna](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)  

**Huomautus:** negatiiviset oikaisut syötetään kirjauskansioon kirjaukset.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Esimerkki 3: Palautustilauksen riville luodaan käyttämällä Etsi myyntitilaus-funktio

Tässä esimerkissä palautustilauksen riville luodaan käyttämällä **Etsi myyntitilaus** funktio. **Luotto-korjaus** parametri ei ole valittuna, kun lasku luodaan.  

[![Palautustilauksen riviin, joka on luotu käyttämällä Etsi myyntitilaus](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)  

**Huomautus:****alennus** ja **Palautuksen kustannushinta** on määritetty oikein. Tämän vuoksi ilmenee tarkasti asiakkaan laskuun.


