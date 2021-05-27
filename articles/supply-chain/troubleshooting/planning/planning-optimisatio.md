---
title: Suunniteltu ostotilaus luodaan, kun osto on negatiivisten päivien sisällä
description: Jos kattavuuskoodi on Minimi/maksimi, suunnittelun optimointi luo suunnitellun ostotilauksen, kun osto on negatiivisten päivien sisällä.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026479"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a><span data-ttu-id="417da-103">Suunniteltu ostotilaus luodaan, kun osto on negatiivisten päivien sisällä</span><span class="sxs-lookup"><span data-stu-id="417da-103">Planned purchase order is created when a purchase exists within negative days</span></span>

<span data-ttu-id="417da-104">Tietopankin numero: 4614298</span><span class="sxs-lookup"><span data-stu-id="417da-104">KB number: 4614298</span></span>

## <a name="symptoms"></a><span data-ttu-id="417da-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="417da-105">Symptoms</span></span>

<span data-ttu-id="417da-106">Jos kattavuuskoodi on *Minimi/maksimi*, suunnittelun optimointi luo suunnitellun ostotilauksen, kun osto on negatiivisten päivien sisällä.</span><span class="sxs-lookup"><span data-stu-id="417da-106">If the coverage code is *Min/max*, Planning Optimization creates a planned purchase order when a purchase exists within negative days.</span></span>

## <a name="resolution"></a><span data-ttu-id="417da-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="417da-107">Resolution</span></span>

<span data-ttu-id="417da-108">Suunnittelun optimointi ei tue negatiivisia päiviä.</span><span class="sxs-lookup"><span data-stu-id="417da-108">Planning Optimization doesn't support negative days.</span></span> <span data-ttu-id="417da-109">Se varmistaa kuitenkin aina, ettei suunniteltuja tilauksia ajoiteta läpimenoajan sisällä suhteessa nykyiseen päivämäärään.</span><span class="sxs-lookup"><span data-stu-id="417da-109">However, it always ensures that planned orders won't be scheduled within the lead time relative to the current date.</span></span> <span data-ttu-id="417da-110">Esimerkiksi oston läpimenoaika on 10 päivää, ja ostotilauksen odotetaan saapuvan kahdeksan päivää tästä päivästä.</span><span class="sxs-lookup"><span data-stu-id="417da-110">For example, the purchase lead time is 10 days, and a purchase order is expected to arrive eight days from today.</span></span> <span data-ttu-id="417da-111">Tässä tapauksessa ostotilausta käytetään kysynnän toimituksena, joka on viisi päivää tästä päivästä alkaen.</span><span class="sxs-lookup"><span data-stu-id="417da-111">In this case, the purchase order will be used as supply for demand that is five days from today.</span></span>

<span data-ttu-id="417da-112">Siksi on suositeltavaa säätää läpimenoaikoja siten, että ne kattavat kaikki skenaariot (tai lähes kaikki).</span><span class="sxs-lookup"><span data-stu-id="417da-112">Therefore, we recommend that you adjust your lead times to cover all (or almost all) of your scenarios.</span></span>
