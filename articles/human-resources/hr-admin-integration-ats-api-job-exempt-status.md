---
title: Työn vapautustila
description: Tässä artikkelissa kuvataan Työn vapautustila -asetusjoukkoa Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: e59a71264d50cecce4d31dfa26ad7f05ef3f34e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894669"
---
# <a name="job-exempt-status"></a>Työn vapautustila


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kuvataan Työn vapautustila -asetusjoukkoa Dynamics 365 Human Resourcesissa.

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
