---
title: Täydennysstrategiat
description: Tässä aiheessa on tietoja täydennysstrategioista ja täydennystavan valitsemisesta käyttämällä Täydennysstrategia-kenttää aallon kysynnän täydennysmallin riveillä.
author: mirzaab
manager: tfehr
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 9c23126c6ab15a1924b34f98d33a0661011ba8bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996095"
---
# <a name="replenishment-strategies"></a>Täydennysstrategiat

[!include [banner](../includes/banner.md)]

**Täydennysmallit**-sivulla määritetään malleja, kuten aallon kysynnän täydennysmallit rivit, joilla voidaan valita täydennystapa. Kullakin rivillä on nyt **Täydennysstrategia**-kenttä.

*Aallon kysynnän määrä* on oletusstrategia. Tätä täydennysstrategiaa käytettiin ennen **Täydennysstrategia**-kentän käyttöönottoa. Se etsii täydennettäviä sijaintia täydennyksen sijaintidirektiivien avulla. Sen jälkeen se täyttää kyseisiä sijaintia, kunnes kysyntä on katettu.

*Sijainnin enimmäiskapasiteetti* -strategia sisältää muutamia uusia toimintoja. *Aallon kysynnän määrä* -strategian tavoin tämä strategia etsii täydennettävät sijainnit täydennyksen sijaintidirektiivien avulla ja täyttää sitten kyseiset sijainnin, kunnes kysyntä on katettu: Se eroaa kuitenkin *Aallon kysynnän määrä* -strategista siten, että kaikki täydennettävät sijainnit täydennetään niiden enimmäiskapasiteettiin saakka, ja tämä kapasiteetti määrittyy sijainnin varastointirajojen mukaan. *Sijainnin enimmäiskapasiteetti* -strategia yrittää luoda työn tuomalla täytettäviin sijainteihin pyydetyn määrän lisäksi myös jonkin verran ylimääräistä. Joissakin tapauksissa tämä ei kuitenkaan onnistu. Esimerkiksi bulkkisijaintien varasto ei ehkä riitä kattamaan ylimääräistä osuutta. Näissä tapauksissa järjestelmä havaitsee virheen ja yrittää palautua.

Esimerkiksi kausihuippu voi olla tilanne, jossa *Sijainnin enimmäiskapasiteetti* -strategia on *Aallon kysynnän määrä* -strategiaa parempi vaihtoehto. Kausihuipun aikana joitakin nimikkeitä voidaan myydä erittäin paljon. Niinpä kyseisiä keräilysijainteja kannattaakin ehkä täydentää ennakoivasti mahdollisimman paljon, mikä vähentää täydennykseen luotujen työtunnusten määrää.

