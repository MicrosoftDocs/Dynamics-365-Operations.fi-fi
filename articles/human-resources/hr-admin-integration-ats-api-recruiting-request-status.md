---
title: Työhönottopyynnön tila
description: Tässä aiheessa kuvataan työhönottopyynnön tilan asetusjoukkoa Dynamics 365 Human Resourcesissa.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125951"
---
# <a name="recruiting-request-status"></a>Työhönottopyynnön tila

Tässä aiheessa kuvataan työhönottopyynnön tilan asetusjoukkoa Dynamics 365 Human Resourcesissa.

Fyysinen nimi: mshr_hcmrecruitingrequeststatus

Tämä valintalista määrittää työhönottopyynnön tilan arvojen asetusjoukon.

| Arvo | Nimiö | kuvaus |
| --- | --- | --- |
| 200000000 | Luonnos | Pyyntö on luonnos eikä se ole valmis aktiiviseen työhönottoon. |
| 200000001 | Tarkistuksessa | Pyyntö on lähetetty, ja se reititetään hyväksyttäväksi työnkulun mukaan. Käytettävissä vain, kun työnkulku on käytössä. |
| 200000002 | Odottava | Pyyntö odottaa työnkulkutoimintoa. Käytettävissä vain, kun työnkulku on käytössä. |
| 200000003 | Peruutettu | Pyyntö on peruutettu. Käytettävissä vain, kun työnkulku on käytössä. |
| 200000004 | Kielletty | Pyyntö on hylätty. Käytettävissä vain, kun työnkulku on käytössä. |
| 200000005 | Käytössä | Kaikki työnkulut on suoritettu ja hyväksytty, ja pyyntö on valmis aktiiviseen työhönottoon. |
| 200000006 | Valmis | Työhönottopyyntö on suljettu. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely työhönottopyyntöä varten](hr-admin-integration-ats-api-recruiting-request-example-query.md)
