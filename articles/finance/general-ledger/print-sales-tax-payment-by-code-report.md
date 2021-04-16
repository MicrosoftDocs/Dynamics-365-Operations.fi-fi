---
title: Arvonlisäveromaksun tulostaminen koodeittain -raportti
description: Tässä ohjeaiheessa on tietoja asetuksista ja toiminnoista, joita tarvitaan, jotta arvonlisäveromaksun koodiraportti voidaan tulostaa kirjanpidon tai verokoodin valuuttana.
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eb3ee4a12d2d29c2769f1ae22e11dc05608b47c1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815449"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>Arvonlisäveromaksun tulostaminen koodeittain -raportti 

[!include [banner](../includes/banner.md)]

Jos haluat tulostaa **Arvonlisäveromaksun koodin perusteella** -raportin, siirry kohtaan **Vero** \> **Tiedustelut ja raportit** \> **Arvonlisäveroraportit** \> **Arvon lisäveromaksu koodin mukaan**. Oletusarvon mukaan raportin summat luodaan yrityksen kirjanpitovaluuttana kaikille raportointikoodeille, jotka on määritetty **Arvonlisäveroilmoituksen koodit** -sivulla.

Voit myös luoda tämän raportin niin, että se näyttää arvonlisäveromaksun summat arvonlisäverokoodien valuuttoina kaikkien niiden raportointikoodien osalta, jotka on liitetty **Arvonlisäverokoodit** -sivun ALV-koodeihin.

## <a name="turn-on-the-feature"></a>Toiminnon ottaminen käyttöön

Ota **Ominaisuuden hallinta** -työtilassa käyttöön seuraava ominaisuus: **Luo arvonlisäveromaksu koodin mukaan -raportti arvonlisäverokoodin valuuttana**.

## <a name="run-the-report"></a>Raportin suorittaminen

1. Siirry kohtaan **Vero** \> **Kyselyt ja raportit** \> **Arvonlisäveroraportit** \> **Arvonlisäveron maksu koodin mukaan**.
2. Valitse **Raportin valuutta** -kentästä jokin seuraavista arvoista:

    - **Kirjanpito valuutta** : Tulosta raportin summat kirjanpitovaluuttana.
    - **Arvonlisäverokoodin valuutta** – Tulosta raportin summat arvonlisäverokoodien valuuttoina.

    ![Arvonlisäveromaksu koodeittain -valintaikkuna](media/Sales-tax-payment-by-code.png)

Seuraavassa kuvassa näkyy esimerkki luotavasta raportista. Raportti osoittaa, että raportointikoodilla **101** on **EUR**-valuutta, jos **Arvonlisäveron valuutta** -kentän arvoksi on määritetty **EUR** sen arvonlisäverokoodin osalta, johon raportointikoodi on liitetty.

![Esimerkki arvonlisäveromaksu koodin mukaan -raportista](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]