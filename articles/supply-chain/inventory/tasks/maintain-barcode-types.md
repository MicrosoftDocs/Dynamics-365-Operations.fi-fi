---
title: Ylläpidä viivakoodin tyyppejä
description: Tässä menettelyssä käsitellään, miten määritetään uusi viivakoodimääritys, jota voidaan sitten käyttää keräilyluetteloraportin osana.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 112438417e425b8b77dd56f25e0b6e6db21c5148
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244396"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="7fff2-103">Ylläpidä viivakoodin tyyppejä</span><span class="sxs-lookup"><span data-stu-id="7fff2-103">Maintain barcode types</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7fff2-104">Tässä menettelyssä käsitellään, miten määritetään uusi viivakoodimääritys, jota voidaan sitten käyttää keräilyluetteloraportin osana.</span><span class="sxs-lookup"><span data-stu-id="7fff2-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="7fff2-105">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="7fff2-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="7fff2-106">Jos käytössä on USMF, voit käyttää esimerkiksi esillä olevia arvoja.</span><span class="sxs-lookup"><span data-stu-id="7fff2-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="7fff2-107">Yleensä varastopäällikkö tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="7fff2-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="7fff2-108">Valitse Viivakoodit.</span><span class="sxs-lookup"><span data-stu-id="7fff2-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="7fff2-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7fff2-109">Click New.</span></span>
3. <span data-ttu-id="7fff2-110">Kirjoita Viivakoodiasetukset-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7fff2-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="7fff2-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7fff2-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7fff2-112">Valitse Viivakoodityyppi-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="7fff2-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="7fff2-113">Jos käytössä on USMF, valitse Koodi 39.</span><span class="sxs-lookup"><span data-stu-id="7fff2-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="7fff2-114">Lisää Koko-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="7fff2-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="7fff2-115">Lisää Enimmäispituus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="7fff2-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="7fff2-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7fff2-116">Click Save.</span></span>
9. <span data-ttu-id="7fff2-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7fff2-117">Close the page.</span></span>
10. <span data-ttu-id="7fff2-118">Valitse Varasto ja varastonhallinnan parametrit.</span><span class="sxs-lookup"><span data-stu-id="7fff2-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="7fff2-119">Anna tai valitse Viivakoodi-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="7fff2-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="7fff2-120">Valitse aiemmin luodut viivakoodiasetukset. Ota kuitenkin huomioon, että viivakoodimuodon on vastattava prosessissa käytetyn tietuetyypin yksilöllistä tunnistetta.</span><span class="sxs-lookup"><span data-stu-id="7fff2-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="7fff2-121">Esimerkiksi keräilyreittien viivakoodimuodon on vastattava keräilyreittiviitteen muotoa, joka on yleensä numerosarja.</span><span class="sxs-lookup"><span data-stu-id="7fff2-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="7fff2-122">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7fff2-122">Click Save.</span></span>
13. <span data-ttu-id="7fff2-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7fff2-123">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]