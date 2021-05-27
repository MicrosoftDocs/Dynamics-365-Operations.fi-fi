---
title: Ennakonpidätyskoodien määrittäminen TDS-verotyypille
description: Tässä aiheessa kerrotaan, miten Vero vähennettynä lähteissä (TDS) -verokoodit määritetään.
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
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023220"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a><span data-ttu-id="36c27-103">Ennakonpidätyskoodien määrittäminen TDS-verotyypille</span><span class="sxs-lookup"><span data-stu-id="36c27-103">Set up withholding tax codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36c27-104">Tässä aiheessa kerrotaan, miten Vero vähennettynä lähteissä (TDS) -verokoodit määritetään.</span><span class="sxs-lookup"><span data-stu-id="36c27-104">This topic explains how to set up tax codes for Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="36c27-105">Siirry kohtaan **Vero \> Välilliset verot \> Ennakonpidätys \> Ennakonpidätyskoodit**.</span><span class="sxs-lookup"><span data-stu-id="36c27-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.</span></span>

    <span data-ttu-id="36c27-106">[![Ennakonpidätyskoodit-sivu](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span><span class="sxs-lookup"><span data-stu-id="36c27-106">[![Withholding tax codes page](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span></span>

2. <span data-ttu-id="36c27-107">Valitse toimintoruudusta **Uusi**, jos haluat luoda TDS:lle ennakonpidätyskoodin, ja syötä tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="36c27-107">On the Action Pane, select **New** to create a withholding tax code for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="36c27-108">Valitse **Yleinen**-pikavälilehden **Verotyyppi**-kentästä **TDS**, jos haluat luokitella verokoodin TDS-verokoodiksi.</span><span class="sxs-lookup"><span data-stu-id="36c27-108">On the **General** FastTab, in the **Tax type** field, select **TDS** to categorize the tax code as a TDS tax code.</span></span>
4. <span data-ttu-id="36c27-109">Valitse **Tilityskausi**-kentässä TDS-verokoodin TDS-tilityskausi.</span><span class="sxs-lookup"><span data-stu-id="36c27-109">In the **Settlement period** field, select the TDS settlement period for the TDS tax code.</span></span>
5. <span data-ttu-id="36c27-110">Valitse **Päätili**-kentässä kirjanpitotili, jonne TDS-summa kirjataan.</span><span class="sxs-lookup"><span data-stu-id="36c27-110">In the **Main account** field, select the ledger account that the TDS amount should be posted to.</span></span>
6. <span data-ttu-id="36c27-111">Valitse **Myyntireskontra**-kentässä myyntireskontratili, jolle myyntitapahtumista vähennetty TDS-summa kirjataan.</span><span class="sxs-lookup"><span data-stu-id="36c27-111">In the **Receivable account** field, select the receivable account that the TDS amount that is deducted in sales transactions should be posted to.</span></span>

    <span data-ttu-id="36c27-112">**Alkuperä**-kentän arvoksi määritetään automaattisesti **Prosenttia bruttosummasta**, eikä arvoa voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="36c27-112">The **Origin** field is automatically set to **Percentage of gross amount**, and the value can't be changed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="36c27-113">TDS-verotyypin verokoodien alkuperäksi ei voi määrittää **Prosenttia nettosummasta**.</span><span class="sxs-lookup"><span data-stu-id="36c27-113">You can't set the origin to **Percentage of net amount** for tax codes of the TDS tax type.</span></span>

7. <span data-ttu-id="36c27-114">Valitse **Ennakonpidätyksen komponentti** -kentässä TDS-verokoodin TDS-verokomponentti.</span><span class="sxs-lookup"><span data-stu-id="36c27-114">In the **Withholding tax component** field, select the TDS tax component for the TDS tax code.</span></span>
8. <span data-ttu-id="36c27-115">Valitse toimintoruudussa **Arvot** avataksesi **Ennakonpidätyksen arvot** -sivun.</span><span class="sxs-lookup"><span data-stu-id="36c27-115">On the Action Pane, select **Values** to open the **Withholding tax values** page.</span></span>
9. <span data-ttu-id="36c27-116">**Päivämäärästä**-kentässä syötä TDS-arvon aloituspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="36c27-116">In the **From date** field, enter the start date for the TDS value.</span></span> <span data-ttu-id="36c27-117">Syötä **Päivämäärään**-kenttään päättymispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="36c27-117">In the **To date** field, enter the end date.</span></span>

    > [!NOTE]
    > <span data-ttu-id="36c27-118">**Vähimmäisraja**-, **Yläraja**- ja **Sulkemis-%**-kentät eivät ole käytettävissä TDS-verotyypin verokoodeissa.</span><span class="sxs-lookup"><span data-stu-id="36c27-118">The **Minimum limit**, **Upper limit**, and **Exclude %** fields aren't available for tax codes of the TDS tax type.</span></span>

10. <span data-ttu-id="36c27-119">Syötä **Arvo**-kenttään TDS-verokoodin TDS-prosentti.</span><span class="sxs-lookup"><span data-stu-id="36c27-119">In the **Value** field, enter the percentage of TDS for the TDS tax code.</span></span>
11. <span data-ttu-id="36c27-120">Sulje **Ennakonpidätyksen arvot** -sivu palataksesi **Ennakonpidätyskoodit**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="36c27-120">Close the **Withholding tax values** page to return to the **Withholding tax codes** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="36c27-121">**Ennakonpidätyskoodit**-sivun **Rajat**-painike ei ole käytettävissä TDS-verotyypin verokoodeissa.</span><span class="sxs-lookup"><span data-stu-id="36c27-121">The **Limits** button on the **Withholding tax codes** page isn't available for tax codes of the TDS tax type.</span></span>

12. <span data-ttu-id="36c27-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36c27-122">Close the page.</span></span>
