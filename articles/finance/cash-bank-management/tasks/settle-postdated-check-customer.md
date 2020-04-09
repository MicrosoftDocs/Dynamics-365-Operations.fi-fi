---
title: Tilitä asiakkaalta jälkeen päin päivitetty lasku
description: Voit maksaa myöhemmäksi päivätyn sekin sen jälkeen, kun pankki on selvittänyt sekin.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bc6f90e7adb3facdfa1facb50fecb0de4ccb04d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141577"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="0f3cf-103">Tilitä asiakkaalta jälkeen päin päivitetty lasku</span><span class="sxs-lookup"><span data-stu-id="0f3cf-103">Settle a postdated check from a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0f3cf-104">Voit maksaa myöhemmäksi päivätyn sekin sen jälkeen, kun pankki on selvittänyt sekin.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="0f3cf-105">Tämä kirjanpitotapahtuma selvittää myös myöhemmäksi päivätyn sekin välitilin tapahtuman.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="0f3cf-106">Seuraavat tehtävät on suoritettava ennen tämän aloittamista:</span><span class="sxs-lookup"><span data-stu-id="0f3cf-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="0f3cf-107">Määritä jälkeen päin päivitetyt sekit</span><span class="sxs-lookup"><span data-stu-id="0f3cf-107">Set up postdated checks</span></span>

2) <span data-ttu-id="0f3cf-108">Rekisteröi ja kirjaa asiakkaan myöhemmäksi päivitetty sekki</span><span class="sxs-lookup"><span data-stu-id="0f3cf-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="0f3cf-109">Tämä tehtäväopastuksen rooli on Rahastonhoitaja.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="0f3cf-110">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="0f3cf-111">Valitse Luotonvalvonta > Kyselyt ja raportit > Maksut > Asiakkaan myöhemmäksi päivätyt sekit.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="0f3cf-112">Valitse Selvitä.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-112">Click Settle.</span></span>
3. <span data-ttu-id="0f3cf-113">Valitse Tilitä siirtokirjaukset.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="0f3cf-114">Selvitä sekkitapahtumien asiakastili</span><span class="sxs-lookup"><span data-stu-id="0f3cf-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="0f3cf-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-115">Close the page.</span></span>
5. <span data-ttu-id="0f3cf-116">Siirry kohtaan Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="0f3cf-117">Valitse vaihtoehto Näytä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="0f3cf-118">Valitse Näytä vain käyttäjän luomat -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="0f3cf-119">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="0f3cf-120">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-120">Click Lines.</span></span>
10. <span data-ttu-id="0f3cf-121">Valitse Tosite.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-121">Click Voucher.</span></span>
11. <span data-ttu-id="0f3cf-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-122">Close the page.</span></span>

