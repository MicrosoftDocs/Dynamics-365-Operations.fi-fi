---
title: Etujen hallinnan ja työntekijän itsepalveluparametrien määrittäminen kaikille yrityksille
description: Etujen hallinnan ja työntekijän itsepalveluparametrien määrittäminen Microsoft Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
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
ms.openlocfilehash: b50c4f71789c34f08ce810312f3c3198303b031e
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692694"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="2e259-103">Etujen hallinnan ja työntekijän itsepalveluparametrien määrittäminen kaikille yrityksille</span><span class="sxs-lookup"><span data-stu-id="2e259-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

<span data-ttu-id="2e259-104">Ennen kuin voit määrittää etusuunnitelmat Microsoft Dynamics 365 Human Resourcesissa, sinun täytyy määrittää etujen hallintaparametrit.</span><span class="sxs-lookup"><span data-stu-id="2e259-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="2e259-105">Nämä parametrit määrittävät oletusarvot, syykoodit ja muut asetukset.</span><span class="sxs-lookup"><span data-stu-id="2e259-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="2e259-106">Konfiguroi yleiset parametrit</span><span class="sxs-lookup"><span data-stu-id="2e259-106">Configure general parameters</span></span>

1. <span data-ttu-id="2e259-107">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdassa **Henkilöstöhallinnon jaetut parametrit**.</span><span class="sxs-lookup"><span data-stu-id="2e259-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="2e259-108">Määritä **Etujen hallinta** -välilehdessä seuraavien kenttien arvot:</span><span class="sxs-lookup"><span data-stu-id="2e259-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="2e259-109">Kenttä</span><span class="sxs-lookup"><span data-stu-id="2e259-109">Field</span></span> | <span data-ttu-id="2e259-110">kuvaus</span><span class="sxs-lookup"><span data-stu-id="2e259-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="2e259-111">**Maa/alue**</span><span class="sxs-lookup"><span data-stu-id="2e259-111">**Country/region**</span></span> | <span data-ttu-id="2e259-112">**Maa/alue**-kenttä määrittää postinumeroiden/valtioiden näyttöjärjestyksen.</span><span class="sxs-lookup"><span data-stu-id="2e259-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="2e259-113">Valittu maa näkyy ensimmäisenä avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="2e259-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="2e259-114">**Rekisteröinnin syykoodi**</span><span class="sxs-lookup"><span data-stu-id="2e259-114">**Enrollment reason code**</span></span> | <span data-ttu-id="2e259-115">Valitse oletussyykoodi, jota käytetään, kun työntekijän suunnitelmat luodaan avoimen rekisteröinnin käsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="2e259-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="2e259-116">**Peruutuksen syykoodi**</span><span class="sxs-lookup"><span data-stu-id="2e259-116">**Cancellation reason code**</span></span> | <span data-ttu-id="2e259-117">Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="2e259-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="2e259-118">Se näkyy valintaikkunassa peruutusprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="2e259-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="2e259-119">Käyttäjät voivat tarvittaessa muuttaa **peruutuksen syykoodia**.</span><span class="sxs-lookup"><span data-stu-id="2e259-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="2e259-120">**Uudelleenavauksen syykoodi**</span><span class="sxs-lookup"><span data-stu-id="2e259-120">**Reopen reason code**</span></span> | <span data-ttu-id="2e259-121">Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma avataan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="2e259-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="2e259-122">Se näkyy valintaikkunassa peruutusprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="2e259-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="2e259-123">Käyttäjät voivat tarvittaessa muuttaa **uudelleen avaamisen syykoodia**.</span><span class="sxs-lookup"><span data-stu-id="2e259-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="2e259-124">**Elinkaaritapahtuman syykoodi**</span><span class="sxs-lookup"><span data-stu-id="2e259-124">**Life event reason code**</span></span> | <span data-ttu-id="2e259-125">Tapahtuma, jota käytetään elinkaaritapahtuman tapahtuessa.</span><span class="sxs-lookup"><span data-stu-id="2e259-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="2e259-126">**Asteen muutoksen syykoodi**</span><span class="sxs-lookup"><span data-stu-id="2e259-126">**Rate change reason code**</span></span> | <span data-ttu-id="2e259-127">Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma peruutetaan ja avataan uudelleen hinnan muutoksen päivitysprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="2e259-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="2e259-128">Se ilmaisee, mitä tietuetta hinnan muutoksen päivitysprosessi on muuttanut.</span><span class="sxs-lookup"><span data-stu-id="2e259-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="2e259-129">**Vuosittainen etupalkka**</span><span class="sxs-lookup"><span data-stu-id="2e259-129">**Benefits annual salary**</span></span> | <span data-ttu-id="2e259-130">Antaa mahdollisuuden määrittää työntekijän **Etuuksien vuosipalkka** -summan.</span><span class="sxs-lookup"><span data-stu-id="2e259-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="2e259-131">Human Resources käyttää **Etuuksien vuosipalkka** -summaa määrittämään katetut summat kiinteän vuosittaisen kompensaatiosumman sijaan.</span><span class="sxs-lookup"><span data-stu-id="2e259-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="2e259-132">**Uusi työntekijä on sallittu**</span><span class="sxs-lookup"><span data-stu-id="2e259-132">**New hire eligible**</span></span> | <span data-ttu-id="2e259-133">Määrittää, ovatko uudet työntekijät kelvollisia.</span><span class="sxs-lookup"><span data-stu-id="2e259-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="2e259-134">**Uuden työntekijän rekisteröintikausi**</span><span class="sxs-lookup"><span data-stu-id="2e259-134">**New hire enrollment period**</span></span> | <span data-ttu-id="2e259-135">Ajanjakso, jolloin uusi osamaksu on sallittu.</span><span class="sxs-lookup"><span data-stu-id="2e259-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="2e259-136">**Huomautus**: Tämä asetus ohittaa uuden suunnitelman oikeutussääntöön määrittämäsi työhönottoajan jakson.</span><span class="sxs-lookup"><span data-stu-id="2e259-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="2e259-137">**Oletusmaksutiheys**</span><span class="sxs-lookup"><span data-stu-id="2e259-137">**Default pay frequency**</span></span> | <span data-ttu-id="2e259-138">Oletusmaksuväli, jota käytetään, kun uusia työntekijöitä lisätään.</span><span class="sxs-lookup"><span data-stu-id="2e259-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="2e259-139">**Elinkaaritapahtumat ovat käytössä**</span><span class="sxs-lookup"><span data-stu-id="2e259-139">**Life events enabled**</span></span> | <span data-ttu-id="2e259-140">Mahdollistaa elinkaaritapahtumat.</span><span class="sxs-lookup"><span data-stu-id="2e259-140">Enables life events.</span></span> |
   | <span data-ttu-id="2e259-141">**Piilota vanhat etulomakkeet**</span><span class="sxs-lookup"><span data-stu-id="2e259-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="2e259-142">Sallii vanhojen etuuslomakkeiden piilottamisen.</span><span class="sxs-lookup"><span data-stu-id="2e259-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="2e259-143">**Edun vahvistus**</span><span class="sxs-lookup"><span data-stu-id="2e259-143">**Benefit verification**</span></span> | <span data-ttu-id="2e259-144">Itsepalvelu-etujen aikana käytettävä tarkistusteksti kassalla.</span><span class="sxs-lookup"><span data-stu-id="2e259-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="2e259-145">**Valitse edustajat automaattisesti**</span><span class="sxs-lookup"><span data-stu-id="2e259-145">**Auto select designees**</span></span> | <span data-ttu-id="2e259-146">Määrittää, valitaanko huollettavat ja edunsaajat automaattisesti suunnitelmavaihtoehtojen kelpoisuuden perusteella.</span><span class="sxs-lookup"><span data-stu-id="2e259-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="2e259-147">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2e259-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="2e259-148">Työntekijän itsepalveluparametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2e259-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="2e259-149">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdassa **Henkilöstöhallinnon parametrit**.</span><span class="sxs-lookup"><span data-stu-id="2e259-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="2e259-150">Määritä **Etujen hallinta** -välilehdessä seuraavien kenttien arvot:</span><span class="sxs-lookup"><span data-stu-id="2e259-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="2e259-151">Kenttä</span><span class="sxs-lookup"><span data-stu-id="2e259-151">Field</span></span> | <span data-ttu-id="2e259-152">kuvaus</span><span class="sxs-lookup"><span data-stu-id="2e259-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="2e259-153">**Edun vahvistus**</span><span class="sxs-lookup"><span data-stu-id="2e259-153">**Benefit verification**</span></span> | <span data-ttu-id="2e259-154">Itsepalvelu-etujen aikana käytettävä tarkistusteksti kassalla.</span><span class="sxs-lookup"><span data-stu-id="2e259-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="2e259-155">**Valitse edustajat automaattisesti**</span><span class="sxs-lookup"><span data-stu-id="2e259-155">**Auto select designees**</span></span> | <span data-ttu-id="2e259-156">Määrittää, valitaanko huollettavat ja edunsaajat automaattisesti suunnitelmavaihtoehtojen kelpoisuuden perusteella.</span><span class="sxs-lookup"><span data-stu-id="2e259-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="2e259-157">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2e259-157">Select **Save**.</span></span>


