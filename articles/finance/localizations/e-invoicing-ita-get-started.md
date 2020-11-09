---
title: Italian sähköisen laskutuksen lisäosan käytön aloittaminen
description: Tässä aiheessa on tietoja, joiden avulla voit aloittaa Italian sähköisen laskutuksen lisäosan käytön Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.
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
ms.openlocfilehash: c513141f820c95fe3842478361693701f1e3641b
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039789"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a>Italian sähköisen laskutuksen lisäosan käytön aloittaminen

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Italian sähköisen laskutuksen lisäosa ei tällä hetkellä välttämättä tue kaikkia funktioita, jotka ovat käytettävissä Microsoft Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin laskuissa. 

Tässä aiheessa on tietoja, joiden avulla voit aloittaa Italian sähköisen laskutuksen lisäosan käytön. Se opastaa Regulatory Configuration Servicesin (RCS) ja Financen maakohtaisissa määritysvaiheissa. Se opastaa myös, miten voidaan lähettää sähköisiä laskuja, jotka on luotu palvelulla Italialle yksilöllisessä **FatturaPA** -muodossa. Lisäksi siinä selitetään, miten käsittelyn tulokset arvioidaan.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin suoritat tämän aiheen vaiheet, sinun on suoritettava aiheen [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md) vaiheet.

## <a name="rcs-setup"></a>RCS-asetukset

RCS:n määrityksen aikana suoritat seuraavat tehtävät:

1. Sähköisen laskutuksen toiminnon tuominen asiakkaiden sähköisten laskujen viemiseen **FatturaPA** -muodossa.
2. Sähköisiä laskuja koskevien vastausten luomiseen, lähettämiseen ja vastaanottamiseen vaadittavien muotomääritysten arvioiminen.
3. Määritä tapahtumat, jotka tukevat sähköisen laskun lähetysskenaarioita.
4. Sähköisen laskutuksen toiminnon julkaiseminen.

> [!NOTE]
> Sähköisen laskutuksen toiminto on sen resurssin yleinen nimi, joka määritetään ja julkaistaan käytettäväksi sähköisen laskutuksen lisäosan palvelimella. Tässä tapauksessa määritettävä sähköisen laskutuksen toiminto on asiakkaiden sähköisten laskujen vienti.

## <a name="import-the-e-invoicing-feature"></a>Sähköisen laskutuksen toiminnon tuominen

1. Kirjaudu RCS-tilille.
2. Valitse **Globalisointitoiminnot** -työtila ja **Toiminnot** -kohdan **Sähköinen laskutus** -ruutu.
3. Valitse **Sähköisen laskutuksen toiminnot** -sivulla **Tuo** tuodaksesi sähköisen laskutuksen toiminnon yleisestä säilöstä.

    > [!NOTE]
    > Jos käytettävissä olevien toimintojen luettelo ei ole näkyvissä, valitse **Synkronoi**. 

4. Valitse **Sähköisten laskujen vienti (IT)** -toiminto ja sitten **Tuo**.

