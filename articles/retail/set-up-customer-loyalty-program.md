---
title: Kanta-asiakkuuden yleiskatsaus
description: "Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Retailiin kanta-asiakastoimintoja ja niitä vastaavia asetusohjeita, jotta jälleenmyyjä pääsee aloittamaan kanta-asiakasohjelmansa."
author: scott-tucker
manager: AnnBe
ms.date: 10/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailLoyaltyPrograms, RetailPriceDiscGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16201
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 09d4e46694e89b648981352f64da4a43ab1522e1
ms.contentlocale: fi-fi
ms.lasthandoff: 01/04/2019

---

# <a name="loyalty-overview"></a>Kanta-asiakkuuden yleiskatsaus

[!include [banner](includes/banner.md)]

Kanta-asiakasohjelmat voivat lisätä asiakasuskollisuutta palkitsemalla asiakkaita, kun ovat tekemisissä jälleenmyyjän brändin kanssa. Microsoft Dynamics 365 for Retailissa voit määrittää yksinkertaisia tai monimutkaisia kanta-asiakasohjelmia yritysten välille missä tahansa vähittäismyyntikanavassa. Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Retailiin kanta-asiakastoimintoja ja niitä vastaavia asetusohjeita, jotta jälleenmyyjä pääsee aloittamaan kanta-asiakasohjelmansa.

Voit määrittää kanta-asiakasohjelman käyttämällä seuraavia vaihtoehtoja.

- Määritä useita palkintoja, joita tarjotaan kanta-asiakasohjelmissa, ja seuraa niihin osallistumista.
- Määritä kanta-asiakasohjelmia, jotka edustavat erilaisia tarjoamiasi kannusteita. Voit sisällyttää kanta ohjelma tasot tarjotaksesi suurempi kannustepalkkiot ja edut asiakkaille, jotka ostavat usein tai käyttävät enemmän rahaa myymälöissäsi.
- Määritä ansaintasäännöt niiden aktiviteettien tunnistamiseksi, jotka asiakkaan on suoritettava palkintojen ansaitsemiseksi. Voit myös asettaa lunastussäännöt määrittämään, milloin ja miten asiakas voi lunastaa edut.
- Voit myöntää kanta-asiakaskortteja mille tahansa vähittäismyyntikanavalle, joka on osana kanta-asiakasohjelmiasi ja yhdistää kanta-asiakaskortteja yhteen tai useampaan kanta-asiakasohjelma, johon asiakas voi osallistua. Voit myös yhdistää asiakastietueen kanta-asiakaskorttiin, jotta asiakas voi kerätä kanta-asiakaspisteitä useilla korteilla sekä lunastaa ne.
- Oikaise kanta-asiakaskortit manuaalisesti tai siirrä kanta-asiakaspalkkioiden saldo kortilta toiselle asiakkaan palkitsemiseksi.

## <a name="setting-up-loyalty-programs"></a>Kanta-asiakasohjelmien määrittäminen

Kun otat kanta-asiakkuusominaisuuden käyttöön Dynamics 365 for Retailissa, sinun on määritettävä useita komponentteja. Seuraavassa kaaviossa on kuvattu kanta-asiakkuuskomponentit ja kuinka ne liittyvät toisiinsa.

![Kanta-asiakkuuden asetusprosessin työnkulku](./media/loyaltyprocess.gif "Kanta-asiakasosat ja niiden keskinäiset suhteet")

## <a name="loyalty-components"></a>Kanta-asiakkuuskomponentit

Seuraavassa taulukossa on kuvattu jokainen komponentti ja sen käyttöpaikka kanta-asiakkuuden määrityksessä.

