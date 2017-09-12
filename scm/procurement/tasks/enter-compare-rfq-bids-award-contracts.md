--- 
title: "Syötä ja vertaa tarjouspyyntöjä ja myönnä sopimuksia"
description: "Seuraavassa menettelyssä kuvataan tarjouspyynnön vastauksien kirjoittaminen, tarjousten pisteytys ja vertailu, sekä tarjouksen antaminen yhdelle toimittajista."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5dea9d7bfb1bf7b11f6c49cccaab1b73d4e58d16
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="46d1e-103">Syötä ja vertaa tarjouspyyntöjä ja myönnä sopimuksia</span><span class="sxs-lookup"><span data-stu-id="46d1e-103">Enter and compare RFQ bids and award contracts</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46d1e-104">Seuraavassa menettelyssä kuvataan tarjouspyynnön vastauksien kirjoittaminen, tarjousten pisteytys ja vertailu, sekä tarjouksen antaminen yhdelle toimittajista.</span><span class="sxs-lookup"><span data-stu-id="46d1e-104">This procedure shows you how to enter replies to an RFQ, score and compare bids, and then award the bid to one of the vendors.</span></span> <span data-ttu-id="46d1e-105">Voit käyttää tätä menettelyä esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="46d1e-105">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="46d1e-106">Ennen kuin aloitat, varmista, että sinulla on tarjouspyyntö, joka sisältää kaksi riviä ja joka on lähetetty vähintään kahdelle toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="46d1e-106">Before you start, you must have an RFQ with two lines that has been sent to at least two vendors.</span></span> <span data-ttu-id="46d1e-107">Voit ajaa "Luo tarjouspyyntö" -toimintosarjan luodaksesi tämän edellytyksen.</span><span class="sxs-lookup"><span data-stu-id="46d1e-107">You can run the "Create a request for quotation" procedure as a prerequisite to create this.</span></span> <span data-ttu-id="46d1e-108">Pisteytysehdot on määritettävä ennen tämän menettelyn suorittamista.</span><span class="sxs-lookup"><span data-stu-id="46d1e-108">You need to have set up scoring criteria before you can run this procedure.</span></span>


## <a name="enter-a-reply-from-a-vendor"></a><span data-ttu-id="46d1e-109">Kirjoita toimittajan vastaus</span><span class="sxs-lookup"><span data-stu-id="46d1e-109">Enter a reply from a vendor</span></span>
1. <span data-ttu-id="46d1e-110">Valitse Hankinta > Tarjouspyynnöt > Kaikki tarjouspyynnöt.</span><span class="sxs-lookup"><span data-stu-id="46d1e-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="46d1e-111">Valitse tarjouspyyntö, jonka tila on lähetetty ja napsauta tarjouspyynnön tapausnumeron linkkiä.</span><span class="sxs-lookup"><span data-stu-id="46d1e-111">Select an RFQ that has a status of Sent and click the link on the Request for quotation case number.</span></span>
    * <span data-ttu-id="46d1e-112">Tarjouspyyntö tulisi lähettää vähintään 2 toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="46d1e-112">The RFQ should have been sent to at least 2 vendors.</span></span>  
3. <span data-ttu-id="46d1e-113">Napsauta otsikkoa siirtyäksesi toimittajien luetteloon.</span><span class="sxs-lookup"><span data-stu-id="46d1e-113">Click Header to go to the list of vendors.</span></span>
4. <span data-ttu-id="46d1e-114">Valitse toimittaja, jolle haluat kirjoittaa vastauksen tarjouspyyntöön.</span><span class="sxs-lookup"><span data-stu-id="46d1e-114">Select the vendor for whom you want to enter a response on the RFQ.</span></span>
5. <span data-ttu-id="46d1e-115">Napsauta Kirjoita vastaus -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="46d1e-115">Click Enter reply.</span></span>
6. <span data-ttu-id="46d1e-116">Valitse toimintoruudussa Vastaa.</span><span class="sxs-lookup"><span data-stu-id="46d1e-116">On the Action Pane, click Reply.</span></span>
7. <span data-ttu-id="46d1e-117">Napsauta Kopioi tiedot vastauskenttiin -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="46d1e-117">Click Copy data to reply.</span></span>
    * <span data-ttu-id="46d1e-118">Toiminto kopioi valitut tiedot, esimerkiksi määrän tarjouspyynnön tapauksesta tarjouspyynnön vastaukseen.</span><span class="sxs-lookup"><span data-stu-id="46d1e-118">This action will copy selected data, for example, the quantity from the RFQ case to the RFQ reply.</span></span> <span data-ttu-id="46d1e-119">Voit ohittaa tämän toiminnon ja täyttää vastauskentät manuaalisesti, kun muokkaat vastausta.</span><span class="sxs-lookup"><span data-stu-id="46d1e-119">Alternatively you can skip this action and fill in all the response fields manually when you edit the reply.</span></span>  
