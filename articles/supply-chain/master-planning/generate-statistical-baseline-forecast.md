---
title: Luo tilastollinen perusennuste
description: Tässä artikkelissa annetaan tietoja kysynnän ennusteissa käytetyistä parametreista ja suodattimista.
author: t-benebo
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 98595d900f9e87a4ec6ed4c1f23971801d334487
ms.sourcegitcommit: d98ecbd9457197ec8f8e281f9c2f24dcce7b8269
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/14/2022
ms.locfileid: "8960140"
---
# <a name="generate-a-statistical-baseline-forecast"></a>Luo tilastollinen perusennuste

[!include [banner](../includes/banner.md)]

Tässä artikkelissa annetaan tietoja kysynnän ennusteissa käytetyistä parametreista ja suodattimista. 

Kun luot perusennusteen, määritä ensin laskennassa käytettävät parametrit ja suodattimet. Voit esimerkiksi luoda perusennusteen, joka arvioi kysyntää tietyn yrityksen edellisen vuoden tapahtumatietojen perusteella tulevalle kuukaudelle ja valitulle nimikeryhmälle. 

Luo kysynnän ennuste kohdassa **Pääsuunnittelu &gt; Ennuste &gt; Kysynnän ennuste &gt; Luo tilastollinen perusennuste**. 

Ennustejakso voidaan valita ennustetta luotaessa. Käytettävissä olevat arvot ovat: Päivä, Viikko ja Kuukausi. 

Aikajaksojen lukumäärä, joille ennuste luodaan, määritetään **Ennustehorisontti**-kentässä. 

Kun ennustestrategiaksi on määritetty **Kopioi historiallisen kysynnän päälle**, historiallisen horisontin päättymispäivä jätetään huomiotta. Järjestelmä kopioi **Ennustehorisontti**-kentässä määritettyjen aikajaksojen lukumäärän kysynnän ennusteeseen, alkaen **Päivämäärästä**-kentässä **Historiallinen horisontti** -kohdassa määritetystä päivämäärästä. Kopioimalla historiallisen kysynnän määrätystä päivämäärästä eteenpäin, tuotannon suunnittelijat voivat tehdä suunnitelman seuraavalle neljännesvuodelle kahdella tavalla:

-   Kopioimalla kysynnän samasta neljännesvuodesta viime vuonna.
-   Kopioimalla kysynnän edellisestä neljännesvuodesta.

Tuotantosuunnitelmiin aiheutuvien sekaannusten välttämiseksi on mahdollista lukita määrätty ennustejaksojen määrä. Tämä luku määritetään **Lukitusaikaraja**-kentässä. Sivulla **Oikaistu kysynnän ennuste**, lukittujen aikajaksojen kentät on poistettu käytöstä. Näin annetaan visuaalinen osoitus, että näitä arvoja ei tule muuttaa. 

Perusmuotoisen kysynnän ennusteen alkamispäivämäärän ei tarvitse olla nykyinen päivä tai tuleva päivä. Määritä uusi alkupäivämäärä **Perusennusteen alkamispäivä - alkaen** -kentässä. Esimerkiksi kesäkuussa käyttäjät voivat luoda ennusteen seuraavalle vuodelle. Koska ennusteen aikajaksot historiallisen kysynnän päättymispäivän ja perusennusteen alkamispäivän välillä puuttuvat, ennusteet eivät ehkä ole oikeita. Jos käytät kysynnän ennustepalvelua, voit täyttää puuttuvat kohdat neljällä tavalla. Voit valita haluamasi menetelmän määrittämällä MISSING\_VALUE\_SUBSTITUTION (Puuttuvan arvon korvaus) -parametrin **Kysynnän ennusteen parametrit** -sivulla. 

> [!NOTE]
> Puuttuvan arvon korvaus toimii vain historiallisten tietojen alkamis-ja päättymispäivämäärien välisten aukkojen tiedoissa. Se ei täytä tietoja ennen viimeisintä fyysistä tietopistettä eikä sen jälkeen, vaan se toimii olemassa olevien tietopisteiden välisenä ekstrapolaationa. 

**Perusennusteen alkamispäivä**  -  **Päivämäärästä** -kenttä on määritettävä ennusteaikajakson alkuun, esimerkiksi Yhdysvalloissa sunnuntaille, jos ennusteaikajakso on viikko. Järjestelmä muokkaa automaattisesti **Perusennusteen alkamispäivä**  -  **Päivämäärästä** -kentän vastaamaan ennusteaikajakson alkua. 

