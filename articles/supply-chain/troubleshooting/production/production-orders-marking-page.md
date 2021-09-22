---
title: Tuotantotilaukset eivät näy Merkintä-sivulla
description: Merkintä-sivu ei näy kaikissa tuotantotilauksissa. Tässä aiheessa kuvataan kolme tuotemääritystä, jotka eivät ole käytettävissä merkitsemistä varten.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 87507e91d3feb2557e7ba771b8e34ff7ca105749
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476174"
---
# <a name="production-orders-arent-shown-on-the-marking-page"></a>Tuotantotilaukset eivät näy Merkintä-sivulla

## <a name="symptoms"></a>Oireet

Erillisvalmistuksen yhteydessä osa tuotantotilauksista ei näy **Merkintä**-sivulla.

## <a name="resolution"></a>Ratkaisu

Tuotteissa, joissa on seuraavat määritykset, ei voi käyttää merkintää. Niinpä **Merkintä**-sivu ei näy niissä:

- Tuotteet, jotka on määritetty *todellinen paino* -tyyppisiksi tuotteiksi.
- Edistykselliset varastoprosessit on otettu niissä käyttöön.
- Ne on määritetty hallittaviksi *standardikustannuksen* mukaisesti.
