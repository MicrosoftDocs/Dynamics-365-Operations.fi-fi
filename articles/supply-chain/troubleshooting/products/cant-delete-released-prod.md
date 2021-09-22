---
title: Vapautettua tuotetta ei voi poistaa
description: Vapautetun tuotteen ja kaikki sen variantit voidaan poistaa vain, jos vapautetussa tuotteessa ei ole liittyviä tapahtumia.
author: SmithaNataraj
ms.date: 06/11/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f03d45a36401314a4b02ff354fabb474568c48b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476260"
---
# <a name="you-cant-delete-a-released-product"></a>Vapautettua tuotetta ei voi poistaa

## <a name="symptoms"></a>Oireet

Vapautetun tuotteen ja kaikki sen variantit voidaan poistaa vain, jos vapautetussa tuotteessa ei ole liittyviä tapahtumia.

## <a name="resolution"></a>Ratkaisu

Poista vapautettu tuote tai päätuote seuraavasti:

1. Sulje kaikki nimikkeiden avoimet tapahtumat.
1. Vähennä varaston arvoksi 0 (nolla).
1. Suorita varaston sulkeminen.
1. Poista kaikki poistettavan päätuotteen tuotevariantit.