| Komponentti                                        | kuvaus | Käyttökohde |
|--------------------------------------------------|-------------|-----------------|
| Määritä alennukset (edellytys)                  | Määritä alennukset, jotka tarjoat kanta-asiakkaille. Voit tarjota esimerkiksi 5 prosentin alennuksen kaikista asusteista. | Alennukset on lisättävä hintaryhmiin, jotta ne voidaan sisällyttää kanta-asiakasohjelmaan. Hintaryhmät liitetään kanta-asiakasohjelmiin ja kanta-asiakastasoihin. |
| Määritä hinta- ja alennusryhmät (edellytys)               | Hintaryhmiä voidaan käyttää vähittäismyyntituotteiden hintojen ja alennusten luomiseen ja hallintaan. Määritä hintaryhmät, jotka sisältävät alennukset, jotka koskevat kanta-asiakasohjelmaa. | Hintaryhmät liitetään kanta-asiakasohjelmiisi ja kanta-asiakasohjelman tasoihin. |
| Määritä kanavat (edellytys)                   | Vähittäismyyntikanavat ovat myymälöitä, jotka osallistuvat kanta-asiakasohjelmiisi, kuten vähittäismyymälöitä, verkkokauppoja tai puhelinkeskuksia. Sinun on asetettava vähittäismyynnin kanavat ennen kuin määrität niihin kanta-asiakasohjelmia. | Määrität vähittäismyynnin kanavat kanta-asiakasohjelmaan, jos vähittäismyynnin kanava osallistuu kanta-asiakasohjelmaan. |
| Määritä kanta-asiakkaan maksutapa (edellytys) | Sinun on määritettävä maksutapa ennen kuin kanta-asiakaskorttia voidaan käyttää kassakoneessa ja kanta-asiakaspisteitä voidaan lunastaa osana kanta-asiakkuusohjelmaa. Sinun on myös lisättävä asiakkaille kanta-asiakkaan maksutapa vähittäismyyntikanavaan, jotta asiakkaat voivat lunastaa tuotteita kanta-asiakkuuspisteillään. | Määritä kanta-asiakkuustyypin maksutapa ja liitä sitten kanta-asiakkuuden maksutapa vähittäismyynnin kanaviin niiden osalta, jotka osallistuvat kanta-asiakasohjelmaan. |
| Määritä päivämäärävälit                            | Päivämäärävälit tarjoavat joustavan tavan kanta-asiakkuustasoja koskevan ajanjakson asettamiseksi. Päivämäärävälien avulla voit määrittää, kuinka kauan asiakas pysyy tietyllä tasolla tai kuinka monta kertaa tietty tehtävä pitää suorittaa, jotta asiakas saavuttaa tietyn tason. | Päivämäärävälit ovat voimassa vain, jos käytät tasoja kanta-asiakasohjelmissasi. Valitset päivämääräväli, joka koskee ohjelmatasoihin ja päivämäärävälin, joka koskee ohjelmatason sääntöjä. |
| Määritä palkintopisteet                             | Palkintopisteet ovat palkintotyyppejä, joita voit tarjota asiakkaillesi. Palkintopisteet voivat olla takaisin ostettavia tai ei-hyvitettäviä. Lunastettavia palkintopisteitä voidaan vaihtaa tuotteisiin. Ei lunastettavia palkkiopisteitä käytetään seurantaan tai asiakkaan siirtämiseksi seuraavalle tasolle kanta-asiakasohjelmassa. | Palkintopisteisiin viitataan tason säännöissä ja niitä käytetään oikeuttamaan tietyn asiakkaan taso. Kanta-asiakkuuspisteisiin viitataan myös kanta-asiakasmallin ansainta- ja lunastussäännöissä. Ansaitsemissäännöissä määrität palkkiot, jotka asiakas voi ansaita tietyst' tehtävästä. Lunastussäännöissä voit määrittää palkinnot, jotka asiakas voi lunastaa. |
| Kanta-asiakkuusohjelmien asetukset                          | Kanta-asiakasohjelmat ovat kanta-asiakkuuden ydinyksikkö. Jokaiseen kanta-asiakasohjelmaan voidaan määrittää myös kanta-asiakkuustasoja. Alennukset ja hintaryhmät määritetään kanta-asiakasohjelmiin joko ohjelman tasolla tai kanta-asiakkuustasolla. | Luot kanta-asiakkuusmalleja kanta-asiakasohjelmillesi. Kanta-asiakaskortit liitetään kanta-asiakasohjelmiin ja kanta-asiakaskortit voidaan määrittää asiakkaalle. Kanta-asiakasohjelmat osallistuvat kanta-asiakkuusohjelmiin, jotka liittyvät kanta-asiakkuusmalleihin. Kuka tahansa kanta-asiakaskortin omistava asiakas voit osallistua kanta-asiakasohjelmiin, jotka on määritetty kortille. |
| Määritä anta-asiakkuustasot ja tason säännöt              | Kanta-asiakastasot ovat valinnaisia tasoja, jotka voit määrittää kanta-asiakasohjelmille. Voit määrittää perusalennukset ja -edut kaikille asiakkaille, jotka osallistuvat kanta-asiakasohjelmaan, ja määrittää muita alennuksia ja etuja asiakkaille, jotka saavuttavat ohjelmassa eri tasoja. Voit määrittää jokaiselle kanta-asiakastasolle säännöt, jotka oikeuttavat asiakkaan kuhunkin tasoon. Voit myös määrittää, kuinka kauan asiakas voi olla saavuttamallaan tasolla. | Kanta-asiakkuuden tasot ja kanta-asiakkuustason säännöt määritetään kanta-asiakasohjelmissa. Jos et määritä mitään kanta-asiakkuustasoja, kaikki asiakkaat, jotka osallistuvat kanta-asiakasohjelmaan, ovat oikeutettuja alennuksiin, jotka määritetään kanta-asiakasohjelman hintaryhmässä. Kanta-asiakastasoa määrittäessäsi voit määrittää ansainta- ja lunastussäännöt kanta-asiakkuusmallille kanta-asiakasmallissa. |
| Kanta-asiakkuusmallien asetukset                           | Kanta-asiakkuusmallit määrittävät valittua kanta-asiakkuusohjemaa koskevat ansainta- ja lunastussäännöt. Määrität vähittäismyynnin kanavat kanta-asiakkuusmalliin tunnistamaan, mitkä kanta-asiakasohjelma, ansaintasäännöt ja lunastussäännöt koskevat vähittäismyymälää. | Kanta-asiakkuusmalli liitetään kanta-asiakasohjelmaan ja vähittäismyyntikanaviin. Voit määrittää useita kanta-asiakkuusmalleja samaan kanta-asiakasohjelmaan ja voit liittää useita kanta-asiakkuusmalleja useisiin vähittäismyyntikanaviin. |
| Kanta-asiakaskorttien asetukset                             | Kanta-asiakaskortin omistava asiakas voi osallistua kanta-asiakasohjelmiin, jotka on määritetty kortille. Kanta-asiakaskortit voidaan antaa nimettömänä tai ne voidaan määrittää tietylle asiakkaalle. Voit tarkastella tietyn kortin kanta-asiakkuustapahtumia ja voit tarkastella kortille kertyneiden kanta-asiakkuuspisteiden yhteenvetoa. Voit lähettää kanta-asiakaskortit mistä tahansa vähittäismyynnin kanavasta. Voit myös manuaalisesti säätää kanta-asiakaskortin päivittämään asiakkaan eri tasolle, lisäämään kanta-asiakkuuspisteitä tai siirtämään kanta-asiakkuuspisteet kortilta toiselle. | Kanta-asiakasohjelmat liitetään kanta-asiakaskorttiin. |

