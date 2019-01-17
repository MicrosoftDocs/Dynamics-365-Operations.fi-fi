---
title: Toimintojen hallinta
description: "Tässä ohjeaiheessa selitetään Microsoft Dynamics 365 for Retailin valikoimien hallinnan peruskäsitteitä ja pohditaan projektin käyttöönottovaihtoehtoja."
author: jblucher
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: jeffbl
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Application update 5
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 033968667048faf475b13f8fb95e693dc26935ca
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="assortment-management"></a>Toimintojen hallinta

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Yleiskuvaus

Microsoft Dynamics 365 for Retailissa on *valikoimia*, joilla voi hallita tuotteiden saatavuutta eri kanavissa. Valikoimat määrittävät, mitkä tuotteet ovat saatavana tietyissä myymälöissä tiettyinä aikoina.

Retailissa valikoimaan yhdistetään vähintään yksi kanava (tai kanavaryhmä organisaatiohierarkioita käytettäessä) vähintään yhteen tuotteeseen (tai tuoteryhmiään luokkahierarkioita käytettäessä).

Kanavan kokonaistuoteyhdistelmä määritetään kanavaan määritettyjen julkaistujen valikoimien mukaan. Tämän vuoksi kanavakohtaisesti voi määrittää useita aktiivisia valikoimia.

### <a name="basic-assortment-setup"></a>Perusvalikoiman asetukset

Seuraavassa esimerkissä kullekin myymälälle on määritetty yksilöllinen valikoima. Tässä tapauksessa vain tuote 1 on saatavana myymälässä 1 ja vain tuote 2 on saatavana myymälässä 2.

![Kukin tuote on saatavana yhdessä myymälässä](./media/Managing-assortments-figure1.png)

Jos haluat, että tuote 2 on saatavan myymälässä 1, voit lisätä tuotteen valikoimaan 1.

![Tuote 2 lisätty valikoimaan 1](./media/Managing-assortments-figure2.png)

Vaihtoehtoisesti voit lisätä myymälän 1 valikoimaan 2.

![Myymälä 1 lisätty valikoimaan 2](./media/Managing-assortments-figure3.png)

### <a name="organization-hierarchies"></a>Organisaatiohierarkiat

Tilanteissa, joissa useat kanavat jakavat samat tuotevalikoimat, valikoimat voidaan määrittää käyttämällä Retailin valikoiman organisaatiohierarkiaa. Kun tämän hierarkian solmuja lisätään, kaikki kyseisen solmun ja sen alisolmujen kanavat lisätään.

![Organisaatiohierarkia](./media/Managing-assortments-figure4.png)

### <a name="product-categories"></a>Tuoteluokat

Tuotepuolella voi vastaavasti sisällyttää tuoteryhmiä tuoteluokkahierarkioiden avulla. Voit määrittää valikoimia sisällyttämällä vähintään yhden luokkahierarkian solmuja. Siinä tapauksessa valikoima sisältää kaikki kyseisen luokkasolmun ja sen alisolmujen tuotteet.

![Tuoteluokat](./media/Managing-assortments-figure5.png)

### <a name="excluded-products-or-categories"></a>Poissuljetut tuotteet tai luokat

Valikoimiin sisällytettävien tuotteiden ja luokkien lisäksi voit määrittää tietyt tai tuotteet suljettaviksi valikoimien ulkopuolelle Sulje pois -asetuksella. Seuraavassa esimerkissä halutaan sisällyttää kaikki tietyn luokan tuotteet tuotetta 2 lukuun ottamatta. Valikoimaa ei kuitenkaan tarvitse määrittää tuote kerrallaan tai luomalla lisää luokkasolmuja. Voit sen sijaan sisällyttää luokan mutta sulkea tuotteen pois.

> [!NOTE]
> Jos tuote on vähintään yhdessä valikoimassa sekä sisällytetty että poissuljettu, tuotetta pidetään aina poissuljettuna.

![Pois suljettu tuote](./media/Managing-assortments-figure6.png)

### <a name="global-and-released-products"></a>Yleiset ja vapautetut tuotteet

Valikoimat määritetään yleisellä tasolla, ja ne voivat sisältää useiden yritysten kanavia. Valikoimiin sisältyvät tuotteet ja luokat myös jaetaan kaikissa yrityksissä. Tuotteen on kuitenkin oltava vapautettu, ennen kuin se voidaan myydä, tilata, inventoida tai vastaanottaa kanavassa (esimerkiksi myyntipisteessä \[myyntipiste\]). Tämän vuoksi kaksi eri yrityksessä olevaa myymälää voi jakaa valikoiman, jossa on samoja tuotteita. Nämä tuotteet ovat kuitenkin saatavana vain, jos ne vapautettu kyseisiin yrityksiin.

### <a name="dynamic-and-static-assortments"></a>Dynaamiset ja staattiset valikoimat

Valikoimat voidaan määrittää sisältämään tietyt kanavat tai tuotteet tai sisällyttämällä organisaatioyksiköitä ja luokkia. Jos valikoimassa viitteitä näihin ryhmiin, niitä pidetään dynaamisina valikoimina. Jos näiden ryhmien määritys tai sisältö muuttuu, kun valikoima on aktiivinen, myös valikoiman määritys muuttuu.

