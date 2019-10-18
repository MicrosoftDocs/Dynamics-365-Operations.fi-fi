---
title: Suunnittele konfiguraatioita luodaksesi sovellustietoja sisältäviä asiakirjoja
description: Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (Osa 1 – konfiguraatioiden tuominen) -menettely on suoritettu.
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
ms.openlocfilehash: 9aec1da7fe168b05af10470221ac745ec1c01f6b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182321"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="795c5-103">Suunnittele konfiguraatioita luodaksesi sovellustietoja sisältäviä asiakirjoja</span><span class="sxs-lookup"><span data-stu-id="795c5-103">Design configurations to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="795c5-104">Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (osa 1: konfiguraatioiden tuominen) -menettely on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="795c5-104">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="795c5-105">Tämän menettelyn vaiheissa opastetaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan sähköisen asiakirjan luomista varten.</span><span class="sxs-lookup"><span data-stu-id="795c5-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="795c5-106">Tässä menettelyssä suoritetaan tuotu ER-muotokonfiguraatio, joka on luotu malliyritykselle Litware Inc. sähköisten asiakirjojen luomista varten.</span><span class="sxs-lookup"><span data-stu-id="795c5-106">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="795c5-107">Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="795c5-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="795c5-108">Nämä vaiheet voidaan suorittaa DEMF-tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="795c5-108">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="795c5-109">Ennen kuin aloitat, muuta DEMF-yrityksen maakonteksti DEU (Saksa) -arvosta BEL (Belgia) -arvoksi.</span><span class="sxs-lookup"><span data-stu-id="795c5-109">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="795c5-110">Valitse Organisaation hallinto > Organisaatiot > Yritykset, kun haluat päivittää yrityksen DEMF ensisijaisen osoitteen maakoodin.</span><span class="sxs-lookup"><span data-stu-id="795c5-110">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="795c5-111">Käynnistä sovellus uudelleen.</span><span class="sxs-lookup"><span data-stu-id="795c5-111">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="795c5-112">Tuodun ER-muodon suorittaminen</span><span class="sxs-lookup"><span data-stu-id="795c5-112">Run imported ER format</span></span>
1. <span data-ttu-id="795c5-113">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="795c5-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="795c5-114">Laajenna puussa Intrastat (model).</span><span class="sxs-lookup"><span data-stu-id="795c5-114">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="795c5-115">Valitse puussa Intrastat (model)\Intrastat (format).</span><span class="sxs-lookup"><span data-stu-id="795c5-115">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="795c5-116">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="795c5-116">Click Run.</span></span>
    * <span data-ttu-id="795c5-117">Suorita ER-muotokonfiguraation luonnosversio, kun haluat luoda Intrastat-raportin.</span><span class="sxs-lookup"><span data-stu-id="795c5-117">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="795c5-118">Kirjoita Syötä tiedostonimi -kenttään intrastat.xml.</span><span class="sxs-lookup"><span data-stu-id="795c5-118">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="795c5-119">Anna tiedoston nimi.</span><span class="sxs-lookup"><span data-stu-id="795c5-119">Specify the name of the file.</span></span>  
6. <span data-ttu-id="795c5-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="795c5-120">Click OK.</span></span>
    * <span data-ttu-id="795c5-121">Tarkista luotu XML-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="795c5-121">Review the generated XML file.</span></span>  
7. <span data-ttu-id="795c5-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="795c5-122">Close the page.</span></span>
8. <span data-ttu-id="795c5-123">Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="795c5-123">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="795c5-124">Avaa tämä lomake, kun haluat tarkastella luodun sähköisen asiakirjan Intrastat-tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="795c5-124">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="795c5-125">Valitse Intrastat-arkisto.</span><span class="sxs-lookup"><span data-stu-id="795c5-125">Click Intrastat archive.</span></span>
    * <span data-ttu-id="795c5-126">Koska suoritettu ER-muoto ei sisällä sovellustietojen päivityksen asetuksia, valmiin Intrastat-raportin tietoja ei ole arkistoitu.</span><span class="sxs-lookup"><span data-stu-id="795c5-126">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="795c5-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="795c5-127">Close the page.</span></span>
11. <span data-ttu-id="795c5-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="795c5-128">Close the page.</span></span>

