--- 
title: "Upotettuja kuvia sisältävien Microsoft Office -muotoisten raporttien tekoon sähköisessä raportoinnissa (ER) käytettyjen konfiguraatioiden tarkistaminen"
description: "Voit suorittaa nämä vaiheet, kun suoritat ensin ER Upotettuja kuvia sisältävien raporttien tekeminen MS Office -muodoissa (Osa 1 – parametrien määrittäminen) -tehtäväoppaan vaiheet."
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: dcc162a4c0ba81079eefb7564ab037c1287acd92
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="review-configurations-to-make-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er"></a><span data-ttu-id="dfb26-103">Upotettuja kuvia sisältävien Microsoft Office -muotoisten raporttien tekoon sähköisessä raportoinnissa (ER) käytettyjen konfiguraatioiden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="dfb26-103">Review configurations to make reports in Microsoft Office formats with embedded images for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dfb26-104">Voit suorittaa nämä vaiheet, kun suoritat ensin ER Raporttien tekeminen MS Office -muodoissa ja upotettujen kuvien kanssa (osa 1: parametrien määrittäminen) -tehtäväoppaan vaiheet.</span><span class="sxs-lookup"><span data-stu-id="dfb26-104">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)” task guide.</span></span>

<span data-ttu-id="dfb26-105">Näissä ohjeissa kerrotaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan, kun tavoitteena on luoda sähköisiä Microsoft Excel- ja Microsoft Word -asiakirjoja, jotka sisältävät upotettuja kuvia.</span><span class="sxs-lookup"><span data-stu-id="dfb26-105">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="dfb26-106">Tässä esimerkissä tarkistetaan ER-konfiguraatiot malliyritykselle Litware Inc.</span><span class="sxs-lookup"><span data-stu-id="dfb26-106">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="dfb26-107">Nämä ohjeet on tarkoitettu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="dfb26-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="dfb26-108">Vaiheet voidaan suorittaa USMF-tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="dfb26-108">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="dfb26-109">Tuodun tietomallin tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="dfb26-109">Review the imported data model</span></span>
1. <span data-ttu-id="dfb26-110">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="dfb26-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="dfb26-111">Valitse puussa Sekkien malli.</span><span class="sxs-lookup"><span data-stu-id="dfb26-111">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="dfb26-112">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="dfb26-112">Click Designer.</span></span>
    * <span data-ttu-id="dfb26-113">Tämä malli on suunniteltu maksusekkien esittämiseen yrityksen näkökulmasta ja tämän mallin yhdistämiseen sovelluksen tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="dfb26-113">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application’s data sources.</span></span> <span data-ttu-id="dfb26-114">Tarkista tämä malli ER-toimintojen suunnitteluohjelman avulla.</span><span class="sxs-lookup"><span data-stu-id="dfb26-114">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="dfb26-115">Ota huomioon esillä olevat mallielementtien määritteet, joita ovat esimerkiksi rakenne, nimi, kuvaus ja tietotyyppi.</span><span class="sxs-lookup"><span data-stu-id="dfb26-115">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="dfb26-116">Laajenna puussa root.</span><span class="sxs-lookup"><span data-stu-id="dfb26-116">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="dfb26-117">Laajenna puussa root\cheques.</span><span class="sxs-lookup"><span data-stu-id="dfb26-117">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="dfb26-118">Laajenna puussa root\cheques.</span><span class="sxs-lookup"><span data-stu-id="dfb26-118">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="dfb26-119">Laajenna puussa root\cheques\attributes.</span><span class="sxs-lookup"><span data-stu-id="dfb26-119">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="dfb26-120">Laajenna puussa root\payer.</span><span class="sxs-lookup"><span data-stu-id="dfb26-120">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="dfb26-121">Valitse puussa root\istestrun.</span><span class="sxs-lookup"><span data-stu-id="dfb26-121">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="dfb26-122">Valitse puussa root\layout.</span><span class="sxs-lookup"><span data-stu-id="dfb26-122">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="dfb26-123">Tämän mallin asetteluelementti edustaa valitun pankkitilin tulostetun sekin lomakkeen asettelun tietoja.</span><span class="sxs-lookup"><span data-stu-id="dfb26-123">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="dfb26-124">Se sisältää myös kaksi Säilö-tietotyypin solmua kuvien tallentamista varten.</span><span class="sxs-lookup"><span data-stu-id="dfb26-124">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="dfb26-125">Laajenna puussa root\layout.</span><span class="sxs-lookup"><span data-stu-id="dfb26-125">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="dfb26-126">Valitse puussa root\layout\company logo.</span><span class="sxs-lookup"><span data-stu-id="dfb26-126">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="dfb26-127">Laajenna puussa root\layout\company logo.</span><span class="sxs-lookup"><span data-stu-id="dfb26-127">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="dfb26-128">Valitse puussa root\layout\company logo\image.</span><span class="sxs-lookup"><span data-stu-id="dfb26-128">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="dfb26-129">Valitse puussa root\layout\company logo\isprinted.</span><span class="sxs-lookup"><span data-stu-id="dfb26-129">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="dfb26-130">Valitse puussa root\layout\signature.</span><span class="sxs-lookup"><span data-stu-id="dfb26-130">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="dfb26-131">Laajenna puussa root\layout\signature.</span><span class="sxs-lookup"><span data-stu-id="dfb26-131">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="dfb26-132">Valitse puussa root\layout\signature\image.</span><span class="sxs-lookup"><span data-stu-id="dfb26-132">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="dfb26-133">Valitse puussa root\layout\signature\isprinted.</span><span class="sxs-lookup"><span data-stu-id="dfb26-133">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="dfb26-134">Ota huomioon, että kaksi kuvan tietomallielementtiä on sidottu sellaisen taulun kenttiin, jotka sisältävät yrityksen logon ja valtuutetun henkilön allekirjoituksen kuvat binaarisessa muodossa.</span><span class="sxs-lookup"><span data-stu-id="dfb26-134">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person’s signature in binary format.</span></span>  
