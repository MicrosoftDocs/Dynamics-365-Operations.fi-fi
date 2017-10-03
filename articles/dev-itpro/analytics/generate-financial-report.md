---
title: Luo raportti
description: "Tässä aiheessa on tietoja talousraporttien luonnista."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9b0d8fd9f5ae9d99f299cc71d7caef021ad3fb9d
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017

---

# <a name="generate-a-financial-report"></a>Luo raportti

[!include[banner](../includes/banner.md)]


Tässä aiheessa on tietoja talousraporttien luonnista. 

Luo raportti avaamalla raportin määritys ja valitsemalla sitten Luo-painike työkalurivillä. Näytölle avautuu Raporttijonon tila -ikkuna, joka näyttää raporttisi paikan jonossa. Luotu raportti avautuu oletuksena Web Viewerissä.
| ![Huomautus](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Huomautus")**Huomautus**        |
|------------------------------------------------------------------------------------------------|
| Voit luoda raportteja vain kansioihin ja sijainteihin, joiden käyttöoikeudet sinulla on. |

Seuraavassa taulukossa kerrotaan raporttien luonnissa käytettävissä olevista vaihtoehdoista.

| Vaihtoehto                                                                                | Lisätietoja |
|---------------------------------------------------------------------------------------|----------------------|
| Määritä aikataulu raportin tai raporttiryhmän automaattista luontia varten              |                      |
| Tarkista, ettei raportista puutu tilejä tai tietoja ja vahvista raportin virheettömyys |                      |

Raportteja luotaessa käytetään Raportin määritys -välilehdissä määritettyjä asetuksia. Voit määrittää Tuotos ja jakelu -välilehdessä raporttikirjaston sijainnin. Tällä tavoin raportti on helppo jakaa.

## <a name="schedule-report-generation"></a> Raportin luonnin ajoitus
Useilla yrityksillä on ydinjoukko raportteja, jotka ajetaan määrätyin väliajoin linjassa yrityksen liiketoimintaprosessien kanssa. Voit ajoittaa raportin muodostumaan säännöllisesti, esim. päivittäin, viikoittain, kuukausittain tai vuosittain. Tämä voi koskea yksittäistä raporttia tai raporttiryhmää, johon sisältyy useita yrityksiä. Sinun on syötettävä tunnistetietosi kullekin määritetylle yritykselle esim. raportointipuun määrityksissä. Jos tunnistetietosi eivät ole voimassa, raportti näyttää sinulle vain ne tiedot, joihin sinulla on käyttöoikeus, kuten yritys, johon olet kirjautunut kyseisellä hetkellä. Tuotostiedot luetaan ensin raporttiryhmästä ja sen jälkeen yksittäisistä raporteista.

Kun raporttien aikatauluja luodaan ja tallennetaan, ne näytetään siirtymisruudun kohdassa Raporttien aikataulut. Voit luoda kansioita raporttien järjestämistä varten. Jos yksittäinen aikataulutettu raportti jää suorittamatta, kaikkien muiden raporttien muodostuminen jatkuu.
| ![Tärkeää](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Tärkeää")**Tärkeää**                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Voidaksesi luoda, muokata ja poistaa raporttien aikatauluja, sinulla on oltava suunnittelijan tai järjestelmänvalvojan rooli. Kun raportti on ajettu, sen luomiseen käytetään sen käyttäjän tunnistetietoja, joka on luonut raportin. |

### <a name="create-a-report-schedule"></a>Raporttiaikataulun luominen

1.  Napsauta raportin suunnitteluohjelman Tiedosto-valikossa Uusi ja valitse sitten Raporttiaikataulu. Näyttöön avautuu valintaikkuna Uusi raporttiaikataulu.
2.  Valitse kohdassa Asetukset yksittäinen ajastettava raportti tai raporttiryhmä. Vain sen yrityksen tai rakenneosavalinnan raportit tai raporttiryhmät, joihin olet kirjautuneena, ovat käytettävissäsi.
3.  Valitse Aktiivinen -valintaruutu ottaaksesi käyttöön raporttiaikataulun. Vain raportin luoja tai järjestelmänvalvoja voi ottaa käyttöön tai poistaa raporttiaikataulun.
4.  Syötä yrityksen tunnistetiedot valitsemalla Käyttöoikeudet -painike. Oletuksena käytetään kirjautumistietojasi sille yritykselle, johon olet kirjautuneena. Jos muita yrityksiä on mukana valinnassa, esim. raportointipuun määrityksissä, valitse Käytä erillisiä tunnistetietoja ja syötä sitten jonkin toisen raporttiaikatauluun sisältyvän yrityksen tunnistetiedot. Voit valita Windows-todennuksen tai kirjoittaa käyttäjänimen ja salasanan kullekin yhtiölle. Tallenna näiden yhtiöiden tunnistetiedot valitsemalla Tallenna tunnistetiedot -valintaruutu ja napsauta sitten OK sulkeaksesi valintaikkunan.
5.  Valitse päivä, jolloin aikataulun tulee alkaa, kohdassa Tiheys kentässä Aloita toisto. Oletusarvona valitaan asiakastietokoneen järjestelmän päivämäärä.
6.  Valitse aika, jolloin raportin tulee muodostua, Muodosta raportti klo -kentässä. Jos syötät ajan, joka on ennen senhetkistä järjestelmän aikaa, raportti muodostuu seuraavana ajoitettuna päivämääränä.
7.  Määritä raportin muodostumistiheys Toistumismalli-alueella. Oletuksena valitaan Päivittäin ja Aikaväli (päivinä) -arvoksi 1. Muut vaihtoehdot ovat Viikoittain, Kuukausittain ja Vuosittain.
8.  Valitse alueella Toistumisalue, milloin raportin luonnin tulee päättyä.
    -   Ei päättymispäivää – Raporttiaikataulu jatkuu toistaiseksi.
    -   Määritä esiintymien määrä – Raporttiaikataulu jatkuu määritetyn toistojen määrän ajan ja poistetaan sitten käytöstä.
    -   Päättymispäivämäärä – Raporttiaikataulu päättyy määritettynä päivänä.

9.  Napsauta Tallenna valikkorivillä. Syötä Tallenna nimellä -valintaikkunaan yksilöivä nimi ja raporttiaikataulun kuvaus.

Voidaksesi kopioida raporttiaikataulun, sinulla on oltava suunnittelijan tai järjestelmänvalvojan rooli. Vaikka järjestelmänvalvoja muokkaisi raporttiaikataulua, raportilla säilyy raportin luojan tunnistetiedot.
### <a name="copy-a-report-schedule"></a>Kopioi raporttiaikataulu

1.  Valitse raportin suunnitteluohjelman siirtymisruudussa Raporttiaikataulut ja avaa kopioitavat raporttiaikataulut.
2.  Valitse Tiedosto-valikossa Tallenna nimellä ja täytä aikataululle uusi nimi ja kuvaus Tallenna nimellä -valintaikkunassa. Napsauta OK ja uusi aikataulu näytetään siirtymisruudussa.
3.  Muokkaa uuden aikataulun kenttiä ja tietoja tarpeen mukaan ja valitse sitten työkalurivissä Tallenna, tai valitse Tallenna Tiedosto-valikossa.

Sinun on oltava raporttiaikataulun omistaja tai sinulla on oltava järjestelmänvalvojan rooli poistaaksesi raporttiaikataulun.
### <a name="delete-a-report-schedule"></a>Raporttiaikataulun poistaminen

1.  Valitse raportin suunnitteluohjelman siirtymisruudussa Raporttiaikataulu.
2.  Valitse poistettava raporttiaikataulu ja napsauta sitten Poista tai paina Poista-näppäintä.
3.  Valitse poiston vahvistusikkunassa Kyllä poistaaksesi raporttiaikataulun pysyvästi. Jos sinulla ei ole oikeuksia poistaa aikataulua, näyttöön tulee sanoma eikä raporttia poisteta.

### <a name="credentials-and-report-schedules"></a>Tunnistetiedot ja raporttiaikataulut

Jos et syötä tarvittavia tunnistetietoja kaikille raportteihin sisältyville yhtiöille, saat seuraavan sanoman tallentaessasi raporttiaikataulun: "Sinun on syötettävä tunnistetietosi raporttiaikatauluun sisältyville yhtiöille. Valitse Käyttöoikeudet-painike syöttääksesi tunnistetietosi.”

Esimerkki: Pirjo kirjautuu Yhtiö A:han käyttäjätunnuksellaan ja salasanallaan. Hän luo aikataulun raportille, joka käyttää raportointipuun määrityksiä tietojen keräämiseen useista yrityksistä. Kun tämä raporttiaikataulu on tallennettu, Pirjolle annetaan kehote syöttää muiden raportointipuun määrityksissä määriteltyjen yritysten tunnistetiedot. Kun tunnistetietojesi voimassaolo päättyy, raporttiaikataulun raportteja ei luoda, kunnes tunnistetiedot on päivitetty. Raporttijonoon tulee sanoma ilmaisemaan, että käyttöoikeudet on päivitettävä. Raporttiaikataulu epäonnistuu, jos mikään seuraavista skenaarioista tapahtuu (koska ne vaativat tunnistetietoja):
-   Uusi yritys on lisätty raportointipuun yksittäiseen raporttiin.
-   Raporttiryhmän raporttia on muokattu.
-   Uusi raportti on lisätty raporttiryhmään lisätylle yritykselle.

Jatka valitsemalla Käyttöoikeudet-painike Raportin ajoitus -valintaikkunassa ja syötä sitten asianmukaiset tunnistetiedot.

## <a name="missing-account-analysis-feature"></a> Puuttuvien tilien analyysi -ominaisuus
Voit etsiä mahdollisesti puuttuvia kirjanpitotilejä ja dimensioita kaikista rivimäärityksistä, raportointipuumäärityksistä ja raporttimäärityksistä rakenneosaryhmässä. Tästä on hyötyä, kun luot tai päivität useita tilejä tai rakenneosia lyhyen ajanjakson aikana ja haluat varmistaa, että kaikki uusi tieto on sisällytetty raportteihisi.

Puuttuvat tilit määritetään käyttämällä rivin tai raportointipuun määrityksen alimpia ja korkeimpia arvoja. Sitten näkyviin tulee luettelo tileistä, joita ei ole rivin tai raportointipuun määrityksessä mutta jotka ovat taloushallinnon tiedoissa. Jos puuttuva tili on suurempi tai pienempi kuin rivimäärityksen arvot, kyseistä tiliä ei sisällytetä puuttuvien tilien luetteloon.
| ![Vihje](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Vihje")**Vihje**                                             |
|----------------------------------------------------------------------------------------------------------------------------------|
| Oikeellisuustarkistuksen suorittamiseksi tämä prosessi tulee ajaa ennen kuin luot kuukausiraportteja ja luodessasi uusia rakenneosia. |

On epätodennäköisempää, että arvovälejä sisältävissä raporteissa on puuttuvia tilejä. Käytä mahdollisuuksien mukaan rakenneosissa alueita, jotta voit sisällyttää uusia tilejä, kun niitä luodaan. Jos raportin määritys on asetettu arvoksi @ANY yritys, voit kirjautua määrättyyn yritykseen ja ajaa puuttuvien tilien analyysin kyseiselle yhtiölle.
| ![Huomautus](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Huomautus")**Huomautus**                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jos uusi yritys on lisätty, sinun on lisättävä tämä uusi yritys kaikkien aiemmin luotujen raporttien raportointipuihin. Muuten yritystä ei sisällytetä puuttuvien tilien analyysiin. |

### <a name="run-missing-account-analysis"></a>Puuttuvien tilien analyysin suorittaminen

1.  Valitse raportin suunnitteluohjelmassa Työkalut ja napsauta sitten Puuttuvien tilien analyysi.
2.  Valitse Yrityssuodatin-kentässä yritys, jonka tulokset suodatetaan, tai valitse Kaikki (ei suodatusta) näyttääksesi kaikkien saatavilla olevien yhtiöiden tiedot.
3.  Valitse Dimensiosuodatin-kentässä dimensio, jonka tiedot suodatetaan, tai valitse Kaikki (ei suodatusta), jos haluat tarkastella kaikkien saatavilla olevien dimensioiden dimensiotietoja.
4.  Valitse Ryhmittely-kentässä vaihtoehto tulosten lajittelulle. Voit lajitella tulokset sen rakenneosan mukaan, jota toimenpide koskee, tai voit lajitella tulokset dimension ja arvojoukkojen mukaan.
5.  Tarkastele näytettäviä tuloksia. Kun valitset nimikkeen ylemmässä ruudussa, alemmassa ruudussa näytetään poikkeuksen lisätiedot. Tämä sisältää asiaan liittyvät dimensiot, arvot ja raportit.
6.  Avaa kohta, johon tämä vaikuttaa, valitsemalla asianmukainen luetteloruudun kuvake tai napsauta kohtaa hiiren kakkospainikkeella ja valitse Avaa. Voit valita useita kohtia pitämällä Ctrl-näppäintä painettuna valitessasi kohdat alaruudussa.
7.  Jos tulokseen sisältyy mitään sellaisia arvoja, rakenneosia tai raportteja, joiden ei pitäisi sisältyä analyysiin, napsauta kyseistä kohtaa hiiren kakkospainikkeella ja valitse Sulje pois, tai valitse Sulje pois -valintaruutu kyseisen kohdan vieressä poistaaksesi sen luettelosta. Poissuljettuja nimikkeitä ei sisällytetä, kun luettelo päivitetään. Voit valita useita kohtia pitämällä Ctrl-näppäintä alhaalla samalla, kun valitset kohdat alaruudussa. Voit tarkastella nimikkeitä, mukaan lukien aiemmin analyysista pois jätettäväksi valitsemasi tulokset, valitsemalla Näytä pois jätetyt rakenneosat ja arvot -valintaruutu ja napsauttamalla sitten Päivitä.
8.  Valitse Päivitä päivittääksesi poikkeukset, jotka olet käsitellyt. Valitse Kyllä suorittaaksesi täyden päivityksen kaikille tuloksille, tai valitse Ei suorittaaksesi osittaisen päivityksen käsitellyille nimikkeille.
    | ![Huomautus](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Huomautus")**Huomautus**                    |
    |------------------------------------------------------------------------------------------------------------|
    | Lomake päivitetään automaattisesti, kun se avautuu, ellei lomaketta ole avattu viimeisen 15 minuutin aikana. |

9.  Kun ongelmat on ratkaistu, valitse OK sulkeaksesi valintaruudun.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Puuttuvien tilien analyysin pikanäppäimet
Kun suoritat puuttuvien tilien analyysin, käytettävissä on seuraavat pikanäppäimet.

| Toiminto                           | Käytä tätä pikanäppäinkoodia |
|--------------------------------------|----------------------------|
| Suodata yrityksen mukaan                    | Alt+C                      |
| Suodata dimension mukaan                  | Alt+D                      |
| Valitse Ryhmittely-kenttä            | Alt+G                      |
| Näytä pois jätetyt lohkot ja arvot      | Alt+S                      |
| Päivitä tulokset                      | Alt+R                      |
| Jätä pois valitut rakenneosat  | Alt+X                      |
| Jätä pois valittu rivimääritys  | Ctrl+B                     |
| Jätä pois valittu dimension arvo | Ctrl+D                     |
| Avaa valittu raportin määritys  | Ctrl+R                     |
| Avaa valittu rivimääritys     | Ctrl+O                     |

 
<a name="see-also"></a>Lisätietoja
--------

[Taloushallinnan raportointi](financial-reporting-intro.md)

[Report Designer -ohjelman käyttöliittymä](report-designer-interface.md)



