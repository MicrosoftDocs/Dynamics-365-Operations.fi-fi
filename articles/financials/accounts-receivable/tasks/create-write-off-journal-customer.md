--- 
title: Poiskirjauksen kirjauskansion luominen asiakkaalle
description: "Tässä tehtävän ohjauksessa näytetään, miten poiston parametrit määritetään. Ohjauksessa kerrotaan myös, miten Perintä-, Avoimet myyntilaskut- ja Asiakas-sivun poistotapahtumat määritetään."
author: ShivamPandey-msft
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
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c90ff4abd343936612866b07577062fe1814085b
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="9d233-103">Poiskirjauksen kirjauskansion luominen asiakkaalle</span><span class="sxs-lookup"><span data-stu-id="9d233-103">Create a write-off journal for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9d233-104">Tässä tehtävän ohjauksessa näytetään, miten poiston parametrit määritetään. Ohjauksessa kerrotaan myös, miten Perintä-, Avoimet myyntilaskut- ja Asiakas-sivun poistotapahtumat määritetään.</span><span class="sxs-lookup"><span data-stu-id="9d233-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="9d233-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="9d233-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="9d233-106">Poiston parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9d233-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="9d233-107">Siirry kohtaan Luotonvalvonta > Asetukset > Myyntireskontran parametrit.</span><span class="sxs-lookup"><span data-stu-id="9d233-107">Go to Credit and collections > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="9d233-108">Valitse Perintä-välilehti.</span><span class="sxs-lookup"><span data-stu-id="9d233-108">Click the Collections tab.</span></span>
3. <span data-ttu-id="9d233-109">Laajenna tai tiivistä Poisto-osa.</span><span class="sxs-lookup"><span data-stu-id="9d233-109">Expand or collapse the Write-off section.</span></span>
    * <span data-ttu-id="9d233-110">Poiston kirjauskansio on yleinen kirjauskansio, joka sisältää luomasi poistotapahtumat.</span><span class="sxs-lookup"><span data-stu-id="9d233-110">The Write-off journal is the general journal that will hold the write-off transactions that you create.</span></span>  
    * <span data-ttu-id="9d233-111">Voit liittää jokaiseen poistoon syykoodin.</span><span class="sxs-lookup"><span data-stu-id="9d233-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="9d233-112">Voit korvata tämän oletusarvon poiston yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="9d233-112">You can override this default at the time of the write-off.</span></span>  
    * <span data-ttu-id="9d233-113">Määritä tämän kohdan arvoksi Kyllä, jos haluat erottaa arvonlisäveron alkuperäisestä tapahtumasta poistossa.</span><span class="sxs-lookup"><span data-stu-id="9d233-113">Set this to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="9d233-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9d233-114">Close the page.</span></span>
5. <span data-ttu-id="9d233-115">Siirry kohtaan Luotonvalvonta > Asetukset > Asiakkaan kirjausprofiilit.</span><span class="sxs-lookup"><span data-stu-id="9d233-115">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
    * <span data-ttu-id="9d233-116">Poistotiliä käytetään kulutilinä tai varauksen oikaisuna yleisessä kirjauskansiossa</span><span class="sxs-lookup"><span data-stu-id="9d233-116">The write-off account will be used as the expense account or reserve adjustment in the general journal</span></span>   
