---
title: Jumittuneiden erätöiden nollaaminen
description: Tässä aiheessa kerrotaan, miten ratkaistaan jumiutuneisiin erätöihin liittyvät ongelmat.
author: andreabichsel
ms.date: 03/19/2021
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
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 01ef0bf8ccc486614eec42d3fb6f0b2941fc47c0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794946"
---
# <a name="reset-stuck-batch-jobs"></a><span data-ttu-id="4a2e9-103">Jumittuneiden erätöiden nollaaminen</span><span class="sxs-lookup"><span data-stu-id="4a2e9-103">Reset stuck batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a><span data-ttu-id="4a2e9-104">Varasto-otto</span><span class="sxs-lookup"><span data-stu-id="4a2e9-104">Issue</span></span>

<span data-ttu-id="4a2e9-105">Microsoft Dynamics 365 Human Resourcesissa voi esiintyä erätöihin liittyviä ongelmia, jotka ovat jumiutuneet **Suoritetaan**- tai **Peruutetaan**-tilaan eivätkä valmistu.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-105">Microsoft Dynamics 365 Human Resources can experience issues with batch jobs that are stuck in either an **Executing** or **Canceling** state and don't complete.</span></span>

## <a name="resolution"></a><span data-ttu-id="4a2e9-106">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="4a2e9-106">Resolution</span></span>

<span data-ttu-id="4a2e9-107">Kun erätyöt ovat jumiutuneet **Suoritetaan**- tai **Peruutetaan**-tilaan, voit nollata tilan pakottamalla työn peruutuksen.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-107">When a batch job is stuck in an **Executing** or **Canceling** state, you can reset the status by forcing the cancellation of the job.</span></span> <span data-ttu-id="4a2e9-108">Kun olet peruuttanut sen, voit nollata erätyön määrittämällä sen tilaksi **Odottaa**.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-108">After you cancel it, you can reset the batch job by setting it to a **Waiting** status.</span></span> <span data-ttu-id="4a2e9-109">Se noudetaan sitten uudelleen suoritettavaksi seuraavassa ajoitetussa eräsuorituksessa.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-109">It will then be picked up again for execution in the next scheduled batch run.</span></span>

1. <span data-ttu-id="4a2e9-110">Valitse **Järjestelmän hallinta** -työtilassa **Linkit**-sivu ja valitse **Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-110">In the **System administration** workspace, select the **Links** page, and select **Batch jobs**.</span></span>

2. <span data-ttu-id="4a2e9-111">Valitse **Erätyö**-luettelosivulla palautettava työ.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-111">On the **Batch job** list page, select the job that needs to be reset.</span></span>

3. <span data-ttu-id="4a2e9-112">Valitse toimintovalintanauhassa **Pakota peruutus** ja vahvista toimenpide.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-112">On the action ribbon, select **Force cancel**, and confirm the action.</span></span>

   > [!NOTE]
   > <span data-ttu-id="4a2e9-113">**Pakota peruutus** -toiminto on käytettävissä vain, kun valitun erätyön tilana on **Suoritetaan** tai **Peruutetaan**, eikä työlle ole käynnissä erän suorituksen tai peruutuksen prosesseja.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-113">The **Force cancel** action is only available when the selected batch job has a status of either **Executing** or **Canceling**, and no batch execution or cancellation processes are running for the job.</span></span>

4. <span data-ttu-id="4a2e9-114">Valitse toimintovalintanauhassa **Muuta tila**.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-114">On the action ribbon, select **Change status**.</span></span>

5. <span data-ttu-id="4a2e9-115">Valitse **Valitse uusi tila** -sivulla **Odottaa** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-115">On the **Select new status** page, select **Waiting**, and then select **OK**.</span></span>

   ![Uuden erätyön tilan valinta](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a><span data-ttu-id="4a2e9-117">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="4a2e9-117">See also</span></span>

[<span data-ttu-id="4a2e9-118">Optimoi suorituskyky erätöiden määrityksellä työajan jälkeen</span><span class="sxs-lookup"><span data-stu-id="4a2e9-118">Optimize performance by scheduling batch jobs after hours</span></span>](hr-admin-troubleshooting-batch-jobs.md)<br>
[<span data-ttu-id="4a2e9-119">Optimoi suorituskyky automaattisilla tyhjennystehtävillä</span><span class="sxs-lookup"><span data-stu-id="4a2e9-119">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
