---
title: Luokittele käyttöomaisuus uudelleen
description: Voit luokitella käyttöomaisuuserän uudelleen siirtämällä sen uuteen käyttöomaisuusryhmään tai määrittämällä sille uuden samaan ryhmään kuuluvan käyttöomaisuuserän numeron.
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47d8cf2ff1e275df0466a7fe327a3180c0399e49
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186920"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="93bb6-103">Luokittele käyttöomaisuus uudelleen</span><span class="sxs-lookup"><span data-stu-id="93bb6-103">Reclassify fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="93bb6-104">Voit luokitella käyttöomaisuuserän uudelleen siirtämällä sen uuteen käyttöomaisuusryhmään tai määrittämällä sille uuden samaan ryhmään kuuluvan käyttöomaisuuserän numeron.</span><span class="sxs-lookup"><span data-stu-id="93bb6-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="93bb6-105">Kun käyttöomaisuuserä luokitellaan uudelleen:</span><span class="sxs-lookup"><span data-stu-id="93bb6-105">When a fixed asset is reclassified:</span></span>

<span data-ttu-id="93bb6-106">• Kaikki aiemman käyttöomaisuuserän kirjat luodaan myös uudelle käyttöomaisuuserälle.</span><span class="sxs-lookup"><span data-stu-id="93bb6-106">• All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="93bb6-107">Alkuperäiselle käyttöomaisuuserälle mahdollisesti määritetyt tiedot kopioidaan uuteen käyttöomaisuuserään.</span><span class="sxs-lookup"><span data-stu-id="93bb6-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="93bb6-108">Alkuperäisen käyttöomaisuuserän kirjojen tila on Suljettu.</span><span class="sxs-lookup"><span data-stu-id="93bb6-108">The status of the books for the original fixed asset is Closed.</span></span> 

<span data-ttu-id="93bb6-109">• Uuden käyttöomaisuuserän kirjoissa on uudelleenluokittelupäivä **Hankintapäivämäärä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="93bb6-109">• The new books of the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="93bb6-110">**Poiston suorituspäivä** -kenttä kopioidaan alkuperäisen käyttöomaisuuden tiedoista.</span><span class="sxs-lookup"><span data-stu-id="93bb6-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="93bb6-111">Jos poistot on jo aloitettu, **Viimeisen poiston suorituspäivä** -kentässä näkyy uudelleenluokittelun päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="93bb6-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

<span data-ttu-id="93bb6-112">• Alkuperäisen käyttöomaisuuserän aiemmin luodut käyttöomaisuustapahtumat peruutetaan ja luodaan uudelleen uudelle käyttöomaisuuserälle.</span><span class="sxs-lookup"><span data-stu-id="93bb6-112">• The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

<span data-ttu-id="93bb6-113">Luokittele käyttöomaisuuserä uudelleen noudattamalla seuraavia vaiheita:</span><span class="sxs-lookup"><span data-stu-id="93bb6-113">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="93bb6-114">Valitse **Käyttöomaisuus > Kausittaiset tehtävät > Uudelleenluokittelu.**</span><span class="sxs-lookup"><span data-stu-id="93bb6-114">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="93bb6-115">Valitse **Käyttöomaisuusryhmä**-kentässä uudelleenluokiteltava ryhmä.</span><span class="sxs-lookup"><span data-stu-id="93bb6-115">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="93bb6-116">Valitse **Käyttöomaisuuserän numero** -kentässä uudelleen luokiteltava käyttöomaisuuserä.</span><span class="sxs-lookup"><span data-stu-id="93bb6-116">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="93bb6-117">Valitse **Uusi käyttöomaisuuserä** -kentässä ryhmä, johon käyttöomaisuuserä siirretään.</span><span class="sxs-lookup"><span data-stu-id="93bb6-117">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="93bb6-118">Jos uusi käyttöomaisuusryhmä on liitetty numerosarjaan, **Uusi käyttöomaisuuserän numero** -kenttä päivitetään uuden käyttöomaisuuserän numerosarjan numerolla.</span><span class="sxs-lookup"><span data-stu-id="93bb6-118">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="93bb6-119">Muussa tapauksessa **Uusi käyttöomaisuuserän numero** -kenttä päivitetään **Käyttöomaisuuserien parametrit** -sivulla määritetyn numerosarjan numerolla.</span><span class="sxs-lookup"><span data-stu-id="93bb6-119">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="93bb6-120">Jos numerosarjaa ei ole määritetty **Käyttöomaisuuserien parametrit** -sivulla, anna numero **Uusi käyttöomaisuuserän numero** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="93bb6-120">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="93bb6-121">Anna **Uudelleenluokittelupäivä** -kentässä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="93bb6-121">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="93bb6-122">Anna tai valitse **Tositesarja**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="93bb6-122">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="93bb6-123">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="93bb6-123">Click **OK**.</span></span>