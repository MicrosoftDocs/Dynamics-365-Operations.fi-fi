---
title: Common Data Service -yksiköt
description: Microsoft Dynamics 365 Human Resources käyttää Common Data Serviceä laajennettavuuden ja integroinnin skenaarioiden mahdollistamiseksi.
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
ms.openlocfilehash: c8e0288da16829c04a9b97c0a52caa8bd27cddf8
ms.sourcegitcommit: fde8045ea49d0cf26d5e7ac5a0da5c0d3d69d5bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/26/2020
ms.locfileid: "3166495"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="eb625-103">Common Data Service -yksiköt</span><span class="sxs-lookup"><span data-stu-id="eb625-103">Common Data Service entities</span></span>

<span data-ttu-id="eb625-104">Microsoft Dynamics 365 Human Resources käyttää Common Data Serviceä laajennettavuuden ja integroinnin skenaarioiden mahdollistamiseksi.</span><span class="sxs-lookup"><span data-stu-id="eb625-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="eb625-105">Lisätietoja Common Data Servicestä on kohdassa [Mikä on Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro) .</span><span class="sxs-lookup"><span data-stu-id="eb625-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="eb625-106">Seuraavat henkilöstöhallinnon resurssiyksiköt ovat käytettävissä Common Data Servicessä.</span><span class="sxs-lookup"><span data-stu-id="eb625-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="eb625-107">Etuyksiköt</span><span class="sxs-lookup"><span data-stu-id="eb625-107">Benefit entities</span></span>

| <span data-ttu-id="eb625-108">Nimi</span><span class="sxs-lookup"><span data-stu-id="eb625-108">Name</span></span> | <span data-ttu-id="eb625-109">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="eb625-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eb625-110">Edun laskentatiheys</span><span class="sxs-lookup"><span data-stu-id="eb625-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="eb625-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="eb625-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="eb625-112">Edun laskennan toistuvuuden maksukausi</span><span class="sxs-lookup"><span data-stu-id="eb625-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="eb625-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="eb625-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="eb625-114">Edun laskentahinta</span><span class="sxs-lookup"><span data-stu-id="eb625-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="eb625-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="eb625-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="eb625-116">Edun laskentahinnan tiedot</span><span class="sxs-lookup"><span data-stu-id="eb625-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="eb625-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="eb625-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="eb625-118">Etuusvaihtoehto</span><span class="sxs-lookup"><span data-stu-id="eb625-118">Benefit Option</span></span> | <span data-ttu-id="eb625-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="eb625-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="eb625-120">Etusuunnitelma</span><span class="sxs-lookup"><span data-stu-id="eb625-120">Benefit Plan</span></span> | <span data-ttu-id="eb625-121">cdm_benefitplan (Ei käytössä mukautetulla kentän tuella)</span><span class="sxs-lookup"><span data-stu-id="eb625-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="eb625-122">Edun tyyppi</span><span class="sxs-lookup"><span data-stu-id="eb625-122">Benefit Type</span></span> | <span data-ttu-id="eb625-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="eb625-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="eb625-124">Liiketoimintaprosessin tehtävien yksiköt</span><span class="sxs-lookup"><span data-stu-id="eb625-124">Business process tasks entities</span></span>

