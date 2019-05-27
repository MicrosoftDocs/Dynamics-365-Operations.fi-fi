---
title: Ylläpidä viivakoodin tyyppejä
description: Tässä menettelyssä käsitellään, miten määritetään uusi viivakoodimääritys, jota voidaan sitten käyttää keräilyluetteloraportin osana.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0d7092228f078f528ec1cb9ac56d7034c44bccf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567880"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="66797-103">Ylläpidä viivakoodin tyyppejä</span><span class="sxs-lookup"><span data-stu-id="66797-103">Maintain barcode types</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="66797-104">Tässä menettelyssä käsitellään, miten määritetään uusi viivakoodimääritys, jota voidaan sitten käyttää keräilyluetteloraportin osana.</span><span class="sxs-lookup"><span data-stu-id="66797-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="66797-105">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="66797-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="66797-106">Jos käytössä on USMF, voit käyttää esimerkiksi esillä olevia arvoja.</span><span class="sxs-lookup"><span data-stu-id="66797-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="66797-107">Yleensä varastopäällikkö tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="66797-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="66797-108">Valitse Viivakoodit.</span><span class="sxs-lookup"><span data-stu-id="66797-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="66797-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="66797-109">Click New.</span></span>
3. <span data-ttu-id="66797-110">Kirjoita Viivakoodiasetukset-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="66797-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="66797-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="66797-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="66797-112">Valitse Viivakoodityyppi-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="66797-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="66797-113">Jos käytössä on USMF, valitse Koodi 39.</span><span class="sxs-lookup"><span data-stu-id="66797-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="66797-114">Lisää Koko-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="66797-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="66797-115">Lisää Enimmäispituus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="66797-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="66797-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="66797-116">Click Save.</span></span>
9. <span data-ttu-id="66797-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="66797-117">Close the page.</span></span>
10. <span data-ttu-id="66797-118">Valitse Varasto ja varastonhallinnan parametrit.</span><span class="sxs-lookup"><span data-stu-id="66797-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="66797-119">Anna tai valitse Viivakoodi-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="66797-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="66797-120">Valitse aiemmin luodut viivakoodiasetukset. Ota kuitenkin huomioon, että viivakoodimuodon on vastattava prosessissa käytetyn tietuetyypin yksilöllistä tunnistetta.</span><span class="sxs-lookup"><span data-stu-id="66797-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="66797-121">Esimerkiksi keräilyreittien viivakoodimuodon on vastattava keräilyreittiviitteen muotoa, joka on yleensä numerosarja.</span><span class="sxs-lookup"><span data-stu-id="66797-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="66797-122">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="66797-122">Click Save.</span></span>
13. <span data-ttu-id="66797-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="66797-123">Close the page.</span></span>

