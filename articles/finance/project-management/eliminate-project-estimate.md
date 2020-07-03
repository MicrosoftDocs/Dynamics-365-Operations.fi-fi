---
title: Projektiarvion poistaminen
description: Tässä ohjeaiheessa on tietoja projektiarvion poistamisesta sen jälkeen, kun se on valmis.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410214"
---
# <a name="eliminate-a-project-estimate"></a>Projektiarvion poistaminen

[!include [banner](../includes/banner.md)]

Projektin arviot sisältävät projektin arvioidun ja ajoitetun työmäärän rahoitusnäkymän. Voidaksesi työskennellä projektin arvioiden kanssa, projekti on liitettävä arviointiprojektiin. Arviointiprojekti perustuu aina aiemmin luotuun projektiin, mutta kuitenkin useat projektit voivat viitata yksittäiseen arviointiprojektiin. Vain kiinteähintaiset ja investointiprojektit voidaan liittää arviointiprojekteihin, ja näiden projektien on kuuluttava samaan projektiryhmään kuin arviointiprojekti.

Arviointiprojektin eliminointi edellyttää, että se on valmis. Seuraavassa kerrotaan, kuinka arvio poistetaan.

1. Valitse **Projektinhallinta ja kirjanpito** > **Kaikki projektit** ja avaa projekti. 
2. Valitse **Hallitse**-välilehdessä **Arviot** ja valitse **Arvio**-sivulla **Poista**.
3. Määritä **Yleiset**-välilehden **Poista arvio** -sivulla seuraavat asetukset:

   - **Kausikoodi**: Valitse kausikoodi arviointiprojektien valintaa varten. 
   - **Arviopäivämäärä**: Valitse eliminoinnin arviopäivämäärä.
   - **Eliminoi ja KET-varoitukset**: Ota tämä vaihtoehto käyttöön, kun keskeneräiseen työhön (KET) liittyvä arvio poistetaan. Jos tämä vaihtoehto ei ole käytössä, eliminointi ei voi jatkua, jos ei-arvioituja tapahtumia on olemassa. 
   > [!NOTE]
   > Tämä vaihtoehto on käytettävissä vain, kun eliminointi kohdistetaan arviointiprojektiin. Se ei ole käytettävissä, jos käytät kausittaisia kirjauksia. Tämä asetus toimii **Projekti parametrit** -sivun **Arvio**-välilehden asetusten **Salli eliminointi, kun ei-arvioidut tapahtumat ovat olemassa** -kenttäryhmässä.
   - **Aseta vaihe valmiiksi**: Ota tämä asetus käyttöön, kun haluat määrittää, että arviointiprojektin vaihe on **Valmis** eliminoinnin suorittamisen jälkeen.
   - **Tulosta arviointiluettelo**: Valitse tiedot, jotka otetaan mukaan arviointiluetteloa tulostettaessa.
   - **Näytä infoloki**: Ota tämä vaihtoehto käyttöön, kun haluat näyttää infolokin.
   - **Kirjauspvm**: Valitse arvion kirjanpidon kirjauspäivämäärä.

4.  Valitse **OK**.
5. Kun eliminointiprosessi on valmis, eliminoitu arviointiprojekti näytetään negatiivisena arvona. 

Jos et aio poistaa arviota, voit valita eliminoidun arvion ja valita **Peruuta eliminointi**.   
