---
title: Nolla-arvoiseen tuotteen vastaanottoon kirjataan oston jaksotus, jonka summa on nolla
description: Kun kirjataan tuotteen vastaanotto, jonka arvo on nolla, järjestelmä luo oston jaksotuskirjauksen, jonka summa on 0 (nolla).
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f8d9d857590dc788d16b01edf77600d8fd8c8444
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026489"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a><span data-ttu-id="75ac2-103">Nolla-arvoiseen tuotteen vastaanottoon kirjataan oston jaksotus, jonka summa on nolla</span><span class="sxs-lookup"><span data-stu-id="75ac2-103">Purchase accrual that has a zero amount is posted for a zero-value product receipt</span></span>

<span data-ttu-id="75ac2-104">Tietopankin numero: 4612588</span><span class="sxs-lookup"><span data-stu-id="75ac2-104">KB number: 4612588</span></span>

## <a name="symptoms"></a><span data-ttu-id="75ac2-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="75ac2-105">Symptoms</span></span>

<span data-ttu-id="75ac2-106">Kun kirjataan tuotteen vastaanotto, jonka arvo on nolla, järjestelmä luo oston jaksotuskirjauksen, jonka summa on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="75ac2-106">When a product receipt that has zero value is posted, the system creates a posting to purchase accrual where the amount is 0 (zero).</span></span>

## <a name="resolution"></a><span data-ttu-id="75ac2-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="75ac2-107">Resolution</span></span>

<span data-ttu-id="75ac2-108">Oletusarvon mukaan *Osto, jaksotus* -tyypin kirjanpitokirjauksissa `IsTransferredIndetail`-kentän arvona on aina *Yhteenveto* alareskontran tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="75ac2-108">By default, for ledger postings of the *Purchase, accrual* type, the `IsTransferredIndetail` field is always set to *Summary* in subledger transactions.</span></span> <span data-ttu-id="75ac2-109">Järjestelmä luo siksi liittyvän tositemerkinnän, vaikka summa olisi 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="75ac2-109">Therefore, the system creates a related voucher entry even if the amount is 0 (zero).</span></span>

<span data-ttu-id="75ac2-110">Jos haluat ohittaa tämän kirjaustavan, kun summa on 0 (nolla), laajenna `subledgerJournalizer.markDoNotTransferEntries`-menetelmää niin, että se sisältää kohdan `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount` seuraavan esimerkin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="75ac2-110">To skip this posting type when the amount is 0 (zero), extend the `subledgerJournalizer.markDoNotTransferEntries` method so that it includes `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, as shown in the following example.</span></span>

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
