---
title: Kassavirtaennusteiden ottaminen käyttöön
description: Tässä artikkelissa käsitellään Kassavirtaennusteet-toiminnon ottamista käyttöön Finance Insightsissa.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 253e3ea9c1c44573b37503f167b4cb3860683c10
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859872"
---
# <a name="enable-cash-flow-forecasting"></a>Kassavirtaennusteiden ottaminen käyttöön

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään Kassavirtaennusteet-toiminnon ottamista käyttöön Finance Insightsissa.

> [!NOTE]
> Jos haluat käyttää kassavirran maksuennusteita, sinun on määritettävä asiakkaan maksuennusteiden toiminto kohdan [Asiakkaan maksuennusteiden käyttöönotto](enable-cust-paymnt-prediction.md) ohjeiden mukaan.
  
1. Avaa **Toimintojen hallinta** -työtila ja toimi seuraavasti:

    1. Valitse **Tarkista päivitysten saatavuus**.
    2. Käytä **Kaikki**-välilehdessä hakusanaa **Kassavirtaennusteet**. Jos ominaisuutta ei löydy, käytä hakusanaa **(Esiversio) Kassavirtaennusteet**. 
    3. Ota toiminto käyttöön.

2. Siirry kohtaan **Maksuliikenteen hallinta \> Kassavirtaennusteen määritys** ja lisää rahatilit, jotka ennusteisiin lisätään. Määritä myös rahatili maksuja varten **Myyntireskontra**- ja **Ostoreskontra**-välilehdissä. Muista laskea kassavirtaennuste uudelleen.

    > [!NOTE]
    > Jos rahatilejä ei ole määritetty, kassavirtaa ei voi luoda.
    >
    > Lisätietoja kassavirtaennusteiden määrittämisestä on kohdassa [Kassavirtaennusteet](../cash-bank-management/cash-flow-forecasting.md).

3. Siirry kohtaan **Maksuliikenteen hallinta \> Asetukset \> Finance Insights (esiversio) \> Kassavirtaennusteet (esiversio)** ja tee seuraavat toiminnot:

    1. Valitse **Kassavirtaennuste**-välilehdessä **Ota toiminto käyttöön**.
    2. Valitse **Luo ennustemalli**.

> [!NOTE]
> **Kassavirtaennuste**-mallin koulutus vaatii tietoja, jotka kattavat yli vuoden ja sisältävät yli 100 tapahtumaa. On suositeltavaa, että käytettävissä on vähintään kahden vuoden edestä tietoja ja yli 1 000 tapahtumaa.

Lisätietoja kassavirtaennusteominaisuudesta on kohdassa [Kassavirtaennusteet](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
