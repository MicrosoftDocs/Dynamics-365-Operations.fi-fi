---
title: Arkistoi tulostetut myyntilaskut hajautusarvonumeroilla
description: Tässä aiheessa kuvataan, kuinka arkistointi otetaan käyttöön, jotta tulostetut asiakaslaskut voidaan tallentaa hajautusnumeroilla.
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 841e6059f5b0d70dbd1fe12a1f8910bbb31ddc86
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018975"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Arkistoi tulostetut myyntilaskut hajautusarvonumeroilla

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Joissakin maissa on lakisääteinen vaatimus tallentaa järjestelmään joidenkin tiedostojen tulosteet sekä lasketut hajautusnumerot. Hajautusnumeroita voidaan käyttää viranomaisille raportoitaessa ja auditoinnissa.

Tässä aiheessa kuvataan, kuinka arkistointi määritetään, jotta tulostetut asiakaslaskut voidaan tallentaa hajautusnumeroilla.

## <a name="prerequisites"></a>Edellytykset

- Ota **ominaisuuden hallinta**-työtilassa käyttöön toiminto **Arkistoi tulostetut myyntilaskut hajautusarvonumeroilla**. Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Tarvittavien tiedostojen tulostettavat muodot konfiguroidaabn **tulostuksenhallinnassa**.

Tämä toiminto koskee seuraavia asiakirjoja.

**Myyntireskontra**
- Myyntilasku
- Asiakkaan hyvityslasku
- Vapaatekstilasku
- Vapaamuotoinen hyvityslasku

**Projektinhallinta ja kirjanpito**
- Projektilasku
- Projektin hyvityslasku

## <a name="configure-customer-master-data"></a>Asiakkaan päätietojen määritys
Seuraavia ohjeita noudattamalla voit konfiguroida asiakastiedot ja ottaa käyttöön mahdollisuuden tallentaa tulostetut laskut automaattisesti liitteinä.

1. Siirry kohtaan **Myyntireskontra** > **Kaikki asiakkaat**. 
2. Valitse asiakas ja valitse **E-INVOCE**-osan **eInvoice-liite**-kentästä **Lasku ja toimitus** -pikavälilehdestä **Kyllä**.

## <a name="print-invoices"></a>Tulosta laskut
Voit kirjata ja tulostaa minkä tahansa edellisessä menettelyssä määritetyn asiakkaan vapaateksti-, asiakas- ja projektilaskun tai hyvityslaskun.

Avaa tulostetun laskun **Liitteet**-sivu. Etsi tulostetulle laskulle laskettu hajautusnumero **Liite**-pikavälilehden **Lisätiedot**-kenttäryhmän **Asiakirjan hajautusnumero** -kentästä.

![Liitteen hajautusnumero](media/attach-hash-num.jpg)

