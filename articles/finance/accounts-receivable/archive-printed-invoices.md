---
title: Arkistoi tulostetut myyntilaskut hajautusarvonumeroilla
description: Tässä artikkelissa kuvataan, kuinka arkistointi otetaan käyttöön, jotta tulostetut asiakaslaskut voidaan tallentaa hajautusnumeroilla.
author: mrolecki
ms.date: 09/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.custom: 539093
ms.search.form: ''
ms.openlocfilehash: 4c9bd7ead1615a4e6b0e8e672e858312ba518b56
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291666"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Arkistoi tulostetut myyntilaskut hajautusarvonumeroilla

[!include [banner](../includes/banner.md)]

Joissakin maissa on lakisääteinen vaatimus tallentaa järjestelmään joidenkin tiedostojen tulosteet sekä lasketut hajautusnumerot. Hajautusnumeroita voidaan käyttää viranomaisille raportoitaessa ja auditoinnissa.

Tässä artikkelissa kuvataan, kuinka arkistointi määritetään, jotta tulostetut asiakaslaskut voidaan tallentaa hajautusnumeroilla.

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

![Liitteen hajautusnumero.](media/attach-hash-num.jpg)

