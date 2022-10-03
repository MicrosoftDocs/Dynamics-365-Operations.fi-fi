---
title: Ranskan sähköisen laskutuksen lisäosan käytön aloittaminen
description: Tässä artikkelissa on tietoja, joiden avulla voit aloittaa Ranskan sähköisen laskutuksen lisäosan käytön.
author: dkalyuzh
ms.date: 07/07/2022
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-00-02
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: 3ac4af8c131e35d9a499d0d558c7cce1d4872b37
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573275"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-france"></a>Ranskan sähköisen laskutuksen lisäosan käytön aloittaminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja, joiden avulla voit aloittaa Ranskan sähköisen laskutuksen käytön. Se opastaa Regulatory Configuration Servicesin (RCS) maa-/aluekohtaisissa määritysvaiheissa. Nämä vaiheet täydentävät [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md) -kohdassa kuvattuja vaiheita.

## <a name="country-specific-configuration-for-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Sähköisen laskutuksen maakohtainen konfigurointi Ranskan Chorus Pron lähetys (FR) – sähköinen laskutus -ominaisuudelle

Joitakin vaiheita tarvitaan **Ranskan Chorus Pron lähetys (FR)** – sähköinen laskutus -ominaisuuden määrittämiseksi. Jotkin määrityksen parametrit julkaistaan oletusarvoilla. Arvot on tarkistettava ja päivitettävä, jotta ne kuvastavat paremmin liiketoimintaasi.

### <a name="prerequisites"></a>Edellytykset

Ennen kuin voit aloittaa tämän artikkelin vaiheita, seuraavien edellytysten on toteuduttava:

- Tutustu sähköiseen laskutukseen. Lisätietoja kohdassa [Sähköisen laskutuksen yleiskatsaus](e-invoicing-service-overview.md).
- Rekisteröidy RCS:ään ja määritä sähköinen laskutus. Lisätietoja on seuraavissa artikkeleissa:

    - [Sähköisen laskutuspalvelun rekisteröityminen ja asentaminen](e-invoicing-sign-up-install.md)
    - [Sähköisen laskutuksen Azure-resurssien määrittäminen](e-invoicing-set-up-azure-resources.md)
    - [Microservices-lisäosan asentaminen Lifecycle Servicesissa](e-invoicing-install-add-in-microservices-lcs.md)
    - [Sähköisen laskutuksen integroinnin aktivointi ja määritys](e-invoicing-activate-setup-integration.md) – Tämän artikkelin tiedoilla voit aktivoida integroinnin Microsoft Dynamics 365 Financen tai Dynamics 365 Supply Chain Management -sovelluksen ja sähköisen laskutuksen välillä.
    - [NAF-koodit ja siret-numerot](emea-fra-naf-codes-siret-numbers.md) ja [Määritä NAF-koodit ja siret-numerot](tasks/fr-00003-naf-codes-siret-numbers.md) – Näiden artikkelien tietojen avulla voit määrittää yrityksille NAF-koodit ja Siret-numerot. 

