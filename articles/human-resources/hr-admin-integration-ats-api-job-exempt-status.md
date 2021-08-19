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
ms.openlocfilehash: 1c3996d8f693b6df0bf6230b25c9339b2aad1ceaf49a790fda90bbfc1b68be41
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720441"
---
# <a name="job-exempt-status"></a>Työn vapautustila

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