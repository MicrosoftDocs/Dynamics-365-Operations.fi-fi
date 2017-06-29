---
title: "Valuutan uudelleenarvostus konsolidointiyrityksessä"
description: 
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 39bcd3d07aa41076debc6b500381ade61763dc33
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="currency-revaluation-in-a-consolidation-company"></a>Valuutan uudelleenarvostus konsolidointiyrityksessä

[!include[banner](../includes/banner.md)]




Kun konsolidoit tietoja yhdestä kirjanpitovaluutasta toiseen, sinun on silti ajettava valuutan uudelleenarvostus, jos vaihtokursseissa tapahtuu muutoksia niin, että tiliesi saldot on uudelleenarvostettu oikein. Kun konsolidoit tiedot ensimmäisen kerran, valitse **Valuutan muuntaminen** -välilehdeltä ensimmäiset vaihtokurssit, jotka muunnetaan konsolidointiprosessin aikana. Kun uusi vaihtokurssi on syötetty (esimerkiksi seuraavana kuukautena), sinun on uudelleenarvostettava tilisaldot. Toteutumattomat voitot tai tappiot päivitetään sitten tämän mukaisesti uuden vaihtokurssin ja päivämäärän perusteella. Seuraavassa esimerkissä on kuvattu kirjanpitomerkinnät, jotka luodaan tämän prosessin aikana.

## <a name="company-setup"></a>Yrityksen asetukset
-   **Lähde/toimintaa harjoittava yritys (USMF)** – Yhdysvaltain dollareita (USD) käytetään kirjanpito- ja raportointivaluuttana.
-   **Konsolidointiyritys (CON)** – Euroja (EUR) käytetään kirjanpito- ja raportointivaluuttana.
    -   **Toteutunut voitto** – Kirjanpitotili 801500
    -   **Toteutunut tappio** – Kirjanpitotili 801600
    -   **Toteutumaton voitto** – Kirjanpitotili 801600
    -   **Toteutumaton tappio** – Kirjanpitotili 801400

## <a name="original-transactions"></a>Alkuperäiset tapahtumat
### <a name="cash-receipt-transactions-in-usmf"></a>Kassamaksut USMF:ssä

| Päivämäärä       | Kirjanpitotili               | Valuutta | Summa |
|------------|------------------------------|----------|--------|
| 11/10/2015 | 110110 – Käteinen                | USD      | 500    |
| 11/10/2015 | 130100 – Myyntireskontra | USD      | -500   |

## <a name="exchange-rates"></a>Vaihtokurssit
| Lähdevaluutta | Valuutaksi | Alkamispäivä | Vaihtokurssi |
|---------------|-------------|------------|---------------|
| Euro           | USD         | 1/10/2015  | 200           |
| Euro           | USD         | 1/11/2015  | 150           |
| Euro           | USD         | 1/12/2012  | 100           |

## <a name="perform-the-consolidation-for-october-2015"></a>Suorita konsolidointi lokakuulle 2015
### <a name="balances-in-the-consolidation-company"></a>Konsolidointiyrityksen saldot

| Kirjanpitotili | Valuutta | Summa | Laskenta    |
|----------------|----------|--------|----------------|
| 110110         | Euro      | 250    | 500 USD × 50 %  |
| 130100         | Euro      | -250   | -500 USD × 50 % |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a>Suorita valuutan uudelleenarvostus tileille kaudella 1.10.2015 - 30.11.2015
### <a name="balances-in-the-consolidation-company"></a>Konsolidointiyrityksen saldot

| Kirjanpitotili | Valuutta | Summa  | Laskenta                        |
|----------------|----------|---------|------------------------------------|
| 110110         | Euro      | 333,33  | Alkuperäinen summa 500 × 66,6667 %  |
| 130100         | Euro      | -333,33 | Alkuperäinen summa -500 × 66,6667 % |
| 801400         | Euro      | 83,33   | 333,33 – 250                       |
| 801600         | Euro      | -83,33  | -333,33 – (-250)                   |

Näet tässä lisätapahtumia raportointivaluutan summille.

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a>Suorita valuutan uudelleenarvostus tileille kaudella 1.10.2015 - 31.12.2015
### <a name="balances-in-the-consolidation-company"></a>Konsolidointiyrityksen saldot

| Kirjanpitotili | Valuutta | Summa  | Laskenta                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | Euro      | 500,00  | Alkuperäinen summa 500 × 1                           |
| 130100         | Euro      | -500,00 | Alkuperäinen summa -500 × 1                          |
| 801400         | Euro      | 250     | 500 – 333,33 = 166,67 166,67 + 83,33 = 250           |
| 801600         | Euro      | -250    | -500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250 |






