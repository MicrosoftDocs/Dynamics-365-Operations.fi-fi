---
title: Pääsuunnittelutyön peruuttaminen
description: Tässä ohjeaiheessa käsitellään kuinka peruuttaa aktiivinen suunnittelutyö, joka käyttää sisäänrakennettua suunnittelutoimintoa.
author: ChristianRytt
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: c04e2b2c0e5d7f28ea688578b3e1d7a1e1d9f6d3
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117445"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="45ea7-103">Pääsuunnittelutyön peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="45ea7-103">Cancel a master planning job</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45ea7-104">Microsoft Dynamics 365 Supply Chain Managementilla on useita vaihtoehtoja pääsuunnittelutyön peruutukseen.</span><span class="sxs-lookup"><span data-stu-id="45ea7-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="45ea7-105">Voit esimerkiksi peruuttaa pääsuunnittelutyön, jos se on käynnistetty vahingossa tai se on odotettua pitempi ja haluat lopettaa sen.</span><span class="sxs-lookup"><span data-stu-id="45ea7-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="45ea7-106">Paras tapa peruuttaa suunnittelutyö on tehdä se **Keskeneräiset suunnitteluprosessit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="45ea7-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="45ea7-107">Muita mahdollisia vaihtoehtoja **Erätyöt** ja **Parannetut erätyöt** -sivuilta tulisi käyttää vain, jos pääsuunnittelutyön peruuttaminen **keskeneräiset suunnitteluprosessit** -sivulta ei onnistu muutaman minuutin kuluessa.</span><span class="sxs-lookup"><span data-stu-id="45ea7-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="45ea7-108">Ensisijainen peruutusvaihtoehto</span><span class="sxs-lookup"><span data-stu-id="45ea7-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="45ea7-109">Peruuta pääsuunnittelutyö **Keskeneräiset suunnitteluprosessit** -sivulla</span><span class="sxs-lookup"><span data-stu-id="45ea7-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="45ea7-110">Siirry kohtaan **Pääsuunnittelu > Kyselyt ja raportit > Pääsuunnittelu > Keskeneräiset suunnitteluprosessit**.</span><span class="sxs-lookup"><span data-stu-id="45ea7-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="45ea7-111">Valitse se rivi, jossa peruutettava suunnitteluprosessi sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="45ea7-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="45ea7-112">Valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="45ea7-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="45ea7-113">Muut peruutusasetukset</span><span class="sxs-lookup"><span data-stu-id="45ea7-113">Additional cancel options</span></span>
<span data-ttu-id="45ea7-114">Näitä tulisi käyttää vain jos pääsuunnittelutyön peruutus **Keskeneräiset suunnitteluprosessit** -sivulla ei onnistu muutaman minuutin kuluessa.</span><span class="sxs-lookup"><span data-stu-id="45ea7-114">These should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="45ea7-115">Poista pääsuunnittelutyö **Erätyöt**-sivulta</span><span class="sxs-lookup"><span data-stu-id="45ea7-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="45ea7-116">Valitse **Järjestelmän hallinta > Kyselyt > Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="45ea7-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="45ea7-117">Valitse se rivi, jossa poistettava suunnittelutyö sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="45ea7-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="45ea7-118">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="45ea7-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="45ea7-119">Keskeytä pääsuunnittelutyötehtävä **Parannetut erätyöt** -sivulta</span><span class="sxs-lookup"><span data-stu-id="45ea7-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="45ea7-120">Valitse **Järjestelmän hallinta > Kyselyt > Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="45ea7-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="45ea7-121">Jos työn tunnusta ei näytetä luettelossa, valitse **Siirry parannettuun lomakkeeseen**, muutoin jatka seuraavaan vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="45ea7-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="45ea7-122">Avaa erätyö.</span><span class="sxs-lookup"><span data-stu-id="45ea7-122">Open the batch job.</span></span> <span data-ttu-id="45ea7-123">Napsauta **työn tunnusta** erätyölle, jonka tehtäviä haluat lopettaa.</span><span class="sxs-lookup"><span data-stu-id="45ea7-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="45ea7-124">Valitse **Erätehtävissä** tehtävät, jotka haluat lopettaa.</span><span class="sxs-lookup"><span data-stu-id="45ea7-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="45ea7-125">Valitse **Erätehtävät**-pikavälilehdellä **Keskeytä**.</span><span class="sxs-lookup"><span data-stu-id="45ea7-125">On the **Batch tasks** FastTab, click **Abort**.</span></span>
