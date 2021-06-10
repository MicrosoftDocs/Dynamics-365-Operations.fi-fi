---
title: Optimoi suorituskyky automaattisilla tyhjennystehtävillä
description: Tässä artikkelissa selitetään, miten voit ratkaista joitakin Microsoftin Dynamics 365 Human Resourcesin suorituskykyongelmia tyhjentämällä erätyöhistorian.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 6a9e94e282aa8f101b42c1378ef21c6c1fe0477e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053488"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="f0811-103">Suorituskyvyn optimointi automaattisten tyhjennystehtävien avulla</span><span class="sxs-lookup"><span data-stu-id="f0811-103">Optimize performance with auto cleanup tasks</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f0811-104">**Lähetä**</span><span class="sxs-lookup"><span data-stu-id="f0811-104">**Issue**</span></span>

<span data-ttu-id="f0811-105">Microsoft Dynamics 365 Human Resourcesissa voi esiintyä suorituskykyongelmia, jos erätyöhistoria kasvaa liian suureksi.</span><span class="sxs-lookup"><span data-stu-id="f0811-105">Microsoft Dynamics 365 Human Resources can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="f0811-106">**Syy**</span><span class="sxs-lookup"><span data-stu-id="f0811-106">**Cause**</span></span>

<span data-ttu-id="f0811-107">Usein suoritettavat erätyöt voivat johtaa erätyöhistorian hallitsemattomaan kasvuun.</span><span class="sxs-lookup"><span data-stu-id="f0811-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="f0811-108">Tämä voi aiheuttaa suorituskykyongelmia.</span><span class="sxs-lookup"><span data-stu-id="f0811-108">This can cause performance issues.</span></span> 

<span data-ttu-id="f0811-109">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="f0811-109">**Resolution**</span></span>

<span data-ttu-id="f0811-110">Ajoita automaattinen tehtävä, joka tyhjentää erätyöhistoriasi.</span><span class="sxs-lookup"><span data-stu-id="f0811-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="f0811-111">Suosittelemme määrittämään tehtävän suoritettavaksi viikoittain, mutta joudut ehkä suorittamaan tyhjennyksen useammin tai harvemmin ympäristösi mukaan.</span><span class="sxs-lookup"><span data-stu-id="f0811-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="f0811-112">Seuraava toimenpide sisältää suosittelemamme asetukset, mutta voit muuttaa niitä tarpeidesi mukaan.</span><span class="sxs-lookup"><span data-stu-id="f0811-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="f0811-113">Valitse Human Resourcesissa **Järjestelmän hallinta**.</span><span class="sxs-lookup"><span data-stu-id="f0811-113">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="f0811-114">Kirjoita **Haku**-palkkiin **Erätöiden historian tyhjennys**.</span><span class="sxs-lookup"><span data-stu-id="f0811-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![Hae erätyöhistorian tyhjennys](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="f0811-116">Syötä **Historiaraja (päivinä)** -kenttään **30**.</span><span class="sxs-lookup"><span data-stu-id="f0811-116">In **History limit (days)**, enter **30**.</span></span>

   ![Määritä historiarajaksi 30](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="f0811-118">Valitse **Suorita taustalla** ja sitten **Toistuminen**.</span><span class="sxs-lookup"><span data-stu-id="f0811-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![Määritä toistuminen](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="f0811-120">Valitse **Määritä toistuvuus** -osiosta **Aloituspäivä** ja **Aloitusaika** tapahtumaan ruuhka-aikojen ulkopuolella tai viikonloppuna ja valitse sitten **PÄÄTTYMISPÄIVÄ PUUTTUU**.</span><span class="sxs-lookup"><span data-stu-id="f0811-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![Määritä toistuvuuden alkamispäivä ja -aika](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="f0811-122">Valitse **TOISTUMISEN KUVIO**, valitse **Päivät** ja määritä **TOISTA, KUN MÄÄRITETTY AIKA ON KULUNUT** -asetukseksi **7**.</span><span class="sxs-lookup"><span data-stu-id="f0811-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![Määritä tyhjennys toistumaan viikoittain](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="f0811-124">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0811-124">Select **OK**.</span></span>

8. <span data-ttu-id="f0811-125">Muuta muita parametrejä **Suorita taustalla**-osiosta tarvittaessa ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0811-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]