| <span data-ttu-id="eb625-125">Nimi</span><span class="sxs-lookup"><span data-stu-id="eb625-125">Name</span></span> | <span data-ttu-id="eb625-126">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="eb625-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eb625-127">Liiketoimintaprosessin kalenteri</span><span class="sxs-lookup"><span data-stu-id="eb625-127">Business Process Calendar</span></span> | <span data-ttu-id="eb625-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="eb625-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="eb625-129">Liiketoimintaprosessin ryhmämääritys</span><span class="sxs-lookup"><span data-stu-id="eb625-129">Business Process Group Assignment</span></span> | <span data-ttu-id="eb625-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="eb625-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="eb625-131">Liiketoimintaprosessikirjaston tehtäväryhmä</span><span class="sxs-lookup"><span data-stu-id="eb625-131">Business Process Library Task Group</span></span> | <span data-ttu-id="eb625-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="eb625-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="eb625-133">Liiketoimintaprosessin vaihe</span><span class="sxs-lookup"><span data-stu-id="eb625-133">Business Process Stage</span></span> | <span data-ttu-id="eb625-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="eb625-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="eb625-135">Tarkistusluettelomallin otsikko</span><span class="sxs-lookup"><span data-stu-id="eb625-135">Checklist Template Header</span></span> | <span data-ttu-id="eb625-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="eb625-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="eb625-137">Tarkistusluettelomallin tehtävä</span><span class="sxs-lookup"><span data-stu-id="eb625-137">Checklist Template Task</span></span> | <span data-ttu-id="eb625-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="eb625-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="eb625-139">Kompensaatioyksiköt</span><span class="sxs-lookup"><span data-stu-id="eb625-139">Compensation entities</span></span>

| <span data-ttu-id="eb625-140">Nimi</span><span class="sxs-lookup"><span data-stu-id="eb625-140">Name</span></span> | <span data-ttu-id="eb625-141">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="eb625-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eb625-142">Kompensaation kiinteä suunnitelma</span><span class="sxs-lookup"><span data-stu-id="eb625-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="eb625-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="eb625-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="eb625-144">Kompensaatioruudukko</span><span class="sxs-lookup"><span data-stu-id="eb625-144">Compensation Grid</span></span> | <span data-ttu-id="eb625-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="eb625-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="eb625-146">Kompensaatiotaso</span><span class="sxs-lookup"><span data-stu-id="eb625-146">Compensation Level</span></span> | <span data-ttu-id="eb625-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="eb625-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="eb625-148">Kompensaation maksutiheys</span><span class="sxs-lookup"><span data-stu-id="eb625-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="eb625-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="eb625-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="eb625-150">Kompensaation viitepisteiden asetukset</span><span class="sxs-lookup"><span data-stu-id="eb625-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="eb625-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="eb625-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="eb625-152">Kompensaation viitepisteen asetusrivi</span><span class="sxs-lookup"><span data-stu-id="eb625-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="eb625-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="eb625-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="eb625-154">Kompensaatioalue</span><span class="sxs-lookup"><span data-stu-id="eb625-154">Compensation Region</span></span> | <span data-ttu-id="eb625-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="eb625-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="eb625-156">Kompensaatiorakenne</span><span class="sxs-lookup"><span data-stu-id="eb625-156">Compensation Structure</span></span> | <span data-ttu-id="eb625-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="eb625-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="eb625-158">Muuttuva kompensaatiosuunnitelma</span><span class="sxs-lookup"><span data-stu-id="eb625-158">Compensation Variable Plan</span></span> | <span data-ttu-id="eb625-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="eb625-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="eb625-160">Muuttuvan kompensaatiosuunnitelman taso</span><span class="sxs-lookup"><span data-stu-id="eb625-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="eb625-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="eb625-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="eb625-162">Muuttuvan kompensaatiosuunnitelman tyyppi</span><span class="sxs-lookup"><span data-stu-id="eb625-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="eb625-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="eb625-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="eb625-164">Kiinteä kompensaatiotapahtuma</span><span class="sxs-lookup"><span data-stu-id="eb625-164">Fixed Compensation Event</span></span> | <span data-ttu-id="eb625-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="eb625-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="eb625-166">Hyvityssääntö</span><span class="sxs-lookup"><span data-stu-id="eb625-166">Vesting Rule</span></span> | <span data-ttu-id="eb625-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="eb625-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="eb625-168">Työntekijän kiinteä kompensaatio</span><span class="sxs-lookup"><span data-stu-id="eb625-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="eb625-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="eb625-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="eb625-170">Organisaatioyksiköt</span><span class="sxs-lookup"><span data-stu-id="eb625-170">Organization entities</span></span>