## <a name="loyalty-processes"></a>Kanta-asiakkuusprosessit

Seuraavassa taulukossa on kuvaus prosesseista, jotka on suoritettava, jotta kanta-asiakkuusmääritykset ja -tiedot voidaan lähettää myymälöihin ja kanta-asiakkuustapahtumat voidaan hakea myymälöistä.

| Prosessin nimi                         | Kuvaus | Sivun nimi |
|--------------------------------------|-------------|-----------|
| 1050 (kanta-asiakkaan tiedot)           | Suorita tämä prosessi, jotta voit lähettää kanta-asiakkuustiedot Microsoft Dynamics 365 for Retailista vähittäismyymälöihin. Tämä prosessi kannattaa ajoittaa suoritettavaksi säännöllisesti, jotta kanta-asiakkuustiedot siirtyvät kaikkiin myymälöihin. | Jakeluaikataulu |
| Käsittele kanta-asiakkuusmallit              | Suorita prosessi, jolla määritetään kanta-asiakkuusmallit vähittäismyynnin kanavien kanssa, jotka liitetään kanta-asiakkuusmalleihin. Tämä prosessi voidaan ajoittaa suoritettavaksi eräprosessina. Tämä prosessi on suoritettava, jos muutat kanta-asiakkuuksien määritystietoja, kuten kanta-asiakkuusmalleja-, -ohjelmia tai -pisteitä. | Käsittele kanta-asiakkuusmallit |
| Käsittele kanta-asiakastapahtumia offline-tilassa | Suorita tämä prosessi, jotta voit päivittää kanta-asiakaskortteihin offline-tilassa käsitellyt tapahtumat. Tätä prosessia käytetään vain, jos **Ansaitse offline-tilassa** -valintaruutu on valittu **Vähittäismyynnin yhteiset parametrit** -sivulta siten, että etuja voi ansaita offline-tilassa. | Käsittele kanta-asiakastapahtumia offline-tilassa |
| Päivitä kanta-asiakaskorttitasot            | Suorita tämä prosessi, jotta voit arvioida asiakkaan ansaitsemat edut kanta-asiakasohjelman tasosääntöjen mukaisesti ja päivittää asiakkaan tasotilanteen. Tämä prosessi tarvitaan vain, jos muutat kanta-asiakasohjelmien tasosääntöjä ja haluat, että päivitetyt säännöt kohdistetaan takautuvasti jo myönnettyihin kanta-asiakaskortteihin. Tämä prosessi voidaan suorittaa eräprosessina tai yksittäisille korteille. | Päivitä kanta-asiakaskorttitasot |

