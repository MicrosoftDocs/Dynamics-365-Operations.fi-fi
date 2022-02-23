---
title: Toimien ennustus
description: Työntekijöihin liittyvät kulut usein muodostavat suuren osa organisaation kuluista. Toimien ennusteiden avulla voit luoda suunnitelmia näille kustannuksille ja sisällyttää ne budjettisuunnitteluun.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPositionForecast
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 64413
ms.assetid: 35e791d2-1905-4808-a579-7f181ddddd91
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5bae90cf7c8f11fa5409014023d36cc68ae1bd0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442808"
---
# <a name="position-forecasting"></a>Toimien ennustus

[!include [banner](../includes/banner.md)]

Työntekijöihin liittyvät kulut usein muodostavat suuren osa organisaation kuluista. Toimien ennusteiden avulla voit luoda suunnitelmia näille kustannuksille ja sisällyttää ne budjettisuunnitteluun.

## <a name="position-forecasting-in-budget-planning"></a>Toimien ennusteet budjettisuunnittelussa

[![Toimien ennustamisen osat](./media/graphic-top.png)](./media/graphic-top.png) 

Toimien ennustaminen käyttää kolmea pääkomponenttia oikeiden toimien kuluja koskevien budjettisummien tarjoamiseen. Nämä summat voidaan sitten tuoda budjettisuunnitelmaan budjettilaskelmia varten. 

Pääkomponentti on **ennusteen toimi**, joka edustaa kaikkia yksittäiseen toimeen liittyviin kuluihin koskevia tietoja. Voit luoda useita versioita ennusteen toimesta määrittämällä kullekin versiolle eri budjettiskenaarion. Useiden versioiden käyttäminen mahdollistaa iteroivan lähestymistavan budjetointiin sekä entä–jos-skenaarioiden vertailun. Kullakin ennusteen toimella on vastaava toimi Henkilöstöhallinnossa.

**budjetin kustannustaso** on asetusten komponentti, joka edustaa määrättyä toimeen liittyvää kustannusta, kuten peruspalkka, työnantajan maksama sairausvakuutus, matkapuhelinedut, ja niin edelleen. Budjetin kustannustaso sisältää päätilin, jota käytetään kustannuksiin ja laskentavaihtoehtoihin. Kukin budjetin kustannustaso voidaan määrittää useille ennusteen toimille. 

**kompensaatioryhmä** on valinnainen asetuskomponentti, jota käytetään budjetin kustannustasojoukon ja palkkalaskelmien soveltamiseen toimilla, joilla on samanlaiset maksuominaisuudet. Kompensaatioryhmä voi sisältää palkkojen kompensaatioruudukon. Kun ryhmä määritetään ennusteen toimelle, ruudukon taso ja vaihe voivat määrittää ennusteen toimen ansiot. Kustannuselementtijoukko lisätään automaattisesti.

### <a name="position-forecasting-processes"></a>Toimien ennustamisprosessit

[![Kuva toimien ennustamisprosesseista](./media/graphic1b.png)](./media/graphic1b.png) 

Tyypillisessä toimien ennustamisprosessissa luot ensin asetuskomponentit (budjetin kustannustasot ja kompensaatioryhmät). Ennusteen toimet luodaan tämän jälkeen aiemmin luotujen toimien perusteella. Tämän jälkeen voit sitten tehdä muokkauksia. Voit esimerkiksi lisätä tai lopettaa toimia, muuttaa palkkoja ja etujen kustannuksia sekä lisätä palkankorotuksia. Voit luoda useita versioita ennusteen toimesta mahdollistaaksesi eri budjettiskenaarioiden vertailun. Seuraavaksi voit sisällyttää ennusteen toimet budjettisuunnitelmissa ja tuoda ennusteen toimista kulut budjettisuunnitelman riveinä.

Voit luoda lisää ennusteen toimiversioita budjettisuunnitelmien muokkauksen yhteydessä. Nämä uudet versiot tarjoavat pohjan päivityksille.

## <a name="position-forecasting-setup"></a>Toimien ennusteiden asetukset
[![Kuva asetuksista](./media/graphic2-1024x327.png)](./media/graphic2.png)

### <a name="budget-cost-elements"></a>Budjetin kustannustasot

Budjetin kustannustasoja käytetään kustannustietojen määrittämiseen ennusteen toimelle. Nämä tiedot sisältävät kustannustyypin, kustannuksen laskentatavan ja tiedon, onko kustannus määritetty useille päiville, kun ennusteen toimi sisällytetään budjettisuunnitelmaan. 

