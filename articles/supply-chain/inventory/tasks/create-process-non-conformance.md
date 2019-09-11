---
title: Luo ja käsittele määritysten noudattaminen
description: Tässä aiheessa kerrotaan, miten voit hallita määrityksistä poikkeamisia aiemmin luodun laatutilauksen perusteella.
author: perlynne
manager: AnnBe
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e9cf42f80ef7a4c9c5f68a308386db5835c8f2e
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916642"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="f075d-103">Luo ja käsittele määritysten noudattaminen</span><span class="sxs-lookup"><span data-stu-id="f075d-103">Create and process a conformance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f075d-104">Tässä aiheessa kerrotaan, miten voit hallita määrityksistä poikkeamisia aiemmin luodun laatutilauksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="f075d-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="f075d-105">Voit toistaa tallenteen USMF-esittely-yrityksessä ja käyttää ehdotettuja arvoja.</span><span class="sxs-lookup"><span data-stu-id="f075d-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="f075d-106">Tämän menettelyn suorittaa yleensä laatuassistentti.</span><span class="sxs-lookup"><span data-stu-id="f075d-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="f075d-107">Edellytyksenä on suorittaa [Tarkista tavaroiden laatu](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) -ohjeet.</span><span class="sxs-lookup"><span data-stu-id="f075d-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="f075d-108">Määrityksistä poikkeamisen hyväksymisen käsittely edellyttää, että tehtävätallenteen suorittajalle on määritetty Nimi-arvo Käyttäjät-sivulla.</span><span class="sxs-lookup"><span data-stu-id="f075d-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="f075d-109">Asiakirjojen huomautusten käyttö taas edellyttää, että tiedoston käsittely on aktivoitu käyttäjäasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="f075d-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="f075d-110">Valitse laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="f075d-110">Select a quality order</span></span>
1. <span data-ttu-id="f075d-111">Valitse siirtymisruudussa **Moduulit > Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > Laadunhallinta > Laatutilaukset**.</span><span class="sxs-lookup"><span data-stu-id="f075d-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="f075d-112">Valitse [Tarkista tavaroiden laatu](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) -ohjeessa luotu laatutilaus listasta.</span><span class="sxs-lookup"><span data-stu-id="f075d-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="f075d-113">Luo määrityksistä poikkeaminen</span><span class="sxs-lookup"><span data-stu-id="f075d-113">Create a nonconformance</span></span>
1. <span data-ttu-id="f075d-114">Valitse toimintoruudussa **Kyselyt**.</span><span class="sxs-lookup"><span data-stu-id="f075d-114">In the action pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="f075d-115">Valitse **Määrityksistä poikkeamiset**.</span><span class="sxs-lookup"><span data-stu-id="f075d-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="f075d-116">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f075d-116">Select **New**.</span></span>
4. <span data-ttu-id="f075d-117">Valitse **Ongelman tyyppi** -kentän avattavasta valikosta ongelma, joka löydettiin tarkastusprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="f075d-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="f075d-118">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f075d-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="f075d-119">Hyväksy tai hylkää määrityksistä poikkeaminen</span><span class="sxs-lookup"><span data-stu-id="f075d-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="f075d-120">Valitse **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="f075d-120">Select **Functions**.</span></span>
2. <span data-ttu-id="f075d-121">Valitse **Hyväksy määrityksistä poikkeaminen**.</span><span class="sxs-lookup"><span data-stu-id="f075d-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="f075d-122">Hyväksy tässä esimerkissä määrityksistä poikkeamisen.</span><span class="sxs-lookup"><span data-stu-id="f075d-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="f075d-123">Hyväksytyt määrityksistä poikkeamiset voidaan liittää liittyviin toimintoihin tallentamaan työ, joka tehdään osana määrityksistä poikkeamisen käsittelyä ja, kuten tässä ohjeaiheessa, korjauskäsittelyn käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="f075d-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="f075d-124">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f075d-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="f075d-125">Luo korjaustoiminto</span><span class="sxs-lookup"><span data-stu-id="f075d-125">Create a correction action</span></span>
1. <span data-ttu-id="f075d-126">Valitse **Korjaukset**.</span><span class="sxs-lookup"><span data-stu-id="f075d-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="f075d-127">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f075d-127">Select **New**.</span></span>
3. <span data-ttu-id="f075d-128">Valitse uuden rivin **Henkilöstönumero**-kentästä haluamasi tietue avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="f075d-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="f075d-129">Klikkaa **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="f075d-129">Click **Select**.</span></span>
5. <span data-ttu-id="f075d-130">Valitse **Liitä**.</span><span class="sxs-lookup"><span data-stu-id="f075d-130">Select **Attach**.</span></span> <span data-ttu-id="f075d-131">Luo korjausta koskeva huomautus.</span><span class="sxs-lookup"><span data-stu-id="f075d-131">Create a note about the correction.</span></span> <span data-ttu-id="f075d-132">Tässä esimerkissä toimintona on yhteydenotto toimittajaan ja keskustelu määrityksistä poikkeamistapauksesta.</span><span class="sxs-lookup"><span data-stu-id="f075d-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="f075d-133">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f075d-133">Select **New**.</span></span>
7. <span data-ttu-id="f075d-134">Valitse **Muistiinpano**.</span><span class="sxs-lookup"><span data-stu-id="f075d-134">Select **Note**.</span></span> <span data-ttu-id="f075d-135">Raporttiasetusten mukaan eri asiakirjatyyppejä voi tulostaa raportteihin, jotka liittyvät määrityksistä poikkeamisen hallintaan.</span><span class="sxs-lookup"><span data-stu-id="f075d-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="f075d-136">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f075d-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="f075d-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f075d-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="f075d-138">Ylläpidä korjausta</span><span class="sxs-lookup"><span data-stu-id="f075d-138">Maintain a correction</span></span>
1. <span data-ttu-id="f075d-139">Valitse **Merkitse valmiiksi**.</span><span class="sxs-lookup"><span data-stu-id="f075d-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="f075d-140">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f075d-140">Select **OK**.</span></span>
3. <span data-ttu-id="f075d-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f075d-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="f075d-142">Sulje määrityksistä poikkeaminen</span><span class="sxs-lookup"><span data-stu-id="f075d-142">Close a nonconformance</span></span>
1. <span data-ttu-id="f075d-143">Valitse **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="f075d-143">Select **Functions**.</span></span>
2. <span data-ttu-id="f075d-144">Valitse **Sulje määrityksistä poikkeaminen**.</span><span class="sxs-lookup"><span data-stu-id="f075d-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="f075d-145">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f075d-145">Select **Yes**.</span></span>
4. <span data-ttu-id="f075d-146">Sulje sivut.</span><span class="sxs-lookup"><span data-stu-id="f075d-146">Close the pages.</span></span>
