---
title: "Ylläpidä viivakoodityyppejä"
description: "Tässä menettelyssä käsitellään, miten määritetään uusi viivakoodimääritys, jota voidaan sitten käyttää keräilyluetteloraportin osana."
author: perlynne
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 45323206550d1b0ed66d89f4be7b995c60af63fc
ms.contentlocale: fi-fi
ms.lasthandoff: 09/12/2017

---
# <a name="maintain-bar-code-types"></a><span data-ttu-id="ea0c7-103">Ylläpidä viivakoodityyppejä</span><span class="sxs-lookup"><span data-stu-id="ea0c7-103">Maintain bar code types</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ea0c7-104">Tässä menettelyssä käsitellään, miten määritetään uusi viivakoodimääritys, jota voidaan sitten käyttää keräilyluetteloraportin osana.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="ea0c7-105">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="ea0c7-106">Jos käytössä on USMF, voit käyttää esimerkiksi esillä olevia arvoja.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="ea0c7-107">Yleensä varastopäällikkö tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="ea0c7-108">Valitse Viivakoodit.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="ea0c7-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-109">Click New.</span></span>
3. <span data-ttu-id="ea0c7-110">Kirjoita Viivakoodiasetukset-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="ea0c7-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ea0c7-112">Valitse Viivakoodityyppi-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="ea0c7-113">Jos käytössä on USMF, valitse Koodi 39.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="ea0c7-114">Lisää Koko-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="ea0c7-115">Lisää Enimmäispituus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="ea0c7-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-116">Click Save.</span></span>
9. <span data-ttu-id="ea0c7-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-117">Close the page.</span></span>
10. <span data-ttu-id="ea0c7-118">Valitse Varasto ja varastonhallinnan parametrit.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="ea0c7-119">Anna tai valitse Viivakoodi-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="ea0c7-120">Valitse aiemmin luodut viivakoodiasetukset. Ota kuitenkin huomioon, että viivakoodimuodon on vastattava prosessissa käytetyn tietuetyypin yksilöllistä tunnistetta.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="ea0c7-121">Esimerkiksi keräilyreittien viivakoodimuodon on vastattava keräilyreittiviitteen muotoa, joka on yleensä numerosarja.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="ea0c7-122">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-122">Click Save.</span></span>
13. <span data-ttu-id="ea0c7-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-123">Close the page.</span></span>

