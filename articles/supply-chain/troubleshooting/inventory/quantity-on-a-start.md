---
title: Aloitetun karanteenitilauksen määrää ei päivitetä, kun tilaus jaetaan
description: Kun luot karanteenitilauksen ja yrität jakaa sen, tilauksen määrää ei päivitetä jaetun jäljellä olevan määrän mukaan.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026486"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Aloitetun karanteenitilauksen määrää ei päivitetä, kun tilaus jaetaan

Tietopankin numero: 4613113

## <a name="symptoms"></a>Oireet

Kun luot karanteenitilauksen ja yrität jakaa sen, tilauksen määrää ei päivitetä jaetun jäljellä olevan määrän mukaan jaon jälkeen.

## <a name="resolution"></a>Ratkaisu

Järjestelmä ei muuta karanteenitilauksen alkuperäistä määrää, jotta voit seurata karanteenitilauksen alkuperäistä määrää. Järjestelmä seuraa kuitenkin karanteenitilauksesta jaettua määrää. Tätä seurantaa varten se käyttää tietokantakenttää, jonka nimi on `QuantityThatHasSplitIntoOtherQuarantineOrders`. Tämä kenttä ei kuitenkaan näy käyttöliittymässä.
