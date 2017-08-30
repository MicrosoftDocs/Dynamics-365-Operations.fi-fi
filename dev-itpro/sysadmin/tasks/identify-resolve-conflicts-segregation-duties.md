--- 
title: "Tunnista ja ratkaise tehtävien eriyttämisen ristiriidat"
description: "Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: fdc0bbd0a239c8d7719271445a4d6a5323e87aad
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Tunnista ja ratkaise tehtävien eriyttämisen ristiriidat

[!include[task guide banner](../../includes/task-guide-banner.md)]

Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät. Tätä kutsutaan tehtävien eriyttämiseksi. Kun käyttäjän käyttöoikeusroolin tai roolimääritysten kuvaus rikkoo sääntöjä, kirjataan ristiriita. Järjestelmänvalvojan on ratkaistava kaikki ristiriidat. Ristiriidat tunnistetaan ja ratkaistaan seuraavalla menettelyllä. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Tarkista, ovatko käyttäjäroolimääritykset tehtävien eriyttämisen uusien sääntöjen mukaisia
1. Valitse Järjestelmänhallinta > Suojaus > Tehtävien eriyttäminen > Tarkista käyttäjäroolimääritysten mukaisuus.
2. Valitse OK.
    * Tarkistuksen tulokset näkyvät ilmoituksessa.     Voit avata ristiriitatilanteessa Käyttäjät-sivun ja muuttaa käyttäjän roolimäärityksiä. Ristiriidat kirjataan myös Tehtävien eriyttämisen ristiriidat -sivulle.     Voit suorittaa erätyön tarkistusprosessin valitsemalla Eräkäsittely ja määrittämällä sitten eräparametrit. Kun erätyö on suoritettu, voit tarkastella ristiriitoja Tehtävien eriyttämisen ristiriidat -sivulla.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Näytä ja ratkaise ristiriitaiset käyttäjäroolimääritykset
1. Valitse Järjestelmänhallinta > Suojaus > Tehtävien eriyttäminen > Tehtävien eriyttämisen ristiriidat.
    * Valitse ristiriita ja napsauta sitten jotakin seuraavista painikkeista: Hylkää liitos – Hylkää käyttäjän liitos toiseen käyttöoikeusrooliin. Jos hylkäät roolien automaattiset määritykset, käyttäjä merkitään roolista poissuljetuksi. Poissuljetulle käyttäjälle ei ole myönnetty rooliin liitettyä käyttöoikeutta eikä käyttäjää voi määrittää rooliin, ennen kuin järjestelmänvalvoja poistaa poissulkemisen.     Salli liitos – Ohittaa ristiriidan ja sallii käyttäjän määrittämisen molempiin käyttöoikeusrooleihin. Jos ohitat ristiriidan, ilmoita syy Ohittamisen syy -kenttään.  
2. Sulje sivu.
3. Valitse Järjestelmänhallinta > Suojaus > Tehtävien eriyttäminen > Tehtävien eriyttämisen ratkaisemattomat ristiriidat.
    * Valitse ristiriita ja napsauta sitten jotakin seuraavista painikkeista: Hylkää liitos – Hylkää käyttäjän liitos toiseen käyttöoikeusrooliin. Jos hylkäät roolien automaattiset määritykset, käyttäjä merkitään roolista poissuljetuksi. Poissuljetulle käyttäjälle ei ole myönnetty rooliin liitettyä käyttöoikeutta eikä käyttäjää voi määrittää rooliin, ennen kuin järjestelmänvalvoja poistaa poissulkemisen.     Salli liitos – Ohittaa ristiriidan ja sallii käyttäjän määrittämisen molempiin käyttöoikeusrooleihin. Jos ohitat ristiriidan, ilmoita syy Ohittamisen syy -kenttään.    
4. Sulje sivu.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Tarkista, ovatko aiemmin luodut roolit tehtävien eriyttämisen uusien sääntöjen mukaisia
1. Valitse Järjestelmänhallinta > Suojaus > Tehtävien eriyttäminen > Tehtävien eriyttämisen säännöt.
    * Valitse sääntö.  
2. Valitse Vahvista velvollisuudet ja roolit.
    * Jos aiemmin luotu rooli ei ole valitun säännön mukainen, avautunut sanoma sisältää roolin ja ristiriitaisten tehtävien nimet. Järjestelmänvalvojan on joko osoitettava suojausriskin mitätöintitapa tai muokattava roolia siten, että se ei riko tehtävien eriyttämissääntöjä.     Jos mikään rooli ei riko valittua sääntöä, sanomassa on tieto siitä, että kaikki roolit ovat vaatimustenmukaisia.  

