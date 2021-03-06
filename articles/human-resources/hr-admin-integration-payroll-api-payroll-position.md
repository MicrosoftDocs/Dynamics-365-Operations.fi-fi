---
title: Palkanlaskennan tiedot toimista
description: Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn palkanlaskennan tiedot toimiyksiköstä Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 8918044dbf84e79015dc3bca904f204123a37db8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056777"
---
# <a name="payroll-position"></a>Palkanlaskennan toimi

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn palkanlaskennan tiedot toimiyksiköstä Dynamics 365 Human Resourcesissa.

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Vuosittaiset vakiotunnit**<br>annualregularhours<br>*Desimaali* | Vain luku<br>Vaadittu | Toimessa määritetyt vuosittaiset säännölliset tunnit.  |
| **Palkanlaskennan toimen tiedot -yksikön tunnus**<br>payrollpositiondetailsentityid<br>*Guid* | Vaadittu<br>Järjestelmän luoma. | Järjestelmän luoma GUID-arvo, jonka avulla toimi voidaan yksilöivästi tunnistaa.  |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vaadittu<br>Järjestelmän luoma |  |
| **Toimen työn tunnuksen arvo**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity |Toimeen liittyvän työn tunnus.|
| **Kiinteän kompensaatiosuunnitelman tunnuksen arvo**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity  | Toimeen liittyvän kiinteän kompensaatiosuunnitelman tunnus. |
| **Maksujakson tunnus**<br>mshr_primaryfield<br>*Merkkijono* | Vain luku<br>Vaadittu | Toimessa määritetty maksusykli. |
| **Yrityksen maksama**<br>paidbylegalentity<br>*Merkkijono* | Vain luku<br>Vaadittu | Maksun määräyksestä vastaavassa toimessa määritetty yritys. |
| **Toimen tunnus**<br>mshr_positionid<br>*Merkkijono* | Vain luku<br>Vaadittu | Toimen tunnus. |
| **Voimassaolo päättyy**<br>validto<br>*Päivämäärä aika siirros* | Vain luku<br>Vaadittu |Päivämäärä, josta toimitiedot ovat voimassa.  |
| **Voimassaolo alkaa**<br>validfrom<br>*Päivämäärä aika siirros* | Vain luku<br>Vaadittu |Päivämäärä, johon toimitiedot ovat voimassa.  |

**Kysely**

**Pyyntö**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**Vastaus**

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
