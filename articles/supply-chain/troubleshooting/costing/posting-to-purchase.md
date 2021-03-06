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
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a>Nolla-arvoiseen tuotteen vastaanottoon kirjataan oston jaksotus, jonka summa on nolla

Tietopankin numero: 4612588

## <a name="symptoms"></a>Oireet

Kun kirjataan tuotteen vastaanotto, jonka arvo on nolla, järjestelmä luo oston jaksotuskirjauksen, jonka summa on 0 (nolla).

## <a name="resolution"></a>Ratkaisu

Oletusarvon mukaan *Osto, jaksotus* -tyypin kirjanpitokirjauksissa `IsTransferredIndetail`-kentän arvona on aina *Yhteenveto* alareskontran tapahtumissa. Järjestelmä luo siksi liittyvän tositemerkinnän, vaikka summa olisi 0 (nolla).

Jos haluat ohittaa tämän kirjaustavan, kun summa on 0 (nolla), laajenna `subledgerJournalizer.markDoNotTransferEntries`-menetelmää niin, että se sisältää kohdan `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount` seuraavan esimerkin mukaisesti.

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
