---
title: Hyvityslaskujen alennuksia sisältävän toimittajan osamaksun tilittäminen
description: Tässä artikkelissa käydään läpi skenaario, jossa hyvityslasku selvitetään laskua vastaan.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 14222
ms.assetid: 2b19f7fd-9ff9-4ee4-bddf-f582946d008e
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
ms.openlocfilehash: b926d94059fb12b143b9c9b4b5c04cb7f39f8e99
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715934"
---
# <a name="settle-a-partial-vendor-payment-that-has-discounts-on-credit-notes"></a>Hyvityslaskujen alennuksia sisältävän toimittajan osamaksun tilittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käydään läpi skenaario, jossa hyvityslasku selvitetään laskua vastaan.

Fabrikamin toimittajat antavat käteisalennuksia hyvityslaskuista. Toimittaja 3050 antaa Fabrikamille 1 prosentin käteisalennuksen, jos lasku maksetaan 14 päivän kuluessa.

## <a name="invoice-and-credit-memo"></a>Lasku ja hyvityslasku
April luo 29. kesäkuuta 1 000,00 arvoisen laskun toimittajalle 3050. 2. heinäkuuta hän luo 200,00 arvoisen hyvityslaskun. **Toimittajat**-sivulla April avaa **Selvitä tapahtumat** -sivun. Hän voi merkitä molemmat hyvityslaskut ja tilitettävän laskun **Selvitä tapahtumat** -sivulla. Hyvityslaskun alennukseksi lasketaan 2,00. Tämän vuoksi hyvityslaskun kokonaisarvoksi pienennetään 198,00.

| Merkitse                     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valittu                 | Normaali            | Var-10070 | 3050    | 29.6.2015 | 29.7.2015 | 10070   | -1 000,00                      | USD      | -990,00          |
| Valitut ja korostetut | Normaali            | KR-10070  | 3050    | 2.7.2015  | 29.7.2015 |         | 200,00                         | USD      | 198,00           |

Hyvityslaskun alennustiedot näkyvät **Tilitä avoimet tapahtumat** -sivun alaosassa.

| Kenttä                        | Arvo     |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 13.7.2015 |
| Käteisalennussumma         | 2.00      |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | 2,00      |

April valitsee **Kirjaa**-kohdan. Hän tarkistaa valmiin tilityksen. April huomaa, että käytettiin hyvityslaskua, jonka arvo oli 198,00, ja annettiin alennus, joka oli 2,00. Kokonaissumma on siis 200,00.

| Merkitse                     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku  | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Valitut ja korostetut | Normaali            | Var-10070 | 3050    | 29.6.2015 | 29.7.2015 | 10070    | -1 000,00                      | USD      | -200,00          |
| Valittu                 | Normaali            | KR-10070  | 3050    | 2.7.2015  | 29.7.2015 | KR-10070 | 200,00                         | USD      | 198,00           |

April voi tarkistaa toimittajan tapahtumat **Toimittajan tapahtumat** -sivulla valitsemalla toimittajan **Kaikki toimittajat**-sivulla ja valitsemalla sitten toimintopaneelissa **Tapahtumat**. Tällä sivulla April näkee, että laskun saldo on -800,00. Näkyvillä ovat myös hyvityslasku (198,00) ja alennus (2,00).

| Tosite    | Tapahtumatyyppi | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo | Valuutta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Var-10070  | Lasku          | 29.6.2015 | 10070   |                                      | 1 000,00                              | -800,00 | USD      |
| Var-10071  |                  | 2.7.2015  | CR10071 | 200,00                               |                                       | 0,00    | USD      |
| ALE-10071 |  Käteisalennus   | 2.7.2015  |         | 2,00                                 |                                       | 0,00    | USD      |
| ALE-10071 |  Käteisalennus   | 2.7.2015  |         |                                      | 2,00                                  | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
