---
title: Meksikon sähköisen laskutuksen lisäosan käytön aloittaminen
description: Tässä aiheessa on tietoja, joiden avulla voit aloittaa Meksikon sähköisen laskutuksen lisäosan käytön Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: a30f5a9b585c826222108563ea10ac4194ee441c
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039819"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-mexico"></a>Meksikon sähköisen laskutuksen lisäosan käytön aloittaminen

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Meksikon sähköisen laskutuksen lisäosa ei välttämättä tällä hetkellä tue kaikkia toimintoja, jotka ovat käytettävissä Comprobante Fiscal Digital por Internet (CFDI) -asiakirjassa tai siihen liittyvässä integroinnissa Microsoft Dynamics 365 Financeen tai Dynamics 365 Supply Chain Managementiin.

Tässä aiheessa on tietoja, joiden avulla voit aloittaa Meksikon sähköisen laskutuksen lisäosan käytön. Se opastaa Regulatory Configuration Servicesin (RCS) ja Financen maakohtaisissa määritysvaiheissa. Saat myös ohjeita siihen, mitä sinun on tehtävä Financessa lähettääksesi CFDI-laskuja palvelulla, ja sinulle selitetään, miten käsittelyn tulokset ja CFDI-laskujen tila arvioidaan.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin suoritat tämän aiheen vaiheet, sinun on suoritettava aiheen [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md) vaiheet.

## <a name="rcs-setup"></a>RCS-asetukset

RCS:n määrityksen aikana suoritat seuraavat tehtävät:

1. Tuo sähköisen laskutuksen toiminto CFDI-laskujen käsittelyyn.
2. Tarkista muotomääritykset, jotka vaaditaan CFID-laskuja koskevien vastausten luomiseen, lähettämiseen ja vastaanottamiseen sekä peruutuksia koskevien vastausten lähettämiseen ja vastaanottamiseen.
3. Määritä tapahtumat, jotka tukevat CFDI-laskun lähetysskenaarioita.
4. Julkaise CFDI-laskujen sähköisen laskutuksen toiminto.

> [!NOTE]
> Sähköisen laskutuksen toiminto on sen resurssin yleinen nimi, joka määritetään ja julkaistaan käytettäväksi sähköisen laskutuksen lisäosan palvelimella. Tässä tapauksessa CFDI-laskut (MX) ovat määritettävä sähköisen laskutuksen toiminto.

## <a name="import-the-e-invoicing-feature"></a>Sähköisen laskutuksen toiminnon tuominen

1. Kirjaudu RCS-tilille.
2. Valitse **Globalisointitoiminnot** -työtila ja **Toiminnot** -kohdan **Sähköinen laskutus** -ruutu.
3. Valitse **Sähköisen laskutuksen toiminnot** -sivulla **Tuo** tuodaksesi **CFDI-laskut (MX)** -toiminnon yleisestä säilöstä.

    > [!NOTE]
    > Jos toiminto ei näy luettelossa, valitse **Synkronoi** ja toista sitten vaihe 3.

