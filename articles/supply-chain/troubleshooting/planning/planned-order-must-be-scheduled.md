---
title: Suunniteltu tuotantotilaus on ajoitettava ennen kuin se voidaan vahvistaa
description: Kun yrität vahvistaa suunnitellun tilauksen, saat virhesanoman, jossa todetaan, että tilaus on ajoitettava, ennen kuin se voidaan vahvistaa.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294069"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a><span data-ttu-id="ea2a2-103">Suunniteltu tuotantotilaus on ajoitettava ennen kuin se voidaan vahvistaa</span><span class="sxs-lookup"><span data-stu-id="ea2a2-103">Planned production order must be scheduled before it can be firmed</span></span>

<span data-ttu-id="ea2a2-104">Virhekoodi: SYS309802</span><span class="sxs-lookup"><span data-stu-id="ea2a2-104">Error code: SYS309802</span></span>

## <a name="symptoms"></a><span data-ttu-id="ea2a2-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="ea2a2-105">Symptoms</span></span>

<span data-ttu-id="ea2a2-106">Kun yrität vahvistaa suunnitellun tilauksen, näyttöön tulee seuraava virhesanoma:</span><span class="sxs-lookup"><span data-stu-id="ea2a2-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="ea2a2-107">Suunniteltu tuotantotilaus on ajoitettava ennen kuin se voidaan vahvistaa.</span><span class="sxs-lookup"><span data-stu-id="ea2a2-107">The planned production order must be scheduled before it can be firmed.</span></span>

## <a name="cause"></a><span data-ttu-id="ea2a2-108">Syy</span><span class="sxs-lookup"><span data-stu-id="ea2a2-108">Cause</span></span>

<span data-ttu-id="ea2a2-109">Ajoitetut aloitus- ja päättymispäivät eivät voi olla tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="ea2a2-109">The scheduled start and end dates can't be blank.</span></span>

## <a name="resolution"></a><span data-ttu-id="ea2a2-110">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ea2a2-110">Resolution</span></span>

<span data-ttu-id="ea2a2-111">Voit määrittää suunnitellun tilauksen alkamis- ja päättymispäivät noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="ea2a2-111">To specify start and end dates for the planned order, follow these steps.</span></span>

1. <span data-ttu-id="ea2a2-112">Valitse **Pääsuunnittelu \> Pääsuunnittelu \> Suunnitellut tilaukset**.</span><span class="sxs-lookup"><span data-stu-id="ea2a2-112">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="ea2a2-113">Avaa asianmukainen suunniteltu tilaus.</span><span class="sxs-lookup"><span data-stu-id="ea2a2-113">Open the relevant planned order.</span></span>
1. <span data-ttu-id="ea2a2-114">Määritä **Yleiset**-pikavälilehden **Ajoitettu**-osassa päivämäärät **Aloitus**- ja **Päättymispäivä**-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="ea2a2-114">On the **General** FastTab, in the **Scheduled** section, specify dates in the **Start date** and **End date** fields.</span></span>
