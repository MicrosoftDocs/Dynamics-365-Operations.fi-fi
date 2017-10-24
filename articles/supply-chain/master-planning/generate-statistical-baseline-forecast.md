---
title: Luo tilastollinen perusennuste
description: "Tässä artikkelissa annetaan tietoja kysynnän ennusteissa käytetyistä parametreista ja suodattimista."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6e55999dcbc1bb9e569f3ec2374f4efb95323fb8
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="generate-a-statistical-baseline-forecast"></a>Luo tilastollinen perusennuste

[!include[banner](../includes/banner.md)]


Tässä artikkelissa annetaan tietoja kysynnän ennusteissa käytetyistä parametreista ja suodattimista. 

Kun luot perusennusteen, määritä ensin laskennassa käytettävät parametrit ja suodattimet. Voit esimerkiksi luoda perusennusteen, joka arvioi kysyntää tietyn yrityksen edellisen vuoden tapahtumatietojen perusteella tulevalle kuukaudelle ja valitulle nimikeryhmälle. 

Luo kysynnän ennuste kohdassa **Pääsuunnittelu &gt; Ennuste &gt; Kysynnän ennuste &gt; Luo tilastollinen perusennuste**. 

Ennustejakso voidaan valita ennustetta luotaessa. Käytettävissä olevat arvot ovat: Päivä, Viikko ja Kuukausi. 

Aikajaksojen lukumäärä, joille ennuste luodaan, määritetään **Ennustehorisontti**-kentässä. 

Kun ennustestrategiaksi on määritetty **Kopioi historiallisen kysynnän päälle**, historiallisen horisontin päättymispäivä jätetään huomiotta. Järjestelmä kopioi **Ennustehorisontti**-kentässä määritettyjen aikajaksojen lukumäärän kysynnän ennusteeseen, alkaen **Päivämäärästä**-kentässä **Historiallinen horisontti** -kohdassa määritetystä päivämäärästä. Kopioimalla historiallisen kysynnän määrätystä päivämäärästä eteenpäin, tuotannon suunnittelijat voivat tehdä suunnitelman seuraavalle neljännesvuodelle kahdella tavalla:

-   Kopioimalla kysynnän samasta neljännesvuodesta viime vuonna.
-   Kopioimalla kysynnän edellisestä neljännesvuodesta.

Tuotantosuunnitelmiin aiheutuvien sekaannusten välttämiseksi on mahdollista lukita määrätty ennustejaksojen määrä. Tämä luku määritetään **Lukitusaikaraja**-kentässä. Sivulla **Oikaistu kysynnän ennuste**, lukittujen aikajaksojen kentät on poistettu käytöstä. Näin annetaan visuaalinen osoitus, että näitä arvoja ei tule muuttaa. 

Perusmuotoisen kysynnän ennusteen alkamispäivämäärän ei tarvitse olla nykyinen päivä tai tuleva päivä. Määritä uusi alkupäivämäärä **Perusennusteen alkamispäivä - alkaen** -kentässä. Esimerkiksi kesäkuussa käyttäjät voivat luoda ennusteen seuraavalle vuodelle. Koska ennusteen aikajaksot historiallisen kysynnän päättymispäivän ja perusennusteen alkamispäivän välillä puuttuvat, ennusteet eivät ehkä ole oikeita. Jos käytät Microsoft Dynamics 365 for Finance and Operationsin kysynnän ennustepalvelua, voit täyttää puuttuvat kohdat neljällä tavalla. Voit valita haluamasi menetelmän määrittämällä MISSING\_VALUE\_SUBSTITUTION (Puuttuvan arvon korvaus) -parametrin **Kysynnän ennusteen parametrit** -sivulla. 

**Perusennusteen alkamispäivä**  -  **Päivämäärästä** -kenttä on määritettävä ennusteaikajakson alkuun, esimerkiksi Yhdysvalloissa sunnuntaille, jos ennusteaikajakso on viikko. Järjestelmä muokkaa automaattisesti **Perusennusteen alkamispäivä**  -  **Päivämäärästä** -kentän vastaamaan ennusteaikajakson alkua. 

