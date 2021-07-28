---
title: Ennakonpidätyksen raportointikoodien määrittäminen TDS-verotyypille
description: Ennakonpidätyksen raportointikoodien avulla luodaan lomakkeen 26Q ja lomakkeen 27Q ilmoitukset Vero vähennettynä lähteissä (TDS) -tiedoille. Tässä ohjeaiheessa kerrotaan, miten ennakonpidätyksen raportointikoodien vaiheet määritetään TDS-raportointikoodien määrittämiseksi.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: c74132af95f088ea88155b722a8270861fba50e7
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361283"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a>Ennakonpidätyksen raportointikoodien määrittäminen TDS-verotyypille

[!include [banner](../includes/banner.md)]

Ennakonpidätyksen raportointikoodien avulla luodaan lomakkeen 26Q ja lomakkeen 27Q ilmoitukset Vero vähennettynä lähteissä (TDS) -tiedoille. Tässä ohjeaiheessa kerrotaan, miten ennakonpidätyksen raportointikoodien vaiheet määritetään TDS-raportointikoodien määrittämiseksi.

1. Siirry kohtaan **Vero \> Asetukset \> Ennakonpidätys \> Ennakonpidätyksen raportointikoodit**.

    [![Ennakonpidätyksen raportointikoodit -sivu.](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)

2. Valitse **Verotyyppi**-kentässä **TDS** määrittääksesi ennakonpidätyksen raportointikoodit TDS-verotyypille.
3. Valitse **Ennakonpidätyksen komponentti** -kentässä TDS-komponentti, jota varten määrität ennakonpidätyksen raportointikoodin. **Ennakonpidätyksen komponenttiryhmä** -kentässä näkyy TDS-komponenttiryhmä, joka on määritetty määrittämällesi TDS-komponentille.

    **Yleinen**-pikavälilehden **Osakoodi**-kentässä näkyy osakoodi, joka on liitetty TDS-komponenttiryhmään.

4. Valitse TDS-raportointikoodi **Yleinen**-pikavälilehden **Raportointikoodi**-kentässä:

    - TDS
    - TCS
    - Lisämaksu
    - PE\_Cess
    - SHE\_Cess

5. Sulje sivu.
