---
title: Resurssin kriittisyystyypit
description: Aiheessa selitetään resurssin kriittisyystyypit resurssien hallinnassa.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetCriticality, EntAssetObjectCriticality
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9edf55c22375a66fda04ae7ff76d7a0a191140e5ffb3a377b9ac1a7ba604a8d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776917"
---
# <a name="asset-criticality-types"></a>Resurssin kriittisyystyypit

[!include [banner](../../includes/banner.md)]

 

Aiheessa selitetään resurssin kriittisyystyypit resurssien hallinnassa. Resurssin kriittisyys liittyy resursseihin ja ne siirretään työtilauksiin. Sitä ei voi muuttaa työtilauksessa. Resurssin kriittisyyttä käytetään laskettaessa työtilauksen kriittisyyttä työtilausten ajoituksessa. Toisin sanoen sen avulla lasketaan, missä määrin resurssin kunnossapitotyö vaikuttaa yrityksen tuotantoaikatauluun ja tuottavuuteen. Lisätietoja asetuksista, jotka liittyvät työtilausten ajoituksen luokituspisteiden laskentaan, on kohdassa [Resurssien hallinnan parametrit.](../setup-for-objects/enterprise-asset-management-parameters.md)

Voit määrittää kriittisyyden määrittämällä ensin kriittisyystyypit, joita käytetään resurssin asetuksissa. Sen jälkeen määritetään resurssin kriittisyydet.

## <a name="set-up-criticality-types"></a>Määritä kriittisyystyypit

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **resurssit** \> **Kriittisyystyypit**.
2. Luo tietue valitsemalla **Uusi**.
3. Kirjoita **Kriittisyys**-kenttään numero, joka ilmaisee kriittisyyden.
4. Kirjoita **Nimi**-kenttään kriittisyystyypin nimi.
5. Syötä **Kerroin**-kenttään kerroin. Tätä kerrointa käytetään työtilausten ajoittamisen laskennassa, kun määritetään käytettävä kriittisyystietue. (Tietuetta, jonka kerroin on korkein, käytetään aina.) Tämä asetus on merkityksellinen, jos, kuten seuraavasta kuvasta näkyy, luodaan kriittisyysrivejä, joilla on sama kriittisyysarvo.

    ![Kriittisyystyypit-sivu.](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a>Määritetä resurssin kriittisyydet.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Resurssin kriittisyydet**.
2. Luo tietue valitsemalla **Uusi**.
3. Tee tarvittavat valinnat seuraavista kentistä sen mukaan, miten yksityiskohtaista resurssin kriittisyyttä tarvitaan: **Toiminnallinen sijainti**, **resurssityyppi**, **Valmistaja**, **malli**, **resurssi**, **Työtyypin luokka**, **Työtyyppi**, **Työtyypin variantti** ja **Työtarve**.

    > [!NOTE]
    > Kun resurssin kriittisyys on valittuna, resurssien hallinta käy läpi kaikki resurssin kriittisyystietueet ja tarkistaa mahdollisen osuvuuden. Se tarkistaa aina kaikkein erikoisimman yhdistelmän ensin. Toisin sanoen resurssien hallinta tarkistaa ensin **Työtarve**-kentän. Jos vastaavuutta ei löydy, se tarkistaa **Työtyypin variantti** -kentän. Jos vastaavuutta ei löydy, se tarkistaa **Työtyyppi**-kentän jne. Kuten näet sivun asettelussa, tämä tarkoittaa sitä, että jos haluat löytää erityisen yhdistelmän, omaisuuden hallinta tarkistaa kunkin tietueen oikealta vasemmalle, jotta se vastaa toisiaan. Jos vastaavuutta ei löydy, käytetään oletustietuetta, jolla ei ole valintoja.

4. Valitse **Kriittisyys**-kentästä jokin edellisessä menettelyssä luomasi kriittisyyden arvo.

### <a name="notes-about-criticality-setup"></a>Huomautuksia kriittisyysasetuksista

- Jos muutat resurssin kriittisyyttä tässä määrityksessäjälkeen, kun olet jo käyttänyt sitä työtilauksessa, työtilauksen kriittisyyttä ei päivitetä vastaavasti.
- Työtilauksen kriittisyys lasketaan uudelleen aina, kun työtilausivi lisätään työtilaukseen tai poistetaan siitä.
- Jos työtilaus sisältää useita työtilaustöitä, suurin kriittisyys, joka määräytyy **Kriittisyystyypit**-sivun **kerroin**-kentän mukaan, on aina käytössä työtilauksessa.
- Yleensä resurssin kriittisyys voi muuttua kauden aikana. Kriittisyyteen voidaan vaikuttaa ostamalla uusia laitteita, kunnostustöitä, ja niin edelleen. Harkitse resurssien kriittisyyden uudelleenarviointia säännöllisin väliajoin (esimerkiksi kerran vuodessa tai joka toinen vuosi) varmistaaksesi, että kriittisyysmääritykset vastaavat nykyisiä tuotannon asetuksia.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]