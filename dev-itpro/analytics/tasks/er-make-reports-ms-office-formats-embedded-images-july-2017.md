--- 
title: "Upotettuja kuvia sisältävien raporttien tekeminen Microsoft Office -muodoissa sähköistä raportointia (ER) varten (osa 1)"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi suunnitella sähköisen raportoinnin (ER) konfiguraatioita luomaan sähköisiä, upotettuja kuvia sisältäviä asiakirjoja MS Office -muodoissa (Excel ja Word)."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: bfc3d09017b864e6b2811cab9d7f4b05b048148b
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="make-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er--part-1"></a><span data-ttu-id="4c1a1-103">Upotettuja kuvia sisältävien raporttien tekeminen Microsoft Office -muodoissa sähköistä raportointia (ER) varten (osa 1)</span><span class="sxs-lookup"><span data-stu-id="4c1a1-103">Make reports in Microsoft Office formats with embedded images for electronic reporting (ER)  (Part 1)</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4c1a1-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi suunnitella sähköisen raportoinnin (ER) konfiguraatioita luomaan sähköisiä, upotettuja kuvia sisältäviä asiakirjoja MS Office -muodoissa (Excel ja Word).</span><span class="sxs-lookup"><span data-stu-id="4c1a1-104">The following steps explain how a user playing either ‘System administrator’ or ‘Electronic reporting developer’ role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="4c1a1-105">Tässä esimerkissä luodaan ER-konfiguraatioita malliyritykselle Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-105">In this example, you will use created ER configurations for sample company, ‘Litware, Inc.’.</span></span>  <span data-ttu-id="4c1a1-106">Voit suorittaa nämä vaiheet, kun suoritat ensin ER Upotettuja kuvia sisältävien raporttien tekeminen MS Office -muodoissa (Osa 2 – konfiguraatioiden tarkistaminen) -tehtäväoppaan vaiheet.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-106">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)” task guide.</span></span> <span data-ttu-id="4c1a1-107">Nämä vaiheet voidaan suorittaa USMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-107">These steps can be performed in ‘USMF’ company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="4c1a1-108">Muodon suorittaminen alkuperäisen mallin yhdistämismäärityksen kanssa</span><span class="sxs-lookup"><span data-stu-id="4c1a1-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="4c1a1-109">Valitse Maksuliikenteen hallinta > Pankkitilit > Pankkitilit.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="4c1a1-110">Pikasuodattimen avulla voit suodattaa Pankkitili-kentän USMF OPER -arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="4c1a1-111">Valitse toimintoruudussa Määritä.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="4c1a1-112">Valitse Tarkista.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-112">Click Check.</span></span>
5. <span data-ttu-id="4c1a1-113">Valitse Tulosta testi.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-113">Click Print test.</span></span>
    * <span data-ttu-id="4c1a1-114">Suorita muoto testausta varten.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="4c1a1-115">Valitse Siirtokelpoisen sekin muoto -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="4c1a1-116">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-116">Click OK.</span></span>
    * <span data-ttu-id="4c1a1-117">Tarkista luotu tuotos.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-117">Review the created output.</span></span> <span data-ttu-id="4c1a1-118">Ota huomioon, että raportissa esitetään sekä yrityksen logo että valtuutetun henkilön allekirjoitus.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-118">Note that the company logo is presented in the report as well as the authorized person’s signature.</span></span> <span data-ttu-id="4c1a1-119">Allekirjoituskuva saadaan valittuun pankkitiliin liitetyn sekin asettelutietueen säilön tietotyypin kentästä.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-119">The signature image is taken from the field of the ‘Container’ data type of the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="4c1a1-120">Laajenna Kopiot-osa.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="4c1a1-121">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-121">Click Edit.</span></span>
