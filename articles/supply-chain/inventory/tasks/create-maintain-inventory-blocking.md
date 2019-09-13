---
title: Luo ja ylläpidä varastoesto
description: Tässä menettelyssä kerrotaan, miten fyysisen käytettävissä olevan varaston varaaminen estetään muiden lähtevien asiakirjojen tai varastoeston avulla.
author: perlynne
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2485eaf31226b11106895074ae0ad95e561777b
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916596"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Luo ja ylläpidä varastoesto

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kerrotaan, miten fyysisen käytettävissä olevan varaston varaaminen estetään muiden lähtevien asiakirjojen tai varastoeston avulla. Voit suorittaa menettelyn esittelytietojen USMF-yrityksen avulla näkyvillä olevilla esimerkkiarvoilla. Aloita tämä menettely vasta, kun käytettävissä on fyysistä käytettävissä olevaa varastoa omaava nimike.


## <a name="create-an-inventory-blocking"></a>Varastoeston luominen
1. Valitse **siirtymisruudussa** **Moduulit > Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > Varastoesto**.
2. Valitse **Uusi**.
3. Avaa haku valitsemalla **Nimiketunnus**-kentässä avattavan valikon painike.
4. Valitse luettelosta nimike. Määritä estettävä nimiketunnus, jolla on fyysistä käytettävissä olevaa varastoa. Jos käytössä on USMF, voit valita nimikkeen M9201.  
5. Anna **Määrä**-kentässä numero. Jos käytössä on nimike M9201, määritä arvo, joka on pienempi kuin 200.
6. Laajenna **Varaston dimensiot** -pikavälilehti.
7. Avaa haku valitsemalla **Varasto**-kentässä avattavan valikon painike.
8. Etsi haluamasi tietue luettelosta ja valitse se. Jos käytössä on nimike M9201, voit valita varaston 51.  
9. Valitse **Tallenna**.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Varastoeston ehtojen päivittäminen
1. Kirjoita numero **Yleiset** -pikavälilehden **Määrä**-kenttään. Päivitä Varastomäärä-kenttä vastaamaan estettävää määrää.  
2. Kirjoita päivämäärä **Odotettu päivämäärä** -kenttään. Haluat ehkä määrittää, milloin estetyn varaston odotetaan olevan varattavissa. Voit määrittää tätä varten odotetun päivämäärän. Jos varastoestolle on valittu Odotetut vastaanotot -asetus, kuten oletusarvoisesti on, voit luoda eston manuaalisesti. Tämä päivä näkyy odotetun tapahtuman kohdalla.  
3. Valitse **Tallenna**.

## <a name="remove-the-inventory-blocking"></a>Varastoeston poistaminen
1. Valitse **toimintoruudussa** **Poista**.
2. Valitse **Kyllä**.
3. Sulje sivu.

