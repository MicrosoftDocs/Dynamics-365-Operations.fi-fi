---
title: Kuljetustenhallinnan numerosarja
description: Tässä artikkelissa käsitellään kuljetustenhallinnan numerosarjojen määrittämistä.
author: Weijiesa
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2a1d3e1a36164215b70d88b10beb35748be2e23b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847814"
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