10. <span data-ttu-id="4c1a1-122">Syötä Vesileima-kenttään Tulosta vesileimaksi mitätöity.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="4c1a1-123">Muuta vesileiman asettelun asetusta niin, että vesileiman teksti näkyy luotavan Excel-muotoisen elementin asiakirjassa.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="4c1a1-124">Valitse Tulosta testi.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-124">Click Print test.</span></span>
12. <span data-ttu-id="4c1a1-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-125">Click OK.</span></span>
    * <span data-ttu-id="4c1a1-126">Tarkista luotu tuotos.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-126">Review the created output.</span></span> <span data-ttu-id="4c1a1-127">Ota huomioon, että vesileima näytetään luodussa raportissa valinnan asetuksen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-127">Note that the watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="4c1a1-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-128">Close the page.</span></span>
14. <span data-ttu-id="4c1a1-129">Valitse toimintoruudussa Maksujen hallinta.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="4c1a1-130">Valitse Sekit.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-130">Click Checks.</span></span>
16. <span data-ttu-id="4c1a1-131">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-131">Click Show filters.</span></span>
17. <span data-ttu-id="4c1a1-132">Käytä seuraavia suodattimia: Syötä suodattimen arvo "381","385","389" Sekin numero -kenttään. Käytä On yksi seuraavista -suodatinoperaattoria.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="4c1a1-133">Merkitse luettelossa kaikki rivit.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="4c1a1-134">Valitse Tulosta sekin kopio.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-134">Click Print check copy.</span></span>
    * <span data-ttu-id="4c1a1-135">Suorita muoto valittujen sekkien uudelleentulostusta varten.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-135">Run the format to re-print the selected cheques.</span></span>  
    * <span data-ttu-id="4c1a1-136">Tarkista luotu tuotos.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-136">Review the created output.</span></span> <span data-ttu-id="4c1a1-137">Ota huomioon, että valitut sekit on tulostettu uudelleen.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-137">Note that the selected cheques have been re-printed.</span></span> <span data-ttu-id="4c1a1-138">Yrityksen logoa ja nimiöitä ei tulosteta, koska näkyvät esitäytetyssä lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="4c1a1-139">Tuodun tietomallin yhdistämismäärityksen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="4c1a1-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="4c1a1-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-140">Close the page.</span></span>
2. <span data-ttu-id="4c1a1-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-141">Close the page.</span></span>
3. <span data-ttu-id="4c1a1-142">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="4c1a1-143">Valitse puussa Sekkien malli.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="4c1a1-144">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-144">Click Designer.</span></span>
6. <span data-ttu-id="4c1a1-145">Valitse Yhdistä malli tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="4c1a1-146">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-146">Click Designer.</span></span>
    * <span data-ttu-id="4c1a1-147">Tietomallin allekirjoitusnimikkeen sidontaa muutetaan, jotta allekirjoituskuva voidaan hakea valittuun pankkitiliin liitetyn sekin asettelutietueeseen liitetystä asiakirjoista.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-147">We will change the binding of the data model’s signature item to get the signature image from the file that has been attached to the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="4c1a1-148">Poista Näytä tiedot -kohta käytöstä.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-148">Turn Show details off.</span></span>
