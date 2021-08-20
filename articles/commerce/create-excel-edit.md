---
title: Excel-työkirjan luominen vähittäismyyntitapahtumien muokkaamista varten
description: Tässä aiheessa kerrotaan, miten Excel-työkirja luodaan niin, että vähittäismyyntitapahtumia voidaan muokata Microsoft Dynamics 365 Commercessa.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: bfc3f6898087445e0276994ceeb52c178785bf3604fa163939327e99a0564f64
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753105"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a>Excel-työkirjan luominen vähittäismyyntitapahtumien muokkaamista varten

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan, miten Excel-työkirja luodaan niin, että vähittäismyyntitapahtumia voidaan muokata Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskatsaus

Asiakkaat voivat käyttää tätä esimääritettyä Excel-mallia järjestelmän eri osissa ja muokata ja tarkistaa sen avulla vähittäismyyntitapahtumia. Asiakkaat voivat luoda myös mukautetun Excel-työkirjan tätä tarkoitusta varten.

## <a name="create-and-configure-an-excel-workbook"></a>Excel-työkirjan luominen ja määrittäminen

Alla olevien ohjeiden avulla voit luoda ja määrittää Excel-työkirjan niin, että vähittäismyyntitapahtumia on mahdollista muokata.

1. Avaa Excel ja luo tyhjä työkirja.
1. Valitse **Lisää**-välilehdessä **Omat apuohjelmat**.
1. Valitse oikeanpuoleisessa ruudussa **Lisää palvelimen tiedot** -linkki.
1. Syötä palvelimen URL-osoite ja valitse **OK**.
1. Jos näyttöön tulee Sovelman rekisteröintejä ei löytynyt -virhesanoma, ratkaise ongelma seuraavasti:

    1. Siirry Commerce-sovelluksessa kohtaan **Järjestelmän hallinta \> Asetukset \> Office-sovelluksen parametrit**.
    1. Valitse **Sovellusparametrit**-pikavälilehdessä **Käynnistä sovellusparametrit**.
    1. Valitse vahvistussanomaruudussa **OK**.
    1. Valitse **Rekisteröidyt sovelmat** -pikavälilehdessä **Käynnistä sovelman rekisteröinti**.
    1. Toista nämä kolme vaihetta tarpeen mukaan.

1. Valitse **Rakenne** ja valitse sitten **Lisää taulukko**.
1. Valitse muokattavien tietojen perusteella entiteetit, jotka on lisättävä Excel-työkirjaan muokkausta varten. Käytä seuraavaa taulukkoa viitteenä.

    | Tapahtumatyyppi | Käytettävät tietoentiteetit |
    |------------------|----------------------|
    | Itsepalvelutukkutapahtumat, Online-tilaukset, Asynkroniset asiakastilaukset, Asynkroniset asiakastarjoukset | Tapahtuma (tarkistettavissa), Myyntitapahtuma (tarkistettavissa), Maksutapahtumat (tarkistettavissa), Verotapahtumat (tarkistettavissa), Alennustapahtumat (tarkistettavissa), Muutostapahtumat (tarkistettavissa) |
    | Toimitus pankkiin | Tapahtuma (tarkistettavissa), Pankkiin toimitetut maksuvälinetapahtumat (tarkistettavissa) |
    | Toimitus kassakaappiin | Tapahtuma (tarkistettavissa), Kassakaapin maksuvälinetapahtumat (tarkistettavissa) |
    | Kassan laskeminen maksuvälineittäin | Tapahtuma (tarkistettavissa), Kassan laskeminen maksuvälineittäin -tapahtumat (tarkistettavissa) |
    | Tulot, kulut | Tapahtuma (tarkistettavissa), Tulo-/kulutapahtumat (tarkistettavissa), Maksutapahtumat (tarkistettavissa) |
    | Ilmoita aloitussumma, Maksuvälineen poisto, Liukuva merkintä, Maksuvälineen vaihto, Laskun maksu, Asiakkaan talletus | Tapahtuma (tarkistettavissa), Maksutapahtumat (tarkistettavissa) |

    > [!NOTE]
    > Excel-työkirjaan tulee lisätä vain yksi tietoentiteetti. Lisäksi kaikki kentät, jotka on merkitty avainsymbolilla, on lisättävä soveltuvaan työkirjaan.

1. Kun työkirja on määritetty, ota tarvittavat suodattimet käyttöön. Varmista, että kohdistat samat suodattimet tiedoston kaikkiin laskentataulukoihin. Vältä suurten tietomäärien lataamista Excel-tiedostoon. Muussa tapauksessa suorituskyky voi alentua, ja Excelin ja järjestelmän toiminta hidastuu. Tiedoston suodattimina kannattaa aina käyttää Yritys-suodatinta ja joko Laskelmanumero- tai Tapahtumanumero-suodatinta.
1. Kun suodattimet on määritetty, päivitä tiedot valitsemalla **Päivitä**.
1. Muokkaa vaadittuja tietoja ja julkaise ne. Jos **Julkaise**-painike ei ole käytettävissä, joitakin kenttiä ei todennäköisesti ole lisätty Excel-työkirjaan.

## <a name="additional-resources"></a>Lisäresurssit

[Kassanhallinnan ja itsepalvelutukun hallintatapahtumien muokkaaminen ja tarkastaminen](edit-cash-trans.md)

[Online-tilauksen ja asynkronisten asiakastilausten tapahtumien muokkaaminen ja tarkistaminen](edit-order-trans.md)

[Vähittäismyyntitapahtumien taloushallinnon dimensioiden muokkaaminen](edit-financial-dim.md)

[Kenttien lisääminen Excel-työkirjaan vähittäismyyntitapahtumien muokkaamista varten](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]