---
title: Kuljetustenhallinnan numerosarja
description: Tässä aiheessa käsitellään kuljetustenhallinnan numerosarjojen määrittämistä.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2c3f087ac76412cd2dce93dcb31b796ce2cb3bc4
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/29/2020
ms.locfileid: "4427537"
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
