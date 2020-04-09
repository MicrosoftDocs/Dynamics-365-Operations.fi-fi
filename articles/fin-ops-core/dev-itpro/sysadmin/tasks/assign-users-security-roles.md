---
title: Käyttäjien liittäminen käyttöoikeusrooleihin
description: Finance and Operations -sovellusten käyttämistä varten käyttäjille on määritettävä käyttöoikeusrooleja.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
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
ms.openlocfilehash: 0744f45ac91dfb9b5aae35091e3675202c9144f9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143539"
---
# <a name="assign-users-to-security-roles"></a>Käyttäjien liittäminen käyttöoikeusrooleihin

[!include [banner](../../includes/banner.md)]

Muiden kuin yhteisten toimintojen käyttöä varten käyttäjät on määritettävä käyttöoikeusrooleihin. Tässä menettelyssä kerrotaan, kuinka järjestelmänvalvojat voivat automaattisesti määrittää rooleja käyttäjille liiketoimintatietojen perusteella. 

## <a name="automatically-assign-users-to-roles"></a>Liitä käyttäjät rooleihin automaattisesti
1. Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin**.
2. Valitse puusta Taloushallintopäällikkö. Valitse rooli, jolle haluat konfiguroida säännön. Valitse tässä esimerkissä Taloushallintopäällikkö. 
3. Avaa avattava luettelo valitsemalla **Lisää sääntö**.
4. Etsi haluamasi tietue **Valitse kysely** -luettelosta ja valitse se. Valitse tämä tässä säännössä käytettävä kysely.  
5. Napsauta **Jäsenyyssäännön nimi** -luettelossa valitulla rivillä olevaa linkkiä.
6. Valitse **Muokkaa kyselyä**. Muokkaa kyselyä tarvittaessa.  
7. Valitse **OK**.
8. Valitse **Suorita automaattinen roolin määritys**.
9. Valitse **Siirtymisruutu > Moduulit > Järjestelmän hallinta > Käyttäjät > Käyttäjät** (mielellään erillisessä selaimen välilehdessä).
10. Vahvista, että roolien määrityskysely oli oikein, tarkistamalla eri käyttäjille määritetyt roolit. Säädä ja suorita tarvittaessa uudelleen.

## <a name="exclude-users-from-automatic-role-assignment"></a>Sulje käyttäjät pois automaattisesta roolin määrityksestä
1. Sulje sivu.
2. Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin**.
3. Valitse puusta Taloushallintopäällikkö. Valitse rooli. Valitse tässä esimerkissä Taloushallintopäällikkö.  
4. Valitse **Roolille määritetyt käyttäjät** -valikossa **Määritä tai sulje pois käyttäjiä manuaalisesti**.
5. Merkitse valittu rivi **Määritä käyttäjiä rooliin tai sulje käyttäjiä pois roolista** -luettelossa. Valitse käyttäjä.  
6. Valitse **toimintoruudussa** **Sulje pois roolista**.
    
    Sulje valitut käyttäjät pois roolista valitsemalla **Sulje pois roolista**. Ohitukset voit poistaa valitsemalla käyttäjät, joiden ohituksen haluat poistaa, ja valitsemalla sitten **Palauta tila**. Kun poistat ohituksen palauttamalla käyttäjän tilan, käyttäjän rooli määritetään uudelleen automaattisesti. Käyttäjää ei kuitenkaan määritetä välittömästi rooliin tai suljeta siitä pois kun palautat tilan. Sen sijaan käyttäjä määritetään rooliin tai poistetaan siitä seuraavalla kerralla, kun automaattisen roolinmäärityksen säännöt ajetaan.  
