---
title: Elämäntapahtumien muutosten käsittely
description: Käsittele elämäntapahtumien muutokset Microsoft Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2726dcb3c847c9af2a431358de04a27341b9e66c
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464247"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="6abde-103">Elämäntapahtumien muutosten käsittely</span><span class="sxs-lookup"><span data-stu-id="6abde-103">Process life event changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6abde-104">Käsittele elämäntapahtumien muutokset Microsoft Dynamics 365 Human Resourcesissa kahden elämäntapahtumamuutoksen osalta:</span><span class="sxs-lookup"><span data-stu-id="6abde-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="6abde-105">Syntymäpäivämuutokset</span><span class="sxs-lookup"><span data-stu-id="6abde-105">Birthday changes</span></span>
- <span data-ttu-id="6abde-106">Etukelpoisuuden ohituksen päättymismuutokset</span><span class="sxs-lookup"><span data-stu-id="6abde-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="6abde-107">Valitse **Etujen hallinta** -työtilassa **Käsittely**-kohdasta **Elämäntapahtumien muutosten käsittely**.</span><span class="sxs-lookup"><span data-stu-id="6abde-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="6abde-108">Määritä **Suorita elämäntapahtuman muutosprosessi** -valintaruudussa arvot seuraaville kentille:</span><span class="sxs-lookup"><span data-stu-id="6abde-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="6abde-109">Kenttä</span><span class="sxs-lookup"><span data-stu-id="6abde-109">Field</span></span> | <span data-ttu-id="6abde-110">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="6abde-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="6abde-111">Rekisteröitymiskausi</span><span class="sxs-lookup"><span data-stu-id="6abde-111">Enrollment period</span></span> | <span data-ttu-id="6abde-112">Rekisteröintijakso, jonka elämäntapahtumien muutokset käsitellään.</span><span class="sxs-lookup"><span data-stu-id="6abde-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="6abde-113">Oikeushenkilö</span><span class="sxs-lookup"><span data-stu-id="6abde-113">Legal entity</span></span> | <span data-ttu-id="6abde-114">Yritys, jonka elämäntapahtumien muutokset käsitellään.</span><span class="sxs-lookup"><span data-stu-id="6abde-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="6abde-115">Jos haluat suorittaa prosessin taustalla, valitse **Suorita taustalla** ja tee seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="6abde-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="6abde-116">Määritä prosessin tiedot.</span><span class="sxs-lookup"><span data-stu-id="6abde-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="6abde-117">Jos haluat määrittää toistuvan työn, valitse **Toistuminen**, kirjoita toistuvuustiedot ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6abde-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="6abde-118">Jos haluat määrittää työpaikkahälytyksen, valitse **Hälytykset**, valitse vastaanotettavat hälytykset ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="6abde-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="6abde-119">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6abde-119">Select **OK**.</span></span> <span data-ttu-id="6abde-120">Prosessi suoritetaan määrittämilläsi parametreilla.</span><span class="sxs-lookup"><span data-stu-id="6abde-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="6abde-121">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6abde-121">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]