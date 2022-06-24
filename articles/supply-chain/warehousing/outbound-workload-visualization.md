---
title: Lähtevän kuormituksen visualisointi
description: Tässä artikkelissa on tietoja lähtevän kuormituksen visualisoinnista. Varastopäälliköt ja työnjohtajat voivat luoda tällä toiminnolla mukautettuja kuormituskaavioita, joilla voidaan seurata nykyisen työn edistymistä ja jäljellä olevia summia. Varastopäälliköt voivat luoda useita näkymiä ja määrittää tarvittavan automaattisen päivityksen.
author: Mirzaab
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0e5a2cd2aa458217ff212d45c0dd13c9d0623bd0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851330"
---
# <a name="outbound-workload-visualization"></a>Lähtevän kuormituksen visualisointi

[!include [banner](../includes/banner.md)]

**Lähtevän kuormituksen visualisointi** -sivulla voi käyttää lisäasetusominaisuuksia, joiden avulla varastopäälliköt ja työnjohtajat voivat luoda mukautettuja kuormituskaavioita. Näiden kaavioiden avulla voidaan sitten seurata nykyisen työn etenemistä ja siinä jäljellä olevaa määrää. Varastopäälliköt voivat luoda useita näkymiä ja määrittää tarvittavan automaattisen päivityksen. Lähtevän kuormituksen visualisoinnit sopivat näytettäväksi varaston suorituskykysivuilla.

Tämän toiminnon avulla voidaan seurata keräilytyön etenemistä. Tämä toiminto integroidaan työntekijöiden hallintaan, ja jos työntekijöiden hallinta on määritetty, lähtevän kuormituksen visualisoinnit voivat näyttää sen tuntimäärän laskelman, joka on jäljellä näytetystä keräilytyöstä (suodatettu).

