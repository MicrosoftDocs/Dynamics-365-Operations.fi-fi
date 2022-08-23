---
title: Viittaaminen alkuperäisiin laskuihin hyvityslaskuissa (toimittajan laskut)
description: Tässä artikkelissa käsitellään alkuperäiseen laskuun tehtävän viitauksen luonti hyvityslaskua luotaessa.
author: AdamTrukawka
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.search.form: ''
ms.openlocfilehash: ed07ae9784da3ca721fcb25a9c5a14c4f75f2e59
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277367"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Viittaaminen alkuperäisiin laskuihin hyvityslaskuissa (toimittajan laskut)

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään alkuperäiseen laskuun tehtävän viitauksen luonti hyvityslaskua luotaessa.

## <a name="prerequisites"></a>Edellytykset

Ota käyttöön **Ota toimittajan laskujen hyvityslaskutus käyttöön** -ominaisuus **Ominaisuuksien hallinta** -työtilassa. Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tässä artikkelissa käsitellyt toiminnot koskevat seuraavia liiketoiminta-asiakirjoja:

**Ostoreskontra:**

- Ostotilaus
- Laskukirjauskansio
- Laskurekisteri

**Kirjanpito:**

- Kirjauskansio

## <a name="define-a-reference-to-an-original-invoice"></a>Alkuperäiseen laskuun tehtävän viittauksen määrittäminen

Seuraavilla menetelmillä voidaan määrittää alkuperäiseen laskuun tehtävä viittaus määritetyissä liiketoiminta-asiakirjatyypeissä.

### <a name="vendor-credit-note-purchase-order"></a>Toimittajan hyvityslasku (ostotilaus)

1. Valitse **Ostoreskontra** \> **Ostotilaukset** \> **Kaikki ostotilaukset**.
2. Luo uusi ostotilaus tai luo hyvityslasku aiemmin luodun perusteella.
3. Valitse Toimintoruudun **Laskutus**-välilehden **Esittele**-ryhmässä **Hyvityslaskutus**.
4. Anna korjauksen syy ja viittaus alkuperäiseen laskuun.

### <a name="vendor-credit-note-ledger-journals"></a>Toimittajan hyvityslasku (kirjanpidon kirjauskansiot)

1. Noudata seuraavia ohjeita:

    - Valitse **Ostoreskontra** \> **Laskun kirjauskansiot**.
    - Valitse **Ostoreskontra** \> **Laskurekisteri**.
    - Valitse **Kirjanpito** \> **Kirjauskansioviennit** \> **Yleiset kirjauskansiot**.

2. Luo uusi kirjauskansio ja uudet kirjauskansion rivit.
3. Valitse toimintoruudussa **Toiminnot** \> **Hyvityslaskutus**.
4. Anna korjauksen syy ja viittaus alkuperäiseen laskuun.

> [!NOTE]
> **Hyvityslaskutus**-komento näkyy kirjauskansion tositteessa, jossa **Tilityyppi**-kentän asetuksena on **Toimittaja**.
