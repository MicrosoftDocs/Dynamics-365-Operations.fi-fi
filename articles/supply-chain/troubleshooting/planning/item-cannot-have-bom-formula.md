---
title: Nimikkeellä ei voi olla tuoterakennetta tai kaavaa
description: Kun yrität vahvistaa tilauksen, näyttöön tulee virhesanoma nimikkeen oikeellisuustarkistuksen aikana. Se määrittää, että nimikkeellä ei voi olla tuoterakennetta tai kaavaa.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294065"
---
# <a name="item-cant-have-a-bom-or-formula"></a><span data-ttu-id="776c4-104">Nimikkeellä ei voi olla tuoterakennetta tai kaavaa</span><span class="sxs-lookup"><span data-stu-id="776c4-104">Item can't have a BOM or formula</span></span>

<span data-ttu-id="776c4-105">Virhekoodi: PRO2614</span><span class="sxs-lookup"><span data-stu-id="776c4-105">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="776c4-106">Oireet</span><span class="sxs-lookup"><span data-stu-id="776c4-106">Symptoms</span></span>

<span data-ttu-id="776c4-107">Kun yrität vahvistaa tilauksen, näyttöön tulee seuraava virhesanoma nimikkeen oikeellisuustarkistuksen aikana:</span><span class="sxs-lookup"><span data-stu-id="776c4-107">When you try to firm an order, you receive the following error message during item validation:</span></span>

> <span data-ttu-id="776c4-108">Nimikkeellä ei voi olla tuoterakennetta tai kaavaa</span><span class="sxs-lookup"><span data-stu-id="776c4-108">Item cannot have a BOM or formula</span></span>

## <a name="resolution"></a><span data-ttu-id="776c4-109">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="776c4-109">Resolution</span></span>

<span data-ttu-id="776c4-110">Nimikkeiden, joissa on tuoterakenne tai kaava, on oltava *suunnittelunimike*-, *tuoterakenne*- tai *kaava* -tyyppi.</span><span class="sxs-lookup"><span data-stu-id="776c4-110">Items that have a bill of materials (BOM) or formula must be of the *Planning item*, *BOM*, or *formula* type.</span></span> <span data-ttu-id="776c4-111">Voit muuttaa nimiketyypin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="776c4-111">To change the type of an item, follow these steps.</span></span>

1. <span data-ttu-id="776c4-112">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="776c4-112">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="776c4-113">Avaa asiaankuuluva tuote.</span><span class="sxs-lookup"><span data-stu-id="776c4-113">Open the relevant product.</span></span>
1. <span data-ttu-id="776c4-114">Nimike on määritettävä *Suunnittelunimikkeeksi*, *Tuoterakenteeksi* tai *Kaavaksi* **Tuotantotyyppi**-kentän **Kehittäjä**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="776c4-114">On the **Engineer** FastTab, set the **Production type** field to *Planning item*, *BOM*, or *formula*.</span></span>
