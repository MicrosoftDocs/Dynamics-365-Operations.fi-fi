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
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b7bb6c9338808828a41801a85a1b93b420e9c75b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004731"
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
