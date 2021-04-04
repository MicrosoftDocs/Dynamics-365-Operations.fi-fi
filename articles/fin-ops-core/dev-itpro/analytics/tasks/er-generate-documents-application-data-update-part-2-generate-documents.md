---
title: Suunnittele konfiguraatioita luodaksesi sovellustietoja sisältäviä asiakirjoja
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) määritysten suunnittelua sähköisen asiakirjan luontia varten. (Osa 1 – Konfiguraatioiden tuonti).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 217eca9bd1502d4327857720fb2d32a3ec3508ef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563171"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="40405-104">Suunnittele konfiguraatioita luodaksesi sovellustietoja sisältäviä asiakirjoja</span><span class="sxs-lookup"><span data-stu-id="40405-104">Design configurations to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="40405-105">Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (osa 1: konfiguraatioiden tuominen) -menettely on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="40405-105">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="40405-106">Tämän menettelyn vaiheissa opastetaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan sähköisen asiakirjan luomista varten.</span><span class="sxs-lookup"><span data-stu-id="40405-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="40405-107">Tässä menettelyssä suoritetaan tuotu ER-muotokonfiguraatio, joka on luotu malliyritykselle Litware Inc. sähköisten asiakirjojen luomista varten.</span><span class="sxs-lookup"><span data-stu-id="40405-107">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="40405-108">Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="40405-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="40405-109">Nämä vaiheet voidaan suorittaa DEMF-tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="40405-109">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="40405-110">Ennen kuin aloitat, muuta DEMF-yrityksen maakonteksti DEU (Saksa) -arvosta BEL (Belgia) -arvoksi.</span><span class="sxs-lookup"><span data-stu-id="40405-110">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="40405-111">Valitse Organisaation hallinto > Organisaatiot > Yritykset, kun haluat päivittää yrityksen DEMF ensisijaisen osoitteen maakoodin.</span><span class="sxs-lookup"><span data-stu-id="40405-111">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="40405-112">Käynnistä sovellus uudelleen.</span><span class="sxs-lookup"><span data-stu-id="40405-112">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="40405-113">Tuodun ER-muodon suorittaminen</span><span class="sxs-lookup"><span data-stu-id="40405-113">Run imported ER format</span></span>
1. <span data-ttu-id="40405-114">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="40405-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="40405-115">Laajenna puussa Intrastat (model).</span><span class="sxs-lookup"><span data-stu-id="40405-115">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="40405-116">Valitse puussa Intrastat (model)\Intrastat (format).</span><span class="sxs-lookup"><span data-stu-id="40405-116">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="40405-117">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="40405-117">Click Run.</span></span>
    * <span data-ttu-id="40405-118">Suorita ER-muotokonfiguraation luonnosversio, kun haluat luoda Intrastat-raportin.</span><span class="sxs-lookup"><span data-stu-id="40405-118">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="40405-119">Kirjoita Syötä tiedostonimi -kenttään intrastat.xml.</span><span class="sxs-lookup"><span data-stu-id="40405-119">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="40405-120">Anna tiedoston nimi.</span><span class="sxs-lookup"><span data-stu-id="40405-120">Specify the name of the file.</span></span>  
6. <span data-ttu-id="40405-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="40405-121">Click OK.</span></span>
    * <span data-ttu-id="40405-122">Tarkista luotu XML-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="40405-122">Review the generated XML file.</span></span>  
7. <span data-ttu-id="40405-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="40405-123">Close the page.</span></span>
8. <span data-ttu-id="40405-124">Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="40405-124">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="40405-125">Avaa tämä lomake, kun haluat tarkastella luodun sähköisen asiakirjan Intrastat-tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="40405-125">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="40405-126">Valitse Intrastat-arkisto.</span><span class="sxs-lookup"><span data-stu-id="40405-126">Click Intrastat archive.</span></span>
    * <span data-ttu-id="40405-127">Koska suoritettu ER-muoto ei sisällä sovellustietojen päivityksen asetuksia, valmiin Intrastat-raportin tietoja ei ole arkistoitu.</span><span class="sxs-lookup"><span data-stu-id="40405-127">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="40405-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="40405-128">Close the page.</span></span>
11. <span data-ttu-id="40405-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="40405-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]