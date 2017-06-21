---
title: "Yhden tositteen ja valuutan uudelleenarvostuksen päivittäminen"
description: "Jotkin organisaatiot kirjaavat kirjauskansioita, jotka sisältävät yhden tositteen, jolla on useampi asiakas tai toimittaja, ja käyttävät myös myynti- tai ostoreskontran ulkomaanvaluutan uudelleenarvostusprosessia. Tässä ohjeaiheessa kuvataan vaiheet, joita näiden organisaatioiden tulee seurata päivittäessään Microsoft Dynamics 365 for Operations -versioon 1611."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d3c6d817424be79b09ccdd89deb7f31599fe9bf5
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a>Yhden tositteen ja valuutan uudelleenarvostuksen päivittäminen

[!include[banner](../includes/banner.md)]


Jotkin organisaatiot kirjaavat kirjauskansioita, jotka sisältävät yhden tositteen, jolla on useampi asiakas tai toimittaja, ja käyttävät myös myynti- tai ostoreskontran ulkomaanvaluutan uudelleenarvostusprosessia. Tässä ohjeaiheessa kuvataan vaiheet, joita näiden organisaatioiden tulee seurata päivittäessään Microsoft Dynamics 365 for Operations -versioon 1611.

Toimi seuraavasti, kun asennat päivityksen Microsoft Dynamics 365 for Operations -versioon 1611.

1.  Ennen kuin päivität Dynamics 365 for Operationsin, suorita ulkomaanvaluutan uudelleenarvostusprosessi myynti- ja ostoreskontralle. Määritä **Tapa**-kentän arvoksi **Laskupäivämäärä**. Järjestelmä luo uudelleenarvostustapahtuman, joka kumoaa edellisen ulkomaanvaluutan uudelleenarvostuksen. Siksi avoimet tapahtumat arvostetaan niiden alkuperäisessä kirjanpitovaluutassa.
2.  Päivitä Dynamics 365 for Operations -versioon 1611.
3.  Aja ulkomaanvaluutan uudelleenarvostus uudelleen osto- ja myyntireskontrassa. Aseta tällä kertaa **Tapa**-kentän arvoksi **Vakio**. Järjestelmä luo uuden uudelleenarvostustapahtuman, joka perustuu nykyisiin vaihtokursseihin. Tähän tapahtumaan tallennetaan toteutumaton voitto/tappio ja oikea reskontrakirjanpitotili.





