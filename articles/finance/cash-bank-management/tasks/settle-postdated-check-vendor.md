---
title: Tilitä toimittajalle jälkeen päin päivitetty lasku
description: Tilitä toimittajalle myönnetty myöhemmäksi päivätty sekki, kun pankki on selvittänyt erääntyneen ja pankin selvittämän sekkitapahtuman.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d66caa83df693445c1b1d40ffdc11e8d10cf7426
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239624"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="6b4f0-103">Tilitä toimittajalle jälkeen päin päivitetty lasku</span><span class="sxs-lookup"><span data-stu-id="6b4f0-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6b4f0-104">Tilitä toimittajalle myönnetty myöhemmäksi päivätty sekki, kun pankki on selvittänyt erääntyneen ja pankin selvittämän sekkitapahtuman.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="6b4f0-105">Suorita seuraavat menettelyt, kuin aloitat tämän menettelyn.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="6b4f0-106">Määritä jälkeen päin päivitetyt sekit</span><span class="sxs-lookup"><span data-stu-id="6b4f0-106">Set up postdated checks</span></span>

2) <span data-ttu-id="6b4f0-107">Rekisteröi ja kirjaa toimittajan myöhemmäksi päivitetty sekki</span><span class="sxs-lookup"><span data-stu-id="6b4f0-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="6b4f0-108">Tämä menettelyn rooli on Rahastonhoitaja.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="6b4f0-109">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="6b4f0-110">Valitse Ostoreskontra > Maksut > Toimittajan myöhemmäksi päivätyt sekit.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="6b4f0-111">Valitse Selvitä.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-111">Click Settle.</span></span>
3. <span data-ttu-id="6b4f0-112">Valitse Tilitä siirtokirjaukset.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="6b4f0-113">Selvitä sekkitapahtumien toimittajan tili</span><span class="sxs-lookup"><span data-stu-id="6b4f0-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="6b4f0-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-114">Close the page.</span></span>
5. <span data-ttu-id="6b4f0-115">Siirry kohtaan Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="6b4f0-116">Valitse Näytä-kentässä Kaikki.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="6b4f0-117">Valitse Näytä vain käyttäjän luomat -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="6b4f0-118">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="6b4f0-119">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-119">Click Lines.</span></span>
10. <span data-ttu-id="6b4f0-120">Valitse Tosite.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-120">Click Voucher.</span></span>
11. <span data-ttu-id="6b4f0-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-121">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]