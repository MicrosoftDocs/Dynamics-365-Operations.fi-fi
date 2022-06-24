---
title: ER-ratkaisujen suorituskyvyn parantaminen vähentämällä ajon aikana haettujen taulukenttien määrää
description: Tässä artikkelissa selitetään suorituskyvyn parantaminen vähentämällä ajon aikana haettujen taulukenttien määrää.
author: NickSelin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: eb76c415da87d421b8135a93b84f4e905f01e70d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847448"
---
# <a name="improve-performance-of-er-solutions-by-reducing-the-number-of-table-fields-that-are-fetched-at-runtime"></a>ER-ratkaisujen suorituskyvyn parantaminen vähentämällä ajon aikana haettujen taulukenttien määrää

[!include[banner](../includes/banner.md)]

Voit suunnitella [sähköisen raportoinnin](general-electronic-reporting.md) (ER) [muotoja](er-overview-components.md#format-components-for-outgoing-electronic-documents), jotka luovat lähteviä tiedostoja eri muodoissa. Kun asiakirja luodaan, ER-muoto kutsuu tietolähteitä, jotka määritettiin vastaavassa [ER-mallimäärityksessä](er-overview-components.md#model-mapping-component). Voit määrittää tietojen noutamisen käyttöoikeudet sovelluksen tauluihin, kyselyihin tai entiteetteihin käyttämällä ER-tietolähteitä, joiden tyyppi on *Taulukkotietueet*. Oletusarvon mukaan *Taulukkotietue*-tyypin tietolähde hakee kaikkien pyydettyjen tietueiden kenttien arvot. Voit kuitenkin konfiguroida tämäntyyppisen tietolähteen niin, että se hakee vain suoritettavan ER-muodon edellyttämät kenttäarvot. Tämän konfiguraation avulla voidaan vähentää tietojen noutamisen ja tietueiden välimuistiin tallentamisen suorittavan sovelluspalvelimen muistinkulutusta.

Tässä ohjeaiheessa on lisätietoja *Taulukkotietue*-tyypin tietolähteiden noudettujen kenttien luettelon rajoittamisesta, kun suoritat tämän artikkelin esimerkin.

## <a name="example-reduce-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Esimerkki: Suorituksen aikana haettujen taulukenttien määrän pienentäminen

Seuraavissa ohjeissa näytetään, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolissa oleva käyttäjä voi konfiguroida ER-mallimäärityksen niin, että se noutaa vain ER-muodon suorittamiseen tarvittavat kentät. Näin voidaan vähentää sovelluspalvelimen muistin kulutusta.

Kaikki nämä menettelyt voidaan suorittaa **USMF**-yrityksessä Microsoft Dynamics 365 Financessa. Koodausta ei tarvita.

Tämän esimerkin suorittaminen edellyttää jonkin seuraavan roolin käyttöoikeutta **USMF**-yrityksessä:

- Sähköisen raportoinnin toiminnallinen konsultti
- Järjestelmänvalvoja

Tässä esimerkissä käytetään ER-[konfiguraatioita](general-electronic-reporting.md#Configuration), jotka ovat olemassa malliyritykselle **Litware, Inc**. Tarkista, että malliyrityksen **Litware, Inc.** (`http://www.litware.com`) konfiguraatiopalvelu luetteloitu ER-kehyksessä ja merkitty tilaan **Aktiivinen**. Jos tämä määrityspalvelu ei ole luettelossa tai jos se ei ole merkittynä **aktiiviseksi**, noudata ohjeaiheen [Konfiguraatiopalvelun luominen ja sen merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) vaiheita.

### <a name="configure-the-er-framework"></a>Määritä ER-kehys

Seuraa vaiheita kohdassa [Määritä ER-kehys](er-quick-start2-customize-report.md#ConfigureFramework) luodaksesi ER-parametrien vähimmäisjoukon. Nämä määritykset on suoritettava, ennen kuin ER-kehystä käytetään annetun ER-ratkaisun tietolähteiden muokkaamiseen.

### <a name="import-the-sample-er-configurations"></a>ER-mallikonfiguraation tuonti

Jos et ole vielä suorittanut [Uuden sähköisen raportoinnin ratkaisun suunnitteleminen mukautetun raportin tulostamista varten](er-quick-start1-new-solution.md) -artikkelin esimerkkiä, lataa XML-tiedostot ja tallenna ne paikallisesti seuraavia tarjotun ER-ratkaisun konfiguraatioita varten.

| Sisällön kuvaus            | Tiedoston nimi |
|--------------------------------|-----------|
| ER-tietomallin konfigurointi    | [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) |
| ER-mallin yhdistämismääritys | [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) |
| ER-muodon konfigurointi        | [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) |

Noudattamalla siten näitä ohjeita voit ladata annetun ER-ratkaisun konfiguraatiot Finance-instanssiin.

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Raportointikonfiguraatiot**.
3. Tuo ER-tietomallin määritys **Määritykset**-sivulla.

    1. Vallitse **Vaihto** ja sitten **Lataa XML-tiedostosta**.
    2. Valitse **Selaa** ja etsi ja valitse **Questionnaires model.version.1.xml** -tiedosto ja valitse **OK**.

4. Tuo ER-mallin yhdistämismäärityksen määritys.

    1. Vallitse **Vaihto** ja sitten **Lataa XML-tiedostosta**.
    2. Valitse **Selaa** ja etsi ja valitse **Questionnaires mapping.1.1.xml** -tiedosto ja valitse **OK**.

5. Tuo ER-muotokonfiguraatio.

    1. Vallitse **Vaihto** ja sitten **Lataa XML-tiedostosta**.
    2. Valitse **Selaa** ja etsi ja valitse **Questionnaires format.1.1.xml** -tiedosto ja valitse **OK**.

6. Laajenna määrityspuussa **kyselyiden malli**.
7. Tarkista tuotujen ER-määritysten luettelo määrityspuussa.

    ![Konfiguraatiot-sivun tuotujen ER-määritysten luettelon tarkastelu.](./media/er-reduce-fetched-fields-number-configurations.png)

### <a name="review-the-provided-er-model-mapping"></a>Annetun ER-mallimäärityksen tarkistaminen

1. Valitse **Konfiguroinnit**-sivulla **kyselyiden määritys**.
2. Valitse toimintoruudussa **Suunnittelija**.
3. Valitse **Yhdistäminen mallista tietolähteeseen** -sivulla **Suunnitteluohjelma**.
4. Valitse **Mallimäärityksen suunnitteluohjelma** -sivun toimintoruudusta **Ryhmänäkymä**, jos haluat ottaa **Ryhmä**-näkymän käyttöön.
5. Laajenna **Tietomalli**-ruudussa **Kyselylomake**.

    Huomaa, että **Kysely**-tietolähde on määritetty käyttämään `KMCollection`-sovellustaulua.

6. Laajenna **Tietolähteet** -ruudussa **Taulun tietueet** \> **Kysely** \> **Kentät**.

    Huomaa, kuinka monta `KMCollection`-sovellustaulun kenttää *Taulutietue*-tyypin **Kysely**-tietolähde käyttää.

    ![Mallin määrityksen suunnittelusivun mallimäärityksen tarkasteleminen, kun Ryhmä-näkymä on käytössä.](./media/er-reduce-fetched-fields-number-mapping1.png)

7. Valitse toimintoruudusta **Ryhmä-näkymä** uudelleen, jos haluat poistaa **Ryhmä**-näkymän käytöstä, ja valitse sitten **Näytä kaikki** \> **Näytä vain yhdistetyt**.

    Huomaa, että ER-tietomallin **Kysely**-tietueluetteloa täytetään muutamista `KMCollection`-sovellustaulun kentistä:

    - `Active`
    - `Description`
    - `questionMode`
    - `kmCollectionId`

    ![Mallin määrityksen suunnittelusivun mallimäärityksen tarkasteleminen, kun Ryhmä-näkymä poistetaan käytöstä.](./media/er-reduce-fetched-fields-number-mapping2.png)

### <a name="turn-on-the-er-performance-trace"></a>ER-suorituskykyjäljityksen ottaminen käyttöön

Määritä ER-käyttäjäparametrit , joiden avulla ER-komponenttien suoritus voidaan jäljittää, noudattamalla aiheen [ER-suorituskykyjäljityksen ottaminen käyttöön](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) vaiheita.

### <a name="run-the-provided-er-format-by-using-the-provided-model-mapping"></a>Suorita annettu ER-muoto käyttämällä annettua mallimääritystä

Suorita ER-muoto yksittäiselle kyselylle **Konfiguroinnit**-sivulla noudattamalla aiheen [Suunnitellun muodon suorittaminen ER-muodosta](er-quick-start1-new-solution.md#RunFormatFromER) vaiheita.

### <a name="review-the-execution-trace-of-the-first-run"></a>Tarkasta ensimmäisen suorituksen jäljitys

1. Siirry kohtaan **Organisaation hallinto** \> **Sähköinen raportointi \> Konfiguraatiot**.
2. Laajenna **Kysely-malli** **Konfiguroinnit**-sivulla ja valitse **Kyselyiden yhdistäminen**.

    > [!NOTE]
    > **Versiot**-pikavälilehden tiedot ilmaisevat, että olet valinnut **kyselylomakkeiden määritys** -konfiguraation luonnosversion. Näin ollen voit muokata tämän mallimäärityksen sisältöä.

3. Valitse toimintoruudussa **Suunnittelija**.
4. Valitse **Yhdistäminen mallista tietolähteeseen** -sivulla **Suunnitteluohjelma**.
5. Valitse **Mallin määrityssuunnittelija** -sivulla hallintapaneelista **Suorituskyvyn jäljitysmuoto**.
6. Valitse **Suorituskyvyn jäljityksen tuloksen asetukset** - valintaikkunassa jäljitys, joka on luotu muodon viimeisen suorituksen aikana.

    ![Valitaan jäljitys Suorituskyvyn jäljitystulosten asetukset -valintaikkunassa.](./media/er-reduce-fetched-fields-number-select-trace-1.png)

7. Valitse **OK**. 
8. Suodata **Tiedot**-pikavälilehdessä **Kysely**-polku, joka osoittaa **Kysely**-tietolähteeseen.
9. Tarkista **Kysely**-tietolähteen kutsumisen yhteydessä luodun tietokantakyselyn tiedot.

    Huomaa, että `KMCollection`-sovellustaulun kaikki kentät noudettiin ajon aikana, kun **Kysely**-tietolähdettä kutsuttiin.

    ![Tarkista tietokantakyselyn tiedot Mallin määrityksen suunnittelusivulla.](./media/er-reduce-fetched-fields-number-query1.png)

### <a name="modify-the-provided-er-model-mapping"></a>Annetun ER-mallimäärityksen muokkaaminen

1. Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähteet**-ruudusta **Kysely**-tietolähde.
2. Valitse **Muokkaa** **Tietolähteet**-ruudussa.
3. Valitse **Tietolähteen ominaisuudet** -valintaikkunassa **Valitse kentät**, jotka määrittävät sen `KMCollection`-sovellustaulun viittaaman kenttien luettelon, joka haetaan suorituksen aikana muokattavissa olevaa **Kysely**-tietolähdettä kutsuttaessa.

    ![Valitse Tietolähteen ominaisuudet -valintaikkunassa Valitse kentät, jotta voit aloittaa niiden kenttien luettelon määrittämisen, joka haetaan sovellustaulusta käyttämällä muokattavissa olevaa tietolähdettä.](./media/er-reduce-fetched-fields-number-select-fields1.png)

4. Valitse **Valitse kentät** -sivulla **Automaattinen täydennys**.

    **Valitut kentät** -luettelo täytetään automaattisesti mallin määrityksen esimääritettyjen artefaktien perusteella. Luetteloon lisätään kaikki viitatun taulun kentät ja suhteet, jotka mainitaan mallin määrityksen missä tahansa sidonnassa, kaavassa tai tietolähteessä.

    ![Sovellustaulun Valitut kentät -sivulla haettavan kenttäluettelon määrittäminen.](./media/er-reduce-fetched-fields-number-select-fields2.png)

5. Valitse **Tallenna** ja sulje **Valitut kentät** -sivu.
6. Tallenna tietolähteen asetuksiin tekemäsi muutokset valitsemalla **OK**.
7. Valitse toimintoruudussa **Näytä kaikki**.

    Huomaa, että **Kysely**-tietolähde näyttää nyt tekstin **\<Fields are filtered\>**. Tämä teksti ilmaisee, että tietolähde on määritetty hakemaan rajoitettu määrä kenttiä viitatusta sovellustaulusta.

    ![Päivitetyn mallin yhdistämismääritysten tarkasteleminen Mallin yhdistämismäärityksen suunnitteluohjelma -sivulla.](./media/er-reduce-fetched-fields-number-mapping3.png)

8. Tallenna muokattavaan mallimääritykseen tekemäsi muutokset valitsemalla **Tallenna**.

    > [!NOTE]
    > Ajon aikana ER analysoi lisätyt suhteet ja lisää kaikki kentät, joita niitä käytetään suhteissa tietokantakyselyyn, vaikka näitä kenttiä ei olisi nimenomaisesti lisätty haettavien kenttien luetteloon suunnittelun aikana.

### <a name="run-the-provided-er-format-by-using-the-updated-model-mapping"></a>Suorita päivitetty ER-muoto käyttämällä annettua mallimääritystä

Suorita ER-muoto yksittäiselle kyselylle **Konfiguroinnit**-sivulla noudattamalla aiheen [Suunnitellun muodon suorittaminen ER-muodosta](er-quick-start1-new-solution.md#RunFormatFromER) vaiheita.

### <a name="review-the-execution-trace-of-the-second-run"></a>Tarkasta toisen suorituksen jäljitys

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Kysely-malli** **Konfiguroinnit**-sivulla ja valitse **Kyselyiden yhdistäminen**.
3. Valitse toimintoruudussa **Suunnittelija**.
4. Valitse **Yhdistäminen mallista tietolähteeseen** -sivulla **Suunnitteluohjelma**.
5. Valitse **Mallin määrityssuunnittelija** -sivulla hallintapaneelista **Suorituskyvyn jäljitysmuoto**.
6. Valitse **Suorituskyvyn jäljityksen tuloksen asetukset** - valintaikkunassa jäljitys, joka on luotu muodon viimeisen suorituksen aikana.
7. Valitse **OK**.
8. Suodata **Tiedot**-pikavälilehdessä **Kysely**-polku, joka osoittaa **Kysely**-tietolähteeseen.
9. Tarkista **Kysely**-tietolähteen kutsumisen yhteydessä luodun tietokantakyselyn tiedot.

    Huomaa, että vain tietolähteen täyttämiseen vaadittavat kentät noudettiin `KMCollection`-sovellustaulusta ajon aikana, kun **Kysely**-tietolähdettä kutsuttiin.

    > [!NOTE]
    > Finance-sovelluksen tiedonhallintakehys lisää automaattisesti joitakin kenttiä, kuten osiointitunnuksen, tietoalueen tunnuksen ja tietuetunnuksen kentät.

    ![Tarkistetaan päivitetyn mallimäärityksen tietokantakyselyn tiedot Mallin määrityksen suunnittelusivulla.](./media/er-reduce-fetched-fields-number-query2.png)

Tämän tekniikan avulla voit vähentää haettujen tietueiden määrää, kun muistinkulutusta on vähennettävä ER-mallimäärityksen ja ER-muodon suorittamisen avulla.

## <a name="limitations"></a>Rajoitukset

Kun rajoitat *Taulutietue*-tyypin tietolähteen haettavien kenttien määrää, et voi käyttää sen sovellustaulun menetelmiä, johon tietolähde viittaa, koska sovelluksen metatiedot eivät anna tietoja näiden menetelmien kutsumiseen tarvittavista taulukentistä.

## <a name="usage-notes"></a>Käyttöhuomautukset

Vaikka **Täytä automaattisesti** -komento lisää kentät automaattisesti, aiemmin lisättyjä kenttiä ei poisteta automaattisesti, vaikka niitä ei enää käytetä muokattavissa olevan mallimäärityksen sidonnoissa, kaavoissa tai tietolähteissä.

Kun valitset **automaattisen täydennyksen**, ER analysoi sidonnat, kaavat ja tietolähteet, joita muokattavissa olevassa mallimäärityksessä oli silloin, kun avasit sen muokkaamista varten. Jos muutat muokattavan mallin määrityksen sidontoja, kaavoja ja tietolähteitä ja haluat käyttää **Täytä automaattisesti** -komentoa, sulje mallin määritysten suunnittelutoiminto ja avaa se sitten uudelleen, jotta voit muokata mallin määritystä. 

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi](trace-execution-er-troubleshoot-perf.md)
- [ER-konfiguraatioiden suorituskykyongelmien vianmääritys](er-troubleshoot-perf-issues-in-configurations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
