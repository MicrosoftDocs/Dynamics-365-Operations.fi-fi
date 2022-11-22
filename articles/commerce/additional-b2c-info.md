---
title: B2C-lisätiedot
description: Tässä artikkelissa on lisätietoja Microsoft Dynamics 365 Commercen kuluttajakaupan vuokraajan määrittämisestä.
author: BrianShook
ms.date: 11/14/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: b60ef15544cd30c44968ee7a588a8a9fb08e8223
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785236"
---
# <a name="additional-b2c-information"></a>B2C-lisätiedot

[!include [banner](includes/banner.md)]

Tässä artikkelissa on lisätietoja Microsoft Dynamics 365 Commercen kuluttajakaupan vuokraajan määrittämisestä.

### <a name="customer-migration"></a>Asiakkaan siirtäminen

Jos harkitset asiakastietojen siirtämistä aiemmasta tunnistetietojen tarjoajan ympäristöstä, tarkista asiakkaan siirron tarpeet Dynamics 365 Commerce -ryhmän kanssa.

Lisätietoja asiakkaan siirron Azure AD B2C -dokumentaatiosta on kohdassa [Käyttäjien siirtäminen Azure Active Directory B2C -sovellukseen](/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Mukautetut käytännöt

Lisätietoja Azure AD B2C -sovelluksen yhteydenottojen ja käytännön työnkulkujen mukauttamisesta erilaisiksi kuin B2C-standardikäytännöt on kohdassa [Azure Active Directory B2C -sovelluksen mukautetut käytännöt](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Toissijainen järjestelmänvalvoja

Valinnainen toissijainen järjestelmänvalvojatili voidaan lisätä B2C-vuokraajan **Käyttäjä**-osaan. Tämä voi olla suora tili tai yleinen tili. Jos sinun on jaettava tili ryhmän resursseille, myös yhteinen tili voidaan luoda. Azure AD B2C -sovellukseen tallennettujen tietojen luottamuksellisuuden vuoksi yrityksen turvakäytäntöjen tulee valvoa yleistä tiliä tarkasti.

### <a name="set-up-a-custom-sign-in-domain"></a>Mukautetun kirjautumistoimialueen asetukset

Azure AD B2C:n avulla voit määrittää mukautetun kirjautumistoimialueen Azure AD B2C-vuokraajalle. Lisätietoja on kohdassa [Mukautettujen toimialueiden käyttöönottaminen Azure Active Directory B2C:ssä](/azure/active-directory-b2c/custom-domain). 

Jos käytät mukautettua kirjautumistoimialuetta, toimialue on syötettävä Commercen sivustonmuodostimeen.

Lisää mukautettu kirjautumistoimialue sivustonmuodostimeen seuraavasti.

1. Valitse sivuston rakennustyökalun oikeasta yläkulmasta sivuston vaihtaja ja valitse sitten **Sivustojen hallinta**.
1. Laajenna se valitsemalla vasemmasta siirtymisruudusta **Vuokraajan asetukset \> Sivuston todennuksen määritys**.
1. Valitse **Sivuston todennusprofiilit** -kohdan vierestä **Hallitse**.
1. Valitse oikealla olevasta pikaikkunavalikosta sen sivuston todennusprofiilin vieressä oleva **Muokkaa**-painike (kynäkuvake), jota varten haluat määrittää mukautetun toimialueen.
1. Kirjoita **Muokkaa sivuston todennusprofiili** -valintaikkunan **Kirjaudu mukautettuun toimialueeseen** -kohtaan mukautettu kirjautumistoimialue (esimerkiksi login.fabrikam.com).

> [!WARNING]
> Kun päivität Azure AD B2C-vuokraajan mukautetulle toimialueelle, muutos vaikuttaa luodun tunnuksen vuokraajan myöntäjän tietoihin. Myöntäjän tiedot sisältävät mukautetun toimialueen Azure AD B2C:n toimittaman oletustoimialueen asemesta. Eri **Myöntäjä**.määritys Commerce headquartersissa (**Retail and Commerce \> Pääkonttorin asetukset \> Parametrit \> Kaupankäynnin yhteiset parametrit \> Tunnistetietojen toimittajat**) muuttaa järjestelmän vuorovaikutusta sivuston käyttäjien kanssa ja saattaa luoda uuden asiakastietueen, jos käyttäjä todentaa tietoja uutta myöntäjää vastaan. Mahdolliset mukautetut toimialuemuutokset on testattava huolellisesti ennen mukautetun toimialueen vaihtamista live Azure AD B2C-ympäristössä.

## <a name="additional-resources"></a>Lisäresurssit

[B2C-vuokraajan määrittäminen Commercessa](set-up-b2c-tenant.md)

[Olemassa olevan Azure AD:n kuluttajakaupan vuokraajan luominen tai linkittäminen Azure-portaalissa](create-link-aad-b2c-tenant.md)

[B2C-sovelluksen luominen](create-b2c-app.md)

[Käyttäjän työnkulkukäytäntöjen luominen](create-user-flow-policies.md)

[Yhteisöpalvelun tunnistetietojen tarjoajien lisääminen (valinnainen)](add-social-identity-providers.md)

[Commerce headquartersin päivittäminen uusilla Azure AD:n kuluttajakaupan tiedoilla](update-hq-aad-b2c-info.md)

[B2C-vuokraajan määrittäminen Commerce-sivuston luontiohjelmassa](config-b2c-tenant-site-builder.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
