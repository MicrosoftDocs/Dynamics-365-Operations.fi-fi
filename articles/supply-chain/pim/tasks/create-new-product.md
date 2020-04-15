---
title: Luo uusi tuote
description: Tässä aiheessa kuvataan, kuinka uusi jaettu tuote luodaan.
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 611fc0cff7fe2d580e971149630e92afd16be228
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147845"
---
# <a name="create-a-new-product"></a><span data-ttu-id="2a25b-103">Luo uusi tuote</span><span class="sxs-lookup"><span data-stu-id="2a25b-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2a25b-104">Tässä aiheessa kuvataan, kuinka uusi jaettu tuote luodaan.</span><span class="sxs-lookup"><span data-stu-id="2a25b-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="2a25b-105">Tehtävän suorittaa yleensä tuotesuunnittelija.</span><span class="sxs-lookup"><span data-stu-id="2a25b-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="2a25b-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="2a25b-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="2a25b-107">Luo tuote</span><span class="sxs-lookup"><span data-stu-id="2a25b-107">Create a product</span></span>
1. <span data-ttu-id="2a25b-108">Valitse siirtymisruudussa **Moduulit > Tuotetietojen hallinta > Tuotteet > Tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="2a25b-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="2a25b-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2a25b-109">Select **New**.</span></span>
3. <span data-ttu-id="2a25b-110">Kirjoita arvo **Tuotenumero**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2a25b-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="2a25b-111">Jos numerosarjaa ei ole määritetty tuotetunnukselle, se on syötettävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="2a25b-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="2a25b-112">Kirjoita arvo **Tuotteen nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2a25b-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="2a25b-113">Tuotenimen oletusarvoksi määritetään hakunimi.</span><span class="sxs-lookup"><span data-stu-id="2a25b-113">The product name defaults to the search name.</span></span> <span data-ttu-id="2a25b-114">Arvoa voi muuttaa tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="2a25b-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="2a25b-115">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a25b-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="2a25b-116">Määritä dimensioryhmät</span><span class="sxs-lookup"><span data-stu-id="2a25b-116">Set up dimension groups</span></span>
1. <span data-ttu-id="2a25b-117">Avaa valintaikkunalomake valitsemalla **Dimensioryhmät**.</span><span class="sxs-lookup"><span data-stu-id="2a25b-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="2a25b-118">Syötä tai valitse arvo **Varastodimensioryhmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="2a25b-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="2a25b-119">Varastodimensioryhmä määrää, mitä varastodimensioita kullekin tuotteen tapahtumalle on syötettävä, ja miten sitä seurataan varastossa.</span><span class="sxs-lookup"><span data-stu-id="2a25b-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="2a25b-120">Syötä tai valitse arvo **Seurantadimensioryhmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="2a25b-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="2a25b-121">Seurantadimensioryhmä määrää, mitä seurantadimensioita kullekin tuotteen tapahtumalle on syötettävä, ja miten sitä käsitellään varastossa.</span><span class="sxs-lookup"><span data-stu-id="2a25b-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="2a25b-122">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a25b-122">Select **OK**.</span></span>

