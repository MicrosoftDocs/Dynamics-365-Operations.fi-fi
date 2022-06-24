---
title: Valmistumisen tila
description: Tässä artikkelissa kuvataan Valmistumisen tila -asetusjoukkoa Dynamics 365 Human Resourcesissa.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 32575dfdd9bcd61b8a16bb544a9e7906ec96eaa1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880564"
---
# <a name="completion-status"></a>Valmistumisen tila


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kuvataan Valmistumisen tila -asetusjoukkoa Dynamics 365 Human Resourcesissa.

Fyysinen nimi: mshr_hcmcompletionstatus

Tämä valintalista määrittää hakijan seulontojen tilan arvojen asetusjoukon. 

| Arvo | Nimiö | kuvaus |
| --- | --- | --- |
| 200000000 | Ei valmis | Hakija ei ole vielä suorittanut seulontaa loppuun. |
| 200000001 | Hyväksy | Hakija läpäisi seulonnan. |
| 200000002 | Epäonnistuminen | Hakija ei läpäissyt seulontaa. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
