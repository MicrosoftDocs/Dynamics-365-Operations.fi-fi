---
title: Optimoi suorituskyky aikatauluttamalla erätyöt sulkemisajan jälkeen
description: Tässä ohjeaiheessa selitetään, miten voit ratkaista Microsoftin Dynamics 365 Human Resourcesin suorituskykyongelmia aikatauluttamalla pitkään jatkuvia erätöitä sulkemisajan jälkeen.
author: andreabichsel
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 92dd281ed718be5c7ebd843d015c108ee121f30a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794922"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="e45fe-103">Optimoi suorituskyky aikatauluttamalla erätyöt sulkemisajan jälkeen</span><span class="sxs-lookup"><span data-stu-id="e45fe-103">Optimize performance by scheduling batch jobs after hours</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="e45fe-104">Otto</span><span class="sxs-lookup"><span data-stu-id="e45fe-104">Issue</span></span>

<span data-ttu-id="e45fe-105">Microsoft Dynamics 365 Human Resourcesissa voi ilmetä suorituskykyongelmia, jos pitkään jatkuvat erätyöt suoritetaan tavallisten aukioloaikojen aikana.</span><span class="sxs-lookup"><span data-stu-id="e45fe-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="e45fe-106">Tarkkuus</span><span class="sxs-lookup"><span data-stu-id="e45fe-106">Resolution</span></span>

<span data-ttu-id="e45fe-107">Aikatauluta seuraavat erätyöt sulkemisajan jälkeen.</span><span class="sxs-lookup"><span data-stu-id="e45fe-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="e45fe-108">Suosittelemme myös usein suoritettavien erätöiden suoritusvälien tarkastamista.</span><span class="sxs-lookup"><span data-stu-id="e45fe-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="e45fe-109">Jos mahdollista, vähennä erätyön toistuvuutta.</span><span class="sxs-lookup"><span data-stu-id="e45fe-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="e45fe-110">Monissa tapauksissa oletusväli riittää.</span><span class="sxs-lookup"><span data-stu-id="e45fe-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="e45fe-111">Seuraavat erätyöt tulisi suorittaa yöaikaan tai sulkemisajan jälkeen.</span><span class="sxs-lookup"><span data-stu-id="e45fe-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="e45fe-112">Muista tarkistaa näiden toistuvien erätöiden aikavyöhyke.</span><span class="sxs-lookup"><span data-stu-id="e45fe-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="e45fe-113">Jotkin erätyöt voivat käyttää Pacific Standard Time (PST) -aikaa.</span><span class="sxs-lookup"><span data-stu-id="e45fe-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="e45fe-114">Erätyö</span><span class="sxs-lookup"><span data-stu-id="e45fe-114">Batch job</span></span> | <span data-ttu-id="e45fe-115">Oletusesiintyminen</span><span class="sxs-lookup"><span data-stu-id="e45fe-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="e45fe-116">Erätyöhistorian siivous</span><span class="sxs-lookup"><span data-stu-id="e45fe-116">Batch job history cleanup</span></span> | <span data-ttu-id="e45fe-117">1 kerran kuukaudessa</span><span class="sxs-lookup"><span data-stu-id="e45fe-117">1 time per month</span></span> |
| <span data-ttu-id="e45fe-118">Viennin väliaikaisen tallennuksen tietojen puhdistus</span><span class="sxs-lookup"><span data-stu-id="e45fe-118">Export staging cleanup</span></span> | <span data-ttu-id="e45fe-119">1 kerran päivässä</span><span class="sxs-lookup"><span data-stu-id="e45fe-119">1 time per day</span></span> |
| <span data-ttu-id="e45fe-120">Common Data Service -integroinnin vastaamattoman pyynnön synkronointi</span><span class="sxs-lookup"><span data-stu-id="e45fe-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="e45fe-121">1 kerran päivässä</span><span class="sxs-lookup"><span data-stu-id="e45fe-121">1 time per day</span></span> |
| <span data-ttu-id="e45fe-122">Tietokannan pakkausjärjestelmätyö, joka pitää suorittaa säännöllisesti sulkemisajan jälkeen</span><span class="sxs-lookup"><span data-stu-id="e45fe-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="e45fe-123">1 kerran päivässä</span><span class="sxs-lookup"><span data-stu-id="e45fe-123">1 time per day</span></span> |
| <span data-ttu-id="e45fe-124">Tietokannan indeksin uudelleenmuodostustyö, joka pitää suorittaa säännöllisesti sulkemisajan jälkeen</span><span class="sxs-lookup"><span data-stu-id="e45fe-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="e45fe-125">1 kerran päivässä</span><span class="sxs-lookup"><span data-stu-id="e45fe-125">1 time per day</span></span> |

1. <span data-ttu-id="e45fe-126">Valitse Human Resourcesissa **Järjestelmän hallinta**.</span><span class="sxs-lookup"><span data-stu-id="e45fe-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="e45fe-127">Hae **Haku**-palkissa yhtä yllä mainituista erätöistä.</span><span class="sxs-lookup"><span data-stu-id="e45fe-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="e45fe-128">Valitse **Suorita taustalla** ja sitten **Toistuminen**.</span><span class="sxs-lookup"><span data-stu-id="e45fe-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Määritä toistuminen](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="e45fe-130">Valitse **Määritä toistuvuus** -osiosta **Aloituspäivä** ja **Aloitusaika** tapahtumaan ruuhka-aikojen ulkopuolella tai viikonloppuna.</span><span class="sxs-lookup"><span data-stu-id="e45fe-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="e45fe-131">Valitse **Ei päättymispäivää**.</span><span class="sxs-lookup"><span data-stu-id="e45fe-131">Select **No end date**.</span></span> 

   ![Määritä toistuvuuden alkamispäivä ja -aika](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="e45fe-133">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e45fe-133">Select **OK**.</span></span>

6. <span data-ttu-id="e45fe-134">Muuta tarvittaessa mitä tahansa muita parametreja kohdassa **Suorita taustalla** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e45fe-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e45fe-135">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e45fe-135">Additional resources</span></span>

[<span data-ttu-id="e45fe-136">Optimoi suorituskyky automaattisilla tyhjennystehtävillä</span><span class="sxs-lookup"><span data-stu-id="e45fe-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]