---
title: Testauksen automatisointi sähköisen raportoinnin avulla
description: Tässä ohjeaiheessa käsitellään sähköisen raportointi- eli ER-kehyksen perustoiminnolla tapahtuvaa toimintojen automaattista testaamista.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: be641e1b2f90f4d19f7ed15e47413c0aa43d5073
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771441"
---
# <a name="automate-testing-with-electronic-reporting"></a>Testauksen automatisointi sähköisen raportoinnin avulla

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa selitetään, miten sähköisen raportointi- eli ER-kehyksellä automatisoidaan joidenkin toimintojen testaus. Ohjeaiheen esimerkin avulla näytetään, miten toimittajan maksujen käsittely automatisoidaan.

Sovellus luo ER-kehyksen avulla maksutiedostot ja vastaavat asiakirjat toimittajan maksujen käsittelyn aikana. ER-kehys sisältää tietomallin, mallien yhdistämismääritykset ja muoto-osia, jotka tukevat eri maksutyyppien maksujen käsittelyä ja eri muotoisten asiakirjojen luontia. Nämä osat voi ladata Microsoft Dynamics Lifecycle Servicesistä (LCS) ja tuoda esiintymään.

Voit myös mukauttaa kutakin Microsoft-osaa ja käyttää sitä oman mukautetun osan perustana. Luomalla mukautetun version voit tehdä tiettyjä tarpeita tukevia muutoksia. Voit esimerkiksi säätää ER-tietomallin ja ER-mallin yhdistämismäärityksen käyttämään asiakaskohtaista sovellustietoa tai voit muuttaa ER-muodon muokkaamaan luodun asiakirjan asettelua.

Voit käyttää mukautettuja ER-muotoja toimittajan maksuja luovien maksutiedostojen käsittelyyn. Voit käsitellä niillä myös tarkistusraportteja. Versiointia tuetaan ER-osissa. Microsoft voikin tämän vuoksi toimittaa toimittajan maksujen käsittelyn ER-ratkaisujen päivitetyt versiot, ja voit automaattisesti yhdistää päivitetyn version mukautettuun osaa pohjustamalla sen. Pohjustettu versio on kuitenkin testattava, jotta voidaan varmistaa, että toimii odotetulla tavalla.

ER-tietomallit ja ER-mallin yhdistämismääritykset ovat yleisiä useissa ER-muodoissa, joilla käsitellään eri tyyppisiä maksuja ja luodaan maa- tai aluekohtaisia maksuasiakirjoja. Tämän vuoksi käyttäjän hyväksynnän tai integroinnin testauksen automatisointi on erittäin toivottavaa, jolloin testaus voidaan tehdä automaattisesti useissa yrityksissä esimerkiksi siten, että kunkin kohdeyrityksen maa- tai aluekonteksti otetaan huomioon ja käytetään eri tietojoukkoja.

Lisätietoja konfiguraation lähteestä vastaanotettuun muotoon perustuvan muodon mukautetun version luomisesta on kohteessa [ER Muodon päivittäminen ottamalla käyttöön kyseisen muodon uusi perusversio](./tasks/er-upgrade-format.md).

## <a name="key-concepts"></a>Avainkäsitteet

Tehotoimintokäyttäjät voivat laatia käyttäjän hyväksyntä- ja integrointitestauksen lähdekoodia kirjoittamatta.

- Vertaa luotuja asiakirjoja pääversioihin ER-perustoiminnolla. Lisätietoja on kohdassa [Luotujen raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md)
- Tallenna testitapauksen tehtävän tallennustoiminnolla ja sisällytä perusarviointi. Lisätietoja on kohdassa [Tehtävän tallennustoiminnon resurssit](../user-interface/task-recorder.md).
- Ryhmitä tarvittavien testiskenaarioiden testitapaukset. Lisätietoja kohdassa [Käyttäjän hyväksymistestien luominen ja automatisointi](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).

    - Muodosta käyttäjän hyväksyntätestien kirjastoja LCS:n liiketoimintaprosessien mallintajalla (BPM).
    - Luo Microsoft Azure DevOps Servicesissä (Azure DevOps) testisuunnitelma ja testisarjoja BPM-testikirjastojen avulla.

Tehotoimintakäyttäjät voivat suorittaa käyttäjän hyväksyntä- ja integrointitestejä.

