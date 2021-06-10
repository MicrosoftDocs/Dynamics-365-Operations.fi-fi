---
title: Dataverse-taulut
description: Microsoft Dynamics 365 Human Resources käyttää Dataverseä laajennettavuuden ja integroinnin skenaarioiden mahdollistamiseksi.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 325bd8a9de07e3978ff6c513975a0e8db22854e0
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054353"
---
# <a name="dataverse-tables"></a><span data-ttu-id="a5a2e-103">Dataverse-taulut</span><span class="sxs-lookup"><span data-stu-id="a5a2e-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a5a2e-104">Microsoft Dynamics 365 Human Resources käyttää Dataverseä laajennettavuuden ja integroinnin skenaarioiden mahdollistamiseksi.</span><span class="sxs-lookup"><span data-stu-id="a5a2e-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="a5a2e-105">Human Resources -yksiköt vastaavat Dataverse-tauluja.</span><span class="sxs-lookup"><span data-stu-id="a5a2e-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="a5a2e-106">Lisätietoja Dataversesta (aiemmin Common Data Service) ja terminologiapäivityksistä on kohdassa [Mikä on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="a5a2e-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="a5a2e-107">Seuraavat Dataverse-taulut ovat käytössä Human Resources -yksiköiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="a5a2e-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="a5a2e-108">Etutaulut</span><span class="sxs-lookup"><span data-stu-id="a5a2e-108">Benefit tables</span></span>

| <span data-ttu-id="a5a2e-109">Nimi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-109">Name</span></span> | <span data-ttu-id="a5a2e-110">Taulu</span><span class="sxs-lookup"><span data-stu-id="a5a2e-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a5a2e-111">Edun laskentatiheys</span><span class="sxs-lookup"><span data-stu-id="a5a2e-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="a5a2e-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="a5a2e-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="a5a2e-113">Edun laskennan toistuvuuden maksukausi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="a5a2e-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="a5a2e-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="a5a2e-115">Edun laskentahinta</span><span class="sxs-lookup"><span data-stu-id="a5a2e-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="a5a2e-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="a5a2e-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="a5a2e-117">Edun laskentahinnan tiedot</span><span class="sxs-lookup"><span data-stu-id="a5a2e-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="a5a2e-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="a5a2e-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="a5a2e-119">Etuusvaihtoehto</span><span class="sxs-lookup"><span data-stu-id="a5a2e-119">Benefit Option</span></span> | <span data-ttu-id="a5a2e-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="a5a2e-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="a5a2e-121">Etusuunnitelma</span><span class="sxs-lookup"><span data-stu-id="a5a2e-121">Benefit Plan</span></span> | <span data-ttu-id="a5a2e-122">cdm_benefitplan (Ei käytössä mukautetulla kentän tuella)</span><span class="sxs-lookup"><span data-stu-id="a5a2e-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="a5a2e-123">Edun tyyppi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-123">Benefit Type</span></span> | <span data-ttu-id="a5a2e-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="a5a2e-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="a5a2e-125">Liiketoimintaprosessin tehtävien taulut</span><span class="sxs-lookup"><span data-stu-id="a5a2e-125">Business process tasks tables</span></span>

| <span data-ttu-id="a5a2e-126">Nimi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-126">Name</span></span> | <span data-ttu-id="a5a2e-127">Taulu</span><span class="sxs-lookup"><span data-stu-id="a5a2e-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a5a2e-128">Liiketoimintaprosessin kalenteri</span><span class="sxs-lookup"><span data-stu-id="a5a2e-128">Business Process Calendar</span></span> | <span data-ttu-id="a5a2e-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="a5a2e-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="a5a2e-130">Liiketoimintaprosessin ryhmämääritys</span><span class="sxs-lookup"><span data-stu-id="a5a2e-130">Business Process Group Assignment</span></span> | <span data-ttu-id="a5a2e-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="a5a2e-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="a5a2e-132">Liiketoimintaprosessikirjaston tehtäväryhmä</span><span class="sxs-lookup"><span data-stu-id="a5a2e-132">Business Process Library Task Group</span></span> | <span data-ttu-id="a5a2e-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="a5a2e-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="a5a2e-134">Liiketoimintaprosessin vaihe</span><span class="sxs-lookup"><span data-stu-id="a5a2e-134">Business Process Stage</span></span> | <span data-ttu-id="a5a2e-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="a5a2e-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="a5a2e-136">Tarkistusluettelomallin otsikko</span><span class="sxs-lookup"><span data-stu-id="a5a2e-136">Checklist Template Header</span></span> | <span data-ttu-id="a5a2e-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="a5a2e-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="a5a2e-138">Tarkistusluettelomallin tehtävä</span><span class="sxs-lookup"><span data-stu-id="a5a2e-138">Checklist Template Task</span></span> | <span data-ttu-id="a5a2e-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="a5a2e-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="a5a2e-140">Kompensaatiotaulut</span><span class="sxs-lookup"><span data-stu-id="a5a2e-140">Compensation tables</span></span>

