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
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530003"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="4b62c-103">Common Data Service -yksiköt</span><span class="sxs-lookup"><span data-stu-id="4b62c-103">Common Data Service entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4b62c-104">Microsoft Dynamics 365 Human Resources käyttää Common Data Serviceä laajennettavuuden ja integroinnin skenaarioiden mahdollistamiseksi.</span><span class="sxs-lookup"><span data-stu-id="4b62c-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="4b62c-105">Lisätietoja Common Data Servicestä on kohdassa [Mikä on Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro) .</span><span class="sxs-lookup"><span data-stu-id="4b62c-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="4b62c-106">Seuraavat henkilöstöhallinnon resurssiyksiköt ovat käytettävissä Common Data Servicessä.</span><span class="sxs-lookup"><span data-stu-id="4b62c-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="4b62c-107">Etuyksiköt</span><span class="sxs-lookup"><span data-stu-id="4b62c-107">Benefit entities</span></span>

| <span data-ttu-id="4b62c-108">Nimi</span><span class="sxs-lookup"><span data-stu-id="4b62c-108">Name</span></span> | <span data-ttu-id="4b62c-109">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="4b62c-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4b62c-110">Edun laskentatiheys</span><span class="sxs-lookup"><span data-stu-id="4b62c-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="4b62c-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="4b62c-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="4b62c-112">Edun laskennan toistuvuuden maksukausi</span><span class="sxs-lookup"><span data-stu-id="4b62c-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="4b62c-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="4b62c-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="4b62c-114">Edun laskentahinta</span><span class="sxs-lookup"><span data-stu-id="4b62c-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="4b62c-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="4b62c-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="4b62c-116">Edun laskentahinnan tiedot</span><span class="sxs-lookup"><span data-stu-id="4b62c-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="4b62c-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="4b62c-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="4b62c-118">Etuusvaihtoehto</span><span class="sxs-lookup"><span data-stu-id="4b62c-118">Benefit Option</span></span> | <span data-ttu-id="4b62c-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="4b62c-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="4b62c-120">Etusuunnitelma</span><span class="sxs-lookup"><span data-stu-id="4b62c-120">Benefit Plan</span></span> | <span data-ttu-id="4b62c-121">cdm_benefitplan (Ei käytössä mukautetulla kentän tuella)</span><span class="sxs-lookup"><span data-stu-id="4b62c-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="4b62c-122">Edun tyyppi</span><span class="sxs-lookup"><span data-stu-id="4b62c-122">Benefit Type</span></span> | <span data-ttu-id="4b62c-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="4b62c-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="4b62c-124">Liiketoimintaprosessin tehtävien yksiköt</span><span class="sxs-lookup"><span data-stu-id="4b62c-124">Business process tasks entities</span></span>

| <span data-ttu-id="4b62c-125">Nimi</span><span class="sxs-lookup"><span data-stu-id="4b62c-125">Name</span></span> | <span data-ttu-id="4b62c-126">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="4b62c-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4b62c-127">Liiketoimintaprosessin kalenteri</span><span class="sxs-lookup"><span data-stu-id="4b62c-127">Business Process Calendar</span></span> | <span data-ttu-id="4b62c-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="4b62c-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="4b62c-129">Liiketoimintaprosessin ryhmämääritys</span><span class="sxs-lookup"><span data-stu-id="4b62c-129">Business Process Group Assignment</span></span> | <span data-ttu-id="4b62c-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="4b62c-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="4b62c-131">Liiketoimintaprosessikirjaston tehtäväryhmä</span><span class="sxs-lookup"><span data-stu-id="4b62c-131">Business Process Library Task Group</span></span> | <span data-ttu-id="4b62c-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="4b62c-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="4b62c-133">Liiketoimintaprosessin vaihe</span><span class="sxs-lookup"><span data-stu-id="4b62c-133">Business Process Stage</span></span> | <span data-ttu-id="4b62c-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="4b62c-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="4b62c-135">Tarkistusluettelomallin otsikko</span><span class="sxs-lookup"><span data-stu-id="4b62c-135">Checklist Template Header</span></span> | <span data-ttu-id="4b62c-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="4b62c-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="4b62c-137">Tarkistusluettelomallin tehtävä</span><span class="sxs-lookup"><span data-stu-id="4b62c-137">Checklist Template Task</span></span> | <span data-ttu-id="4b62c-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="4b62c-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="4b62c-139">Kompensaatioyksiköt</span><span class="sxs-lookup"><span data-stu-id="4b62c-139">Compensation entities</span></span>

