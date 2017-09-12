--- 
title: "Asiakirjojen luominen päivitetyillä sovellustiedoilla sähköistä raportointia (ER) varten"
description: "Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (Osa 1 – konfiguraatioiden tuominen) -menettely on suoritettu."
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
ms.openlocfilehash: aa737abc9273e0068d864416ffb85302468088ed
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a><span data-ttu-id="66da0-103">Asiakirjojen luominen päivitetyillä sovellustiedoilla sähköistä raportointia (ER) varten</span><span class="sxs-lookup"><span data-stu-id="66da0-103">Generate documents with application data update for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="66da0-104">Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (osa 1: konfiguraatioiden tuominen) -menettely on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="66da0-104">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="66da0-105">Tämän menettelyn vaiheissa opastetaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan sähköisen asiakirjan luomista varten.</span><span class="sxs-lookup"><span data-stu-id="66da0-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="66da0-106">Tässä menettelyssä suoritetaan tuotu ER-muotokonfiguraatio, joka on luotu malliyritykselle Litware Inc. sähköisten asiakirjojen luomista varten.</span><span class="sxs-lookup"><span data-stu-id="66da0-106">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="66da0-107">Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="66da0-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="66da0-108">Nämä vaiheet voidaan suorittaa DEMF-tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="66da0-108">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="66da0-109">Ennen kuin aloitat, muuta DEMF-yrityksen maakonteksti DEU (Saksa) -arvosta BEL (Belgia) -arvoksi.</span><span class="sxs-lookup"><span data-stu-id="66da0-109">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="66da0-110">Valitse Organisaation hallinto > Organisaatiot > Yritykset, kun haluat päivittää yrityksen DEMF ensisijaisen osoitteen maakoodin.</span><span class="sxs-lookup"><span data-stu-id="66da0-110">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="66da0-111">Käynnistä sovellus uudelleen.</span><span class="sxs-lookup"><span data-stu-id="66da0-111">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="66da0-112">Tuodun ER-muodon suorittaminen</span><span class="sxs-lookup"><span data-stu-id="66da0-112">Run imported ER format</span></span>
1. <span data-ttu-id="66da0-113">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="66da0-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="66da0-114">Laajenna puussa Intrastat (model).</span><span class="sxs-lookup"><span data-stu-id="66da0-114">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="66da0-115">Valitse puussa Intrastat (model)\Intrastat (format).</span><span class="sxs-lookup"><span data-stu-id="66da0-115">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="66da0-116">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="66da0-116">Click Run.</span></span>
    * <span data-ttu-id="66da0-117">Suorita ER-muotokonfiguraation luonnosversio, kun haluat luoda Intrastat-raportin.</span><span class="sxs-lookup"><span data-stu-id="66da0-117">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="66da0-118">Kirjoita Syötä tiedostonimi -kenttään intrastat.xml.</span><span class="sxs-lookup"><span data-stu-id="66da0-118">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="66da0-119">Anna tiedoston nimi.</span><span class="sxs-lookup"><span data-stu-id="66da0-119">Specify the name of the file.</span></span>  
6. <span data-ttu-id="66da0-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="66da0-120">Click OK.</span></span>
    * <span data-ttu-id="66da0-121">Tarkista luotu XML-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="66da0-121">Review the generated XML file.</span></span>  
7. <span data-ttu-id="66da0-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="66da0-122">Close the page.</span></span>
8. <span data-ttu-id="66da0-123">Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="66da0-123">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="66da0-124">Avaa tämä lomake, kun haluat tarkastella luodun sähköisen asiakirjan Intrastat-tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="66da0-124">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="66da0-125">Valitse Intrastat-arkisto.</span><span class="sxs-lookup"><span data-stu-id="66da0-125">Click Intrastat archive.</span></span>
    * <span data-ttu-id="66da0-126">Koska suoritettu ER-muoto ei sisällä sovellustietojen päivityksen asetuksia, valmiin Intrastat-raportin tietoja ei ole arkistoitu.</span><span class="sxs-lookup"><span data-stu-id="66da0-126">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="66da0-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="66da0-127">Close the page.</span></span>
11. <span data-ttu-id="66da0-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="66da0-128">Close the page.</span></span>


