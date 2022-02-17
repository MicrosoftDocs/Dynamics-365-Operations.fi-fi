---
title: Työn vapautustila
description: Tässä aiheessa kuvataan Työn vapautustila -asetusjoukkoa Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 29d3c4fd37a219b520172c6866c5fec488c698f7
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8064988"
---
# <a name="job-exempt-status"></a>Työn vapautustila


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Työn vapautustila -asetusjoukkoa Dynamics 365 Human Resourcesissa.

Fyysinen nimi: cdm_jobexemptstatus

Tämä valintaluettelo määrittää asetusjoukon työn FLSA-vapautustilan arvoille. Tämä tieto esitetään aiemmin luodussa cdm_jobexemptstatus-asetusjoukossa.

| Arvo | Nimiö | kuvaus |
| --- | --- | --- |
| 200000000 | Veroton | Työllä on vapautustila FLSA-ohjeiden mukaisesti. |
| 200000001 | Ei-vapautustila | Työllä on ei-vapautustila FLSA-ohjeiden mukaisesti. |
| 200000002 | Ei koske | FLSA-tilan ohjeet eivät koske työtä. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely työhönottopyyntöä varten](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
