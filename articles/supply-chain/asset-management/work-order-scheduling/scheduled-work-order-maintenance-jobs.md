---
title: Ajoitetut työtilauksen ylläpitotyöt
description: Tässä ohjeaiheessa selitetään ajoitetut työtilausten ylläpitotyöt resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d9f1cd6d22fd17505c3a4ece8a881629b00694d2
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652077"
---
# <a name="scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="33e25-103">Ajoitetut työtilauksen ylläpitotyöt</span><span class="sxs-lookup"><span data-stu-id="33e25-103">Scheduled work order maintenance jobs</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="33e25-104">**Ajoitetut työtilauksen ylläpitotyöt** -sivulla näkyy yleiskuva resurssille kohdennetuista työtilauksista.</span><span class="sxs-lookup"><span data-stu-id="33e25-104">The **Scheduled work order maintenance jobs** page shows an overview of the work orders allocated to a resource.</span></span> <span data-ttu-id="33e25-105">Näkyvissä ovat työtilaukset, joissa käytetään resurssilajeja "henkilöstö", "työkalu" ja "kone".</span><span class="sxs-lookup"><span data-stu-id="33e25-105">Work orders using resource types "Human resources", "Tool", and "Machine" are shown.</span></span> <span data-ttu-id="33e25-106">Jos esimerkiksi varastotyöntekijä ilmoittautuu sairaaksi, voit käyttää tätä sivua löytääksesi nopeasti hänelle kohdennetut työtilaukset ja kohdentaa sitten tehtävälle toisen ylläpitotyöntekijän.</span><span class="sxs-lookup"><span data-stu-id="33e25-106">For example, if a maintenance worker calls in sick, you can use this page to quickly find work orders allocated to the worker, and then allocate another maintenance worker to the job.</span></span>

## <a name="view-scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="33e25-107">Näytä ajoitetut työtilauksen ylläpitotyöt</span><span class="sxs-lookup"><span data-stu-id="33e25-107">View scheduled work order maintenance jobs</span></span>

1. <span data-ttu-id="33e25-108">Valitse **Resurssien hallinta** > **Yhteiset** > **Työtilaukset** > **Ajoitetut työtilauksen ylläpitotyöt**.</span><span class="sxs-lookup"><span data-stu-id="33e25-108">Click **Asset management** > **Common** > **Work orders** > **Scheduled work order maintenance jobs**.</span></span> <span data-ttu-id="33e25-109">Näet luettelon kaikista työtilauksista, jotka on asetettu työtilauksen elinkaaren tilaan "ajoitettu" tai "käynnissä".</span><span class="sxs-lookup"><span data-stu-id="33e25-109">You see a list of all work orders set to work order lifecycle state "Scheduled" or "In progress".</span></span>

2. <span data-ttu-id="33e25-110">Voit lajitella luettelon esimerkiksi kunnossapitotyöntekijän mukaan.</span><span class="sxs-lookup"><span data-stu-id="33e25-110">You can sort the list, for example, by maintenance worker.</span></span> <span data-ttu-id="33e25-111">Voit myös käyttää suodatinta rajoittamaan luetteloa niin, että se näyttää tietylle resurssille tai kunnossapitotyöntekijälle kohdistetut työtilaukset.</span><span class="sxs-lookup"><span data-stu-id="33e25-111">You can also use the filter to limit the list to display work orders allocated to a specific resource or maintenance worker.</span></span>

3. <span data-ttu-id="33e25-112">Voit tarkastella työtilauksen muistiinpanoja ja lisätä tarvittaessa uusia muistiinpanoja valitsemalla työtilaustyön ja napsauttamalla sitten **Muistiinpanot**.</span><span class="sxs-lookup"><span data-stu-id="33e25-112">You can see notes on the work order and, if required, add new notes by selecting the work order job, and then click **Notes**.</span></span>

4. <span data-ttu-id="33e25-113">Jos haluat kohdistaa yhden kunnossapitotyöntekijän työtilaukseen, valitse työtilaus ja napsauta sitten **Työtilaus**.</span><span class="sxs-lookup"><span data-stu-id="33e25-113">If you want to allocate one maintenance worker to a work order, select the work order, and then click **Work order**.</span></span>

5. <span data-ttu-id="33e25-114">**Työtilaus**-sivu aukeaa.</span><span class="sxs-lookup"><span data-stu-id="33e25-114">The **Work order** page opens.</span></span> <span data-ttu-id="33e25-115">Ajoita työtilaus tietylle kunnossapitotyöntekijälle valitsemalla **Resursoi**.</span><span class="sxs-lookup"><span data-stu-id="33e25-115">Click **Dispatch** to schedule the work order to a specific maintenance worker.</span></span>

>[!NOTE]
><span data-ttu-id="33e25-116">Lisätietoja useiden työtilausten tai yhden työtilauksen ajoittamisesta on kohdassa [Ajoita työtilauksia](../work-order-scheduling/schedule-work-orders.md) ja [Resursoi työtilaus](../work-order-scheduling/dispatch-work-order.md).</span><span class="sxs-lookup"><span data-stu-id="33e25-116">Read more about scheduling several work orders or one work order in [Schedule work orders](../work-order-scheduling/schedule-work-orders.md) and [Dispatch work order](../work-order-scheduling/dispatch-work-order.md).</span></span>

<span data-ttu-id="33e25-117">Alla olevassa näyttökuvassa on esimerkki **Ajoitetut työtilauksen ylläpitotyöt** -sivusta.</span><span class="sxs-lookup"><span data-stu-id="33e25-117">The following screenshot shows an example of the **Scheduled work order maintenance jobs** page.</span></span>

![Kuva 1](media/07-work-order-scheduling.png)

