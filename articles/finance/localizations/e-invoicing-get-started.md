---
title: Sähköisen laskutuksen lisäosan käytön aloittaminen
description: Tässä aiheessa on tietoja, joiden avulla voit aloittaa sähköisen laskutuksen lisäosan käytön Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.
author: gionoder
manager: AnnBe
ms.date: 10/08/2020
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
ms.openlocfilehash: 7b2a3aae43d42060c7fcd9e1ea3db814fc5d8f22
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/19/2020
ms.locfileid: "4442951"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Sähköisen laskutuksen lisäosan käytön aloittaminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa on tietoja, joiden avulla voit aloittaa sähköisen laskutuksen lisäosan käytön. Ensinnäkin se opastaa sinua Microsoft Dynamics Lifecycle Servicesin (LCS), Regulatory Configuration Servicesin ja Dynamics 365 Financen määritysvaiheissa. Seuraavaksi se kuvaa prosessin, jossa asiakirjoja lähetetään palvelun kautta käyttäen Dynamics 365 Financea tai Dynamics 365 Supply Chain Managementia. Tutustut myös lähetyslokien tulkitsemiseen.

## <a name="availability"></a>Käytettävyys

Sähköisen laskutuksen lisäosa on alkuun käytettävissä useissa maissa. Apuohjelma tukee sähköisten laskujen luontia ja seuraavien liiketoiminta-asiakirjojen lähettämistä:

| Maa/alue  | Yritysasiakirja                          |
|-----------------|--------------------------------------------|
| Itävalta         | Myynti- ja projektilaskut                 |
| Belgia         | Myynti- ja projektilaskut                 |
| Brasilia          | Sähköinen veroasiakirjamalli 55 (NF-e) |
| Tanska         | Myynti- ja projektilaskut                 |
| Viro         | Myynti- ja projektilaskut                 |
| Suomi         | Myynti- ja projektilaskut                 |
| Ranska          | Myynti- ja projektilaskut                 |
| Saksa         | Myynti- ja projektilaskut                 |
| Italia           | Myynti- ja projektilaskut                 |
| Meksiko          | CFDI-lasku                               |
| Alankomaat     | Myynti- ja projektilaskut                 |
| Norja          | Myynti- ja projektilaskut                 |
| Espanja           | Myynti- ja projektilaskut                 |
| Eurooppa          | PEPPOL-myynti- ja projektilaskut          |
    
## <a name="licensing"></a>Käyttöoikeudet

Voit käyttää sähköisen laskutuksen lisäosaa nykyisellä lisenssilläsi. Palvelun käyttämiseen ei tarvita lisälisenssejä.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit suorittaa tämän ohjeaiheen vaiheita, seuraavien edellytysten on toteuduttava:

