---
title: "Etuohjelman määrittäminen ja hallinta"
description: "Henkilöstöhallinto sisältää joukon työkaluja, joiden avulla organisaation tarjoamia tai työntekijöitä varten käsittelemiä etuja, vähennyksiä ja työntekijöiden kompensaatiosuunnitelmia voi määrittää ja ylläpitää. Tässä artikkelissa on tietoja etujen määrittämisestä ja hallinnasta."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fc325b519299098a4f8257c013bce0842237f9ea
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="define-and-manage-a-benefits-program"></a><span data-ttu-id="fc5ca-104">Etuohjelman määrittäminen ja hallinta</span><span class="sxs-lookup"><span data-stu-id="fc5ca-104">Define and manage a benefits program</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fc5ca-105">Henkilöstöhallinto sisältää joukon työkaluja, joiden avulla organisaation tarjoamia tai työntekijöitä varten käsittelemiä etuja, vähennyksiä ja työntekijöiden kompensaatiosuunnitelmia voi määrittää ja ylläpitää.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-105">Human resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers.</span></span> <span data-ttu-id="fc5ca-106">Tässä artikkelissa on tietoja etujen määrittämisestä ja hallinnasta.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-106">This topic provides information about how to set up and manage benefits.</span></span>

<a name="benefit-setup"></a><span data-ttu-id="fc5ca-107">Etujen asetukset</span><span class="sxs-lookup"><span data-stu-id="fc5ca-107">Benefit setup</span></span>
-------------

<span data-ttu-id="fc5ca-108">Työntekijät voidaan rekisteröidä etuihin sen jälkeen, kun kunkin edun elementit on luotu.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-108">Before workers can be enrolled in benefits, you must create the elements of each benefit.</span></span> <span data-ttu-id="fc5ca-109">Nämä elementit yhdistävät samanlaiset etusuunnitelmat ja määrittävät oletusasetukset, kuten vähennysten määrät ja kirjanpitotiedot.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-109">These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details.</span></span> <span data-ttu-id="fc5ca-110">Useita asetuksia voidaan muokata myöhemmin, kun työntekijät rekisteröidään etuun.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-110">Many of these settings can be adjusted when workers are later enrolled in the benefit.</span></span> <span data-ttu-id="fc5ca-111">Organisaation etusuunnitelmassa voi olla useita rekisteröitymisasetuksia tai työntekijä voi peruuttaa suunnitelmaan rekisteröitymisen.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-111">For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan.</span></span> 

