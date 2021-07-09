---
title: Suunniteltujen tilausten tarkasteleminen, hallinta ja hyväksyminen
description: Tässä ohjeaiheessa on tietoja suunnittelun optimoinnin suunniteltujen tilausten tarkastelusta, hallinnasta ja hyväksymisestä.
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 71ec26bea2063bcf8b6d302a7ece804b3ac934b3
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304364"
---
# <a name="view-manage-and-approve-planned-orders"></a><span data-ttu-id="11e4e-103">Suunniteltujen tilausten tarkasteleminen, hallinta ja hyväksyminen</span><span class="sxs-lookup"><span data-stu-id="11e4e-103">View, manage, and approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11e4e-104">Tässä ohjeaiheessa on tietoja suunnittelun optimoinnin suunniteltujen tilausten tarkastelusta, hallinnasta ja hyväksymisestä.</span><span class="sxs-lookup"><span data-stu-id="11e4e-104">This topic provides information about how to view, manage, and approve planned orders in Planning Optimization.</span></span>

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a><span data-ttu-id="11e4e-105">Suunniteltujen tilausten tarkasteleminen ja hallinta</span><span class="sxs-lookup"><span data-stu-id="11e4e-105">View and manage planned orders</span></span>

<span data-ttu-id="11e4e-106">Voit tarkastella ja hallita suunniteltuja tilauksia minkä tahansa suunnitellun tilauksen luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="11e4e-106">You can view and manage planned orders on any planned orders list page.</span></span> <span data-ttu-id="11e4e-107">Siirry yhteen seuraavista paikoista sen mukaan, minkä tyyppisiä suunniteltuja tilauksia haluat käyttää:</span><span class="sxs-lookup"><span data-stu-id="11e4e-107">Go to one of the following places, depending on the type of planned orders that you want to work with:</span></span>

- <span data-ttu-id="11e4e-108">Pääsuunnittelu \> Työtila \> Pääsuunnittelu</span><span class="sxs-lookup"><span data-stu-id="11e4e-108">Master planning \> Workspaces \> Master planning</span></span>
- <span data-ttu-id="11e4e-109">Pääsuunnittelu \> Pääsuunnittelu \> Suunnitellut tilaukset</span><span class="sxs-lookup"><span data-stu-id="11e4e-109">Master planning \> Master planning \> Planned orders</span></span>
- <span data-ttu-id="11e4e-110">Tuotannonhallinta \> Tuotantotilaukset \> Suunnitellut tuotantotilaukset</span><span class="sxs-lookup"><span data-stu-id="11e4e-110">Production control \> Production orders \> Planned production orders</span></span>
- <span data-ttu-id="11e4e-111">Hankinta \> Ostotilaukset \> Suunnitellut ostotilaukset</span><span class="sxs-lookup"><span data-stu-id="11e4e-111">Procurement and sourcing \> Purchase orders \> Planned purchase orders</span></span>
- <span data-ttu-id="11e4e-112">Varastonhallinta \> Saapuvat tilaukset \> Suunnitellut siirrot</span><span class="sxs-lookup"><span data-stu-id="11e4e-112">Inventory management \> Inbound orders \> Planned transfers</span></span>
- <span data-ttu-id="11e4e-113">Varastonhallinta \> Lähtevät tilaukset \> Suunnitellut siirrot</span><span class="sxs-lookup"><span data-stu-id="11e4e-113">Inventory management \> Outbound orders \> Planned transfers</span></span>

## <a name="view-and-edit-the-status-of-planned-orders"></a><span data-ttu-id="11e4e-114">Tarkastele ja muokkaa suunniteltujen tilausten tilaa</span><span class="sxs-lookup"><span data-stu-id="11e4e-114">View and edit the status of planned orders</span></span>

<span data-ttu-id="11e4e-115">Kunkin suunnitellun tilauksen **Tila**-kentän avulla voit seurata etenemistäsi tai muuttaa suunnitellun tilauksen käsittelyjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="11e4e-115">You can use the **Status** field of each planned order to help track your progress or change how a planned order will be processed.</span></span> <span data-ttu-id="11e4e-116">Seuraavat **Tila**-arvot ovat käytettävissä:</span><span class="sxs-lookup"><span data-stu-id="11e4e-116">The following **Status** values are available:</span></span>

