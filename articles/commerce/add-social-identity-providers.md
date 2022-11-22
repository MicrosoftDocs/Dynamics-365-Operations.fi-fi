---
title: Yhteisöpalvelun tunnistetietojen tarjoajien lisääminen
description: Tässä artikkelissa kerrotaan, miten yhteisöpalvelun tunnistetietojen tarjoajat lisätään Microsoft Azure -portaalissa.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 5596097a5484acafda54adcfffa68fb59c8fbc65
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785241"
---
# <a name="add-social-identity-providers"></a>Yhteisöpalvelun tunnistetietojen tarjoajien lisääminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten yhteisöpalvelun tunnistetietojen tarjoajat lisätään Microsoft Azure -portaalissa.

Yhteisöpalvelun tunnistetietojen tarjoajat sallivat käyttäjien käyttää yhteisöpalvelun tilejä todennuksessa. Yhteisöpalvelun tunnistepalvelun tarjoajan todentamisen lisääminen on valinnaista Dynamics 365 Commercessa. 

Jos yhteisöpalvelun tunnistetietojen tarjoajan todentamista ei lisätä, Azure Active Directoryn (Azure AD) kuluttajakaupan oletusprofiilit ovat käyttäjäkunnan pääprofiilit. Käyttäjät valitsevat oman käyttäjätunnuksen (haluamansa sähköpostiosoite) ja määrittävät salasanan. Azure AD B2C todentaa käyttäjät suoraan. 

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

> [!NOTE]
> Yhteisöpalvelujen tunnistetietojen tarjoajien lisääminen on kuluttajakaupan vuokraajan määrittämisen valinnainen vaihe Microsoft Dynamics 365 Commercessa.

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
1. Voit liittää sisäänkirjauksen/rekisteröitymisen käyttäjän työnkulun käytännön valitsemalla kunkin tunnistetietojen tarjoajan, jonka olet määrittänyt tiliä varten. Jos haluat testata työnkulut, valitse **Suorita käyttäjän työnkulku** jokaisen tunnistetietojen tarjoajan kohdalla. Uudessa välilehdessä näkyy kirjautumissivu, joka sisältää uuden tunnistetietojen tarjoajan valintaruudun.

Seuraavassa kuvassa on esimerkki **Lisää tunnistetietojen tarjoaja**- ja **Määritä yhteisöpalvelujen tunnistetietojen tarjoaja** -näytöistä Azure AD B2C:ssä.

![Yhteisöpalvelujen tunnistetietojen tarjoajan lisääminen sovellukseen.](./media/B2CImage_14.png)

Seuraavassa kuvassa on esimerkki siitä, miten tunnistetietojen tarjoajat valitaan Azure AD B2C:n **Tunnistetietojen tarjoaja** -sivulla.

![Valitse käytäntöä varten kaikki yhteisöpalvelujen tunnistetietojen tarjoajat, jotka otetaan käyttöön.](./media/B2CImage_16.png)

Seuraavassa kuvassa on esimerkki oletussisäänkirjausnäytöstä, jossa näkyy yhteisöpalveluiden tunnistetietojen tarjoajan sisäänkirjauspainike.

> [!NOTE]
> Jos käytät Commercessa luotuja mukautettuja sivuja käyttäjätyönkulkuihin, yhteisöpalveluiden tunnistetietojen toimittajien painikkeet on lisättävä käyttäen Commerce-moduulikirjaston laajennusominaisuuksia. Kun määrität sovelluksille tietyn yhteisöpalvelun tunnistetietojen tarjoajan, joissakin tapauksissa URL- tai konfiguraatiomerkkijonoissa voi kirjainkoolla olla merkitystä. Lisätietoja saat hteisöpalvelujen tunnistetietojen tarjoajalta.
 
![Esimerkki oletussisäänkirjausnäytöstä, jossa näkyy yhteisöpalveluiden tunnistetietojen tarjoajan sisäänkirjauspainike.](./media/B2CImage_17.png)

## <a name="next-steps"></a>Seuraavat vaiheet

Jos haluat jatkaa kuluttajakaupan vuokraajan määritysprosessia Commercessa, jatka [Commerce headquartersin päivittäminen uusilla Azure AD:n kuluttajakaupan tiedoilla](update-hq-aad-b2c-info.md) -kohtaan.

## <a name="additional-resources"></a>Lisäresurssit

[B2C-vuokraajan määrittäminen Commercessa](set-up-b2c-tenant.md)

[Olemassa olevan Azure AD:n kuluttajakaupan vuokraajan luominen tai linkittäminen Azure-portaalissa](create-link-aad-b2c-tenant.md)

[B2C-sovelluksen luominen](create-b2c-app.md)

[Käyttäjän työnkulkukäytäntöjen luominen](create-user-flow-policies.md)

[Commerce headquartersin päivittäminen uusilla Azure AD:n kuluttajakaupan tiedoilla](update-hq-aad-b2c-info.md)

[B2C-vuokraajan määrittäminen Commerce-sivuston luontiohjelmassa](config-b2c-tenant-site-builder.md)

[B2C-lisätiedot](additional-b2c-info.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
