---
title: Egyptin sähköisen laskutuksen käytön aloittaminen
description: Tässä aiheessa on tietoja, joiden avulla voit aloittaa Egyptin sähköisen laskutuksen käytön Financessa ja Supply Chain Managementissa.
author: gionoder
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b25a3489d009a02b45d66d4c3a0271a56a92f5ac
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985622"
---
# <a name="get-started-with-electronic-invoicing-for-egypt"></a>Egyptin sähköisen laskutuksen käytön aloittaminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa on tietoja, joiden avulla voit aloittaa Egyptin sähköisen laskutuksen käytön. Ohjeaihe ohjaa sinua niissä konfigurointivaiheissa, jotka ovat maa-/aluekohtaisia Regulatory Configuration Services (RCS) -palveluissa ja täydentävät seuraavassa ohjeaiheessa kuvattuja vaiheita: [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Sähköisen laskutuksen maakohtainen konfigurointi Egyptin sähköinen laskutus (EG) -ominaisuudelle

Osa **Egyptin sähköinen lasku (EG) – sähköinen laskutus** -ominaisuuden parametreista julkaistaan oletusarvoilla. Tarkista ja päivitä tarvittaessa arvot liiketoimintasi tarpeisiin sopivaksi, ennen kuin otat sähköisen laskutuksen käyttöön ominaisuuden palveluympäristössä.

Tämä os täydentää **Sähköisen laskutuksen maa-/aluekohtainen konfigurointi sähköisen laskutuksen ominaisuudelle** -osaa ohjeaiheessa [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md).

### <a name="prerequisites"></a>Edellytykset

Ennen kuin tämän osan menettelyn voi suorittaa, edellytetään seuraavaa:

- Luo digitaalisen sertifikaatin salasana, joka on kuvattu ohjeaiheen **Luo digitaalisen sertifikaatin salasana** -osassa ohjeessa [Sähköisen laskutuksen hallinnan käytön aloittaminen](e-invoicing-get-started-service-administration.md). Testitarkoituksia varten Egyptin veroviranomainen antaa erityisiä digitaalisia sertifikaatteja, joita on käytettävä vain testaus- ja ratkaisutarkistuksen vaiheiden aikana. Lisätietoja voit konsultoida Egyptin verotusviranomaisen verkkosivustosta käyttäen linkkiä paketista [Egyptin e-laskutuksen SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).

1. Valitse RCS:ssä **Globalisaatio-ominaisuus** -työtilan **Toiminnot**-osassa **Sähköinen laskutus** -ruutu.
2. Varmista **Sähköisen laskutuksen ominaisuudet** -sivulla, että luomasi sähköisen laskutuksen **Egyptin sähköinen lasku (EG)** -ominaisuus on valittuna.
3. Tarkista **Versiot**-välilehdessä, että **Luonnos**-versio on valittuna.
4. Valitse **Asetukset**-välilehden ruudukosta **Myyntilasku**-toiminnon asetukset.
5. Valitse **Muokkaa** ja valitse **Toiminnot**-välilehden **Toiminnot**-kenttäryhmästä **Allekirjoita JSON-tiedosto Egyptin veroviranomaiselle** -toiminto.
6. Valitse **Parametrit**-kenttäryhmästä parametri **Sertifikaatin nimi** ja valitse sähköisen laskutuksen yhteyteen luodun digitaalisen sertifikaatin nimi.
7. Valitse **Toiminnot**-kenttäryhmästä **Integroi Egyptin ETA-palvelun kanssa**. Toista tämä vaihe kahdelle tämän toiminnon esiintymälle.
8. Valitse **Parametrit**-kenttäryhmästä **Verkkopalvelun URL-osoite** ja **Kirjautumispalvelun URL-osoite** ja tarkista tarvittaessa URL-parametrit. Egyptin verotusviranomaisen verkkosivustosta saat testauksen ja tuotannon URL-osoitteen käyttäen linkkiä paketista [Egyptin e-laskutuksen SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).
9. Valitse **Tallenna** ja sulje sivu.
10. Lisätietoja sähköisen laskutuksen ominaisuuden käyttöönotosta palveluympäristössä on kohdassa [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Sovellusmäärityksen sähköisen laskutuksen maakohtainen konfigurointi Egyptin sähköinen laskutus (EG) -ominaisuudelle

Suorita nämä vaiheet, ennen kuin otat sovelluksen määritykset käyttöön yhdistetyssä Finance- tai Supply Chain Management -sovelluksessa.

Tämä osa täydentää **Sovellusetusten maa-/aluekohtainen konfigurointi** -osaa ohjeaiheessa [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md).

1. Valitse RCS:ssä **Globalisaatio-ominaisuus** -työtilan **Toiminnot**-osassa **Sähköinen laskutus** -ruutu.
2. Varmista **Sähköisen laskutuksen ominaisuudet** -sivulla, että sähköisen laskutuksen **Egyptin sähköinen lasku (EG)** -ominaisuus on valittuna.
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
14. Jos haluat ottaa sovelluksen asetukset käyttöön yhdistetyssä Finance- tai Supply Chain Management -sovelluksessa, katso ohjetta [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Tietosuojatiedot

**Egyptin sähköinen lasku (EG)** -ominaisuuden käyttöönotto saattaa edellyttää rajoitettujen tietojen, joihin kuuluu organisaation verorekisteritunnus, lähettämistä. Tiedot välitetään kolmannen osapuolen virastoille, jotka veroviranomaiset ovat hyväksyneet sähköisten laskujen kyseiselle veroviranomaiselle lähettämistä varten siinä esimääritetyssä muodossa, jota integrointi valtion verkkopalveluun edellyttää. Järjestelmänvalvoja voi ottaa toiminnon käyttöön ja poistaa sen käytöstä siirtymällä kohtaan **Organisaation hallinta** > **Määritykset** > **Sähköisten asiakirjojen parametrit**. Valitse **Ominaisuudet**-välilehdestä se rivi, joka sisältää **Egyptin sähköinen lasku (EG)** -ominaisuuden, ja tee sitten haluamasi valinta. Näistä ulkoisista järjestelmistä tähän Dynamics 365 -verkkopalveluun tuotuihin tietoihin sovelletaan [tietosuojalausuntoamme](https://go.microsoft.com/fwlink/?LinkId=512132). Katso lisätietoja maakohtaisten toimintodokumentaatioiden tietosuojaosista.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen laskutuksen yleiskatsaus](e-invoicing-service-overview.md)
- [Sähköisen laskutuksen palvelun hallinnan aloittaminen](e-invoicing-get-started-service-administration.md)
- [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md)
- [Asiakkaiden sähköiset laskut Egyptissä](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
