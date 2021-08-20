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
ms.openlocfilehash: 970930bbdd30b57a8374de7810bb3ece8cb19a7010b5ef19d90bfc39d09f172b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740548"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>Keräysluettelon kirjauskansion varastoa ei päivitetä tuoterakennerivillä

Tietopankin numero: 4614848

## <a name="symptoms"></a>Oireet

Keräysluettelon kirjauskansion varastoa ei päivitetä tuoterakennerivillä.

## <a name="resolution"></a>Ratkaisu

Järjestelmä käyttäytyy suunnitellulla tavalla. Jos keräysluettelon kirjauskansiorivi on luotu ja siinä on viite (erän tunnuksen kautta) tuotannon tuoterakenneriviin, tuotannon tuoterakennerivin varastoa ei päivitetä, jos tuotannon keräysluettelon kirjauskansiorivin varastodimensiota muutetaan myöhemmin.
