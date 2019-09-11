---
title: Työtilauksien luonti
description: Tässä ohjeaiheessa selitetään, miten työtilaukset luodaan käyttöomaisuuden hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b23ed3251b2f6cf4f34b423ce2f85301d6ab31a1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875625"
---
# <a name="creating-work-orders"></a><span data-ttu-id="ba36f-103">Työtilauksien luonti</span><span class="sxs-lookup"><span data-stu-id="ba36f-103">Creating work orders</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="ba36f-104">Kun olet ajoittanut ennaltaehkäiseviä kunnossapitotöitä, seuraava vaihe on töiden työtilausten luominen.</span><span class="sxs-lookup"><span data-stu-id="ba36f-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="ba36f-105">Sen voi tehdä ylläpitoaikatauluissa.</span><span class="sxs-lookup"><span data-stu-id="ba36f-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="ba36f-106">Ylläpitoaikataulun ajoitettujen töiden viitetyypit voivat olla erilaiset:</span><span class="sxs-lookup"><span data-stu-id="ba36f-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="ba36f-107">Viitetyyppi</span><span class="sxs-lookup"><span data-stu-id="ba36f-107">Reference type</span></span> | <span data-ttu-id="ba36f-108">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="ba36f-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba36f-109">Ylläpitosuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="ba36f-109">Maintenance plans</span></span>     | <span data-ttu-id="ba36f-110">Ennaltaehkäisevät huoltotyöt, jotka perustuvat huoltosuunnitelmatyyppeihin "aika" tai "laskuri".</span><span class="sxs-lookup"><span data-stu-id="ba36f-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="ba36f-111">Ylläpitokierrokset</span><span class="sxs-lookup"><span data-stu-id="ba36f-111">Maintenance rounds</span></span>    | <span data-ttu-id="ba36f-112">Ennaltaehkäisevät huoltotyöt useille samantyyppistä kunnossapitoa vaativille käyttökohteille.</span><span class="sxs-lookup"><span data-stu-id="ba36f-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="ba36f-113">Ylläpitopyyntö</span><span class="sxs-lookup"><span data-stu-id="ba36f-113">Maintenance request</span></span>   | <span data-ttu-id="ba36f-114">Manuaalisesti luotava käyttöomaisuuserän huolto- tai korjauspyyntö, joka voidaan muuntaa työtilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="ba36f-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="ba36f-115">Valitse **Resurssien hallinta** > **Yhteiset** > **Kaikki ylläpitoaikataulut** tai **Avoimet ylläpitoaikataulurivit** tai **Avoimet ylläpitoaikataulupoolit**.</span><span class="sxs-lookup"><span data-stu-id="ba36f-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="ba36f-116">Valitse ajoitetut ylläpitotyöt, joille haluat luoda työtilauksen, ja valitse sitten **Työtilaus**.</span><span class="sxs-lookup"><span data-stu-id="ba36f-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="ba36f-117">Valittujen rivien ennustetuntien kokonaismäärä näkyy **Ylläpitoennusteen tunnit** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="ba36f-117">The total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="ba36f-118">Valitse **Parametrit**-osassa, kuinka monta työtilausta tulee tehdä.</span><span class="sxs-lookup"><span data-stu-id="ba36f-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="ba36f-119">Voit luoda yhden työtilauksen ylläpitoaikatauluriviä kohden tai useita työtilauksia, jotka perustuvat **Yksi työtilaus per** -osan valintoihin.</span><span class="sxs-lookup"><span data-stu-id="ba36f-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="ba36f-120">Valitse **Työtilaustyyppi**, jota käytetään kaikissa työtilauksissa, jotka luot.</span><span class="sxs-lookup"><span data-stu-id="ba36f-120">Select a **Work order type** that will be used on all the work orders you create.</span></span>

5. <span data-ttu-id="ba36f-121">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ba36f-121">Click **OK**.</span></span> <span data-ttu-id="ba36f-122">Yksi tai monta työtilausta luodaan.</span><span class="sxs-lookup"><span data-stu-id="ba36f-122">One or more work orders are created.</span></span>

![Kuva 1](media/18-preventive-maintenance.png)

