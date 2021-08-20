---
title: Painon on oltava positiivinen
description: Painon on oltava positiivinen
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 27ec37e0c0644ff10ece4626d5c136bca3c52ef12f1c6de947afd03003a5368a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776773"
---
# <a name="weight-must-be-positive"></a>Painon on oltava positiivinen

Virhekoodi: WeightMustBePositive

## <a name="symptoms"></a>Oireet

Järjestelmä näyttää seuraavan virhesanoman:

> Painon on oltava positiivinen.

## <a name="cause"></a>Syy

**Bruttopaino**-kentän arvoksi määritetään *0* (nolla) tai negatiivinen arvo.

## <a name="resolution"></a>Ratkaisu

Jos haluat määrittää painon, seuraa jotakin näistä vaiheista.

- Määritä arvo **Bruttopaino**-kentässä. Valitse sitten yksikkö avattavasta luettelosta.
- Valitse **Hae järjestelmän paino** laskeaksesi **Bruttopaino**-arvon.
