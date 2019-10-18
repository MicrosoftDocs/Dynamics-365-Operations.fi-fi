---
title: EUR-00012 EU-saapumistodistuksen myöntäminen
description: Tässä menettelyssä selvitetään, miten EU-saapumistodistus otetaan käyttöön, miten asiakastiliä muutetaan varmenteiden käyttöä varten ja miten varmenne myönnetään.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustTable, SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CustEntryCertificateJour_W, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 735331fd399ba9501031084e236b88c0e11bb179
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183619"
---
# <a name="eur-00012-issue-an-eu-entry-certificate"></a><span data-ttu-id="1384d-103">EUR-00012 EU-saapumistodistuksen myöntäminen</span><span class="sxs-lookup"><span data-stu-id="1384d-103">EUR-00012 Issue an EU entry certificate</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1384d-104">Tässä menettelyssä selvitetään, miten EU-saapumistodistus otetaan käyttöön, miten asiakastiliä muutetaan varmenteiden käyttöä varten ja miten varmenne myönnetään.</span><span class="sxs-lookup"><span data-stu-id="1384d-104">This procedure walks you through enabling an EU entry certificate, configuring a customer account to use entry certificates and issue a certificate.</span></span> <span data-ttu-id="1384d-105">Tämä menettelyn luomisessa käytettiin DEMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="1384d-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="enable-entry-certificate-management"></a><span data-ttu-id="1384d-106">Ota käyttöön merkinnän varmenteen hallinta</span><span class="sxs-lookup"><span data-stu-id="1384d-106">Enable entry certificate management</span></span>
1. <span data-ttu-id="1384d-107">Valitse Myyntireskontra > Asetukset > Myyntireskontran parametrit.</span><span class="sxs-lookup"><span data-stu-id="1384d-107">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="1384d-108">Valitse Lähetykset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="1384d-108">Click the Shipments tab.</span></span>
3. <span data-ttu-id="1384d-109">Laajenna Merkinnän varmenne -osaa.</span><span class="sxs-lookup"><span data-stu-id="1384d-109">Expand the Entry certificate section.</span></span>
4. <span data-ttu-id="1384d-110">Valitse Ota käyttöön merkinnän varmenteen hallinta -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="1384d-110">Select Yes in the Enable entry certificate management field.</span></span>
5. <span data-ttu-id="1384d-111">Valitse Ota käyttöön merkinnän varmenteen myöntäminen -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="1384d-111">Select Yes in the Enable entry certificate issuing field.</span></span>
6. <span data-ttu-id="1384d-112">Valitse Numerojärjestykset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="1384d-112">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="1384d-113">Etsi ja valitse luettelosta Merkinnän varmenne -rivi.</span><span class="sxs-lookup"><span data-stu-id="1384d-113">In the list, find and select Entry certificate row.</span></span>
8. <span data-ttu-id="1384d-114">Anna tai valitse Numerojärjestyskoodi-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="1384d-114">In the Number sequence code field, enter or select a value.</span></span>

## <a name="set-up-a-customer"></a><span data-ttu-id="1384d-115">Määritä asiakas</span><span class="sxs-lookup"><span data-stu-id="1384d-115">Set up a customer</span></span>
1. <span data-ttu-id="1384d-116">Siirry kohtaan Myyntireskontra > Asiakkaat > Kaikki asiakkaat.</span><span class="sxs-lookup"><span data-stu-id="1384d-116">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="1384d-117">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="1384d-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1384d-118">Voit esimerkiksi suodattaa Tili-kenttää arvolla DE-015.</span><span class="sxs-lookup"><span data-stu-id="1384d-118">For example, filter on the Account field with a value of 'DE-015'.</span></span>
3. <span data-ttu-id="1384d-119">Avaa asiakastilin tiedot.</span><span class="sxs-lookup"><span data-stu-id="1384d-119">Open customer account details.</span></span>
4. <span data-ttu-id="1384d-120">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="1384d-120">Click Edit.</span></span>
5. <span data-ttu-id="1384d-121">Laajenna Lasku ja toimitus -osa.</span><span class="sxs-lookup"><span data-stu-id="1384d-121">Expand the Invoice and delivery section.</span></span>
6. <span data-ttu-id="1384d-122">Valitse Merkinnän varmenne tarvitaan -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="1384d-122">Select Yes in the Entry certificate required field.</span></span>
7. <span data-ttu-id="1384d-123">Valitse Myönnä merkinnän varmenne -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="1384d-123">Select Yes in the Issue entry certificate field.</span></span>
8. <span data-ttu-id="1384d-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1384d-124">Click Save.</span></span>

