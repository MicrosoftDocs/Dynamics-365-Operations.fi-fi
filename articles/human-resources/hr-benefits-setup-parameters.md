---
title: Aseta etujenhallinnan parametrit
description: Määritä etujen hallinnan parametrit Microsoft Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3e001c08751ea9c8bcab0e11a04b6cf639e51d1d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429981"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="3bd42-103">Etujen hallinnan parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3bd42-103">Set Benefits management parameters</span></span>

<span data-ttu-id="3bd42-104">Ennen kuin voit määrittää lomasuunnitelmia Microsoft Dynamics 365 Human Resourcesissa, sinun täytyy määrittää etujen hallintaparametrit.</span><span class="sxs-lookup"><span data-stu-id="3bd42-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="3bd42-105">Nämä parametrit määrittävät oletusarvot, syykoodit ja muut asetukset.</span><span class="sxs-lookup"><span data-stu-id="3bd42-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="3bd42-106">Konfiguroi yleiset parametrit</span><span class="sxs-lookup"><span data-stu-id="3bd42-106">Configure general parameters</span></span>

1. <span data-ttu-id="3bd42-107">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="3bd42-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="3bd42-108">Määritä **Yleiset**-välilehdelle seuraavien kenttien arvot:</span><span class="sxs-lookup"><span data-stu-id="3bd42-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="3bd42-109">Kenttä</span><span class="sxs-lookup"><span data-stu-id="3bd42-109">Field</span></span> | <span data-ttu-id="3bd42-110">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="3bd42-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3bd42-111">**Maa/alue**</span><span class="sxs-lookup"><span data-stu-id="3bd42-111">**Country/region**</span></span> | <span data-ttu-id="3bd42-112">**Maa/alue**-kenttä määrittää postinumeroiden/valtioiden näyttöjärjestyksen.</span><span class="sxs-lookup"><span data-stu-id="3bd42-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="3bd42-113">Valittu maa näkyy ensimmäisenä avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3bd42-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="3bd42-114">**Rekisteröinnin syykoodi**</span><span class="sxs-lookup"><span data-stu-id="3bd42-114">**Enrollment reason code**</span></span> | <span data-ttu-id="3bd42-115">Valitse oletussyykoodi, jota käytetään, kun työntekijän suunnitelmat luodaan avoimen rekisteröinnin käsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="3bd42-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="3bd42-116">**Peruutuksen syykoodi**</span><span class="sxs-lookup"><span data-stu-id="3bd42-116">**Cancellation reason code**</span></span> | <span data-ttu-id="3bd42-117">Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="3bd42-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="3bd42-118">Se näkyy valintaikkunassa peruutusprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="3bd42-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="3bd42-119">Käyttäjät voivat tarvittaessa muuttaa **peruutuksen syykoodia**.</span><span class="sxs-lookup"><span data-stu-id="3bd42-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="3bd42-120">**Uudelleenavauksen syykoodi**</span><span class="sxs-lookup"><span data-stu-id="3bd42-120">**Reopen reason code**</span></span> | <span data-ttu-id="3bd42-121">Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma avataan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="3bd42-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="3bd42-122">Se näkyy valintaikkunassa peruutusprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="3bd42-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="3bd42-123">Käyttäjät voivat tarvittaessa muuttaa **uudelleen avaamisen syykoodia**.</span><span class="sxs-lookup"><span data-stu-id="3bd42-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="3bd42-124">**Elinkaaritapahtuman syykoodi**</span><span class="sxs-lookup"><span data-stu-id="3bd42-124">**Life event reason code**</span></span> | <span data-ttu-id="3bd42-125">Tapahtuma, jota käytetään elinkaaritapahtuman tapahtuessa.</span><span class="sxs-lookup"><span data-stu-id="3bd42-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="3bd42-126">**Asteen muutoksen syykoodi**</span><span class="sxs-lookup"><span data-stu-id="3bd42-126">**Rate change reason code**</span></span> | <span data-ttu-id="3bd42-127">Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma peruutetaan ja avataan uudelleen hinnan muutoksen päivitysprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="3bd42-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="3bd42-128">Se ilmaisee, mitä tietuetta hinnan muutoksen päivitysprosessi on muuttanut.</span><span class="sxs-lookup"><span data-stu-id="3bd42-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="3bd42-129">**Uusi työntekijä on sallittu**</span><span class="sxs-lookup"><span data-stu-id="3bd42-129">**New hire eligible**</span></span> | <span data-ttu-id="3bd42-130">Määrittää, ovatko uudet työntekijät kelvollisia.</span><span class="sxs-lookup"><span data-stu-id="3bd42-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="3bd42-131">**Uuden työntekijän rekisteröintikausi**</span><span class="sxs-lookup"><span data-stu-id="3bd42-131">**New hire enrollment period**</span></span> | <span data-ttu-id="3bd42-132">Ajanjakso, jolloin uusi osamaksu on sallittu.</span><span class="sxs-lookup"><span data-stu-id="3bd42-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="3bd42-133">**Huomautus**: Tämä asetus ohittaa uuden suunnitelman oikeutussääntöön määrittämäsi työhönottoajan jakson.</span><span class="sxs-lookup"><span data-stu-id="3bd42-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="3bd42-134">**Elinkaaritapahtumat ovat käytössä**</span><span class="sxs-lookup"><span data-stu-id="3bd42-134">**Life events enabled**</span></span> | <span data-ttu-id="3bd42-135">Mahdollistaa elinkaaritapahtumat.</span><span class="sxs-lookup"><span data-stu-id="3bd42-135">Enables life events.</span></span> |
   | <span data-ttu-id="3bd42-136">**Piilota vanhat etulomakkeet**</span><span class="sxs-lookup"><span data-stu-id="3bd42-136">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="3bd42-137">Sallii vanhojen etuuslomakkeiden piilottamisen.</span><span class="sxs-lookup"><span data-stu-id="3bd42-137">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="3bd42-138">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="3bd42-138">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="3bd42-139">Määritä työntekijän itsepalveluparametrit</span><span class="sxs-lookup"><span data-stu-id="3bd42-139">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="3bd42-140">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="3bd42-140">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="3bd42-141">Määritä **Työntekijän itsepalvelu**-välilehdelle seuraavien kenttien arvot:</span><span class="sxs-lookup"><span data-stu-id="3bd42-141">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="3bd42-142">Kenttä</span><span class="sxs-lookup"><span data-stu-id="3bd42-142">Field</span></span> | <span data-ttu-id="3bd42-143">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="3bd42-143">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3bd42-144">**Edun vahvistus**</span><span class="sxs-lookup"><span data-stu-id="3bd42-144">**Benefit verification**</span></span> | <span data-ttu-id="3bd42-145">Itsepalvelu-etujen aikana käytettävä tarkistusteksti kassalla.</span><span class="sxs-lookup"><span data-stu-id="3bd42-145">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="3bd42-146">**Valitse edustajat automaattisesti**</span><span class="sxs-lookup"><span data-stu-id="3bd42-146">**Auto select designees**</span></span> | <span data-ttu-id="3bd42-147">Määrittää, valitaanko huollettavat ja edunsaajat automaattisesti suunnitelmavaihtoehtojen kelpoisuuden perusteella.</span><span class="sxs-lookup"><span data-stu-id="3bd42-147">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="3bd42-148">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="3bd42-148">Select **Save**.</span></span>
