---
title: Kauppasopimuksen valuuttamuunto-ongelmat
description: Kauppasopimusten hintoja ei lasketa uudelleen valuutan mukaan, kun valuutta on ostotilauksessa eri
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 1b6dc36c5f5ee6b611eebd81f378399ce1748c63
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476192"
---
# <a name="trade-agreement-currency-conversion-issues"></a>Kauppasopimuksen valuuttamuunto-ongelmat

## <a name="symptoms"></a>Oireet

Kauppasopimusten hintoja ei lasketa uudelleen valuutan mukaan, kun valuutta on ostotilauksessa eri.

## <a name="resolution"></a>Ratkaisu

*Yleinen valuutta* -toiminnon avulla voit määrittää hinnat ja alennukset vain yhdessä valuutassa. Tällöin voit muuntaa muihin valuuttoihin tarpeen mukaan. Lisäksi kun muunnos on tehty, toiminto voi automaattisesti käyttää taktista pyöristystä.