- Suorita toivotun testisarjan testitapaukset Regression Suite Automation Tool (RSAT) -työkalulla.
- Raportoi testauksen tulokset Azure DevOpsiin ja tutustu kyseisiin tuloksiin tässä palvelussa.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit suorittaa tämän ohjeaiheen tehtäviä, seuraavien edellytysten on toteuduttava:

- Ota käyttöön testauksen automatisointia tukeva topologia. Sinulla on oltava tämän topologiaesiintymän **Järjestelmänvalvoja**-rooli. Topologian on sisällettävä tässä esimerkissä käytettävät demotiedot. Lisätietoja on kohdassa [Jatkuvaa koonnin ja testauksen automaatiota tukevien topologioiden käyttöönotto ja käyttäminen](../perf-test/continuous-build-test-automation.md).
- Voit suorittaa käyttäjän hyväksyntä- ja integrointitestit automaattisesti asentamalla RSAT-työkalu käytössä olevaan topologiaan ja tekemällä tarvittavat määritykset. Lisätietoja RSAT-työkalun asentamisesta ja sen määrittämisestä Finance and Operations -sovelluksissa ja Azure DevOpsissa käytettäväksi on kohdassa [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357). Ota huomioon työkalun käytön edellytykset. Seuraavassa kuvassa on esimerkki RSAT-asetuksista. Sinisen suorakulmion sisällä ovat parametrit, jotka määrittävät Azure DevOps -käytön. Vihreän suorakulmion sisällä on parametrit, jotka määrittävät esiintymän käyttöoikeudet.

    ![RSAT-asetukset](media/GER-Configure.png "Näyttökuva RSAT-asetukset-valintaikkunasta")

