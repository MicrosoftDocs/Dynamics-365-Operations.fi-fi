---
title: Aseta etujenhallinnan parametrit
description: Määritä etujen hallinnan parametrit Microsoft Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: AnnBe
ms.date: 07/16/2020
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
ms.openlocfilehash: 85bbe5d3b422f2f29f1d1fe8ee269b407da691c2
ms.sourcegitcommit: 9dc5c7dd5877cc6e7cd0059d173bcd8052ba13bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/16/2020
ms.locfileid: "3599353"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="5bcf4-103">Etujen hallinnan parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5bcf4-103">Set Benefits management parameters</span></span>

<span data-ttu-id="5bcf4-104">Ennen kuin voit määrittää lomasuunnitelmia Microsoft Dynamics 365 Human Resourcesissa, sinun täytyy määrittää etujen hallintaparametrit.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="5bcf4-105">Nämä parametrit määrittävät oletusarvot, syykoodit ja muut asetukset.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="5bcf4-106">Konfiguroi yleiset parametrit</span><span class="sxs-lookup"><span data-stu-id="5bcf4-106">Configure general parameters</span></span>

1. <span data-ttu-id="5bcf4-107">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdassa **Henkilöstöhallinnon jaetut parametrit**.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="5bcf4-108">Määritä **Yleiset**-välilehdelle seuraavien kenttien arvot:</span><span class="sxs-lookup"><span data-stu-id="5bcf4-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="5bcf4-109">Kenttä</span><span class="sxs-lookup"><span data-stu-id="5bcf4-109">Field</span></span> | <span data-ttu-id="5bcf4-110">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="5bcf4-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5bcf4-111">**Maa/alue**</span><span class="sxs-lookup"><span data-stu-id="5bcf4-111">**Country/region**</span></span> | <span data-ttu-id="5bcf4-112">**Maa/alue**-kenttä määrittää postinumeroiden/valtioiden näyttöjärjestyksen.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="5bcf4-113">Valittu maa näkyy ensimmäisenä avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="5bcf4-114">**Rekisteröinnin syykoodi**</span><span class="sxs-lookup"><span data-stu-id="5bcf4-114">**Enrollment reason code**</span></span> | <span data-ttu-id="5bcf4-115">Valitse oletussyykoodi, jota käytetään, kun työntekijän suunnitelmat luodaan avoimen rekisteröinnin käsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="5bcf4-116">**Peruutuksen syykoodi**</span><span class="sxs-lookup"><span data-stu-id="5bcf4-116">**Cancellation reason code**</span></span> | <span data-ttu-id="5bcf4-117">Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="5bcf4-118">Se näkyy valintaikkunassa peruutusprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="5bcf4-119">Käyttäjät voivat tarvittaessa muuttaa **peruutuksen syykoodia**.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="5bcf4-120">**Uudelleenavauksen syykoodi**</span><span class="sxs-lookup"><span data-stu-id="5bcf4-120">**Reopen reason code**</span></span> | <span data-ttu-id="5bcf4-121">Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma avataan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="5bcf4-122">Se näkyy valintaikkunassa peruutusprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="5bcf4-123">Käyttäjät voivat tarvittaessa muuttaa **uudelleen avaamisen syykoodia**.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="5bcf4-124">**Elinkaaritapahtuman syykoodi**</span><span class="sxs-lookup"><span data-stu-id="5bcf4-124">**Life event reason code**</span></span> | <span data-ttu-id="5bcf4-125">Tapahtuma, jota käytetään elinkaaritapahtuman tapahtuessa.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="5bcf4-126">**Asteen muutoksen syykoodi**</span><span class="sxs-lookup"><span data-stu-id="5bcf4-126">**Rate change reason code**</span></span> | <span data-ttu-id="5bcf4-127">Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma peruutetaan ja avataan uudelleen hinnan muutoksen päivitysprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="5bcf4-128">Se ilmaisee, mitä tietuetta hinnan muutoksen päivitysprosessi on muuttanut.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="5bcf4-129">**Vuosittainen etupalkka**</span><span class="sxs-lookup"><span data-stu-id="5bcf4-129">**Benefits annual salary**</span></span> | <span data-ttu-id="5bcf4-130">Antaa mahdollisuuden määrittää työntekijän **Etuuksien vuosipalkka** -summan.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="5bcf4-131">Human Resources käyttää **Etuuksien vuosipalkka** -summaa määrittämään katetut summat kiinteän vuosittaisen kompensaatiosumman sijaan.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-131">Human Resources will use the **Benefits annual salary** amount when determing coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="5bcf4-132">**Uusi työntekijä on sallittu**</span><span class="sxs-lookup"><span data-stu-id="5bcf4-132">**New hire eligible**</span></span> | <span data-ttu-id="5bcf4-133">Määrittää, ovatko uudet työntekijät kelvollisia.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="5bcf4-134">**Uuden työntekijän rekisteröintikausi**</span><span class="sxs-lookup"><span data-stu-id="5bcf4-134">**New hire enrollment period**</span></span> | <span data-ttu-id="5bcf4-135">Ajanjakso, jolloin uusi osamaksu on sallittu.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="5bcf4-136">**Huomautus**: Tämä asetus ohittaa uuden suunnitelman oikeutussääntöön määrittämäsi työhönottoajan jakson.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="5bcf4-137">**Oletusmaksutiheys**</span><span class="sxs-lookup"><span data-stu-id="5bcf4-137">**Default pay frequency**</span></span> | <span data-ttu-id="5bcf4-138">Oletusmaksuväli, jota käytetään, kun uusia työntekijöitä lisätään.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="5bcf4-139">**Elinkaaritapahtumat ovat käytössä**</span><span class="sxs-lookup"><span data-stu-id="5bcf4-139">**Life events enabled**</span></span> | <span data-ttu-id="5bcf4-140">Mahdollistaa elinkaaritapahtumat.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-140">Enables life events.</span></span> |
   | <span data-ttu-id="5bcf4-141">**Piilota vanhat etulomakkeet**</span><span class="sxs-lookup"><span data-stu-id="5bcf4-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="5bcf4-142">Sallii vanhojen etuuslomakkeiden piilottamisen.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-142">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="5bcf4-143">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-143">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="5bcf4-144">Määritä työntekijän itsepalveluparametrit</span><span class="sxs-lookup"><span data-stu-id="5bcf4-144">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="5bcf4-145">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdassa **Henkilöstöhallinnon parametrit**.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-145">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="5bcf4-146">Määritä **Työntekijän itsepalvelu**-välilehdelle seuraavien kenttien arvot:</span><span class="sxs-lookup"><span data-stu-id="5bcf4-146">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="5bcf4-147">Kenttä</span><span class="sxs-lookup"><span data-stu-id="5bcf4-147">Field</span></span> | <span data-ttu-id="5bcf4-148">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="5bcf4-148">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5bcf4-149">**Edun vahvistus**</span><span class="sxs-lookup"><span data-stu-id="5bcf4-149">**Benefit verification**</span></span> | <span data-ttu-id="5bcf4-150">Itsepalvelu-etujen aikana käytettävä tarkistusteksti kassalla.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-150">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="5bcf4-151">**Valitse edustajat automaattisesti**</span><span class="sxs-lookup"><span data-stu-id="5bcf4-151">**Auto select designees**</span></span> | <span data-ttu-id="5bcf4-152">Määrittää, valitaanko huollettavat ja edunsaajat automaattisesti suunnitelmavaihtoehtojen kelpoisuuden perusteella.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-152">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="5bcf4-153">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5bcf4-153">Select **Save**.</span></span>
