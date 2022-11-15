---
title: Vanhentuneella pääsuunnittelumoduulilla luodun työn peruuttaminen
description: Tässä artikkelissa käsitellään vanhentunutta pääsuunnittelumoduulia käyttävän aktiivisen suunnittelutyön peruuttamista.
author: t-benebo
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7b71a43f407050dccb7550db7c4b6a98a596d589
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740874"
---
# <a name="cancel-a-job-that-was-created-using-the-deprecated-master-planning-engine"></a>Vanhentuneella pääsuunnittelumoduulilla luodun työn peruuttaminen

[!include [banner](../includes/banner.md)]

Vanhentuneella pääsuunnittelumoduulilla luodun työn voi peruuttaa monin eri tavoin. Voit esimerkiksi peruuttaa pääsuunnittelutyön, jos se on käynnistetty vahingossa tai se on odotettua pitempi ja haluat lopettaa sen.

Paras tapa peruuttaa suunnittelutyö on tehdä se **Keskeneräiset suunnitteluprosessit** -sivulla. Muita mahdollisia vaihtoehtoja **Erätyöt** ja **Parannetut erätyöt** -sivuilta tulisi käyttää vain, jos pääsuunnittelutyön peruuttaminen **keskeneräiset suunnitteluprosessit** -sivulta ei onnistu muutaman minuutin kuluessa.

## <a name="preferred-cancel-option"></a>Ensisijainen peruutusvaihtoehto

### <a name="cancel-master-planning-job-from-the-unfinished-planning-processes-page"></a>Pääsuunnittelutyön peruuttaminen Keskeneräiset suunnitteluprosessit -sivulla

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
3. Avaa erätyö. Valitse sen erätyön **Työn tunnus**, jonka tehtäviä haluat lopettaa.
4. Valitse **Erätehtävissä** tehtävät, jotka haluat lopettaa.
5. Valitse **Muuta tilaa**, valitse **Peruuttaminen** ja napsauta **OK**.
6. Valitse **Erätehtävät**-pikavälilehdellä **Keskeytä**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]