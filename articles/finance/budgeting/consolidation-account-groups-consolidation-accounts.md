---
title: Konsolidointitiliryhmät ja lisäkonsolidointitilit
description: Tässä ohjeaiheessa on tietoja konsolidointitiliryhmistä ja lisäkonsolidointitileistä ja siinä kerrotaan, kuinka niitä käytetään Microsoft Dynamics 365 Financessa.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8db7a60656434aafd8114b08c2c0e9493140f27b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442891"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Konsolidointitiliryhmät ja lisäkonsolidointitilit

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja konsolidointitiliryhmistä ja lisäkonsolidointitileistä ja siinä kerrotaan, kuinka niitä käytetään Microsoft Dynamics 365 Financessa.

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



