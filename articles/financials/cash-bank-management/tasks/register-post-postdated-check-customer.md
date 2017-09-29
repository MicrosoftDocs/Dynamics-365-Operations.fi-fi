--- 
title: "Rekisteröi ja kirjaa asiakkaan myöhemmäksi päivitetty sekki"
description: "Voit rekisteröidä asiakkaalta saadun myöhemmäksi päivätyn sekin tiedot."
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
ms.openlocfilehash: 1610036815349f625a67d5dd67260114d42fff97
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="a5571-103">Rekisteröi ja kirjaa asiakkaan myöhemmäksi päivitetty sekki</span><span class="sxs-lookup"><span data-stu-id="a5571-103">Register and post a postdated check for a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a5571-104">Voit rekisteröidä asiakkaalta saadun myöhemmäksi päivätyn sekin tiedot.</span><span class="sxs-lookup"><span data-stu-id="a5571-104">You can register details of a postdated cheque received from a customer.</span></span> <span data-ttu-id="a5571-105">Voit myös kirjata myöhemmäksi päivätyn sekin ja luoda kirjanpitotapahtumat.</span><span class="sxs-lookup"><span data-stu-id="a5571-105">You can also post the postdated cheque and generate financial transactions.</span></span>   <span data-ttu-id="a5571-106">Suorita seuraavat tehtävät ennen asiakkaalta saadun myöhemmäksi päivitetyn sekin rekisteröintiä ja kirjaamista: • Määritä myöhemmäksi päivitetyt sekit Maksuliikenteen hallinta -sivulla. • Määritä myöhemmäksi päivitettyjen sekkien maksutapa . Tämän menettelyn rooli on Rahastonhoitaja.</span><span class="sxs-lookup"><span data-stu-id="a5571-106">Complete the following tasks before you register and post a postdated cheque received from a customer:   • Set up postdated Cheques in the Cash and bank management page • Set up a method of payment for postdated Cheques   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="a5571-107">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="a5571-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="a5571-108">Siirry kohtaan Myyntireskontra > Maksut > Maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="a5571-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="a5571-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a5571-109">Click New.</span></span>
3. <span data-ttu-id="a5571-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a5571-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a5571-111">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="a5571-111">Click Lines.</span></span>
5. <span data-ttu-id="a5571-112">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a5571-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="a5571-113">Määritä Tili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="a5571-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="a5571-114">Syötä Kredit-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="a5571-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="a5571-115">Anna myöhemmäksi päivätyssä sekissä määritetty summa.</span><span class="sxs-lookup"><span data-stu-id="a5571-115">Enter the amount specified in the postdated cheque.</span></span>  
8. <span data-ttu-id="a5571-116">Valitse Maksu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="a5571-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="a5571-117">Syötä arvo Maksutapa-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a5571-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="a5571-118">Valitse myöhemmäksi päivätyn sekin maksutapa</span><span class="sxs-lookup"><span data-stu-id="a5571-118">Select the method of payment for the postdated cheque</span></span>  
10. <span data-ttu-id="a5571-119">Valitse Myöhemmäksi päivätyt sekit -välilehti.</span><span class="sxs-lookup"><span data-stu-id="a5571-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="a5571-120">Anna päivämäärä Erääntymispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a5571-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="a5571-121">Anna myöhemmäksi päivätyn sekin eräpäivä.</span><span class="sxs-lookup"><span data-stu-id="a5571-121">Enter the date when the postdated cheque is due for payment.</span></span>  
12. <span data-ttu-id="a5571-122">Kirjoita arvo Myöntävä pankin konttori -kenttään.</span><span class="sxs-lookup"><span data-stu-id="a5571-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="a5571-123">Anna myöhemmäksi päivätyn sekin pankkitiedot.</span><span class="sxs-lookup"><span data-stu-id="a5571-123">Enter the bank details of the postdated cheque.</span></span>  
13. <span data-ttu-id="a5571-124">Kirjoita arvo Sekin numero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="a5571-124">In the cheque number field, type a value.</span></span>
14. <span data-ttu-id="a5571-125">Kirjoita arvo Myöntävän pankin nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="a5571-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="a5571-126">Anna myöhemmäksi päivätyn sekin pankkitiedot.</span><span class="sxs-lookup"><span data-stu-id="a5571-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="a5571-127">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="a5571-127">Click Post.</span></span>
16. <span data-ttu-id="a5571-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a5571-128">Close the page.</span></span>


