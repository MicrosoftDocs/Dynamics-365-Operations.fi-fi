---
title: Käyttäjän työnkulkukäytäntöjen luominen
description: Tässä artikkelissa kerrotaan käyttäjän työkulun käytäntöjen luomisesta Microsoft Azure -portaalissa.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 91b9d99dfd8c3d100ca197aa499ca86799bbffc8
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785255"
---
# <a name="create-user-flow-policies"></a>Käyttäjän työnkulkukäytäntöjen luominen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan käyttäjän työkulun käytäntöjen luomisesta Microsoft Azure -portaalissa.

Käyttäjän työnkulut ovat käytäntöjä, joita Azure Active Directoryn (Azure AD) kuluttajakauppa käyttää suojatun sisäänkirjauksen, rekisteröitymisen, profiilin muokkaamisen ja unohdetun salasanan käyttökokemusten määrittämisessä. Dynamics 365 Commerce suorittaa näiden työnkulkujen avulla käytäntöjen toiminnot, joiden avulla se toimii Azure AD B2C -vuokraajan kanssa. Kun käyttäjä käyttää näitä käytäntöjä, ne ohjataan uudelleen Azure AD:n kuluttajakaupan vuokraajalle toimintojen suorittamista varten.

Azure AD B2C sisältää seuraavat kolme käyttäjän perustyönkulkutyyppiä:
- Rekisteröityminen ja sisäänkirjaus
- Profiilin muokkaaminen
- Salasanan palauttaminen

Voit halutessasi käyttää Azure AD:n käyttäjän oletustyönkulkua. Se näyttää Azure AD B2C:n isännöimän sivun. Vaihtoehtoisesti voit luoda HTML-sivun, jonka avulla hallitaan näiden käyttäjän työnkulkukokemusten ulkoasua. 