| <span data-ttu-id="eb625-171">Nimi</span><span class="sxs-lookup"><span data-stu-id="eb625-171">Name</span></span> | <span data-ttu-id="eb625-172">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="eb625-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eb625-173">Osasto</span><span class="sxs-lookup"><span data-stu-id="eb625-173">Department</span></span> | <span data-ttu-id="eb625-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="eb625-174">cdm_department</span></span> |
| <span data-ttu-id="eb625-175">Työsuhde</span><span class="sxs-lookup"><span data-stu-id="eb625-175">Employment</span></span> | <span data-ttu-id="eb625-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="eb625-176">cdm_employment</span></span> |
| <span data-ttu-id="eb625-177">Yritys </span><span class="sxs-lookup"><span data-stu-id="eb625-177">Company</span></span> | <span data-ttu-id="eb625-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="eb625-178">cdm_company</span></span> |
| <span data-ttu-id="eb625-179">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="eb625-179">Job</span></span> | <span data-ttu-id="eb625-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="eb625-180">cdm_job</span></span> |
| <span data-ttu-id="eb625-181">Työtehtävä</span><span class="sxs-lookup"><span data-stu-id="eb625-181">Job Function</span></span> | <span data-ttu-id="eb625-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="eb625-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="eb625-183">Toimi</span><span class="sxs-lookup"><span data-stu-id="eb625-183">Job Position</span></span> | <span data-ttu-id="eb625-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="eb625-184">cdm_jobposition</span></span> |
| <span data-ttu-id="eb625-185">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="eb625-185">Position Type</span></span> | <span data-ttu-id="eb625-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="eb625-186">cdm_positiontype</span></span> |
| <span data-ttu-id="eb625-187">Toimen työntekijän toimeksianto</span><span class="sxs-lookup"><span data-stu-id="eb625-187">Position Worker Assignment</span></span> | <span data-ttu-id="eb625-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="eb625-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="eb625-189">Toimen dimensio</span><span class="sxs-lookup"><span data-stu-id="eb625-189">Job Position Dimension</span></span> | <span data-ttu-id="eb625-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="eb625-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="eb625-191">Työlaji</span><span class="sxs-lookup"><span data-stu-id="eb625-191">Job Type</span></span> | <span data-ttu-id="eb625-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="eb625-192">cdm_jobtype</span></span> |
| <span data-ttu-id="eb625-193">Kieli</span><span class="sxs-lookup"><span data-stu-id="eb625-193">Language</span></span> | <span data-ttu-id="eb625-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="eb625-194">cdm_language</span></span> |
| <span data-ttu-id="eb625-195">Tehtävänimike</span><span class="sxs-lookup"><span data-stu-id="eb625-195">Title</span></span> | <span data-ttu-id="eb625-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="eb625-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="eb625-197">Talous hallinnon dimensiot **Toimityypille**, **Toimen työntekijämääritykselle** ja **Työllisyydelle** tarjoavat yhdensuuntaisen integroinnin Common Data Service -järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="eb625-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="eb625-198">Taloushallinnon dimensioiden päivityksiä ei tällä hetkellä synkronoida Common Data Service -sovelluksesta Human Resources -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="eb625-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="eb625-199">Loman ja poissaolon kohteet</span><span class="sxs-lookup"><span data-stu-id="eb625-199">Leave and absence entities</span></span>

