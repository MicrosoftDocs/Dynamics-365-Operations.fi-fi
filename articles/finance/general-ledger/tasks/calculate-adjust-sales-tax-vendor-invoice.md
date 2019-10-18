---
title: Toimittajalaskun arvonlisäveron laskeminen ja täsmäytys
description: Tässä ohjeaiheessa kerrotaan, miten toimittajan laskun arvonlisäveroa oikaistaan Dynamics 365 Financeissa.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a68e0df78516875168d977f78adf023887b2362d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186276"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="ee179-103">Toimittajalaskun arvonlisäveron laskeminen ja täsmäytys</span><span class="sxs-lookup"><span data-stu-id="ee179-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee179-104">Tässä ohjeaiheessa käsitellään toimittajan laskun arvonlisäveron oikaisemista.</span><span class="sxs-lookup"><span data-stu-id="ee179-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="ee179-105">Jos alkuperäinen lähdeasiakirja sisältää eri verosummat kuin lasketut summat, voit oikaista summat ennen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="ee179-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="ee179-106">Tässä tehtävässä käytetään esittely-yritystä DEMF.</span><span class="sxs-lookup"><span data-stu-id="ee179-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="ee179-107">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Laskut > Laskukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="ee179-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="ee179-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ee179-108">Select **New**.</span></span>
3. <span data-ttu-id="ee179-109">Valitse uuden rivin **Nimi**-kentässä avattavasta valikosta vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="ee179-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="ee179-110">Valitse toimintoruudussa **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="ee179-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="ee179-111">Määritä **Tili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="ee179-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="ee179-112">Kirjoita **Lasku**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ee179-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="ee179-113">Syötä **Kredit**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ee179-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="ee179-114">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="ee179-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="ee179-115">Valitse **Arvonlisävero**.</span><span class="sxs-lookup"><span data-stu-id="ee179-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="ee179-116">Syötä **Toteutunut kokonaisarvonlisäverosumma** -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ee179-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="ee179-117">Arvonlisäverosummat voidaan oikaista **Oikaisu**-välilehdessä arvonlisäverokoodin mukaan.</span><span class="sxs-lookup"><span data-stu-id="ee179-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="ee179-118">Valitse **Nollaa todellinen lasketuista summista**.</span><span class="sxs-lookup"><span data-stu-id="ee179-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="ee179-119">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee179-119">Select **OK**.</span></span>
14. <span data-ttu-id="ee179-120">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ee179-120">Select **Save**.</span></span>