| <span data-ttu-id="4b62c-140">Nimi</span><span class="sxs-lookup"><span data-stu-id="4b62c-140">Name</span></span> | <span data-ttu-id="4b62c-141">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="4b62c-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4b62c-142">Kompensaation kiinteä suunnitelma</span><span class="sxs-lookup"><span data-stu-id="4b62c-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="4b62c-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="4b62c-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="4b62c-144">Kompensaatioruudukko</span><span class="sxs-lookup"><span data-stu-id="4b62c-144">Compensation Grid</span></span> | <span data-ttu-id="4b62c-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="4b62c-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="4b62c-146">Kompensaatiotaso</span><span class="sxs-lookup"><span data-stu-id="4b62c-146">Compensation Level</span></span> | <span data-ttu-id="4b62c-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="4b62c-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="4b62c-148">Kompensaation maksutiheys</span><span class="sxs-lookup"><span data-stu-id="4b62c-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="4b62c-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="4b62c-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="4b62c-150">Kompensaation viitepisteiden asetukset</span><span class="sxs-lookup"><span data-stu-id="4b62c-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="4b62c-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="4b62c-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="4b62c-152">Kompensaation viitepisteen asetusrivi</span><span class="sxs-lookup"><span data-stu-id="4b62c-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="4b62c-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="4b62c-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="4b62c-154">Kompensaatioalue</span><span class="sxs-lookup"><span data-stu-id="4b62c-154">Compensation Region</span></span> | <span data-ttu-id="4b62c-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="4b62c-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="4b62c-156">Kompensaatiorakenne</span><span class="sxs-lookup"><span data-stu-id="4b62c-156">Compensation Structure</span></span> | <span data-ttu-id="4b62c-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="4b62c-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="4b62c-158">Muuttuva kompensaatiosuunnitelma</span><span class="sxs-lookup"><span data-stu-id="4b62c-158">Compensation Variable Plan</span></span> | <span data-ttu-id="4b62c-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="4b62c-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="4b62c-160">Muuttuvan kompensaatiosuunnitelman taso</span><span class="sxs-lookup"><span data-stu-id="4b62c-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="4b62c-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="4b62c-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="4b62c-162">Muuttuvan kompensaatiosuunnitelman tyyppi</span><span class="sxs-lookup"><span data-stu-id="4b62c-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="4b62c-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="4b62c-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="4b62c-164">Kiinteä kompensaatiotapahtuma</span><span class="sxs-lookup"><span data-stu-id="4b62c-164">Fixed Compensation Event</span></span> | <span data-ttu-id="4b62c-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="4b62c-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="4b62c-166">Hyvityssääntö</span><span class="sxs-lookup"><span data-stu-id="4b62c-166">Vesting Rule</span></span> | <span data-ttu-id="4b62c-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="4b62c-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="4b62c-168">Työntekijän kiinteä kompensaatio</span><span class="sxs-lookup"><span data-stu-id="4b62c-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="4b62c-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="4b62c-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="4b62c-170">Organisaatioyksiköt</span><span class="sxs-lookup"><span data-stu-id="4b62c-170">Organization entities</span></span>