Tietyt kentät määrittävät budjetin kustannustason toiminnan. Jokaiselle budjetin kustannustasolle on määritetty yksi seuraavista budjetin kustannustyypeistä: **Ansio**, **Etu**, **Verot**, tai **Muu**. Budjetin kustannustyyppejä käytetään pääasiallisesti summien laskentaan. **Ennusteen toimen ohitus** -arvo määrittää, voidaanko tason summia muokata ennusteen toimessa. **Kohdistusmenetelmä**-kenttää käytetään, kun ennusteen toimi lisätään budjettisuunnitelmaan. Voit jakaa kustannuksen summan erillisille budjettisuunnitelman riveille, joilla on eri päivämäärät, kuukausittain, neljännesvuosittain, viikoittain tai kahden viikon välein. Valitsemalla aloituspäivän määrität kustannuksen yksittäiseksi summaksi ennusteen toimessa määritettynä aloituspäivänä. 

Budjetin kustannustason kulusumman laskemisessa käytetään voimassaolopäivämääriä, jotta samaa kustannustasoa voidaan käyttää useille kausille. Kullekin kaudelle määritetään yksi päätili, samoin kuin vuosisumman prosenttiosuus, joka osoittaa kulun määrän. Budjetin kustannustasossa voidaan käyttää muiden kustannustasojen prosenttiosuuksia tai vuosittaisia summia mutta ei molempia. Voit myös määrittää vuosittaisen rajan. 

Jos kustannustaso perustuu prosenttiosuuteen, sinun on määritettävä budjetin kustannustasot, joita käytetään laskennan perustana.

**Esimerkki** 

Jaanan organisaatio tarjoaa koulutuskorvauksen, jonka määrä on viisi prosenttia työntekijän peruspalkasta. Jaana haluaa luoda budjetin kustannustason tälle kululle. Hän luo uuden budjetin kustannustason ja määrittää sille **Etu** -budjetin kustannustyypin.

Jaana ei halua, että päälliköt muuttavat edun määrää. Tämän vuoksi hän valitsee **Älä salli kustannusten muutoksia** kentässä **Ennusteen toimen ohitus**. Organisaatio haluaa, että tämä kustannus kohdistetaan tasaisesti kullekin kuukaudelle. Tästä syystä Jaana valitsee **Neljännesvuosittain** kentässä **Kohdistusmenetelmä**. 

Seuraavaksi Jodi lisää kustannuslaskentarivin, määrittää päivämäärät ja päätilin ja syöttää prosentiksi **5,00**. Hänen organisaatiollaan on 5.000 euron raja tälle edulle. Näin ollen Jaana syöttää tämän summan vuosittaiseksi rajaksi. 

Lopuksi Jaana lisää kaikki ansion kustannustasot, joita käytetään peruspalkan laskentaperusteena. Hänen budjetin kustannustasonsa on nyt valmis käytettäväksi.

### <a name="compensation-groups"></a>Kompensaatioryhmät

Kompensaatioryhmiä voidaan käyttää ryhmittämään ennusteen toimia, joilla on samanlaiset kompensaatiomääritteet. Niitä voidaan myös käyttää määrittelemään ennusteen toimen ansiot ja vuosittaiset korotukset ja määrittämään yhteisten budjetin kustannustasojen joukko. 

Kompensaatioryhmien perustoiminto on määrittää yhteisten budjetin kustannustasojen joukko ennusteen toimelle. Näin ollen kompensaatioryhmiä voidaan käyttää yhteisten kustannusten, kuten etuussuunnitelmien ja verojen, lisäämiseen. Ennusteen toimen luovan päällikön ei tarvitse tietää kaikkia lisättäviä kustannustasoja. Kustannustasoja voidaan lisätä kompensaatioryhmän valinnan yhteydessä. Tasot lisätään kompensaatioryhmän asetuksiin **Budjetin kustannustasot** -välilehdellä. 

Kompensaatioryhmät voivat myös määrittää ennusteen toimen ansiotasot. Voit määrittää ryhmän käyttämään joko tuntipohjaista tai vuosittaista palkkaa ennusteen toimen ansioiden laskentaan. Palkkojen kompensaatioruudukko määrittää ennusteen toimelle lisättävät ansiot välilehdellä **Kompensaatiotaulukot** määritetyn tason ja vaiheen perusteella. Nämä ruudukot voivat perustua olemassa oleviin Henkilöstöhallinnon kompensaatioruudukkoihin. Voit vaihtoehtoisesti luoda uuden kompensaatioruudukon budjettisuunnittelua varten. 

