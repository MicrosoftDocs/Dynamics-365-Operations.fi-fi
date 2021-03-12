---
title: Määritä ja suunnittele vastaanottoluetteloiden muodot
description: Tässä aiheessa kerrotaan, miten voit lomakeasetteluja muokkaamalla määrittää, miten kuitit, laskut ja muut asiakirjat tulostetaan. Dynamics 365 Commerce sisältää lomakkeen asettelun suunnittelutoiminnon, jolla voit helposti luoda ja muokata erilaisia lomakkeen asetteluja.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFormLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a66590f18df04d2be0500b7fb1ab183cf64718e8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979750"
---
# <a name="set-up-and-design-receipt-formats"></a>Määritä ja suunnittele vastaanottoluetteloiden muodot

[!include [banner](includes/banner.md)]

Tässä aiheessa kerrotaan, miten voit lomakeasetteluja muokkaamalla määrittää, miten kuitit, laskut ja muut asiakirjat tulostetaan. Dynamics 365 Commerce sisältää lomakkeen asettelun suunnittelutoiminnon, jolla voit helposti luoda ja muokata erilaisia lomakkeen asetteluja.

> [!IMPORTANT]
> Sinun on määritettävä lomakkeiden asettelut ja kuittiprofiilit kuittien ja muiden asiakirjojen tulostamiseksi Retail Modern POS:ssa ja Cloud POS:ssa. Voit sisällyttää kuittiprofiiliin useita lomakeasetteluita. Voit sitten määrittää kuittiprofiilin tulostimeen laitteistoprofiilia muuttamalla.

## <a name="set-up-a-receipt-format"></a>Kuittimuodon määrittäminen

1. Valitse **Retail ja Commerce** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Myyntipiste** &gt; **Kuitin muodot**.
2. Valitse **Kuitin muoto** -sivulla **Uusi** luodaksesi uuden lomakeasettelun, tai valitse aiemmin luodun lomakeasettelu.
3. Kirjoita **Kuitin muoto** -kenttään lomakeasettelun tunnus ja valitse sitten kuitin tyyppi, johon tätä asettelua käytetään. Voit myös kirjoittaa kuitille kuvauksen ja lyhyen nimen **Otsikko**-kenttään.
4. Valitse **Yleinen**-pikavälilehdessä tulostustoiminnot määrittävä asetus:

    - **Tulosta aina** – Kuitti tulostetaan aina tarpeen mukaan.
    - **Älä tulosta** – Kuittia ei tulosteta.
    - **Kehote käyttäjälle** – Käyttäjää kehotetaan tulostamaan kuitti..
    - **Tarvittaessa** – Tätä vaihtoehtoa käytetään vain lahjojen kuiteille. Kun tämä vaihtoehto on valittuna, käyttäjä voi tulostaa lahjan kuitin **Muuta**-sivulta, jos lahjan kuitti tarvitaan.

## <a name="print-images"></a>Kuvien tulostaminen

Kuittien suunnittelussa on **Logo**-muuttuja, jonka avulla kuittiin tulostettavat kuvat voidaan määrittää. **Logo**-muuttujaa käyttäen kuitteihin lisättyjen kuvien on mustavalkoisia bittikartan (.bmp) tiedostotyyppejä. Jos kuittien suunnittelussa on määritetty .bmp-kuva, mutta se ei tulostu tulostimelle lähetettäessä, tiedoston koko voi olla liian suuri tai kuvan kuvapistedimensiot eivät ole yhteensopivia tulostimen kanssa. Jos näin tapahtuu, kokeile pienentää kuvatiedoston tarkkuutta.   

## <a name="design-a-receipt-format"></a>Kuitin muodon suunnittelu

Lomakkeen asettelun suunnittelutoiminnon avulla voit luoda lomakkeen asettelun graafisesti. Sivulla **Kuitin muodon suunnittelutoiminto** on kolme osiota: **Ylätunniste**, **Rivit**, ja **Alatunniste**. Tietyt lomakeasettelut käyttävät elementtejä kaikista kolmesta osasta ja osa vain yhdestä tai kahdesta osasta. Tarkastele jokaisen osan käytettävissä olevia elementtejä napsauttamalla sopivaa painiketta sivun vasemmassa laidassa olevassa siirtymisruudussa.

