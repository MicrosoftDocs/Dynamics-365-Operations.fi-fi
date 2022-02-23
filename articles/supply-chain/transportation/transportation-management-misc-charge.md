---
title: Kuljetustenhallinnan muut kulut
description: Tässä aiheessa käsitellään kuljetuksesta syntyviä kuluja, joihin on liitettävä kulukoodi
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2b703d770c7f9ea684716368cf1e7dbe5fec8710
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/29/2020
ms.locfileid: "4427543"
---
# <a name="transportation-management-miscellaneous-charges"></a>Kuljetustenhallinnan muut kulut

[!include [banner](../includes/banner.md)]

Muiden kulujen tavoin kuljetuksesta syntyviin kuluihin on liitettävä kulukoodi. Muussa tapauksessa niitä ei lisätä takaisin tilaukseen muina kuluina. **Kulujen koodi** määrittää, miten kulut käsitellään suhteessa tilaukseen ja tilausriviin, jossa se lisättiin.

Valitsemalla **Kuljetuksenhallinta > Määritys > Luokitus > Muut kulut** voit määrittää ehdot, joiden mukaan määritetään, milloin **kulujen koodia** käytetään kuluun.

Kullekin sopivalle **Kulumoduuli**-asetukselle (*Asiakas* ja *Toimittaja*) on oltava vähintään yksi määritys, jossa **Muun kulun tyyppi** -asetuksena on *Ei mitään*. Jos tämä puuttuu, muuta kulua *ei* lisätä tilaukseen.