Kompensaatiotaulukoiden voimassaolopäivien ja vanhentumispäivien avulla voit muuttaa palkkoja haluaminasi päivänä. Tämä toiminto on hyödyllinen, kun neuvotteluyksikkö on neuvotellut yleisen palkankorotuksen kesken budjettijakson. Tässä tapauksessa muutat olemassa olevan taulukon vanhentumispäivän palkan muutosta edeltäväksi päiväksi ja lisäät uuden palkkataulukon, joka alkaa uudesta päivämäärästä. Luodessasi uutta palkkataulukkoa, valinnalla **Luo aiemmin luodusta ruudukosta uusi kompensaatioruudukko** voit valita aiemmin luodun palkkataulukon kohdasta Henkilöstöhallinto. Luodussa taulukossa voit **Joukkomuutos**-valinnan avulla määrittää prosentuaalisen tai kiinteän korotuksen tai alennuksen kaikille ruudukon palkoille. 

Kompensaatioryhmän kenttiä **Palkankorotusaikataulu** ja **Palkankorotuspäivä** käytetään, kun sinun on luotava palkankorotuksia, koska toimet siirtyvät yhdestä vaiheesta toiseen. Vuosittaiset palkankorotukset ovat tyypillinen skenaario. Palkankorotusaikataulu määrittää, käytetäänkö vaihekorotukseen toimen vuosipäivää vai samaa yleistä päivämäärää. Palkankorotusaikataulua sovelletaan kaikkiin kompensaatioryhmän ennusteen toimiin. 

Kompensaatioryhmässä valittua ansion kustannustasoa käytetään, kun luot ansioita ryhmän ennusteen toimille, mukaan lukien heidän peruspalkkansa ja mahdolliset vaihekorotukset. Kenttä **Kiinteä kompensaatiosuunnitelma** linkittää kompensaatioryhmän kiinteään kompensaatiosuunnitelmaan Henkilöstöhallinnossa. Tämä linkki voi kohdistaa työntekijän kiinteät kompensaatiotiedot ennusteen toimeen ja ne voivat siten tehdä budjettisuunnittelusta tarkempaa. Muista, että kompensaatioryhmän kompensaatioruudukon rakenteen (tasot ja vaiheet) tulee vastata kiinteän kompensaatiosuunnitelman rakennetta. Muuten järjestelmä ei pysty linkittämään kompensaatioryhmää ja kiinteää kompensaatiosuunnitelmaa oikein.

## <a name="creating-forecast-positions"></a>Ennusteen toimien luonti
[![Kuva, jossa valittuna Luo ennusteen toimet](./media/graphic3-1024x327.png)](./media/graphic3.png)

### <a name="creating-forecast-positions-for-existing-positions"></a>Ennusteen toimien luominen aiemmin luoduille toimille

Tarkinta budjettisuunnittelua varten voit luoda ennusteen toimia käyttämällä aiemmin luotujen toimien tietoja riippumatta siitä, ovatko toimet kyseisellä hetkellä täytettyjä vai ei. 

**Lisää aiemmin luotuja toimia** -toiminto näyttää kaikki organisaation toimet. Asettamalla **Alkaen**-päivämäärän voit muuttaa toimien luetteloa niin, että se sisältää toimet, jotka olivat olemassa tiettynä menneisyyden päivänä tai yleisemmin, tulevaisuudessa (esimerkiksi seuraavan budjettijakson alussa). Valitse budjettisuunnitteluprosessi ja budjettisuunnitelman skenaario, valitse toimet luettelosta ja valitse sitten **OK** luodaksesi ennusteen toimet valituille toimille. Huomaa, että voit luoda vain yhden ennusteen toimen kullekin aiemmin luodulle toimelle budjettisuunnitteluprosessissa ja -skenaariossa. Voit kuitenkin luoda lisäversioita määrittämällä eri budjettiskenaarioita. 

Jos budjetin kustannustasot on määritetty toimelle Henkilöstöhallinnossa, kyseiset budjetin kustannustasot on myös määritetty ennusteen toimelle ja ne käyttävät oletussummia. Ennusteen toimen **Määritetty työntekijä** -kentän asetus on sen työntekijän nimi, joka on määritetty toimelle, jos työntekijä on määritetty. Tämä on yksinkertainen tekstikenttä. Suoraa linkkiä ei luoda. 

