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
ms.openlocfilehash: ac15eba28d777017e8a4f34ff16ec4ea8a1d645222f218aa5024d98ac547b3e5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753201"
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