---
title: Sähköisen raportoinnin (ER) määrittäminen hakemaan tiedot Power BI:hin
description: Tässä ohjeaiheessa kerrotaan, miten omaa sähköisen raportoinnin konfiguraatiota voidaan käyttää tietojen siirron järjestämiseen omasta esiintymästä Power BI -palveluihin.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 34d4ad9106b2751c77db4fd03d83932e587a5332
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680117"
---
# <a name="configure-electronic-reporting-er-to-pull-data-into-power-bi"></a>Sähköisen raportoinnin (ER) määrittäminen hakemaan tiedot Power BI:hin

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten omaa sähköisen raportoinnin konfiguraatiota voidaan käyttää tietojen siirron järjestämiseen omasta esiintymästä Power BI -palveluihin. Tässä aiheessa käytetään esimerkkinä Intrastat-tapahtumia siirrettävinä liiketoimintatietoina. Power BI -karttavisualisointi käyttää tätä Intrastat-tapahtumatietoa näkymän esittämiseen yrityksen tuonti-/vientitoimintojen analyysia varten Power BI -raportissa.

## <a name="overview"></a>Yleiskuvaus

Microsoft Power BI on kokoelma ohjelmistopalveluita, sovelluksia ja yhdistimiä, jotka yhdessä muuttavat ulkoiset tietolähteet yhdenmukaiseksi, visuaalisesti mukaansatempaavaksi ja interaktiiviseksi tiedoksi. Sähköisen raportoinnin (ER) avulla in käyttäjät voivat helposti määrittää tietolähteet ja järjestää sovelluksen tietojen siirron Power BI -palveluun. Tiedot siirretään tiedostoina OpenXML-laskentataulukkomuodossa (Microsoft Excel -työkirjatiedostona). Siirretyt tiedostot tallennetaan Microsoft SharePoint Serveriin, joka on konfiguroitu tähän tarkoitukseen. Tallennettuja tiedostoja Power BI:ssa laadittaessa raportteja, jotka sisältävät visualisointeja (taulukot, kaaviot, kartat ja niin edelleen). Power BI -raportit jaetaan Power BI -käyttäjille, ja ne saadaan käyttöön Power BI -koontinäytöissä ja sovelluksen sivuilla. Tässä aiheessa esitellään seuraavat tehtävät:

- Määritä Microsoft Dynamics 365 Finance.
- Sähköisen raportoinnin konfiguraation valmistelu Finance-sovelluksen tietojen noutoa varten.
- ER-ympäristön konfigurointi tietojen siirtoon Power BI:sta
- Siirretyn tiedon käyttö Power BI -raporttia luotaessa
- Power BI -raportin valmistelu Finance-käyttöä varten.

## <a name="prerequisites"></a>Edellytykset
Tämän aiheen esimerkin suorittaminen edellyttää seuraavia käyttöoikeuksia:

- Käyttöoikeudet seuraaville rooleille:

    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

- Sovelluksen käyttöön määritetyn SharePoint Serverin käyttöoikeudet.
- Power BI -kehikon käyttöoikeudet

