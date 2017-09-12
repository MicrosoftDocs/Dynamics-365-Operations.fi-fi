--- 
title: Luo puhelinkeskustilauksia
description: "Tässä menettelyssä esitellään asiakkaan etsiminen, uuden tilauksen luominen, tuotteen hakeminen ja maksun periminen asiakkaalta."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 62f88cc2e28405a9d2eb43819fb09d83a64658b6
ms.contentlocale: fi-fi
ms.lasthandoff: 07/28/2017

---
# <a name="create-call-center-orders"></a><span data-ttu-id="86f11-103">Luo puhelinkeskustilauksia</span><span class="sxs-lookup"><span data-stu-id="86f11-103">Create call center orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="86f11-104">Tässä menettelyssä esitellään asiakkaan etsiminen, uuden tilauksen luominen, tuotteen hakeminen ja maksun periminen asiakkaalta.</span><span class="sxs-lookup"><span data-stu-id="86f11-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="86f11-105">Tässä menettelyssä käytetään esittely-yritystä USRT. Tämä on tarkoitettu myyntitilauksia käsittelevälle assistentille.</span><span class="sxs-lookup"><span data-stu-id="86f11-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="86f11-106">Edellytykset: Menettelyn suorittava käyttäjä on määritetty puhelinkeskuksen käyttäjiksi. Julkaistussa Fabrikamin puolivuosittaisessa luettelossa on vähintään yksi lähdekoodi.</span><span class="sxs-lookup"><span data-stu-id="86f11-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="86f11-107">Valitse Vähittäismyynti ja kauppa > Asiakkaat > Asiakaspalvelu.</span><span class="sxs-lookup"><span data-stu-id="86f11-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="86f11-108">Syötä SearchText-kenttään hakuehdot, joilla etsit asiakasta.</span><span class="sxs-lookup"><span data-stu-id="86f11-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="86f11-109">Valitse tässä esimerkissä menettelytyypiksi Nieminen ja paina sarkainnäppäintä.</span><span class="sxs-lookup"><span data-stu-id="86f11-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="86f11-110">Valitse Haku.</span><span class="sxs-lookup"><span data-stu-id="86f11-110">Click Search.</span></span>
    * <span data-ttu-id="86f11-111">Koska esittelytiedoissa on vain yksi asiakas nimeltä Nieminen, hänet valitaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="86f11-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="86f11-112">Valitse Uusi myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="86f11-112">Click New sales order.</span></span>
5. <span data-ttu-id="86f11-113">Laajenna tai tiivistä Myyntitilauksen otsikko -osa.</span><span class="sxs-lookup"><span data-stu-id="86f11-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="86f11-114">Valitse luettelon lähdekoodi.</span><span class="sxs-lookup"><span data-stu-id="86f11-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="86f11-115">Jos aktiivisia lähdekoodeja ei ole, voit sulkea Lähde-kentän ja ohittaa tämän vaiheen.</span><span class="sxs-lookup"><span data-stu-id="86f11-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="86f11-116">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="86f11-116">Click Add line.</span></span>
8. <span data-ttu-id="86f11-117">Syötä Nimiketunnus-kenttään nimikkeen hakuehto.</span><span class="sxs-lookup"><span data-stu-id="86f11-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="86f11-118">Syötä tässä mallimenettelyssä osittainen nimikenumero 8111 ja paina sarkainnäppäintä.</span><span class="sxs-lookup"><span data-stu-id="86f11-118">For this sample procedure enter a partial item number of '8111' and press tab.</span></span> <span data-ttu-id="86f11-119">Nimike tulee esille hakuikkunaan.</span><span class="sxs-lookup"><span data-stu-id="86f11-119">This will pop up the item search window.</span></span>  
9. <span data-ttu-id="86f11-120">Myyntitilaukseen lisättävän tuotteen valitseminen</span><span class="sxs-lookup"><span data-stu-id="86f11-120">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="86f11-121">Syötä myyntimäärä.</span><span class="sxs-lookup"><span data-stu-id="86f11-121">Enter the sales quantity.</span></span>
11. <span data-ttu-id="86f11-122">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="86f11-122">Click Create.</span></span>
12. <span data-ttu-id="86f11-123">Valitse Valmis, kun haluat tarkistaa asiakkaan maksun.</span><span class="sxs-lookup"><span data-stu-id="86f11-123">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="86f11-124">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="86f11-124">Click Add.</span></span>
    * <span data-ttu-id="86f11-125">Lisää-linkki löytyy Maksut-välilehdestä.</span><span class="sxs-lookup"><span data-stu-id="86f11-125">The Add link is in the Payments tab.</span></span> <span data-ttu-id="86f11-126">Laajenna Maksut-välilehti, jos se on tiivistetty.</span><span class="sxs-lookup"><span data-stu-id="86f11-126">Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="86f11-127">Valitse maksutapa.</span><span class="sxs-lookup"><span data-stu-id="86f11-127">Select the payment method.</span></span>
    * <span data-ttu-id="86f11-128">Valitse tässä menettelyssä käteismaksutapa.</span><span class="sxs-lookup"><span data-stu-id="86f11-128">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="86f11-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="86f11-129">Close the page.</span></span>
16. <span data-ttu-id="86f11-130">Anna määrä.</span><span class="sxs-lookup"><span data-stu-id="86f11-130">Enter the amount.</span></span>
    * <span data-ttu-id="86f11-131">Syötä tässä menettelyssä tilaussummaksi summa, joka löytyy Myyntitilauksen yhteenveto -sivun summakentän vasemmalta puolelta.</span><span class="sxs-lookup"><span data-stu-id="86f11-131">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="86f11-132">Näin voit määrittää tilauksen kokonaan maksetuksi.</span><span class="sxs-lookup"><span data-stu-id="86f11-132">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="86f11-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="86f11-133">Click OK.</span></span>
18. <span data-ttu-id="86f11-134">Valitse Lähetä.</span><span class="sxs-lookup"><span data-stu-id="86f11-134">Click Submit.</span></span>