Jos budjetin kustannustaso on valittuna, ennusteen toimelle määritetään kiinteä vuosikorvaus valitun kustannustason avulla, jos määritetyllä työntekijällä on kiinteä kompensaatiosuunnitelma. Jos työntekijällä ei ole kiinteää kompensaatiosuunnitelmaa tai jos työntekijää ei ole määritetty, budjetin kustannustasolle käytetään oletussummaa. 

Kun **Määritä kompensaatioryhmä** -asetuksena on **Kyllä**, jos toimeen määritetyllä työntekijällä on vaiheperusteinen kiinteä kompensaatiosuunnitelma, joka on linkitetty kompensaatioryhmään aiemmin kuvatulla tavalla, työntekijän taso ja vaihe määritetään ennusteen toimeen samoin kuin kompensaatioryhmä. Palkkojen kompensaatioryhmästä tuleva budjetin kustannustaso lisätään ennusteen toimelle, ja laskennassa käytetään kompensaatioryhmästä tulevaa tason ja vaiheen palkkaa. 

Kohdan **Määritä kompensaatioryhmä** asetus ohittaa **Budjetin kustannustason määritys** -asetuksen. Näitä kahta asetusta voidaan käyttää samaan aikaan. 

[![Määritä kompensaatioryhmä -kaavio](./media/graphic4.png)](./media/graphic4.png) 

Toinen vaihtoehto on määrittää arvoksi vuosipäivä. Määritettyä työntekijää koskeva valittu päivä (muutettu aloituspäivä, työntekijän aloituspäivä, työsuhteen alkupäivä tai ikälisäpäivä) määritetään sitten ennusteen toimen vuosipäiväksi ja sitä käytetään tiedoksi ja palkankorotuksia muodostettaessa.

### <a name="creating-new-forecast-positions"></a>Uusien ennusteen toimien luonti

Voit luoda uusia ennusteen toimia kahdella tavalla: kopioimalla aiemmin luotu ennusteen toimi tai luomalla täysin uusi ennusteen toimi. 

Kun ennusteen toimi valitaan, valitse **Kopioi valittu ennusteen toimi** luodaksesi uuden ennusteen toimen, jonka ennusteen tilan asetus on **Ehdotettu**. Ennusteen toimella on kaikki samat tiedot kuin kopioidulla ennusteen toimella, lukuun ottamatta määritettyä työntekijää ja mahdollisia budjetin kustannustasoa koskevia huomautuksia. Huomioi, että vastaava uusi toimi luodaan myös Henkilöstöhallinnossa. Tämän toimen kuvaus on **Ennusteen luoma**. 

Voit myös luoda täysin uuden ennusteen toimen. Valitse aiemmin luotu työ sekä budjettisuunnitelmaprosessi ja budjettisuunnitelman skenaario. Voit sitten lisätä muita haluamiasi tietoja. Tässäkin tapauksessa uusi toimi luodaan myös Henkilöstöhallinnossa samanaikaisesti.

## <a name="working-with-forecast-positions"></a>Ennusteen toimien käyttäminen
[![Kuva, jossa valittuna Muokkaa ennusteen toimia](./media/graphic5-1024x327.png)](./media/graphic5.png)

### <a name="multiple-versions-of-a-forecast-position"></a>Ennusteen toimen useat versiot

Voit muokata ennusteen toimia joko tehdäksesi tiedossa olevat muutokset budjettijaksoon tai mallintaaksesi ehdotetut muutokset. Yleinen käytäntö on luoda ennusteen toimien perusjoukko, luoda kopiot näistä ennusteen toimista ja käyttää sitten kopioita mallintamaan eri muutosjoukkoja. Kopiot määritetään eri budjettisuunnitelman skenaariolle, mutta ainakin siihen asti, kun muutokset on tehty, ne ovat muuten identtiset sen ennusteen toimen kanssa, josta ne kopioitiin. Alkuperäisillä ja kopioilla on sama toimi Henkilöstöhallinnossa. 

**Kopioi skenaarioon** -toiminto tarjoaa tämän toiminnallisuuden. Huomaa, että kullakin Henkilöstöhallinnon toimella voi olla vain yksi ennusteen toimi kussakin budjettisuunnitelman skenaariossa.

### <a name="modifying-forecast-positions"></a>Ennusteen toimien muokkaaminen

