---
title: Lifecycle Servicesin (LCS) poistetut tai vanhentuneet ominaisuudet
description: Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Microsoft Dynamics Lifecycle Servicesistä (LCS).
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e571cc26f55e0bd7a1eef301e193921e0b3f8e31
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454692"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="b05ed-103">Lifecycle Servicesin (LCS) poistetut tai vanhentuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="b05ed-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b05ed-104">Tässä ohjeaiheessa käsitellään Microsoft Dynamics Lifecycle Servicesin (LCS) ominaisuuksia, jotka on poistettu tai jotka ovat vanhentuneita.</span><span class="sxs-lookup"><span data-stu-id="b05ed-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="b05ed-105">*Poistettu* ominaisuus ei ole enää käytettävissä palvelussa.</span><span class="sxs-lookup"><span data-stu-id="b05ed-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="b05ed-106">*Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.</span><span class="sxs-lookup"><span data-stu-id="b05ed-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="b05ed-107">Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi.</span><span class="sxs-lookup"><span data-stu-id="b05ed-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="b05ed-108">Lokakuu 2019 ilmoitukset</span><span class="sxs-lookup"><span data-stu-id="b05ed-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="b05ed-109">Liiketoimintaprosessien mallintajan vuokaaviot</span><span class="sxs-lookup"><span data-stu-id="b05ed-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="b05ed-110"><strong>Poiston tai vanhentumisen syy</strong></span><span class="sxs-lookup"><span data-stu-id="b05ed-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="b05ed-111">Olemme poistamassa vuokaavioiden komponentin liiketoimintaprosessien mallintaja (BPM)-osassa, koska vanha muotoilu aiheutti vähäisen käytön.</span><span class="sxs-lookup"><span data-stu-id="b05ed-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b05ed-112"><strong>Onko toinen ominaisuus korvannut?</strong></span><span class="sxs-lookup"><span data-stu-id="b05ed-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="b05ed-113">Ei</span><span class="sxs-lookup"><span data-stu-id="b05ed-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b05ed-114"><strong>Alueet, joihin avain vaikuttaa</strong></span><span class="sxs-lookup"><span data-stu-id="b05ed-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="b05ed-115">Liiketoimintaprosessien mallintaja</span><span class="sxs-lookup"><span data-stu-id="b05ed-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b05ed-116"><strong>Tila</strong></span><span class="sxs-lookup"><span data-stu-id="b05ed-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="b05ed-117">Vanhentunut: vuokakaavioiden osaa BPM:ssä odotetaan poistettavaksi vuonna 2020.</span><span class="sxs-lookup"><span data-stu-id="b05ed-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="b05ed-118">Seuraavat toiminnot eivät ole käytettävissä:</span><span class="sxs-lookup"><span data-stu-id="b05ed-118">The following functionality will be unavailable:</span></span>
<ul>
<li><span data-ttu-id="b05ed-119">Kaikki vuokaaviot ovat vain luku -muotoisia eikä niitä voi muokata.</span><span class="sxs-lookup"><span data-stu-id="b05ed-119">All flowcharts will be read-only and unavailable for editing.</span></span> <span data-ttu-id="b05ed-120">Myöskään vuokaaviotehtäviin liitetyt muodon ominaisuudet eivät ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b05ed-120">The shape properties that are associated with flowchart activities will also be unavailable.</span></span> <span data-ttu-id="b05ed-121">Nämä vuokaaviot sisältävät sekä oletusarvoiset vuokaaviot, jotka luodaan automaattisesti, että mukautettuja vuokaavioita, joita muokataan näiden oletusarvoisten vuokaavioiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="b05ed-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="b05ed-122">Prosessivaiheet ovat vain luku -muotoisia eikä niitä voi muokata.</span><span class="sxs-lookup"><span data-stu-id="b05ed-122">The process steps will be read-only and unavailable for editing.</span></span></li>     
<li><span data-ttu-id="b05ed-123">Vanha sovitus/aukkoanalyysiominaisuus ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b05ed-123">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="b05ed-124">Tämän vuoksi väliluetteloa ei luoda automaattisesti eikä se ole käytettävissä vientiä varten.</span><span class="sxs-lookup"><span data-stu-id="b05ed-124">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="b05ed-125"><strong>Huomautus:</strong> Tämä ominaisuus on aiemmin vanhentunut ja korvattu Microsoft Azure DevOps-integraatiolla.</span><span class="sxs-lookup"><span data-stu-id="b05ed-125"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="b05ed-126">Vuokaavion versiohistoria ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b05ed-126">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
