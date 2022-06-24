---
title: Luo ostokäytännöt
description: Tässä artikkelissa kuvataan, miten luot ostokäytäntöjä, jotka vastaavat ostojen liiketoimintaprosessejasi.
author: GalynaFedorova
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 011705723466d746fa5b23c5499d03a548f133f1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878842"
---
# <a name="create-purchasing-policies"></a>Luo ostokäytännöt

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan, miten luot ostokäytäntöjä, jotka vastaavat ostojen liiketoimintaprosessejasi. Ennen kuin voit luoda ostokäytäntöjä, sinun täytyy määrittää ostokäytäntöparametrit. Voit luoda, muokata ja keskeyttää ostokäytännön, mutta et voi poistaa ostokäytäntöä. Yleensä ostopäällikkö tekee tämän tehtävän. Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]