---
title: Suoraan johdetut vahvistetut tilaukset käsitellään tarkistustyönkulussa.
description: Suoraan johdetut vahvistetut tilaukset käsitellään työnkulussa, jonka tilana on Tarkistettavana.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026481"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a><span data-ttu-id="95997-103">Suoraan johdetut vahvistetut tilaukset käsitellään tarkistustyönkulussa.</span><span class="sxs-lookup"><span data-stu-id="95997-103">Directly derived firmed orders are processed by an in-review workflow</span></span>

<span data-ttu-id="95997-104">Tietopankin numero: 4612450</span><span class="sxs-lookup"><span data-stu-id="95997-104">KB number: 4612450</span></span>

## <a name="symptoms"></a><span data-ttu-id="95997-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="95997-105">Symptoms</span></span>

<span data-ttu-id="95997-106">Suoraan johdetut vahvistetut tilaukset käsitellään työnkulussa, jonka tilana on *Tarkistettavana*.</span><span class="sxs-lookup"><span data-stu-id="95997-106">Directly derived firmed orders are processed by a workflow that has a status of *In-review*.</span></span>

## <a name="resolution"></a><span data-ttu-id="95997-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="95997-107">Resolution</span></span>

<span data-ttu-id="95997-108">Kun muutosten seuranta on käytössä, *Tarkistettavana*-tila on määritetty vahvistetuille johdetuille tilauksille (alihankintaostotilaukset).</span><span class="sxs-lookup"><span data-stu-id="95997-108">When change tracking is enabled, a status of *In-review* is assigned to firmed derived orders (subcontract purchase orders).</span></span> <span data-ttu-id="95997-109">Jos ostotilaus on johdettu (alihankintaostotilaus), se lähetetään vain työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="95997-109">Therefore, if a purchase order is derived (a subcontract purchase order), it's only submitted to a workflow.</span></span> <span data-ttu-id="95997-110">Jos ostotilaus on vahvistettu suunniteltu ostotilaus, se hyväksytään automaattisesti, jotta suunnittelumoduuli ei luo uusia suunniteltuja tilauksia ostotilauksen ollessa edelleen *Luonnos*-tilassa.</span><span class="sxs-lookup"><span data-stu-id="95997-110">If a purchase order is a firmed planned purchase order, it's automatically approved to ensure that the planning engine doesn't create new planned orders while the purchase order is still in *Draft* status.</span></span>
