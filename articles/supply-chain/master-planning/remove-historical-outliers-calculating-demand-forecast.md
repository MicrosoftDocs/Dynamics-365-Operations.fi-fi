---
title: Poista poikkeavat tiedot aiemmista tapahtumatiedoista laskettaessa ennustetarvetta
description: Tässä artikkelissa käsitellään, miten poikkeavat arvot suljetaan pois kysynnän ennusteen laskemiseen käytettävistä historiatiedoista. Voit parantaa ennusteen tarkkuuta jättämällä poikkeavat arvot pois.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ce8ebaf32b30c57b307f0d8799660ba6b42365a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "323614"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Poista poikkeavat tiedot aiemmista tapahtumatiedoista laskettaessa ennustetarvetta

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään, miten poikkeavat arvot suljetaan pois kysynnän ennusteen laskemiseen käytettävistä historiatiedoista. Voit parantaa ennusteen tarkkuuta jättämällä poikkeavat arvot pois.

Voit parantaa ennusteen tarkkuuta jättämällä poikkeavat arvot pois. Tämä tehtävä on valinnainen. Prosessin yhteenveto:

1.  Voit avata **Poikkeavan arvon poistaminen** -sivun valitsemalla **Pääsuunnittelu** &gt; **Asetukset** &gt; **Kysynnän ennuste** &gt; **Poikkeavan arvon poistaminen**. Voit valita poistettavat tapahtumat tällä sivulla tekemällä kyselyjä.
2.  Valitse yritys, jota kysely koskee, ja sitten anna nimi ja kuvaus. **Kyselyn päivämäärä** -kenttään valitaan automaattisesti nykyinen päivämäärä.
3.  Valitsemalla **Aktiivinen**-valintaruudun voit jättää historiallisista tiedoista pois kyselyyn sisältyvät tapahtumat. Tämä asetus tulee voimaan, kun luot perusennusteen.
4.  Voit lisätä, poistaa ja valita **Poikkeavan arvon kysely** -sivulla ehtoja, jotka määrittävät mitkä tapahtumat jätetään pois perusennusteen laskennasta. Valitse esimerkiksi tietty nimike tai tilaus, jonka haluat sulkea pois.
5.  Valitse **Näytä tapahtumat**. **Poikkeavan arvon tapahtumat** -sivulla on luettelo tapahtumista, jotka vastaavat kyselyssä määritettyä ehtoa ja jotka suljetaan pois historiatiedoista, kun kysynnän ennuste lasketaan.

**Huomautus:** Voit luoda myös kyselyn, joka perustuu aiemmin luotuun kyselyyn. Valitse kysely, jonka haluat kopioida, ja valitse sitten **Monista**. **Kyselyn päivämäärä** -kenttä ilmaisee version. Voit käyttää kyselyä sellaisenaan tai muokata ehtoja valitsemalla **Muokkaa kyselyä**. Voit halutessasi muokata uuden kyselyn nimeä ja kuvausta.

<a name="additional-resources"></a>Lisäresurssit
--------

[Kysynnän ennusteen esittely](introduction-demand-forecasting.md)

[Ennusteen tarkkuuden valvonta](monitor-forecast-accuracy.md)