- Pääsy LCS-tiliisi.
- LCS-käyttöönottoprojekti, joka sisältää Financen tai Supply Chain Managementin version 10.0.13 tai sitä uudemman.
- Pääsy RCS-tiliisi.
- RCS-tilin globalisointiominaisuuden käyttöönotto **Toiminnonhallinta**-moduulin kautta. Lisätietoja [Regulatory Configuration Services (RCS) – globalisointitoiminnot](rcs-globalization-feature.md)
- Luo avainsäilöresurssi ja tallennustili Azuressa. Lisätietoja [Azure-tallennustilin ja -avainsäilön luominen](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="overview"></a>Yleiskuvaus

Seuraavassa kuvassa esitetään viisi päävaihetta, jotka suoritat tässä aiheessa.

![Tämän aiheen viiden vaiheen yleiskatsaus](media/e-invoicing-services-get-started-overview-5-steps.png)

1. **Azure-resurssien määritys:** Azure-tallennustilan määrittäminen ja digitaalisten varmenteiden lataaminen Azure Key Vaultiin.
2. **LCS-määritys:** Asenna mikropalvelujen apuohjelma.
3. **RCS-määritys:** Määritä ympäristö, käyttöoikeudet ja sähköisen laskutuksen toiminnot.
4. **Asiakkaan asetukset:** Määritä asiakkaan ja sähköisen laskutuksen lisäohjelman välinen yhteys ja poista käytöstä vanhat toiminnot sähköisten asiakirjojen lähettämiselle ja vastausten vastaanottamiselle.
5. **Laskujen lähettäminen:** Lähetä sähköisiä asiakirjoja sähköisen laskutuksen lisäosalla ja vastaanota vastauksia.

> [!NOTE]
> Jotkut tämän aiheen määritysvaiheet ovat yleisiä ja maasta/alueesta riippumattomia. Maa-/aluekohtaiset vaiheet ja määritysmenettelyt on kuvattu maa-/aluekohtaisissa aiheissa.

## <a name="lcs-setup"></a>LCS-asetukset

1. Kirjaudu LCS-tilille.
2. Valitse **Esiversiotoiminnon hallinta** -ruutu ja valitse sitten **Julkisen esiversion toiminnot** -kenttäryhmässä **BusinessDocumentSubmission**.
3. Merkitse **Esiversiotoiminto käytössä** -kenttä.
4. Valitse LCS-käyttöönottoprojekti. Ennen kuin voit valita projektin, sen on oltava käynnissä.
5. Valitse **Ympäristöapuohjelmat**-pikavälilehdessä **Asenna uusi apuohjelma**.
6. Valitse **Liikeasiakirjojen lähetys**.
7. Syötä **Apuohjelman määritys**-valintaikkunan **AAD-sovellustunnus**-kenttään **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Tämä arvo on kiinteä arvo.
8. Syötä **AAD-vuokraajatunnus**-kenttään Azure-tilaustilisi tunnus.

    ![Apuohjelman valintaikkunan määrittäminen LCS:ssä](media/e-invoicing-services-get-started-lcs-addin-setup.png)

9. Hyväksy ehdot valitsemalla valintaruutu.
10. Valitse **Asenna**.

## <a name="rcs-setup"></a>RCS-asetukset

RCS:n määrityksen aikana suoritat seuraavat tehtävät:

1. Määritä avainsäilö RCS:ssä.
2. Määritä RCS-integrointi sähköisen laskutuksen lisäosapalvelimeen.
3. Luo organisaatiolle sähköisen laskutuksen lisäosaympäristö.

### <a name="set-up-the-key-vault-in-rcs"></a>Määritä avainsäilö RCS:ssä

1. Kirjaudu RCS-tilille.
2. Valitse **Globalisointitoiminnot**-työtila ja **Ympäristöt**-kohdan **Sähköinen laskutus** -ruutu.
3. Valitse **Palveluympäristöt**.

    ![Palveluympäristöjen valinta](media/e-invoicing-services-get-started-select-service-environments.png)

> [!NOTE]
> **Yhdistetyt sovellukset**-asetus myöntää käyttöoikeuden sähköisen laskutuksen lisäosan automaattiseen määritykseen Financessa tai Supply Managementissa RCS:n kautta. Tällä hetkellä tämä ominaisuus on kuitenkin vielä kehitteillä.

4. Valitse toimintoruudussa **Avainsäilön parametrit**.

    ![Avainsäilön parametrin valinta](media/e-invoicing-services-get-started-select-key-vault-parameters.png)

5. Lisää avainsäilö valitsemalla toimintoruudussa **Uusi**.
6. Syötä **Avainsäilön URI** -kenttään Azuressa määrittämäsi avainsäilöresurssin **DNS-nimi**-määritearvo. Lisätietoja **DNS-nimen** sijainnista: [Azure-tallennustilin ja Key Vaultin luominen](e-invoicing-create-azure-storage-account-key-vault.md).

    ![Avainsäilön URI -kenttä](media/e-invoicing-services-get-started-enter-key-vault-uri.png)

7. Valitsemalla **Varmenteet**-pikavälilehdessä **Lisää** voit antaa kaikki digitaaliset varmennenimet ja avainsäilön salaisuudet, joita tarvitaan luotettavien yhteyksien muodostamiseen. Voit määrittää **Tyyppi**-sarakkeessa, onko se varmenne vai salainen koodi. Molemmat arvojoukot määritetään Azuren avainsäilöresurssissa.

    ![Varmenteiden lisääminen](media/e-invoicing-services-get-started-add-digital-certificates.png)

8. Jos maa-/aluekohtainen laskusi edellyttää tiettyjen varmenteiden soveltamista digitaaliseen allekirjoitukseen, valitse toimintoruudusta **Varmenneketju** ja syötä ketjuun kuuluva joukko varmenteita tai avainsäilösalasanoja.

### <a name="set-up-the-rcs-integration-with-the-electronic-invoicing-add-on-server"></a>Määritä RCS-integrointi sähköisen laskutuksen lisäosapalvelimeen

1. Valitse **Globalisaatiotoiminnot**-työtilan **Liittyvät asetukset** -osassa **Sähköisen raportoinnin parametrit** -linkki.
2. Valitse **Yhdistä elinkaaripalveluun napsauttamalla tästä**. Jos et halua yhdistää LCS:ään, valitse **Peruuta**.
3. Anna **Sähköiset laskutuspalvelut** -välilehden **Järjestelmän päätepisteen URI** -kentässä arvo seuraavien käytettävissä olevien maantieteellisten alueiden mukaan: `https://businessdocumentsubmission.us.operations365.dynamics.com/` tai `https://businessdocumentsubmission.eu.operations365.dynamics.com/`.
4. Varmista, että tunnus **0cdb527f-a8d1-4bf8-9436-b352c68682b2** näkyy **Sovellustunnus**-kentässä. Tämä arvo on kiinteä arvo.
5. Syötä **LCS-ympäristötunnus**-kenttään LCS-tilaustilisi tunnus.

![Sähköisen laskutuksen lisäosan parametrien syöttäminen](media/e-invoicing-services-get-started-enter-e-invoicing-parameters.png)

### <a name="add-an-electronic-invoicing-add-on-environment"></a>Sähköisen laskutuksen lisäosaympäristön lisääminen

Sähköisen laskutuksen lisäosassa voi luoda erilaisia ympäristöjä, kuten kehitys-, testaus- tai tuotantoympäristöjä.

1. Valitse **Globalisointitoiminnot**-työtila ja **Ympäristöt**-kohdan **Sähköinen laskutus** -ruutu.
2. Luo uusi ympäristö valitsemalla **Uusi**.
3. Syötä **Tallennustilan SAS-tunnustili** -kenttään sen avainsäilöresurssin salasanan, jonka määritit RCS:n avainsäilössä.

    ![Tallennustilan SAS-tunnustilin kenttä](media/e-invoicing-services-get-started-enter-sas-token-secret.png)

4. Myönnä käyttäjille käyttöoikeus tähän ympäristöön valitsemalla **Käyttäjät**-pikavälilehdessä **Uusi**.

    ![Palvelun käyttäjien lisääminen](media/e-invoicing-services-get-started-enter-service-users.png)

5. Julkaise ympäristö sähköisen laskutuksen lisäosan palvelimella valitsemalla toimintoruudussa **Julkaise**.

    ![Julkaise-painike](media/e-invoicing-services-get-started-publish-service-environment.png)

### <a name="e-invoicing-feature-setup"></a>Sähköisen laskutuksen toiminnon määritys

Sähköisen laskutuksen toiminto on sen resurssin yleinen nimi, joka määritetään ja julkaistaan käytettäväksi sähköisen laskutuksen lisäosan palvelimella. Sähköisen laskutuksen toiminnon määrityksessä yhdistyvät muun muassa sähköisen raportoinnin (ER) määrityksen muodot määritettävien vienti- ja tuontitiedostojen luomista varten sekä toimintojen ja toimintokulkujen käyttäminen määritettävien pyyntöjen lähettämisen sääntöjen luomiseen, vastausten tuomiseen sekä vastausten sisältöjen jäsentämiseen.

Laskumuotojen ja toimintokulkujen välisten erojen vuoksi toiminnon määritys on maa-/aluekohtainen.

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Sähköisen laskutuksen lisäosan integroinnin määrittäminen Financessa tai Supply Chain Managementissa 

Tämän määrityksen aikana suoritat seuraavat tehtävät:

1. Väliversion avaaminen
2. Sähköisen laskutuksen lisäosan integrointitoiminnon käyttöönotto Financeen integroinnin mahdollistamiseksi.
3. Sähköisen laskutuksen päätepisteen URL-osoitteen määrittäminen.
4. Maa-/aluekohtaiseen sähköisen laskutuksen toimintoon liittyvien ER-määritysten tuominen.
5. Sovellettavan maa-/aluekohtaisen sähköisen laskutuksen toiminnon käyttöönotto.
6. ER-määritysten tuonti ja niiden vastaustyyppien määrittäminen, jotka tarvitaan maa-/aluekohtaisen laskutusasiakirjan päivittämiseen lähetysprosessin tuloksena.

### <a name="open-flighted-feature"></a>Väliversion avaaminen
Sähköisen laskun integrointitoiminto on otettu käyttöön väliversion avulla. Väliversiointi on konsepti, jonka ansiosta toiminto voi olla oletusarvoisesti KÄYTÖSSÄ tai POIS KÄYTÖSTÄ. Seuraavat vaiheet mahdollistavat väliversioinnin muussa kuin tuotantoympäristössä. 

1. Suorita seuraava SQL-komento:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)
    
