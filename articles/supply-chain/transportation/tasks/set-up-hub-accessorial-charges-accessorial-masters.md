--- 
title: "Määritä keskuksen lisämaksut ja lisämaksun päätiedot"
description: "Tässä menettelyssä kerrotaan, miten keskuksen lisämaksun päätiedot luodaan ja miten päätietoja käytetään keskuksen lisämaksun luomisessa."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 61a506b3824fa220d052ca667199edac526c1cbc
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="3013e-103">Määritä keskuksen lisämaksut ja lisämaksun päätiedot</span><span class="sxs-lookup"><span data-stu-id="3013e-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3013e-104">Tässä menettelyssä kerrotaan, miten keskuksen lisämaksun päätiedot luodaan ja miten päätietoja käytetään keskuksen lisämaksun luomisessa.</span><span class="sxs-lookup"><span data-stu-id="3013e-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="3013e-105">Menettelyssä käytetään USMF-tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="3013e-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="3013e-106">Kuljetuskoordinaattori määrittää tämän yleensä.</span><span class="sxs-lookup"><span data-stu-id="3013e-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="3013e-107">Määritä keskuksen päätietoja</span><span class="sxs-lookup"><span data-stu-id="3013e-107">Set up a hub master</span></span>
1. <span data-ttu-id="3013e-108">Valitse Kuljetustenhallinta > Asetukset > Luokitus > Lisämaksun päätiedot.</span><span class="sxs-lookup"><span data-stu-id="3013e-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="3013e-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3013e-109">Click New.</span></span>
3. <span data-ttu-id="3013e-110">Kirjoita arvo Lisämaksun päätiedot -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3013e-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="3013e-111">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3013e-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3013e-112">Valitse Lisämaksun tyyppi -kentässä Keskus.</span><span class="sxs-lookup"><span data-stu-id="3013e-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="3013e-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3013e-113">Click Save.</span></span>
7. <span data-ttu-id="3013e-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3013e-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="3013e-115">Keskuksen lisämaksun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3013e-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="3013e-116">Valitse Kuljetustenhallinta > Asetukset > Luokitus > Keskuksen lisämaksut.</span><span class="sxs-lookup"><span data-stu-id="3013e-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="3013e-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3013e-117">Click New.</span></span>
3. <span data-ttu-id="3013e-118">Kirjoita Keskuksen lisämaksun tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="3013e-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="3013e-119">Avaa haku valitsemalla Keskus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="3013e-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3013e-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="3013e-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="3013e-121">Valitse vaihtoehto Keskuksen sijainti -kentässä.</span><span class="sxs-lookup"><span data-stu-id="3013e-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="3013e-122">Voit luoda joko nouto- tai jättökulun.</span><span class="sxs-lookup"><span data-stu-id="3013e-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="3013e-123">Kulu kohdistetaan valintaasi vastaavaan kuljetussegmenttiin reitillä.</span><span class="sxs-lookup"><span data-stu-id="3013e-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="3013e-124">Avaa haku valitsemalla Lisämaksun päätiedot -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="3013e-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="3013e-125">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3013e-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3013e-126">Valitse juuri luomasi päätiedot.</span><span class="sxs-lookup"><span data-stu-id="3013e-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="3013e-127">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3013e-127">Click Save.</span></span>
10. <span data-ttu-id="3013e-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3013e-128">Close the page.</span></span>


