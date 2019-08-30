---
title: Resurssien palvelutasot
description: Tässä ohjeaiheessa kerrotaan resurssien palvelutasoista resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f079e6899a2e3949eff5945f867472c801d9e95c
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783244"
---
# <a name="asset-service-levels"></a>Resurssien palvelutasot

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Tässä ohjeaiheessa kerrotaan resurssien palvelutasoista resurssien hallinnassa. Resurssien palvelutasot liittyvät varoihin, ja ne siirretään ylläpitopyyntöihin ja työtilauksiin. Niitä käytetään työtilausten prioriteetin laskemiseen työtilausten ajoituksen aikana. Resurssien palvelutasoja voidaan muuttaa, jos muutoksia tarvitaan.

Lisätietoja asetuksista, jotka liittyvät työtilausten ajoituksen luokituspisteiden laskentaan, on kohdassa [Resurssien hallinnan parametrit.](../setup-for-objects/enterprise-asset-management-parameters.md) Vähintään yksi oletustietue on määritettävä resurssien palvelutasolle. Tätä oletustietuetta käytetään, jos työtilauksen ajoituksen aikana ei löydy muuta vastaavuutta.

**Esimerkki 1:** oletuspalvelutaso, jota käytetään, jos muita vastaavuutta ei löydy. Tässä tietueessa valitaan vain palvelutaso.

**Esimerkki 2:** korkea palvelutaso, jota käytetään töiden ajoittamiseen Volvo-rekan moottoreille. Tässä tietueessa valitaan asiaankuuluva resurssityyppi (kuten **kuorma-auton moottori**), valmistaja (**Volvo**) ja palvelutaso.

## <a name="set-up-asset-service-levels"></a>Resurssien palvelutasojen määrittäminen

1. valitse **Resurssien hallinta** \> **Asetukset** \> **Resurssien palvelutasot**.
2. Luo tietue valitsemalla **Uusi**.
3. Resurssien palveluasolle vaadittavien yksityiskohtien tasosta riippuen tee asiaankuuluvat valinnat kentissä **Toiminnallinen sijainti**, **Resurssin tyyppi**, **Valmistaja**, **Malli**, **Resurssi**, **Työtilauksen tyyppi** ja **Palvelutaso**.

    > [!NOTE]
    > Kun resurssien palvelutasoa käytetään kunnossapitopyyntöihin ja työtilauksiin, resurssien hallinta käy läpi kaikki resurssien palvelutasotietueet mahdollisen vastaavuuden tarkastamiseen. Se tarkistaa aina kaikkein erikoisimman yhdistelmän ensin. Toisin sanoen resurssien hallinta tarkistaa ensin **Työtilauksen tyyppi** -kentän vastaavuuden. Jos vastaavuutta ei löydy, se tarkistaa **Resurssit** -kentän vastaavuuden ja niin edelleen. Kuten näet **resurssien palvelutasot** -sivun asettelussa, tämä tarkoittaa sitä, että jos haluat löytää erityisen yhdistelmän, resurssien hallinta tarkistaa kunkin tietueen oikealta vasemmalle, jotta se vastaa toisiaan. Jos vastaavuutta ei löydy, käytetään oletustietuetta, jolla ei ole valintoja kyseisissä kentissä.

4. Valitse **Palvelutaso**-kentässä numero, joka ilmaisee palvelutason (prioriteetin).


> [!NOTE]
> Jos muutat resurssien palvelutasotietuetta **Resurssien palvelutasot** -sivulla sen jälkeen, kun olet jo käyttänyt sitä työtilauksessa, kunnossapitopyyntöjen ja työtilausten palvelutasoa ei päivitetä vastaavasti.