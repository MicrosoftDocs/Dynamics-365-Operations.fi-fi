---
title: Tositetta ei luoda
description: Tämä ohjeaihe sisältää vianmääritystietoja, jotka voivat auttaa, kun tosite pitäisi luoda mutta niin ei tehdä.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: eafc9110ec58be5083569188d59b67a62e86c85d
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947634"
---
# <a name="voucher-isnt-generated"></a><span data-ttu-id="af142-103">Tositetta ei luoda</span><span class="sxs-lookup"><span data-stu-id="af142-103">Voucher isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af142-104">Jos tosite pitäisi luoda, mutta **Tositetapahtumat**-sivulla ei ole tositteita, suorita tämän ongelman vianmäärityksessä tarvittavat seuraavien osien vaiheet.</span><span class="sxs-lookup"><span data-stu-id="af142-104">If a voucher should be generated, but the **Voucher transactions** page doesn't show any vouchers, follow the steps in the following sections as required to troubleshoot this issue.</span></span>

<span data-ttu-id="af142-105">[![Tositetapahtumat-sivu, jolla ei ole tositteita](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="af142-105">[![Voucher transactions page that has no vouchers](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span></span>

## <a name="check-the-tax-applicability"></a><span data-ttu-id="af142-106">Veron käytettävyyden tarkistus</span><span class="sxs-lookup"><span data-stu-id="af142-106">Check the tax applicability</span></span>

1. <span data-ttu-id="af142-107">Valitse **Vero** \> **Kausittaiset tehtävät** \> **Alareskontran kirjauskansioviennit, joita ei ole vielä siirretty**.</span><span class="sxs-lookup"><span data-stu-id="af142-107">Go to **Tax** \> **Periodic tasks** \> **Subledger journal entries not yet transferred**.</span></span>
2. <span data-ttu-id="af142-108">Jos kirjauskansiotietue on olemassa, valitse se ja valitse sitten **Siirrä nyt**.</span><span class="sxs-lookup"><span data-stu-id="af142-108">If there is a journal record, select it, and then select **Transfer now**.</span></span>

    <span data-ttu-id="af142-109">[![Siirrä nyt -painike Alareskontran kirjauskansioviennit, joita ei ole vielä siirretty -sivulla](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="af142-109">[![Transfer now button on the Subledger journal entries not yet transferred page](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span></span>

3. <span data-ttu-id="af142-110">Avaa **Tositetapahtumat**-sivu uudelleen ja tarkista, onko tosite luotu.</span><span class="sxs-lookup"><span data-stu-id="af142-110">Open the **Voucher transactions** page again to see whether the voucher was generated.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="af142-111">Määritä, onko mukautus olemassa</span><span class="sxs-lookup"><span data-stu-id="af142-111">Determine whether customization exists</span></span>

<span data-ttu-id="af142-112">Jos olet suorittanut edellisen osan vaiheet, mutta et ole löytänyt ongelmaa, selvitä, onko mukautus olemassa.</span><span class="sxs-lookup"><span data-stu-id="af142-112">If you've completed the steps in the previous section but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="af142-113">Jos mukautusta ei ole, luo Microsoftin huoltopyyntö lisätuen saamiseksi.</span><span class="sxs-lookup"><span data-stu-id="af142-113">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