| <span data-ttu-id="a5a2e-141">Nimi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-141">Name</span></span> | <span data-ttu-id="a5a2e-142">Taulu</span><span class="sxs-lookup"><span data-stu-id="a5a2e-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a5a2e-143">Kiinteä kompensaatiosuunnitelma</span><span class="sxs-lookup"><span data-stu-id="a5a2e-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="a5a2e-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="a5a2e-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="a5a2e-145">Kompensaatioruudukko</span><span class="sxs-lookup"><span data-stu-id="a5a2e-145">Compensation Grid</span></span> | <span data-ttu-id="a5a2e-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="a5a2e-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="a5a2e-147">Kompensaatiotaso</span><span class="sxs-lookup"><span data-stu-id="a5a2e-147">Compensation Level</span></span> | <span data-ttu-id="a5a2e-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="a5a2e-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="a5a2e-149">Kompensaation maksutiheys</span><span class="sxs-lookup"><span data-stu-id="a5a2e-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="a5a2e-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="a5a2e-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="a5a2e-151">Kompensaation viitepisteiden asetukset</span><span class="sxs-lookup"><span data-stu-id="a5a2e-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="a5a2e-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="a5a2e-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="a5a2e-153">Kompensaation viitepisteen asetusrivi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="a5a2e-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="a5a2e-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="a5a2e-155">Kompensaatioalue</span><span class="sxs-lookup"><span data-stu-id="a5a2e-155">Compensation Region</span></span> | <span data-ttu-id="a5a2e-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="a5a2e-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="a5a2e-157">Kompensaatiorakenne</span><span class="sxs-lookup"><span data-stu-id="a5a2e-157">Compensation Structure</span></span> | <span data-ttu-id="a5a2e-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="a5a2e-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="a5a2e-159">Muuttuva kompensaatiosuunnitelma</span><span class="sxs-lookup"><span data-stu-id="a5a2e-159">Compensation Variable Plan</span></span> | <span data-ttu-id="a5a2e-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="a5a2e-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="a5a2e-161">Muuttuvan kompensaatiosuunnitelman taso</span><span class="sxs-lookup"><span data-stu-id="a5a2e-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="a5a2e-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="a5a2e-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="a5a2e-163">Muuttuvan kompensaatiosuunnitelman tyyppi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="a5a2e-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="a5a2e-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="a5a2e-165">Kiinteä kompensaatiotapahtuma</span><span class="sxs-lookup"><span data-stu-id="a5a2e-165">Fixed Compensation Event</span></span> | <span data-ttu-id="a5a2e-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="a5a2e-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="a5a2e-167">Hyvityssääntö</span><span class="sxs-lookup"><span data-stu-id="a5a2e-167">Vesting Rule</span></span> | <span data-ttu-id="a5a2e-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="a5a2e-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="a5a2e-169">Työntekijän kiinteä kompensaatio</span><span class="sxs-lookup"><span data-stu-id="a5a2e-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="a5a2e-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="a5a2e-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="a5a2e-171">Organisaatiotaulut</span><span class="sxs-lookup"><span data-stu-id="a5a2e-171">Organization tables</span></span>

