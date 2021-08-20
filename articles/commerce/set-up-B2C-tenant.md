---
title: B2C-vuokraajan määrittäminen Commercessa
description: Tässä ohjeaiheessa kerrotaan, miten Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajat määritetään Dynamics 365 Commercen käyttäjän sivuston todennusta varten.
author: BrianShook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: 13dad5f3b82914514688bfa0c7e4f82b8b85b8dd73458618d2fcfddb169927c9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772249"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>B2C-vuokraajan määrittäminen Commercessa

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajat määritetään Dynamics 365 Commercen käyttäjän sivuston todennusta varten.

Dynamics 365 Commerce käyttää Azure AD B2C -ratkaisua käyttäjän tunnistetietojen ja todennuksen työnkulkujen tukemisessa. Käyttäjä voi rekisteröityä, kirjautua sisään ja nollata salasanan näiden työnkulkujen avulla. Azure AD B2C tallentaa luottamukselliset käyttäjän todennustiedot, kuten käyttäjätunnuksen ja salasanan. B2C-vuokraajan käyttäjätietueeseen tallennetaan B2C:n paikallisen tilin tietue tai B2C:n yhteisöpalvelun tunnuksen tarjoajan tietue. Nämä B2C-tietueet linkitetään takaisin asiakastietueeseen Commerce-ympäristössä.

> [!WARNING] 
> Azure AD B2C poistaa vanhat käyttäjätyönkulut käytöstä 1.8.2021 mennessä. Näin ollen on hyvä suunnitella käyttäjätyönkulkujen siirtämistä uuteen suositeltuun versioon. Uudessa versiossa on ominaisuuksien pariteetti ja uusia ominaisuuksia. Commerce-version 10.0.15 tai sitä uudemman version moduulikirjastoa tulee käyttää suositeltujen B2C-käyttäjätyönkulkujen kanssa. Lisätietoja on kohdassa [Työnkulut Azure Active Directory B2C:ssä](/azure/active-directory-b2c/user-flow-overview).
 
 > [!NOTE]
 > Commerce-arviointiympäristöt tulevat esiladatun Azure AD B2C -vuokraajan kanssa esittelytarkoituksiin. Arviointiympäristöissä ei tarvitse ladata omaa Azure AD B2C -vuokraajaa alla olevia vaiheita käyttäen.

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a>Olemassa olevan AAD B2C -vuokraajan luominen tai linkittäminen Azure-portaalissa

