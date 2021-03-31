---
title: Vähittäismyyntikanavien määrittäminen ja ylläpitäminen
description: Tämä ohjeaihe sisältää perinteisten myymälöiden määrittämisprosessin yleiskatsauksen. Perinteisiä myymälöitä kutsutaan Dynamics 365 Commercessa myymälöiksi. Artikkeli sisältää myös tietoja tehtävistä, jotka on suoritettava ennen myymälän määrittämistä ja sen jälkeen.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a2ac4a4a42447e4ee57d24548a79f43b88b03927
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213695"
---
# <a name="define-and-maintain-retail-channels"></a>Vähittäismyyntikanavien määrittäminen ja ylläpitäminen

[!include [banner](includes/banner.md)]

Tämä ohjeaihe sisältää perinteisten myymälöiden määrittämisprosessin yleiskatsauksen. Perinteisiä myymälöitä kutsutaan Dynamics 365 Commercessa myymälöiksi. Artikkeli sisältää myös tietoja tehtävistä, jotka on suoritettava ennen myymälän määrittämistä ja sen jälkeen.

Commerce tukee useita kanavia, kuten verkkokauppoja, verkkokauppoja, puhelinkeskuksia ja perinteisiä myymälöitä. Perinteistä myymälöitä kutsutaan myymäläksi. Jokaisella myymälällä voi olla omat maksuvälineet, hintaryhmät, kassakoneet, tulo- ja kulutilit sekä oma henkilökunta. Myymälälle on määritettävä kaikki edellä luetellut elementit, ennen kuin se voidaan luoda. Kun olet luonut myymälän, voit määrittää myymälän tuotteet. Voit myös liittää työntekijät, kassapäätteet ja asiakkaat myymälään. Lopuksi lisäät uuden myymälän organisaatiohierarkiaan.

## <a name="setting-up-stores"></a>Myymälöiden määritys

Ennen kuin voit määrittää myymälän Commercessä, sinun on suoritettava edellytettäviä toimia. Tämän jälkeen voit luoda myymälän ja lisätä tiedot.

### <a name="prerequisites"></a>Edellytykset

Ennen kuin voit määrittää myymälän, sinun on suoritettava seuraavat tehtävät:

1. Määritä organisaatiorakenne ja organisaation hierarkiat vähittäismyynnin valikoimille, täydennyksille ja raportointia varten.
2. Määritä varasto, joka vastaa myymälää.
3. Myymälöiden numerosarjojen, myymälän laskelmien ja laskelman tositteiden määrittäminen.
4. Commercen parametrien määritys.
5. Määritä maksutapoja, jotka myymälä hyväksyy.
6. Voit myös määrittää maksupalvelut prosessoimaan luottokorttitapahtumat myyntipisteen kassakoneissa.
7. Määritä arvonlisäveroryhmät.
8. Määritä tuotteet. Tässä tehtävässä määritetään myös tuotteiden hierarkiat, tuotevariantit ja tuotevalikoimat.
9. Voit määrittää tuotehintaryhmät.
10. Tuotehinnoittelujen määritys. Tässä tehtävässä määritetään myös hinnanoikaisut, alennukset ja alennuskaudet.
11. Henkilökunnan jäsenten määrittäminen.

    > [!NOTE]
    > Määritä myös työntekijöille soveltuvat käyttöoikeudet, joiden avulla he voivat kirjautua POS-järjestelmään ja suorittaa siellä tehtäviä.

12. Määritä myymälään liitettävät POS-profiilit. Tämä tehtävä sisältää useita tehtäviä, kuten kassapäätteiden määrittäminen, offline profiilien määrittäminen ja kuitin muodon ja profiilien määrittäminen.

Tarkastele kaikkia näihin edellytyksiin sisältyviä tehtäviä ja suorita vain tehtävät, jotka koskevat sinua.

### <a name="set-up-a-store"></a>Määritä myymälä

Kun olet tehnyt edellytettävät toimet, määritä myymälän tiedot suorittamalla nämä tehtävät:

1. Luo myymälä.
2. Määritä arvonlisäveroryhmä myymälälle.
3. Määritä hyväksytyt maksutavat myymälälle.
4. Lisää tietoja niiden tuotteiden tuotekuvauksiin, joita myyt myymälöissäsi. Voit esimerkiksi lisätä rtf-tekstiä ja kuvia. Nämä tuotetiedot näkyvät useissa paikoissa, kuten myyntipisteen kassakoneella ja tulostetuissa etiketeissä.
5. Lisää myymälä oletusorganisaatiohierarkiaan, joka on liitetty **vähittäismyyntivalikoimaan**, **vähittäismyynnin täydennykseen** tai **vähittäismyynnin raportointiin**.

### <a name="after-you-set-up-a-store"></a>Kun olet määrittänyt myymälän

Kun olet lisännyt myymälälle tietoja, päätä tehtävät lähettämällä uudet vähittäismyymälän tiedot POS-järjestelmään:

1. Määritä myymälän myyntipisteiden kassakoneet.
2. Määritä tuotevalikoimia myymälään.
3. Käsittele valikoimat luodaksesi luettelo tuotteista, jotka sisältyvät valikoimaan ja tehdäksesi tuotteet saataviksi myymälässä.
4. Lähetä POS-sovelluksen kassakoneille tietoja, kuten numerosarjat, laitteistojen laiteprofiilit ja myyntipisteen näytön asettelut.
5. Julkaise myymälän tietojen lähettämiseksi POS-järjestelmään.
6. Suorita työt lähettääksesi myymälän tiedot POS-järjestelmään.

## <a name="organization-hierarchies"></a>Organisaatiohierarkiat

Commerce käyttää organisaatiohierarkioita määrittämään vähittäismyynnin kanavien rakenteen. Organisaatiohierarkiat edustavat liiketoimintasi muodostavien organisaatioiden välisiä suhteita. Kun perustat kauppoja, voit lisätä ne organisaatiohierarkiaan. Myymälät jakavat sitten valikoimissa, täydennyksissä ja raportoinnissa käytettävät tiedot.

> [!NOTE]
> Jos haluat käyttää Commercen myyntitoimintoa, **usean toimitusasiakkaan** konfigurointiavain on otettava käyttöön. Tämä konfigurointiavain löytyy **Kaupan määritysavaimet** -osiosta kohdasta **Järjestelmänhallinta**\> **Asetukset** \> **Käyttöoikeuden määritys**. Tämä vaaditaan, koska myyntitilauksen rivitasolla määritettyjen toimitusosoitteiden perusteella suoritetaan erilaisia tarkistuksia.



[!INCLUDE[footer-include](../includes/footer-banner.md)]