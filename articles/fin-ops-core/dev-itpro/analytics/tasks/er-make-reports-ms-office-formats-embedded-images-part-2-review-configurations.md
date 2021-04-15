---
title: Konfiguraatioiden tarkistaminen raporttien luomiseksi Office-muodoissa, joissa on upotettuja kuvia
description: Tässä aiheessa käsitellään raportoinnin määritysten suunnittelua luomaan upotettuja kuvia sisältäviä sähköisiä asiakirjoja. (Osa 1 – Parametrien määrittäminen).
author: NickSelin
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de815b363daa9135b50a2f5c9c4ac19e87b6b7ee
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751579"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="997a7-104">Konfiguraatioiden tarkistaminen raporttien luomiseksi Office-muodoissa, joissa on upotettuja kuvia</span><span class="sxs-lookup"><span data-stu-id="997a7-104">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="997a7-105">Voit suorittaa nämä vaiheet, kun suoritat ensin ER Upotettuja kuvia sisältävien raporttien tekeminen MS Office -muodoissa (Osa 1: parametrien määrittäminen) -tehtäväoppaan vaiheet.</span><span class="sxs-lookup"><span data-stu-id="997a7-105">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)" task guide.</span></span>

<span data-ttu-id="997a7-106">Näissä ohjeissa kerrotaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan, kun tavoitteena on luoda sähköisiä Microsoft Excel- ja Microsoft Word -asiakirjoja, jotka sisältävät upotettuja kuvia.</span><span class="sxs-lookup"><span data-stu-id="997a7-106">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="997a7-107">Tässä esimerkissä tarkistetaan ER-konfiguraatiot malliyritykselle Litware Inc.</span><span class="sxs-lookup"><span data-stu-id="997a7-107">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="997a7-108">Nämä ohjeet on tarkoitettu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="997a7-108">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="997a7-109">Vaiheet voidaan suorittaa USMF-tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="997a7-109">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="997a7-110">Tuodun tietomallin tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="997a7-110">Review the imported data model</span></span>
1. <span data-ttu-id="997a7-111">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="997a7-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="997a7-112">Valitse puussa Sekkien malli.</span><span class="sxs-lookup"><span data-stu-id="997a7-112">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="997a7-113">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="997a7-113">Click Designer.</span></span>
    * <span data-ttu-id="997a7-114">Tämä malli on suunniteltu maksusekkien esittämiseen yrityksen näkökulmasta ja tämän mallin yhdistämiseen sovelluksen tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="997a7-114">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application's data sources.</span></span> <span data-ttu-id="997a7-115">Tarkista tämä malli ER-toimintojen suunnitteluohjelman avulla.</span><span class="sxs-lookup"><span data-stu-id="997a7-115">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="997a7-116">Ota huomioon esillä olevat mallielementtien määritteet, joita ovat esimerkiksi rakenne, nimi, kuvaus ja tietotyyppi.</span><span class="sxs-lookup"><span data-stu-id="997a7-116">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="997a7-117">Laajenna puussa root.</span><span class="sxs-lookup"><span data-stu-id="997a7-117">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="997a7-118">Laajenna puussa root\cheques.</span><span class="sxs-lookup"><span data-stu-id="997a7-118">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="997a7-119">Laajenna puussa root\cheques.</span><span class="sxs-lookup"><span data-stu-id="997a7-119">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="997a7-120">Laajenna puussa root\cheques\attributes.</span><span class="sxs-lookup"><span data-stu-id="997a7-120">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="997a7-121">Laajenna puussa root\payer.</span><span class="sxs-lookup"><span data-stu-id="997a7-121">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="997a7-122">Valitse puussa root\istestrun.</span><span class="sxs-lookup"><span data-stu-id="997a7-122">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="997a7-123">Valitse puussa root\layout.</span><span class="sxs-lookup"><span data-stu-id="997a7-123">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="997a7-124">Tämän mallin asetteluelementti edustaa valitun pankkitilin tulostetun sekin lomakkeen asettelun tietoja.</span><span class="sxs-lookup"><span data-stu-id="997a7-124">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="997a7-125">Se sisältää myös kaksi Säilö-tietotyypin solmua kuvien tallentamista varten.</span><span class="sxs-lookup"><span data-stu-id="997a7-125">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="997a7-126">Laajenna puussa root\layout.</span><span class="sxs-lookup"><span data-stu-id="997a7-126">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="997a7-127">Valitse puussa root\layout\company logo.</span><span class="sxs-lookup"><span data-stu-id="997a7-127">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="997a7-128">Laajenna puussa root\layout\company logo.</span><span class="sxs-lookup"><span data-stu-id="997a7-128">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="997a7-129">Valitse puussa root\layout\company logo\image.</span><span class="sxs-lookup"><span data-stu-id="997a7-129">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="997a7-130">Valitse puussa root\layout\company logo\isprinted.</span><span class="sxs-lookup"><span data-stu-id="997a7-130">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="997a7-131">Valitse puussa root\layout\signature.</span><span class="sxs-lookup"><span data-stu-id="997a7-131">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="997a7-132">Laajenna puussa root\layout\signature.</span><span class="sxs-lookup"><span data-stu-id="997a7-132">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="997a7-133">Valitse puussa root\layout\signature\image.</span><span class="sxs-lookup"><span data-stu-id="997a7-133">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="997a7-134">Valitse puussa root\layout\signature\isprinted.</span><span class="sxs-lookup"><span data-stu-id="997a7-134">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="997a7-135">Ota huomioon, että kaksi kuvan tietomallielementtiä on sidottu sellaisen taulun kenttiin, jotka sisältävät yrityksen logon ja valtuutetun henkilön allekirjoituksen kuvat binaarisessa muodossa.</span><span class="sxs-lookup"><span data-stu-id="997a7-135">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person's signature in binary format.</span></span>  
