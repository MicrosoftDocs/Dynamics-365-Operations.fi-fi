---
title: Modern POS:n (MPOS:n) ja pilvimyyntipisteen esittelytietojen näyttöasettelut
description: Tässä artikkelissa on tietoja Dynamics 365 Commerce -sovelluksen myyntipisteiden käyttökokemusten demotietojoukon näyttöasetteluista.
author: josaw1
ms.date: 10/05/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: eb7a288b61e8b467dd8ad6a8f7dc42b7fca0d943
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897222"
---
# <a name="demo-data-screen-layouts-in-modern-pos-mpos-and-cloud-pos"></a>Modern POS:n (MPOS:n) ja pilvimyyntipisteen esittelytietojen näyttöasettelut

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja Dynamics 365 Commerce -sovelluksen myyntipisteiden käyttökokemusten demotietojoukon näyttöasetteluista.

## <a name="overview"></a>Yleiskatsaus

Commerce-demotietoihin sisältyvissä mallinäyttöasetteluissa on sisältöä, joka on optimoitu useita vähittäismyyntisegmenttejä, myymälän työntekijöiden rooleja ja laitteita varten. Yksi asettelu voi sisältää useita painikeruudukoiden asettelukokoja ja -yhdistelmiä. Näin myymälän työntekijät voiva siirtyä laitteiden ja asemien välillä. Tässä artikkelissa käsitellään näiden asetteluiden välisiä eroja, asetteluiden työvaiheita ja niiden mahdollistamia yleisiä käyttökokemuksia.

