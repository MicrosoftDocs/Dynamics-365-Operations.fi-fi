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
ms.openlocfilehash: 66d5b10e1471b98274d4049df18a2e53873f789a
ms.sourcegitcommit: 92cd55028be556a0bd41b6972c9c6d14b695dfa0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/10/2020
ms.locfileid: "2947477"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="b07f0-103">Pääsuunnittelutyön peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="b07f0-103">Cancel a master planning job</span></span>

<span data-ttu-id="b07f0-104">Microsoft Dynamics 365 Supply Chain Managementilla on useita vaihtoehtoja pääsuunnittelutyön peruutukseen.</span><span class="sxs-lookup"><span data-stu-id="b07f0-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="b07f0-105">Voit esimerkiksi peruuttaa pääsuunnittelutyön, jos se on käynnistetty vahingossa tai se on odotettua pitempi ja haluat lopettaa sen.</span><span class="sxs-lookup"><span data-stu-id="b07f0-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="b07f0-106">Paras tapa peruuttaa suunnittelutyö on tehdä se **Keskeneräiset suunnitteluprosessit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b07f0-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="b07f0-107">Muita mahdollisia vaihtoehtoja **Erätyöt** ja **Parannetut erätyöt** -sivuilta tulisi käyttää vain, jos pääsuunnittelutyön peruuttaminen **keskeneräiset suunnitteluprosessit** -sivulta ei onnistu muutaman minuutin kuluessa.</span><span class="sxs-lookup"><span data-stu-id="b07f0-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="b07f0-108">Ensisijainen peruutusvaihtoehto</span><span class="sxs-lookup"><span data-stu-id="b07f0-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="b07f0-109">Peruuta pääsuunnittelutyö **Keskeneräiset suunnitteluprosessit** -sivulla</span><span class="sxs-lookup"><span data-stu-id="b07f0-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="b07f0-110">Siirry kohtaan **Pääsuunnittelu > Kyselyt ja raportit > Pääsuunnittelu > Keskeneräiset suunnitteluprosessit**.</span><span class="sxs-lookup"><span data-stu-id="b07f0-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="b07f0-111">Valitse se rivi, jossa peruutettava suunnitteluprosessi sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="b07f0-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="b07f0-112">Valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="b07f0-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="b07f0-113">Muut peruutusasetukset</span><span class="sxs-lookup"><span data-stu-id="b07f0-113">Additional cancel options</span></span>
<span data-ttu-id="b07f0-114">Näitä tulisi käyttää vain jos pääsuunnittelutyön peruutus **Keskeneräiset suunnitteluprosessit** -sivulla ei onnistu muutaman minuutin kuluessa.</span><span class="sxs-lookup"><span data-stu-id="b07f0-114">These should only be used iif cancelin the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="b07f0-115">Poista pääsuunnittelutyö **Erätyöt**-sivulta</span><span class="sxs-lookup"><span data-stu-id="b07f0-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="b07f0-116">Valitse **Järjestelmän hallinta > Kyselyt > Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="b07f0-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="b07f0-117">Valitse se rivi, jossa poistettava suunnittelutyö sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="b07f0-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="b07f0-118">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="b07f0-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="b07f0-119">Keskeytä pääsuunnittelutyötehtävä **Parannetut erätyöt** -sivulta</span><span class="sxs-lookup"><span data-stu-id="b07f0-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="b07f0-120">Valitse **Järjestelmän hallinta > Kyselyt > Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="b07f0-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="b07f0-121">Jos työn tunnusta ei näytetä luettelossa, valitse **Siirry parannettuun lomakkeeseen**, muutoin jatka seuraavaan vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="b07f0-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="b07f0-122">Avaa erätyö.</span><span class="sxs-lookup"><span data-stu-id="b07f0-122">Open the batch job.</span></span> <span data-ttu-id="b07f0-123">Napsauta **työn tunnusta** erätyölle, jonka tehtäviä haluat lopettaa.</span><span class="sxs-lookup"><span data-stu-id="b07f0-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="b07f0-124">Valitse **Erätehtävissä** tehtävät, jotka haluat lopettaa.</span><span class="sxs-lookup"><span data-stu-id="b07f0-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="b07f0-125">Valitse **Erätehtävät**-pikavälilehdellä **Keskeytä**.</span><span class="sxs-lookup"><span data-stu-id="b07f0-125">On the **Batch tasks** FastTab, click **Abort**.</span></span>