<span data-ttu-id="fc5ca-112">[![Etuprosessin työnkulku](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="fc5ca-112">[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span></span>

## <a name="benefit-elements"></a><span data-ttu-id="fc5ca-113">Edun elementit</span><span class="sxs-lookup"><span data-stu-id="fc5ca-113">Benefit elements</span></span>
<span data-ttu-id="fc5ca-114">Ennen etujen luomista ja työntekijöiden rekisteröimistä niihin määritetään edun muodostavat elementit, joita ovat tyyppi, suunnitelma ja asetukset.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-114">Before you begin to create to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.</span></span>

-   <span data-ttu-id="fc5ca-115">**Tyyppi** – kokoelma tietynlaisia etuussuunnitelmia, kuten työterveys tai pysäköinti.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-115">**Type** – A collection of plans for a specific benefit, such as medical or parking.</span></span>
-   <span data-ttu-id="fc5ca-116">**Suunnitelma** – tietty etuus, jonka tarjoamisesta on tehty sopimus palveluntarjoajan kanssa.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-116">**Plan** – A specific benefit that is contracted from a provider.</span></span>
-   <span data-ttu-id="fc5ca-117">**Asetus** – kattavuustaso, kuten vain työntekijöille tarkoitettu tai työntekijä ja puoliso/kumppani.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-117">**Option** – The coverage level, such as employee only, or employee and spouse/partner.</span></span>

<span data-ttu-id="fc5ca-118">Organisaatio voi tarjota työntekijöille jokaista etutyyppiä, kuten näöntarkistusta tai hammashuoltoa, varten yhden tai useita suunnitelmia.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-118">For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers.</span></span> <span data-ttu-id="fc5ca-119">Organisaatio voi tarjota kutakin suunnitelmaa varten useita asetuksia.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-119">For each plan, the organization can offer different options.</span></span> <span data-ttu-id="fc5ca-120">Työntekijät voivat ostaa esimerkiksi henkivakuutuksen lisävakuutusturvan, joka on vuosipalkan suuruinen tai kaksi tai kolme kertaan sen suuruinen.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-120">For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary.</span></span> <span data-ttu-id="fc5ca-121">Jokaisesta suunnitelman ja asetusten yhdistelmästä muodostuu etu, johon työntekijät voivat rekisteröityä.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-121">Each combination of a plan and options becomes a benefit that workers can enroll in.</span></span> 

<span data-ttu-id="fc5ca-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span><span class="sxs-lookup"><span data-stu-id="fc5ca-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span></span>

## <a name="eligibility"></a><span data-ttu-id="fc5ca-123">Oikeutus</span><span class="sxs-lookup"><span data-stu-id="fc5ca-123">Eligibility</span></span>
<span data-ttu-id="fc5ca-124">Useat tekijät määrittävät työntekijän kelpoisuuden työnantajan tarjoamiin erilaisiin etutyyppeihin.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-124">Many factors determine worker eligibility for the various types of benefits that an employer offers.</span></span> <span data-ttu-id="fc5ca-125">Kun etu luodaan Microsoft Talentissa, etuun liittyvän kelpoisuuden tyyppi voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-125">When you create a benefit in Microsoft Talent, you can set the type of eligibility that applies to that benefit.</span></span> 

<span data-ttu-id="fc5ca-126">Voit tehdä edun käytettäväksi kaikille työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-126">You can make a benefit available to all workers.</span></span> <span data-ttu-id="fc5ca-127">Jotkin yritykset tarjoavat esimerkiksi pysäköintilippuja luontaisetuna kaikille työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-127">For example, some companies offer parking passes to all employees as a fringe benefit.</span></span> <span data-ttu-id="fc5ca-128">Kun tämä etu luodaan, määritä kelpoisuuden arvoksi **Kaikki työntekijät ovat oikeutettuja**.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-128">When you create this benefit, you set the eligibility to **All workers are eligible**.</span></span> 

<span data-ttu-id="fc5ca-129">Muissa eduissa, kuten, palkanpidätyksissä ja veroissa, kelpoisuus ei ole voimassa.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-129">For other benefits, such as garnishments and tax levies, eligibility doesn't apply.</span></span> <span data-ttu-id="fc5ca-130">Kun luot tämän tyyppisiä etuja, kelpoisuuden arvoksi määritetään **Kaikki työntekijät ovat oikeutettuja**.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-130">Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**.</span></span> 

<span data-ttu-id="fc5ca-131">Etukelpoisuus voi perustua sääntöön.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-131">Finally, benefit eligibility can be rule-based.</span></span> <span data-ttu-id="fc5ca-132">Esimerkissä yritys tarjoaa työntekijöille kahta erityyppistä henkivakuutusetua.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-132">For example, a company offers two types of life insurance benefit to employees.</span></span> <span data-ttu-id="fc5ca-133">Johtotason työntekijät ovat oikeutettuja eri henkivakuutussuunnitelmaan kuin kokoaikaiset työntekijät.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-133">Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan.</span></span> <span data-ttu-id="fc5ca-134">Talentissa voidaan luoda etukelpoisuuden sääntö, jonka avulla etsitään johtotason työntekijät, ja toinen sääntö, jonka avulla etsitään kokoaikaiset työntekijät. Tämän jälkeen säännöt kohdistetaan soveltuvaan etuun.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-134">In Talent, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.</span></span>

## <a name="enrollment"></a><span data-ttu-id="fc5ca-135">Rekisteröityminen</span><span class="sxs-lookup"><span data-stu-id="fc5ca-135">Enrollment</span></span>
<span data-ttu-id="fc5ca-136">Kun organisaation tarjoamat edut on luotu ja kelpoisuus määritetty, voit rekisteröidä työntekijät etuihin.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-136">After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits.</span></span> <span data-ttu-id="fc5ca-137">Yhden prosessin aikana etuihin voi rekisteröidä yhden työntekijän tai useita työntekijäitä yhteen tai useaan etuun.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-137">You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process.</span></span> 

<span data-ttu-id="fc5ca-138">Joskus organisaatio lopettaa tietyn edun tarjoamisen.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-138">Sometimes, an organization stops offering certain benefits.</span></span> <span data-ttu-id="fc5ca-139">Tällöin etu ja siihen rekisteröidyt työntekijät on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-139">In this case, you must update the benefit and the workers who are enrolled in.</span></span> <span data-ttu-id="fc5ca-140">Etujen joukkopäättämisen avulla voit muuttaa samalla sekä edun että työntekijän rekisteröimisten päättymispäivää.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-140">Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time.</span></span> <span data-ttu-id="fc5ca-141">Voit myös valita useita työntekijöitä, joka on rekisteröity johonkin etuun, ja muuttaa niiden kattamiseen päättymispäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-141">You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage.</span></span> 

<span data-ttu-id="fc5ca-142">Etujen joukkopäättämisen avulla voi samaan tapaan laajentaa sekä edun että työntekijöiden rekisteröitymisten päättymispäivää, jos haluat edun olevan käytettävissä alkuperäistä aikaa pidempään.</span><span class="sxs-lookup"><span data-stu-id="fc5ca-142">Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.</span></span>

<a name="additional-resources"></a><span data-ttu-id="fc5ca-143">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="fc5ca-143">Additional resources</span></span>
--------

[<span data-ttu-id="fc5ca-144">Etukelpoisuuden käytännöt</span><span class="sxs-lookup"><span data-stu-id="fc5ca-144">Benefit eligibility policies</span></span>](benefit-eligibility-policies.md)




