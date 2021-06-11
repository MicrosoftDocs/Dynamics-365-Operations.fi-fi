---
title: Ennakonpidätyksen täsmäytyskausien määrittäminen TDS-verotyypille
description: Tässä aiheessa kuvataan, miten Vero vähennettynä lähteissä (TDS) -tilityskausille määritetään tilityskaudet.
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
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023195"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a><span data-ttu-id="c83b4-103">Ennakonpidätyksen täsmäytyskausien määrittäminen TDS-verotyypille</span><span class="sxs-lookup"><span data-stu-id="c83b4-103">Set up withholding tax settlement periods for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c83b4-104">Tässä aiheessa kuvataan, miten Vero vähennettynä lähteissä (TDS) -tilityskausille määritetään tilityskaudet.</span><span class="sxs-lookup"><span data-stu-id="c83b4-104">This topic explains how to set up settlement periods for Tax Deducted at Source (TDS) settlement periods.</span></span>

1. <span data-ttu-id="c83b4-105">Siirry kohtaan **Vero \> Välilliset verot \> Ennakonpidätys \> Ennakonpidätyksen tilityskaudet**.</span><span class="sxs-lookup"><span data-stu-id="c83b4-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="c83b4-106">[![Ennakonpidätyksen tilityskaudet -sivu](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span><span class="sxs-lookup"><span data-stu-id="c83b4-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span></span>

2. <span data-ttu-id="c83b4-107">Valitse **Verotyyppi**-kentässä **TDS**, jos haluat määrittää ennakonpidätyksen tilityskaudet TDS-verotyypille.</span><span class="sxs-lookup"><span data-stu-id="c83b4-107">In the **Tax type** field, select **TDS** to set up withholding tax settlement periods for the TDS tax type.</span></span>
3. <span data-ttu-id="c83b4-108">Valitse **Uusi** luodaksesi rivin.</span><span class="sxs-lookup"><span data-stu-id="c83b4-108">Select **New** to create a line.</span></span>
4. <span data-ttu-id="c83b4-109">Kirjoita **Tilityskausi**-kenttään TDS-tilityskauden nimi tai kuvaus.</span><span class="sxs-lookup"><span data-stu-id="c83b4-109">In the **Settlement period** field, enter a name for the TDS settlement period.</span></span>
5. <span data-ttu-id="c83b4-110">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="c83b4-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="c83b4-111">Valitse **Ennakonpidätysviranomainen**-kentästä TDS-viranomainen, jolle TDS-tilityskausi määritetään.</span><span class="sxs-lookup"><span data-stu-id="c83b4-111">In the **Withholding tax authority** field, select the TDS authority that you're defining the TDS settlement period for.</span></span>
7. <span data-ttu-id="c83b4-112">Valitse **Yleinen**-pikavälilehden **Kausiväli**-kentästä TDS-tilityskauden kausivälin tyyppi.</span><span class="sxs-lookup"><span data-stu-id="c83b4-112">On the **General** FastTab, in the **Period interval** field, select the type of period interval for the TDS settlement period.</span></span>
8. <span data-ttu-id="c83b4-113">Määritä **Yksikkömäärä**-kenttään kausivälin tyypin yksikkömäärä.</span><span class="sxs-lookup"><span data-stu-id="c83b4-113">In the **Number of units** field, specify the number of units for the period interval type.</span></span>
9. <span data-ttu-id="c83b4-114">Valitse **Kaudet**-pikavälilehden **Päivämäärästä**-kentästä TDS-tilityskauden alkamispäivä.</span><span class="sxs-lookup"><span data-stu-id="c83b4-114">On the **Periods** FastTab, in the **From date** field, select the start date for the TDS settlement period.</span></span> <span data-ttu-id="c83b4-115">Valitse **Päivämäärään**-kentässä päättymispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="c83b4-115">In the **To date** field, select the end date.</span></span>
10. <span data-ttu-id="c83b4-116">Voit luoda seuraavan TDS-tilityskauden aiemmin luodulle kaudelle kausivälin ja kausiyksiköiden perusteella valitsemalla **Uusi kausi**.</span><span class="sxs-lookup"><span data-stu-id="c83b4-116">To create a subsequent TDS settlement period for an existing period, based on the period interval and period units, select **New period**.</span></span>
11. <span data-ttu-id="c83b4-117">Voit tarkastella tietylle tilityskaudelle suoritettavan kausittaisen TDS-tilityksen tietoja valitsemalla **Ennakonpidätysmaksut** avataksesi **Ennakonpidätysmaksut**-sivun.</span><span class="sxs-lookup"><span data-stu-id="c83b4-117">To view the details of the periodic TDS settlement that is run for a specific settlement period, select **Withholding tax payments** to open the **Withholding tax payment** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c83b4-118">Voit suorittaa kausittaisen TDS-tilitysprosessin valitsemalla **Kirjanpito \> Kausittainen \> Ennakonpidätys \> Ennakonpidätysmaksu**.</span><span class="sxs-lookup"><span data-stu-id="c83b4-118">To run the periodic TDS settlement process, go to **General ledger \> Periodic \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="c83b4-119">[![Ennakonpidätysmaksu-sivu](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span><span class="sxs-lookup"><span data-stu-id="c83b4-119">[![Withholding tax payment page](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span></span>

12. <span data-ttu-id="c83b4-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c83b4-120">Close the page.</span></span>