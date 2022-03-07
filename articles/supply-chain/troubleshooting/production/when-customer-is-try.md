---
title: Eränumero tyhjennetään, kun uusi erätunnus valitaan
description: Kun tarkastelet keräysluettelon kirjauskansioriviä, Eränumero-kentän arvo poistetaan, jos valitset uuden arvon Erätunnus-kentästä.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026458"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>Eränumero tyhjennetään, kun uusi erätunnus valitaan

Tietopankin numero: 4613107

## <a name="symptoms"></a>Oireet

Kun tarkastelet keräysluettelon kirjauskansioriviä, **Eränumero**-kentän arvo poistetaan, jos valitset uuden arvon **Erätunnus**-kentästä.

## <a name="resolution"></a>Ratkaisu

Järjestelmä käyttäytyy suunnitellulla tavalla. Jos muutat erätunnuksen, muutat nimikekontekstia. Näin ollen eränumero nollataan.

Jos haluat liittää eränumeron erätunnukseen, erätunnus on määritettävä ensin.
