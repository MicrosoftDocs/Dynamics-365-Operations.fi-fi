---
title: Tietyt tuotteen elinkaaren tilat sisältävien tuotteiden jättäminen pois
description: Tässä aiheessa käsitellään tuotteiden jättämistä pois elinkaaren tilan perusteella, kun suunnittelun optimointitoiminto on käytössä.
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 02c31aa3862df8dabc2b8c065dc3a94877d237f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992417"
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