---
title: Konfiguraatioiden suunnitteleminen raporttien luomiseksi Office-muodoissa, joissa on upotettuja kuvia
description: Tässä aiheessa käsitellään määritysten suunnittelua luomaan upotettuja kuvia sisältäviä Excel- ja Word-muotoisia sähköisiä asiakirjoja.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944554"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="c74ec-103">Konfiguraatioiden suunnitteleminen raporttien luomiseksi Office-muodoissa, joissa on upotettuja kuvia</span><span class="sxs-lookup"><span data-stu-id="c74ec-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c74ec-104">ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen tämän menettelyn vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="c74ec-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="c74ec-105">Näissä ohjeissa kerrotaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan, kun tavoitteena on luoda Microsoft Excel- ja Word -asiakirjoja, jotka sisältävät upotettuja kuvia.</span><span class="sxs-lookup"><span data-stu-id="c74ec-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="c74ec-106">Tässä menettelyssä luodaan pakollisia ER-konfiguraatioita malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa USMF-tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="c74ec-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="c74ec-107">Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="c74ec-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="c74ec-108">Ennen aloittamista seuraavat tiedostot täytyy ladata ja tallentaa:</span><span class="sxs-lookup"><span data-stu-id="c74ec-108">Before you begin, download and save the following files:</span></span> 