## <a name="loyalty-enhancements"></a>Kanta-asiakasparannukset

Retailin lokakuun 2018 versiossa on uusi kanta-asiakastoiminto. Jokainen uusi parannus käsitellään myöhemmin.

- Edellisten versioiden kanta-asiakkuusmallissa jälleenmyyjät pystyivät luomaan erilaisia tasokohtaisia ansaitsemis- ja lunastussääntöjä, mikä mahdollisti palkkioiden erittelen eri tasojen asiakkaille. Jälleenmyyjät voivat nyt sisällyttää liitoksia ansaitsemis- ja lunastussääntöjen osaksi, jotta tietty asiakasryhmä voi kuulua aiemmin luotuihin tasoihin ja jotta heidän palkkionsa voivat olla erilaiset. Tämän vuoksi lisätasoja ei tarvitse luoda.
    
    > [!NOTE]
    > Kanta-asiakkuusmallin ansaitsemissäännöt ovat lisäsääntöjä. Jos esimerkiksi luot säännön, jolla kultatason jäsenelle annetaan 10 pistettä jokaista dollaria kohden, sekä säännön, jolla veteraaniliitoksen asiakkaalle annetaan 5 pistettä jokaista dollaria kohden, kultatason veteraani ansaitsisi tässä tapauksessa 15 pistettä jokaisesta dollarista, sillä tällainen asiakas hyväksytään kummallekin riville. Jos veteraaniasiakas ei kuitenkaan ole kultatason jäsen, hän ansaitsee 5 pistettä jokaista dollaria kohden. Voit toteuttaa muutokset kanavissa suorittamalla työt **Käsittele kanta-asiakkuusmallit** ja **1050** (kanta-asiakastiedot).
    
    ![Liitoksen perustuva ansaitseminen](./media/Affiliation%20based%20earning.png "Liitoksen perustuva ansaitseminen")

