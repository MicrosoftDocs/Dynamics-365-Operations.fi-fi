---
title: Tuotevariantin numeroiden ja nimien nimikkeistö
description: Tässä artikkelissa kuvataan, miten tuotenumeroiden nimikkeistö määritetään korvaamaan kiinteän muodon [päätuotteen numero - konfiguraatio - koko - väri - malli].
author: t-benebo
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 8b437279c275244e96692c1a629e891973d30d48
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850609"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a>Tuotevariantin numeroiden ja nimien nimikkeistö

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, miten tuotenumeroiden nimikkeistö määritetään korvaamaan kiinteän muodon [päätuotteen numero - konfiguraatio - koko - väri - malli]. Uusi nimikkeistö sisältää kohdennetun muodon, joka sisältää päätuotteen numeron, aktiiviset tuotedimensiot ja haluamasi tekstierottimet. Myös tuotenimille voi luoda nimikkeistön. Voit myös luoda nimikkeistön konfiguraatioiden tunnistamiseksi, jotka on luotu poissulkevan tuotekonfiguraattorin avulla. Nämä nimikkeistöt voivat sisältää valitsemiasi määritteitä.

Tuotevariantin numeroiden ja nimien uusien nimikkeistöjen avulla voi sisällyttää segmenttejä tuotevarianttien tunnuksiin. Nämä segmentit voivat sisältää päätuotenumeron ja nimen, tuotedimensioiden tunnukset ja nimet, numerosarjat, tekstivakioita ja määritteitä. Kun luot myyntitilauksen tai ostotilauksen, löydät nopeasti tietyt tuotevariantit tämän toiminnon avulla. Sekä tuotevariantin numeroille että nimille voi luoda nimikkeistöjä **Tuotenimikkeistö**-sivulla. Avaa tämä sivu valitsemalla **Tuotetietojen hallinta** &gt; **Asetukset**.

## <a name="nomenclature-of-predefined-product-variants"></a>Ennalta määritettyjen tuotevarianttien nimikkeistö
Tuotevariantit luodaan päätuotteelle jollain kolmesta määritysmenetelmästä:

-   Ennalta määritetyt variantit
-   Rajoitukseen perustuva
-   Dimensioon perustuva

Jokaisella tuotevariantilla on numero ja nimi, ja tuotevariantin numeroiden nimikkeistöjen avulla voi valita segmentit, jotka sisällytetään tuotevariantin numeroihin tai nimiin. **Tuotenimikkeistö**-sivulla voi seuraavat segmentit:

-   Päätuotteen numero
-   Päätuotteen nimi
-   Numerosarjan arvo
-   Tekstivakio
-   Tuotedimensiot
    -   Konfiguraation tunnus tai nimi
    -   Värin tunnus tai nimi
    -   Koon tunnus tai nimi
    -   Tyylin tunnus tai nimi

Kun olet määrittänyt tuotevariantin numeron nimikkeistön, voit yhdistää sen tuotedimensioryhmään. Tämän jälkeen kaikki tähän tuotedimensioryhmään viittaavat päätuotteet määritetään tuotevariantin numeroille nimikkeistön mukaan. Tuotevariantin nimien nimikkeistöjä ei kuitenkaan voi yhdistää tuotedimensioryhmiin. Voit myös yhdistää tuotevariantin tunnuksen nimikkeistön suoraan päätuotteeseen. Tässä tapauksessa päätuotteeseen kuuluvat tuotevariantit yhdistetään tuotevariantin numeroihin ja nimiin nimikkeistöjen mukaan.

### <a name="example"></a>Esimerkki

T-paitaa (TS1234) valmistetaan kolme eri kokoa (S, M, L), neljä eri väriä (punainen, vihreä, sininen, keltainen) ja kaksi mallia (poolo, V). Mahdollisia tuotevariantteja on siis 24 (= 3 × 4 × 2). Voit luoda tuotevariantin numeron nimikkeistön, jolla on seuraavat segmentit:

1.  Päätuotteen numero
2.  Tekstivakio: -
3.  Väri
4.  Tekstivakio: -
5.  Koko
6.  Tekstivakio: -
7.  Tyyli

