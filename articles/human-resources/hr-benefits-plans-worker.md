---
title: Työntekijöiden etuussuunnitelmien luominen
description: Voit luoda työntekijöiden etuussuunnitelmia Microsoft Dynamics 365 Human Resourcesissa valitaksesi etuussuunnitelmia työntekijöille ja vahvistaaksesi etuussuunnitelmavalintoja.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitPlanEmployee
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 65b0ce2200a3c63a00ccd73fb26c79556aec55ad
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008896"
---
# <a name="create-worker-benefit-plans"></a><span data-ttu-id="bbf19-103">Työntekijöiden etuussuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="bbf19-103">Create worker benefit plans</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="bbf19-104">Voit luoda työntekijöiden etuussuunnitelmia Microsoft Dynamics 365 Human Resourcesissa valitaksesi etuussuunnitelmia työntekijöille ja vahvistaaksesi etuussuunnitelmavalintoja.</span><span class="sxs-lookup"><span data-stu-id="bbf19-104">You can create worker benefit plans in Microsoft Dynamics 365 Human Resources to select benefit plans for employees and to confirm benefit plan selections.</span></span> <span data-ttu-id="bbf19-105">Yleensä työntekijät valitsevat etuussuunnitelmat itse työntekijän itsepalvelun avulla, minkä jälkeen etujen järjestelmänvalvoja vahvistaa valinnat.</span><span class="sxs-lookup"><span data-stu-id="bbf19-105">Typically, employees select benefit plans themselves by using Employee self service, and then a benefits administrator confirms the selections.</span></span> 

1. <span data-ttu-id="bbf19-106">Valitse **Etujen hallinta** -työtilassa **Suunnitelmat**-kohdasta **Työntekijän etuussuunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="bbf19-106">In the **Benefits management** workspace, under **Plans**, select **Worker benefit plans**.</span></span>

2. <span data-ttu-id="bbf19-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="bbf19-107">Select **New**.</span></span>

3. <span data-ttu-id="bbf19-108">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="bbf19-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="bbf19-109">Kenttä</span><span class="sxs-lookup"><span data-stu-id="bbf19-109">Field</span></span> | <span data-ttu-id="bbf19-110">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="bbf19-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bbf19-111">Kausi</span><span class="sxs-lookup"><span data-stu-id="bbf19-111">Period</span></span> | <span data-ttu-id="bbf19-112">Määrittää etuusjakson Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="bbf19-112">Specifies a benefits period to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> <span data-ttu-id="bbf19-113">Valitse esimerkiksi luomasi jakso nimeltään 2015 vahvistaaksesi kaikki vuoden 2015 etuusrekisteröintivalinnat.</span><span class="sxs-lookup"><span data-stu-id="bbf19-113">For example, select a period you created called 2015 to confirm all the benefit enrollment selections for 2015.</span></span> |
   | <span data-ttu-id="bbf19-114">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="bbf19-114">Worker</span></span> | <span data-ttu-id="bbf19-115">Määrittää työntekijän Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="bbf19-115">Specifies a worker to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="bbf19-116">Oikeushenkilö</span><span class="sxs-lookup"><span data-stu-id="bbf19-116">Legal entity</span></span> | <span data-ttu-id="bbf19-117">Määrittää yrityksen Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="bbf19-117">Specifies a legal entity to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="bbf19-118">Kattavuusvaihtoehto</span><span class="sxs-lookup"><span data-stu-id="bbf19-118">Coverage option</span></span> | <span data-ttu-id="bbf19-119">Määrittää kattavuusasetuksen Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="bbf19-119">Specifies a coverage option to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="bbf19-120">Oletus</span><span class="sxs-lookup"><span data-stu-id="bbf19-120">Default</span></span> | <span data-ttu-id="bbf19-121">Suodattaa etuussuunnitelmat sen perusteella, ovatko ne oletusarvoisia.</span><span class="sxs-lookup"><span data-stu-id="bbf19-121">Filters the benefit plans based on whether they are a default plan.</span></span> <span data-ttu-id="bbf19-122">Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmaan tietueiden osajoukon sen vahvistamista varten.</span><span class="sxs-lookup"><span data-stu-id="bbf19-122">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="bbf19-123">Tila</span><span class="sxs-lookup"><span data-stu-id="bbf19-123">Status</span></span> | <span data-ttu-id="bbf19-124">Suodattaa etuussuunnitelmia niiden tilan perusteella.</span><span class="sxs-lookup"><span data-stu-id="bbf19-124">Filters benefit plans based on their status.</span></span> <span data-ttu-id="bbf19-125">Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmaan tietueiden osajoukon sen vahvistamista varten.</span><span class="sxs-lookup"><span data-stu-id="bbf19-125">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="bbf19-126">Vahvistus</span><span class="sxs-lookup"><span data-stu-id="bbf19-126">Confirmation</span></span> | <span data-ttu-id="bbf19-127">Määrittää vahvistustilan Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="bbf19-127">Specifies the confirmation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="bbf19-128">Peruutus</span><span class="sxs-lookup"><span data-stu-id="bbf19-128">Cancellation</span></span> | <span data-ttu-id="bbf19-129">Määrittää peruutustilan Suunnitelmat-pikavälilehden suunnitelmien suodattamista varten. Suodata suunnitelmia, jotta voit helpommin valita kaikkien suunnitelmatietueiden osajoukon ja siten vahvistaa osajoukon.</span><span class="sxs-lookup"><span data-stu-id="bbf19-129">Specifies the cancellation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="bbf19-130">Voimassaolopäivämäärien suodatin</span><span class="sxs-lookup"><span data-stu-id="bbf19-130">Effective date filter</span></span> | <span data-ttu-id="bbf19-131">Suodattaa suunnitelmat sen perusteella, ovatko ne vanhentuneita, aktiivisia vai tulevaisuudessa aktivoitavia.</span><span class="sxs-lookup"><span data-stu-id="bbf19-131">Filters the plans based on whether they’re expired, active, or will be active in the future.</span></span> <span data-ttu-id="bbf19-132">Valitse valintaruudut, jotka vastaavat suunnitelmia, jotka haluat nähdä Suunnitelmat-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="bbf19-132">Select the check boxes that correspond to the plans you want to see in the Plans fast tab.</span></span> |
   | <span data-ttu-id="bbf19-133">Suunnitelmat</span><span class="sxs-lookup"><span data-stu-id="bbf19-133">Plans</span></span> | <span data-ttu-id="bbf19-134">Suunnitelmat-pikavälilehti sisältää ne suunnitelmat, jotka täyttävät määrittämäsi suodatusperusteet.</span><span class="sxs-lookup"><span data-stu-id="bbf19-134">The Plans fast tab contains the plans that meet the filter criteria you specified.</span></span> <span data-ttu-id="bbf19-135">Henkilöstöhallinnon työntekijöiden määrittämät asiaan liittyvät määritysvalinnat ja työntekijöiden valitsemat rekisteröintivaihtoehdot sisällytetään jokaiselle riville.</span><span class="sxs-lookup"><span data-stu-id="bbf19-135">The relevant configuration options that were set by HR staff and the enrollment selections that were chosen by employees are included on each line.</span></span> <span data-ttu-id="bbf19-136">Kelvollinen-kenttä ilmaisee, onko suunnitelman valinnan kanssa vahvistusristiriitaa.</span><span class="sxs-lookup"><span data-stu-id="bbf19-136">The Qualified field specifies whether there is a validation conflict with the plan selection.</span></span> |

4. <span data-ttu-id="bbf19-137">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="bbf19-137">Select **Save**.</span></span>
