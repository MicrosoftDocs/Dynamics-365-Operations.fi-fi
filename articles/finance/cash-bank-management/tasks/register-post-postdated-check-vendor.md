---
title: Rekisteröi ja kirjaa toimittajan myöhemmäksi päivitetty sekki
description: Voit rekisteröidä myöhemmäksi päivätyn sekin tiedot kirjauskansion tositteella, ennen kuin kirjoitat sekin toimittajalle.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb7f9935b20d042551b0ce77fd6bdbf55e9f9669
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834665"
---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="15812-103">Rekisteröi ja kirjaa toimittajan myöhemmäksi päivitetty sekki</span><span class="sxs-lookup"><span data-stu-id="15812-103">Register and post a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="15812-104">Voit rekisteröidä myöhemmäksi päivätyn sekin tiedot kirjauskansion tositteella, ennen kuin kirjoitat sekin toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="15812-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="15812-105">Voit myös kirjata myöhemmäksi päivätyn sekin ja luoda kirjanpitotapahtumat.</span><span class="sxs-lookup"><span data-stu-id="15812-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="15812-106">Tee seuraava tehtävä, ennen kuin rekisteröit ja kirjaat toimittajalta saadun myöhemmäksi päivätyn sekin:</span><span class="sxs-lookup"><span data-stu-id="15812-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="15812-107">Määritä myöhemmäksi päivitetyt sekit Maksuliikenteen hallinta -sivulla.</span><span class="sxs-lookup"><span data-stu-id="15812-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="15812-108">Tämä tehtäväopastuksen rooli on Rahastonhoitaja.</span><span class="sxs-lookup"><span data-stu-id="15812-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="15812-109">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="15812-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="15812-110">Valitse Ostoreskontra > Maksut > Maksukirjauskansio</span><span class="sxs-lookup"><span data-stu-id="15812-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="15812-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="15812-111">Click New.</span></span>
3. <span data-ttu-id="15812-112">Kirjoita Nimi-kenttään VendPay.</span><span class="sxs-lookup"><span data-stu-id="15812-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="15812-113">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="15812-113">Click Lines.</span></span>
5. <span data-ttu-id="15812-114">Määritä Tili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="15812-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="15812-115">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="15812-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="15812-116">Syötä Debet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="15812-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="15812-117">Avaa haku valitsemalla Maksutapa-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="15812-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="15812-118">Valitse myöhemmäksi päivätyn sekin maksutapa</span><span class="sxs-lookup"><span data-stu-id="15812-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="15812-119">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="15812-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="15812-120">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="15812-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="15812-121">Valitse Myöhemmäksi päivätyt sekit -välilehti.</span><span class="sxs-lookup"><span data-stu-id="15812-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="15812-122">Kirjoita arvo Sekin numero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="15812-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="15812-123">Anna myöhemmäksi päivätyn sekin numero tai muokkaa sitä.</span><span class="sxs-lookup"><span data-stu-id="15812-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="15812-124">Kirjoita arvo Myöntävän pankin nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="15812-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="15812-125">anna myöntävän pankin tiedot</span><span class="sxs-lookup"><span data-stu-id="15812-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="15812-126">Valitse Luettelo-välilehti.</span><span class="sxs-lookup"><span data-stu-id="15812-126">Click the List tab.</span></span>
15. <span data-ttu-id="15812-127">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="15812-127">Click Post.</span></span>
16. <span data-ttu-id="15812-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15812-128">Close the page.</span></span>
17. <span data-ttu-id="15812-129">Valitse Myöhemmäksi päivätyt sekit -välilehti.</span><span class="sxs-lookup"><span data-stu-id="15812-129">Click the Postdated checks tab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]