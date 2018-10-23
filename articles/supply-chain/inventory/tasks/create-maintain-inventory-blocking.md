--- 
title: "Luo ja ylläpidä varastoesto"
description: "Tässä menettelyssä kerrotaan, miten fyysisen käytettävissä olevan varaston varaaminen estetään muiden lähtevien asiakirjojen tai varastoeston avulla."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 09789dc0b89f8bd36cca9b3e5be366bf17246243
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="create-and-maintain-an-inventory-blocking"></a>Luo ja ylläpidä varastoesto

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kerrotaan, miten fyysisen käytettävissä olevan varaston varaaminen estetään muiden lähtevien asiakirjojen tai varastoeston avulla. Voit suorittaa menettelyn esittelytietojen USMF-yrityksen avulla näkyvillä olevilla esimerkkiarvoilla. Aloita tämä menettely vasta, kun käytettävissä on fyysistä käytettävissä olevaa varastoa omaava nimike.


## <a name="create-an-inventory-blocking"></a>Varastoeston luominen
1. Valitse Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > Varastoesto.
2. Valitse Uusi.
3. Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.
4. Valitse luettelosta nimike. 
    * Määritä estettävä nimiketunnus, jolla on fyysistä käytettävissä olevaa varastoa. Jos käytössä on USMF, voit valita nimikkeen M9201.  
5. Kirjoita numero Määrä-kenttään.
    * Jos käytössä on nimike M9201, määritä arvo, joka on pienempi kuin 200.  
6. Ota käyttöön Varastodimensiot-osan laajennus.
7. Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.
8. Etsi haluamasi tietue luettelosta ja valitse se.
    * Jos käytössä on nimike M9201, voit valita varaston 51.  
9. Valitse Tallenna.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Varastoeston ehtojen päivittäminen
1. Kirjoita numero Määrä-kenttään.
    * Päivitä Varastomäärä-kenttä vastaamaan estettävää määrää.  
2. Kirjoita päivämäärä Odotettu päivämäärä -kenttään.
    * Haluat ehkä määrittää, milloin estetyn varaston odotetaan olevan varattavissa. Voit määrittää tätä varten odotetun päivämäärän. Jos varastoestolle on valittu Odotetut vastaanotot -asetus, kuten oletusarvoisesti on, voit luoda eston manuaalisesti. Tämä päivä näkyy odotetun tapahtuman kohdalla.  
3. Valitse Tallenna.

## <a name="remove-the-inventory-blocking"></a>Varastoeston poistaminen
1. Valitse Poista.
2. Valitse Kyllä.
3. Sulje sivu.


