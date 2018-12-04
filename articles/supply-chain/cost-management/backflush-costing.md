---
title: "Jälkikustannuslaskenta"
description: "Tässä aiheessa esitellään jälkikustannuslaskennan käsite, jota käytetään Lean-valmistuksessa."
author: cvocph
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanCosting, LeanCostingTimeBucket
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272063
ms.assetid: 62a2a7da-ff79-49bf-a6e8-29460ba5252f
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: conradv
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9fe717752da4c697cf0d896c0d40832330f0d118
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="backflush-costing"></a>Jälkikustannuslaskenta

[!include [banner](../includes/banner.md)]

Tässä aiheessa esitellään jälkikustannuslaskennan käsite, jota käytetään Lean-valmistuksessa. 

Lean-valmistuksen kustannuslaskenta mahdollistaa jälkikustannuslaskentana tunnetun kustannuskertymämenetelmän käytön tuotantovirrassa. Jälkikustannuslaskentamenetelmässä kulutettavat suorat materiaalit kerätään tuotantovirran keskeneräisten töiden (KET) kustannustilille. Menetelmässä käytetään standardikustannusten varastomalliryhmää. Tuotantovirrasta vastaanotetut tuotteet vähennetään KET-tililtä niiden vakiokustannuksen mukaisesti. Tärkein ero jälkikustannuslaskennan ja vakiokustannuksen välillä on, että jälkikustannuslaskennassa variansseja ei lasketa kanban- tai lopputuotekohtaisesti. Sen sijaan varianssit lasketaan tuotantovirtakohtaisesti tietyllä aikavälillä. Tämä menetelmä esittelee todellisen Lean-konseptin materiaalikulutuksen raportointiin. Kohdistettuja materiaalin poimintamääriä ei raportoida kanbaniin tai tuotantotilaukseen. Sen sijaan kokonaiset erät tai materiaalin käsittely-yksiköt vaiheistetaan tuotantovirtaan. Kun erät tai materiaalin käsittely-yksiköt rekisteröidään tyhjiksi, ne ilmoitetaan kulutetuiksi. Erityiskulutusta voidaan käyttää, riippuen [tuotantovirran konfiguraatiosta](../production-control/lean-manufacturing-modeling-lean-organization.md). Jotta erityiskulutusta voisi käyttää, organisaatioiden on sallittava materiaalin katoaminen tuotantovirran keskeneräisistä töistä. Ajoittainen jälkikustannuslaskenta määrittää keskeneräisten töiden voimassa olevan arvon kauden loppuun. Tämä määritys perustuu kanbanin materiaalin käsittely-yksiköihin ja kanban-työn tilaan. Voimassa olevien arvojen ja todellisten KET-arvojen väliset erot kustannusryhmittäin ja nimikkeittäin lasketaan ja näytetään variansseina.

## <a name="configuring-backflush-costing"></a>Jälkikustannuslaskennan määrittäminen
Kustannuslaskenta otetaan käyttöön seuraavasti:

