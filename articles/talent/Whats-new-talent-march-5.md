---
title: Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (5. maaliskuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
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
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 115d7cd3d71eaddce2434cb1939c503d36bccdf8
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527287"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-5-2019"></a><span data-ttu-id="35548-103">Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (5. maaliskuuta 2019)</span><span class="sxs-lookup"><span data-stu-id="35548-103">What's new or changed in Dynamics 365 Talent (March 5, 2019)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="35548-104">Tässä ohjeaiheessa käsitellään Talentin uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="35548-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="35548-105">Attractin muutokset</span><span class="sxs-lookup"><span data-stu-id="35548-105">Changes in Attract</span></span>

### <a name="extending-option-sets-in-attract"></a><span data-ttu-id="35548-106">Attractin asetusjoukkojen laajentaminen</span><span class="sxs-lookup"><span data-stu-id="35548-106">Extending option sets in Attract</span></span>

<span data-ttu-id="35548-107">Attractissa on useita kenttiä, jotka ovat Common Data Servicen asetusjoukkoja.</span><span class="sxs-lookup"><span data-stu-id="35548-107">In Attract, there are multiple fields that are option sets within the Common Data Service.</span></span> <span data-ttu-id="35548-108">Asetusjoukkojen laajentamiseen on käytössä uusia asetuksia, kuten **Hylkäyssyy**-kenttä, **Työsuhteen tyyppi** -kenttä ja **Virkaikätyyppi**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="35548-108">New capabilities have been introduced to extend the option sets, beginning with the **Rejection** reason field, **Employment type** field, and **Seniority type** field.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35548-109">Työpaikan LinkedIniin julkaisemistoiminto edellyttää **Työn tiedot** -sivun **Työsuhteen tyyppi**- ja **Virkaikätyyppi**-kenttien käyttöä.</span><span class="sxs-lookup"><span data-stu-id="35548-109">The job posting to LinkedIn functionality requires the use of the **Employment type** and **Seniority type** fields on the **Job details** page.</span></span> <span data-ttu-id="35548-110">LinkedIn tukee näiden kenttien oletusarvoja, ja ne näkyvät, kun työpaikka julkaistaan.</span><span class="sxs-lookup"><span data-stu-id="35548-110">The default values in these fields are supported by LinkedIn and are displayed when the job is posted.</span></span> <span data-ttu-id="35548-111">Jos julkaiset työpaikkoja LinkedIniin ja muokkaat näiden kenttien nykyisiä asetusjoukon arvoja, työpaikka kyllä julkaistaan mutta LinkedIn ei näytä mukautettuja **Työsuhteen tyyppi**- ja **Virkaikätyyppi**-arvoja.</span><span class="sxs-lookup"><span data-stu-id="35548-111">If you are posting jobs to LinkedIn and you modify the existing option set values for these fields, the job will still post, but LinkedIn will not display the custom **Employment type** and **Seniority type** values.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="35548-112">Onboardingin muutokset</span><span class="sxs-lookup"><span data-stu-id="35548-112">Changes in Onboarding</span></span>

### <a name="private-preview-for-onboard-teams"></a><span data-ttu-id="35548-113">Onboard-ryhmien yksityinen esiversio</span><span class="sxs-lookup"><span data-stu-id="35548-113">Private preview for Onboard teams</span></span>
<span data-ttu-id="35548-114">Malleja on nyt helppo jakaa ja niitä voi käyttää kätevästi koko organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="35548-114">You can now easily share and collaborate on templates across your entire organization.</span></span> <span data-ttu-id="35548-115">Lisätietoja on kohdassa [Parhaiden käytäntöjen jakaminen organisaatiossa Onboard-ryhmien avulla](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span><span class="sxs-lookup"><span data-stu-id="35548-115">For more information, see [Share best practices across your organization using Onboard Teams](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span></span>

### <a name="private-preview-for-assignee-placeholders"></a><span data-ttu-id="35548-116">Vastuuhenkilöiden paikkamerkkien yksityinen esiversio</span><span class="sxs-lookup"><span data-stu-id="35548-116">Private preview for assignee placeholders</span></span>
<span data-ttu-id="35548-117">Voit täydentää malleja määrittämällä tehtäviä rooleille henkilöiden sijaan.</span><span class="sxs-lookup"><span data-stu-id="35548-117">You can enrich your templates by assigning activities to roles instead of individuals.</span></span> <span data-ttu-id="35548-118">Roolit määritetään sitten henkilöille oppaan luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="35548-118">Roles are then assigned to individuals at the time of guide creation.</span></span> <span data-ttu-id="35548-119">Lisätietoja on kohdassa [Oppaan hallinnan sujuvoittaminen määrittämällä tehtäviä rooleille](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span><span class="sxs-lookup"><span data-stu-id="35548-119">For more information, see [Streamline guide administration by assigning activities to roles](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="35548-120">Core HR:n muutokset</span><span class="sxs-lookup"><span data-stu-id="35548-120">Changes in Core HR</span></span>
<span data-ttu-id="35548-121">**Koontiversio 8.1.2178**</span><span class="sxs-lookup"><span data-stu-id="35548-121">**Build 8.1.2178**</span></span>

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a><span data-ttu-id="35548-122">Työnkulun määrittäminen hyväksymään työnkulku automaattisesti tai seuraamaan sitä, kun henkilöstöosasto tai linjaesimies lähettää tai päivittää poissaolopyyntöjä</span><span class="sxs-lookup"><span data-stu-id="35548-122">Configure workflow to auto-approve or follow workflow when an HR or line manager submits or updates time off requests</span></span>
<span data-ttu-id="35548-123">Lisätyillä uusilla työnkulun ehdoilla lomapyynnöt voidaan hyväksyä automaattisesti, jos lähettäjä on työntekijän esimies tai henkilöstöosasto.</span><span class="sxs-lookup"><span data-stu-id="35548-123">New workflow conditions have been added to allow for leave requests to be automatically approved if submitted by an employee’s manager or by HR.</span></span> <span data-ttu-id="35548-124">Yksi tapa hyväksyä työnkulku automaattisesti on ottaa automaattinen toiminto käyttöön työnkulun hyväksymisessä.</span><span class="sxs-lookup"><span data-stu-id="35548-124">One way to achieve this auto-approval on a workflow is to enable an automatic action on the workflow approval.</span></span>

<span data-ttu-id="35548-125">Seuraavat ehdot on lisätty:</span><span class="sxs-lookup"><span data-stu-id="35548-125">The conditions that have been added include:</span></span>

- <span data-ttu-id="35548-126">Lähettäjä – käytetään arvioimaan pyynnön työnkulkuun lähettäneen käyttäjän järjestelmän käyttäjätunnus.</span><span class="sxs-lookup"><span data-stu-id="35548-126">Submitted by - Used to evaluate the system user ID of the user who submitted the request to workflow.</span></span>
- <span data-ttu-id="35548-127">Lähetetty seuraavan puolesta – käytetään arvioimaan, onko lomapyyntö lähetetty pyyntöön liitetyn työntekijän puolesta.</span><span class="sxs-lookup"><span data-stu-id="35548-127">Submitted on behalf of - Used to evaluate if the leave request was submitted on behalf of the worker associated to the request.</span></span>
- <span data-ttu-id="35548-128">Henkilöstöosaston lähettämä – käytetään arvioimaan, onko pyynnön työnkulkuun lähettäneellä järjestelmän käyttäjällä henkilöstöhallinnon rooli.</span><span class="sxs-lookup"><span data-stu-id="35548-128">Submitted by human resources - Used to evaluate if the system user who submitted the request to workflow is in a Human Resources role.</span></span>
- <span data-ttu-id="35548-129">Lähettäjänä esimies – käytetään arvioimaan, lomapyynnön työnkulkuun lähettänyt käyttäjä pyyntöön liitetyn työntekijän linjahierarkian esimies.</span><span class="sxs-lookup"><span data-stu-id="35548-129">Submitted by manager - Used to evaluate if the user who submitted the leave request to workflow is a line hierarchy manager of the worker associated to the request.</span></span>

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a><span data-ttu-id="35548-130">Työntekijän kiinteän kompensaation ottaminen käyttöön tulevissa toimimäärityksissä</span><span class="sxs-lookup"><span data-stu-id="35548-130">Enable employee fixed compensation for future position assignments</span></span>
<span data-ttu-id="35548-131">Organisaatioon liittyvien työntekijöiden aloituspäivämäärä on tyypillisesti tulevaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="35548-131">It is typical for employees to join an organization with a future start date.</span></span> <span data-ttu-id="35548-132">Tämän muutoksen ansiosta voidaan määrittää kiinteä kompensaatio työntekijöille, joiden toimimääritykset ovat tulevaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="35548-132">This change enables defining fixed compensation for employees with future position assignments.</span></span>

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a><span data-ttu-id="35548-133">Toimen palkanlaskentakentät ovat tyhjiä toimea muokatessa</span><span class="sxs-lookup"><span data-stu-id="35548-133">Position Payroll fields are blank when editing the position</span></span>
<span data-ttu-id="35548-134">Tämän muutoksen ansiosta palkanlaskentakenttien arvot palautuvat nyt nykyisiin arvoihin, kun nykyisiin toimiin pyydetään muutoksia.</span><span class="sxs-lookup"><span data-stu-id="35548-134">With this change, when requesting changes to existing positions, the payroll fields will now default to the current values.</span></span>

### <a name="other-miscellaneous-bug-fixes"></a><span data-ttu-id="35548-135">Muita ohjelmakorjauksia</span><span class="sxs-lookup"><span data-stu-id="35548-135">Other miscellaneous bug fixes</span></span>
<span data-ttu-id="35548-136">Tässä julkaisussa on muita vähäisiä ohjelmakorjauksia.</span><span class="sxs-lookup"><span data-stu-id="35548-136">Other minor bug fixes are included with this release.</span></span>

### <a name="upgrade-to-common-data-service"></a><span data-ttu-id="35548-137">Päivitä versioon Common Data Service</span><span class="sxs-lookup"><span data-stu-id="35548-137">Upgrade to Common Data Service</span></span>
<span data-ttu-id="35548-138">Common Data Service -versioon tapahtuvan päivityksen määräajat lähestyvät nopeasti.</span><span class="sxs-lookup"><span data-stu-id="35548-138">Deadlines to upgrade to Common Data Service are quickly approaching.</span></span> <span data-ttu-id="35548-139">Kirjaudu sisään Power Apps-hallintakeskukseen ja tarkista, onko tietokantasi päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="35548-139">Sign in to the Power Apps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="35548-140">Lisätietoja määräajoista ja päivityksen vaiheista on kohdassa [Päivittäminen Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span><span class="sxs-lookup"><span data-stu-id="35548-140">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="35548-141">Tulossa pian</span><span class="sxs-lookup"><span data-stu-id="35548-141">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="35548-142">Kompensaation lisäsuojaus (kiinteä ja muuttuva)</span><span class="sxs-lookup"><span data-stu-id="35548-142">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="35548-143">Monissa organisaatioissa etuuspäälliköt voivat käyttää vain tiettyjä kompensaatiotietueita, kuten johtajien tai alueellisten työntekijöiden tietueita.</span><span class="sxs-lookup"><span data-stu-id="35548-143">In many organizations, compensation and benefits managers can only access certain compensation records, such as records for executives or regional-based employees.</span></span> <span data-ttu-id="35548-144">Tämä muutoksen ansiosta voit hallita ja ylläpitää organisaation erilaisten työntekijäryhmien kompensaatiosuunnitelmia.</span><span class="sxs-lookup"><span data-stu-id="35548-144">With this change, you can manage and maintain the compensation plans for different employee populations in the organization.</span></span> <span data-ttu-id="35548-145">Kiinteille ja muuttuville suunnitelmille voidaan määrittää käyttöoikeusrooleja, jotka määrittävät kyseisten suunnitelmien ja niihin liittyvien työntekijätietojen, kuten palkkatietojen tai bonustietueiden, käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="35548-145">Fixed and variable plans can be assigned security roles, which will determine the access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="35548-146">Vain roolit, joilla on tietty käyttöoikeus, voivat käsitellä kyseisten työntekijöiden kompensaatiota.</span><span class="sxs-lookup"><span data-stu-id="35548-146">Only the roles with the given access will be able to process compensation for those employees.</span></span>

###  <a name="platform-update-24-for-finance-and-operations"></a><span data-ttu-id="35548-147">Ympäristön päivitys 24 Finance and Operationsille</span><span class="sxs-lookup"><span data-stu-id="35548-147">Platform update 24 for Finance and Operations</span></span>
<span data-ttu-id="35548-148">Lisätietoja Finance and Operationsin Platform update 24:stä on kohdassa [Finance and Operations Platform update 24:n (maaliskuu 2019) uudet ja muuttuneet ominaisuudet](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="35548-148">For additional details about Platform update 24 for Finance and Operations, see [What's new or changed in Finance and Operations platform update 24 (March 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span></span>
