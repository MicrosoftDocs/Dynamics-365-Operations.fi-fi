---
title: Rekisteröi ja kirjaa asiakkaan myöhemmäksi päivitetty sekki
description: Voit rekisteröidä asiakkaalta saadun myöhemmäksi päivätyn sekin tiedot.
author: kweekley
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7b7899e11849175976b4c7ee44be4355e733d1d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225342"
---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="ae89f-103">Rekisteröi ja kirjaa asiakkaan myöhemmäksi päivitetty sekki</span><span class="sxs-lookup"><span data-stu-id="ae89f-103">Register and post a postdated check for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae89f-104">Voit rekisteröidä asiakkaalta saadun myöhemmäksi päivätyn sekin tiedot.</span><span class="sxs-lookup"><span data-stu-id="ae89f-104">You can register details of a postdated check received from a customer.</span></span> <span data-ttu-id="ae89f-105">Voit myös kirjata myöhemmäksi päivätyn sekin ja luoda kirjanpitotapahtumat.</span><span class="sxs-lookup"><span data-stu-id="ae89f-105">You can also post the postdated check and generate financial transactions.</span></span>   <span data-ttu-id="ae89f-106">Suorita seuraavat tehtävät ennen asiakkaalta saadun myöhemmäksi päivitetyn sekin rekisteröintiä ja kirjaamista: \* Määritä myöhemmäksi päivitetyt sekit Maksuliikenteen hallinta -sivulla. \* Määritä myöhemmäksi päivitettyjen sekkien maksutapa . Tämän menettelyn rooli on Rahastonhoitaja.</span><span class="sxs-lookup"><span data-stu-id="ae89f-106">Complete the following tasks before you register and post a postdated check received from a customer:   \* Set up postdated check in the Cash and bank management page \* Set up a method of payment for postdated checks   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="ae89f-107">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="ae89f-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="ae89f-108">Siirry kohtaan Myyntireskontra > Maksut > Maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="ae89f-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="ae89f-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ae89f-109">Click New.</span></span>
3. <span data-ttu-id="ae89f-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ae89f-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ae89f-111">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="ae89f-111">Click Lines.</span></span>
5. <span data-ttu-id="ae89f-112">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ae89f-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="ae89f-113">Määritä Tili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="ae89f-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="ae89f-114">Syötä Kredit-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ae89f-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="ae89f-115">Anna myöhemmäksi päivätyssä sekissä määritetty summa.</span><span class="sxs-lookup"><span data-stu-id="ae89f-115">Enter the amount specified in the postdated check.</span></span>  
8. <span data-ttu-id="ae89f-116">Valitse Maksu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="ae89f-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="ae89f-117">Syötä arvo Maksutapa-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ae89f-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="ae89f-118">Valitse myöhemmäksi päivätyn sekin maksutapa.</span><span class="sxs-lookup"><span data-stu-id="ae89f-118">Select the method of payment for the postdated check.</span></span>  
10. <span data-ttu-id="ae89f-119">Valitse Myöhemmäksi päivätyt sekit -välilehti.</span><span class="sxs-lookup"><span data-stu-id="ae89f-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="ae89f-120">Anna päivämäärä Erääntymispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ae89f-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="ae89f-121">Anna myöhemmäksi päivätyn sekin eräpäivä.</span><span class="sxs-lookup"><span data-stu-id="ae89f-121">Enter the date when the postdated check is due for payment.</span></span>  
12. <span data-ttu-id="ae89f-122">Kirjoita arvo Myöntävä pankin konttori -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ae89f-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="ae89f-123">Anna myöhemmäksi päivätyn sekin pankkitiedot.</span><span class="sxs-lookup"><span data-stu-id="ae89f-123">Enter the bank details of the postdated check.</span></span>  
13. <span data-ttu-id="ae89f-124">Kirjoita arvo Sekin numero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ae89f-124">In the check number field, type a value.</span></span>
14. <span data-ttu-id="ae89f-125">Kirjoita arvo Myöntävän pankin nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ae89f-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="ae89f-126">Anna myöhemmäksi päivätyn sekin pankkitiedot.</span><span class="sxs-lookup"><span data-stu-id="ae89f-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="ae89f-127">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="ae89f-127">Click Post.</span></span>
16. <span data-ttu-id="ae89f-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ae89f-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]