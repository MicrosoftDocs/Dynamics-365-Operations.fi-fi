---
title: Mukautettujen sivujen määrittäminen käyttäjän sisäänkirjautumisia varten
description: Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 Commercessa luodaan mukautettuja sivuja, jotka käsittelevät Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajien mukautettuja sisäänkirjauksia.
author: brianshook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 210a7d1c2b0a9a9606723b48681cca3a50fcc05b
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096794"
---
# <a name="set-up-custom-pages-for-user-logins"></a>Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 Commercessa luodaan mukautettuja sivuja, jotka käsittelevät Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajien mukautettuja sisäänkirjauksia.

## <a name="overview"></a>Yleiskatsaus

Jotta Dynamics 365 Commercessa tehdyt mukautetut sivut voivat käyttää käyttäjän sisäänkirjausten työnkulkuja, Commerce-ympäristössä viitattavat Azure AD -käytännöt on määritettävä. Voit määrittää Azure AD:n kuluttajakaupan Rekisteröinti ja sisäänkirjaus-, Profiilin muokkaus- ja Sanasanan nollaus -käytännöt käyttämällä Azure AD:n kuluttajakaupan sovellusta. Azure AD:n kuluttajakaupan vuokraajan ja käytännön nimiin ei voi viitata valmisteluprosessin aikana, kun se tehdään Commerce-ympäristössä Microsoft Dynamics Lifecycle Services (LCS) -palvelun avulla.

Mukautetut Commerce-sivut voidaan luoda käyttämällä sisäänkirjauksen, rekisteröinnin, tiliprofiilin muokkauksen tai salasanan nollauksen moduulia. Näille mukautetuille sivuille julkaistaviin sivun URL-osoitteisiin on tämän jälkeen viitattava Azure AD:n kuluttajakaupan käytännön määrityksissä Azure-portaalissa.

## <a name="set-up-b2c-policies"></a>Kuluttajakaupan käytäntöjen määrittäminen

Kun olet määrittänyt Azure AD:n kuluttajakaupan vuokraajan ja liittänyt sen Commerce-ympäristöön, siirry **Azure AD:n kuluttajakauppa** -sivulla Azure-portaalissa ja valitse sitten **Käytännöt**-kohdassa **Käyttäjän työnkulut (käytännöt)**.

![Käyttäjän työnkulut (käytännöt) -komento valikossa](./media/B2C_CustomPage_PoliciesMenu.png)

Nyt voit määrittää käyttäjän Rekisteröinti ja sisäänkirjaus-, Profiilin muokkaus ja Salasanan nollaus -työnkulut.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Rekisteröinti ja sisäänkirjaus -käytännön määrittäminen

Voit määrittää Rekisteröinti ja sisäänkirjaus -käytännön seuraavasti.

1. Valitse **Uusi käyttäjän työnkulku** ja valitse sitten **Suositellut**-välilehdessä **Rekisteröinti ja sisäänkirjaus** -käytäntö.
1. Syötä käytännön nimi (esimerkiksi **B2C\_1\_SignInSignUp**).
1. Valitse **Tunnistetietojen toimittajat** -osassa käytännön kanssa käytettävät tunnistetietojen toimittajat. Vähintään **Sähköpostirekisteröityminen** on valittava.
1. Valitse **Kerää määrite** -sarakkeessa **Sähköpostiosoite**-, **Etunimi**- ja **Sukunimi**-valintaruudut.
1. Valitse **Palauta vaatimus** -sarakkeessa **Sähköpostiosoitteet**-, **Etunimi**-, **Tunnistetietojen tarjoaja**-, **Sukunimi**- ja **Käyttäjän objektin tunnus** -valintaruudut.

    ![Valitut määritteet ja vaatimukset](./media/B2C_SignInSignUp_Attributes.png)

