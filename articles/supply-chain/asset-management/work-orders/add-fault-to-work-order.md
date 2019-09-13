---
title: Vian lisääminen työtilaukseen
description: Tässä aiheessa kuvataan, miten vikamerkinnät lisätään työtilauksiin käyttöomaisuuden hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875635"
---
# <a name="add-fault-to-work-order"></a>Vian lisääminen työtilaukseen

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Voit lisätä vikasuunnittelijassa vikamäärityksiä työtilaukseen. Työtilauksessa valitulla käyttöomaisuuserällä on oltava käyttöomaisuustyypit, joihin on liitetty yksi tai useita vikatietueita. Lisätietoja määrityksestä on kohdassa [Vikojen hallinta](../setup-for-work-orders/fault-management.md).

1. Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse luettelosta työtilaus, johon haluat tehdä vikamerkinnän, ja valitse **Resurssin vika**.

3. Valitse **Oireet** -pikavälilehdessä **Lisää rivi**. **Vika**-kenttään syötetään automaattisesti vian järjestysnumero.

4. Valitse asiaankuuluva oire **vian oire** -kentästä.

5. Valitse **Vika-alue** ja **Vikatyyppi**.

6. **Vian päivämäärä** -kenttään valitaan automaattisesti nykyinen päivämäärä. Voit muuttaa päivämäärää tarpeen mukaan.

7. Lisää **Valitun oireen syyt** -pikavälilehdessä rivi, joka kuvaa ongelman syytä.

8. Lisää **Valitun oireen korjaukset** -pikavälilehdessä rivi, joka kuvaa ongelman mahdollista ratkaisua.

9. Valitse **Tallenna**.

![Kuva 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Näytä resurssin viat

**Resurssin viat** -luettelossa voit saada yleiskuvan kaikista omaisuuteen rekisteröidyistä virheistä.

Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssin vika** > **Resurssin viat** avatksesi listan.


## <a name="print-asset-fault-report"></a>Tulosta resurssin vikaraportti

**Kaikki resurssit** luettelosivulla voit tulostaa omaisuusvikaraportin, jossa näkyvät kaikki vikamerkinnät sekä graafisen yhteenvedon vikatilastoista.

1. Valitse **Resurssien hallinta**  >  **Yhteiset**  >  **Resurssit**  >  **Kaikki resurssit**.

2. Valitse **Resurssit**-luettelosta resurssi, jolle haluat tulostaa vikaraportin.

3. Valitse **Yleiset**-välilehden **Raportit**-osassa **Resurssin vika**.

4. Lisää tietty kausi tai valitse vikatyyppi.

5. Tulosta raportti valitsemalla **OK**.

>[!NOTE]
>Voit myös tulostaa useiden resurssien tai resurssityyppien vikaraportin valitsemalla **Resurssien hallinta** > **Raportit** > **Resurssit** > **Resurssin vika**.