8. <span data-ttu-id="46d1e-120">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="46d1e-120">Click Edit.</span></span>
9. <span data-ttu-id="46d1e-121">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="46d1e-121">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="46d1e-122">Valitse toinen tarjousrivi.</span><span class="sxs-lookup"><span data-stu-id="46d1e-122">Choose the other quotation line.</span></span>
11. <span data-ttu-id="46d1e-123">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="46d1e-123">In the Unit price field, enter a number.</span></span>

## <a name="score-the-bid"></a><span data-ttu-id="46d1e-124">Pisteytä tarjous</span><span class="sxs-lookup"><span data-stu-id="46d1e-124">Score the bid</span></span>
1. <span data-ttu-id="46d1e-125">Napsauta otsikkoa siirtyäksesi tarjouksen pisteytykseen.</span><span class="sxs-lookup"><span data-stu-id="46d1e-125">Click Header to go to the scoring of the bid.</span></span>
2. <span data-ttu-id="46d1e-126">Laajenna Tarjouksen pisteytys -osa.</span><span class="sxs-lookup"><span data-stu-id="46d1e-126">Expand the Bid scoring section.</span></span>
3. <span data-ttu-id="46d1e-127">Kirjoita Tulos-kenttään jokin pisteytysehdon numero.</span><span class="sxs-lookup"><span data-stu-id="46d1e-127">In the Score field, enter a number for one of the scoring criteria.</span></span>
    * <span data-ttu-id="46d1e-128">Jos pidät kohdistinta pisteytysperusteen yllä, työkaluvihjeen näyttää alueen, jolle pisteytys on annettava.</span><span class="sxs-lookup"><span data-stu-id="46d1e-128">If you hover over one of the scoring criteria a tooltip shows the range that you have to score within.</span></span> <span data-ttu-id="46d1e-129">Tässä demossa voit lisätä numeron väliltä 1-5 mihin tahansa perusteeseen.</span><span class="sxs-lookup"><span data-stu-id="46d1e-129">In this demo you can add a number between 1 and 5 to any of the criteria.</span></span>  
4. <span data-ttu-id="46d1e-130">Valitse toinen pisteytysehto.</span><span class="sxs-lookup"><span data-stu-id="46d1e-130">Select another scoring criterion.</span></span>
5. <span data-ttu-id="46d1e-131">Kirjoita Tulos-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="46d1e-131">In the Score field, enter a number.</span></span>
6. <span data-ttu-id="46d1e-132">Laajenna Kyselylomakkeet-osa.</span><span class="sxs-lookup"><span data-stu-id="46d1e-132">Expand the Questionnaires section.</span></span>
    * <span data-ttu-id="46d1e-133">Jos tarjouspyynnön tapauksessa on kyselylomake, joka on lähetetty toimittajille, voit kirjoittaa vastaukset kyselylomakkeen osaan.</span><span class="sxs-lookup"><span data-stu-id="46d1e-133">If the RFQ case has a questionnaire that was sent to the vendors, you can enter their responses in the questionnaire section.</span></span>  
7. <span data-ttu-id="46d1e-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="46d1e-134">Close the page.</span></span>

