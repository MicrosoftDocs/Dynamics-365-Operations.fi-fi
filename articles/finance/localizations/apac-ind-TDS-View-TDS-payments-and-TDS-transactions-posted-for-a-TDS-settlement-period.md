---
title: Näytä TDS-tilitysjaksolle kirjatut TDS-maksut ja -tapahtumat
description: Tässä ohjeaiheessa on tietoja siitä, miten voit tarkastella tilityskaudelle kirjattuja Vero vähennettynä lähteissä (TDS) -maksuja ja -tapahtumia.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 2bada42073e46c69101e6d31f3328a2eeb95f880
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023201"
---
# <a name="view-posted-tds-payments-and-transactions-for-a-tds-settlement-period"></a><span data-ttu-id="868b8-103">Näytä TDS-tilitysjaksolle kirjatut TDS-maksut ja -tapahtumat</span><span class="sxs-lookup"><span data-stu-id="868b8-103">View posted TDS payments and transactions for a TDS settlement period</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="868b8-104">Tässä ohjeaiheessa on tietoja siitä, miten voit tarkastella tilityskaudelle kirjattuja Vero vähennettynä lähteissä (TDS) -maksuja ja -tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="868b8-104">This topic explains how to view the Tax Deducted at Source (TDS) payments and transactions that were posted for a settlement period.</span></span>

1. <span data-ttu-id="868b8-105">Siirry kohtaan **Vero \> Välilliset verot \> Ennakonpidätys \> Ennakonpidätyksen tilityskaudet**.</span><span class="sxs-lookup"><span data-stu-id="868b8-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="868b8-106">[![Ennakonpidätyksen tilityskaudet -sivu](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span><span class="sxs-lookup"><span data-stu-id="868b8-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span></span>

2. <span data-ttu-id="868b8-107">Valitse **Ennakonpidätyksen tilityskaudet** -sivulla **Ennakonpidätysmaksut** avataksesi **Ennakonpidätysmaksut** -sivun, jolla voit tarkastella tietylle TDS-tilityskaudella tehtyjä TDS-tilityksiä.</span><span class="sxs-lookup"><span data-stu-id="868b8-107">On the **Withholding tax settlement periods** page, select **Withholding tax payments** to open the **Withholding tax payments** page, where you can view the TDS settlements that were made for a specific TDS settlement period.</span></span>

    <span data-ttu-id="868b8-108">**Yhteenveto**-välilehdessä on seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="868b8-108">The **Overview** tab shows the following information:</span></span>

    - <span data-ttu-id="868b8-109">**Päivämäärä** – TDS-tilityksen päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="868b8-109">**Date** – The date of TDS settlement.</span></span>
    - <span data-ttu-id="868b8-110">**Tosite** – TDS-tilitystapahtuman tositenumero.</span><span class="sxs-lookup"><span data-stu-id="868b8-110">**Voucher** – The voucher number of the TDS settlement transaction.</span></span>
    - <span data-ttu-id="868b8-111">**Verotyyppi** – Verotyyppi, jota varten tilitysprosessi suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="868b8-111">**Tax type** – The tax type that the settlement process is run for.</span></span>
    - <span data-ttu-id="868b8-112">**Verotilin numero (TAN)** – Tilitetyn TDS-tapahtuman verotilin numero (TAN).</span><span class="sxs-lookup"><span data-stu-id="868b8-112">**Tax Account Number (TAN)** – The Tax Account Number (TAN) of the settled TDS transaction.</span></span>
    - <span data-ttu-id="868b8-113">**Tilityskausi** – Tilityskausi, jolle TDS-tilitysprosessi suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="868b8-113">**Settlement period** – The settlement period that the TDS settlement process is run for.</span></span>
    - <span data-ttu-id="868b8-114">**Päivämäärästä** – Tilityskauden aloituspäivä.</span><span class="sxs-lookup"><span data-stu-id="868b8-114">**From date** – The start date of the settlement period.</span></span>
    - <span data-ttu-id="868b8-115">**Päivämäärään** – Tilityskauden päättymispäivä.</span><span class="sxs-lookup"><span data-stu-id="868b8-115">**To date** – The end date of the settlement period.</span></span>
    - <span data-ttu-id="868b8-116">**Ennakonpidätysmaksun versio** – Ennakonpidätysmaksun versio: **Alkuperäinen**, **Uusimmat korjaukset** tai **Summa-luettelo**.</span><span class="sxs-lookup"><span data-stu-id="868b8-116">**Withholding tax payment version** – The version of the withholding tax payment: **Original**, **Latest corrections**, or **Total list**.</span></span>

5. <span data-ttu-id="868b8-117">Valitsemalla **Tosite** voit tarkastella TDS-tapahtuman tositemerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="868b8-117">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
6. <span data-ttu-id="868b8-118">Valitse **Ennakonpidätystapahtumat**, kun haluat tarkastella tietylle ajanjaksolle tilityskauden aikana tilitettyjen TDS-tapahtumien tietoja.</span><span class="sxs-lookup"><span data-stu-id="868b8-118">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for a specific period during a settlement period.</span></span> <span data-ttu-id="868b8-119">Valitsemalla **Tosite** voit tarkastella TDS-tapahtuman tositemerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="868b8-119">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span> <span data-ttu-id="868b8-120">Valitse **Ennakonpidätyksen komponentit** tarkastellaksesi TDS-verokomponenttia kohti laskettua TDS:ää tietylle TDS-verokoodille.</span><span class="sxs-lookup"><span data-stu-id="868b8-120">Select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>
7. <span data-ttu-id="868b8-121">Palaa **Ennakonpidätyksen tilityskaudet** -sivulle sulkemalla **Ennakonpidätysmaksut**-sivu.</span><span class="sxs-lookup"><span data-stu-id="868b8-121">Close the **Withholding tax payments** page to return to the **Withholding tax settlement periods** page.</span></span>
8. <span data-ttu-id="868b8-122">Valitse **Ennakonpidätystapahtumat**, kun haluat tarkastella tilityskaudelle tilitettyjen TDS-tapahtumien tietoja.</span><span class="sxs-lookup"><span data-stu-id="868b8-122">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for the settlement period.</span></span>
