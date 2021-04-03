---
title: Egyptin sähköisen laskutuksen lisäosan käytön aloittaminen
description: Tässä aiheessa on tietoja, joiden avulla voit aloittaa Egyptin sähköisen laskutuksen lisäosan käytön Financessa ja Supply Chain Managementissa.
author: gionoder
manager: AnnBe
ms.date: 02/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 68ee08226f440e850a080600dbf5e16768b45e43
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592595"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-egypt"></a>Egyptin sähköisen laskutuksen lisäosan käytön aloittaminen

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Tässä aiheessa on tietoja, joiden avulla voit aloittaa Egyptin sähköisen laskutuksen lisäosan käytön. Ohjeaihe ohjaa sinua niissä konfigurointivaiheissa, jotka ovat maa-/aluekohtaisia Regulatory Configuration Services (RCS) -palveluissa ja täydentävät seuraavassa ohjeaiheessa kuvattuja vaiheita: [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Sähköisen laskutuksen maakohtainen konfigurointi Egyptin sähköinen laskutus (EG) -ominaisuudelle

Konfiguroidaksesi Egyptin sähköisen laskutuksen (EG) ominaisuuden, tässä on joitakin suoritettavia vaiheita. Osa konfiguraatioiden parametreista julkaistaan oletusarvoilla, joten ne on tarkistettava ja päivitettävä liiketoimintaasi sopiviksi.

### <a name="prerequisites"></a>Edellytykset

Ennen kuin tämän osan menettelyn voi suorittaa, edellytetään seuraavaa:

- Luo digitaalisen sertifikaatin salasana, joka on kuvattu ohjeaiheen **Luo digitaalisen sertifikaatin salasana** -osassa ohjeessa [Sähköisen laskutuksen lisäpalvelun hallinnan käytön aloittaminen](e-invoicing-get-started-service-administration.md). Testitarkoituksia varten Egyptin veroviranomainen antaa erityisiä digitaalisia sertifikaatteja, joita on käytettävä vain testaus- ja ratkaisutarkistuksen vaiheiden aikana. Lisätietoja voit konsultoida Egyptin verotusviranomaisen verkkosivustosta käyttäen linkkiä paketista [Egyptin e-laskutuksen SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).
- Luo organisaatiollesi Egyptin sähköisen laskutuksen (EG) toiminto, kuten on kuvattu ohjeaiheen [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md) **Luo organisaation palveluntarjoajassa sähköisen laskutuksen ominaisuus** -osassa.

1. Valitse RCS:ssä **Globalisaatio-ominaisuudet**-työtilan **Toiminnot**-osassa **Sähköisen laskutuksen lisäosa** -ruutu.
2. Varmista **Sähköisen laskutuksen laajennuksen ominaisuudet** -sivulla, että luomasi sähköisen laskutuksen **Egyptin sähköinen lasku (EG)** -ominaisuus on valittuna.
3. Tarkista **Versiot**-välilehdessä, että **Luonnos**-versio on valittuna.
4. Valitse **Asetukset**-välilehden ruudukosta **Myyntilasku**-toiminnon asetukset.
5. Valitse **Muokkaa** ja valitse **Toiminnot**-välilehden **Toiminnot**-kenttäryhmästä **Allekirjoita JSON-tiedosto Egyptin veroviranomaiselle** -toiminto.
6. Valitse **Parametrit**-kenttäryhmästä parametri **Sertifikaatin nimi** ja valitse sähköisen laskutuksen yhteyteen luodun digitaalisen sertifikaatin nimi.
7. Valitse **Toiminnot**-kenttäryhmästä **Integroi Egyptin ETA-palvelun kanssa**. Toista tämä vaihe kahdelle tämän toiminnon esiintymälle.
8. Valitse **Parametrit**-kenttäryhmästä **Verkkopalvelun URL-osoite** ja **Kirjautumispalvelun URL-osoite** ja tarkista tarvittaessa URL-parametrit. Egyptin verotusviranomaisen verkkosivustosta saat testauksen ja tuotannon URL-osoitteen käyttäen linkkiä paketista [Egyptin e-laskutuksen SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).
9. Valitse **Tallenna** ja sulje sivu.
10. Tietoja sovelluksen asetusten määrittämisestä on kohdassa [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Sovellusmäärityksen sähköisen laskutuksen maakohtainen konfigurointi Egyptin sähköinen laskutus (EG) -ominaisuudelle

Sovellusmäärityksen **Egyptin sähköinen lasku (EG)** -ominaisuuden konfigurointi edellyttää tiettyjen toimien suorittamista. Suorita nämä vaiheet, ennen kuin otat sähköisen laskutusominaisuuden käyttöön sähköisen laskutuksen laajennuksen palveluympäristössä.

### <a name="prerequisites"></a>Edellytykset

Ennen kuin suoritat tämän osan menettelyn, luo ja käynnistä sovellusmäärityksen **Egyptin sähköinen lasku (EG)** -toiminto määrittääksesi **Egyptin sähköinen lasku (EG)** -toiminnon sovellusasetukset, kuten on kuvattu ohjeaiheen [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md) **Sovellusmäärityksen määritys** -osassa.

1. Valitse RCS:ssä **Globalisaatio-ominaisuudet**-työtilan **Toiminnot**-osassa **Sähköisen laskutuksen lisäosa** -ruutu.
2. Varmista **Sähköisen laskutuksen laajennuksen ominaisuudet** -sivulla, että sähköisen laskutuksen **Egyptin sähköinen lasku (EG)** -ominaisuus on valittuna.
3. Tarkista **Versiot**-välilehdessä, että **Luonnos**-versio on valittuna.
4. Valitse **Asetukset**-välilehden **Sovelluksen asetukset** -vaihtoehto ja valitse **Yhdistetty sovellus** -kentästä sovellus, jossa haluat ottaa käyttöön.
5. Varmista **Taulun nimi** -kentässä, että myyntilaskukirjauskansio on valittu.
6. Valitse **Vastaustyypit** ja valitse sitten **Uusi**.
7. Kirjoita **Vastaustyyppi**-kenttään "Response" ja kirjoita **Kuvaus**-kenttään "Description".
8. Valitse **Lähetystila**-kentässä **Odottaa**.
9. Valitse **Mallin yhdistämismääritys** -kentässä **Mallin yhdistämismääritys vastaussanomasta** ja **(Esiversio) Vastaussanoman tuontimuoto** ja valitse sitten **Tallenna**.
10. Valitse **Uusi** ja syötä sitten **Vastaustyyppi**-kenttään "ResponseData" kiinteänä arvona. Syötä **Kuvaus**-kenttään "Description".
11. Valitse **Lähetystila**-kentässä **Odottaa**.
12. Valitse **Tietoyksikön nimi** -kentässä **Myyntilaskun otsikot V2**.
13. Valitse **Mallin yhdistämismääritys** -kentässä **Egypti – vastaustietojen tuonti** ja **(Esiversio) Egypti – vastaustietojen tuonti** ja valitse sitten **Tallenna**.
14. Lisätietoja sähköisen laskutuksen ominaisuuden käyttöönotosta on kohdassa [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Tietosuojatiedot

**Egyptin sähköinen lasku (EG)** -ominaisuuden käyttöönotto saattaa edellyttää rajoitettujen tietojen, joihin kuuluu organisaation verorekisteritunnus, lähettämistä. Tiedot välitetään kolmannen osapuolen virastoille, jotka veroviranomaiset ovat hyväksyneet sähköisten laskujen kyseiselle veroviranomaiselle lähettämistä varten siinä esimääritetyssä muodossa, jota integrointi valtion verkkopalveluun edellyttää. Järjestelmänvalvoja voi ottaa toiminnon käyttöön ja poistaa sen käytöstä siirtymällä kohtaan **Organisaation hallinta** > **Määritykset** > **Sähköisten asiakirjojen parametrit**. Valitse **Ominaisuudet**-välilehdestä se rivi, joka sisältää **Egyptin sähköinen lasku (EG)** -ominaisuuden, ja tee sitten haluamasi valinta. Näistä ulkoisista järjestelmistä tähän Dynamics 365 -verkkopalveluun tuotuihin tietoihin sovelletaan [tietosuojalausuntoamme](https://go.microsoft.com/fwlink/?LinkId=512132). Katso lisätietoja maakohtaisten toimintodokumentaatioiden tietosuojaosista.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen laskutuksen lisäosan yleiskatsaus](e-invoicing-service-overview.md)
- [Sähköisen laskutuksen lisäosan palvelun hallinnan aloittaminen](e-invoicing-get-started-service-administration.md)
- [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md)
- [Asiakkaiden sähköiset laskut Egyptissä](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
