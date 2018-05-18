--- 
title: "Käyttäjien liittäminen käyttöoikeusrooleihin"
description: "Microsoft Dynamics 365 for Finance and Operationsin käyttö edellyttää, että käyttäjille on määritetty käyttöoikeusroolit."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: da96ec8357ea209fd958e32ab438b13e668735df
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---
# <a name="assign-users-to-security-roles"></a>Käyttäjien liittäminen suojausrooleihin

[!include [task guide banner](../../includes/task-guide-banner.md)]

Microsoft Dynamics 365 for Finance and Operationsin käyttö edellyttää, että käyttäjille on määritetty käyttöoikeusroolit. Tässä menettelyssä kerrotaan, kuinka järjestelmänvalvojat voivat määrittää rooleja käyttäjille automaattisesti liiketoimintatietojen perusteella. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="automatically-assign-users-to-roles"></a>Liitä käyttäjät rooleihin automaattisesti
1. Valitse Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin.
2. Valitse puusta Taloushallintopäällikkö.
    * Valitse rooli, jolle haluat konfiguroida säännön. Valitse tässä esimerkissä Taloushallintopäällikkö.  
3. Avaa valintaikkuna napsauttamalla Lisää sääntö -painiketta.
4. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse tämä tässä säännössä käytettävä kysely.  
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Valitse Muokkaa kyselyä.
    * Muokkaa kyselyä tarvittaessa.  
7. Valitse OK.

## <a name="exclude-users-from-automatic-role-assignment"></a>Sulje käyttäjät pois automaattisesta roolin määrityksestä
1. Sulje sivu.
2. Valitse Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin.
3. Valitse puusta Taloushallintopäällikkö.
    * Valitse rooli. Valitse tässä esimerkissä Taloushallintopäällikkö.  
4. Napsauta Määritä tai sulje pois käyttäjiä manuaalisesti -kohtaa.
5. Merkitse valittu rivi luettelossa.
    * Valitse käyttäjä.  
6. Napsauta Sulje pois roolista -kohtaa.
    * Napsauta Sulje pois roolista -painiketta sulkeaksesi valitut käyttäjät pois roolista. Ohitukset voit poistaa valitsemalla käyttäjät, joiden ohituksen haluat poistaa ja napsauttamalla Palauta tila -painiketta. Kun poistat ohituksen palauttamalla käyttäjän tilan, käyttäjän rooli määritetään uudelleen automaattisesti. Käyttäjää ei kuitenkaan määritetä välittömästi rooliin tai suljeta siitä pois kun palautat tilan. Sen sijaan käyttäjä määritetään rooliin tai poistetaan siitä seuraavalla kerralla, kun automaattisen roolinmäärityksen säännöt ajetaan.  


