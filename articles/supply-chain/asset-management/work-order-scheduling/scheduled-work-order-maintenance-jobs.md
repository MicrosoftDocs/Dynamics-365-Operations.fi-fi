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
ms.openlocfilehash: 4b3cc32d6ff263967c1ee843702c28968219ac33
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887179"
---
# <a name="scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="6b941-103">Ajoitetut työtilauksen ylläpitotyöt</span><span class="sxs-lookup"><span data-stu-id="6b941-103">Scheduled work order maintenance jobs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6b941-104">**Ajoitetut työtilauksen ylläpitotyöt** -sivun avulla saadaan yleiskuva resurssille kohdistetuista työtilauksista.</span><span class="sxs-lookup"><span data-stu-id="6b941-104">The **Scheduled work order maintenance jobs** page is used to get an overview of the work orders allocated to a resource.</span></span> <span data-ttu-id="6b941-105">Työtilaukset, joissa käytetään resurssilajeja "henkilöstö", "työkalu" ja "kone", näkyvät luettelossa.</span><span class="sxs-lookup"><span data-stu-id="6b941-105">Work orders using resource types "Human resources", "Tool", and "Machine" are shown in the list.</span></span> <span data-ttu-id="6b941-106">Luettelon avulla saadaan yleiskuva tietylle resurssille kohdistetuista työtilauksista.</span><span class="sxs-lookup"><span data-stu-id="6b941-106">The list can be used to get an overview of work orders allocated to a specific resource.</span></span> <span data-ttu-id="6b941-107">Sen avulla voit myös nopeasti löytää työtilauksen, joka on kohdistettu huoltotyöntekijälle, joka esimerkiksi on ilmoittautunut sairaaksi tänä aamuna, ja kohdistaa sitten nopeasti toisen kunnossapitotyöntekijän työhön.</span><span class="sxs-lookup"><span data-stu-id="6b941-107">You can also use it to quickly find a work order allocated to a maintenance worker who, for example, called in sick this morning, and then quickly allocate another maintenance worker to the job.</span></span>

## <a name="view-scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="6b941-108">Näytä ajoitetut työtilauksen ylläpitotyöt</span><span class="sxs-lookup"><span data-stu-id="6b941-108">View scheduled work order maintenance jobs</span></span>

1. <span data-ttu-id="6b941-109">Valitse **Resurssien hallinta** > **Yhteiset** > **Työtilaukset** > **Ajoitetut työtilauksen ylläpitotyöt**.</span><span class="sxs-lookup"><span data-stu-id="6b941-109">Click **Asset management** > **Common** > **Work orders** > **Scheduled work order maintenance jobs**.</span></span> <span data-ttu-id="6b941-110">Näet luettelon kaikista työtilauksista, jotka on asetettu työtilauksen elinkaaren tilaan "ajoitettu" tai "käynnissä".</span><span class="sxs-lookup"><span data-stu-id="6b941-110">You see a list of all work orders set to work order lifecycle state "Scheduled" or "In progress".</span></span>

2. <span data-ttu-id="6b941-111">Voit lajitella luettelon esimerkiksi kunnossapitotyöntekijän mukaan.</span><span class="sxs-lookup"><span data-stu-id="6b941-111">You can sort the list, for example, by maintenance worker.</span></span> <span data-ttu-id="6b941-112">Voit myös käyttää suodatinta rajoittamaan luetteloa niin, että se näyttää tietylle resurssille tai kunnossapitotyöntekijälle kohdistetut työtilaukset.</span><span class="sxs-lookup"><span data-stu-id="6b941-112">You can also use the filter to limit the list to display work orders allocated to a specific resource or maintenance worker.</span></span>

3. <span data-ttu-id="6b941-113">Voit tarkastella työtilauksen muistiinpanoja ja lisätä tarvittaessa uusia muistiinpanoja valitsemalla työtilaustyön luettelosta ja valitsemalla sitten **Muistiinpanot**.</span><span class="sxs-lookup"><span data-stu-id="6b941-113">You can see notes on the work order and, if required, add new notes by selecting the work order job in the list and clicking **Notes**.</span></span>

4. <span data-ttu-id="6b941-114">Jos haluat kohdistaa yhden kunnossapitotyöntekijän työtilaukseen, valitse työtilaus-luettelosta ja valitse sitten **Työtilaus**.</span><span class="sxs-lookup"><span data-stu-id="6b941-114">If you want to allocate one maintenance worker to a work order, select the work order in the list, and click **Work order**.</span></span>

5. <span data-ttu-id="6b941-115">**Työtilaus**-sivu aukeaa.</span><span class="sxs-lookup"><span data-stu-id="6b941-115">The **Work order** page opens.</span></span> <span data-ttu-id="6b941-116">Ajoita työtilaus tietylle kunnossapitotyöntekijälle valitsemalla **Resursoi**.</span><span class="sxs-lookup"><span data-stu-id="6b941-116">Click **Dispatch** to schedule the work order to a specific maintenance worker.</span></span>

>[!NOTE]
><span data-ttu-id="6b941-117">Lisätietoja useiden työtilausten tai yhden työtilauksen ajoittamisesta on kohdassa [Ajoita työtilauksia](../work-order-scheduling/schedule-work-orders.md) ja [Resursoi työtilaus](../work-order-scheduling/dispatch-work-order.md).</span><span class="sxs-lookup"><span data-stu-id="6b941-117">Read more about scheduling several work orders or one work order in [Schedule work orders](../work-order-scheduling/schedule-work-orders.md) and [Dispatch work order](../work-order-scheduling/dispatch-work-order.md).</span></span>

<span data-ttu-id="6b941-118">Alla olevassa kuvassa on esimerkki **Ajoitetut työtilauksen ylläpitotyöt** -sivusta.</span><span class="sxs-lookup"><span data-stu-id="6b941-118">The figure below shows an example of the **Scheduled work order maintenance jobs** page.</span></span>

![Kuva 1](media/07-work-order-scheduling.png)

