---
title: "Konsolidointitiliryhmät ja lisäkonsolidointitilit"
description: "Tässä ohjeaiheessa on tietoja konsolidointitiliryhmistä ja lisäkonsolidointitileistä. Siinä kerrotaan myös, miten niitä käytetään Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa."
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4fcdaa26eb2f15bbf6f7d80bd59a54899f637a2c
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

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


Lisätietoja on ohjeaiheessa [Konsolidaatioryhmien ja lisäkonsolidaatiotilien luominen](../general-ledger/tasks/create-consolidation-groups.md) 




