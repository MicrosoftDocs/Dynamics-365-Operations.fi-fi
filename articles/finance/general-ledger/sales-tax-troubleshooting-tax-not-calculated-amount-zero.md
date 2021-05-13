---
title: Veroa ei lasketa tai veron summa on nolla.
description: Tässä aiheessa on vianmääritystietoja, jotka voivat auttaa, kun veron summa on 0 (nolla) tai veroa ei lasketa.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ead979081692d4dcee9812c89f5f10c7879d3f7e
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947632"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a>Veroa ei lasketa tai veron summa on nolla.

[!include [banner](../includes/banner.md)]

Tapahtuman rivisumma ei ole välttämättä 0 (nolla), mutta joko veroa ei lasketa tai laskettu verosumma on 0. Voit ratkaista tämän ongelman noudattamalla seuraavien osien ohjeita tarpeen mukaan.

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a>Tarkista, että tapahtuma on valinnut verokoodit oikein

Jos tapahtuma ei valitse oikeita verokoodeja tai jos se ei valitse mitään verokoodeja, veroja ei lasketa sen perusteella. Tarkista, että tapahtuma on valinnut verokoodit oikein, näiden ohjeiden avulla. 

1. Varmista tapahtumarivin **Rivitiedot**-pikavälilehden **Asetukset**-välilehden **Arvonlisävero**-osassa, että oikeat veroryhmät ovat valittuina **Nimikkeen arvonlisäveroryhmä**- ja **Arvonlisäveroryhmä**-kentissä. Jos oikeat veroryhmät eivät ole valittuina, valitse ne.

    [![Nimikkeen arvonlisäveroryhmä- ja Arvonlisäveroryhmä-kentät](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)

2. Siirry kohtaan **Vero** \> **Välilliset verot** \> **Arvonlisävero** \> **Arvonlisäveroryhmät**.
3. Valitse haluamasi arvonlisäveroryhmä ja tee sitten huomautus **Arvonlisäverokoodi**-kentän verokoodista **Asetukset**-pikavälilehdessä.

    [![Arvonlisäveroryhmät-sivu](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)

4. Siirry kohtaan **VeroTax** \> **Välilliset verot** \> **Arvonlisävero** \> **Arvonlisäveroryhmät**.
5. Valitse asianmukainen nimikkeen arvonlisäveroryhmä ja varmista **Asetukset**-pikavälilehdessä, että **Arvonlisäverokoodi**-kentän verokoodi vastaa arvonlisäveroryhmän verokoodia.

    [![Nimikkeiden arvonlisäveroryhmät -sivu](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)

6. Jos verokoodit eivät täsmää, päivitä yhden ryhmän arvonlisäverokoodi.

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a>Varmista, että valittuja verokoodeja ei ole vapautettu ja että niiden veroprosenttiarvo on oikea.

Jos verokoodit ovat vapautettuja tai jos veroprosentti on 0 (nolla), veron laskentatulos on 0. Seuraavia ohjeita noudattamalla voit määrittää, ovatko valitut verokoodit vapautettuja, ja tarkistaa, että veroihin sovelletaan oikeaa veroprosenttia.

1. Siirry kohtaan **Vero** \> **Välilliset verot** \> **Arvonlisävero** \> **Arvonlisäveroryhmät**.
2. Valitse haluamasi arvonlisäveroryhmä ja varmista sitten **Asetukset**-pikavälilehdessä, että **Vapautus**-valintaruutua ei ole. Jos se on valittuna, poista valinta.

    [![Arvonlisäveroryhmät-sivun Vapautus-valintaruutu](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)

3. Valitse **Vero** \> **Välilliset verot** \> **Arvonlisävero** \> **Arvonlisäverokoodit**.
4. Valitse asianmukainen arvonlisäverokoodi ja varmista sitten, että **Arvo**-kentän veroprosenttiarvo ei ole 0 (nolla). Jos arvo on 0, päivitä kenttä niin, että sen arvoksi on määritetty oikea veroprosentti.

    [![Arvonlisäverokoodin arvot -sivun Arvo-kenttä](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a>Määritä, onko oikea verosumma nolla

Joissakin tilanteissa verosumma 0 (nolla) on oikea. Seuraavia ohjeita noudattamalla voit määrittää, onko tapahtumalle oikea verosumma 0.

1. Siirry kohtaan **Kirjanpito** \> **Kirjanpidon asetukset** \> **Kirjanpitoparametrit**.
2. **Arvonlisävero**-välilehden **Laskentatapa**-kentässä vahvista, että **Yhteensä** on valittuna.

    [![Kirjanpitoparametrit-sivun Laskentatapa-kenttä](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)

3. Valitse **Vero** \> **Välilliset verot** \> **Arvonlisävero** \> **Arvonlisäverokoodit**.
4. Valitse asianmukainen arvonlisäverokoodi, valitse **Laskenta** \> **Alv-rajan peruste** ja vahvista, että alv-rajan perusteen arvona on **Laskun saldon nettosumma** tai **Laskun loppusumma muut arvonlisäverosummat mukaan luettuna**. Lisätietoja on kohdassa [Laskun loppusumma muut arvonlisäverosummat mukaan luettuna](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).
5. Jos oikeat arvot on määritetty vaiheissa 2 ja 4, määritä, onko tapahtuman kokonaissumma 0 (nolla). Jos kokonaissumma on 0, odotettu tulos on veron summa 0. Koska veron laskenta perustuu laskun saldon kokonaissummaan eikä summaa ole rivi riviltä, veron summa 0 kohdistetaan kullekin riville veron laskennan jälkeen.

## <a name="determine-whether-customization-exists"></a>Määritä, onko mukautus olemassa

Jos olet suorittanut edellisten osien vaiheet, mutta et ole löytänyt ongelmaa, selvitä, onko mukautus olemassa. Jos mukautusta ei ole, luo Microsoftin huoltopyyntö lisätuen saamiseksi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
