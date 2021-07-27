---
title: Mukautettujen sivujen määrittäminen käyttäjän sisäänkirjautumisia varten
description: Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 Commercessa luodaan mukautettuja sivuja, jotka käsittelevät Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajien mukautettuja sisäänkirjauksia.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 214f99563f8bb08d8c051f904d0ca0a88267aa6b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349647"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Mukautettujen sivujen määrittäminen käyttäjän sisäänkirjautumisia varten

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 Commercessa luodaan mukautettuja sivuja, jotka käsittelevät Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajien mukautettuja sisäänkirjauksia.

Jotta Dynamics 365 Commercessa tehdyt mukautetut sivut voivat käyttää käyttäjän sisäänkirjausten työnkulkuja, Commerce-ympäristössä viitattavat Azure AD -käytännöt on määritettävä. Voit määrittää Azure AD:n kuluttajakaupan Rekisteröinti ja sisäänkirjaus-, Profiilin muokkaus- ja Sanasanan nollaus -käytännöt käyttämällä Azure AD:n kuluttajakaupan sovellusta. Azure AD:n kuluttajakaupan vuokraajan ja käytännön nimiin ei voi viitata valmisteluprosessin aikana, kun se tehdään Commerce-ympäristössä Microsoft Dynamics Lifecycle Services (LCS) -palvelun avulla.

Mukautetut Commerce-sivut voidaan luoda käyttämällä sisäänkirjauksen, rekisteröinnin, tiliprofiilin muokkauksen tai salasanan nollauksen moduulia tai yleistä AAD-moduulia. Näille mukautetuille sivuille julkaistaviin sivun URL-osoitteisiin on tämän jälkeen viitattava Azure AD:n kuluttajakaupan käytännön määrityksissä Azure-portaalissa.

> [!WARNING] 
> Azure AD B2C poistaa vanhat käyttäjätyönkulut käytöstä 1.8.2021 mennessä. Näin ollen on hyvä suunnitella käyttäjätyönkulkujen siirtämistä uuteen suositeltuun versioon. Uudessa versiossa on ominaisuuksien pariteetti ja uusia ominaisuuksia. Lisätietoja on kohdassa [Työnkulut Azure Active Directory B2C:ssä](/azure/active-directory-b2c/user-flow-overview).

>Commerce-version 10.0.15 tai sitä uudemman version moduulikirjastoa tulee käyttää suositeltujen B2C-käyttäjätyönkulkujen kanssa. Myös Azure AD B2C:ssä tarjottua oletuskäyttäjäkäytäntösivuja voidaan käyttää ja niiden avulla voidaan lisätä taustakuvia, logoja ja taustavärin muutoksia, jotka liittyvät yrityksen brändiin. Vaikka suunnitteluominaisuudet ovat rajoitetumpia, käyttäjien oletuskäytäntösivut tarjoavat Azure AD B2C -käytäntötoiminnallisuuden luomatta ja konfiguroimatta erillisiä mukautettuja sivuja. 

## <a name="set-up-b2c-policies"></a>Kuluttajakaupan käytäntöjen määrittäminen

Kun olet määrittänyt Azure AD:n kuluttajakaupan vuokraajan ja liittänyt sen Commerce-ympäristöön, siirry **Azure AD:n kuluttajakauppa** -sivulla Azure-portaalissa ja valitse sitten **Käytännöt**-kohdassa **Käyttäjän työnkulut (käytännöt)**.

![Käyttäjän työnkulut (käytännöt) -komento valikossa.](./media/B2C_CustomPage_PoliciesMenu.png)

Nyt voit määrittää käyttäjän Rekisteröinti ja sisäänkirjaus-, Profiilin muokkaus ja Salasanan nollaus -työnkulut.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Rekisteröinti ja sisäänkirjaus -käytännön määrittäminen

Voit määrittää Rekisteröinti ja sisäänkirjaus -käytännön seuraavasti.

1. Valitse **Uusi käyttäjän työnkulku**, **Rekisteröinti ja sisäänkirjaus**, **Suositellut**-välilehti ja sitten **Luo**.
1. Syötä käytännön nimi (esimerkiksi **B2C\_1\_SignInSignUp**).
1. Valitse **Tunnistetietojen toimittajat** -osassa käytännön kanssa käytettävät tunnistetietojen toimittajat. Vähintään **Sähköpostirekisteröityminen** on valittava.
1. Valitse **Kerää määrite** -sarakkeessa **Sähköpostiosoite**-, **Etunimi**- ja **Sukunimi**-valintaruudut.
1. Valitse **Palauta vaatimus** -sarakkeessa **Sähköpostiosoitteet**-, **Etunimi**-, **Tunnistetietojen tarjoaja**-, **Sukunimi**- ja **Käyttäjän objektin tunnus** -valintaruudut.

    ![Valitut määritteet ja vaatimukset.](./media/B2C_SignInSignUp_Attributes.png)

