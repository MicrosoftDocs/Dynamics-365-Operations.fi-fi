---
title: Luo online-toimintoprofiili
description: Tässä artikkelissa käsitellään verkkotoimintoprofiilin luontia Microsoft Dynamics 365 Commercessa.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 5ce81900cd0648132748167d03906afc64e97f25
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276798"
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
