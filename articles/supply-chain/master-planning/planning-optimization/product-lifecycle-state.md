---
title: Tietyt tuotteen elinkaaren tilat sisältävien tuotteiden jättäminen pois
description: Tässä aiheessa käsitellään tuotteiden jättämistä pois elinkaaren tilan perusteella, kun suunnittelun optimointitoiminto on käytössä.
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7028a509aa884589958542f7ec627d69dffcfcec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839244"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="224d6-103">Tietyt tuotteen elinkaaren tilat sisältävien tuotteiden jättäminen pois</span><span class="sxs-lookup"><span data-stu-id="224d6-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="224d6-104">Vapautetut tuotteet ja vapautetut tuoteversiot sisältävät **Tuotteen elinkaaren tila** -kentän.</span><span class="sxs-lookup"><span data-stu-id="224d6-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="224d6-105">Tämän kentän avulla voi hallita esimerkiksi, mitä tuotteita sisällytetään pääsuunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="224d6-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="224d6-106">Voit lisätä, poistaa ja muokata elinkaaren tiloja tarvittaessa valitsemalla **Tuotetietojen hallinta \> Määritys \> Tuotteen elinkaaren tila**.</span><span class="sxs-lookup"><span data-stu-id="224d6-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="224d6-107">Määritä kunkin tuotteen elinkaaren tilan **On käytettävissä suunnitteluun** -asetukseksi *Kyllä*, jos tuotteella on tila, joka on sisällytettävä pääsuunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="224d6-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="224d6-108">Kun vaihtoehdon määrityksenä *Ei*, liitetyt tuotteet ja variantit jätetään pois kaikesta pääsuunnittelusta ja kaikista laskelmista tuoterakennetasolla.</span><span class="sxs-lookup"><span data-stu-id="224d6-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="224d6-109">Vapautettuja tuotteita ja variantteja, joiden **Tuotteen elinkaaren tila** -kenttä jätetään tyhjäksi, käsitellään aivan kuin niiden tuotteen elinkaaren tilan **On käytettävissä suunnitteluun** -asetuksena olisi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="224d6-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="224d6-110">Ne siis sisällytetään pääsuunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="224d6-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="224d6-111">Tarpeettomia toimitusehdotuksia voidaan välttää, kun kaikkiin vanhentuneisiin vapautettuihin tuotteisiin ja variantteihin liitetään tuotteen elinkaaren tila siten, että **On käytettävissä suunnitteluun** -asetuksena on *Ei*.</span><span class="sxs-lookup"><span data-stu-id="224d6-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="224d6-112">Tämä on erityisen tärkeää, kun käytössä on tuotemääritysvariantteja, joita ei voi käyttää uudelleen, sillä se auttaa estämään hävikkiä.</span><span class="sxs-lookup"><span data-stu-id="224d6-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="224d6-113">Liittyvät resurssit</span><span class="sxs-lookup"><span data-stu-id="224d6-113">Related resources</span></span>

<span data-ttu-id="224d6-114">Lisätietoja tuotteen elinkaaren tilasta on kohdassa [Tuotteen elinkaaren tilan yleiskatsaus](../../pim/product-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="224d6-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="224d6-115">Lisätietoja vaiheista, joilla tuotteen elinkaaren tiloja voidaan käyttää tuotteiden poisjättämiseen pääsuunnittelusta ja tuoterakennetason laskelmista [Tuotteen elinkaaren tilan luonti jättämään tuotteita pääsuunnittelun ulkopuolelle](../../pim/tasks/exclude-products-master-planning.md).</span><span class="sxs-lookup"><span data-stu-id="224d6-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]