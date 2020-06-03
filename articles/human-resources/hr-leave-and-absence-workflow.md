---
title: Luo lomapyyntötyönkulku
description: Luo loma- ja poissaolopyyntöjen työnkulku, jonka avulla voit hallita lomapyyntöjä johdonmukaisesti Dynamics 365 Human Resources -ohjelmassa.
author: andreabichsel
manager: AnnBe
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c985a0cb242fb6696b55a2514bd788ff4269f8ca
ms.sourcegitcommit: def66a9dc7feadd33411248af2545ee4a9e27c4f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/19/2020
ms.locfileid: "3385545"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="9fc88-103">Luo lomapyyntötyönkulku</span><span class="sxs-lookup"><span data-stu-id="9fc88-103">Create a leave request workflow</span></span>

<span data-ttu-id="9fc88-104">Voit luoda loma- ja poissaolopyyntöjen työnkulun, jonka avulla voit hallita lomapyyntöjä johdonmukaisesti Dynamics 365 Human Resources -ohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="9fc88-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="9fc88-105">**Loma ja poissaolo** -työnkulun avulla voit:</span><span class="sxs-lookup"><span data-stu-id="9fc88-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="9fc88-106">Määrittää tehtäviä</span><span class="sxs-lookup"><span data-stu-id="9fc88-106">Define tasks</span></span>
- <span data-ttu-id="9fc88-107">Määrittää, kenen tehtävät on suoritettava</span><span class="sxs-lookup"><span data-stu-id="9fc88-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="9fc88-108">Määrittää, ketkä voivat hyväksyä tai hylätä pyyntöjä</span><span class="sxs-lookup"><span data-stu-id="9fc88-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="9fc88-109">Luoda loma- tai poissaolopyyntötyönkulun</span><span class="sxs-lookup"><span data-stu-id="9fc88-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="9fc88-110">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="9fc88-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="9fc88-111">Valitse **Määritys**-kohdasta **Henkilöstöhallinnon työnkulut**.</span><span class="sxs-lookup"><span data-stu-id="9fc88-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="9fc88-112">Valitse **Uusi** ja valitse sitten **Loma- ja poissaolopyyntö**.</span><span class="sxs-lookup"><span data-stu-id="9fc88-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="9fc88-113">Kun **Avaa tämä tiedosto?** -sanomaruutu tulee näkyviin, valitse **Avaa** ja kirjaudu sisään yrityksen tunnistetiedoilla.</span><span class="sxs-lookup"><span data-stu-id="9fc88-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="9fc88-114">Työnkulkueditorin avulla voit luoda työnkulun lomapyyntöihin.</span><span class="sxs-lookup"><span data-stu-id="9fc88-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="9fc88-115">Lisätietoja työnkulkujen käyttämisestä on kohdassa [Luo työnkulkujen yhteenveto](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="9fc88-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="9fc88-116">Loma- tai poissaolopyyntötyönkulun tietoelementit</span><span class="sxs-lookup"><span data-stu-id="9fc88-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="9fc88-117">Seuraavien tietoelementtien avulla voit luoda ehdollisia tai automaattisia hyväksyntöjä loma- ja poissaolopyyntöjen työnkuluissa:</span><span class="sxs-lookup"><span data-stu-id="9fc88-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="9fc88-118">**summa**</span><span class="sxs-lookup"><span data-stu-id="9fc88-118">**Amount**</span></span>
- <span data-ttu-id="9fc88-119">**Kommentti**</span><span class="sxs-lookup"><span data-stu-id="9fc88-119">**Comment**</span></span>
- <span data-ttu-id="9fc88-120">**Yritys**</span><span class="sxs-lookup"><span data-stu-id="9fc88-120">**Company**</span></span>
- <span data-ttu-id="9fc88-121">**Luonut**</span><span class="sxs-lookup"><span data-stu-id="9fc88-121">**Created by**</span></span>
- <span data-ttu-id="9fc88-122">**Luonnin päivämäärä ja aika**</span><span class="sxs-lookup"><span data-stu-id="9fc88-122">**Created date and time**</span></span>
- <span data-ttu-id="9fc88-123">**Päättymispäivämäärä**</span><span class="sxs-lookup"><span data-stu-id="9fc88-123">**End date**</span></span>
- <span data-ttu-id="9fc88-124">**Lomatyyppi**</span><span class="sxs-lookup"><span data-stu-id="9fc88-124">**Leave type**</span></span>
- <span data-ttu-id="9fc88-125">**Muokkaaja**</span><span class="sxs-lookup"><span data-stu-id="9fc88-125">**Modified by**</span></span>
- <span data-ttu-id="9fc88-126">**Muokkauksen päivämäärä ja aika**</span><span class="sxs-lookup"><span data-stu-id="9fc88-126">**Modified date and time**</span></span>
- <span data-ttu-id="9fc88-127">**Syykoodi**</span><span class="sxs-lookup"><span data-stu-id="9fc88-127">**Reason code**</span></span>
- <span data-ttu-id="9fc88-128">**Pyynnön tunnus**</span><span class="sxs-lookup"><span data-stu-id="9fc88-128">**Request ID**</span></span>
- <span data-ttu-id="9fc88-129">**Aloituspäivämäärä**</span><span class="sxs-lookup"><span data-stu-id="9fc88-129">**Start date**</span></span>
- <span data-ttu-id="9fc88-130">**Tila**</span><span class="sxs-lookup"><span data-stu-id="9fc88-130">**Status**</span></span> 
- <span data-ttu-id="9fc88-131">**Lähetyspäivämäärä**</span><span class="sxs-lookup"><span data-stu-id="9fc88-131">**Submission date**</span></span>
- <span data-ttu-id="9fc88-132">**Lähettäjä**</span><span class="sxs-lookup"><span data-stu-id="9fc88-132">**Submitted by**</span></span>
- <span data-ttu-id="9fc88-133">**Henkilöstöhallinnon lähettämä**</span><span class="sxs-lookup"><span data-stu-id="9fc88-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="9fc88-134">**Esimiehen lähettämä**</span><span class="sxs-lookup"><span data-stu-id="9fc88-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="9fc88-135">**Lähetetty puolesta**</span><span class="sxs-lookup"><span data-stu-id="9fc88-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="9fc88-136">**Työntekijä**</span><span class="sxs-lookup"><span data-stu-id="9fc88-136">**Worker**</span></span>
- <span data-ttu-id="9fc88-137">**Työntekijätyyppi**</span><span class="sxs-lookup"><span data-stu-id="9fc88-137">**Worker type**</span></span>

<span data-ttu-id="9fc88-138">Nämä esimerkit osoittavat, miten voit luoda erityyppisiä työnkulkuehtoja käyttämällä näitä tietoelementtejä:</span><span class="sxs-lookup"><span data-stu-id="9fc88-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="9fc88-139">Voit käyttää ehtolausekkeen **syykoodia** reitittämään sairauslomapyyntöjä, joiden syykoodi on **leikkaus** HR:n hyväksyttäväksi, ja reitittää kaikki muut syykoodit esimiehelle.</span><span class="sxs-lookup"><span data-stu-id="9fc88-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="9fc88-140">Lisätietoja ehdollisesta lausekkeista on kohdassa [ehdollisen päätöksenteon määrittäminen työnkulussa](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span><span class="sxs-lookup"><span data-stu-id="9fc88-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="9fc88-141">Käytä automaattisia **Henkilöstöhallinnon toimittama**- ja **Esimiehen lähettämä** -toimintoja, jotka hyväksyvät automaattisesti lomapyynnöt, jotka nämä roolit lähettävät työntekijöiden puolesta.</span><span class="sxs-lookup"><span data-stu-id="9fc88-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="9fc88-142">Lisätietoja automaattisista toiminnoista on kohdassa [Määritä hyväksyntäprosessit työnkulussa](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="9fc88-142">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="9fc88-143">Käytä **lomatyyppiä** ehtolauseessa tai automaattisessa toiminnossa, kun haluat hallita sitä, miten työnkulkureititykset on pyydetty tietyillä lomatyypeillä.</span><span class="sxs-lookup"><span data-stu-id="9fc88-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="9fc88-144">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="9fc88-144">See also</span></span>

- [<span data-ttu-id="9fc88-145">Lomien ja poissaolojen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="9fc88-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
