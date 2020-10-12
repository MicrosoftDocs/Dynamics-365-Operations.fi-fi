---
title: Brasilian sähköisen laskutuksen lisäosan käytön aloittaminen
description: Tässä aiheessa on tietoja, joiden avulla voit aloittaa Brasilian sähköisen laskutuksen lisäosan käytön Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
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
ms.openlocfilehash: 6472672f5d618cc6d100298dd35939afa4c0066d
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835950"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Brasilian sähköisen laskutuksen lisäosan käytön aloittaminen 

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Brasilian sähköisen laskutuksen lisäosa ei tällä hetkellä tue kaikkia toimintoja, jotka ovat käytettävissä veroasiakirjan integroinnissa Microsoft Dynamics 365 Financeen ja Dynamics 365 Supply Chain Managementiin.

Tässä aiheessa on tietoja, joiden avulla voit aloittaa Brasilian sähköisen laskutuksen lisäosan käytön. Se opastaa Regulatory Configuration Servicesin (RCS), Financen ja Supply Chain Managementin maakohtaisissa määritysvaiheissa. Se opastaa myös NF-e-veroasiakirjan (sähköinen veroasiakirjamalli 55) lähettämisessä palvelun kautta ja selittää, miten käsittelyn tulokset ja veroasiakirjojen tila arvioidaan.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin suoritat tämän aiheen vaiheet, sinun on suoritettava aiheen [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md) vaiheet.

## <a name="rcs-setup"></a>RCS-asetukset

RCS:n määrityksen aikana suoritat seuraavat tehtävät:

1. NF-e-veroasiakirjojen sähköisen laskutuksen toiminnon tuonti.
2. Niiden tiedostomuotojen tarkistaminen, joita edellytetään NF-e-veroasiakirjojen hyväksyttäväksi lähettämisessä.
3. Niiden tiedostomuotojen tarkistaminen, joita edellytetään hyväksytyn NF-e-veroasiakirjan peruuttamiseen.
4. Sen tapahtuman määrittäminen, joka vaaditaan NF-e-veroasiakirjojen hyväksyttäväksi lähettämisessä.
5. Sen tapahtuman määrittäminen, jota edellytetään hyväksytyn NF-e-veroasiakirjan peruuttamiseen.
6. Sähköisen laskutuksen toiminnon määrittäminen sähköisen laskutuksen lisäosaympäristölle.
7. Sähköisen laskutuksen toiminnon julkaiseminen.

> [!NOTE]
> Sähköisen laskutuksen toiminto on sen resurssin yleinen nimi, joka määritetään ja julkaistaan käytettäväksi sähköisen laskutuksen lisäosan palvelimella. Sähköisen laskutuksen toiminnon määrityksessä yhdistyvät muun muassa sähköisen raportoinnin (ER) määrityksen muodot määritettävien vienti- ja tuontitiedostojen luomista varten sekä toimintojen ja toimintokulkujen käyttäminen määritettävien pyyntöjen lähettämisen sääntöjen luomiseen, vastausten tuomiseen sekä vastausten sisältöjen jäsentämiseen.

## <a name="import-the-e-invoicing-feature"></a>Sähköisen laskutuksen toiminnon tuominen

