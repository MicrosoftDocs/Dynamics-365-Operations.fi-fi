--- 
title: "Myönnä EU-saapumistodistus"
description: "Tässä menettelyssä selvitetään, miten EU-saapumistodistus otetaan käyttöön, miten asiakastiliä muutetaan varmenteiden käyttöä varten ja miten varmenne myönnetään."
author: mrolecki
manager: AnnBe
ms.date: 02/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ff00ff0df3835ee2cbf21219ad6f07bfeba6e7ac
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="issue-an-eu-entry-certificate"></a><span data-ttu-id="fcdac-103">Myönnä EU-saapumistodistus</span><span class="sxs-lookup"><span data-stu-id="fcdac-103">Issue an EU entry certificate</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fcdac-104">Tässä menettelyssä selvitetään, miten EU-saapumistodistus otetaan käyttöön, miten asiakastiliä muutetaan varmenteiden käyttöä varten ja miten varmenne myönnetään.</span><span class="sxs-lookup"><span data-stu-id="fcdac-104">This procedure walks you through enabling an EU entry certificate, configuring a customer account to use entry certificates and issue a certificate.</span></span> <span data-ttu-id="fcdac-105">Tämä menettelyn luomisessa käytettiin DEMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="fcdac-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="enable-entry-certificate-management"></a><span data-ttu-id="fcdac-106">Ota käyttöön merkinnän varmenteen hallinta</span><span class="sxs-lookup"><span data-stu-id="fcdac-106">Enable entry certificate management</span></span>
1. <span data-ttu-id="fcdac-107">Valitse Myyntireskontra > Asetukset > Myyntireskontran parametrit.</span><span class="sxs-lookup"><span data-stu-id="fcdac-107">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="fcdac-108">Valitse Lähetykset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="fcdac-108">Click the Shipments tab.</span></span>
3. <span data-ttu-id="fcdac-109">Laajenna Merkinnän varmenne -osaa.</span><span class="sxs-lookup"><span data-stu-id="fcdac-109">Expand the Entry certificate section.</span></span>
4. <span data-ttu-id="fcdac-110">Valitse Ota käyttöön merkinnän varmenteen hallinta -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="fcdac-110">Select Yes in the Enable entry certificate management field.</span></span>
5. <span data-ttu-id="fcdac-111">Valitse Ota käyttöön merkinnän varmenteen myöntäminen -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="fcdac-111">Select Yes in the Enable entry certificate issuing field.</span></span>
6. <span data-ttu-id="fcdac-112">Valitse Numerojärjestykset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="fcdac-112">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="fcdac-113">Etsi ja valitse luettelosta Merkinnän varmenne -rivi.</span><span class="sxs-lookup"><span data-stu-id="fcdac-113">In the list, find and select Entry certificate row.</span></span>
8. <span data-ttu-id="fcdac-114">Anna tai valitse Numerojärjestyskoodi-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="fcdac-114">In the Number sequence code field, enter or select a value.</span></span>

## <a name="set-up-a-customer"></a><span data-ttu-id="fcdac-115">Määritä asiakas</span><span class="sxs-lookup"><span data-stu-id="fcdac-115">Set up a customer</span></span>
1. <span data-ttu-id="fcdac-116">Siirry kohtaan Myyntireskontra > Asiakkaat > Kaikki asiakkaat.</span><span class="sxs-lookup"><span data-stu-id="fcdac-116">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="fcdac-117">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="fcdac-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="fcdac-118">Voit esimerkiksi suodattaa Tili-kenttää arvolla DE-015.</span><span class="sxs-lookup"><span data-stu-id="fcdac-118">For example, filter on the Account field with a value of 'DE-015'.</span></span>
3. <span data-ttu-id="fcdac-119">Avaa asiakastilin tiedot.</span><span class="sxs-lookup"><span data-stu-id="fcdac-119">Open customer account details.</span></span>
4. <span data-ttu-id="fcdac-120">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="fcdac-120">Click Edit.</span></span>
5. <span data-ttu-id="fcdac-121">Laajenna Lasku ja toimitus -osa.</span><span class="sxs-lookup"><span data-stu-id="fcdac-121">Expand the Invoice and delivery section.</span></span>
6. <span data-ttu-id="fcdac-122">Valitse Merkinnän varmenne tarvitaan -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="fcdac-122">Select Yes in the Entry certificate required field.</span></span>
7. <span data-ttu-id="fcdac-123">Valitse Myönnä merkinnän varmenne -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="fcdac-123">Select Yes in the Issue entry certificate field.</span></span>
8. <span data-ttu-id="fcdac-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="fcdac-124">Click Save.</span></span>