1. Kirjaudu [Azure-portaalin osoitteessa](https://portal.azure.com/).
1. Valitse Azure-portaalin valikossa **Luo resurssi**. Varmista,. että käytät tilausta ja hakemistoa, joka yhdistetään Commerce-ympäristöön.

    ![Resurssin luominen Azure-portaalissa.](./media/B2CImage_1.png)

1. Siirry kohtaan **Tunnistetiedot \> Azure Active Directory B2C**.
1. Käytä **Uuden B2C-vuokraajan luominen tai linkittäminen olemassa olevaan vuokraajaan** -sivulla seuraavista vaihtoehdoista sitä, joka sopii yrityksen tarpeisiin parhaiten:

    - **Luo uusi Azure AD B2C -vuokraaja**: Käytä tätä vaihtoehtoa, jos haluat luoda uuden AAD B2C -vuokraajan.
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

    ![Linkki uuteen AAD-hakemistoon.](./media/B2CImage_4.png)

> [!NOTE]
> Jos sinulla on useita Azure-tilin tilauksia tai jos olet määrittänyt B2C-vuokraajan ilman aktiivisen tilauksen linkkiä, **Vianmääritys**-banneri ohjaa sinut kohtaan, jossa voit linkittää vuokraajan ja tilauksen. Valitse vianmäärityksen sanoma ja ratkaise tilaukseen liittyvä ongelma ohjeiden avulla.

Seuraavassa kuvassa on esimerkki Azure AD B2C:n **Vianmääritys**-bannerista.

![Varoitus siitä, että hakemistolla ei ole aktiivista tilausta.](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a>B2C-sovelluksen luominen

Kun B2C-vuokraaja on luotu, voit luoda B2C-sovelluksen uudessa Azure AD B2C -vuokraajassa ja käyttää Commercea.

Luo B2C-sovellus seuraavasti.

1. Valitse Azure-portaalissa **Sovellusten rekisteröinnit** ja sitten **Uusi rekisteröinti**.
1. Anna tälle Azure AD B2C -sovellukselle nimi **Nimi**-kentässä.
1. Valitse **Tuetut tilityypit** -kohdasta **Tilit mistä tahansa tunnistetietojen tarjoajasta tai organisaatiohakemistosta (käyttäjien tunnistamiseksi käyttäjätyönkulkujen avulla)**.
1. Syötä **Uudelleenohjauksen URI** -kenttään erilliset vastaus-URL-osoitteet **Internet**-tyyppisinä. Katso lisätietoja vastauksen URL-osoitteista ja niiden muotoilusta allal olevasta [Vastauksen URL-osoitteet](#reply-urls) -kohdasta.
1. Jos sinulla on **käyttöoikeudet**, valitse **Myönnä järjestelmänvalvojan hyväksyntä OpenId- ja offline_access-käyttöoikeuksille**.
1. Valitse **Rekisteröi**.
1. Valitse juuri luotu sovellus ja siirry **Todennus**-valikkoon. Voit tarvittaessa lisätä **Uudelleenohjauksen URI** -osoitteita (nyt tai myöhemmin). Jatka seuraavaan vaiheeseen, jos sitä ei tarvita tällä hetkellä.
1. Ota ne käyttöön sovelluksessa valitsemalla **Implisiittinen myöntäminen** -kohdasta sekä **Käyttöoikeustunnukset** että **Tunnukset**. Valitse **Tallenna**.
1. Siirry Azure-portaalin **Yhteenveto**-valikkoon ja kopioi **Sovelluksen (asiakasohjelman) tunnus**. Huomaa, että tämä tunnus tarvitaan myöhemmissä määritysvaiheissa (viitataan myöhemmin nimellä **Asiakasohjelman GUID**).

Lisätietoja sovelluksen rekisteröinneistä Azure AD B2C:ssä on kohdassa [Azure Active Directory B2C:n uusi sovelluksen rekisteröintikokemus](/azure/active-directory-b2c/app-registrations-training-guide)

### <a name="reply-urls"></a>Vastauksen URL-osoitteet

Vastauksen URL-osoitteet ovat tärkeitä, koska ne tarjoavat sallitut palautustoimialueet, kun sivusto kutsuu Azure AD B2C -ratkaisua käyttäjän todentamista varten. Toiminto sallii todennetun käyttäjän paluun takaisin toimialueelle, jolta nämä kirjautuvat (oman sivuston toimialue). 

Lisää **Vastauksen URL-osoite** -ruudun **Azure AD B2C - sovellukset \> Uusi sovellus** -näytössä erilliset rivit sivuston toimialueelle ja (ympäristön valmistelun jälkeen) Commercen luomalle URL-osoitteelle. Näissä URL-osoitteissa on aina käytettävä sallittua URL-osoitteen muotoa. Niiden on aina oltava perus-URL-osoitteita (ei lopussa olevia vinoviivoja tai polkuja). Merkkijono ``/_msdyn365/authresp`` on siis liitettävä perus-URL-osoitteisiin seuraavien esimerkkien mukaisesti.

- ``https://www.fabrikam.com/_msdyn365/authresp`` (Toimialueen tulisi täsmätä sähköisen kaupankäynnin toimialueeseen kokonaan. Jos sinulla on useita toimialueita, sinun on lisättävä tämä URL-osoite kullekin toimialueelle.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a>Käyttäjän työnkulkukäytäntöjen luominen

Käyttäjän työnkulut ovat käytäntöjä, joita Azure AD B2C käyttää suojatun sisäänkirjauksen, rekisteröitymisen, profiilin muokkaamisen ja unohdetun salasanan käyttökokemusten määrittämisessä. Dynamics 365 Commerce suorittaa näiden työnkulkujen avulla käytäntöjen toiminnot, joiden avulla se toimii Azure AD B2C -vuokraajan kanssa. Kun käyttäjä käyttää näitä käytäntöjä, ne ohjataan uudelleen Azure AD B2C -vuokraajalle toimintojen suorittamista varten.

Azure AD B2C sisältää seuraavat kolme käyttäjän perustyönkulkutyyppiä:
- Rekisteröityminen ja sisäänkirjaus
- Profiilin muokkaaminen
- Salasanan palauttaminen

Voit halutessasi käyttää Azure AD:n käyttäjän oletustyönkulkua. Se näyttää AAD B2C:n isännöimän sivun. Vaihtoehtoisesti voit luoda HTML-sivun, jonka avulla hallitaan näiden käyttäjän työnkulkukokemusten ulkoasua. 

Jos haluat mukauttaa Dynamics 365 Commercella luotuja käyttäjän käytäntöjen sivuja, katso [Käyttäjän sisäänkirjausten mukautettujen sivujen määrittäminen](custom-pages-user-logins.md). Lisätietoja on kohdassa [Azure Active Directory B2C:n käyttäjäkokemusten käyttöliittymän mukauttaminen](/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulkukäytännön luominen

Voit luoda rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulkukäytännön seuraavasti.

1. Valitse Azure-portaalin vasemmanpuoleisessa siirtymisruudussa **Käyttäjän työnkulut (käytännöt)**.
1. Valitse **Azure AD B2C – käyttäjän työnkulut (käytännöt)** -sivulla **Uusi käyttäjän työnkulku**.
1. Valitse **Rekisteröinti ja sisäänkirjaus** -käytäntö ja sitten **Suositellut**-versio.
1. Anna käytännön nimi **Nimi**-kohdassa. Tämä nimi näkyy myöhemmin portaalin määrittämän etuliitteen kanssa (esimerkiksi B2C_1_).
1. Valitse **Tunnistetietojen tarjoajat** -kohdassa soveltuva valintaruutu.
1. Valitse **Usean tekijän todennus** yritykselle soveltuva vaihtoehto. 
1. Valitse **Käyttäjän määritteet ja vaatimukset** -kohdassa vaihtoehdot määritteiden tai palautusvaatimusten keräämistä varten. Commerce edellyttää seuraavien oletusasetusten käyttämistä:

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

Seuraavassa kuvassa on **Suorita käyttäjän työnkulku** -vaihtoehto Azure AD B2C:n rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulussa.

![Käyttäjän työnkulku -vaihtoehdon suorittaminen käytännön työnkulussa.](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a>Profiilin muokkaamisen käyttäjän työnkulkukäytännön luominen

Voit luoda profiilin muokkaamisen käyttäjän työnkulkukäytännön seuraavasti.

1. Valitse Azure-portaalin vasemmanpuoleisessa siirtymisruudussa **Käyttäjän työnkulut (käytännöt)**.
1. Valitse **Azure AD B2C – käyttäjän työnkulut (käytännöt)** -sivulla **Uusi käyttäjän työnkulku**.
1. Valitse **Profiilin muokkaus** ja valitse sitten **Suositeltu**-versio.
1. Anna **Nimi**-kohtaan profiilin muokkaamisen käyttäjän työnkulku. Tämä nimi näkyy myöhemmin portaalin määrittämän etuliitteen kanssa (esimerkiksi B2C_1_).
1. Valitse **Tunnistetietojen tarjoajat** -kohdassa **Sisäänkirjaus sähköpostiosoitteella**.
1. Valitse **Käyttäjän määritteet** -kohdassa seuraavat valintaruudut:
    - **Sähköpostiosoitteet** (vain **Palautusvaatimus**)
    - **Etunimi** (**Keräilymäärite** ja **Palautusvaatimus**)
    - **Tunnistetietojen tarjoaja** (vain **Palautusvaatimus**)
    - **Sukunimi** (**Keräilymäärite** ja **Palautusvaatimus**)
    - **Käyttäjän objektin tunnus** (vain **Palautusvaatimus**)
1. Valitse **Luo**.

Seuraavassa kuvassa on esimerkki Azure AD B2C:n profiilin muokkauksen käyttäjän työnkulusta.

![Profiilin muokkaamisen käyttäjän työnkulun luominen.](./media/B2CImage_12.png)

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

## <a name="add-social-identity-providers-optional"></a>Yhteisöpalvelun tunnistetietojen tarjoajien lisääminen (valinnainen)

Yhteisöpalvelun tunnistetietojen tarjoajat sallivat käyttäjien käyttää yhteisöpalvelun tilejä todennuksessa. Yhteisöpalvelun tunnistepalvelun tarjoajan todentamisen lisääminen on valinnaista Dynamics 365 Commercessa. 

Jos yhteisöpalvelun tunnistetietojen tarjoajan todentamista ei lisätä, Azure AD B2C:n oletusprofiilit ovat käyttäjäkunnan pääprofiilit. Käyttäjät valitsevat oman käyttäjätunnuksen (haluamansa sähköpostiosoite) ja määrittävät salasanan. Azure AD B2C todentaa käyttäjät suoraan. 

Jos yhteisöpalveluiden tunnustietojen tarjoajan todentaminen lisätään ja käyttäjä valitsee jonkin tarjotuista yhteisöpalveluiden tunnistetietojen tarjoajista, Azure AD B2C -vuokraajaan luodaan yhä yksikkö. Azure AD B2C todentaa tämän jälkeen käyttäjän valtuustiedot yhteisöpalvelujen tunnistetietojen tarjoajan avulla.

> [!NOTE]
> Tunnistetietojen tarjoajan sisäänkirjaus luo tietueen B2C-vuokraajaan. Se tehdään kuitenkin eri muodossa kuin paikalliset tilit, koska se kutsuu ulkoisen yhteisöpalvelujen tunnistetietojen tarjoajan viitteen todennusta varten. Käyttäjä voi käyttää samaa sähköpostiosoitetta eri yhteisöpalvelujen tunnistetietojen tarjoajien kanssa. Tämä tarkoittaa sitä, että vuokraajan tunnistuksen käyttäjätunnuksena käyttämä sähköpostiosoite ei ehkä ole yksilöllinen. Azure AD B2C edellyttää vain, että käyttäjillä on yksilöllinen sähköpostiosoite paikallisilla B2C-tileillä.

Ennen kuin lisäät yhteisöpalvelujen tunnistetietojen tarjoajan todennusta varten, siirry tunnistetietojen tarjoajan portaaliin ja määritä tunnistetietojen tarjoajan sovellus Azure AD B2C -dokumentaatiossa määritetyllä tavalla. Alla on luettelo dokumentaation linkeistä.

- [Amazon](/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (yksi vuokraaja)](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsoft-tili](/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Yhteisöpalvelujen tunnistetietojen tarjoajan lisääminen ja määrittäminen

Voit lisätä ja määrittää yhteisöpalveluiden tunnistetietojen tarjoajan seuraavasti.  

1. Siirry Azure-portaalissa kohtaan **Tunnistetietojen tarjoajat**.
1. Valitse **Lisää**. Näkyviin tulee **Lisää tunnistetietojen tarjoaja** -näyttö.
1. Anna **Nimi**-kohtaan käyttäjille sisäänkirjausnäytössä näytettävä nimi.
1. Valitse **Tunnistetietojen tarjoajan tyyppi** -kohtaan luettelosta tunnistetietojen tarjoaja.
1. Valitse **OK**.
1. Valitse **Määritä tämä tunnistetietojen tarjoaja**, jos haluat ottaa käyttöön **Määritä yhteisöpalvelujen tunnistetietojen tarjoaja** -näytön.
1. Anna **Asiakasohjelman tunnus** -kohdassa tunnistetietojen tarjoajan sovelluksen asetuksista saatu asiakasohjelman tunnus.
1. Anna **Asiakasohjelman salasana** -kohdassa tunnistetietojen tarjoajan sovelluksen asetuksista saatu asiakasohjelman salasana.
1. Liitä käyttäjän työnkulku rekisteröitymis ja sisäänkirjauskäytäntöihin seuraavasti:
1. Siirry kohtaan **Azure AD B2C – käyttäjän työnkulut (käytännöt) \> {oma sisäänkirjaus- ja rekisteröitymiskäytäntö} \> Tunnistetietojen tarjoajat**.
1. Voit liittää sisäänkirjauksen/rekisteröitymisen käyttäjän työnkulun käytännön valitsemalla kunkin tunnistetietojen tarjoajan, jonka olet määrittänyt tiliä varten. Jos haluat testata nämä, valitse **Suorita käyttäjän työnkulku** jokaisen tunnistetietojen tarjoajan kohdalla. Uudessa välilehdessä näkyy kirjautumissivu, joka sisältää uuden tunnistetietojen tarjoajan valintaruudun.

Seuraavassa kuvassa on esimerkki **Lisää tunnistetietojen tarjoaja**- ja **Määritä yhteisöpalvelujen tunnistetietojen tarjoaja** -näytöistä Azure AD B2C:ssä.

![Yhteisöpalvelujen tunnistetietojen tarjoajan lisääminen sovellukseen.](./media/B2CImage_14.png)

Seuraavassa kuvassa on esimerkki siitä, miten tunnistetietojen tarjoajat valitaan Azure AD B2C:n **Tunnistetietojen tarjoaja** -sivulla.

![Valitse käytäntöä varten kaikki yhteisöpalvelujen tunnistetietojen tarjoajat, jotka otetaan käyttöön.](./media/B2CImage_16.png)

Seuraavassa kuvassa on esimerkki oletussisäänkirjausnäytöstä, jossa näkyy yhteisöpalveluiden tunnistetietojen tarjoajan sisäänkirjauspainike.

> [!NOTE]
> Jos käytät Commercessa luotuja mukautettuja sivuja käyttäjätyönkulkuihin, yhteisöpalveluiden tunnistetietojen toimittajien painikkeet on lisättävä käyttäen Commerce-moduulikirjaston laajennusominaisuuksia. Kun määrität sovelluksille tietyn yhteisöpalvelun tunnistetietojen tarjoajan, joissakin tapauksissa URL- tai konfiguraatiomerkkijonoissa voi kirjainkoolla olla merkitystä. Lisätietoja saat hteisöpalvelujen tunnistetietojen tarjoajalta.
 
![Esimerkki oletussisäänkirjausnäytöstä, jossa näkyy yhteisöpalveluiden tunnistetietojen tarjoajan sisäänkirjauspainike.](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Commerce-pääkonttorin päivittäminen uusilla Azure AD B2C -tiedoilla

Kun Azure AD B2C:n yllä mainitut valmisteluvaiheet on tehty, Azure AD B2C -sovellus on rekisteröitävä Dynamics 365 Commerce -ympäristöön.

Voit päivittää pääkonttorin uusilla Azure AD B2C -tiedoilla seuraavasti.

1. Valitse Commercessa **Kaupan yhteiset parametrit** ja valitse **Tunnistetietojen tarjoajat** vasemmanpuoleisessa valikossa.
1. Tee **Tunnistetietojen tarjoajat** -kohdassa seuraavat toiminnot:
    1. Anna **Myöntäjä**-ruutuun tunnistetietojen tarjoajan myöntäjän URL-osoite. Voit etsiä myöntäjän URL-osoitteen alla olevan [Myöntäjän URL-osoitteen hankkiminen](#obtain-issuer-url) -kohdan avulla.
    1. Anna **Nimi**-ruutuun myöntäjän tietueen nimi.
    1. Anna **Tyyppi**-ruutuun **Azure AD B2C (id_token)**.
1. Valitse yllä mainittu B2C:n tunnistetietojen tarjoajan nimike ja tee **Luovuttavat osapuolet** -kohdassa seuraavat toiminnot:
    1. Anna **ClientID**-ruutuun B2C-sovelluksen tunnus. Se löytyy **Sovelluksen tunnus** -ruudusta B2C-sovelluksen ominaisuuksien sivulta.
    1. Kirjoita **Tyyppi**-ruutuun **Julkinen**.
    1. Kirjoita **Käyttäjätyyppi**-ruutuun **Asiakas**.
1. Valitse toimintoruudussa **Tallenna**.
1. Hae Commerce-hakuruudussa **Jakeluaikataulu**
1. Valitse **Jakeluaikataulut**-sivun vasemmanpuoleisessa valikossa **1110 Yleinen määritys** -työ.
1. Valitse toimintoruudussa **Suorita nyt**.

### <a name="obtain-issuer-url"></a>Myöntäjän URL-osoitteen hankkiminen

Voit hankkia tunnistetietojen tarjoajan URL-osoitteen seuraavasti.
1. Siirry Azure-portaalin Azure AD B2C -sivulla **Rekisteröityminen ja sisäänkirjaus** -käyttäjävirtaan.
1. Valitse vasemman siirtymisvalikon **Sivun asettelut**, valitse **Asettelun nimi** -kohdasta **Yhdistetty rekisteröitymis- ja sisäänkirjaussivu** ja valitse sitten **Suorita käyttäjävirta**.
1. Varmista, että sovellus on määritetty edellä luotuun haluttuun Azure AD B2C-sovellukseen, ja valitse sitten linkki **Suorita käyttäjävirta** -otsikosta, joka sisältää ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``.
1. Selaimen välilehdessä näkyy metatietosivu. Kopioi tunnistetietojen tarjoajan myöntäjän URL-osoite (arvo kohdassa **"issuer"**).
   - Esimerkki: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**TAI**: Voit muodostaa saman metatietojen URL-osoitteen manuaalisesti seuraavasti.

1. Luo metatietojen URL-osoite seuraavassa muodossa käyttämällä B2C-vuokraajaa ja käytäntöä seuraavasti: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Esimerkki: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Kirjoita metatietojen osoitteen URL-osoite selaimen osoitepalkkiin.
1. Kopioi metatiedoissa tunnistetietojen tarjoajan myöntäjän URL-osoite (**myöntäjän** arvo).
    - Esimerkki: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>B2C-vuokraajan määrittäminen Commerce-sivuston luontiohjelmassa

Kun Azure AD B2C -vuokraajan määrittäminen on tehty, B2C-vuokraaja on määritettävä Commerce-sivuston luontiohjelmassa. Määritysvaiheita ovat esimerkiksi B2C-sovelluksen tietojen kerääminen Azure-portaalista, B2C-sovelluksen tietojen syöttäminen sivuston luontiohjelmaan ja B2C-sovelluksen liittäminen sivustoon ja kanavaan.

### <a name="collect-the-required-application-information"></a>Tarvittavien sovellustietojen kerääminen

Voit kerätä tarvittavat sovellustiedot seuraavasti.

1. Siirry Azure-portaalissa kohtaan **Aloitus \> Azure AD B2C - sovellukset**.
1. Valitse sovellus ja valitse sitten vasemmanpuoleisesta navigointiruudusta **Ominaisuudet**, jos haluat hakea sovelluksen tiedot.
1. Kerää **Sovelluksen tunnus** -ruudusta B2C-sovelluksen tunnus, jonka B2C-vuokraaja loi. Tämä syötetään myöhemmin **Asiakasohjelman GUID** -arvona sivuston luontiohjelmaan.
1. Kerää **Vastauksen URL-osoite** -kohdasta vastauksen URL-osoite.
1. Siirry kohtaan **Aloitus \> Azure AD B2C – käyttäjän työnkulut (käytännöt)** ja kerää sitten kunkin käyttäjän työnkulkukäytännön nimet.

Seuraavassa kuvassa on esimerkki **Azure AD B2C - sovellukset** -sivusta.

![Siirtyminen vuokraajan B2C-sovellukseen.](./media/B2CImage_19.png)

Seuraavassa kuvassa on esimerkki sovelluksen **Ominaisuudet** -sivusta Azure AD B2C -ratkaisussa. 

![Sovelluksen tunnuksen kopioiminen B2C-sovelluksen ominaisuuksista.](./media/B2CImage_21.png)

Seuraavassa kuvassa on esimerkki käyttäjän työnkulkukäytännöistä **Azure AD B2C – käyttäjän työnkulut (käytännöt)** -sivulla.

![Kaikkien B2C-käytännön työnkulun nimien kerääminen.](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a>AAD B2C -vuokraajan sovelluksen tietojen syöttäminen Commerceen

Anna Azure AD B2C -vuokraajan tiedot Commercen sivuston luontiohjelmaan ennen B2C-vuokraajan liittämistä sivustoihin.

Voit lisätä AAD B2C -vuokraajan sovelluksen tiedot Commerceen seuraavasti.

1. Kirjaudu sisään järjestelmänvalvojana Commerce-sivuston luontiohjelmaan ympäristössä.
1. Laajenna se valitsemalla vasemmasta siirtymisruudusta **Vuokraajan asetukset**.
1. Valitse **Vuokraajan asetukset** -kohdasta **B2C-asetukset**. 
1. Valitse pääikkunassa **B2C-sovellukset**-kohdan vieressä oleva **Hallitse**. (Jos vuokraaja näkyy B2C-sovellukset-luettelossa, järjestelmänvalvoja on jo lisännyt sen. Tarkista, että vaiheen 6 nimikkeet vastaavat B2C-sovellusta.)
1. Valitse **Lisää B2C-sovellus**.
1. Anna seuraavat pakolliset nimikkeet näkyvissä olevassa muodossa käyttämällä B2C-vuokraajan ja sovelluksen arvoja. Kentät, jotka eivät ole pakollisia (joissa ei ole tähteä), voidaan jättää tyhjäksi.

    - **Sovelluksen nimi**: B2C-sovelluksen nimi, esimerkiksi FABRIKAM B2C.
    - **Vuokralaisen nimi**: B2C-vuokralaisen nimi (Käytä esimerkiksi fabrikam-nimeä, jos toimialue näkyy muodossa "fabrikam.onmicrosoft.com" B2C-vuokralaiselle). 
    - **Unohdetun salasanan käytännön tunnus**: Unohdetun salasanan käyttäjän työnkulkukäytännön tunnus, esimerkiksi B2C_1_PasswordReset.
    - **SignUp SignIn -käytännön tunnus**: Rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulkukäytännön tunnus, esimerkiksi B2C_1_signup_signin.
    - **Asiakasohjelman GUID**: B2C-sovelluksen tunnus, esimerkiksi 22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6.
    - **Profiilin muokkauskäytännön tunnus**: Profiilin muokkaamisen käyttäjän työnkulkukäytännön tunnus, esimerkiksi B2C_1A_ProfileEdit.

1. Valitse **OK**. B2C-sovelluksen nimi tulee nyt näkyviin luetteloon.
1. Tallenna muutokset valitsemalla **Tallenna**.

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>B2C-sovelluksen liittäminen sivustoon ja kanavaan

> [!WARNING]
> Jos sivusto on jo liitetty B2C-sovellukseen, toiseen B2C-sovellukseen vaihtaminen poistaa tähän ympäristöön jo rekisteröityneiden käyttäjien nykyiset viitteet. Jos tätä muutetaan, mitkään tällä hetkellä liitetyn B2C-sovelluksen tunnistetiedot eivät ole käyttäjien käytettävissä. 
> 
> Päivitä vain B2C-sovellus, jos olet määrittämässä kanavan B2C-sovellusta ensimmäistä kertaa tai jos yrität saada käyttäjät rekisteröitymään uudelleen tähän kanavaan uuden B2C-sovelluksen avulla uusilla tunnistetiedoilla. Ole varovainen, kun liität kanavia B2C-sovelluksiin. Anna sovelluksille selkeät nimet. Jos kanavaa ei ole liitetty B2C-sovellukseen alla kuvattujen vaiheiden avulla, kanavaan kirjautuvat käyttäjät siirretään B2C-sovellukseen, joka on **oletussovellus** B2C-sovellusten **Vuokraajan asetukset \> B2C-asetukset** -luettelossa.

Voit liittää B2C-sovelluksen sivustoon ja kanavaan seuraavasti.

1. Siirry sivustoon Commerce-sivuston luontiohjelmassa.
1. Laajenna se valitsemalla vasemmasta siirtymisruudusta **Sivuston asetukset**.
1. Valitse **Sivuston asetukset** -kohdassa **Kanavat**.
1. Valitse pääikkunassa **Kanavat**-kohdassa kanava.
1. Valitse oikeanpuoleisessa kanavan ominaisuuksien ruudussa B2C-sovelluksen nimi avattavasta **Valitse B2C-sovellus** -luettelosta.
1. Valitse **Sulje** ja valitse sitten **Tallenna ja julkaise**.

## <a name="additional-b2c-information"></a>B2C-lisätiedot

### <a name="customer-migration"></a>Asiakkaan siirtäminen

Jos harkitset asiakastietojen siirtämistä aiemmasta tunnistetietojen tarjoajan ympäristöstä, tarkista asiakkaan siirron tarpeet Dynamics 365 Commerce -ryhmän kanssa.

Lisätietoja asiakkaan siirron Azure AD B2C -dokumentaatiosta on kohdassa [Käyttäjien siirtäminen Azure Active Directory B2C -sovellukseen](/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Mukautetut käytännöt

Lisätietoja Azure AD B2C -sovelluksen yhteydenottojen ja käytännön työnkulkujen mukauttamisesta erilaisiksi kuin B2C-standardikäytännöt on kohdassa [Azure Active Directory B2C -sovelluksen mukautetut käytännöt](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Toissijainen järjestelmänvalvoja

Valinnainen toissijainen järjestelmänvalvojatili voidaan lisätä B2C-vuokraajan **Käyttäjä**-osaan. Tämä voi olla suora tili tai yleinen tili. Jos sinun on jaettava tili ryhmän resursseille, myös yhteinen tili voidaan luoda. Azure AD B2C -sovellukseen tallennettujen tietojen luottamuksellisuuden vuoksi yrityksen turvakäytäntöjen tulee valvoa yleistä tiliä tarkasti.

## <a name="additional-resources"></a>Lisäresurssit

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto](deploy-ecommerce-site.md)

[Sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md)

[Dynamics 365 Commerce -sivuston liittäminen online-kanavaan](associate-site-online-store.md)

[Robots.txt-tiedostojen hallinta](manage-robots-txt-files.md)

[URL-uudelleenohjausten joukkolataus palveluun](upload-bulk-redirects.md)

[Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)

[Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä](configure-multi-B2C-tenants.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]