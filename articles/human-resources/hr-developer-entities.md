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
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087343"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="62e77-103">Common Data Service -yksiköt</span><span class="sxs-lookup"><span data-stu-id="62e77-103">Common Data Service entities</span></span>

<span data-ttu-id="62e77-104">Microsoft Dynamics 365 Human Resources käyttää Common Data Serviceä laajennettavuuden ja integroinnin skenaarioiden mahdollistamiseksi.</span><span class="sxs-lookup"><span data-stu-id="62e77-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="62e77-105">Lisätietoja Common Data Servicestä on kohdassa [Mikä on Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro) .</span><span class="sxs-lookup"><span data-stu-id="62e77-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="62e77-106">Seuraavat henkilöstöhallinnon resurssiyksiköt ovat käytettävissä Common Data Servicessä.</span><span class="sxs-lookup"><span data-stu-id="62e77-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="62e77-107">Etuyksiköt</span><span class="sxs-lookup"><span data-stu-id="62e77-107">Benefit entities</span></span>

| <span data-ttu-id="62e77-108">Nimi</span><span class="sxs-lookup"><span data-stu-id="62e77-108">Name</span></span> | <span data-ttu-id="62e77-109">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="62e77-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="62e77-110">Edun laskentatiheys</span><span class="sxs-lookup"><span data-stu-id="62e77-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="62e77-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="62e77-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="62e77-112">Edun laskennan toistuvuuden maksukausi</span><span class="sxs-lookup"><span data-stu-id="62e77-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="62e77-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="62e77-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="62e77-114">Edun laskentahinta</span><span class="sxs-lookup"><span data-stu-id="62e77-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="62e77-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="62e77-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="62e77-116">Edun laskentahinnan tiedot</span><span class="sxs-lookup"><span data-stu-id="62e77-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="62e77-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="62e77-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="62e77-118">Etuusvaihtoehto</span><span class="sxs-lookup"><span data-stu-id="62e77-118">Benefit Option</span></span> | <span data-ttu-id="62e77-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="62e77-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="62e77-120">Etusuunnitelma</span><span class="sxs-lookup"><span data-stu-id="62e77-120">Benefit Plan</span></span> | <span data-ttu-id="62e77-121">cdm_benefitplan (Ei käytössä mukautetulla kentän tuella)</span><span class="sxs-lookup"><span data-stu-id="62e77-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="62e77-122">Edun tyyppi</span><span class="sxs-lookup"><span data-stu-id="62e77-122">Benefit Type</span></span> | <span data-ttu-id="62e77-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="62e77-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="62e77-124">Liiketoimintaprosessin tehtävien yksiköt</span><span class="sxs-lookup"><span data-stu-id="62e77-124">Business process tasks entities</span></span>

| <span data-ttu-id="62e77-125">Nimi</span><span class="sxs-lookup"><span data-stu-id="62e77-125">Name</span></span> | <span data-ttu-id="62e77-126">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="62e77-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="62e77-127">Liiketoimintaprosessin kalenteri</span><span class="sxs-lookup"><span data-stu-id="62e77-127">Business Process Calendar</span></span> | <span data-ttu-id="62e77-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="62e77-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="62e77-129">Liiketoimintaprosessin ryhmämääritys</span><span class="sxs-lookup"><span data-stu-id="62e77-129">Business Process Group Assignment</span></span> | <span data-ttu-id="62e77-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="62e77-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="62e77-131">Liiketoimintaprosessikirjaston tehtäväryhmä</span><span class="sxs-lookup"><span data-stu-id="62e77-131">Business Process Library Task Group</span></span> | <span data-ttu-id="62e77-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="62e77-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="62e77-133">Liiketoimintaprosessin vaihe</span><span class="sxs-lookup"><span data-stu-id="62e77-133">Business Process Stage</span></span> | <span data-ttu-id="62e77-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="62e77-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="62e77-135">Tarkistusluettelomallin otsikko</span><span class="sxs-lookup"><span data-stu-id="62e77-135">Checklist Template Header</span></span> | <span data-ttu-id="62e77-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="62e77-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="62e77-137">Tarkistusluettelomallin tehtävä</span><span class="sxs-lookup"><span data-stu-id="62e77-137">Checklist Template Task</span></span> | <span data-ttu-id="62e77-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="62e77-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="62e77-139">Kompensaatioyksiköt</span><span class="sxs-lookup"><span data-stu-id="62e77-139">Compensation entities</span></span>

