---
title: Määritä keskuksen lisämaksut ja lisämaksun päätiedot
description: Tässä menettelyssä kerrotaan, miten keskuksen lisämaksun päätiedot luodaan ja miten päätietoja käytetään keskuksen lisämaksun luomisessa.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad89afe0a21261c57311c439153b969d837748e4
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/29/2020
ms.locfileid: "4427534"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="91060-103">Määritä keskuksen lisämaksut ja lisämaksun päätiedot</span><span class="sxs-lookup"><span data-stu-id="91060-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="91060-104">Tässä menettelyssä kerrotaan, miten keskuksen lisämaksun päätiedot luodaan ja miten päätietoja käytetään keskuksen lisämaksun luomisessa.</span><span class="sxs-lookup"><span data-stu-id="91060-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="91060-105">Menettelyssä käytetään USMF-tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="91060-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="91060-106">Kuljetuskoordinaattori määrittää tämän yleensä.</span><span class="sxs-lookup"><span data-stu-id="91060-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="91060-107">Määritä keskuksen päätietoja</span><span class="sxs-lookup"><span data-stu-id="91060-107">Set up a hub master</span></span>
1. <span data-ttu-id="91060-108">Valitse Kuljetustenhallinta > Asetukset > Luokitus > Lisämaksun päätiedot.</span><span class="sxs-lookup"><span data-stu-id="91060-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="91060-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="91060-109">Click New.</span></span>
3. <span data-ttu-id="91060-110">Kirjoita arvo Lisämaksun päätiedot -kenttään.</span><span class="sxs-lookup"><span data-stu-id="91060-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="91060-111">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="91060-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="91060-112">Valitse Lisämaksun tyyppi -kentässä Keskus.</span><span class="sxs-lookup"><span data-stu-id="91060-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="91060-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="91060-113">Click Save.</span></span>
7. <span data-ttu-id="91060-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="91060-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="91060-115">Keskuksen lisämaksun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="91060-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="91060-116">Valitse Kuljetustenhallinta > Asetukset > Luokitus > Keskuksen lisämaksut.</span><span class="sxs-lookup"><span data-stu-id="91060-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="91060-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="91060-117">Click New.</span></span>
3. <span data-ttu-id="91060-118">Kirjoita Keskuksen lisämaksun tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="91060-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="91060-119">Avaa haku valitsemalla Keskus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="91060-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="91060-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="91060-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="91060-121">Valitse vaihtoehto Keskuksen sijainti -kentässä.</span><span class="sxs-lookup"><span data-stu-id="91060-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="91060-122">Voit luoda joko nouto- tai jättökulun.</span><span class="sxs-lookup"><span data-stu-id="91060-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="91060-123">Kulu kohdistetaan valintaasi vastaavaan kuljetussegmenttiin reitillä.</span><span class="sxs-lookup"><span data-stu-id="91060-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="91060-124">Avaa haku valitsemalla Lisämaksun päätiedot -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="91060-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="91060-125">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="91060-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="91060-126">Valitse juuri luomasi päätiedot.</span><span class="sxs-lookup"><span data-stu-id="91060-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="91060-127">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="91060-127">Click Save.</span></span>
10. <span data-ttu-id="91060-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="91060-128">Close the page.</span></span>