-   **Määritä KET-tilit tuotantoryhmälle ja tuotantovirralle.** Tuotantovirran KET-tilit määritetään tuotantoryhmässä. Jälkikustannuslaskennan tuotantovirta laskee varianssit KET-arvon erona ennen ja jälkeen jälkikustannuslaskennan ajamista kullekin tuotantovirralle. Siksi suosittelemme, että luot KET-tilin kullekin tuotantovirralle.
-   **Määritä kustannusluokka resurssiryhmään.** Työsolun ajoaikaluokkaan on määritettävä kustannusluokka. Tehtäväkohtaisen varianssin määrittämiseksi kullekin työsolulle on luotava kustannusluokka. Määrityksen ja määrän kustannusluokkia ei oteta huomioon Lean-valmistuksen kustannuslaskennassa. Resurssiryhmäkohtaisia KET-tilejä ei huomioida jälkikustannuslaskennassa. Kustannusluokka ei ole pakollinen alihankintatehtäville. Sen sijaan käytetään aktiiviselle palvelulle määritettyä kustannusryhmää.
-   **Määritä kustannusryhmät.** Tuotantovirran kustannusten osuuksien segmentointi otetaan käyttöön määrittämällä kustannusryhmät kustannusryhmätyypin mukaan.
    -   **Suorat materiaalit -kustannusryhmä** - Suora materiaali tarvitsee kustannusryhmän, jossa tunnistetaan kustannuslaskennan materiaaliluokka. Tämä kustannusryhmä mahdollistaa kootun näkymän suorien materiaalien kustannuksista, keskeneräisistä töistä ja variansseista.
    -   **Suoran tuotannon kustannusryhmä** - Suoran tuotannon kustannusryhmä sieppaa toiminnallisten resurssien suorien kustannusten osuuden tuotantovirtaan. Tämä kustannusryhmä mahdollistaa kootun suoran valmistuskustannuksen mukaisen näkymän kustannuksista, keskeneräisistä töistä ja variansseista.
    -   **Epäsuora kustannusryhmä** - Epäsuora kustannusryhmä tarvitaan, jotta epäsuorien kustannusten osuus tuotantovirrasta voidaan laskea. Tämä kustannusryhmä mahdollistaa kootun, epäsuorien kustannusten mukaisen näkymän kustannuksista, keskeneräisistä töistä ja variansseista.
    -   **Suoran ulkoistamisen kustannusryhmä** - Palveluiden kustannus mahdollistaa kootun näkymän määritetyistä kustannuksista ja keskeneräisistä töistä ja määrittää alihankittujen palveluiden kustannusvarianssit.
    -   **Valmiin tuotteen kustannusryhmä** - Valmiit tuotteet tarvitsevat kustannusryhmän, joka tunnistaa tuoteluokan kustannuslaskentaa varten. Tämä kustannusryhmä mahdollistaa kootun, tuoteluokkakohtaisen näkymän kustannuksista, keskeneräisistä töistä ja variansseista. Tuotteiden vakiokustannus lasketaan kustannuslaskelmalla, joka perustuu tuoterakenteeseen ja joko tuotantovirtaan sekä kanban-sääntöihin, tai reittiin.

### <a name="costing-sheet"></a>Kustannuslaskentalomake

Kustannuslaskennan lomake mallintaa yrityksen kustannusrakenteen ja perustuu kustannusryhmiin, jotka luokittelevat kustannukset. Kustannuslaskentalomakkeella on useita muotoja. Se näyttää kustannustiedot siinä suunnitellun rakenteen mukaisesti. Kustannuslaskentalomakkeessa määritetään myös kaava, jolla epäsuora kustannus lasketaan. Laskentakaava voi perustua määriin, painoon, tilavuuteen tai arvoon.

-   **Määritä kustannuslaskentaversio.** Kustannuslaskentaversiossa yritys määrittää, miten kustannuksia ylläpidetään. Kustannuslaskelmaversiossa voi olla standardikustannustietueiden joukko tai suunniteltujen kustannustietueiden joukko, kustannuslaskelmaversioon määritetystä kustannuslaskelmatyyppistä riippuen. Lean-valmistuksen kustannuslaskennassa käytettävän kustannuslaskentaversion on perustuttava vakiokustannukseen.
-   **Määritä varastomalliryhmä vapautetuille tuotteille.** Kaikki tuotantovirtaan liittyvät tuotteet on määritettävä varastomalliryhmään, joka käyttää **Vakiokustannus**-varastomalliryhmää. Vakiokustannuksia ylläpidetään sijainti- ja aktivointipäivämääräkohtaisesti. Päätuotteille voi valita varastomalliryhmän, jos kustannusta ylläpidetään variantti- tai päätuotekohtaisesti.
-   **Alihankintapalvelut ovat määritelmällisesti varastoimattomia palveluita.** Alihankintatehtäville ei ole varastomalliryhmää. Jotta alihankintatehtävän kustannuslaskenta voitaisiin suorittaa oikein, varmista, että palvelutehtävä kuuluu varastomalliryhmään, jonka varastointikäytäntö on **Varastoitu tuote = Epätosi**.