- Voit varmistaa testitapausten oikean suoritusjärjestyksen järjestämällä testitapaukset sarjoiksi. Voit kerätä tällä tavoin testauksen suorituslokeja lisäraportointia ja perehtymistä varten. Tätä varten tarvitaan käyttöönotetun topologian Azure DevOpsin käyttöoikeus.
- Tämän ohjeaiheen esimerkin suorittamista varten kannattaa ladata [RSAT-testien ER-käyttö](https://go.microsoft.com/fwlink/?linkid=874684). Tämä zip-tiedosto sisältää seuraavat tehtäväoppaat:

    | Sisältö                                           | Tiedoston nimi ja sijainti |
    |---------------------------------------------------|------------------------|
    | Tehtävätallennenäyte tietojen valmisteluun testausta varten | Prepare\\Recording.xml |
    | Tehtävätallennenäyte toimittajan maksujen käsittelyyn   | Process\\Recording.xml |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a>Ostoreskontra-moduulin valmisteleminen käsittelemään toimittajan maksuja

1. Kirjaudu sisään esiintymääsi.
2. Lataa seuraavat ER-konfiguraatiot LCS:stä. Ohjeet ovat kohdassa [ER Tuo konfiguraatio Lifecycle Services -palvelusta](./tasks/er-import-configuration-lifecycle-services.md).

    - **Maksumalli** ER-mallikonfiguraatio
    - **Maksumallin yhdistämismääritys 1611** ER-mallin yhdistämismääritys
    - **BACS (UK)** ER-muotokonfiguraatio

    ![Sähköisen raportoinnin konfiguraatiot](media/GER-Configurations.png "Näyttökuva sähköisen raportoinnin Konfiguroinnit-sivusta")

3. **GBSI**-demotietoyritys, sillä sen alue- tai maakonteksti on Iso-Britannia.
4. Määritä ostoreskontran parametrit:

    1. Valitse **Ostoreskontra \> Maksun asetukset \> Maksutavat**.
    2. Valitse maksutavaksi **Sähköinen**.
    3. Määritä valittu maksutapa käyttämään aiemmin toimittajan maksujen käsittelyä varten ladattua **BACS (UK)** -ER-muotoa:

        1. Määritä **Tiedostomuodot**-pikavälilehden **Yleinen sähköinen vientimuoto** -asetukseksi **Kyllä**.
        2. Valitse **Vie muotokonfiguraatio** -kentässä **BACS (UK)**.

    ![Maksutavat-sivu](media/GER-APParameters.png "Näyttökuva Maksutavat-sivusta")

    > [!NOTE]
    > Jos sinulla on tämän ER-muodon johdettu versio, joka luotiin tukemaan mukautuksia, voit valita tämän konfiguraation **Sähköinen**-maksutavassa.

5. Luo toimittajan maksuesimerkki:

    1. Valitse **Ostoreskontra \> Maksut \> Maksukirjauskansio**.
    2. Varmista, ettei maksukirjauskansioon ole tehty kirjausta.

        ![Maksukirjauskansio-sivu](media/GER-APJournal.png "Näyttökuva Maksukirjauskansio-sivusta")

    3. Valitse **Rivit**ja lisää rivi, jossa on seuraavat tiedot.

        | Kenttä               | Esimerkkiarvo   |
        |---------------------|-----------------|
        | Toimittajan nimi         | GB\_SI\_000001  |
        | Veloitus               | 1,000.00        |
        | Valuutta            | GBP             |
        | Vastatilityyppi | Pankki            |
        | Vastatili      | GBSI OPER       |
        | Maksutapa   | Sähköinen      |

    ![Toimittajan maksut -sivu](media/GER-APJournalLines.png "Näyttökuva Toimittajan maksut -sivusta")

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a>ER-kehyksen valmisteleminen toimittajan maksujen käsittelyn testaamiseen

### <a name="configure-er-parameters"></a>Konfiguroi ER-parametrit

1. Valitse **Organisaation hallinto \> Sähköinen raportointi \> Sähköisen raportoinnin parametrit**.
2. Valitse **Liitteet**-välilehden **Perusrivi**-kentässä **Tiedosto** asiakirjatyypiksi, jota tiedostonhallinta- eli DM-kehys käyttää säilyttämään perustoimintoon DM-liitteinä liittyviä tiedostoja.

    ![Sähköisen raportoinnin parametrit -sivu](media/GER-ERParameters.png "Näyttökuva Sähköisen raportoinnin parametrit -sivusta")

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a>Toimittajan maksuihin liittyvien asiakirjojen peruskopioiden luominen

1. Valitse **Ostoreskontra \> Maksut \> Maksukirjauskansio**.
2. Valitse **Rivit**.
3. Valitse **Muodosta maksut**.
4. Valitse maksutavaksi **Sähköinen**.
5. Valitse **GBSI OPER** -pankkitili.
6. Määritä **Tulosta valvontaraportti** -asetukseksi **Kyllä**.
7. Lataa tulos zip-tiedostona.
8. Avaa ladattu tiedosto.
9. Pura seuraavat tiedostot ladatusta tiedostosta:

    - **Tiedosto**-maksutiedosto tekstimuotoisena
    - **ERVendOutPaymControlReport**-valvontaraporttitiedosto XLSX-muodossa

    ![Puretut tiedostot](media/GER-APJournalProcessed.png "Näyttökuva puretuista tiedostonimissä Windowsin Resurssienhallinnassa")

### <a name="turn-on-the-er-baseline-feature"></a>ER-perusrivitoiminnon ottaminen käyttöön

1. Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.
2. Valitse toimintoruudun **Konfiguroinnit**-välilehdessä **Käyttäjän parametrit**.
3. Määritä **Suorita virheenkorjaustila** -asetukseksi **Kyllä**.

**Suorita vianmääritystilassa** -parametrin ottaminen käyttöön pakottaa ER-kehyksen suorittamaan seuraavat toiminnot sen jälkeen, kun lähteviä asiakirjoja luova ER-muoto on suoritettu:

1. Määritetään, määritettiinkö millekään suoritetun ER-muodon osalle perusrivi.
2. Määritetään, yksi kerrallaan soveltuuko määritetty perusrivi nykyiseen tilanteeseen (esimerkiksi kirjautuneen yrityksen yrityskoodi sekä tuloksen tiedostonimi ja tiedostotunniste).
3. Kunkin soveltuvan perusrivin kohdalla tehdään seuraavat toiminnot:

    1. ER-muodon suorituksen aikana luotua tulosta verrataan vastaavaan perusriviin.
    2. Vertailun tulokset tallennetaan ER-konfiguraatioiden virheenkorjauslokiin.

### <a name="configure-er-baselines-for-vendor-payment-processing"></a>ER-perusrivien määrittäminen toimittajan maksujen käsittelyä varten

1. Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.
2. Valitse **Perusrivit**.
3. Valitse **Uusi**.
4. Valitse **Viite**-kentässä **BACS (UK)** -muoto.
5. Valitse **Liitteet**.
6. Lisää uusi toimittajan maksutiedoston perusrivi:

    1. Valitse **Uusi**.
    2. Tallenna perusrivin tiedot valitsemalla **Tyyppi**-kentässä se**Tiedosto**-DM-asiakirjatyyppi, jonka määritit ER-parametreissa.
    3. Siirry valitsemaan paikallisesti tallennettu tekstimuotoinen **Tiedosto**-maksutiedosto.
    4. Kirjoita **Kuvaus**-kenttään **Maksun TXT-tiedosto**.

7. Lisää toimittajan maksujen seurantaraportin uusi perusrivi:

    1. Valitse **Uusi**.
    2. Tallenna perusrivin tiedot valitsemalla **Tyyppi**-kentässä se**Tiedosto**-DM-asiakirjatyyppi, jonka määritit ER-parametreissa.
    3. Siirry valitsemaan paikallisesti tallennettu XLSX-muotoinen **ERVendOutPaymControlReport**-seurantatiedosto.
    4. Kirjoita **Kuvaus**-kenttään **Maksun XLSX-seurantaraportti**.

    ![Toimittajan maksutiedoston ja seurantaraportin perusrivit](media/GER-BaselineAttachments.png "Näyttökuva Konfiguroinnit-sivusta, jossa valittuna Maksun XLSX-seurantaraportti")

8. Sulje sivu.
9. Määritä maksutiedoston perusrivi valitsemalla **Perusrivit**-pikavälilehdessä **Uusi**.

    1. Anna rivin nimeksi **Maksutiedoston perusriviasetus**.
    2. Valitse **Tiedosto-osan nimi**-kentässä **tiedosto**. Tätä perusriviä käytetään nyt ER-muodon tuloksessa, joka luo maksutiedoston BACS (UK) -tekstimuodossa.
    3. Valitsemalla **Yritykset**-kentässä **GBSI** voit käyttää tätä perusriviä, kun **BACS (UK)** -ER-muoto suoritetaan GBSI-yrityksessä.
    4. Jos **Tiedostonimen peite** -kentässä annetaan **\*.TXT**, tätä perusriviä käytetään vain niissä **tiedosto**-muoto-osan tuloksissa, joiden tiedostotunniste on **.txt**.
    5. Valitse **Perusrivi**-kentässä **Maksun TXT-tiedosto**, jolloin tätä perusriviä käytetään verratessa luotua tulosta.

10. Määritä seurantaraportin perusrivi valitsemalla **Uusi**.

    1. Anna rivin nimeksi **Seurantaraportin perusriviasetus**.
    2. Valitse **Tiedosto-osan nimi**-kentässä **ERVendOutPaymControlReport**. Tätä perusriviä käytetään nyt ER-muodon tuloksessa, joka luo seurantaraportin.
    3. Valitsemalla **Yritykset**-kentässä **GBSI** voit käyttää tätä perusriviä, kun **BACS (UK)** -ER-muoto suoritetaan GBSI-yrityksessä.
    4. Jos **Tiedostonimen peite** -kentässä annetaan **\*.XLSX**, tätä perusriviä käytetään vain niissä **ERVendOutPaymControlReport**-muoto-osan tuloksissa, joiden tiedostotunniste on **.xslx**.
    5. Valitse **Perusrivi**-kentässä **Maksun XLSX-seurantaraportti**, jolloin tätä perusriviä käytetään verratessa luotua tulosta.

    ![Konfigurointi-sivun Perusrivit-pikavälilehti](media/GER-BaselineRules.png "Näyttökuva Konfigurointi-sivun Perusrivit-pikavälilehdestä")

## <a name="record-tests-to-validate-vendor-payment-processing"></a>Testien tallentaminen toimittajan maksujen käsittelyn tarkistamiseen

Voit tehotoimintakäyttäjänä tallentaa ovat toimittajan maksujen käsittelyn testivaiheet. Aiemmin ladattu **Prepare\\Recording.xml** -tehtävätallenne kannattaa toistaa (ja muokata tarvittaessa). Tämän tallenteen avulla voi määrittää oikean tilan kaikille testitiedoille. Kyseinen vaihe on pakolinen, sillä testaus voidaan tehdä useita kertoja ja jokaisen testin on käytettävä tietoja, joilla on sama tila.

### <a name="reset-user-settings"></a>Käyttäjäasetusten nollaaminen

1. Avaa oletuskoontinäyttö.
2. Valitse **Asetukset**-painike (rataskuvake).
3. Valitse **Käyttäjäasetukset**.
4. Valitse **Käyttötiedot**.
5. Valitse **Nollaa**.
6. Vahvista, että haluat nollata käyttötiedot valitsemalla **Kyllä**.
7. Sulje sivu.

### <a name="record-the-steps-to-prepare-data-for-testing"></a>Tiedostojen testauksen valmisteluvaiheiden tallentaminen

1. Valitse **Asetukset**-painike (rataskuvake).
2. Valitse **Tehtävän tallennustoiminto**.
3. Valitset **Toista tallenne**.
4. Valitse **Avaa tältä tietokoneelta**.
5. Valitse **Selaa** ja tallenna sitten **Prepare\\Recording.xml**-tiedosto paikallisesti.
6. Valitse **Aloita**.
7. Valitse **Toista seuraava odottava vaihe** niin monta kertaa, että kaikki tallenteen vaiheet on toistettu.

Tämä tehtävätallenne suorittaa seuraavat toimenpiteet:

1. Käsitellyn maksurivin tilaksi määritetään **Ei mitään**.

    ![Tehtävätallenteen vaiheet 3–4](media/GER-Recording1Review1.png "Näyttökuva tehtävätallenteen vaiheista 3–4")

2. Ota käyttäjän **Suorita virheenkorjaustilassa** -ER-parametri käyttöön.

    ![Tehtävätallenteen vaiheet 9–10](media/GER-Recording1Review2.png "Näyttökuva tehtävätallenteen vaiheista 9–10")

3. Tyhjennä ER-virheenkorjausloki, joka sisältää luotujen tiedostojen ja perusrivien vertailutulokset.

    ![Tehtävätallenteen vaiheet 13–15](media/GER-Recording1Review3.png "Näyttökuva tehtävätallenteen vaiheista 13–15")

### <a name="record-the-steps-to-test-vendor-payment-processing"></a>Toimittajan maksujen käsittelyn testausvaiheiden tallentaminen

Aiemmin ladattu **Process\\Recording.xml** -tehtävätallenne kannattaa toistaa (ja muokata tarvittaessa). Tätä tallennetta käytetään toimittajan maksujen käsittelemiseen sekä luotujen asiakirjojen ja vastaavien perusrivien vertailutulosten tarkistamiseen.

1. Valitse **Asetukset**-painike (rataskuvake).
2. Valitse **Tehtävän tallennustoiminto**.
3. Valitset **Toista tallenne**.
4. Valitse **Avaa tältä tietokoneelta**.
5. Valitse **Selaa** ja valitse sitten paikallisesti tallennettu **Process\\Recording.xml**-tiedosto.
6. Valitse **Aloita**.
7. Valitse **Toista seuraava odottava vaihe** niin monta kertaa, että kaikki tallenteen vaiheet on toistettu.

Tämä tehtävätallenne suorittaa seuraavat toimenpiteet:

1. Aloita toimittajan maksujen käsittely.
2. Valitse oikeat suorituksenaikaiset parametrit ja ota seurantaraportin luonti käyttöön.

    ![Tehtävätallenteen vaiheet 3–8](media/GER-Recording2Review1.png "Näyttökuva tehtävätallenteen vaiheista 3–8")

3. Siirry ER-virheenkorjauslokiin kirjaamaan luotujen tulosten ja vastaavien perusrivien vertailutulokset.

    Vertailun tulokset näkyvät ER-virheenkorjauslokissa **Luotu teksti** -kentässä. **Muoto-osa**- ja **Lokimerkinnän aiheuttaneen muodon polku** -kentät viittaavat tiedosto-osaan, jolle luotua tulosta on verrattu perusriviin.

    ![Merkinnät Sähköisen raportoinnin ajolokit -sivulla](media/GER-ERDebugLog.png "Näyttökuva Sähköisen raportoinnin ajon lokit -sivusta")

4. Nykyisen tuloksen ja perusrivin vertailu tallennetaan käyttämällä tehtävän tallennustoiminnon **Tarkista**-asetusta ja valitsemalla **Nykyinen arvo**.

    ![Tarkista-asetuksen käyttäminen nykyisen arvon vertailussa](media/GER-TRRecordValidation.png "Näyttökuva Tarkista-asetuksen käyttämisestä nykyisen arvon vertailussa")

    Seuraava kuva osoittaa, miltä tallennetut tarkistusvaiheet näyttävät tehtävätallenteessa.

    ![Tehtävätallenteen vaiheet 13–15](media/GER-Recording2Review2.png "Näyttökuva tehtävätallenteen vaiheista 13–15")

## <a name="add-the-recorded-tests-to-azure-devops"></a>Tallennettujen testien lisääminen Azure DevOpsiin

1. Avaa Azure DevOps -ympäristö.
2. Valitse projekti, jonka määritit RSAT-parametreissa [työkalua määritettäessä](#prerequisites).
3. Valitse testisuunnitelma, jonka määritit RSAT-parametreissa [työkalua määritettäessä](#prerequisites).
4. Luo uusi testitapaus valitulle testisuunnitelmalle:

    1. Anna testitapaukselle nimi **Tietojen valmistelu testaamaan toimittajan sähköisten maksujen käsittelyä**.
    2. Liitä aiemmin ladattu **Recording.xml**-tiedosto **Prepare**-kansiosta.

5. Luo uusi testitapaus valitulle testisuunnitelmalle:

    1. Anna testitapaukselle nimeksi **Toimittajan maksujen testaaminen käyttämällä ER-muotoa BACS (UK)**.
    2. Liitä aiemmin ladattu **Recording.xml**-tiedosto **Process**-kansiosta.

    ![Valitun testisuunnitelman uudet testitapaukset](media/GER-RSAT-DevOps-Tests-Passed.png "Näyttökuva valitun testisuunnitelman uusista testitapauksista")

> [!NOTE]
> Varmista, että testit lisätään oikeassa suoritusjärjestyksessä.

## <a name="prepare-rsat-to-run-the-recorded-tests"></a>RSAT-valmistelu suorittamaan tallennetut testit

### <a name="load-the-tests-from-azure-devops-to-rsat"></a>Testien lataaminen Azure DevOpsista RSAT-työkaluun

1. Avaa paikallinen RSAT-sovellus nykyisessä topologiassa.
2. Lataa tällä hetkellä Azure DevOpsissa sijaitsevat testit RSAT-työkaluun valitsemalla **Lataa**.

    ![RSAT-työkaluun ladatut testit](media/GER-RSAT-RSAT-Tests-Loaded.png "Näyttökuva RSAT-työkaluun ladatuista testeistä")

### <a name="create-automation-and-parameters-files"></a>Automaatio- ja parametritiedostojen luominen

1. Valitse RSAT-työkalussa Azure DevOpsista ladatut testit.
2. Luo RSAT-työkalun automaatio- ja parametritiedostot valitsemalla **Uusi**.

    ![RSAT-työkalussa luodut automaatio- ja parametritiedostot](media/GER-RSAT-RSAT-Tests-Initiated.png "Näyttökuva RSAT-työkalussa luoduista automaatio- ja parametritiedostoista")

### <a name="modify-the-parameters-files"></a>Parametritiedostojen muokkaaminen

1. Valitse RSAT-työkalussa **Tietojen valmistelu testaamaan toimittajan sähköisten maksujen käsittelyä** -testitapaus.
2. Valitse **Muokkaa**.
3. Muuta avatun Microsoft Excel -työkirjan **Yleiset**-laskentataulukossa yrityksen koodiksi **GBSI**, sillä tätä yritystä käytetään testiä suorittamiseen.
4. Valitse RSAT-työkalussa **Toimittajan maksujen testaaminen käyttämällä ER-muotoa BACS (UK)** -testitapaus.
5. Valitse **Muokkaa**.
6. Muuta avoimen Excel-työkirjan **Yleiset**-laskentataulukossa yrityksen koodiksi **GBSI**.
7. Huomaa, että **ERFormatMappingRunLogTable**-laskentataulukon soluissa A:3 and C:3 niiden ER-virheenkorjauslokitaulun kenttien teksti, joilla tarkistettiin tuloksen ja perusrivin vertailun tulokset. Näillä teksteillä arvioidaan testin suorittamisen aikana luotavia ER-virheenkorjauslokin tietueita.

    ![ERFormatMappingRunLogTable-laskentataulukko](media/GER-RSAT-RSAT-ExcelParameters.png "Näyttökuva ERFormatMappingRunLogTable-laskentataulukosta")

## <a name="run-the-tests-and-analyze-the-results"></a>Testien suorittaminen ja tulosten analysoiminen

### <a name="run-the-tests-in-rsat"></a>Testien suorittaminen RSAT-työkalussa

1. Valitse ladatut testit RSAT-työkalussa.
2. Valitse **Suorita**.

Huomaa, että testitapaukset suoritetaan automaattisesti sovelluksessa selainta käyttämällä.

### <a name="analyze-the-results-of-test-execution"></a>Suoritetun testin tulosten analysoiminen

Suoritetun testin tulokset tallennetaan RSAT-työkaluun. Huomaa, että molemmat testit hyväksyttiin.

![RSAT-työkalussa hyväksytyt testit](media/GER-RSAT-RSAT-Tests-Passed.png "Näyttökuva RSAT-työkalussa hyväksytyistä testeistä")

Huomaa, että suoritetun testin tulokset lähetetään myös Azure DevOpsiin lisäanalyyseja varten.

![Suoritetun testin tulokset Azure DevOpsissa](media/GER-RSAT-DevOps-Tests-Added.png "Näyttökuva suoritetun testin tuloksista Azure DevOpsissa")

### <a name="simulate-a-situation-where-tests-fail"></a>Testien epäonnistumistilanteen simulointi

Tämän testisarjan on epäonnistuttava, kun ainakin yksi luoduista tuloksista ei vastaa vastaavaa perusriviä. Tämä tilanne saadaan käyttämällä **BACS (UK)** -muodosta johdettua versiota, jonka luomassa maksutiedostossa on eri sisältö kuin vastaavalla perusrivillä. Voit simuloida tilanteen käyttämällä samaa **BACS (UK)** -muotoa mutta vaihtamalla maksun summan käsitellyllä maksurivillä.

1. Avaa sovellus ja valitse **Ostoreskontra \> Maksut \> Maksukirjauskansio**.
2. Valitse **Rivit**.
3. Valitse ensin maksurivi ja sitten **Maksun tila \> Ei mitään**.
4. Muuta **Veloitus**-kentän arvo**1 000,00** arvoksi **2 000,00**.
5. Tallenna muutokset valitsemalla **Tallenna**.

### <a name="run-the-tests-in-rsat"></a>Testien suorittaminen RSAT-työkalussa

1. Valitse ladatut testit RSAT-työkalussa.
2. Valitse **Suorita**.

Huomaa, että testitapaukset suoritetaan automaattisesti sovelluksessa selainta käyttämällä.

### <a name="analyze-the-results-of-test-execution"></a>Suoritetun testin tulosten analysoiminen

Suoritetun testin tulokset tallennetaan RSAT-työkaluun. Huomaa, että toinen testi epäonnistui toisen suorituksen aikana.

![Epäonnistuneet testitulokset RSAT-työkalussa](media/GER-RSAT-RSAT-Tests-Failed.png "Näyttökuva epäonnistuneista testituloksista RSAT-työkalussa")

Huomaa, että suoritetun testin tulokset lähetetään myös Azure DevOpsiin lisäanalyyseja varten.

![Epäonnistuneet testitulokset Azure DevOpsissa](media/GER-RSAT-DevOps-Tests-Failed.png "Näyttökuva epäonnistuneista testituloksista Azure DevOpsissa")

Pääset käyttämään kunkin testin tilaa. Pääset käyttämään myös suorituslokia, joten voit analysoida virheen syyt. Seuraavan kuvan suorituslokissa näkyy, että virhe johtui luodun maksutiedoston ja sen perusrivin sisällön välisestä erosta.

![Virheiden analysointiin Azure DevOpsissa käytettävä suoritusloki](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Näyttökuva virheiden analysointiin Azure DevOpsissa käytettävästä suorituslokista")

Tämän vuoksi ER-muodon toimintaa voidaan arvioida osoitetulla tavalla automaattisesti käyttämällä RSAT-työkalua testausympäristönä ja tehtävän tallennustoimintoon perustuvia testitapauksia, jotka käyttävät ER-perusrivitoimintoa.

## <a name="additional-resources"></a>Lisäresurssit

- [Tehtävän tallennustoiminnon resurssit](../user-interface/task-recorder.md)
- [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357)
- [Käyttäjän hyväksymistestien luominen ja automatisointi](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [Jatkuvaa koonnin ja testauksen automaatiota tukevien topologioiden käyttöönotto ja käyttäminen](../perf-test/continuous-build-test-automation.md)
- [Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md)
- [ER Muodon päivittäminen ottamalla käyttöön sitä koskeva uusi perusversio](tasks/er-upgrade-format.md)
- [ER Tuo kokoonpano Lifecycle Services -palvelusta](tasks/er-import-configuration-lifecycle-services.md)
