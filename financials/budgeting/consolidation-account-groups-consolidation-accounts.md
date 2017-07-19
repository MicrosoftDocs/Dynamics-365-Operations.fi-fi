---
title: "Konsolidointitiliryhmät ja lisäkonsolidointitilit"
description: "Tässä ohjeaiheessa on tietoja konsolidointitiliryhmistä ja lisäkonsolidointitileistä. Siinä kerrotaan myös, miten niitä käytetään Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa."
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 835669de01deb1ba0dcc5752d9d6d8f498e6ff7d
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Konsolidointitiliryhmät ja lisäkonsolidointitilit

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa on tietoja konsolidointitiliryhmistä ja lisäkonsolidointitileistä. Siinä kerrotaan myös, miten niitä käytetään Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa.

<a name="consolidation-account-groups"></a>Konsolidointitiliryhmät
----------------------------

Konsolidointitiliryhmien avulla voit luoda tiliryhmiä, joita haluat käyttää tietojen konsolidointiin. Useimmiten konsolidointitiliryhmä vastaa hallituksen määräämää tilikarttaa tai yhdistää tilit ryhmään, joka on määritetty yrityksen pääkonttorissa. Löydät konsolidoinnin tiliryhmät **Konsolidoinnit**-moduulin **Määritys**-alueelta. Kun lisäät uuden ryhmän, kirjoita tiliryhmän yksilöivä tunnus sekä nimi.

## <a name="additional-consolidation-accounts"></a>Lisäkonsolidointitilit
Lisäkonsolidointitilien avulla voit liittää tilin aiemmin luodusta tilikartasta konsolidoinnin tiliryhmään. Sitten voit määrittää konsolidointitilin arvon ja nimen. 

Löydät konsolidoinnin lisätiliryhmät **Konsolidoinnit**-moduulin **Määritys**-alueelta. Kun luot uuden konsolidointitilin, sinun on määritettävä seuraavat tiedot:

-   **Päätili** – kenttä on valinta, joka näyttää kaikki päätilit, jotka perustuvat tilikarttaan, jonka valitsit sivulla. Kun valitset tilin, sen nimi syötetään automaattisesti **Päätilin nimi** -kenttään.
-   **Konsolidointitiliryhmä** – Tämän kentän avulla voit määrittää ryhmän, johon tili määritetään. Jos konsolidoit kahdella eri tavalla, sama tili pitää lisätä kaikkiin neljään konsolidointitiliryhmään.
-   **Konsolidointitili** – Anna konsolidointitilin arvo. Tämän arvon ei tarvitse olla tilikartan tili. Se voi olla mikä tahansa arvo, jota tarvitset.
-   **Konsolidointitilin nimi** – Kirjoita tilin nimi muodossa, jossa haluat sen näkyvän kyselyissä ja raporteissa.
-   **SAT-taso** – tätä kenttää käytetään ilmoittamaan tiliotteet Meksikon veroviranomaisille. 

Kun olet luonut konsolidointitiliryhmät ja lisäkonsolidointilit, voit valita ryhmän Konsolidoi verkossa -prosessissa.





