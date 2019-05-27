---
title: Muokkaa muotoja ottamalla Excel-mallit uudelleen käyttöön
description: Tämän menettelyn vaiheiden suorittaminen edellyttää, että ER Määrityksen suunnittelu OPENXML-muotoisten raporttien luomiseksi -menettelyn vaiheet on suoritettu ensin.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d5752caba9327475bb28c7bc6b0ee7e072f44f3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551158"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a><span data-ttu-id="fcd61-103">Muokkaa muotoja ottamalla Excel-mallit uudelleen käyttöön</span><span class="sxs-lookup"><span data-stu-id="fcd61-103">Modify formats by reapplying Excel templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fcd61-104">Tämän menettelyn vaiheiden suorittaminen edellyttää, että ER Määrityksen suunnittelu OPENXML-muotoisten raporttien luomiseksi -menettelyn vaiheet on suoritettu ensin.</span><span class="sxs-lookup"><span data-stu-id="fcd61-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="fcd61-105">Menettelyssä kerrotaan, miten sähköisen raportoinnin (ER) muodon määrityksiä muokataan käyttämällä uudelleen muokattua Microsoft Excel -mallia.</span><span class="sxs-lookup"><span data-stu-id="fcd61-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="fcd61-106">Tässä menettelyssä tuodaan muokattu Excel-malli ER-muotokonfiguraatioihin, jotka on luotu malliyritykselle Litware Inc. ja joita käytetään sähköisten asiakirjojen luomisessa.</span><span class="sxs-lookup"><span data-stu-id="fcd61-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="fcd61-107">Nämä ohjeet on tarkoitettu käyttäjille, joilla on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="fcd61-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="fcd61-108">Nämä vaiheet voidaan suorittaa GBSI-tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="fcd61-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="fcd61-109">Lataa ja tallenna ennen aloittamista SampleVendPaymWsReport2.xlsx-tiedosto, joka on mainittu ohjeaiheessa Sähköisen raportoinnin muodon muokkaaminen käyttämällä uudelleen Excel-mallia (modify-electronic-reporting-format-reapply-excel-template/).</span><span class="sxs-lookup"><span data-stu-id="fcd61-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="fcd61-110">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="fcd61-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="fcd61-111">Varmista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="fcd61-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="fcd61-112">Jos konfiguraation lähde ei ole näkyvissä, suorita Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="fcd61-112">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="fcd61-113">Valitse ER-muoto</span><span class="sxs-lookup"><span data-stu-id="fcd61-113">Select the ER format</span></span>
1. <span data-ttu-id="fcd61-114">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="fcd61-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="fcd61-115">Laajenna puussa solmu Payment model.</span><span class="sxs-lookup"><span data-stu-id="fcd61-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="fcd61-116">Valitse puusta Maksumalli\Laskentataulukkoraportin esimerkki.</span><span class="sxs-lookup"><span data-stu-id="fcd61-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="fcd61-117">Napsauta Liitteet.</span><span class="sxs-lookup"><span data-stu-id="fcd61-117">Click Attachments.</span></span>
    * <span data-ttu-id="fcd61-118">Ota huomioon, että Excel-tiedostoa SampleVendPaymWsReport.xlsx käytetään tällä hetkellä maksukirjauskansion käsittelyn mallina.</span><span class="sxs-lookup"><span data-stu-id="fcd61-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="fcd61-119">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="fcd61-119">Click Open.</span></span>
    * <span data-ttu-id="fcd61-120">Valitse Avaa, kun haluat katsoa Excel-mallin asettelua.</span><span class="sxs-lookup"><span data-stu-id="fcd61-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="fcd61-121">Tarkista malli.</span><span class="sxs-lookup"><span data-stu-id="fcd61-121">Review the template.</span></span> <span data-ttu-id="fcd61-122">Ota huomioon, että se sisältää tällä hetkellä seuraavat tiedot kunkin maksurivin osalta: toimittajan tilinumero, toimittajan nimi, pankki, reititysnumero, tilinumero, hyvitys, veloitus ja valuutta.</span><span class="sxs-lookup"><span data-stu-id="fcd61-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="fcd61-123">Tässä esimerkissä halutaan laajentaa luetteloa lisäämällä maksupäivämäärän tiedot.</span><span class="sxs-lookup"><span data-stu-id="fcd61-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="fcd61-124">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fcd61-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="fcd61-125">Käytä uutta Excel-mallia uudelleen ER-muodossa</span><span class="sxs-lookup"><span data-stu-id="fcd61-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="fcd61-126">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="fcd61-126">Click Designer.</span></span>
    * <span data-ttu-id="fcd61-127">Avaa valitun ER-muodon luonnosversio muokkausta varten.</span><span class="sxs-lookup"><span data-stu-id="fcd61-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="fcd61-128">Valitse toimintoruudussa Tuo.</span><span class="sxs-lookup"><span data-stu-id="fcd61-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="fcd61-129">Valitse Päivitä Excelistä.</span><span class="sxs-lookup"><span data-stu-id="fcd61-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="fcd61-130">Valitse Päivitä malli ja valitse sitten tiedosto (SampleVendPaymWsReport2.xlsx).</span><span class="sxs-lookup"><span data-stu-id="fcd61-130">Click ‘Update template’, and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="fcd61-131">Valitse Päivitä malli ja siirry aiemmin ladattuun SampleVendPaymWsReport2.xlsx-tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="fcd61-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="fcd61-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fcd61-132">Click OK.</span></span>
    * <span data-ttu-id="fcd61-133">SampleVendPaymWsReport2.xlsx-malli on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="fcd61-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="fcd61-134">ER-muodon rakenne on synkronoitu sen mallin sisällön kanssa, jonka elementit on lisätty ER-muotoon.</span><span class="sxs-lookup"><span data-stu-id="fcd61-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="fcd61-135">Kaikki ER-muodot, jotka eivät sisälly malliin, poistetaan muodon määrityksestä.</span><span class="sxs-lookup"><span data-stu-id="fcd61-135">Any existing elements in the ER format that aren’t included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="fcd61-136">Valitse puussa Excel.</span><span class="sxs-lookup"><span data-stu-id="fcd61-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="fcd61-137">Ota huomioon, että Malli-kenttä sisältää nyt uuden mallin viitteen.</span><span class="sxs-lookup"><span data-stu-id="fcd61-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="fcd61-138">Napsauta Liitteet.</span><span class="sxs-lookup"><span data-stu-id="fcd61-138">Click Attachments.</span></span>
