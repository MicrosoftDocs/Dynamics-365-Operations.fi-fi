--- 
title: "Luokittele käyttöomaisuus uudelleen"
description: "Voit luokitella käyttöomaisuuserän uudelleen siirtämällä sen uuteen käyttöomaisuusryhmään tai määrittämällä sille uuden samaan ryhmään kuuluvan käyttöomaisuuserän numeron."
author: saraschi2
manager: AnnBe
ms.date: 06/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fda4d71b050edde2752536985b18ebcad203d078
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="118da-103">Luokittele käyttöomaisuus uudelleen</span><span class="sxs-lookup"><span data-stu-id="118da-103">Reclassify fixed assets</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="118da-104">Voit luokitella käyttöomaisuuserän uudelleen siirtämällä sen uuteen käyttöomaisuusryhmään tai määrittämällä sille uuden samaan ryhmään kuuluvan käyttöomaisuuserän numeron.</span><span class="sxs-lookup"><span data-stu-id="118da-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="118da-105">Kun käyttöomaisuuserä luokitellaan uudelleen:</span><span class="sxs-lookup"><span data-stu-id="118da-105">When a fixed asset is reclassified:</span></span>

<span data-ttu-id="118da-106">• Kaikki aiemman käyttöomaisuuserän arvomallit luodaan myös uudelle käyttöomaisuuserälle.</span><span class="sxs-lookup"><span data-stu-id="118da-106">• All value models for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="118da-107">Alkuperäiselle käyttöomaisuuserälle mahdollisesti määritetyt tiedot kopioidaan uuteen käyttöomaisuuserään.</span><span class="sxs-lookup"><span data-stu-id="118da-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="118da-108">Alkuperäisen käyttöomaisuuserän tila on Suljettu.</span><span class="sxs-lookup"><span data-stu-id="118da-108">The status of the value models for the original fixed asset is Closed.</span></span> 

<span data-ttu-id="118da-109">• Uuden käyttöomaisuuserän arvomalleissa on uudelleenluokittelupäivä Hankintapäivämäärä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="118da-109">• The new value models of the new fixed asset contain the date of the reclassification in the Acquisition date field.</span></span> <span data-ttu-id="118da-110">Poiston suorituspäivä -kenttä kopioidaan alkuperäisen käyttöomaisuuden tiedoista.</span><span class="sxs-lookup"><span data-stu-id="118da-110">The date in the Depreciation run date field is copied from the original asset information.</span></span> <span data-ttu-id="118da-111">Jos poistot on jo aloitettu, Viimeisen poiston suorituspäivä -kentässä näkyy uudelleenluokittelun päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="118da-111">If the depreciation has already started, the Date when depreciation was last run field displays the date of the reclassification.</span></span> 

<span data-ttu-id="118da-112">• Alkuperäisen käyttöomaisuuserän aiemmin luodut käyttöomaisuustapahtumat peruutetaan ja luodaan uudelleen uudelle käyttöomaisuuserälle.</span><span class="sxs-lookup"><span data-stu-id="118da-112">• The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

1. <span data-ttu-id="118da-113">Valitse Käyttöomaisuus > Kausittaiset tehtävät > Uudelleenluokittelu.</span><span class="sxs-lookup"><span data-stu-id="118da-113">Go to Fixed assets > Periodic tasks > Reclassification.</span></span>
2. <span data-ttu-id="118da-114">Valitse Käyttöomaisuusryhmä-kentässä uudelleenluokiteltava ryhmä.</span><span class="sxs-lookup"><span data-stu-id="118da-114">In the Fixed asset group field, selet the group to reclassify.</span></span>
3. <span data-ttu-id="118da-115">Valitse Käyttöomaisuuserän numero -kentässä uudelleen luokiteltava käyttöomaisuuserä.</span><span class="sxs-lookup"><span data-stu-id="118da-115">In the Fixed asset number field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="118da-116">Valitse Uusi käyttöomaisuuserä -kentässä ryhmä, johon käyttöomaisuuserä siirretään.</span><span class="sxs-lookup"><span data-stu-id="118da-116">In the New fixed asset group field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="118da-117">Jos uusi käyttöomaisuusryhmä on liitetty numerosarjaan, Uusi käyttöomaisuuserän numero -kenttä päivitetään uuden käyttöomaisuuserän numerosarjan numerolla.</span><span class="sxs-lookup"><span data-stu-id="118da-117">If the new fixed asset group is attached to a number sequence, the New fixed asset number field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="118da-118">Muussa tapauksessa Uusi käyttöomaisuuserän numero -kenttä päivitetään Käyttöomaisuuserien parametrit -sivulla määritetyn numerosarjan numerolla.</span><span class="sxs-lookup"><span data-stu-id="118da-118">Otherwise, the New fixed asset number field is updated with the number from the number sequence that is set up in the Fixed asset parameters page.</span></span> <span data-ttu-id="118da-119">Jos numerosarjaa ei ole määritetty Käyttöomaisuuserien parametrit -sivulla, anna numero Uusi käyttöomaisuuserän numero -kentässä.</span><span class="sxs-lookup"><span data-stu-id="118da-119">If a number sequence is not set up in the Fixed asset parameters page, enter a number in the New fixed asset number field.</span></span>  
5. <span data-ttu-id="118da-120">Anna Uudelleenluokittelupäivä-kentässä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="118da-120">In the Reclassification date field, enter a date.</span></span>
6. <span data-ttu-id="118da-121">Anna tai valitse Tositesarja-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="118da-121">In the Voucher series field, enter or select a value.</span></span>
7. <span data-ttu-id="118da-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="118da-122">Click OK.</span></span>