2. Kun olet tehnyt edellä mainitun muutoksen, suorita kaikille AOS-solmuille IISReset

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Sähköisen laskutuksen lisäosan integrointitoiminnon käyttöönotto

1. Kirjaudu Financeen tai Supply Chain Managementiin.
2. Etsi uutta toimintoa **Määritettävä sähköisen laskutuksen lisäosan integrointi** **Toiminnonhallinta**-työtilassa. Jos toimintoa ei vieläkään näy toiminnonhallinnan sivulla, suorita **Hae päivityksiä** -toiminto
3. Valitse toiminto ja valitse sitten **Ota käyttöön nyt**.

### <a name="set-up-the-service-endpoint-url"></a>Palvelun päätepisteen URL-osoitteen määritys

1. Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.
2. Syötä **Järjestelmän päätepisteen URL** -kentän **Lähetyspalvelu**-välilehteen `https://businessdocumentsubmission.us.operations365.dynamics.com/`.
3. Syötä **Ympäristö**-kenttään RCS-määrityksen yhteydessä luomasi sähköisen laskutuksen lisäosaympäristön nimi.

![Palveluparametrien syöttäminen](media/e-invoicing-services-get-started-enter-service-endpoint.png)

### <a name="import-the-er-configurations"></a>ER-määritysten tuominen