## <a name="create-an-eu-entry-certificate-automatically"></a><span data-ttu-id="1384d-125">Luo EU-saapumistodistus automaattisesti</span><span class="sxs-lookup"><span data-stu-id="1384d-125">Create an EU entry certificate automatically</span></span>
1. <span data-ttu-id="1384d-126">Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="1384d-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="1384d-127">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1384d-127">Click New.</span></span>
3. <span data-ttu-id="1384d-128">Syötä tai valitse arvo Asiakastili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1384d-128">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="1384d-129">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1384d-129">Click OK.</span></span>
5. <span data-ttu-id="1384d-130">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1384d-130">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="1384d-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1384d-131">Click Save.</span></span>
7. <span data-ttu-id="1384d-132">Valitse toimintoruudussa Kerää ja pakkaa.</span><span class="sxs-lookup"><span data-stu-id="1384d-132">On the Action Pane, click Pick and pack.</span></span>
8. <span data-ttu-id="1384d-133">Valitse Kirjaa pakkausluettelo.</span><span class="sxs-lookup"><span data-stu-id="1384d-133">Click Post packing slip.</span></span>
9. <span data-ttu-id="1384d-134">Laajenna Parametrit-osa.</span><span class="sxs-lookup"><span data-stu-id="1384d-134">Expand the Parameters section.</span></span>
10. <span data-ttu-id="1384d-135">Valitse Määrä-kentässä Kaikki.</span><span class="sxs-lookup"><span data-stu-id="1384d-135">In the Quantity field, select 'All'.</span></span>
11. <span data-ttu-id="1384d-136">Poista Myönnä merkinnän varmenne -valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="1384d-136">Clear the Issue entry certificate check box.</span></span>
    * <span data-ttu-id="1384d-137">Saapumistodistus voidaan myöntää pakkausluettelon kirjauksen aikana tai tilausta laskutettaessa.</span><span class="sxs-lookup"><span data-stu-id="1384d-137">An entry certificate can be issued during packing slip posting or during order invoicing.</span></span> <span data-ttu-id="1384d-138">Älä valitse Myönnä merkinnän varmenne -valintaruutua ja myönnä se myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="1384d-138">Leave the Issue entry certificate checkbox unchecked to issue it later.</span></span>  
12. <span data-ttu-id="1384d-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1384d-139">Click OK.</span></span>
13. <span data-ttu-id="1384d-140">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1384d-140">Click OK.</span></span>
14. <span data-ttu-id="1384d-141">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="1384d-141">On the Action Pane, click Invoice.</span></span>
15. <span data-ttu-id="1384d-142">Valitse Lasku.</span><span class="sxs-lookup"><span data-stu-id="1384d-142">Click Invoice.</span></span>
    * <span data-ttu-id="1384d-143">Tarkista, että Merkinnän varmenne tarvitaan- ja Myönnä merkinnän varmenne -valintaruudut on valittu Yhteenveto-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="1384d-143">Verify that the Entry certificate required and Issue entry certificate checkboxes in the Overview section are marked.</span></span>  <span data-ttu-id="1384d-144">Jos valitset Tulosta merkinnän varmenne - valintaruudun, voit tulostaa varmenteen.</span><span class="sxs-lookup"><span data-stu-id="1384d-144">You can also select the Print entry certificate check box to allow printing of the certificate.</span></span>  
16. <span data-ttu-id="1384d-145">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1384d-145">Click OK.</span></span>
17. <span data-ttu-id="1384d-146">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1384d-146">Click OK.</span></span>
18. <span data-ttu-id="1384d-147">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="1384d-147">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="1384d-148">Valitse Lasku.</span><span class="sxs-lookup"><span data-stu-id="1384d-148">Click Invoice.</span></span>
20. <span data-ttu-id="1384d-149">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="1384d-149">On the Action Pane, click Invoice.</span></span>
21. <span data-ttu-id="1384d-150">Valitse Näytä myönnetyt merkinnän varmenteet.</span><span class="sxs-lookup"><span data-stu-id="1384d-150">Click View issued entry certificates.</span></span>
22. <span data-ttu-id="1384d-151">Valitse Tulosta.</span><span class="sxs-lookup"><span data-stu-id="1384d-151">Click Print.</span></span>
23. <span data-ttu-id="1384d-152">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1384d-152">Close the page.</span></span>
24. <span data-ttu-id="1384d-153">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="1384d-153">Click Change status.</span></span>
25. <span data-ttu-id="1384d-154">Valitse Uusi tila -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="1384d-154">In the New status field, select an option.</span></span>
26. <span data-ttu-id="1384d-155">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1384d-155">Click OK.</span></span>
27. <span data-ttu-id="1384d-156">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1384d-156">Close the page.</span></span>

## <a name="create-an-eu-entry-certificate-manually"></a><span data-ttu-id="1384d-157">Luo EU-saapumistodistus manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="1384d-157">Create an EU entry certificate manually</span></span>
1. <span data-ttu-id="1384d-158">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="1384d-158">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="1384d-159">Valitse Luo merkinnän varmenne.</span><span class="sxs-lookup"><span data-stu-id="1384d-159">Click Create entry certificate.</span></span>
3. <span data-ttu-id="1384d-160">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1384d-160">Click OK.</span></span>
4. <span data-ttu-id="1384d-161">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="1384d-161">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="1384d-162">Valitse Näytä myönnetyt merkinnän varmenteet.</span><span class="sxs-lookup"><span data-stu-id="1384d-162">Click View issued entry certificates.</span></span>