| <span data-ttu-id="62e77-140">Nimi</span><span class="sxs-lookup"><span data-stu-id="62e77-140">Name</span></span> | <span data-ttu-id="62e77-141">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="62e77-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="62e77-142">Kompensaation kiinteä suunnitelma</span><span class="sxs-lookup"><span data-stu-id="62e77-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="62e77-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="62e77-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="62e77-144">Kompensaatioruudukko</span><span class="sxs-lookup"><span data-stu-id="62e77-144">Compensation Grid</span></span> | <span data-ttu-id="62e77-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="62e77-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="62e77-146">Kompensaatiotaso</span><span class="sxs-lookup"><span data-stu-id="62e77-146">Compensation Level</span></span> | <span data-ttu-id="62e77-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="62e77-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="62e77-148">Kompensaation maksutiheys</span><span class="sxs-lookup"><span data-stu-id="62e77-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="62e77-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="62e77-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="62e77-150">Kompensaation viitepisteiden asetukset</span><span class="sxs-lookup"><span data-stu-id="62e77-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="62e77-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="62e77-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="62e77-152">Kompensaation viitepisteen asetusrivi</span><span class="sxs-lookup"><span data-stu-id="62e77-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="62e77-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="62e77-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="62e77-154">Kompensaatioalue</span><span class="sxs-lookup"><span data-stu-id="62e77-154">Compensation Region</span></span> | <span data-ttu-id="62e77-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="62e77-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="62e77-156">Kompensaatiorakenne</span><span class="sxs-lookup"><span data-stu-id="62e77-156">Compensation Structure</span></span> | <span data-ttu-id="62e77-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="62e77-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="62e77-158">Muuttuva kompensaatiosuunnitelma</span><span class="sxs-lookup"><span data-stu-id="62e77-158">Compensation Variable Plan</span></span> | <span data-ttu-id="62e77-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="62e77-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="62e77-160">Muuttuvan kompensaatiosuunnitelman taso</span><span class="sxs-lookup"><span data-stu-id="62e77-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="62e77-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="62e77-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="62e77-162">Muuttuvan kompensaatiosuunnitelman tyyppi</span><span class="sxs-lookup"><span data-stu-id="62e77-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="62e77-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="62e77-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="62e77-164">Kiinteä kompensaatiotapahtuma</span><span class="sxs-lookup"><span data-stu-id="62e77-164">Fixed Compensation Event</span></span> | <span data-ttu-id="62e77-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="62e77-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="62e77-166">Hyvityssääntö</span><span class="sxs-lookup"><span data-stu-id="62e77-166">Vesting Rule</span></span> | <span data-ttu-id="62e77-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="62e77-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="62e77-168">Työntekijän kiinteä kompensaatio</span><span class="sxs-lookup"><span data-stu-id="62e77-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="62e77-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="62e77-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="62e77-170">Organisaatioyksiköt</span><span class="sxs-lookup"><span data-stu-id="62e77-170">Organization entities</span></span>

