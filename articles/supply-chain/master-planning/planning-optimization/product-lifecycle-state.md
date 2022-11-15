---
title: Tietyt tuotteen elinkaaren tilat sisältävien tuotteiden jättäminen pois
description: Tässä artikkelissa kerrotaan, miten tuotteita voidaan jättää pois niiden elinkaaren tilan perusteella.
author: t-benebo
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 647e2cf4f14dbdfc3e7f04f43dcbd7115f19e8dc
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740762"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a>Tietyt tuotteen elinkaaren tilat sisältävien tuotteiden jättäminen pois

[!include [banner](../../includes/banner.md)]

Vapautetut tuotteet ja vapautetut tuoteversiot sisältävät **Tuotteen elinkaaren tila** -kentän. Tämän kentän avulla voi hallita esimerkiksi, mitä tuotteita sisällytetään pääsuunnittelun aikana. Voit lisätä, poistaa ja muokata elinkaaren tiloja tarvittaessa valitsemalla **Tuotetietojen hallinta \> Määritys \> Tuotteen elinkaaren tila**. Määritä kunkin tuotteen elinkaaren tilan **On käytettävissä suunnitteluun** -asetukseksi *Kyllä*, jos tuotteella on tila, joka on sisällytettävä pääsuunnittelun aikana. Kun vaihtoehdon määrityksenä *Ei*, liitetyt tuotteet ja variantit jätetään pois kaikesta pääsuunnittelusta ja kaikista laskelmista tuoterakennetasolla.

Vapautettuja tuotteita ja variantteja, joiden **Tuotteen elinkaaren tila** -kenttä jätetään tyhjäksi, käsitellään aivan kuin niiden tuotteen elinkaaren tilan **On käytettävissä suunnitteluun** -asetuksena olisi *Kyllä*. Ne siis sisällytetään pääsuunnitteluun.

> [!NOTE]
> Tarpeettomia toimitusehdotuksia voidaan välttää, kun kaikkiin vanhentuneisiin vapautettuihin tuotteisiin ja variantteihin liitetään tuotteen elinkaaren tila siten, että **On käytettävissä suunnitteluun** -asetuksena on *Ei*. Tämä on erityisen tärkeää, kun käytössä on tuotemääritysvariantteja, joita ei voi käyttää uudelleen, sillä se auttaa estämään hävikkiä.

## <a name="related-resources"></a>Liittyvät resurssit

Lisätietoja tuotteen elinkaaren tilasta on kohdassa [Tuotteen elinkaaren tilan yleiskatsaus](../../pim/product-lifecycle.md).

Lisätietoja vaiheista, joilla tuotteen elinkaaren tiloja voidaan käyttää tuotteiden poisjättämiseen pääsuunnittelusta ja tuoterakennetason laskelmista [Tuotteen elinkaaren tilan luonti jättämään tuotteita pääsuunnittelun ulkopuolelle](../../pim/tasks/exclude-products-master-planning.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]