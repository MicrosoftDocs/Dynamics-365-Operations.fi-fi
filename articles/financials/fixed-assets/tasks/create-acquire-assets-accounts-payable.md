---
title: Käyttöomaisuuserien luominen ja hankkiminen ostoreskontrasta
description: Tässä tehtävän ohjauksessa esitellään käyttöomaisuuden luominen ja hankinta ostoprosessissa.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6c36338cc67855c79ec97d88bb8b633417b85c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "316415"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="cd747-103">Käyttöomaisuuserien luominen ja hankkiminen ostoreskontrasta</span><span class="sxs-lookup"><span data-stu-id="cd747-103">Create and acquire assets from Accounts payable</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd747-104">Tässä tehtävän ohjauksessa esitellään käyttöomaisuuden luominen ja hankinta ostoprosessissa.</span><span class="sxs-lookup"><span data-stu-id="cd747-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="cd747-105">Siinä tarvitaan kirjanpitäjää ja ostoreskontran käsittelijää sekä esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="cd747-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="cd747-106">Käyttöomaisuusparametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="cd747-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="cd747-107">Siirry kohtaan Käyttöomaisuus > Asetukset > Käyttöomaisuuden parametrit.</span><span class="sxs-lookup"><span data-stu-id="cd747-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="cd747-108">Laajenna tai tiivistä Ostotilaukset-osa.</span><span class="sxs-lookup"><span data-stu-id="cd747-108">Expand or collapse the Purchase orders section.</span></span>
3. <span data-ttu-id="cd747-109">Valitse Salli käyttöomaisuuserän hankinta ostosta -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="cd747-109">Check the Allow asset acquisition from Purchasing checkbox.</span></span>
4. <span data-ttu-id="cd747-110">Valitse Luo käyttöomaisuuserä tuotteen vastaanoton tai laskun kirjaamisen aikana -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="cd747-110">Check the Create asset during product receipt or invoice posting checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="cd747-111">Uuden toimittajan laskun luominen</span><span class="sxs-lookup"><span data-stu-id="cd747-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="cd747-112">Siirry kohtaan Ostoreskontra > Työtilat > Toimittajan laskun syöttö.</span><span class="sxs-lookup"><span data-stu-id="cd747-112">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="cd747-113">Valitse Uusi toimittajan lasku.</span><span class="sxs-lookup"><span data-stu-id="cd747-113">Click New vendor invoice.</span></span>
3. <span data-ttu-id="cd747-114">Avaa haku valitsemalla Laskutustili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="cd747-114">In the Invoice account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="cd747-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cd747-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="cd747-116">Kirjoita arvo Numero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cd747-116">In the Number field, type a value.</span></span>
6. <span data-ttu-id="cd747-117">Syötä päivämäärä Kirjauspäivämäärä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cd747-117">In the Posting date field, enter a date.</span></span>
7. <span data-ttu-id="cd747-118">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="cd747-118">Click Add line.</span></span>
8. <span data-ttu-id="cd747-119">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="cd747-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cd747-120">Muita kuin varastoituja nimikkeitä ja hankintaluokkia voi käyttää käyttöomaisuuden hankinnassa.</span><span class="sxs-lookup"><span data-stu-id="cd747-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="cd747-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cd747-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="cd747-122">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cd747-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="cd747-123">Yksi laskurivi voi luoda vain yhden käyttöomaisuuden määrästä riippumatta.</span><span class="sxs-lookup"><span data-stu-id="cd747-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span>  <span data-ttu-id="cd747-124">Laskun määrä -kentän arvo siirretään käyttöomaisuuden määrään.</span><span class="sxs-lookup"><span data-stu-id="cd747-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="cd747-125">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="cd747-125">In the Unit price field, enter a number.</span></span>
12. <span data-ttu-id="cd747-126">Laajenna tai tiivistä Rivitiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="cd747-126">Expand or collapse the Line details section.</span></span>
13. <span data-ttu-id="cd747-127">Valitse Käyttöomaisuus-välilehti.</span><span class="sxs-lookup"><span data-stu-id="cd747-127">Click the Fixed assets tab.</span></span>
14. <span data-ttu-id="cd747-128">Valitse Luo uusi käyttöomaisuus -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="cd747-128">Check the Create a new fixed asset checkbox.</span></span>
15. <span data-ttu-id="cd747-129">Avaa haku valitsemalla Käyttöomaisuusryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="cd747-129">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="cd747-130">Valitse luettelosta käyttöomaisuusryhmä, jota käytetään uuden käyttöomaisuuden luomisessa.</span><span class="sxs-lookup"><span data-stu-id="cd747-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="cd747-131">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cd747-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="cd747-132">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="cd747-132">Click Post.</span></span>
    * <span data-ttu-id="cd747-133">Käyttöomaisuus luodaan ja hankitaan, kun lasku on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="cd747-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  

