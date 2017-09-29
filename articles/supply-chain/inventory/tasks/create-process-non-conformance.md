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
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: e5187c44aac881273900b2fc0ca91045a65cd838
ms.contentlocale: fi-fi
ms.lasthandoff: 09/12/2017

---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="1c330-103">Luo ja käsittele määritysten noudattaminen</span><span class="sxs-lookup"><span data-stu-id="1c330-103">Create and process a conformance</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c330-104">Tällä menettelyllä voi hallita määrityksistä poikkeamisia aiemmin luodun laatutilauksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="1c330-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="1c330-105">Voit toistaa tallenteen USMF-esittely-yrityksessä ja käyttää ehdotettuja arvoja.</span><span class="sxs-lookup"><span data-stu-id="1c330-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="1c330-106">Tämän menettelyn suorittaa yleensä laatuassistentti.</span><span class="sxs-lookup"><span data-stu-id="1c330-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="1c330-107">Edellytyksenä on suorittaa Tarkista tavaroiden laatu -tehtävätallenteen suorittaminen.</span><span class="sxs-lookup"><span data-stu-id="1c330-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="1c330-108">Määrityksistä poikkeamisen hyväksymisen käsittely edellyttää, että tehtävätallenteen suorittajalle on määritetty Nimi-arvo Käyttäjät-sivulla.</span><span class="sxs-lookup"><span data-stu-id="1c330-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="1c330-109">Asiakirjojen huomautusten käyttö taas edellyttää, että tiedoston käsittely on aktivoitu käyttäjäasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="1c330-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="1c330-110">Valitse laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="1c330-110">Select a quality order</span></span>
1. <span data-ttu-id="1c330-111">Valitse Laatutilaukset.</span><span class="sxs-lookup"><span data-stu-id="1c330-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="1c330-112">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="1c330-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1c330-113">Valitse Tarkista tavaroiden laatu -tehtävätallenteessa luotu laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="1c330-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="1c330-114">Luo määrityksistä poikkeaminen</span><span class="sxs-lookup"><span data-stu-id="1c330-114">Create a nonconformance</span></span>
1. <span data-ttu-id="1c330-115">Valitse Kyselyt.</span><span class="sxs-lookup"><span data-stu-id="1c330-115">Click Inquiries.</span></span>
2. <span data-ttu-id="1c330-116">Valitse Määrityksistä poikkeamiset.</span><span class="sxs-lookup"><span data-stu-id="1c330-116">Click Non conformances.</span></span>
3. <span data-ttu-id="1c330-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1c330-117">Click New.</span></span>
4. <span data-ttu-id="1c330-118">Avaa haku napsauttamalla Ongelman tyyppi -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="1c330-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1c330-119">Valitse tarkistuksen aikana löytynyt ongelma.</span><span class="sxs-lookup"><span data-stu-id="1c330-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="1c330-120">Avaa haku napsauttamalla Ongelman tyyppi -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="1c330-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="1c330-121">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="1c330-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="1c330-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1c330-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="1c330-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1c330-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="1c330-124">Hyväksy tai hylkää määrityksistä poikkeaminen</span><span class="sxs-lookup"><span data-stu-id="1c330-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="1c330-125">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="1c330-125">Click Functions.</span></span>
2. <span data-ttu-id="1c330-126">Valitse Hyväksy määrityksistä poikkeaminen.</span><span class="sxs-lookup"><span data-stu-id="1c330-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="1c330-127">Hyväksy tässä esimerkissä määrityksistä poikkeamisen.</span><span class="sxs-lookup"><span data-stu-id="1c330-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="1c330-128">Hyväksytyt määrityksistä poikkeamiset voidaan liittää liittyviin toimintoihin tallentamaan työ, joka tehdään osana määrityksistä poikkeamisen käsittelyä ja, kuten tässä työvaiheessa, korjauskäsittelyn käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="1c330-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="1c330-129">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="1c330-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="1c330-130">Luo korjaustoiminto</span><span class="sxs-lookup"><span data-stu-id="1c330-130">Create a correction action</span></span>
1. <span data-ttu-id="1c330-131">Valitse Korjaukset.</span><span class="sxs-lookup"><span data-stu-id="1c330-131">Click Corrections.</span></span>
2. <span data-ttu-id="1c330-132">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1c330-132">Click New.</span></span>
3. <span data-ttu-id="1c330-133">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="1c330-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="1c330-134">Avaa haku napsauttamalla Henkilöstönumero-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="1c330-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="1c330-135">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1c330-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="1c330-136">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="1c330-136">Click Select.</span></span>
7. <span data-ttu-id="1c330-137">Valitse Liitä.</span><span class="sxs-lookup"><span data-stu-id="1c330-137">Click Attach.</span></span>
    * <span data-ttu-id="1c330-138">Luo korjausta koskeva huomautus.</span><span class="sxs-lookup"><span data-stu-id="1c330-138">Create a note about the correction.</span></span> <span data-ttu-id="1c330-139">Tässä esimerkissä toimintona on yhteydenotto toimittajaan ja keskustelu määrityksistä poikkeamistapauksesta.</span><span class="sxs-lookup"><span data-stu-id="1c330-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="1c330-140">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1c330-140">Click New.</span></span>
9. <span data-ttu-id="1c330-141">Valitse Huomautus.</span><span class="sxs-lookup"><span data-stu-id="1c330-141">Click Note.</span></span>
    * <span data-ttu-id="1c330-142">Huomaa, että raporttiasetusten mukaan eri asiakirjatyyppejä voi tulostaa raportteihin, jotka liittyvät määrityksistä poikkeamisen hallintaan.</span><span class="sxs-lookup"><span data-stu-id="1c330-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="1c330-143">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1c330-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="1c330-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1c330-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="1c330-145">Ylläpidä korjausta</span><span class="sxs-lookup"><span data-stu-id="1c330-145">Maintain a correction</span></span>
1. <span data-ttu-id="1c330-146">Valitse Merkitse valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="1c330-146">Click Mark complete.</span></span>
2. <span data-ttu-id="1c330-147">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1c330-147">Click OK.</span></span>
3. <span data-ttu-id="1c330-148">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1c330-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="1c330-149">Sulje määrityksistä poikkeaminen</span><span class="sxs-lookup"><span data-stu-id="1c330-149">Close a nonconformance</span></span>
1. <span data-ttu-id="1c330-150">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="1c330-150">Click Functions.</span></span>
2. <span data-ttu-id="1c330-151">Valitse Sulje määrityksistä poikkeaminen.</span><span class="sxs-lookup"><span data-stu-id="1c330-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="1c330-152">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="1c330-152">Click Yes.</span></span>
4. <span data-ttu-id="1c330-153">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1c330-153">Close the page.</span></span>
5. <span data-ttu-id="1c330-154">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1c330-154">Close the page.</span></span>

