---
title: Käyttäjien liittäminen käyttöoikeusrooleihin
description: Finance and Operations -sovellusten käyttämistä varten käyttäjille on määritettävä käyttöoikeusrooleja.
author: Peakerbl
manager: AnnBe
ms.date: 05/06/2020
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
ms.openlocfilehash: f0421ad6c932f2c91de51169bda6c98f53d3bc65
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346442"
---
# <a name="assign-users-to-security-roles"></a>Käyttäjien liittäminen käyttöoikeusrooleihin

[!include [banner](../../includes/banner.md)]

Muiden kuin yhteisten toimintojen käyttöä varten Finance and Operations -sovelluksissa käyttäjät on määritettävä käyttöoikeusrooleihin. Voit määrittää käyttäjille roolit automaattisesti sääntöjen ja liiketoimintatietojen perusteella, sulkea käyttäjät pois automaattisesta roolimäärityksestä tai lisätä käyttäjiä rooleihin manuaalisesti.

## <a name="automatically-assign-users-to-roles"></a>Liitä käyttäjät rooleihin automaattisesti
Tässä menettelyssä kerrotaan, kuinka järjestelmänvalvojat voivat automaattisesti määrittää rooleja käyttäjille liiketoimintatietojen perusteella. 
1. Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin**.
2. Valitse puusta Taloushallintopäällikkö. Valitse rooli, jolle haluat konfiguroida säännön. Valitse tässä esimerkissä Taloushallintopäällikkö. 
3. Avaa valintaikkuna valitsemalla **Lisää rooli**.
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
7. Sulje valitut käyttäjät pois roolista valitsemalla **Sulje pois roolista**. Ohitukset voit poistaa valitsemalla käyttäjät, joiden ohituksen haluat poistaa, ja valitsemalla sitten **Palauta tila**. Kun poistat ohituksen palauttamalla käyttäjän tilan, käyttäjän rooli määritetään automaattisesti. Käyttäjää ei kuitenkaan määritetä välittömästi rooliin tai suljeta siitä pois kun palautat tilan. Sen sijaan käyttäjä määritetään rooliin tai poistetaan siitä seuraavalla kerralla, kun automaattisen roolinmäärityksen säännöt ajetaan.  

## <a name="manually-assign-users-to-roles"></a>Käyttäjien liittäminen rooleihin manuaalisesti
Järjestelmänvalvojan on myös poistettava käyttöoikeusrooleihin manuaalisesti määritetyt käyttäjät manuaalisesti. Näitä käyttäjiä ei poisteta rooleista automaattisen roolienmäärityssääntöjen perusteella.

1. Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin**.
2. Valitse puussa rooli ja **Roolille määritetyt käyttäjät** -valikossa **Määritä tai sulje pois käyttäjiä manuaalisesti**.
4. Käyttäjät, joille ei ole määritetty roolia **Määritä käyttäjiä rooliin tai sulje käyttäjät pois roolista** -kohdassa määritetään **Roolienmääritystilassa** asetuksella **Ei mitään**. Valitse vähintään yksi käyttäjä, jolle rooli liitetään.
5. Valitse **toimintoruudussa** **Määritä rooliin**. **Määritystila** päivitetään **Manuaaliseksi**, ja käyttäjät voivat nyt määrittää uuden roolin.