20. <span data-ttu-id="997a7-136">Laajenna puussa root\layout\watermark.</span><span class="sxs-lookup"><span data-stu-id="997a7-136">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="997a7-137">Valitse Yhdistä malli tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="997a7-137">Click Map model to datasource.</span></span>
22. <span data-ttu-id="997a7-138">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="997a7-138">Click Designer.</span></span>
23. <span data-ttu-id="997a7-139">Laajenna puussa chequesselected.</span><span class="sxs-lookup"><span data-stu-id="997a7-139">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="997a7-140">Laajenna puussa layout.</span><span class="sxs-lookup"><span data-stu-id="997a7-140">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="997a7-141">Laajenna puussa layout\company logo.</span><span class="sxs-lookup"><span data-stu-id="997a7-141">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="997a7-142">Laajenna puussa layout\signature.</span><span class="sxs-lookup"><span data-stu-id="997a7-142">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="997a7-143">Laajenna puussa layout\watermark.</span><span class="sxs-lookup"><span data-stu-id="997a7-143">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="997a7-144">Vaihda Näytä tiedot käyttöön</span><span class="sxs-lookup"><span data-stu-id="997a7-144">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="997a7-145">Ota huomioon, että sekkien tietomallielementti on sidottu TmpChequePrintout-tauluun, joka sisältää suorituksen aikana käyttäjän tulostettavaksi valitsemien sekkien tietueita.</span><span class="sxs-lookup"><span data-stu-id="997a7-145">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="997a7-146">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="997a7-146">Close the page.</span></span>
30. <span data-ttu-id="997a7-147">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="997a7-147">Close the page.</span></span>
31. <span data-ttu-id="997a7-148">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="997a7-148">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="997a7-149">Tuodun muodon tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="997a7-149">Review the imported format</span></span>
1. <span data-ttu-id="997a7-150">Valitse puussa Model for cheques.</span><span class="sxs-lookup"><span data-stu-id="997a7-150">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="997a7-151">Valitse puussa Model for cheques\Cheques printing format.</span><span class="sxs-lookup"><span data-stu-id="997a7-151">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="997a7-152">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="997a7-152">Click Designer.</span></span>
4. <span data-ttu-id="997a7-153">Napsauta Liitteet.</span><span class="sxs-lookup"><span data-stu-id="997a7-153">Click Attachments.</span></span>
5. <span data-ttu-id="997a7-154">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="997a7-154">Click Open.</span></span>
    * <span data-ttu-id="997a7-155">Avaa Excelissä liitetyn raportin malli.</span><span class="sxs-lookup"><span data-stu-id="997a7-155">Open the attached report's template in Excel.</span></span>  
    * <span data-ttu-id="997a7-156">Tarkista sekkien tulostamisessa käytettävä liitetyn raportin Excel-malli.</span><span class="sxs-lookup"><span data-stu-id="997a7-156">Review the attached report's Excel template that will be used to print cheques.</span></span> <span data-ttu-id="997a7-157">Mallissa on kaksi sekkiä sivulla. Se on suunniteltu tulostamaan sekit esitäytettyyn lomakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="997a7-157">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="997a7-158">Ota huomioon kaksi tyhjää upotettua kuvaa.</span><span class="sxs-lookup"><span data-stu-id="997a7-158">Note that two blank images are embedded.</span></span> <span data-ttu-id="997a7-159">Nämä tyhjät kuvat on tarkoitettu yrityksen logoa ja maksun hyväksyvän henkilön allekirjoitusta varten.</span><span class="sxs-lookup"><span data-stu-id="997a7-159">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="997a7-160">Varmista, että kuvien nimet ovat Excelissä CompLogo ja SignatureImage.</span><span class="sxs-lookup"><span data-stu-id="997a7-160">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="997a7-161">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="997a7-161">Close the page.</span></span>
