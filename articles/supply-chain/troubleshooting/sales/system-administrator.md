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
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026490"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a>Järjestelmänvalvojat eivät voi poistaa tilausten pitoja, koska heillä ei ole valtuuksia

Tietopankin numero: 4614642

## <a name="symptoms"></a>Oireet

Järjestelmänvalvojat eivät voi poistaa myyntitilausten pitoja, ellei heillä ole tilauksen järjestyskoodissa määritettyä roolia.

## <a name="resolution"></a>Ratkaisu

Joidenkin toimien, kuten myyntitilauksen pitojen poistamisen, käyttö perustuu liiketoimintakäytännön määritykseen. Järjestelmänvalvojilla ei yleensä ole valtuuksia tämäntyyppisten toimintojen suorittamiseen. 

Yleensä tietyn tehtävän suorittamiseen sovelletaan liiketoimintakäytäntöjä, ja vain organisaation tietyt henkilöt hyväksytään suorittamaan tämä tehtävä. Esimerkkejä tällaisista ovat työnkulun hyväksynnän tuloksena tehtävät hyväksynnät sekä työnkulun konfiguraation tuloksena olevat tehtävät.

Vaikka tilausten pitoon ei ole liitetty työnkulkua, periaate on samanlainen. Asianmukainen rooli määrittää organisaation tietyn henkilöryhmän, jolla on oikeus poistaa tilausten pito. Tätä oikeutta ei välttämättä pidä myöntää kaikille järjestelmänvalvojille, koska se rikkoo määritettyä liiketoimintakäytäntöä.