1. Valitse **OK**, kun haluat luoda käytännön.
1. Kaksoisnapsauta uuden käytännön nimeä ja valitse siirtymisruudussa **Ominaisuudet**.
1. Määritä **Ota JavaScriptia käyttävä sivun asettelu käyttöön (esikatselu)** -asetuksen arvoksi **Käytössä**.

    ![Uuden käytännön Ominaisuudet-sivu](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> Käytännön nimeen viitataan täysin Commerce-ympäristössä. (**B2C\_1\_**-etuliite sisällytetään viitteeseen.) Käytäntöjä ei voi nimetä uudelleen luomisen jälkeen. Jos korvaat Commerce-ympäristön olemassa olevan käytännön, voit poistaa alkuperäisen käytännön ja luoda uuden käytännön, jolla on sama nimi. Vaihtoehtoisesti, jos ympäristö on jo valmisteltu, voit lähettää uuden käytännön nimen palvelupyynnön kautta.

Palaa tähän käytäntöön ja tee määritykset loppuun, kun mukautetut sivut on luotu. Nyt voit sulkea käytännön ja palata **Käyttäjän työnkulut (käytännöt)** -sivulle Azure-portaalissa.

### <a name="configure-the-profile-editing-policy"></a>Profiilin muokkaus -käytännön määrittäminen

Voit määrittää Profiilin muokkaus -käytännön seuraavasti.

1. Valitse **Uusi käyttäjän työnkulku** ja valitse sitten **Suositellut**-välilehdessä **Profiilin muokkaus** -käytäntö.
1. Syötä käytännön nimi (esimerkiksi **B2C\_1\_EditProfile**).
1. Valitse **Tunnistetietojen toimittajat** -osassa käytännön kanssa käytettävät tunnistetietojen toimittajat. Vähintään **Paikallisen tilin sisäänkirjaus** on valittava.
1. Valitse **Kerää määrite** -sarakkeessa **Sähköpostiosoitteet**- ja **Sukunimi**-valintaruudut.
1. Valitse **Palauta vaatimus** -sarakkeessa **Sähköpostiosoitteet**-, **Etunimi**-, **Tunnistetietojen tarjoaja**-, **Sukunimi**- ja **Käyttäjän objektin tunnus** -valintaruudut.
1. Valitse **OK**, kun haluat luoda käytännön.
1. Kaksoisnapsauta uuden käytännön nimeä ja valitse siirtymisruudussa **Ominaisuudet**.
1. Määritä **Ota JavaScriptia käyttävä sivun asettelu käyttöön (esikatselu)** -asetuksen arvoksi **Käytössä**.

Palaa tähän käytäntöön ja tee määritykset loppuun, kun mukautetut sivut on luotu. Nyt voit sulkea käytännön ja palata **Käyttäjän työnkulut (käytännöt)** -sivulle Azure-portaalissa.

### <a name="configure-the-password-reset-policy"></a>Salasanan nollaus -käytännön määrittäminen

Voit määrittää Salasanan nollaus -käytännön seuraavasti.

1. Valitse **Uusi käyttäjän työnkulku** ja valitse sitten **Esikatselu**-välilehdessä **Salasanan nollaus versio 1.1** -käytäntö.

    ![Salasanan nollaus versio 1.1 -käytäntö valittuna Esikatselu-välilehdessä](./media/B2C_ForgetPassword_Menu.png)

1. Syötä käytännön nimi (esimerkiksi **B2C\_1\_ForgetPassword**).
1. Valitse **Tunnistetietojen tarjoajat** -osassa **Nollaa salasana sähköpostiosoitteen avulla**.
1. Valitse **Palauta vaatimus** -sarakkeessa **Sähköpostiosoitteet**-, **Etunimi**, **Sukunimi**- ja **Käyttäjän objektin tunnus** valintaruudut.

    ![Valitut vaatimukset](./media/B2C_ForgetPassword_Attributes.png)

1. Valitse **OK**, kun haluat luoda käytännön.
1. Kaksoisnapsauta uuden käytännön nimeä ja valitse siirtymisruudussa **Ominaisuudet**.
1. Määritä **Ota JavaScriptia käyttävä sivun asettelu käyttöön (esikatselu)** -asetuksen arvoksi **Käytössä**.

Palaa tähän käytäntöön ja tee määritykset loppuun, kun mukautetut sivut on luotu. Nyt voit sulkea käytännön ja palata **Käyttäjän työnkulut (käytännöt)** -sivulle Azure-portaalissa.

## <a name="build-the-custom-pages"></a>Mukautettujen sivujen luominen

Voit luoda mukautettuja sivuja käyttäjän sisäänkirjausten käsittelemistä varten seuraavasti.

1. Siirry Commerce-muokkaustyökalut-kohdassa sivustoon.
1. Muodosta seuraavat viisi mallia ja sivua:

    - **Sisäänkirjaus**-malli ja -sivu, jotka käyttävät sisäänkirjauksen moduulia.
    - **Rekisteröinti**-malli ja -sivu, jotka käyttävät rekisteröinnin moduulia.
    - **Salasanan nollaus** -malli ja -sivu, jotka käyttävät salasanan nollauksen moduulia.
    - **Salasanan nollauksen vahvistus** -malli ja -sivu, jotka käyttävät salasanan nollauksen vahvistuksen moduulia.
    - **Profiilin muokkaus** -malli ja -sivu, jotka käyttävät tiliprofiilin muokkauksen moduulia

Kun luot sivuja, noudata seuraavia ohjeita:

- Käytä kunkin sivun tai moduulin kohdalla asettelua ja tyyliä, joka sopii parhaiten liiketoiminnan vaatimuksiin.
- Julkaise kaikki sivut ja URL-osoitteet, joita on käytettävä Azure AD:n kuluttajakaupan määrityksessä.
- Kun sivut ja URL-osoitteet on julkaistu, kerää Azure AD:n kuluttajakaupan käytännön määrityksessä käytettävät URL-osoitteet. Jälkiliite **?preloadscripts=true** lisätään jokaiseen URL-osoitteeseen käytön yhteydessä.

> [!IMPORTANT]
> Älä käytä universaaleja ylä- ja alatunnisteita, joissa on suhteellisia linkkejä. Koska Azure AD:n kuluttajakaupan toimialue isännöi näitä sivuja käytön yhteydessä, kaikissa linkeissä tulisi käyttää vain absoluuttisia URL-osoitteita.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Azure AD:n kuluttajakaupan käytäntöjen ja mukautetun sivun tietojen määrittäminen 

Palaa Azure-portaalissa **Azure AD:n kuluttajakauppa** -sivulla ja valitse **Käytännöt**-kohdassa valikosta **Käyttäjän työnkulut (käytännöt)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>Rekisteröidy ja kirjaudu -käytännön päivittäminen mukautetun sivun tiedoilla

Voit päivittää Rekisteröinti ja sisäänkirjaus -käytännön mukautetun sivun tiedoilla seuraavasti.

1. Valitse aiemmin määritetyn **Rekisteröinti ja sisäänkirjaus** -käytännön siirtymisruudussa **Sivun asettelut**.
1. Valitse **Yhtenäinen rekisteröinti tai sisäänkirjaus -sivu** -asettelu
1. Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.
1. Syötä **Mukautetun sivun URI** -kenttään sisäänkirjauksen täydellinen URL-osoite. Sisällytä jälkiliite **?preloadscripts=true**. Syötä arvoksi esimerkiksi ``www.<my domain>.com/sign-in?preloadscripts=true``.
1. Valitse **Sivun asettelun versio (esikatselu)** -kentässä **1.2.0**.
1. Valitse **Paikallisen tilin rekisteröinti -sivu** -asettelu.
1. Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.
1. Syötä **Mukautetun sivun URI** -kenttään rekisteröitymisen täydellinen URL-osoite. Sisällytä jälkiliite **?preloadscripts=true**. Syötä arvoksi esimerkiksi ``www.<my domain>.com/sign-up?preloadscripts=true``.
1. Valitse **Sivun asettelun versio (esikatselu)** -kentässä **1.2.0**.
1. Tee seuraavat toiminnot **Käyttäjän määritteet** -osassa:

    1. Valitse **Sähköpostiosoite**-, **Etunimi**- ja **Sukunimi**-määritteille **Ei**-arvo **Vaatii tarkistuksen** -kentässä.
    1. Valitse **Etunimi**- ja **Sukunimi**-määritteille **Ei**-arvo **Valinnainen**-kentässä.

    ![Paikallisen tilin rekisteröinti -sivun käytännön määrittäminen](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>Profiilin muokkaus -käytännön päivittäminen mukautetun sivun tiedoilla

Voit päivittää Profiilin muokkaus -käytännön mukautetun sivun tiedoilla seuraavasti.

1. Valitse aiemmin määritetyn **Profiilin muokkaus** -käytännön siirtymisruudussa **Sivun asettelut**.
1. Valitse **Profiilin muokkaus -sivu** -asettelu.
1. Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.
1. Syötä **Mukautetun sivun URI** -kenttään profiilin muokkaussivun täydellinen URL-osoite. Sisällytä jälkiliite **?preloadscripts=true**. Syötä arvoksi esimerkiksi ``www.<my domain>.com/profile-edit?preloadscripts=true``.
1. Valitse **Sivun asettelun versio (esikatselu)** -kentässä **1.2.0**.
1. Tee seuraavat toiminnot **Käyttäjän määritteet** -osassa:

    1. Valitse **Sähköpostiosoite**- ja **Etunimi**-määritteille **Ei**-arvo **Vaatii tarkistuksen** -kentässä.
    1. Valitse **Etunimi**- ja **Sukunimi**-määritteille **Ei**-arvo **Valinnainen**-kentässä.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>Salasanan nollaus -käytännön päivittäminen mukautetun sivun tiedoilla

Voit päivittää Salasanan nollaus -käytännön mukautetun sivun tiedoilla seuraavasti.

1. Valitse aiemmin määritetyn **Salasanan nollaus** -käytännön siirtymisruudussa **Sivun asettelut**.
1. Valitse **Uusi salasana -sivu** -asettelu.
1. Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.
1. Syötä **Mukautetun sivun URI** -kenttään salasanan palauttamisen täydellinen URL-osoite. Sisällytä jälkiliite **?preloadscripts=true**. Syötä arvoksi esimerkiksi ``www.<my domain>.com/passwordreset?preloadscripts=true``.
1. Valitse **Sivun asettelun versio (esikatselu)** -kentässä **1.2.0**.
1. Valitse **Tilin tarkistus -sivu** -asettelu.
1. Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.
1. Syötä **Mukautetun sivun URI** -kenttään salasanan palauttamisen todentamisen URL-osoite. Sisällytä jälkiliite **?preloadscripts=true**. Syötä arvoksi esimerkiksi ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.
1. Valitse **Sivun asettelun versio (esikatselu)** -kentässä **1.2.0**.



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Otsikoiden ja kuvausten oletustekstimerkkijonojen mukauttaminen

Aloituspakkauksen sisäänkirjausmoduulit täytetään etukäteen otsikoiden ja kuvausten oletustekstimerkkijonoilla. Voit mukauttaa nämä SDK:n merkkijonot päivittämällä sisäänkirjausmoduulin global.json-tiedoston arvot.

Esimerkiksi unohtuneen salasanan oletusteksti on **Unohtuiko salasana?** Alla näkyy sisäänkirjaussivun oletusteksti.

![Sisäänkirjaussivun oletusteksti unohtunutta salasanaan varten](./media/B2C_SignUp_ModuleFace.png)

Voit muokata moduulin aloituspakkauksen global.json-tiedostossa **Unohtuiko salasana?** -kohdan tekstiä seuraavasti.

![Sisäänkirjauksen päivitetty linkkiteksti moduulin global.json-tiedostossa](./media/B2C_CustomizingStringsForModule.png)

Kun olet päivittänyt global.json-tiedoston ja julkaissut muutokset, uusi linkkiteksti näkyy sisäänkirjausmoduulissa sekä Commercessa että julkaistulla sisäänkirjaussivulla.

## <a name="additional-resources"></a>Lisäresurssit

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Uuden sähköisen kaupankäynnin sivuston käyttöönotto](deploy-ecommerce-site.md)

[Määritä verkkokauppakanava](online-stores.md)

[Sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md)

[Liitä verkkosivusto kanavaan](associate-site-online-store.md)

[Robots.txt-tiedostojen hallinta](manage-robots-txt-files.md)

[URL-osoitteen uudelleenohjausten lataaminen joukkona](upload-bulk-redirects.md)

[B2C-vuokraajan määrittäminen Commercessa](set-up-B2C-tenant.md)

[Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä](configure-multi-B2C-tenants.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)
