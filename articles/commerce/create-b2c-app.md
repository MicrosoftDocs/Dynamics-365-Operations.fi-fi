---
title: Kuluttajakauppasovelluksen luominen
description: Tässä artikkelissa kerrotaan, miten kuluttajakauppasovellus luodaan Microsoft Azure -portaalissa.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: d8956d51bac7bf2a162a370ae5ef1c7e7cdc1e2f
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785245"
---
# <a name="create-a-b2c-application"></a>Kuluttajakauppasovelluksen luominen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten kuluttajakauppasovellus luodaan Microsoft Azure -portaalissa.

Kun kuluttajakaupan vuokraaja on luotu, luodaan kuluttajakauppasovellus uudessa Azure Active Directoryn (Azure AD) vuokraajassa Commercen kanssa käytettäväksi.

Luo B2C-sovellus seuraavasti.

1. Valitse Azure-portaalissa **Sovellusten rekisteröinnit** ja sitten **Uusi rekisteröinti**.
1. Anna tälle Azure AD B2C -sovellukselle nimi **Nimi**-kentässä.
1. Valitse **Tuetut tilityypit** -kohdasta **Tilit mistä tahansa tunnistetietojen tarjoajasta tai organisaatiohakemistosta (käyttäjien tunnistamiseksi käyttäjätyönkulkujen avulla)**.
1. Syötä **Uudelleenohjauksen URI** -kenttään erilliset vastaus-URL-osoitteet **Internet**-tyyppisinä. Katso lisätietoja vastauksen URL-osoitteista ja niiden muotoilusta allal olevasta [Vastauksen URL-osoitteet](#reply-urls) -kohdasta. Sinun on syötettävä uudelleenohjauksen URI tai vastauksen URL-osoite, jotta Azure AD B2C -järjestelmän uudelleenohjaus takaisin sivustoon voidaan ottaa käyttöön, kun käyttäjä tekee todennuksen. Vastauksen URL-osoite voidaan lisätä rekisteröintiprosessin aikana, tai sen voi lisätä myöhemmin valitsemalla B2C-sovelluksen **Yhteenveto**-osan **Yhteenveto**-valikosta **Lisää uudelleenohjauksen URI** -linkin.
1. Jos sinulla on **käyttöoikeudet**, valitse **Myönnä järjestelmänvalvojan hyväksyntä OpenId- ja offline_access-käyttöoikeuksille**.
1. Valitse **Rekisteröi**.
1. Valitse juuri luotu sovellus ja siirry **Todennus**-valikkoon. 
1. Jos vastauksen URL-osoite on syötetty, ota se käyttöön sovelluksessa valitsemalla **Implisiittinen myöntäminen ja hybridityönkulut** -kohdassa sekä **Käyttöoikeustunnukset** että **Tunnuksen tunnisteet** ja valitse sitten **Tallenna**. Jos vastauksen URL-osoitetta ei ole syötetty rekisteröinnin aikana, voit lisätä sen myös tälle sivulle valitsemalla **Lisää ympäristö**, valitsemalla **Verkko** ja syöttämällä sitten sovelluksen uudelleenohjauksen URI-osoitteen. Tämän jälkeen voit **Implisiittinen myöntäminen ja hybridityönkulut** -kohdassa valita sekä **Käyttöoikeustunnukset** että **Tunnuksen tunnisteet** -vaihtoehdot.
1. Siirry Azure-portaalin **Yhteenveto**-valikkoon ja kopioi **Sovelluksen (asiakasohjelman) tunnus**. Huomaa, että tämä tunnus tarvitaan myöhemmissä määritysvaiheissa (viitataan myöhemmin nimellä **Asiakasohjelman GUID**).

Lisätietoja sovelluksen rekisteröinneistä Azure AD B2C:ssä on kohdassa [Azure Active Directory B2C:n uusi sovelluksen rekisteröintikokemus](/azure/active-directory-b2c/app-registrations-training-guide)

### <a name="reply-urls"></a>Vastauksen URL-osoitteet

Vastauksen URL-osoitteet ovat tärkeitä, koska ne tarjoavat sallitut palautustoimialueet, kun sivusto kutsuu Azure AD B2C -ratkaisua käyttäjän todentamista varten. Toiminto sallii todennetun käyttäjän paluun takaisin toimialueelle, jolta nämä kirjautuvat (oman sivuston toimialue). 

Lisää **Vastauksen URL-osoite** -ruudun **Azure AD B2C - sovellukset \> Uusi sovellus** -näytössä erilliset rivit sivuston toimialueelle ja (ympäristön valmistelun jälkeen) Commercen luomalle URL-osoitteelle. Näissä URL-osoitteissa on aina käytettävä sallittua URL-osoitteen muotoa. Niiden on aina oltava perus-URL-osoitteita (ei lopussa olevia vinoviivoja tai polkuja). Merkkijono ``/_msdyn365/authresp`` on siis liitettävä perus-URL-osoitteisiin seuraavien esimerkkien mukaisesti.

- ``https://www.fabrikam.com/_msdyn365/authresp`` (Toimialueen tulisi täsmätä sähköisen kaupankäynnin toimialueeseen kokonaan. Jos sinulla on useita toimialueita, sinun on lisättävä tämä URL-osoite kullekin toimialueelle.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="next-steps"></a>Seuraavat vaiheet

Jos haluat jatkaa kuluttajakaupan vuokraajan määrittämisprosessia Commercessa, jatka [Käyttäjän työnkulkujen käytäntöjen luominen](create-user-flow-policies.md) -kohtaan.

## <a name="additional-resources"></a>Lisäresurssit

[B2C-vuokraajan määrittäminen Commercessa](set-up-b2c-tenant.md)

[Olemassa olevan Azure AD:n kuluttajakaupan vuokraajan luominen tai linkittäminen Azure-portaalissa](create-link-aad-b2c-tenant.md)

[Käyttäjän työnkulkukäytäntöjen luominen](create-user-flow-policies.md)

[Yhteisöpalvelun tunnistetietojen tarjoajien lisääminen (valinnainen)](add-social-identity-providers.md)

[Commerce headquartersin päivittäminen uusilla Azure AD:n kuluttajakaupan tiedoilla](update-hq-aad-b2c-info.md)

[B2C-vuokraajan määrittäminen Commerce-sivuston luontiohjelmassa](config-b2c-tenant-site-builder.md)

[B2C-lisätiedot](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
