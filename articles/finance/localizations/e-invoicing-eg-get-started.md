---
title: Sähköinen laskutus (Egypti)
description: Tässä artikkelissa on tietoja, joiden avulla voit aloittaa sähköisen laskutuksen käytön Egyptissä Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: e603bcad4d6dc46bd2594cfdcdf8871eb1f49019
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269498"
---
# <a name="electronic-invoicing-for-egypt"></a>Sähköinen laskutus (Egypti)

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja, joiden avulla voit aloittaa Egyptin sähköisen laskutuksen käytön. Se opastaa Regulatory Configuration Servicesin (RCS) maa-/aluekohtaisissa määritysvaiheissa. Nämä vaiheet täydentävät [Sähköisen laskutuksen määritys](e-invoicing-set-up-overview.md) -kohdassa kuvattuja vaiheita.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit aloittaa tämän artikkelin vaiheita, seuraavien edellytysten on toteuduttava:

- Tutustu sähköiseen laskutukseen, kuten [sähköisen laskutuksen yleiskatsauksessa](e-invoicing-service-overview.md) on kuvattu.
- Rekisteröidy RCS:ään ja määritä sähköinen laskutus. Lisätietoja on seuraavissa aiheissa:

    - [Sähköisen laskutuspalvelun rekisteröityminen ja asentaminen](e-invoicing-sign-up-install.md)
    - [Sähköisen laskutuksen Azure-resurssien määrittäminen](e-invoicing-set-up-azure-resources.md)
    - [Microservices-lisäosan asentaminen Lifecycle Servicesissa](e-invoicing-install-add-in-microservices-lcs.md)
    
