---
title: Käyttäjien liittäminen käyttöoikeusrooleihin
description: Finance and Operations -sovellusten käyttö edellyttää, että käyttäjille on määritetty käyttöoikeusroolit.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180964"
---
# <a name="assign-users-to-security-roles"></a>Käyttäjien liittäminen käyttöoikeusrooleihin

[!include [task guide banner](../../includes/task-guide-banner.md)]

Muiden kuin yhteisten toimintojen käyttöä varten käyttäjät on määritettävä käyttöoikeusrooleihin. Tässä menettelyssä kerrotaan, kuinka järjestelmänvalvojat voivat automaattisesti määrittää rooleja käyttäjille liiketoimintatietojen perusteella. 

## <a name="automatically-assign-users-to-roles"></a>Liitä käyttäjät rooleihin automaattisesti
1. Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin**.
2. Valitse puusta Taloushallintopäällikkö. Valitse rooli, jolle haluat konfiguroida säännön. Valitse tässä esimerkissä Taloushallintopäällikkö. 
3. Avaa avattava luettelo valitsemalla **Lisää sääntö**.
4. Etsi haluamasi tietue **Valitse kysely** -luettelosta ja valitse se. Valitse tämä tässä säännössä käytettävä kysely.  
5. Napsauta **Jäsenyyssäännön nimi** -luettelossa valitulla rivillä olevaa linkkiä.
6. Valitse **Muokkaa kyselyä**. Muokkaa kyselyä tarvittaessa.  
7. Valitse **OK**.

## <a name="exclude-users-from-automatic-role-assignment"></a>Sulje käyttäjät pois automaattisesta roolin määrityksestä
1. Sulje sivu.
2. Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin**.
3. Valitse puusta Taloushallintopäällikkö. Valitse rooli. Valitse tässä esimerkissä Taloushallintopäällikkö.  
4. Valitse **Roolille määritetyt käyttäjät** -valikossa **Määritä tai sulje pois käyttäjiä manuaalisesti**.
5. Merkitse valittu rivi **Määritä käyttäjiä rooliin tai sulje käyttäjiä pois roolista** -luettelossa. Valitse käyttäjä.  
6. Valitse **toimintoruudussa** **Sulje pois roolista**.
    
    Sulje valitut käyttäjät pois roolista valitsemalla **Sulje pois roolista**. Ohitukset voit poistaa valitsemalla käyttäjät, joiden ohituksen haluat poistaa, ja valitsemalla sitten **Palauta tila**. Kun poistat ohituksen palauttamalla käyttäjän tilan, käyttäjän rooli määritetään uudelleen automaattisesti. Käyttäjää ei kuitenkaan määritetä välittömästi rooliin tai suljeta siitä pois kun palautat tilan. Sen sijaan käyttäjä määritetään rooliin tai poistetaan siitä seuraavalla kerralla, kun automaattisen roolinmäärityksen säännöt ajetaan.  