![Sähköisten laskujen vienti (IT) -toiminnon tuominen](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

Kun tuot **Sähköisten laskujen vienti (IT)** -toiminnon yleisestä säilöstä, myös kaikki seuraavissa osissa kuvatut asetukset tuodaan.

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a>Uuden versoin luominen Sähköisten laskujen vienti (IT) -toiminnosta

1. Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot** -välilehdellä **Uusi**. 

    ![Uuden sähköisen laskutuksen toiminnon version lisääminen](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    Seuraavaksi määritetään sähköisen raportoinnin (ER) muodot, jotka liittyvät sähköisen laskutuksen toimintoon.

2. Hallitse märitysversioita valitsemalla **Määritykset** -välilehdessä **Lisää**.

    ![Sähköisen laskutuksen toiminnon määritysversioiden hallinta](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    Tässä vaiheessa lisätään ja määritetään italialaisten sähköisten laskujen viemisessä käytettävien eri tiedostojen ER-muotoja. Italialaisissa sähköisissä FatturaPA-laskuissa käytetään joko seuraavia vakiomäärityksiä tai ajantasaisia mukautettuja määrityksiä, joita käytät sähköisessä laskutuksessa:

    - Myyntilasku (IT)
    - Projektilasku (IT)

    Kun luot sähköisen laskun toiminnon, joka johdetaan toisesta vastaavasta, kaikki ER-muodot periytyvät alkuperäisestä toiminnosta.

3. Valitse tietty tiedoston ER-muodon määritys.
4. Avaa **Muodon suunnittelija** -sivu valitsemalla **Muokkaa** tai **Näytä**.

    ![Muodon suunnittelija -sivun avaaminen](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. Käytä **Muodon suunnittelija** -sivua muokataksesi ja tarkastellaksesi ER-muodon tiedostomäärityksiä.

    ![Muodon suunnittelutoiminto -sivu](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>Sähköisen laskutuksen toiminnon määritysten hallinta

- Voit hallita sähköisen laskutuksen toiminnon määrityksiä valitsemalla **Sähköisen laskutuksen toiminnot** -sivun **Määritykset** -välilehdessä **Lisää** , **Poista** tai **Muokkaa**.

![Sähköisen laskutuksen toiminnon määritysten hallinta](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

Tässä vaiheessa määritetään sähköisiin laskuihin sovellettavat tapahtumat, kuten XML-tulostetiedostojen luonti **FatturaPA** -muodossa ja digitaalinen allekirjoitus (tarvittaessa).

### <a name="configure-the-sales-invoice-feature-setup"></a>Myyntilaskutoiminnon asetusten määrittäminen

1. Valitse **Sähköisen laskutuksen toiminnot** -sivun **Määritykset** -välilehden **Toiminnon määritys** -sarakkeessa **Myyntilasku**.
2. Valitse **Muokkaa**.
3. Voit hallita toimiluetteloa valitsemalla **Toimintoversion määritys** -sivulla **Toimet** -välilehti. Toimet määrittävät luettelon toiminnoista, jotka on suoritettava peräkkäisessä järjestyksessä, jotta toiminto suoritetaan kokonaisuudessaan.

    ![Toimet-välilehti](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | Toimenpiteen tunnus | Toiminnon nimi        | Toiminnon kuvaus                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | 1         | Muunna asiakirja | Luo sähköisen laskun XML-tiedosto **fatturaPA** -muodossa. |
    | 2         | Allekirjoita tiedosto      | Käytä XML-tiedostossa digitaalista allekirjoitusta.             |

4. Voit tarkastella ja hallita soveltuvuusääntöjä valitsemalla **Soveltuvuussäännöt** -välilehden. Soveltuvuussäännöt määrittävät kontekstin, jossa toimi suoritetaan.

    ![Soveltuvuussääntöjen välilehti](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. Voit tarkastella ja hallita muuttujia valitsemalla **Muuttujat** -välilehden.

    ![Muuttujat-välilehti](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. Määritä julkiset muuttujat, jotka tarvitaan toimien suorittamiseen.

### <a name="configure-the-project-invoice-feature-setup"></a>Projektilaskutoiminnon asetusten määrittäminen 

Vaiheet ja asetukset, joita tarvitaan **Projektilasku** -toiminnon määrittämiseen ovat hyvin samankaltaisia kuin **Myyntilasku** -toiminnon määrittämisen vaiheet ja asetukset. Kun käytät projektilaskuja, katso myyntilaskujen menettelyt.

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a>Sähköisen laskutuksen toiminnon määrittäminen ympäristölle

1. Valitse **Sähköisen laskutuksen toiminnot** -sivun **Ympäristöt** -välilehdellä **Ota käyttöön**.
2. Valitse ympäristö **Ympäristöt** -kentässä.
3. Valitse **Voimaantulo** -kentässä päivämäärä, jona uusi ympäristö on tarkoitus ottaa käyttöön.
4. Valitse **Ota käyttöön**. 

![Sähköisen laskutuksen ympäristön käyttöönotto](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a>Sähköisen laskutuksen toiminnon julkaiseminen

Voit julkaista sähköisen laskutuksen toiminnon muuttamalla version tilaksi **Valmis** tai **Julkaistu**.

### <a name="change-the-version-status-to-completed"></a>Version tilan muuttaminen valmiiksi

1. Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot** -välilehdessä se sähköisen laskutuksen toiminto, jonka tilana on **Luonnos**.
2. Valitse **Muutoksen tila \> Viimeistele**. 

### <a name="change-the-version-status-to-published"></a>Version tilan muuttaminen julkaistuksi 

1. Valitse **Sähköisen laskutuksen toiminnot** -sivun **Versiot** -välilehdessä se sähköisen laskutuksen toiminto, jonka tilana on **Valmis**.
2. Valitse **Muuta tilaa \> Julkaise**.

![Sähköisen laskutuksen toiminnon tilan muuttaminen](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a>Sähköisen laskutuksen lisäosan integroinnin määritys Financessa

Financen määrityksen aikana suoritat seuraavat tehtävät:

1. Tuo ER-tietomalli, ER-tietomallin yhdistämismääritys ja CFDI-laskujen kontekstimääritykset sähköisiä FatturaPA-laskuja varten.
2. Määritä varmenne, joka vaaditaan italialaisten sähköisten laskujen digitaaliseen allekirjoittamiseen.

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a>ER-tietomallin, tietomallin yhdistämismäärityksen ja muotojen tuonti

1. Varmista **Sähköinen raportointi** -työtilassa, että **Liiketoiminta-asiakirjapalvelu** -määrityspalvelun tilana on **Aktiivinen**.
2. Valitse **Säilöt**.
3. Valitse **Yleinen resurssi \> Avaa**.
4. Tuo **Laskumalli** , **Laskumallin yhdistämismääritys** ja **Asiakkaan laskukontekstimalli**.

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a>Ota käyttöön toiminto, jolla viedään asiakkaan sähköisiä laskuja Italiassa

1. Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.
2. Valitse **Toiminnot** -välilehdellä **Käytössä** -valintaruutu toimintoviitteen **IT00036** rivillä.

![FatturaPA-toiminnon käyttöönotto](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a>Sähköisten asiakirjojen määrittäminen

1. Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.
2. Valitse **Sähköinen asiakirja** -välilehdessä **Lisää** ja syötä taulukot, joita tarvitaan italialaisten sähköisten laskujen luonnissa:

    - **Taulukon nimi:** Asiakkaan laskukirjauskansio
    - **Taulukon nimi** Projektilasku

3. Määritä kullekin taulukolle liittyvä asiakirjakonteksti:

    - Valitse kohdassa **Asiakkaan laskukirjauskansio** **Asiakkaan laskukonteksti**.
    - Valitse kohdassa **Projektilasku** **Projektilaskun konteksti**.

![Vastaustyyppien määrittäminen](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a>Sähköisen laskun käsittely

Financessa käsittelyn aikana suoritat seuraavat tehtävät:

1. Italialaisten sähköisten laskujen luominen sähköisen laskutuksen lisäosan kautta
2. Suorituslokien tarkasteleminen ja käsittelytulosten arvioiminen

### <a name="generate-electronic-invoices"></a>Sähköisten laskujen luominen

Kun otat käyttöön **Määritettävä sähköisen laskutuksen lisäosan integrointi** -toiminnon ja aktivoit **IT00036** -toiminnon, Financen vanhaa prosessia italialaisten sähköisten laskujen luomiseen ei enää voi käyttää. Se korvataan uudella prosessilla, jonka nimi on **Lähetä sähköiset asiakirjat**.

Voit lähettää asiakirjat manuaalisesti riippuen sähköisten laskujen asiakirjojen tarpeestasi.

> [!NOTE]
> Varmista ennen jatkamista, että italialaisten sähköisten laskujen edellyttämä määritys on tehty. Lisätietoja: [Asiakkaiden sähköiset laskut](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices). Huomaa, että osa kyseisessä aiheessa kuvatuista määritysvaiheista ei välttämättä ole käytettävissä sähköisen laskutuksen lisäosan aktivoinnin vuoksi.

1. Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Lähetä sähköisiä asiakirjoja**.
2. Kun mikä tahansa asiakirja lähetetään ensimmäistä kertaa, määritä **Lähetä asiakirjat uudelleen** -asetukseksi **Ei**. Jos sinun on lähetettävä asiakirja uudelleen palvelun kautta, määritä asetukseksi **Kyllä**.
3. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** avataksesi **Kysely** -valintaruudun, jossa voit muodostaa kyselyn lähetettävien asiakirjojen valitsemista varten.

![Sähköisten asiakirjojen lähettämisen valintaruutu](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a>Suodatinkysely

1. Määritä **Kysely** -valintaruudussa sekä myynti- että projektilaskujen suodatusehdot tai jätä ehdot tyhjiksi, jos haluat sisällyttää kaikki lähettämättömät laskut.

    ![Lähetyksen suodatusehtojen määrittäminen](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. Valitse **OK** , jotta voit sulkea **Kysely** -valintaikkunan.
3. Lähetä valitut asiakirjat valitsemalla **OK**.

> ![HUOMAA] Kun yrität lähettää asiakirjan palvelun kautta ensimmäisen kerran, järjestelmä pyytää vahvistamaan yhteyden sähköisen laskutuksen lisäosaan. Valitse **Yhdistä sähköisten asiakirjojen lähetyspalveluun napsauttamalla tätä**.

#### <a name="view-submission-logs"></a>Lähetyslokien tarkasteleminen

Voit tarkastella kaikkien lähetettyjen asiakirjojen lähetyslokeja.

1. Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Sähköisen asiakirjan lähetysloki**.
2. Valitse **Asiakirjatyyppi** -kentässä **Asiakkaan laskukirjauskansio** tai **Projektilasku** suodattaaksesi vaadittavat sähköiset asiakirjat.

    ![Asiakirjatyypin valinta lähetyslokien tarkastelua varten](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    **Lähetystila** -sarakkeessa näkyvä arvo edustaa lähetysprosessin tilaa. Se ilmaisee, suoritettiinko prosessi määrityksen mukaisesti ja tarvitaanko lisätoimia.

3. Valitse toimintoruudussa **Kyselyt \> Lähetystiedot** tarkastellaksesi lähetyksen toteutuslokien tietoja.

    ![Lähetyslokitietojen tarkastelu](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. **Käsittelytoimet** -pikavälilehdessä näkyy RCS:ssä määritetyssä toimintoversiossa määritettyjen toimien suoritusloki. **Tila** -sarakkeessa näkyy, suoritettiinko toimi onnistuneesti.
5. **Toimitiedostot** -pikavälilehdessä näkyvät välitiedostot, jotka luotiin toimien suorittamisen aikana. Voit valita **Näytä** ladataksesi tulote-XML-tiedoston **FatturaPA** -muodossa ja tarkastellaksesi sen sisältöä.

## <a name="related-topics"></a>Liittyvät aiheet

- [Sähköisen laskutuksen yleiskatsaus](e-invoicing-service-overview.md)
- [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md)
- [Sähköisen laskutuksen lisäosan määrittäminen](e-invoicing-setup.md)
