---
title: Tapahtumien selvitys kirjanpitotilien välillä
description: Tässä menettelyssä käsitellään, miten kirjanpitotilien väliset tapahtumien tilitetään ja miten kirjanpidon tilitys peruutetaan.
author: aprilolson
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a871e379826626edbad2434b11281fce5e29e14e
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717303"
---
# <a name="settle-transactions-between-ledger-accounts"></a>Tapahtumien selvitys kirjanpitotilien välillä

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään, miten kirjanpitotilien väliset tapahtumien tilitetään ja miten kirjanpidon tilitys peruutetaan. Menettely käyttää USMF-yrityksen demotietoja.


## <a name="settle-transaction-between-ledger-accounts"></a>Tilitä kirjanpitotilien välinen tapahtuma
1. Valitse **Kirjanpito > Kausittaiset tehtävät > Tapahtuman selvitykset**.
2. Etsi tilitettävä tapahtuma luettelosta.
   > [!NOTE]
   > Summan saldon on oltava nolla.  
3. Valitse **Sisällytä**.
4. Valitse **Hyväksy**.

## <a name="cancel-a-ledger-settlement"></a>Tapahtuman selvityksen peruuttaminen

1. Valitse **Kirjanpito > Kyselyt ja raportit > Pääkirja**.
2. Avaa valintaikkuna valitsemalla **Parametrit**.
3. Valitse **Päivitä**.
4. Etsi luettelosta tili, jossa on tilitetty tapahtuma.
5. Valitse **Kaikki tapahtumat**.
6. Suodattimen käyttö nopeuttaa tapahtuman etsimistä luettelosta.
7. Valitse **Tapahtuman selvitykset**.
8. Merkitse valittu rivi luettelossa.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