| <span data-ttu-id="a5a2e-172">Nimi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-172">Name</span></span> | <span data-ttu-id="a5a2e-173">Taulu</span><span class="sxs-lookup"><span data-stu-id="a5a2e-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a5a2e-174">Osasto</span><span class="sxs-lookup"><span data-stu-id="a5a2e-174">Department</span></span> | <span data-ttu-id="a5a2e-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="a5a2e-175">cdm_department</span></span> |
| <span data-ttu-id="a5a2e-176">Työsuhde</span><span class="sxs-lookup"><span data-stu-id="a5a2e-176">Employment</span></span> | <span data-ttu-id="a5a2e-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="a5a2e-177">cdm_employment</span></span> |
| <span data-ttu-id="a5a2e-178">Yhtiö</span><span class="sxs-lookup"><span data-stu-id="a5a2e-178">Company</span></span> | <span data-ttu-id="a5a2e-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="a5a2e-179">cdm_company</span></span> |
| <span data-ttu-id="a5a2e-180">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="a5a2e-180">Job</span></span> | <span data-ttu-id="a5a2e-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="a5a2e-181">cdm_job</span></span> |
| <span data-ttu-id="a5a2e-182">Työtehtävä</span><span class="sxs-lookup"><span data-stu-id="a5a2e-182">Job Function</span></span> | <span data-ttu-id="a5a2e-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="a5a2e-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="a5a2e-184">Toimi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-184">Job Position</span></span> | <span data-ttu-id="a5a2e-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="a5a2e-185">cdm_jobposition</span></span> |
| <span data-ttu-id="a5a2e-186">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-186">Position Type</span></span> | <span data-ttu-id="a5a2e-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="a5a2e-187">cdm_positiontype</span></span> |
| <span data-ttu-id="a5a2e-188">Toimen työntekijän toimeksianto</span><span class="sxs-lookup"><span data-stu-id="a5a2e-188">Position Worker Assignment</span></span> | <span data-ttu-id="a5a2e-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="a5a2e-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="a5a2e-190">Toimen dimensio</span><span class="sxs-lookup"><span data-stu-id="a5a2e-190">Job Position Dimension</span></span> | <span data-ttu-id="a5a2e-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="a5a2e-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="a5a2e-192">Työlaji</span><span class="sxs-lookup"><span data-stu-id="a5a2e-192">Job Type</span></span> | <span data-ttu-id="a5a2e-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="a5a2e-193">cdm_jobtype</span></span> |
| <span data-ttu-id="a5a2e-194">Kieli</span><span class="sxs-lookup"><span data-stu-id="a5a2e-194">Language</span></span> | <span data-ttu-id="a5a2e-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="a5a2e-195">cdm_language</span></span> |
| <span data-ttu-id="a5a2e-196">Tehtävänimike</span><span class="sxs-lookup"><span data-stu-id="a5a2e-196">Title</span></span> | <span data-ttu-id="a5a2e-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="a5a2e-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="a5a2e-198">Talous hallinnon dimensiot **Toimityypille**, **Toimen työntekijämääritykselle** ja **Työllisyydelle** tarjoavat yhdensuuntaisen integroinnin Dataverse -järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="a5a2e-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="a5a2e-199">Taloushallinnon dimensioiden päivityksiä ei tällä hetkellä synkronoida Dataverse -sovelluksesta Human Resources -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="a5a2e-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="a5a2e-200">Loma- ja poissaolotaulut</span><span class="sxs-lookup"><span data-stu-id="a5a2e-200">Leave and absence tables</span></span>

| <span data-ttu-id="a5a2e-201">Nimi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-201">Name</span></span> | <span data-ttu-id="a5a2e-202">Taulu</span><span class="sxs-lookup"><span data-stu-id="a5a2e-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a5a2e-203">Lomapankkitapahtuma</span><span class="sxs-lookup"><span data-stu-id="a5a2e-203">Leave Bank Transaction</span></span> | <span data-ttu-id="a5a2e-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="a5a2e-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="a5a2e-205">Lomarekisteröinti</span><span class="sxs-lookup"><span data-stu-id="a5a2e-205">Leave Enrollment</span></span> | <span data-ttu-id="a5a2e-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="a5a2e-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="a5a2e-207">Lomasuunnitelma</span><span class="sxs-lookup"><span data-stu-id="a5a2e-207">Leave Plan</span></span> | <span data-ttu-id="a5a2e-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="a5a2e-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="a5a2e-209">Lomapyyntö</span><span class="sxs-lookup"><span data-stu-id="a5a2e-209">Leave Request</span></span> | <span data-ttu-id="a5a2e-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="a5a2e-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="a5a2e-211">Lomapyynnön tiedot</span><span class="sxs-lookup"><span data-stu-id="a5a2e-211">Leave Request Detail</span></span> | <span data-ttu-id="a5a2e-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="a5a2e-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="a5a2e-213">Lomatyyppi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-213">Leave Type</span></span> | <span data-ttu-id="a5a2e-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="a5a2e-214">cdm_leavetype</span></span> |
| <span data-ttu-id="a5a2e-215">Lomatyypin syykoodi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-215">Leave Type Reason Code</span></span> | <span data-ttu-id="a5a2e-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="a5a2e-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="a5a2e-217">Palkanlaskentataulut</span><span class="sxs-lookup"><span data-stu-id="a5a2e-217">Payroll tables</span></span>

