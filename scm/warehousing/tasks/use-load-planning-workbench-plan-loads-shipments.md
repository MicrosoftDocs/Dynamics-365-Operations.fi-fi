--- 
title: "Suunnittele kuormat ja lähetykset kuormasuunnittelun työtilassa"
description: "Tässä menettelyssä kerrotaan, miten myyntitilaukselle luodaan kuorma kuormasuunnittelun työtilan avulla."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
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
ms.openlocfilehash: 982c746de1329be435d9047d4057cba100475b1b
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Suunnittele kuormat ja lähetykset kuormasuunnittelun työtilassa

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kerrotaan, miten myyntitilaukselle luodaan kuorma kuormasuunnittelun työtilan avulla. Ensimmäiseksi luodaan edellytyksenä oleva myyntitilaus. Tämä menettely on osa kuljetuskoordinaattorin päivittäistä työtä. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="create-a-sales-order"></a>Luo myyntitilaus
1. Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.
2. Valitse Uusi.
3. Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.
4. Valitse tili US-004.
5. Valitse OK.
6. Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.
7. Valitse nimike A0001.
    * A0001 on kuljetustenhallinnan käytössä.  
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Kirjoita numero Määrä-kenttään.
10. Syötä Varasto-kenttään 24.
    * Valitse tässä esimerkissä varasto 24. Kuljetuksenhallinta ja varastonhallinnan lisätoiminnot ovat tässä varastossa käytössä.  
11. Valitse Tallenna.
12. Sulje sivu.

## <a name="create-a-new-load"></a>Uuden kuorman luominen
1. Valitse Kuljetustenhallinta > Suunnittelu > Kuormasuunnittelun työtila.
2. Valitse Myyntirivit-välilehti.
    * Muodostetaan nyt juuri luodulle myyntitilaukselle kuorma. Kuormat voidaan muodostaa tarjonnan ja kysynnän perusteella ostotilauksista, siirtotilauksista ja myyntitilauksista.  
3. Valitse toimintoruudussa Tarjonta ja kysyntä.
4. Valitse Uuteen kuormaan.
5. Avaa haku valitsemalla Kuorman mallitunnus -kentässä avattavan valikon painike.
    * Kuormamalli määrittää koko kuorman painon ja tilavuuden enimmäismitat. Kuormamalli voi esittää esimerkiksi kontin tai kuorma-auton koon.  
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Valitse OK.

## <a name="rate-and-route-the-load"></a>Kuorman hinnan ja reitityksen määrittäminen
1. Valitse Hinnoittelu ja reititys.
2. Valitse Hinnan ja reitin työtila.
3. Valitse Hintavertailu.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Valitse Liitä.
6. Sulje sivu.
7. Sulje sivu.


