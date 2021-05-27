---
title: Asiakkaalle näkyvää myyntitilausta ei voi laskuttaa
description: Et voi enää laskuttaa alkuperäistä myyntitilausta ja alkuperäistä suoratoimitusostotilausta sen jälkeen, kun Kirjaa lasku automaattisesti -asetus on käytössä.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026469"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a><span data-ttu-id="b06a1-103">Asiakkaalle näkyvää myyntitilausta ei voi laskuttaa</span><span class="sxs-lookup"><span data-stu-id="b06a1-103">You can't invoice a customer-facing sales order</span></span>

<span data-ttu-id="b06a1-104">Tietopankin numero: 4611793</span><span class="sxs-lookup"><span data-stu-id="b06a1-104">KB number: 4611793</span></span>

## <a name="symptoms"></a><span data-ttu-id="b06a1-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="b06a1-105">Symptoms</span></span>

<span data-ttu-id="b06a1-106">Et voi enää laskuttaa alkuperäistä myyntitilausta ja alkuperäistä suoratoimitusostotilausta sen jälkeen, kun **Kirjaa lasku automaattisesti** -asetus on käytössä toimittajan **Konsernin sisäinen** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b06a1-106">You can no longer invoice the original sales order and the original direct delivery purchase order after you enable the **Post invoice automatically** option on the **Intercompany** page for a vendor.</span></span>

## <a name="resolution"></a><span data-ttu-id="b06a1-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="b06a1-107">Resolution</span></span>

<span data-ttu-id="b06a1-108">Konsernin sisäisen ja suoratoimitustilauslaskujen synkronointia ohjaavat ja pakottavat parametrit, jotka on kuvattu kohdassa [Konsernin sisäisen tilauksen kirjausparametrien määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span><span class="sxs-lookup"><span data-stu-id="b06a1-108">The synchronization behavior for intercompany and direct delivery order invoices is controlled and forced by the parameters that are described in [Set up parameters to post an intercompany order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span></span>

<span data-ttu-id="b06a1-109">Kun olet määrittänyt nämä parametrit, sinun on ensin laskutettava konsernin sisäinen myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="b06a1-109">After you set those parameters, you must invoice the intercompany sales order first.</span></span> <span data-ttu-id="b06a1-110">Tämän jälkeen alkuperäiset myyntitilaukset ja ostotilaukset synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="b06a1-110">The original sales orders and purchase orders will then be synchronized.</span></span>