Ennusteen toimiin tehdyt muutokset rajoittuvat näihin ennusteen toimiin. Muutokset eivät vaikuta Henkilöstöhallinnon toimitietueisiin. Useimmat muutokset myös rajoittuvat muokattavana olevaan ennusteen toimeen. Toisin sanoen, muutokset koskevat nimenomaan sitä budjettisuunnitteluprosessia ja budjettisuunnitteluskenaariota, joihin toimet määritetään. Poikkeuksena tähän ovat muutokset kenttiin, jotka jaetaan tätä toimea koskien kaikissa prosesseissa ja skenaarioissa. Näihin kenttiin kuuluvat **Yleinen**-välilehden ja **Taloushallinnon dimensiot** -välilehden kentät. Kun näitä kenttiä muutetaan, uudet arvot koskevat kyseistä toimea kaikissa budjettisuunnitelman skenaarioissa. Voit näin ollen päivittää kaikkia versioita nopeasti näiden kenttien kautta.

#### <a name="budget-cost-elements"></a>Budjetin kustannustasot

Budjetin kustannustasot tarjoavat tärkeimmät tiedot budjettisuunnitelmaa varten: budjetin summan ja päätilin. Budjetin summa on summa, joka lähetetään budjettisuunnitelmaan, kun ennusteen toimi sisällytetään suunnitelmaan. Budjettisumma on laskennan tulos ja sitä ei voi muuttaa suoraan. Tämä summa on joko vuosittainen summa tai laskennallinen prosenttiosuus vuosittaisen summan peruselementeistä, jotka on kuvattu budjetin kustannustason asetuksissa. Tämä summa huomioidaan tason päivämääräalueen sisältämien päivien lukumäärän perusteella (alkupäivästä päättymispäivään) sekä ennusteen toimen **Kokopäivätyötä vastaava** (FTE) arvo. 

Esimerkiksi budjettikustannusrivi aikavälillä 1.1.2017 - 30.6.2017, jonka vuosittainen summa on 100 000 ja FTE-arvo **0,50** lasketaan kaavalla 100,000 × (181 päivää ÷ 365 päivää) × 0,50 = 24 794,52. 

Budjetin kustannuselementin rivit on laskettava uudelleen, kun FTE-arvoa muutetaan ennusteen toimella. Rivit on myös laskettava uudelleen, kun aktivointi- tai päättymispäivämääriä muutetaan. Näihin päivämääriin tehtävät muutokset voivat aiheuttaa päivityksen budjetin kustannustason aloitus- ja päättymispäivämääriin, joiden on oltava ennusteen toimen päivämäärien sisällä. Kun uudelleenlaskenta on tarpeen, **Laske uudelleen** -painike tulee saataville, ja näyttöön tulee "Vaatii laskentaa" -sanoma. Uudelleenlaskenta vaaditaan myös, jos lisäät tai poistat budjetin kustannustason.

**Esimerkki** 

Organisaatio harkitsee kahta vaihtoehtoa kirjanpitäjän toimen kustannusten alentamiseen. Yksi vaihtoehto on päättää toimi, kun vuotta on kulunut jonkin aikaa. Toinen vaihtoehto on muuttaa toimi osa-aikaiseksi koko vuoden ajaksi. Pekka on luonut ennusteen toimen nykyiselle kirjanpitäjän toimelle perusskenaariossa. Hän kopioi tämän perusmuotoisen ennusteen toimen skenaario A:han, määrittää päättymispäiväksi 31.5. ja suorittaa uudelleenlaskennan. Pekka kopioi sitten tämän perusmuotoisen ennusteen toimen skenaario B:hen, muuttaa FTE-arvoksi **0,50** ja suorittaa uudelleenlaskennan. Pekalla on nyt kolme versiota, joista kullakin on siihen vaihtoehtoon liittyvä kokonaiskustannus.

#### <a name="assigning-a-compensation-group"></a>Kompensaatioryhmän määrittäminen

Kun määrität ennusteen toimelle kompensaatioryhmän ensimmäistä kertaa, siihen lisätään oletusmuotoiset budjetin kustannustasot. Jos kustannustasot on jo määritetty ennusteen toimelle, nämä kustannustasot säilyvät. Jos kompensaatioryhmä on jo määritetty ja sitä muutetaan, aiemmin luodut budjetin kustannustasot poistetaan ja korvataan kompensaatioryhmästä tulevalla joukolla. 

Kun valitset kompensaatiotason ja vaiheen, lisätään tulobudjetin kustannustaso (joka on määritetty kompensaatioryhmässä). Vuosittainen summa lasketaan käyttämällä valitun tason ja vaiheen palkkaa ja vuosittaista tuntien määrää kompensaatioryhmässä (tai vuosipalkan ollessa kyseessä, tason ja vaiheen täyttä määrää). Tässäkin tilanteessa summassa huomioidaan budjetin kustannustason päivämääräalue ja ennusteen toimen FTE-arvo.