20. <span data-ttu-id="dfb26-135">Laajenna puussa root\layout\watermark.</span><span class="sxs-lookup"><span data-stu-id="dfb26-135">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="dfb26-136">Valitse Yhdistä malli tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="dfb26-136">Click Map model to datasource.</span></span>
22. <span data-ttu-id="dfb26-137">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="dfb26-137">Click Designer.</span></span>
23. <span data-ttu-id="dfb26-138">Laajenna puussa chequesselected.</span><span class="sxs-lookup"><span data-stu-id="dfb26-138">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="dfb26-139">Laajenna puussa layout.</span><span class="sxs-lookup"><span data-stu-id="dfb26-139">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="dfb26-140">Laajenna puussa layout\company logo.</span><span class="sxs-lookup"><span data-stu-id="dfb26-140">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="dfb26-141">Laajenna puussa layout\signature.</span><span class="sxs-lookup"><span data-stu-id="dfb26-141">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="dfb26-142">Laajenna puussa layout\watermark.</span><span class="sxs-lookup"><span data-stu-id="dfb26-142">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="dfb26-143">Vaihda Näytä tiedot käyttöön</span><span class="sxs-lookup"><span data-stu-id="dfb26-143">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="dfb26-144">Ota huomioon, että sekkien tietomallielementti on sidottu TmpChequePrintout-tauluun, joka sisältää suorituksen aikana käyttäjän tulostettavaksi valitsemien sekkien tietueita.</span><span class="sxs-lookup"><span data-stu-id="dfb26-144">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="dfb26-145">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dfb26-145">Close the page.</span></span>
30. <span data-ttu-id="dfb26-146">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dfb26-146">Close the page.</span></span>
31. <span data-ttu-id="dfb26-147">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dfb26-147">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="dfb26-148">Tuodun muodon tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="dfb26-148">Review the imported format</span></span>
1. <span data-ttu-id="dfb26-149">Valitse puussa Model for cheques.</span><span class="sxs-lookup"><span data-stu-id="dfb26-149">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="dfb26-150">Valitse puussa Model for cheques\Cheques printing format.</span><span class="sxs-lookup"><span data-stu-id="dfb26-150">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="dfb26-151">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="dfb26-151">Click Designer.</span></span>
4. <span data-ttu-id="dfb26-152">Napsauta Liitteet.</span><span class="sxs-lookup"><span data-stu-id="dfb26-152">Click Attachments.</span></span>
5. <span data-ttu-id="dfb26-153">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="dfb26-153">Click Open.</span></span>
    * <span data-ttu-id="dfb26-154">Avaa Excelissä liitetyn raportin malli.</span><span class="sxs-lookup"><span data-stu-id="dfb26-154">Open the attached report’s template in Excel.</span></span>  
    * <span data-ttu-id="dfb26-155">Tarkista sekkien tulostamisessa käytettävä liitetyn raportin Excel-malli.</span><span class="sxs-lookup"><span data-stu-id="dfb26-155">Review the attached report’s Excel template that will be used to print cheques.</span></span> <span data-ttu-id="dfb26-156">Mallissa on kaksi sekkiä sivulla. Se on suunniteltu tulostamaan sekit esitäytettyyn lomakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="dfb26-156">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="dfb26-157">Ota huomioon kaksi tyhjää upotettua kuvaa.</span><span class="sxs-lookup"><span data-stu-id="dfb26-157">Note that two blank images are embedded.</span></span> <span data-ttu-id="dfb26-158">Nämä tyhjät kuvat on tarkoitettu yrityksen logoa ja maksun hyväksyvän henkilön allekirjoitusta varten.</span><span class="sxs-lookup"><span data-stu-id="dfb26-158">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="dfb26-159">Varmista, että kuvien nimet ovat Excelissä CompLogo ja SignatureImage.</span><span class="sxs-lookup"><span data-stu-id="dfb26-159">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="dfb26-160">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dfb26-160">Close the page.</span></span>