| <span data-ttu-id="eb625-200">Nimi</span><span class="sxs-lookup"><span data-stu-id="eb625-200">Name</span></span> | <span data-ttu-id="eb625-201">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="eb625-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eb625-202">Lomapankkitapahtuma</span><span class="sxs-lookup"><span data-stu-id="eb625-202">Leave Bank Transaction</span></span> | <span data-ttu-id="eb625-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="eb625-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="eb625-204">Lomailmoittautuminen</span><span class="sxs-lookup"><span data-stu-id="eb625-204">Leave Enrollment</span></span> | <span data-ttu-id="eb625-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="eb625-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="eb625-206">Lomasuunnitelma</span><span class="sxs-lookup"><span data-stu-id="eb625-206">Leave Plan</span></span> | <span data-ttu-id="eb625-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="eb625-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="eb625-208">Lomapyyntö</span><span class="sxs-lookup"><span data-stu-id="eb625-208">Leave Request</span></span> | <span data-ttu-id="eb625-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="eb625-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="eb625-210">Lomapyynnön tiedot</span><span class="sxs-lookup"><span data-stu-id="eb625-210">Leave Request Detail</span></span> | <span data-ttu-id="eb625-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="eb625-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="eb625-212">Lomatyyppi</span><span class="sxs-lookup"><span data-stu-id="eb625-212">Leave Type</span></span> | <span data-ttu-id="eb625-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="eb625-213">cdm_leavetype</span></span> |
| <span data-ttu-id="eb625-214">Lomatyypin syykoodi</span><span class="sxs-lookup"><span data-stu-id="eb625-214">Leave Type Reason Code</span></span> | <span data-ttu-id="eb625-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="eb625-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="eb625-216">Palkanlaskentayksiköt</span><span class="sxs-lookup"><span data-stu-id="eb625-216">Payroll entities</span></span>

| <span data-ttu-id="eb625-217">Nimi</span><span class="sxs-lookup"><span data-stu-id="eb625-217">Name</span></span> | <span data-ttu-id="eb625-218">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="eb625-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eb625-219">Maksujakso</span><span class="sxs-lookup"><span data-stu-id="eb625-219">Pay Cycle</span></span> | <span data-ttu-id="eb625-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="eb625-220">cdm_paycycle</span></span> |
| <span data-ttu-id="eb625-221">Maksukausi</span><span class="sxs-lookup"><span data-stu-id="eb625-221">Pay Period</span></span> | <span data-ttu-id="eb625-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="eb625-222">cdm_payperiod</span></span> |
| <span data-ttu-id="eb625-223">Palkanlaskennan ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="eb625-223">Payroll Earning Code</span></span> | <span data-ttu-id="eb625-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="eb625-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="eb625-225">Pankkitilisuoritukset</span><span class="sxs-lookup"><span data-stu-id="eb625-225">Bank Account Disbursement</span></span> | <span data-ttu-id="eb625-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="eb625-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="eb625-227">Verotusalue</span><span class="sxs-lookup"><span data-stu-id="eb625-227">Tax Region</span></span> | <span data-ttu-id="eb625-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="eb625-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="eb625-229">Työntekijäyksiköt</span><span class="sxs-lookup"><span data-stu-id="eb625-229">Worker entities</span></span>

| <span data-ttu-id="eb625-230">Nimi</span><span class="sxs-lookup"><span data-stu-id="eb625-230">Name</span></span> | <span data-ttu-id="eb625-231">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="eb625-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eb625-232">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="eb625-232">Worker</span></span> | <span data-ttu-id="eb625-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="eb625-233">cdm_worker</span></span> |
| <span data-ttu-id="eb625-234">Työntekijän osoite</span><span class="sxs-lookup"><span data-stu-id="eb625-234">Worker Address</span></span> | <span data-ttu-id="eb625-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="eb625-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="eb625-236">Työntekijän henkilötiedot</span><span class="sxs-lookup"><span data-stu-id="eb625-236">Worker Personal Detail</span></span> | <span data-ttu-id="eb625-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="eb625-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="eb625-238">Työntekijän tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="eb625-238">Worker Person Identification Number</span></span> | <span data-ttu-id="eb625-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="eb625-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="eb625-240">Työntekijän tunnustyyppi</span><span class="sxs-lookup"><span data-stu-id="eb625-240">Worker Person Identification Type</span></span> | <span data-ttu-id="eb625-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="eb625-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="eb625-242">Työkalenteri</span><span class="sxs-lookup"><span data-stu-id="eb625-242">Work Calendar</span></span> | <span data-ttu-id="eb625-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="eb625-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="eb625-244">Työkalenteripäivämäärä</span><span class="sxs-lookup"><span data-stu-id="eb625-244">Work Calendar Day</span></span> | <span data-ttu-id="eb625-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="eb625-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="eb625-246">Työkalenterin lomapäivä</span><span class="sxs-lookup"><span data-stu-id="eb625-246">Work Calendar Holiday</span></span> |<span data-ttu-id="eb625-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="eb625-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="eb625-248">Työkalenterin lomapäivärivi</span><span class="sxs-lookup"><span data-stu-id="eb625-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="eb625-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="eb625-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="eb625-250">Työkalenterin aikaväli</span><span class="sxs-lookup"><span data-stu-id="eb625-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="eb625-251">cdm_workcalendartimeinterval (Ei käytössä mukautetulla kentän tuella)</span><span class="sxs-lookup"><span data-stu-id="eb625-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="eb625-252">Työntekijän pankkitili</span><span class="sxs-lookup"><span data-stu-id="eb625-252">Worker Bank Account</span></span> | <span data-ttu-id="eb625-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="eb625-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="eb625-254">Työntekijän asetusyksiköt</span><span class="sxs-lookup"><span data-stu-id="eb625-254">Worker setup entities</span></span>

