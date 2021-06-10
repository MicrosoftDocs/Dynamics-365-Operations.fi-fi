---
title: Etujen hallinnan ja työntekijän itsepalveluparametrien määrittäminen kaikille yrityksille
description: Etujen hallinnan ja työntekijän itsepalveluparametrien määrittäminen Microsoft Dynamics 365 Human Resourcesissa.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d668238378e41287c7a9f845ae3e67078fc7776a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058965"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="09063-103">Etujen hallinnan ja työntekijän itsepalveluparametrien määrittäminen kaikille yrityksille</span><span class="sxs-lookup"><span data-stu-id="09063-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="09063-104">Ennen kuin voit määrittää etusuunnitelmat Microsoft Dynamics 365 Human Resourcesissa, sinun täytyy määrittää etujen hallintaparametrit.</span><span class="sxs-lookup"><span data-stu-id="09063-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="09063-105">Nämä parametrit määrittävät oletusarvot, syykoodit ja muut asetukset.</span><span class="sxs-lookup"><span data-stu-id="09063-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="09063-106">Konfiguroi yleiset parametrit</span><span class="sxs-lookup"><span data-stu-id="09063-106">Configure general parameters</span></span>

1. <span data-ttu-id="09063-107">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdassa **Henkilöstöhallinnon jaetut parametrit**.</span><span class="sxs-lookup"><span data-stu-id="09063-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="09063-108">Määritä **Etujen hallinta** -välilehdessä seuraavien kenttien arvot:</span><span class="sxs-lookup"><span data-stu-id="09063-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="09063-109">Kenttä</span><span class="sxs-lookup"><span data-stu-id="09063-109">Field</span></span> | <span data-ttu-id="09063-110">kuvaus</span><span class="sxs-lookup"><span data-stu-id="09063-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="09063-111">**Maa/alue**</span><span class="sxs-lookup"><span data-stu-id="09063-111">**Country/region**</span></span> | <span data-ttu-id="09063-112">**Maa/alue**-kenttä määrittää postinumeroiden/valtioiden näyttöjärjestyksen.</span><span class="sxs-lookup"><span data-stu-id="09063-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="09063-113">Valittu maa näkyy ensimmäisenä avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="09063-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="09063-114">**Rekisteröinnin syykoodi**</span><span class="sxs-lookup"><span data-stu-id="09063-114">**Enrollment reason code**</span></span> | <span data-ttu-id="09063-115">Valitse oletussyykoodi, jota käytetään, kun työntekijän suunnitelmat luodaan avoimen rekisteröinnin käsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="09063-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="09063-116">**Peruutuksen syykoodi**</span><span class="sxs-lookup"><span data-stu-id="09063-116">**Cancellation reason code**</span></span> | <span data-ttu-id="09063-117">Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="09063-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="09063-118">Se näkyy valintaikkunassa peruutusprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="09063-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="09063-119">Käyttäjät voivat tarvittaessa muuttaa **peruutuksen syykoodia**.</span><span class="sxs-lookup"><span data-stu-id="09063-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="09063-120">**Uudelleenavauksen syykoodi**</span><span class="sxs-lookup"><span data-stu-id="09063-120">**Reopen reason code**</span></span> | <span data-ttu-id="09063-121">Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma avataan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="09063-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="09063-122">Se näkyy valintaikkunassa peruutusprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="09063-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="09063-123">Käyttäjät voivat tarvittaessa muuttaa **uudelleen avaamisen syykoodia**.</span><span class="sxs-lookup"><span data-stu-id="09063-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="09063-124">**Elinkaaritapahtuman syykoodi**</span><span class="sxs-lookup"><span data-stu-id="09063-124">**Life event reason code**</span></span> | <span data-ttu-id="09063-125">Tapahtuma, jota käytetään elinkaaritapahtuman tapahtuessa.</span><span class="sxs-lookup"><span data-stu-id="09063-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="09063-126">**Asteen muutoksen syykoodi**</span><span class="sxs-lookup"><span data-stu-id="09063-126">**Rate change reason code**</span></span> | <span data-ttu-id="09063-127">Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma peruutetaan ja avataan uudelleen hinnan muutoksen päivitysprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="09063-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="09063-128">Se ilmaisee, mitä tietuetta hinnan muutoksen päivitysprosessi on muuttanut.</span><span class="sxs-lookup"><span data-stu-id="09063-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="09063-129">**Vuosittainen etupalkka**</span><span class="sxs-lookup"><span data-stu-id="09063-129">**Benefits annual salary**</span></span> | <span data-ttu-id="09063-130">Antaa mahdollisuuden määrittää työntekijän **Etuuksien vuosipalkka** -summan.</span><span class="sxs-lookup"><span data-stu-id="09063-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="09063-131">Human Resources käyttää **Etuuksien vuosipalkka** -summaa määrittämään katetut summat kiinteän vuosittaisen kompensaatiosumman sijaan.</span><span class="sxs-lookup"><span data-stu-id="09063-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="09063-132">**Uusi työntekijä on sallittu**</span><span class="sxs-lookup"><span data-stu-id="09063-132">**New hire eligible**</span></span> | <span data-ttu-id="09063-133">Määrittää, ovatko uudet työntekijät kelvollisia.</span><span class="sxs-lookup"><span data-stu-id="09063-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="09063-134">**Uuden työntekijän rekisteröintikausi**</span><span class="sxs-lookup"><span data-stu-id="09063-134">**New hire enrollment period**</span></span> | <span data-ttu-id="09063-135">Ajanjakso, jolloin uusi osamaksu on sallittu.</span><span class="sxs-lookup"><span data-stu-id="09063-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="09063-136">**Huomautus**: Tämä asetus ohittaa uuden suunnitelman oikeutussääntöön määrittämäsi työhönottoajan jakson.</span><span class="sxs-lookup"><span data-stu-id="09063-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="09063-137">**Oletusmaksutiheys**</span><span class="sxs-lookup"><span data-stu-id="09063-137">**Default pay frequency**</span></span> | <span data-ttu-id="09063-138">Oletusmaksuväli, jota käytetään, kun uusia työntekijöitä lisätään.</span><span class="sxs-lookup"><span data-stu-id="09063-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="09063-139">**Elinkaaritapahtumat ovat käytössä**</span><span class="sxs-lookup"><span data-stu-id="09063-139">**Life events enabled**</span></span> | <span data-ttu-id="09063-140">Mahdollistaa elinkaaritapahtumat.</span><span class="sxs-lookup"><span data-stu-id="09063-140">Enables life events.</span></span> |
   | <span data-ttu-id="09063-141">**Piilota vanhat etulomakkeet**</span><span class="sxs-lookup"><span data-stu-id="09063-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="09063-142">Sallii vanhojen etuuslomakkeiden piilottamisen.</span><span class="sxs-lookup"><span data-stu-id="09063-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="09063-143">**Edun vahvistus**</span><span class="sxs-lookup"><span data-stu-id="09063-143">**Benefit verification**</span></span> | <span data-ttu-id="09063-144">Itsepalvelu-etujen aikana käytettävä tarkistusteksti kassalla.</span><span class="sxs-lookup"><span data-stu-id="09063-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="09063-145">**Valitse edustajat automaattisesti**</span><span class="sxs-lookup"><span data-stu-id="09063-145">**Auto select designees**</span></span> | <span data-ttu-id="09063-146">Määrittää, valitaanko huollettavat ja edunsaajat automaattisesti suunnitelmavaihtoehtojen kelpoisuuden perusteella.</span><span class="sxs-lookup"><span data-stu-id="09063-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="09063-147">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="09063-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="09063-148">Työntekijän itsepalveluparametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="09063-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="09063-149">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdassa **Henkilöstöhallinnon parametrit**.</span><span class="sxs-lookup"><span data-stu-id="09063-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="09063-150">Määritä **Etujen hallinta** -välilehdessä seuraavien kenttien arvot:</span><span class="sxs-lookup"><span data-stu-id="09063-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="09063-151">Kenttä</span><span class="sxs-lookup"><span data-stu-id="09063-151">Field</span></span> | <span data-ttu-id="09063-152">kuvaus</span><span class="sxs-lookup"><span data-stu-id="09063-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="09063-153">**Edun vahvistus**</span><span class="sxs-lookup"><span data-stu-id="09063-153">**Benefit verification**</span></span> | <span data-ttu-id="09063-154">Itsepalvelu-etujen aikana käytettävä tarkistusteksti kassalla.</span><span class="sxs-lookup"><span data-stu-id="09063-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="09063-155">**Valitse edustajat automaattisesti**</span><span class="sxs-lookup"><span data-stu-id="09063-155">**Auto select designees**</span></span> | <span data-ttu-id="09063-156">Määrittää, valitaanko huollettavat ja edunsaajat automaattisesti suunnitelmavaihtoehtojen kelpoisuuden perusteella.</span><span class="sxs-lookup"><span data-stu-id="09063-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="09063-157">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="09063-157">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]