## <a name="enter-a-reply-for-another-vendor"></a><span data-ttu-id="46d1e-135">Kirjoita toisen toimittajan vastaus</span><span class="sxs-lookup"><span data-stu-id="46d1e-135">Enter a reply for another vendor</span></span>
1. <span data-ttu-id="46d1e-136">Valitse seuraava toimittaja poistamalla kentästä se toimittaja,jolle olet kirjoittanut vastauksen ja valitsemalla sitten seuraavan toimittajan rivi.</span><span class="sxs-lookup"><span data-stu-id="46d1e-136">Select the next vendor by clearing the vendor you have just entered the reply for and then selecting the row for the next vendor.</span></span>
2. <span data-ttu-id="46d1e-137">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="46d1e-137">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="46d1e-138">Napsauta Kirjoita vastaus -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="46d1e-138">Click Enter reply.</span></span>
4. <span data-ttu-id="46d1e-139">Napsauta Kopioi tiedot vastauskenttiin -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="46d1e-139">Click Copy data to reply.</span></span>
5. <span data-ttu-id="46d1e-140">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="46d1e-140">Click Edit.</span></span>
6. <span data-ttu-id="46d1e-141">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="46d1e-141">In the Unit price field, enter a number.</span></span>
7. <span data-ttu-id="46d1e-142">Valitse toinen tarjousrivi.</span><span class="sxs-lookup"><span data-stu-id="46d1e-142">Choose the other quotation line.</span></span>
8. <span data-ttu-id="46d1e-143">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="46d1e-143">In the Unit price field, enter a number.</span></span>

## <a name="score-the-second-bid"></a><span data-ttu-id="46d1e-144">Pisteytä toinen tarjous</span><span class="sxs-lookup"><span data-stu-id="46d1e-144">Score the second bid</span></span>
1. <span data-ttu-id="46d1e-145">Napsauta otsikkoa siirtyäksesi tarjouksen pisteytykseen.</span><span class="sxs-lookup"><span data-stu-id="46d1e-145">Click Header to go to scoring of the bid.</span></span>
2. <span data-ttu-id="46d1e-146">Kirjoita Tulos-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="46d1e-146">In the Score field, enter a number.</span></span>
3. <span data-ttu-id="46d1e-147">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="46d1e-147">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="46d1e-148">Kirjoita Tulos-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="46d1e-148">In the Score field, enter a number.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="46d1e-149">Vertaa vastauksia</span><span class="sxs-lookup"><span data-stu-id="46d1e-149">Compare the replies</span></span>
1. <span data-ttu-id="46d1e-150">Valitse toimintoruudussa Yleiset.</span><span class="sxs-lookup"><span data-stu-id="46d1e-150">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="46d1e-151">Napsauta Vertaa vastauksia -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="46d1e-151">Click Compare replies.</span></span>
3. <span data-ttu-id="46d1e-152">Kirjoita Sijoitus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="46d1e-152">In the Rank field, enter a number.</span></span>
    * <span data-ttu-id="46d1e-153">Tällä sivulla näytetään tarjoukset otsikossa ja riveillä, ja kokonaispistemäärä otsikon tasolla.</span><span class="sxs-lookup"><span data-stu-id="46d1e-153">This page shows the bids with the header and lines, and the total score on the header level.</span></span> <span data-ttu-id="46d1e-154">Voit verrata rivejä lajittelemalla ruudukon siten, että vertailtavat rivit ovat vierekkäin.</span><span class="sxs-lookup"><span data-stu-id="46d1e-154">You can compare the lines by sorting in the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="46d1e-155">Tietoihin sisältyy myös: Määrä: toimittajan tarjoama määrä.</span><span class="sxs-lookup"><span data-stu-id="46d1e-155">The information also includes:   Quantity: The quantity quoted by the vendor.</span></span> <span data-ttu-id="46d1e-156">Tämä määrä ei ehkä vastaa tarjouspyynnössä määritettyä määrää.</span><span class="sxs-lookup"><span data-stu-id="46d1e-156">This might not equal the quantity specified in the RFQ.</span></span>   <span data-ttu-id="46d1e-157">Nettosumma: Toimittajan tarjouksen hinta rivin nimikkeistä alennusten vähentämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="46d1e-157">Net amount: The price quoted by a vendor, after subtracting any discounts, for the items on the line.</span></span>   <span data-ttu-id="46d1e-158">Poikkeama: Päivien määrä, jonka verran tarjouksen otsikon tai rivin toimituspäivämäärä poikkeaa tarjouspyynnön otsikon tai tarjouspyynnön rivin pyydetystä toimituspäivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="46d1e-158">Deviation: The number of days that the delivery date in the bid header or line deviates from the requested delivery date in the RFQ header or RFQ line.</span></span>   <span data-ttu-id="46d1e-159">Voit määrittää kullekin tarjoukselle sijoituksen.</span><span class="sxs-lookup"><span data-stu-id="46d1e-159">You can enter a rank for each bid.</span></span>  