Valmistettavien tuotteiden kustannuslaskenta, joka perustuu tuotantovirtaan edellyttää, että vakiokustannuksia ylläpidetään palveluille, jotka liittyvät alihankintatehtäviin. Palveluille määritettävä kustannusryhmä määrittää alihankittavan tehtävän kustannusvarianssit.

## <a name="cost-calculation-for-lean-manufacturing"></a>Lean-valmistuksen kustannuslaskenta
Tuotantovirrasta valmistettujen tuotteiden tuoterakennelaskelman on perustuttava joko reitin versioon tai tuotantovirtaan. Tuoterakennelaskelman tuloksena on tuotteen kustannus ja siihen liittyvä erittely resursseista ja materiaaleista, jotka tarvitaan tuotteen rakentamiseen. Vähennys tuotantovirran KET-tililtä tapahtuu tuotteen nimike- ja kustannusryhmäerittelyn avulla.

### <a name="calculation-that-is-based-on-the-production-flow"></a>Laskelma, joka perustuu tuotantovirtaan

Microsoft Dynamics 365 for Finance and Operationsin Lean-valmistus on reittiriippumaton. Tuotantovirrasta valmistettavien tuotteiden kustannuslaskenta voi perustua tuotantovirtaan itseensä. Ennen laskennan suorittamista on luotava kanban-sääntö, joka valmistaa tuotteen tuotantovirrasta. Jos tuotteen voi valmistaa useammasta saman sijainnin tuotantovirrasta laskentapäivänä, voit valita tuotantovirran tuoterakenteen laskelmaan. Voit määrittää oletustuotantovirran kullekin nimikkeelle **Oletustuotantovirta**-sivulla. Jos saman tuotantovirran samalle tuotteelle, joka on aktiivinen laskentapäivänä, on useita kanban-sääntöjä, laskenta valitsee ensimmäisen kanban-säännön, joka on aktiivinen laskennalla.

### <a name="calculation-that-is-based-on-the-route"></a>Reittiin perustuva laskenta

Reittiin perustuva laskenta on yhtä kelvollinen kuin tuotantovirtaan perustuva laskenta. Reittiin perustuva laskenta ei kuitenkaan käytä Lean-valmistuksen kustannuslaskennan toimintoja. Reitin tulisi käyttää resurssiryhmissä resurssin tarpeita. Systemaattisen varianssin välttämiseksi sen tulisi myös käyttää samoja työsoluja tai vähintään samoja kustannusluokkia. Vältä määrityksen ja määrän kustannusluokkia myös tässä tapauksessa. Ne eivät tarjoa kustannuslaskennalle Lean-valmistuksen jälkikustannuslaskentaa eritellympää tulosta. Valitse kustannuslaskennassa käytettävä vaihtoehto (tuotantovirta vai reitti) kustannuserittelyn tulosten perusteella. Lähempänä oikeaa tilannetta ja vähemmän varianssia tuottava versio on keskimäärin parempi vaihtoehto. Lean-valmistusympäristössä, jossa tuote valmistetaan yhdessä tuotantovirrassa yhden kanban-säännön alaisena, tuotantovirtaan perustuva laskenta on luultavasti tarkempi. Tuote, joka voidaan valmistaa Lean-valmistuksen ja tuotantotilausten kautta samassa toimipisteessä, tai jolla voi olla useita tuotantovirtoja tai useita kanban-sääntöjä samassa virrassa voi saada tarkempia tuloksia reittiin perustuvan laskennan perusteella, jos se on erityisesti luotu kustannuslaskentaa varten tuotannon sijaan. Tuotantovirran laskentaa on käytettävä alihankintaa sisältävien tuotteiden laskennassa. Laskentamallit alihankinnalle tuotantotilausten kautta ja alihankinnalle Lean-valmistuksessa käyttävät eri lähestymistapoja Microsoft Dynamics 365 for Finance and Operationsissa. Lean-valmistuksessa esitellään uusi kustannusryhmätyyppi, **Suora ulkoistus**, joka koskee alihankintapalveluiden laskentaa.

## <a name="material-consumption"></a>Materiaalikulutus
Kun materiaali kulutetaan varastosta keskeneräisiin töihin, materiaalin kustannus lisätään myös keskeneräisiin töihin sen todellisen vakiokustannuksen ryhmän mukaisesti. Tämä toiminto suoritetaan seuraavissa tilanteissa:

-   Kanbanin varasto-otot kirjataan kanbanin keräysluettelon riveille, jotka päivittävät varastoa.
-   Poimittaessa, mutta ei vastaanottaessa varaston päivittävät siirtotyöt valmistuvat (Materiaalisiirto varastosta keskeneräisiin töihin).

## <a name="receiving-products-from-the-production-flow"></a>Tuotteiden vastaanottaminen tuotantovirrasta
Tuotteita vastaanotetaan tuotantovirrasta seuraavissa tilanteissa:

-   Prosessitöitä, joiden **Päivitä varasto vastaanotettaessa** -asetus on **Kyllä** valmistuu.
-   Varaston vastaanotossa päivittäviä siirtotöitä valmistuu, mutta niiden **Päivitä varasto poiminnan yhteydessä** -asetus on **Ei** (Siirto keskeneräisistä töistä varastoon). Tämän vaihtoehdon avulla voit vastaanottaa tuotteita tuotantovirrasta tuoterakenteesta ja reittimäärityksestä riippumatta. Prosessi seuraa vain fyysisiä virtoja. Tämä vaihtoehto on erityisen sopiva sivutuotteiden, oheistuotteiden tai hävikin vastaanottamiseen tuotantovirrasta sekä tuotantovirran keskeneräisten töiden kustannussaldon korjaamiseen.

Tuotantovirrasta vastaanotetut tuotteet vähennetään KET-tililtä.

## <a name="products-in-wip"></a>Keskeneräisissä töissä olevat tuotteet
Microsoft Dynamics for Finance and Operationsin Lean-valmistuksen KET-mallin avulla voit käyttää kanbanin materiaalin käsittely-yksikön tiloja keskeneräisiin töihin kuuluvan materiaalin, puolivalmiiden ja valmiiden tuotteiden hallintaan.

-   **Määritetty** - Kanban voi sisältää kulutettua materiaalia, joka on laskettu keskeneräisiin töihin.
-   **Vastaanotettu** - Jos kanban viittaa viimeisimpään tehtävään, jossa **Päivitä varasto vastaanotettaessa** -asetus on **Ei**, se ilmaisee kokonaisen materiaalin käsittely-yksikön tuotteelle tai puolivalmiille tuotteelle, jota ei ole rekisteröity varastoon.

Huomaa, keskeneräisten töiden materiaali ei näy käytettävissä olevan varaston yhteenvedoissa. Ne näkyvät kuitenkin kanbanin määräyhteenvedoissa.

## <a name="consuming-products-in-wip"></a>KET-tuotteiden kuluttaminen
KET-tuotteet kuluttaan, kun niitä vastaava kanbanin materiaalin käsittely-yksikkö tyhjennetään. Kanbanin tyhjä-signaali ei tuota aktiivista kustannuslaskennan tapahtumaa, vaan ilmenee, kun seuraava jälkikustannuslaskenta suoritetaan. Tyhjennettyjä kanbanin materiaalin käsittely-yksiköitä ei käsitellä käytettävissä olevina, ja siten ne lasketaan kulutetuiksi kyseisessä jaksossa.

### <a name="automatic-empty-registration"></a>Automaattinen rekisteröinti tyhjäksi

Ajoitetut tai tapahtuma-kanbanit voidaan asettaa suorittamaan automaattinen tyhjäksi rekisteröinti kanban-säännössä:

-   **Kun materiaalin käsittely-yksiköt vastaanotetaan** - Ajoitetut kanbanit merkitsevät materiaalin kulutetuksi oletuksena, kun kanbanin viimeinen työ on valmis. Kiinteän määrän kanbaneissa tätä vaihtoehtoa ei suositella kuin yhden lokeron kanbaneille, koska se palauttaa kortin tarpeen lähteelle aina, kun kanban vastaanotetaan loppukohteessa.
-   **Kun lähdevaatimus rekisteröidään** - Tämä vaihtoehto on käytettävissä ainoastaan tapahtumakanbaneille; tämä on oletusvaihtoehto. Keskeneräisiin töihin liittyen, tämä vaihtoehto auttaa pitämään KET-työjonon tyhjänä, sillä keskeneräisten komponenttien kanbanit tyhjennetään automaattisesti, eli kulutetaan KET-töistä, kun niiden ylätason kanban valmistellaan.

