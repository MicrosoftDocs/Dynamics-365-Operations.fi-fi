---
title: Ennakonpidätyksen raportointikoodien määrittäminen TDS-verotyypille
description: Ennakonpidätyksen raportointikoodien avulla luodaan lomakkeen 26Q ja lomakkeen 27Q ilmoitukset Vero vähennettynä lähteissä (TDS) -tiedoille. Tässä ohjeaiheessa kerrotaan, miten ennakonpidätyksen raportointikoodien vaiheet määritetään TDS-raportointikoodien määrittämiseksi.
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
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023218"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a><span data-ttu-id="cc1fc-104">Ennakonpidätyksen raportointikoodien määrittäminen TDS-verotyypille</span><span class="sxs-lookup"><span data-stu-id="cc1fc-104">Set up withholding tax reporting codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc1fc-105">Ennakonpidätyksen raportointikoodien avulla luodaan lomakkeen 26Q ja lomakkeen 27Q ilmoitukset Vero vähennettynä lähteissä (TDS) -tiedoille.</span><span class="sxs-lookup"><span data-stu-id="cc1fc-105">Withholding tax reporting codes are used to generate Form 26Q and Form 27Q statements for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="cc1fc-106">Tässä ohjeaiheessa kerrotaan, miten ennakonpidätyksen raportointikoodien vaiheet määritetään TDS-raportointikoodien määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="cc1fc-106">This topic explains how to set up withholding tax reporting codes steps so that you can set up TDS reporting codes.</span></span>

1. <span data-ttu-id="cc1fc-107">Siirry kohtaan **Vero \> Asetukset \> Ennakonpidätys \> Ennakonpidätyksen raportointikoodit**.</span><span class="sxs-lookup"><span data-stu-id="cc1fc-107">Go to **Tax \> Setup \> Withholding tax \> Withholding tax reporting codes**.</span></span>

    <span data-ttu-id="cc1fc-108">[![Ennakonpidätyksen raportointikoodit -sivu](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span><span class="sxs-lookup"><span data-stu-id="cc1fc-108">[![Withholding tax reporting codes page](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span></span>

2. <span data-ttu-id="cc1fc-109">Valitse **Verotyyppi**-kentässä **TDS** määrittääksesi ennakonpidätyksen raportointikoodit TDS-verotyypille.</span><span class="sxs-lookup"><span data-stu-id="cc1fc-109">In the **Tax type** field, select **TDS** to define withholding tax reporting codes for the TDS tax type.</span></span>
3. <span data-ttu-id="cc1fc-110">Valitse **Ennakonpidätyksen komponentti** -kentässä TDS-komponentti, jota varten määrität ennakonpidätyksen raportointikoodin.</span><span class="sxs-lookup"><span data-stu-id="cc1fc-110">In the **Withholding tax component** field, select the TDS component to that you're defining the withholding tax reporting code for.</span></span> <span data-ttu-id="cc1fc-111">**Ennakonpidätyksen komponenttiryhmä** -kentässä näkyy TDS-komponenttiryhmä, joka on määritetty määrittämällesi TDS-komponentille.</span><span class="sxs-lookup"><span data-stu-id="cc1fc-111">The **Withholding tax component group** field shows the TDS component group that was defined for the TDS component that you're defining.</span></span>

    <span data-ttu-id="cc1fc-112">**Yleinen**-pikavälilehden **Osakoodi**-kentässä näkyy osakoodi, joka on liitetty TDS-komponenttiryhmään.</span><span class="sxs-lookup"><span data-stu-id="cc1fc-112">The **Section code** field on the **General** FastTab shows the section code that is attached to the TDS component group.</span></span>

4. <span data-ttu-id="cc1fc-113">Valitse TDS-raportointikoodi **Yleinen**-pikavälilehden **Raportointikoodi**-kentässä:</span><span class="sxs-lookup"><span data-stu-id="cc1fc-113">On the **General** FastTab, in the **Reporting code** field, select the TDS reporting code:</span></span>

    - <span data-ttu-id="cc1fc-114">TDS</span><span class="sxs-lookup"><span data-stu-id="cc1fc-114">TDS</span></span>
    - <span data-ttu-id="cc1fc-115">TCS</span><span class="sxs-lookup"><span data-stu-id="cc1fc-115">TCS</span></span>
    - <span data-ttu-id="cc1fc-116">Lisämaksu</span><span class="sxs-lookup"><span data-stu-id="cc1fc-116">Surcharge</span></span>
    - <span data-ttu-id="cc1fc-117">PE\_Cess</span><span class="sxs-lookup"><span data-stu-id="cc1fc-117">PE\_Cess</span></span>
    - <span data-ttu-id="cc1fc-118">SHE\_Cess</span><span class="sxs-lookup"><span data-stu-id="cc1fc-118">SHE\_Cess</span></span>

5. <span data-ttu-id="cc1fc-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="cc1fc-119">Close the page.</span></span>
