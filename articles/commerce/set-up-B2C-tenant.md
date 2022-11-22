---
title: B2C-vuokraajan määrittäminen Commercessa
description: Tässä artikkelissa kerrotaan, miten Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajat määritetään Microsoft Dynamics 365 Commercen käyttäjän sivuston todennusta varten.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 3421dd3d67198a99ac236a56cbb4f300cb591a03
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785124"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>B2C-vuokraajan määrittäminen Commercessa

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajat määritetään Dynamics 365 Commercen käyttäjän sivuston todennusta varten.

Dynamics 365 Commerce käyttää Azure AD B2C -ratkaisua käyttäjän tunnistetietojen ja todennuksen työnkulkujen tukemisessa. Käyttäjä voi rekisteröityä, kirjautua sisään ja nollata salasanan näiden työnkulkujen avulla. Azure AD B2C tallentaa luottamukselliset käyttäjän todennustiedot, kuten käyttäjätunnuksen ja salasanan. B2C-vuokraajan käyttäjätietueeseen tallennetaan B2C:n paikallisen tilin tietue tai B2C:n yhteisöpalvelun tunnuksen tarjoajan tietue. Nämä B2C-tietueet linkitetään takaisin asiakastietueeseen Commerce-ympäristössä.

> [!WARNING] 
> Azure AD B2C poistaa vanhat käyttäjätyönkulut käytöstä 1.8.2021 mennessä. Näin ollen on hyvä suunnitella käyttäjätyönkulkujen siirtämistä uuteen suositeltuun versioon. Uudessa versiossa on ominaisuuksien pariteetti ja uusia ominaisuuksia. Commerce-version 10.0.15 tai sitä uudemman version moduulikirjastoa tulee käyttää suositeltujen B2C-käyttäjätyönkulkujen kanssa. Lisätietoja on kohdassa [Työnkulut Azure Active Directory B2C:ssä](/azure/active-directory-b2c/user-flow-overview).
 
 > [!NOTE]
 > Commerce-arviointiympäristöt tulevat esiladatun Azure AD B2C -vuokraajan kanssa esittelytarkoituksiin. Arviointiympäristöissä ei tarvitse ladata omaa Azure AD B2C -vuokraajaa alla olevia vaiheita käyttäen.

> [!TIP]
> Sivuston käyttäjiä voi suojata entisestään ja parantaa Azure AD:n B2C-vuokraajien suojausta Azure AD:n tunnistetietojen suojauksella ja ehdollisella käyttöoikeudella. Lisätietoja Azure AD:n B2C Premium P1- ja Premium P2 -vuokraajien käytettävissä olevien ominaisuuksien tarkastelemisesta on kohdassa [Azure AD B2C:n tunnistetietojen suojauksella ja ehdollisella käyttöoikeudella](/azure/active-directory-b2c/conditional-access-identity-protection-overview).

## <a name="dynamics-environment-prerequisites"></a>Dynamics-ympäristön edellytykset

Varmista ennen aloittamista, että Dynamics 365 Commerce -ympäristösi ja sähköisen kaupankäynnin kanavasi on määritetty asianmukaisesti täyttämällä seuraavat edellytykset.

- Määritä myyntipistetoimintojen **AllowAnonymousAccess**-arvoksi 1 Commerce-pääkonttorissa:
    1. Siirry kohtaan **Myyntipistetoiminnot**.
    1. Napsauta **Mukauta**-kohtaa toimintoruudukossa hiiren kakkospainikkeella ja valitse se.
    1. Valitse **Lisää kenttä**.
    1. Lisää käytettävissä olevien sarakkeiden luettelosta **AllowAnonymousAccess**-sarake valitsemalla se.
    1. Valitse **Päivitä**.
    1. Muuta **612**-asiakkaanlisäystoiminnon osalta **AllowAnonymousAccess**-arvoksi 1.
    1. Suorita **1090 (rekisterit)** -työ.
- Määritä numerosarjan asiakastilin **Manuaalinen**-määritteen arvoksi **Ei** Commerce-pääkonttorissa:
    1. Valitse **Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Myyntireskontran parametrit**.
    1. Valitse **Numerosarjat**.
    1. Kaksoisnapsauta **Numerosarjan koodi** -arvoa **Asiakastili**-rivillä.
    1. Määritä numerosarjan **Yleistä**-pikavälilehden **Manuaalinen**-arvoksi **Ei**.

Kun Dynamics 365 Commerce -ympäristö on otettu käyttöön, on myös suositeltavaa [alustaa alkutiedot](enable-configure-retail-functionality.md) ympäristössä.

## <a name="next-steps"></a>Seuraavat vaiheet

Jos haluat jatkaa kuluttajakaupan vuokraajan määritysprosessia Commercessa, jatka [Olemassa olevan Azure AD:n kuluttajakaupan luominen tai siihen linkittäminen Azure-portaalissa](create-link-aad-b2c-tenant.md) -kohtaan.

## <a name="additional-resources"></a>Lisäresurssit

[Olemassa olevan Azure AD:n kuluttajakaupan vuokraajan luominen tai linkittäminen Azure-portaalissa](create-link-aad-b2c-tenant.md)

[B2C-sovelluksen luominen](create-b2c-app.md)

[Käyttäjän työnkulkukäytäntöjen luominen](create-user-flow-policies.md)

[Yhteisöpalvelun tunnistetietojen tarjoajien lisääminen (valinnainen)](add-social-identity-providers.md)

[Commerce headquartersin päivittäminen uusilla Azure AD:n kuluttajakaupan tiedoilla](update-hq-aad-b2c-info.md)

[B2C-vuokraajan määrittäminen Commerce-sivuston luontiohjelmassa](config-b2c-tenant-site-builder.md)

[B2C-lisätiedot](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
