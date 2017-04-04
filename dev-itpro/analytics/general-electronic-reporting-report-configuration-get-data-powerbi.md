---
title: "Määritä sähköisen Power BI toimittaa tietoja Dynamics 365 työvaiheiden raportointi"
description: "Tässä aiheessa kerrotaan, miten omaa sähköisen raportoinnin ER-konfiguraatiota voidaan käyttää tietojen siirron järjestämiseen omasta Dynamics 365 for Operations -esiintymästä Power BI-palveluihin. Tässä aiheessa käytetään esimerkkinä Intrastat-tapahtumia siirrettävinä liiketoimintatietoina. Power BI -karttavisualisointi käyttää tätä Intrastat-tapahtumatietoa näkymän esittämiseen yrityksen tuonti-/vientitoimintojen analyysia varten Power BI-raportissa."
author: kfend
manager: AnnBe
ms.date: 2016-10-31 13 - 22 - 29
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ed0192c44b6d7e88120c64e539ebb0ac3b379831
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-electronic-reporting-to-provide-power-bi-with-data-from-dynamics-365-for-operations"></a>Määritä sähköisen Power BI toimittaa tietoja Dynamics 365 työvaiheiden raportointi

Tässä aiheessa kerrotaan, miten omaa sähköisen raportoinnin ER-konfiguraatiota voidaan käyttää tietojen siirron järjestämiseen omasta Dynamics 365 for Operations -esiintymästä Power BI-palveluihin. Tässä aiheessa käytetään esimerkkinä Intrastat-tapahtumia siirrettävinä liiketoimintatietoina. Power BI -karttavisualisointi käyttää tätä Intrastat-tapahtumatietoa näkymän esittämiseen yrityksen tuonti-/vientitoimintojen analyysia varten Power BI-raportissa.

<a name="overview"></a>Yleiskuvaus
--------

Microsoft Power BI on kokoelma ohjelmistopalveluita, sovelluksia ja yhdistimiä, jotka yhdessä muuttavat ulkoiset tietolähteet yhdenmukaiseksi, visuaalisesti mukaansatempaavaksi ja interaktiiviseksi tiedoksi. Sähköisen raportoinnin (ER) avulla Microsoft Dynamics 365 for Operations -käyttäjät voivat helposti määrittää tietolähteet ja järjestää Dynamics 365 for Operations -tietojen siirron Power BI -palveluun. Tiedot siirretään tiedostoina OpenXML-laskentataulukko (Microsoft Excel -työkirjatiedosto) -muodossa. Siirretyt tiedostot tallennetaan Microsoft SharePoint Serveriin, joka on konfiguroitu tähän tarkoitukseen. Tallennettuja tiedostoja Power BI:ssa laadittaessa raportteja, jotka sisältävät visualisointeja (taulukot, kaaviot, kartat ja niin edelleen). Power BI -raportit jaetaan Power BI -käyttäjille, ja ne saadaan käyttöön Power BI -koontinäytöissä ja Dynamics 365 for Operations -sivuilla. Tässä aiheessa esitellään seuraavat tehtävät:

-   Dynamics 365 for Operations -konfigurointi
-   ER-muotokokoonpanon valmistelu Dynamics 365 for Operations -tietojen noutoa varten
-   ER-ympäristön konfigurointi tietojen siirtoon Power BI:sta
-   Siirretyn tiedon käyttö Power BI -raporttia luotaessa
-   Power BI -raportin valmistelu käytettäväksi Dynamics 365 for Operationsissa

## <a name="prerequisites"></a>Edellytykset
Tämän aiheen esimerkin suorittaminen edellyttää seuraavia käyttöoikeuksia:

-   Dynamics 365 for Operations -käyttöoikeudet seuraaville rooleille:
    -   Sähköisen raportoinnin kehittäjä
    -   Sähköisen raportoinnin toiminnallinen konsultti
    -   Järjestelmänvalvoja
-   Dynamics 365 for Operations -käyttöön konfiguroidun SharePoint Serverin käyttöoikeudet
-   Power BI-kehikon käyttöoikeudet

