---
title: Konfiguraatioiden suunnitteleminen raporttien luomiseksi Office-muodoissa, joissa on upotettuja kuvia
description: Tässä aiheessa käsitellään määritysten suunnittelua luomaan upotettuja kuvia sisältäviä Excel- ja Word-muotoisia sähköisiä asiakirjoja.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b60ed6b07851c44ceb4b8f313bc65f04b802e646
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093667"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="5f4ad-103">Konfiguraatioiden suunnitteleminen raporttien luomiseksi Office-muodoissa, joissa on upotettuja kuvia</span><span class="sxs-lookup"><span data-stu-id="5f4ad-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5f4ad-104">ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen tämän menettelyn vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="5f4ad-105">Näissä ohjeissa kerrotaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan, kun tavoitteena on luoda Microsoft Excel- ja Word -asiakirjoja, jotka sisältävät upotettuja kuvia.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="5f4ad-106">Tässä menettelyssä luodaan pakollisia ER-konfiguraatioita malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa USMF-tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="5f4ad-107">Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="5f4ad-108">Ennen kuin aloitat, lataa ja tallenna kohdan [Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](../electronic-reporting-embed-images-shapes.md) tiedostot.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in documents that you generate by using ER](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="5f4ad-109">Tiedostot ovat seuraavat: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png ja Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="5f4ad-110">Edellytysten tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="5f4ad-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="5f4ad-111">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="5f4ad-112">Varmista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="5f4ad-113">Jos konfiguraation lähde ei ole näkyvissä, suorita Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-113">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="5f4ad-114">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="5f4ad-115">Uuden ER-mallimäärityksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="5f4ad-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="5f4ad-116">Uuden mallin luomisen sijaan voit ladata ER-mallimääritystiedoston (Model for cheques.xml), jonka tallensit aiemmin.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="5f4ad-117">Tämä tiedosto sisältää maksusekkien tietomalliesimerkin ja tietomallin Dynamics 365 for Operations -sovelluksen vastaavuuden tieto-osiin.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="5f4ad-118">Valitse Versiot-pikavälilehdessä Vaihda.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="5f4ad-119">Valitse Lataa XML-tiedostosta.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="5f4ad-120">Valitse Selaa ja valitse sitten Model for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="5f4ad-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-121">Click OK.</span></span>  
 6. <span data-ttu-id="5f4ad-122">Ladattua mallia käytetään tietolähteenä luotaessa asiakirjoja, jotka sisältävät Excelin tai Wordin kuvia.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="5f4ad-123">Uuden ER-muotokonfiguraation lisääminen</span><span class="sxs-lookup"><span data-stu-id="5f4ad-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="5f4ad-124">Uuden muodon luomisen sijaan voit ladata ER-muotomääritystiedoston (Cheques printing format.xml), jonka tallensit aiemmin.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="5f4ad-125">Tämä tiedosto sisältää sekkien tulostamisen muodon malliasettelun. Se käyttää esitäytettyä lomaketta ja tämän muodon vastaavuutta Model for cheques -tiedoston tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="5f4ad-126">Valitse Vaihto.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="5f4ad-127">Valitse Lataa XML-tiedostosta.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="5f4ad-128">Valitse Selaa ja valitse sitten tiedosto Cheques printing format.xml.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="5f4ad-129">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-129">Click OK.</span></span>  
 6. <span data-ttu-id="5f4ad-130">Valitse puussa Model for cheques.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="5f4ad-131">Valitse puussa Model for cheques\Cheques printing format.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="5f4ad-132">Ladattua muotoa käytetään luotaessa asiakirjoja, jotka sisältävät Excelin tai Wordin kuvia.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="5f4ad-133">ER-käyttäjän parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5f4ad-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="5f4ad-134">Valitse toimintoruudussa Konfiguroinnit.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="5f4ad-135">Valitse Käyttäjän parametrit.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="5f4ad-136">Valitse Suorita asetukset -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="5f4ad-137">Ota käyttöön Suorita luonnos -osoitin, kun haluat aloittaa valitun mallin luonnosversiolla valmiin version sijaan.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-137">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="5f4ad-138">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="5f4ad-139">Määritä Maksuliikennetiedot</span><span class="sxs-lookup"><span data-stu-id="5f4ad-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="5f4ad-140">Valitse Maksuliikenteen hallinta > Pankkitilit > Pankkitilit.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="5f4ad-141">Pikasuodattimen avulla voit suodattaa Pankkitili-kentän USMF OPER -arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="5f4ad-142">Valitse toimintoruudussa Määritä.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="5f4ad-143">Valitse Tarkista.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-143">Click Check.</span></span>  
 5. <span data-ttu-id="5f4ad-144">Laajenna osa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="5f4ad-145">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-145">Click Edit.</span></span>  
 7. <span data-ttu-id="5f4ad-146">Valitse Yrityksen logo -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="5f4ad-147">Valitse Yrityksen logo.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="5f4ad-148">Valitse Muuta.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-148">Click Change.</span></span>  
 10. <span data-ttu-id="5f4ad-149">Valitse Selaa ja valitse sitten aiemmin ladattu tiedosto Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="5f4ad-150">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-150">Click Save.</span></span>  
 12. <span data-ttu-id="5f4ad-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-151">Close the page.</span></span>  
 13. <span data-ttu-id="5f4ad-152">Laajenna Allekirjoitus-osa.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="5f4ad-153">Valitse Tulosta ensimmäinen allekirjoitus -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="5f4ad-154">Valitse Muuta.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-154">Click Change.</span></span>  
 16. <span data-ttu-id="5f4ad-155">Valitse Selaa ja valitse sitten aiemmin ladattu tiedosto Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="5f4ad-156">Laajenna Kopiot-osa.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="5f4ad-157">Valitse vaihtoehto Vesileima-kentässä.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="5f4ad-158">Valitse Yleinen sähköinen vientimuoto -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="5f4ad-159">Valitse Sekkien tulostusmuoto -konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="5f4ad-160">Nyt valittua ER-muotoa käytetään sekkien tulostamisessa.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="5f4ad-161">Valitse Liitä.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-161">Click Attach.</span></span>  
 23. <span data-ttu-id="5f4ad-162">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-162">Click New.</span></span>  
 24. <span data-ttu-id="5f4ad-163">Napsauta Tiedosto.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-163">Click File.</span></span>  
 25. <span data-ttu-id="5f4ad-164">Valitse Selaa ja valitse sitten aiemmin ladattu tiedosto Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="5f4ad-165">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-165">Close the page.</span></span>  
 27. <span data-ttu-id="5f4ad-166">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-166">Close the page.</span></span>  
 28. <span data-ttu-id="5f4ad-167">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-167">Close the page.</span></span>  
 29. <span data-ttu-id="5f4ad-168">Valitse Maksuliikenteen hallinta > Asetukset > Maksuliikennetiedot.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="5f4ad-169">Valitse Kyllä kohdassa Salli esilaskun luonti käytöstä poistetuille pankkitileille: kenttä.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="5f4ad-170">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-170">Click Save.</span></span>  
 32. <span data-ttu-id="5f4ad-171">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5f4ad-171">Close the page.</span></span>  
