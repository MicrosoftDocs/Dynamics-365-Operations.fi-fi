---
title: "Luvun nimikkeistö"
description: "Tässä aiheessa kuvataan, kuinka voit määrittää luvun nimikkeistö korvaamaan kiinteässä muodossa [tuotteen master - määritys - koon - väri - tyylillä], kohdennettuja muodossa, joka sisältää tuotteen perusmuodon numeroa, aktiivisia tuotedimensiota ja tekstin valinta erottimia. Voit myös luoda nimikkeistön konfiguraatioiden tunnistamiseksi, jotka on luotu poissulkevan tuotekonfiguraattorin avulla. Nämä nimikkeistöt voivat sisältää valitsemiasi määritteitä."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220104
ms.assetid: 31c9efb4-b5f6-4af3-b884-8f1e128469bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 58afcd62e7ef317e624fd26d198c2606bf53e6a5
ms.lasthandoff: 03/31/2017


---

# <a name="product-number-nomenclature"></a>Luvun nimikkeistö

Tässä aiheessa kuvataan, kuinka voit määrittää luvun nimikkeistö korvaamaan kiinteässä muodossa [tuotteen master - määritys - koon - väri - tyylillä], kohdennettuja muodossa, joka sisältää tuotteen perusmuodon numeroa, aktiivisia tuotedimensiota ja tekstin valinta erottimia. Voit myös luoda nimikkeistön konfiguraatioiden tunnistamiseksi, jotka on luotu poissulkevan tuotekonfiguraattorin avulla. Nämä nimikkeistöt voivat sisältää valitsemiasi määritteitä.

Uuden tuotevariantin numeroiden nimikkeistön ansiosta voit sisällyttää segmenttejä tuotevariantin numeroihin. Nämä segmentit voivat sisältää päätuotenumeron, tuotedimensiot, numerosarjat, tekstivakioita ja määritteitä. Kun luot myyntitilauksen tai ostotilauksen, löydät nopeasti tietyt tuotevariantit tämän toiminnon avulla.

## <a name="nomenclature-of-predefined-product-variants"></a>Ennalta määritettyjen tuotevarianttien nimikkeistö
Tuotevariantit luodaan päätuotteelle jollain kolmesta määritysmenetelmästä:

-   Ennalta määritetyt variantit
-   Rajoitukseen perustuva
-   Dimensioon perustuva

Jokaisella tuotevariantilla on numero, ja tuotevariantin numeroiden nimikkeistön ansiosta voit valita segmentit, jotka sisällytetään tuotevariantin numeroihin . Voit valita seuraavat segmentit **Tuotenimikkeistö**-sivulla.

-   Päätuotteen numero
-   Numerosarjan arvo
-   Tekstivakio
-   Tuotedimensiot
    -   Konfiguraatio
    -   Väri
    -   Koko
    -   Tyyli

Kun olet määrittänyt tuotevariantin numeroiden nimikkeistön, se voidaan yhdistää tuotedimensioryhmään. Näin ollen kaikille päätuotteille, jotka viittaavat tähän tuotedimensioryhmään, määritetään tuotevariantin numero nimikkeistön mukaan. On myös mahdollista määrittää tuotevariantin numeroiden nimikkeistö suoraan päätuotteelle, jolloin päätuotteeseen kuuluville tuotevarianteille määritetään tuotevariantin numero nimikkeistön mukaan.

### <a name="example"></a>Esimerkki

T-paitaa (TS1234) valmistetaan 3 eri kokoa (S, M, L) ja 4 eri väriä (punainen, vihreä, sininen, keltainen) sekä 2 mallia (Polo, V), jolloin mahdollisia tuotevariantteja on 24. Tuotevariantin numeron nimikkeistöön luodaan seuraavat segmentit:

1.  Päätuotteen numero
2.  Tekstivakio: '-'
3.  Väri
4.  Tekstivakio: '-'
5.  Koko
6.  Tekstivakio: '-'
7.  Tyyli

Tuotevariantin numero ominaisuuksille punainen, S, poolo on: TS1234-punainen-S-poolo.