| <span data-ttu-id="eb625-255">Nimi</span><span class="sxs-lookup"><span data-stu-id="eb625-255">Name</span></span> | <span data-ttu-id="eb625-256">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="eb625-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eb625-257">Sotaveteraanitila</span><span class="sxs-lookup"><span data-stu-id="eb625-257">Veteran Status</span></span> | <span data-ttu-id="eb625-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="eb625-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="eb625-259">Etninen tausta</span><span class="sxs-lookup"><span data-stu-id="eb625-259">Ethnic Origin</span></span> | <span data-ttu-id="eb625-260">HcmEthnicOrigin</span><span class="sxs-lookup"><span data-stu-id="eb625-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="eb625-261">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="eb625-261">Reason Code</span></span> | <span data-ttu-id="eb625-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="eb625-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="eb625-263">Henkilötunnuksen myöntänyt virasto</span><span class="sxs-lookup"><span data-stu-id="eb625-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="eb625-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="eb625-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="eb625-265">Osaamisyksiköt</span><span class="sxs-lookup"><span data-stu-id="eb625-265">Competency entities</span></span>

| <span data-ttu-id="eb625-266">Nimi</span><span class="sxs-lookup"><span data-stu-id="eb625-266">Name</span></span> | <span data-ttu-id="eb625-267">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="eb625-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eb625-268">Osaamisaluetyyppi</span><span class="sxs-lookup"><span data-stu-id="eb625-268">Skill Type</span></span> | <span data-ttu-id="eb625-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="eb625-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="eb625-270">Yksikkösuhteen mallit</span><span class="sxs-lookup"><span data-stu-id="eb625-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="eb625-271">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="eb625-271">Worker</span></span>

![Työntekijä](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="eb625-273">Työ ja työn sijainti</span><span class="sxs-lookup"><span data-stu-id="eb625-273">Job and Job Position</span></span>

![Työ ja työn sijainti](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="eb625-275">Edut</span><span class="sxs-lookup"><span data-stu-id="eb625-275">Benefits</span></span>

![Edut](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="eb625-277">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="eb625-277">Compensation</span></span>

![Kompensaatio](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="eb625-279">Poistu</span><span class="sxs-lookup"><span data-stu-id="eb625-279">Leave</span></span>

![Poistu](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="eb625-281">Työkalenteri</span><span class="sxs-lookup"><span data-stu-id="eb625-281">Work Calendar</span></span>

![Työkalenteri](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="eb625-283">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="eb625-283">See also</span></span>

[<span data-ttu-id="eb625-284">Valitse tietojen integraatioteknologia</span><span class="sxs-lookup"><span data-stu-id="eb625-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="eb625-285">Common Data Service -integroinnin määritys</span><span class="sxs-lookup"><span data-stu-id="eb625-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