#### <a name="generating-increases"></a>Palkankorotusten muodostaminen

Vuosittaiset palkankorotukset (yksi kalenterivuodessa) voidaan luoda automaattisesti ennusteen toimille, joille on määritetty vaiheperusteinen kompensaatioryhmä. Valitse **Muodosta palkankorotukset** lisätäksesi tulobudjetin kustannustaso toiseksi korkeimmassa vaiheessa. Uuden tulobudjetin kustannustason aloituspäivä on ennusteen toimella näytettävä ajoitetun korotuksen päivämäärä. Tämä päivämäärä voidaan määrittää kompensaatioryhmässä kahdella eri tavalla: Jos kompensaatioryhmän palkankorotusaikataulun arvoksi on määritetty **Yleinen päivämäärä**, palkankorotuksen päivämäärä määritellään kompensaatioryhmässä. Jos palkankorotuksen aikataulun arvoksi on määritetty **Vuosipäivän päivämäärä**, käytetään ennusteen toimen vuosipäivän päivämäärä -kenttää ja vuosi tulee budjettijaksosta. Jos budjettijaksossa on useita kalenterivuosia, lisätään useita palkankorotuksia. 

Nykyisen tulobudjetin kustannustason päättymispäivämääräksi päivitetään korotusta edeltävä päivä. Uudelleenlaskentaprosessia käytetään automaattisesti, kun palkankorotuksia muodostetaan. Näin ollen, sinun ei tarvitse suorittaa uudelleenlaskentaa manuaalisesti. 

Jos valitset **Muodosta palkankorotukset** toisen kerran, prosessi suoritetaan uudelleen, mutta uusia tietueita ei lisätä. Järjestelmä muodostaa vain yhden palkankorotuksen kalenterivuotta kohden.

#### <a name="changes-from-other-pages"></a>Muutokset muilta sivuilta

Ennusteen toimien päivitykset voivat tulla myös muilta alueilta, kuten budjetin kustannustasojen ja kompensaatioryhmien asetussivuilta. Voit myös muokata ennusteen toimia joukkopäivitysprosessin avulla. 

Kaksi vaihtoehtoa on käytettävissä **Budjetin kustannustaso** -asetussivulla: **Lisää toimiin** ja **Päivitä toimia**. **Lisää toimiin** -asetus lisää budjetin kustannustason valittuihin ennusteen toimiin. Jos kustannustaso on jo määritetty ennusteen toimelle, tämä ennusteen toimi ohitetaan. **Päivitä toimet** -asetus koskee valittujen ennusteen toimien nykyisiä arvoja (päätili, prosentti, vuosittainen summa jne.) 

Kullakin prosessilla on samanlainen sivu, josta voit valita ennusteen toimia. **Lisää toimiin** -sivulla näytetään kaikki valittavissa olevat ennusteen toimet, kun taas **Päivitä toimet** -sivulla näytetään vain ne ennusteen toimet, joille on jo määritetty budjetin kustannustaso. (Näin ollen **Päivitä toimet** -sivulla voit selvittää, mihin ennusteen toimiin on jo liitetty kustannustaso.) Siirrät ennusteen toimet ylemmästä ruudukosta alempaan ruudukkoon sisällyttääksesi ne päivitykseen. 

Huomioi, että **Muuta päivämääriä** -toiminto **Kustannuslaskenta**-välilehdessä muuttaa välittömästi budjetin kustannustason ennusteen toimien aloitus- ja päättymispäivämäärät. Valintavaihtoehtoja ei ole käytettävissä. 

**Kompensaatioryhmä**-sivun **Päivitä ennusteen palkat** -toiminto määrittää nykyiset kompensaatiotaulukon summat ryhmään määritetyille ennusteen toimille. Palkat päivitetään ja kustannustasorivejä lisätään mahdollisille uusille palkkataulukon riveille (perustuen päivämääriin). Budjetin kustannustasoa ja korotuksen päivämääriä ei kuitenkaan päivitetä. Voit valita päivitettävän budjettisuunnitelmaprosessin ja budjettisuunnitelman skenaarion. Voit siten päivittää yhden skenaarion mutta jättää muut skenaariot ennalleen vertailun vuoksi. 