Voit ottaa käyttöön liiketoimintatietojen keräämisen ja lähettämisen sähköisen laskutuksen lisäosaan tuomalla ER-tietomallin ja ER-tietomallin määrityksen, jotka liittyvät siihen maa-/aluekohtaiseen sähköisen laskutuksen toimintoon, jota haluat käyttää.

1. Valitse **Sähköisen raportointi** -työtilan **Määrityslähteet** -osassa **Microsoft**. Varmista, että tämän määrityspalvelun arvoksi on määritetty **Aktiivinen**. Tietoja palvelun arvon **Aktiivinen**-muotoon määrittämisestä: [Luo määrityspalveluja ja merkitse ne aktiiviseksi](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Valitse **Säilöt**.
4. Valitse **Yleinen resurssi** ja valitse sitten **Avaa**.
5. Valitse **Yhdistä Lifecycle Servicesiin** -valintaikkunassa **Yhdistä elinkaaripalveluun napsauttamalla tästä**.
6. Sen mukaan, missä maassa tai millä alueella haluat käyttää sähköisen laskutuksen toimintoa, sinun on tuotava sovellettava tietomalli, tietomallin yhdistämismääritys sekä muodot. Tietoja niistä ER-määrityksistä, jotka kannattaa tuoda, esitetään maa-/aluekohtaisessa aiheessa Sähköisen laskutuksen lisäosan käytön aloittaminen.
7. Tuo **Asiakaslaskun kontekstimalli**. Tämä malli sisältää lisäparametreja, jotka kuvaavat muun muassa sen ympäristön Financessa, jota käytetään sähköisen laskutuksen lisäosan kanssa liiketoimintatietoja lähetettäessä.

### <a name="turn-on-countryregion-specific-e-invoicing-features"></a><a name="region-specific"></a>Maa-/aluekohtaisen sähköisen laskutuksen toimintojen käyttöönotto

Jos haluat ottaa käyttöön maa-/aluekohtaisen sähköisen laskutuksen toiminnot siten, että ne toimivat sähköisen laskutuksen lisäosassa, sinun on otettava toiminto käyttöön jokaisessa yrityksessä, jossa haluat käyttää sitä. Tämän jälkeen vanhaa sähköisen laskutuksen integrointia ei voi enää käyttää, ja integrointi uudella sähköisen laskutuksen lisäosalla on käytössä.

1. Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.
2. Valitse maa-/aluekohtaiseen sähköisen laskutuksen toimintoosi liittyvän rivin **Toiminnot**-välilehdellä **Käytössä**-sarakkeen valintaruutu. Tietoja siitä, mikä toiminto kannattaa ottaa käyttöön, esitetään maa-/aluekohtaisessa aiheessa Sähköisen laskutuksen lisäosan käytön aloittaminen.

![Sähköisen laskutuksen toiminnon käyttöönotto](media/e-invoicing-services-get-started-enable-invoicing-feature.png)

> [!NOTE]
> Jos sinulla on useita eri maita tai alueita varten määritettyjä yrityksiä, voit ottaa käyttöön maa-/aluekohtaisen sähköisen laskutuksen toiminnon käyttöön kullekin yritykselle.

### <a name="import-er-configurations-and-set-up-the-response-types-to-update-your-countryregion-specific-invoice-document"></a>Tuo ER-määritykset ja määritä vastaustyypit päivittämään maa-/aluekohtainen laskuasiakirjasi

Jos lähetetty laskuasiakirja vaati päivitystä valtiollisilta hyväksymispalveluilta saadun vastauksen perusteella, kun se on niille lähetetty, sinun on tuota erityinen ER-tietomalli ja määritykset, jotta laskuasiakirjan tai muun lisäkentän tila voidaan muuttaa.

1. Valitse **Sähköisen raportointi** -työtilan **Määrityslähteet** -osassa **Microsoft**.
2. Valitse **Säilöt**.
3. Valitse **Yleinen resurssi** ja valitse sitten **Avaa**.
4. Tuo **Vastausviestin malli**, **Vastausviestin tuontimuoto**, **Vastausviestin mallin yhdistämismääritys kohteeseen** ja **Tiedostosisältöjen tuontimuoto**.
5. Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.
6. Valitse **Sähköinen tiedosto** -välilehdessä **Lisää** syöttääksesi sen taulukon nimen, joka liittyy maa-/aluekohtaiseen laskuasiakirjaasi. Tietoja siitä, mitkä taulukkonimet kannattaa valita, esitetään maa-/aluekohtaisessa aiheessa Sähköisen laskutuksen lisäosan käytön aloittaminen.
7. Määritä vastaustyypit valitsemalla **Vastaustyypit**. Tietoja siitä, mitkä taulukkonimet kannattaa valita, esitetään maa-/aluekohtaisessa aiheessa Sähköisen laskutuksen lisäosan käytön aloittaminen.

![Vastaustyyppien määrittäminen](media/e-invoicing-services-get-started-set-up-response-types.png)

## <a name="e-invoicing-feature-names-by-country"></a>Sähköisen laskutuksen maakohtaiset toimintonimet 
Seuraavassa taulukossa kuvataan muita sähköisen laskutuksen toimintoja, joita voi ladata sähköisen raportoinnin yleisestä säilöstä sähköisten laskujen luomista varten.
RCS:ssä voit ladata tässä taulukossa luetellut sähköisen laskutuksen palvelut, ER-määritykset ja käytettävissä olevat sähköisen laskutuksen toiminnon määritykset.
Financessa voit ottaa käyttöön liittyvän toiminnon viitteet **Sähköisen asiakirjan parametrit** -sivulla luodaksesi sähköisiä laskuja kyseisisä maita varten. Lisätietoja on aiemmin tässä aiheessa osassa [Maa-/aluekohtaisen sähköisen laskutuksen toimintojen käyttöönotto](#region-specific).

| Toiminnon nimi                      | kuvaus                                 | ER-määritykset                                                                                                  | Asetukset                                                                                                                                                         | Maa/alue  | Ominaisuuden viite      |
|-----------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|------------------------|
| Itävallan sähköiset laskut (AT) | Myynti- ja projektilaskut Itävallassa      | - OIOUBL-myyntilasku <br>- OIOUBL-projektilasku <br>- OIOUBL, myynnin hyvityslasku <br>- OIOUBL, projektin hyvityslasku | - Myyntilaskujen luonti (AT) <br>- Projektilaskujen luonti (AT) <br>- Myynnin hyvityslaskujen luonti (AT) <br>- Projektien hyvityslaskujen luonti (AT)         | Itävalta         | EUR-00023              |
| Belgian sähköinen lasku (BE)   | Myynti- ja projektilaskut Belgiassa      | - UBL-myyntilasku BE <br>- UBL-projektilasku BE <br>- UBL, projektin hyvityslasku, BE <br>- UBL, myynnin hyvityslasku, BE | - Myyntilaskujen luonti (BE)<br>- Projektilaskujen luonti (BE) <br>- Myynnin hyvityslaskujen luonti (BE) <br>- Projektien hyvityslaskujen luonti (BE)         | Belgia         | EUR-00023              |
| Tanskan sähköinen lasku (DK)    | Myynti- ja projektilaskut Tanskassa      | - OIOUBL-myyntilasku <br>- OIOUBL-projektilasku <br>- OIOUBL, myynnin hyvityslasku <br>- OIOUBL, projektin hyvityslasku | - Myyntilaskujen luonti (DK) <br>- Projektilaskujen luonti (DK) <br>- Myynnin hyvityslaskujen luonti (DK)<br>- Projektien hyvityslaskujen luonti (DK)         | Tanska         | EUR-00023<br> DK-00001 |
| Alankomaiden sähköinen lasku (NL)     | Myynti- ja projektilaskut Alankomaissa  | - UBL-myyntilasku NL <br>- UBL-projektilasku NL <br>- UBL, myynnin hyvityslasku, NL <br>- UBL, projektin hyvityslasku, NL | - Myyntilaskujen luonti (NL) <br> - Projektilaskujen luonti (NL) <br> - Myynnin hyvityslaskujen luonti (NL) <br>- Projektien hyvityslaskujen luonti (NL)          | Alankomaat | EUR-00023              |
| Viron sähköinen lasku (EE)  | Myynti- ja projektilaskut Virossa      | - Myyntilasku (EE) <br> - Projektilasku (EE)                                                                     | - Myyntilaskujen luonti (EE) <br>- Projektilaskujen luonti (EE)                                                                                           | Viro         | EUR-00023              |
| Suomen sähköinen lasku (FI)   | Myynti- ja projektilaskut Suomessa      | - Myyntilasku (FI) <br>- Projektilaskujen luonti (FI)                                                          | - Myyntilaskujen luonti (FI) <br>- Projektilaskujen luonti (FI)                                                                                           | Suomi         | EUR-00023              |
| Ranskan sähköinen lasku (FR)    | Myynti- ja projektilaskut Ranskassa    | - UBL-myyntilasku (FR) <br> - UBL-projektilasku FR <br> - UBL, myynnin hyvityslasku, FR <br>- UBL, projektin hyvityslasku, FR | - Myyntilaskujen luonti (FR) <br> - Projektilaskujen luonti (FR) <br>- Myynnin hyvityslaskujen luonti (FR) <br>- Projektien hyvityslaskujen luonti (FR)         | Ranska          | EUR-00023              |
| Saksan sähköinen lasku (DE)    | Myynti- ja projektilaskut Saksassa      |- Myyntilasku (DE) <br> - Projektilasku <DE>                                                                     | - Myyntilaskujen luonti (DE) <br>- Projektilaskujen luonti (DE)                                                                                           | Saksa         | EUR-00023              |
| Norjan sähköinen lasku (NO) | Myynti- ja projektilaskut Norjassa       | - OIOUBL-myyntilasku <br>- OIOUBL-projektilasku <br>- OIOUBL, myynnin hyvityslasku <br>- OIOUBL, projektin hyvityslasku | - Myyntilaskujen luonti (NO) <br>- Projektilaskujen luonti (NO) <br>- Myynnin hyvityslaskujen luonti (NO) <br>- Projektien hyvityslaskujen luonti (NO)          | Norja          | EUR-00023<br> NO-00010 |
| Espanjan sähköinen lasku (ES)   | Myynti- ja projektilaskut Espanjassa        | - Myyntilasku (ES) <br>- Projektilasku (ES)                                                                     | - Myyntilaskujen luonti (ES) <br>- Projektilaskujen luonti (ES)                                                                                           | Espanja           | EUR-00023 <br>ES-00025 |
| Italian sähköinen lasku (IT)   | Myynti- ja projektilaskut Italiassa        | - (Esikatselu) Myyntilasku (IT) <br> - Projektilasku (IT)                                                           | - Myyntilasku <br> - Projektilasku                                                                                                                           | Italia           | EUR-00023 <br>IT-00036 |
| Sähköinen PEPPOL-lasku         | PEPPOL-myynti- ja projektilaskujen luonti | - PEPPOL-myyntilasku <br>- PEPPOL-projektilasku <br>- PEPPOL, myynnin hyvityslasku <br> - PEPPOL, projektin hyvityslasku | - PEPPOL-myyntilaskujen luonti <br>- PEPPOL-projektilaskujen luonti <br>- PEPPOL, myynnin hyvityslaskujen luonti <br>- PEPPOL, projektien hyvityslaskujen luonti |                 | EUR-00023              |


## <a name="electronic-invoice-processing-in-finance-and-supply-chain-management"></a>Sähköinen laskujen käsittely Financessa ja Supply Chain Managementissa

Käsittelyn aikana suoritat seuraavat tehtävät:

1. Liiketoiminta-asiakirjan (lasku) lähettäminen sähköisen laskutuksen lisäosalla.
2. Lähetyksen suorituslokien tarkastelu.

### <a name="submit-business-documents"></a>Liiketoiminta-asiakirjojen lähettäminen

Säännöllisen lähetysprosessin aikana asiakkaan ja sähköisen laskutuksen lisäosan välinen yhteys on kaksisuuntainen. Tarkoituksena on suorittaa kaksi päätehtävää sähköisten asiakirjojen toimittamisen aikana:

1. Lähettää kaikki sähköiset asiakirjat, jotka odottavat lähetystä Financesta, joiden tila on oikea lähettämistä varten ja jotka täyttävät valintaperusteet.
2. Tuo Financeen vastaus, jonka sähköisen laskutuksen lisäosa palauttaa aiemmin lähetettyjen sähköisten asiakirjojen osalta. Tuonnin jälkeen vastaukset jäsennetään ja liiketoiminta-asiakirjojen tila päivitetään sen mukaisesti.

Voit lähettää liiketoiminta-asiakirjoja joko manuaalisesti tai aikatauluvaatimusten perusteella.

1. Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Lähetä sähköisiä asiakirjoja**.
2. Kun mikä tahansa asiakirja lähetetään ensimmäistä kertaa, määritä **Lähetä asiakirjat uudelleen** -asetukseksi aina **Ei**. Jos sinun on lähetettävä asiakirja uudelleen palvelun kautta, määritä asetukseksi **Kyllä**.
3. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** avataksesi **Kysely**-valintaruudun, jossa voit muodostaa kyselyn lähetettävien asiakirjojen valitsemista varten.

![Sähköisten asiakirjojen lähettämisen valintaruutu](media/e-invoicing-services-get-started-submission-form.png)

### <a name="filter-query"></a>Suodatinkysely

1. Syötä **Alue**-välilehden **Tiedustelu**-valintaikkunaan suodatusperusteet käyttämällä kenttiä **Taulukko**, **Johdettu taulukko**, **Kenttä** ja **Perusteet**.
2. Lisää liiketoiminta-asiakirjojen valintaan tarvittava määrä lisäperusteita valitsemalla **Lisää**.

    ![Lähetyksen suodatusehtojen määrittäminen](media/e-invoicing-services-get-started-set-up-submission-filter-criteria.png)

3. Valitse **OK**, jotta voit sulkea **Kysely**-valintaikkunan.
4. Lähetä valitut liiketoiminta-asiakirjat sähköisen laskutuksen lisäosaan valitsemalla **OK**.

    > [!NOTE]
    > Kun yrität lähettää asiakirjan palvelun kautta ensimmäisen kerran, järjestelmä pyytää vahvistamaan yhteyden sähköisen laskutuksen lisäosaan. Valitse **Yhdistä sähköisten asiakirjojen lähetyspalveluun napsauttamalla tätä**.
    >
    > ![Yhdistä sähköisten asiakirjojen lähetyspalveluun viestiruutuun](media/e-invoicing-services-get-started-dialog-form-connect-e-Invoicing-services.png)
    >
    > Jos yhteyden muodostaminen onnistuu, näyttöön tulee vahvistusviesti.
    >
    > ![Sähköisen laskutuksen lisäosan yhteyden vahvistus](media/e-invoicing-services-get-started-confirmation-connection-e-invoicing-services.png)

5. Sulje valintaikkuna.

> [!NOTE]
> Kunkin lähetyksen jälkeen toimintokeskuksessa näkyy lähetettyjen asiakirjojen määrä.
>
> ![Toimintokeskuksen viestit](media/e-invoicing-services-get-started-view-action-center-messages.png)

### <a name="submission-by-batch"></a>Erälähetys

Asiakirjojen manuaalisen lähettämisen sijaan voit automatisoida lähetysprosessin ja suorittaa sen taustalla määritetyn eräsuoritustiheyden perusteella.

1. Määritä **Lähetä sähköisiä asiakirjoja** -valintaruudussa **Suorita taustalla** -pikavälilehdessä **Eräkäsittely**-asetuksen arvoksi **Kyllä**.
2. Määritä käsittelytaajuus **Toistuvuus**-välilehdessä.

![Erälähetyksen määritys](media/e-invoicing-services-get-started-set-up-submission-batch.png)

### <a name="view-all-submission-logs"></a>Kaikkien lähetyslokien tarkastelu

1. Siirry kohtaan **Organisaation hallinta \> Säännölliset \> Sähköiset asiakirjat \> Sähköisen asiakirjan lähetysloki**.
2. Valitse suodatusperusteena toimiva asiakirjatyyppi **Asiakirjatyyppi**-kentässä.

    ![Asiakirjatyypin valinta lähetyslokien tarkastelua varten](media/e-invoicing-services-get-started-select-document-type-for-viewing-submission-log.png)

    > [!IMPORTANT]
    > **Lähetystila** -sarakkeessa näkyvä arvo edustaa tilaa, joka liittyy itse lähetysprosessin valmistumiseen. Se ilmaisee, onko RCS:ssä määritetty toimintokulku suoritettu loppuun riippumatta siitä, hyväksyttiinkö vai hylättiinkö sähköinen asiakirja. **Lähetyksen tila** -sarakkeen arvo ei edusta lähetetyn asiakirjan tilaa. Voit tarkastella lähetetyn tiedoston tilaa (eli sitä, onko asiakirja hyväksytty vai hylätty) **Käsittelytoimen loki** -pikavälilehden lähetyslokitiedoissa, kuten seuraavassa kuvataan.

3. Valitse toimintoruudussa **Tiedustelut \> Lähetystiedot**.
4. Näytä lähetyslokitiedot.

    ![Lähetyslokin tiedot](media/e-invoicing-services-get-started-view-submission-log-form.png)

Lähetyslokissa näkyvät tulokset määräytyvät sen mukaan, miten sähköisen laskutuksen toiminto on määritetty RCS:ssä. Lähetyslokilla on kuitenkin määrityksestä riippumatta kolme pikavälilehteä:

- **Käsittelytoimet** – Tässä pikavälilehdessä näkyy RCS:ssä määritetyssä toimintoversiossa määritettyjen toimien suoritusloki. **Tila**-sarakkeessa näkyy, suoritettiinko toimi onnistuneesti.
- **Toimitiedostot** – Tässä pikavälilehdessä näkyvät välitiedostot, jotka luotiin toimien suorittamisen aikana. Voit ladata tiedoston ja tarkastella sen sisältöä valitsemalla **Näytä**.
- **Käsittelytoimen loki** – Tässä pikavälilehdessä näkyvät sähköisen laskutuksen lisäosan ja kohteena olevan verkkopalvelun välisen tiedonsiirron tulokset. Siinä näkyy myös, mitä verkkopalvelun käsittely palautti.

## <a name="related-topics"></a>Liittyvät aiheet

- [Sähköisen laskutuksen yleiskatsaus](e-invoicing-service-overview.md)
- [Brasilian sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-bra-get-started.md)
- [Meksikon sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-mex-get-started.md)
- [Italian sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-ita-get-started.md)
- [Sähköisen laskutuksen lisäosan määrittäminen](e-invoicing-setup.md)
