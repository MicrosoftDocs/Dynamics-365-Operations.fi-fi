---
title: Työntekijöiden etuussuunnitelmien luominen
description: Voit luoda työntekijöiden etuussuunnitelmia Microsoft Dynamics 365 Human Resourcesissa valitaksesi etuussuunnitelmia työntekijöille ja vahvistaaksesi etuussuunnitelmavalintoja.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitPlanEmployee, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5ac357bbef4bf84b9eaf153834bc7a609240c45e
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464223"
---
# <a name="create-worker-benefit-plans"></a><span data-ttu-id="24443-103">Työntekijöiden etuussuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="24443-103">Create worker benefit plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="24443-104">Voit luoda työntekijöiden etuussuunnitelmia Microsoft Dynamics 365 Human Resourcesissa valitaksesi etuussuunnitelmia työntekijöille ja vahvistaaksesi etuussuunnitelmavalintoja.</span><span class="sxs-lookup"><span data-stu-id="24443-104">You can create worker benefit plans in Microsoft Dynamics 365 Human Resources to select benefit plans for employees and to confirm benefit plan selections.</span></span> <span data-ttu-id="24443-105">Yleensä työntekijät valitsevat etuussuunnitelmat itse työntekijän itsepalvelun avulla, minkä jälkeen etujen järjestelmänvalvoja vahvistaa valinnat.</span><span class="sxs-lookup"><span data-stu-id="24443-105">Typically, employees select benefit plans themselves by using Employee self service, and then a benefits administrator confirms the selections.</span></span> 

1. <span data-ttu-id="24443-106">Valitse **Etujen hallinta** -työtilassa **Suunnitelmat**-kohdasta **Työntekijän etuussuunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="24443-106">In the **Benefits management** workspace, under **Plans**, select **Worker benefit plans**.</span></span>

2. <span data-ttu-id="24443-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="24443-107">Select **New**.</span></span>

3. <span data-ttu-id="24443-108">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="24443-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="24443-109">Kenttä</span><span class="sxs-lookup"><span data-stu-id="24443-109">Field</span></span> | <span data-ttu-id="24443-110">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="24443-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="24443-111">Kausi</span><span class="sxs-lookup"><span data-stu-id="24443-111">Period</span></span> | <span data-ttu-id="24443-112">Määrittää etuusjakson Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="24443-112">Specifies a benefits period to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> <span data-ttu-id="24443-113">Valitse esimerkiksi luomasi jakso nimeltään 2015 vahvistaaksesi kaikki vuoden 2015 etuusrekisteröintivalinnat.</span><span class="sxs-lookup"><span data-stu-id="24443-113">For example, select a period you created called 2015 to confirm all the benefit enrollment selections for 2015.</span></span> |
   | <span data-ttu-id="24443-114">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="24443-114">Worker</span></span> | <span data-ttu-id="24443-115">Määrittää työntekijän Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="24443-115">Specifies a worker to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="24443-116">Oikeushenkilö</span><span class="sxs-lookup"><span data-stu-id="24443-116">Legal entity</span></span> | <span data-ttu-id="24443-117">Määrittää yrityksen Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="24443-117">Specifies a legal entity to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="24443-118">Kattavuusvaihtoehto</span><span class="sxs-lookup"><span data-stu-id="24443-118">Coverage option</span></span> | <span data-ttu-id="24443-119">Määrittää kattavuusasetuksen Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="24443-119">Specifies a coverage option to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="24443-120">Oletus</span><span class="sxs-lookup"><span data-stu-id="24443-120">Default</span></span> | <span data-ttu-id="24443-121">Suodattaa etuussuunnitelmat sen perusteella, ovatko ne oletusarvoisia.</span><span class="sxs-lookup"><span data-stu-id="24443-121">Filters the benefit plans based on whether they are a default plan.</span></span> <span data-ttu-id="24443-122">Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmaan tietueiden osajoukon sen vahvistamista varten.</span><span class="sxs-lookup"><span data-stu-id="24443-122">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="24443-123">Tila</span><span class="sxs-lookup"><span data-stu-id="24443-123">Status</span></span> | <span data-ttu-id="24443-124">Suodattaa etuussuunnitelmia niiden tilan perusteella.</span><span class="sxs-lookup"><span data-stu-id="24443-124">Filters benefit plans based on their status.</span></span> <span data-ttu-id="24443-125">Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmaan tietueiden osajoukon sen vahvistamista varten.</span><span class="sxs-lookup"><span data-stu-id="24443-125">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="24443-126">Vahvistus</span><span class="sxs-lookup"><span data-stu-id="24443-126">Confirmation</span></span> | <span data-ttu-id="24443-127">Määrittää vahvistustilan Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="24443-127">Specifies the confirmation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="24443-128">Peruutus</span><span class="sxs-lookup"><span data-stu-id="24443-128">Cancellation</span></span> | <span data-ttu-id="24443-129">Määrittää peruutustilan Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="24443-129">Specifies the cancellation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="24443-130">Voimassaolopäivämäärien suodatin</span><span class="sxs-lookup"><span data-stu-id="24443-130">Effective date filter</span></span> | <span data-ttu-id="24443-131">Suodattaa suunnitelmat sen perusteella, ovatko ne vanhentuneita, aktiivisia vai tulevaisuudessa aktivoitavia.</span><span class="sxs-lookup"><span data-stu-id="24443-131">Filters the plans based on whether they’re expired, active, or will be active in the future.</span></span> <span data-ttu-id="24443-132">Valitse valintaruudut, jotka vastaavat suunnitelmia, jotka haluat nähdä Suunnitelmat-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="24443-132">Select the check boxes that correspond to the plans you want to see in the Plans fast tab.</span></span> |
   | <span data-ttu-id="24443-133">Suunnitelmat</span><span class="sxs-lookup"><span data-stu-id="24443-133">Plans</span></span> | <span data-ttu-id="24443-134">Suunnitelmat-pikavälilehti sisältää ne suunnitelmat, jotka täyttävät määrittämäsi suodatusperusteet.</span><span class="sxs-lookup"><span data-stu-id="24443-134">The Plans fast tab contains the plans that meet the filter criteria you specified.</span></span> <span data-ttu-id="24443-135">Henkilöstöhallinnon työntekijöiden määrittämät asiaan liittyvät määritysvalinnat ja työntekijöiden valitsemat rekisteröintivaihtoehdot sisällytetään jokaiselle riville.</span><span class="sxs-lookup"><span data-stu-id="24443-135">The relevant configuration options that were set by HR staff and the enrollment selections that were chosen by employees are included on each line.</span></span> <span data-ttu-id="24443-136">Kelvollinen-kenttä ilmaisee, onko suunnitelman valinnan kanssa vahvistusristiriitaa.</span><span class="sxs-lookup"><span data-stu-id="24443-136">The Qualified field specifies whether there is a validation conflict with the plan selection.</span></span> |

4. <span data-ttu-id="24443-137">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="24443-137">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]