## <a name="create-an-eu-entry-certificate-automatically"></a><span data-ttu-id="fcdac-125">Luo EU-saapumistodistus automaattisesti</span><span class="sxs-lookup"><span data-stu-id="fcdac-125">Create an EU entry certificate automatically</span></span>
1. <span data-ttu-id="fcdac-126">Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="fcdac-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="fcdac-127">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="fcdac-127">Click New.</span></span>
3. <span data-ttu-id="fcdac-128">Syötä tai valitse arvo Asiakastili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="fcdac-128">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="fcdac-129">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fcdac-129">Click OK.</span></span>
5. <span data-ttu-id="fcdac-130">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="fcdac-130">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="fcdac-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="fcdac-131">Click Save.</span></span>
7. <span data-ttu-id="fcdac-132">Valitse toimintoruudussa Kerää ja pakkaa.</span><span class="sxs-lookup"><span data-stu-id="fcdac-132">On the Action Pane, click Pick and pack.</span></span>
8. <span data-ttu-id="fcdac-133">Valitse Kirjaa pakkausluettelo.</span><span class="sxs-lookup"><span data-stu-id="fcdac-133">Click Post packing slip.</span></span>
9. <span data-ttu-id="fcdac-134">Laajenna Parametrit-osa.</span><span class="sxs-lookup"><span data-stu-id="fcdac-134">Expand the Parameters section.</span></span>
10. <span data-ttu-id="fcdac-135">Valitse Määrä-kentässä Kaikki.</span><span class="sxs-lookup"><span data-stu-id="fcdac-135">In the Quantity field, select 'All'.</span></span>
11. <span data-ttu-id="fcdac-136">Poista Myönnä merkinnän varmenne -valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="fcdac-136">Clear the Issue entry certificate check box.</span></span>
    * <span data-ttu-id="fcdac-137">Saapumistodistus voidaan myöntää pakkausluettelon kirjauksen aikana tai tilausta laskutettaessa.</span><span class="sxs-lookup"><span data-stu-id="fcdac-137">An entry certificate can be issued during packing slip posting or during order invoicing.</span></span> <span data-ttu-id="fcdac-138">Älä valitse Myönnä merkinnän varmenne -valintaruutua ja myönnä se myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="fcdac-138">Leave the Issue entry certificate checkbox unchecked to issue it later.</span></span>  
12. <span data-ttu-id="fcdac-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fcdac-139">Click OK.</span></span>
13. <span data-ttu-id="fcdac-140">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fcdac-140">Click OK.</span></span>
14. <span data-ttu-id="fcdac-141">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="fcdac-141">On the Action Pane, click Invoice.</span></span>
15. <span data-ttu-id="fcdac-142">Valitse Lasku.</span><span class="sxs-lookup"><span data-stu-id="fcdac-142">Click Invoice.</span></span>
    * <span data-ttu-id="fcdac-143">Tarkista, että Merkinnän varmenne tarvitaan- ja Myönnä merkinnän varmenne -valintaruudut on valittu Yhteenveto-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="fcdac-143">Verify that the Entry certificate required and Issue entry certificate checkboxes in the Overview section are marked.</span></span>  <span data-ttu-id="fcdac-144">Jos valitset Tulosta merkinnän varmenne - valintaruudun, voit tulostaa varmenteen.</span><span class="sxs-lookup"><span data-stu-id="fcdac-144">You can also select the Print entry certificate check box to allow printing of the certificate.</span></span>  
16. <span data-ttu-id="fcdac-145">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fcdac-145">Click OK.</span></span>
17. <span data-ttu-id="fcdac-146">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fcdac-146">Click OK.</span></span>
18. <span data-ttu-id="fcdac-147">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="fcdac-147">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="fcdac-148">Valitse Lasku.</span><span class="sxs-lookup"><span data-stu-id="fcdac-148">Click Invoice.</span></span>
20. <span data-ttu-id="fcdac-149">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="fcdac-149">On the Action Pane, click Invoice.</span></span>
21. <span data-ttu-id="fcdac-150">Valitse Näytä myönnetyt merkinnän varmenteet.</span><span class="sxs-lookup"><span data-stu-id="fcdac-150">Click View issued entry certificates.</span></span>
22. <span data-ttu-id="fcdac-151">Valitse Tulosta.</span><span class="sxs-lookup"><span data-stu-id="fcdac-151">Click Print.</span></span>
23. <span data-ttu-id="fcdac-152">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fcdac-152">Close the page.</span></span>
24. <span data-ttu-id="fcdac-153">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="fcdac-153">Click Change status.</span></span>
25. <span data-ttu-id="fcdac-154">Valitse Uusi tila -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="fcdac-154">In the New status field, select an option.</span></span>
26. <span data-ttu-id="fcdac-155">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fcdac-155">Click OK.</span></span>
27. <span data-ttu-id="fcdac-156">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fcdac-156">Close the page.</span></span>

## <a name="create-an-eu-entry-certificate-manually"></a><span data-ttu-id="fcdac-157">Luo EU-saapumistodistus manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="fcdac-157">Create an EU entry certificate manually</span></span>
1. <span data-ttu-id="fcdac-158">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="fcdac-158">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="fcdac-159">Valitse Luo merkinnän varmenne.</span><span class="sxs-lookup"><span data-stu-id="fcdac-159">Click Create entry certificate.</span></span>
3. <span data-ttu-id="fcdac-160">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fcdac-160">Click OK.</span></span>
4. <span data-ttu-id="fcdac-161">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="fcdac-161">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="fcdac-162">Valitse Näytä myönnetyt merkinnän varmenteet.</span><span class="sxs-lookup"><span data-stu-id="fcdac-162">Click View issued entry certificates.</span></span>