9. <span data-ttu-id="4c1a1-149">Laajenna puussa layout.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="4c1a1-150">Laajenna puussa layout\signature.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="4c1a1-151">Valitse puussa layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="4c1a1-152">Laajenna puussa chequesaccount.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="4c1a1-153">Laajenna puussa chequesaccount\<Relations.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="4c1a1-154">Laajenna puussa chequesaccount\<Relations\BankChequeLayout.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="4c1a1-155">Laajenna puussa chequesaccount\<Relations\BankChequeLayout\<Relations.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="4c1a1-156">Laajenna puussa chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="4c1a1-157">Valitse puussa chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer().</span><span class="sxs-lookup"><span data-stu-id="4c1a1-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="4c1a1-158">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-158">Click Bind.</span></span>
19. <span data-ttu-id="4c1a1-159">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-159">Click Save.</span></span>
20. <span data-ttu-id="4c1a1-160">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-160">Close the page.</span></span>
21. <span data-ttu-id="4c1a1-161">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-161">Close the page.</span></span>
22. <span data-ttu-id="4c1a1-162">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-162">Close the page.</span></span>
23. <span data-ttu-id="4c1a1-163">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="4c1a1-164">Muodon suorittaminen muokatun mallin yhdistämismäärityksen avulla</span><span class="sxs-lookup"><span data-stu-id="4c1a1-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="4c1a1-165">Valitse Maksuliikenteen hallinta > Pankkitilit > Pankkitilit.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="4c1a1-166">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4c1a1-167">Voit esimerkiksi suodattaa Pankkitili-kenttää arvolla USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="4c1a1-168">Valitse toimintoruudussa Määritä.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="4c1a1-169">Valitse Tarkista.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-169">Click Check.</span></span>
5. <span data-ttu-id="4c1a1-170">Valitse Tulosta testi.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-170">Click Print test.</span></span>
6. <span data-ttu-id="4c1a1-171">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-171">Click OK.</span></span>
    * <span data-ttu-id="4c1a1-172">Tarkista luotu tuotos.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-172">Review the created output.</span></span> <span data-ttu-id="4c1a1-173">Ota huomioon, että tiedostojen hallinnan liitteen kuva näkyy valtuutetun henkilön allekirjoituksena.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-173">Note that the image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="4c1a1-174">MS Word -asiakirjan käyttäminen mallina tuodussa muodossa</span><span class="sxs-lookup"><span data-stu-id="4c1a1-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="4c1a1-175">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-175">Close the page.</span></span>
2. <span data-ttu-id="4c1a1-176">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-176">Close the page.</span></span>
3. <span data-ttu-id="4c1a1-177">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="4c1a1-178">Valitse puussa Model for cheques.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="4c1a1-179">Valitse puussa Model for cheques\Cheques printing format.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="4c1a1-180">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-180">Click Designer.</span></span>
7. <span data-ttu-id="4c1a1-181">Napsauta Liitteet.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-181">Click Attachments.</span></span>
8. <span data-ttu-id="4c1a1-182">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-182">Click Delete.</span></span>
9. <span data-ttu-id="4c1a1-183">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-183">Click Yes.</span></span>
10. <span data-ttu-id="4c1a1-184">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-184">Click New.</span></span>
11. <span data-ttu-id="4c1a1-185">Napsauta Tiedosto.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-185">Click File.</span></span>
    * <span data-ttu-id="4c1a1-186">Valitse Selaa ja valitse sitten etukäteen ladattu tiedosto nimeltä Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-186">Click Browse and select the downloaded in advance ‘Cheque template Word.docx’ file.</span></span>  
12. <span data-ttu-id="4c1a1-187">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-187">Close the page.</span></span>
13. <span data-ttu-id="4c1a1-188">Syötä tai valitse Malli-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="4c1a1-189">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-189">Click Save.</span></span>
15. <span data-ttu-id="4c1a1-190">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-190">Close the page.</span></span>
16. <span data-ttu-id="4c1a1-191">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-191">Click Edit.</span></span>
17. <span data-ttu-id="4c1a1-192">Valitse Suorita luonnos -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="4c1a1-193">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-193">Close the page.</span></span>
19. <span data-ttu-id="4c1a1-194">Valitse Maksuliikenteen hallinta > Pankkitilit > Pankkitilit.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="4c1a1-195">Pikasuodattimen avulla voit suodattaa Pankkitili-kentän USMF OPER -arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="4c1a1-196">Valitse Tarkista.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-196">Click Check.</span></span>
22. <span data-ttu-id="4c1a1-197">Valitse Tulosta testi.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-197">Click Print test.</span></span>
23. <span data-ttu-id="4c1a1-198">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-198">Click OK.</span></span>
    * <span data-ttu-id="4c1a1-199">Tarkista luotu tuotos.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-199">Review the created output.</span></span> <span data-ttu-id="4c1a1-200">Ota huomioon, että tuloste on luotu MS Word -asiakirjana, joka sisältää yrityksen logoa esittävät upotetut kuvat, valtuutetun henkilön allekirjoituksen ja vesileiman valitun tekstin.</span><span class="sxs-lookup"><span data-stu-id="4c1a1-200">Note that the output has been generated as a MS Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  


