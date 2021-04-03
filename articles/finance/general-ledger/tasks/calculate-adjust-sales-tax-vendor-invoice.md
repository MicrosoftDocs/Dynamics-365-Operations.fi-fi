---
title: Toimittajalaskun arvonlisäveron laskeminen ja täsmäytys
description: Tässä ohjeaiheessa kerrotaan, miten toimittajan laskun arvonlisäveroa oikaistaan Dynamics 365 Financessa.
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
ms.openlocfilehash: f4d01fe7587e01c04af28be934a235d955455216
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204734"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="9088d-103">Toimittajalaskun arvonlisäveron laskeminen ja täsmäytys</span><span class="sxs-lookup"><span data-stu-id="9088d-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9088d-104">Tässä ohjeaiheessa käsitellään toimittajan laskun arvonlisäveron oikaisemista.</span><span class="sxs-lookup"><span data-stu-id="9088d-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="9088d-105">Jos alkuperäinen lähdeasiakirja sisältää eri verosummat kuin lasketut summat, voit oikaista summat ennen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="9088d-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="9088d-106">Tässä tehtävässä käytetään esittely-yritystä DEMF.</span><span class="sxs-lookup"><span data-stu-id="9088d-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="9088d-107">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Laskut > Laskukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="9088d-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="9088d-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="9088d-108">Select **New**.</span></span>
3. <span data-ttu-id="9088d-109">Valitse uuden rivin **Nimi**-kentässä avattavasta valikosta vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="9088d-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="9088d-110">Valitse toimintoruudussa **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="9088d-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="9088d-111">Määritä **Tili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="9088d-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="9088d-112">Kirjoita **Lasku**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="9088d-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="9088d-113">Syötä **Kredit**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="9088d-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="9088d-114">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="9088d-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="9088d-115">Valitse **Arvonlisävero**.</span><span class="sxs-lookup"><span data-stu-id="9088d-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="9088d-116">Syötä **Toteutunut kokonaisarvonlisäverosumma** -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="9088d-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="9088d-117">Arvonlisäverosummat voidaan oikaista **Oikaisu**-välilehdessä arvonlisäverokoodin mukaan.</span><span class="sxs-lookup"><span data-stu-id="9088d-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="9088d-118">Valitse **Nollaa todellinen lasketuista summista**.</span><span class="sxs-lookup"><span data-stu-id="9088d-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="9088d-119">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9088d-119">Select **OK**.</span></span>
14. <span data-ttu-id="9088d-120">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="9088d-120">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]