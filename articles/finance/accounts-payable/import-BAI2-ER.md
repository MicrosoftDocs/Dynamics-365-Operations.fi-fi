---
title: Pankkitilin täsmäytyksen edistyneen tuonnin käyttöönottäminen sähköisen raportoinnin avulla
description: Tässä ohjeaiheessa kerrotaan, kuinka sähköisen raportoinnin avulla määritetään edistynyt pankkien täsmäytysprosessi BAI2-tiliotteita varten.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 39f1d8ba561ab0e36346f1dfb4f70df318c92a37
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544507"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Pankkitilin täsmäytyksen edistyneen tuonnin käyttöönottäminen sähköisen raportoinnin avulla

[!include [banner](../includes/banner.md)]

Voit tuoda pankkitilin täsmäytyksen lisätoimintojen avulla sähköiset tiliotteet ja täsmäyttää ne automaattisesti pankkitapahtumien kanssa Microsoft Dynamics 365 Financessa. Tässä aiheessa käsitellään BAI2-tiliotteiden tuontitoimintoa.

## <a name="set-up-the-electronic-reporting-configuration"></a>Määritä sähköisen raportoinnin konfiguraatio

1. Valitse **Työtilat \> Sähköinen raportointi**.
2. Valitse **Microsoft**-määrityspalveluntarjoajan ruudusta **Arkistot**.
3. Valitse **Yleinen** ja valitse sitten **Avaa**.
4. Jos tietovarastoon on oltava yhteys, valitse sininen linkki valintaikkunasta.
5. Konfigurointiluettelosta löytyy **pankin tiliotteen malli \> BAI2-pankkitiliotemalli**.
6. Valitse **BAI2**-muoto.
7. Valitse **Versiot**-pikavälilehdellä valitun uusin versio ja valitse sitten **Tuo**.

## <a name="set-up-the-bank-statement-format"></a>Määritä tiliotemuotoilu

1. Valitse **Maksuliikenteen hallinta \> Asetukset \> Pankkitilin täsmäytyksen lisätoimintojen asetukset \> Tiliotteen muotoilu**.
2. Valitse **Uusi**.
3. Määritä **laskelman muoto**- ja **nimi**-kentät.
4. Valitse **Yleinen sähköinen tuontimuoto** -valintaruutu.
5. Aseta **Tuontimuodon määritys** -kentän arvoksi **BAI2**-muoto.

## <a name="set-up-the-bank-account"></a>Määritä pankkitili

1. Valitse **Maksuliikenteen hallinta \> Pankkitilit \> Pankkitilit**.
2. Avaa pankkitili.
3. Valitse **Täsmäytys**-pikavälilehdessä **Pankkitilin täsmäytyksen lisätoiminnot**-asetukseksi **Kyllä**.
4. Määritä **Tiliotteen muotoilu** -kenttään aiemmin luomasi muoto **BAI2**.

## <a name="import-the-bank-statement"></a>Tuo tiliote

1. Siirry kohtaan **Maksuliikenteen hallinta \> Tiliotteen täsmäytys \> Tiliotteet**.
2. Valitse **Tiliotteet**-sivun yläosasta **Tuo tiliote**.
3. Määritä **Pankkitili**-kenttä tiliotteen pankkitilille.
4. Määritä **Tiliotteen muotoilu** -kenttään aiemmin luomasi muoto **BAI2**.
5. Valitse ensin **Selaa** ja sitten **BAI**-tiedosto.
6. Valitse **Lataa palvelimeen**.
7. Valitse **OK** tuodaksesi valitun tiedoston.
