---
title: Jumittuneiden erätöiden nollaaminen
description: Tässä artikkelissa kerrotaan, miten ratkaistaan jumiutuneisiin erätöihin liittyvät ongelmat.
author: twheeloc
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: b56a16257a45dd093d10b7550b13d6a4a1ceb1f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896015"
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
