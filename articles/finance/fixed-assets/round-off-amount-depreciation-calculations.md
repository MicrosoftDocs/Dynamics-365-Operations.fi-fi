---
title: Poistojen laskennan pyöristyssumma
description: Tässä artikkelissa käsitellään Kirja-asetussivuilta löytyvää Poiston pyöristys -kenttää.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: kfend
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a93842f7cca483df89188695c945edf77e118cef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870101"
---
# <a name="round-off-amount-for-depreciation-calculations"></a>Poistojen laskennan pyöristyssumma

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään **Kirja**-asetussivuilta löytyvää **Poiston pyöristys** -kenttää.

Poiston pyöristyssummat määritetään erikseen jokaiselle kirjalle. Poiston pyöristyssummia käytetään käyttöomaisuuserän poistoprofiilissa, joka sisältää tulevat poistot ja käyttöomaisuuserän arvon, ja lisäksi myös poistoehdotuksissa. Kirjan pienin kirjalle sallittu poisto. 

Viimeisen poistokauden poistosummaa ei määritetystä pyöristyksestä riippumatta pyöristetä. Viimeisen poistokauden lopussa käyttöomaisuuden arvon on oltava 0 (nolla) tai jäännösarvo, jos jäännösarvot ovat käytössä.

### <a name="example"></a>Esimerkki

Poistoksi on laskettu ilman pyöristyksiä 2 444,44. Kuten seuraavasta taulukosta selviää, ehdotetut summat vaihtelevat sen mukaan, miten pyöristys on määritetty.

| Pyöristystapa | Poiston määrä |
|-----------------|---------------------|
| Pyöristys 0,1    | 2 444,40            |
| Pyöristys 1,00   | 2 444,00            |
| Pyöristys 10,00  | 2 440,00            |
| Pyöristys 100,00 | 2 400,00            |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