Valikoima on esimerkiksi määritetty ja julkaistu alun perin siten, että se viittaa tuoteluokkaan. Jos kyseiseen luokkaan lisätään myöhemmin uusia tuotteita, kyseiset tuotteet sisällytetään automaattisesti aiemmin luodun valikoiman määritykseen. Tuotteita ei tarvitse lisätä valikoimaan manuaalisesti. Jos vastaavasti organisaatioyksikkö lisätään eri solmuun, organisaatioyksikön valikoimaa säädetään automaattisesti kyseisen määrityksen perusteella.

### <a name="stopped-products"></a>Pysäytetyt tuotteet

Voit pysäyttää myyntiprosessiin vapautetut tuotteet ottamalla asetuksen käyttöön **Tilauksen oletusasetuksissa**. Tätä asetusta käytetään useimmiten, kun tuotteen käyttöikä on päättynyt eikä sitä saa myydä missään kanavassa. Valikoimat noudattavat tätä asetukset eikä pysäytettyjä tuotteita lajitella valikoimamäärityksestä huolimatta.

### <a name="blocked-products"></a>Toimituskiellossa olevat tuotteet

Tuotteen myynnin pysäyttämisen lisäksi voit asettaa tuotteen väliaikaisesti toimituskieltoon. Voit määrittää tämän asetuksen vapautetun tuotteen **Vähittäismyynti**-välilehdessä. Toimituskiellossa olevat tuotteet kyllä lajitellaan mutta myyntipisteeseen tulee ilmoitus, jonka mukaan tuotetta ei voi myydä.

### <a name="date-effectivity"></a>Voimassaolopäivä

Valikoimilla on voimaantulopäivämäärä. Vähittäismyyjät voivatkin määrittää, milloin tuotteet voivat kanavakohtaisesti olla saatavana tai milloin ne eivät voi olla saatavana. Voit määrittää ja julkaista valikoimia etukäteen määrittämällä niiden alkamis- ja päättymispäivämäärät. Tuotteet tulevat automaattisesti saataville tai ne eivät ole saatavilla määritettyinä päivämäärinä.

### <a name="process-assortments-batch-job"></a>Valikoimien suorittaminen erätyönä

Retailissa määritetyt valikoimat on määritettävä, ennen kuin ne tulevat voimaan. Käsittely tehdään seuraavista syistä:

- Valikoiman määritysten normalisointi on poistettava, minkä ansiosta kanavien on helpompi kuluttaa niitä. Kanavan tuoteyhdistelmä voidaan määrittää useita eri päivämääräalueita kattavien useiden valikoimien kautta. Kun osa näistä tiedoista lasketaan etukäteen palvelimessa, kanavan suorituskyky paranee.
- Valikoiman tuotteet ja kanavat voivat muuttua itse valikoiman ulkopuolella. Luokkiin tai organisaatioyksiköihin viitteitä sisältävät dynaamiset valikoimat on käsiteltävä säännöllisesti, jotta ne voivat sisällyttää tai sulkea pois tietueita nykyisen märityksen perusteella.

## <a name="implementation-considerations"></a>Toteutuksessa huomioitavaa

Seuraavat käyttöönottovaatimukset kannattaa ottaa huomioon, kun suunnittelet tai hallitset valikoimia vähittäismyynnin käyttöönotossa:

- **Tietojen replikointi ja tietokannan koko** – Vaikka valikoimat voivat auttaa hallitsemaan tuotteiden saatavuutta liiketoimintatarpeen mukaisesti, ne ovat myös tärkeä työkalu kanavan ja paikallisten tietokantojen koon hallinnassa. Hyvin hallitut valikoimat auttavat vähentämään kanavassa ja paikallisissa tietokannoissa käsiteltävien ja replikoitavien tietojen määrää. Ne auttavat myös vähentämään säilytettävien tietueiden määrää. Koska näissä tietokannoissa on vähemmän tietueita, suorituskyky paranee, kun lisäät nimikkeitä tapahtumaan, hakuun ja tuoteselailuun.
- **Valikoimien voimassaolopäivä ja vanheneminen** – Yksi tehokkaimmista tavoista hallita kanavassa ja paikallisissa tietokannoissa olevien tuotteiden määrää on valikoimien voimassaolopäivämäärät. Jos sesonkituotteiden tai elinkaaren lopussa olevien tuotteiden valikoimien päivämäärä jää avoimeksi (tuotteet eivät vanhene), kyseiset tietokannat kasvavat rajattomasti. Tämän tilanteen voit ottaa hallintaan eri tavoin. Voit esimerkiksi ylläpitää erillisiä valikoimia sesonkituotteille ja aina saatavilla oleville tuotteille.
- **Valikoimien ulkopuolinen myynti ja palautukset** – Tämä toiminto auttaa jälleenmyyjiä hallitsemaan valikoimiaan tehokkaasti, sillä he voivat rajoittaa saatavana olevien tuotteiden määrän tuotteisiin, jotka sisältyvät myymälän ydintuoteyhdistelmään. Tämä toiminto auttaa jälleenmyyjiä käsittelemään myös tilanteita, joissa tuote jätettiin vahingossa pois valikoimasta tai joissa tuote palautettiin valikoiman voimassaoloajankohdan ulkopuolella.

Jos tuotetiedot eivät ole kanavatietokannassa, myyntipiste soittaa reaaliaikaisesti pääkonttoriin ja noutaa tarvittavat tiedot, jotta tuote voidaan myydä, palauttaa tai siirtää asiakastilaukseen. Tällä tavoin noudetut tuotetiedot ovat käytettävissä vain kyseisen tapahtuman aikana. Tuotetta ei lisätä valikoiman määritykseen. Niinpä jatkossa tehdään tarpeen mukaan reaaliaikaisia soittoja.

