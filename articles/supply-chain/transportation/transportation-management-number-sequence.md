---
title: Kuljetustenhallinnan numerosarja
description: Tässä aiheessa käsitellään kuljetustenhallinnan numerosarjojen määrittämistä.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3da757cbf47e0e1af781b720d17a673e19aeb3b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807677"
---
# <a name="transportation-management-number-sequence"></a>Kuljetustenhallinnan numerosarja

[!include [banner](../includes/banner.md)]

Määritä erilaiset tuotenumerot kuljetustenhallintamoduulin **Numerosarjat**-sivulla. Rahdinkuljettajat käyttävät tuotenumeroita kunkin lähetyksen organisointiin ja seurantaan.

## <a name="create-a-number-sequence-for-a-pro-number"></a>Valmistenumeron numerosarjan luominen

Valmistenumeron numerosarja luodaan seuraavasti:

1. Valitse **Kuljetustenhallinta \> Asetukset \> Rahdinkuljettajat \> Numerosarjat**.
1. Luo uusi numerosarja valitsemalla **Uusi**.
1. Anna numerosarjalle yksilöivä tunnus ja kuvaava nimi.
1. **Numerosarjan tyyppi** -kentän ainoa vaihtoehto on *Tuotenumero*.
1. **Tarkistusnumero**-kentän ainoa vaihtoehto on *Tarkistusnumero*, ja se on määritetty yleisenä laskentana.
1. Anna järjestyksen tiedot **Järjestys**-pikavälilehdessä.
1. Sulje sivu.

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a>Numerosarjan linkittäminen lähetyksen rahdinkuljettajaan

Numerosarja linkitetään rahdinkuljettajaan seuraavasti:

1. Valitse **Kuljetustenhallinta \> Asetukset \> Rahdinkuljettajat \> Lähetyksen rahdinkuljettajat**.
1. Valitse lähetyksen rahdinkuljettaja.
1. Valitse **Muokkaa**.
1. Valitse **Yleiskatsaus**-pikavälilehdessä **Tuotenumerosarja**-kentässä vaihtoehto.
1. Sulje sivu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]