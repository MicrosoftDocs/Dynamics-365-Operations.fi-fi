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
ms.openlocfilehash: 46523c55f4fd42b0985397752f0c62a3e1a55e177f2308e20b7064e339758269
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742025"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Viimeinen testauspäivämäärä -kenttää ei päivitetä, kun useita laatutilauksia luodaan

Tietopankin numero: 4612803

## <a name="symptoms"></a>Oireet

**Viimeinen testauspäivämäärä** -kenttää ei päivitetä, kun useita laatutilauksia luodaan.

## <a name="resolution"></a>Ratkaisu

Järjestelmä käyttäytyy suunnitellulla tavalla. Viimeinen testauspäivämäärä ei liity laatutilauksiin. Se tallentaa päivämäärän, jolloin valmiit tavarat on ensin ostettu tai valmistettu. Tätä päivämäärää käytetään suositeltavan säilyvyysajan laskemiseen.
