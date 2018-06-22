---
title: "Lisää sijainnin ja osapuolen suhteen tyypit"
description: "Tässä ohjeaiheessa kerrotaan, miten voit lisätä uuden sijainnin ja osapuolen suhteen tyypin."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8435389a523d8393e9d4daa0cb1244203c0dbb12
ms.openlocfilehash: bd8c5a18d69e1952d32675d759b8b2a997844822
ms.contentlocale: fi-fi
ms.lasthandoff: 05/21/2018

---

# <a name="add-new-location-roles-and-party-relationship-types"></a>Lisää uudet sijaintiroolit ja osapuolen suhteen tyypit 

## <a name="add-new-location-roles"></a>Uusien sijaintiroolien lisääminen

On kaksi tapaa lisätä uusia sijaintirooleja osoitteelle ja yhteystiedoille:

-  Lisää ne **Osoitteen ja yhteystietojen tarkoitus** -sivulla. Uusi rooli tallennetaan **LogisticsLocationRole**-tauluun tyyppinä 0, mikä ilmaisee, että rooli ei ole järjestelmärooli, joka on määritetty **LogisticsLocationRoleType**-luettelossa ja sen laajennuksissa. Käyttäjä voi käyttää tätä roolia luodessaan osoitteen tai yhteyshenkilön tiedot.

    ![Osoitteen ja yhteystietojen tarkoitus](media/Address-Contact.PNG)

-  Lisää se **LogisticsLocationRoleType**-valintalistan laajennukseen, minkä jälkeen se täyttää taulut tietokannan synkronoinnin prosessin kautta.

    1.  Luo laajennus **LogisticsLocationRoleType**-valintalistalle ja lisää uusi rooli laajennukseen. 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. Luo uuden roolin uusi resurssitiedosto ja määritä sitten arvot sen ominaisuuksille.
     
     ![Uusi resurssitiedosto](media/Resource.PNG)
        
    3.  Luo tietojen täyttöluokka ja anna käsittelijämetodi uuden roolin täyttämiseen. 

        ![Tietojen täyttö](media/Dirdata.PNG)

    4.  Voit testata uuden sijaintiroolin täyttöä luomalla runnable-luokan ja kutsumalla DirDataPopulation::insertLogisticsLocationRoles()-metodia Main()-metodissa. Kun tämä prosessi on valmis, sinun pitäisi nähdä, että uusi rooli täytetään **LogisticsLocationRole**-tauluun määritteellä type \> 0. Uusi rooli tulee näkyviin **Osoitteen ja yhteystietojen tarkoitus** -sivulle.

        ![Lisää uusi sijainti](media/InsertNewLocation.PNG)

## <a name="add-new-party-relationship-types"></a>Lisää uusia osapuolen suhteen tyyppejä 

Voit lisätä uusia suhteen tyyppejä kahdella tavalla:

-   Lisää se **Suhdetyypit**-sivulla. Uusi suhde tallennetaan **DirRelationshipTypeTable**-tauluun määritteelllä systemtype = 0.

    ![Suhdetyypit](media/Relationship.PNG)

-  Lisää se **DirSystemRelationshipType**-valintalistan laajennukseen, minkä jälkeen se täyttää taulut tietokannan synkronoinnin prosessin kautta.

    1.  Luo laajennus **DirSystemRelationshipType**-valintalistalle ja lisää uusi suhdetyyppi.

    2. Luo alustustoiminto tälle uudelle tyypille. Löydät useita esimerkkejä ydinkoodissa, esimerkiksim kohdassa **DirRelationshipTypeChildInitialize**. Tämä on alustajatoimintoluokka osapuolen suhteen tyypille Child (alataso). Voit aloittaa oman alustimen kirjoittamisen kopioimalla ja liittämällä tämän koodin ja päivittämällä korostetut alueet.
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  Voit testata uuden suhdetyypin täyttöä luomalla runnable-luokan ja kutsumalla DirDataPopulation::insertDirRelationshipTypes()-metodia Main()-metodissa. Näkyviin tulee uusi suhteen laji **DirRelationshipTypeTable**-taulussa ja uusi suhdetyyppi on käytettävissä **Suhdetyypit**-sivulla.

        ![Runnable-luokka](media/Runnable.PNG)

