---
title: Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (29. lokakuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 83b4734190163ebd2dc29096632642bd45c61e8f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773874"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a><span data-ttu-id="acfd9-103">Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (29. lokakuuta 2019)</span><span class="sxs-lookup"><span data-stu-id="acfd9-103">What's new or changed in Dynamics 365 Talent (October 29, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="acfd9-104">Tässä ohjeaiheessa käsitellään Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="acfd9-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="acfd9-105">Attractin muutokset</span><span class="sxs-lookup"><span data-stu-id="acfd9-105">Changes in Attract</span></span>

<span data-ttu-id="acfd9-106">Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.</span><span class="sxs-lookup"><span data-stu-id="acfd9-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="acfd9-107">Onboardin muutokset</span><span class="sxs-lookup"><span data-stu-id="acfd9-107">Changes in Onboard</span></span>

<span data-ttu-id="acfd9-108">Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.</span><span class="sxs-lookup"><span data-stu-id="acfd9-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="acfd9-109">Core HR:n muutokset</span><span class="sxs-lookup"><span data-stu-id="acfd9-109">Changes in Core HR</span></span>

<span data-ttu-id="acfd9-110">Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2586.</span><span class="sxs-lookup"><span data-stu-id="acfd9-110">Changes described in this section apply to build number 8.1.2586.</span></span> <span data-ttu-id="acfd9-111">Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.</span><span class="sxs-lookup"><span data-stu-id="acfd9-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a><span data-ttu-id="acfd9-112">Roolittomien osapuolien poistamisen pitäisi olla oletusarvoisesti käytössä (371233)</span><span class="sxs-lookup"><span data-stu-id="acfd9-112">Delete parties with no roles should be on by default (371233)</span></span>

<span data-ttu-id="acfd9-113">Kun valmistelet uuden ympäristön Talentissa, **Poista osapuolet, jos roolia ei ole** on otettu oletusarvoisesti käyttöön.</span><span class="sxs-lookup"><span data-stu-id="acfd9-113">When you provision a new environment in Talent, **Delete parties if no roles exist** is turned on by default.</span></span> <span data-ttu-id="acfd9-114">Kun poistat työntekijän, työntekijään liitettyä osapuolta ei poisteta ellei tätä asetusta ole otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="acfd9-114">When you delete a worker, the party associated with the worker is not removed unless this setting is on.</span></span> <span data-ttu-id="acfd9-115">Tämä muutos rajoittaa yleisen osoitekirjan tietueiden kaksoiskappaleita, kun työntekijöitä on tuotava, muutettava tai tuotava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="acfd9-115">This change limits duplicate records in the global address book when you need to import, change, or reimport workers.</span></span>

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a><span data-ttu-id="acfd9-116">Lomapyyntöjen luonnosten ja peruutettujen lomapyyntöjen poistaminen Common Data Servicessa on sallittava (376999)</span><span class="sxs-lookup"><span data-stu-id="acfd9-116">Draft and cancelled leave requests should be allowed to be deleted in Common Data Service (376999)</span></span>

<span data-ttu-id="acfd9-117">Tämän muutoksen myötä voi nyt poistaa lomapyyntöjä, joiden tila Common Data Servicessa on **Luonnos** tai **Peruutettu**.</span><span class="sxs-lookup"><span data-stu-id="acfd9-117">With this change, you can now delete leave requests with a status of **Draft** or **Cancelled** in Common Data Service.</span></span>

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a><span data-ttu-id="acfd9-118">Mukautettujen kenttien luettelon lisäarvot eivät heijastu Common Data Serviceen, kun Mukautetut kentät -lomakkeessa valitaan Käytä (379599)</span><span class="sxs-lookup"><span data-stu-id="acfd9-118">Additional list values in custom fields aren't reflected in Common Data Service after clicking Apply on the Custom fields form (379599)</span></span>

<span data-ttu-id="acfd9-119">Kun lisäät uusia luetteloarvoja aiemmin luotuun mukautettuun kenttään, joka on jo synkronoitu Common Data Servicessa, ne ovat nyt käytettävissä Common Data Servicessa sen jälkeen, kun käytät muutoksia **Mukautetut kentät** -lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="acfd9-119">When you add new list values to an existing custom field that has already synchronized with Common Data Service, they're now available in Common Data Serivce after you apply your changes in the **Custom fields** form.</span></span>

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a><span data-ttu-id="acfd9-120">Perehdytyksen tarkistusluetteloiden käyttäminen yrityksissä, kun työsuhteita on useampi kuin yksi (371270)</span><span class="sxs-lookup"><span data-stu-id="acfd9-120">Apply onboarding checklists across legal entities when more than one employment exists (371270)</span></span>

<span data-ttu-id="acfd9-121">Tämän viikon julkaisussa voit käyttää tarkistusluetteloita työntekijöillä, joilla on useampi kuin yks työsuhde kohdassa **Työntekijä-lomake > Tarkistusluettelot**.</span><span class="sxs-lookup"><span data-stu-id="acfd9-121">In this week's release, you can apply checklists to employees with more than one employment in **Worker form > Checklists**.</span></span>

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a><span data-ttu-id="acfd9-122">Etuuksien avoimen haun esiversiotoiminto on poistettu</span><span class="sxs-lookup"><span data-stu-id="acfd9-122">Benefits open enrollment preview feature has been removed</span></span>

<span data-ttu-id="acfd9-123">Blogikirjoituksessa [Core HR:ään tehdyt strategiset sijoitukset edistävät operatiivista suorituskykyä](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) annetun ilmoituksen myötä Microsoft on poistanut etuuksien avoimen haun ominaisuuden julkisesta esiversiosta.</span><span class="sxs-lookup"><span data-stu-id="acfd9-123">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog post, Microsoft has removed the benefits open enrollment feature from public preview.</span></span> <span data-ttu-id="acfd9-124">Uusi toiminto julkaistaan myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="acfd9-124">New functionality will be released in the future.</span></span> <span data-ttu-id="acfd9-125">Etuuksien avoimen haun toiminnon tuotantokäyttöä ei tueta.</span><span class="sxs-lookup"><span data-stu-id="acfd9-125">Production use of the benefits open enrollment feature isn't be supported.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="acfd9-126">Tulossa pian</span><span class="sxs-lookup"><span data-stu-id="acfd9-126">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="acfd9-127">Kehityskeskustelujen tulostaminen</span><span class="sxs-lookup"><span data-stu-id="acfd9-127">Print performance reviews</span></span>

<span data-ttu-id="acfd9-128">Katso lisätietoja Dynamics 365: vuoden 2019 julkaisuaallon 2 suunnitelman kohdasta [Kehityskeskustelujen tulostaminen](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews).</span><span class="sxs-lookup"><span data-stu-id="acfd9-128">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="acfd9-129">Ominaisuushallinnan työtila</span><span class="sxs-lookup"><span data-stu-id="acfd9-129">Feature management workspace</span></span>

<span data-ttu-id="acfd9-130">Ominaisuudet lisätään ja päivitetään jokaisessa versiossa.</span><span class="sxs-lookup"><span data-stu-id="acfd9-130">Features are added and updated in every release.</span></span> <span data-ttu-id="acfd9-131">Toiminnon hallintakokemus tarjoaa työtilan, jossa voit tarkastella kussakin julkaisussa toimitettujen toimintojen luetteloa.</span><span class="sxs-lookup"><span data-stu-id="acfd9-131">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="acfd9-132">Uudet asetukset ovat oletusarvoisesti poissa käytöstä.</span><span class="sxs-lookup"><span data-stu-id="acfd9-132">By default, new features are turned off.</span></span> <span data-ttu-id="acfd9-133">Työtilan avulla voit ottaa ne käyttöön ja tarkastella niiden dokumentaatiota.</span><span class="sxs-lookup"><span data-stu-id="acfd9-133">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="acfd9-134">Lisätietoja tulevista toimintojen hallinnan muutoksista löytyy [Toimintojen hallinnan yleiskuvauksesta](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="acfd9-134">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
