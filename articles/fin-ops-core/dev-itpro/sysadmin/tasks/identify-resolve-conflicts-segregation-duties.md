---
title: Tehtävien eriyttämisen ristiriitojen tunnistaminen ja ratkaiseminen
description: Tässä ohjeaiheessa kerrotaan, miten tehtävien eriyttämisen ristiriidat tunnistetaan ja ratkaistaan.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0638699c0e569bbe67024a87d6c55729642557cb085ee899aa98aa0022b12840
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748309"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Tehtävien eriyttämisen ristiriitojen tunnistaminen ja ratkaiseminen

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten tehtävien eriyttämisen ristiriidat tunnistetaan ja ratkaistaan. Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät. Tätä kutsutaan tehtävien eriyttämiseksi. Kun käyttäjän käyttöoikeusroolin tai roolimääritysten kuvaus rikkoo sääntöjä, kirjataan ristiriita. Järjestelmänvalvojan on ratkaistava kaikki ristiriidat. Ristiriidat tunnistetaan ja ratkaistaan seuraavalla menettelyllä.

Varmista säännön lisäämisen jälkeen, että kaikki aiemmin luodut säännöt ovat niiden mukaiset. 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a>Tarkista, ovatko aiemmin luodut roolit ja tehtävät tehtävien eriyttämisen uusien sääntöjen mukaisia
1. Valitse **Järjestelmänhallinta** > **Suojaus** > **Tehtävien eriyttäminen** > **Tehtävien eriyttämisen säännöt**.
3. Valitse **Vahvista velvollisuudet ja roolit**. Jos jokin rooli ei ole sääntöjen mukainen, avautunut sanoma sisältää säännön, roolin ja ristiriitaisten tehtävien nimet. Ristiriitaisia rooleja on muokattava **suojausmäärityksen** avulla, eivätkä ne saa sisältää ristiriitaisia tehtäviä. Jos mikään rooli ei riko valittua sääntöä, sanomassa on tieto siitä, että kaikki roolit ovat vaatimustenmukaisia.   

> [!NOTE]
> Oikeellisuustarkistus tehdään vain valitulle säännölle. On tärkeää, että jokaisen säännön vaatimustenmukaisuus tarkistetaan.   

Kun rooli luodaan tai sitä muokataan, tehtävien eriyttämissääntöjen noudattamista seurataan automaattisesti. Roolille ei voi määrittää ristiriitaisia tehtäviä.

Seuraavaksi tarkistetaan, että kaikki aiemmin luodut roolimääritykset ovat vaatimustenmukaisia.

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Tarkista, ovatko käyttäjäroolimääritykset tehtävien eriyttämisen uusien sääntöjen mukaisia
1. Valitse **Järjestelmänhallinta > Suojaus > Tehtävien eriyttäminen > Tarkista käyttäjäroolimääritysten mukaisuus**.
2. Valitse **OK**. Tarkistuksen tulokset näkyvät ilmoituksessa. Ristiriidat kirjataan lokiin **Tehtävien eriyttämisen ratkaisemattomat ristiriidat** -sivulla.   

Kun rooleja määritetään käyttäjille, tehtävien eriyttämissääntöjen noudattamista seurataan automaattisesti. Jos käyttäjälle yritetään määrittää rooleja, joissa on ristiriitaisia tehtäviä, seurauksena on virhesanoma. Ristiriita on silloin ratkaistava estämällä tai sallimalla lisäroolin määritys. Lisärooli määritetään, kun määritys sallitaan. 

> [!NOTE]
> Ristiriitoja ei tällä hetkellä tarkisteta niiden käyttäjien osalta, joille roolit on määritetty Active Directory -toimialueryhmien perusteella.

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Näytä ja ratkaise ristiriitaiset käyttäjäroolimääritykset
1. Valitse **Järjestelmänhallinta** > **Suojaus** > **Tehtävien eriyttäminen** > **Tehtävien eriyttämisen ratkaisemattomat ristiriidat**. 
2. Valitse ristiriita ja valitse sitten jokin seuraavista toiminnoista: 

  - **Hylkää liitos**: Käyttäjän määritys toiseen käyttöoikeusrooliin hylätään. Jos hylkäät roolien automaattiset määritykset, käyttäjä merkitään roolista poissuljetuksi. Poissuljetulle käyttäjälle ei ole myönnetty rooliin liitettyä käyttöoikeutta eikä käyttäjää voi määrittää rooliin, ennen kuin järjestelmänvalvoja poistaa poissulkemisen. 
-  **Salli liitos**: Ristiriita ohitetaan ja käyttäjä voidaan määrittää lisäkäyttöoikeusrooleihin. Jos ohitat ristiriidan, ilmoita syy **Ohittamisen syy** -kenttään. Kaikkia ohitettuja roolimäärityksiä voi tarkastella **Tehtävien eriyttämisen ristiriidat** -sivulla.  

> [!NOTE]
> Jos samalla käyttäjällä on useita ristiriitoja, valitse käyttäjätietue ja arvioi määritetyt roolit **Käyttäjät**-sivulla. Tämä ristiriita voidaan välttää tarkistamalla kukin rooli sen jälkeen, kun se on luotu tai sitä on muokattu.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]