7. <span data-ttu-id="997a7-162">Laajenna puussa Report.</span><span class="sxs-lookup"><span data-stu-id="997a7-162">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="997a7-163">Laajenna puussa Report\ChequeLines.</span><span class="sxs-lookup"><span data-stu-id="997a7-163">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="997a7-164">Valitse puussa Report\ChequeLines\CompLogo.</span><span class="sxs-lookup"><span data-stu-id="997a7-164">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="997a7-165">Vaihda Näytä tiedot käyttöön</span><span class="sxs-lookup"><span data-stu-id="997a7-165">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="997a7-166">Ota huomioon, että CompLogo-muodon solun elementti edustaa Excel-kohdetta, jonka avulla yrityksen logon kuvan täytetään raporttiin.</span><span class="sxs-lookup"><span data-stu-id="997a7-166">Note that the 'CompLogo' format's cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="997a7-167">Tämä muotoelementti on sidottu kuvan tietomallielementtiin, joka sisältää suorituksen aikana yrityksen logon kuvan binaarisessa muodossa.</span><span class="sxs-lookup"><span data-stu-id="997a7-167">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="997a7-168">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="997a7-168">Click the Mapping tab.</span></span>
12. <span data-ttu-id="997a7-169">Valitse Muokkaus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="997a7-169">Click Edit enabled.</span></span>
    * <span data-ttu-id="997a7-170">Ota huomioon, että voit ottaa CompLogo-muodon solun elementin pois käytöstä.</span><span class="sxs-lookup"><span data-stu-id="997a7-170">Note that you can make the 'CompLogo' format's cell element so that it's no longer enabled.</span></span> <span data-ttu-id="997a7-171">Tällöin liitetty Excel-kuvaelementti piilottaa yrityksen logon luodussa raportissa.</span><span class="sxs-lookup"><span data-stu-id="997a7-171">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="997a7-172">Jos käytössä oleva lauseke palauttaa TRUE-arvon ja määritetty sidonta ei tuo kuvaa, liitetty Excel-kuvaelementti näyttää Excel-malliin tallennetun kuvan.</span><span class="sxs-lookup"><span data-stu-id="997a7-172">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="997a7-173">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="997a7-173">Close the page.</span></span>
14. <span data-ttu-id="997a7-174">Laajenna puussa labels: Container.</span><span class="sxs-lookup"><span data-stu-id="997a7-174">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="997a7-175">Jotkin esitäytetyn sekin lomakkeessa olevat nimiöt sisällytetään raporttiin, kun se luodaan testausta varten.</span><span class="sxs-lookup"><span data-stu-id="997a7-175">Some labels that are presented in the preprinted cheque form will be included in the report when it's created for testing purposes.</span></span> <span data-ttu-id="997a7-176">Näitä nimiöitä ei kuitenkaan tulosteta todellisen tulostuksen aikana, koska ne ovat jo esitäytetyssä lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="997a7-176">However, those labels won't be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="997a7-177">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="997a7-177">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]