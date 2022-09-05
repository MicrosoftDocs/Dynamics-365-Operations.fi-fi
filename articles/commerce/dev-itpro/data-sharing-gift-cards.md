---
title: Yritysten välisten tietojen jakaminen lahjakortteja varten
description: Tässä artikkelissa kuvaillaan, kuinka Microsoft Dynamics 365 Commerce määritetään käyttämään Dynamics 365 Finance -tietojen jakamistoimintoa tietoalueiden välillä lahjakorttitietojen synkronoimista varten.
author: BrianShook
ms.date: 08/26/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: b56890b546c3cd74b75cf447e62495733ea8d288
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387065"
---
# <a name="cross-company-data-sharing-for-gift-cards"></a>Yritysten välisten tietojen jakaminen lahjakortteja varten

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tässä artikkelissa kuvaillaan, kuinka Microsoft Dynamics 365 Commerce määritetään käyttämään Dynamics 365 Finance -tietojen jakamistoimintoa tietoalueiden välillä lahjakorttitietojen synkronoimista varten. Tietueiden jakamista voidaan tämän jälkeen käyttää tietojen jakamiseen yritysten välillä kahden tietoalueen välillä. Näin Commercen sisäinen lahjataulu voi jakaa tietoja kahden yritysentiteetin välillä. Lisätietoja Dynamics 365 Finance -ohjelman yritysten välisestä tietojen jakamisesta on kohdassa [Yritysten välinen tietojen jakaminen](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

## <a name="key-terms"></a>Tärkeimmät termit

| Kausi | Kuvaus |
|---|---|
| Yritys | Yritys Dynamics 365 Finance -ympäristössä. |
| Lahjakortti | Sisäinen Dynamics 365 Commerce -lahjakorttituote. |

## <a name="prerequisites"></a>Edellytykset

Käyttäjien on määritettävä ympäristönsä yritystenvälistä tietojen jakamista varten kohdassa [Yritysten välinen tietojen jakaminen](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing) kuvatulla tavalla.

**RetailGiftCardTable** -taulun **DataSharingType** -kentän arvon on oltava **Kaksoiskappale** tietueiden kaksoiskappaleiden jakamisen (DRS) ottamiseksi käyttöön lahjakorttitaululle. Lisätietoja on kohdassa [Yritysten välinen tietojen jakaminen kehittäjille](/dynamics365/fin-ops-core/dev-itpro/sysadmin/drs-srs-dev).

## <a name="configure-cross-company-data-sharing-for-gift-cards"></a>Yritysten välisten tietojen jakamisen määrittäminen lahjakortteja varten

Yritysten välisten tietojen jakamisen määrittäminen lahjakortteja varten tapahtuu seuraavia vaiheita seuraamalla.

1. Valitse Commerce headquartersissa **Järjestelmänhallinta\> Asetukset \> Määritä yritysten välinen tietojen jakaminen**.
1. Lisää uusi tietojenjakamistietue valitsemalla toimintoruudusta **Uusi**.
1. Kirjoita **Nimi**-kenttään tietojen jakamistietueen nimi (esimerkiksi **Lahjakortit**).
1. Valitse **Jaettavat taulut ja kentät** -osasta **Lisää**.
1. Kirjoita **Jaa uusi taulu** -valintaikkunan **Taulun nimi** -kenttään **RETAILGIFTCARDTABLE** (vähittäismyynnin lahjakorttien taulu). **Taulun otsikko** -kentän arvoksi tulee määrittyä automaattisesti **Lahjakorttitaulu**.
1. Varmista, että **Tallenna tiedot yrityskohtaisesti** -, **Onko yksilöivä indeksi** - ja **Ei vielä jaettu** -valintaruudut on valittu. Näiden valintaruutujen valitseminen käynnistää tietojen jakamistoimintoon liittyvät oikeellisuustarkistukset.
1. Valitse **Lisää taulu**. **Lahjakorttitaulu (RetailGiftCardTable)** -tietueen tulisi nyt näkyä kohdan **Jaettavat taulut ja kentät** alla. Valitse caret-merkki (^), jos haluat tarkastella kaikkia taulun kenttiä, jotka liittyvät automaattisesti tauluun jakamista varten.
1. Valitse **Yritykset , jotka jakavat näiden taulujen tietueet** -osassa **Lisää**, kun haluat lisätä yrityksen, jonka kanssa tietoja jaetaan.
1. Valitse yritys **Yritys**-kohdan alla olevalta riviltä avattavasta luettelosta.
1. Kirjoita **Nimi**-kenttään yrityksen nimi.
1. Voit lisätä yritysrivejä toistamalla kohtien 8–10 toimet.
1. Kun olet lisännyt yritysrivit, valitse toimintoruudusta **Ota käyttöön**.
1. Näyttöön tulee varoitussanoma, jossa todetaan, että "On suositeltavaa suorittaa tämä toimenpide työajan ulkopuolella". Samanaikaiset tapahtumatoiminnot epäonnistuvat käytännön taulujen osalta. Haluatko jatkaa?" Suostu valitsemalla **Kyllä**.
1. Saat varoitusilmoituksen, jossa sanotaan: "Haluatko kopioida kaikki nykyiset tiedot kaikkien jaettujen yritysten kesken nyt?" Suostu valitsemalla **Kyllä**.

Kun hyväksyt molemmat sanomat, taulut alkavat kopioida tietoja konfiguroitujen yritysten välillä. Tällöin yhdessä yrityksen lahjakortissa esiintyvät saldot näkyvät myös toiselle yritykselle.

## <a name="additional-resources"></a>Lisäresurssit

[Maksut – usein kysytyt kysymykset](payments-retail.md)

[Kassamoduuli](../add-checkout-module.md)

[Maksumoduuli](../payment-module.md)
