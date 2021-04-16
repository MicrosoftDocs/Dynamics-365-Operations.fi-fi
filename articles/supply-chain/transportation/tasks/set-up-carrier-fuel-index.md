---
title: Rahdinkuljettajan polttoaineindeksin määrittäminen
description: Tässä ohjauksessa kerrotaan, miten polttoaineindeksialue, polttoaineindeksi ja rahdinkuljettajan polttoaineindeksi luodaan.
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFuelIndexRegion,TMSCarrierFuelIndexTable,TMSFuelIndex
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1e972f2ba8211c47b11a4b83dac9ff60f813b1a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837577"
---
# <a name="set-up-a-carrier-fuel-index"></a>Rahdinkuljettajan polttoaineindeksin määrittäminen

[!include [banner](../../includes/banner.md)]

Tässä ohjauksessa kerrotaan, miten polttoaineindeksialue, polttoaineindeksi ja rahdinkuljettajan polttoaineindeksi luodaan. Polttoaineindeksialue määrittää, millä alueella polttoaineindeksiä käytetään. Polttoaineindeksi määrittää polttoaineen hinnan tiettynä aikana. Jotta muutos huomioidaan polttoainehinnoissa ajan kuluessa, voit liittää useat polttoaineindeksit rahdinkuljettajaan.  Yleensä kuljetuskoordinaattori tekee nämä tehtävät. Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.


## <a name="create-a-fuel-index-region"></a>Polttoaineindeksialueen luominen
1. Valitse Kuljetustenhallinta > Asetukset > Polttoaineindeksit > Polttoaineindeksialueet.
    * Ensin luodaan erilaisia toiminta-alueita ja lasketaan polttoaineen lisämaksut.  
2. Valitse Uusi.
3. Syötä Alue-kenttään arvo.
4. Kirjoita arvo Nimi-kenttään.
5. Valitse Tallenna.

## <a name="create-a-fuel-index"></a>Luo polttoaineindeksi
1. Valitse Kuljetustenhallinta > Asetukset > Polttoaineindeksit > Polttoaineindeksit.
    * Määritetyille alueille on syötettävä nykyiset polttoainemaksut.  
2. Valitse Uusi.
3. Avaa haku valitsemalla Alue-kentässä avattavan valikon painike.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Syötä Litrahinta-kenttään numero.
6. Syötä Voimaantulon aloituspäivä ja -aika -kenttään päivämäärä ja aika.
7. Valitse Tallenna.

## <a name="create-a-carrier-fuel-index"></a>Rahdinkuljettajan polttoaineindeksin luominen
1. Valitse Kuljetustenhallinta > Asetukset > Polttoaineindeksit > Rahdinkuljettajan polttoaineindeksit.
2. Valitse Uusi.
3. Kirjoita Rahdinkuljettajan polttoaineindeksi -kenttään arvo.
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse Uusi.
6. Syötä Voimaantulon aloituspäivä ja -aika -kenttään päivämäärä ja aika.
7. Syötä Litrahinta alkaen -kenttään numero.
    * Tässä esimerkissä Litrahinta alkaen -kenttään syötetään arvo 1,95.  
8. Litrahinta enintään -kenttään numero.
    * Tässä esimerkissä Litrahinta enintään -kenttään syötetään arvo 2.  
9. Syötä Prosentti-kenttään numero.
    * Tässä esimerkissä prosentiksi syötetään 3.  
10. Avaa haku valitsemalla Valuutta-kentässä avattavan valikon painike.
11. Etsi haluamasi tietue luettelosta ja valitse se.
12. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
13. Valitse Tallenna.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]