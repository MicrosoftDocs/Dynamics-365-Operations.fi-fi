---
title: Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (14. helmikuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32f3bab38233833498ed566fa1558a023b3bc0dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461053"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-14-2019"></a><span data-ttu-id="5e346-103">Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (14. helmikuuta 2019)</span><span class="sxs-lookup"><span data-stu-id="5e346-103">What's new or changed in Dynamics 365 Talent (February 14, 2019)</span></span>

<span data-ttu-id="5e346-104">Tässä ohjeaiheessa käsitellään Talentin uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="5e346-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="5e346-105">Attractin muutokset</span><span class="sxs-lookup"><span data-stu-id="5e346-105">Changes in Attract</span></span>
<span data-ttu-id="5e346-106">Tässä julkaisussa on vähäisiä ohjelmakorjauksia.</span><span class="sxs-lookup"><span data-stu-id="5e346-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="5e346-107">Onboardingin muutokset</span><span class="sxs-lookup"><span data-stu-id="5e346-107">Changes in Onboarding</span></span>
<span data-ttu-id="5e346-108">Tässä julkaisussa on vähäisiä ohjelmakorjauksia.</span><span class="sxs-lookup"><span data-stu-id="5e346-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="5e346-109">Core HR:n muutokset</span><span class="sxs-lookup"><span data-stu-id="5e346-109">Changes in Core HR</span></span> 
<span data-ttu-id="5e346-110">**Koontiversio 8.1.2146**</span><span class="sxs-lookup"><span data-stu-id="5e346-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="5e346-111">Työntekijän kiinteä kompensaatio -yksikkö ei vie kaikkia tietueita</span><span class="sxs-lookup"><span data-stu-id="5e346-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="5e346-112">Tämän muutoksen ansiosta **Työntekijän kiinteä kompensaatio** -yksikkö vie nyt kaikki tietueet.</span><span class="sxs-lookup"><span data-stu-id="5e346-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="5e346-113">Yksikön avulla voidaan luoda ja päivittää aiemmin luodut työntekijöiden kiinteän kompensaation tietueet.</span><span class="sxs-lookup"><span data-stu-id="5e346-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="5e346-114">Työsuhteen päättymispäivä ei noudata työntekijän ensisijaisen aikavyöhykkeen asetuksia</span><span class="sxs-lookup"><span data-stu-id="5e346-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="5e346-115">Työsuhteen päättymispäivät noudattavat nyt käyttäjän ensisijaista aikavyöhykettä, kun työsuhde yrityksessä luodaan tai se päättyy.</span><span class="sxs-lookup"><span data-stu-id="5e346-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="5e346-116">Brittiläiset osoitteet näkyvät analytiikassa itäsveitsiläisinä osoitteina.</span><span class="sxs-lookup"><span data-stu-id="5e346-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="5e346-117">Tässä julkaisussa on tehty muutos, joka korjaa **henkilöstöhallinnon** sijaintikohtaisen henkilömääräraportin osoitteiden virheellisen kohdistuksen.</span><span class="sxs-lookup"><span data-stu-id="5e346-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="5e346-118">Työsuhteen päättymiskoodia ei täytetä työntekijän toimen määritystietueessa toimea päätettäessä</span><span class="sxs-lookup"><span data-stu-id="5e346-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="5e346-119">Irtisanomisen syy -oletuskoodiin on tehty muutos, kun sitä käytetään työtekijän toimimäärityksen päättämiseen.</span><span class="sxs-lookup"><span data-stu-id="5e346-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="5e346-120">Työn kompensaatiotasojen uuden yksikön luonti</span><span class="sxs-lookup"><span data-stu-id="5e346-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="5e346-121">Luotiin uusi Data Management Framework (DMF).</span><span class="sxs-lookup"><span data-stu-id="5e346-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="5e346-122">Yksikkö mahdollistaa kunkin järjestelmässä määritetyn työn kompensaatiotasojen, markkina-arvojen ja kyselytietojen luonnin ja päivittämisen.</span><span class="sxs-lookup"><span data-stu-id="5e346-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>
