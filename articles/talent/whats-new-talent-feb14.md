---
title: Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (14. helmikuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.
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
ms.openlocfilehash: 1db7d032eade3f996e0554e64d6ea0704a347ed8
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/19/2019
ms.locfileid: "859387"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a><span data-ttu-id="f71df-103">Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (14. helmikuuta 2019)</span><span class="sxs-lookup"><span data-stu-id="f71df-103">What's new or changed in Dynamics 365 for Talent (February 14, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f71df-104">Tässä ohjeaiheessa käsitellään Talentin uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="f71df-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="f71df-105">Attractin muutokset</span><span class="sxs-lookup"><span data-stu-id="f71df-105">Changes in Attract</span></span>
<span data-ttu-id="f71df-106">Tässä julkaisussa on vähäisiä ohjelmakorjauksia.</span><span class="sxs-lookup"><span data-stu-id="f71df-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="f71df-107">Onboardingin muutokset</span><span class="sxs-lookup"><span data-stu-id="f71df-107">Changes in Onboarding</span></span>
<span data-ttu-id="f71df-108">Tässä julkaisussa on vähäisiä ohjelmakorjauksia.</span><span class="sxs-lookup"><span data-stu-id="f71df-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="f71df-109">Core HR:n muutokset</span><span class="sxs-lookup"><span data-stu-id="f71df-109">Changes in Core HR</span></span> 
<span data-ttu-id="f71df-110">**Koontiversio 8.1.2146**</span><span class="sxs-lookup"><span data-stu-id="f71df-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="f71df-111">Työntekijän kiinteä kompensaatio -yksikkö ei vie kaikkia tietueita</span><span class="sxs-lookup"><span data-stu-id="f71df-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="f71df-112">Tämän muutoksen ansiosta **Työntekijän kiinteä kompensaatio** -yksikkö vie nyt kaikki tietueet.</span><span class="sxs-lookup"><span data-stu-id="f71df-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="f71df-113">Yksikön avulla voidaan luoda ja päivittää aiemmin luodut työntekijöiden kiinteän kompensaation tietueet.</span><span class="sxs-lookup"><span data-stu-id="f71df-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="f71df-114">Työsuhteen päättymispäivä ei noudata työntekijän ensisijaisen aikavyöhykkeen asetuksia</span><span class="sxs-lookup"><span data-stu-id="f71df-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="f71df-115">Työsuhteen päättymispäivät noudattavat nyt käyttäjän ensisijaista aikavyöhykettä, kun työsuhde yrityksessä luodaan tai se päättyy.</span><span class="sxs-lookup"><span data-stu-id="f71df-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="f71df-116">Brittiläiset osoitteet näkyvät analytiikassa itäsveitsiläisinä osoitteina.</span><span class="sxs-lookup"><span data-stu-id="f71df-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="f71df-117">Tässä julkaisussa on tehty muutos, joka korjaa **henkilöstöhallinnon** sijaintikohtaisen henkilömääräraportin osoitteiden virheellisen kohdistuksen.</span><span class="sxs-lookup"><span data-stu-id="f71df-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="f71df-118">Työsuhteen päättymiskoodia ei täytetä työntekijän toimen määritystietueessa toimea päätettäessä</span><span class="sxs-lookup"><span data-stu-id="f71df-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="f71df-119">Irtisanomisen syy -oletuskoodiin on tehty muutos, kun sitä käytetään työtekijän toimimäärityksen päättämiseen.</span><span class="sxs-lookup"><span data-stu-id="f71df-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="f71df-120">Työn kompensaatiotasojen uuden yksikön luonti</span><span class="sxs-lookup"><span data-stu-id="f71df-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="f71df-121">Luotiin uusi Data Management Framework (DMF).</span><span class="sxs-lookup"><span data-stu-id="f71df-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="f71df-122">Yksikkö mahdollistaa kunkin järjestelmässä määritetyn työn kompensaatiotasojen, markkina-arvojen ja kyselytietojen luonnin ja päivittämisen.</span><span class="sxs-lookup"><span data-stu-id="f71df-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>
