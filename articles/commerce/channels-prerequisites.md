---
title: Kanava-asetusten edellytykset
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen kanava-asetusten edellytyksistä.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002286"
---
# <a name="channel-setup-prerequisites"></a>Kanava-asetusten edellytykset


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen kanava-asetusten edellytyksistä.

## <a name="overview"></a>Yleiskatsaus

Ennen Dynamics 365 Commerce -kanavan luontia on suoritettava useita ennakkoedellytystehtäviä. Seuraava edellytysten tehtäväluettelo on organisoitu kanavatyypin mukaan.

> [!NOTE]
> Osaa ohjeistuksesta kirjoitetaan edelleen ja linkit päivitetään, kun uutta sisältöä julkaistaan.

## <a name="initialization"></a>Alustus

- [Alkutietojen alustaminen](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Kaikissa kanavatyypeissä tarvittavat yleiset edellytykset

- [Yrityksen rakenteen määrittäminen ja asetusten määrittäminen](channels-legal-entities.md) 
- [Organisaatiohierarkian asetusten määrittäminen](channels-org-hierarchies.md)
- [Varaston määrittäminen](channels-setup-warehouse.md)
- [Arvonlisäveron määrittäminen](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [Sähköpostin ilmoitusprofiilin määrittäminen](email-notification-profiles.md)
- [Numerosarjojen määrittäminen](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [Oletusasiakkaan ja -osoitekirjan määrittäminen](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Vähittäismyyntikanavan edellytykset

- [Tietokoodit ja tietokoodiryhmät](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [Vähittäismyynnin toimintoprofiilin määrittäminen](retail-functionality-profile.md)
- [Työntekijän osoitekirjan määrittäminen](new-address-book.md)
- [Aseta näyttöpohja](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [Laiteaseman määrittäminen](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a>Puhelinkeskuskanavan edellytykset

- Puhelinkeskuksen parametrit
- Puhelinkeskuksen palautusmenetelmät
- Vuokratyypit
- Maksupalvelut
- Tilauksen pitokoodit

## <a name="online-channel-prerequisites"></a>Verkkokanavan edellytykset

- [Verkkotoimintoprofiilin luominen](online-functionality-profile.md)

## <a name="additional-resources"></a>Lisäresurssit

[Kanavien yleiskatsaus](channels-overview.md)

[Organisaatiot ja organisaatiohierarkiat – yleiskatsaus](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organisaatiohierarkioiden määrittäminen](channels-org-hierarchies.md)

[Yritysten luominen](channels-legal-entities.md)

[Vähittäismyyntikanavan määrittäminen](channel-setup-retail.md)
    
[Verkkokanavan määrittäminen](channel-setup-online.md)
