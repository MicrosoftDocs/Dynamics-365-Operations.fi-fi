---
title: Resurssin palvelutasot
description: Tässä artikkelissa kerrotaan resurssien palvelutasoista resurssien hallinnassa.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f7429b30253f540925e67ff9239667a0a404f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908682"
---
# <a name="asset-service-levels"></a>Resurssin palvelutasot

[!include [banner](../../includes/banner.md)]

 

Tässä artikkelissa kerrotaan resurssien palvelutasoista resurssien hallinnassa. Resurssien palvelutasot liittyvät varoihin, ja ne siirretään ylläpitopyyntöihin ja työtilauksiin. Niitä käytetään työtilausten prioriteetin laskemiseen työtilausten ajoituksen aikana. Resurssien palvelutasoja voidaan muuttaa, jos muutoksia tarvitaan.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]