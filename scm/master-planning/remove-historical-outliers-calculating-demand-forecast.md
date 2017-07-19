---
title: Poista poikkeavat tiedot aiemmista tapahtumatiedoista laskettaessa ennustetarvetta
description: "Tässä artikkelissa käsitellään, miten poikkeavat arvot suljetaan pois kysynnän ennusteen laskemiseen käytettävistä historiatiedoista. Voit parantaa ennusteen tarkkuuta jättämällä poikkeavat arvot pois."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 72735c9e3fb4291076f0b577f45384dec319b2a7
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017

---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Poista poikkeavat tiedot aiemmista tapahtumatiedoista laskettaessa ennustetarvetta

[!include[banner](../includes/banner.md)]


Tässä artikkelissa käsitellään, miten poikkeavat arvot suljetaan pois kysynnän ennusteen laskemiseen käytettävistä historiatiedoista. Voit parantaa ennusteen tarkkuuta jättämällä poikkeavat arvot pois.

Voit parantaa ennusteen tarkkuuta jättämällä poikkeavat arvot pois. Tämä tehtävä on valinnainen. Prosessin yhteenveto:

1.  Voit avata **Poikkeavan arvon poistaminen** -sivun valitsemalla **Pääsuunnittelu** &gt; **Asetukset** &gt; **Kysynnän ennuste** &gt; **Poikkeavan arvon poistaminen**. Voit valita poistettavat tapahtumat tällä sivulla tekemällä kyselyjä.
2.  Valitse yritys, jota kysely koskee, ja sitten anna nimi ja kuvaus. **Kyselyn päivämäärä** -kenttään valitaan automaattisesti nykyinen päivämäärä.
3.  Valitsemalla **Aktiivinen**-valintaruudun voit jättää historiallisista tiedoista pois kyselyyn sisältyvät tapahtumat. Tämä asetus tulee voimaan, kun luot perusennusteen.
4.  Voit lisätä, poistaa ja valita **Poikkeavan arvon kysely** -sivulla ehtoja, jotka määrittävät mitkä tapahtumat jätetään pois perusennusteen laskennasta. Valitse esimerkiksi tietty nimike tai tilaus, jonka haluat sulkea pois.
5.  Valitse **Näytä tapahtumat**. **Poikkeavan arvon tapahtumat** -sivulla on luettelo tapahtumista, jotka vastaavat kyselyssä määritettyä ehtoa ja jotka suljetaan pois historiatiedoista, kun kysynnän ennuste lasketaan.

**Huomautus:** Voit luoda myös kyselyn, joka perustuu aiemmin luotuun kyselyyn. Valitse kysely, jonka haluat kopioida, ja valitse sitten **Monista**. **Kyselyn päivämäärä** -kenttä ilmaisee version. Voit käyttää kyselyä sellaisenaan tai muokata ehtoja valitsemalla **Muokkaa kyselyä**. Voit halutessasi muokata uuden kyselyn nimeä ja kuvausta.

<a name="see-also"></a>Lisätietoja
--------

[Kysynnän ennusteen esittely](introduction-demand-forecasting.md)

[Ennusteen tarkkuuden valvonta](monitor-forecast-accuracy.md)




