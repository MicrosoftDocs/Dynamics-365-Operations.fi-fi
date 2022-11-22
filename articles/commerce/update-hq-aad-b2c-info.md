---
title: Commerce-pääkonttorin päivittäminen uusilla Azure AD B2C -tiedoilla
description: Tässä artikkelissa kerrotaan, miten Microsoft Dynamics 365 Commerce headquarters päivitetään uuden Azure Active Directoryn (Azure AD) kuluttajakaupan tiedoilla.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: c65949ff97182d2692319ac2af00e3ef35a79580
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785265"
---
# <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Commerce-pääkonttorin päivittäminen uusilla Azure AD B2C -tiedoilla

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten Microsoft Dynamics 365 Commerce headquarters päivitetään uuden Azure Active Directoryn (Azure AD) kuluttajakaupan tiedoilla.

Kun Azure AD B2C:n yllä mainitut valmisteluvaiheet on tehty, Azure AD B2C -sovellus on rekisteröitävä Dynamics 365 Commerce -ympäristöön.

Voit päivittää pääkonttorin uusilla Azure AD B2C -tiedoilla seuraavasti.

1. Valitse Commercessa **Kaupan yhteiset parametrit** ja valitse **Tunnistetietojen tarjoajat** vasemmanpuoleisessa valikossa.
1. Tee **Tunnistetietojen tarjoajat** -kohdassa seuraavat toiminnot:
    1. Anna **Myöntäjä**-ruutuun tunnistetietojen tarjoajan myöntäjän merkkijono. Ohjeet myöntäjän merkkijonon löytämiseksi on alla kohdassa [Myöntäjän merkkijonon hankkiminen pääkonttorin määritystä varten](#obtain-issuer-string-for-headquarters-setup).
    1. Anna **Nimi**-ruutuun myöntäjän tietueen nimi.
    1. Anna **Tyyppi**-ruutuun **Azure AD B2C (id_token)**.
1. Valitse yllä mainittu B2C:n tunnistetietojen tarjoajan nimike ja tee **Luovuttavat osapuolet** -kohdassa seuraavat toiminnot:
    1. Syötä **ClientID** -ruutuun kuluttajakauppasovelluksen ominaisuuksien sivun **Sovellustunnus**-ruudussa oleva kuluttajakauppasovelluksen tunnus.
    1. Kirjoita **Tyyppi**-ruutuun **Julkinen**.
    1. Kirjoita **Käyttäjätyyppi**-ruutuun **Asiakas**.
1. Valitse toimintoruudussa **Tallenna**.
1. Hae Commerce-hakuruudussa **Jakeluaikataulu**
1. Valitse **Jakeluaikataulut**-sivun vasemmanpuoleisessa valikossa **1110 Yleinen määritys** -työ.
1. Valitse toimintoruudussa **Suorita nyt**.

### <a name="obtain-issuer-string-for-headquarters-setup"></a>Myöntäjän merkkijonon hankkiminen pääkonttorin määritystä varten

Voit hankkia tunnistetietojen tarjoajan merkkijonon seuraavasti.

1. Siirry Azure-portaalin Azure AD B2C -sivulla **Rekisteröityminen ja sisäänkirjaus** -käyttäjävirtaan.
1. Valitse vasemman siirtymisvalikon **Sivun asettelut**, valitse **Asettelun nimi** -kohdasta **Yhdistetty rekisteröitymis- ja sisäänkirjaussivu** ja valitse sitten **Suorita käyttäjävirta**.
1. Varmista, että sovellus on määritetty edellä luotuun haluttuun Azure AD B2C-sovellukseen, ja valitse sitten käyttäjätyönkulun linkki, joka tulee näkyviin osan ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>`` sisältävän **Suorita käyttäjävirta** -otsikon alle. (Älä valitse **Suorita käyttäjätyönkulku** -kohtaa.) Avautuu uusi välilehti, jossa näkyy metatietoja myöntäjän merkkijonon käytäntöä varten.
1. Kopioi selainvälilehdessä näkyvällä metatietosivulla tunnistetietojen tarjoajan myöntäjän merkkijono (**myöntäjä**-arvo, joka alkaa https:// ja päättyy /v2.0/), joka näyttää samankaltaiselta kuin seuraava esimerkki.
   - ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**TAI**: Voit muodostaa saman metatietojen URL-osoitteen manuaalisesti seuraavasti.

1. Luo metatietojen URL-osoite seuraavassa muodossa käyttämällä B2C-vuokraajaa ja käytäntöä seuraavasti: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Esimerkki: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Kirjoita metatietojen osoitteen URL-osoite selaimen osoitepalkkiin.
1. Kopioi metatiedoissa tunnistetietojen tarjoajan myöntäjän URL-osoite (**myöntäjän** arvo).
    - Esimerkki: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="next-steps"></a>Seuraavat vaiheet

Jos haluat jatkaa kuluttajakaupan vuokraajan määritysprosessia Commercessa, jatka [B2C-vuokraajan määrittäminen Commercen sivustonmuodostimessa](config-b2c-tenant-site-builder.md) -kohtaan.

## <a name="additional-resources"></a>Lisäresurssit

[B2C-vuokraajan määrittäminen Commercessa](set-up-b2c-tenant.md)

[Olemassa olevan Azure AD:n kuluttajakaupan vuokraajan luominen tai linkittäminen Azure-portaalissa](create-link-aad-b2c-tenant.md)

[B2C-sovelluksen luominen](create-b2c-app.md)

[Käyttäjän työnkulkukäytäntöjen luominen](create-user-flow-policies.md)

[Yhteisöpalvelun tunnistetietojen tarjoajien lisääminen (valinnainen)](add-social-identity-providers.md)

[B2C-vuokraajan määrittäminen Commerce-sivuston luontiohjelmassa](config-b2c-tenant-site-builder.md)

[B2C-lisätiedot](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
