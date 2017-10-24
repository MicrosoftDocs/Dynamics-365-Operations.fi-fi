--- 
title: "Rahdinkuljettajan polttoaineindeksin määrittäminen"
description: "Tässä ohjauksessa kerrotaan, miten polttoaineindeksialue, polttoaineindeksi ja rahdinkuljettajan polttoaineindeksi luodaan."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 81f3244ff42cf13cd93ac10656c47f8a9204ef99
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-carrier-fuel-index"></a>Rahdinkuljettajan polttoaineindeksin määrittäminen

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