1. Kirjaudu RCS-tilille
2. Valitse **Globalisointitoiminnot**-työtila ja **Toiminnot**-kohdan **Sähköinen laskutus** -ruutu.
3. Valitse **Sähköisen laskutuksen toiminnot** -sivulla **Tuo** tuodaksesi NF-e-veroasiakirjan sähköisen laskutuksen toiminnon yleisestä säilöstä.

    ![Tuontipainike](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. Valitse NF-e-veroasiakirjan toiminto ja sitten **Tuo**.

    ![NF-e-toiminnon tuominen](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a>Uuden versoin luominen NF-e-veroasiakirjan toiminnosta

- Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot**-välilehdellä **Uusi**.

![Uuden sähköisen laskutuksen toiminnon version lisääminen](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a>Määritysversion päivittäminen

1. Voit hallita määritysversioita (ER-tiedostomuodon määrityksiä) valitsemalla **Sähköisen laskutuksen toiminnot** -sivun **Määritykset**-välilehdessä **Lisää** tai **Poista**.

    ![Sähköisen laskutuksen toimintojen määritysten hallinta](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - Kun luot uuden version NF-e-veroasiakirjan toiminnosta, kaikki määritysversiot (ER-tiedostomuodot) periytyvät uusimmasta versiosta.
    - NF-e-veroasiakirjan lähettäminen hyväksyttäväksi edellyttää seuraavia määritysversioita:

        - NFe-lähetyksen vientimuoto
        - NFe-vastaussanoman tuonti
        - NFe-virhelokin tuonti

    - NF-e-peruutuksen lähettäminen edellyttää seuraavaa määritysversiota:

        - NFe-peruutuksen vientimuoto

2. Valitse luettelosta määritysversio ja valitse sitten **Muokkaa** tai **Näytä** avataksesi **Muodon suunnittelija** -sivun, jolla voit muokata tai tarkastella määritystä.

    ![Muodon suunnittelija -sivun avaaminen](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. Käytä **Muodon suunnittelija** -sivua muokataksesi tai tarkastellaksesi ER-muodon tiedostomäärityksiä. Lisätietoja on kohdassa [Sähköisten asiakirjojen määritysten luominen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration)

    ![Muodon suunnittelutoiminto -sivu](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a>Sähköisen laskutuksen toiminnon määritysten hallinta

- Voit hallita sähköisen laskutuksen toiminnon määrityksiä (eli NF-e-tapahtumia) valitsemalla **Sähköisen laskutuksen toiminnot** -sivun **Määritykset**-välilehdessä **Lisää** tai **Poista**.

![Sähköisen laskutuksen toiminnon määritysten hallinta](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

Kun luot uuden version NF-e-veroasiakirjan toiminnosta, joka on johdettu toisesta sähköisen laskutuksen toiminnosta, kaikki toiminnon määritykset (NF-e-tapahtumat) periytyvät uusimmasta versiosta.

NF-e-veroasiakirjojen hyväksyttäväksi lähettäminen edellyttää **Lähetä**-toimintamääritystä.

NF-e-peruutuksen lähettäminen edellyttää **Peruutus**-toimintomääritystä

#### <a name="configure-the-submit-feature-setup"></a>Lähetä-toimintomäärityksen määrittäminen

1. Valitse **Sähköisen laskutuksen toiminnot** -sivun **Määritykset**-välilehden **Toiminnon määritys** -sarakkeessa **Lähetä**.
2. Valitse **Muokkaa**.

    ![Sähköisen laskutuksen toiminnon muokkaaminen](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. Voit hallita toimiluetteloa valitsemalla **Toimintoversion määritys** -sivulla **Toimet**-välilehti.

    ![Toimet-välilehti](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. Niiden toimien tarkistaminen, joita edellytetään NF-e-veroasiakirjojen hyväksyttäväksi lähettämisessä.

    | Toimenpiteen tunnus | Toiminnon nimi                  | Toiminnon kuvaus                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | 1         | Muunna asiakirja           | Luo NF-e-XML-tiedosto lähetystä varten.                          |
    | 2         | Allekirjoita tiedosto                | Käytä XML-tiedostossa digitaalista varmennetta.                    |
    | 3         | Brasilian SEFAZ-palvelun kutsuminen | Lähetä allekirjoitettu XML-tiedosto verkkopalveluihin hyväksymistä varten. |
    | 4         | Käsittele vastaus             | Vastaanota verkkopalvelun vastaus.                                     |
    | 5         | Muunna asiakirja           | Jäsennä vastauksena saatavan tiedoston sisältö.     |
    | 6         | Muunna asiakirja           | Luo XML-tiedosto lähetyksen tilan kyselemistä varten.    |
    | 7         | Brasilian SEFAZ-palvelun kutsuminen | Lähetä XML-tiedosto, joka pyytää lähetystilaa.          |
    | 8         | Käsittele vastaus             | Vastaanota verkkopalvelun vastaus.                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>Määritä SEFAZ-verkkopalvelujen URL-osoite 

1. Valitse **Toimet**-pikavälilehden **Toimet**-välilehden **Toiminnon versiomääritys** -sivulla **Kutsu Brasilian SEFAZ-palvelua** (toimitunnus **3**).
2. Syötä **Parametrit**-pikavälilehden **URL-osoiteparametri**-kenttään NF-e-lähetyksen SEFAZ-verkkopalvelun URL-osoite.
3. Valitse **Toimet**-pikavälilehdessä **Kutsu Brasilian SEFAZ-palvelua** (toimitunnus **7**).
4. Syötä **Parametrit**-pikavälilehden **URL-osoiteparametri**-kenttään NF-e-lähetyksen SEFAZ-verkkopalvelun URL-osoite.

#### <a name="configure-the-cancellation-feature-setup"></a>Peruutus-toimintomäärityksen määrittäminen

1. Valitse **Sähköisen laskutuksen toiminnot** -sivun **Määritykset**-välilehden **Toiminnon määritys** -sarakkeessa **Peruuta**.
2. Valitse **Muokkaa**.
3. Voit hallita toimiluetteloa valitsemalla **Toimintoversion määritys** -sivulla **Toimet**-välilehti.
4. Niiden toimien tarkistaminen, joita edellytetään hyväksytyn NF-e-veroasiakirjan peruuttamiseen.

    | Toimenpiteen tunnus | Toiminnon nimi                  | Toiminnon kuvaus                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | 1         | Muunna asiakirja           | Luo NF-e-XML-peruutustiedosto lähetystä varten.            |
    | 2         | Allekirjoita tiedosto                | Käytä XML-tiedostossa digitaalista varmennetta.                   |
    | 3         | Brasilian SEFAZ-palvelun kutsuminen | Lähetä allekirjoitettu XML-tiedosto verkkopalveluihin peruuttamista varten. |
    | 4         | Käsittele vastaus             | Vastaanota verkkopalvelun vastaus.                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>Määritä SEFAZ-verkkopalvelujen URL-osoite

1. Valitse **Toimet**-pikavälilehden **Toimet**-välilehden **Toiminnon versiomääritys** -sivulla **Kutsu Brasilian SEFAZ-palvelua** (toimitunnus **3**).
2. Syötä **Parametrit**-pikavälilehden **URL-osoiteparametri**-kenttään SEFAZ-verkkopalvelun URL-osoite hyväksytyn NF-e-veroasiakirjan peruuttamista varten.

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a>Sähköisen laskutuksen ympäristön käyttöön ottaminen ja luonnosversion määrittäminen

1. Valitse **Sähköisen laskutuksen toiminnot** -sivun **Ympäristöt**-välilehdellä **Ota käyttöön**.
2. Valitse ympäristö **Ympäristöt**-kentässä.
3. Valitse **Voimaantulo**-kentässä päivämäärä, jona uusi ympäristö on tarkoitus ottaa käyttöön.
4. Valitse **Ota käyttöön**.

![Sähköisen laskutuksen ympäristön käyttöönotto](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a>Version tilan muuttaminen valmiiksi

1. Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot**-välilehdessä se sähköisen laskutuksen toiminto, jonka tilana on **Luonnos**.
2. Valitse **Muutoksen tila \> Viimeistele**.

### <a name="change-the-status-to-publish"></a>Version tilan muuttaminen muotoon Julkaise

1. Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot**-välilehdessä se sähköisen laskutuksen toiminto, jonka tilana on **Valmis**.
2. Valitse **Muuta tilaa \> Julkaise**.

![Sähköisen laskutuksen toiminnon julkaiseminen](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Sähköisen laskutuksen lisäosan integroinnin määrittäminen Financessa tai Supply Chain Managementissa

Määrityksen aikana suoritat seuraavat tehtävät:

1. NF-e Federal -toiminnon käyttöönotto Brasilian osalta.
2. Tuo tietty ER-tietomalli, ER-tietomallin yhdistämismääritys ja NF-e-veroasiakirjoja varten vaadittavat muodot.
3. ER-määrityksen tuonti ja niiden vastaustyyppien määrittäminen, jotka tarvitaan veroasiakirjan tilan päivittämiseen, kun lähetysprosessi palautetaan.

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a>NF-e Federal -toiminnon käyttöönotto Brasilian osalta

1. Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.
2. Valitse **Toiminnot**-välilehdellä **Ota käyttöön** -valintaruutu toimintoviitteen **BR00053** rivillä.

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a>NF-e-veroasiakirjojen edellyttämän ER-tietomallin yhdistämismäärityksen tuonti

1. Kirjaudu Financeen.
2. Valitse **Sähköisen raportointi** -työtilan **Määrityslähteet** -osassa **Microsoft**. Varmista, että tämän määrityspalvelun arvoksi on määritetty **Aktiivinen**. Tietoja palvelun arvon **Aktiivinen**-muotoon määrittämisestä: [Luo määrityspalveluja ja merkitse ne aktiiviseksi](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Valitse **Säilöt**.
4. Valitse **Yleinen resurssi \> Avaa**.
5. Tuo **Veroasiakirjojen yhdistämismääritys** -määritykset.

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a>ER-määritysten tuominen ja veroasiakirjojen vastaustyyppien määrittäminen

1. Valitse **Sähköisen raportointi** -työtilan **Määrityslähteet** -osassa **Microsoft**.
2. Valitse **Säilöt**.
3. Valitse **Yleinen resurssi \> Avaa**.
4. Tuo **NF-e-virhelokin tuonti (BR)**, **NF-e-vastausten tietotuonnin muoto (BR)** ja **NF-e-vastaussanoman tuonti (BR)**.
5. Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.
6. Valitse **Sähköinen asiakirja** -välilehdellä **Lisää**.
6. Syötä **Taulukon nimi** -kenttään **Veroasiakirjan otsikko**.
7. Valitse **Asiakirjan konteksti** -kentässä **Asiakaslaskun kontekstimalli – veroasiakirjan konteksti**.
8. Valitse **Vastaustyypit**.
9. Valitse **Uusi** ja sitten **Vastaustyyppi** -kentässä **Vastaus**.
10. Valitse **Lähetystila**-kentässä **Odottaa**.
11. Valitse **Mallin yhdistämismääritys** -kentässä **Vastaussanoman tuontimuoto – mallin yhdistämismääritys vastaussanomasta**.
12. Valitse **Tallenna**.
13. Valitse **Uusi** ja syötä sitten **Vastaustyyppi**-kenttään **ResponseData**.
14. Valitse **Lähetystila**-kentässä **Odottaa**.
15. Valitse **Mallin yhdistämismääritys** -kentässä **NFe-vastaustietojen tuontimuoto – vastaustietojen tuonti**
16. Valitse **Tallenna**.

## <a name="electronic-invoice-processing"></a>Sähköisen laskun käsittely

Financessa käsittelyn aikana suoritat seuraavat tehtävät:

1. Veroasiakirjan lähettäminen sähköisen laskutuksen lisäosalla.
2. Lähetyksen suorituslokien tarkasteleminen ja käsittelytulosten arvioiminen.
3. Veroasiakirjan peruutuksen lähettäminen sähköisen laskutuksen lisäosalla.

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a>NF-e-veroasiakirjojen lähettäminen SEFAZ:n hyväksyttäväksi 

Kun olet ottanut käyttöön **Määritettävä sähköisen laskutuksen lisäosan integrointi** vanhaa prosessia NF-e-veroasiakirjojen hyväksyttäväksi lähettämiseen (**Vie/tuo NF-e-prosessi)** ei voi enää käyttää. Se korvataan uudella prosessilla, jonka nimi on **Lähetä sähköiset asiakirjat**.

> [!NOTE]
> Varmista ennen jatkamista, että sinulla on vähintään yksi asiakkaan veroasiakirjamalli 55, jotka asiakkaan talousosasto on luonut. Näiden veroasiakirjojen suunnan on oltava **Lähtevä** ja tilan **Luotu**. Lisätietoja [Asiakkaan veroasiakirjan luominen (Brasilia)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).

1. Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Lähetä sähköisiä asiakirjoja**.
2. Kun mikä tahansa asiakirja lähetetään ensimmäistä kertaa, määritä **Lähetä asiakirjat uudelleen** -asetukseksi aina **Ei**. Jos sinun on lähetettävä asiakirja uudelleen palvelun kautta, määritä asetukseksi **Kyllä**.
3. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** avataksesi **Kysely**-valintaruudun, jossa voit muodostaa kyselyn lähetettävien asiakirjojen valitsemista varten.
4. Valitse **Alue**-välilehdessä **Lisää**.
5. Valitse **Taulukko** -kentässä **Veroasiakirjan otsikko**.
6. Valitse **Johdettu taulukko** -kentässä **Veroasiakirjan otsikko**.
6. Valitse **Kenttä** -kentässä **Numero**.
7. Syötä **Perusteet**-kenttään lähetettävän veroasiakirjan numero.
8. Valitse **OK**, jotta voit sulkea **Kysely**-valintaikkunan.
8. Lähetä valitut asiakirjat valitsemalla **OK**.

> [!NOTE]
> Kun yrität lähettää asiakirjan palvelun kautta ensimmäisen kerran, järjestelmä pyytää vahvistamaan yhteyden sähköisen laskutuksen lisäosaan. Valitse **Yhdistä sähköisten asiakirjojen lähetyspalveluun napsauttamalla tätä**.

### <a name="view-all-submission-logs"></a>Kaikkien lähetyslokien tarkastelu

Kun olet ottanut **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminnon käyttöön, käytettävissä on uusi sivu, jolla voi seurata asiakirjan lähetysprosessia. Voit käyttää tätä sivua kaikkien lähetettyjen asiakirjojen lähetyslokien tarkasteluun.

1. Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Sähköisen asiakirjan lähetysloki**.
2. Valitse **Asiakirjatyyppi**-kentässä **Veroasiakirjan otsikko** suodattaaksesi vain veroasiakirjoja.
3. Valitse toimintoruudussa **Kyselyt \> Lähetystiedot** tarkastellaksesi lähetyksen toteutuslokien tietoja.

![Lähetyslokitietojen tarkastelu](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> Muiden kuin NF-e-veroasiakirjojen osalta **Virhekoodi**-sarakkeessa näkyy SEFAZ-verkkopalvelujen palauttama palautuskoodi.

### <a name="view-submission-logs-through-the-fiscal-document-page"></a>Lähetyslokien tarkasteleminen veroasiakirjan sivun kautta

Kun otat **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminnon käyttöön, voit myös tarkastella lähetyslokeja veroasiakirjojen sivun kautta.

1. Siirry kohtaan **Kirjanpito \> Kyselyt ja raportit \> Veroasiakirjat \> Kaikki veroasiakirjat**.
2. Valitse veroasiakirja, joka on lähetetty sähköisen laskutuksen lisäosan kautta.
3. Valitse toimintoruudun **NF-e federal**-välilehdessä **Sähköisen asiakirjan loki**.

![Lähetyslokien tarkasteleminen veroasiakirjan sivun kautta](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a>Hyväksyttyjen NF-e-veroasiakirjojen lähettäminen SEFAZ:n peruutettavaksi

Kun olet ottanut **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminnon käyttöön, vanhaa NF-e-veroasiakirjojen peruutusprosessia ei voi enää käyttää. Se korvataan uudella peruutusprosessilla, joka on upotettu **Sähköisen asiakirjan lähetysloki** -sivulle.

> [!NOTE]
> Varmista, että olet suorittanut asiakkaan veroasiakirjan peruuttamisen hyväksytyn NF-e-veroasiakirjan osalta. Lisätietoja: [Asiakkaan veroasiakirjan peruuttaminen (Brasilia)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).

1. Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Sähköisen asiakirjan lähetysloki**.
2. Valitse veroasiakirja ja valitse sitten **Funktiot \> Lähetä liittyvät lähetykset**.
3. Kirjoita liittyvän lähetyksen kuvaus ja valitse sitten **OK**.

### <a name="view-cancellation-submission-logs"></a>Peruutusten lähetyslokien tarkastelu

1. Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Sähköisen asiakirjan lähetysloki**.
2. Valitse **Asiakirjatyyppi**-kentässä **Veroasiakirjan otsikko** suodattaaksesi vain veroasiakirjoja.
3. Valitse veroasiakirja ja valitse sitten toimintoruudussa **Tiedustelut \> Liittyvä lähetys**.

    Liittyvät lähetykset ovat lähetyksiä, jotka liittyvät aiemmin luotuun päälähetykseen. Esimerkiksi tietyn NF-e-veroasiakirjan hyväksyvä lähetys on päälähetys. Lähetys, jossa pyydetään saman NF-e-veroasiakirjan peruuttamista SEFAZ:ssa on liittyvä lähetys. Se on olemassa vain siksi, että sillä pyydetään toisella lähetyksellä suoritetun tehtävän peruuttamista.

    **Liittyvät lähetykset** -sivulla näkyvät kaikki liittyvät lähetykset ja niiden lähetystila tietyn veroasiakirjan osalta. Seuraavassa kuvassa ensimmäinen rivi edustaa lähetystä, joka pyysi veroasiakirjan hyväksymistä. Toinen rivi vastaa edustaa lähetystä, joka peruutti veroasiakirjan.

    ![Peruutusten lähetyslokien tarkastelu](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. Valitse toimintoruudussa **Kyselyt \> Lähetystiedot** tarkastellaksesi lähetyksen toteutuslokien tietoja.

    ![Peruutusten lähetyslokitietojen tarkastelu](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a>Tietosuojatiedot
BR-00053 (NF-e Federal) -toiminnon käyttöönotto saattaa edellyttää rajoitettujen tietojen, joihin kuuluu organisaation verorekisteritunnus, lähettämistä. Ne välitetään kolmannen osapuolen virastoille, jotka veroviranomaiset ovat hyväksyneet sähköisten laskujen kyseiselle veroviranomaiselle lähettämistä varten siinä esimääritetyssä muodossa, jota integrointi valtion verkkopalveluun edellyttää. Järjestelmänvalvoja voi ottaa toiminnon BR-00053 (NF-e Federal) -toiminnon käyttöön ja poistaa sen käytöstä siirtymällä kohtaan **Organisaation hallinta \> Määritykset \> Sähköisten asiakirjojen parametrit**. Valitse **Toiminnot**-välilehti, valitse toiminnon BR-00053 sisältävä rivi ja tee sitten haluamasi valinta. Näistä ulkoisista järjestelmistä tähän Dynamics 365 -verkkopalveluun tuotuihin tietoihin sovelletaan [tietosuojalausuntoamme](https://go.microsoft.com/fwlink/?LinkId=512132). Katso lisätietoja maakohtaisten toimintodokumentaatioiden tietosuojaosista.


## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen laskutuksen yleiskatsaus](e-invoicing-service-overview.md)
- [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md)
- [Sähköisen laskutuksen lisäosan määrittäminen](e-invoicing-setup.md)