| <span data-ttu-id="62e77-171">Nimi</span><span class="sxs-lookup"><span data-stu-id="62e77-171">Name</span></span> | <span data-ttu-id="62e77-172">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="62e77-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="62e77-173">Osasto</span><span class="sxs-lookup"><span data-stu-id="62e77-173">Department</span></span> | <span data-ttu-id="62e77-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="62e77-174">cdm_department</span></span> |
| <span data-ttu-id="62e77-175">Työsuhde</span><span class="sxs-lookup"><span data-stu-id="62e77-175">Employment</span></span> | <span data-ttu-id="62e77-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="62e77-176">cdm_employment</span></span> |
| <span data-ttu-id="62e77-177">Yritys </span><span class="sxs-lookup"><span data-stu-id="62e77-177">Company</span></span> | <span data-ttu-id="62e77-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="62e77-178">cdm_company</span></span> |
| <span data-ttu-id="62e77-179">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="62e77-179">Job</span></span> | <span data-ttu-id="62e77-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="62e77-180">cdm_job</span></span> |
| <span data-ttu-id="62e77-181">Työtehtävä</span><span class="sxs-lookup"><span data-stu-id="62e77-181">Job Function</span></span> | <span data-ttu-id="62e77-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="62e77-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="62e77-183">Toimi</span><span class="sxs-lookup"><span data-stu-id="62e77-183">Job Position</span></span> | <span data-ttu-id="62e77-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="62e77-184">cdm_jobposition</span></span> |
| <span data-ttu-id="62e77-185">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="62e77-185">Position Type</span></span> | <span data-ttu-id="62e77-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="62e77-186">cdm_positiontype</span></span> |
| <span data-ttu-id="62e77-187">Toimen työntekijän toimeksianto</span><span class="sxs-lookup"><span data-stu-id="62e77-187">Position Worker Assignment</span></span> | <span data-ttu-id="62e77-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="62e77-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="62e77-189">Työtyyppi</span><span class="sxs-lookup"><span data-stu-id="62e77-189">Job Type</span></span> | <span data-ttu-id="62e77-190">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="62e77-190">cdm_jobtype</span></span> |
| <span data-ttu-id="62e77-191">Kieli</span><span class="sxs-lookup"><span data-stu-id="62e77-191">Language</span></span> | <span data-ttu-id="62e77-192">cdm_language</span><span class="sxs-lookup"><span data-stu-id="62e77-192">cdm_language</span></span> |

## <a name="leave-and-absence-entities"></a><span data-ttu-id="62e77-193">Loman ja poissaolon kohteet</span><span class="sxs-lookup"><span data-stu-id="62e77-193">Leave and absence entities</span></span>

| <span data-ttu-id="62e77-194">Nimi</span><span class="sxs-lookup"><span data-stu-id="62e77-194">Name</span></span> | <span data-ttu-id="62e77-195">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="62e77-195">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="62e77-196">Loman pankkitapahtuma</span><span class="sxs-lookup"><span data-stu-id="62e77-196">Leave Bank Transaction</span></span> | <span data-ttu-id="62e77-197">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="62e77-197">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="62e77-198">Lomailmoittautuminen</span><span class="sxs-lookup"><span data-stu-id="62e77-198">Leave Enrollment</span></span> | <span data-ttu-id="62e77-199">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="62e77-199">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="62e77-200">Lomasuunnitelma</span><span class="sxs-lookup"><span data-stu-id="62e77-200">Leave Plan</span></span> | <span data-ttu-id="62e77-201">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="62e77-201">cdm_leaveplan</span></span> |
| <span data-ttu-id="62e77-202">Lomapyyntö</span><span class="sxs-lookup"><span data-stu-id="62e77-202">Leave Request</span></span> | <span data-ttu-id="62e77-203">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="62e77-203">cdm_leaverequest</span></span> |
| <span data-ttu-id="62e77-204">Lomapyynnön tiedot</span><span class="sxs-lookup"><span data-stu-id="62e77-204">Leave Request Detail</span></span> | <span data-ttu-id="62e77-205">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="62e77-205">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="62e77-206">Lomatyyppi</span><span class="sxs-lookup"><span data-stu-id="62e77-206">Leave Type</span></span> | <span data-ttu-id="62e77-207">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="62e77-207">cdm_leavetype</span></span> |
| <span data-ttu-id="62e77-208">Lomatyypin syykoodi</span><span class="sxs-lookup"><span data-stu-id="62e77-208">Leave Type Reason Code</span></span> | <span data-ttu-id="62e77-209">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="62e77-209">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="62e77-210">Palkanlaskentayksiköt</span><span class="sxs-lookup"><span data-stu-id="62e77-210">Payroll entities</span></span>

