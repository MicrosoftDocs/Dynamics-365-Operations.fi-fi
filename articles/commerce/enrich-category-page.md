---
title: Luokan saapumissivun täydentäminen
description: Tässä ohjeaiheessa kerrotaan luokkasivujen täydentämisestä Dynamics 365 Commerce -sovelluksessa.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4ab152dff0925f9c816419083577b5272ac813be
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945777"
---
# <a name="enrich-a-category-landing-page"></a>Luokan saapumissivun täydentäminen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan luokkasivujen täydentämisestä Dynamics 365 Commerce -sovelluksessa.

## <a name="overview"></a>Yleiskatsaus

Commerce tarjoaa oletusluokan saapumissivun, jota käytetään, kun luokkatiedot näytetään. Oletusluokkasivulla on pakollisia elementtejä, kuten tarkentimia, luokiteltua tuotesijoittelua, lajitteluvaihtoehtoja, valinnan yhteenveto ja sivutuksen ohjausobjekteja. 

Oletusluokkasivun sijaan voidaan käyttää luokan täydennettyä saapumissivua. Siinä on enemmän sisältöä ja erityisiä elementtejä. Tyypilliseen täydennykseen voi kuulua luokkakohtaisen markkinointisisällön lisääminen luokkasivulle. Tämä sisältö voi sisältää eri luokkien tuotesijoittelua ristiinmyyntitarkoituksia, toimituksellisia luetteloita, kuvia, videoita ja muuta tekstiä varten. Voit muokata oletusluokkasivua tai määrittää tietylle luokalle toisen luokkasivun.

![Täydennetty luokan saapumissivu](./media/CategoryLandingPages.png)

Muokkaustyökalun **Tuote**-sivulla on luokkaluettelo kanavista, jotka on määritetty sivustoon. Jos luokkasivulle on valittu **Täydennetty**-tila, luokkasivua on täydennetty. Muussa tapauksessa luokassa käytetään oletusluokkasivua ja -sisältöä. Voit esikatsella sekä täydennettyjä että muita kuin täydennettyjä luokkasivuja luokassa valitsemalla luokan nimen.

Voit täydentää luokkasivua seuraavasti:

1. Valitse **Tuotteet**-sivulla sen luokan nimi, jonka luokkasivun haluat täydentää. Valitun luokan oletusluokkasivu avautuu sivueditoriin.
2. Valitse **Täydennä luokkasivua**.
3. Valitse täydennetyn luokkasivun malli. Jos teet vain vähäisiä muutoksia, voit valita oletusluokkasivun. Vaihtoehtoisesti voit valita tietyn luokkasivunmallin. Kun valitset mallin, sivueditori avataan ja valitun mallin avulla luodaan uusi luokkasivu valitulle luokalle. Sivu kuitataan ulos sinulle. Nyt voit tehdä muutoksia.

> [!NOTE]
> Moduulit, joissa käytetään luokan määritystietoja, käyttävät valitun luokan tietoja.
>
> Valitsemasi mallin asetukset määrittävät muutokset, jotka voit tehdä.

## <a name="additional-resources"></a>Lisäresurssit

[Aiemmin luodun sivuston sivun muokkaaminen](modify-existing-page.md)

[Uuden sivuston sivun lisääminen](add-new-page.md)

[Sivun asettelujen valitseminen](select-page-layouts.md)

[SEO-metatietojen hallinta](manage-seo-metadata.md)

[Sivun tallentaminen, esikatseleminen ja julkaiseminen](save-preview-publish-page.md)

[Tuotesivun täydentäminen](enrich-product-page.md)

[Sivun sisällön helppokäyttöisyyden tarkistaminen](verify-accessibility.md)
