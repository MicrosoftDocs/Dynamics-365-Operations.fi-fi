---
title: Konsolidointitiliryhmät ja lisäkonsolidointitilit
description: Tässä ohjeaiheessa on tietoja konsolidointitiliryhmistä ja lisäkonsolidointitileistä ja siinä kerrotaan, kuinka niitä käytetään Microsoft Dynamics 365 Financessa.
author: aprilolson
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3e6671e5f3ceff671210011913a3a91194613c7c0e4e1d8e8063e4e27e5f3cf5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727417"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Konsolidointitiliryhmät ja lisäkonsolidointitilit

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja konsolidointitiliryhmistä ja lisäkonsolidointitileistä ja siinä kerrotaan, kuinka niitä käytetään Microsoft Dynamics 365 Financessa.

## <a name="consolidation-account-groups"></a>Konsolidointitiliryhmät

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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]