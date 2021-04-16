---
title: Rekisteröi ja kirjaa asiakkaan myöhemmäksi päivitetty sekki
description: Voit rekisteröidä asiakkaalta saadun myöhemmäksi päivätyn sekin tiedot.
author: kweekley
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9cb49ac6ebbd04e71215af010cb5a7b6302fe44e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834689"
---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="c3159-103">Rekisteröi ja kirjaa asiakkaan myöhemmäksi päivitetty sekki</span><span class="sxs-lookup"><span data-stu-id="c3159-103">Register and post a postdated check for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c3159-104">Voit rekisteröidä asiakkaalta saadun myöhemmäksi päivätyn sekin tiedot.</span><span class="sxs-lookup"><span data-stu-id="c3159-104">You can register details of a postdated check received from a customer.</span></span> <span data-ttu-id="c3159-105">Voit myös kirjata myöhemmäksi päivätyn sekin ja luoda kirjanpitotapahtumat.</span><span class="sxs-lookup"><span data-stu-id="c3159-105">You can also post the postdated check and generate financial transactions.</span></span>   <span data-ttu-id="c3159-106">Suorita seuraavat tehtävät ennen asiakkaalta saadun myöhemmäksi päivitetyn sekin rekisteröintiä ja kirjaamista: \* Määritä myöhemmäksi päivitetyt sekit Maksuliikenteen hallinta -sivulla. \* Määritä myöhemmäksi päivitettyjen sekkien maksutapa . Tämän menettelyn rooli on Rahastonhoitaja.</span><span class="sxs-lookup"><span data-stu-id="c3159-106">Complete the following tasks before you register and post a postdated check received from a customer:   \* Set up postdated check in the Cash and bank management page \* Set up a method of payment for postdated checks   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="c3159-107">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="c3159-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="c3159-108">Siirry kohtaan Myyntireskontra > Maksut > Maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="c3159-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="c3159-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c3159-109">Click New.</span></span>
3. <span data-ttu-id="c3159-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c3159-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c3159-111">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="c3159-111">Click Lines.</span></span>
5. <span data-ttu-id="c3159-112">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c3159-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="c3159-113">Määritä Tili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="c3159-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="c3159-114">Syötä Kredit-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c3159-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="c3159-115">Anna myöhemmäksi päivätyssä sekissä määritetty summa.</span><span class="sxs-lookup"><span data-stu-id="c3159-115">Enter the amount specified in the postdated check.</span></span>  
8. <span data-ttu-id="c3159-116">Valitse Maksu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="c3159-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="c3159-117">Syötä arvo Maksutapa-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c3159-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="c3159-118">Valitse myöhemmäksi päivätyn sekin maksutapa.</span><span class="sxs-lookup"><span data-stu-id="c3159-118">Select the method of payment for the postdated check.</span></span>  
10. <span data-ttu-id="c3159-119">Valitse Myöhemmäksi päivätyt sekit -välilehti.</span><span class="sxs-lookup"><span data-stu-id="c3159-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="c3159-120">Anna päivämäärä Erääntymispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c3159-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="c3159-121">Anna myöhemmäksi päivätyn sekin eräpäivä.</span><span class="sxs-lookup"><span data-stu-id="c3159-121">Enter the date when the postdated check is due for payment.</span></span>  
12. <span data-ttu-id="c3159-122">Kirjoita arvo Myöntävä pankin konttori -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c3159-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="c3159-123">Anna myöhemmäksi päivätyn sekin pankkitiedot.</span><span class="sxs-lookup"><span data-stu-id="c3159-123">Enter the bank details of the postdated check.</span></span>  
13. <span data-ttu-id="c3159-124">Kirjoita arvo Sekin numero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c3159-124">In the check number field, type a value.</span></span>
14. <span data-ttu-id="c3159-125">Kirjoita arvo Myöntävän pankin nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c3159-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="c3159-126">Anna myöhemmäksi päivätyn sekin pankkitiedot.</span><span class="sxs-lookup"><span data-stu-id="c3159-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="c3159-127">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="c3159-127">Click Post.</span></span>
16. <span data-ttu-id="c3159-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c3159-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]