---
title: Tapahtumien selvitys kirjanpitotilien välillä
description: Tässä menettelyssä käsitellään, miten kirjanpitotilien väliset tapahtumien tilitetään ja miten kirjanpidon tilitys peruutetaan.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8220bacc8d683163e97956ec59a5af929b04319c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994412"
---
# <a name="settle-transactions-between-ledger-accounts"></a>Tapahtumien selvitys kirjanpitotilien välillä

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään, miten kirjanpitotilien väliset tapahtumien tilitetään ja miten kirjanpidon tilitys peruutetaan. Menettely käyttää USMF-yrityksen demotietoja.


## <a name="settle-transaction-between-ledger-accounts"></a>Tilitä kirjanpitotilien välinen tapahtuma
1. Valitse Kirjanpito > Kausittaiset tehtävät > Tapahtuman selvitykset.
2. Etsi tilitettävä tapahtuma luettelosta.
   > [!NOTE]
   > Summan saldon on oltava nolla.  
3. Valitse Sisällytä.
4. Valitse Hyväksy.

## <a name="cancel-a-ledger-settlement"></a>Tapahtuman selvityksen peruuttaminen

1. Valitse Kirjanpito > Kyselyt ja raportit > Pääkirja.
2. Avaa valintaikkuna valitsemalla Parametrit.
3. Valitse Päivitä.
4. Etsi luettelosta tili, jossa on tilitetty tapahtuma.
5. Valitse Kaikki tapahtumat.
6. Suodattimen käyttö nopeuttaa tapahtuman etsimistä luettelosta.
7. Valitse Tapahtuman selvitykset.
8. Merkitse valittu rivi luettelossa.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]