4. <span data-ttu-id="46d1e-160">Valitse sijoitettavan tarjouksen otsikkorivi.</span><span class="sxs-lookup"><span data-stu-id="46d1e-160">Select the header line for the other bid that you want to rank.</span></span>
5. <span data-ttu-id="46d1e-161">Kirjoita Sijoitus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="46d1e-161">In the Rank field, enter a number.</span></span>
6. <span data-ttu-id="46d1e-162">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="46d1e-162">Click Save.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="46d1e-163">Hylkää tarjous</span><span class="sxs-lookup"><span data-stu-id="46d1e-163">Reject a bid</span></span>
1. <span data-ttu-id="46d1e-164">Valitse hylättävän tarjouksen otsikkorivi.</span><span class="sxs-lookup"><span data-stu-id="46d1e-164">Select the header line for the bid that you want to reject.</span></span>
    * <span data-ttu-id="46d1e-165">Voit hyväksyä, hylätä tai palauttaa vain yhden tarjouksen tai yhden tarjouksen rivejä kerralla.</span><span class="sxs-lookup"><span data-stu-id="46d1e-165">You can only accept, reject, or return one bid or lines within one bid at a time.</span></span>  
2. <span data-ttu-id="46d1e-166">Valitse Merkitse-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="46d1e-166">Select the Mark check box.</span></span>
    * <span data-ttu-id="46d1e-167">Jos valitset Merkitse-valintaruudun tarjouksen otsikossa, kaikki tarjouksen rivit merkitään lisäksi.</span><span class="sxs-lookup"><span data-stu-id="46d1e-167">If you select the Mark check box on the Header of the bid then all the lines will be marked as well.</span></span> <span data-ttu-id="46d1e-168">Voit myös merkitä osan tarjouksen riveistä hylättäväksi tai hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="46d1e-168">You could also choose to mark a subset of the lines within the bid to reject or accept those.</span></span> <span data-ttu-id="46d1e-169">On mahdollista hyväksyä yhden toimittajan tarjous tietyille tarjouspyynnön riveille ja antaa muut tarjouspyynnön rivit toiselle toimittajalle; tämä on kuitenkin tehtävä 2 vaiheessa, yksi tarjous kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="46d1e-169">It’s possible to accept one vendor’s bid for some lines of an RFQ, and then award other RFQ lines to a different vendor, however you need to do this in 2 steps, one bid at a time.</span></span> <span data-ttu-id="46d1e-170">Jos on olemassa vaihtoehtoisia rivejä, voit hyväksyä vain joko alkuperäisen tarjousrivin tai sen vaihtoehdon, mutta et molempia.</span><span class="sxs-lookup"><span data-stu-id="46d1e-170">If alternate lines are present, you can only accept either the original bid line or its alternate, but not both.</span></span>  
3. <span data-ttu-id="46d1e-171">Napsauta Hylkää.</span><span class="sxs-lookup"><span data-stu-id="46d1e-171">Click Reject.</span></span>
4. <span data-ttu-id="46d1e-172">Avaa valintaikkuna valitsemalla Parametrit.</span><span class="sxs-lookup"><span data-stu-id="46d1e-172">Click Parameters to open the drop dialog.</span></span>
5. <span data-ttu-id="46d1e-173">Anna tai valitse Hylkäyksen syy -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="46d1e-173">In the Reason reject field, enter or select a value.</span></span>
    * <span data-ttu-id="46d1e-174">Vastaukseen tallennetaan hylkäyksen syy.</span><span class="sxs-lookup"><span data-stu-id="46d1e-174">The reason for rejection will be stored on the reply.</span></span>  