- Jälleenmyyjillä on usein erikoishinnat sellaisille asiakasryhmille, joiden yhteydessä he eivät halua käyttää kanta-asiakasohjelmia. Tällaisia ovat esimerkiksi tukkukauppiaat ja työntekijät, joille käytetään erikoishintoja mutta jotka eivät saa kanta-asiakaspisteitä. Yleensä liitosten avulla erikoishinnoittelu voidaan kohdistaa kyseisille asiakasryhmille. Jos jälleenmyyjä haluaa estää tietyn asiakasryhmän asiakkaita ansaitsemasta kanta-asiakaspisteitä, hän voi määrittää yhden liitoksen tai useita liitoksia kanta-asiakasmallin **Pois suljetut liitokset** -osassa. Tällä tavoin pois suljettuun liitokseen kuuluvat asiakkaat ovat nykyisiä kanta-asiakasohjelman jäseniä, mutta he eivät ansaitse kanta-asiakaspisteitä ostoksistaan. Voit toteuttaa muutokset kanavissa suorittamalla työt **Käsittele kanta-asiakkuusmallit** ja **1050** (kanta-asiakastiedot).

    ![Pois suljetut liitokset](./media/Excluded%20affiliations.png "Liitosten sulkeminen kanta-asiakaspisteiden ansaitseminen ulkopuolelle")
    
- Jälleenmyyjät voivat luoda kanta-asiakaskortin numeroita kanavissa. Ennen lokakuun 2018 päivitystä jälleenmyyjät pystyivät käyttämään fyysisiä kanta-asiakaskortteja tai luomaan kanta-asiakaskortin jonkin yksilöivän asiakastiedon, kuten puhelinnumeron, avulla. Jos haluat ottaa käyttöön kanta-asiakaskorttien automaattisen luonnin vähittäismyymälässä, ota **Luo kanta-asiakaskortin numero** käyttöön myymälään liitetyssä toimintoprofiilissa. Jälleenmyyjät voivat myöntää kanta-asiakaskortteja asiakkaille verkkokanavissa IssueLoyaltyCard-ohjelmointirajapinnan avulla. Jälleenmyyjät voivat joko antaa kanta-asiakaskortin numeron tähän ohjelmointirajapintaan, ja kanta-asiakas muodostetaan sitten sen perusteella, tai sitten järjestelmä käyttää Dynamics 365 for Retailissa määritettyä kanta-asiakaskortin numerosarjaa. Jos numerosarjaa ei ole kuitenkaan ole eikä jälleenmyyjä anna kanta-asiakaskortin numero ohjelmointirajapintaa kutsuttaessa, seurauksena on virheilmoitus.

    ![Kanta-asiakaskortin luonti](./media/Generate%20loyalty%20card.png "Kanta-asiakaskortin numeron luominen automaattisesti")

- Ansaitut ja lunastetut kanta-asiakaspisteet tallennetaan nyt jokaiselle tapahtumalle ja myyntitilaukselle myyntiriveillä, joten sama summa voidaan hyvittää tai poistaa täyden tai osittaisen palautuksen yhteydessä. Koska pisteet ovat nähtävillä myyntirivitasolla, puhelinkeskuksen käyttäjät voivat vastata asiakkaiden kunkin rivin ansaittuja tai lunastettuja pisteitä koskeviin kysymyksiin. Ennen tätä muutosta palkkiopisteet laskettiin aina uudelleen palautusten aikana, jolloin tulokseksi saatu summa ei ollut sama kuin alkuperäinen summa, jos ansaitsemis- tai lunastussääntöjä oli muutettu. Puhelinkeskuksen käyttäjät eivät myöskään nähneet piste-erittelyä. Pisteitä voidaan tarkastella kunkin kanta-asiakaskortin **Korttitapahtumat**-lomakkeessa.    
- Jälleenmyyjät voivat nyt määrittää muodostumiskauden kullekin palkkiopisteelle. Muodostumiskauden määritykset määrittävät keston ansaitsemispäivästä, jonka jälkeen palkkiopisteet tulevat asiakkaiden käyttöön. Muodostumattomia pisteitä voidaan tarkastella **Kanta-asiakaskortit**-sivun **Muodostumattomat pisteet** -sarakkeessa. Jälleenmyyjät voit määrittää myös kanta-asiakaskorttikohtaisen kanta-asiakaspisteiden enimmäismäärän. Tämän kentän avulla voidaan vähentää kanta-asiakkuuspetosten vaikutusta. Kun kanta-asiakaspisteitä on enimmäismäärä, käyttäjä ei voi ansaita lisää pisteitä. Jälleenmyyjä voi päättää estää kyseisten korttien käytön siihen saakka, että mahdollinen petos on tutkittu. Jos jälleenmyyjä tulee siihen tulokseen, että kyse on petoksesta, jälleenmyyjä voi asiakkaan kanta-asiakaskortin estämisen lisäksi merkitä myös asiakkaan estetyksi. Voit tehdä sen määrittämällä **Estä asiakasta liittymästä kanta-asiakasohjelmaan** -ominaisuudeksi **Kyllä** **Vähittäismyynti**-pikavälilehden **Kaikki asiakkaat** -kohdassa. Estetyille asiakkaille ei voi myöntää kanta-asiakaskorttia missään kanavassa.

    ![Muodostuminen ja palkkiopisteiden enimmäismäärä](./media/Vesting%20and%20maximum%20reward%20points.png "Muodostumisen ja palkkipisteiden enimmäismäärän määrittäminen")

