---
title: Monitasoiset resurssit
description: Tässä ohjeaiheessa kerrotaan, kuinka voit luoda ja poistaa monitasoisia resursseja.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c2a4052f9beca554932d7f2547288e02358b603
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571504"
---
# <a name="multi-level-assets"></a><span data-ttu-id="c17b9-103">Monitasoiset resurssit</span><span class="sxs-lookup"><span data-stu-id="c17b9-103">Multi-level assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c17b9-104">Tässä ohjeaiheessa kerrotaan, kuinka voit luoda ja poistaa monitasoisia resursseja.</span><span class="sxs-lookup"><span data-stu-id="c17b9-104">This topic explains how to create and delete multi-level assets.</span></span> <span data-ttu-id="c17b9-105">Voit luoda resursseja ja niihin liittyviä alaresursseja hierarkkisessa puurakenteessa.</span><span class="sxs-lookup"><span data-stu-id="c17b9-105">You can create assets and related sub-assets in a hierarchical tree structure.</span></span> <span data-ttu-id="c17b9-106">Näin voit näyttää suhteet ja riippuvuudet resurssien välillä.</span><span class="sxs-lookup"><span data-stu-id="c17b9-106">In this way, you can show relations and dependencies among assets.</span></span> <span data-ttu-id="c17b9-107">Ylläpitotöitä voidaan liittää kaikkiin puurakenteen tasoihin.</span><span class="sxs-lookup"><span data-stu-id="c17b9-107">Maintenance jobs can be related to all levels of the tree structure.</span></span> <span data-ttu-id="c17b9-108">Tilastoja voidaan luoda myös yksittäiselle tasolle tai kaikkien aliresurssitasojen summana.</span><span class="sxs-lookup"><span data-stu-id="c17b9-108">Statistics can also be created for an individual level or as a sum of all sub-asset levels.</span></span>

<span data-ttu-id="c17b9-109">**Kaikki resurssit** -luettelosivun (**Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit**) **Resurssi**-sarakkeessa on resurssit hirarkkisessa jäsjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="c17b9-109">On the **All Assets** list page (**Asset management** \> **Common** \> **Assets** \> **All assets**), the **Asset** column lists assets in hierarchical order.</span></span> <span data-ttu-id="c17b9-110">**Ylätaso**-sarakkeessa näkyy liittyvä ylätaso.</span><span class="sxs-lookup"><span data-stu-id="c17b9-110">The **Parent** column shows the related parent.</span></span> <span data-ttu-id="c17b9-111">Lisäksi jos resurssit ja aliresurssit on jo luotu,**Liittyvät tiedot** -ruudun **Resurssipuu**-osassa näkyvät resurssit puurakenteessa.</span><span class="sxs-lookup"><span data-stu-id="c17b9-111">Additionally, if assets and sub-assets have already been created, the **Asset tree** section in the **Related information** pane shows the assets in a tree structure.</span></span>

