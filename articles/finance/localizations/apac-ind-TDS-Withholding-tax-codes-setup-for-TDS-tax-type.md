---
title: Ennakonpidätyskoodien määrittäminen TDS-verotyypille
description: Tässä artikkelissa kerrotaan, miten Vero vähennettynä lähteissä (TDS) -verokoodit määritetään.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: fabe14b74c445434c37cb6ee79597d37affb162d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904380"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a>Ennakonpidätyskoodien määrittäminen TDS-verotyypille

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten Vero vähennettynä lähteissä (TDS) -verokoodit määritetään.

1. Siirry kohtaan **Vero \> Välilliset verot \> Ennakonpidätys \> Ennakonpidätyskoodit**.

    [![Ennakonpidätyskoodit-sivu.](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)

2. Valitse toimintoruudusta **Uusi**, jos haluat luoda TDS:lle ennakonpidätyskoodin, ja syötä tarvittavat tiedot.
3. Valitse **Yleinen**-pikavälilehden **Verotyyppi**-kentästä **TDS**, jos haluat luokitella verokoodin TDS-verokoodiksi.
4. Valitse **Tilityskausi**-kentässä TDS-verokoodin TDS-tilityskausi.
5. Valitse **Päätili**-kentässä kirjanpitotili, jonne TDS-summa kirjataan.
6. Valitse **Myyntireskontra**-kentässä myyntireskontratili, jolle myyntitapahtumista vähennetty TDS-summa kirjataan.

    **Alkuperä**-kentän arvoksi määritetään automaattisesti **Prosenttia bruttosummasta**, eikä arvoa voi muuttaa.

    > [!NOTE]
    > TDS-verotyypin verokoodien alkuperäksi ei voi määrittää **Prosenttia nettosummasta**.

7. Valitse **Ennakonpidätyksen komponentti** -kentässä TDS-verokoodin TDS-verokomponentti.
8. Valitse toimintoruudussa **Arvot** avataksesi **Ennakonpidätyksen arvot** -sivun.
9. **Päivämäärästä**-kentässä syötä TDS-arvon aloituspäivämäärä. Syötä **Päivämäärään**-kenttään päättymispäivämäärä.

    > [!NOTE]
    > **Vähimmäisraja**-, **Yläraja**- ja **Sulkemis-%**-kentät eivät ole käytettävissä TDS-verotyypin verokoodeissa.

10. Syötä **Arvo**-kenttään TDS-verokoodin TDS-prosentti.
11. Sulje **Ennakonpidätyksen arvot** -sivu palataksesi **Ennakonpidätyskoodit**-sivulle.

    > [!NOTE]
    > **Ennakonpidätyskoodit**-sivun **Rajat**-painike ei ole käytettävissä TDS-verotyypin verokoodeissa.

12. Sulje sivu.
