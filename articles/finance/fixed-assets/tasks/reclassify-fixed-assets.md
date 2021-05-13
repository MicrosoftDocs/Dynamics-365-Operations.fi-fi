---
title: Luokittele käyttöomaisuus uudelleen
description: Voit luokitella käyttöomaisuuserän uudelleen siirtämällä sen uuteen käyttöomaisuusryhmään tai määrittämällä sille uuden samaan ryhmään kuuluvan käyttöomaisuuserän numeron.
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbfb754459fad1f3b1509f4f9c65c20e0385b013
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944709"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="b316e-103">Luokittele käyttöomaisuus uudelleen</span><span class="sxs-lookup"><span data-stu-id="b316e-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b316e-104">Voit luokitella käyttöomaisuuserän uudelleen siirtämällä sen uuteen käyttöomaisuusryhmään tai määrittämällä sille uuden samaan ryhmään kuuluvan käyttöomaisuuserän numeron.</span><span class="sxs-lookup"><span data-stu-id="b316e-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="b316e-105">Kun käyttöomaisuuserä luokitellaan uudelleen:</span><span class="sxs-lookup"><span data-stu-id="b316e-105">When a fixed asset is reclassified:</span></span>

- <span data-ttu-id="b316e-106">Kaikki aiemman käyttöomaisuuserän kirjat luodaan myös uudelle käyttöomaisuuserälle.</span><span class="sxs-lookup"><span data-stu-id="b316e-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="b316e-107">Alkuperäiselle käyttöomaisuuserälle mahdollisesti määritetyt tiedot kopioidaan uuteen käyttöomaisuuserään.</span><span class="sxs-lookup"><span data-stu-id="b316e-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="b316e-108">Alkuperäisen käyttöomaisuuserän kirjojen tila on Suljettu.</span><span class="sxs-lookup"><span data-stu-id="b316e-108">The status of the books for the original fixed asset is Closed.</span></span> 

- <span data-ttu-id="b316e-109">Uuden käyttöomaisuuserän kirjoissa on uudelleenluokittelupäivä **Hankintapäivämäärä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b316e-109">The new books for the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="b316e-110">**Poiston suorituspäivä** -kenttä kopioidaan alkuperäisen käyttöomaisuuden tiedoista.</span><span class="sxs-lookup"><span data-stu-id="b316e-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="b316e-111">Jos poistot on jo aloitettu, **Viimeisen poiston suorituspäivä** -kentässä näkyy uudelleenluokittelun päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="b316e-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

- <span data-ttu-id="b316e-112">Alkuperäisen käyttöomaisuuserän aiemmin luodut käyttöomaisuustapahtumat peruutetaan ja luodaan uudelleen uudelle käyttöomaisuuserälle.</span><span class="sxs-lookup"><span data-stu-id="b316e-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

