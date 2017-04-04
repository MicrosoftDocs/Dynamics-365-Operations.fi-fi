---
title: "Yksittäisen tositteen ja valuutan uudelleenarvostuksen päivittäminen Microsoft Dynamics-365-version toimintoja 1611"
description: "Jotkin organisaatiot Anna kirjauskansiot, joiden sisältämä yksi tosite, jossa on useampi kuin yksi asiakas tai toimittaja ja ne myös suorittaa myyntireskontran tai tilien ostoreskontran ulkomaanvaluutan uudelleenarvostuksen prosessi. Tässä ohjeaiheessa kuvataan vaiheet, jotka näiden organisaatioiden tulee kun ne päivitetään Microsoft Dynamics-365 version toiminnot 1611."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-28 16 - 04 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d42c753d0dc8b8efc2a0d2a26da32a4951d85503
ms.lasthandoff: 03/31/2017


---

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>Yksittäisen tositteen ja valuutan uudelleenarvostuksen päivittäminen Microsoft Dynamics-365-version toimintoja 1611

Jotkin organisaatiot Anna kirjauskansiot, joiden sisältämä yksi tosite, jossa on useampi kuin yksi asiakas tai toimittaja ja ne myös suorittaa myyntireskontran tai tilien ostoreskontran ulkomaanvaluutan uudelleenarvostuksen prosessi. Tässä ohjeaiheessa kuvataan vaiheet, jotka näiden organisaatioiden tulee kun ne päivitetään Microsoft Dynamics-365 version toiminnot 1611.

Toimi seuraavasti, kun päivität Microsoft Dynamics-365-version toimintoja 1611.

1.  Ennen kuin päivität Dynamics 365 operaatioille, Suorita ulkomaanvaluutan uudelleenarvostuksen prosessien Myyntireskontra ja Ostoreskontra. Määrittää **menetelmä** kentän arvoksi **laskun päivämäärä**. Uudelleenarvostustapahtuma luodaan, joka kumoaa edellisen ulkomaanvaluutan uudelleenarvostuksen. Siksi avoimet tapahtumat arvostetaan niiden alkuperäinen kirjanpitovaluutta.
2.  Päivitä työvaiheiden versio 1611 Dynamics 365.
3.  Myyntireskontran ja tilien ostoreskontran ulkomaanvaluutan uudelleenarvostuksen prosessit suorittaa uudelleen. Tällä hetkellä on määritetty **menetelmä** kentän arvoksi **Vakio**. Luodaan uusi Uudelleenarvostustapahtuma, joka perustuu nykyisten vaihtokurssien. Tämän tapahtuman tallentaa Realisoitumaton voitto/tappio ja yhteenveto oikean kirjanpitotilin.



