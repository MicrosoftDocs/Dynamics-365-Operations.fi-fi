---
title: Aseta etujenhallinnan parametrit
description: Määritä etujen hallinnan parametrit Microsoft Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008891"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="89ee8-103">Aseta etujenhallinnan parametrit</span><span class="sxs-lookup"><span data-stu-id="89ee8-103">Set Benefits management parameters</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="89ee8-104">Ennen kuin voit määrittää lomasuunnitelmia Microsoft Dynamics 365 Human Resourcesissa, sinun on määritettävä etujen hallintaparametrit.</span><span class="sxs-lookup"><span data-stu-id="89ee8-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you need to configure Benefits management parameters.</span></span> <span data-ttu-id="89ee8-105">Nämä parametrit määrittävät oletusarvot, syykoodit ja muut asetukset.</span><span class="sxs-lookup"><span data-stu-id="89ee8-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="89ee8-106">Konfiguroi yleiset parametrit</span><span class="sxs-lookup"><span data-stu-id="89ee8-106">Configure general parameters</span></span>

1. <span data-ttu-id="89ee8-107">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="89ee8-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="89ee8-108">Määritä **Yleiset**-välilehdelle seuraavien kenttien arvot:</span><span class="sxs-lookup"><span data-stu-id="89ee8-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="89ee8-109">Kenttä</span><span class="sxs-lookup"><span data-stu-id="89ee8-109">Field</span></span> | <span data-ttu-id="89ee8-110">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="89ee8-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="89ee8-111">**Maa/alue**</span><span class="sxs-lookup"><span data-stu-id="89ee8-111">**Country/region**</span></span> | <span data-ttu-id="89ee8-112">**Maa/alue**-kenttä määrittää postinumeroiden/valtioiden näyttöjärjestyksen.</span><span class="sxs-lookup"><span data-stu-id="89ee8-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="89ee8-113">Valittu maa näkyy ensimmäisenä avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="89ee8-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="89ee8-114">**Rekisteröinnin syykoodi**</span><span class="sxs-lookup"><span data-stu-id="89ee8-114">**Enrollment reason code**</span></span> | <span data-ttu-id="89ee8-115">Valitse oletussyykoodi, jota käytetään, kun työntekijän suunnitelmat luodaan avoimen rekisteröinnin käsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="89ee8-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="89ee8-116">**Peruutuksen syykoodi**</span><span class="sxs-lookup"><span data-stu-id="89ee8-116">**Cancellation reason code**</span></span> | <span data-ttu-id="89ee8-117">Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="89ee8-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="89ee8-118">Se näkyy valintaikkunassa peruutusprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="89ee8-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="89ee8-119">Käyttäjät voivat tarvittaessa muuttaa **peruutuksen syykoodia**.</span><span class="sxs-lookup"><span data-stu-id="89ee8-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="89ee8-120">**Uudelleenavauksen syykoodi**</span><span class="sxs-lookup"><span data-stu-id="89ee8-120">**Reopen reason code**</span></span> | <span data-ttu-id="89ee8-121">Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma avataan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="89ee8-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="89ee8-122">Se näkyy valintaikkunassa peruutusprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="89ee8-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="89ee8-123">Käyttäjät voivat tarvittaessa muuttaa **uudelleen avaamisen syykoodia**.</span><span class="sxs-lookup"><span data-stu-id="89ee8-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="89ee8-124">**Elinkaaritapahtuman syykoodi**</span><span class="sxs-lookup"><span data-stu-id="89ee8-124">**Life event reason code**</span></span> | <span data-ttu-id="89ee8-125">Tapahtuma, jota käytetään elinkaaritapahtuman tapahtuessa.</span><span class="sxs-lookup"><span data-stu-id="89ee8-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="89ee8-126">**Asteen muutoksen syykoodi**</span><span class="sxs-lookup"><span data-stu-id="89ee8-126">**Rate change reason code**</span></span> | <span data-ttu-id="89ee8-127">Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma peruutetaan ja avataan uudelleen hinnan muutoksen päivitysprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="89ee8-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="89ee8-128">Se ilmaisee, mitä tietuetta hinnan muutoksen päivitysprosessi on muuttanut.</span><span class="sxs-lookup"><span data-stu-id="89ee8-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="89ee8-129">**Uusi työntekijä on sallittu**</span><span class="sxs-lookup"><span data-stu-id="89ee8-129">**New hire eligible**</span></span> | <span data-ttu-id="89ee8-130">Määrittää, ovatko uudet työntekijät kelvollisia.</span><span class="sxs-lookup"><span data-stu-id="89ee8-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="89ee8-131">**Uuden työntekijän rekisteröintikausi**</span><span class="sxs-lookup"><span data-stu-id="89ee8-131">**New hire enrollment period**</span></span> | <span data-ttu-id="89ee8-132">Ajanjakso, jolloin uusi osamaksu on sallittu.</span><span class="sxs-lookup"><span data-stu-id="89ee8-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="89ee8-133">**Huomautus**: Tämä asetus ohittaa uuden suunnitelman oikeutussääntöön määrittämäsi työhönottoajan jakson.</span><span class="sxs-lookup"><span data-stu-id="89ee8-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="89ee8-134">**Vuosipalkan lisäys**</span><span class="sxs-lookup"><span data-stu-id="89ee8-134">**Annual salary enhancement**</span></span> | <span data-ttu-id="89ee8-135">Määrittää, lasketaanko **vuotuisen etuuspalkan** summa automaattisesti **työsuhteen lisätiedot** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="89ee8-135">Specifies whether to automatically calculate the **Annual benefit salary** amount in **Employment Benefit Details**.</span></span> <span data-ttu-id="89ee8-136">Se perustuu työntekijän **Kiinteän kompensaatiotaksan**, **Keskituntien** ja **Maksutiheyden** mukaan.</span><span class="sxs-lookup"><span data-stu-id="89ee8-136">It's based on the employee’s **Fixed compensation pay rate**, **Average hours**, and **Payment frequency**.</span></span></br></br><span data-ttu-id="89ee8-137">**Keskimääräinen työaika** x **kiinteä taksa** x **maksutiheys** (# maksukaudet) = **vuotuinen etuuspalkka**</span><span class="sxs-lookup"><span data-stu-id="89ee8-137">**Average hours** x **Fixed pay rate** x **Payment frequency** (# of pay periods) = **Annual benefit salary**</span></span> </br></br><span data-ttu-id="89ee8-138">Jos joku **Keskimääräiset tunnit**-, **kiinteä kompensaatiotaksa**- tai **maksutiheys** -kenttien arvo muuttuu, järjestelmä laskee työntekijän **vuotuisen etuuspalkan** automaattisesti uudelleen muuttuneiden arvojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="89ee8-138">If any of the values in the **Average hours**, **Fixed compensation pay rate**, or **Payment frequency** fields change, the system automatically recalculates the employee’s **Annual benefit salary** amount based on the changed values.</span></span> <span data-ttu-id="89ee8-139">Järjestelmä luo **päivämäärän voimaantulo** -tietueen, joka määrittää muutoksen tarkan päivämäärän ja ajan.</span><span class="sxs-lookup"><span data-stu-id="89ee8-139">The system creates a **Date effective** record to identify the exact date and time the change occurred.</span></span> <span data-ttu-id="89ee8-140">Voit tarvittaessa muokata **vuotuisen etuuspalkan** määrää manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="89ee8-140">You can manually edit the **Annual benefit salary** amount if necessary.</span></span> |
   | <span data-ttu-id="89ee8-141">**Elinkaaritapahtumat ovat käytössä**</span><span class="sxs-lookup"><span data-stu-id="89ee8-141">**Life events enabled**</span></span> | <span data-ttu-id="89ee8-142">Mahdollistaa elinkaaritapahtumat.</span><span class="sxs-lookup"><span data-stu-id="89ee8-142">Enables life events.</span></span> |
   | <span data-ttu-id="89ee8-143">**Piilota vanhat etulomakkeet**</span><span class="sxs-lookup"><span data-stu-id="89ee8-143">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="89ee8-144">Sallii vanhojen etuuslomakkeiden piilottamisen.</span><span class="sxs-lookup"><span data-stu-id="89ee8-144">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="89ee8-145">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="89ee8-145">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="89ee8-146">Määritä työntekijän itsepalveluparametrit</span><span class="sxs-lookup"><span data-stu-id="89ee8-146">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="89ee8-147">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="89ee8-147">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="89ee8-148">Määritä **Työntekijän itsepalvelu**-välilehdelle seuraavien kenttien arvot:</span><span class="sxs-lookup"><span data-stu-id="89ee8-148">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="89ee8-149">Kenttä</span><span class="sxs-lookup"><span data-stu-id="89ee8-149">Field</span></span> | <span data-ttu-id="89ee8-150">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="89ee8-150">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="89ee8-151">**Edun vahvistus**</span><span class="sxs-lookup"><span data-stu-id="89ee8-151">**Benefit verification**</span></span> | <span data-ttu-id="89ee8-152">Itsepalvelu-etujen aikana käytettävä tarkistusteksti kassalla.</span><span class="sxs-lookup"><span data-stu-id="89ee8-152">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="89ee8-153">**Valitse edustajat automaattisesti**</span><span class="sxs-lookup"><span data-stu-id="89ee8-153">**Auto select designees**</span></span> | <span data-ttu-id="89ee8-154">Määrittää, valitaanko huollettavat ja edunsaajat automaattisesti suunnitelmavaihtoehtojen kelpoisuuden perusteella.</span><span class="sxs-lookup"><span data-stu-id="89ee8-154">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="89ee8-155">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="89ee8-155">Select **Save**.</span></span>
