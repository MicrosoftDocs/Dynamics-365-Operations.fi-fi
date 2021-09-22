---
title: Sama kauppasopimus valitaan, kun luodaan myyntitilausrivejä
description: Jos tietylle päivälle on määritetty useita kauppasopimuksia, valitaan aina matalimman hinnan kauppasopimus, kun luodaan myyntitilausrivejä.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a586a399fb349965b972191bec1271651bec5fcb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476233"
---
# <a name="if-two-trade-agreements-exist-for-overlapping-dates-the-same-one-is-always-selected"></a>Jos päällekkäisille päivämäärille on kaksi kauppasopimusta, sama valitaan aina

## <a name="symptoms"></a>Oireet

Jos samalle jaksolle tai päällekkäisille jakosoille on määritetty kaksi kauppasopimusta, vaikuttaa siltä, että sama kauppasopimus valitaan aina, kun luodaan asianomaisia nimikkeitä sisältäviä myyntitilausrivejä.

## <a name="resolution"></a>Ratkaisu

Jos tietylle päivälle on useita kauppasopimuksia, valitaan aina matalimman hinnan kauppasopimus. Lisä tietoja saat lataamalla seuraavan teknisen raportin: [Kauppasopimukset Microsoft Dynamics AX 2012:ssa](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).
