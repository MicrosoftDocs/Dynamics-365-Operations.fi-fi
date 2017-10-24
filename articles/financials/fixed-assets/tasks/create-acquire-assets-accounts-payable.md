--- 
title: "Käyttöomaisuuserien luominen ja hankkiminen ostoreskontrasta"
description: "Tässä tehtävän ohjauksessa esitellään käyttöomaisuuden luominen ja hankinta ostoprosessissa."
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9149378047fc22efbd401b7af86df07c1403e4f5
ms.openlocfilehash: cfe920b2ef493ab3ae36a9557001086ed99c3e4e
ms.contentlocale: fi-fi
ms.lasthandoff: 10/05/2017

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="db4c3-103">Käyttöomaisuuserien luominen ja hankkiminen ostoreskontrasta</span><span class="sxs-lookup"><span data-stu-id="db4c3-103">Create and acquire assets from accounts payable</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="db4c3-104">Tässä tehtävän ohjauksessa esitellään käyttöomaisuuden luominen ja hankinta ostoprosessissa.</span><span class="sxs-lookup"><span data-stu-id="db4c3-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span> <span data-ttu-id="db4c3-105">Siinä tarvitaan kirjanpitäjää ja ostoreskontran käsittelijää sekä esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="db4c3-105">It uses the Accountant and Accounts payable clerks and the demo company USMF.</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="db4c3-106">Käyttöomaisuusparametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="db4c3-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="db4c3-107">Siirry kohtaan Käyttöomaisuus > Asetukset > Käyttöomaisuuden parametrit.</span><span class="sxs-lookup"><span data-stu-id="db4c3-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="db4c3-108">Laajenna tai tiivistä Ostotilaukset-osa.</span><span class="sxs-lookup"><span data-stu-id="db4c3-108">Expand or collapse the Purchase orders section.</span></span>
3. <span data-ttu-id="db4c3-109">Valitse Salli käyttöomaisuuserän hankinta ostosta -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="db4c3-109">Check the Allow asset acquisition from Purchasing checkbox.</span></span>
4. <span data-ttu-id="db4c3-110">Valitse Luo käyttöomaisuuserä tuotteen vastaanoton tai laskun kirjaamisen aikana -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="db4c3-110">Check the Create asset during product receipt or invoice posting checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="db4c3-111">Uuden toimittajan laskun luominen</span><span class="sxs-lookup"><span data-stu-id="db4c3-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="db4c3-112">Siirry kohtaan Ostoreskontra > Työtilat > Toimittajan laskun syöttö.</span><span class="sxs-lookup"><span data-stu-id="db4c3-112">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="db4c3-113">Valitse Uusi toimittajan lasku.</span><span class="sxs-lookup"><span data-stu-id="db4c3-113">Click New vendor invoice.</span></span>
3. <span data-ttu-id="db4c3-114">Avaa haku valitsemalla Laskutustili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="db4c3-114">In the Invoice account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="db4c3-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="db4c3-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="db4c3-116">Kirjoita arvo Numero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="db4c3-116">In the Number field, type a value.</span></span>
6. <span data-ttu-id="db4c3-117">Syötä päivämäärä Kirjauspäivämäärä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="db4c3-117">In the Posting date field, enter a date.</span></span>
7. <span data-ttu-id="db4c3-118">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="db4c3-118">Click Add line.</span></span>
8. <span data-ttu-id="db4c3-119">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="db4c3-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="db4c3-120">Muita kuin varastoituja nimikkeitä ja hankintaluokkia voi käyttää käyttöomaisuuden hankinnassa.</span><span class="sxs-lookup"><span data-stu-id="db4c3-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="db4c3-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="db4c3-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="db4c3-122">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="db4c3-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="db4c3-123">Yksi laskurivi voi luoda vain yhden käyttöomaisuuden määrästä riippumatta.</span><span class="sxs-lookup"><span data-stu-id="db4c3-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span>  <span data-ttu-id="db4c3-124">Laskun määrä -kentän arvo siirretään käyttöomaisuuden määrään.</span><span class="sxs-lookup"><span data-stu-id="db4c3-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="db4c3-125">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="db4c3-125">In the Unit price field, enter a number.</span></span>
12. <span data-ttu-id="db4c3-126">Laajenna tai tiivistä Rivitiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="db4c3-126">Expand or collapse the Line details section.</span></span>
13. <span data-ttu-id="db4c3-127">Valitse Käyttöomaisuus-välilehti.</span><span class="sxs-lookup"><span data-stu-id="db4c3-127">Click the Fixed assets tab.</span></span>
14. <span data-ttu-id="db4c3-128">Valitse Luo uusi käyttöomaisuus -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="db4c3-128">Check the Create a new fixed asset checkbox.</span></span>
15. <span data-ttu-id="db4c3-129">Avaa haku valitsemalla Käyttöomaisuusryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="db4c3-129">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="db4c3-130">Valitse luettelosta käyttöomaisuusryhmä, jota käytetään uuden käyttöomaisuuden luomisessa.</span><span class="sxs-lookup"><span data-stu-id="db4c3-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="db4c3-131">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="db4c3-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="db4c3-132">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="db4c3-132">Click Post.</span></span>
    * <span data-ttu-id="db4c3-133">Käyttöomaisuus luodaan ja hankitaan, kun lasku on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="db4c3-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  