| <span data-ttu-id="4b62c-171">Nimi</span><span class="sxs-lookup"><span data-stu-id="4b62c-171">Name</span></span> | <span data-ttu-id="4b62c-172">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="4b62c-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4b62c-173">Osasto</span><span class="sxs-lookup"><span data-stu-id="4b62c-173">Department</span></span> | <span data-ttu-id="4b62c-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="4b62c-174">cdm_department</span></span> |
| <span data-ttu-id="4b62c-175">Työsuhde</span><span class="sxs-lookup"><span data-stu-id="4b62c-175">Employment</span></span> | <span data-ttu-id="4b62c-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="4b62c-176">cdm_employment</span></span> |
| <span data-ttu-id="4b62c-177">Yritys </span><span class="sxs-lookup"><span data-stu-id="4b62c-177">Company</span></span> | <span data-ttu-id="4b62c-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="4b62c-178">cdm_company</span></span> |
| <span data-ttu-id="4b62c-179">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="4b62c-179">Job</span></span> | <span data-ttu-id="4b62c-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="4b62c-180">cdm_job</span></span> |
| <span data-ttu-id="4b62c-181">Työtehtävä</span><span class="sxs-lookup"><span data-stu-id="4b62c-181">Job Function</span></span> | <span data-ttu-id="4b62c-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="4b62c-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="4b62c-183">Toimi</span><span class="sxs-lookup"><span data-stu-id="4b62c-183">Job Position</span></span> | <span data-ttu-id="4b62c-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="4b62c-184">cdm_jobposition</span></span> |
| <span data-ttu-id="4b62c-185">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="4b62c-185">Position Type</span></span> | <span data-ttu-id="4b62c-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="4b62c-186">cdm_positiontype</span></span> |
| <span data-ttu-id="4b62c-187">Toimen työntekijän toimeksianto</span><span class="sxs-lookup"><span data-stu-id="4b62c-187">Position Worker Assignment</span></span> | <span data-ttu-id="4b62c-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="4b62c-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="4b62c-189">Toimen dimensio</span><span class="sxs-lookup"><span data-stu-id="4b62c-189">Job Position Dimension</span></span> | <span data-ttu-id="4b62c-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="4b62c-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="4b62c-191">Työlaji</span><span class="sxs-lookup"><span data-stu-id="4b62c-191">Job Type</span></span> | <span data-ttu-id="4b62c-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="4b62c-192">cdm_jobtype</span></span> |
| <span data-ttu-id="4b62c-193">Kieli</span><span class="sxs-lookup"><span data-stu-id="4b62c-193">Language</span></span> | <span data-ttu-id="4b62c-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="4b62c-194">cdm_language</span></span> |
| <span data-ttu-id="4b62c-195">Tehtävänimike</span><span class="sxs-lookup"><span data-stu-id="4b62c-195">Title</span></span> | <span data-ttu-id="4b62c-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="4b62c-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="4b62c-197">Talous hallinnon dimensiot **Toimityypille**, **Toimen työntekijämääritykselle** ja **Työllisyydelle** tarjoavat yhdensuuntaisen integroinnin Common Data Service -järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="4b62c-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="4b62c-198">Taloushallinnon dimensioiden päivityksiä ei tällä hetkellä synkronoida Common Data Service -sovelluksesta Human Resources -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="4b62c-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="4b62c-199">Loman ja poissaolon kohteet</span><span class="sxs-lookup"><span data-stu-id="4b62c-199">Leave and absence entities</span></span>