## <a name="turn-the-outbound-workload-visualization-feature-on-or-off"></a>Lähtevän kuormituksen visualisointitoiminnon ottaminen käyttöön tai pois käytöstä

Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä. Järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Lähtevän kuormituksen visualisointi* -toimintoa [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

## <a name="set-up-outbound-workload-visualizations"></a>Lähtevän kuormituksen visualisoinnin määrittäminen

Visualisoinnit määritetään luomalla suodatinkokoelma (näkymät) ja suunnittelemalla kukin suodatin siten, että se näyttää erityyppisen analyysin. Voit suunnitella suodattimet **Määritä suodattimet** -sivulla.

Lähtevän kuormituksen visualisointi määritetään seuraavasti:

1. Valitse **Varastonhallinta \> Varaston seurantaraportit \> Lähtevän kuormituksen visualisointi**.

    **Lähtevän kuormituksen visualisointi** -sivu avautuu. Kun suodattimia on luotu, visualisointi näkyy tällä sivulla. Voit luoda tarvittavan määrän suodattimia. Kaikki luodut suodattimet tallennetaan käyttäjätilille myöhempää käyttöä varten. Kullakin käyttäjällä on toisin sanoen itse luotu suodatinjoukko. Näitä suodattimia ei jaeta muiden käyttäjien kanssa.

1. Valitse **Lähtevän kuormituksen visualisointi** -sivun toimintoruudun **Suodattimet**-välilehdessä **Määritä suodattimet**.
1. Lisää suodatin valitsemalla **Määritä suodattimet** -sivun toimintoruudussa **Uusi** ja määritä sitten siinä seuraavat kentät:

    - **X-akselin ryhmätaulu** – valitse taulukko, jonka kenttiä käytetään X-akselin arvojen ryhmittämiseen.
    - **X-akselin ryhmäkenttä** – valitse **X-akselin ryhmätaulu** -kentässä valitun taulun kentistä kenttä, jolla X-akselin arvot ryhmitetään.
    - **X-akselin arvotaulu** – valitse taulukko, jonka kenttiä käytetään ryhmien lisäanalysointiin.
    - **X-akselin arvokenttä** – valitse **X-akselin arvotaulu** -kentässä valitun taulun kentistä kenttä, jonka arvoilla kutakin ryhmää analysoidaan.
    - **Automaatiinen päivitys** – valitse, päivitetäänkö visualisointi automaattisesti.
    - **Päivitysväli (minuuttia)** – anna automaattisten päivitysten väli minuutteina.
    - **Näyttötaso** – valitse, näkyykö kaaviossa avoimien rivien vai avoimien otsikoiden määrät.
    - **Keräilytyyppi** – jos **Näyttötaso**-kentän asetukseksi määritetään _Avoimet rivit_, valitse, sisältääkö kaavion avoimien työrivien määrä ensimmäiset keräilyt, vaiheittaiset keräilyt vai sekä ensimmäiset että vaiheistetut keräilyt.
    - **Toimipaikka** – valitse toimipaikka, johon kaavio ladataan.
    - **Varasto** – valitse varasto, johon kaavio ladataan.
    - **Sisällytettävät päivä** – anna niiden päivien määrä menneisyydessä, joille kaavio luodaan.
    - **Työtilauksen tyyppi** – valitse suodatusperusteena käytettävät työtilauksen tyypit.

    ![Määritä suodattimet -sivu.](media/work-viz-filters-1.png "Määritä suodattimet -sivu")

1. Palaa **Lähtevän kuormituksen visualisoinnit** -sivulle sulkemalla **Määritä suodattimet** -sivu.

    **Lähtevän kuormituksen visualisoinnit** -sivulla näkyy nyt uusiin suodatusasetuksiin perustuvia tietoja. Uusi suodatin on nyt käytettävissä ja valitaan **Suodatin**-kentässä. Seuraavat kentät ovat käytettävissä kaavion yläosassa:

    - **Suodatin** – Tämä kenttä sisältää kaikki tähän mennessä luodut kentät. Valitse suodatin, jonka tiedot näytetään kaaviossa.
    - **Päivitetty viimeksi** – tässä kentässä päivämäärä ja aika, jolloin kaavion tiedot viimeksi päivitettiin.
    - **Arvioitu tai toteutunut aika** – Jos järjestelmään on määritetty työn standardit, määritä asetukseksi *Kyllä*, jolloin kertyneet keräilyaika-arviot näytetään kaavion kunkin sarakkeen yläosassa. Jos työn standardeja ei käytetä, tämä vaihtoehto ei ole käytettävissä.

    ![Esimerkkivisualisointi.](media/work-viz-chart.png "Esimerkkivisualisointi")

1. Näytä liitetyn työrivin tiedot valitsemalla jokin kaavion palkki.

    ![Työrivin tiedot.](media/work-viz-work-details.png "Työrivin tiedot")

## <a name="example-outbound-workload-visualization-for-zones"></a>Esimerkki: vyöhykkeiden lähtevän kuormituksen visualisointi

Tässä esimerkissä määritetään visualisointi näyttämään kunkin vyöhykkeen työrivit ja kunkin työrivin tila (_Avoin_, _Suljettu_ tai _Peruutettu_). Tässä tapauksessa voidaan määrittää suodatin, jossa on seuraavat asetukset:

- **Suodattimen nimi** – anna suodattimen nimi (kuten _Vyöhykkeen ja työn tilan vertailu_).
- **Kuvaus** – anna suodattimen lyhyt kuvaus (kuten _Vyöhykkeen ja työn tilan vertailu_).
- **X-akselin ryhmätaulu** – valitse _Sijainnit_.
- **X-akselin ryhmä** – valitse _Vyöhyketunnus_.
- **X-akselin arvotaulukko** – valitse _Työ_, koska työtä halutaan tarkastella vyöhykekohtaisesti.
- **X-akselin arvokenttä** – valitse _Työn tila_, koska työn tilaa halutaan tarkastella.
- **Automaatiinen päivitys** – valitse, päivitetäänkö visualisointi automaattisesti.
- **Keräilytyyppi** – Valitse _Ensimmäiset keräilyt ja vaiheistetut keräilyt_, koska sekä ensimmäiset keräilyt ja valmistelusijaintien keräilyt halutaan sisällyttää. Toisin sanoen kaikki keräilytyörivit halutaan sisällyttää.
- **Näyttötaso** – valitse _Avoimet rivit_, koska tietoja halutaan tarkastella rivi- eikä työotsikkokohtaisesti.

Seuraavassa kuvassa on esimerkki tuloksena saatavasta kaaviosta.

![Vyöhykkeen ja työn tilan vertailun visualisointi.](media/work-viz-chart.png "Vyöhykkeen ja työn tilan vertailun visualisointi")

Kaaviossa on kaksi vyöhykettä, **TUOTANTO** ja **MÄÄRÄ**, sekä **Tyhjä**-niminen vyöhyke. **Tyhjä**-vyöhyke ilmaisee kaikki työrivit, jotka eivät ole vyöhykkeiden jäseniä. Kaavio näyttää aina kaikki ei-liittyvät suodatut tiedot **tyhjänä**, sillä näin saadaan mahdollisimman suuri näkyvyys. **TUOTANTO**-vyöhykkeen osalta kaavio näyttää kolme suljettua riviä ja neljä avointa riviä. **MÄÄRÄ**-vyöhykkeen osalta kaavio näyttää neljä suljettua riviä, yhden avoimen rivin ja 24 peruutettua riviä. Kaaviossa on vielä kahdeksan suljettua riviä, jotka eivät kuulu mihinkään vyöhykkeeseen ja jotka ovat siksi **Tyhjä**-vyöhykkeessä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]