Tässä tapauksessa tuotevariantin numero ominaisuuksille punainen, S, poolo, T-paita TS1234-punainen-S-poolo.

## <a name="nomenclature-of-constraint-based-configurations"></a>Poissulkeva konfiguraationimikkeistö
Poissulkeville konfiguraatioille voi luoda konfiguraation tuotedimension kohdistetun nimikkeistön. **Tuotenimikkeistö**-sivulla voi seuraavat segmentit:

-   Numerosarjan arvo
-   Tekstivakio
-   Määritteen arvo

Jokaisella tuotemääritysmallin komponentilla voi olla oma konfiguraationimikkeistö. Vain komponenttiin kuuluvia määritteitä saa käyttää. Alikomponenttien tai käyttäjävaatimuksien määritteitä ei voi käyttää.

### <a name="example"></a>Esimerkki

Tuotemääritysmallin juurikomponentissa on seuraavat kaksi määritettä:

-   Materiaali (muovi, puu, teräs)
-   Pituus (10... 100)

Voit luoda konfiguraation nimikkeistön, jolla on seuraavat segmentit:

1.  Määritteen arvo: materiaali
2.  Tekstivakio: AAA
3.  Määritteen arvo: pituus

Tässä tapauksessa puumateriaalin konfiguraatiotunnus, jonka pituus on, on WoodAAA78.

## <a name="nomenclature-of-dimension-based-configurations"></a>Dimensioihin perustuva konfiguraationimikkeistö
Dimensioihin perustuville konfiguraatioille voi luoda konfiguraation tuotedimension kohdistetun nimikkeistön. **Tuotenimikkeistö**-sivulla voi seuraavat segmentit:

-   Numerosarjan arvo
-   Tekstivakio
-   Konfiguraatioryhmän nimike

Konfiguraationimikkeistö voidaan määrittää tuoterakenteelle.

### <a name="example"></a>Esimerkki

Tuoterakenne sisältää neljä tuoterakenteen riviä, jotka on jaettu kahteen konfiguraatioryhmään:

-   Tuoterakennerivi: M0007, vakiokaiutinkaappi
    -   Konfiguraatioryhmä: kaiutinkaappi
-   Tuoterakennerivi: M0008, korkealuokkainen kaiutinkaappi
    -   Konfiguraatioryhmä: kaiutinkaappi
-   Tuoterakennerivi: M0021, kaiuttimen etukangas
    -   Konfiguraatioryhmä: teräsverkkko
-   Tuoterakennerivi: M0022, kaiuttimen teräsverkko
    -   Konfiguraatioryhmä: teräsverkkko

Voit luoda konfiguraation nimikkeistön, jolla on seuraavat segmentit:

1.  Konfiguraatioryhmä: kaiutinkaappi
2.  Tekstivakio: &
3.  Konfiguraatioryhmä: teräsverkkko

Tässä tapauksessa etukankaalla varustetun vakiokaiutinkotelon konfiguraatiotunnus on M0007&M0021.

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a>Tuotevarianttien ja konfiguraatioiden yhdistelmän nimikkeistö
Jos käytät poissulkevaa tai dimensioihin perustuvaa määritysmenetelmää päätuotteen tuotevarianttien määritykseen, tuotevarianttien numerot voivat sisältää konfigurointidimension nimikkeistön. Jos haluat konfiguroida variantit, noudata seuraavia vaiheita.

1.  Määritä **Tuotenimikkeistö**-sivulla tuotevariantin numeron nimikkeistö, joka sisältää konfigurointidimension.
2.  Määritä nimikkeistö tuotedimensioryhmälle, jolla on konfigurointidimensio.
3.  Määritä konfiguraationimikkeistö komponenteille tai tuoterakenteille, jota käytetään tuotevarianttien konfiguroimisessa.

Myös tuotevariantin nimille voi luoda nimikkeistön. Tuotevariantin nimet voidaan konfiguroida niin, että ne sisältävät konfiguraation tunnuksen tai nimen.

### <a name="example-for-constraint-based-configurations"></a>Esimerkki poissulkevasta konfiguraatiosta

