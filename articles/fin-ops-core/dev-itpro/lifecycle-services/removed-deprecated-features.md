---
title: Lifecycle Servicesin (LCS) poistetut tai vanhentuneet ominaisuudet
description: Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Microsoft Dynamics Lifecycle Servicesistä (LCS).
author: AngelMarshall
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e583ec66f24940f44113433042f5e2340cf0f52c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748436"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="88413-103">Lifecycle Servicesin (LCS) poistetut tai vanhentuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="88413-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="88413-104">Tässä ohjeaiheessa käsitellään Microsoft Dynamics Lifecycle Servicesin (LCS) ominaisuuksia, jotka on poistettu tai jotka ovat vanhentuneita.</span><span class="sxs-lookup"><span data-stu-id="88413-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="88413-105">*Poistettu* ominaisuus ei ole enää käytettävissä palvelussa.</span><span class="sxs-lookup"><span data-stu-id="88413-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="88413-106">*Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.</span><span class="sxs-lookup"><span data-stu-id="88413-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="88413-107">Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi.</span><span class="sxs-lookup"><span data-stu-id="88413-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="88413-108">Lokakuu 2019 ilmoitukset</span><span class="sxs-lookup"><span data-stu-id="88413-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="88413-109">Liiketoimintaprosessien mallintajan vuokaaviot</span><span class="sxs-lookup"><span data-stu-id="88413-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="88413-110"><strong>Poiston tai vanhentumisen syy</strong></span><span class="sxs-lookup"><span data-stu-id="88413-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="88413-111">Olemme poistamassa vuokaavioiden komponentin liiketoimintaprosessien mallintaja (BPM)-osassa, koska vanha muotoilu aiheutti vähäisen käytön.</span><span class="sxs-lookup"><span data-stu-id="88413-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88413-112"><strong>Onko toinen ominaisuus korvannut?</strong></span><span class="sxs-lookup"><span data-stu-id="88413-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="88413-113">Ei</span><span class="sxs-lookup"><span data-stu-id="88413-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88413-114"><strong>Alueet, joihin avain vaikuttaa</strong></span><span class="sxs-lookup"><span data-stu-id="88413-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="88413-115">Liiketoimintaprosessien mallintaja</span><span class="sxs-lookup"><span data-stu-id="88413-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88413-116"><strong>Tila</strong></span><span class="sxs-lookup"><span data-stu-id="88413-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="88413-117">Vanhentunut: vuokakaavioiden osaa BPM:ssä odotetaan poistettavaksi vuonna 2020.</span><span class="sxs-lookup"><span data-stu-id="88413-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="88413-118">Seuraavat toiminnot eivät ole käytettävissä:</span><span class="sxs-lookup"><span data-stu-id="88413-118">The following functionality will be unavailable:</span></span>
<ul>
<li><span data-ttu-id="88413-119">Kaikki vuokaaviot ovat vain luku -muotoisia eikä niitä voi muokata.</span><span class="sxs-lookup"><span data-stu-id="88413-119">All flowcharts will be read-only and unavailable for editing.</span></span> <span data-ttu-id="88413-120">Myöskään vuokaaviotehtäviin liitetyt muodon ominaisuudet eivät ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="88413-120">The shape properties that are associated with flowchart activities will also be unavailable.</span></span> <span data-ttu-id="88413-121">Nämä vuokaaviot sisältävät sekä oletusarvoiset vuokaaviot, jotka luodaan automaattisesti, että mukautettuja vuokaavioita, joita muokataan näiden oletusarvoisten vuokaavioiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="88413-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="88413-122">Prosessivaiheet ovat vain luku -muotoisia eikä niitä voi muokata.</span><span class="sxs-lookup"><span data-stu-id="88413-122">The process steps will be read-only and unavailable for editing.</span></span></li>     
<li><span data-ttu-id="88413-123">Vanha sovitus/aukkoanalyysiominaisuus ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="88413-123">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="88413-124">Tämän vuoksi väliluetteloa ei luoda automaattisesti eikä se ole käytettävissä vientiä varten.</span><span class="sxs-lookup"><span data-stu-id="88413-124">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="88413-125"><strong>Huomautus:</strong> Tämä ominaisuus on aiemmin vanhentunut ja korvattu Microsoft Azure DevOps-integraatiolla.</span><span class="sxs-lookup"><span data-stu-id="88413-125"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="88413-126">Vuokaavion versiohistoria ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="88413-126">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]