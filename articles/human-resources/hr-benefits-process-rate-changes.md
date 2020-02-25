---
title: Maksumuutosten käsittely
description: Etujen maksumuutosten käsittely Microsoft Dynamics 365 Human Resourcesissa, kun uuden tai olemassa olevan etuussuunnitelman kelpoisuussääntöasetukset muuttuvat.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9ebe5cfc2bdf7790770d27ece2dc67f7677db593
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008841"
---
# <a name="process-rate-changes"></a><span data-ttu-id="82542-103">Maksumuutosten käsittely</span><span class="sxs-lookup"><span data-stu-id="82542-103">Process rate changes</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="82542-104">Etujen maksumuutosten käsittely Microsoft Dynamics 365 Human Resourcesissa, kun uuden tai olemassa olevan etuussuunnitelman kelpoisuussääntöasetukset muuttuvat.</span><span class="sxs-lookup"><span data-stu-id="82542-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="82542-105">Jos uusi kelpoisuussääntö luodaan ja liitetään suunnitelmaan, järjestelmää kehotetaan tarkistamaan työntekijän kelpoisuus uudelleen sen tarkistamiseksi, täyttävätkö työntekijät suunnitelman uusien kelpousuusasetusten vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="82542-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to re-run worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="82542-106">Valitse **Etujen hallinta** -työtilassa **Käsittely**-kohdasta **Maksumuutoksen päivityskäsittely**.</span><span class="sxs-lookup"><span data-stu-id="82542-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="82542-107">Määritä **Suorita edun maksupäivitysprosessi** -valintaruudussa arvot seuraaville kentille:</span><span class="sxs-lookup"><span data-stu-id="82542-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="82542-108">Kenttä</span><span class="sxs-lookup"><span data-stu-id="82542-108">Field</span></span> | <span data-ttu-id="82542-109">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="82542-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="82542-110">Rekisteröitymiskausi</span><span class="sxs-lookup"><span data-stu-id="82542-110">Enrollment period</span></span> | <span data-ttu-id="82542-111">Rekisteröintijakso, jonka maksumuutokset käsitellään.</span><span class="sxs-lookup"><span data-stu-id="82542-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="82542-112">Jos haluat suorittaa prosessin taustalla, valitse **Suorita taustalla** ja tee seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="82542-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="82542-113">Määritä prosessin tiedot.</span><span class="sxs-lookup"><span data-stu-id="82542-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="82542-114">Jos haluat määrittää toistuvan työn, valitse **Toistuminen**, kirjoita toistuvuustiedot ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="82542-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="82542-115">Jos haluat määrittää työpaikkahälytyksen, valitse **Hälytykset**, valitse vastaanotettavat hälytykset ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="82542-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="82542-116">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="82542-116">Select **OK**.</span></span> <span data-ttu-id="82542-117">Prosessi suoritetaan määrittämilläsi parametreilla.</span><span class="sxs-lookup"><span data-stu-id="82542-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="82542-118">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="82542-118">Select **OK**.</span></span>