| <span data-ttu-id="a5a2e-218">Nimi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-218">Name</span></span> | <span data-ttu-id="a5a2e-219">Taulu</span><span class="sxs-lookup"><span data-stu-id="a5a2e-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a5a2e-220">Maksujakso</span><span class="sxs-lookup"><span data-stu-id="a5a2e-220">Pay Cycle</span></span> | <span data-ttu-id="a5a2e-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="a5a2e-221">cdm_paycycle</span></span> |
| <span data-ttu-id="a5a2e-222">Maksukausi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-222">Pay Period</span></span> | <span data-ttu-id="a5a2e-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="a5a2e-223">cdm_payperiod</span></span> |
| <span data-ttu-id="a5a2e-224">Palkkalaji</span><span class="sxs-lookup"><span data-stu-id="a5a2e-224">Payroll Earning Code</span></span> | <span data-ttu-id="a5a2e-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="a5a2e-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="a5a2e-226">Pankkitilisuoritukset</span><span class="sxs-lookup"><span data-stu-id="a5a2e-226">Bank Account Disbursement</span></span> | <span data-ttu-id="a5a2e-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="a5a2e-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="a5a2e-228">Verotusalue</span><span class="sxs-lookup"><span data-stu-id="a5a2e-228">Tax Region</span></span> | <span data-ttu-id="a5a2e-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="a5a2e-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="a5a2e-230">Työntekijätaulut</span><span class="sxs-lookup"><span data-stu-id="a5a2e-230">Worker tables</span></span>

| <span data-ttu-id="a5a2e-231">Nimi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-231">Name</span></span> | <span data-ttu-id="a5a2e-232">Taulu</span><span class="sxs-lookup"><span data-stu-id="a5a2e-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a5a2e-233">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="a5a2e-233">Worker</span></span> | <span data-ttu-id="a5a2e-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="a5a2e-234">cdm_worker</span></span> |
| <span data-ttu-id="a5a2e-235">Työntekijän osoite</span><span class="sxs-lookup"><span data-stu-id="a5a2e-235">Worker Address</span></span> | <span data-ttu-id="a5a2e-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="a5a2e-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="a5a2e-237">Työntekijän henkilötiedot</span><span class="sxs-lookup"><span data-stu-id="a5a2e-237">Worker Personal Detail</span></span> | <span data-ttu-id="a5a2e-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="a5a2e-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="a5a2e-239">Työntekijän tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="a5a2e-239">Worker Person Identification Number</span></span> | <span data-ttu-id="a5a2e-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="a5a2e-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="a5a2e-241">Työntekijän tunnustyyppi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-241">Worker Person Identification Type</span></span> | <span data-ttu-id="a5a2e-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="a5a2e-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="a5a2e-243">Työkalenteri</span><span class="sxs-lookup"><span data-stu-id="a5a2e-243">Work Calendar</span></span> | <span data-ttu-id="a5a2e-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="a5a2e-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="a5a2e-245">Työkalenteripäivämäärä</span><span class="sxs-lookup"><span data-stu-id="a5a2e-245">Work Calendar Day</span></span> | <span data-ttu-id="a5a2e-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="a5a2e-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="a5a2e-247">Työkalenterin lomapäivä</span><span class="sxs-lookup"><span data-stu-id="a5a2e-247">Work Calendar Holiday</span></span> |<span data-ttu-id="a5a2e-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="a5a2e-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="a5a2e-249">Työkalenterin lomapäivärivi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="a5a2e-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="a5a2e-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="a5a2e-251">Työkalenterin aikaväli</span><span class="sxs-lookup"><span data-stu-id="a5a2e-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="a5a2e-252">cdm_workcalendartimeinterval (Ei käytössä mukautetulla kentän tuella)</span><span class="sxs-lookup"><span data-stu-id="a5a2e-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="a5a2e-253">Työntekijän pankkitili</span><span class="sxs-lookup"><span data-stu-id="a5a2e-253">Worker Bank Account</span></span> | <span data-ttu-id="a5a2e-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="a5a2e-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="a5a2e-255">Työntekijän asetustaulut</span><span class="sxs-lookup"><span data-stu-id="a5a2e-255">Worker setup tables</span></span>

