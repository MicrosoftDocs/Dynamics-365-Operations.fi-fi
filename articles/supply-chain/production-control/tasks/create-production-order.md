--- 
title: Luo tuotantotilaus
description: "Tässä menettelyssä näytetään, miten tuotantotilaus luodaan."
author: johanhoffmann
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 4db56f76c7f8ce0cccf85ab04024d9a1e88a8822
ms.contentlocale: fi-fi
ms.lasthandoff: 02/06/2018

---
# <a name="create-a-production-order"></a>Luo tuotantotilaus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä näytetään, miten tuotantotilaus luodaan. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä on ensimmäinen seitsemästä tuotantotilauksen elinkaaresta kertovasta menettelystä.


## <a name="create-a-production-order"></a>Luo tuotantotilaus
1. Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.
2. Valitse Uusi tuotantotilaus.
3. Kirjoita Nimiketunnus-kenttään D0001.
4. Syötä päivämäärä Toimitus-kenttään.
    * Toimituspäivämäärä osoittaa, milloin tuotantotilauksen tulee päättyä, jotta se voidaan toimittaa ajoissa. Tätä päivämäärää käytetään ajoitusprosessissa. Voit ajoittaa tilauksen esimerkiksi toimituspäivämäärästä taaksepäin.  
5. Valitse määräksi 20.
    * Huomautus: Tuoterakenteen numero -kentässä näkyy automaattisesti nykyisen nimikkeen jonkin aktiivisen tuoterakenteen numero. Voit vaihtaa tuotantotilauksen tuoterakenteen valitsemalla aktiivisen tuoterakenteen hyväksyttyjen tuoterakenneversioiden luettelosta.    Reitin numero -kentässä näkyy automaattisesti nykyisen nimikkeen jonkin aktiivisen reitin numero. Voit vaihtaa tuotantotilauksen reitin valitsemalla aktiivisen reitin hyväksyttyjen reittiversioiden luettelosta.  
6. Valitse Luo.

## <a name="validate-the-production-order"></a>Tuotantotilaus tarkistaminen
1. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse juuri luomasi tuotantotilauksen numeron linkkiä. Tilauksen tietojen sivu avautuu.  
2. Valitse Muokkaa.
3. Syötä päivämäärä Toimitus-kenttään.
    * Voit muuttaa esimerkiksi tuotantotilauksen toimituspäivämäärää.  
4. Valitse Tallenna.
5. Sulje sivu.

## <a name="update-the-bom"></a>Tuoterakenteen päivittäminen
1. Valitse toimintoruudussa Tuotantotilaus.
2. Valitse Tuoterakenne.
    * Avaa tuoterakenteen sivu, kun haluat tarkistaa oletustiedoista tuotantotilauksen luomisen yhteydessä kopioidut tuotantorakennetiedot. Tässä menettelyssä tuoterakenteen määrä on päivitettävä.  
3. Valitse Muokkaa.
4. Kirjoita numero Määrä-kenttään.
    * Tuoterakennerivin määrän muuttaminen vaikuttaa tuotantotilauksen materiaalikulutuksen kustannusarvioon.  
5. Valitse Tallenna.
6. Sulje sivu.

## <a name="update-the-production-route"></a>Tuotantoreitin päivittäminen
1. Valitse toimintoruudussa Tuotantotilaus.
2. Valitse Reitti.
    * Avaa reitin sivu, kun haluat tarkistaa oletustiedoista tilauksen luomisen yhteydessä kopioidut tuotantoreitin tiedot. Tässä menettelyssä päivitetään yhden tuotantoreitin työvaiheen määrä.  
3. Etsi haluamasi tietue luettelosta ja valitse se.
4. Valitse Muokkaa.
5. Syötä Prosessimäärä-kenttään numero.
    * Prosessin muuttaminen vaikuttaa reitin arvioituun kulutukseen ja tuotantotilauksen kustannuksiin.  
6. Valitse Tallenna.
7. Sulje sivu.


