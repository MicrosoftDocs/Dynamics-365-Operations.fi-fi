---
title: Keräysluettelon kirjauskansion varastoa ei päivitetä tuoterakennerivillä.
description: Keräysluettelon kirjauskansion varastoa ei päivitetä tuoterakennerivillä.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5d24c0b8538f3894fd1d2a3edb3a6ed8633c9609
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026464"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>Keräysluettelon kirjauskansion varastoa ei päivitetä tuoterakennerivillä

Tietopankin numero: 4614848

## <a name="symptoms"></a>Oireet

Keräysluettelon kirjauskansion varastoa ei päivitetä tuoterakennerivillä.

## <a name="resolution"></a>Ratkaisu

Järjestelmä käyttäytyy suunnitellulla tavalla. Jos keräysluettelon kirjauskansiorivi on luotu ja siinä on viite (erän tunnuksen kautta) tuotannon tuoterakenneriviin, tuotannon tuoterakennerivin varastoa ei päivitetä, jos tuotannon keräysluettelon kirjauskansiorivin varastodimensiota muutetaan myöhemmin.
