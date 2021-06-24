---
title: Regulatory Configuration Service
description: Tämä ohjeaihe sisältää yhteenvedon Regulatory Configuration Servicen (RCS) ominaisuuksista ja tietoja palvelun käytön ominaisuudesta.
author: JaneA07
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 7f946988f124c814452e1774c700d5c7354f39b0
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216559"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

Regulatory Configuration Service (RCS) on erillinen suunnittelu- ja elinkaaren hallintapalvelu, jossa ei ole koodia tai koodia vähäisen koodin yleistystoimintoa. RCS:n globalisoinnin laajennus ja mukauttaminen laajentavat ja mukauttavat verotuksen, sähköisen laskutuksen, säännösten raportoinnin, pankki- ja liiketoiminta-asiakirjojen tärkeimpiä globalisointialueita ilman kehittäjien apua. Tämä ei-koodia/vähäisen koodin globalisoinnin menetelmä helpottaa ja nopeuttaa globalisointia ja kustannuksien tehokasta luontia tai ulottumista.

RCS tarjoaa seuraavat ominaisuudet:

- Kaikkien sähköisen raportoinnin (ER) toimintojen tuki.
- Uusien globalisoinnin mikropalveluiden konfiguroimisen edellytykset.
- Sähköisen laskutuksen tuki. Lisätietoja kohdassa [Sähköinen laskutus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).
- Veron laskennan tuet. Lisätietoja on kohdassa [Veropalvelu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).
- Tuki uusille globalisointitoiminnon toiminnoille, jotka yksinkertaistavat monikomponentin ominaisuuksien elinkaaren hallintaa, sekä mahdollistaa toimintojen konfiguroinnin ja ominaisuusparametrien määrittämisen lisätoiminnon. Lisätietoja on kohdassa [Regulatory Configuration Service – globalisointipaleluiden yksinkertaisen globalisoinnin ominaisuuksien hallinta](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).
- Tukee keskitettyä julkaisu- ja varastointitilaa sekä mukautettujen konfiguraatioiden jakamista yleisessä tietovarastossa, jotta konfiguroinnin hallintaa voidaan yksinkertaistaa edellyttämättä Microsoft Dynamics Lifecycle Services (LCS) -palveluiden käyttöä.

## <a name="access-rcs"></a>Käytä RCS:ää

Voit rekisteröityä tai kirjautua sisään RCS-palveluun [Regulatory Configuration Service -sivulla](https://marketing.configure.global.dynamics.com/).

![RCS:n rekisteröityminen/sisäänkirjaus](media/202103_RCS%20Marketing%20page_updated_1.jpg)

Tarkista ja hyväksy **Regulatory Configuration Service** -sivulla palvelun käytön lisäehdot ja -ehdot ja valitse sitten jokin seuraavista painikkeista:

- **Rekisteröityminen**, jos olet palvelun ensimmäinen käyttäjä ja käytät yrityksen sähköpostiosoitetta organisaatiosi palveluympäristön järjestämiseen
- **kirjaudu sisään**, jos olet aiemmin rekisteröitynyt palveluun ja haluat käyttää organisaatioympäristöäsi

## <a name="regional-availability"></a>Paikallinen käytettävyys

RCS on yleensä käytettävissä seuraavilla alueilla:

- Yhdysvallat
- Intia
- Ranska
- Eurooppa

Täydellinen luettelo alueista on kohdassa [Dynamics 365 ja Power Platform: Saatavuus, tietojen sijainti, kieli ja lokalisointi](https://aka.ms/dynamics_365_international_availability_deck).

## <a name="rcs-default-company"></a>RCS-oletusyritys

Suunnittele RCS:ssä käytettävät aikatoiminnot, jotka jaetaan kaikille yrityksille. Yrityskohtaisia toimintoja ei ole. Siksi on suositeltavaa käyttää yhtä yritystä (**DAT**) RCS-ympäristössäsi.

Joissakin tilanteissa haluat ehkä kuitenkin ER-muotojen käyttävän tiettyyn yritykseen liittyviä parametreja. Vain näissä tilanteissa on käytettävä oletusyrityksen valitsinta. Katso esimerkiksi: [Sähköisen raportoinnin muotojen määrittäminen käyttämään yrityskohtaisesti määritettyjä parametreja](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).

## <a name="related-rcs-documentation"></a>Aiheeseen liittyviä RCS-asiakirjoja

Katso lisätietoja liittyvistä komponenteista seuraavista aiheista:

- **RCS:**

    - [Sähköisen raportoinnin konfiguraatioiden luominen RCS:ssä ja niiden lataaminen yleiseen säilöön](rcs-global-repo-upload.md)

- **Yleinen säilö:**

    - [Luo ER-konfiguraatio ja lataa global repo -palveluun](rcs-global-repo-upload.md)
    - [Jaa konfiguraatio Global repo -määrityksessä](rcs-global-repo-share-configuration.md)
    - [Parannettu suodatus Global repossa](enhanced-filtering-global-repo.md)
    - [Sähköisen raportoinnin konfiguraatioiden lataaminen Global reposta](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [Määritysten lopettaminen Global repossa](discontinuing-configurations-rcs-global-repo.md)
    - [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) -tallennustilan vanhentuminen](rcs-lcs-repo-dep-faq.md)

- **Globalisaatio-ominaisuus:**

    - [Regulatory configuration service (RCS) – globalisointiominaisuus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a>RCS-rekisteröinnin vianmääritys

Kun rekisteröidyt RCS:ään palvelun sivulta, saatat kohdata Azure Active Directoryyn (Azure AD) liittyvän ongelman. Näyttöön avautuva virhesanoma ilmoittaa, että RCS-rekisteröityminen on poistettuna käytöstä, ja se on otettava käyttöön, ennen kuin rekisteröintiprosessi voidaan suorittaa.

![RCS-rekisteröitymisen virhesanoma](media/01_RCSSignUpError.jpg)

Tämä ongelma ilmenee, koska ad-hoc-tilausten rekisteröityminen on estetty ja `AllowAdHocSubscriptions`-ominaisuus on otettava käyttöön vuokraajassa. 

- Jos IT-osastosi hallitsee organisaatiosi Azure-vuokraajia, ota yhteyttä tähän osastoon ja raportoi ongelma.
- Jos vastaat Azure-vuokraajien hallinnasta, voit korjata ongelmat noudattamalla seuraavia ohjeita: [Azure Active Directory -rekisteröityminen itsepalveluna](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).
