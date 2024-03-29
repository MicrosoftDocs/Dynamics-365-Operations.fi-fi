---
title: CPOS:n määrittäminen käyttämään mukautettua Azure AD -sovellusta
description: Tässä artikkelissa kerrotaan, kuinka määritetään Cloud POS (CPOS) käyttämään mukautettua Azure Active Directory (Azure AD) -sovellusta.
author: boycez
ms.date: 11/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 5e4ff797410e1e94869cc37684e7622ec0d97842
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746257"
---
# <a name="configure-cpos-to-use-a-custom-azure-ad-app"></a>CPOS:n määrittäminen käyttämään mukautettua Azure AD -sovellusta

[!include [banner](includes/banner.md)]

Oletusarvon mukaan Cloud POS (CPOS) Microsoft Dynamics 365 Commercessa viittaa rekisteröityyn ensimmäisen osapuolen Microsoft-sovellukseen Azure Active Directoryssa (Azure AD). Voit siis käyttää CPOS:ssä ilman, että sinun tarvitse tehdä muutoksia Azure AD:ssä. Voit kuitenkin määrittää CPOS-esiintymäsi hallitsemaasi mukautettuun Azure AD -sovellukseen. Tässä artikkelissa kerrotaan, kuinka määritetään CPOS käyttämään mukautettua Azure AD -sovellusta.

## <a name="set-up-a-custom-retail-server-app-in-azure-ad"></a>Mukautetun Retail Server -sovelluksen määrittäminen Azure AD -sovelluksessa

Noudattamalla seuraavia ohjeita voit luoda ja konfiguroida mukautetun Retail Server -sovelluksen Azure AD:ssa.