## <a name="configure-document-management-parameters"></a>Tiedostonhallintaparametrien konfigurointi
1.  Konfiguroi **Tiedostonhallintaparametrit**-sivulla SharePoint Serve -käyttöoikeudet, joita käytetään yrityksessä, johon olet kirjautunut (DEMF tässä esimerkissä).
2.  Testaa yhteys varmistaaksesi, että sinulle myönnetty SharePoint Server -käyttöoikeudet. [![Asiakirjojen hallinnan parametrit sivun](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)
3.  Avaa määritetty SharePoint-sivusto. Luo uusi kansio, johon ER tallentaa Excel-tiedostot, jotka sisältävä liiketoimintatietoja, joita Power BI -raportit tarvitsevat Power BI-tietojoukkojen lähteenä.
4.  Dynamics 365 for Operationsin **Tiedostotyypit**-sivulla voit luoda uuden tiedostotyypin, jota käytetään juuri luomasi SharePoint-kansioon kirjauduttaessa. Kirjoita **Tiedosto** **Ryhmä**-kenttään ja **SharePoint** **Sijainti**-kenttään ja kirjoita SharePoint-kansion osoite. [![Tyypit-sivulta asiakirjaan](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>Konfiguroi ER-parametrit
1.  **Sähköinen raportointi** -työtilassa valitse **Sähköisen raportoinnin parametrit** -linkki.
2.  **Liitteet** -välilehdessä valitse **Tiedosto** -tiedostotyyppi kaikissa kentissä.
3.  **Sähköinen raportointi** -työtilassa aktivoi pakollinen palveluntarjoaja valitsemalla **Aktivoi**. Lisätietoja saat **ER Valitse palveluntarjoaja** -tehtäväoppaasta.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>ER-tietomallin käyttö tietolähteenä
ER-tietomallin täytyy olla liiketoimintatietolähteenä, jota käytetään Power BI -raporteissa. Tämä tietomalli ladataan ER-konfiguraatiot-tietovarastosta. Lisätietoja on kohdassa [Lataa sähköiset raportoinnin määritykset Lifecycle Services -palvelusta](download-electronic-reporting-configuration-lcs.md) tai **ER Tuo kokoonpano Lifecycle Services -palvelusta** -tehtäväoppaasta. Valitse **Intrastat **tietomalliksi joka ladataan valitusta ER-konfiguraatiot-tietovarastosta. (Tässä esimerkissä 1 versio on käytössä.) Tämän jälkeen voit käyttää **Intrastat** ER mallin kokoonpano **kokoonpanot** sivulla. [![Sivun määritykset](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>Suunnittele ER-muotokonfiguraatio
Sinun on luotava uusi ER-muotokonfiguraatio, joka käyttää **Intrastat**-tietomallia liiketoimintatietolähteenä. Tämän muotokonfiguraation on luotava tulosteet sähköisinä asiakirjoina OpenXML (Excel-tiedosto) -muodossa. Lisätietoja on **Sähköisen raportoinnin OPENXML-muotoisten raporttimääritysten luonti** -tehtäväoppaassa. Nimeä uusi konfiguraatio **Import / export activities** (Tuonti-/vientitoiminnot) kuvassa esitetyllä tavalla. Käytä Excel-tiedostoa [ER data - import and export details](https://go.microsoft.com/fwlink/?linkid=845208) mallina suunniteltaessa ER-muotoa. (Lisätietoja muoto-malli tuo peli tehtävän opas.) [![Tuo / Vie määritys toimintaa](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png) muuttamiseen **tuo / vientitoimintaan** kokoonpano muodossa, toimi seuraavasti.

1.  Valitse **Suunnittelutoiminto**.
2.  **Muoto**-välilehdellä anna tämän muodon tiedostoelementille nimi **Excel-tulostustiedosto**. [![Excel tuotoksen tiedosto elementti](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)
3.  Määritä **Määritys**-välilehdessä Excel-tiedoston nimi, joka luodaan aina, kun tämä muoto suoritetaan. Määritä liittyvä lauseke palauttamaan arvon **Import and export details** (Tuodut ja viedyt tiedot) (.xlsx-tiedostotunniste lisätään automaattisesti). [![Format designer](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)
4.  Lisää uusi tietolähdenimike tälle muodolle. (Tätä numerointia tarvitaan myöhempää tietojen sidontaa varten.)
    1.  Tietolähteen nimi **suuntaan\_enum**.
    2.  Valitse **Tietomallin luettelointi** tietolähdetyypiksi.
    3.  Lisätietoja on kohdassa **Suunta**-tietomallin luettelointi.

    [![suuntaan\_luettelo](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)
5.  Suorita **Intrastat**-tietomallin elementtien ja suunnitellun muodon elementtien sidonta kuvassa esitetyllä tavalla. [![Viimeistellään sidonta](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Kun se on suoritettu, ER-muoto luo tulosteen Excel-muodossa. Se lähettää Intrastat-tapahtumien tiedot tulosteeseen ja erottaa ne tapahtumina, jotka kuvaavat tuonti- tai vientitehtäviä. Valitse **suorittaa** Testaa Intrastat-tapahtumien luettelosta uuden ER muoto **Intrastat** sivu (**vero**&gt;**ilmoitukset**&gt;**ulkomaankaupan**&gt;**Intrastat**). [![Intrastat-sivun](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png) muodostetaan seuraavan tulosteen tuloksen. Tiedoston nimi on **Import and export details.xlsx**, kuten määritit muodon asetuksissa. [![Tuonti- ja details.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>ER-kohteiden määrittäminen
Sinun on määritettävä ER-kehys uuden ER-muotokonfiguraation tulosteen lähettämiseksi erityistavalla.

-   Tuloste on lähetettävä valitun SharePoint Serverin kansioon.
-   Jokaisen muotokonfiguraatioon suorituksen on luotava saman Excel-tiedoston uusi versio.

- **Sähköisen raportoinnin** sivulla (**organisaation hallinta**&gt;**sähköisen raportoinnin**), valitse **sähköisen raportoinnin kohde** kohteen ja lisätä uuden kohteen. **Viite**-kentässä valitse **Tuonti-/vientitoiminnot**-muotokonfiguraatio, jonka loit aiemmin. Lisää uusi tiedoston kohdetietue viitteeksi seuraavasti.

1.  Valitse **Nimi**-kenttään tiedoston kohteen otsikko.
2.  **Tiedostonimi**-kentässä valitse nimi **Excel-tulostustiedosto** Excel-tiedoston muodoksi.

Valitse **Asetukset**-painike uudelle kohdetietueelle. Noudata seuraavia ohjeita **Kohdeasetukset**-valintaikkunassa.

1.  **Power BI** -välilehdessä määritä **Käytössä**-asetukseksi **Kyllä**.
2.  **SharePoint**-kentässä valitse **Jaettu**-tiedostotyyppi jonka loit aiemmin.

## <a name="schedule-execution-of-the-configured-er-format"></a>Konfiguroidun ER-muodon suorituksen ajoittaminen
- **Kokoonpanot** sivun (**organisaation hallinta**&gt;**sähköisen raportoinnin**&gt;**kokoonpanot**), kokoonpanot puussa, valitse **tuo / vientitoimintaan** määritykset, jotka olet luonut aiemmin. Vaihda version 1.1 tila**Luonnos**-tilasta **Valmis** -tilaan, jotta voit ottaa tämän muodon käyttöön. [![Määritykset-sivulla](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png) valmis versio **Tuo / Vie toimintaa** määritys ja valitse sitten **suorittaa**. Huomaa, että konfiguroitua kohdetta sovelletaan tulosteeseen, joka luodaan Excel-muodossa. Määritä **Eräkäsittely**-asetukseksi **Kyllä** raportin suorittamiseksi valvomattomassa tilassa. Valitse **Toistuminen** ja ajoita eräajon suorittamisen pakollinen toistuminen. Toistuminen määrittää, kuinka usein päivitetyt tiedot siirretään Dynamics 365 for Operationsista Power BI:hin. [![Sähköinen raportin parametrit-valintaikkunan](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png) kun on määritetty, löydät ER raportin suorittamisen työn **erätyöt** sivulla (**järjestelmän hallinta &gt;kyselyt &gt;erätyöt**). [![Työt-sivu erän](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png) tämä työ suoritetaan ensimmäisen kerran, kun kohde Luo uusi Excel-tiedosto, jolla on määritetty nimi valitun SharePoint-kansioon. Myöhemmin joka kerta, kun työ suoritetaan, kohde luo Excel-tiedostosta uuden version. [![Uusi versio Excel-tiedosto](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>Power BI -tietojoukon luominen käyttämällä ER-muodon tulostetta
Kirjaudu Power BI:hin ja avaa aiemmin luotu Power BI -ryhmä (työtila) tai luo uusi ryhmä. Joko napsauttamalla **Lisää** kohdassa **tiedostoja** - **tuominen tai yhteyden muodostaminen tietoihin** osan tai napsauttamalla plus-merkkiä (**+**) vieressä **DataSet-ryhmien** vasemmassa ruudussa. [![Tietojoukon luominen](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png) Valitse **SharePoint – sivustojen Team** vaihtoehto ja kirjoita sitten polku, jota käytät SharePoint Server (**https://ax7partner.spoppe.com** Esimerkissämme). Etsi **/Shared Documents/GER data/PowerBI**-kansio ja valitse Excel-tiedosto, jonka olet luonut uuden Power BI -tietojoukon tietojen lähteeksi. [![Excel-tiedosto valitsemalla](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png) Valitse **Connect**, ja sitten **tuo**. Luodaan uusi tietojoukko, joka perustuu valittuun Excel-tiedostoon. Tietojoukko voidaan lisätä myös automaattisesti äsken luotuun raporttinäkymään. [![DataSet kojelaudassa](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png) pakottamaan kausittaista päivitystä tämän DataSet-ryhmän Päivitä aikataulun määrittäminen. Kausittaiset päivitykset mahdollistavat uusien Dynamics 365 for Operationsin liiketoimintatietojen käytön ER-raportin kausittaisen suorittamisen ansiosta SharePoint Serverille luodun Excel-tiedoston uuden version avulla.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Power BI -raportin luominen käyttämällä uutta tietojoukkoa
Voit luoda uuden Power BI-raportin valitsemalla **Tietojen tuonti ja vienti** Power BI tietojoukon, jonka olet luonut. Määritä sitten visualisointi. Valitse esimerkiksi **Täytetty kartta** -visualisointi ja määritä se seuraavasti:

-   Määritä **CountryOrigin**- tietojoukkokenttä kartan visualisoinnin **Sijainti**-kenttään.
-   Määritä **Määrä**- tietojoukkokenttä kartan visualisoinnin **Värikylläisyys**-kenttään.
-   Lisää **Tehtävä** ja **Vuosi** tietojoukkokentät kartan visualisoinnin **Suodattimet**-tietokenttäkokoelmaan.

Tallenna Power BI -raportti **Tuodut ja viedyt tiedot -raporttina**. [![Tuoda ja viedä raportin tiedot](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png) Huomaa, että kartta näyttää Excel-tiedosto (Itävallan ja Sveitsin esimerkin) mainituista maista/alueista. Nämä maat/alueet näkyvät värillisinä ja osoittavat laskutettujen summien osuuden. Päivitä Intrastat-tapahtumien luettelo. Vientitapahtuma, joka on peräisin Italiasta, lisätään. [![Intrastat-tapahtumien luettelo](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png) odottamaan seuraavan ajoitetun toteuttamisen ER-raportti ja teho BI DataSet seuraavan ajoitetun päivityksen. Käy läpi Power BI -raportti (valitse vain tuotujen tapahtumien näyttö). Päivitetyssä kartassa näkyy nyt Italia. [![Päivitetty kartta](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-dynamics-365-for-operations"></a>Access Power BI -raportin käyttö Dynamics 365 for Operationsissa
Määritä Dynamics 365 for Operationsin ja Power BI:n integrointi. Lisätietoja on kohdassa [Power BI -integroinnin konfiguroiminen työtiloille](configure-power-bi-integration.md). - **Sähköisen raportoinnin** virtaa BI-integrointia tukeva työtila-sivun (**organisaation hallinta**&gt;**työtilojen**&gt;**sähköisen raportoinnin työtilan**), valitse **asetukset**&gt;**Avaa raportti luettelo**. Valitse **Tuodut ja viedyt tiedot** Power BI -raportti, jonka olet luonut, jotta raportti näytetään valitun sivun toimintonimikkeenä. Valitse toimintonimike, joka avaa Dynamics 365 for Operations -sivun, jossa näkyy Power BI:ssa suunniteltu raportti. [![Tuoda ja viedä raportin tiedot](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

<a name="see-also"></a>Lisätietoja
--------

[Sähköisen raportoinnin kohteet](electronic-reporting-destinations.md)

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)


