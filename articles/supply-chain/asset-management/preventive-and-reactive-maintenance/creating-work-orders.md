---
title: Työtilauksien luonti
description: Tässä ohjeaiheessa selitetään, miten työtilaukset luodaan käyttöomaisuuden hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427113"
---
# <a name="creating-work-orders"></a><span data-ttu-id="4abfb-103">Työtilauksien luonti</span><span class="sxs-lookup"><span data-stu-id="4abfb-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4abfb-104">Kun olet ajoittanut ennaltaehkäiseviä kunnossapitotöitä, seuraava vaihe on töiden työtilausten luominen.</span><span class="sxs-lookup"><span data-stu-id="4abfb-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="4abfb-105">Sen voi tehdä ylläpitoaikatauluissa.</span><span class="sxs-lookup"><span data-stu-id="4abfb-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="4abfb-106">Ylläpitoaikataulun ajoitettujen töiden viitetyypit voivat olla erilaiset:</span><span class="sxs-lookup"><span data-stu-id="4abfb-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="4abfb-107">Viitetyyppi</span><span class="sxs-lookup"><span data-stu-id="4abfb-107">Reference type</span></span> | <span data-ttu-id="4abfb-108">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="4abfb-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4abfb-109">Ylläpitosuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="4abfb-109">Maintenance plans</span></span>     | <span data-ttu-id="4abfb-110">Ennaltaehkäisevät huoltotyöt, jotka perustuvat huoltosuunnitelmatyyppeihin "aika" tai "laskuri".</span><span class="sxs-lookup"><span data-stu-id="4abfb-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="4abfb-111">Ylläpitokierrokset</span><span class="sxs-lookup"><span data-stu-id="4abfb-111">Maintenance rounds</span></span>    | <span data-ttu-id="4abfb-112">Ennaltaehkäisevät huoltotyöt useille samantyyppistä kunnossapitoa vaativille käyttökohteille.</span><span class="sxs-lookup"><span data-stu-id="4abfb-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="4abfb-113">Ylläpitopyyntö</span><span class="sxs-lookup"><span data-stu-id="4abfb-113">Maintenance request</span></span>   | <span data-ttu-id="4abfb-114">Manuaalisesti luotava käyttöomaisuuserän huolto- tai korjauspyyntö, joka voidaan muuntaa työtilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="4abfb-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="4abfb-115">Valitse **Resurssien hallinta** > **Yhteiset** > **Kaikki ylläpitoaikataulut** tai **Avoimet ylläpitoaikataulurivit** tai **Avoimet ylläpitoaikataulupoolit**.</span><span class="sxs-lookup"><span data-stu-id="4abfb-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="4abfb-116">Valitse ajoitetut ylläpitotyöt, joille haluat luoda työtilauksen, ja valitse sitten **Työtilaus**.</span><span class="sxs-lookup"><span data-stu-id="4abfb-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="4abfb-117">Valittujen rivien ennustetuntien kokonaismäärä näkyy **Luo työtilauksia** - valintaikkunan **Ylläpitoennusteen tunnit** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="4abfb-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="4abfb-118">Valitse **Parametrit**-osassa, kuinka monta työtilausta tulee tehdä.</span><span class="sxs-lookup"><span data-stu-id="4abfb-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="4abfb-119">Voit luoda yhden työtilauksen ylläpitoaikatauluriviä kohden tai useita työtilauksia, jotka perustuvat **Yksi työtilaus per** -osan valintoihin.</span><span class="sxs-lookup"><span data-stu-id="4abfb-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="4abfb-120">Valitse **Työtilaustyyppi**, jota käytetään kaikissa työtilauksissa, jotka luot.</span><span class="sxs-lookup"><span data-stu-id="4abfb-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="4abfb-121">Seuraavassa kuvassa on esimerkki **Luo työtilauksia** -valintaikkunasta.</span><span class="sxs-lookup"><span data-stu-id="4abfb-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![Kuva 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="4abfb-123">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="4abfb-123">Click **OK**.</span></span> <span data-ttu-id="4abfb-124">Yksi tai monta työtilausta luodaan.</span><span class="sxs-lookup"><span data-stu-id="4abfb-124">One or more work orders are created.</span></span>

