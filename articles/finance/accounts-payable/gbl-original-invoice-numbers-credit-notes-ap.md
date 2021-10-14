---
title: Viittaaminen alkuperäisiin laskuihin hyvityslaskuissa (toimittajan laskut)
description: Tässä aiheessa käsitellään alkuperäiseen laskuun tehtävän viitauksen luonti hyvityslaskua luotaessa.
author: v-oloski
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6114ffb4d3b9e942887cbfa10c6039b0d73af7e1
ms.sourcegitcommit: 86f0574363fb869482ef73ff294f345f81d17c5b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7562223"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Viittaaminen alkuperäisiin laskuihin hyvityslaskuissa (toimittajan laskut)

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään alkuperäiseen laskuun tehtävän viitauksen luonti hyvityslaskua luotaessa.

## <a name="prerequisites"></a>Edellytykset

Ota käyttöön **Ota toimittajan laskujen hyvityslaskutus käyttöön** -ominaisuus **Ominaisuuksien hallinta** -työtilassa. Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tässä aiheessa käsitellyt toiminnot koskevat seuraavia liiketoiminta-asiakirjoja:

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