Voit lisätä useamman kuin yhden ennusteen toimen tai muuttaa niitä samanaikaisesti valitsemalla ennusteen toimet ja napsauttamalla **Joukkopäivitys**. Käytettävissäsi on useita vaihtoehtoja. Yksi asetus **Taloushallinnon dimensiot** -välilehdellä on hieman erilainen kuin muut, ja se liittyy budjetin kustannustasoihin. Voit lisätä budjetin kustannustasoja määrittämällä **Budjetin oletusarvot** -asetukseksi **Kyllä**. Jos budjetin kustannustasoja ei ole valittu, mutta **Budjetin oletusarvot** -asetukseksi on määritelty **Kyllä**, kaikki sillä hetkellä määritetyt budjetin kustannustasot on poistettu. 

Uudelleenlaskentaprosessia käytetään automaattisesti muutetulle ennusteen toimelle.

## <a name="bringing-forecast-positions-into-budget-plans"></a>Ennusteen toimien tuominen budjettisuunnitelmiin.

[![Kuva, jossa on valittuna Lisää budjettisuunnitelmaan](./media/graphic6-1024x327.png)](./media/graphic6.png)

Ennusteen toimien luomisen ja muokkaamisen tarkoitus on lisätä ne budjettisuunnitelmiin niin, että budjettisuunnitelmat sisältävät tarkimmat budjetin summat. Ennusteen toimia voi lisätä budjettisuunnitelmiin kahdella tavalla. Voit käyttää joko budjettisuunnitelmalla olevaa luontiprosessia tai valintaprosessia.

### <a name="generating-a-budget-plan-from-forecast-positions"></a>Budjettisuunnitelman muodostaminen ennusteen toimista

**Muodosta budjettisuunnitelma ennusteen toimista** -toiminto luo tai päivittää budjettisuunnitelmat siten, että niillä on ennusteen toimista tulevat budjetin summat ja FTE-määrät. Ennusteen toimista tulevista budjettisummista tulee budjettisuunnitelman rivien summat ja ne koostetaan taloushallinnon dimensioiden arvojen ja voimaantulopäivien perusteella. Luontiprosessissa lähteen ennusteen toimet määritetään budjettisuunnitelman riville. Voit tarkastella toimea joko lisäämällä ennusteen toimen rivinä budjettisuunnitelman asetteluun tai käyttämällä **Budjettisuunnitelman rivit** -kyselyä. Ohita tämä määritys määrittämällä **Sisällytä toimi budjettisuunnitelman riville** -asetukseksi **Ei**. 

Voit määrittää budjettisuunnitelman FTE-skenaarion sisältämään budjettisuunnitelman kokopäivätoimisuuksien (FTE) lukumäärän. Voit valita vain määrä-tyyppisiä skenaarioita, jotka sisällytetään kohdebudjettisuunnitelmaan. Kun valitset FTE-skenaarion, sinun on myös määritettävä FTE-päätili. Tätä tiliä käytetään määrä-tyyppisten budjettisuunnitelmarivien luontiin 

Lähteessä valittu budjettisuunnitteluprosessi ja budjettisuunnitelman skenaario määrittävät kohteen budjettisuunnitteluprosessin ja -skenaarion. Koska nämä määritteet on liitetty ennusteen toimille, ne on synkronoitava budjettisuunnitelman kanssa. Näin ollen näitä määritteitä ei voida muokata kohteessa. 

Samoin kuin muissakin luontiprosesseissa, saatavilla on kolme vaihtoehtoa:

-   **Luo uusi budjettisuunnitelma** – Luo uusi suunnitelmaa, jolla on **Kohde**-osassa valitut määritteet.
-   **Korvaa nykyinen budjettisuunnitelman skenaario**– Poista kaikki kohdebudjettisuunnitelman tiedot valitussa budjettisuunnitelmaskenaariossa ja luo uusia rivejä, joilla on valitun ennusteen toimen tiedot.
-   **Päivitä nykyinen budjettisuunnitelman skenaario ja liitä uudet tiedot** – Päivitä kohdesuunnitelman aiemmin luodut, lähderivejä vastaavat rivit, ja lisää myös uusia rivejä uusille tiedoille. Vastaavuus perustuu kirjanpitotiliin, päivämäärään, budjettiluokkaan ja muihin arvoihin, kuten ennusteen toimeen. Kaikki rivit, joilla on toimen lähdenumeroa vastaava toimen numero, korvataan uusilla riveillä lähteestä.

### <a name="selecting-forecast-positions"></a>Ennusteen toimien valitseminen

Voit myös lisätä ennusteen toimien budjettisummia suoraan budjettisuunnitelmaan. Valitse **Lisää toimiin** -toiminto budjettisuunnitelman rivien yläpuolella valitaksesi sisällytettävät ennusteen toimet. 