| <span data-ttu-id="4b62c-200">Nimi</span><span class="sxs-lookup"><span data-stu-id="4b62c-200">Name</span></span> | <span data-ttu-id="4b62c-201">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="4b62c-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4b62c-202">Lomapankkitapahtuma</span><span class="sxs-lookup"><span data-stu-id="4b62c-202">Leave Bank Transaction</span></span> | <span data-ttu-id="4b62c-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="4b62c-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="4b62c-204">Lomailmoittautuminen</span><span class="sxs-lookup"><span data-stu-id="4b62c-204">Leave Enrollment</span></span> | <span data-ttu-id="4b62c-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="4b62c-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="4b62c-206">Lomasuunnitelma</span><span class="sxs-lookup"><span data-stu-id="4b62c-206">Leave Plan</span></span> | <span data-ttu-id="4b62c-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="4b62c-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="4b62c-208">Lomapyyntö</span><span class="sxs-lookup"><span data-stu-id="4b62c-208">Leave Request</span></span> | <span data-ttu-id="4b62c-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="4b62c-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="4b62c-210">Lomapyynnön tiedot</span><span class="sxs-lookup"><span data-stu-id="4b62c-210">Leave Request Detail</span></span> | <span data-ttu-id="4b62c-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="4b62c-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="4b62c-212">Lomatyyppi</span><span class="sxs-lookup"><span data-stu-id="4b62c-212">Leave Type</span></span> | <span data-ttu-id="4b62c-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="4b62c-213">cdm_leavetype</span></span> |
| <span data-ttu-id="4b62c-214">Lomatyypin syykoodi</span><span class="sxs-lookup"><span data-stu-id="4b62c-214">Leave Type Reason Code</span></span> | <span data-ttu-id="4b62c-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="4b62c-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="4b62c-216">Palkanlaskentayksiköt</span><span class="sxs-lookup"><span data-stu-id="4b62c-216">Payroll entities</span></span>

| <span data-ttu-id="4b62c-217">Nimi</span><span class="sxs-lookup"><span data-stu-id="4b62c-217">Name</span></span> | <span data-ttu-id="4b62c-218">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="4b62c-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4b62c-219">Maksujakso</span><span class="sxs-lookup"><span data-stu-id="4b62c-219">Pay Cycle</span></span> | <span data-ttu-id="4b62c-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="4b62c-220">cdm_paycycle</span></span> |
| <span data-ttu-id="4b62c-221">Maksukausi</span><span class="sxs-lookup"><span data-stu-id="4b62c-221">Pay Period</span></span> | <span data-ttu-id="4b62c-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="4b62c-222">cdm_payperiod</span></span> |
| <span data-ttu-id="4b62c-223">Palkanlaskennan ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="4b62c-223">Payroll Earning Code</span></span> | <span data-ttu-id="4b62c-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="4b62c-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="4b62c-225">Pankkitilisuoritukset</span><span class="sxs-lookup"><span data-stu-id="4b62c-225">Bank Account Disbursement</span></span> | <span data-ttu-id="4b62c-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="4b62c-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="4b62c-227">Verotusalue</span><span class="sxs-lookup"><span data-stu-id="4b62c-227">Tax Region</span></span> | <span data-ttu-id="4b62c-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="4b62c-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="4b62c-229">Työntekijäyksiköt</span><span class="sxs-lookup"><span data-stu-id="4b62c-229">Worker entities</span></span>

| <span data-ttu-id="4b62c-230">Nimi</span><span class="sxs-lookup"><span data-stu-id="4b62c-230">Name</span></span> | <span data-ttu-id="4b62c-231">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="4b62c-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4b62c-232">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="4b62c-232">Worker</span></span> | <span data-ttu-id="4b62c-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="4b62c-233">cdm_worker</span></span> |
| <span data-ttu-id="4b62c-234">Työntekijän osoite</span><span class="sxs-lookup"><span data-stu-id="4b62c-234">Worker Address</span></span> | <span data-ttu-id="4b62c-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="4b62c-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="4b62c-236">Työntekijän henkilötiedot</span><span class="sxs-lookup"><span data-stu-id="4b62c-236">Worker Personal Detail</span></span> | <span data-ttu-id="4b62c-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="4b62c-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="4b62c-238">Työntekijän tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="4b62c-238">Worker Person Identification Number</span></span> | <span data-ttu-id="4b62c-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="4b62c-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="4b62c-240">Työntekijän tunnustyyppi</span><span class="sxs-lookup"><span data-stu-id="4b62c-240">Worker Person Identification Type</span></span> | <span data-ttu-id="4b62c-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="4b62c-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="4b62c-242">Työkalenteri</span><span class="sxs-lookup"><span data-stu-id="4b62c-242">Work Calendar</span></span> | <span data-ttu-id="4b62c-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="4b62c-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="4b62c-244">Työkalenteripäivämäärä</span><span class="sxs-lookup"><span data-stu-id="4b62c-244">Work Calendar Day</span></span> | <span data-ttu-id="4b62c-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="4b62c-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="4b62c-246">Työkalenterin lomapäivä</span><span class="sxs-lookup"><span data-stu-id="4b62c-246">Work Calendar Holiday</span></span> |<span data-ttu-id="4b62c-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="4b62c-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="4b62c-248">Työkalenterin lomapäivärivi</span><span class="sxs-lookup"><span data-stu-id="4b62c-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="4b62c-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="4b62c-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="4b62c-250">Työkalenterin aikaväli</span><span class="sxs-lookup"><span data-stu-id="4b62c-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="4b62c-251">cdm_workcalendartimeinterval (Ei käytössä mukautetulla kentän tuella)</span><span class="sxs-lookup"><span data-stu-id="4b62c-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="4b62c-252">Työntekijän pankkitili</span><span class="sxs-lookup"><span data-stu-id="4b62c-252">Worker Bank Account</span></span> | <span data-ttu-id="4b62c-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="4b62c-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="4b62c-254">Työntekijän asetusyksiköt</span><span class="sxs-lookup"><span data-stu-id="4b62c-254">Worker setup entities</span></span>

