---
title: Kuittimallit ja tulostus
description: "Tässä aiheessa kerrotaan, miten voit lomakeasetteluja muokkaamalla määrittää, miten kuitit, laskut ja muut asiakirjat tulostetaan. Microsoft Dynamicsin 365 - toimintoja varten Retail sisältää lomakkeen asettelun suunnittelutoiminnon, jonka avulla voit helposti luoda ja muokata erilaisia graafisia lomakkeen asetteluja."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fabaacbc7187b38a1745c2139a9eb7760f2be987
ms.lasthandoff: 03/31/2017


---

# <a name="receipt-templates-and-printing"></a>Kuittimallit ja tulostus

Tässä aiheessa kerrotaan, miten voit lomakeasetteluja muokkaamalla määrittää, miten kuitit, laskut ja muut asiakirjat tulostetaan. Microsoft Dynamicsin 365 - toimintoja varten Retail sisältää lomakkeen asettelun suunnittelutoiminnon, jonka avulla voit helposti luoda ja muokata erilaisia graafisia lomakkeen asetteluja.

**Tärkeää:** on määritetty lomakkeen asetteluja ja kuitin kuitit ja muut asiakirjat tulostetaan Retail POS-Sovelluksen Moderni ja Cloud POS-profiilit. Voit sisällyttää useita lomakkeen asetteluja Kuittiprofiilin. Voit sitten määrittää kuittiprofiilin tulostimeen laitteistoprofiilia muuttamalla.

## <a name="set-up-a-receipt-format"></a>Kuittimuodon määrittäminen
1.  Valitse **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**POS**&gt;**kuitin muotoja**.
2.  Valitse **Kuitin muoto** -sivulla **Uusi** luodaksesi uuden lomakeasettelun, tai valitse aiemmin luodun lomakeasettelu.
3.  Kirjoita **Kuitin muoto** -kenttään lomakeasettelun tunnus ja valitse sitten kuitin tyyppi, johon tätä asettelua käytetään. Voit myös kirjoittaa kuitille kuvauksen ja lyhyen nimen **Otsikko**-kenttään.
4.  Valitse **Yleinen**-pikavälilehdessä tulostustoiminnot määrittävä asetus:
    -   **Tulosta aina** – Kuitti tulostetaan aina tarpeen mukaan.
    -   **Älä tulosta** – Kuittia ei tulosteta.
    -   **Kehote käyttäjälle** – Käyttäjää kehotetaan tulostamaan kuitti..
    -   **Tarvittaessa** – Tätä vaihtoehtoa käytetään vain lahjojen kuiteille. Kun tämä vaihtoehto on valittuna, käyttäjä voi tulostaa lahjan kuitin **Muuta**-sivulta, jos lahjan kuitti tarvitaan.

## <a name="design-a-receipt-format"></a>Kuitin muodon suunnittelu
Lomakkeen asettelun suunnittelutoiminnon avulla voit luoda lomakkeen asettelun graafisesti. Sivulla **Kuitin muodon suunnittelutoiminto** on kolme osiota: **Ylätunniste**, **Rivit**, ja **Alatunniste**. Tietyt lomakeasettelut käyttävät elementtejä kaikista kolmesta osasta ja osa vain yhdestä tai kahdesta osasta. Tarkastele jokaisen osan käytettävissä olevia elementtejä napsauttamalla sopivaa painiketta sivun vasemmassa laidassa olevassa siirtymisruudussa.

1.  Valitse **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**POS**&gt;**kuitin muotoja**.
2.  Valitse **Kuitin muoto** -sivulla lomakeasettelu ja napsauta sitten **Suunnittelutoiminto**.
3.  Valitse **Suorita** aloittaaksesi Retail-suunnittelutoiminnon isännän asennus.
4.  Napsauta Internet Explorer -ikkunan alaosassa näkyvällä ilmoitusrivillä **Avaa** aloittaaksesi yhden napsautuksen suunnittelutoiminnon asennuksen. (Ilmoituspalkkia saattaa näkyä eri paikassa muissa selaimissa.) Tilanneilmaisin näyttää asennuksen edistymisen.
5.  Kun asennus on valmis, kirjoita Dynamics-365 toimintojen käyttäjänimi ja salasana ja valitse sitten **kirjautua sisään** suunnittelija käynnistämiseen.
6.  Kun tunnistetietosi on tarkistettu ja suunnittelutoiminta alkaa, voit aloittaa kuitin asettelun suunnittelun tai aiemmin luodun asettelun muokkaamisen.
7.  Jos haluat luoda lomakkeen elementit, valitse **Ylätunniste-**, **Rivit-**, tai **Alatunniste**-osio ja vedä sitten elementti tästä osiosta työtilaan. Useimmat elementit sisältävät muuttujia, jotka täytetään automaattisesti tietokannan tiedoilla. Muut osat, kuten **Teksti**, mahdollistavat mukautetun tekstin kirjoittamisen kuitille. **Huomautus:** Osan oikeassa alakulmassa olevaa lukua muuttamalla voit määrittää, montako riviä kukin osa kattaa. Jos haluat helpottaa osan muokkaamista, lisää sen korkeutta vetämällä alaosassa olevaa koon muuttamiseen tarkoitettua palkkia. Työtilan osan korkeus ei vaikuta todellisen kuitin rivien lukumäärään.
8.  Kun olet vetänyt elementin työtilaan, määritä osan ominaisuudet sivun alaosassa olevassa **Objektin tiedot **-ruudussa. Kirjoita yksi tai useampia seuraavista asetuksista:
    -   **Tasaa** – määritä kentän tasaukseksi **Vasen** tai **Oikea**.
    -   **Täyttömerkki** – Määritä tyhjän tilan merkki. Oletusarvon mukaan tyhjä tila on käytössä, mutta voit syöttää minkä tahansa merkin.
    -   **Etuliite** – Kirjoita arvo, joka näkyy valitun kentän alussa. Tämä asetus koskee vain asettelun **Rivit**-osaa.
    -   **Merkit** – Määrittää kentän merkkien enimmäismäärän, jos elementti sisältää muuttujan. Jos kentän teksti on pidempi kuin määrittämäsi merkkien määrä, teksti katkaistaan kenttään sopivaksi.
    -   **Muuttuja** – Jos elementti sisältää muuttujan eikä sitä voi mukauttaa, tämä valintaruutu valitaan automaattisesti.
    -   **Fonttityyppi** – Fonttityyppi voi olla joko **Normaali** tai **Lihavoitu**. Lihavoitu teksti käyttää kaksi kertaa normaaleja kirjaimia enemmän tilaa. Tämän vuoksi jotkut merkit ovat ehkä katkenneet.
    -   **Poista** – Tätä painiketta napsauttamalla voit poistaa valitun osan lomakkeen asettelusta.

## <a name="assign-receipt-profiles"></a>Määritä kuittiprofiilit
Kuittiprofiilit määritetään suoraan tulostimeen laitteistoprofiilin kautta.

1.  Avaa laitteistoprofiili napsauttamalla **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**POS-profiilit**&gt;**laitteistoprofiilin**.
2.  Valitse tulostin ja määritä sitten **Kuittiprofiili**-kentässä kassapäätteessä käytettävä kuittiprofiili.

**Huomautus:** Jos käytössä on kaksi tulostinta, yhtä tulostinta voidaan käyttää standardimuotoisten 40-sarakkeisten lämpökuittien tulostamiseen. Toista tulostinta käytetään tyypillisesti suuremman tietomäärän vaativien koko sivun kuittityyppien tulostamiseen. Näihin kuittityyppeihin sisältyvät asiakastilausten kuitit ja myyntilaskut.


