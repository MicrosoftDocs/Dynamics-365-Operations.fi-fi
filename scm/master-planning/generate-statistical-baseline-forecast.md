---
title: Luo ennuste tilastollinen perusaikataulu
description: "Tässä artikkelissa annetaan tietoja kysynnän ennusteissa käytetyistä parametreista ja suodattimista."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c0c918b94fe96d123bb6c25c42fe168a026cd8a9
ms.lasthandoff: 03/31/2017


---

# <a name="generate-a-statistical-baseline-forecast"></a>Luo ennuste tilastollinen perusaikataulu

Tässä artikkelissa annetaan tietoja kysynnän ennusteissa käytetyistä parametreista ja suodattimista. 

Kun luot perusennusteen, määritä ensin laskennassa käytettävät parametrit ja suodattimet. Voit esimerkiksi luoda perusennusteen, joka arvioi kysyntää tietyn yrityksen edellisen vuoden tapahtumatietojen perusteella tulevalle kuukaudelle ja valitulle nimikeryhmälle. 

Luo kysynnän ennuste, siirry **Master planning &gt;Ennustaminen &gt;kysynnän ennusteiden &gt;Luo tilastollinen perusaikataulun ennuste**. 

Ennustejakso voidaan valita ennustetta luotaessa. Käytettävissä olevat arvot ovat: Päivä, Viikko ja Kuukausi. 

Aikajaksojen lukumäärä, joille ennuste luodaan, määritetään** Ennustehorisontti**-kentässä. 

Kun ennustestrategiaksi on määritetty **Kopioi historiallisen kysynnän päälle**, historiallisen horisontin päättymispäivä jätetään huomiotta. Järjestelmä kopioi uudelleenkäytettävät määritetty määrä **horisontti ennuste** ennustettuun kysyntään, asettaa päivämäärä alkaen-kenttään **päivästä** kentän alla **historiallinen horisontti**. Kopioimalla historiallisen kysynnän määrätystä päivämäärästä eteenpäin, tuotannon suunnittelijat voivat tehdä suunnitelman seuraavalle neljännesvuodelle kahdella tavalla:

-   Kopioimalla kysynnän samasta neljännesvuodesta viime vuonna.
-   Kopioimalla kysynnän edellisestä neljännesvuodesta.

Tuotantosuunnitelmiin aiheutuvien sekaannusten välttämiseksi on mahdollista lukita määrätty ennustejaksojen määrä. Tämä luku määritetään **Lukitusaikaraja**-kentässä. Sivulla **Oikaistu kysynnän ennuste **, lukittujen aikajaksojen kentät on poistettu käytöstä. Näin annetaan visuaalinen osoitus, että näitä arvoja ei tule muuttaa. 

Perusmuotoisen kysynnän ennusteen alkamispäivämäärän ei tarvitse olla nykyinen päivä tai tuleva päivä. Määritä uusi alkupäivämäärä **Perusennusteen alkamispäivä - alkaen** -kentässä. Esimerkiksi kesäkuussa käyttäjät voivat luoda ennusteen seuraavalle vuodelle. Koska ennusteen aikajaksot historiallisen kysynnän päättymispäivän ja perusennusteen alkamispäivän välillä puuttuvat, ennusteet eivät ehkä ole oikeita. Jos käytössäsi on Microsoft Dynamics-365 toimia kysynnän ennusteet palvelu on neljä tapaa, jolla voit täyttää puuttuvat aukot. Voit valita menetelmä, jota PUUTTUVA asettamalla\_arvo\_KORVAAMISEN parametrien **kysynnän ennusteet parametrit** sivulla. 

**Ennusteen aloituspäivä perusaikataulun** - **päivästä** kentälle on määritettävä alkuun ennusteen bucket, esimerkiksi Yhdysvalloissa, jos Ennustaminen-bucket on viikon sunnuntai. Järjestelmä säätää automaattisesti **ennusteen aloituspäivä perusaikataulun** - **päivästä** vastaa ennusteen bucket alku-kenttään. 

**Ennusteen aloituspäivä perusaikataulun** - **päivästä** voidaan määrittää kentän päivämäärä on jo mennyt. On toisin sanoen mahdollista luoda kysynnän ennuste menneisyydelle. Tämä on hyödyllistä, koska sen avulla käyttäjät voivat optimoida ennustepalvelun parametrit siten, että tilastollinen menneisyydelle luotu ennuste vastaa todellista historiallista kysyntää. Käyttäjät voivat sitten jatkaa näiden parametriasetusten käyttöä luodakseen tilastollisen perusennusteen tulevaisuudelle. 

Aiemmissa kysynnän ennusteen iteraatioissa tehtyjä manuaalisia oikaisuja voidaan käyttää automaattisesti uudessa perusennusteessa, jos **Siirrä manuaaliset oikaisut kysynnän ennusteeseen** -valintaruutu on valittuna. Jos tämä valintaruutu on tyhjä, manuaalisia oikaisuja ei lisätä perusennusteeseen, mutta niitä ei poisteta. Ennusteeseen tehdyt manuaaliset oikaisut voidaan poistaa vain ennusteen tuontihetkellä tyhjentämällä **Tallenna kysynnän perusennusteeseen tehdyt manuaaliset oikaisut** -valintaruutu. Manuaaliset oikaisut tallennetaan varmennushetkellä. Siksi, jos käyttäjä tekee ennusteen manuaalisia muutoksia, mutta ei hyväksy ennuste takaisin Dynamics 365 operaatioille, muutokset menetetään. Saat lisätietoja manuaalisiin lisäyksiin ja miten ne toimivat, [sallimisesta oikaistu ennustetta](authorize-adjusted-forecast.md). 

Kysynnän ennusteen luonnilla voi olla nimi ja kommentteja, jotka auttavat käyttäjiä tunnistamaan luodun ennusteen. Nämä arvot näkyvät ennusteen luontihistoriassa **Tilastollisen perusennusteen luontihistoria** -sivulla. 

Konsernin sisäinen suunnitteluryhmä, nimikkeen kohdistustunnukset ja muut suodattimet voidaan määrittää ennusteen luontihetkellä. Niitä voidaan käyttää parantamaan suorituskykyä tai jakamaan tiedot hallittaviin paloihin. Huomaa kuitenkin, että kysynnän ennustetta ei luoda nimikkeen kohdistusryhmän jäsenille, joita ei ole määritetty konsernin sisäiseen suunnitteluryhmään, vaikka kyseinen nimikkeen kohdistustunnus olisi valittuna kyselyssä. 

**Vihje**Joskus käyttäjät saattavat saada virheitä luodessaan kysynnän ennusteita, tai kysynnän ennuste suoritetaan loppuun ilman istuntolokia. Tämän voivat aiheuttaa aiemmin ennusteen luonnissa käytetyt kyselyn ylijäämätiedot. Voit ratkaista tämän ongelman valitsemalla **Valitse** avataksesi **Kysely**-sivun, napsauta **Nollaa**, ja luo sitten perusennuste. 

Ennuste ei luoda suuri joukko kohteita, mutta, esimerkiksi yhden nimikkeen tai Nimikkeenkohdistustunnus yksi kerrallaan ja sitten saada paremman suorituskyvyn, voit valita **käyttää pyynnön vastauksen tilaa** -valintaruudun **Pääsuunnittelu - Setup - kysynnän ennusteet suunnittelun** - **kysynnän ennusteet parametrit - Azure Machine Learning** välilehti.

<a name="see-also"></a>Lisätietoja
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)