7. <span data-ttu-id="dfb26-161">Laajenna puussa Report.</span><span class="sxs-lookup"><span data-stu-id="dfb26-161">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="dfb26-162">Laajenna puussa Report\ChequeLines.</span><span class="sxs-lookup"><span data-stu-id="dfb26-162">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="dfb26-163">Valitse puussa Report\ChequeLines\CompLogo.</span><span class="sxs-lookup"><span data-stu-id="dfb26-163">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="dfb26-164">Vaihda Näytä tiedot käyttöön</span><span class="sxs-lookup"><span data-stu-id="dfb26-164">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="dfb26-165">Ota huomioon, että CompLogo-muodon solun elementti edustaa Excel-kohdetta, jonka avulla yrityksen logon kuvan täytetään raporttiin.</span><span class="sxs-lookup"><span data-stu-id="dfb26-165">Note that the ‘CompLogo’ format’s cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="dfb26-166">Tämä muotoelementti on sidottu kuvan tietomallielementtiin, joka sisältää suorituksen aikana yrityksen logon kuvan binaarisessa muodossa.</span><span class="sxs-lookup"><span data-stu-id="dfb26-166">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="dfb26-167">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="dfb26-167">Click the Mapping tab.</span></span>
12. <span data-ttu-id="dfb26-168">Valitse Muokkaus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="dfb26-168">Click Edit enabled.</span></span>
    * <span data-ttu-id="dfb26-169">Ota huomioon, että voit ottaa CompLogo-muodon solun elementin pois käytöstä.</span><span class="sxs-lookup"><span data-stu-id="dfb26-169">Note that you can make the ‘CompLogo’ format’s cell element so that it’s no longer enabled.</span></span> <span data-ttu-id="dfb26-170">Tällöin liitetty Excel-kuvaelementti piilottaa yrityksen logon luodussa raportissa.</span><span class="sxs-lookup"><span data-stu-id="dfb26-170">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="dfb26-171">Jos käytössä oleva lauseke palauttaa TRUE-arvon ja määritetty sidonta ei tuo kuvaa, liitetty Excel-kuvaelementti näyttää Excel-malliin tallennetun kuvan.</span><span class="sxs-lookup"><span data-stu-id="dfb26-171">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="dfb26-172">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dfb26-172">Close the page.</span></span>
14. <span data-ttu-id="dfb26-173">Laajenna puussa labels: Container.</span><span class="sxs-lookup"><span data-stu-id="dfb26-173">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="dfb26-174">Jotkin esitäytetyn sekin lomakkeessa olevat nimiöt sisällytetään raporttiin, kun se luodaan testausta varten.</span><span class="sxs-lookup"><span data-stu-id="dfb26-174">Some labels that are presented in the preprinted cheque form will be included in the report when it’s created for testing purposes.</span></span> <span data-ttu-id="dfb26-175">Näitä nimiöitä ei kuitenkaan tulosteta todellisen tulostuksen aikana, koska ne ovat jo esitäytetyssä lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="dfb26-175">However, those labels won’t be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="dfb26-176">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dfb26-176">Close the page.</span></span>


