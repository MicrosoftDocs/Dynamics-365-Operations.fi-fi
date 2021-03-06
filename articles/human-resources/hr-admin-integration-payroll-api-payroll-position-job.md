---
title: Palkanlaskennan työ
description: Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn Palkanlaskennan työntekijän työyksiköstä Dynamics 365 Human Resourcesissa.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 62b9caf94f1c9aa8bb5758e62565fe57dfdd245a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055025"
---
# <a name="payroll-position-job"></a>Palkanlaskennan työ

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn Palkanlaskennan työntekijän työsuhdeyksiköstä Dynamics 365 Human Resourcesissa.

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Työn tunnus**<br>mshr_jobid<br>*Merkkijono* | Readp-only<br>Vaadittu |Työn tunnus. |
| **Voimassaolo alkaa**<br>mshr_validto<br>*Päivämäärä aika siirros* | Vain luku <br>Vaadittu | Päivämäärä, josta kirjaamis- ja työsuhde on voimassa. |
| **Voimassaolo päättyy**<br>mshr_validto<br>*Päivämäärä aika siirros* | Vain luku <br>Vaadittu | Päivämäärä, johon kirjaamis- ja työsuhde on voimassa.  |
| **Toimen tunnus**<br>mshr_positionid<br>*Merkkijono* | Vain luku<br>Vaadittu | Toimen tunnus. |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vaadittu<br>Järjestelmän luoma |  |
| **Toimen työn tunnuksen arvo**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity |Toimeen liittyvän työn tunnus.|
| **Kiinteän kompensaatiosuunnitelman tunnuksen arvo**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity  | Toimeen liittyvän kiinteän kompensaatiosuunnitelman tunnus. |
| **Palkanlaskennan työn yksikkötunnus**<br>mshr_payrollpositionjobentityid<br>*Guid* | Vaadittu<br>Järjestelmän luoma. | Järjestelmän luoma GUID-arvo, jonka avulla työ voidaan yksilöivästi tunnistaa.  |