## <a name="nomenclature-of-constraintbased-configurations"></a>Nimikkeistön constraintbased kokoonpanoissa.
Poissulkevan kokoonpanoissa kiinteä nimikkeistön voi muodostaa kokoonpano tuote-dimension. Voit valita seuraavat segmentit **Tuotenimikkeistö**-sivulla.

-   Numerosarjan arvo
-   Tekstivakio
-   Määritteen arvo 

Jokaisella tuotemääritysmallin komponentilla voi olla oma konfiguraationimikkeistö. Vain komponenttiin kuuluvia määritteitä saa käyttää. Määritteet alikomponenteista tai käyttäjävaatimuksista eivät ole käytettävissä.

### <a name="example"></a>Esimerkki

Tuotemääritysmallin juurikomponentissa on kaksi määritettä.

-   Materiaali (muovi, puu, teräs)
-   Pituus (10... 100)

Konfiguraationimikkeistö määritetään seuraavien komponenttien avulla:

1.  Määritteen arvo: materiaali
2.  Tekstivakio: 'AAA'
3.  Määritteen arvo: pituus

Puumateriaalin konfiguraatiotunnus, jonka pituus on 78, saa seuraavan konfiguraatiotunnuksen: WoodAAA78.

## <a name="nomenclature-of-dimensionbased-configurations"></a>Nimikkeistön dimensionbased kokoonpanoissa.
Dimensioihin perustuvat konfiguraatiot kiinteä nimikkeistön on rakennettu kokoonpano tuote-dimension. Voit valita seuraavat segmentit **Tuotenimikkeistö**-sivulla.

-   Numerosarjan arvo
-   Tekstivakio
-   Konfiguraatioryhmän nimike

Konfiguraationimikkeistö voidaan määrittää tuoterakenteelle (BOM).

### <a name="example"></a>Esimerkki

Tuoterakenteessa on 4 tuoterakenneriviä, jotka on jaettu 2 konfiguraatioryhmään.

-   Tuoterakennerivi: M0007, vakiokaiutinkaappi
    -   Konfiguraatioryhmä: kaiutinkaappi
-   Tuoterakennerivi: M0008, korkealuokkainen kaiutinkaappi
    -   Konfiguraatioryhmä: kaiutinkaappi
-   Tuoterakennerivi: M0021, kaiuttimen etukangas
    -   Konfiguraatioryhmä: teräsverkkko
-   Tuoterakennerivi: M0022, kaiuttimen teräsverkko
    -   Konfiguraatioryhmä: teräsverkkko

Konfiguraationimikkeistö määritetään seuraavien komponenttien avulla:

1.  Konfiguraatioryhmä: kaiutinkaappi
2.  Tekstivakio: '&'
3.  Konfiguraatioryhmä: teräsverkkko

Etukankaalla varustetun vakiokaiutinkotelon konfiguraatiotunnus on: M0007 ja M0021.

## <a name="nomenclature-of-a-combination-of-product-variants-and-configurations"></a>Tuotevarianttien ja konfiguraatioiden yhdistelmän nimikkeistö
Jos käytät poissulkevaa konfiguraatiota tai dimensioihin perustuvaa konfiguraatiomenetelmää päätuotteen tuotevarianttien suunnitteluun, tuotevarianteille voidaan antaa tuotevarianttinumerot, jotka sisältävät konfigurointidimension nimikkeistön. Jos haluat konfiguroida variantit, noudata seuraavia vaiheita:

1.  Määrittää tuotevariantin numeron nimikkeistö, joka sisältää konfigurointidimension **Tuotenimikkeistö**-sivulla.
2.  Määritä tämä nimikkeistö tuotedimensioryhmälle konfigurointidimension kanssa.
3.  Määritä konfiguraationimikkeistö komponenteille tai tuoterakenteille, jota käytetään tuotevarianttien määrittämistä varten.

### <a name="example-for-constraint-based-configurations"></a>Esimerkki poissulkevasta konfiguraatiosta