**Perusennusteen alkamispäivä**  -  **Päivämäärästä** -kenttään voidaan määrittää mennyt päivämäärä. On toisin sanoen mahdollista luoda kysynnän ennuste menneisyydelle. Tämä on hyödyllistä, koska sen avulla käyttäjät voivat optimoida ennustepalvelun parametrit siten, että tilastollinen menneisyydelle luotu ennuste vastaa todellista historiallista kysyntää. Käyttäjät voivat sitten jatkaa näiden parametriasetusten käyttöä luodakseen tilastollisen perusennusteen tulevaisuudelle. 

Aiemmissa kysynnän ennusteen iteraatioissa tehtyjä manuaalisia oikaisuja voidaan käyttää automaattisesti uudessa perusennusteessa, jos **Siirrä manuaaliset oikaisut kysynnän ennusteeseen** -valintaruutu on valittuna. Jos tämä valintaruutu on tyhjä, manuaalisia oikaisuja ei lisätä perusennusteeseen, mutta niitä ei poisteta. Ennusteeseen tehdyt manuaaliset oikaisut voidaan poistaa vain ennusteen tuontihetkellä tyhjentämällä **Tallenna kysynnän perusennusteeseen tehdyt manuaaliset oikaisut** -valintaruutu. Manuaaliset oikaisut tallennetaan varmennushetkellä. Niinpä jos käyttäjä tekee manuaalisia oikaisuja ennusteeseen mutta ei varmenna ennustetta takaisin Supply Chain Managementiin, muutokset häviävät. Lisätietoja manuaalisista oikaisuista ja niiden toiminnasta on kohdassa [Oikaistun ennusteen varmennus](authorize-adjusted-forecast.md). 

Kysynnän ennusteen luonnilla voi olla nimi ja kommentteja, jotka auttavat käyttäjiä tunnistamaan luodun ennusteen. Nämä arvot näkyvät ennusteen luontihistoriassa **Tilastollisen perusennusteen luontihistoria** -sivulla. 

Konsernin sisäinen suunnitteluryhmä, nimikkeen kohdistustunnukset ja muut suodattimet voidaan määrittää ennusteen luontihetkellä. Niitä voidaan käyttää parantamaan suorituskykyä tai jakamaan tiedot hallittaviin paloihin. Huomaa kuitenkin, että kysynnän ennustetta ei luoda nimikkeen kohdistusryhmän jäsenille, joita ei ole määritetty konsernin sisäiseen suunnitteluryhmään, vaikka kyseinen nimikkeen kohdistustunnus olisi valittuna kyselyssä. 

> [!TIP]
> Joskus käyttäjät saattavat saada virheitä luodessaan kysynnän ennusteita, tai kysynnän ennuste suoritetaan loppuun ilman istuntolokia. Tämän voivat aiheuttaa aiemmin ennusteen luonnissa käytetyt kyselyn ylijäämätiedot. Voit ratkaista tämän ongelman avaamalla **Kysely**-sivun valitsemalla **Valitse**, valitsemalla **Palauta** ja luomalla sitten perusennusteen. 

Jos ennustetta ei luoda isolle nimikejoukolle vaan esimerkiksi yhdelle nimikkeelle tai yhdelle nimikkeen kohdistustunnukselle kerrallaan, voit saavuttaaksesi paremman suorituskyvyn valita **Käytä pyyntö-vastaus-tilaa** -valintaruudun **Pääsuunnittelu - Asetukset - Kysynnän ennusteet**  -  **Kysynnän ennusteiden parametrit - Azuren automaattianalyysipalvelut** -välilehti.

> [!NOTE]
> Mahdollisen tyhjän ennusteen syynä voi olla historialliset tiedot, joiden on oltava pidemmältä historiallisesta ajanjaksolta (vähintään 3 aikajaksoa, jotta mallit voidaan havaita; esimerkiksi 3 vuotta kuukausiennusteessa). Voit yrittää saada paremman tuloksen muuttamalla aikavälin tarkkuutta tai suurentamalla sitä.

## <a name="additional-resources"></a>Lisäresurssit

- [Kysynnän ennusteiden asetukset](demand-forecasting-setup.md)
- [Manuaalisten oikaisujen tekeminen perusennusteeseen](manual-adjustments-baseline-forecast.md)
- [Oikaistun ennusteen valtuuttaminen](authorize-adjusted-forecast.md)
- [Verkkoseminaari: Kysynnän ennustaminen Azuren koneoppimispalvelun sarjojen avulla](https://aka.ms/DemandForecastingwithAzureMachineLearningSeries)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