| <span data-ttu-id="4b62c-255">Nimi</span><span class="sxs-lookup"><span data-stu-id="4b62c-255">Name</span></span> | <span data-ttu-id="4b62c-256">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="4b62c-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4b62c-257">Sotaveteraanitila</span><span class="sxs-lookup"><span data-stu-id="4b62c-257">Veteran Status</span></span> | <span data-ttu-id="4b62c-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="4b62c-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="4b62c-259">Etninen tausta</span><span class="sxs-lookup"><span data-stu-id="4b62c-259">Ethnic Origin</span></span> | <span data-ttu-id="4b62c-260">HcmEthnicOrigin</span><span class="sxs-lookup"><span data-stu-id="4b62c-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="4b62c-261">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="4b62c-261">Reason Code</span></span> | <span data-ttu-id="4b62c-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="4b62c-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="4b62c-263">Henkilötunnuksen myöntänyt virasto</span><span class="sxs-lookup"><span data-stu-id="4b62c-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="4b62c-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="4b62c-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="4b62c-265">Osaamisyksiköt</span><span class="sxs-lookup"><span data-stu-id="4b62c-265">Competency entities</span></span>

| <span data-ttu-id="4b62c-266">Nimi</span><span class="sxs-lookup"><span data-stu-id="4b62c-266">Name</span></span> | <span data-ttu-id="4b62c-267">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="4b62c-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4b62c-268">Osaamisaluetyyppi</span><span class="sxs-lookup"><span data-stu-id="4b62c-268">Skill Type</span></span> | <span data-ttu-id="4b62c-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="4b62c-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="4b62c-270">Yksikkösuhteen mallit</span><span class="sxs-lookup"><span data-stu-id="4b62c-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="4b62c-271">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="4b62c-271">Worker</span></span>

![Työntekijä](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="4b62c-273">Työ ja työn sijainti</span><span class="sxs-lookup"><span data-stu-id="4b62c-273">Job and Job Position</span></span>

![Työ ja työn sijainti](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="4b62c-275">Edut</span><span class="sxs-lookup"><span data-stu-id="4b62c-275">Benefits</span></span>

![Edut](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="4b62c-277">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="4b62c-277">Compensation</span></span>

![Kompensaatio](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="4b62c-279">Poistu</span><span class="sxs-lookup"><span data-stu-id="4b62c-279">Leave</span></span>

![Poistu](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="4b62c-281">Työkalenteri</span><span class="sxs-lookup"><span data-stu-id="4b62c-281">Work Calendar</span></span>

![Työkalenteri](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="4b62c-283">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="4b62c-283">See also</span></span>

[<span data-ttu-id="4b62c-284">Valitse tietojen integraatioteknologia</span><span class="sxs-lookup"><span data-stu-id="4b62c-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="4b62c-285">Common Data Service -integroinnin määritys</span><span class="sxs-lookup"><span data-stu-id="4b62c-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
