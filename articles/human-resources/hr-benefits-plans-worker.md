---
title: Työntekijöiden etuussuunnitelmien luominen
description: Voit luoda työntekijöiden etuussuunnitelmia Microsoft Dynamics 365 Human Resourcesissa valitaksesi etuussuunnitelmia työntekijöille ja vahvistaaksesi etuussuunnitelmavalintoja.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: baa131b3bcab73d29c7059f6595f1e8943f8164f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804933"
---
# <a name="create-worker-benefit-plans"></a><span data-ttu-id="242e7-103">Työntekijöiden etuussuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="242e7-103">Create worker benefit plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="242e7-104">Voit luoda työntekijöiden etuussuunnitelmia Microsoft Dynamics 365 Human Resourcesissa valitaksesi etuussuunnitelmia työntekijöille ja vahvistaaksesi etuussuunnitelmavalintoja.</span><span class="sxs-lookup"><span data-stu-id="242e7-104">You can create worker benefit plans in Microsoft Dynamics 365 Human Resources to select benefit plans for employees and to confirm benefit plan selections.</span></span> <span data-ttu-id="242e7-105">Yleensä työntekijät valitsevat etuussuunnitelmat itse työntekijän itsepalvelun avulla, minkä jälkeen etujen järjestelmänvalvoja vahvistaa valinnat.</span><span class="sxs-lookup"><span data-stu-id="242e7-105">Typically, employees select benefit plans themselves by using Employee self service, and then a benefits administrator confirms the selections.</span></span> 

1. <span data-ttu-id="242e7-106">Valitse **Etujen hallinta** -työtilassa **Suunnitelmat**-kohdasta **Työntekijän etuussuunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="242e7-106">In the **Benefits management** workspace, under **Plans**, select **Worker benefit plans**.</span></span>

2. <span data-ttu-id="242e7-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="242e7-107">Select **New**.</span></span>

3. <span data-ttu-id="242e7-108">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="242e7-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="242e7-109">Kenttä</span><span class="sxs-lookup"><span data-stu-id="242e7-109">Field</span></span> | <span data-ttu-id="242e7-110">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="242e7-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="242e7-111">Kausi</span><span class="sxs-lookup"><span data-stu-id="242e7-111">Period</span></span> | <span data-ttu-id="242e7-112">Määrittää etuusjakson Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="242e7-112">Specifies a benefits period to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> <span data-ttu-id="242e7-113">Valitse esimerkiksi luomasi jakso nimeltään 2015 vahvistaaksesi kaikki vuoden 2015 etuusrekisteröintivalinnat.</span><span class="sxs-lookup"><span data-stu-id="242e7-113">For example, select a period you created called 2015 to confirm all the benefit enrollment selections for 2015.</span></span> |
   | <span data-ttu-id="242e7-114">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="242e7-114">Worker</span></span> | <span data-ttu-id="242e7-115">Määrittää työntekijän Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="242e7-115">Specifies a worker to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="242e7-116">Oikeushenkilö</span><span class="sxs-lookup"><span data-stu-id="242e7-116">Legal entity</span></span> | <span data-ttu-id="242e7-117">Määrittää yrityksen Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="242e7-117">Specifies a legal entity to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="242e7-118">Kattavuusvaihtoehto</span><span class="sxs-lookup"><span data-stu-id="242e7-118">Coverage option</span></span> | <span data-ttu-id="242e7-119">Määrittää kattavuusasetuksen Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="242e7-119">Specifies a coverage option to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="242e7-120">Oletus</span><span class="sxs-lookup"><span data-stu-id="242e7-120">Default</span></span> | <span data-ttu-id="242e7-121">Suodattaa etuussuunnitelmat sen perusteella, ovatko ne oletusarvoisia.</span><span class="sxs-lookup"><span data-stu-id="242e7-121">Filters the benefit plans based on whether they are a default plan.</span></span> <span data-ttu-id="242e7-122">Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmaan tietueiden osajoukon sen vahvistamista varten.</span><span class="sxs-lookup"><span data-stu-id="242e7-122">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="242e7-123">Tila</span><span class="sxs-lookup"><span data-stu-id="242e7-123">Status</span></span> | <span data-ttu-id="242e7-124">Suodattaa etuussuunnitelmia niiden tilan perusteella.</span><span class="sxs-lookup"><span data-stu-id="242e7-124">Filters benefit plans based on their status.</span></span> <span data-ttu-id="242e7-125">Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmaan tietueiden osajoukon sen vahvistamista varten.</span><span class="sxs-lookup"><span data-stu-id="242e7-125">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="242e7-126">Vahvistus</span><span class="sxs-lookup"><span data-stu-id="242e7-126">Confirmation</span></span> | <span data-ttu-id="242e7-127">Määrittää vahvistustilan Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="242e7-127">Specifies the confirmation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="242e7-128">Peruutus</span><span class="sxs-lookup"><span data-stu-id="242e7-128">Cancellation</span></span> | <span data-ttu-id="242e7-129">Määrittää peruutustilan Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="242e7-129">Specifies the cancellation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="242e7-130">Voimassaolopäivämäärien suodatin</span><span class="sxs-lookup"><span data-stu-id="242e7-130">Effective date filter</span></span> | <span data-ttu-id="242e7-131">Suodattaa suunnitelmat sen perusteella, ovatko ne vanhentuneita, aktiivisia vai tulevaisuudessa aktivoitavia.</span><span class="sxs-lookup"><span data-stu-id="242e7-131">Filters the plans based on whether they’re expired, active, or will be active in the future.</span></span> <span data-ttu-id="242e7-132">Valitse valintaruudut, jotka vastaavat suunnitelmia, jotka haluat nähdä Suunnitelmat-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="242e7-132">Select the check boxes that correspond to the plans you want to see in the Plans fast tab.</span></span> |
   | <span data-ttu-id="242e7-133">Suunnitelmat</span><span class="sxs-lookup"><span data-stu-id="242e7-133">Plans</span></span> | <span data-ttu-id="242e7-134">Suunnitelmat-pikavälilehti sisältää ne suunnitelmat, jotka täyttävät määrittämäsi suodatusperusteet.</span><span class="sxs-lookup"><span data-stu-id="242e7-134">The Plans fast tab contains the plans that meet the filter criteria you specified.</span></span> <span data-ttu-id="242e7-135">Henkilöstöhallinnon työntekijöiden määrittämät asiaan liittyvät määritysvalinnat ja työntekijöiden valitsemat rekisteröintivaihtoehdot sisällytetään jokaiselle riville.</span><span class="sxs-lookup"><span data-stu-id="242e7-135">The relevant configuration options that were set by HR staff and the enrollment selections that were chosen by employees are included on each line.</span></span> <span data-ttu-id="242e7-136">Kelvollinen-kenttä ilmaisee, onko suunnitelman valinnan kanssa vahvistusristiriitaa.</span><span class="sxs-lookup"><span data-stu-id="242e7-136">The Qualified field specifies whether there is a validation conflict with the plan selection.</span></span> |

4. <span data-ttu-id="242e7-137">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="242e7-137">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]