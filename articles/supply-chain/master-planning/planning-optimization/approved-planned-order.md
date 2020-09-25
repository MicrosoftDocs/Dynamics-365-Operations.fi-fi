---
title: Hyväksy suunnitellut tilaukset
description: Tässä ohjeaiheessa kuvataan suunnittelun optimoinnin tukemien suunniteltujen tilausten hyväksyntä.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b7975088be898ccecceb1f7be009cecff107f6e6
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759685"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="84154-103">Hyväksy suunnitellut tilaukset</span><span class="sxs-lookup"><span data-stu-id="84154-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="84154-104">Tässä ohjeaiheessa on tietoja suunnittelun optimoinnin suunniteltujen tilausten tilan päivittämisestä.</span><span class="sxs-lookup"><span data-stu-id="84154-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="84154-105">Huomaa, että suunniteltujen tilausten hyväksyminen on valinnainen vaihe. Se tehdään luotaessa vahvistettu tilaus suunnitellusta tilauksesta.</span><span class="sxs-lookup"><span data-stu-id="84154-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="84154-106">On suositeltavaa hyväksyä muutetut suunnitellut tilaukset. Muussa tapauksessa muokkaukset ohitetaan, ja seuraava suunnittelun suoritus korvaa ne.</span><span class="sxs-lookup"><span data-stu-id="84154-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![Suunniteltu tilausten työnkulku](media/approved-planned-orders-1.png)

<span data-ttu-id="84154-108">**Tila**-kentän avulla voit seurata edistymistä käyttämällä seuraavia arvoja:</span><span class="sxs-lookup"><span data-stu-id="84154-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="84154-109">**Käsittelemätön:** Kun pääsuunnittelu luo suunniteltuja tilauksia, suunniteltujen tilausten tilana on *Käsittelemätön*.</span><span class="sxs-lookup"><span data-stu-id="84154-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="84154-110">Tässä tilassa olevat suunnitellut tilaukset poistetaan seuraavan suunnittelun suorittamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="84154-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="84154-111">**Valmis:** Jos päätät olla vahvistamatta suunniteltua tilausta, voit muuttaa tilaksi *Valmis*. Näin osoitat, että tämän suunnitellun tilauksen arvioiminen on tehty.</span><span class="sxs-lookup"><span data-stu-id="84154-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="84154-112">Huomaa, että *Käsittelemätön*- ja *Valmis*-tiloja käsitellään järjestelmässä samalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="84154-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="84154-113">**Hyväksytty:** Jos haluat säilyttää muokkaukset tai suunnittelet suunnitellun tilauksen vahvistamista, muuta tilaksi *Hyväksytty*.</span><span class="sxs-lookup"><span data-stu-id="84154-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="84154-114">Suunniteltuja tilauksia, joiden tila on *Hyväksytty*, pidetään valmiina. Niiden toimitusta odotetaan pääsuunnittelussa. Niitä ei muokata tai poisteta myöhemmin pääsuunnittelun suorituksissa.</span><span class="sxs-lookup"><span data-stu-id="84154-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="84154-115">Tämän saavuttamiseksi suunnittelulogiikka kopioi *hyväksytyt* suunnitellut tilaukset vanhasta suunnitelmaversiosta uuteen suunnitelmaversioon pääsuunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="84154-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="84154-116">Huomaa, että *hyväksyttyjä* suunniteltuja tilauksia pidetään tarjontana vain tietyssä pääsuunnitelmassa.</span><span class="sxs-lookup"><span data-stu-id="84154-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="84154-117">Voit hallita suunniteltuja tilauksia **Pääsuunnittelu**-työtilassa, **Suunniteltu tilaus** -luettelossa tai **Suunnitellut tuotantotilaukset**-, **Suunnitellut ostotilaukset**- ja **Suunniteltu siirto** -luetteloissa.</span><span class="sxs-lookup"><span data-stu-id="84154-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>
