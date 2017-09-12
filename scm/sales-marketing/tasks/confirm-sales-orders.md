--- 
title: Vahvista myyntitilaukset
description: "Seuraavassa menettelyssä selvitetään, miten myyntitilaukset vahvistetaan."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7cab69222c5004e6a62c632a9e85085403434ffd
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="confirm-sales-orders"></a><span data-ttu-id="a93dc-103">Vahvista myyntitilaukset</span><span class="sxs-lookup"><span data-stu-id="a93dc-103">Confirm sales orders</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a93dc-104">Seuraavassa menettelyssä selvitetään, miten myyntitilaukset vahvistetaan.</span><span class="sxs-lookup"><span data-stu-id="a93dc-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="a93dc-105">Näet, miten yksi tilaus vahvistetaan. Näet myös, miten useita tilauksia voi vahvistaa samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="a93dc-105">You’ll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="a93dc-106">Yleensä myyntitilauksen käsittelijä tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="a93dc-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="a93dc-107">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="a93dc-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="a93dc-108">Varmista ennen aloittamista, että samalla asiakkaalla on useita avoimia myyntitilauksia.</span><span class="sxs-lookup"><span data-stu-id="a93dc-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="a93dc-109">Jos käytössä on USMF, käytä asiakasta US-027.</span><span class="sxs-lookup"><span data-stu-id="a93dc-109">If you’re using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="a93dc-110">Vahvista yksi myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="a93dc-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="a93dc-111">Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="a93dc-111">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="a93dc-112">Etsi ja valitse luettelosta vahvistettava tilaus.</span><span class="sxs-lookup"><span data-stu-id="a93dc-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="a93dc-113">Avaa valittu tilaus napsauttamalla myyntitilauksen numeron linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a93dc-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="a93dc-114">Valitse toimintoruudussa Myynti.</span><span class="sxs-lookup"><span data-stu-id="a93dc-114">On the Action Pane, click Sell.</span></span>
5. <span data-ttu-id="a93dc-115">Valitse Vahvista myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="a93dc-115">Click Confirm sales order.</span></span>
6. <span data-ttu-id="a93dc-116">Laajenna tai tiivistä Parametrit-osa.</span><span class="sxs-lookup"><span data-stu-id="a93dc-116">Expand or collapse the Parameters section.</span></span>
    * <span data-ttu-id="a93dc-117">Varmista, että kirjauksen Kyllä-kenttä on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="a93dc-117">Make sure that the Posting Yes field is active.</span></span>  
7. <span data-ttu-id="a93dc-118">Valitse Tulosta vahvistus -vaihtoehdoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="a93dc-118">Set the Print confirmation option to Yes.</span></span>
    * <span data-ttu-id="a93dc-119">Tarkista luottoraja -kenttä määrittää menetelmän, jolla asiakkaan jäljellä oleva luotto lasketaan.</span><span class="sxs-lookup"><span data-stu-id="a93dc-119">The Check credit limit field specifies the method that’s used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="a93dc-120">Oletusarvoisesti se kopioidaan Myyntireskontran parametrit -sivulta.</span><span class="sxs-lookup"><span data-stu-id="a93dc-120">By default, it’s copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="a93dc-121">Jos haluat ohittaa luottorajatarkistuksen tietyn myyntitilauksen vahvistuksessa, valitse Tarkista luottoraja -arvoksi Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="a93dc-121">If you want to skip the credit limit check when confirming a specific sales order, set the Check credit limit to None.</span></span> <span data-ttu-id="a93dc-122">Muista kuitenkin, että vaikka tämän kentän arvo on Ei mitään, luottorajatarkistus suoritetaan, jos asiakkaan päätiedoissa on valittu Pakollinen luottoraja -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="a93dc-122">However, you should be aware that even with if this field is set to None, the credit limit check will still be performed if the Mandatory credit limit option is selected on the customer master data.</span></span>  
8. <span data-ttu-id="a93dc-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a93dc-123">Click OK.</span></span>
9. <span data-ttu-id="a93dc-124">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="a93dc-124">Click Yes.</span></span>
10. <span data-ttu-id="a93dc-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a93dc-125">Close the page.</span></span>
11. <span data-ttu-id="a93dc-126">Valitse toimintoruudussa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="a93dc-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="a93dc-127">Valitse Vaihda näkymä.</span><span class="sxs-lookup"><span data-stu-id="a93dc-127">Click Change view.</span></span>
13. <span data-ttu-id="a93dc-128">Valitse Otsikkonäkymä.</span><span class="sxs-lookup"><span data-stu-id="a93dc-128">Click Header view.</span></span>
    * <span data-ttu-id="a93dc-129">Kun tilaus on vahvistettu, asiakirjan tilaksi määritetään Vahvistus.</span><span class="sxs-lookup"><span data-stu-id="a93dc-129">When an order is confirmed, the Document status is set to Confirmation.</span></span>  