- Organisaatiosi on rekisteröidyttävä, jotta se voi käyttää Chorus Prota. Microsoft tarjoaa integroinnin Chorus pron kanssa OAuth2 Modessa ohjelmointirajapinnan kautta. [Virallisessa dokumentaatiossa](https://communaute.chorus-pro.gouv.fr/documentation/help-for-api-developers-in-oauth2-mode/) on yksityiskohtaisia tietoja Chorus Pro -rekisteröinnistä ja sovelluksen aktivoinnista.

    Rekisteröidy Chorus Prohon näiden ohjeiden avulla.

    1. Aloita rekisteröintisi [PISTE-portaalissa](https://piste.gouv.fr/en/component/apiportal/registration). 
    2. Rekisteröi sovellus ja ota käyttöön OAuth (Open Authorization) -tunnistetiedot.
    3. Kopioi ja tallenna OAuth-tunnistetietojen työasematunnus ja salainen avain. Näitä tietoja käytetään myöhemmin.
    4. Rekisteröityäksesi siirry [Chorus Pro -portaaliin](https://portail.chorus-pro.gouv.fr/aife_csm/?id=aife_enrollment). 
    5. Luo tekninen tili ohjelmointirajapinnan käyttöä varten. Lisätietoja on [Teknisen tilin luominen ohjelmointirajapinnan käyttöä varten tuotannossa](https://communaute.chorus-pro.gouv.fr/documentation/creation-of-a-technical-account-for-an-api-access-in-production/).
    6. Kopioi teknisen tilin käyttäjätunnus ja salasana. Näitä tietoja käytetään myöhemmin.

## <a name="country-specific-configuration-of-the-application-setup-for-the-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Sovellusmäärityksen sähköisen laskutuksen maakohtainen konfigurointi Ranskan Chorus Pron lähetys (FR) – sähköinen laskutus -ominaisuudelle

Osa **Ranskan Chorus Pron lähetys (FR) – sähköinen laskutus** -ominaisuuden parametreista julkaistaan oletusarvoilla. Tarkista ja päivitä tarvittaessa arvot liiketoimintasi tarpeisiin sopivaksi, ennen kuin otat sähköisen laskutuksen käyttöön ominaisuuden palveluympäristössä.

1. Luo salaisia koodeja ja vastaava viittaus niihin Azure Key Vaultissa. Lisätietoja on kohdassa [Asiakkaan varmenteet ja salaiset koodit](e-invoicing-customer-certificates-secrets.md).
2. Tuo **Ranskan Chorus Pron lähetys (FR)** -globalisointiominaisuuden viimeisin versio kohdassa [Ominaisuuksien tuonti yleisestä säilöstä](e-invoicing-import-feature-global-repository.md) kuvatulla tavalla.
3. Luo kopio tuodusta globalisointiominaisuudesta ja valitse konfiguraatiopalvelu. Lisätietoja on kohdassa [Globalisaatio-ominaisuuden luominen](e-invoicing-create-new-globalization-feature.md).
4. Tarkista **Versiot**-välilehdessä, että **Luonnos**-versio on valittuna.
5. Valitse **Asetukset**-välilehden ruudukosta **UBL-myyntilasku, johdettu**-toiminnon asetukset.
6. Valitse **Muokkaa** ja valitse sitten **Käsitellään jaksoa** -välilehden **Käsitellään jaksoa** -osasta **(Esiversio) Integroi ranskalaisen Chorus Pron kanssa** ja toimenpiteen nimi **Ranskan Chorus Pron lähetys**.
7. Valitse **Parametrit**-osan **Asiakastunnuksen salaisen koodin nimi** -kentästä asiakkaan tunnukselle Key Vaultissa luomasi salainen koodi.
8. Valitse **Asiakkaan salasanan salaisen koodin nimi** -kentästä asiakkaan salasanalle Key Vaultissa luomasi salainen koodi.
9. Valitse **Teknisen kirjautumisen salaisen koodin nimi** -kentästä teknisen tilin kirjautumiselle Key Vaultissa luomasi salainen koodi.
10. Valitse **Teknisen salasanan salaisen koodin nimi** -kentästä teknisen tilin salasanalle Key Vaultissa luomasi salainen koodi.
11. Valitse **Käsitellään jaksoa** -välilehden **Käsitellään jaksoa** -osasta **Integroi ranskalaisen Chorus Pron kanssa** ja toimenpiteen nimi **Ranskan Chorus Pron pyynnön tila**.
12. Valitse **Parametrit**-osan **Asiakastunnuksen salaisen koodin nimi** -kentästä asiakkaan tunnukselle Key Vaultissa luomasi salainen koodi.
13. Valitse **Asiakkaan salasanan salaisen koodin nimi** -kentästä asiakkaan salasanalle Key Vaultissa luomasi salainen koodi.
14. Valitse **Teknisen kirjautumisen salaisen koodin nimi** -kentästä teknisen tilin kirjautumiselle Key Vaultissa luomasi salainen koodi.
15. Valitse **Teknisen salasanan salaisen koodin nimi** -kentästä teknisen tilin salasanalle Key Vaultissa luomasi salainen koodi.
16. Valitse **Tallenna** ja sulje sitten sivu.
17. Toista vaiheet 6–16 **UBL-projektilasku, johdettu** -ominaisuuden asetukselle, **UBL, myynnin hyvityslasku, johdettu** -ominaisuuden asetukselle ja **UBL, projektin hyvityslasku, johdettu** -ominaisuuden asetukselle.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen laskutuksen lisäosan yleiskatsaus](e-invoicing-service-overview.md)
- [Sähköisen laskutuksen lisäosan palvelun hallinnan aloittaminen](e-invoicing-get-started-service-administration.md)
- [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md)