- <span data-ttu-id="11e4e-117">**Käsittelemätön** – Kun pääsuunnittelu luo suunniteltuja tilauksia, niille annetaan tämä tila.</span><span class="sxs-lookup"><span data-stu-id="11e4e-117">**Unprocessed** – When master planning generates planned orders, they are given this status.</span></span> <span data-ttu-id="11e4e-118">Tässä tilassa olevat suunnitellut tilaukset poistetaan seuraavan suunnittelun suorittamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="11e4e-118">Planned orders that have this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="11e4e-119">**Valmis** – Tämä tila ilmaisee, että suunniteltu tilaus on valmis.</span><span class="sxs-lookup"><span data-stu-id="11e4e-119">**Completed** – This status indicates that the planned order has been completed.</span></span> <span data-ttu-id="11e4e-120">Jos et halua vahvistaa suunniteltua tilausta, voit muuttaa sen tilaksi manuaalisesti *Valmis*.</span><span class="sxs-lookup"><span data-stu-id="11e4e-120">If you decide not to firm a planned order, you can manually change its status to *Completed*.</span></span> <span data-ttu-id="11e4e-121">Huomaa, että *Käsittelemätön*- ja *Valmis*-tiloja käsitellään järjestelmässä samalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="11e4e-121">Note that the system treats the *Unprocessed* and *Completed* statuses in the same way.</span></span>
- <span data-ttu-id="11e4e-122">**Hyväksytty** – Tämä tila ilmaisee, että suunniteltu tilaus on hyväksytty vahvistettavaksi.</span><span class="sxs-lookup"><span data-stu-id="11e4e-122">**Approved** – This status indicates that the planned order is approved for firming.</span></span> <span data-ttu-id="11e4e-123">Jos haluat vahvistaa suunnitellun tilauksen, voit muuttaa sen tilaksi *Hyväksytty*.</span><span class="sxs-lookup"><span data-stu-id="11e4e-123">If you want to firm a planned order, you can change its status to *Approved*.</span></span> <span data-ttu-id="11e4e-124">Jos haluat säilyttää suunniteltuun tilaukseen tehdyt muutokset tai jos aiot vahvistaa suunnitellun tilauksen, muuta sen tilaksi *Hyväksytty*.</span><span class="sxs-lookup"><span data-stu-id="11e4e-124">If you want to keep the edits that have been made to a planned order, or if you're planning to firm a planned order, change its status to *Approved*.</span></span> <span data-ttu-id="11e4e-125">Suunnitellut tilaukset, joiden tila on *Hyväksytty*, pidetään valmiina. Niiden toimitusta odotetaan pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="11e4e-125">Planned orders that have a status of *Approved* are considered fixed and expected supply by master planning.</span></span> <span data-ttu-id="11e4e-126">Siksi niitä ei muokata tai poisteta myöhemmin pääsuunnittelun suorituksissa.</span><span class="sxs-lookup"><span data-stu-id="11e4e-126">Therefore, they aren't modified or deleted during later master planning runs.</span></span> <span data-ttu-id="11e4e-127">Tämän käytöksen saavuttamiseksi suunnittelulogiikka kopioi *Hyväksytty*-tilassa olevat suunnitellut tilaukset vanhasta suunnitelmaversiosta uuteen suunnitelmaversioon pääsuunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="11e4e-127">To achieve this behavior, the planning logic copies planned orders that have a status of *Approved* from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="11e4e-128">Huomaa, että *Hyväksytty*-tilassa olevia suunniteltuja tilauksia pidetään tarjontana vain tietyssä pääsuunnitelmassa.</span><span class="sxs-lookup"><span data-stu-id="11e4e-128">Note that planned orders that have a status of *Approved* are considered supply only within the specific master plan.</span></span>

