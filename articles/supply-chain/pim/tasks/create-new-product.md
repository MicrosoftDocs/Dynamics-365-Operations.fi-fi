---
title: Luo uusi tuote
description: Tässä tehtävässä esitellään uuden jaetun tuotteen luominen.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a603d89749242a4c6039ab83da286ec6ab727d8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "328536"
---
# <a name="create-a-new-product"></a><span data-ttu-id="a993a-103">Luo uusi tuote</span><span class="sxs-lookup"><span data-stu-id="a993a-103">Create a new product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a993a-104">Tässä tehtävässä esitellään uuden jaetun tuotteen luominen.</span><span class="sxs-lookup"><span data-stu-id="a993a-104">This task shows how to create a new shared product.</span></span> <span data-ttu-id="a993a-105">Tehtävän suorittaa yleensä tuotesuunnittelija.</span><span class="sxs-lookup"><span data-stu-id="a993a-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="a993a-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="a993a-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="a993a-107">Valitse Tuotetietojen hallinta > Tuotteet > Tuotteet.</span><span class="sxs-lookup"><span data-stu-id="a993a-107">Go to Product information management > Products > Products.</span></span>

## <a name="create-a-product"></a><span data-ttu-id="a993a-108">Luo tuote</span><span class="sxs-lookup"><span data-stu-id="a993a-108">Create a product</span></span>
1. <span data-ttu-id="a993a-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a993a-109">Click New.</span></span>
2. <span data-ttu-id="a993a-110">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a993a-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="a993a-111">Jos numerosarjaa ei ole määritetty tuotetunnukselle, se on syötettävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="a993a-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
3. <span data-ttu-id="a993a-112">Kirjoita arvo Tuotteen nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="a993a-112">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="a993a-113">Tuotenimen oletusarvoksi määritetään hakunimi.</span><span class="sxs-lookup"><span data-stu-id="a993a-113">The product name defaults to the search name.</span></span> <span data-ttu-id="a993a-114">Arvoa voi muuttaa tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="a993a-114">You can change this if needed.</span></span>  
4. <span data-ttu-id="a993a-115">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a993a-115">Click OK.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="a993a-116">Määritä dimensioryhmät</span><span class="sxs-lookup"><span data-stu-id="a993a-116">Set up dimension groups</span></span>
1. <span data-ttu-id="a993a-117">Avaa valintaikkunalomake valitsemalla Dimensioryhmät.</span><span class="sxs-lookup"><span data-stu-id="a993a-117">Click Dimension groups to open the drop dialog.</span></span>
2. <span data-ttu-id="a993a-118">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a993a-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="a993a-119">Varastodimensioryhmä määrää, mitä varastodimensioita kullekin tuotteen tapahtumalle on syötettävä, ja miten sitä seurataan varastossa.</span><span class="sxs-lookup"><span data-stu-id="a993a-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="a993a-120">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a993a-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="a993a-121">Seurantadimensioryhmä määrää, mitä seurantadimensioita kullekin tuotteen tapahtumalle on syötettävä, ja miten sitä käsitellään varastossa.</span><span class="sxs-lookup"><span data-stu-id="a993a-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="a993a-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a993a-122">Click OK.</span></span>

