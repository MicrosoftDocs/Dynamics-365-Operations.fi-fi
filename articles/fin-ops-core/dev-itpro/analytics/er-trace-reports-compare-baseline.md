---
title: Seuraa luotuja raporttituloksia ja vertaa niitä perusarvoihin
description: Tässä ohjeaiheessa on tietoja tavasta, jolla voit verrata tuloksia luoduista sähköisen raportoinnin (ER) raporteista perusriviraportin arvoihin.
author: NickSelin
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: e4245f5951cc4891b378f2343a1563ced33bc937
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345837"
---
# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Seuraa luotuja raporttituloksia ja vertaa niitä perusarvoihin

[!include[banner](../includes/banner.md)]

Voit seurata lähteviä sähköisiä tiedostoja luovien sähköisen raportoinnin (ER) muotojen tuloksia. Kun seuranta on käytössä (ER-käyttäjän parametri **Suorita vianmääritystilassa** on käytössä), uusi jäljitystietue luodaan ER-muodon suorittamisen lokiin aina, kun ER-raportti suoritetaan. Seuraavat tiedot on tallennettu jokaiseen luotuun jäljitykseen:

- Kaikki varoitukset, jotka on luonut oikeellisuustarkistussäännöt
- Kaikki virheet, jotka on luonut oikeellisuustarkistussäännöt
- Kaikki luodut tiedostot, jotka on tallennettu seurantatietueen liitteinä

Voit tallentaa yksittäisiä kohdearvon sovellustiedostoja kaikille ER-muodoille. Tiedostoja käsitellään kohdearvotiedostoina, kun ne kuvaavat suoritettavien raporttien odotettuja tuloksia. Jos kohdearvotiedosto on käytettävissä ER-muodolle, joka suoritetaan, kun jäljitysluonti on otettu käyttöön, jäljitys tallentaa aiemmin mainittujen tietojen lisäksi tulokset luodun sähköisen tiedoston vertailusta kohdearvotiedostoon. Yhdellä napsautuksella voit ladata myös luodun sähköisen tiedoston ja sen kohdearvotiedoston yhtenä zip-tiedostona. Sitten voit tehdä yksityiskohtaisen vertailun ulkoisella työkalulla, kuten WinDiff.

Voit arvioida jäljitystä analysoidaksesi, sisältävätkö luodut sähköiset tiedostot odotetun sisällön. Voit tehdä tämän arvioinnin hyväksyntätestausympäristössä, kun koodiperuste on muutettu (kun esimerkiksi päivitit sovelluksen uuteen ilmentymään, asensit korjaustiedostopaketit tai otit koodin muutokset käyttöön). Näin voit varmistaa, että arviointi ei vaikuta käytettävien ER-raporttien suorittamiseen. Monille ER-raporteille arviointi voidaan tehdä automaattisesti.