- Liitokset mahdollistavat erikoishinnoittelun ja alennukset, mutta käytössä voi olla myös sellaisia liitoksia, joita jälleenmyyjät eivät halua asiakkaiden näkevän. Esimerkiksi Paljon kuluttava asiakas -niminen liitos ei välttämällä miellytä kaikki asiakkaita. Lisäksi on joitakin liitoksia, joita ei pitäisi hallita myymälässä. Tällaisia ovat esimerkiksi työntekijäliitokset, sillä kassojen ei haluat määrittävän, kuka on työntekijä ja kenelle voi antaa työntekijäalennuksia. Jälleenmyyjät voivat valita liitokset, jotka on piilotettava vähittäismyyntikanavissa. Liitoksia, joissa on merkintä **Piilota kanaviin**, ei voi tarkastella, lisätä eikä poistaa myyntipisteessä. Liitokseen liitettyjä hintoja ja alennuksia käytetään silti tuotteissa.

    ![Liitosten piilotus](./media/Hide%20affiliations.png "Liitosten piilotus kanaviin")
    
- Puhelinkeskuksen käyttäjien on nyt helpompi etsiä asiakkaita kanta-asiakaskortin tietojen avulla sekä siirtyä asiakkaan kanta-asiakaskorttiin ja kanta-asiakaskortin tapahtumasivulle **Asiakaspalvelu**-sivulta.

    ![Asiakaspalvelu](./media/Customer%20service.png "Asiakkaan kanta-asiakastietojen etsiminen")
    
- Jos kanta-asiakaskortti on vaarantunut, sen korvaava kortti on luotava ja kortin pisteet siirrettävä uudelle kortille. Korvaavan kortin työnkulkua on yksinkertaistettu tässä versiossa. Lisäksi asiakkaat voivat lahjoittaa osan kanta-asiakaspisteistä tai kaikki pisteet ystäville ja perheenjäsenille. Kun pisteitä siirretään, kummallekin kanta-asiakaskortille luodaan pisteiden oikaisukirjaukset. Korvaava kortti ja saldon siirtotoiminto ovat käytettävissä **Kanta-asiakaskortit**-sivulta.

    ![Pisteiden korvaaminen ja siirtäminen](./media/Replace%20and%20transfer%20points.png "Asiakaskortin korvaaminen tai saldon siirtäminen")
    
