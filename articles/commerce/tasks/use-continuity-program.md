---
title: Jatkuvuusohjelman käyttäminen
description: Näissä toimintaohjeissa neuvotaan, miten jatkuvuusohjelman avulla tehdään myyntejä ja käsitellään niihin liittyviä myyntitilauksia.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2baf0127a35cc62952fd78daaf8204d35ec8d2b3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412000"
---
# <a name="using-continuity-program"></a><span data-ttu-id="c0ebb-103">Jatkuvuusohjelman käyttäminen</span><span class="sxs-lookup"><span data-stu-id="c0ebb-103">Using continuity program</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0ebb-104">Näissä toimintaohjeissa neuvotaan, miten jatkuvuusohjelman avulla tehdään myyntejä ja käsitellään niihin liittyviä myyntitilauksia.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="c0ebb-105">Käyttäjä on määritettävä puhelinkeskuksen käyttäjäksi, jotta tämän menettelyn voi suorittaa.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="c0ebb-106">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="c0ebb-107">Valitse Retail ja Commerce > Asiakkaat > Asiakaspalvelu.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="c0ebb-108">Kirjoita SearchText-kenttään "Karen" ja paina sitten sarkainnäppäintä.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="c0ebb-109">Tarkennettu haku -valintaikkunan tulisi aueta.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="c0ebb-110">Jos näin ei tapahdu, valitse Etsi kentän oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="c0ebb-111">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c0ebb-112">Tuloksissa tulisi olla vain yksi rivi nimellä Karen Berg.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="c0ebb-113">Valitse rivi napsauttamalla valintamerkkiä ruudukon vasemmassa laidassa.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="c0ebb-114">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-114">Click Select.</span></span>
5. <span data-ttu-id="c0ebb-115">Valitse Uusi myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-115">Click New sales order.</span></span>
    * <span data-ttu-id="c0ebb-116">Ota muistiin myyntitilauksen numero.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="c0ebb-117">Tarvitset sitä myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="c0ebb-118">Kirjoita Nimiketunnus-kenttään 88000 ja paina sitten sarkainnäppäintä.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="c0ebb-119">Tämä on jatkuvuusnimike USRT-yrityksen esittelytiedoissa.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="c0ebb-120">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-120">Click Complete.</span></span>
8. <span data-ttu-id="c0ebb-121">Kirjoita Maksutapa-kenttään "Visa".</span><span class="sxs-lookup"><span data-stu-id="c0ebb-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="c0ebb-122">Valitse Lisää luottokortti.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-122">Click Add credit card.</span></span>
    * <span data-ttu-id="c0ebb-123">Anna pakolliset luottokorttitiedot tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="c0ebb-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-124">Click OK.</span></span>
11. <span data-ttu-id="c0ebb-125">Laajenna Maksu-osa.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="c0ebb-126">Jotta puhelinkeskus voi lähettää tilauksen, tilaukselle on syötettävä maksuja.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="c0ebb-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-127">Click OK.</span></span>
13. <span data-ttu-id="c0ebb-128">Valitse Lähetä.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-128">Click Submit.</span></span>
    * <span data-ttu-id="c0ebb-129">Jatkuvuustilauksen luonti on nyt valmis.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="c0ebb-130">Seuraavaksi ajat kaksi eräprosessia, jotka käsittelevät jatkuvuustilaukset.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="c0ebb-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-131">Close the page.</span></span>
15. <span data-ttu-id="c0ebb-132">Valitse Retail ja Commerce > Jatkuvuus > Käsittele jatkuvuusmaksut.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-132">Go to Retail and Commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="c0ebb-133">Kirjoita Jatkuvuusnimike-kenttään 88000 ja paina sitten sarkainnäppäintä.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="c0ebb-134">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-134">Click OK.</span></span>
18. <span data-ttu-id="c0ebb-135">Valitse Retail ja Commerce > Jatkuvuus > Luo jatkuvuuden alitilaukset.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-135">Go to Retail and Commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="c0ebb-136">Tämä prosessi luo uusia myyntitilauksia, jotka perustuvat jatkuvuusohjelmasi asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="c0ebb-137">Kirjoita Jatkuvuusnimike-kenttään 88000 ja paina sitten sarkainnäppäintä.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="c0ebb-138">Nimike 88000 on jatkuvuusnimike USRT-yrityksen esittelytiedoissa.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="c0ebb-139">Syötä tai valitse arvo kentässä Myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="c0ebb-140">Anna aiemmin ohjeessa muistiin ottamasi myyntitilauksen numero.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="c0ebb-141">Tämä vähentää ohjeiden suoritusaikaa huomattavasti.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="c0ebb-142">Myyntitilaus-kenttä on valinnainen – voit käsitellä kaikki yhden ohjelman tilaukset.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="c0ebb-143">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c0ebb-143">Click OK.</span></span>

