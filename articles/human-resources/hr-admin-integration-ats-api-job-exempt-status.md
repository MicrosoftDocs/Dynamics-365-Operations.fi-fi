---
title: Työn vapautustila
description: Tässä aiheessa kuvataan Työn vapautustila -asetusjoukkoa Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 0cd6ffc01793c8ff12e36175c7c9feaf8a4b3cdf
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125566"
---
# <a name="job-exempt-status"></a>Työn vapautustila

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