## <a name="configure-document-management-parameters"></a>Tiedostonhallintaparametrien konfigurointi
1. Konfiguroi **Tiedostonhallintaparametrit**-sivulla SharePoint Serve -käyttöoikeudet, joita käytetään yrityksessä, johon olet kirjautunut (DEMF tässä esimerkissä).
2. Testaa yhteys varmistaaksesi, että sinulle myönnetty SharePoint Server -käyttöoikeudet.

    [![Asiakirjahallinnan parametrisivu](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)

3. Avaa määritetty SharePoint-sivusto. Luo uusi kansio, johon ER tallentaa Excel-tiedostot, jotka sisältävä liiketoimintatietoja, joita Power BI -raportit tarvitsevat Power BI -tietojoukkojen lähteenä.
4. Voit luoda **Tiedostotyypit**-sivulla uuden tiedostotyypin, jota käytetään juuri luomaasi SharePoint-kansioon kirjauduttaessa. Kirjoita **Tiedosto** **Ryhmä**-kenttään ja **SharePoint** **Sijainti**-kenttään ja kirjoita SharePoint-kansion osoite.

    [![Tiedostotyypit-sivu](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>Konfiguroi ER-parametrit
1. **Sähköinen raportointi** -työtilassa valitse **Sähköisen raportoinnin parametrit** -linkki.
2. **Liitteet** -välilehdessä valitse **Tiedosto** -tiedostotyyppi kaikissa kentissä.
3. **Sähköinen raportointi** -työtilassa aktivoi pakollinen palveluntarjoaja valitsemalla **Aktivoi**. Lisätietoja saat **ER Valitse palveluntarjoaja** -tehtäväoppaasta.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>ER-tietomallin käyttö tietolähteenä
ER-tietomallin täytyy olla liiketoimintatietolähteenä, jota käytetään Power BI -raporteissa. Tämä tietomalli ladataan ER-konfiguraatiot-tietovarastosta. Lisätietoja on kohdassa [Lataa sähköiset raportoinnin määritykset Lifecycle Services -palvelusta](download-electronic-reporting-configuration-lcs.md) tai **ER Tuo kokoonpano Lifecycle Services -palvelusta** -tehtäväoppaasta. Valitse **Intrastat** tietomalliksi joka ladataan valitusta ER-konfiguraatiot-tietovarastosta. (Tässä esimerkissä käytetään mallin 1 versiota.) Tämän jälkeen voit käyttää **Intrastatin** ER-mallin kokoonpanoa **Konfiguroinnit**-sivulla.

[![Konfiguroinnit-sivu](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>Suunnittele ER-muotokonfiguraatio
Sinun on luotava uusi ER-muotokonfiguraatio, joka käyttää **Intrastat**-tietomallia liiketoimintatietolähteenä. Tämän muotokonfiguraation on luotava tulosteet sähköisinä asiakirjoina OpenXML (Excel-tiedosto) -muodossa. Lisätietoja on **Sähköisen raportoinnin OPENXML-muotoisten raporttimääritysten luonti** -tehtäväoppaassa. Nimeä uusi konfiguraatio **Tuonti-/vientitoiminnot** (Tuonti-/vientitoiminnot) kuvassa esitetyllä tavalla. Käytä Excel-tiedostoa [ER-tiedot - tuonnin ja viennin tiedot](https://go.microsoft.com/fwlink/?linkid=845208) mallina suunniteltaessa ER-muotoa. (Lisätietoja muotomallin tuomisesta on tehtäväoppassa.)

[![Tuonti- tai vientitehtävien määritys](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png)

Voit muokata **Tuonti-/vientitoiminnot** muotokonfiguraatiota seuraavasti.

1. Valitse **Suunnittelutoiminto**.
2. **Muoto**-välilehdellä anna tämän muodon tiedostoelementille nimi **Excel-tulostustiedosto**.

    [![Excel-tulostiedoston elementti](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)

3. Määritä **Määritys**-välilehdessä Excel-tiedoston nimi, joka luodaan aina, kun tämä muoto suoritetaan. Määritä liittyvä lauseke palauttamaan arvon **Tietojen tuonti ja vienti** (Tuodut ja viedyt tiedot) (.xlsx-tiedostotunniste lisätään automaattisesti).

    [![Muodon suunnittelija](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)

4. Lisää uusi tietolähdenimike tälle muodolle. (Tätä numerointia tarvitaan myöhempää tietojen sidontaa varten.)

    1. Nimeä tietolähde **direction\_enum**.
    2. Valitse **Tietomallin luettelointi** tietolähdetyypiksi.
    3. Lisätietoja on kohdassa **Suunta**-tietomallin luettelointi.

    [![direction_enum](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)

5. Suorita **Intrastat**-tietomallin elementtien ja suunnitellun muodon elementtien sidonta kuvassa esitetyllä tavalla.

    [![Sidonnan viimeistely](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Kun se on suoritettu, ER-muoto luo tulosteen Excel-muodossa. Se lähettää Intrastat-tapahtumien tiedot tulosteeseen ja erottaa ne tapahtumina, jotka kuvaavat tuonti- tai vientitehtäviä. Valitsemalla **Suorita** voit testata Intrastat-tapahtumaluettelon uuden ER-muodon **Intrastat**-sivulla (**Vero** &gt; **Ilmoitukset** &gt; **Ulkomaankauppa** &gt; **Intrastat**).

[![Intrastat-sivu](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png)

Seuraava tuloste luodaan. Tiedoston nimi on **Import and export details.xlsx**, kuten määritit muodon asetuksissa.

[![Import and export details.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>ER-kohteiden määrittäminen
Sinun on määritettävä ER-kehys uuden ER-muotokonfiguraation tulosteen lähettämiseksi erityistavalla.

- Tuloste on lähetettävä valitun SharePoint Serverin kansioon.
- Jokaisen muotokonfiguraatioon suorituksen on luotava saman Excel-tiedoston uusi versio.

**Sähköinen raportointi** -sivulla (**Organisaation hallinto** &gt; **Sähköinen raportointi**) valitse kohta **Sähköisen raportoinnin kohde** ja lisää uusi kohde. **Viite**-kentässä valitse **Tuonti-/vientitoiminnot**-muotokonfiguraatio, jonka loit aiemmin. Lisää uusi tiedoston kohdetietue viitteeksi seuraavasti.

1. Valitse **Nimi**-kenttään tiedoston kohteen otsikko.
2. **Tiedostonimi**-kentässä valitse nimi **Excel-tulostustiedosto** Excel-tiedoston muodoksi.

Valitse **Asetukset**-painike uudelle kohdetietueelle. Noudata seuraavia ohjeita **Kohdeasetukset**-valintaikkunassa.

1. Määritä **Power BI** -välilehdessä **Käytössä**-asetukseksi **Kyllä**.
2. Valitse **SharePoint**-kentässä **Jaettu**-tiedostotyyppi, jonka loit aiemmin.

## <a name="schedule-execution-of-the-configured-er-format"></a>Konfiguroidun ER-muodon suorituksen ajoittaminen
1. **Konfiguroinnit**-sivulla (**Organisaation hallinto** &gt; **Sähköinen raportointi** &gt; **Konfiguroinnit**) konfiguraatioiden puurakenteessa, valitse **Tuonti-/vientitoiminnot**-konfiguraatio, jonka loit aiemmin.
2. Vaihda version 1.1 tila **Luonnos**-tilasta **Valmis** -tilaan, jotta voit ottaa tämän muodon käyttöön.

    [![Konfiguroinnit-sivu](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png)

3. Valitse valmis versio **Tuonti-/vientitoiminnot**-konfiguraatiosta ja valitse sitten **Suorita**. Huomaa, että konfiguroitua kohdetta sovelletaan tulosteeseen, joka luodaan Excel-muodossa.
4. Määritä **Eräkäsittely**-asetukseksi **Kyllä** raportin suorittamiseksi valvomattomassa tilassa.
5. Valitse **Toistuminen** ja ajoita eräajon suorittamisen pakollinen toistuminen. Toistuminen määrittää, kuinka usein päivitetyt tiedot siirretään Power BI:hin.

    [![Sähköisen raportin parametrit -valintaikkuna](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png)

6. Kun se on määritetty, ER-raportin suoritustyö löytyy **Erätyöt**-sivulla (**Järjestelmän hallinta &gt; Kyselyt &gt; Erätyöt**).

    [![Erätyöt-sivu](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png)

7. Kun tämä työ suoritetaan ensimmäisen kerran, kohde luo uuden Excel-tiedoston, jolle on määritetty nimi valitussa SharePoint-kansiossa. Myöhemmin joka kerta, kun työ suoritetaan, kohde luo Excel-tiedostosta uuden version.

    [![Excel-tiedoston uusi versio](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>Power BI -tietojoukon luominen käyttämällä ER-muodon tulostetta
1. Kirjaudu Power BI:hin ja avaa aiemmin luotu Power BI -ryhmä (työtila) tai luo uusi ryhmä. Napsauta **Lisää** kohdassa **Tiedostot** **Tuo tai yhdistä tietoihin** -osassa tai napsauta plus-merkkiä (**+**) **Tietojoukot**-kohdan vieressä vasemmassa ruudussa.

    [![Tietojoukon luonti](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png)

2. Valitse **SharePoint - ryhmäsivustot** -vaihtoehto ja kirjoita polku, jota käytät SharePoint Serverissä (esimerkissä `https://ax7partner.litware.com`).
3. Siirry **/Shared Documents/GER data/PowerBI**-kansioon ja valitse Excel-tiedosto, jonka olet luonut uuden Power BI -tietojoukon tietojen lähteeksi.

    [![Excel-tiedoston valitseminen](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png)

4. Valitse **Yhdistä** ja valitse **Tuo**. Luodaan uusi tietojoukko, joka perustuu valittuun Excel-tiedostoon. Tietojoukko voidaan lisätä myös automaattisesti äsken luotuun raporttinäkymään.

    [![Tietojoukko koontinäytössä](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png)

5. Määritä päivitysaikataulu tälle tietojoukolle kausittainen päivityksen pakottamiseksi Kausittaiset päivitykset mahdollistavat uusien liiketoimintatietojen käytön ER-raportin kausittaisen suorittamisen ansiosta SharePoint Serverille luodun Excel-tiedoston uuden version avulla.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Power BI -raportin luominen käyttämällä uutta tietojoukkoa
1. Valitse **Tietojen tuonti ja vienti** luomassasi Power BI -tietojoukossa.
2. Määritä visualisointi. Valitse esimerkiksi **Täytetty kartta** -visualisointi ja määritä se seuraavasti:

    - Määritä **CountryOrigin**- tietojoukkokenttä kartan visualisoinnin **Sijainti**-kenttään.
    - Määritä **Määrä**- tietojoukkokenttä kartan visualisoinnin **Värikylläisyys**-kenttään.
    - Lisää **Tehtävä** ja **Vuosi** tietojoukkokentät kartan visualisoinnin **Suodattimet**-tietokenttäkokoelmaan.

3. Tallenna Power BI -raportti **Tuodut ja viedyt tiedot -raporttina**.

    [![Tuonnin ja viennin tietojen raportti](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png)

    Huomaa, että kartassa näkyvät maat/alueet, jotka on mainittu Excel-tiedostosta (Itävalta ja Sveitsi tässä esimerkissä). Nämä maat/alueet näkyvät värillisinä ja osoittavat laskutettujen summien osuuden.

4. Päivitä Intrastat-tapahtumien luettelo. Vientitapahtuma, joka on peräisin Italiasta, lisätään.

    [![Intrastat-tapahtumien luettelo](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png)

5. Odota ER-raportin seuraavaa ajoitettua suorittamista ja Power BI -tietojoukon seuraavaa ajoitettua päivitystä. Käy läpi Power BI -raportti (valitse vain tuotujen tapahtumien näyttö). Päivitetyssä kartassa näkyy nyt Italia.

    [![Päivitetty määritys](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-finance"></a>Power BI -raportin käyttö Financessa
Voit määrittää Power BI -integraation. Lisätietoja on kohdassa [Power BI -integroinnin määrittäminen työtiloille](configure-power-bi-integration.md).

1. Valitse **Sähköinen raportointi** -työtilan sivulla, joka tukee Power BI -integrointia (**Organisaation hallinto** &gt; **Työtilat** &gt; **Sähköisen raportoinnin työtila**), **Asetukset** &gt; **Avaa raporttiluettelo**.
2. Valitse **Tuodut ja viedyt tiedot** Power BI -raportti, jonka olet luonut, jotta raportti näytetään valitun sivun toimintonimikkeenä.
3. Valitse toimintonimike, joka avaa sivun, jossa näkyy Power BI:ssa suunniteltu raportti.

    [![Tuonnin ja viennin tietojen raportti](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md)

[Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)