14. <span data-ttu-id="a93dc-130">Valitse toimintoruudussa Myynti.</span><span class="sxs-lookup"><span data-stu-id="a93dc-130">On the Action Pane, click Sell.</span></span>
15. <span data-ttu-id="a93dc-131">Valitse Myyntitilausvahvistus.</span><span class="sxs-lookup"><span data-stu-id="a93dc-131">Click Sales order confirmation.</span></span>
16. <span data-ttu-id="a93dc-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a93dc-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="a93dc-133">Vahvista useita myyntitilauksia samanaikaisesti</span><span class="sxs-lookup"><span data-stu-id="a93dc-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="a93dc-134">Valitse Myynti ja markkinointi > Myyntitilaukset > Tilausvahvistus > Vahvista myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="a93dc-134">Go to Sales and marketing > Sales orders > Order confirmation > Confirm sales order.</span></span>
2. <span data-ttu-id="a93dc-135">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="a93dc-135">Click Select.</span></span>
3. <span data-ttu-id="a93dc-136">Etsi ja valitse Alueet-välilehdessä tietue, joka viittaa Asiakastili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a93dc-136">In the list on the Range tab, find and select the record that references the Customer account field.</span></span>
4. <span data-ttu-id="a93dc-137">Avaa haku valitsemalla Ehdot-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a93dc-137">In the Criteria field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a93dc-138">Etsi ja valitse luettelosta asiakastili, jossa on useita tilauksia, jotka haluat joukkovahvistaa.</span><span class="sxs-lookup"><span data-stu-id="a93dc-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span>
    * <span data-ttu-id="a93dc-139">Jos käytössä on USMF, voit valita tilin US-027.</span><span class="sxs-lookup"><span data-stu-id="a93dc-139">If you’re using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="a93dc-140">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a93dc-140">Click OK.</span></span>
    * <span data-ttu-id="a93dc-141">Yhteenveto-välilehdessä on luettelo kyselyehtoja vastaavista tilauksista.</span><span class="sxs-lookup"><span data-stu-id="a93dc-141">The Overview tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="a93dc-142">Ne sisältyvät vahvistukseen.</span><span class="sxs-lookup"><span data-stu-id="a93dc-142">These will be included in the confirmation.</span></span>  
    * <span data-ttu-id="a93dc-143">Päivitysyhteenveto mille: -kenttä määrittää parametrin, jonka mukaan useista tilauksista tehdään yhteenveto yhteen vahvistusasiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="a93dc-143">The Summary update for field specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="a93dc-144">Oletusarvoisesti asetus kopioidaan Myyntireskontran parametrit -sivun Päivitysyhteenvedon oletusarvot -asetuksesta.</span><span class="sxs-lookup"><span data-stu-id="a93dc-144">By default, the option is copied from the Default values for summary update setting on the Accounts receivable parameters page.</span></span>  
7. <span data-ttu-id="a93dc-145">Valitse Päivitysyhteenveto mille: -kentässä Tilaus.</span><span class="sxs-lookup"><span data-stu-id="a93dc-145">In the Summary update for field, select 'Order'.</span></span>
    * <span data-ttu-id="a93dc-146">Yhteenvetopäivitysten luontiin tarvitaan ainakin parametrit Laskutustili ja Valuutta.</span><span class="sxs-lookup"><span data-stu-id="a93dc-146">The minimum parameters that are required to create summary updates are Invoice account and Currency.</span></span> <span data-ttu-id="a93dc-147">Näin ollen yhteenvetopäivityksiä, joissa on eri laskutustilit ja valuutat, ei sallita.</span><span class="sxs-lookup"><span data-stu-id="a93dc-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="a93dc-148">Yhteenvedon päivitysparametrit -sivulla voi määrittää lisäparametreja. Sivun voi avata Myyntireskontran parametrit -sivulta.</span><span class="sxs-lookup"><span data-stu-id="a93dc-148">Additional parameters can be set up in the Summary update parameters page which is accessible from the Accounts receivable parameters page.</span></span>  
8. <span data-ttu-id="a93dc-149">Avaa haku napsauttamalla Myyntitilaus-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="a93dc-149">In the Sales order field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a93dc-150">Valitse luettelossa tilausnumero, jonka haluat yhteenvetotilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="a93dc-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="a93dc-151">Valitse Järjestä.</span><span class="sxs-lookup"><span data-stu-id="a93dc-151">Click Arrange.</span></span>
11. <span data-ttu-id="a93dc-152">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a93dc-152">Click OK.</span></span>
12. <span data-ttu-id="a93dc-153">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a93dc-153">Click OK.</span></span>


