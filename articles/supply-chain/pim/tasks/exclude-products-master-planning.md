---
title: Tuotteen elinkaaren tason luonti jättämään tuotteita pääsuunnittelun ulkopuolelle
description: Tässä menettelyssä kuvataan, miten luodaan uuden tuotteen elinkaaren tila, joka sulkee pois tuotteet pääsuunnittelusta ja tuoterakennetason laskennasta.
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
ms.openlocfilehash: 5f9573fd220cd8b6a58f81e4d17ca65234f41beb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426932"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="feea1-103">Tuotteen elinkaaren tason luonti jättämään tuotteita pääsuunnittelun ulkopuolelle</span><span class="sxs-lookup"><span data-stu-id="feea1-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="feea1-104">Tässä menettelyssä kuvataan, miten luodaan uuden tuotteen elinkaaren tila, joka sulkee pois tuotteet pääsuunnittelusta ja tuoterakennetason laskennasta.</span><span class="sxs-lookup"><span data-stu-id="feea1-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="feea1-105">Vanhentuneen tilan luominen</span><span class="sxs-lookup"><span data-stu-id="feea1-105">Create an obsolete state</span></span>
1. <span data-ttu-id="feea1-106">Valitse Tuotetietojen hallinta > Asetukset > Tuotteen elinkaaren tila.</span><span class="sxs-lookup"><span data-stu-id="feea1-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="feea1-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="feea1-107">Click New.</span></span>
3. <span data-ttu-id="feea1-108">Kirjoita arvo Tila-kenttään.</span><span class="sxs-lookup"><span data-stu-id="feea1-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="feea1-109">Valitse On käytettävissä suunnitteluun -kentässä Ei.</span><span class="sxs-lookup"><span data-stu-id="feea1-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="feea1-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="feea1-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="feea1-111">Vanhentuneen tilan liittäminen julkaistuun tuotteeseen</span><span class="sxs-lookup"><span data-stu-id="feea1-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="feea1-112">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="feea1-112">Close the page.</span></span>
2. <span data-ttu-id="feea1-113">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="feea1-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="feea1-114">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="feea1-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="feea1-115">Suodata esimerkiksi Haun nimi -kenttä arvolla M00.</span><span class="sxs-lookup"><span data-stu-id="feea1-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="feea1-116">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="feea1-116">Click Edit.</span></span>
5. <span data-ttu-id="feea1-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="feea1-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="feea1-118">Syötä tai valitse arvo Tuotteen elinkaaren tila -kenttään.</span><span class="sxs-lookup"><span data-stu-id="feea1-118">In the Product lifecycle state field, enter or select a value.</span></span>