Kanbanien materiaalin käsittely-yksiköt voidaan määrittää (= kesken), vastaanottaa (=täysi) tai tyhjentää. Osittainen tyhjentäminen ei ole mahdollista. Jotta kulutuksen rekisteröinti olisi mahdollisimman tarkkaa, on tärkeää rajoittaa kanbanin tuotemääriä niin, että ne ovat pienemmät kun kauden kulutus. Tuotteita, jotka siirretään työnohjaukseen suurissa erissä kattamaan päivien tai viikkojen tarpeen ei tule kuluttaa keskeneräisiin töihin. Nämä tuotteet tulee sen sijaan pitää varastossa.

## <a name="backflush-costing"></a>Jälkikustannuslaskenta
Arvota KET-työt ja tuota kauden päätöstila, johon lasketaan materiaalin, työvoiman ja epäsuorien kustannusten varianssi suorittamalla jälkikustannuslaskenta säännöllisesti. Lasketut varianssit kirjataan varianssitileille. Kaikkia yrityksen tuotantovirtoja käytetään samassa jälkikustannuslaskentaprosessin eräajossa. Kun jälkikustannuslaskenta ajetaan eräajona, tuotantovirta voi suorittaa prosessin useammassa säikeessä. Jälkikustannuskausi määräytyy päättymispäivän mukaan. Uusia tapahtumia ei voi kirjata päivälle, jona jälkikustannuslaskenta on ajettu. Älä aja jälkikustannuslaskentaa kuluvalle päivälle ennen kuin päivä on ohi. Jälkikustannuslaskenta suorittaa seuraavat toimet.

1.  Määrittää tuotantovirrassa käyttämättömät määrät kauden päättymispäivästä alkaen. Kun jälkikustannuslaskenta on suoritettu, näet käyttämättömät määrät kustannuslaskennan suorituspäivämäärän kohdalla **Käyttämättömät määrät** -valintaikkunassa.
2.  Laskee tuotantovirran toteutuneen nettokäytön kauden aikana.
3.  Puhdistaa toteutuneet resurssin kulutukset ja tuotteet keskeneräisistä töistä.
4.  Laskee tuotannon varianssien vakiokustannukselle kauden aikana. **Kauden aikana kulutetuille osille:**
    -   Päivittää tuotantovirran kauden aikana kuluttaman materiaalin toteutuneen nettomäärän kirjanpitoon. Järjestelmä käsittelee yksittäiset varastotapahtumat ensin sisään - ensin ulos -periaatteen mukaisesti päivittäessään kirjanpitoon tuotantovirran fyysisesti päivitetyt tapahtumat, kunnes kauden toteutuneet nettomäärät on saavutettu.
    -   Tapahtumien kirjanpito jaetaan, jotta tarkat kulutusmäärät voidaan selvittää.
    -   Tuotantovirran keskeneräisissä töissä olevat käyttämättömät määrät pidetään fyysisesti päivitetyssä tilassa.

    **Kauden valmiille tuotantomäärille:**
    -   Päivittää kauden aikana valmistuneiden varastotapahtumien määrät kirjanpitoon.

    **Muunnoskustannukselle:**
    -   Käytettävät muunnoskustannustapahtumat (reittitapahtumat), jotka on kirjattu kauden aikana päivitetään kirjanpitoon.
    -   Kaikki suorat tuotannon kustannukset päivitetään kirjanpitoon. Kaikki kauden aikana valmistuneet kanban-prosessityöt kerrytetään.
    -   Kaikki kauden kulutetun materiaalin välilliset kustannukset lasketaan ja vähennetään keskeneräisistä töistä. Välillisten kustannusten jäännösarvo kirjataan varianssina.

5.  Laskee tuotannon varianssien vakiokustannukset. Varianssi lasketaan kustannusryhmäkohtaisesti.






