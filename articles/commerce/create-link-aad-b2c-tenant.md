---
title: Olemassa olevan Azure AD B2C -vuokraajan luominen tai linkittäminen Azure-portaalissa
description: Tässä artikkelissa kerrotaan, miten olemassa olevan Azure Active Directoryn (Azure AD) kuluttajakaupan vuokraaja luodaan ja miten siihen linkitetään Microsoft Azure -portaalissa.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 0aa12387f00ffc3dd10688c6385c7952f089ab12
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785250"
---
# <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>Olemassa olevan Azure AD B2C -vuokraajan luominen tai linkittäminen Azure-portaalissa

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten Azure Active Directoryn (Azure AD) kuluttajakaupan vuokraaja luodaan ja miten siihen linkitetään Microsoft Azure -portaalissa. Lisätietoja: [Opas: Luo Azure Active Directory B2C -vuokraaja](/azure/active-directory-b2c/tutorial-create-tenant).

Voit luoda Azure AD:n kuluttajakaupan vuokraajan tai linkittää siihen Azure-portaalissa alla olevien ohjeiden mukaan.

1. Kirjaudu [Azure-portaalin osoitteessa](https://portal.azure.com/).
1. Valitse Azure-portaalin valikossa **Luo resurssi**. Varmista,. että käytät tilausta ja hakemistoa, joka yhdistetään Commerce-ympäristöön.

    ![Resurssin luominen Azure-portaalissa.](./media/B2CImage_1.png)

1. Siirry kohtaan **Tunnistetiedot \> Azure Active Directory B2C**.
1. Käytä **Uuden B2C-vuokraajan luominen tai linkittäminen olemassa olevaan vuokraajaan** -sivulla seuraavista vaihtoehdoista sitä, joka sopii yrityksen tarpeisiin parhaiten:

    - **Luo uusi Azure AD B2C -vuokraaja**: Käytä tätä vaihtoehtoa, jos haluat luoda uuden Azure AD B2C -vuokraajan.
        1. Valitse **Luo uusi Azure AD B2C -vuokraaja**.
        1. Määritä **Organisaation nimi** -kohdassa organisaation nimi.
        1. Anna **Alkuperäinen toimialueen nimi** -kohdassa alkuperäinen toimialueen nimi.
        1. Valitse **Maa tai alue** -kohdassa maa tai alue.
        1. Valitse **Luo**, jos haluat luoda vuokraajan.

     ![Uuden Azure AD -vuokraajan luominen.](./media/B2CImage_2.png)

     - **Linkitä olemassa oleva Azure AD B2C -vuokraaja omaan Azure-tilaukseen**: Käytä tätä vaihtoehtoa, jos sinulla on jo Azure AD B2C -vuokraaja, johon haluat linkittää.
        1. Valitse **Linkitä olemassa oleva Azure AD B2C -vuokraaja Azure-tilaukseen**.
        1. Valitse **Azure AD B2C -vuokraaja** -kohdassa soveltuva B2C-vuokraaja. Jos valintaikkunaan tulee Kelvollisia B2C-vuokraajia ei löytynyt -sanoma, sinulla ei ole olemassa olevaa B2C-vuokraajaa, vaan se on luotava.
        1. Valitse **Resurssiryhmä**-kohdassa **Luo uusi**. Anna **nimi** resurssiryhmälle, joka sisältää vuokraajan ja valitse **Resurssiryhmän sijainti**. Valitse lopuksi **Luo**.

    ![Linkitä olemassa oleva Azure AD B2C -vuokraaja Azure-tilaukseen.](./media/B2CImage_3.png)

1. Kun uusi Azure AD B2C -hakemisto on luotu (tämä voi kestää jonkin aikaa), koontinäyttöön tulee näkyviin uuden hakemiston linkki. Tämä linkki ohjaa sinut Tervetuloa Azure Active Directory B2C -ratkaisun käyttäjäksi -sivulle.

    ![Linkki uuteen Azure AD -hakemistoon.](./media/B2CImage_4.png)

> [!NOTE]
> Jos sinulla on useita Azure-tilin tilauksia tai jos olet määrittänyt B2C-vuokraajan ilman aktiivisen tilauksen linkkiä, **Vianmääritys**-banneri ohjaa sinut kohtaan, jossa voit linkittää vuokraajan ja tilauksen. Valitse vianmäärityksen sanoma ja ratkaise tilaukseen liittyvä ongelma ohjeiden avulla.

Seuraavassa kuvassa on esimerkki Azure AD B2C:n **Vianmääritys**-bannerista.

![Varoitus siitä, että hakemistolla ei ole aktiivista tilausta.](./media/B2CImage_5.png)

## <a name="next-steps"></a>Seuraavat vaiheet

Jos haluat jatkaa kuluttajakaupan vuokraajan määrittämisprosessia Commercessa, jatka [Kuluttajakaupan sovelluksen luominen](create-b2c-app.md) -kohtaan.

## <a name="additional-resources"></a>Lisäresurssit

[B2C-vuokraajan määrittäminen Commercessa](set-up-b2c-tenant.md)

[B2C-sovelluksen luominen](create-b2c-app.md)

[Käyttäjän työnkulkukäytäntöjen luominen](create-user-flow-policies.md)

[Yhteisöpalvelun tunnistetietojen tarjoajien lisääminen (valinnainen)](add-social-identity-providers.md)

[Commerce headquartersin päivittäminen uusilla Azure AD:n kuluttajakaupan tiedoilla](update-hq-aad-b2c-info.md)

[B2C-vuokraajan määrittäminen Commerce-sivuston luontiohjelmassa](config-b2c-tenant-site-builder.md)

[B2C-lisätiedot](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
