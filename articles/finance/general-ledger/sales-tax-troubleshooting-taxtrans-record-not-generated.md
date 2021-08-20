---
title: TaxTrans-tietuetta ei luoda
description: Tämä ohjeaihe sisältää vianmääritystietoja, jotka voivat auttaa, kun TaxTrans-tietuetta ei luoda.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 82b00387e39b88e1ab2bc27d9dbc4e36aac3a7a605c04669171997ba236ae39a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751299"
---
# <a name="taxtrans-record-isnt-generated"></a>TaxTrans-tietuetta ei luoda

[!include [banner](../includes/banner.md)]

Jos valitset tapahtumalle **Kirjattu arvonlisävero** ja **Kirjattu arvonlisävero** -sivulla ei ole verorivejä tai verorivi puuttuu, **TaxTrans**-tietuetta ei ehkä ole luotu.

[![Kirjattu arvonlisävero -sivu, jolla ei ole rivinimikkeitä.](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)

Voit ratkaista tämän ongelman noudattamalla seuraavien osien ohjeita tarpeen mukaan.

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a>Tarkista arvonlisävero ennen tapahtuman kirjaamista

1. Tarkista laskelma ennen tapahtuman kirjausta valitsemalla **Laskun kirjaus** -sivulla **Arvonlisävero**.

    [![Arvonlisävero-painike Laskun kirjaus -sivulla.](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)

2. Tarkista **Tilapäiset arvonlisäverotapahtumat** -sivulla laskelman tulos. Jos veroa ei lasketa, katso kohta [Veroa ei lasketa tai veron summa on nolla](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a>TaxTrans-tietueen etsiminen kaikista kirjatuista arvonlisäveroista

1. Valitse **Vero** \> **Kyselyt ja raportit** \> **Arvonlisäverokyselyt** > **Kirjattu arvonlisävero**.
2. Valitse **Tosite**-sarakeotsikossa suodatussymboli etsiäksesi **TaxTrans**-tietueen.
3. Jos löydät etsimäsi arvonlisäverotietueen, tarkista päivämäärä. Jos päivämäärä on eri kuin kirjauskansion otsikon päivämäärä, luo Microsoftin huoltopyyntö lisätuen saamiseksi.

    [![Kirjattu arvonlisävero -sivu.](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)

## <a name="debug-to-check-details"></a>Tarkista suorittamalla virheenkorjaus

1. Lisätietoja virheenkorjauksesta ja siitä, luodaanko **TmpTaxWorkTrans** ja **TaxUncommitted** oikein on kohdassa [TaxTrans-kentän arvo on virheellinen](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).
2. Jos **TaxTmpWorkTrans** tai **TaxUncommitted** on luotu oikein, lisää keskeytyskohta kohteisiin **TaxPost::SaveAndPost()** ja **Tax::SaveAndPost** suorittaaksesi virheenkorjauksen syylle, miksi **TaxTrans**-kohdetta ei lisätä.

    [![Koodiin lisätyt keskeytyskohdat.](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)

    [![Lisättyjen keskeytyskohtien tulokset.](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)

## <a name="determine-whether-customization-exists"></a>Määritä, onko mukautus olemassa

Jos olet suorittanut edellisten osien vaiheet, mutta et ole löytänyt ongelmaa, selvitä, onko mukautus olemassa. Jos mukautusta ei ole, luo Microsoftin huoltopyyntö lisätuen saamiseksi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