| <span data-ttu-id="62e77-211">Nimi</span><span class="sxs-lookup"><span data-stu-id="62e77-211">Name</span></span> | <span data-ttu-id="62e77-212">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="62e77-212">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="62e77-213">Maksujakso</span><span class="sxs-lookup"><span data-stu-id="62e77-213">Pay Cycle</span></span> | <span data-ttu-id="62e77-214">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="62e77-214">cdm_paycycle</span></span> |
| <span data-ttu-id="62e77-215">Maksukausi</span><span class="sxs-lookup"><span data-stu-id="62e77-215">Pay Period</span></span> | <span data-ttu-id="62e77-216">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="62e77-216">cdm_payperiod</span></span> |
| <span data-ttu-id="62e77-217">Palkanlaskennan ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="62e77-217">Payroll Earning Code</span></span> | <span data-ttu-id="62e77-218">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="62e77-218">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="62e77-219">Pankkitilisuoritukset</span><span class="sxs-lookup"><span data-stu-id="62e77-219">Bank Account Disbursement</span></span> | <span data-ttu-id="62e77-220">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="62e77-220">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="62e77-221">Verotusalue</span><span class="sxs-lookup"><span data-stu-id="62e77-221">Tax Region</span></span> | <span data-ttu-id="62e77-222">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="62e77-222">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="62e77-223">Työntekijäyksiköt</span><span class="sxs-lookup"><span data-stu-id="62e77-223">Worker entities</span></span>

| <span data-ttu-id="62e77-224">Nimi</span><span class="sxs-lookup"><span data-stu-id="62e77-224">Name</span></span> | <span data-ttu-id="62e77-225">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="62e77-225">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="62e77-226">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="62e77-226">Worker</span></span> | <span data-ttu-id="62e77-227">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="62e77-227">cdm_worker</span></span> |
| <span data-ttu-id="62e77-228">Työntekijän osoite</span><span class="sxs-lookup"><span data-stu-id="62e77-228">Worker Address</span></span> | <span data-ttu-id="62e77-229">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="62e77-229">cdm_workeraddress</span></span> |
| <span data-ttu-id="62e77-230">Työntekijän henkilötiedot</span><span class="sxs-lookup"><span data-stu-id="62e77-230">Worker Personal Detail</span></span> | <span data-ttu-id="62e77-231">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="62e77-231">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="62e77-232">Työntekijän tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="62e77-232">Worker Person Identification Number</span></span> | <span data-ttu-id="62e77-233">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="62e77-233">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="62e77-234">Työntekijän tunnustyyppi</span><span class="sxs-lookup"><span data-stu-id="62e77-234">Worker Person Identification Type</span></span> | <span data-ttu-id="62e77-235">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="62e77-235">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="62e77-236">Työkalenteri</span><span class="sxs-lookup"><span data-stu-id="62e77-236">Work Calendar</span></span> | <span data-ttu-id="62e77-237">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="62e77-237">cdm_workcalendar</span></span> |
| <span data-ttu-id="62e77-238">Työkalenteripäivämäärä</span><span class="sxs-lookup"><span data-stu-id="62e77-238">Work Calendar Day</span></span> | <span data-ttu-id="62e77-239">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="62e77-239">cdm_workcalendarday</span></span> |
| <span data-ttu-id="62e77-240">Työkalenterin lomapäivä</span><span class="sxs-lookup"><span data-stu-id="62e77-240">Work Calendar Holiday</span></span> |<span data-ttu-id="62e77-241">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="62e77-241">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="62e77-242">Työkalenterin lomapäivärivi</span><span class="sxs-lookup"><span data-stu-id="62e77-242">Work Calendar Holiday Line</span></span> | <span data-ttu-id="62e77-243">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="62e77-243">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="62e77-244">Työkalenterin aikaväli</span><span class="sxs-lookup"><span data-stu-id="62e77-244">Work Calendar Time Interval</span></span> | <span data-ttu-id="62e77-245">cdm_workcalendartimeinterval (Ei käytössä mukautetulla kentän tuella)</span><span class="sxs-lookup"><span data-stu-id="62e77-245">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="62e77-246">Työntekijän pankkitili</span><span class="sxs-lookup"><span data-stu-id="62e77-246">Worker Bank Account</span></span> | <span data-ttu-id="62e77-247">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="62e77-247">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="62e77-248">Työntekijän asetusyksiköt</span><span class="sxs-lookup"><span data-stu-id="62e77-248">Worker setup entities</span></span>