Tässä esimerkissä voit käyttää tuotevarianttinumeronimikkeistöä, jossa on seuraavat segmentit:

1.  Päätuotteen numero
2.  Tekstivakio "\_"
3.  Konfiguraatio

Konfiguraationimikkeistö voi koostua seuraavista segmenteistä:

1.  Määritteen arvo: materiaali
2.  Tekstivakio: 'AAA'
3.  Määritteen arvo: pituus

Voit kirjoittaa seuraavat segmenttien arvot:

-   Päätuotteen numero = M0099
-   Materiaali = muovi
-   Pituus = 12

Tulee variant-tuotenumero: M0099\_PlasticAAA12.

### <a name="example-for-dimension-based-configurations"></a>Esimerkki dimensioihin perustuvasta konfiguraatiosta

Tässä esimerkissä voit käyttää tuotevarianttinumeronimikkeistöä, jossa on seuraavat segmentit:

1.  Päätuotteen numero
2.  Tekstivakio '//'
3.  Konfiguraatio

Konfiguraationimikkeistö voi koostua seuraavista segmenteistä:

1.  Konfiguraatioryhmä: kaiutinkaappi
2.  Tekstivakio: '&'
3.  Konfiguraatioryhmä: teräsverkkko

Voit kirjoittaa seuraavat segmenttien arvot:

-   Päätuotteen numero = D0123
-   Kaiutinkaappi = M0008
-   Etusäleikkö = M0022

Tuotevariantin numeroksi tulee: D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Numerointiristiriidat
On mahdollista määrittää tuotevariantin numeronimikkeistö, joka ei tuota yksilöiviä tuotevariantin numeroita. Esimerkiksi näin voi tapahtua, jos yksi aktiivinen tuotedimensio ei sisälly päätuotteen nimikkeistöön, joka käyttää esimääritettyä variantin määritysmenetelmää . Ristiriitoja käsitellään eri tavoin erilaisilla määritysmenetelmillä.

### <a name="predefined-variants"></a>Ennalta määritetyt variantit

Jos yrität luoda manuaalisesti tai automaattisesti tuotevariantteja, joista yksi tai useita päättyy samaan tuotevarianttinumeroon, tapahtuu virhe. Voit välttää tämän käyttämällä kaikkia aktiivisia tuotedimensioita tuotedimensioryhmässä tai liittää numerosarjan sen varmistamiseksi, että tuotevarianttinumerot ovat yksilöiviä.

### <a name="constraint-based-configurations"></a>Poissulkevat konfiguraatiot

Nimikkeistön mukaan järjestelmä yrittää määrittää ei-yksilöivän tuotevarianttinumeron konfiguraatioon. Tässä tapauksessa järjestelmä käyttää numerosarjan konfiguroinnin dimensio on tuotteen varianttinumero sen sijaan. Jos näin tapahtuu, näyttöön tulee varoitus. Tämän voi välttää sisällyttämällä tarpeeksi määritteitä nimikkeistöön, mikä varmistaa yksilöllisyyden ja varmistamalla, että **Käytä uudelleen** -asetus on käytössä komponentille.

### <a name="dimension-based-configurations"></a>Dimensioihin perustuvat konfiguraatiot

Konfigurointiprosessi käsittää vaiheen, jossa järjestelmä ehdottaa konfiguraatioarvoa nimikkeistön mukaan. Et voi muuttaa konfigurointiarvoa manuaalisesti tässä vaiheessa. Kun konfiguraatio tallennetaan, järjestelmä tarkistaa, onko konfiguraation arvo yksilöllinen. Jos näin ei ole, näyttöön tulee virhesanoma. Yksilöllinen konfiguraatioarvo on määritettävä, jotta konfiguraatio tallennetaan.



<a name="see-also"></a>Lisätietoja
--------

[Luo numero nimikkeistö ennalta tuotevarianttien (tehtävän guide)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-predefined-product-variants/)

[Luo numero nimikkeistö määritetty tuotevarianttien (tehtävän guide)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-configured-product-variants/)


