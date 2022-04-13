---
title: Toimet
description: Tässä ohjeaiheessa kuvataan käsitteelliset elementit, joita toimi voi sisältää. Se tarjoaa myös esimerkkejä, jotka osoittavat, miten voit käyttää näitä elementtejä organisaatiossasi.
author: twheeloc
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: twheeloc
ms.reviewer: twheeloc
ms.search.scope: Human Resources
ms.custom: 269054
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b0b11458ac5d41d08a245a1f5aa48fb4633ae075
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2022
ms.locfileid: "8534298"
---
# <a name="positions"></a>Toimet


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä ohjeaiheessa kuvataan käsitteelliset elementit, joita toimi voi sisältää. Se tarjoaa myös esimerkkejä, jotka osoittavat, miten voit käyttää näitä elementtejä organisaatiossasi.

Ennen kuin voit luoda toimen, sinulla täytyy olla työ määritettynä. Joillakin toimen tiedoilla, kuten kompensaatioalueella, työntekijän toimeksiannolla, toimen kestolla ja raportointisuhteella, on voimaantulopäivät.

## <a name="general-information"></a>Yleistiedot

Kun luot toimen, sinun on valittava työ. Seuraavat tiedot täytetään automaattisesti valitsemastasi työstä:

- kuvaus
- Titteli
- Kokopäiväinen (FTE)
- Työluokka

Toimen otsikkoa käytetään viittaamaan työntekijän ammattinimikkeeseen. (Työntekijälle mainittua otsikkoa ei käytetä). Siksi toimien otsikot tulisi standardoida mahdollisimman laajasti.

> [!NOTE]
> Työntekijää ei voi kohdistaa toimeen päivämääränä, joka on ennen Käytettävissä toimeksiantoa varten -päivämäärää.
>
> **Henkilöstöhallinnon jaetut parametrit** -sivun **Toimet**-välilehdessä oleva parametri hallitsee työntekijän kohdistustapaa. Valitse jokin seuraavista:
>
> - **Aina** – Voit määrittää työntekijöitä uusiin toimiin toimien luonnin yhteydessä. Kun toimet on luotu, **Käytettävissä toimeksiantoa varten** -päivämäärä ja -aika **Yleinen** -välilehden **Toimi**-sivulla asetetaan automaattisesti sen luontipäivämääräksi ja -ajaksi.
> - **Ei koskaan** – Et voi määrittää työntekijöitä uusiin toimiin toimien luonnin yhteydessä. Jos valitset tämän vaihtoehdon, sinun on avattava kunkin uuden toimen **Toimi**-sivu, kun se tulee saataville. Syötä sitten **Yleiset**-välilehdessä **Käytettävissä toimeksiantoa varten** -päivämäärä mahdollistaaksesi työntekijän kohdistamisen. Jos valitset tämän vaihtoehdon, työntekijän kohdistuspäiväksi määritetään oletusarvoisesti **Ei koskaan**, kun yrität kohdistaa työntekijää.

## <a name="position-duration"></a>Toimen kesto

Jokainen toimi on voimassa tietyn ajan, jota kutsutaan kestoksi. Esimerkiksi kesätöiden kesto voi olla 1. toukokuuta 2021 – 31. elokuuta 2021. Aktivointipäivä on päivämäärä, jolloin toimi on aktiivinen järjestelmässä. Päättymispäivä on päivämäärä, jolloin toimi ei ole enää aktiivinen järjestelmässä.

Huomaa, että Käytettävissä toimeksiantoa varten -päivämäärä tai työntekijän kohdistuspäivä eivät voi olla ennen aktivointipäivää. Toimea ei pidetä aktiivisena ennen kuin aktivointipäivä on saavutettu. Lisäksi työntekijän toimeksianto ei voi ulottua toimen päättymispäivän yli.

## <a name="reports-to-position"></a>Raportoi toimelle

Toimet ovat tärkeitä elementtejä organisaatiohierarkian alemmassa tasossa. **Toimi**-sivulta voit määrittää toimen, jolle toinen toimi raportoi. Kun kohdistat työntekijän toimeen, joka raportoi toiselle toimelle, luot näihin kahteen toimeen kohdistetun työntekijöiden välille raportointisuhteen. Oletetaan esimerkiksi, että toimi 000220 raportoi toimelle 000300. Kim Akers on nimitetty toimeen 000220 ja Sanjay Patel on nimetty toimeen 000300. Kim Akers raportoi siis Sanjay Patelille.

> [!TIP]
> Raportoi toimelle -asetusta käytetään koko järjestelmässä työntekijän esimiehen määrittämiseksi. Edellisessä esimerkissä, jos esimiehen rooli on määritetty järjestelmässä Sanjay Patelille, hän näkee Kim Akersin alaisenaan Esimiehen itsepalvelu -työtilassa. Raportointisuhdetta voidaan käyttää myös, kun luot työnkulun reitityssääntöjä ja tarkistusluettelotehtäviä.

## <a name="relationships"></a>Suhteet

Jos organisaatiosi käyttää matriisihierarkiaa tai muuta mukautettua hierarkiaa, voit määrittää toimihierarkiatyyppejä. Sen jälkeen voit lisätä toimiin raportointisuhteita jokaista määrittämääsi hierarkiatyyppiä varten. Oletetaan esimerkiksi, Lori Penor on Adventure Worksin johtaja, joka on kohdistettu **Pääjohtaja**-toimeen. Lori johtaa pienoissovellusten puhdistamiseen käytettävän tuotteen kehitystyötä. Hän tarvitsee kirjanpitäjän auttamaan raha-asioissa. Tästä syystä hän on rekrytoinut Kim Akersin kirjanpitäjäksi. Kim raportoi suoraan Sanjay Patelille, mutta hän työskentelee myös Lori Penorin kanssa pienoissovelluksen tuotekehityksen taloushallinnossa.

Edellisessä esimerkissä sinun tulisi suorittaa seuraavat tehtävät määrittääksesi työsuhteen Kim Akersin ja Lori Penorin välille:

1. Luo **Pienoissovellus**-niminen mukautettu toimihierarkiatyyppi luodaksesi hierarkian, joka sisältää pienoissovelluksen tuotekehityksestä vastaavat toimet.
2. Määritä **Pääjohtaja**-toimi toimeksi, jolle Kimin toimi raportoi **Pienoissovellus**-hierarkiassa.
3. Toimihierarkian avulla voit tarkastella toimien raportointirakennetta. Jos toimihierarkioita on useita, voit tarkastella kutakin hierarkiatyyppiä toimihierarkiassa. Voit myös hakea toimia toimen tunnuksen tai siihen nimitetyn työntekijän nimen perusteella. Toimihierarkia on organisaatiohierarkia.

## <a name="labor-union"></a>Ammattijärjestö

Voit kirjata, tarvitaanko toimeen ammattiliittosopimus ja mitä ammattiliittoa käytetään. Voit liittää sopimuksen myös yritykseen.

## <a name="financial-dimensions"></a>Taloushallinnon dimensiot

Kun luot taloushallinnon dimension toimelle, sinun on määritettävä yritys. Voit valita kunkin dimension oletusdimensiot erikseen. Vaihtoehtoisesti voit valita jakelumallin, joka täyttää oletusdimensiot automaattisesti. Jakelumalli tarjoaa myös vaihtoehdon, jolla voit allokoida summia useille dimensioarvoille.