6. <span data-ttu-id="9d233-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9d233-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="9d233-118">Asiakkaan saldon poiskirjaus erääntyneiden saldojen sivulla</span><span class="sxs-lookup"><span data-stu-id="9d233-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="9d233-119">Siirry kohtaan Luotonvalvonta > Perintä > Erääntyneet saldot.</span><span class="sxs-lookup"><span data-stu-id="9d233-119">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="9d233-120">Merkitse se asiakkaan rivi, jonka haluat poistaa.</span><span class="sxs-lookup"><span data-stu-id="9d233-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="9d233-121">Merkitse esimerkiksi rivi, jolla on Birch-niminen yritys.</span><span class="sxs-lookup"><span data-stu-id="9d233-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="9d233-122">Valitse toimintoruudussa Perintä.</span><span class="sxs-lookup"><span data-stu-id="9d233-122">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="9d233-123">Valitse Poisto.</span><span class="sxs-lookup"><span data-stu-id="9d233-123">Click Write off.</span></span>
5. <span data-ttu-id="9d233-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9d233-124">Click OK.</span></span>
6. <span data-ttu-id="9d233-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9d233-125">Close the page.</span></span>
7. <span data-ttu-id="9d233-126">Siirry kohtaan Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="9d233-126">Go to General ledger > Journal entries > General journals.</span></span>
8. <span data-ttu-id="9d233-127">Valitse poiston sisältävän kirjauskansion eränumero.</span><span class="sxs-lookup"><span data-stu-id="9d233-127">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="9d233-128">Yksi rivi luodaan asiakkaan saldon palauttamiseksi.</span><span class="sxs-lookup"><span data-stu-id="9d233-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="9d233-129">Yksi tai useita rivejä luodaan poiston kirjaamiseksi poistotilille.</span><span class="sxs-lookup"><span data-stu-id="9d233-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="9d233-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9d233-130">Close the page.</span></span>
10. <span data-ttu-id="9d233-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9d233-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="9d233-132">Kirjaa pois tapahtumia perintälomakkeelta.</span><span class="sxs-lookup"><span data-stu-id="9d233-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="9d233-133">Siirry kohtaan Luotonvalvonta > Perintä > Erääntyneet saldot.</span><span class="sxs-lookup"><span data-stu-id="9d233-133">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="9d233-134">Valitse sen asiakkaan nimi, jolla on poistettavia tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="9d233-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="9d233-135">Valitse esimerkiksi Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="9d233-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="9d233-136">Merkitse rivi ensimmäistä tapahtumaa varten.</span><span class="sxs-lookup"><span data-stu-id="9d233-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="9d233-137">Merkitse rivi toista tapahtumaa varten.</span><span class="sxs-lookup"><span data-stu-id="9d233-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="9d233-138">Valitse Poisto.</span><span class="sxs-lookup"><span data-stu-id="9d233-138">Click Write off.</span></span>
6. <span data-ttu-id="9d233-139">Syötä Syyn kommentti -kenttään Luottotappio.</span><span class="sxs-lookup"><span data-stu-id="9d233-139">In the Reason comment field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="9d233-140">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9d233-140">Click OK.</span></span>
8. <span data-ttu-id="9d233-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9d233-141">Close the page.</span></span>
9. <span data-ttu-id="9d233-142">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9d233-142">Close the page.</span></span>
10. <span data-ttu-id="9d233-143">Siirry kohtaan Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="9d233-143">Go to General ledger > Journal entries > General journals.</span></span>
11. <span data-ttu-id="9d233-144">Valitse poiston sisältävän kirjauskansion eränumero.</span><span class="sxs-lookup"><span data-stu-id="9d233-144">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="9d233-145">Yksi rivi luodaan asiakkaan saldon palauttamiseksi.</span><span class="sxs-lookup"><span data-stu-id="9d233-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="9d233-146">Yksi tai useita rivejä luodaan poiston kirjaamiseksi poistotilille.</span><span class="sxs-lookup"><span data-stu-id="9d233-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="9d233-147">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9d233-147">Close the page.</span></span>
13. <span data-ttu-id="9d233-148">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9d233-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="9d233-149">Laskun poiskirjaus Avoimet myyntilaskut -sivulta</span><span class="sxs-lookup"><span data-stu-id="9d233-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="9d233-150">Siirry kohtaan Myyntireskontra > Laskut > Avoimet myyntilaskut.</span><span class="sxs-lookup"><span data-stu-id="9d233-150">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="9d233-151">Merkitse laskun rivi.</span><span class="sxs-lookup"><span data-stu-id="9d233-151">Mark the line for an invoice.</span></span> <span data-ttu-id="9d233-152">Voit esimerkiksi merkitä kohteen CIV-000667 rivin.</span><span class="sxs-lookup"><span data-stu-id="9d233-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="9d233-153">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="9d233-153">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="9d233-154">Valitse Poisto.</span><span class="sxs-lookup"><span data-stu-id="9d233-154">Click Write off.</span></span>
5. <span data-ttu-id="9d233-155">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9d233-155">Click OK.</span></span>
6. <span data-ttu-id="9d233-156">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9d233-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="9d233-157">Asiakkaan saldon poiskirjaus Asiakas-sivulta</span><span class="sxs-lookup"><span data-stu-id="9d233-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="9d233-158">Siirry kohtaan Myyntireskontra > Asiakkaat > Kaikki asiakkaat.</span><span class="sxs-lookup"><span data-stu-id="9d233-158">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="9d233-159">Valitse asiakastili.</span><span class="sxs-lookup"><span data-stu-id="9d233-159">Select a customer account.</span></span> <span data-ttu-id="9d233-160">Valitse esimerkiksi US-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="9d233-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="9d233-161">Valitse toimintoruudussa Perintä.</span><span class="sxs-lookup"><span data-stu-id="9d233-161">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="9d233-162">Valitse Poisto.</span><span class="sxs-lookup"><span data-stu-id="9d233-162">Click Write off.</span></span>
5. <span data-ttu-id="9d233-163">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9d233-163">Click OK.</span></span>
6. <span data-ttu-id="9d233-164">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9d233-164">Close the page.</span></span>


