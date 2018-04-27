---
title: "MPOS- ja CPOS-myyntipisteiden demotietojen näyttöasettelut"
description: "Tässä ohjeaiheessa on tietoja Microsoft Dynamics 365 for Retail -sovelluksen myyntipisteiden käyttökokemusten demotietojoukon näyttöasetteluista."
author: zlinster
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: zlinster
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 797058bdbbdb63a08eb35034ffe3c913307f38df
ms.openlocfilehash: e812bb13c903e72e31e62effd0c70f9b9d62de55
ms.contentlocale: fi-fi
ms.lasthandoff: 03/05/2018

---

# <a name="demo-data-screen-layouts-in-mposcpos"></a>MPOS- ja CPOS-myyntipisteiden demotietojen näyttöasettelut

[!INCLUDE [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja Microsoft Dynamics 365 for Retail -sovelluksen myyntipisteiden käyttökokemusten demotietojoukon näyttöasetteluista.

## <a name="overview"></a>Yleiskuvaus

Retail-demotietoihin sisältyvissä mallinäyttöasetteluissa on sisältöä, joka on optimoitu useita vähittäismyyntisegmenttejä, myymälän työntekijöiden rooleja ja laitteita varten. Yksi asettelu voi sisältää useita painikeruudukoiden asettelukokoja ja -yhdistelmiä. Näin myymälän työntekijät voiva siirtyä laitteiden ja asemien välillä. Tässä ohjeaiheessa käsitellään näiden asetteluiden välisiä eroja, asetteluiden työvaiheita ja niiden mahdollistamia yleisiä käyttökokemuksia.

![Laitteiden välisten demotietojen asettelut](../retail/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a>Näyttöasettelun tunnuksen rakenne

Retail-sovelluksen äyttöasettelut ovat kohdassa **Retail** > **Kanavan asetukset** > **Myyntipisteen asetukset** > **Myyntipiste** > **Näyttöasetukset**.

![Retail-sovelluksen näyttöasettelut](../retail/media/demo-screen-layouts-fig-2-1.png)

Näyttöasetteluiden tunnuksissa voi olla enintään 10 merkkiä. Tunnus on merkkijono, joka sisältää seuraavat kolme tietoa tässä järjestyksessä:

1. Yritys 
2. Asetteluversio
3. Henkilötyyppi

### <a name="company"></a>Yritys 

| Kirje | Yritys          |
|--------|-----------------|
| A      | Adventure Works |
| P      | Fabrikam:        |
| Y      | Contoso         |

### <a name="layout-version"></a>Asetteluversio

| Version numero | kuvaus                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| 3              | Perusversio, joka tukee eri laitteiden ja kuvasuhteiden useita näyttökokoja |
| 3.1            | Perusversio, jolla on **Suositellut tuotteet** -ruudun lisätuki        |

### <a name="persona"></a>Henkilötyyppi

| Lyhenne | Henkilötyyppi       | Sisältö |
|--------------|---------------|----------|
| CSH          | Kassa       | Kassa-asettelut sisältävät kaikki tapahtumiin liittyvät työvaiheet, kuten asiakastilaukset, palautukset, alennukset, mitätöinnit ja lahjakortit. Nämä asettelut sisältävät myös varastonhallinnan päivittäiset tehtävät, kuten hintatarkistukset, varastohaut ja varaston inventoinnit. Aloitussummat, vuorojen keskeytykset ja kello sisältävät myös perusvuorojen hallinnan. |
| MGR          | Myymäläpäällikkö | Myymäläpäällikön asettelu sisältää kaikki tapahtumiin liittyvät työvaiheet, jotka löytyvät kassanhoitajan asetteluista. Niiden lisäksi se sisältää verojen ohitukset. Nämä asettelut sisältävät myös varastonhallinnan päivittäiset tehtävät, kuten hintatarkistukset, varastohaut ja varaston inventoinnit. Vuoronhallinta sisältää vuorojen aloittamisen, keskeyttämisen ja päättämisen. Lisäksi asettelut sisältävät kassatoiminnot tapahtumille, poistoille, kassan laskemiselle maksuvälineittäin ja toimituksille kassakaappiin ja pankkiin. Näiden asetteluiden avulla voi myös käyttää suoritusraportteja ja tulostaa X- ja Z-raportteja. |
| STK          | Varastonhoitaja   | Varastonhoitajan asettelut on optimoitu varastonhallintaa varten. Niiden avulla voi käyttää hinnantarkistusten, varastohakujen, keräilyjen ja vastaanottojen, varaston inventointien ja myyntirakenteen purkamisen päivittäisiä tehtäviä. Nämä asettelut sisältävät myös aikaan ja vuorojen keskeytykseen liittyvät vuorojen perustyövaiheet. Vaikka nämä asettelut on tarkoitettu pääasiassa tilausjärjestelmätehtäviä varten, myymälänhoitajilla on samoja tapahtumanäyttöjen työvaiheet kuin kassanhoitajilla. |

### <a name="example-layout"></a>Esimerkkiasettelu

Tässä on esimerkki Fabrikam-yrityksen asettelun versio 3 näyttöasettelun tunnuksesta sekä myymäläpäällikön henkilötyyppi:

F3MGR

Seuraavassa kuvassa on esimerkki Fabrikamin myymäläpäällikön aloitusnäytöstä.

![Fabrikam myymäläpäällikön aloitusnäyttö](../retail/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a>Asettelukoot

### <a name="full-vs-compact-layouts"></a>Täydeliset ja kompaktit asettelut

Näyttöasettelu voi sisältää täysikokoisten ja pienikokoisten laitteiden kokoonpanoja. Tämän vuoksi käyttäjä voidaan määrittää yhteen näyttöasetteluun, joka toimii myymälän erikokoissa ja erityyppisissä laitteissa.

- **Modern POS - täydellinen** - täydelliset asettelut ovat yleensä parhaimmillaan suurissa näytöissä kuten pöytätietokoneiden näytöissä tai tableteissa. Käyttäjät voivat valita asettelun sisältämät käyttöliittymäelementit, määrittää elementtien koon ja sijoittelun sekä elementtien yksityiskohtaiset ominaisuudet. Täydelliset asettelut tukevat sekä vaaka- että pystykokoonpanoja.
- **Modern POS - kompakti** - kompaktit asettelut sopivat yleensä parhaiten puhelimiin tai pieniin tabletteihin. Kompaktien laitteiden suunnittelumahdollisuudet ovat rajalliset. Käyttäjät voivat määrittää kuitti- ja summaruutujen sarakkeet ja kentät.

### <a name="screen-resolutions-that-are-provided"></a>Käytettävissä olevat näytön tarkkuudet

Seuraavassa taulukossa ovat tavallisissa näyttöjen resoluutioissa käytettävissä olevat asetteluiden koot.

| Asettelutyyppi | Tarkkuus | Kuvasuhde | Kohdenäyttö          |
|-------------|------------|--------------|-------------------------|
| Järjestä uudelleen\*   | 480 × 853  | 16:9         | Puhelimet                  |
| Täysi        | 1 024 × 768 | 4:3          | Tabletit                 |
| Täysi\*      | 1 280 × 720 | 16:9         | Tabletit                 |
| Täysi        | 1 366 × 768 | 16:9         | Tabletit, suuret näytöt |
| Täysi        | 1 440 × 960 | 3:2          | Tabletit, suuret näytöt |

\* Nämä asettelujen lisäkoot ovat käytettävissä vain Adventure Works- ja Fabrikam-asetteluissa.


>[!TIP]
> Myyntipiste valitsee automaattisesti asettelujen koot sen mukaan, mikä käytettävissä oleva koko on lähimpänä nykyisen sovellusikkunan näytön resoluutiota. Voit etsiä Retail Modern POS (MPOS)- tai Retail Cloud POS (CPOS) -sovelluksessa tällä hetkellä käytössä olevan näyttöasettelun tunnuksen ja näytön resoluution avaamalla **Asetukset**-sivun ja siirtymällä **Istunnon tiedot** -osaan. Voit tarkastella myös nykyisen sovelluksen tai selainkehyksen todellista ikkunan resoluutiota. Kun nämä tiedot ovat käytettävissä, löydät Retail-sovelluksen asettelun sisällön lähteen siirtymällä kohtaan **Kanavan asetukset** > **Myyntipisteen asetukset** > **Myyntipiste** > **Näyttöasettelut**.


![Näyttöasettelut ja asettelun resoluutiot/koot Retail-ohjelmassa ja myyntipisteessä](../retail/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a>Yritykset ja tuotemerkit

Jokainen kuvitteellinen yritys on luotu eri vähittäismyyntisegmenttiä varten. Yritykset sisältävät tuoteluettelot, jotka on suunniteltu yrityksen markkinoita varten. Jokaisella yrityksellä on yksilöivä visuaalinen tuotemerkki ja tuotteet. Brändäyksen elementtejä ovat korostusväri, tumma tai vaalea teema ja valokuvat, jotka tarjoavat realistiset käyttökokemukset.

### <a name="company-segment-and-visual-characteristics"></a>Yrityksen segmentti ja visuaaliset ominaisuudet

| Yritys          | Toimipaikka | Segmentti        | Korostus | Teema |
|-----------------|----------|----------------|--------|-------|
| Adventure Works | Seattle  | Urheilutarvikkeet | Sininen   | Tumma  |
| Fabrikam:        | Houston  | Muoti        | Vihreä  | Vaalea |
| Contoso         | Boston   | Elektroniikka    | Punainen    | Tumma  |


>[!NOTE]
> Adventure Works ja Fabrikam on tuotemerkkien kaksi lippulaivaa. Contoso on käytettävissä, mutta se ei sisällä kaikkia asetteluita.


Seuraavissa kuvissa ovat kolmen kuvitteellisen yrityksen aloitussivut ja tapahtumasivut.

### <a name="adventure-works"></a>Adventure Works

![Adventure Worksin demotietojen aloitussivu.](../retail/media/demo-screen-layouts-fig-4-1a.png)

![Adventure Worksin demotietojen tapahtumasivu.](../retail/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a>Fabrikam:

![Fabrikamin demotietojen aloitussivu.](../retail/media/demo-screen-layouts-fig-4-2a.png)

![Fabrikamin demotietojen tapahtumasivu.](../retail/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a>Contoso

![Contoso demotietojen asettelut](../retail/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a>Käyttäjän sisäänkirjausmatriisi

Käyttäjien käytettävissä on erilaisia näyttöasetteluita. Näytöt voi ottaa käyttöön seuraavan taulukon avulla. Kirjaudu sisään soveltuvan operaattorin tunnuksen avulla.

| Yritys          | Näyttöasettelun tunnus | Henkilötyyppi          | Operaattorin tunnukset           |
|-----------------|------------------|---------------   |------------------------|
| Adventure Works | A3MGR            | Myymäläpäällikkö    | 000154, 000137, 000073 |
| Adventure Works | A3CSH            | Kassa          | 000150, 000175, 000165 |
| Adventure Works | A3STK            | Varastonhoitaja      | 000155, 000181, 000152 |
| Fabrikam:        | F3MGR            | Myymäläpäällikkö    | 000160, 000168, 000163 |
| Fabrikam:        | F3CSH            | Kassa          | 000161, 000113, 000114 |
| Fabrikam:        | F3STK            | Varastonhoitaja      | 000164, 000112, 000123 |
| Contoso         | C3MGR            | Myymäläpäällikkö    | 000100, 000111         |
| Contoso         | C3CSH            | Kassa          | 000110, 000120         |
| Contoso         | Ei käytettävissä   | Varastonhoitaja      | Ei käytettävissä         |


>[!TIP]
> Saat parhaat tulokset, kun aktivoit vastaavan myymäläsijainnin kassakoneen ja määrität yritykseksi sen henkilötyypin yrityksen, jonka haluat kirjautuvan sisään. Näin voit varmistaa, että visuaalinen profiili ja brändäyskuvat ovat kaikkialla samanlaiset. Jos esimerkiksi haluat nähdä Fabrikamin kassanhoitajan asettelun, aktivoi Houstonin alueen kassakone.


<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail > Channel setup > POS setup > POS > Images**. -->

<!-- ![Images in Dynamics 365 for Retail](../retail/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../retail/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->

