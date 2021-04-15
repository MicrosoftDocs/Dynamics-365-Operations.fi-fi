---
title: Valmistumisen tila
description: Tässä aiheessa kuvataan Valmistumisen tila -asetusjoukkoa Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: f1b0c61ac9d9dc611d2a4700a1a004e3d15b4445
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798366"
---
# <a name="completion-status"></a>Valmistumisen tila

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Valmistumisen tila -asetusjoukkoa Dynamics 365 Human Resourcesissa.

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