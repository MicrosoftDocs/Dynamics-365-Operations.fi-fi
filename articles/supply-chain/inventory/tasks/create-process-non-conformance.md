---
title: "Luo ja käsittele määritysten noudattaminen"
description: "Tällä menettelyllä voi hallita määrityksistä poikkeamisia aiemmin luodun laatutilauksen perusteella."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: adecf9b2ea29abaee378f1c02c64551c3aeede6d
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="a50e0-103">Luo ja käsittele määritysten noudattaminen</span><span class="sxs-lookup"><span data-stu-id="a50e0-103">Create and process a conformance</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a50e0-104">Tällä menettelyllä voi hallita määrityksistä poikkeamisia aiemmin luodun laatutilauksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="a50e0-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="a50e0-105">Voit toistaa tallenteen USMF-esittely-yrityksessä ja käyttää ehdotettuja arvoja.</span><span class="sxs-lookup"><span data-stu-id="a50e0-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="a50e0-106">Tämän menettelyn suorittaa yleensä laatuassistentti.</span><span class="sxs-lookup"><span data-stu-id="a50e0-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="a50e0-107">Edellytyksenä on suorittaa Tarkista tavaroiden laatu -tehtävätallenteen suorittaminen.</span><span class="sxs-lookup"><span data-stu-id="a50e0-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="a50e0-108">Määrityksistä poikkeamisen hyväksymisen käsittely edellyttää, että tehtävätallenteen suorittajalle on määritetty Nimi-arvo Käyttäjät-sivulla.</span><span class="sxs-lookup"><span data-stu-id="a50e0-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="a50e0-109">Asiakirjojen huomautusten käyttö taas edellyttää, että tiedoston käsittely on aktivoitu käyttäjäasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="a50e0-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="a50e0-110">Valitse laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="a50e0-110">Select a quality order</span></span>
1. <span data-ttu-id="a50e0-111">Valitse Laatutilaukset.</span><span class="sxs-lookup"><span data-stu-id="a50e0-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="a50e0-112">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a50e0-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a50e0-113">Valitse Tarkista tavaroiden laatu -tehtävätallenteessa luotu laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="a50e0-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="a50e0-114">Luo määrityksistä poikkeaminen</span><span class="sxs-lookup"><span data-stu-id="a50e0-114">Create a nonconformance</span></span>
1. <span data-ttu-id="a50e0-115">Valitse Kyselyt.</span><span class="sxs-lookup"><span data-stu-id="a50e0-115">Click Inquiries.</span></span>
2. <span data-ttu-id="a50e0-116">Valitse Määrityksistä poikkeamiset.</span><span class="sxs-lookup"><span data-stu-id="a50e0-116">Click Non conformances.</span></span>
3. <span data-ttu-id="a50e0-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a50e0-117">Click New.</span></span>
4. <span data-ttu-id="a50e0-118">Avaa haku napsauttamalla Ongelman tyyppi -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="a50e0-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a50e0-119">Valitse tarkistuksen aikana löytynyt ongelma.</span><span class="sxs-lookup"><span data-stu-id="a50e0-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="a50e0-120">Avaa haku napsauttamalla Ongelman tyyppi -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="a50e0-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a50e0-121">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a50e0-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="a50e0-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a50e0-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a50e0-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a50e0-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="a50e0-124">Hyväksy tai hylkää määrityksistä poikkeaminen</span><span class="sxs-lookup"><span data-stu-id="a50e0-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="a50e0-125">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="a50e0-125">Click Functions.</span></span>
2. <span data-ttu-id="a50e0-126">Valitse Hyväksy määrityksistä poikkeaminen.</span><span class="sxs-lookup"><span data-stu-id="a50e0-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="a50e0-127">Hyväksy tässä esimerkissä määrityksistä poikkeamisen.</span><span class="sxs-lookup"><span data-stu-id="a50e0-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="a50e0-128">Hyväksytyt määrityksistä poikkeamiset voidaan liittää liittyviin toimintoihin tallentamaan työ, joka tehdään osana määrityksistä poikkeamisen käsittelyä ja, kuten tässä työvaiheessa, korjauskäsittelyn käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="a50e0-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="a50e0-129">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="a50e0-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="a50e0-130">Luo korjaustoiminto</span><span class="sxs-lookup"><span data-stu-id="a50e0-130">Create a correction action</span></span>
1. <span data-ttu-id="a50e0-131">Valitse Korjaukset.</span><span class="sxs-lookup"><span data-stu-id="a50e0-131">Click Corrections.</span></span>
2. <span data-ttu-id="a50e0-132">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a50e0-132">Click New.</span></span>
3. <span data-ttu-id="a50e0-133">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a50e0-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a50e0-134">Avaa haku napsauttamalla Henkilöstönumero-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="a50e0-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a50e0-135">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a50e0-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a50e0-136">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="a50e0-136">Click Select.</span></span>
7. <span data-ttu-id="a50e0-137">Valitse Liitä.</span><span class="sxs-lookup"><span data-stu-id="a50e0-137">Click Attach.</span></span>
    * <span data-ttu-id="a50e0-138">Luo korjausta koskeva huomautus.</span><span class="sxs-lookup"><span data-stu-id="a50e0-138">Create a note about the correction.</span></span> <span data-ttu-id="a50e0-139">Tässä esimerkissä toimintona on yhteydenotto toimittajaan ja keskustelu määrityksistä poikkeamistapauksesta.</span><span class="sxs-lookup"><span data-stu-id="a50e0-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="a50e0-140">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a50e0-140">Click New.</span></span>
9. <span data-ttu-id="a50e0-141">Valitse Huomautus.</span><span class="sxs-lookup"><span data-stu-id="a50e0-141">Click Note.</span></span>
    * <span data-ttu-id="a50e0-142">Huomaa, että raporttiasetusten mukaan eri asiakirjatyyppejä voi tulostaa raportteihin, jotka liittyvät määrityksistä poikkeamisen hallintaan.</span><span class="sxs-lookup"><span data-stu-id="a50e0-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="a50e0-143">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a50e0-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="a50e0-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a50e0-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="a50e0-145">Ylläpidä korjausta</span><span class="sxs-lookup"><span data-stu-id="a50e0-145">Maintain a correction</span></span>
1. <span data-ttu-id="a50e0-146">Valitse Merkitse valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="a50e0-146">Click Mark complete.</span></span>
2. <span data-ttu-id="a50e0-147">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a50e0-147">Click OK.</span></span>
3. <span data-ttu-id="a50e0-148">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a50e0-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="a50e0-149">Sulje määrityksistä poikkeaminen</span><span class="sxs-lookup"><span data-stu-id="a50e0-149">Close a nonconformance</span></span>
1. <span data-ttu-id="a50e0-150">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="a50e0-150">Click Functions.</span></span>
2. <span data-ttu-id="a50e0-151">Valitse Sulje määrityksistä poikkeaminen.</span><span class="sxs-lookup"><span data-stu-id="a50e0-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="a50e0-152">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="a50e0-152">Click Yes.</span></span>
4. <span data-ttu-id="a50e0-153">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a50e0-153">Close the page.</span></span>
5. <span data-ttu-id="a50e0-154">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a50e0-154">Close the page.</span></span>