Budjettisuunnitelman skenaariot, jotka voit valita lähteeksi, rajoittuvat suunnitelman asetteluun sisältyviin skenaarioihin. Yksi asetus **Kohde**-välilehdellä mahdollistaa määrityksen tekemisen, jonka mukaan FTE-skenaario ja päätili ovat käytettävissä sisältämään FTE-määrät, mutta niitä ei tarvita. 

Tämä valintaprosessi toimii samoin kuin **Päivitä nykyinen budjettisuunnitelman skenaario ja liitä uudet tiedot** -asetus luontiprosessissa. Kaikki aiemmin luodut budjettisuunnitelman rivit, joissa ennusteen toimia ollaan lisäämässä, poistetaan ja ne korvataan uusilla riveillä, jotka perustuvat ennusteen toimen nykyiseen tilaan.

#### <a name="date-options"></a>Päivämääräasetukset

Sekä luontiprosessissa että valintaprosessissa budjetin kustannustason alkamispäivä määrittää vastaavan budjettisuunnitelman rivin voimaantulopäivän. Budjetin kustannustason asetussivun **Kohdistusmenetelmä**-kentässä määritetään kohdistusmenetelmä.

-   **Aloituspäivä** – Budjetin kustannustason aloituspäivää käytetään budjettisuunnitelman rivin voimaantulopäivänä.
-   **Kuukausittain** – Budjetin summa jaetaan tasan päivämääräalueeseen sisältyville kuukausille. Näin luodaan tyypillinen kuukausittainen summa, joka kohdistetaan kunkin kuukauden ensimmäiselle päivälle. Jos ensimmäinen kausi on osittainen kuukausi, kyseisen kuukauden summa muodostetaan niiden päivien lukumäärän perusteella, jolloin kulu on aktiivinen kyseisen kuukauden aikana, ja tulos kohdistetaan alkupäivälle. Viimeisen kuukauden summa on budjetin yhteissumman ja kaikkien muiden kuukausien summan erotus. Näin ollen, pyöristyksellä saattaa olla vaikutusta viimeisen kuukauden summaan.
-   **Neljännesvuosittain** – Tämä menetelmä on sama kuin **Kuukausittain**, mutta laskelmat suoritetaan kolmen kuukauden ajanjaksoille.
-   **Viikoittain** – Logiikka muistuttaa **Kuukausittain-** ja **Neljännesvuosittain**-menetelmiä. Budjetin summa jaetaan tasan päivämääräalueeseen sisältyville viikoille. Näin luodaan tyypillinen viikoittainen summa, joka kohdistetaan kunkin viikon ensimmäiselle päivälle. Jos ensimmäinen kausi on osittainen viikko, kyseisen viikon summa muodostetaan niiden päivien lukumäärän perusteella, jolloin kulu on aktiivinen kyseisen viikon aikana, ja tulos kohdistetaan alkupäivälle. Viimeisen viikon summa on budjetin yhteissumman ja kaikkien muiden viikkojen summan erotus. Näin ollen, pyöristyksellä saattaa olla vaikutusta viimeisen viikon summaan.
-   **Kahden viikon välein** – Tämä menetelmä on sama kuin **Viikoittain**, mutta laskelmat suoritetaan kahden viikon ajanjaksoille.

#### <a name="changing-budget-plan-lines-that-have-forecast-positions"></a>Ennusteen toimia sisältävien budjettisuunnitelman rivien muuttaminen

Budjettisuunnitelman rivit näyttävät budjettisummien lähteen (ennusteen toimen numero), mutta niitä ei ole linkitetty. Näin ollen ennusteen toimeen tehdyt muutokset eivät näy budjettisuunnitelman rivillä, ja budjettisuunnitelman rivin muutokset näkyvät ennusteen toimessa. Jos muutat ennusteen toimea ja haluat, että päivitykset sisällytetään budjettisuunnitelmaan, sinun on tuotava ennusteen toimi uudelleen suunnitelmaan. Muista kuitenkin, että tämä prosessi poistaa kaikki rivit, joihin ennusteen toimi on määritetty. Näin ollen kaikki näille riveille tekemäsi muutokset poistetaan. 

Jos halut nähdä, mihin budjettisuunnitelmiin ennusteen toimi on sisällytetty, voit muodostaa **Ennusteen toimet budjettisuunnitelman mukaan** -raportin. Vaihtoehtoisesti voit avata ennusteen toimella **Liittyvät budjettisuunnitelmat** -tietoruudun tarkastellaksesi suunnitelmia.



