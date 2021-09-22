---
title: Virhe lähetettäessä ostotilausta uudelleen työnkulkuun muutoksen jälkeen
description: Virhe lähetettäessä ostotilausta uudelleen työnkulkuun muutoksen jälkeen
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4b8465d198c440f27a4b3cc4268445e0aa450f5b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476275"
---
# <a name="error-on-resubmitting-a-purchase-order-to-a-workflow-after-a-change"></a>Virhe lähetettäessä ostotilausta uudelleen työnkulkuun muutoksen jälkeen


## <a name="symptoms"></a>Oireet

Työnkulussa tapahtuu seuraava virhe, kun ostotilaus lähetetään uudelleen muutoksen jälkeen:

> Pysäytetty (virhe): X ++ -poikkeus: Ostotilaukseen PO0000569 tehtävät muutokset ovat sallittuja Luonnos-tilassa, vain, kun muutoksenhallinta aktivoidaan seuraavissa kohdissa:<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

Tämä ongelma ilmenee vain, jos ostotilaus oli tilassa *Vahvistettu*, ennen kuin muutoksia pyydettiin. Jos pyydät muutoksia ostotilauksen ollessa tilassa *Hyväksytty*, työnkulku voidaan käsitellä onnistuneesti.

## <a name="resolution"></a>Ratkaisu

Tämä ongelma voi esiintyä, kun ostotilausten jaoissa on epäjohdonmukaisuuksia.

Voit poistaa tämän ongelman eston ja palauttaa ostotilauksen *Luonnos* siirtymällä kohtaan **Ostot ja hankinnat \> Säännölliset tehtävät \> Tyhjennys \> Ostotilauksen jaon palautus**. Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostotilausten jakovirheiden korjaaminen Dynamics 365 Supply Chain Managementissa](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Ongelma korjataan [tämän Microsoft Knowledge Base (KB) -artikkelin](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138) avulla.