> [!IMPORTANT]
> *Sijainnin enimmäiskapasiteetti* -strategian tehokas käyttö edellyttää, että liittyvien sijaintien varastointirajat määritetään uudelleen. Muussa tapauksessa strategia toimii samoin kuin *Aallon kysynnän määrä* -strategia.

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a>Varastointirajoihin perustuvan enimmäismäärään täydentävän toiminnon ottaminen käyttöön

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat tarkistaa tämän toiminnon tilan ja ottaa sen tarvittaessa käyttöön käyttämällä [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Enimmäistäydennys varastointirajojen perusteella*

## <a name="set-up-replenishment-strategies"></a>Täydennysstrategioiden määrittäminen

Voit käyttää malleja valitsemalla **Varastonhallinta \> Asetukset \> Täydennys \> Täydennysmallit** Valitse tai luo aallon kysynnän täydennysmalli **Yleiskuvaus**-osa kohdassa, jossa **Täydennystyyppi**-kentän asetuksena on *Aallon kysyntä*. Määritä sitten täydennysmallin rivit **Täydennysmallin tiedot** -osassa. Valitse kunkin rivin **Täydennysstrategia**-kentässä käytettävä strategia.

![Täydennysmallit-sivu](media/ReplenTempWaveDmdMaxLocCap.png "Täydennysmallit-sivu")

Jos **Täydennysstrategia**-sarake ei ole näkyvissä **Täydennysmallin tiedot** -osan ruudukossa, varmista, että toiminto on otettu käyttöön ja että valitun täydennysmallin täydennystyyppi on *Aallon kysyntä*.

> [!NOTE]
> *Aallon kysynnän määrä* on oletusstrategia. Niinpä vain ne täydennysmallin rivit on päivitettävä, joissa haluat käyttää *Sijainnin enimmäiskapasiteetti* -strategiaa.

## <a name="example-scenarios"></a>Esimerkkiskenaariot

### <a name="example-1"></a>Esimerkki 1

Tässä esimerkissä on vain yksi täydennysmalli, jossa on vain yksi täydennysmallin rivi.

Nimikkeelle A0001 luodaan 130 kappaleen (kpl) myyntitilaus. Varasto määritetään ennen tilauksen vapauttamista varastoon seuraavasti:

- Käytössä on vain yksi bulkkivarasto, jonka käytettävissä oleva varasto on 500 kpl.
- Keräilysijainteja on kolme, joista kunkin varastorajoitus on 100 kpl. (Muista, että *Sijainnin enimmäiskapasiteetti* -strategia edellyttää varastorajoituksia.)
- Täydennyksen asetussijainnit ovat samoja kuin myynnin keräilysijainnit.
- Täydennysyksikkö on laatikko (1 laatikko = 20 kpl).

Tilaushetkellä myynnin keräilysijainneissa on seuraavat käytettävissä olevat varastot:

- **Keräily-001:** 20 kpl (1 laatikko)
- **Keräily-002:** 0 kpl
- **Keräily-003:** 0 kpl

Täydennysstrategiana on aluksi *Aallon kysynnän määrä*.

Kun myyntitilaus vapautetaan varastoon ja aallon käsittely suorittaa aallon, tuloksena on seuraava täydennystyö:

- **Täydennystyö 1:** kerää 4 laatikkoa bulkkisijainnista ja aseta ne sijaintiin keräily-001.
- **Täydennystyö 2:** kerää 2 laatikkoa bulkkisijainnista ja aseta ne sijaintiin keräily-002.

Tuloksena on kaksi täydennystyötunnusta, koska täydennettäviä sijainteja on kaksi eikä moni-asettamisia tueta.

Jos täydennysstrategiaksi määritetään kuitenkin *Sijainnin enimmäiskapasiteetti*, tuloksena on seuraava täydennystyö:

- **Täydennystyö 1:** kerää 4 laatikkoa bulkkisijainnista ja aseta ne sijaintiin keräily-001.
- **Täydennystyö 2:** kerää 5 laatikkoa bulkkisijainnista ja aseta ne sijaintiin keräily-002.

[![Esimerkki 1](media/ReplenTemp_example_1.png "Esimerkki 1")](media/ReplenTemp_example_1_large.png)

### <a name="example-2"></a>Esimerkki 2

Tämä esimerkki osoittaa, mitä tapahtuu, kun bulkkisijainnin varasto ei riitä ylimäärän kattamiseen. Käytössä on sama skenaario kuin esimerkissä 1, mutta bulkkisijainnissa on nimikettä 160 kpl (8 laatikkoa).

*Aallon kysynnän määrä* -strategia luo saman työn kuin esimerkissä 1.

Koska *Sijainnin enimmäiskapasiteetti* -strategia kuitenkin yrittää luoda työtunnukset samoin kuin esimerkissä 1, se voi epäonnistua. Tässä vaiheessa järjestelmä yrittää palautua.

Täydennyksen keräilyn sijaintidirektiivien **Salli jakaminen** -asetuksen perusteella tulosvaihtoehtoja on kaksi:

- Jos **Salli jakaminen** -asetuksena on *Kyllä*, seuraava täydennystyö luodaan:

    - **Täydennystyö 1:** kerää 4 laatikkoa bulkkisijainnista ja aseta ne sijaintiin keräily-001.
    - **Täydennystyö 2:** kerää 4 laatikkoa bulkkisijainnista ja aseta ne sijaintiin keräily-002.

- Jos **Salli jakaminen** -asetuksena on *Ei*, seuraava täydennystyö luodaan:

    - **Täydennystyö 1:** kerää 4 laatikkoa bulkkisijainnista ja aseta ne sijaintiin keräily-001.
    - **Täydennystyö 2:** kerää 2 laatikkoa bulkkisijainnista ja aseta ne sijaintiin keräily-002.

Tulosten ero perustuu työtä luotaessa käytettävissä oleviin tietoihin. Kun täydennyksen keräilyn sijaintidirektiivien **Salli jakaminen** -asetuksena on *Kyllä*, löydetyt 160 kpl ovat tiedossa. Niinpä työ luodaan kyseiselle määrälle. Jos **Salli jakaminen** -asetuksena on kuitenkin *Ei*, tiedossa ei ole, että nimikkeitä on 160 kpl. Koska täydennettävä ylimäärä on 3 laatikkoa, kyseinen ylimäärä jätetään pois ja alkuperäistä määrää yritetään uudelleen.

[![Esimerkki 2](media/ReplenTemp_example_2.png "Esimerkki 2")](media/ReplenTemp_example_2_large.png)

Tämän vuoksi täydennyssijainteihin saadaan enimmäismäärä, kun täydennyksen keräilyn sijaintidirektiivien **Salli jakaminen** -asetukseksi on määritetty *Kyllä*.
