--- 
title: "Asiakirjojen luominen päivitetyillä sovellustiedoilla sähköistä raportointia (ER) varten"
description: "Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (Osa 4 – muodon muokkaaminen) -menettely on suoritettu."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.openlocfilehash: 332cfcbdb6ccbb78d30a421adde33a12360df94b
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a><span data-ttu-id="8847a-103">Asiakirjojen luominen päivitetyillä sovellustiedoilla sähköistä raportointia (ER) varten</span><span class="sxs-lookup"><span data-stu-id="8847a-103">Generate documents with application data update for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8847a-104">Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (osa 4: muodon muokkaaminen) -menettely on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="8847a-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 4: Modify format)”.</span></span>



<span data-ttu-id="8847a-105">Tämän menettelyn vaiheissa opastetaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan sähköisen asiakirjan luomista ja sovellustietojen päivitystä varten.</span><span class="sxs-lookup"><span data-stu-id="8847a-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="8847a-106">Tässä menettelyssä suoritetaan ER-muotokonfiguraatio Intrastat-raportin luontia ja sovellustietojen päivitystä varten, jotta raportointiprosessin tiedot voidaan arkistoida.</span><span class="sxs-lookup"><span data-stu-id="8847a-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="8847a-107">Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="8847a-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="8847a-108">Nämä vaiheet voidaan suorittaa DEMF-tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="8847a-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="8847a-109">Ennen kuin aloitat, varmista, että DEMF-yrityksen maakonteksti on BEL (Belgia).</span><span class="sxs-lookup"><span data-stu-id="8847a-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="8847a-110">Määritä ulkomaankaupan parametrit</span><span class="sxs-lookup"><span data-stu-id="8847a-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="8847a-111">Valitse Vero > Asetukset > Ulkomaankauppa > Ulkomaankaupan parametrit.</span><span class="sxs-lookup"><span data-stu-id="8847a-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="8847a-112">Valitse Numerojärjestykset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="8847a-112">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="8847a-113">Intrastat-raportointiprosessin tietojen arkistointia varten on tunnistettava kunkin luodun arkiston tietueet.</span><span class="sxs-lookup"><span data-stu-id="8847a-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="8847a-114">Sitä varten on määritettävä myös erityinen numerosarja.</span><span class="sxs-lookup"><span data-stu-id="8847a-114">A special number sequence must be configured for that.</span></span>  
3. <span data-ttu-id="8847a-115">Valitse Intrastat-arkiston tunnus -viite.</span><span class="sxs-lookup"><span data-stu-id="8847a-115">Select the ‘Intrastat archive ID’ reference.</span></span>
4. <span data-ttu-id="8847a-116">Kirjoita arvo Numerosarjan koodi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="8847a-116">In the Number sequence code field, type a value.</span></span>
    * <span data-ttu-id="8847a-117">Anna tai valitse Numerosarjan koodi -kenttään Fore_2-arvo.</span><span class="sxs-lookup"><span data-stu-id="8847a-117">In the ‘Number sequence code’ field, enter or select the value ‘Fore_2’.</span></span>  
5. <span data-ttu-id="8847a-118">Ratkaise muutokset numerosarjan koodissa.</span><span class="sxs-lookup"><span data-stu-id="8847a-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="8847a-119">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8847a-119">Click Save.</span></span>
7. <span data-ttu-id="8847a-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8847a-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="8847a-121">Muokatun ER-muodon suorittaminen</span><span class="sxs-lookup"><span data-stu-id="8847a-121">Run modified ER format</span></span>
1. <span data-ttu-id="8847a-122">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="8847a-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="8847a-123">Laajenna puussa Intrastat (model).</span><span class="sxs-lookup"><span data-stu-id="8847a-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="8847a-124">Valitse puussa Intrastat (model)\Intrastat (format).</span><span class="sxs-lookup"><span data-stu-id="8847a-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="8847a-125">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="8847a-125">Click Run.</span></span>
5. <span data-ttu-id="8847a-126">Kirjoita Syötä tiedostonimi -kenttään intrastat2.xml.</span><span class="sxs-lookup"><span data-stu-id="8847a-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
    * <span data-ttu-id="8847a-127">intrastat2.xml</span><span class="sxs-lookup"><span data-stu-id="8847a-127">intrastat2.xml</span></span>  
6. <span data-ttu-id="8847a-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8847a-128">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="8847a-129">ER-muodon suorittamisen tulosten tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="8847a-129">Review ER format execution’s results</span></span>
    * <span data-ttu-id="8847a-130">Tarkista luotu XML-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="8847a-130">Review the generated XML file.</span></span>  
1. <span data-ttu-id="8847a-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8847a-131">Close the page.</span></span>
2. <span data-ttu-id="8847a-132">Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="8847a-132">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="8847a-133">Avaa tämä sähköiseen asiakirjaan sisällytetyt Intrastat-tapahtumat sisältävä lomake.</span><span class="sxs-lookup"><span data-stu-id="8847a-133">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  
3. <span data-ttu-id="8847a-134">Valitse Intrastat-arkisto.</span><span class="sxs-lookup"><span data-stu-id="8847a-134">Click Intrastat archive.</span></span>
    * <span data-ttu-id="8847a-135">Koska suoritettu ER-muoto sisältää nyt sovellustietojen päivityksen asetukset, valmiin Intrastat-raportoinnin tiedot on arkistoitu.</span><span class="sxs-lookup"><span data-stu-id="8847a-135">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="8847a-136">Tämä lomake sisältää luodun arkiston otsikkotietueen.</span><span class="sxs-lookup"><span data-stu-id="8847a-136">In this form, you can see the header record of the created archive.</span></span>  
4. <span data-ttu-id="8847a-137">Valitse Erittely.</span><span class="sxs-lookup"><span data-stu-id="8847a-137">Click Details.</span></span>
    * <span data-ttu-id="8847a-138">Tämä lomake sisältää luodun arkiston tiedot.</span><span class="sxs-lookup"><span data-stu-id="8847a-138">In this form, you can see the details for the created archive.</span></span>  
5. <span data-ttu-id="8847a-139">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8847a-139">Close the page.</span></span>
6. <span data-ttu-id="8847a-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8847a-140">Close the page.</span></span>
7. <span data-ttu-id="8847a-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8847a-141">Close the page.</span></span>