| <span data-ttu-id="62e77-249">Nimi</span><span class="sxs-lookup"><span data-stu-id="62e77-249">Name</span></span> | <span data-ttu-id="62e77-250">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="62e77-250">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="62e77-251">Sotaveteraanitila</span><span class="sxs-lookup"><span data-stu-id="62e77-251">Veteran Status</span></span> | <span data-ttu-id="62e77-252">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="62e77-252">cdm_veteranstatus</span></span> |
| <span data-ttu-id="62e77-253">Etninen tausta</span><span class="sxs-lookup"><span data-stu-id="62e77-253">Ethnic Origin</span></span> | <span data-ttu-id="62e77-254">HcmEthnicOrigin</span><span class="sxs-lookup"><span data-stu-id="62e77-254">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="62e77-255">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="62e77-255">Reason Code</span></span> | <span data-ttu-id="62e77-256">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="62e77-256">cdm_reasoncode</span></span> |
| <span data-ttu-id="62e77-257">Henkilötunnuksen myöntänyt virasto</span><span class="sxs-lookup"><span data-stu-id="62e77-257">Person Identification Issuing Agency</span></span> | <span data-ttu-id="62e77-258">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="62e77-258">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="62e77-259">Osaamisyksiköt</span><span class="sxs-lookup"><span data-stu-id="62e77-259">Competency entities</span></span>

| <span data-ttu-id="62e77-260">Nimi</span><span class="sxs-lookup"><span data-stu-id="62e77-260">Name</span></span> | <span data-ttu-id="62e77-261">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="62e77-261">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="62e77-262">Osaamisaluetyyppi</span><span class="sxs-lookup"><span data-stu-id="62e77-262">Skill Type</span></span> | <span data-ttu-id="62e77-263">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="62e77-263">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="62e77-264">Yksikkösuhteen mallit</span><span class="sxs-lookup"><span data-stu-id="62e77-264">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="62e77-265">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="62e77-265">Worker</span></span>

![Työntekijä](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="62e77-267">Työ ja työn sijainti</span><span class="sxs-lookup"><span data-stu-id="62e77-267">Job and Job Position</span></span>

![Työ ja työn sijainti](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="62e77-269">Edut</span><span class="sxs-lookup"><span data-stu-id="62e77-269">Benefits</span></span>

![Edut](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="62e77-271">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="62e77-271">Compensation</span></span>

![Kompensaatio](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="62e77-273">Poistu</span><span class="sxs-lookup"><span data-stu-id="62e77-273">Leave</span></span>

![Poistu](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="62e77-275">Työkalenteri</span><span class="sxs-lookup"><span data-stu-id="62e77-275">Work Calendar</span></span>

![Työkalenteri](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="62e77-277">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="62e77-277">See also</span></span>

[<span data-ttu-id="62e77-278">Valitse tietojen integraatioteknologia</span><span class="sxs-lookup"><span data-stu-id="62e77-278">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="62e77-279">Common Data Service -integroinnin määritys</span><span class="sxs-lookup"><span data-stu-id="62e77-279">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)