| <span data-ttu-id="a5a2e-256">Nimi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-256">Name</span></span> | <span data-ttu-id="a5a2e-257">Taulu</span><span class="sxs-lookup"><span data-stu-id="a5a2e-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a5a2e-258">Sotaveteraanitila</span><span class="sxs-lookup"><span data-stu-id="a5a2e-258">Veteran Status</span></span> | <span data-ttu-id="a5a2e-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="a5a2e-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="a5a2e-260">Etninen alkuperä</span><span class="sxs-lookup"><span data-stu-id="a5a2e-260">Ethnic Origin</span></span> | <span data-ttu-id="a5a2e-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="a5a2e-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="a5a2e-262">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-262">Reason Code</span></span> | <span data-ttu-id="a5a2e-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="a5a2e-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="a5a2e-264">Henkilötunnuksen myöntäjätaho</span><span class="sxs-lookup"><span data-stu-id="a5a2e-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="a5a2e-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="a5a2e-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="a5a2e-266">Pätevyystaulut</span><span class="sxs-lookup"><span data-stu-id="a5a2e-266">Competency tables</span></span>

| <span data-ttu-id="a5a2e-267">Nimi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-267">Name</span></span> | <span data-ttu-id="a5a2e-268">Taulu</span><span class="sxs-lookup"><span data-stu-id="a5a2e-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a5a2e-269">Osaamisaluetyyppi</span><span class="sxs-lookup"><span data-stu-id="a5a2e-269">Skill Type</span></span> | <span data-ttu-id="a5a2e-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="a5a2e-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="a5a2e-271">Taulukkosuhteen mallit</span><span class="sxs-lookup"><span data-stu-id="a5a2e-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="a5a2e-272">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="a5a2e-272">Worker</span></span>

![Työntekijä](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="a5a2e-274">Työ ja työn sijainti</span><span class="sxs-lookup"><span data-stu-id="a5a2e-274">Job and Job Position</span></span>

![Työ ja työn sijainti](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="a5a2e-276">Edut</span><span class="sxs-lookup"><span data-stu-id="a5a2e-276">Benefits</span></span>

![Edut](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="a5a2e-278">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="a5a2e-278">Compensation</span></span>

![Kompensaatio](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="a5a2e-280">Poistu</span><span class="sxs-lookup"><span data-stu-id="a5a2e-280">Leave</span></span>

![Poistu](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="a5a2e-282">Työkalenteri</span><span class="sxs-lookup"><span data-stu-id="a5a2e-282">Work Calendar</span></span>

![Työkalenteri](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="a5a2e-284">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="a5a2e-284">See also</span></span>

[<span data-ttu-id="a5a2e-285">Valitse tietojen integraatioteknologia</span><span class="sxs-lookup"><span data-stu-id="a5a2e-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="a5a2e-286">Dataverse -integroinnin määritys</span><span class="sxs-lookup"><span data-stu-id="a5a2e-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="a5a2e-287">Määritä Dataverse -virtuaalitaulukot</span><span class="sxs-lookup"><span data-stu-id="a5a2e-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="a5a2e-288">Human Resourcesin virtuaalitaulut – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="a5a2e-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="a5a2e-289">Mikä on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="a5a2e-289">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="a5a2e-290">Terminologiapäivitykset</span><span class="sxs-lookup"><span data-stu-id="a5a2e-290">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]