<span data-ttu-id="11e4e-129">Jos haluat muuttaa yksittäisen suunnitellun tilauksen tilan, [avaa jokin suunniteltujen tilausten luettelosivu](#view-planned-orders), avaa tilaus ja noudata sitten toista seuraavista vaiheista:</span><span class="sxs-lookup"><span data-stu-id="11e4e-129">To change the status of a single planned order, [open any planned orders list page](#view-planned-orders), open the order, and then follow one of these steps:</span></span>

- <span data-ttu-id="11e4e-130">Muuta **Yleinen**-pikavälilehdellä **Tila**-kentän arvoa.</span><span class="sxs-lookup"><span data-stu-id="11e4e-130">On the **General** FastTab, change the value of the **Status** field.</span></span>
- <span data-ttu-id="11e4e-131">Valitse toimintoruudun **Suunniteltu tilaus**-välilehden **Prosessi**-ryhmässä **Muuta tila**.</span><span class="sxs-lookup"><span data-stu-id="11e4e-131">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="11e4e-132">Voit merkitä tilauksen hyväksytyksi valitsemalla toimintoruudussa **Hyväksy**.</span><span class="sxs-lookup"><span data-stu-id="11e4e-132">On the Action Pane, select **Approve** to mark the order as approved.</span></span>

<span data-ttu-id="11e4e-133">Jos haluat muuttaa usean suunnitellun tilauksen tilaa samanaikaisesti, [avaa jokin suunniteltujen tilausten luettelosivu](#view-planned-orders), valitse kunkin muutettavan tilauksen valintaruutu ja tee jokin seuraavista vaiheista:</span><span class="sxs-lookup"><span data-stu-id="11e4e-133">To change the status of several planned orders at the same time, [open any planned orders list page](#view-planned-orders), select the check box for each order that you want to change, and then follow one of these steps:</span></span>

- <span data-ttu-id="11e4e-134">Valitse toimintoruudun **Suunniteltu tilaus**-välilehden **Prosessi**-ryhmässä **Muuta tila**.</span><span class="sxs-lookup"><span data-stu-id="11e4e-134">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="11e4e-135">Voit merkitä tilaukset hyväksytyksi valitsemalla toimintoruudussa **Hyväksy**.</span><span class="sxs-lookup"><span data-stu-id="11e4e-135">On the Action Pane, select **Approve** to mark the orders as approved.</span></span>

## <a name="approve-planned-orders"></a><span data-ttu-id="11e4e-136">Suunniteltujen tilausten hyväksyminen</span><span class="sxs-lookup"><span data-stu-id="11e4e-136">Approve planned orders</span></span>

<span data-ttu-id="11e4e-137">Suunniteltujen tilausten hyväksyminen on valinnainen vaihe. Se tehdään luotaessa vahvistettu tilaus suunnitellusta tilauksesta.</span><span class="sxs-lookup"><span data-stu-id="11e4e-137">Approval of planned orders is an optional step in the process of creating a firmed order from a planned order.</span></span>

<span data-ttu-id="11e4e-138">Seuraavassa kuvassa näytetään, kuinka voit käyttää kullekin suunnitellulle tilaukselle määritettyä **Tila**-arvoa hyväksyntätyönkulun käyttöönotossa.</span><span class="sxs-lookup"><span data-stu-id="11e4e-138">The following illustration shows how you can use the **Status** value that is assigned to each planned order to implement an approval workflow.</span></span> <span data-ttu-id="11e4e-139">Voit ottaa hyväksyntäprosessin käyttöön säätämällä kunkin suunnitellun tilauksen **Tila**-arvon manuaalisesti edellisessä osassa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="11e4e-139">To implement an approval process, manually adjust the **Status** value for each planned order as described in the previous section.</span></span>

![Suunniteltu tilausten työnkulku](media/approved-planned-orders-1.png)

> [!TIP]
> <span data-ttu-id="11e4e-141">On suositeltavaa hyväksyä kaikki muokatut suunnitellut tilaukset.</span><span class="sxs-lookup"><span data-stu-id="11e4e-141">We recommend that you approve any modified planned orders.</span></span> <span data-ttu-id="11e4e-142">Muussa tapauksessa seuraava suunnitteluajo ohittaa ja korvaa muokkaukset.</span><span class="sxs-lookup"><span data-stu-id="11e4e-142">Otherwise, the edits will be ignored and overwritten by the next planning run.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="11e4e-143">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="11e4e-143">Additional resources</span></span>

- [<span data-ttu-id="11e4e-144">Vahvista suunnitellut tilaukset</span><span class="sxs-lookup"><span data-stu-id="11e4e-144">Firm planned orders</span></span>](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
