---
title: Hyväksy suunnitellut tilaukset
description: Tässä ohjeaiheessa kuvataan suunnittelun optimoinnin tukemien suunniteltujen tilausten hyväksyntä.
author: ChristianRytt
ms.date: 08/21/2020
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
ms.openlocfilehash: 6c215a89403f16336caae5c62cde6df469c4091c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825888"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="ccc52-103">Hyväksy suunnitellut tilaukset</span><span class="sxs-lookup"><span data-stu-id="ccc52-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ccc52-104">Tässä ohjeaiheessa on tietoja suunnittelun optimoinnin suunniteltujen tilausten tilan päivittämisestä.</span><span class="sxs-lookup"><span data-stu-id="ccc52-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="ccc52-105">Huomaa, että suunniteltujen tilausten hyväksyminen on valinnainen vaihe. Se tehdään luotaessa vahvistettu tilaus suunnitellusta tilauksesta.</span><span class="sxs-lookup"><span data-stu-id="ccc52-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="ccc52-106">On suositeltavaa hyväksyä muutetut suunnitellut tilaukset. Muussa tapauksessa muokkaukset ohitetaan, ja seuraava suunnittelun suoritus korvaa ne.</span><span class="sxs-lookup"><span data-stu-id="ccc52-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![Suunniteltu tilausten työnkulku](media/approved-planned-orders-1.png)

<span data-ttu-id="ccc52-108">**Tila**-kentän avulla voit seurata edistymistä käyttämällä seuraavia arvoja:</span><span class="sxs-lookup"><span data-stu-id="ccc52-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="ccc52-109">**Käsittelemätön:** Kun pääsuunnittelu luo suunniteltuja tilauksia, suunniteltujen tilausten tilana on *Käsittelemätön*.</span><span class="sxs-lookup"><span data-stu-id="ccc52-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="ccc52-110">Tässä tilassa olevat suunnitellut tilaukset poistetaan seuraavan suunnittelun suorittamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="ccc52-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="ccc52-111">**Valmis:** Jos päätät olla vahvistamatta suunniteltua tilausta, voit muuttaa tilaksi *Valmis*. Näin osoitat, että tämän suunnitellun tilauksen arvioiminen on tehty.</span><span class="sxs-lookup"><span data-stu-id="ccc52-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="ccc52-112">Huomaa, että *Käsittelemätön*- ja *Valmis*-tiloja käsitellään järjestelmässä samalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="ccc52-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="ccc52-113">**Hyväksytty:** Jos haluat säilyttää muokkaukset tai suunnittelet suunnitellun tilauksen vahvistamista, muuta tilaksi *Hyväksytty*.</span><span class="sxs-lookup"><span data-stu-id="ccc52-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="ccc52-114">Suunniteltuja tilauksia, joiden tila on *Hyväksytty*, pidetään valmiina. Niiden toimitusta odotetaan pääsuunnittelussa. Niitä ei muokata tai poisteta myöhemmin pääsuunnittelun suorituksissa.</span><span class="sxs-lookup"><span data-stu-id="ccc52-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="ccc52-115">Tämän saavuttamiseksi suunnittelulogiikka kopioi *hyväksytyt* suunnitellut tilaukset vanhasta suunnitelmaversiosta uuteen suunnitelmaversioon pääsuunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="ccc52-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="ccc52-116">Huomaa, että *hyväksyttyjä* suunniteltuja tilauksia pidetään tarjontana vain tietyssä pääsuunnitelmassa.</span><span class="sxs-lookup"><span data-stu-id="ccc52-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="ccc52-117">Voit hallita suunniteltuja tilauksia **Pääsuunnittelu**-työtilassa, **Suunniteltu tilaus** -luettelossa tai **Suunnitellut tuotantotilaukset**-, **Suunnitellut ostotilaukset**- ja **Suunniteltu siirto** -luetteloissa.</span><span class="sxs-lookup"><span data-stu-id="ccc52-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]