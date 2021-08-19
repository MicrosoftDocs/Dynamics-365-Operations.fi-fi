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
ms.openlocfilehash: 6b4361682246397732e8326b98b1b86ff878664e54c8c352296b0d7eaff6bbbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719548"
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