| <span data-ttu-id="c74ec-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="c74ec-109">Description</span></span>                                          | <span data-ttu-id="c74ec-110">Tiedostonimi</span><span class="sxs-lookup"><span data-stu-id="c74ec-110">File name</span></span>                   |
|------------------------------------------------------|-----------------------------|
| <span data-ttu-id="c74ec-111">ER-tietomallin konfigurointi</span><span class="sxs-lookup"><span data-stu-id="c74ec-111">ER data model configuration</span></span>                          | [<span data-ttu-id="c74ec-112">Model for cheques.xml</span><span class="sxs-lookup"><span data-stu-id="c74ec-112">Model for cheques.xml</span></span>](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| <span data-ttu-id="c74ec-113">ER-muodon konfigurointi</span><span class="sxs-lookup"><span data-stu-id="c74ec-113">ER format configuration</span></span>                              | [<span data-ttu-id="c74ec-114">Cheques printing format.xml</span><span class="sxs-lookup"><span data-stu-id="c74ec-114">Cheques printing format.xml</span></span>](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| <span data-ttu-id="c74ec-115">Yrityksen logokuva</span><span class="sxs-lookup"><span data-stu-id="c74ec-115">Company logo image</span></span>                                   | [<span data-ttu-id="c74ec-116">Yrityksen logo.png</span><span class="sxs-lookup"><span data-stu-id="c74ec-116">Company logo.png</span></span>](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| <span data-ttu-id="c74ec-117">Allekirjoituksen kuva</span><span class="sxs-lookup"><span data-stu-id="c74ec-117">Signature image</span></span>                                      | [<span data-ttu-id="c74ec-118">Allekirjoituksen kuva.png</span><span class="sxs-lookup"><span data-stu-id="c74ec-118">Signature image.png</span></span>](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| <span data-ttu-id="c74ec-119">Vaihtoehtoisen allekirjoituksen kuva</span><span class="sxs-lookup"><span data-stu-id="c74ec-119">Alternative signature image</span></span>                          | [<span data-ttu-id="c74ec-120">Allekirjoituksen kuva 2.png</span><span class="sxs-lookup"><span data-stu-id="c74ec-120">Signature image 2.png</span></span>](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| <span data-ttu-id="c74ec-121">Microsoft Word -malli sekkien tulostukseen</span><span class="sxs-lookup"><span data-stu-id="c74ec-121">Microsoft Word template for printing payment checks</span></span>  | [<span data-ttu-id="c74ec-122">Sekkimalli Word.docx</span><span class="sxs-lookup"><span data-stu-id="c74ec-122">Cheque template Word.docx</span></span>](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a><span data-ttu-id="c74ec-123">Edellytysten tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="c74ec-123">Verify prerequisites</span></span>  
 1. <span data-ttu-id="c74ec-124">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="c74ec-124">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="c74ec-125">Varmista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="c74ec-125">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="c74ec-126">Jos konfiguraation lähde ei ole näkyvissä, suorita Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="c74ec-126">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="c74ec-127">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="c74ec-127">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="c74ec-128">Uuden ER-mallimäärityksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="c74ec-128">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="c74ec-129">Uuden mallin luomisen sijaan voit ladata ER-mallimääritystiedoston (Model for cheques.xml), jonka tallensit aiemmin.</span><span class="sxs-lookup"><span data-stu-id="c74ec-129">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="c74ec-130">Tämä tiedosto sisältää maksusekkien tietomalliesimerkin ja tietomallin Dynamics 365 for Operations -sovelluksen vastaavuuden tieto-osiin.</span><span class="sxs-lookup"><span data-stu-id="c74ec-130">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="c74ec-131">Valitse Versiot-pikavälilehdessä Vaihda.</span><span class="sxs-lookup"><span data-stu-id="c74ec-131">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="c74ec-132">Valitse Lataa XML-tiedostosta.</span><span class="sxs-lookup"><span data-stu-id="c74ec-132">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="c74ec-133">Valitse Selaa ja valitse sitten Model for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="c74ec-133">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="c74ec-134">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c74ec-134">Click OK.</span></span>  
 6. <span data-ttu-id="c74ec-135">Ladattua mallia käytetään tietolähteenä luotaessa asiakirjoja, jotka sisältävät Excelin tai Wordin kuvia.</span><span class="sxs-lookup"><span data-stu-id="c74ec-135">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="c74ec-136">Uuden ER-muotokonfiguraation lisääminen</span><span class="sxs-lookup"><span data-stu-id="c74ec-136">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="c74ec-137">Uuden muodon luomisen sijaan voit ladata ER-muotomääritystiedoston (Cheques printing format.xml), jonka tallensit aiemmin.</span><span class="sxs-lookup"><span data-stu-id="c74ec-137">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="c74ec-138">Tämä tiedosto sisältää sekkien tulostamisen muodon malliasettelun. Se käyttää esitäytettyä lomaketta ja tämän muodon vastaavuutta Model for cheques -tiedoston tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="c74ec-138">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="c74ec-139">Valitse Vaihto.</span><span class="sxs-lookup"><span data-stu-id="c74ec-139">Click Exchange.</span></span>  
 3. <span data-ttu-id="c74ec-140">Valitse Lataa XML-tiedostosta.</span><span class="sxs-lookup"><span data-stu-id="c74ec-140">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="c74ec-141">Valitse Selaa ja valitse sitten tiedosto Cheques printing format.xml.</span><span class="sxs-lookup"><span data-stu-id="c74ec-141">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="c74ec-142">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c74ec-142">Click OK.</span></span>  
 6. <span data-ttu-id="c74ec-143">Valitse puussa Model for cheques.</span><span class="sxs-lookup"><span data-stu-id="c74ec-143">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="c74ec-144">Valitse puussa Model for cheques\Cheques printing format.</span><span class="sxs-lookup"><span data-stu-id="c74ec-144">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="c74ec-145">Ladattua muotoa käytetään luotaessa asiakirjoja, jotka sisältävät Excelin tai Wordin kuvia.</span><span class="sxs-lookup"><span data-stu-id="c74ec-145">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="c74ec-146">ER-käyttäjän parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c74ec-146">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="c74ec-147">Valitse toimintoruudussa Konfiguroinnit.</span><span class="sxs-lookup"><span data-stu-id="c74ec-147">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="c74ec-148">Valitse Käyttäjän parametrit.</span><span class="sxs-lookup"><span data-stu-id="c74ec-148">Click User parameters.</span></span>  
 3. <span data-ttu-id="c74ec-149">Valitse Suorita asetukset -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="c74ec-149">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="c74ec-150">Ota käyttöön Suorita luonnos -osoitin, kun haluat aloittaa valitun mallin luonnosversiolla valmiin version sijaan.</span><span class="sxs-lookup"><span data-stu-id="c74ec-150">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="c74ec-151">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c74ec-151">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="c74ec-152">Määritä Maksuliikennetiedot</span><span class="sxs-lookup"><span data-stu-id="c74ec-152">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="c74ec-153">Valitse Maksuliikenteen hallinta > Pankkitilit > Pankkitilit.</span><span class="sxs-lookup"><span data-stu-id="c74ec-153">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="c74ec-154">Pikasuodattimen avulla voit suodattaa Pankkitili-kentän USMF OPER -arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="c74ec-154">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="c74ec-155">Valitse toimintoruudussa Määritä.</span><span class="sxs-lookup"><span data-stu-id="c74ec-155">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="c74ec-156">Valitse Tarkista.</span><span class="sxs-lookup"><span data-stu-id="c74ec-156">Click Check.</span></span>  
 5. <span data-ttu-id="c74ec-157">Laajenna osa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="c74ec-157">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="c74ec-158">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="c74ec-158">Click Edit.</span></span>  
 7. <span data-ttu-id="c74ec-159">Valitse Yrityksen logo -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="c74ec-159">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="c74ec-160">Valitse Yrityksen logo.</span><span class="sxs-lookup"><span data-stu-id="c74ec-160">Click Company logo.</span></span>  
 9. <span data-ttu-id="c74ec-161">Valitse Muuta.</span><span class="sxs-lookup"><span data-stu-id="c74ec-161">Click Change.</span></span>  
 10. <span data-ttu-id="c74ec-162">Valitse Selaa ja valitse sitten aiemmin ladattu tiedosto Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="c74ec-162">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="c74ec-163">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c74ec-163">Click Save.</span></span>  
 12. <span data-ttu-id="c74ec-164">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c74ec-164">Close the page.</span></span>  
 13. <span data-ttu-id="c74ec-165">Laajenna Allekirjoitus-osa.</span><span class="sxs-lookup"><span data-stu-id="c74ec-165">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="c74ec-166">Valitse Tulosta ensimmäinen allekirjoitus -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="c74ec-166">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="c74ec-167">Valitse Muuta.</span><span class="sxs-lookup"><span data-stu-id="c74ec-167">Click Change.</span></span>  
 16. <span data-ttu-id="c74ec-168">Valitse Selaa ja valitse sitten aiemmin ladattu tiedosto Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="c74ec-168">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="c74ec-169">Laajenna Kopiot-osa.</span><span class="sxs-lookup"><span data-stu-id="c74ec-169">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="c74ec-170">Valitse vaihtoehto Vesileima-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c74ec-170">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="c74ec-171">Valitse Yleinen sähköinen vientimuoto -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="c74ec-171">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="c74ec-172">Valitse Sekkien tulostusmuoto -konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="c74ec-172">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="c74ec-173">Nyt valittua ER-muotoa käytetään sekkien tulostamisessa.</span><span class="sxs-lookup"><span data-stu-id="c74ec-173">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="c74ec-174">Valitse Liitä.</span><span class="sxs-lookup"><span data-stu-id="c74ec-174">Click Attach.</span></span>  
 23. <span data-ttu-id="c74ec-175">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c74ec-175">Click New.</span></span>  
 24. <span data-ttu-id="c74ec-176">Napsauta Tiedosto.</span><span class="sxs-lookup"><span data-stu-id="c74ec-176">Click File.</span></span>  
 25. <span data-ttu-id="c74ec-177">Valitse Selaa ja valitse sitten aiemmin ladattu tiedosto Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="c74ec-177">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="c74ec-178">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c74ec-178">Close the page.</span></span>  
 27. <span data-ttu-id="c74ec-179">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c74ec-179">Close the page.</span></span>  
 28. <span data-ttu-id="c74ec-180">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c74ec-180">Close the page.</span></span>  
 29. <span data-ttu-id="c74ec-181">Valitse Maksuliikenteen hallinta > Asetukset > Maksuliikennetiedot.</span><span class="sxs-lookup"><span data-stu-id="c74ec-181">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="c74ec-182">Valitse Kyllä kohdassa Salli esilaskun luonti käytöstä poistetuille pankkitileille: kenttä.</span><span class="sxs-lookup"><span data-stu-id="c74ec-182">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="c74ec-183">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c74ec-183">Click Save.</span></span>  
 32. <span data-ttu-id="c74ec-184">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c74ec-184">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
