---
title: Elämäntapahtumien muutosten käsittely
description: Käsittele elämäntapahtumien muutokset Microsoft Dynamics 365 Human Resourcesissa.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1bfbd7347581e57edcab39a675b17ef66e262582
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059013"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="05947-103">Elämäntapahtumien muutosten käsittely</span><span class="sxs-lookup"><span data-stu-id="05947-103">Process life event changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="05947-104">Käsittele elämäntapahtumien muutokset Microsoft Dynamics 365 Human Resourcesissa kahden elämäntapahtumamuutoksen osalta:</span><span class="sxs-lookup"><span data-stu-id="05947-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="05947-105">Syntymäpäivämuutokset</span><span class="sxs-lookup"><span data-stu-id="05947-105">Birthday changes</span></span>
- <span data-ttu-id="05947-106">Etukelpoisuuden ohituksen päättymismuutokset</span><span class="sxs-lookup"><span data-stu-id="05947-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="05947-107">Valitse **Etujen hallinta** -työtilassa **Käsittely**-kohdasta **Elämäntapahtumien muutosten käsittely**.</span><span class="sxs-lookup"><span data-stu-id="05947-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="05947-108">Määritä **Suorita elämäntapahtuman muutosprosessi** -valintaruudussa arvot seuraaville kentille:</span><span class="sxs-lookup"><span data-stu-id="05947-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="05947-109">Kenttä</span><span class="sxs-lookup"><span data-stu-id="05947-109">Field</span></span> | <span data-ttu-id="05947-110">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="05947-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="05947-111">Rekisteröitymiskausi</span><span class="sxs-lookup"><span data-stu-id="05947-111">Enrollment period</span></span> | <span data-ttu-id="05947-112">Rekisteröintijakso, jonka elämäntapahtumien muutokset käsitellään.</span><span class="sxs-lookup"><span data-stu-id="05947-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="05947-113">Oikeushenkilö</span><span class="sxs-lookup"><span data-stu-id="05947-113">Legal entity</span></span> | <span data-ttu-id="05947-114">Yritys, jonka elämäntapahtumien muutokset käsitellään.</span><span class="sxs-lookup"><span data-stu-id="05947-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="05947-115">Jos haluat suorittaa prosessin taustalla, valitse **Suorita taustalla** ja tee seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="05947-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="05947-116">Määritä prosessin tiedot.</span><span class="sxs-lookup"><span data-stu-id="05947-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="05947-117">Jos haluat määrittää toistuvan työn, valitse **Toistuminen**, kirjoita toistuvuustiedot ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="05947-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="05947-118">Jos haluat määrittää työpaikkahälytyksen, valitse **Hälytykset**, valitse vastaanotettavat hälytykset ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="05947-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="05947-119">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="05947-119">Select **OK**.</span></span> <span data-ttu-id="05947-120">Prosessi suoritetaan määrittämilläsi parametreilla.</span><span class="sxs-lookup"><span data-stu-id="05947-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="05947-121">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="05947-121">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]