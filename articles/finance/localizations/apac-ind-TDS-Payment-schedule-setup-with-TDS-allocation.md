---
title: Määritä maksusuunnitelmia, joissa on TDS-kohdistus
description: Tässä aiheessa kuvataan, miten maksusuunnitelmat määritetään Vero vähennettynä lähteissä (TDS) -kohdistuksella.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023216"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a><span data-ttu-id="4637f-103">Määritä maksusuunnitelmia, joissa on TDS-kohdistus</span><span class="sxs-lookup"><span data-stu-id="4637f-103">Set up payment schedules with TDS allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4637f-104">Tässä aiheessa kuvataan, miten maksusuunnitelmat määritetään Vero vähennettynä lähteissä (TDS) -kohdistuksella.</span><span class="sxs-lookup"><span data-stu-id="4637f-104">This topic explains how to set up payment schedules with Tax Deducted at Source (TDS) allocation.</span></span>

1. <span data-ttu-id="4637f-105">Siirry kohtaan **Ostoreskontra \> Maksun asetukset \> Maksusuunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="4637f-105">Go to **Accounts payable \> Payment setup \> Payment schedules**.</span></span>

    <span data-ttu-id="4637f-106">[![Maksusuunnitelmat-sivu](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span><span class="sxs-lookup"><span data-stu-id="4637f-106">[![Payment schedules page](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span></span>

2. <span data-ttu-id="4637f-107">Valitse toimintoruudusta **Uusi**, jos haluat luoda maksusuunnitelman, ja syötä tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="4637f-107">On the Action Pane, select **New** to create a payment schedule, and enter the required details.</span></span>
3. <span data-ttu-id="4637f-108">Valitse **Kohdistus**-kentässä maksutapa, jota käytetään maksusuunnitelman maksun kohdistuksena:</span><span class="sxs-lookup"><span data-stu-id="4637f-108">In the **Allocation** field, select the method to use to allocate the payment for the payment schedule:</span></span>

    - <span data-ttu-id="4637f-109">Yhteensä</span><span class="sxs-lookup"><span data-stu-id="4637f-109">Total</span></span>
    - <span data-ttu-id="4637f-110">Kiinteä summa</span><span class="sxs-lookup"><span data-stu-id="4637f-110">Fixed amount</span></span>
    - <span data-ttu-id="4637f-111">Kiinteä määrä</span><span class="sxs-lookup"><span data-stu-id="4637f-111">Fixed quantity</span></span>
    - <span data-ttu-id="4637f-112">Määritetty</span><span class="sxs-lookup"><span data-stu-id="4637f-112">Specified</span></span>

    <span data-ttu-id="4637f-113">**Ennakonpidätyksen kohdistus** -kenttä näyttää maksusuunnitelman TDS-kohdistusmenetelmän.</span><span class="sxs-lookup"><span data-stu-id="4637f-113">The **Withholding tax allocation** field shows the TDS allocation method for the payment schedule.</span></span> <span data-ttu-id="4637f-114">Jos valitset **Yhteensä** **Kohdistus**-kentässä, **Ennakonpidätyksen kohdistus** -kentän arvoksi tulee automaattisesti **Yhteensä**.</span><span class="sxs-lookup"><span data-stu-id="4637f-114">If you select **Total** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Total**.</span></span> <span data-ttu-id="4637f-115">Jos valitset **Kohdistus**-kentässä **Kiinteä summa**, **Kiinteä määrä** tai **Määritetty**, **Ennakonpidätyksen kohdistus** -kentän arvoksi määritetään automaattisesti **Suhteellinen**.</span><span class="sxs-lookup"><span data-stu-id="4637f-115">If you select **Fixed amount**, **Fixed quantity**, or **Specified** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Proportionally**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4637f-116">Jos **Ennakonpidätyksen kohdistus** -kentän arvoksi määritetään **Kokonaissumma**, maksun maksuerät lasketaan bruttosumman perusteella, joka sisältää TDS-summan.</span><span class="sxs-lookup"><span data-stu-id="4637f-116">If the **Withholding tax allocation** field is set to **Total**, the payment installments are calculated based on the gross amount, which includes the TDS amount.</span></span> <span data-ttu-id="4637f-117">Jos **Ennakonpidätyksen kohdistus** -kentän arvoksi määritetään **Suhteellinen**, maksun maksuerät lasketaan nettolaskusumman perusteella TDS-summan vähentämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="4637f-117">If the **Withholding tax allocation** field is set to **Proportionally**, the payment installments are calculated based on the net invoice amount after the TDS amount is deducted.</span></span>

4. <span data-ttu-id="4637f-118">Lisää muut pakolliset yksityiskohdat ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="4637f-118">Enter the other required details, and then close the page.</span></span>
