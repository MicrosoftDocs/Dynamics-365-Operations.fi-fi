---
title: Yhden tositteen kirjauskansioiden ja valuutan uudelleenarvostusten päivittäminen
description: Tässä aiheessa käsitellään yhden tositteen kirjauskansioiden ja valuutan uudelleenarvostusten päivittämistä.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3504c01a4ed1571866fd2a0cd83eef86a57d684a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127300"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>Yhden tositteen kirjauskansioiden ja valuutan uudelleenarvostusten päivittäminen

[!include [banner](../includes/banner.md)]

Jotkin organisaatiot kirjaavat kirjauskansioita, jotka sisältävät yhden tositteen, jolla on useampi asiakas tai toimittaja, ja käyttävät myös myynti- tai ostoreskontran ulkomaanvaluutan uudelleenarvostusprosessia. Tässä ohjeaiheessa kuvataan vaiheet, joita näiden organisaatioiden tulee seurata päivittäessään Microsoft Dynamics 365 for Operationsin versioon 1611.

Tee päivitys Microsoft Dynamics 365 for Operationsin versioon 1611 seuraavien ohjeiden avulla.

1.  Ennen kuin päivität Finance and Operationsiin, suorita ulkomaanvaluutan uudelleenarvostusprosessi myynti- ja ostoreskontralle. Määritä **Tapa**-kentän arvoksi **Laskupäivämäärä**. Järjestelmä luo uudelleenarvostustapahtuman, joka kumoaa edellisen ulkomaanvaluutan uudelleenarvostuksen. Siksi avoimet tapahtumat arvostetaan niiden alkuperäisessä kirjanpitovaluutassa.
2.  Päivitä versioon 1611.
3.  Aja ulkomaanvaluutan uudelleenarvostus uudelleen osto- ja myyntireskontrassa. Aseta tällä kertaa **Tapa**-kentän arvoksi **Vakio**. Järjestelmä luo uuden uudelleenarvostustapahtuman, joka perustuu nykyisiin vaihtokursseihin. Tähän tapahtumaan tallennetaan toteutumaton voitto/tappio ja oikea reskontrakirjanpitotili.
