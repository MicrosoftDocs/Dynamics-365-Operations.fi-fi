---
title: Azure Active Directory -todennuksen käyttöönotto myyntipisteen sisäänkirjauksessa
description: Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 Commercen myyntipisteen sisäänkirjauskokemus määritetään käyttämään Azure Active Directory -todennusta.
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d6073a04814adf8237b4caa952b31b011f4b34bf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982737"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a>Azure Active Directory -todennuksen käyttöönotto myyntipisteen sisäänkirjauksessa
[!include [banner](includes/banner.md)]


Useat Microsoft Dynamics 365 Commercea käyttävät asiakkaat käyttävät myös muita Microsoftin pilvipalveluita. He voivat hallita näiden palveluiden käyttäjän tunnistetietoja Azure Active Directoryn (Azure AD) avulla. Näissä tapauksissa asiakkaat saattavat haluta käyttää samaa Azure AD -tiliä kaikissa sovelluksissa. Tässä ohjeaiheessa kerrotaan, miten Commercen myyntipisteen sisäänkirjauskokemus määritetään käyttämään Azure AD -todennusta.

## <a name="configure-azure-ad-authentication"></a>Azure AD -todennuksen määrittäminen

Jos haluat määrittää Azure AD:n todennusmenetelmäksi myymälän myyntipisteen sisäänkirjauksessa, määritä myymälän toimintoprofiilin asetukset ja ota ne sitten käyttöön myyntipisteen asiakassovelluksissa.

Määritä uusi toimintoprofiili seuraavasti.

1. Siirry kohtaan **Retail ja Commerce** \> **Kanavan asetukset** \> **POS-asetukset** \> **POS-profiilit** \> **Toimintoprofiilit**.
1. Valitse muutettava toimintoprofiili.
1. Muuta **Toiminnot**-pikavälilehden **Myyntipisteen henkilöstön sisäänkirjaus** -osassa **Sisäänkirjauksen todennusmenetelmä** -kentän arvo **Henkilöstön tunnus ja salasana** -arvosta **Azure Active Directory** -arvoksi.

Oletusarvoisesti kaikki toimintoprofiilit käyttävät myyntipisteen todennusmenetelmänä **Henkilöstön tunnus ja salasana** -arvoa. Tämän vuoksi sinun on muutettava **Sisäänkirjauksen todennusmenetelmä** -kentän arvoa, jos haluat käyttää Azure AD:ta. Tämä muutos vaikuttaa jokaiseen valittuun toimintoprofiiliin linkitettyyn vähittäismyymälään.

Voit ottaa asetukset käyttöön myyntipisteen asiakassovelluksissa seuraavasti.

1. Mene kohtaan **Retail ja Commerce** \> **Retail ja Commerce IT** \> **Jakeluaikataulu**.
1. Suorita **1070** (**Kanavan määritys**) -jakeluaikataulu.

> [!NOTE]
> Azure AD -todennus vaatii Internet-yhteyden. Todennus ei toimi, jos myyntipiste on offline-tilassa.
> 
> **Esimiehen ohitus** -toiminto ei tällä hetkellä tue Azure AD:tä todennusmenetelmänä. Operaattoritunnus ja salasana ovat pakollisia, vaikka Azure AD olisi määritetty myyntipistekirjautumisen todennusmenetelmäksi.

## <a name="associate-an-azure-ad-account-with-a-worker"></a>Azure AD -tilin liittäminen työntekijään

Ennen kuin myymälän työntekijä voi käyttää Azure AD -tiliä myyntipistesovellukseen kirjautumisessa, Azure AD -tili on liitettävä kyseiselle työntekijälle.

Voit liittää Azure AD -tilin työntekijälle seuraavasti.

1. Siirry kohtaan **Vähittäismyynti ja kauppa** \> **Työntekijät** \> **Työntekijät**.
1. Avaa työntekijän tietosivu.
1. Valitse toimintoruudun **Kauppa**-välilehden **Ulkoinen tunnus** -ryhmässä **Liitä aiemmin luotu tunnus**.
1. Valitse **Käytä aiemmin määritettyä ulkoista tunnusta** -valintaikkunassa **Hae sähköpostiosoitteen avulla**, anna Azure AD -sähköpostiosoite ja valitse **Hae**.
1. Valitse palautettu Azure AD -tili ja valitse sitten **OK**.

Työntekijän tietosivun **Alias**, **Täydellinen käyttäjätunnus**- ja **Ulkoinen alitunnus** -kentät **Kauppa**-välilehdessä täytetään.

> [!NOTE]
> Kun työntekijän tietue on päivitetty esimerkiksi uuden Azure AD -tilin liittämisen, salasanan muuttamisen tai työntekijän osoitekirjan päivittämisen vuoksi, on suositeltavaa suorittaa **1060** (**Henkilöstö**) -jakeluaikataulu ja synkronoida uusimmat henkilöstötiedot kanavaan. Näin myyntipistesovellus voi hakea oikeat tiedot käyttäjän valtuutusta ja valtuutuksen tarkistusta varten.

## <a name="additional-resources"></a>Lisäresurssit

[Laajennetun MPOS- ja pilvimyyntipistekirjautumisen määrittäminen](extended-logon.md)

[Vähittäismyynnin toimintoprofiilin luominen](retail-functionality-profile.md)

[Työntekijän konfiguroiminen](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