Tässä esimerkissä voit käyttää tuotevariantin numeron nimikkeistöä, jossa on seuraavat segmentit:

1.  Päätuotteen numero
2.  Tekstivakio \_
3.  Konfiguraatio

Konfiguraationimikkeistö sisältää seuraavat segmentit:

1.  Määritteen arvo: materiaali
2.  Tekstivakio: AAA
3.  Määritteen arvo: pituus

Syötä segmenteille seuraavat arvot:

-   Päätuotteen numero = **M0099**
-   Materiaali = **muovi**
-   Pituus = **12**

Tässä tapauksessa tuotevariantin numero on M0099\_PlasticAAA12.

### <a name="example-for-dimension-based-configurations"></a>Esimerkki dimensioihin perustuvasta konfiguraatiosta

Tässä esimerkissä voit käyttää tuotevariantin numeron nimikkeistöä, jossa on seuraavat segmentit:

1.  Päätuotteen numero
2.  Tekstivakio //
3.  Konfiguraatio

Konfiguraationimikkeistö sisältää seuraavat segmentit:

1.  Konfiguraatioryhmä: kaiutinkaappi
2.  Tekstivakio: &
3.  Konfiguraatioryhmä: teräsverkkko

Syötä segmenteille seuraavat arvot:

-   Päätuotteen numero = **D0123**
-   Kaiutinkaappi = **M0008**
-   Etusäleikkö = **M0022**

Tässä tapauksessa tuotevariantin numero on D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Numerointiristiriidat
Joissakin tapauksissa tuotevariantin numeron määritetty nimikkeistö ei tuota yksilöiviä tuotevariantin numeroita. Esimerkiksi tuotevariantin numerot eivät ole yksilöiviä, jos yksi aktiivinen tuotedimensio ei sisälly päätuotteen nimikkeistöön, joka käyttää esimääritettyä variantin määritysmenetelmää. Ristiriitatilanteiden käsittelytapa vaihtelee määritysmenetelmän mukaan.

### <a name="predefined-variants"></a>Ennalta määritetyt variantit

Jos yrität luoda manuaalisesti tai automaattisesti tuotevariantteja, joista vähintään yksi päättyy samaan tuotevariantin numeroon, tapahtuu virhe. Voit välttää tämän käyttämällä tuotedimensioryhmässä kaikkia aktiivisia tuotedimensioita. Vaihtoehtoisesti voit ottaa mukaan numerosarjat, joiden avulla varmistetaan, että tuotevariantin numerot ovat yksilöiviä.

### <a name="constraint-based-configurations"></a>Poissulkevat konfiguraatiot

Nimikkeistön mukaan järjestelmä yrittää määrittää ei-yksilöivän tuotevariantin numeron konfiguraatioon. Tällöin järjestelmä käyttää sen sijaan konfigurointidimension numerosarjaa tuotevariantin numerona, ja näyttöön tulee varoitus. Voit välttää tämän, kun nimikkeistössä on riittävästi määritteitä. Tällöin yksilöivien tuotevariantin numeroiden varmistaminen on helpompaa. Varmista myös, että komponentin **Käytä uudelleen** -vaihtoehto on käytössä.

### <a name="dimension-based-configurations"></a>Dimensioihin perustuvat konfiguraatiot

Konfigurointiprosessin yhden vaiheen aikana järjestelmä ehdottaa konfiguraatioarvoa nimikkeistön mukaan. Et voi muuttaa konfigurointiarvoa manuaalisesti tässä vaiheessa. Kun konfiguraatio tallennetaan, järjestelmä tarkistaa, onko konfiguraation arvo yksilöllinen. Jos syötetty arvo ei ole yksilöivä, näyttöön tulee virhesanoma. Voit tallentaa konfiguraation syöttämällä yksilöivän konfiguraatioarvon.

## <a name="additional-resources"></a>Lisäresurssit

[Luo tuotenumeroiden nimikkeistö esimääritetyille tuotevarianteille](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[Tuotenumeroiden nimikkeistön luominen konfiguroiduille tuotevarianteille](tasks/create-product-number-nomenclature-product-variants_2016_11.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]