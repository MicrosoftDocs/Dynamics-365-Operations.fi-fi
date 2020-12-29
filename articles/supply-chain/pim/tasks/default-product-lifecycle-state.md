---
title: Tuotteen elinkaaren oletustilan luominen
description: Tässä menettelyssä kerrotaan, miten tuotteen elinkaaren oletustila luodaan sekä miten oletustila liitetään julkaistuihin tuotteisiin.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8766208f0dff0cf24db7335ef00c42749811f8fd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427063"
---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="ea990-103">Tuotteen elinkaaren oletustilan luominen</span><span class="sxs-lookup"><span data-stu-id="ea990-103">Create a default product lifecycle state</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ea990-104">Tässä menettelyssä kerrotaan, miten tuotteen elinkaaren oletustila luodaan sekä miten oletustila liitetään julkaistuihin tuotteisiin.</span><span class="sxs-lookup"><span data-stu-id="ea990-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="ea990-105">Elinkaaren oletustilan luominen</span><span class="sxs-lookup"><span data-stu-id="ea990-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="ea990-106">Valitse Tuotetietojen hallinta > Asetukset > Tuotteen elinkaaren tila.</span><span class="sxs-lookup"><span data-stu-id="ea990-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="ea990-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ea990-107">Click New.</span></span>
3. <span data-ttu-id="ea990-108">Kirjoita arvo Tila-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ea990-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="ea990-109">Valitse Oletusarvo vapautettaessa yritykselle -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="ea990-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="ea990-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ea990-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="ea990-111">Valitse On käytettävissä suunnitteluun -kentässä Ei.</span><span class="sxs-lookup"><span data-stu-id="ea990-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="ea990-112">Jos uutta vapautettua tuotetta ei sisällytetä pääsuunnitteluun, valitse Ei.</span><span class="sxs-lookup"><span data-stu-id="ea990-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="ea990-113">Jos se sisällytetään pääsuunnitteluun, älä muuta ohjausobjektin oletusarvoa Kyllä.</span><span class="sxs-lookup"><span data-stu-id="ea990-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="ea990-114">Uuden julkaistun tuotteen luominen</span><span class="sxs-lookup"><span data-stu-id="ea990-114">Create a new released product</span></span>
1. <span data-ttu-id="ea990-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ea990-115">Close the page.</span></span>
2. <span data-ttu-id="ea990-116">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="ea990-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="ea990-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ea990-117">Click New.</span></span>
4. <span data-ttu-id="ea990-118">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ea990-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="ea990-119">Kirjoita arvo Tuotteen nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ea990-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="ea990-120">Kirjoita arvo Hakunimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ea990-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="ea990-121">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ea990-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="ea990-122">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ea990-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="ea990-123">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ea990-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="ea990-124">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ea990-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="ea990-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ea990-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="ea990-126">Tuotteen elinkaaren oletustila on yleinen määritys.</span><span class="sxs-lookup"><span data-stu-id="ea990-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="ea990-127">Tuotteen tilan muuttaminen aktiiviseksi</span><span class="sxs-lookup"><span data-stu-id="ea990-127">Change the product to an active state</span></span>
1. <span data-ttu-id="ea990-128">Syötä tai valitse arvo Tuotteen elinkaaren tila -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ea990-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="ea990-129">Oletetaan, että olet määrittänyt aktiivisen tilan. Voit nyt valita aktiivisen tilan ja sallia tuotteen käyttämisen pääsuunnittelussa ja tuoterakennetason laskennassa.</span><span class="sxs-lookup"><span data-stu-id="ea990-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="ea990-130">Luonnollisesti tämä kannattaa tehdä vain, jos kaikki yhdenmukaisen suunnittelun vaatimat tuotetiedot on määritetty.</span><span class="sxs-lookup"><span data-stu-id="ea990-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  

