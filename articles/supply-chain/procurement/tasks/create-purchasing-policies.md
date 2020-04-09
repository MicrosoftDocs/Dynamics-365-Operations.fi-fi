---
title: Luo ostokäytännöt
description: Tässä aiheessa kuvataan, miten luot ostokäytäntöjä, jotka vastaavat ostojen liiketoimintaprosessejasi.
author: mkirknel
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8416f9a869b9144a63a6fb08c667cc32dec9854
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149708"
---
# <a name="create-purchasing-policies"></a>Luo ostokäytännöt

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten luot ostokäytäntöjä, jotka vastaavat ostojen liiketoimintaprosessejasi. Ennen kuin voit luoda ostokäytäntöjä, sinun täytyy määrittää ostokäytäntöparametrit. Voit luoda, muokata ja keskeyttää ostokäytännön, mutta et voi poistaa ostokäytäntöä. Yleensä ostopäällikkö tekee tämän tehtävän. Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.


## <a name="set-up-policy-parameters"></a>Aseta käytäntöparametri
1. Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Asetukset > Käytännöt > Ostokäytännöt**.
2. Valitse toimintoruudussa **Parametrit**.
- Käytännön ohitussäännöt koskevat eri tasoja organisaatiossasi. Näkyvissä olevat organisaatioyksiköt määräytyvät organisaatiohierarkian mukaan ja mille hierarkian tasoille on määritetty tarkoitukseksi hankinnan sisäinen tarkistus. Organisaatiossa voi olla yrityksiä, kustannuspaikkoja, alueita ja osastoja, mutta voi olla, että vain joillain näistä on hierarkian tarkoituksena hankinnan sisäinen tarkastus. Oletuksena käytettävä organisaation tyyppi on Yritys.  
3. Napsauta **Käytäntösäännön tyyppiparametrit** -välilehteä.
4. Valitse puurakenteessa **Ostokäytäntö > Ostoehdotuksen hallintasääntö**.
- Voit määrittää käytännön ratkaisun käsittelyjärjestyksen käytännön tasolla. Kuitenkin tiettyjen käytäntötyyppien käsittelyjärjestyksen voi ohittaa yksittäisissä käytäntösääntötyypeissä. Voit esimerkiksi määrittää ostokäytäntöjen ensisijaisuuden tässä järjestyksessä: kustannuskeskus, osasto, yritys. Voit haluta luettelon käytäntösäännön ensisijaisuusjärjestyksen olevan tässä järjestyksessä: osasto, kustannuspaikka, yritys. Voit muuttaa luettelon käytäntösäännön käsittelyjärjestystä. Kun työntekijä luo varasto-ottoehdotuksen, näytettävä luettelo määräytyy järjestyksessä niiden käytäntöjen perusteella, jotka on liitetty työntekijän osastoon, sitten kustannuspaikkaan ja viimeiseksi yritykseen.  
- Jos luettelossa on useampi organisaatiotaso, voit määrittää järjestyssäännön ylä-/alanuolilla Ostoehdotuksen ohjaussäännölle.  
5. Sulje sivu.

## <a name="create-a-new-policy"></a>Luo uusi käytäntö
1. Valitse **Uusi**.
2. Kirjoita arvo **Nimi**-kenttään.
3. Kirjoita **Kuvaus**-kenttään arvo.
- Yksi ostokäytäntö voi koskea vain yhtä organisaatiohierarkiaa. Yksi hierarkia voi olla esimerkiksi "Maantieteellinen" ja toinen "Osasto", ja molemmilla voi olla erillinen ostokäytäntö.  
- Valitse organisaatio, jota käytäntö koskee.  
4. Valitse haluttu organisaatio napsauttamalla nuolta.
- Voit toistaa prosessin lisätäksesi useita organisaatioita.  

## <a name="add-a-policy-rule"></a>Lisää käytäntösääntö
1. Valitse **Käytäntösäännön tyyppi** -luettelossa **Ehdotuksen tarkoitussääntö**.
- Luot säännön, joka määrittää ostoehdotuksen oletustarkoitukseksi kulutuksen, mutta sallii myös täydennyksen valinnan sen sijaan.  
2. Valitse **Luo käytäntösääntö**.
3. Valitse **Salli manuaalinen ohitus** -kentässä **Kyllä**.
4. Valitse **Sulje**.
- Voit nyt määrittää muut ostokäytännön käytäntösäännöt. Huomaa, että käytäntösääntötyyppi ei voi sisältää päällekkäisiä sääntöjä, jotka ovat aktiivisia samaan aikaan yhdessä hankintasäännössä.  