Saat lisätietoja tästä toiminnosta toistamalla tehtäväoppaat **ER Luo raportteja ja vertaa tuloksia (osa 1)** ja **ER Luo raportteja ja vertaa tuloksia (osa 2)**, jotka ovat osa **7.5.4.3 Testaa IT-palveluita ja ratkaisuja (10679)** -liiketoimintaprosessia. Tämän prosessin voi ladata [Microsoft Download Centeristä](https://go.microsoft.com/fwlink/?linkid=874684). Näissä tehtäväoppaissa kerrotaan, miten voit määrittää ER-kehyksen käyttämään kohdearvotiedostoja, jotta voit arvioida sähköisiä asiakirjoja.

## <a name="example-trace-generated-report-results-and-compare-them-with-baseline-values"></a>Esimerkki: Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin

Tässä menettelyssä käsitellään tapaa, jolla ER-kehys määritetään keräämään tietoja ER-muodon suorittamisista ja arvioimaan sitten kyseisten suoritusten tulokset. Tämän arvioinnin yhteydessä luotuja asiakirjoja verrataan niiden perusrivitiedostoihin. Tässä esimerkissä luodaan pakollisia ER-konfiguraatioita malliyritykselle Litware, Inc. Nämä ohjeet on tarkoitettu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. Nämä vaiheet voidaan suorittaa minkä tahansa tietojoukon avulla.

Tämän esimerkin vaiheiden suorittamista varten on ensin suoritettava ohjeaiheessa [Konfiguraation lähteiden luominen ja niiden merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) käsitellyt vaiheet.

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Tarkista **Lokalisointikonfiguroinnit**-sivun **Konfiguraation lähteet** -osassa, että näyteyrityksen Litware, Inc. konfiguraation lähde on luettelossa ja että se on merkitty **aktiiviseksi**. Jos konfiguraation lähde ei ole näkyvissä, suorita kohdan [Konfiguraation lähteiden luominen ja niiden merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) vaiheet.

### <a name="configure-document-management-parameters"></a>Tiedostonhallintaparametrien konfigurointi

1. Valitse **Organisaation hallinto** \> **Tiedostojen hallinta** \> **Tiedostotyypit** ja tallenna perusrivitiedostot luomalla uusi asiakirjatyyppi.
2. Anna **Luokka**-kentässä **Liitä tiedosto**.
3. Anna **Ryhmä**-kentässä **Tiedosto**.

![Tiedostotyypit-sivu.](media/GER-BaselineSample-SetupDocumentType.PNG "Näyttökuva Tiedostotyypit-sivusta")

> [!NOTE]
> Saman niminen uusi tiedostotyyppi on määritettävä jokaiselle tietojoukolle, jossa aiot käyttää ER-perusrivitaulua.

### <a name="configure-er-parameters-to-start-to-use-the-baseline-feature"></a>ER-parametrien määrittäminen aloittamaan perusrivitoiminnon käyttäminen

1. Valitse **Sähköisen raportointi** -työtilan **Liittyvät linkit** -osassa **Sähköisen raportoinnin parametrit**.

    ![Sähköisen raportoinnin työtila.](media/GER-BaselineSample-ERWorkspace.PNG "Näyttökuva Sähköinen raportointi -työtilasta")

2. Anna tai valitse juuri luomasi asiakirjatyyppi **Liitteet**-välilehden **Perusrivi**-kenttä.

    ![Sähköisen raportoinnin parametrit -sivun Liitteet-välilehti.](media/GER-BaselineSample-ERParameters.PNG "Näyttökuva sähköisen raportoinnin parametreista")

3. Valitse **Tallenna** ja sulje sitten **Sähköisen raportoinnin parametrit** -sivu.

### <a name="add-a-new-er-model-configuration"></a>Uuden ER-mallimäärityksen lisääminen

1. Valitse **Sähköinen raportointi** -työtilan **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.
2. Valitse toimintoruudussa **Luo konfigurointi**.
3. Kirjoita avattavan luettelon **Nimi**-kenttään **ER-perusrivien oppimismalli**.
4. Vahvista uuden ER-tietomallimerkinnän luonti valitsemalla **Luo konfigurointi**.

![Avattava Luo konfigurointi -luettelo -valintaruutu.](media/GER-BaselineSample-ModelAdd.PNG "Näyttökuva Avattava Luo konfigurointi -luettelo -valintaruudusta")

### <a name="design-a-data-model"></a>Tietomallin suunnitteleminen

1. Valitse toimintoruudun **Konfiguroinnit**-välilehdessä **Suunnittelutoiminto**.
2. Valitse **Uusi**.
3. Kirjoita avattavan luettelon valintaikkunan **Nimi**-kentässä **Juuri**.
4. Valitse **Lisää**.
5. Valitse **Juuriviite**.
6. Valitse ensin **OK** ja sitten **Tallenna**.
7. Sulje **Mallin suunnittelu** -sivu.
8. Valitse **Muutoksen tila**.
9. Valitse ensin **Valmis** ja sitten **OK**.

![Konfiguraatiot-sivu.](media/GER-BaselineSample-ModelComplete.PNG "Näyttökuva Konfiguroinnit-sivusta")

### <a name="add-a-new-er-format-configuration"></a>Uuden ER-muotokonfiguraation lisääminen

1. Valitse toimintoruudun **Konfiguroinnit**-välilehdessä **Luo konfigurointi**.
2. Valitse avattavasta valintaikkunasta **Uusi**-kenttäryhmässä **ER-perusrivien oppimismalli -tietomalliin perustuva muoto**.
3. Anna **Nimi**-kentässä **ER-perusrivien oppimismuoto**.
4. Vahvista uuden ER-muotomerkinnän luonti valitsemalla **Luo konfigurointi**.

![Avattava Luo konfigurointi -luettelo -valintaruutu.](media/GER-BaselineSample-FormatAdd.PNG "Näyttökuva Avattava Luo konfigurointi -luettelo -valintaruudusta")

### <a name="design-a-format"></a>Muodon suunnittelu

Tässä esimerkissä luodaan yksinkertainen ER-muoto XML-tiedostojen luontia varten.

1. Valitse toimintoruudun **Konfiguroinnit**-välilehdessä **Suunnittelutoiminto**.
2. Valitse **Lisää pääkansio**.
2. Toimi avattavassa valintaikkunassa seuraavasti:

    1. Valitse puussa **Common\\File**.
    2. Kirjoita **Nimi**-kenttään **Tulos**.
    3. Valitse **OK**.

3. Valitse **Lisää**.
4. Toimi avattavassa valintaikkunassa seuraavasti:

    1. Valitse puussa **XML\\Elementti**.
    2. Kirjoita **Nimi**-kenttään **Asiakirja**.
    3. Valitse **OK**.

5. Valitse puussa **Tuloste\\Asiakirja**.
6. Valitse **Lisää**.
7. Toimi avattavassa valintaikkunassa seuraavasti:

    1. Valitse puussa **XML\\Määrite**.
    2. Kirjoita **Nimi**-kenttään **Tunnus**.
    3. Valitse **OK**.

    ![Muodon suunnittelutoiminto -sivu.](media/GER-BaselineSample-FormatLayoutDesign.PNG "Näyttökuva Muodon suunnittelija -sivusta")

8. Valitse **Yhdistämismääritys**-välilehdessä **Poista**.
9. Valitse **Lisää pääkansio**.
10. Valitse puun avattavassa valintaikkunassa **Yleinen\\Käyttäjän syöttöparametrit** ja toimi sitten seuraavasti:

    1. Kirjoita **Nimi**-kenttään **Tunnus**.
    2. Kirjoita **Etiketti**-kenttään **Anna tunnus**.
    3. Valitse **OK**.

11. Valitse puussa **Tuloste\\Asiakirja\\Tunnus**.
12. Valitse ensin **Sidonta** ja sitten **Tallenna**.

![Muodon suunnittelutoiminto -sivu.](media/GER-BaselineSample-FormatMappingDesign.PNG "Näyttökuva Muodon suunnittelija -sivusta")

Määritetty muoto luo XML-tiedoston suunnitellun rakenteen perusteella. Tämä XML-tiedosto sisältää **Juuri**-elementin, jonka **Tunnus**-määrite on määritetty käyttäjän ER-ajonaikaisuus-valintaikkunaan annettavaksi arvoksi.

### <a name="generate-a-new-baseline-file-for-a-designed-er-format"></a>Uuden perusrivitiedoston luominen suunnitellulle ER-muodolle

1. Valitse **Konfiguroinnit**-sivun **Versiot**-pikavälilehdessä **Suorita**.
2. Kirjoita **Anna tunnus** -kenttään **1**.
3. Valitse **OK**.

    ![Sähköisen raportin parametrit -valintaikkuna.](media/GER-BaselineSample-FormatRunToMakeBaselineFile1.PNG "Näyttökuva Sähköisen raportin parametrit -valintaikkunasta")

4. Tallenna luodun **out.Admin.xml**-tiedoston paikallinen kopio, jotta voit käyttää sitä myöhemmin ER-muodon perusrivinä.

    ![Ilmoitus luodusta tiedostosta Konfiguroinnit-sivulla.](media/GER-BaselineSample-FormatRunToMakeBaselineFile2.PNG "Näyttökuva ilmoituksesta luodusta tiedostosta Konfiguroinnit-sivulla")

### <a name="configure-er-parameters-to-use-the-baseline-feature"></a>ER-parametrien määrittäminen käyttämään perusrivitoimintoa

1. Valitse **Konfiguroinnit**-sivun toimintoruudun **Konfiguroinnit**-välilehdessä **Käyttäjän parametrit**.
2. Määritä **Suorita virheenkorjaustila** -asetukseksi **Kyllä**.
3. Valitse **OK**.

![Käyttäjän parametrit -valintaikkuna.](media/GER-BaselineSample-ERUserParameters.PNG "Näyttökuva Käyttäjän parametrit -valintaikkunasta")

### <a name="add-a-new-baseline-for-designed-er-format"></a>Uuden perusrivitiedoston lisääminen suunnitellulle ER-muodolle

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse toimintoruudussa **Perusrivit**.

    ![Konfigurointi-sivun Perusrivit-painike.](media/GER-BaselineSample-OpenBaselinePage.PNG "Näyttökuva Konfigurointi-sivun Perusrivit-painikkeesta")

3. Valitse toimintoruudussa **Uusi**.
4. Valitse **ER-perusrivien oppimismuoto** -kohdassa aiemmin suunniteltu ER-muoto.
5. Valitse **Tallenna**.

![Sähköisen raportointimuotojen perusrivit -sivu.](media/GER-BaselineSample-AddBaseline.PNG "Näyttökuva Sähköisen raportointimuotojen perusrivit -sivusta")

Perusrivi lisätään **ER-perusrivien oppimismuoto** -muotoon.

### <a name="configure-a-baseline-rule-for-the-added-baseline"></a>Lisätyn perusrivin perusrivisäännön määrittäminen

1. Valitse toimintoruudun **Sähköisten raportointimuotojen perusrivit** -sivulla **Liitteet**-painike (paperiliitinkuvake).
2. Valitse toimintoruudussa **Uusi** \> **Tiedosto**. ER-parametreissa **Tiedosto**-asiakirjatyyppi on pitänyt valita aiemmin perusrivitiedostojen tallentamiseen käytettävänä asiakirjatyyppinä.
3. Valitse ensin **Selaa** ja sitten **out.Admin.xml**-tiedosto, joka luotiin, kun suoritit aiemmin määritetyn ER-muodon.

    ![Liitteet-sivu.](media/GER-BaselineSample-UploadBaselineFile.PNG "Näyttökuva Liitteet-sivusta")

4. Sulje **Liitteet**-sivu.
5. Valitse **Perusrivit**-pikavälilehdessä **Uusi**.
6. Kirjoita **Nimi**-kenttään **Perusrivi 1**.
7. Anna tai valitse **Tiedosto-osan nimi** -kenttään **Tuloste**. Tämä arvo ilmaisee, että määritettyä perusriviä verrataan tiedostoon, joka muodostettiin käyttämällä **Tuloste**-muotoelementtiä.
8. Kirjoita **Tiedostonimen peite** -kenttään **\*.xml**.

    > [!NOTE]
    > Voit määrittää tiedostonimen peitteen. Jos tiedostonimen peite on määritetty, luotu tuloste arvioidaan perusrivitietueen avulla vain silloin, kun luodun tulostiedoston nimi vastaa peitettä.

9. Jos määritettyä perusriviä käytetään vain silloin, kun **ER-perusrivien oppimismuoto** -ER-muodon suorittavat käyttäjät ovat kirjautuneet tiettyihin yrityksiin, valitse kyseiset yritykset **Yritykset**-kentässä.
10. Anna tai valitse **Perusrivi**-kentässä **out.Admin**-liite.
11. Valitse **Tallenna**.

![Sähköisen raportointimuotojen perusrivit -sivu.](media/GER-BaselineSample-SetupBaselineLine.PNG "Näyttökuva Sähköisen raportointimuotojen perusrivit -sivusta")

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Suunnitellun ER-muoto suorittaminen ja tulosten analysointi lokia tarkastelemalla

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna puussa **ER-perusrivien oppimismalli** ja valitse **ER-perusrivien oppimismalli\\ER-perusrivien oppimismuoto**.
3. Valitse **Versiot**-pikavälilehdessä **Suorita**.
4. Kirjoita **Anna tunnus** -kenttään **1**.
5. Valitse **OK**.
6. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Määritysten virheenkorjauslokit**.

    ![Sähköisen raportoinnin ajolokit -sivulla.](media/GER-BaselineSample-ReviewBaselineComparison1.PNG "Näyttökuva Sähköisen raportoinnin ajolokit -sivusta")

    > [!NOTE]
    > Suorituslokissa sisältää tietoja luodun tiedoston ja määritetyn perusrivin vertailutuloksista. Tässä esimerkissä loki ilmaisee, että luotu tiedosto ja perusaikataulu ovat samanlaisia.

7. Valitse **Poista kaikki**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Suunnitellun ER-muoto suorittaminen ja tulosten analysointi lokia tarkastelemalla

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna puussa **ER-perusrivien oppimismalli** ja valitse **ER-perusrivien oppimismalli\\ER-perusrivien oppimismuoto**.
3. Valitse **Versiot**-pikavälilehdessä **Suorita**.
4. Kirjoita **Anna tunnus** -kenttään **2**.
5. Valitse **OK**.
6. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Määritysten virheenkorjauslokit**.

    ![Sähköisen raportoinnin ajolokit -sivulla.](media/GER-BaselineSample-ReviewBaselineComparison2.PNG "Näyttökuva Sähköisen raportoinnin ajolokit -sivusta")

    > [!NOTE]
    > Suorituslokissa sisältää tietoja luodun tiedoston ja määritetyn perusrivin vertailutuloksista. Tässä esimerkissä loki ilmaisee, että luotu tiedosto ja perusaikataulu ovat erilaisia.

7. Valitse **Vertaa**

> [!NOTE]
> Luotu tiedosto ja perusrivitiedosto on käytettävissä zip-tiedostona. Voit käyttää tiedostojen vertailuun ulkoisia työkaluja, kuten WinDiff, ja tarkastella eroja.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin (ER) kehyksen määrittäminen](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]