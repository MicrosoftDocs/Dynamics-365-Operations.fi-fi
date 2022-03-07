---
title: Valmiiksi ilmoittamisen peruuttaminen luo odottamattoman avoimen tapahtuman
description: Valmiiksi ilmoittamisen peruutus, jossa on merkintä, luo avoimen tapahtuman, jossa peruutetulla määrällä on samat varastodimensiot kuin peruutetulla tapahtumalla.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026485"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Valmiiksi ilmoittamisen peruuttaminen luo odottamattoman avoimen tapahtuman

Tietopankin numero: 4612469

## <a name="symptoms"></a>Oireet

Jos peruutat valmiiksi ilmoittamisen, jossa on merkintä, järjestelmä luo avoimen tapahtuman, jossa peruutetulla määrällä on samat varastodimensiot kuin peruutetulla tapahtumalla.

## <a name="resolution"></a>Ratkaisu

Kun peruutat valmiiksi ilmoittamistoiminnon, varastodimensio alustetaan tuotantokirjauskansiosta. Näin ollen se saa eränumeron. Merkinnän vuoksi myyntitilaustapahtumat perivät eränumeron.

Dimension voi nollata, kun valmiiksi ilmoittaminen kirjataan.
