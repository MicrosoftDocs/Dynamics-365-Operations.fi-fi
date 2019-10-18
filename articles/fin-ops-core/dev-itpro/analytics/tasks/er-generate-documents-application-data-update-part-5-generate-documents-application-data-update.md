---
title: Luo sovellustietoja sisältäviä asiakirjoja
description: Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (Osa 4 – muodon muokkaaminen) -menettely on suoritettu.
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
ms.openlocfilehash: 1d95feb3395c36f9cf8a23770dc3173377067d9b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184873"
---
# <a name="generate-documents-that-have-application-data"></a><span data-ttu-id="a59e3-103">Luo sovellustietoja sisältäviä asiakirjoja</span><span class="sxs-lookup"><span data-stu-id="a59e3-103">Generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a59e3-104">Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (osa 4: muodon muokkaaminen) -menettely on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="a59e3-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 4: Modify format)”.</span></span>



<span data-ttu-id="a59e3-105">Tämän menettelyn vaiheissa opastetaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan sähköisen asiakirjan luomista ja sovellustietojen päivitystä varten.</span><span class="sxs-lookup"><span data-stu-id="a59e3-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="a59e3-106">Tässä menettelyssä suoritetaan ER-muotokonfiguraatio Intrastat-raportin luontia ja sovellustietojen päivitystä varten, jotta raportointiprosessin tiedot voidaan arkistoida.</span><span class="sxs-lookup"><span data-stu-id="a59e3-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="a59e3-107">Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="a59e3-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="a59e3-108">Nämä vaiheet voidaan suorittaa DEMF-tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="a59e3-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="a59e3-109">Ennen kuin aloitat, varmista, että DEMF-yrityksen maakonteksti on BEL (Belgia).</span><span class="sxs-lookup"><span data-stu-id="a59e3-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="a59e3-110">Määritä ulkomaankaupan parametrit</span><span class="sxs-lookup"><span data-stu-id="a59e3-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="a59e3-111">Valitse Vero > Asetukset > Ulkomaankauppa > Ulkomaankaupan parametrit.</span><span class="sxs-lookup"><span data-stu-id="a59e3-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="a59e3-112">Valitse Numerojärjestykset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="a59e3-112">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="a59e3-113">Intrastat-raportointiprosessin tietojen arkistointia varten on tunnistettava kunkin luodun arkiston tietueet.</span><span class="sxs-lookup"><span data-stu-id="a59e3-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="a59e3-114">Sitä varten on määritettävä myös erityinen numerosarja.</span><span class="sxs-lookup"><span data-stu-id="a59e3-114">A special number sequence must be configured for that.</span></span>  
3. <span data-ttu-id="a59e3-115">Valitse Intrastat-arkiston tunnus -viite.</span><span class="sxs-lookup"><span data-stu-id="a59e3-115">Select the ‘Intrastat archive ID’ reference.</span></span>
4. <span data-ttu-id="a59e3-116">Kirjoita arvo Numerosarjan koodi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="a59e3-116">In the Number sequence code field, type a value.</span></span>
    * <span data-ttu-id="a59e3-117">Anna tai valitse Numerosarjan koodi -kenttään Fore_2-arvo.</span><span class="sxs-lookup"><span data-stu-id="a59e3-117">In the ‘Number sequence code’ field, enter or select the value ‘Fore_2’.</span></span>  
5. <span data-ttu-id="a59e3-118">Ratkaise muutokset numerosarjan koodissa.</span><span class="sxs-lookup"><span data-stu-id="a59e3-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="a59e3-119">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a59e3-119">Click Save.</span></span>
7. <span data-ttu-id="a59e3-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a59e3-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="a59e3-121">Muokatun ER-muodon suorittaminen</span><span class="sxs-lookup"><span data-stu-id="a59e3-121">Run modified ER format</span></span>
1. <span data-ttu-id="a59e3-122">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="a59e3-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a59e3-123">Laajenna puussa Intrastat (model).</span><span class="sxs-lookup"><span data-stu-id="a59e3-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="a59e3-124">Valitse puussa Intrastat (model)\Intrastat (format).</span><span class="sxs-lookup"><span data-stu-id="a59e3-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="a59e3-125">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="a59e3-125">Click Run.</span></span>
5. <span data-ttu-id="a59e3-126">Kirjoita Syötä tiedostonimi -kenttään intrastat2.xml.</span><span class="sxs-lookup"><span data-stu-id="a59e3-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
    * <span data-ttu-id="a59e3-127">intrastat2.xml</span><span class="sxs-lookup"><span data-stu-id="a59e3-127">intrastat2.xml</span></span>  
6. <span data-ttu-id="a59e3-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a59e3-128">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="a59e3-129">ER-muodon suorittamisen tulosten tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="a59e3-129">Review ER format execution’s results</span></span>
    * <span data-ttu-id="a59e3-130">Tarkista luotu XML-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="a59e3-130">Review the generated XML file.</span></span>  
1. <span data-ttu-id="a59e3-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a59e3-131">Close the page.</span></span>
2. <span data-ttu-id="a59e3-132">Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="a59e3-132">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="a59e3-133">Avaa tämä sähköiseen asiakirjaan sisällytetyt Intrastat-tapahtumat sisältävä lomake.</span><span class="sxs-lookup"><span data-stu-id="a59e3-133">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  
3. <span data-ttu-id="a59e3-134">Valitse Intrastat-arkisto.</span><span class="sxs-lookup"><span data-stu-id="a59e3-134">Click Intrastat archive.</span></span>
    * <span data-ttu-id="a59e3-135">Koska suoritettu ER-muoto sisältää nyt sovellustietojen päivityksen asetukset, valmiin Intrastat-raportoinnin tiedot on arkistoitu.</span><span class="sxs-lookup"><span data-stu-id="a59e3-135">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="a59e3-136">Tämä lomake sisältää luodun arkiston otsikkotietueen.</span><span class="sxs-lookup"><span data-stu-id="a59e3-136">In this form, you can see the header record of the created archive.</span></span>  
4. <span data-ttu-id="a59e3-137">Valitse Erittely.</span><span class="sxs-lookup"><span data-stu-id="a59e3-137">Click Details.</span></span>
    * <span data-ttu-id="a59e3-138">Tämä lomake sisältää luodun arkiston tiedot.</span><span class="sxs-lookup"><span data-stu-id="a59e3-138">In this form, you can see the details for the created archive.</span></span>  
5. <span data-ttu-id="a59e3-139">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a59e3-139">Close the page.</span></span>
6. <span data-ttu-id="a59e3-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a59e3-140">Close the page.</span></span>
7. <span data-ttu-id="a59e3-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a59e3-141">Close the page.</span></span>