Jos haluat mukauttaa Dynamics 365 Commercella luotuja käyttäjän käytäntöjen sivuja, katso [Käyttäjän sisäänkirjausten mukautettujen sivujen määrittäminen](custom-pages-user-logins.md). Lisätietoja on kohdassa [Azure Active Directoryn kuluttajakaupan käyttäjäkokemusten käyttöliittymän mukauttaminen](/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulkukäytännön luominen

Voit luoda rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulkukäytännön seuraavasti.

1. Valitse Azure-portaalin vasemmanpuoleisessa siirtymisruudussa **Käyttäjän työnkulut (käytännöt)**.
1. Valitse **Azure AD B2C – käyttäjän työnkulut (käytännöt)** -sivulla **Uusi käyttäjän työnkulku**.
1. Valitse **Rekisteröinti ja sisäänkirjaus** -käytäntö ja sitten **Suositellut**-versio.
1. Anna käytännön nimi **Nimi**-kohdassa. Tämä nimi näkyy myöhemmin portaalin määrittämän etuliitteen kanssa (esimerkiksi B2C_1_).
1. Valitse **Tunnistetietojen tarjoajat** -kohdan **Paikalliset tilit** -osasta **Sähköpostirekisteröityminen**. Sähköpostitodennusta käytetään yleisimpiä Commerce-skenaarioita varten. Jos käytät myös henkilöllisyyden palveluntarjoajan todennusta, voit valita ne myös tässä.
1. Valitse **Usean tekijän todennus** yritykselle soveltuva vaihtoehto. 
1. Valitse **Käyttäjän määritteet ja vaatimukset** -kohdassa vaihtoehdot määritteiden tai palautusvaatimusten keräämistä varten. Valitse **Näytä lisää...**, jotta saat koko luettelon määritteistä ja claim-vaihtoehdoista. Commerce edellyttää seuraavien oletusasetusten käyttämistä:

    | **Keräilymäärite** | **Palautusvaatimus** |
    | ---------------------- | ----------------- |
    | Sähköpostiosoite          | Sähköpostiosoitteet   |
    | Etunimi             | Etunimi        |
    |                        | Tunnistetietojen toimittaja |
    | Sukunimi                | Sukunimi           |
    |                        | Käyttäjän objektin tunnus  |

1. Valitse **Luo**.

Seuraavassa kuvassa on esimerkki Azure AD B2C:n rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulusta.

![Rekisteröinti ja sisäänkirjaus -käytännön asetukset.](./media/B2CImage_11.png)

   
### <a name="create-a-profile-editing-user-flow-policy"></a>Profiilin muokkaamisen käyttäjän työnkulkukäytännön luominen

Voit luoda profiilin muokkaamisen käyttäjän työnkulkukäytännön seuraavasti.

1. Valitse Azure-portaalin vasemmanpuoleisessa siirtymisruudussa **Käyttäjän työnkulut (käytännöt)**.
1. Valitse **Azure AD B2C – käyttäjän työnkulut (käytännöt)** -sivulla **Uusi käyttäjän työnkulku**.
1. Valitse **Profiilin muokkaus** ja valitse sitten **Suositeltu**-versio.
1. Anna **Nimi**-kohtaan profiilin muokkaamisen käyttäjän työnkulku. Tämä nimi näkyy myöhemmin portaalin määrittämän etuliitteen kanssa (esimerkiksi B2C_1_).
1. Valitse **Tunnistetietojen tarjoajat** -kohdan **Paikalliset tilit** -osasta **Sähköpostikirjautuminen**.
1. Valitse **Käyttäjän määritteet** -kohdassa seuraavat valintaruudut:
    
    | **Keräilymäärite** | **Palautusvaatimus** |
    | ---------------------- | ----------------- |
    |                        | Sähköpostiosoitteet   |
    | Etunimi             | Etunimi        |
    |                        | Tunnistetietojen toimittaja |
    | Sukunimi                | Sukunimi           |
    |                        | Käyttäjän objektin tunnus  |
    
1. Valitse **Luo**.

Seuraavassa kuvassa on esimerkki Azure AD B2C:n profiilin muokkauksen käyttäjän työnkulusta.

![Azure AD B2C -profiilin muokkaamisen käyttäjän työnkulun esimerkki](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Salasanan palauttamisen käyttäjän työnkulkukäytännön luominen

Voit luoda salasanan palauttamisen käyttäjän työnkulkukäytännön seuraavasti.

1. Valitse Azure-portaalin vasemmanpuoleisessa siirtymisruudussa **Käyttäjän työnkulut (käytännöt)**.
1. Valitse **Azure AD B2C – käyttäjän työnkulut (käytännöt)** -sivulla **Uusi käyttäjän työnkulku**.
1. Valitse **Salasanan nollaus** ja valitse sitten **Suositeltu**-versio.
1. Anna **Nimi**-kohtaan salasanan palauttamisen käyttäjän työnkulun nimi.
1. Valitse **Tunnistetietojen tarjoajat** -kohdassa **Nollaa salasana sähköpostiosoitteen avulla**.
1. Valitse **Luo**.
1. Valitse **Sovelluksen vaatimukset** -kohdassa seuraavat valintaruudut:
    - **Sähköpostiosoitteet**
    - **Etunimi**
    - **Sukunimi**
    - **Käyttäjän objektin tunnus**
1. Valitse **Luo**.

Seuraavassa kuvassa näytetään, miten **Palauta salasana sähköpostiosoitteen avulla** määritetään Azure AD B2C:n salasanan palauttamisen käyttäjän työnkulussa.

![Salasanan palauttamisen käytännön Palauta salasana sähköpostiosoitteen avulla -kohdan määrittäminen](./media/B2CImage_13.png)

## <a name="next-steps"></a>Seuraavat vaiheet

Jos haluat jatkaa kuluttajakaupan vuokraajan määrittämisprosessia Commercessa, jatka [Yhteisöpalvelun tunnistetietojen tarjoajien lisääminen](add-social-identity-providers.md) -kohtaan.

## <a name="additional-resources"></a>Lisäresurssit

[B2C-vuokraajan määrittäminen Commercessa](set-up-b2c-tenant.md)

[Olemassa olevan Azure AD:n kuluttajakaupan vuokraajan luominen tai linkittäminen Azure-portaalissa](create-link-aad-b2c-tenant.md)

[B2C-sovelluksen luominen](create-b2c-app.md)

[Yhteisöpalvelun tunnistetietojen tarjoajien lisääminen (valinnainen)](add-social-identity-providers.md)

[Commerce headquartersin päivittäminen uusilla Azure AD:n kuluttajakaupan tiedoilla](update-hq-aad-b2c-info.md)

[B2C-vuokraajan määrittäminen Commerce-sivuston luontiohjelmassa](config-b2c-tenant-site-builder.md)

[B2C-lisätiedot](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