- Aktivoi Microsoft Dynamics 365 Finance- tai Dynamics 365 Supply Chain Management -sovelluksen ja sähköisen laskutuspalvelun välinen integrointi [Sähköisen laskutuksen integroinnin aktivointi ja määritys](e-invoicing-activate-setup-integration.md) -kohdassa kuvatulla tavalla.
- Luo digitaalisen sertifikaatin salaisuus Azure Key Vaultissa, ja määritä se kohdassa [Asiakkaan varmenteet ja salaiset koodit](e-invoicing-customer-certificates-secrets.md) kuvatulla tavalla. Testitarkoituksia varten Egyptin veroviranomainen antaa erityisiä digitaalisia sertifikaatteja, joita on käytettävä vain testaus- ja ratkaisutarkistuksen vaiheiden aikana. Lisätietoja voit saada Egyptin verotusviranomaisen verkkosivustosta käyttäen linkkiä paketista [Egyptin e-laskutuksen SDK](https://sdk.invoicing.eta.gov.eg/faq/).

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-feature"></a>Sähköisen laskutuksen maakohtainen konfigurointi Egyptin sähköinen laskutus (EG) -ominaisuudelle

Osa **Egyptin sähköinen lasku (EG) – sähköinen laskutus** -ominaisuuden parametreista julkaistaan oletusarvoilla. Tarkista ja päivitä tarvittaessa arvot liiketoimintasi tarpeisiin sopivaksi, ennen kuin otat sähköisen laskutuksen käyttöön ominaisuuden palveluympäristössä.

1. Tuo **Egyptin sähköinen lasku (EG)** -globalisointiominaisuuden viimeisin versio kohdassa [Ominaisuuksien tuonti yleisestä säilöstä](e-invoicing-import-feature-global-repository.md) kuvatulla tavalla.
2. Luo kopio tuodusta globalisointiominaisuudesta ja valitse sen konfiguraatiopalvelu kohdassa [Globalisointitoiminnon luominen](e-invoicing-create-new-globalization-feature.md) kuvatulla tavalla.
3. Tarkista **Versiot**-välilehdessä, että **Luonnos**-versio on valittuna.
4. Valitse **Asetukset**-välilehden ruudukosta **Myyntilasku, johdettu**-toiminnon asetukset.
5. Valitse **Muokkaa**.
6. Valitse **Käsittelyputki**-välilehden **Käsittelyputki**-osasta **Allekirjoita JSON-tiedosto Egyptin veroviranomaiselle** -toiminto.
7. Valitse **Parametrit**-osassa **Varmenteen nimi** ja valitse sitten luomasi digitaalisen varmenteen nimi.
8. Valitse **Käsittelyputki**-osasta **Integroi Egyptin ETA-palvelun kanssa**. Toista tämä vaihe kahdelle tämän toiminnon esiintymälle.
9. Valitse **Parametrit**-osassa **Verkkopalvelun URL-osoite** ja **Kirjautumispalvelun URL-osoite**. Tarkista sitten URL-parametrit. Egyptin verotusviranomaisen verkkosivustosta saat testauksen ja tuotannon URL-osoitteen käyttäen linkkiä paketista [Egyptin e-laskutuksen SDK](https://sdk.invoicing.eta.gov.eg/faq/).
10. Valitse **Tallenna** ja sulje sivu.
11. Toista vaiheet 4–10 **Projektilasku, johdettu** -ominaisuusasetuksille.

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-application-setup"></a>Sähköisen laskutuksen maakohtainen konfigurointi Egyptin sähköinen laskutus (EG) -sovellusasetukselle

Finance- tai Supply Chain Management -ympäristössä on määritettävä tietyt parametrit. Nämä asetukset voi määrittää jommassakummassa seuraavista paikoista:

- Suoraan Finance- tai Supply Chain Management -ympäristössä. Lisätietoja: [Sähköisen laskutuksen parametrin määritys](e-invoicing-set-up-parameters.md).
- RCS:ssä. Sähköisen laskutuksen ominaisuusasetuksissa voit määrittää kaikki parametrit ja ottaa ne sitten suoraan käyttöön Finance- tai Supply Chain Management -ympäristössä, kun otat sähköisen laskutuksen käyttöön.

Molemmissa vaihtoehdoissa parametrit ovat samat. Jos määrität sähköisen laskutuksen palvelun ensimmäistä toimintoa, suosittelemme, että määrität parametrit RCS:ssä näiden vaiheiden mukaisesti ja otat ne sitten käyttöön liitetyssä sovelluksessa.

> [!NOTE]
> Jotkin sähköiset laskutustoimintoversiot saattavat sisältää ennalta määritetyn joukon Financen tai Supply Chain Managementin sovelluskohtaisia parametreja. Tässä tapauksessa on tarkistettava, että tiedot ovat oikein. Muussa tapauksessa voit määrittää parametrit manuaalisesti.

1. Etsi luomasi **Egyptin sähköinen lasku (EG)** -globalisaatio-ominaisuuden kopio.
2. Tarkista **Versiot**-välilehdessä, että **Luonnos**-versio on valittuna.
3. Valitse **Asetukset** -välilehdessä **Sovelluksen asetukset**.
4. Valitse **Yhdistetyt sovellukset** -kentästä sovellus, jossa haluat ottaa parametrit käyttöön.
5. Luo tietue valitsemalla **Sähköiset tiedostotyypit** -sivulla **Lisää**.
6. Lisää **Taulun nimi** -kenttään **CustInvoiceJour**.
7. Lisää **Konteksti**-kenttään viite **Myyntilaskun konteksti** -määrityksen nimeen. Konfiguraatio on **Myyntilaskun kontekstimalli**.
8. Lisää **Sähköisen asiakirjan määritys**-kenttään viite **Myyntilasku**-määrityksen nimeen. Määritys on **Laskumallin yhdistämismääritys**.
9. Valitse **Tallenna**.
10. Valitse **Vastaustyypit**-sivulla **Lisää**.
11. Anna **Vastaustyyppi**-kentässä **Vastaus**.
12. Anna **Kuvaus**-kenttään arvo **Käsittele vastaus**.
13. Valitse **Lähetystila**-kentässä **Odottaa**.
14. Valitse **Mallin määritys** -kentässä **Vastaussanoman tuonti**. Konfiguraatio on **Egyptin vastaussanoman tuonti (EG)**.
15. Valitse **Tallenna**.
16. Valitse **Lisää**.
17. Anna **Vastaustyyppi**-kentässä **ResponseData**.
18. Anna **Kuvaus**-kenttään arvo **Käsittele vastaustiedot**.
19. Valitse **Lähetystila**-kentässä **Odottaa**.
20. Valitse **Tietoyksikön nimi** -kentässä **SalesInvoiceHeaderV2Entity**.
21. Valitse **Mallin määritys** -kentässä **Vastaustietojen tuonti**. Konfiguraatio on **Egyptin vastaustietojen tuontimuoto (EG)**.
22. Valitse **Tallenna** ja sulje sivu.
23. Sulje sivu.

Tietoja toiminnon käyttöönottamisesta palveluympäristössä ja sovelluksen määrityksestä yhdistetyssä Finance- tai Supply Chain Management -sovelluksessa on kohdassa [Globalisaatiotoiminnon viimeisteleminen, julkaiseminen ja käyttöönottaminen](e-invoicing-complete-publish-deploy-globalization-feature.md)

## <a name="privacy-notice"></a>Tietosuojatiedot

**Egyptin sähköisen laskun (EG)** ottaminen käyttöön saattaa edellyttää, että rajoitetut tiedot lähetetään. Tietoihin sisältyy organisaation verorekisteröintitunnus. Tiedot välitetään kolmannen osapuolen virastoille, jotka veroviranomaiset ovat hyväksyneet sähköisten laskujen kyseiselle veroviranomaiselle lähettämistä varten siinä esimääritetyssä muodossa, jota integrointi valtion verkkopalveluun edellyttää. Järjestelmänvalvoja voi ottaa toiminnon käyttöön ja poistaa sen käytöstä siirtymällä kohtaan **Organisaation hallinta** \> **Määritykset** \> **Sähköisten asiakirjojen parametrit**. Valitse **Ominaisuudet**-välilehdestä se rivi, joka sisältää **Egyptin sähköinen lasku (EG)** -ominaisuuden, ja tee sitten haluamasi valinta. Ulkoisista järjestelmistä tähän Dynamics 365 -verkkopalveluun tuotuihin tietoihin sovelletaan [tietosuojalausuntoamme](https://go.microsoft.com/fwlink/?LinkId=512132). Katso lisätietoja maa-/aluekohtaisten toimintodokumentaatioiden tietosuojaosista.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen laskutuksen yleiskatsaus](e-invoicing-service-overview.md)
- [Sähköisen laskutuksen palvelun hallinnan aloittaminen](e-invoicing-get-started-service-administration.md)
- [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md)
- [Asiakkaiden sähköiset laskut Egyptissä](emea-egy-e-invoices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
