---
title: Luo online-toimintoprofiili
description: Tässä artikkelissa käsitellään verkkotoimintoprofiilin luontia Microsoft Dynamics 365 Commercessa.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 686bc6440c31f3a4d729f2d92e3e57a1cc7b641f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895423"
---
# <a name="create-an-online-functionality-profile"></a>Luo online-toimintoprofiili

[!include [banner](includes/banner.md)]

Tässä artikkelissa on yleiskatsaus Microsoft Dynamics 365 Commercen online-toimintoprofiilin määrittämiseen.

Online-toimintojen profiilissa on erilaisia online-kanavien asetuksia. Kunkin online-kanavan on määritettävä online-toimintoprofiili.

## <a name="create-an-online-functionality-profile"></a>Verkkotoimintoprofiilin luominen

Seuraavassa kuvataan, miten online-toimintoprofiili luodaan Commerce Headquarters -sovelluksesta.

1. Siirry siirtymisruudussa kohtaan **Moduulit \> Kanavan määritys \> Verkkokaupan määritys \> Toimintoprofiilit**.
1. Valitse toimintoruudussa **Uusi**.
1. Kirjoita **Profiili**-kenttään nimi profiilille.
1. Kirjoita **Kuvaus**-kenttään arvo (Adventure Works -profiili alla olevaan esimerkkikuvaan).
1. Muokkaa **Toiminnot**-osassa **OSTOSKÄRRYÄ**, **VÄHITTÄISMYYNTIASIAKKAITA** tai **KASSALLE**-asetuksia tarpeen mukaan.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa on esimerkki verkkotoimintoprofiilista.
  
![Verkon toimintoprofiiliesimerkki.](media/online-functionality-profile.png)

## <a name="functions"></a>Funktiot

- **Koostetuotteet**: Kun tämä toiminto on käytössä, ostoskärry voi päivittää määrän, kun sama nimike lisätään useita kertoja.
- **Salli uloskuittaus ilman maksuja**: Kun tämä toiminto on käytössä, se käsittelee skenaarion, kun ostoskärryyn lisätyistä nimikkeistä veloitetaan hinta 0,00 $.
- **Luo asiakas asynkronisessa tilassa**: Tämä on kolmannen osapuolen sähköisen kaupankäynnin kanaviin sovellettava perintöasetus, eikä se koske Dynamics 365 -verkkokauppasivustoa.

## <a name="additional-resources"></a>Lisäresurssit

[Kanavien yleiskatsaus](channels-overview.md)

[Kanava-asetusten edellytykset](channels-prerequisites.md)

[Verkkokanavan määrittäminen](channel-setup-online.md)

[Vähittäismyyntikanavan määrittäminen](channel-setup-retail.md)

[Puhelinkeskuskanavan määrittäminen](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
