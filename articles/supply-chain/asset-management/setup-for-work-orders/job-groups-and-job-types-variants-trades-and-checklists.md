---
title: Ylläpitotöiden tyyppiluokat ja ylläpitotöiden tyypit, ylläpitotöiden tyyppien variantit, ylläpitotöiden toimialat ja ylläpidon tarkistuslistat
description: Tässä ohjeaiheessa kuvataan ylläpitotöiden tyyppiluokat ja ylläpitotöiden tyypit, ylläpitotöiden tyyppien variantit, ylläpitotöiden toimialat ja ylläpidon tarkistuslistat resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetJobTypeDefaultForecast, EntAssetJobTrade, EntAssetJobTypeDefaultCopy, EntAssetChecklistVariableValueLookup, EntAssetChecklistTemplateCreate, EntAssetJobVariant, EntAssetJobTypeDefaultReference, EntAssetJobTypeDefaultChecklist, EntAssetJobTypeDefault, EntAssetJobType, EntAssetJobTypeDefaultChecklistCopy, EntAssetChecklistTemplate, EntAssetJobTypeDefaultDescription, EntAssetJobTypeLookup, EntAssetJobTypeDefaultToolCopy, EntAssetJobTypePreviewPart, EntAssetJobTypeDefaultTool, EntAssetJobTypeDefaultForecastCopy, EntAssetChecklistTemplateLookup, EntAssetJobGroup, EntAssetChecklistVariable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8bf7c53a6150a2beeca5c6e9b5ab4ea98584158d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427055"
---
# <a name="maintenance-job-type-categories-and-maintenance-job-types-maintenance-job-type-variants-maintenance-job-trades-and-maintenance-checklists"></a>Ylläpitotöiden tyyppiluokat ja ylläpitotöiden tyypit, ylläpitotöiden tyyppien variantit, ylläpitotöiden toimialat ja ylläpidon tarkistuslistat

[!include [banner](../../includes/banner.md)]

 

Käyttöomaisuustyyppi on liitetty jokaiseen käyttöomaisuuserään. Käyttöomaisuustyypit määrittävät kunnossapitotöiden tyypit (ja näin ollen kunnossapitotyöt), jotka voidaan suorittaa omaisuuserille. Sinun on valittava ylläpitotyötyyppi, kun luot työtilauksen. Voit valita vain ylläpitotyölajit, jotka liittyvät käyttöomaisuuserän tyypin asetuksiin.

Lisätietoja graafisen yhteenvedon käyttöomaisuuksien ja kunnossapidon työtyypeistä sekä niiden yhteydestä työtilauksiin on kohdassa [Toiminnalliset sijainnit ja resurssit](../overview/functional-locations-and-objects.md).

Kunnossapitotöiden tyypin variantit voidaan määrittää ylläpitotyön tyypille. Kunnossapitotöiden lajien variantit määrittävät työlajin variaatiot, kuten koot (pieni, keskikokoinen tai suuri), kaudet (viikoittain, joka toinen viikko, kuukausi tai kolme kuukautta) ja konfiguraatiot (matala vakio, joustava tai korkea suorituskyky).

Kunnossapitotöiden toimialat tarjoavat tietoja ammattialoista, kuten mekaaninen, sähkötyöt ja hydrauliset. Pätevyysvaatimukset voidaan määrittää kunnossapitotöiden toimialaan. Kaikkia kunnossapitotöiden toimialoja voidaan käyttää suhteessa kaikkiin kunnossapitotöiden tyyppeihin. Työtilauksen kunnossapitotöiden tyypin variantin ja/tai kunnossapitotyön toimialan valinta on valinnainen.

Kunkin ylläpitotyypin osalta voidaan määrittää ylläpitotyötyypin asetusten muunnoksia. Jos sinulla on esimerkiksi huoltotyön tyyppi nimeltä **Huolto**, voit luoda seuraavat muunnelmat huoltotyön tyypille: **Kuorma-autot 30 000 km**, **Autot 30 000 km** ja **Pakettiautot 30 000 km**.

Kunnossapitotöiden tyyppiluokkia käytetään, kun kerätään kunnossapitotyötyyppien ryhmä yleiskatsausta varten. Kunnossapitotöiden tyyppi luokkia voivat olla esimerkiksi **kalibrointi**, **tarkistus**, **peruskorjaus** ja **instrumentointi**.

