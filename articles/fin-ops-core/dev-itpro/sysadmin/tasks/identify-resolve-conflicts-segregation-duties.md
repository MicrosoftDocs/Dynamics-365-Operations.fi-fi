---
title: Tehtävien eriyttämisen ristiriitojen tunnistaminen ja ratkaiseminen
description: Tässä ohjeaiheessa kerrotaan, miten tehtävien eriyttämisen ristiriidat tunnistetaan ja ratkaistaan.
author: maertenm
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 70fe3bb707f2f204cda92ec979fe9fe1a3b96bac
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143601"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Tehtävien eriyttämisen ristiriitojen tunnistaminen ja ratkaiseminen

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten tehtävien eriyttämisen ristiriidat tunnistetaan ja ratkaistaan. Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät. Tätä kutsutaan tehtävien eriyttämiseksi. Kun käyttäjän käyttöoikeusroolin tai roolimääritysten kuvaus rikkoo sääntöjä, kirjataan ristiriita. Järjestelmänvalvojan on ratkaistava kaikki ristiriidat. Ristiriidat tunnistetaan ja ratkaistaan seuraavalla menettelyllä. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Tarkista, ovatko käyttäjäroolimääritykset tehtävien eriyttämisen uusien sääntöjen mukaisia
1. Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Tehtävien eriyttäminen > Tarkista käyttäjäroolimääritysten mukaisuus**.
2. Valitse **OK**. Tarkistuksen tulokset näkyvät ilmoituksessa. Voit avata ristiriitatilanteessa **Käyttäjät**-sivun ja muuttaa käyttäjän roolimäärityksiä. Ristiriidat kirjataan myös **Tehtävien eriyttämisen ristiriidat** -sivulle. Voit suorittaa erätyön tarkistusprosessin valitsemalla **Eräkäsittely** ja määrittämällä sitten eräparametrit. Kun erätyö on suoritettu, voit tarkastella ristiriitoja **Tehtävien eriyttämisen ristiriidat** -sivulla.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Näytä ja ratkaise ristiriitaiset käyttäjäroolimääritykset
1. Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Tehtävien eriyttäminen > Tehtävien eriyttämisen ristiriidat**. Valitse ristiriita ja napsauta sitten jotakin seuraavista painikkeista: **Hylkää liitos – Hylkää käyttäjän liitos toiseen käyttöoikeusrooliin**. Jos hylkäät roolien automaattiset määritykset, käyttäjä merkitään roolista poissuljetuksi. Poissuljetulle käyttäjälle ei ole myönnetty rooliin liitettyä käyttöoikeutta eikä käyttäjää voi määrittää rooliin, ennen kuin järjestelmänvalvoja poistaa poissulkemisen. Salli liitos – **Ohita** ristiriita ja sallii käyttäjän määrittämisen molempiin käyttöoikeusrooleihin. Jos ohitat ristiriidan, ilmoita syy **Ohittamisen syy** -kenttään.  
2. Sulje sivu.
3. Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Tehtävien eriyttäminen > Tehtävien eriyttämisen ratkaisemattomat ristiriidat**. Valitse ristiriita ja napsauta sitten jotakin seuraavista painikkeista: **Hylkää liitos – Hylkää käyttäjän liitos toiseen käyttöoikeusrooliin**. Jos hylkäät roolien automaattiset määritykset, käyttäjä merkitään roolista poissuljetuksi. Poissuljetulle käyttäjälle ei ole myönnetty rooliin liitettyä käyttöoikeutta eikä käyttäjää voi määrittää rooliin, ennen kuin järjestelmänvalvoja poistaa poissulkemisen. Salli liitos – **Ohita** ristiriita ja sallii käyttäjän määrittämisen molempiin käyttöoikeusrooleihin. Jos ohitat ristiriidan, ilmoita syy **Ohittamisen syy** -kenttään.    
4. Sulje sivu.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Tarkista, ovatko aiemmin luodut roolit tehtävien eriyttämisen uusien sääntöjen mukaisia
1. Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Tehtävien eriyttäminen > Tehtävien eriyttämisen säännöt**. Valitse sääntö.  
2. Valitse **Vahvista velvollisuudet ja roolit**. Jos aiemmin luotu rooli ei ole valitun säännön mukainen, avautunut sanoma sisältää roolin ja ristiriitaisten tehtävien nimet. Järjestelmänvalvojan on joko osoitettava suojausriskin mitätöintitapa tai muokattava roolia siten, että se ei riko tehtävien eriyttämissääntöjä. Jos mikään rooli ei riko valittua sääntöä, sanomassa on tieto siitä, että kaikki roolit ovat vaatimustenmukaisia.  

