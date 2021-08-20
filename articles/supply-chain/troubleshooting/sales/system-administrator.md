---
title: Järjestelmänvalvojat eivät voi poistaa tilausten pitoja, koska heillä ei ole valtuuksia
description: Järjestelmänvalvojat eivät voi poistaa tilausten pitoja, koska heillä ei ole valtuuksia.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0d0fbcc111d77ae1a362984033216f5973e2bc74f2ee95947b662ef60a13d83e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750903"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a>Järjestelmänvalvojat eivät voi poistaa tilausten pitoja, koska heillä ei ole valtuuksia

Tietopankin numero: 4614642

## <a name="symptoms"></a>Oireet

Järjestelmänvalvojat eivät voi poistaa myyntitilausten pitoja, ellei heillä ole tilauksen järjestyskoodissa määritettyä roolia.

## <a name="resolution"></a>Ratkaisu

Joidenkin toimien, kuten myyntitilauksen pitojen poistamisen, käyttö perustuu liiketoimintakäytännön määritykseen. Järjestelmänvalvojilla ei yleensä ole valtuuksia tämäntyyppisten toimintojen suorittamiseen. 

Yleensä tietyn tehtävän suorittamiseen sovelletaan liiketoimintakäytäntöjä, ja vain organisaation tietyt henkilöt hyväksytään suorittamaan tämä tehtävä. Esimerkkejä tällaisista ovat työnkulun hyväksynnän tuloksena tehtävät hyväksynnät sekä työnkulun konfiguraation tuloksena olevat tehtävät.

Vaikka tilausten pitoon ei ole liitetty työnkulkua, periaate on samanlainen. Asianmukainen rooli määrittää organisaation tietyn henkilöryhmän, jolla on oikeus poistaa tilausten pito. Tätä oikeutta ei välttämättä pidä myöntää kaikille järjestelmänvalvojille, koska se rikkoo määritettyä liiketoimintakäytäntöä.
