---
title: Jumittuneiden erätöiden nollaaminen
description: Tässä aiheessa kerrotaan, miten ratkaistaan jumiutuneisiin erätöihin liittyvät ongelmat.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 859f039a928cdc57c9f227885d0f00ef79980f28
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070397"
---
# <a name="reset-stuck-batch-jobs"></a>Jumittuneiden erätöiden nollaaminen


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Varasto-otto

Microsoft Dynamics 365 Human Resourcesissa voi esiintyä erätöihin liittyviä ongelmia, jotka ovat jumiutuneet **Suoritetaan**- tai **Peruutetaan**-tilaan eivätkä valmistu.

## <a name="resolution"></a>Ratkaisu

Kun erätyöt ovat jumiutuneet **Suoritetaan**- tai **Peruutetaan**-tilaan, voit nollata tilan pakottamalla työn peruutuksen. Kun olet peruuttanut sen, voit nollata erätyön määrittämällä sen tilaksi **Odottaa**. Se noudetaan sitten uudelleen suoritettavaksi seuraavassa ajoitetussa eräsuorituksessa.

1. Valitse **Järjestelmän hallinta** -työtilassa **Linkit**-sivu ja valitse **Erätyöt**.

2. Valitse **Erätyö**-luettelosivulla palautettava työ.

3. Valitse toimintovalintanauhassa **Pakota peruutus** ja vahvista toimenpide.

   > [!NOTE]
   > **Pakota peruutus** -toiminto on käytettävissä vain, kun valitun erätyön tilana on **Suoritetaan** tai **Peruutetaan**, eikä työlle ole käynnissä erän suorituksen tai peruutuksen prosesseja.

4. Valitse toimintovalintanauhassa **Muuta tila**.

5. Valitse **Valitse uusi tila** -sivulla **Odottaa** ja valitse sitten **OK**.

   ![Uuden erätyön tilan valinta.](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>Lisätietoja

[Suorituskyvyn optimointi erätöiden määrityksellä työajan jälkeen](hr-admin-troubleshooting-batch-jobs.md)<br>
[Optimoi suorituskyky automaattisilla tyhjennystehtävillä](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
