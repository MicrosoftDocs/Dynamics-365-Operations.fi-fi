---
title: Liitä polttoaineindeksi rahdinkuljettajaan lisämaksuna
description: Tässä ohjauksessa kerrotaan, miten polttoaineen lisämaksun määritys, rahdinkuljettajan lisämaksu, lisämaksun päätiedot luodaan ja liitetään rahdinkuljettajan polttoaineindeksiin rahdinkuljettajan kanssa.
author: Weijiesa
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2df77fe94156e2b60b77fa1c995ea10eab048a0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670549"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a>Liitä polttoaineindeksi rahdinkuljettajaan lisämaksuna

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]