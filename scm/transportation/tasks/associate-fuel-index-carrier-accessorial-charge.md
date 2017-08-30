--- 
title: "Liitä polttoaineindeksi rahdinkuljettajaan lisämaksuna"
description: "Tässä ohjauksessa kerrotaan, miten polttoaineen lisämaksun määritys, rahdinkuljettajan lisämaksu, lisämaksun päätiedot luodaan ja liitetään rahdinkuljettajan polttoaineindeksiin rahdinkuljettajan kanssa."
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
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: d3ab4ee1a8ab74226b784496b56f26d26ed04ed8
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a>Liitä polttoaineindeksi rahdinkuljettajaan lisämaksuna

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä ohjauksessa kerrotaan, miten polttoaineen lisämaksun määritys, rahdinkuljettajan lisämaksu, lisämaksun päätiedot luodaan ja liitetään rahdinkuljettajan polttoaineindeksiin rahdinkuljettajan kanssa. Rahdinkuljettajan polttoaineindeksi on määritettävä ennen tämän ohjauksen suorittamista. Sen voi määrittää Määritä rahdinkuljettajan polttoaineindeksi -ohjauksessa. Logistiikkapäällikkö tekee yleensä nämä tehtävät. Tämän menettelyn luomisessa käytetty esittelytietojen yritys on USMF.


## <a name="create-an-accessorial-master"></a>Lisämaksun päätietojen luominen
1. Valitse Kuljetustenhallinta > Asetukset > Luokitus > Lisämaksun päätiedot.
2. Valitse Uusi.
3. Kirjoita arvo Lisämaksun päätiedot -kenttään.
4. Kirjoita arvo Nimi-kenttään.
5. Valitse Tallenna.

## <a name="create-a-carrier-accessorial-charge"></a>Rahdinkuljettajan lisämaksun luominen
1. Valitse Kuljetustenhallinta > Asetukset > Luokitus > Rahdinkuljettajan lisämaksut.
2. Valitse Uusi.
3. Kirjoita Rahdinkuljettajan lisämaksun tunnus -kenttään arvo.
4. Avaa haku valitsemalla Lähetyksen rahdinkuljettaja -kentässä avattavan valikon painike.
5. Etsi haluamasi tietue luettelosta ja valitse se.
    * Tässä esimerkissä valitaan kuorma-autonkuljettaja.  
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Avaa haku valitsemalla Rahdinkuljettajan palvelu -kentässä avattavan valikon painike.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Avaa haku valitsemalla Lisämaksun päätiedot -kentässä avattavan valikon painike.
10. Etsi haluamasi tietue luettelosta ja valitse se.
    * Tässä esimerkissä valitaan juuri luodut lisämaksun päätiedot.  
11. Valitse Tallenna.

## <a name="create-an-accessorial-assignment"></a>Lisämaksun määritysten luominen
1. Valitse Lisämaksun määritykset.
2. Valitse Uusi.
3. Kirjoita arvo Nimi-kenttään.
4. Ota käyttöön Ehdot-osan laajennus.
    * Voit määrittää ehdoissa, että polttoaineen lisämaksua käytetään aina. Tässä esimerkissä voit myös valita, että sitä käytetään vain tietyllä alueella.  
5. Kirjoita arvo Postinumero lähtö -kenttään.
6. Kirjoita arvo Postinumero kohde -kenttään.
7. Ota käyttöön Laskenta-osan laajennus.
    * Laskenta-osassa voit määrittää, miten polttoaineen lisämaksu lasketaan. Laskenta riippuu laskelman perustaksi valitusta lisämaksun yksiköstä.  
8. Valitse Lisämaksun tyyppi -kentässä Polttoaineen lisämaksu.
9. Valitse Lisämaksun yksikkö -kentässä Kilometri.
10. Avaa haku valitsemalla Alue-kentässä avattavan valikon painike.
11. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
12. Valitse Tallenna.

## <a name="update-the-carrier-rating-profile"></a>Rahdinkuljettajan hinnoitteluprofiilin päivittäminen
1. Valitse Kuljetustenhallinta > Asetukset > Rahdinkuljettajat > Lähetyksen rahdinkuljettajat.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Ota Luokituksen profiilit -osan laajennus käyttöön.
4. Valitse Muokkaa.
5. Avaa haku valitsemalla Rahdinkuljettajan polttoaineindeksi -kentässä avattavan valikon painike.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Valitse Tallenna.

