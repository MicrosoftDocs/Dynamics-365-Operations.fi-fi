---
title: Viimeinen testauspäivämäärä -kenttää ei päivitetä, kun useita laatutilauksia luodaan
description: Viimeinen testauspäivämäärä -kenttää ei päivitetä, kun useita laatutilauksia luodaan.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026484"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Viimeinen testauspäivämäärä -kenttää ei päivitetä, kun useita laatutilauksia luodaan

Tietopankin numero: 4612803

## <a name="symptoms"></a>Oireet

**Viimeinen testauspäivämäärä** -kenttää ei päivitetä, kun useita laatutilauksia luodaan.

## <a name="resolution"></a>Ratkaisu

Järjestelmä käyttäytyy suunnitellulla tavalla. Viimeinen testauspäivämäärä ei liity laatutilauksiin. Se tallentaa päivämäärän, jolloin valmiit tavarat on ensin ostettu tai valmistettu. Tätä päivämäärää käytetään suositeltavan säilyvyysajan laskemiseen.