1. Valitse **OK**, kun haluat luoda käytännön.
1. Kaksoisnapsauta uuden käytännön nimeä ja valitse siirtymisruudussa **Ominaisuudet**.
1. Määritä **Ota JavaScriptia käyttävä sivun asettelu käyttöön (esikatselu)** -asetuksen arvoksi **Käytössä**.

    ![Uuden käytännön Ominaisuudet-sivu.](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> Käytännön nimeen viitataan täysin Commerce-ympäristössä. (**B2C\_1\_**-etuliite sisällytetään viitteeseen.) Käytäntöjä ei voi nimetä uudelleen luomisen jälkeen. Jos korvaat Commerce-ympäristön olemassa olevan käytännön, voit poistaa alkuperäisen käytännön ja luoda uuden käytännön, jolla on sama nimi. Vaihtoehtoisesti, jos ympäristö on jo valmisteltu, voit lähettää uuden käytännön nimen palvelupyynnön kautta.

Palaa tähän käytäntöön ja tee määritykset loppuun, kun mukautetut sivut on luotu. Nyt voit sulkea käytännön ja palata **Käyttäjän työnkulut (käytännöt)** -sivulle Azure-portaalissa.

### <a name="configure-the-profile-editing-policy"></a>Profiilin muokkaus -käytännön määrittäminen

Voit määrittää Profiilin muokkaus -käytännön seuraavasti.

1. Valitse **Uusi käyttäjän työnkulku**, **Profiilin muokkaus**, **Suositellut**-välilehti ja sitten **Luo**.
1. Syötä käytännön nimi (esimerkiksi **B2C\_1\_EditProfile**).
1. Valitse **Tunnistetietojen toimittajat** -osassa käytännön kanssa käytettävät tunnistetietojen toimittajat. Vähintään **Paikallisen tilin sisäänkirjaus** on valittava.
1. Valitse **Kerää määrite** -sarakkeessa **Etunimi**- ja **Sukunimi**-valintaruudut.
1. Valitse **Palauta vaatimus** -sarakkeessa **Sähköpostiosoitteet**-, **Etunimi**-, **Tunnistetietojen tarjoaja**-, **Sukunimi**- ja **Käyttäjän objektin tunnus** -valintaruudut.
1. Valitse **OK**, kun haluat luoda käytännön.
1. Kaksoisnapsauta uuden käytännön nimeä ja valitse siirtymisruudussa **Ominaisuudet**.
1. Määritä **Ota JavaScriptia käyttävä sivun asettelu käyttöön (esikatselu)** -asetuksen arvoksi **Käytössä**.

Palaa tähän käytäntöön ja tee määritykset loppuun, kun mukautetut sivut on luotu. Nyt voit sulkea käytännön ja palata **Käyttäjän työnkulut (käytännöt)** -sivulle Azure-portaalissa.

### <a name="configure-the-password-reset-policy"></a>Salasanan nollaus -käytännön määrittäminen

Voit määrittää Salasanan nollaus -käytännön seuraavasti.

1. Valitse **Uusi käyttäjän työnkulku**, **Salasanan nollaus**-asetus, **Suositellut**-välilehti ja sitten **Luo**.
1. Syötä käytännön nimi (esimerkiksi **B2C\_1\_ForgetPassword**).
1. Valitse **Tunnistetietojen tarjoajat** -osassa **Nollaa salasana sähköpostiosoitteen avulla**.
1. Valitse **Palauta vaatimus** -sarakkeessa **Sähköpostiosoitteet**-, **Etunimi**, **Sukunimi**- ja **Käyttäjän objektin tunnus** valintaruudut.
1. Valitse **OK**, kun haluat luoda käytännön.
1. Kaksoisnapsauta uuden käytännön nimeä ja valitse siirtymisruudussa **Ominaisuudet**.
1. Määritä **Ota JavaScriptia käyttävä sivun asettelu käyttöön (esikatselu)** -asetuksen arvoksi **Käytössä**.

Palaa tähän käytäntöön ja tee määritykset loppuun, kun mukautetut sivut on luotu. Nyt voit sulkea käytännön ja palata **Käyttäjän työnkulut (käytännöt)** -sivulle Azure-portaalissa.

## <a name="build-the-custom-pages"></a>Mukautettujen sivujen luominen

Commerce sisältää eriliset Azure AD -moduulit, joilla voi luoda mukautettuja sivuja Azure AD B2C -käyttäjäkäytäntöjä varten. Kunkin käyttäjäkäytäntösivun asettelun voi luoda erikseen käyttäen alla esiteltyjä Azure AD B2C -päämoduuleita. Vaihtoehtoisesti **AAD – yleinen** -moduulia voidaan käyttää kaikissa Azure AD B2C:n sivuasetteluissa ja käytännöistä (myös sivuasetteluille, jotka eivät kuulu alla lueteltuihin käytäntöihin). 

- Sivukohtaiset Azure AD -moduulit ovat sidottuja Azure AD B2C:n muodostamiiin tietosyötekohteisiin. Näiden moduulien avulla voit hallita paremmin elementtien sijoittelua sivuilla. Jäljempänä kuvattuja oletusasetuksia tarkempia muunnoksia varten on kuitenkin ehkä rakennettava useita sivuja ja moduulilaajennuksia.
- **AAD – yleinen** -moduuli luo div-elementin Azure AD B2C:lle, jotta kaikki käyttäjäkäytäntösivun asettelun elementit voidaan hahmontaa. Tämä tuo joustavuutta sivun B2C-funktioille, mutta vähentää sijoittelun ja tyylin hallintaa (vaikka CSS:ää voidaan kuitenkin käyttää sivuston ulkoasun mukaan).

Voit luoda yhden sivun **AAD – yleinen** -moduulissa ja käyttää sitä kaikissa käyttäjäkäytäntösivuissa, tai voit Azure AD -moduulien avulla luoda yksittäisiä sivuja kirjautumista, rekisteröitymistä, profiilin muokkausta, salasanan palautusta ja salasanan palauttamisen varmistusta varten. Voit käyttää myös molempia käyttämällä alla kuvatun sivuasettelun tiettyjä Azure AD -sivuja ja yleistä AAD-moduulisivua lopuille sivuasetteluille tai muille käyttäjäkäytäntösivuille.

Lisätietoja moduulikirjaston mukana toimitetuista Azure AD -moduuleista: [Käyttäjätietojen hallintasivut ja -moduulit](identity-mgmt-modules.md).

Voit luoda mukautettuja sivuja, joissa on tietyt käyttäjätietomoduulit, käyttäjän sisäänkirjausten käsittelemistä varten seuraavasti.

1. Siirry sivustollesi Commerce-sivuston luontiohjelmassa.
1. Luo seuraavat viisi mallia ja sivua (jos ne eivät vielä ole sivustossasi):
    - **Sisäänkirjaus**-malli ja -sivu, jotka käyttävät sisäänkirjauksen moduulia.
    - **Rekisteröinti**-malli ja -sivu, jotka käyttävät rekisteröinnin moduulia.
    - **Salasanan nollaus** -malli ja -sivu, jotka käyttävät salasanan nollauksen moduulia.
    - **Salasanan nollauksen vahvistus** -malli ja -sivu, jotka käyttävät salasanan nollauksen vahvistuksen moduulia.
    - **Profiilin muokkaus** -malli ja -sivu, jotka käyttävät tiliprofiilin muokkauksen moduulia.

Kun luot sivuja, noudata seuraavia ohjeita:

- Käytä kunkin sivun tai moduulin kohdalla asettelua ja tyyliä, joka sopii parhaiten liiketoiminnan vaatimuksiin.
- Julkaise kaikki sivut ja URL-osoitteet, joita on käytettävä Azure AD:n kuluttajakaupan määrityksessä.
- Kun sivut ja URL-osoitteet on julkaistu, kerää Azure AD:n kuluttajakaupan käytännön määrityksessä käytettävät URL-osoitteet. Jälkiliite **?preloadscripts=true** lisätään jokaiseen URL-osoitteeseen käytön yhteydessä.

> [!IMPORTANT]
> Azure AD B2C:ssä viitatut sivut tuotetaan suoraan Azure AD B2C -vuokraajan toimialueesta. Älä käytä universaaleja ylä- ja alatunnisteita, joissa on suhteellisia linkkejä. Koska Azure AD:n kuluttajakaupan toimialue isännöi näitä sivuja käytön yhteydessä, kaikissa linkeissä tulisi käyttää vain absoluuttisia URL-osoitteita. On suositeltavaa luoda tietty ylä- ja alatunniste, joka sisältää absoluuttiset URL-osoitteet Azure AD:hen liittyville mukautetuille sivuille, ja joista on poistettu kaikki Commerce-kohtaiset moduulit, jotka edellyttävät yhteyttä Retail Serveriin. Esimerkiksi suosikki-, hakupalkki-, kirjautumislinkki- ja ostoskorimoduuleita ei saa sisällyttää mihinkään sivuun, jota käytetään Azure AD B2C -käyttäjätyönkuluissa.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Azure AD:n kuluttajakaupan käytäntöjen ja mukautetun sivun tietojen määrittäminen 

Palaa Azure-portaalissa **Azure AD:n kuluttajakauppa** -sivulla ja valitse **Käytännöt**-kohdassa valikosta **Käyttäjän työnkulut (käytännöt)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>Rekisteröidy ja kirjaudu -käytännön päivittäminen mukautetun sivun tiedoilla

Voit päivittää Rekisteröinti ja sisäänkirjaus -käytännön mukautetun sivun tiedoilla seuraavasti.

1. Valitse aiemmin määritetyn **Rekisteröinti ja sisäänkirjaus** -käytännön siirtymisruudussa **Sivun asettelut**.
1. Valitse **Yhtenäinen rekisteröinti tai sisäänkirjaus -sivu** -asettelu
1. Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.
1. Syötä **Mukautetun sivun URI** -kenttään sisäänkirjauksen täydellinen URL-osoite. Sisällytä jälkiliite **?preloadscripts=true**. Syötä arvoksi esimerkiksi ``www.<my domain>.com/sign-in?preloadscripts=true``.
1. Valitse **Sivun asetteluversio** -kentässä versio **2.1.0** tai myöhempi versio (vaatii Commerce-version 10.0.15 moduulikirjaston tai sitä uudemman).
1. Valitse **Tallenna**.
1. Valitse **Paikallisen tilin rekisteröinti -sivu** -asettelu.
1. Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.
1. Syötä **Mukautetun sivun URI** -kenttään rekisteröitymisen täydellinen URL-osoite. Sisällytä jälkiliite **?preloadscripts=true**. Syötä arvoksi esimerkiksi ``www.<my domain>.com/sign-up?preloadscripts=true``.
1. Valitse **Sivun asetteluversio** -kentässä versio **2.1.0** tai myöhempi versio (vaatii Commerce-version 10.0.15 moduulikirjaston tai sitä uudemman).
1. Tee seuraavat toiminnot **Käyttäjän määritteet** -osassa:
    1. Valitse **Etunimi**- ja **Sukunimi**-määritteille **Ei**-arvo **Vaatii tarkistuksen** -sarakkeessa.
    1. **Sähköpostiosoite**-määritteelle on suositeltavaa jättää oletusarvo **Kyllä** valituksi **Vaatii tarkistuksen** -sarakkeeseen. Tämä asetus varmistaa, että käyttäjät, jotka rekisteröityvät tietyllä sähköpostiosoitteella, vahvistavat sähköpostiosoitteen omistamisen.
    1. Valitse **Sähköpostiosoite**-, **Etunimi**- ja **Sukunimi**-määritteille **Ei**-arvo **Valinnainen**-sarakkeessa.
1. Valitse **Tallenna**.

    ![Paikallisen tilin rekisteröinti -sivun käytännön määrittäminen.](./media/B2C_SignInSignUp_Recommended_PageLayoutExample.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>Profiilin muokkaus -käytännön päivittäminen mukautetun sivun tiedoilla

Voit päivittää Profiilin muokkaus -käytännön mukautetun sivun tiedoilla seuraavasti.

1. Valitse aiemmin määritetyn **Profiilin muokkaus** -käytännön siirtymisruudussa **Sivun asettelut**.
1. Valitse **profiilin muokkaussivun** asettelu (saattaa edellyttää, että siirryt näytössä alaspäin muiden asetteluvaihtoehtojen ohi).
1. Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.
1. Syötä **Mukautetun sivun URI** -kenttään profiilin muokkaussivun täydellinen URL-osoite. Sisällytä jälkiliite **?preloadscripts=true**. Syötä arvoksi esimerkiksi ``www.<my domain>.com/profile-edit?preloadscripts=true``.
1. Valitse **Sivun asetteluversio** -kohdassa versio **2.1.0** tai uudempi versio (vaatii Commerce-version 10.0.15 moduulikirjaston tai sitä uudemman).
1. Tee seuraavat toiminnot **Käyttäjän määritteet** -osassa:
    1. Valitse **Etunimi**- ja **Sukunimi**-määritteille **Ei**-arvo **Valinnainen**-sarakkeessa.
    1. Valitse **Etunimi**- ja **Sukunimi**-määritteille **Ei**-arvo **Vaatii tarkistuksen** -sarakkeessa.
1. Valitse **Tallenna**.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>Salasanan nollaus -käytännön päivittäminen mukautetun sivun tiedoilla

Voit päivittää Salasanan nollaus -käytännön mukautetun sivun tiedoilla seuraavasti.

1. Valitse aiemmin määritetyn **Salasanan nollaus** -käytännön siirtymisruudussa **Sivun asettelut**.
1. Valitse **Salasana unohtui -sivu** -asettelu.
1. Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.
1. Syötä **Mukautetun sivun URI** -kenttään salasanan palauttamisen todentamisen URL-osoite. Sisällytä jälkiliite **?preloadscripts=true**. Syötä arvoksi esimerkiksi ``www.<my domain>.com/password-reset-verification?preloadscripts=true``.
1. Valitse **Sivun asetteluversio** -kentässä versio **2.1.0** tai uudempi versio (vaatii Commerce-version 10.0.15 moduulikirjaston tai sitä uudemman).
2. Valitse **Tallenna**.
3. Valitse **Vaihda salasana -sivu** -asettelu.
4. Määritä **Käytä mukautettua sivun sisältöä** -asetukseksi **Kyllä**.
5. Syötä **Mukautetun sivun URI** -kenttään salasanan palauttamisen täydellinen URL-osoite. Sisällytä jälkiliite **?preloadscripts=true**. Syötä arvoksi esimerkiksi ``www.<my domain>.com/password-reset?preloadscripts=true``.
6. Valitse **Sivun asetteluversio** -kentässä versio **2.1.0** tai uudempi versio (vaatii Commerce-version 10.0.15 moduulikirjaston tai sitä uudemman).
7. Valitse **Tallenna**.

## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Otsikoiden ja kuvausten oletustekstimerkkijonojen mukauttaminen

Moduulikirjastossa sisäänkirjausmoduulit täytetään etukäteen otsikoiden ja kuvausten oletustekstimerkkijonoilla. Voit mukauttaa merkkijonoja käsitellyn moduulin ominaisuusruudussa. Sivun lisämerkkijonot (esimerkiksi **Unohditko salasanan?** -linkkiteksti tai **Luo tili** -toimintokehotteen teksti) edellyttävät Commerce-ohjelmistokehityspaketin (SDK) käyttöä ja kirjautumismoduulin global.json-tiedoston arvojen päivittämistä.

Esimerkiksi unohtuneen salasanan oletusteksti on **Unohtuiko salasana?** Alla näkyy sisäänkirjaussivun oletusteksti.

![Unohtuneen salasanan oletusteksti kirjautumissivulla.](./media/B2C_SignUp_ModuleFace.png)

Voit kuitenkin muokata moduulikirjaston kirjautumismoduulin global.json-tiedoston tekstin muotoon **Unohtuiko salasanasi?**, kuten seuraavassa kuvassa näkyy.

![Linkin päivitetty teksti sisäänkirjautumismoduulin global.json-tiedostossa.](./media/B2C_CustomizingStringsForModule.png)

Kun olet päivittänyt global.json-tiedoston ja julkaissut muutokset, uusi linkkiteksti näkyy sisäänkirjausmoduulissa sekä Commercessa että julkaistulla sisäänkirjaussivulla.

## <a name="additional-resources"></a>Lisäresurssit

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto](deploy-ecommerce-site.md)

[Sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md)

[Dynamics 365 Commerce -sivuston liittäminen online-kanavaan](associate-site-online-store.md)

[Robots.txt-tiedostojen hallinta](manage-robots-txt-files.md)

[URL-uudelleenohjausten joukkolataus palveluun](upload-bulk-redirects.md)

[B2C-vuokraajan määrittäminen Commercessa](set-up-B2C-tenant.md)

[Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä](configure-multi-B2C-tenants.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]