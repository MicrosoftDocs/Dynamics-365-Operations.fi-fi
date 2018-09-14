--- 
title: "Toimittajalaskun arvonlisäveron laskeminen ja täsmäytys"
description: "Jos alkuperäinen lähdeasiakirja sisältää eri verosummat kuin lasketut summat, voit oikaista summat ennen kirjaamista."
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 803c038d907b68a3c72a83a3e035c4e08b8a8661
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="22a82-103">Toimittajalaskun arvonlisäveron laskeminen ja täsmäytys</span><span class="sxs-lookup"><span data-stu-id="22a82-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22a82-104">Jos alkuperäinen lähdeasiakirja sisältää eri verosummat kuin lasketut summat, voit oikaista summat ennen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="22a82-104">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="22a82-105">Tässä tehtävässä käytetään esittely-yritystä DEMF.</span><span class="sxs-lookup"><span data-stu-id="22a82-105">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="22a82-106">Siirry kohtaan Ostoreskontra > Laskut > Laskun kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="22a82-106">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="22a82-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="22a82-107">Click New.</span></span>
3. <span data-ttu-id="22a82-108">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="22a82-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="22a82-109">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="22a82-109">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="22a82-110">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="22a82-110">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="22a82-111">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="22a82-111">Click Lines.</span></span>
7. <span data-ttu-id="22a82-112">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="22a82-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="22a82-113">Määritä Tili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="22a82-113">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="22a82-114">Kirjoita Lasku-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="22a82-114">In the Invoice field, type a value.</span></span>
10. <span data-ttu-id="22a82-115">Syötä Kredit-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="22a82-115">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="22a82-116">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="22a82-116">In the Offset account field, specify the desired values.</span></span>
12. <span data-ttu-id="22a82-117">Valitse Arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="22a82-117">Click Sales tax.</span></span>
13. <span data-ttu-id="22a82-118">Syötä Toteutunut kokonaisarvonlisäverosumma -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="22a82-118">In the Total actual sales tax amount field, enter a number.</span></span>
14. <span data-ttu-id="22a82-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="22a82-119">Click OK.</span></span>
15. <span data-ttu-id="22a82-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="22a82-120">Click Save.</span></span>
16. <span data-ttu-id="22a82-121">Valitse Arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="22a82-121">Click Sales tax.</span></span>
17. <span data-ttu-id="22a82-122">Arvonlisäverosummat voidaan oikaista Oikaisu-välilehdessä arvonlisäverokoodin mukaan.</span><span class="sxs-lookup"><span data-stu-id="22a82-122">On the Adjustment tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
18. <span data-ttu-id="22a82-123">Valitse Nollaa todellinen lasketuista summista.</span><span class="sxs-lookup"><span data-stu-id="22a82-123">Click Reset actual from calculated amounts.</span></span>
19. <span data-ttu-id="22a82-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="22a82-124">Click OK.</span></span>
20. <span data-ttu-id="22a82-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="22a82-125">Click Save.</span></span>