1. Valitse **Retail ja Commerce** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Myyntipiste** &gt; **Kuitin muodot**.
2. Valitse **Kuitin muoto** -sivulla lomakeasettelu ja napsauta sitten **Suunnittelutoiminto**.
3. Valitse **Suorita** aloittaaksesi Commerce-suunnittelutoiminnon isännän asennus.
4. Napsauta Internet Explorer -ikkunan alaosassa näkyvällä ilmoitusrivillä **Avaa** aloittaaksesi yhden napsautuksen suunnittelutoiminnon asennuksen. (Ilmoitusrivi saattaa näkyä eri kohdassa muissa selaimissa.) Edistymisen ilmaisin näyttää asennusprosessin edistymisen tilanteen.
5. Kun asennus on valmis, anna Commerce-käyttäjänimesi ja salasanasi ja käynnistä suunnittelutoiminto valitsemalla **Kirjaudu sisään**.
6. Kun tunnistetietosi on tarkistettu ja suunnittelutoiminta alkaa, voit aloittaa kuitin asettelun suunnittelun tai aiemmin luodun asettelun muokkaamisen.
7. Jos haluat luoda lomakkeen elementit, valitse **Ylätunniste-**, **Rivit-**, tai **Alatunniste**-osio ja vedä sitten elementti tästä osiosta työtilaan. Useimmat elementit sisältävät muuttujia, jotka täytetään automaattisesti tietokannan tiedoilla. Muut osat, kuten **Teksti**, mahdollistavat mukautetun tekstin kirjoittamisen kuitille.

    > [!NOTE]
    > Osan oikeassa alakulmassa olevaa lukua muuttamalla voit määrittää, montako riviä kukin osa kattaa. Jos haluat helpottaa osan muokkaamista, lisää sen korkeutta vetämällä alaosassa olevaa koon muuttamiseen tarkoitettua palkkia. Työtilan osan korkeus ei vaikuta todellisen kuitin rivien lukumäärään.

8. Kun olet vetänyt elementin työtilaan, määritä osan ominaisuudet sivun alaosassa olevassa **Objektin tiedot**-ruudussa. Kirjoita yksi tai useampia seuraavista asetuksista:

    - **Tasaa** – määritä kentän tasaukseksi **Vasen** tai **Oikea**.
    - **Täyttömerkki** – Määritä tyhjän tilan merkki. Oletusarvon mukaan tyhjä tila on käytössä, mutta voit syöttää minkä tahansa merkin.
    - **Etuliite** – Kirjoita arvo, joka näkyy valitun kentän alussa. Tämä asetus koskee vain asettelun **Rivit**-osaa.
    - **Merkit** – Määrittää kentän merkkien enimmäismäärän, jos elementti sisältää muuttujan. Jos kentän teksti on pidempi kuin määrittämäsi merkkien määrä, teksti katkaistaan kenttään sopivaksi.
    - **Muuttuja** – Jos elementti sisältää muuttujan eikä sitä voi mukauttaa, tämä valintaruutu valitaan automaattisesti.
    - **Fonttityyppi** – Fonttityyppi voi olla joko **Tavallinen** tai **Lihavoitu**. Lihavoitu teksti käyttää kaksi kertaa tavallisia kirjaimia enemmän tilaa. Tämän vuoksi jotkut merkit ovat ehkä katkenneet.
    - **Fontin koko** – Fontin koko voi olla joko **Tavallinen** tai **Suuri**. Suuret kirjaimet ovat kaksi kertaa korkeampia kuin tavalliset kirjaimet. Suurien kirjaimien käyttö voikin saa aikaan sen, että kuitissa on päällekkäistä tekstiä.
    - **Poista** – Tätä painiketta napsauttamalla voit poistaa valitun osan lomakkeen asettelusta.

## <a name="assign-receipt-profiles"></a>Määritä kuittiprofiilit

Kuittiprofiilit määritetään suoraan tulostimeen laitteistoprofiilin kautta.

1. Avaa laitteistoprofiili valitsemalla **Retail ja Commerce** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Myyntipisteen profiilit** &gt; **Laiteprofiili**.
2. Valitse tulostin ja määritä sitten **Kuittiprofiili**-kentässä kassapäätteessä käytettävä kuittiprofiili.

> [!NOTE]
> Jos käytössä on kaksi tulostinta, yhtä tulostinta voidaan käyttää standardimuotoisten 40-sarakkeisten lämpökuittien tulostamiseen. Toista tulostinta käytetään tyypillisesti suuremman tietomäärän vaativien koko sivun kuittityyppien tulostamiseen. Näihin kuittityyppeihin sisältyvät asiakastilausten kuitit ja myyntilaskut.
