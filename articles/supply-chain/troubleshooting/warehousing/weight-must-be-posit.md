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
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924300"
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
