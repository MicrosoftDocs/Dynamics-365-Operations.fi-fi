---
title: Työtä ei ole estetty
description: Työtä ei ole estetty
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924201"
---
# <a name="work-isnt-blocked"></a>Työtä ei ole estetty

Virhekoodi: WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>Oireet

Järjestelmä näyttää seuraavan virhesanoman:

> Työtä tunnuksella %1 ei ole estetty.

## <a name="cause"></a>Syy

**Estetty aalto** -asetuksen arvo aallossa on *Ei*. Työn estoa ei voi poistaa, koska se ei ole estettynä.

## <a name="resolution"></a>Ratkaisu

 Vain työn, jonka **Estetty aalto** -asetuksen arvona on *Kyllä*, esto voidaan poistaa.
