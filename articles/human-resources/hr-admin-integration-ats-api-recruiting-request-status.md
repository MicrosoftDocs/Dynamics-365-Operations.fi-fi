---
title: Työhönottopyynnön tila
description: Tässä aiheessa kuvataan työhönottopyynnön tilan asetusjoukkoa Dynamics 365 Human Resourcesissa.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 888fbc511bffbecd837c929049006266191da5ba
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5806039"
---
# <a name="recruiting-request-status"></a>Työhönottopyynnön tila

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]