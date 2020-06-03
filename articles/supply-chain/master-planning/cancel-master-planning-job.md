---
title: Pääsuunnittelutyön peruuttaminen
description: Tässä ohjeaiheessa käsitellään kuinka peruuttaa aktiivinen suunnittelutyö, joka käyttää sisäänrakennettua suunnittelutoimintoa.
author: ChristianRytt
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1e38b1bb84414dde603dbf5bcda0e8253a12e40b
ms.sourcegitcommit: 78a1aa37f9a1565135b139e36501b759e7b2f849
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/14/2020
ms.locfileid: "3374793"
---
# <a name="cancel-a-master-planning-job"></a>Pääsuunnittelutyön peruuttaminen

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Managementilla on useita vaihtoehtoja pääsuunnittelutyön peruutukseen. Voit esimerkiksi peruuttaa pääsuunnittelutyön, jos se on käynnistetty vahingossa tai se on odotettua pitempi ja haluat lopettaa sen. Paras tapa peruuttaa suunnittelutyö on tehdä se **Keskeneräiset suunnitteluprosessit** -sivulla. Muita mahdollisia vaihtoehtoja **Erätyöt** ja **Parannetut erätyöt** -sivuilta tulisi käyttää vain, jos pääsuunnittelutyön peruuttaminen **keskeneräiset suunnitteluprosessit** -sivulta ei onnistu muutaman minuutin kuluessa.

## <a name="preferred-cancel-option"></a>Ensisijainen peruutusvaihtoehto
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>Peruuta pääsuunnittelutyö **Keskeneräiset suunnitteluprosessit** -sivulla
1. Siirry kohtaan **Pääsuunnittelu > Kyselyt ja raportit > Pääsuunnittelu > Keskeneräiset suunnitteluprosessit**.
2. Valitse se rivi, jossa peruutettava suunnitteluprosessi sijaitsee.
3. Valitse **Peruuta**.

## <a name="additional-cancel-options"></a>Muut peruutusasetukset
Näitä tulisi käyttää vain jos pääsuunnittelutyön peruutus **Keskeneräiset suunnitteluprosessit** -sivulla ei onnistu muutaman minuutin kuluessa.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Poista pääsuunnittelutyö **Erätyöt**-sivulta
1. Valitse **Järjestelmän hallinta > Kyselyt > Erätyöt**.
2. Valitse se rivi, jossa poistettava suunnittelutyö sijaitsee.
3. Valitse **Poista**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Keskeytä pääsuunnittelutyötehtävä **Parannetut erätyöt** -sivulta
1. Valitse **Järjestelmän hallinta > Kyselyt > Erätyöt**.
2. Jos työn tunnusta ei näytetä luettelossa, valitse **Siirry parannettuun lomakkeeseen**, muutoin jatka seuraavaan vaiheeseen.
3. Avaa erätyö. Napsauta **työn tunnusta** erätyölle, jonka tehtäviä haluat lopettaa.
4. Valitse **Erätehtävissä** tehtävät, jotka haluat lopettaa.
5. Valitse ensin **Muuta tilaa**, sitten **Peruuttaminen** ja lopuksi **OK**.
6. Valitse **Erätehtävät**-pikavälilehdellä **Keskeytä**.
