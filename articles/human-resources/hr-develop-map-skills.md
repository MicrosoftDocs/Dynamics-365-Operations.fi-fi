---
title: Osaamisalueiden kartoitus
description: Voit luoda osaamisaluekartoitushaun, etsiäksesi pätevää henkilöä Dynamics 365 Human Resourcesista.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 03b7860fbde89097141cfe48f2c240dc127aa9c3
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076589"
---
# <a name="map-skills"></a><span data-ttu-id="eba9e-103">Osaamisalueiden kartoitus</span><span class="sxs-lookup"><span data-stu-id="eba9e-103">Map skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="eba9e-104">Voit luoda osaamisaluekartoitushaun, etsiäksesi pätevää henkilöä Dynamics 365 Human Resourcesista.</span><span class="sxs-lookup"><span data-stu-id="eba9e-104">You can create a skill-mapping search to find a qualified person in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="eba9e-105">Osaamisaluekartoitus etsii hakutuloksia hakuehtoihin, jotka voit lisätä käyttämällä seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="eba9e-105">Skill-mapping searches return results for criteria you enter by looking through the following information:</span></span>

- <span data-ttu-id="eba9e-106">Osaamisalueet</span><span class="sxs-lookup"><span data-stu-id="eba9e-106">Skills</span></span>
- <span data-ttu-id="eba9e-107">Koulutus</span><span class="sxs-lookup"><span data-stu-id="eba9e-107">Education</span></span>
- <span data-ttu-id="eba9e-108">Sertifikaatit</span><span class="sxs-lookup"><span data-stu-id="eba9e-108">Certificates</span></span>
- <span data-ttu-id="eba9e-109">Toimet</span><span class="sxs-lookup"><span data-stu-id="eba9e-109">Positions</span></span>
- <span data-ttu-id="eba9e-110">Projektikokemus</span><span class="sxs-lookup"><span data-stu-id="eba9e-110">Project experience</span></span>

<span data-ttu-id="eba9e-111">Voit esimerkiksi etsiä organisaatiosi henkilöitä, jotka ovat ansainneet CPA:n.</span><span class="sxs-lookup"><span data-stu-id="eba9e-111">For example, you can find people in your organization who have earned their CPA.</span></span>

<span data-ttu-id="eba9e-112">Osaamisaluekartoitusprofiilien avulla voit etsiä nykyisiä työntekijöitä tai hakijoita, joiden pätevyys vastaa suoraan liiketoiminnan tarpeita.</span><span class="sxs-lookup"><span data-stu-id="eba9e-112">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>

> [!NOTE]
> <span data-ttu-id="eba9e-113">Vain osaamisaluekartoitushakuihin valitut työntekijät, hakijat ja yhteyshenkilöt näytetään osaamisaluekartoituksen tulosluettelossa tai sisällytetään osaamisalueprofiilin.</span><span class="sxs-lookup"><span data-stu-id="eba9e-113">Only workers, applicants, and contact persons who are selected to be included in skill-mapping searches will display in a skill-mapping results list, or be included in a skill profile.</span></span> <span data-ttu-id="eba9e-114">Jos haluat sisällyttää henkilön osaamisaluekartoitushakuihin, määritä **Sisällytä osaamisaluekartoitukseen** -asetukseksi **Kyllä** seuraavilla sivuilla:</span><span class="sxs-lookup"><span data-stu-id="eba9e-114">To include a person in skill mapping searches, set the **Include in skill mapping** selection to **Yes** in the following pages:</span></span><br>
> - <span data-ttu-id="eba9e-115">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="eba9e-115">Worker</span></span><br>
> - <span data-ttu-id="eba9e-116">Työntekijä </span><span class="sxs-lookup"><span data-stu-id="eba9e-116">Employee</span></span><br>
> - <span data-ttu-id="eba9e-117">Hakija</span><span class="sxs-lookup"><span data-stu-id="eba9e-117">Applicant</span></span><br>
> - <span data-ttu-id="eba9e-118">Yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="eba9e-118">Contacts</span></span><br>

<span data-ttu-id="eba9e-119">Voit luoda osaamisaluekartoituksen menemällä kohtaan **Työntekijän kehitys > linkit > osaamisaluekartoitus**.</span><span class="sxs-lookup"><span data-stu-id="eba9e-119">To create a skill mapping, go to **Employee development > Links > Skill mapping**.</span></span> <span data-ttu-id="eba9e-120">Voit luoda osaamisaluekartoitusprofiilin menemällä kohtaan **Työntekijän kehitys > linkit > osaamisaluekartoitusprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="eba9e-120">To create a skill-mapping profile, go to **Employee development > Links > Skill mapping profiles**.</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="eba9e-121">Osaamiseroanalyysi ja osaamisprofiilianalyysi</span><span class="sxs-lookup"><span data-stu-id="eba9e-121">Skill gap analysis and skill profile analysis</span></span>

<span data-ttu-id="eba9e-122">Voit luoda osaamisalueprofiilianalyysin, joka sisältää luettelon henkilön osaamisalueista.</span><span class="sxs-lookup"><span data-stu-id="eba9e-122">You can create a skill profile analysis to view a list of a person's competencies.</span></span> <span data-ttu-id="eba9e-123">Voit luoda osaamisalueaukkoanalyysin, jotta voit verrata henkilön taitoja ja työhön vaadittavia taitoja.</span><span class="sxs-lookup"><span data-stu-id="eba9e-123">You can create a skill gap analysis to compare a person’s skills and the skills required for a job.</span></span>

<span data-ttu-id="eba9e-124">Jos haluat luoda välianalyysin, siirry kohtaan **Työntekijän kehitys > Linkit > osaamisalueaukkoanalyysityö - henkilö**.</span><span class="sxs-lookup"><span data-stu-id="eba9e-124">To create a gap analysis, go to **Employee development > Links > Skill gap analysis job - person**.</span></span> <span data-ttu-id="eba9e-125">Voit luoda osaamisalueprofiilianalyysin menemällä kohtaan **Työntekijän kehitys > linkit > osaamisalueprofiilianalyysi**.</span><span class="sxs-lookup"><span data-stu-id="eba9e-125">To create a skill profile analysis, go to **Employee development > Links > Skill profile analysis**.</span></span>

## <a name="see-also"></a><span data-ttu-id="eba9e-126">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="eba9e-126">See also</span></span>

[<span data-ttu-id="eba9e-127">Osaamisalueiden määritykset</span><span class="sxs-lookup"><span data-stu-id="eba9e-127">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="eba9e-128">Syötä osaamisalueet</span><span class="sxs-lookup"><span data-stu-id="eba9e-128">Enter skills</span></span>](hr-develop-enter-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]