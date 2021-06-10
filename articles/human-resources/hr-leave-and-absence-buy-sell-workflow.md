---
title: Loman rahaksi tai lomapalkan vapaaksi vaihtamisen työnkulkujen luominen
description: Luo loman rahaksi tai lomapalkan vapaaksi vaihtamisen työnkulku, jonka avulla voit hallita loman rahaksi tai lomapalkan vapaaksi vaihtamista johdonmukaisesti Dynamics 365 Human Resourcesissa.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5bc31740218e3f171d89debace339dee0177d826
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053968"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="5e1ad-103">Loman rahaksi tai lomapalkan vapaaksi vaihtamisen työnkulkujen luominen</span><span class="sxs-lookup"><span data-stu-id="5e1ad-103">Create a buy and sell leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5e1ad-104">Voit luoda Dynamics 365 Human Resourcesissa työnkulun, jolla voi hallita loman rahaksi tai lomapalkan vapaaksi vaihtamispyyntöjä johdonmukaisesti.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="5e1ad-105">**Loman rahaksi tai lomapalkan vapaaksi vaihtaminen** -työnkulun avulla voi tehdä seuraavat:</span><span class="sxs-lookup"><span data-stu-id="5e1ad-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="5e1ad-106">Määrittää tehtäviä</span><span class="sxs-lookup"><span data-stu-id="5e1ad-106">Define tasks</span></span>
- <span data-ttu-id="5e1ad-107">Määrittää, kenen tehtävät on suoritettava</span><span class="sxs-lookup"><span data-stu-id="5e1ad-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="5e1ad-108">Määrittää, ketkä voivat hyväksyä tai hylätä pyyntöjä</span><span class="sxs-lookup"><span data-stu-id="5e1ad-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="5e1ad-109">Loman rahaksi tai lomapalkan vapaaksi vaihtamisen työnkulkujen luominen</span><span class="sxs-lookup"><span data-stu-id="5e1ad-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="5e1ad-110">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="5e1ad-111">Valitse **Määritys**-kohdasta **Henkilöstöhallinnon työnkulut**.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="5e1ad-112">Valitse **Uusi** ja valitse sitten **Loman rahaksi tai lomapalkan vapaaksi vaihtamispyyntö**.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="5e1ad-113">Kun **Avaa tämä tiedosto?** -sanomaruutu tulee näkyviin, valitse **Avaa** ja kirjaudu sisään yrityksen tunnistetiedoilla.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="5e1ad-114">Työnkulkueditorin avulla voit luoda työnkulun lomapyyntöihin.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="5e1ad-115">Lisätietoja työnkulkujen käyttämisestä on kohdassa [Luo työnkulkujen yhteenveto](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span><span class="sxs-lookup"><span data-stu-id="5e1ad-115">For more information about working with workflows, see [Create workflows overview](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="5e1ad-116">Loma- tai poissaolopyyntötyönkulun tietoelementit</span><span class="sxs-lookup"><span data-stu-id="5e1ad-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="5e1ad-117">Seuraavien tietoelementtien avulla voit luoda ehdollisia tai automaattisia hyväksyntöjä Loman rahaksi tai lomapalkan vapaaksi vaihtamispyyntöjen työnkulkuja:</span><span class="sxs-lookup"><span data-stu-id="5e1ad-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="5e1ad-118">**summa**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-118">**Amount**</span></span>
- <span data-ttu-id="5e1ad-119">**Lomien osto- ja myyntikäytäntö**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="5e1ad-120">**Yritys**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-120">**Company**</span></span>
- <span data-ttu-id="5e1ad-121">**Luonut**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-121">**Created by**</span></span>
- <span data-ttu-id="5e1ad-122">**Luonnin päivämäärä ja aika**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-122">**Created date and time**</span></span>
- <span data-ttu-id="5e1ad-123">**Päättymispäivämäärä**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-123">**End date**</span></span>
- <span data-ttu-id="5e1ad-124">**Lomatyyppi**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-124">**Leave type**</span></span>
- <span data-ttu-id="5e1ad-125">**Muokannut**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-125">**Modified by**</span></span>
- <span data-ttu-id="5e1ad-126">**Muokkauksen päivämäärä ja aika**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-126">**Modified date and time**</span></span>
- <span data-ttu-id="5e1ad-127">**Pyynnön tunnus**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-127">**Request ID**</span></span>
- <span data-ttu-id="5e1ad-128">**Aloituspäivä**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-128">**Start date**</span></span>
- <span data-ttu-id="5e1ad-129">**Tila**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-129">**Status**</span></span> 
- <span data-ttu-id="5e1ad-130">**Lähetyspäivämäärä**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-130">**Submission date**</span></span>
- <span data-ttu-id="5e1ad-131">**Lähettäjä**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-131">**Submitted by**</span></span>
- <span data-ttu-id="5e1ad-132">**Henkilöstöhallinnon lähettämä**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="5e1ad-133">**Esimiehen lähettämä**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="5e1ad-134">**Lähetetty puolesta**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="5e1ad-135">**Työntekijä**</span><span class="sxs-lookup"><span data-stu-id="5e1ad-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="5e1ad-136">Työnkulkuesimerkit</span><span class="sxs-lookup"><span data-stu-id="5e1ad-136">Workflow examples</span></span>

<span data-ttu-id="5e1ad-137">Nämä esimerkit osoittavat, miten voit luoda erityyppisiä työnkulkuehtoja käyttämällä näitä tietoelementtejä:</span><span class="sxs-lookup"><span data-stu-id="5e1ad-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="5e1ad-138">Käytä automaattisia **Henkilöstöhallinnon toimittama**- ja **Esimiehen lähettämä** -toimintoja, jotka hyväksyvät automaattisesti Loman rahaksi tai lomapalkan vapaaksi vaihtamispyynnöt, jotka nämä roolit lähettävät työntekijöiden puolesta.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="5e1ad-139">Lisätietoja automaattisista toiminnoista on kohdassa [Määritä hyväksyntäprosessit työnkulussa](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="5e1ad-139">For more information about automatic actions, see [Configure approval processes in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span></span>

- <span data-ttu-id="5e1ad-140">Käytä **lomatyyppiä** ehtolauseessa tai automaattisessa toiminnossa, kun haluat hallita sitä, miten työnkulkureititykset on pyydetty tietyillä lomatyypeillä.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e1ad-141">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="5e1ad-141">See also</span></span>

[<span data-ttu-id="5e1ad-142">Lomien ja poissaolojen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="5e1ad-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="5e1ad-143">Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi</span><span class="sxs-lookup"><span data-stu-id="5e1ad-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]