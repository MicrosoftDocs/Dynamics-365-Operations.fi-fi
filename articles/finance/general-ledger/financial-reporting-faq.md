---
title: Taloushallinnon raportoinnin usein kysytyt kysymykset
description: Tässä ohjeaiheessa käsitellään kysymyksiä, joita muilla käyttäjillä on ollut taloushallinnon raportoinnista.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3f9381f5b656d0cc0b46c8828b2ef9d024e296b0
ms.sourcegitcommit: 14785208d84b2c1efd30f140c52df35a2ccd1577
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/27/2021
ms.locfileid: "5070214"
---
# <a name="financial-reporting-faq"></a>Taloushallinnon raportoinnin usein kysytyt kysymykset 

Tässä ohjeaiheessa käsitellään kysymyksiä, joita muilla käyttäjillä on ollut taloushallinnon raportoinnista. 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Miten rajoitan raportin käyttöoikeuksia puurakenteen suojauksen avulla?

Skenaario: esittely-yrityksellä USMF on taseraportti, jota se ei halua kaikkien taloushallinnon raportoinnin käyttäjien voivan nähdä D365:ssä. Ratkaisu: voit rajoittaa yksittäisen raportin käyttöoikeutta puurakenteen suojauksen avulla siten, että vain tietyt käyttäjät voivat käyttää raporttia. 

1.  Kirjaudu raporttien suunnitteluohjelmaan

2.  Luo uusi puumääritys (Tiedosto | Uusi | Puumääritys) a.    Kaksoisnapsauta **Yhteenveto**-riviä **Yksikkösuojaus**-sarakkeessa.
  i.    Valitse Käyttäjät ja ryhmät.  
          1. Valitse käyttäjät tai ryhmä, joiden haluat voivat käyttää tätä raporttia. 
          
[![käyttäjänäyttö](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)

[![suojausnäyttö](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)

  b.    Valitse **Tallenna**.
  
[![Tallenna-painike](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)

3.  Lisää uusi puumäärityksesi raportin määritykseen

[![puumäärityslomake](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)

A.  Valitse puumäärityksessä Asetus ja valitse Raporttiyksikön valinta -kohdassa Sisällytä kaikki yksiköt

[![raporttiyksikön valintalomake](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)

**Ennen:** [![ennen-näyttökuva](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)

**Jälkeen:** [![jälkeen-näyttökuva](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)

Huomautus: edellä kuvatun sanoman syy on se, että käyttäjällä ei ole raportin käyttöoikeutta yksikön suojauksen käyttöönoton jälkeen



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a>Miten selvitän, mitkä tilit eivät täsmää saldojeni kanssa D365:ssä?

Jos sinulla on D365:ssä raportti, joka ei vastaa odotuksiasi, voit kokeilla seuraavia toimia täsmäämättömien tilien ja niiden varianssien tunnistamiseksi. 

### <a name="in-financial-reporter-report-designer"></a>Raporttien suunnitteluohjelmassa

1.  Luo uusi rivimääritys a.    Valitse Muokkaa | Lisää rivit dimensioista i.  Valitse MainAccount [![Valitse päätili ‑näyttö_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)
    
    ii. Valitse Ok b.    Tallenna rivimääritys

2.  Luo uusi sarakemääritys     [![Luo uusi sarakemääritys](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)

3.  Luo uusi raportin määritys a.    Valitse Asetukset ja poista [![Asetukset-lomakkeen](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png) valinta
   
4.  Luo raportti. 

5.  Vie raportti Exceliin.

### <a name="in-d365"></a>D365:ssä: 
1.  Valitse Kirjanpito | Kyselyt ja raportit | Pääkirja a.    Parametrit i.  Aloituspäivä: tilikauden alku ii. Päivämäärään: päivämäärä, jolle olet luonut raportin iii.    Taloushallinnon dimensioyhdistelmä ”Asetettu päätili” [![Päätili-lomake](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)
      
  b.    Valitse Laske

2.  Vie raportti Exceliin

Nyt sinun pitäisi nyt pystyä kopioimaan tiedot FR Excel -raportista D365:n Pääkirja-raporttiin ja vertaamaan Loppusaldo-sarakkeita.