- <span data-ttu-id="b316e-113">Kun käyttöomaisuuserä, jolla on siirtotapahtuma, on luokiteltu uudelleen, järjestelmä näyttää **toimintokeskuksessa** sanoman, jossa ilmoitetaan, ettei siirtotapahtumaa ole suoritettu uudelleenluokitteluprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="b316e-113">When an asset that has a transfer transaction has been reclassified, the system will display a message in the **Action center** to indicate that a transfer transaction wasn't completed during the reclassification process.</span></span> <span data-ttu-id="b316e-114">Siirtotapahtuma on suoritettava valmiiksi, jotta olemassa olevat uudelleenluokittelutapahtumat voidaan siirtää asianmukaisiin taloushallinnon dimensioihin.</span><span class="sxs-lookup"><span data-stu-id="b316e-114">It's necessary to complete a transfer transaction to move the existing reclassification transactions to the appropriate financial dimensions.</span></span> 

   <span data-ttu-id="b316e-115">Uudelleenluokittelun aikana järjestelmä luokittelee käyttöomaisuussaldon alkuperäisestä käyttöomaisuuserästä uuteen käyttöomaisuuserään uudelleen seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b316e-115">During the reclassification process, the system runs the following actions to reclassify the asset balance from the original asset to the new asset.</span></span> 
   
   - <span data-ttu-id="b316e-116">Uudelleenluokitteluprosessi kopioi tiedot alkuperäisestä käyttöomaisuuskirjasta uuteen käyttöomaisuuskirjaan.</span><span class="sxs-lookup"><span data-stu-id="b316e-116">The reclassification process copies the data from the original fixed asset book to the new fixed asset book.</span></span>

   - <span data-ttu-id="b316e-117">Uudelleenluokittelutapahtuma käyttää alkuperäisen kirjatun hankinnan tietoja, jotka sisältävät hankintatapahtumaan sisältyviä kirjanpitodimensiotietoja.</span><span class="sxs-lookup"><span data-stu-id="b316e-117">The reclassification transaction uses information from the original posted acquisition that includes financial dimension information that is included in the acquisition transaction.</span></span>  
   
   - <span data-ttu-id="b316e-118">Uudelleenluokitteluprosessi palauttaa samalla alkuperäisen käyttöomaisuuden hankinta- ja käyttöomaisuussiirtotapahtuman.</span><span class="sxs-lookup"><span data-stu-id="b316e-118">At the same time, the reclassification process reverses the original asset acquisition and asset transfer transaction.</span></span> 

<span data-ttu-id="b316e-119">Seuraavassa kaaviossa ja menettelyssä on esimerkki uudelleenluokitteluprosessista.</span><span class="sxs-lookup"><span data-stu-id="b316e-119">The following diagram and procedure provide an example of the reclassification process.</span></span> 

<span data-ttu-id="b316e-120">[![Kaavio, jossa näkyy uudelleenluokitteluprosessi](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span><span class="sxs-lookup"><span data-stu-id="b316e-120">[![Diagram showing the reclassicification process](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span></span>

<span data-ttu-id="b316e-121">Luokittele käyttöomaisuuserä uudelleen noudattamalla seuraavia vaiheita:</span><span class="sxs-lookup"><span data-stu-id="b316e-121">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="b316e-122">Valitse **Käyttöomaisuus > Kausittaiset tehtävät > Uudelleenluokittelu.**</span><span class="sxs-lookup"><span data-stu-id="b316e-122">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="b316e-123">Valitse **Käyttöomaisuusryhmä**-kentässä uudelleenluokiteltava ryhmä.</span><span class="sxs-lookup"><span data-stu-id="b316e-123">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="b316e-124">Valitse **Käyttöomaisuuserän numero** -kentässä uudelleen luokiteltava käyttöomaisuuserä.</span><span class="sxs-lookup"><span data-stu-id="b316e-124">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="b316e-125">Valitse **Uusi käyttöomaisuuserä** -kentässä ryhmä, johon käyttöomaisuuserä siirretään.</span><span class="sxs-lookup"><span data-stu-id="b316e-125">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="b316e-126">Jos uusi käyttöomaisuusryhmä on liitetty numerosarjaan, **Uusi käyttöomaisuuserän numero** -kenttä päivitetään uuden käyttöomaisuuserän numerosarjan numerolla.</span><span class="sxs-lookup"><span data-stu-id="b316e-126">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="b316e-127">Muussa tapauksessa **Uusi käyttöomaisuuserän numero** -kenttä päivitetään **Käyttöomaisuuserien parametrit** -sivulla määritetyn numerosarjan numerolla.</span><span class="sxs-lookup"><span data-stu-id="b316e-127">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="b316e-128">Jos numerosarjaa ei ole määritetty **Käyttöomaisuuserien parametrit** -sivulla, anna numero **Uusi käyttöomaisuuserän numero** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="b316e-128">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="b316e-129">Anna **Uudelleenluokittelupäivä** -kentässä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="b316e-129">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="b316e-130">Anna tai valitse **Tositesarja**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="b316e-130">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="b316e-131">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b316e-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