![Laitteiden välisten demotietojen asettelut.](../commerce/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a>Näyttöasettelun tunnuksen rakenne

Retail-sovelluksen näyttöasettelut ovat kohdassa **Retail ja Commerce** \> **Kanavan asetukset** \> **Myyntipisteen asetukset** \> **Myyntipiste** \> **Näyttöasetukset**.

![Näytön asettelusivu.](../commerce/media/demo-screen-layouts-fig-2-1.png)

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
| 4              | Päivitetyn laajennetun Fabrikam-asettelun laajennettu versio                                  |

### <a name="persona"></a>Henkilötyyppi

| Lyhenne | Henkilötyyppi       | Sisältö |
|--------------|---------------|----------|
| CSH          | Kassa       | Kassa-asettelut sisältävät kaikki tapahtumiin liittyvät työvaiheet, kuten asiakastilaukset, palautukset, alennukset, mitätöinnit ja lahjakortit. Nämä asettelut sisältävät myös varastonhallinnan päivittäiset tehtävät, kuten hintatarkistukset, varastohaut ja varaston inventoinnit. Aloitussummat, vuorojen keskeytykset ja kello sisältävät myös perusvuorojen hallinnan. |
| MGR          | Myymäläpäällikkö | Myymäläpäällikön asettelu sisältää kaikki tapahtumiin liittyvät työvaiheet, jotka löytyvät kassanhoitajan asetteluista. Niiden lisäksi se sisältää verojen ohitukset. Nämä asettelut sisältävät myös varastonhallinnan päivittäiset tehtävät, kuten hintatarkistukset, varastohaut ja varaston inventoinnit. Vuoronhallinta sisältää vuorojen aloittamisen, keskeyttämisen ja päättämisen. Lisäksi asettelut sisältävät kassatoiminnot tapahtumille, poistoille, kassan laskemiselle maksuvälineittäin ja toimituksille kassakaappiin ja pankkiin. Näiden asetteluiden avulla voi myös käyttää suoritusraportteja ja tulostaa X- ja Z-raportteja. |
| STK          | Varastonhoitaja   | Varastonhoitajan asettelut on optimoitu varastonhallintaa varten. Niiden avulla voi käyttää hinnantarkistusten, varastohakujen, keräilyjen ja vastaanottojen, varaston inventointien ja myyntirakenteen purkamisen päivittäisiä tehtäviä. Nämä asettelut sisältävät myös aikaan ja vuorojen keskeytykseen liittyvät vuorojen perustyövaiheet. Vaikka nämä asettelut on tarkoitettu pääasiassa tilausjärjestelmätehtäviä varten, myymälänhoitajilla on samoja tapahtumanäyttöjen työvaiheet kuin kassanhoitajilla. |

### <a name="example-layout"></a>Esimerkkiasettelu

Tässä on esimerkki Fabrikam-yrityksen asettelun versio 4 näyttöasettelun tunnuksesta sekä myymäläpäällikön henkilötyyppi:

F4MGR

Seuraavassa kuvassa on esimerkki Fabrikamin myymäläpäällikön aloitusnäytöstä.

![Fabrikamin myymäläpäällikön aloitusnäyttö.](../commerce/media/demo-screen-layouts-fig-2-2.png)

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
| Täysi\*      | 1536 × 864 | 16:9         | Tabletit, suuret näytöt |

\* Nämä asettelujen lisäkoot ovat käytettävissä vain Adventure Works- ja Fabrikam-asetteluissa.

> [!TIP]
> Myyntipiste valitsee automaattisesti asettelujen koot sen mukaan, mikä käytettävissä oleva koko on lähimpänä nykyisen sovellusikkunan näytön resoluutiota. Voit etsiä Modern POS (MPOS)- tai Retail Cloud POS (CPOS) -sovelluksessa tällä hetkellä käytössä olevan näyttöasettelun tunnuksen ja näytön resoluution avaamalla **Asetukset**-sivun ja siirtymällä **Istunnon tiedot** -osaan. Voit tarkastella myös nykyisen sovelluksen tai selainkehyksen todellista ikkunan resoluutiota. Kun nämä tiedot ovat käytettävissä, löydät asettelun sisällön lähteen valitsemalla **Kanavan asetukset** \> **POS-asetukset** \> **Myyntipiste** \> **Näytön asettelut**.

![Näyttöasettelut ja asettelun resoluutiot/koot Commercessa ja myyntipisteessä.](../commerce/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a>Yritykset ja tuotemerkit

Jokainen kuvitteellinen yritys on luotu eri vähittäismyyntisegmenttiä varten. Yritykset sisältävät tuoteluettelot, jotka on suunniteltu yrityksen markkinoita varten. Jokaisella yrityksellä on yksilöivä visuaalinen tuotemerkki ja tuotteet. Brändäyksen elementtejä ovat korostusväri, tumma tai vaalea teema ja valokuvat, jotka tarjoavat realistiset käyttökokemukset.

### <a name="company-segment-and-visual-characteristics"></a>Yrityksen segmentti ja visuaaliset ominaisuudet

| Yritys          | Toimipaikka | Segmentti        | Korostus | Teema |
|-----------------|----------|----------------|--------|-------|
| Adventure Works | Seattle  | Urheilutarvikkeet | Sininen   | Tumma  |
| Fabrikam        | San Francisco  | Muoti        | Vihreä  | Vaalea |
| Contoso         | Boston   | Elektroniikka    | Punainen    | Tumma  |

> [!NOTE]
> Adventure Works ja Fabrikam on tuotemerkkien kaksi lippulaivaa. Contoso on käytettävissä, mutta se ei sisällä kaikkia asetteluita.

Seuraavissa kuvissa ovat kolmen kuvitteellisen yrityksen aloitussivut ja tapahtumasivut.

### <a name="adventure-works"></a>Adventure Works

![Adventure Worksin demotietojen aloitussivu.](../commerce/media/demo-screen-layouts-fig-4-1a.png)

![Adventure Worksin demotietojen tapahtumasivu.](../commerce/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a>Fabrikam

![Fabrikamin demotietojen aloitussivu.](../commerce/media/demo-screen-layouts-fig-4-2a.png)

![Fabrikamin demotietojen tapahtumasivu.](../commerce/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a>Contoso

![Contoso demotietojen asettelut.](../commerce/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a>Käyttäjän sisäänkirjausmatriisi

Käyttäjien käytettävissä on erilaisia näyttöasetteluita. Näytöt voi ottaa käyttöön seuraavan taulukon avulla. Kirjaudu sisään soveltuvan operaattorin tunnuksen avulla.

| Yritys          | Näyttöasettelun tunnus | Henkilötyyppi       | Operaattorin tunnukset           |
|-----------------|------------------|---------------|------------------------|
| Adventure Works | A3MGR            | Myymäläpäällikkö | 000154, 000137, 000073 |
| Adventure Works | A3CSH            | Kassa       | 000150, 000175, 000165 |
| Adventure Works | A3STK            | Varastonhoitaja   | 000155, 000181, 000152 |
| Fabrikam        | F4MGR            | Myymäläpäällikkö | 000160, 000713         |
| Fabrikam        | F3CSH            | Kassa       | 000161, 000113, 000114 |
| Fabrikam        | F3STK            | Varastonhoitaja   | 000164, 000112, 000123 |
| Contoso         | C3MGR            | Myymäläpäällikkö | 000100, 000111         |
| Contoso         | C3CSH            | Kassa       | 000110, 000120         |
| Contoso         | Ei käytettävissä   | Varastonhoitaja   | Ei käytettävissä         |

> [!TIP]
> Saat parhaat tulokset, kun aktivoit vastaavan myymäläsijainnin kassakoneen ja määrität yritykseksi sen henkilötyypin yrityksen, jonka haluat kirjautuvan sisään. Näin voit varmistaa, että visuaalinen profiili ja brändäyskuvat ovat kaikkialla samanlaiset. Jos esimerkiksi haluat nähdä Fabrikamin kassanhoitajan asettelun, aktivoi Houstonin alueen kassakone.

<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail and Commerce \> Channel setup \> POS setup \> POS \> Images**. -->

<!-- ![Images in Dynamics 365 Commerce.](../commerce/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../commerce/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->


[!INCLUDE[footer-include](../includes/footer-banner.md)]