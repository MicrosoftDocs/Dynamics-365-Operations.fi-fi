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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2536e87953267eae13cf3b42c2bd5476fc647c22
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994712"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="aae60-103">Toimittajalaskun arvonlisäveron laskeminen ja täsmäytys</span><span class="sxs-lookup"><span data-stu-id="aae60-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aae60-104">Tässä ohjeaiheessa käsitellään toimittajan laskun arvonlisäveron oikaisemista.</span><span class="sxs-lookup"><span data-stu-id="aae60-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="aae60-105">Jos alkuperäinen lähdeasiakirja sisältää eri verosummat kuin lasketut summat, voit oikaista summat ennen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="aae60-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="aae60-106">Tässä tehtävässä käytetään esittely-yritystä DEMF.</span><span class="sxs-lookup"><span data-stu-id="aae60-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="aae60-107">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Laskut > Laskukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="aae60-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="aae60-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="aae60-108">Select **New**.</span></span>
3. <span data-ttu-id="aae60-109">Valitse uuden rivin **Nimi**-kentässä avattavasta valikosta vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="aae60-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="aae60-110">Valitse toimintoruudussa **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="aae60-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="aae60-111">Määritä **Tili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="aae60-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="aae60-112">Kirjoita **Lasku**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="aae60-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="aae60-113">Syötä **Kredit**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="aae60-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="aae60-114">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="aae60-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="aae60-115">Valitse **Arvonlisävero**.</span><span class="sxs-lookup"><span data-stu-id="aae60-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="aae60-116">Syötä **Toteutunut kokonaisarvonlisäverosumma** -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="aae60-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="aae60-117">Arvonlisäverosummat voidaan oikaista **Oikaisu**-välilehdessä arvonlisäverokoodin mukaan.</span><span class="sxs-lookup"><span data-stu-id="aae60-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="aae60-118">Valitse **Nollaa todellinen lasketuista summista**.</span><span class="sxs-lookup"><span data-stu-id="aae60-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="aae60-119">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="aae60-119">Select **OK**.</span></span>
14. <span data-ttu-id="aae60-120">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="aae60-120">Select **Save**.</span></span>