7. <span data-ttu-id="fcd61-139">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="fcd61-139">Click Open.</span></span>
    * <span data-ttu-id="fcd61-140">Valitse Avaa, kun haluat katsoa muokatun Excel-mallin asettelua.</span><span class="sxs-lookup"><span data-stu-id="fcd61-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="fcd61-141">Tarkista malli.</span><span class="sxs-lookup"><span data-stu-id="fcd61-141">Review the template.</span></span> <span data-ttu-id="fcd61-142">Ota huomioon, että se sisältää maksupäivämäärän rivin.</span><span class="sxs-lookup"><span data-stu-id="fcd61-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="fcd61-143">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fcd61-143">Close the page.</span></span>
9. <span data-ttu-id="fcd61-144">Laajenna puussa Excel.</span><span class="sxs-lookup"><span data-stu-id="fcd61-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="fcd61-145">Valitse puussa Excel\PaymLines.</span><span class="sxs-lookup"><span data-stu-id="fcd61-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="fcd61-146">Valitse puussa Excel\PaymLines\PaymDate.</span><span class="sxs-lookup"><span data-stu-id="fcd61-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="fcd61-147">Ota huomioon, että ER-muoto sisältää nyt yhden lisänimikkeen.</span><span class="sxs-lookup"><span data-stu-id="fcd61-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="fcd61-148">PaymDate-solu on lisätty Excel-malliin.</span><span class="sxs-lookup"><span data-stu-id="fcd61-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="fcd61-149">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="fcd61-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="fcd61-150">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="fcd61-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="fcd61-151">Laajenna puussa solmu model\Payments.</span><span class="sxs-lookup"><span data-stu-id="fcd61-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="fcd61-152">Valitse puussa solmu model\Payments\Transaction date(TransactionDate).</span><span class="sxs-lookup"><span data-stu-id="fcd61-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="fcd61-153">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="fcd61-153">Click Bind.</span></span>
    * <span data-ttu-id="fcd61-154">Määritä, mitkä tiedot lisätään uuteen soluun suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="fcd61-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="fcd61-155">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="fcd61-155">Click Save.</span></span>
18. <span data-ttu-id="fcd61-156">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fcd61-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="fcd61-157">Ota käyttöön ER-muodon muokattu luonnosversio maksukirjauskansion käsittelyssä</span><span class="sxs-lookup"><span data-stu-id="fcd61-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="fcd61-158">Valitse toimintoruudussa Konfiguroinnit.</span><span class="sxs-lookup"><span data-stu-id="fcd61-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="fcd61-159">Valitse Käyttäjän parametrit.</span><span class="sxs-lookup"><span data-stu-id="fcd61-159">Click User parameters.</span></span>
3. <span data-ttu-id="fcd61-160">Valitse Suorita asetukset -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="fcd61-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="fcd61-161">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fcd61-161">Click OK.</span></span>
5. <span data-ttu-id="fcd61-162">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="fcd61-162">Click Edit.</span></span>
6. <span data-ttu-id="fcd61-163">Valitse Suorita luonnos -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="fcd61-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="fcd61-164">Käytä ER-muodon muokattua luonnosversiota maksukirjauskansion käsittelyssä</span><span class="sxs-lookup"><span data-stu-id="fcd61-164">Use the modified draft version of the ER format for payment journal processing</span></span>
    * <span data-ttu-id="fcd61-165">Tarkista luotu laskentataulukko ja maksurivien uudet maksupäivämäärien tiedot.</span><span class="sxs-lookup"><span data-stu-id="fcd61-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  