<span data-ttu-id="c17b9-112">Lisä tietoja resurssien luomisesta on kohdassa [Resurssin luominen](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="c17b9-112">For information about how to create an asset, see [Create an asset](../objects/create-an-object.md).</span></span> <span data-ttu-id="c17b9-113">Jos haluat luoda aliresurssin, valitse ylätason resurssi **Ylätaso**-kentässä **Yleiset**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="c17b9-113">To create a sub-asset, select the parent asset in the **Parent** field on the **General** FastTab.</span></span>

## <a name="copy-an-asset-or-asset-structure"></a><span data-ttu-id="c17b9-114">Kopioi resurssi tai resurssirakenne</span><span class="sxs-lookup"><span data-stu-id="c17b9-114">Copy an asset or asset structure</span></span>

<span data-ttu-id="c17b9-115">Jos yritykselläsi on useita samankaltaisia resurssirakenteita, voit luoda ne nopeasti käyttämällä resurssien hallinnan Kopioi-toimintoa.</span><span class="sxs-lookup"><span data-stu-id="c17b9-115">If your company has several similar asset structures, you can use the Copy function in Asset Management to quickly create them.</span></span>

1. <span data-ttu-id="c17b9-116">Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit**.</span><span class="sxs-lookup"><span data-stu-id="c17b9-116">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="c17b9-117">Valitse **Kaikki resurssit** -luettelosivulla kopioitava resurssi.</span><span class="sxs-lookup"><span data-stu-id="c17b9-117">On the **All assets** list page, select the asset to copy.</span></span> <span data-ttu-id="c17b9-118">Jos esimerkiksi haluat kopioida koko resurssirakenteen, mukaan lukien aliresurssit, valitse ylätason resurssi.</span><span class="sxs-lookup"><span data-stu-id="c17b9-118">For example, if you want to copy the whole asset structure, including sub-assets, select a parent asset.</span></span>
3. <span data-ttu-id="c17b9-119">Valitse **Kopioi resurssi**.</span><span class="sxs-lookup"><span data-stu-id="c17b9-119">Select **Copy asset**.</span></span> <span data-ttu-id="c17b9-120">**Kopioi kohteesta**-osassa **Resurssi**-kentän arvoksi on valittu resurssi, jonka valitsit luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="c17b9-120">In the **Copy from** section, the **Asset** field is set to the asset that you selected on the list page.</span></span>
4. <span data-ttu-id="c17b9-121">Kirjoita **Kopioi kohteeseen** -osassa **Resurssi**-kenttään uuden resurssin nimi.</span><span class="sxs-lookup"><span data-stu-id="c17b9-121">In the **Copy to** section, in the **Asset** field, enter the name of the new asset.</span></span>
5. <span data-ttu-id="c17b9-122">Jos luotavalla resurssin on oltava osa aiemmin luotua resurssirakennetta, valitse **Ylätason resurssi** -osan **Resurssi** -kentässä ylätason tunnus.</span><span class="sxs-lookup"><span data-stu-id="c17b9-122">If the asset that you're creating should be part of an existing asset structure, in the **Parent asset** section, in the **Asset** field, select a parent ID.</span></span>
6. <span data-ttu-id="c17b9-123">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="c17b9-123">Select **OK**.</span></span> <span data-ttu-id="c17b9-124">Uusi resurssirakenne näkyy **Kaikki resurssit** -luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="c17b9-124">The new asset structure is shown on the **All assets** list page.</span></span> <span data-ttu-id="c17b9-125">Kaikki resurssin määritteet, ylläpitosuunnitelmat ja kunnossapitokierrokset, jotka liittyvät kopioimaasi resurssiin, siirretään uuteen resurssiin tai resurssirakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="c17b9-125">All asset attributes, maintenance plans, and maintenance rounds that are related to the asset that you copied are transferred to the new asset or asset structure.</span></span>

<span data-ttu-id="c17b9-126">Kun kopioit resurssirakenteen, uuden rakenteen alivresursseilla on sama nimi kuin kopioimillasi aliresursseilla.</span><span class="sxs-lookup"><span data-stu-id="c17b9-126">When you copy an asset structure, the sub-assets in the new structure have the same name as the sub-assets that you copied.</span></span> <span data-ttu-id="c17b9-127">Kun kopiointitoiminto on valmis, voit helposti muuttaa resurssin nimeä ja muita asetuksia.</span><span class="sxs-lookup"><span data-stu-id="c17b9-127">After the copy procedure is completed, you can easily change the name and other settings for an asset.</span></span> <span data-ttu-id="c17b9-128">Valitse resurssi **Kaikki resurssit** -luettelosivulla ja valitse sitten **Muokkaa**-painike.</span><span class="sxs-lookup"><span data-stu-id="c17b9-128">Select the asset on the **All assets** list page, and then select the **Edit** button.</span></span>

> [!NOTE]
> <span data-ttu-id="c17b9-129">Kun kopioit resurssin tai resurssirakenteen, uusien resurssien elinkaaritila palautetaan mihin tahansa tilaan, jonka olet määrittänyt resurssien elinkaaren alkutilaksi.</span><span class="sxs-lookup"><span data-stu-id="c17b9-129">When you copy an asset or asset structure, the lifecycle state of the new assets is reset to whatever state you defined as the initial lifecycle state for assets.</span></span> <span data-ttu-id="c17b9-130">Toiminnallinen sijainti palautetaan oletusarvoiseen toiminnalliseen sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="c17b9-130">The functional location is reset to the default functional location.</span></span>

## <a name="delete-an-asset-or-asset-structure"></a><span data-ttu-id="c17b9-131">Poista resurssi tai resurssirakenne</span><span class="sxs-lookup"><span data-stu-id="c17b9-131">Delete an asset or asset structure</span></span>

<span data-ttu-id="c17b9-132">Jos resurssiin liittyy alaresursseja, voit poistaa sen vain, jos mihinkään resurssiin ei ole rekisteröity ylläpitopyyntöjä, työtilaustöitä, vikarekisteröintejä tai kunnon arviointeja.</span><span class="sxs-lookup"><span data-stu-id="c17b9-132">If an asset has related sub-assets, you can delete it only if no maintenance requests, work order jobs, fault registrations, or condition assessments are registered on any of the assets.</span></span>

1. <span data-ttu-id="c17b9-133">Valitse **Kaikki resurssit** -luettelosivulla poistettava resurssi.</span><span class="sxs-lookup"><span data-stu-id="c17b9-133">On the **All assets** list page, select the asset to delete.</span></span>
2. <span data-ttu-id="c17b9-134">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="c17b9-134">Select **Delete**.</span></span>

> [!NOTE]
> <span data-ttu-id="c17b9-135">Jos et voi poistaa resurssia tämän menettelyn avulla, toinen tapa käsitellä poistoa on määrittää resurssin elinkaaren tila tätä tarkoitusta varten.</span><span class="sxs-lookup"><span data-stu-id="c17b9-135">If you can't delete an asset by using this procedure, another way to handle deletion is to set up an asset lifecycle state for this purpose.</span></span> <span data-ttu-id="c17b9-136">Voit esimerkiksi määrittää elinkaareen **Hävikki**- tai **Poistettu**-tilan **Resurssien elinkaaritilat** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c17b9-136">For example, you can set up a **Scrapped** or **Deleted** lifecycle state on the **Asset lifecycle states** page.</span></span>
