---
title: Käyttäjien liittäminen käyttöoikeusrooleihin
description: Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin käyttämistä varten käyttäjille on määritettävä käyttöoikeusrooleja.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "349949"
---
# <a name="assign-users-to-security-roles"></a>Käyttäjien liittäminen käyttöoikeusrooleihin

[!include [task guide banner](../../includes/task-guide-banner.md)]

Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin käyttämistä varten käyttäjille on määritettävä käyttöoikeusrooleja. Tässä menettelyssä kerrotaan, kuinka järjestelmänvalvojat voivat määrittää rooleja käyttäjille automaattisesti liiketoimintatietojen perusteella. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


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