Kunnossapidon tarkistusluettelomallien ja kunnossapidon tarkistusluettelomuuttujien avulla määritetään kunnossapitotarkistuslistoja. Kunnossapitotarkistusluettelot määritetään huoltotöiden tyypeille, ja niitä käytetään työtilauksissa.

Ensin määrität tarvittavat ylläpitotöiden tyyppiluokat, ylläpitotöiden tyyppien variantit ja ylläpitotöiden toimialat. Tämän jälkeen voit luoda kunnossapitotöiden tyyppejä. **Ylläpitotyön tyyppien oletukset** -sivulla voit luoda kaikki laitteessa tarvittavat ylläpitotyön tyyppien muutokset. Tällä sivulla voit myös määrittää ennusteita, ylläpitotarkistuslistoja ja työkaluja ylläpitotöiden yhdistelmiä varten.

> [!NOTE]
> Kunnossapitotyön tyyppi voi liittyä vain yhteen ylläpitotyön tyyppiluokkaan.

## <a name="create-a-maintenance-job-type-category"></a>Luo ylläpitotyön tyypin luokka

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Työt** \> **Ylläpitotöiden tyyppiluokat**.
2. Valitse **Uusi**.
3. Kirjoita **Ylläpitotyön tyyppiluokka** -kenttään ylläpitotyön tyyppiluokan tunnus.
4. Anna nimi **Nimi**-kenttään.

    Kun kunnossapitotöiden tyyppiluokat on liitetty kunnossapitotyötyyppeihin, **Työlajit**-kentässä näkyy tähän kunnossapitotyötyyppiin liittyvien huoltotöiden tyyppien määrä.