6. <span data-ttu-id="46d1e-175">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="46d1e-175">Click OK.</span></span>
7. <span data-ttu-id="46d1e-176">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="46d1e-176">Click OK.</span></span>
8. <span data-ttu-id="46d1e-177">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="46d1e-177">Close the page.</span></span>
9. <span data-ttu-id="46d1e-178">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="46d1e-178">Close the page.</span></span>
10. <span data-ttu-id="46d1e-179">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="46d1e-179">Refresh the page.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="46d1e-180">Hyväksy tarjous</span><span class="sxs-lookup"><span data-stu-id="46d1e-180">Accept a bid</span></span>
1. <span data-ttu-id="46d1e-181">Valitse tarjous, jonka haluat hyväksyä ja napsauta sitten tarjouspyyntökentän linkkiä.</span><span class="sxs-lookup"><span data-stu-id="46d1e-181">Select the bid that you want to accept and then click the link in the Request for quotation field.</span></span>
2. <span data-ttu-id="46d1e-182">Valitse toimintoruudussa Vastaa.</span><span class="sxs-lookup"><span data-stu-id="46d1e-182">On the Action Pane, click Reply.</span></span>
3. <span data-ttu-id="46d1e-183">Valitse Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="46d1e-183">Click Accept.</span></span>
    * <span data-ttu-id="46d1e-184">Jos olet merkinnyt tiettyjä rivejä mutta jättänyt muita merkitsemättä, Hyväksy-toimenpide sisältää vain merkityt rivit.</span><span class="sxs-lookup"><span data-stu-id="46d1e-184">If you have marked specific lines and not others then the accept action will only include the marked lines.</span></span> <span data-ttu-id="46d1e-185">Voit hyväksyä kaikki tarjouksen rivit merkitsemättä niitä.</span><span class="sxs-lookup"><span data-stu-id="46d1e-185">If you want to accept all lines on the bid then you do not have to mark the lines.</span></span>  
4. <span data-ttu-id="46d1e-186">Avaa valintaikkuna valitsemalla Parametrit.</span><span class="sxs-lookup"><span data-stu-id="46d1e-186">Click Parameters to open the drop dialog.</span></span>
    * <span data-ttu-id="46d1e-187">Voit kirjata syyn tarjouksen hyväksynnälle.</span><span class="sxs-lookup"><span data-stu-id="46d1e-187">This allows you to record a reason for accepting the bid.</span></span> <span data-ttu-id="46d1e-188">Syy tallennetaan tarjoukseen.</span><span class="sxs-lookup"><span data-stu-id="46d1e-188">The reason will be stored on the bid.</span></span>  
5. <span data-ttu-id="46d1e-189">Anna tai valitse Hyväksynnän syy -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="46d1e-189">In the Reason accept field, enter or select a value.</span></span>
6. <span data-ttu-id="46d1e-190">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="46d1e-190">Click OK.</span></span>
7. <span data-ttu-id="46d1e-191">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="46d1e-191">Click OK.</span></span>
    * <span data-ttu-id="46d1e-192">Kun napsautat OK, järjestelmä luo ostotilauksen tarjouspyynnössä hyväksyttyjen rivien perusteella..</span><span class="sxs-lookup"><span data-stu-id="46d1e-192">When you click OK this generates a purchase order based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="46d1e-193">Jos tarjouspyynnöllä on muita tarjouksia, joita ei ole käsitelty (hyväksytty, hylätty tai palautettu), järjestelmä kehottaa hylkäämään jäljellä olevat tarjoukset.</span><span class="sxs-lookup"><span data-stu-id="46d1e-193">If there are other bids that have not been processed (accepted, rejected, or returned) then the system will prompt you to reject the remaining bids.</span></span>  

## <a name="view-the-purchase-order-thats-been-generated"></a><span data-ttu-id="46d1e-194">Näytä luotu ostotilaus</span><span class="sxs-lookup"><span data-stu-id="46d1e-194">View the purchase order that's been generated</span></span>
1. <span data-ttu-id="46d1e-195">Valitse toimintoruudussa Yleiset.</span><span class="sxs-lookup"><span data-stu-id="46d1e-195">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="46d1e-196">Valitse Ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="46d1e-196">Click Purchase order.</span></span>
    * <span data-ttu-id="46d1e-197">Tässä kentässä näet ostotilauksen, joka luotiin, kun hyväksyit tarjouksen.</span><span class="sxs-lookup"><span data-stu-id="46d1e-197">Here you can see the purchase order that was generated when you accepted the bid.</span></span>  
3. <span data-ttu-id="46d1e-198">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="46d1e-198">Close the page.</span></span>
4. <span data-ttu-id="46d1e-199">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="46d1e-199">Close the page.</span></span>
5. <span data-ttu-id="46d1e-200">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="46d1e-200">Close the page.</span></span>
6. <span data-ttu-id="46d1e-201">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="46d1e-201">Close the page.</span></span>