**Perusennusteen alkamispäivä**  -  **Päivämäärästä** -kenttään voidaan määrittää mennyt päivämäärä. On toisin sanoen mahdollista luoda kysynnän ennuste menneisyydelle. Tämä on hyödyllistä, koska sen avulla käyttäjät voivat optimoida ennustepalvelun parametrit siten, että tilastollinen menneisyydelle luotu ennuste vastaa todellista historiallista kysyntää. Käyttäjät voivat sitten jatkaa näiden parametriasetusten käyttöä luodakseen tilastollisen perusennusteen tulevaisuudelle. 

Aiemmissa kysynnän ennusteen iteraatioissa tehtyjä manuaalisia oikaisuja voidaan käyttää automaattisesti uudessa perusennusteessa, jos **Siirrä manuaaliset oikaisut kysynnän ennusteeseen** -valintaruutu on valittuna. Jos tämä valintaruutu on tyhjä, manuaalisia oikaisuja ei lisätä perusennusteeseen, mutta niitä ei poisteta. Ennusteeseen tehdyt manuaaliset oikaisut voidaan poistaa vain ennusteen tuontihetkellä tyhjentämällä **Tallenna kysynnän perusennusteeseen tehdyt manuaaliset oikaisut** -valintaruutu. Manuaaliset oikaisut tallennetaan varmennushetkellä. Niinpä jos käyttäjä tekee manuaalisia oikaisuja ennusteeseen mutta ei varmenna ennustetta takaisin Finance and Operationsiin, muutokset häviävät. Lisätietoja manuaalisista oikaisuista ja miten ne toimivat on kohdassa [Oikaistun ennusteen varmennus](authorize-adjusted-forecast.md). 

Kysynnän ennusteen luonnilla voi olla nimi ja kommentteja, jotka auttavat käyttäjiä tunnistamaan luodun ennusteen. Nämä arvot näkyvät ennusteen luontihistoriassa **Tilastollisen perusennusteen luontihistoria** -sivulla. 

Konsernin sisäinen suunnitteluryhmä, nimikkeen kohdistustunnukset ja muut suodattimet voidaan määrittää ennusteen luontihetkellä. Niitä voidaan käyttää parantamaan suorituskykyä tai jakamaan tiedot hallittaviin paloihin. Huomaa kuitenkin, että kysynnän ennustetta ei luoda nimikkeen kohdistusryhmän jäsenille, joita ei ole määritetty konsernin sisäiseen suunnitteluryhmään, vaikka kyseinen nimikkeen kohdistustunnus olisi valittuna kyselyssä. 

**Vihje** Joskus käyttäjät saattavat saada virheitä luodessaan kysynnän ennusteita, tai kysynnän ennuste suoritetaan loppuun ilman istuntolokia. Tämän voivat aiheuttaa aiemmin ennusteen luonnissa käytetyt kyselyn ylijäämätiedot. Voit ratkaista tämän ongelman valitsemalla **Valitse** avataksesi **Kysely**-sivun, napsauta **Nollaa**, ja luo sitten perusennuste. 

Jos ennustetta ei luoda isolle nimikejoukolle vaan esimerkiksi yhdelle nimikkeelle tai yhdelle nimikkeen kohdistustunnukselle kerrallaan, voit saavuttaaksesi paremman suorituskyvyn valita **Käytä pyyntö-vastaus-tilaa** -valintaruudun **Pääsuunnittelu - Asetukset - Kysynnän ennusteet**  -  **Kysynnän ennusteiden parametrit - Azuren automaattianalyysipalvelut** -välilehti.

<a name="see-also"></a>Lisätietoja
--------

[Kysynnän ennusteiden asetukset](demand-forecasting-setup.md)

[Manuaalisten oikaisujen tekeminen perusennusteeseen](manual-adjustments-baseline-forecast.md)

[Oikaistun kysynnän ennusteen valtuuttaminen](authorize-adjusted-forecast.md)