1. Kirjaudu [Azure Active Directory -hallintakeskukseen](https://aad.portal.azure.com) mitä tahansa Azure AD -käyttäjätiliä käyttäen. Käyttäjätilillä ei tarvitse olla järjestelmänvalvojan käyttöoikeuksia.
1. Valitse **Azure Active Directory**.
1. Valitse **Sovelluksen rekisteröinnit** ja avaa sovelluksen **Sovelluksen rekisteröinti** -valintaikkunassa valitsemalla **Uusi rekisteröinti**.
1. Määritä seuraavat kentät:

    - **Nimi** – Anna sovelluksen mukautettu nimi. Kirjoita esimerkiksi **Mukautettu Retail Server**.
    - **Tuetut tilityypit** – Valitse oletusasetus **Vain tämän organisaation hakemiston tilit (Vain Microsoft - Yksittäinen vuokraaja)**.
    - **Uudelleenohjauksen URI** – Tämä kenttä ei ole pakollinen. Jätä se tyhjäksi.
    - **Palvelupuun tunniste** – Tämä kenttä ei ole pakollinen. Jätä se tyhjäksi.
    
1. Valitse **Rekisteröi**. Näkyviin tulee juuri rekisteröidyn sovelluksen konfigurointisivu.
1. Valitse **Yleiskuvaus \> Essentials** -osassa **Lisää sovelluksen tunnuksen URI** ja valitse sitten **Aseta** kohdan **Sovelluksen tunnuksen URI** vieressä. Kirjoita ehdotettu arvo muistiin ja hyväksy arvo valitsemalla **Tallenna**. 
1. Valitse **Lisää laajuus** ja valitse sitten seuraavat kentät:

    - **Laajuuden nimi** – Anna laajuuden mukautettu nimi. Kirjoita esimerkiksi **Legacy.Access.Full**.
    - **Kuka voi antaa hyväksynnän** – Määritä organisaation suojauskäytäntöjen mukaan, voivatko sekä järjestelmänvalvojat että käyttäjät tai vain järjestelmänvalvojat antaa hyväksynnän.
    - **Järjestelmänvalvojan hyväksynnän näyttönimi** – Kirjoita näyttönimi. Kirjoita esimerkiksi **Retail Serverin käyttöoikeus**.
    - **Järjestelmänvalvojan hyväksynnän kuvas** – Kirjoita kuvaus. Kirjoita esimerkiksi **Antaa Retail Serverin ohjelmointirajapintojen käyttöoikeuden**.

1. Suorita laajuuden luontiprosessi loppuun valitsemalla **Lisää laajuus**.

## <a name="set-up-a-custom-cpos-app-in-azure-ad"></a>Mukautetun CPOS-sovelluksen asetukset Azure AD:ssä

> [!IMPORTANT]
> Jos olet päivittämässä olemassa olevaa mukautettua CPOS Azure AD -sovellusta, joka luotiin ennen Commerce-versiota 10.0.21, noudata ohjeita, jotka on kuvattu kohdassa [Ennen Commerce-versiota 10.0.21 luodun mukautetun CPOS Azure AD -sovelluksen päivittäminen](#upgrade-an-existing-custom-cpos-azure-ad-app-created-before-commerce-version-10021).

Noudattamalla seuraavia ohjeita voit luoda ja konfiguroida mukautetun CPOS-sovelluksen Azure AD:ssa.

1. Kirjaudu [Azure Active Directory -hallintakeskukseen](https://aad.portal.azure.com) mitä tahansa Azure AD -käyttäjätiliä käyttäen. Käyttäjätilillä ei tarvitse olla järjestelmänvalvojan käyttöoikeuksia.
1. Valitse **Azure Active Directory**.
1. Valitse **Sovelluksen rekisteröinnit** ja avaa sovelluksen **Sovelluksen rekisteröinti** -valintaikkunassa valitsemalla **Uusi rekisteröinti**.
1. Määritä seuraavat kentät:

    - **Nimi** – Anna sovelluksen nimi. Kirjoita esimerkiksi **Mukautettu Cloud POS**.
    - **Tuetut tilityypit** – Valitse oletusasetus **Vain tämän organisaation hakemiston tilit (Vain Microsoft - Yksittäinen vuokraaja)**.
    - **Uudelleenohjauksen URI** – Valitse avattavasta luetteloruudusta **Yhden sivun sovellus (SPA)** ja kirjoita CPOS URI.
    - **Palvelupuun tunniste** – Tämä kenttä ei ole pakollinen. Jätä se tyhjäksi.

1. Valitse **Rekisteröi**. Näkyviin tulee juuri rekisteröidyn sovelluksen konfigurointisivu.
1. Määritä **Luettelo**-osassa **oauth2AllowIdTokenImplicitFlow**- ja **oauth2AllowImplicitFlow**-parametrien arvoksi **tosi** ja valitse sitten **Tallenna**.
1. Lisää kaksi väitettä noudattamalla seuraavia ohjeita **Tunnuksen määritys** -osassa:

    1. Valitse **Lisää valinnainen väite**. Määritä **Tunnuksen tyyppi** -kentän arvoksi **Tunnus** ja valitse sitten **sid**-väite. Valitse **Lisää**.
    1. Valitse **Lisää valinnainen väite**. Määritä **Tunnuksen tyyppi** -kentän arvoksi **Käyttöoikeudet** ja valitse sitten **sid**-väite. Valitse **Lisää**.

1. Valitse **API-käyttöoikeudet**-osassa **Lisää käyttöoikeus**.
1. Etsi **Organisaationi käyttämät API:t** -välilehdessä Retail Server -sovellus, jonka loit [Mukautetun Retail Server -sovelluksen määrittäminen Azure AD:ssä](#set-up-a-custom-retail-server-app-in-azure-ad) -osassa. Valitse sitten **Lisää käyttöoikeudet**.
1. Tee **Yleiskuvaus**-osassa huomautus **Sovelluksen (asiakasohjelman) tunnus** -kentän arvosta.

### <a name="upgrade-an-existing-custom-cpos-azure-ad-app-created-before-commerce-version-10021"></a>Ennen Commerce-versiota 10.0.21 luodun mukautetun CPOS Azure AD -sovelluksen päivittäminen

Jos haluat päivittää ennen Commerce-versiota 10.0.21 luodun mukautetun CPOS Azure AD -sovelluksen, noudata näitä ohjeita. 

1. Avaa mukautettu CPOS Azure AD -sovelluksesi Azure-portaalissa.
1. Valitse **Todennus**-välilehti.
1. Kopioi alkuperäinen uudelleenohjauksen URI-osoite **Verkko**-tyypistä, tallenna se myöhempää käyttöä varten ja poista se.
1. Valitse **Lisää ympäristö** ja valitse sitten **Yhden sivun sovellus (SPA)**.
1. Lisää yllä kopioitu alkuperäinen verkon uudelleenohjauksen URI-osoite SPA-ympäristöön.
1. Lisää kaksi väitettä noudattamalla seuraavia ohjeita **Tunnuksen määritys** -osassa:
    1. Valitse **Lisää valinnainen väite**. Määritä **Tunnuksen tyyppi** -kentän arvoksi **Tunnus** ja valitse sitten **sid**-väite. Valitse **Lisää**.
    1. Valitse **Lisää valinnainen väite**. Määritä **Tunnuksen tyyppi** -kentän arvoksi **Käyttöoikeudet** ja valitse sitten **sid**-väite. Valitse **Lisää**.

## <a name="update-the-cpos-configuration-file"></a>Päivitä CPOS-konfiguraatiotiedosto

Avaa CPOS config.json -tiedosto ja tee seuraavat päivitykset tiedostoon.

1. Korvaa **AADClientId**-avainarvo mukautetun CPOS-sovelluksen **Sovelluksen (asiakasohjelman) tunnus** -arvolla, jonka olet luonut [Mukautetun CPOS-sovelluksen asetukset Azure AD:ssä](#set-up-a-custom-cpos-app-in-azure-ad) -osassa.
1. Korvaa **AADRetailServerResourceId**-avainarvo mukautetun Retail Server -sovelluksen **Sovelluksen tunnuksen URI** -arvolla, jonka olet luonut [Mukautetun Retail Server -sovelluksen määrittäminen Azure AD:ssä](#set-up-a-custom-retail-server-app-in-azure-ad) -osassa.

CPOS käyttää molempia parametreja, kun se lähettää pyyntöjä Azure AD:hen suojaustunnuksen hankkimiseksi.

## <a name="update-identity-providers-settings-in-commerce-headquarters"></a>Commerce headquartersin tunnistetietojen toimittajien asetusten päivittäminen

Seuraavaksi pitää päivittää Commerce headquartersin tunnistetietojen toimittajien asetukset.

1. Avaa Commerce headquartersissa **Kaupankäynnin yhteiset parametrit** -sivu.
1. Valitse **Tunnistetietojen toimittajat** -välilehden **Tunnistetietojen toimittajat** -osassa rivi,jossa **Tyyppi**-kentän arvona on **Azure Active Directory** ja **Myöntäjä**-kenttä osoittaa Azure AD -vuokraajaan. Tämä asetus ilmoittaa, että käytät aliruudukoita, jotka sisältävät Azure AD -vuokraajaasi vastaavaan tunnistetietojen toimittajaan liittyvät tiedot.
1. Lisää rivi valitsemalla **Liittyvät osapuolet** -osasta **Lisää**.
1. Määritä seuraavat kentät:

    - **ClientId** – Lisää mukautetun CPOS-sovelluksen **Sovelluksen (asiakasohjelman) tunnus** -arvo, jonka olet luonut [Mukautetun CPOS-sovelluksen asetukset Azure AD:ssä](#set-up-a-custom-cpos-app-in-azure-ad) -osassa.
    - **Tyyppi** – Valitse **Julkinen**.
    - **UserType** – Valitse **Työntekijä**.

1. Valitse lisäämäsi rivi. **Liittyvät osapuolet** -osan alapuolella olevassa **Palvelimen resurssitunnukset** -osassa on Retail Server -sovelluksen tunnukset, joita voidaan käyttää **Liittyvät osapuolet** -ruudukossa valitsemassasi sovelluksessa.
1. Lisää rivi valitsemalla **Palvelimen resurssitunnukset** -osasta **Lisää**.
1. Kirjoita **Palvelimen resurssitunnus** -kenttään mukautetun Retail Server -sovelluksen **Sovelluksen tunnuksen URI** -arvo, jonka olet luonut [Mukautetun Retail Server -sovelluksen määrittäminen Azure AD:ssä](#set-up-a-custom-retail-server-app-in-azure-ad) -osassa.

    > [!IMPORTANT]
    > Kaikissa edellisissä vaiheissa mainituissa kentissä kirjainkoolla on merkitystä. Syötettyjen arvojen on vastattava täsmälleen arvoja, jotka on määritetty Azure AD -hallintakeskuksessa.

1. Siirry kohtaan **Retail ja Commerce IT \> Jakeluaikataulu** ja suorita työ **1110** (**Yleinen konfiguraatio**) -työ.

Voit nyt aktivoida CPOS-laitteet oman Azure AD -sovelluksesi avulla.

## <a name="additional-resources"></a>Lisäresurssit

[Myyntipisteen (POS) laitteen aktivointi](dev-itpro/retail-device-activation.md)

[Aktivointitilien hallinta ja laitteiden vahvistaminen](set-up-activation-accounts-validate-devices-hq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