- Jälleenmyyjät haluavat ehkä hyödyntää tiettyä tehokasta kanavaa asiakkaiden rekisteröinnissä kanta-asiakasohjelmaan. Kanta-asiakaskorttien rekisteröintilähteen voi nyt tallentaa, joten jälleenmyyjät voivat luoda raportteja näiden tietojen perusteella. Rekisteröintilähde tallennetaan automaattisesti kaikille MPOS/CPOS- tai sähköisten kaupankäyntikanavien kautta myönnetyille kanta-asiakaskorteille. Jos kanta-asiakaskortti on myönnetty taustasovelluksesta, puhelinkeskuksen käyttäjä voi valita soveltuvan kanavan.
- Aiemmissa versioissa jälleenmyyjät voivat käyttää MPOS/CPOS:aa asiakkaiden kanta-asiakaspisteiden lunastamiseen myymälässä. Koska näissä versioissa kanta-asiakassaldo näytettiin kanta-asiakaspisteinä, kassa ei voinut tarkastella summaa valuutta-arvona, jota olisi voitu käyttää nykyisessä tapahtumassa. Kassan oli muunnettava pisteet valuutaksi, ennen kuin hän pystyi maksamaan kanta-asiakaspisteet. Sen jälkeen kun nykyisessä versiossa rivit on lisätty tapahtumaan, kassa näkee summan, jonka kanta-asiakaspisteet kattavat nykyisessä tapahtumassa. Niinpä tapahtumaan voi käyttää kaikki kanta-asiakaspisteet tai osan niistä. Lisäksi kassa näkee 30 päivän kuluessa vanhenevat pisteet, mikä mahdollistaa lisä- tai ristiinmyynnin, sillä asiakasta voidaan kannustaa käyttämään vanhenevat pisteet kyseissä tapahtumassa.

    ![Kanta-asiakassaldon kattamat pisteet](./media/Points%20covered%20by%20loyalty%20balance.png "Kanta-asiakaspisteiden kattaman saldon näyttäminen")

    ![Vanhentuvat pisteet](./media/Expiring%20points.png "Vanhentuvien pisteiden näyttäminen")
    
## <a name="upcoming-enhancements"></a>Tulevat parannukset

Seuraavat ominaisuudet tulevat käyttöön Dynamics 365 for Retailin tulevissa kuukausipäivityksissä.
    
- Asiakkaat haluavat mahdollisuuden tarkastella kanta-asiakassaldon tietoja kuluttajille suunnatuissa kanavia. Vastaavasti on tärkeää, että kassat näkevät asiakkaan kanta-asiakaspisteiden historian MPOS/CPOS:ssä, jotta he voivat vastata nopeasti asiakkaiden kysymyksiin. Asiakkaat ja kassat tulevat näkemään kanta-asiakashistorian tiedot tulevassa kuukausijulkaisussa.
- Monet jälleenmyyjät voivat myöntää kanta-asiakaspisteitä vain myyntitapahtumien perusteella. Asiakaskeskeiset jälleenmyyjät haluavat kuitenkin palkita asiakkaansa myös muista brändiin liittyvästä toiminnosta. He haluavat esimerkiksi palkita verkkokyselyyn vastaamisesta, myymälävierailusta, jälleenmyyjän tykkäämisestä Facebook ja jälleenmyyjästä twiittaamisesta. Mahdollisuus antaa kanta-asiakaspisteitä asiakkaan kaikenlaisesta toiminnasta tullaan lisäämään myöhemmin. Sitä varten jälleenmyyjä voi määrittää muun tehtävätyypin ja näille tehtäville ansaitsemissäännöt. Paljastemme myös Retail Server -ohjelmointirajapinnan, jota voidaan kutsua, kun määritetään tehtävä, jota käytetään kanta-asiakaspisteiden myöntämisen ansaitsemissääntönä.
- Aidon monikanavaisen jälleenmyyntikokemuksen toteutumista varten annamme asiakkaalle mahdollisuuden ansaita ja lunastaa kanta-asiakaspisteitä kaikissa kanavissa.
- Maksuton tai alennettu toimitus on yksi tärkeimmistä tekijöistä, joilla asiakkaat motivoidaan tekemään verkko-ostoksia. Jotta jälleenmyyjät voisivat määrittää toimituskampanjat, olemme ottaneet uudenlaisen kampanjan, jossa jälleenmyyjä määrittää raja-arvot, jonka ylitettyään asiakkaat saavat alennetun tai maksuttoman toimituksen.