![Ylläpitotyön tyypin luokkasivu](media/01-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type-variant"></a>Luo ylläpitotyön tyypin variantti

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Työt** \> **Ylläpitotöiden tyyppien variantit**.
2. Valitse **Uusi**.
3. Kirjoita **Ylläpitotyön tyypin variantti** -kenttään ylläpitotyön tyypin variantin tunnus.
4. Syötä **Kuvaus**-kenttään kuvaus.
5. Lisää kunnossapitotyön tyyppi valitsemalla **Ylläpitotöiden tyypit** -pikavälilehdessä **Lisää**.
6. Valitse kunnossapitotyön tyyppi **Ylläpitotyön tyyppi** -kentässä.
7. Toista vaiheet 5-6, jos haluat lisätä kunnossapitotöiden tyyppejä kunnossapitotöiden tyyppivarianttiin.

    **Tiedot**-pikavälilehden **Työtyypit**-kentässä näkyy kunnossapitotöiden tyyppien määrä, jotka on lisätty tähän kunnossapitotöiden tyyppivarianttiin.

![Ylläpitotyön tyypin varianttisivu](media/02-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-trade"></a>Luo ylläpitotyön toimilala

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Työt** \> **Ylläpitotyön toimiala**.
2. Valitse **Uusi**.
3. Kirjoita **Toimiala**-kenttään kunnossapitotöiden toimialan tunnus.
4. Syötä **Kuvaus**-kenttään kuvaus.
5. Valitse **Osaamisalue**-pikavälilehdessä **Lisää**, jos haluat lisätä uuden osaamisalueen, joka liittyy kunnossapitotöiden toimialaan.
6. Valitse **Osaamisalue**-kentästä osaaminen.
7. Valitse **Taso**-kentästä osaamistaso.
8. Toista vaiheet 5-7, jos haluat lisätä kunnossapitotyöhön osaamisalueita.

    **Tiedot**-pikavälilehden **Osaamisalueet**-kentässä näkyy osaamisalueiden määrä, jotka on lisätty tähän kunnossapitotöiden toimialaan.

9. Lisää todistus kunnossapitottyön toimialaan valitsemalla **Todistukset** -pikavälilehdessä **Lisää**.
10. Valitse **Todistuksen tyyppi**-kentästä todistus.
11. Toista vaiheet 9-10, jos haluat lisätä kunnossapitotyöhön todistuksia.

    **Tiedot**-pikavälilehden **Todistukset**-kentässä näkyy todistuksien määrä, jotka on lisätty tähän kunnossapitotöiden toimialaan.

![Ylläpitotyön toimialasivu](media/03-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-variable"></a>Huollon tarkistusluettelon muuttujan luominen

Kun kunnossapitotyön oletustyypissä luodaan huollon tarkistusluettelon rivejä, sinun on valittava huollon tarkistusluettelon tyyppi. **Muuttuja** on yksi huollon tarkistusluettelon tyyppi. Sen avulla määritetään mahdollinen tulos sellaisen huollon tarkistusluettelorivin arvoalueelle, joka liittyy työtilausriviin. Muuttujan avulla voit luoda joukon ennalta määritettyjä tuloksia tarvitsematta tehdä tarkkaa mittausta.

**Esimerkki 1:** voit mitata öljymäärän määrittämällä kolme arvoa **: Taso on liian korkea**, **Taso liian matala** ja **Taso arvoalueella.** Kullekin arvolle määritetään, onko arvo **hyväksytty**, **hylätty** vai **ei mitään.**

**Esimerkki 2:** voit tarkastaa laitteen silmämääräisesti kulumisen ja repeämien arvioimiseksi.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Ylläpidon tarkistuslistat** \> **Ylläpidon tarkistuslistan muuttujat**.
2. Valitse **Uusi**.
3. Kirjoita **Muuttuja**-kenttään kunnossapitotarkistuslistan muuttujan tunnus.
4. Anna nimi **Nimi**-kenttään.
5. Lisää muuttujalle rivi valitsemalla **Yleiset**-pikavälilehdessä **Lisää**.

    **Rivinumero**-kenttään syötetään automaattisesti rivin järjestysnumero. Kun olet lisännyt kaikki rivit, voit muuttaa rivinumeroita tarpeen mukaan. Kun valitset rivin ja painat **alanuolta**, sarjan seuraava numero lisätään automaattisesti seuraavalle riville.

6. Syötä arvon kuvaus **Arvo**-kentässä.
7. Valitse **Tulos**-kentästä rivin tulos.

![Ylläpidon tarkistuslistan muuttujasivu](media/04-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-template"></a>Huollon tarkistusluettelon mallin luominen

Kunnossapidon tarkistusluettelomalleja voidaan käyttää yhteisenä tehtäväluettelona, joka työntekijän on suoritettava, jotta työtilaus saadaan valmiiksi oikein. Malleihin viitataan huoltotyön oletustyypin kunnossapidon tarkistusluetteloriveiltä. Malleihin voidaan viitata useissa kunnossapitotöiden tyypin oletusriveiltä. Näin voit helposti käyttää uudelleen joukon yleisiä huollontarkistusluettelon tehtäviä. Esimerkkejä kunnossapidon tarkistusluettelomalleista ovat yleiset turvallisuusohjeet sekä luettelo nimikkeistä ja ehdoista, jotka on tarkistettava tietyssä pumpussa tai vastaavissa kuljetinvyön malleissa.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Ylläpidon tarkistuslistat** \> **Ylläpidon tarkistuslistan mallit**.
2. Valitse **Uusi**.

    Mallin tunnus lisätään automaattisesti **Ylläpidon tarkistuslistan malli** -kenttään.

3. Kirjoita ylläpidon tarkistuslistan mallin nimi **Nimi**-kenttään.
4. Lisää malliin rivi valitsemalla **Ylläpidon tarkistuslistan rivit** -pikavälilehdessä **Lisää**.

    **Rivinumero**-kenttään syötetään automaattisesti rivin järjestysnumero. Kun olet lisännyt kaikki rivit, voit muuttaa rivinumeroita tarpeen mukaan. Kun valitset rivin ja painat **alanuolta**, sarjan seuraava numero lisätään automaattisesti seuraavalle riville.

5. Kirjoita **tyyppi**-kenttään ylläpiton tarkistuslistan rivin tyyppi. Kunkin huollon tarkistusluettelotyyppiin liittyvät kentät näkyvät **Rivin tiedot** -pikavälilehdessä. Käytettävissä ovat seuraavat arvot:

    - **Teksti** – rivillä on teksti, joka kuvaa, mitä tehdä. Käytä tätä huollon tarkistusluettelon tyyppiä, jos työntekijä haluaa tarkistaa jotain, mutta ei odota tiettyä (mitattavaa) tulosta. Kun olet valinnut tämän tyypin, kirjoita nimi tai otsikko **Nimi** -kenttään. Kirjoita **Ohjeet** -kenttään kuvaus siitä, mitä on tehtävä. Jos huollon tarkistusluettelon vaihe on pakollinen, määritä **Pakollinen**-asetukseksi **Kyllä.**
    - **Otsikko** – Riviä käytetään otsikkona, kun ryhmitellään otsikon alla näkyviä kunnossapidon tarkistusluettelon rivejä. Tästä tyypistä on hyötyä, jos sinulla on useita huollon tarkistusluettelon rivejä, jotka voidaan jakaa tiettyihin alueisiin. Otsikkotiedot sisältävät sille työntekijälle yhteenvedon, joka suorittaa huollon tarkistusluettelon, jossa on useita huollon tarkistusluettelorivejä. Kun olet valinnut tämän tyypin, kirjoita kuvaava nimi **Nimi** -kenttään.
    - **Malli** – riviä käytetään viittauksen tekemiseen aiemmin luotuun malliin. Kun olet valinnut tämän tyypin, kirjoita mallin nimi **Nimi** -kenttään. Valitse malli **Malli**-kentässä.
    - **Muuttuja** – rivin avulla määritetään mahdollinen tulos arvoalueella. Lisätietoja huollon tarkistusluettelon muuttujien määrittämisestä on kohdassa [Huollon tarkistusluettelon muuttujan luominen](#create-a-maintenance-checklist-variable). Kun olet valinnut tämän tyypin, kirjoita muuttujaa kuvaava nimi **Nimi** -kenttään. Valitse muuttuja **Muuttuja**-kentästä. Kirjoita **Ohjeet** -kenttään kuvaus siitä, mitä on tehtävä. Jos huollon tarkistusluettelon vaihe on pakollinen, määritä **Pakollinen**-asetukseksi **Kyllä.**
    - **Mittaus** – riviä käytetään tietyn mittauksen tallentamiseen. Voit määrittää mittauksen, joka liittyy ennalta määritettyyn laskuriin. Kun olet valinnut tämän tyypin, kirjoita mallin nimi **Nimi** -kenttään. Jos huollon tarkistusluettelon tämä vaihe on pakollinen, määritä **Pakollinen**-asetukseksi **Kyllä.** Jos haluat käyttää mittausriviä laskurirekisteröintiin, valitse laskuri kentästä **Laskuri**. Liittyvä **Yksikkö**-kenttä päivittyy sitten automaattisesti. Jos olet valinnut laskurin, valitse päivitysmenetelmä **Arvo**-kentästä. Anna **Pienin arvo**- ja **Suurin arvo**-kentissä, sallittu arvoalue. Kirjoita **Ohjeet** -kenttään kuvaus siitä, mitä on tehtävä.

        > [!NOTE]
        > Mitä tahansa **Mittaus**-tyypin riviä, jolla ei ole laskuriasetuksia, käsitellään itsenäisenä mittauksen rekisteröintin', jota ei ole määritetty automaattisesti käyttöomaisuuden hallinnassa. Vastaavasti, jos valittua laskurityyppiä ei ole työtilaukseen liittyvässä käyttöomaisuuskohteessa, kunnossapidon tarkistusluettelon tehtävää käsitellään itsenäisenä mittauksena. Laskurin arvoa voidaan muuttaa useita kertoja. Sitä ei kirjata, ennen kuin [Työtilauksen elinkaaren tila](work-order-lifecycle-states.md) muutetaan tilaksi, jossa **Käsittele ylläpidon tarkistuslista** -asetukseksi on määritetty **Kyllä**.

    **Tiedot**-pikavälilehden **Tarkistukset** -kentässä näkyy mallin tarkistusluettelorivien kokonaismäärä. Tämä määrä sisältää sisäkkäiset rivit kaikissa aiemmin luoduissa malleissa, joihin olet viitannut mallissa.

![Ylläpidon tarkistuslistan mallisivu](media/05-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type"></a>Luo ylläpitotyön tyyppi

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Työt** \> **Ylläpitotyön tyypit**.
2. Valitse **Uusi**.
3. Kirjoita **Ylläpitotyön tyyppi** -kenttään ylläpitotyön tyypin tunnus.
4. Anna nimi **Nimi**-kenttään.

    **Tiedot**-pikavälilehdessä on yleiskuvaus kunnossapitotöiden tyyppien, taitojen, sertifikaattien, seuraavien töiden ja käyttöomaisuustyyppien määristä, jotka on luotu tälle kunnossapitotöiden tyypille. **Asetusrivit**-kentässä näkyy huoltotyön oletustyypin rivien määrä, joka on määritetty tälle kunnossapitotyön tyypille. **Resurssit**-kentässä näkyy niiden aktiivisten käyttökohteiden määrä, jotka käyttävät tällä hetkellä tätä ylläpitotyötä.

5. Valitse **Yleiset**-pikavälilehden **Ylläpitotyön tyyppiluokka** -kentässä ylläpitotyön tyyppiluokka.
6. Määritä **Ylläpidon käyttökatkojen toiminnot** -asetukseksi **Kyllä**, jos kunnossapitotöiden tyyppi edellyttää laitteen huoltopysähdystä, ennen kuin työ voidaan suorittaa.
7. Määritä kunnossapitotyön tyypin kuvaus **Kuvaus**-pikavälilehdessä.
8. Voit lisätä **Ylläpitotyön tyypin variantit** -pikavälilehdessä ylläpitotyön tyypille variantteja.
9. **Vaaditut osaamisalueet**- ja **Vaaditut todistukset** -pikavälilehdissä voit lisätä kunnossapitotyön tyyppiin osaamisalueita ja todistusvaatimuksia.
10. Jos seuraavaksi on suoritettava tietty kunnossapitotyön tyyppi, lisää se **Seuraavat työt** -pikavälilehteen. Voit myös määrittää kunnossapitotyötyypin variantin ja toimialan, jotka liittyvät kunnossapitotyön tyyppiin. Jos seuraava työ on aloitettava tietty päivien määrä ennen tätä kunnossapitotyötyyppiä käyttävän työn aloittamista tai sen jälkeen, määritä päivien määrä **Viive päivinä** -kentässä. Positiiviset luvut kuvaavat päiviä liittyvän työn alkamisen jälkeen, ja negatiiviset luvut edustavat päiviä ennen liittyvän työn ajoitettua alkua. Jos esimerkiksi määrität arvoksi **5**, seuraavan työn alkamispäivä on viisi päivää sen työn alkamisen jälkeen, joka liittyy kunnossapitotyötyyppiin. Jos esimerkiksi määrität arvoksi **-3**, seuraavan työn alkamispäivä on kolme päivää sen työn alkamista ennen, joka liittyy kunnossapitotyötyyppiin.

    > [!NOTE]
    > Jos lisäät useamman kuin yhden kunnossapitotyön tyypin rivin, rivien järjestys ilmaisee, missä järjestyksessä ne on suoritettava. Järjestys alkaa luettelon yläreunasta.

11. **Resurssityypit**-pikavälilehdessä voit lisätä käyttöomaisuustyyppejä ylläpitotyön tyyppiin.

![Ylläpitotyön tyyppisivu](media/06-setup-for-work-orders.png)

## <a name="create-maintenance-job-type-default-lines-and-related-forecasts-maintenance-checklists-tools-description-and-attachments"></a>Luo kunnossapitotöiden tyypin oletusrivit ja niihin liittyvät ennusteet, ylläpidon tarkistus luettelot, työkalut, kuvaus ja liitteet

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Työt** \> **Ylläpitotöiden tyyppien oletukset**.

    –TAI–

    Valitse **Resurssien hallinta** \> **Asetukset** \> **Työt** \> **Ylläpitotyön tyypit**, valitse ylläpitotyön tyyppi ja sitten **Ylläpitotyön tyypin oletukset**.

2. Valitse **Uusi**.
3. Valitse **toiminnallinen sijainti**-, **Resurssityyppi**-, **Valmistaja**-, **Malli**-ja **Resurssi**-kentissä asianmukaiset arvot sen mukaan, miten tarkka kunnossapitotöiden tyypin oletusarvojen on oltava.
4. Valitse **Ylläpitotyön tyyppi** -kentässä ylläpitotyön tyyppi, jos sitä ei ole valittu automaattisesti.
5. Valitse **Ylläpitotyön tyypin variantti**- ja **Toimiala**-kentissä kunnossapitotöiden tyyppivariantti ja kunnossapitotöiden toimiala tarpeen mukaan.
6. Valitse **Ennuste**.
7. **Ylläpitotöiden tyypin oletusennuste** -sivulla voit tehdä ennusteita tunneista, nimikkeistä ja kuluista. Valitse asianmukaisissa välilehdissä **Lisää** ja tee valinnat, joiden avulla voit luoda tarvittavat ylläpitotyön tyypin ennusteet.
8. **Nimike ennuste** -välilehdessä voit valita varastodimensioita, jotka näytetään nimikerivillä. Valitse **Varasto** \> **Dimensiot**, valitse näytettävät dimensiot, määritä **Tallenna asetukset** -asetukseksi **Kyllä** ja valitse sitten **OK**.
9. Valitse **Nimike-ennuste**-välilehden **Nimike, missä käytetty** -kohta saadaksesi yleiskatsauksen siitä, missä resurssien hallinnassa valitulla rivillä olevaa nimikettä käytetään suhteessa resursseihin, ylläpitotyötyypin oletuksiin, varaosiin ja työtilauksiin. 

    **Ylläpitoennusteen summat**-pikavälilehdessä näkyy yhteenveto ennusteiden kokonaissummista. Tässä yhteenvedossa on luotujen tuntien ja ennusterivien kokonaismäärä.

    > [!NOTE]
    > Jos haluat kopioida ennusteasetuksia toisesta kunnossapitotyön tyypistä, valitse **Kopioi ennuste** ja valitse sitten kunnossapitotöiden tyyppi, josta määritykset kopioidaan.

11. Tallenna muutokset valitsemalla **Tallenna**.
12. Voit palata **Ylläpitotöiden tyypin oletukset** -sivulle sulkemalla **Ylläpitotöiden tyypin oletusennuste** -sivun.
13. Valitse **Ylläpidon tarkistuslista**.
14. **Ylläpitotyön tyyppien oletusten tarkistuslista** -sivulla voit lisätä huollon tarkistusluettelorivejä valittuun kunnossapitotyön tyypin oletuksiin. Lisää ylläpidon tarkistuslistan rivi valitsemalla **Ylläpidon tarkistusrivit** -pikavälilehdessä **Uusi**.

    **Rivinumero**- kenttään lisätään automaattisesti rivinumero, joka ilmaisee kunnossapidon tarkistuslistan rivien järjestyksen. Voit muokata rivinumeroita tarpeen mukaan. Kun olet luonut ensimmäisen huollon tarkistusluettelorivin, valitse rivi ja lisää sitten rivi sen alapuolelle painamalla **alanuoli**-näppäintä. Vaihtoehtoisesti voit valita huollon tarkistusluettelorivin ja valita sitten **Uusi**. Tällöin valitun huollon tarkistusluettelorivin yläpuolelle lisätään uusi rivi.

15. Valitse **Tyyppi**-kentässä rivityyppi ja lisää sitten huollon tarkistusluettelotyyppiin liittyvät tiedot. Käytettävissä olevien tyyppien ja liittyvien kenttien kuvaukset ovat kohdassa [Huollon tarkistusluettelon mallin luominen](#create-a-maintenance-checklist-template).

    > [!NOTE]
    > Jos haluat kopioida ylläpidon tarkistuslistan asetuksia toisesta kunnossapitotyön tyypistä, valitse **Kopioi ylläpidon tarkistuslista** ja valitse sitten kunnossapitotöiden tyyppi, josta määritykset kopioidaan.
    >
    > Voit helposti luoda mallin aiemmin luodusta ylläpidon tarkistuslistasta. Tämän jälkeen voit käyttää mallia uudelleen useissa kunnossapitotarkistulistoissa. Uusi malli on tarkka kopio aktiivisesta huollon tarkistuslistasta. Valitse **Luo malli** ja kirjoita mallin nimi. Jos haluat korvata aiemmin luodun huollon tarkistusluettelon yhdellä rivillä, joka viittaa uuteen malliin, aseta **Korvaa**-asetukseksi **Kyllä**. Voit tarkastella mallin sisältöä **Ylläpidon tarkistuslistan mallit** -tietosivulla.

16. Tallenna muutokset valitsemalla **Tallenna**.
17. Palaa **Ylläpitotyön tyyppien oletukset** -sivulle.
18. Valitse **Työkalut**.
19. **Ylläpitotyön tyyppien oletustyökalut** -sivulla voit lisätä työkalut (resurssit), joita käytetään tässä kunnossapitotyön tyypissä. Valitse **Uusi** ja sitten työkalu **Resurssi**-kentässä.

    > [!NOTE]
    > Jos haluat kopioida työkaluasetuksia toisesta kunnossapitotyön tyypistä, valitse **Kopioi työkalut** ja valitse sitten kunnossapitotöiden tyyppi, josta määritykset kopioidaan.

20. Tallenna muutokset valitsemalla **Tallenna**.
21. Palaa **Ylläpitotyön tyyppien oletukset** -sivulle.
22. Valitse **Työn kuvaus**.
23. Valitse **Työn kuvaus** -sivulla **Muokkaa** ja lisää sitten valittuun kunnossapitotyön tyyppiin liittyvä kuvaus, kuten tarvitset.
24. Tallenna kuvaus valitsemalla **Tallenna**.

    Jos lisäät työn kuvauksen tähän, se korvaa kaikki kuvaukset, jotka on määritetty huoltotyötyypille **Ylläpitotyön tyypit** -sivulla. Jos et lisää tässä työkuvausta, käytössä on kaikki kunnossapitotöiden tyypille määritetyt kuvaukset. Kuvaukset siirretään automaattisesti työtilauksiin, joissa käytetään ylläpitotyön tyyppiä tai ylläpitotyön tyypin oletusarvoja.

25. Palaa **Ylläpitotyön tyyppien oletukset** -sivulle.
26. Jos haluat määrittää valitun kunnossapitotyön tyypin liitteet oletusriville, valitse **Liitä asiakirjoja**. Liitteet, jotka on määritetty kunnossapitotyötyypin oletusriville, sisällytetään automaattisesti työtilausriveihin, jotka käyttävät kyseistä kunnossapitotyön tyypin oletusriviä.
27. Valitse **Uusi** ja sitten asiakirjatyyppi.
28. Lataa asiakirja tai tiedosto palvelimeen.
29. Aseta kentät **Liitteet**-sivulla. Liiteasetukset käyttävät normaalia tiedoston määritystoimintoa.
30. Tallenna liite valitsemalla **Tallenna**.

    > [!NOTE]
    > Kunnossapitotöiden oletusrivin liitteet tulostetaan yhdessä työtilausraportin kanssa vain, jos liitteiden tiedostotyypit on valittu **Resurssienhallinnan parametrit** -sivun **Asiakirjatyypit** -välilehdessä (**Resurssien hallinta** \> **Asetukset** \> **Resurssienhallinnan parametrit**). Esimerkkejä liitteistä ovat ohjeet, joissa selitetään, miten tietty työ tai valmiiksi määritetty huollon tarkistusluettelo voidaan suorittaa (jos kunnossapitotöiden tarkistusluettelotoimintoa ei ole käytössä oletusriveille).

    **Ylläpitotyön tyyppien oletukset** -sivulla kullakin rivillä näkyy ennustettujen tuntien määrä ja myös nimikkeille, kuluille, kunnossapitotarkistuslistoille ja työkaluille luotujen rivien määrä. **Resurssit**-kentässä näkyy niiden aktiivisten käyttökohteiden määrä, jotka liittyvät ylläpitotyötyypin oletusriviin.

31. Jos haluat kopioida kunnossapitotyön tyypin oletusarvon toiseen kunnossapitotyön tyyppiin, valitse oletusrivi, johon haluat kopioida toisen asetuksen, valitse **Kopioi asetukset** ja valitse sitten kopioitava ylläpitotyön tyypin oletus.
32. Jos haluat tarkastella käyttöomaisuuksien, ylläpitosuunnitelmien tai kunnossapitokierrosten luetteloita, jotka käyttävät tällä hetkellä ylläpitotyön tyypin oletusriviä, valitse rivi ja valitse sitten **Käyttäjä**.

![Ylläpitotyön tyyppien oletussivu](media/07-setup-for-work-orders.png)

Kun järjestelmä valitsee käytettävissä olevan kunnossapitotyön tyypin oletus arvon, jota käytetään työtilausrivillä, valinta perustuu käyttöomaisuuserään ja siihen liittyviin käyttöomaisuustyypin asetuksiin. Käyttöomaisuuden hallinta käy läpi kaikki kunnossapitotöiden tyypin oletustietueet, jotka liittyvät käyttöomaisuustyyppiin liittyvään ylläpitotyön tyyppiin, jotta mahdollinen vastaavuus voidaan tarkistaa. Se tarkistaa aina kaikkein erikoisimman yhdistelmän ensin. Toisin sanoen, jos haluat löytää tarkimman yhdistelmän, käyttöomaisuuden hallinta tarkistaa ensin, onko **Toimiala**-kentässä mahdollista vastinetta. Jos vastaavuutta ei löydy, se tarkistaa **Ylläpitotyön tyypin variantti** -kentän vastaavuuden. Jos vastaavuutta ei löydy, se etsii vastaavuutta **Ylläpitotyön tyyppi** -kentästä ja niin edelleen (**Toimiala**, sitten **Ylläpitotyön tyypin variantti**, **Ylläpitotyön tyyppi**, sitten **Resurssi**, sitten **Malli**, sitten **Valmistaja** ja sitten **Resurssityyppi**). Jos vastinetta ei löydy, käytetään oletustietuetta, jossa valitaan vain ylläpitotyön tyyppi.

Projektitehtävän tunnus liitetään automaattisesti kaikkiin luotaviin ylläpitotyön tyypin oletusriveihin. Projektitehtävä luodaan ennusteprojektiin, joka on valittu **Ylläpitoennusteen projekti** -kentässä (**Resurssit**-välilehti **Resurssienhallinnan parametrit** -sivulla). Projektitehtävän tarkoitus on hallita työtilauksiin liittyvien tuntien, nimikkeiden ja kulujen ennusteita. Kunnossapitotöiden tyypin ennusteet siirretään automaattisesti työtilausriville, ja ne kopioidaan ennusteprojektista työtilausriville luotuun työtilauksen projektiin. Projektitehtävän tarkoitus on hallita työtilauksiin liittyviä ennusteita.

Voit määrittää erätyön päivittämään kunnossapitotyön tyypin oletusviitteet säännöllisin väliajoin tai voit suorittaa työn manuaalisesti. Voit luoda erätyön tai suorittaa manuaalisen päivityksen valitsemalla **Resurssien hallinta** \> **Kausittainen** \> **Ennalta ehkäisevä ylläpito** \> **Päivitä ylläpitotyön tyypin oletusten viitteet**.

## <a name="overview-of-maintenance-job-types-that-are-related-to-assets"></a>Käyttöomaisuuteen liittyvien kunnossapitotyötyyppien yleiskatsaus

Kun olet luonut tarvittavat ylläpitotyötyypin oletusyhdistelmät, voit käyttää **Kaikki resurssit** -sivua ja tarkastella nykyisen kunnossapitotyön tyypin oletusarvoa, joka liittyy tiettyyn käyttöomaisuuserään. Yhteenvedossa näkyvät kaikki kunnossapitotyön tyypin oletusyhdistelmät, joita voidaan käyttää käyttöomaisuuserän tyypille. Nämä yhdistelmät sisältävät yhdistelmiä, joissa on kunnossapitotöiden tyypin variantteja ja kunnossapitotöiden toimialoja.

1. Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit** tai **Aktiiviset resurssit**.
2. Valitse luettelosta käyttöomaisuuserä, jonka kunnossapitotöiden tyyppiyhdistelmät haluat nähdä.
3. Valitse toimintoruudun **Yleiset**-välilehden **Aiheeseen liittyvät tiedot**-ryhmästä **Ylläpitotyön tyypit**.

    **Resurssien ylläpidon työtyypit** -sivun vasemmassa ruudussa näkyy luettelo kaikista kunnossapitotöiden tyyppiyhdistelmistä, jotka liittyvät valittuun käyttöomaisuuserään.

4. Valitse ylläpitotöiden tyyppien yhdistelmä nähdäksesi liittyvät asetukset ylläpidon tarkistuslistoille, ennusteille ja työkaluille. **Ylläpitotyön tyyppien oletukset** -pikavälilehden **Tiedot**-osassa näkyy valittuun kunnossapitotöiden tyyppiyhdistelmään liittyvien huoltotarkistusluetteloiden, ennustettujen tuntien ja nimikkeiden jne. määrä.
5. Voit tarkastella valitun kunnossapitotyön tyypin tietoja valitsemalla **Ylläpitotyön tyypit**.

![Resurssien ylläpidon työtyyppisivu](media/08-setup-for-work-orders.png)

## <a name="automatic-update-of-maintenance-job-type-forecasts"></a>Kunnossapitotöiden tyypin ennusteiden automaattinen päivitys

Käyttöomaisuuden hallinnassa voit päivittää automaattisesti ylläpitotyön tyypin ennusteiden muutokset, jotka koskevat tuntikustannuksia, nimikekustannuksia ja kuluja, jotka on päivitetty muissa moduuleissa. Näin taataan, että kunnossapitotöiden tyypin ennusteissa käytetään aina uusimpia kustannushintoja.

1. Valitse **Resurssien hallinta** \> **Kausittainen** \> **Ennuste** \> **Päivitä ylläpitotyön tyypin ennuste**.
2. Voit lisätä tiettyjen kunnossapitotöiden tyyppien valintoja tarpeen mukaan käyttämällä **Päivitä ylläpitotyön tyypin ennuste** -valintaikkunan **Sisällytettävät tietueet** -pikavälilehteä. Valitse **Suodatin** ja tee sitten valinnat valitsemalla **Valitse**.
3. **Suorita taustalla** -pikavälilehdessä voit määrittää automaattisen päivityksen erätyönä tarpeen mukaan.
4. Käynnistä ennusteen päivitys valitsemalla **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]