---
title: Määritä kulukäytännöt
description: Voit määrittää kulukäytäntöjä tai sääntöjä, joita työntekijöiden on noudatettava kirjatessaan ja lähettäessään kuluraportteja ja matkustusehdotuksia Microsoft Dynamics 365 for Finance and Operationsissa.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26336710b277ce9594c8546f2214e152a3460204
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840886"
---
# <a name="expense-policies"></a>Kulukäytännöt

[!include [banner](../includes/banner.md)]

Voit määrittää käytäntöjä tai sääntöjä, joita työntekijöiden on noudatettava kirjatessaan ja lähettäessään kuluraportteja ja matkustusehdotuksia.         
Kulukäytäntöjen käyttöönotto auttaa hallitsemaan kuluja tehokkaasti.         

Voit esimerkiksi määrittää käytännön, jonka mukaan hotellikulut New Yorkissa yötä kohti eivät saa ylittää 250 Yhdysvaltain dollaria.       
Jos työntekijä lähettää kuluraportin tai matkustusehdotuksen, jonka huoneen hinta ylittää tämän summan, järjestelmä ilmoittaa        
työntekijälle, että kulukäytännön summa on ylitetty. Voit määrittää työntekijälle lähetettävän viestin, kun        
määrität käytännön.      
        
Voit määrittää kolmenlaisia käytäntöjä:         
        
- Varoitus – antaa työntekijän lähettää kuluraportin tai matkustusehdotuksen, mutta kulu merkitään kaikille hyväksyjille ja        
  myöhempää raportointia varten.        

- Virhe – edellyttää, että työntekijä muuttaa kulua vastaamaan käytäntöä ennen kuluraportin tai matkustusehdotuksen lähettämistä.       
 
 - Peruse – edellyttää, että työntekijä tai esimies antaa käytännön summan ylittämiselle perusteen ennen kuluraportin tai matkustusehdotuksen lähettämistä.        

## <a name="policy-tips"></a>Käytännön vinkkejä
Seuraavassa on muutamia ehdotuksia, jotka voivat auttaa sinua uusien kulujen hallintakäytäntöjen luomisessa. 
* Käytännöt ovat riippuvaisia voimaantulopäivästä, eivätkä ne tule voimaan, jos käytäntö luodaan sen päivämäärän jälkeen, jolloin kulu on syntynyt. Jos esimerkiksi olet luomassa uutta käytäntöä, jonka mukaan $50 enimmäisateriakustannukset ovat voimassa, kaikkia eilisestä lähtien määritettyjä kuluja ei tarkisteta tätä käytäntöä vasten.
* Kun luot käytännön kululuokalle, joka voidaan määrittää, harkitse kulujen rivityypin ehdon lisäämistä. Jotkin käytännöt, kuten kuittauksen vaatiminen, eivät ehkä ole järkeviä eriteltyjä rivejä varten, ja niitä tulisi käyttää vain otsikkorivillä tai ei-eriteltyjen rivien yhteydessä. 

## <a name="when-to-evaluate-policies"></a>Käytäntöjen arvioiminen

Kulujenhallinnan parametreissa voit joko arvioida kulunhallintakäytäntöjä, kun rivi tallennetaan tai kun kuluraportti lähetetään. Jos päätät arvioida, milloin rivi tallennetaan, tämä varmistaa, että käyttäjillä on aiemmin ollut näkyvyyttä, jotta he voivat täyttää kuluraportin kerralla. Muussa tapauksessa voit viivyttää käytännön arviointia ja säästää aikaa, jos oikeellisuustarkistus tapahtuu lopussa, työn kulkuun lähettämisen aikana.