![CFDI-laskujen (MX) tuominen](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

Kun tuot **CFDI-laskut (MX)** -toiminnon yleisestä säilöstä, kaikki toiminnon asetukset, kuten määritykset ja toimet, tuodaan myös.

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a>Uuden versoin luominen CFDI-laskujen (MX) toiminnosta

Voit luoda uuden version, jos esimerkiksi URL-osoitteita on päivitettävä. Lisätietoja: [Sähköinen CFDI-laskutus](tasks/mx-00010-e-invoicing-cfdi.md).

- Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot** -välilehdellä **Uusi**.

![Uuden sähköisen laskutuksen toiminnon version lisääminen](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a>Määritysversion päivittäminen

1. Voit hallita määritysversioita (ER-tiedostomuodon määrityksiä) valitsemalla **Sähköisen laskutuksen toiminnot** -sivun **Määritykset** -välilehdessä **Lisää** tai **Poista**.

    ![Sähköisen laskutuksen toimintojen määritysten hallinta](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    Kun luot uuden version, kaikki määritykset periytyvät edellisestä julkaistusta versiosta. CFDI-laskujen käsittelyä varten tarvitaan seuraavat määritykset:

    - CFDI-lasku (BusinessDocumentService)
    - CFDI-vastaussanoman tuonti
    - CFDI-virhelokin tuonti
    - CFDI-peruutuspyyntö (MX) (BusinessDocumentService)
    - CFDI-lasku (BusinessDocumentService)

2. Valitse luettelosta määritysversio ja valitse sitten **Muokkaa** tai **Näytä** avataksesi **Muodon suunnittelija** -sivun, jolla voit muokata tai tarkastella määritystä.

    ![Muodon suunnittelija -sivun avaaminen](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. Käytä **Muodon suunnittelija** -sivua muokataksesi ja tarkastellaksesi ER-muodon tiedostomäärityksiä. Lisätietoja on kohdassa [Sähköisten asiakirjojen määritysten luominen](../../dev-itpro/analytics/electronic-reporting-configuration.md)

    ![Muodon suunnittelutoiminto -sivu](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>Sähköisen laskutuksen toiminnon määritysten hallinta

- Voit hallita sähköisen laskutuksen toiminnon määrityksiä valitsemalla **Sähköisen laskutuksen toiminnot** -sivun **Määritykset** -välilehdessä **Lisää** , **Poista** tai **Muokkaa**.

![Sähköisen laskutuksen toiminnon määritysten hallinta](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

Jos haluat lähettää CFDI-laskuja hyväksyttäväksi (luoda XML-tiedoston, lähettää XML-tiedoston ja käsitellä vastauksen), tarvitaan **Myyntilasku** -toimintomääritys.

CFDI-laskun peruutuksen lähettämiseen vaaditaan toimintomääritykset **Peruutus** ja **Peruuta**.

### <a name="configure-the-sales-invoice-feature-setup"></a>Myyntilaskutoiminnon asetusten määrittäminen

1. Valitse **Sähköisen laskutuksen toiminnot** -sivun **Määritykset** -välilehden **Toiminnon määritys** -sarakkeessa **Myyntilasku**.
2. Määritä toimet, soveltuvuussäännöt ja muuttujat valitsemalla **Muokkaa**.

    ![Sähköisen laskutuksen toiminnon määritysten muokkaaminen](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. Voit hallita toimiluetteloa valitsemalla **Toimintoversion määritys** -sivulla **Toimet** -välilehti. Toimet määrittävät luettelon toiminnoista, jotka on suoritettava peräkkäisessä järjestyksessä, jotta toiminto suoritetaan kokonaisuudessaan.

    ![Toimet-välilehti](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | Toimenpiteen tunnus | Toimenpide                   | Toiminnon nimi                                  | Toiminnon kuvaus                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | 1         | Muunna asiakirja       | Luo sähköinen CFDI-lasku ilman digitaalista allekirjoitusta | Luo sähköinen CFDI-lasku.                                |
    | 2         | Allekirjoita tiedosto            | Digitaalinen allekirjoitus                                 | Allekirjoita sähköinen lasku lähetystä varten digitaalisesti.                |
    | 3         | Kutsu Meksikon PAC-palvelua | Lähetä sähköinen CFDI-lasku                        | Windows Communication Foundation (WCF) -asiakas lähettää sähköisen CFDI-laskun. |
    | 4         | Käsittele vastaus         | Verkkopalvelun vastauksen analysoiminen                 | Analysoi verkkopalvelun vastaus ja palauta virheloki. |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a>Määritä Meksikon PAC-verkkopalvelujen URL-osoite 

1. Valitse **Toimet** -pikavälilehden **Toimet** -välilehden **Toiminnon versiomääritys** -sivulla **Kutsu Meksikon PAC-palvelua**.
2. Syötä **Parametrit** -pikavälilehden **URL-osoitteet** -kenttään CFDI-laskun lähetyksen verkkopalvelun URL-osoite.

> [!NOTE]
> Käytä samoja vaiheita toimintovaiheiden **Peruuta** ja **Peruutuspyyntö** **Kutsu Meksikon PAC-palvelua** -toiminnon URL-osoitteen päivittämiseen.

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a>Luonnosversion määrittäminen sähköisen laskutuksen ympäristölle

1. Valitse **Sähköisen laskutuksen toiminnot** -sivun **Ympäristöt** -välilehdellä **Ota käyttöön**.
2. Valitse ympäristö **Ympäristöt** -kentässä.
3. Valitse **Voimaantulo** -kentässä päivämäärä, jona uusi ympäristö on tarkoitus ottaa käyttöön.
3. Valitse **Ota käyttöön**.

![Sähköisen laskutuksen ympäristön käyttöönotto](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a>Version tilan muuttaminen valmiiksi

1. Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot** -välilehdessä se sähköisen laskutuksen toiminto, jonka tilana on **Luonnos**.
2. Valitse **Muutoksen tila \> Viimeistele**.

## <a name="change-the-version-status-to-published"></a>Version tilan muuttaminen julkaistuksi

- Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot** -välilehdellä **Muuta tilaa \> Julkaise**.

## <a name="publish-the-e-invoicing-feature"></a>Sähköisen laskutuksen toiminnon julkaiseminen

1. Valitse **Sähköisen laskutuksen toiminnot** -sivulla **Versiot** -välilehti hallitaksesi **CFDI-laskut (MX)** -toiminnon tilaa.
2. Muuta toiminnon tilaa valitsemalla **Muuta tilaa**.

![Sähköisen laskutuksen toiminnon tilan muuttaminen](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance"></a>Sähköisen laskutuksen lisäosan integroinnin määritys Financessa

Sähköisen laskutuksen lisäosa määritetään Financessa suorittamalla seuraavat tehtävät:

1. Tuo ER-tietomalli, ER-tietomallin yhdistämismääritys ja CFDI-laskuja varten vaadittavat muodot.
2. Määritä CFDI-laskujen päivityksen vastaustyypit. Näitä vastaustyyppejä käytetään vastaukseen hyväksytyn varmenteentarjoajan (PAC) palvelimelta.

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a>Tuo ER-tietomalli, ER-tietomallin yhdistämismääritys ja CFDI-laskujen kontekstimääritykset

1. Kirjaudu Financeen.
2. Valitse **Sähköisen raportointi** -työtilan **Määrityslähteet** -osassa **Microsoft** -ruutu. Varmista, että tämän määrityspalvelun arvoksi on määritetty **Aktiivinen**. Tietoja palvelun arvon **Aktiivinen** -muotoon määrittämisestä: [Luo määrityspalveluja ja merkitse ne aktiiviseksi](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Valitse **Säilöt**.
4. Valitse **Yleinen resurssi \> Avaa**.
5. Tuo **Laskumalli** , **Laskumallin yhdistämismääritys** , **CFDI-laskun muoto (MX)** , **CFDI-laskun peruutuspyynnön muoto (MX)** sekä **CFDI-laskun peruutusmuoto (MX)**.

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a>CFDI-laskujen käsittelytoiminnon käyttöönotto

1. Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.
2. Valitse **Toiminnot** -välilehdellä **Ota käyttöön** -valintaruutu toimintoviitteiden **MX-00010** ja **MX-00016** riveillä.

![CFDI-laskujen käsittelytoimintojen käyttöönotto](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a>ER-määritysten tuominen ja CFDI-laskujen päivittämisen vastaustyyppien määrittäminen

#### <a name="import-er-configurations"></a>ER-konfiguraatioiden tuominen

1. Valitse **Sähköisen raportointi** -työtilan **Määrityslähteet** -osassa **Microsoft** -ruutu.
3. Valitse **Säilöt**.
4. Valitse **Yleinen resurssi \> Avaa**.
5. Tuo **Vastaussanoman malli** , **CFDI-virhelokin tuonti (MX)** , **CFDI-virhelokin tuonti (MX)** ja **CFDI-vastaussanoman tuonti (MX)**.

#### <a name="set-up-the-response-types"></a>Vastaustyyppien määrittäminen

1. Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.
2. Valitse **Sähköinen asiakirja** -välilehdellä **Lisää**.
3. Siirry asiakkaan laskukirjauskansioon ja valitse projektin lasku sitten **Taulukon nimi** -kentässä.
4. Määritä kullekin taulukolle liittyvä asiakirjakonteksti:

    - Syötä kohtaan **Asiakkaan laskukirjauskansio** **Asiakkaan laskukonteksti**.
    - Syötä kohtaan **Projektilasku** **Projektilaskun konteksti**.

4. Valitsemalla **Vastaustyypit** määrittää vastaustyypit, jotka voidaan palauttaa sähköisen laskutuksen lisäosasta ja lisätä asiakkaan laskukirjauskansioon tai projektilaskuun.
5. Valitse **Uusi** ja sitten **Vastaustyyppi** -kentässä **Vastaus**.
6. Valitse **Lähetystila** -kentässä **Odottaa**.
7. Valitse **Mallin yhdistämismääritys** -kentässä **Vastaussanoman tuontimuoto – mallin yhdistämismääritys vastaussanomasta**.
8. Valitse **Tallenna**.
9. Valitse **Uusi** ja sitten **Vastaustyyppi** -kentässä **ResponseData**.
10. Valitse **Lähetystila** -kentässä **Odottaa**.
11. Valitse **Mallin yhdistämismääritys** -kentässä **CFDI-vastaustietojen tuontimuoto (tiedot) – vastaustietojen tuonti**
12. Valitse **Tallenna**.

## <a name="process-electronic-invoices-in-finance"></a>Sähköisten laskujen käsittely Financessa 

Kun käsittelet CFDI-laskuja Financessa sähköisen laskutuksen lisäosan kautta, voit suorittaa seuraavia tehtäviä:

- CFDI-laskujen lähettäminen.
- Lähetyksen suorituslokien tarkastelu.
- CFDI-laskun peruutuksen lähettäminen.

### <a name="submit-cfdi-invoices"></a>CFDI-laskujen lähettäminen

Kun olet ottanut käyttöön **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminnon **Vie/tuo sähköinen lasku** -prosessia ( **Myyntireskontra \> Laskut \> Sähköiset laskut** ) CFDI-laskujen lähettämiseen ei voida enää käyttää. Se korvataan uudella prosessilla, jonka nimi on **Lähetä sähköiset asiakirjat**.

> [!NOTE]
> Ennen kuin käytät uutta **Lähetä sähköisiä asiakirjoja** -prosessia, varmista, että Meksikon sähköisten laskujen edellyttämät määritykset on tehty. Lisätietoja [CFDI-asettelun versio 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).

1. Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Lähetä sähköisiä asiakirjoja**.
2. Kun mikä tahansa asiakirja lähetetään ensimmäistä kertaa, määritä **Lähetä asiakirjat uudelleen** -asetukseksi aina **Ei**. Jos sinun on lähetettävä asiakirja uudelleen palvelun kautta, määritä asetukseksi **Kyllä**.
3. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** avataksesi **Kysely** -valintaruudun, jossa voit muodostaa kyselyn lähetettävien asiakirjojen valitsemista varten.

![CFDI-asiakirjan lähettäminen](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> Kun yrität lähettää asiakirjan palvelun kautta ensimmäisen kerran, järjestelmä pyytää vahvistamaan yhteyden sähköisen laskutuksen lisäosaan. Valitse **Yhdistä sähköisten asiakirjojen lähetyspalveluun napsauttamalla tätä**.

### <a name="view-submission-logs"></a>Lähetyslokien tarkasteleminen

Voit tarkastella kaikkien lähetettyjen asiakirjojen tai vain yhden lähetetyn asiakirjan lähetyslokeja.

#### <a name="view-all-submission-logs"></a>Kaikkien lähetyslokien tarkastelu

Kun olet ottanut **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminnon käyttöön, käytettävissä on uusi sivu, jolla voi seurata asiakirjan lähetysprosessia. Voit käyttää tätä sivua kaikkien lähetettyjen asiakirjojen lähetyslokien tarkasteluun.

1. Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Sähköisen asiakirjan lähetysloki**.
2. Valitse **Asiakirjatyyppi** -kentässä **Asiakkaan laskukirjauskansio** suodattaaksesi vaadittavat sähköiset asiakirjat.

    ![Asiakirjatyypin valinta lähetyslokien tarkastelua varten](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. Valitse toimintoruudussa **Kyselyt \> Lähetystiedot** tarkastellaksesi lähetyksen toteutuslokien tietoja.

    ![Lähetyslokitietojen tarkastelu](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

Lähetyslokien tiedot jakautuvat kolmeen pikavälilehteen:

- **Käsittelytoimet** – Tässä pikavälilehdessä näkyy RCS:ssä määritetyssä toimintoversiossa määritettyjen toimien suoritusloki. **Tila** -sarakkeessa näkyy, suoritettiinko toimi onnistuneesti.
- **Toimitiedostot** – Tässä pikavälilehdessä näkyvät välitiedostot, jotka luotiin toimien suorittamisen aikana. Voit ladata tiedoston ja tarkastella sitä valitsemalla **Näytä**.
- **Käsittelytoimen loki** – Tässä pikavälilehdessä näkyvät sähköisen laskutuksen lisäosan ja kohteena olevan verkkopalvelun välisen tiedonsiirron tulokset. Siinä näkyy myös, mitä verkkopalvelun käsittely palautti. **Virhekoodi** -sarakkeessa näkyy palautuskoodi, jonka hyväksynnän verkkopalvelu palautti.

Kun lähetetty CFDI-lasku on hyväksytty, sen tilaksi päivitetään **Hyväksytty**.

#### <a name="view-submission-logs-from-cfdi-invoices"></a>CFDI-laskujen lähetyslokien tarkastelu

Kun otat **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminnon käyttöön, voit myös tarkastella CFDI-laskujen lähetyslokeja.

1. Siirry kohtaan **Myyntireskontra \> Kyselyt ja raportit \> CFDI (sähköiset laskut)**.
2. Valitse CFDI-lasku, joka on lähetetty sen jälkeen, kun **Määritettävä sähköisen laskutuksen lisäosan integrointi** on otettu käyttöön.
3. Valitse toimintoruudun **Historia** -välilehdessä **Sähköisen asiakirjan loki**.

![CFDI-laskujen lähetyslokien tarkastelu](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> **Historia** -painike on käytettävissä sellaisten CFDI-laskujen osalta, jotka on lähetetty, ennen kuin **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminto otettiin käyttöön. **Historia** -painike ei ole käytettävissä sellaisten CFDI-laskujen osalta, jotka on lähetetty sen jälkeen, kun **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminto otettiin käyttöön.

### <a name="submit-cancellation-of-cfdi-invoices"></a>CFDI-laskujen peruutuksen lähettäminen

Kun olet ottanut **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminnon käyttöön, vanhaa CFDI-laskujen peruutusprosessia ei voi enää käyttää. Se korvataan uudella peruutusprosessilla, joka on upotettu **Sähköisen asiakirjan lähetysloki** -sivulle.

1. Siirry kohtaan **Myyntireskontra \> Kyselyt ja raportit \> CFDI (sähköiset laskut)**.
2. Jos CFDI-laskun tila on **Hyväksytty** , valitse **Funktiot \> Peruuta CFDI**.
3. Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Sähköisen asiakirjan lähetysloki**.
4. Valitse CFDI-lasku ja valitse sitten **Funktiot \> Lähetä liittyvät lähetykset**.
5. Kirjoita liittyvän lähetyksen kuvaus ja valitse sitten **OK**.

#### <a name="view-cancellation-submission-logs"></a>Peruutusten lähetyslokien tarkastelu

1. Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Sähköisen asiakirjan lähetysloki**.
2. Valitse **Asiakirjatyyppi** -kentässä **Asiakkaan laskukirjauskansio** suodattaaksesi vain asiakkaan laskukirjauskansion asiakirjoja.
3. Valitse CFDI-lasku ja valitse sitten toimintoruudussa **Kyselyt \> Liittyvä lähetys**.

    **Liittyvät lähetykset** -sivulla näkyvät kaikki liittyvät lähetykset ja niiden lähetystila tietyn CFDI-laskun osalta. Seuraavassa kuvassa ensimmäinen rivi edustaa lähetystä, joka pyysi CFDI-laskun hyväksymistä. Toinen rivi vastaa edustaa lähetystä, joka peruutti CFDI-laskun.

    ![Peruutusten lähetyslokien tarkastelu](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. Valitse toimintoruudussa **Kyselyt \> Lähetystiedot** tarkastellaksesi lähetyksen toteutuslokien tietoja.

    ![Peruutusten lähetyslokitietojen tarkastelu](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a>Tietosuojatiedot
Toimintojen MX-00010 ja MX-00016 (CFDI-lasku ja CFDI-peruutus) käyttöönotto saattaa edellyttää rajoitettujen tietojen, organisaation verorekisteritunnus mukaan luettuna, lähettämistä. Ne välitetään kolmannen osapuolen virastoille, jotka veroviranomaiset ovat hyväksyneet sähköisten laskujen kyseiselle veroviranomaiselle lähettämistä varten siinä esimääritetyssä muodossa, jota integrointi valtion verkkopalveluun edellyttää. Järjestelmänvalvoja voi ottaa toiminnot MX-00010 ja MX-00016 (CFDI-lasku ja CFDI-peruutus) käyttöön ja poistaa ne käytöstä siirtymällä kohtaan **Organisaation hallinta \> Määritykset \> Sähköisten asiakirjojen parametrit**. Valitse **Toiminnot** -välilehti, valitse toiminnot MX-00010 ja MX-00016 sisältävät rivit ja tee sitten haluamasi valinta. Näistä ulkoisista järjestelmistä tähän Dynamics 365 -verkkopalveluun tuotuihin tietoihin sovelletaan [tietosuojalausuntoamme](https://go.microsoft.com/fwlink/?LinkId=512132). Katso lisätietoja maakohtaisten toimintodokumentaatioiden tietosuojaosista.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen laskutuksen yleiskatsaus](e-invoicing-service-overview.md)
- [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md)
- [Sähköisen laskutuksen lisäosan määrittäminen](e-invoicing-setup.md)
