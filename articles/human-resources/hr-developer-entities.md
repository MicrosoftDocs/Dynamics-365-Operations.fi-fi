---
title: Dataverse-taulut
description: Microsoft Dynamics 365 Human Resources käyttää Dataverseä laajennettavuuden ja integroinnin skenaarioiden mahdollistamiseksi.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: 2f075a8e96af55b1363d2d51db377c5b25c38775
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112410"
---
# <a name="dataverse-tables"></a><span data-ttu-id="a6c3b-103">Dataverse-taulut</span><span class="sxs-lookup"><span data-stu-id="a6c3b-103">Dataverse tables</span></span>

<span data-ttu-id="a6c3b-104">Microsoft Dynamics 365 Human Resources käyttää Dataverseä laajennettavuuden ja integroinnin skenaarioiden mahdollistamiseksi.</span><span class="sxs-lookup"><span data-stu-id="a6c3b-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="a6c3b-105">Human Resources -yksiköt vastaavat Dataverse-tauluja.</span><span class="sxs-lookup"><span data-stu-id="a6c3b-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="a6c3b-106">Lisätietoja Dataversesta (aiemmin Common Data Service) ja terminologiapäivityksistä on kohdassa [Mikä on Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="a6c3b-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="a6c3b-107">Seuraavat Dataverse-taulut ovat käytössä Human Resources -yksiköiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="a6c3b-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="a6c3b-108">Etutaulut</span><span class="sxs-lookup"><span data-stu-id="a6c3b-108">Benefit tables</span></span>

| <span data-ttu-id="a6c3b-109">Nimi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-109">Name</span></span> | <span data-ttu-id="a6c3b-110">Taulu</span><span class="sxs-lookup"><span data-stu-id="a6c3b-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a6c3b-111">Edun laskentatiheys</span><span class="sxs-lookup"><span data-stu-id="a6c3b-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="a6c3b-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="a6c3b-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="a6c3b-113">Edun laskennan toistuvuuden maksukausi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="a6c3b-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="a6c3b-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="a6c3b-115">Edun laskentahinta</span><span class="sxs-lookup"><span data-stu-id="a6c3b-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="a6c3b-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="a6c3b-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="a6c3b-117">Edun laskentahinnan tiedot</span><span class="sxs-lookup"><span data-stu-id="a6c3b-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="a6c3b-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="a6c3b-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="a6c3b-119">Etuusvaihtoehto</span><span class="sxs-lookup"><span data-stu-id="a6c3b-119">Benefit Option</span></span> | <span data-ttu-id="a6c3b-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="a6c3b-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="a6c3b-121">Etusuunnitelma</span><span class="sxs-lookup"><span data-stu-id="a6c3b-121">Benefit Plan</span></span> | <span data-ttu-id="a6c3b-122">cdm_benefitplan (Ei käytössä mukautetulla kentän tuella)</span><span class="sxs-lookup"><span data-stu-id="a6c3b-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="a6c3b-123">Edun tyyppi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-123">Benefit Type</span></span> | <span data-ttu-id="a6c3b-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="a6c3b-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="a6c3b-125">Liiketoimintaprosessin tehtävien taulut</span><span class="sxs-lookup"><span data-stu-id="a6c3b-125">Business process tasks tables</span></span>

| <span data-ttu-id="a6c3b-126">Nimi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-126">Name</span></span> | <span data-ttu-id="a6c3b-127">Taulu</span><span class="sxs-lookup"><span data-stu-id="a6c3b-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a6c3b-128">Liiketoimintaprosessin kalenteri</span><span class="sxs-lookup"><span data-stu-id="a6c3b-128">Business Process Calendar</span></span> | <span data-ttu-id="a6c3b-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="a6c3b-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="a6c3b-130">Liiketoimintaprosessin ryhmämääritys</span><span class="sxs-lookup"><span data-stu-id="a6c3b-130">Business Process Group Assignment</span></span> | <span data-ttu-id="a6c3b-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="a6c3b-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="a6c3b-132">Liiketoimintaprosessikirjaston tehtäväryhmä</span><span class="sxs-lookup"><span data-stu-id="a6c3b-132">Business Process Library Task Group</span></span> | <span data-ttu-id="a6c3b-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="a6c3b-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="a6c3b-134">Liiketoimintaprosessin vaihe</span><span class="sxs-lookup"><span data-stu-id="a6c3b-134">Business Process Stage</span></span> | <span data-ttu-id="a6c3b-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="a6c3b-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="a6c3b-136">Tarkistusluettelomallin otsikko</span><span class="sxs-lookup"><span data-stu-id="a6c3b-136">Checklist Template Header</span></span> | <span data-ttu-id="a6c3b-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="a6c3b-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="a6c3b-138">Tarkistusluettelomallin tehtävä</span><span class="sxs-lookup"><span data-stu-id="a6c3b-138">Checklist Template Task</span></span> | <span data-ttu-id="a6c3b-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="a6c3b-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="a6c3b-140">Kompensaatiotaulut</span><span class="sxs-lookup"><span data-stu-id="a6c3b-140">Compensation tables</span></span>

| <span data-ttu-id="a6c3b-141">Nimi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-141">Name</span></span> | <span data-ttu-id="a6c3b-142">Taulu</span><span class="sxs-lookup"><span data-stu-id="a6c3b-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a6c3b-143">Kiinteä kompensaatiosuunnitelma</span><span class="sxs-lookup"><span data-stu-id="a6c3b-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="a6c3b-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="a6c3b-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="a6c3b-145">Kompensaatioruudukko</span><span class="sxs-lookup"><span data-stu-id="a6c3b-145">Compensation Grid</span></span> | <span data-ttu-id="a6c3b-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="a6c3b-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="a6c3b-147">Kompensaatiotaso</span><span class="sxs-lookup"><span data-stu-id="a6c3b-147">Compensation Level</span></span> | <span data-ttu-id="a6c3b-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="a6c3b-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="a6c3b-149">Kompensaation maksutiheys</span><span class="sxs-lookup"><span data-stu-id="a6c3b-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="a6c3b-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="a6c3b-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="a6c3b-151">Kompensaation viitepisteiden asetukset</span><span class="sxs-lookup"><span data-stu-id="a6c3b-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="a6c3b-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="a6c3b-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="a6c3b-153">Kompensaation viitepisteen asetusrivi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="a6c3b-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="a6c3b-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="a6c3b-155">Kompensaatioalue</span><span class="sxs-lookup"><span data-stu-id="a6c3b-155">Compensation Region</span></span> | <span data-ttu-id="a6c3b-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="a6c3b-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="a6c3b-157">Kompensaatiorakenne</span><span class="sxs-lookup"><span data-stu-id="a6c3b-157">Compensation Structure</span></span> | <span data-ttu-id="a6c3b-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="a6c3b-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="a6c3b-159">Muuttuva kompensaatiosuunnitelma</span><span class="sxs-lookup"><span data-stu-id="a6c3b-159">Compensation Variable Plan</span></span> | <span data-ttu-id="a6c3b-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="a6c3b-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="a6c3b-161">Muuttuvan kompensaatiosuunnitelman taso</span><span class="sxs-lookup"><span data-stu-id="a6c3b-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="a6c3b-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="a6c3b-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="a6c3b-163">Muuttuvan kompensaatiosuunnitelman tyyppi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="a6c3b-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="a6c3b-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="a6c3b-165">Kiinteä kompensaatiotapahtuma</span><span class="sxs-lookup"><span data-stu-id="a6c3b-165">Fixed Compensation Event</span></span> | <span data-ttu-id="a6c3b-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="a6c3b-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="a6c3b-167">Hyvityssääntö</span><span class="sxs-lookup"><span data-stu-id="a6c3b-167">Vesting Rule</span></span> | <span data-ttu-id="a6c3b-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="a6c3b-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="a6c3b-169">Työntekijän kiinteä kompensaatio</span><span class="sxs-lookup"><span data-stu-id="a6c3b-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="a6c3b-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="a6c3b-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="a6c3b-171">Organisaatiotaulut</span><span class="sxs-lookup"><span data-stu-id="a6c3b-171">Organization tables</span></span>

| <span data-ttu-id="a6c3b-172">Nimi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-172">Name</span></span> | <span data-ttu-id="a6c3b-173">Taulu</span><span class="sxs-lookup"><span data-stu-id="a6c3b-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a6c3b-174">Osasto</span><span class="sxs-lookup"><span data-stu-id="a6c3b-174">Department</span></span> | <span data-ttu-id="a6c3b-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="a6c3b-175">cdm_department</span></span> |
| <span data-ttu-id="a6c3b-176">Työsuhde</span><span class="sxs-lookup"><span data-stu-id="a6c3b-176">Employment</span></span> | <span data-ttu-id="a6c3b-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="a6c3b-177">cdm_employment</span></span> |
| <span data-ttu-id="a6c3b-178">Yhtiö</span><span class="sxs-lookup"><span data-stu-id="a6c3b-178">Company</span></span> | <span data-ttu-id="a6c3b-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="a6c3b-179">cdm_company</span></span> |
| <span data-ttu-id="a6c3b-180">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="a6c3b-180">Job</span></span> | <span data-ttu-id="a6c3b-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="a6c3b-181">cdm_job</span></span> |
| <span data-ttu-id="a6c3b-182">Työtehtävä</span><span class="sxs-lookup"><span data-stu-id="a6c3b-182">Job Function</span></span> | <span data-ttu-id="a6c3b-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="a6c3b-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="a6c3b-184">Toimi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-184">Job Position</span></span> | <span data-ttu-id="a6c3b-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="a6c3b-185">cdm_jobposition</span></span> |
| <span data-ttu-id="a6c3b-186">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-186">Position Type</span></span> | <span data-ttu-id="a6c3b-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="a6c3b-187">cdm_positiontype</span></span> |
| <span data-ttu-id="a6c3b-188">Toimen työntekijän toimeksianto</span><span class="sxs-lookup"><span data-stu-id="a6c3b-188">Position Worker Assignment</span></span> | <span data-ttu-id="a6c3b-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="a6c3b-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="a6c3b-190">Toimen dimensio</span><span class="sxs-lookup"><span data-stu-id="a6c3b-190">Job Position Dimension</span></span> | <span data-ttu-id="a6c3b-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="a6c3b-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="a6c3b-192">Työlaji</span><span class="sxs-lookup"><span data-stu-id="a6c3b-192">Job Type</span></span> | <span data-ttu-id="a6c3b-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="a6c3b-193">cdm_jobtype</span></span> |
| <span data-ttu-id="a6c3b-194">Kieli</span><span class="sxs-lookup"><span data-stu-id="a6c3b-194">Language</span></span> | <span data-ttu-id="a6c3b-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="a6c3b-195">cdm_language</span></span> |
| <span data-ttu-id="a6c3b-196">Tehtävänimike</span><span class="sxs-lookup"><span data-stu-id="a6c3b-196">Title</span></span> | <span data-ttu-id="a6c3b-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="a6c3b-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="a6c3b-198">Talous hallinnon dimensiot **Toimityypille**, **Toimen työntekijämääritykselle** ja **Työllisyydelle** tarjoavat yhdensuuntaisen integroinnin Dataverse -järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="a6c3b-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="a6c3b-199">Taloushallinnon dimensioiden päivityksiä ei tällä hetkellä synkronoida Dataverse -sovelluksesta Human Resources -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="a6c3b-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="a6c3b-200">Loma- ja poissaolotaulut</span><span class="sxs-lookup"><span data-stu-id="a6c3b-200">Leave and absence tables</span></span>

| <span data-ttu-id="a6c3b-201">Nimi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-201">Name</span></span> | <span data-ttu-id="a6c3b-202">Taulu</span><span class="sxs-lookup"><span data-stu-id="a6c3b-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a6c3b-203">Lomapankkitapahtuma</span><span class="sxs-lookup"><span data-stu-id="a6c3b-203">Leave Bank Transaction</span></span> | <span data-ttu-id="a6c3b-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="a6c3b-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="a6c3b-205">Lomarekisteröinti</span><span class="sxs-lookup"><span data-stu-id="a6c3b-205">Leave Enrollment</span></span> | <span data-ttu-id="a6c3b-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="a6c3b-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="a6c3b-207">Lomasuunnitelma</span><span class="sxs-lookup"><span data-stu-id="a6c3b-207">Leave Plan</span></span> | <span data-ttu-id="a6c3b-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="a6c3b-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="a6c3b-209">Lomapyyntö</span><span class="sxs-lookup"><span data-stu-id="a6c3b-209">Leave Request</span></span> | <span data-ttu-id="a6c3b-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="a6c3b-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="a6c3b-211">Lomapyynnön tiedot</span><span class="sxs-lookup"><span data-stu-id="a6c3b-211">Leave Request Detail</span></span> | <span data-ttu-id="a6c3b-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="a6c3b-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="a6c3b-213">Lomatyyppi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-213">Leave Type</span></span> | <span data-ttu-id="a6c3b-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="a6c3b-214">cdm_leavetype</span></span> |
| <span data-ttu-id="a6c3b-215">Lomatyypin syykoodi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-215">Leave Type Reason Code</span></span> | <span data-ttu-id="a6c3b-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="a6c3b-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="a6c3b-217">Palkanlaskentataulut</span><span class="sxs-lookup"><span data-stu-id="a6c3b-217">Payroll tables</span></span>

| <span data-ttu-id="a6c3b-218">Nimi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-218">Name</span></span> | <span data-ttu-id="a6c3b-219">Taulu</span><span class="sxs-lookup"><span data-stu-id="a6c3b-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a6c3b-220">Maksujakso</span><span class="sxs-lookup"><span data-stu-id="a6c3b-220">Pay Cycle</span></span> | <span data-ttu-id="a6c3b-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="a6c3b-221">cdm_paycycle</span></span> |
| <span data-ttu-id="a6c3b-222">Maksukausi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-222">Pay Period</span></span> | <span data-ttu-id="a6c3b-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="a6c3b-223">cdm_payperiod</span></span> |
| <span data-ttu-id="a6c3b-224">Palkkalaji</span><span class="sxs-lookup"><span data-stu-id="a6c3b-224">Payroll Earning Code</span></span> | <span data-ttu-id="a6c3b-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="a6c3b-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="a6c3b-226">Pankkitilisuoritukset</span><span class="sxs-lookup"><span data-stu-id="a6c3b-226">Bank Account Disbursement</span></span> | <span data-ttu-id="a6c3b-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="a6c3b-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="a6c3b-228">Verotusalue</span><span class="sxs-lookup"><span data-stu-id="a6c3b-228">Tax Region</span></span> | <span data-ttu-id="a6c3b-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="a6c3b-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="a6c3b-230">Työntekijätaulut</span><span class="sxs-lookup"><span data-stu-id="a6c3b-230">Worker tables</span></span>

| <span data-ttu-id="a6c3b-231">Nimi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-231">Name</span></span> | <span data-ttu-id="a6c3b-232">Taulu</span><span class="sxs-lookup"><span data-stu-id="a6c3b-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a6c3b-233">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="a6c3b-233">Worker</span></span> | <span data-ttu-id="a6c3b-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="a6c3b-234">cdm_worker</span></span> |
| <span data-ttu-id="a6c3b-235">Työntekijän osoite</span><span class="sxs-lookup"><span data-stu-id="a6c3b-235">Worker Address</span></span> | <span data-ttu-id="a6c3b-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="a6c3b-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="a6c3b-237">Työntekijän henkilötiedot</span><span class="sxs-lookup"><span data-stu-id="a6c3b-237">Worker Personal Detail</span></span> | <span data-ttu-id="a6c3b-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="a6c3b-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="a6c3b-239">Työntekijän tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="a6c3b-239">Worker Person Identification Number</span></span> | <span data-ttu-id="a6c3b-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="a6c3b-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="a6c3b-241">Työntekijän tunnustyyppi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-241">Worker Person Identification Type</span></span> | <span data-ttu-id="a6c3b-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="a6c3b-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="a6c3b-243">Työkalenteri</span><span class="sxs-lookup"><span data-stu-id="a6c3b-243">Work Calendar</span></span> | <span data-ttu-id="a6c3b-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="a6c3b-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="a6c3b-245">Työkalenteripäivämäärä</span><span class="sxs-lookup"><span data-stu-id="a6c3b-245">Work Calendar Day</span></span> | <span data-ttu-id="a6c3b-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="a6c3b-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="a6c3b-247">Työkalenterin lomapäivä</span><span class="sxs-lookup"><span data-stu-id="a6c3b-247">Work Calendar Holiday</span></span> |<span data-ttu-id="a6c3b-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="a6c3b-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="a6c3b-249">Työkalenterin lomapäivärivi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="a6c3b-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="a6c3b-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="a6c3b-251">Työkalenterin aikaväli</span><span class="sxs-lookup"><span data-stu-id="a6c3b-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="a6c3b-252">cdm_workcalendartimeinterval (Ei käytössä mukautetulla kentän tuella)</span><span class="sxs-lookup"><span data-stu-id="a6c3b-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="a6c3b-253">Työntekijän pankkitili</span><span class="sxs-lookup"><span data-stu-id="a6c3b-253">Worker Bank Account</span></span> | <span data-ttu-id="a6c3b-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="a6c3b-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="a6c3b-255">Työntekijän asetustaulut</span><span class="sxs-lookup"><span data-stu-id="a6c3b-255">Worker setup tables</span></span>

| <span data-ttu-id="a6c3b-256">Nimi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-256">Name</span></span> | <span data-ttu-id="a6c3b-257">Taulu</span><span class="sxs-lookup"><span data-stu-id="a6c3b-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a6c3b-258">Sotaveteraanitila</span><span class="sxs-lookup"><span data-stu-id="a6c3b-258">Veteran Status</span></span> | <span data-ttu-id="a6c3b-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="a6c3b-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="a6c3b-260">Etninen alkuperä</span><span class="sxs-lookup"><span data-stu-id="a6c3b-260">Ethnic Origin</span></span> | <span data-ttu-id="a6c3b-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="a6c3b-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="a6c3b-262">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-262">Reason Code</span></span> | <span data-ttu-id="a6c3b-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="a6c3b-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="a6c3b-264">Henkilötunnuksen myöntäjätaho</span><span class="sxs-lookup"><span data-stu-id="a6c3b-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="a6c3b-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="a6c3b-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="a6c3b-266">Pätevyystaulut</span><span class="sxs-lookup"><span data-stu-id="a6c3b-266">Competency tables</span></span>

| <span data-ttu-id="a6c3b-267">Nimi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-267">Name</span></span> | <span data-ttu-id="a6c3b-268">Taulu</span><span class="sxs-lookup"><span data-stu-id="a6c3b-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="a6c3b-269">Osaamisaluetyyppi</span><span class="sxs-lookup"><span data-stu-id="a6c3b-269">Skill Type</span></span> | <span data-ttu-id="a6c3b-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="a6c3b-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="a6c3b-271">Taulukkosuhteen mallit</span><span class="sxs-lookup"><span data-stu-id="a6c3b-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="a6c3b-272">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="a6c3b-272">Worker</span></span>

![Työntekijä](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="a6c3b-274">Työ ja työn sijainti</span><span class="sxs-lookup"><span data-stu-id="a6c3b-274">Job and Job Position</span></span>

![Työ ja työn sijainti](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="a6c3b-276">Edut</span><span class="sxs-lookup"><span data-stu-id="a6c3b-276">Benefits</span></span>

![Edut](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="a6c3b-278">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="a6c3b-278">Compensation</span></span>

![Kompensaatio](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="a6c3b-280">Poistu</span><span class="sxs-lookup"><span data-stu-id="a6c3b-280">Leave</span></span>

![Poistu](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="a6c3b-282">Työkalenteri</span><span class="sxs-lookup"><span data-stu-id="a6c3b-282">Work Calendar</span></span>

![Työkalenteri](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="a6c3b-284">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="a6c3b-284">See also</span></span>

[<span data-ttu-id="a6c3b-285">Valitse tietojen integraatioteknologia</span><span class="sxs-lookup"><span data-stu-id="a6c3b-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="a6c3b-286">Dataverse -integroinnin määritys</span><span class="sxs-lookup"><span data-stu-id="a6c3b-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="a6c3b-287">Määritä Dataverse -virtuaalitaulukot</span><span class="sxs-lookup"><span data-stu-id="a6c3b-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="a6c3b-288">Human Resourcesin virtuaalitaulut – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="a6c3b-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="a6c3b-289">Mikä on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="a6c3b-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="a6c3b-290">Terminologiapäivitykset</span><span class="sxs-lookup"><span data-stu-id="a6c3b-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
