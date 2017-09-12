--- 
title: "Tilitä asiakkaalta jälkeen päin päivitetty lasku"
description: "Voit maksaa myöhemmäksi päivätyn sekin sen jälkeen, kun pankki on selvittänyt sekin."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9cb6064a83e02ddf1fea2de7928965773d08bbc9
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="ec2bc-103">Tilitä asiakkaalta jälkeen päin päivitetty lasku</span><span class="sxs-lookup"><span data-stu-id="ec2bc-103">Settle a postdated check from a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ec2bc-104">Voit maksaa myöhemmäksi päivätyn sekin sen jälkeen, kun pankki on selvittänyt sekin.</span><span class="sxs-lookup"><span data-stu-id="ec2bc-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="ec2bc-105">Tämä kirjanpitotapahtuma selvittää myös myöhemmäksi päivätyn sekin välitilin tapahtuman.</span><span class="sxs-lookup"><span data-stu-id="ec2bc-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="ec2bc-106">Seuraavat tehtävät on suoritettava ennen tämän aloittamista:</span><span class="sxs-lookup"><span data-stu-id="ec2bc-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="ec2bc-107">Määritä jälkeen päin päivitetyt sekit</span><span class="sxs-lookup"><span data-stu-id="ec2bc-107">Set up postdated checks</span></span>

2) <span data-ttu-id="ec2bc-108">Rekisteröi ja kirjaa asiakkaan myöhemmäksi päivitetty sekki</span><span class="sxs-lookup"><span data-stu-id="ec2bc-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="ec2bc-109">Tämä tehtäväopastuksen rooli on Rahastonhoitaja.</span><span class="sxs-lookup"><span data-stu-id="ec2bc-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="ec2bc-110">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="ec2bc-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="ec2bc-111">Valitse Luotonvalvonta > Kyselyt ja raportit > Maksut > Asiakkaan myöhemmäksi päivätyt sekit.</span><span class="sxs-lookup"><span data-stu-id="ec2bc-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="ec2bc-112">Valitse Selvitä.</span><span class="sxs-lookup"><span data-stu-id="ec2bc-112">Click Settle.</span></span>
3. <span data-ttu-id="ec2bc-113">Valitse Tilitä siirtokirjaukset.</span><span class="sxs-lookup"><span data-stu-id="ec2bc-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="ec2bc-114">Selvitä sekkitapahtumien asiakastili</span><span class="sxs-lookup"><span data-stu-id="ec2bc-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="ec2bc-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ec2bc-115">Close the page.</span></span>
5. <span data-ttu-id="ec2bc-116">Siirry kohtaan Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="ec2bc-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="ec2bc-117">Valitse vaihtoehto Näytä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ec2bc-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="ec2bc-118">Valitse Näytä vain käyttäjän luomat -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="ec2bc-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="ec2bc-119">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ec2bc-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="ec2bc-120">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="ec2bc-120">Click Lines.</span></span>
10. <span data-ttu-id="ec2bc-121">Valitse Tosite.</span><span class="sxs-lookup"><span data-stu-id="ec2bc-121">Click Voucher.</span></span>
11. <span data-ttu-id="ec2bc-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ec2bc-122">Close the page.</span></span>


