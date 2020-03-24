---
title: Kanava-asetusten edellytykset
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen kanava-asetusten edellytyksistä.
author: samjarawan
manager: annbe
ms.date: 02/21/2020
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
ms.openlocfilehash: 0da0457240cf12686fff2fa929c7fb510c11f242
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113779"
---
# <a name="channel-setup-prerequisites"></a>Kanava-asetusten edellytykset


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen kanava-asetusten edellytyksistä.

## <a name="overview"></a>Yleiskatsaus

Ennen Dynamics 365 Commerce -kanavan luontia on suoritettava useita ennakkoedellytystehtäviä. Seuraava edellytysten tehtäväluettelo on organisoitu kanavatyypin mukaan.

> [!NOTE]
> Osaa ohjeistuksesta kirjoitetaan edelleen ja linkit päivitetään, kun uutta sisältöä julkaistaan.

## <a name="initialization"></a>Alustus

- [Alkutietojen alustaminen](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Kaikissa kanavatyypeissä tarvittavat yleiset edellytykset

- [Yrityksen rakenteen määrittäminen ja asetusten määrittäminen](channels-legal-entities.md) 
- [Organisaatiohierarkian asetusten määrittäminen](channels-org-hierarchies.md)
- [Varaston määrittäminen](channels-setup-warehouse.md)
- [Arvonlisäveron määrittäminen](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [Sähköpostin ilmoitusprofiilin määrittäminen](email-notification-profiles.md)
- [Numerosarjojen määrittäminen](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [Oletusasiakkaan ja -osoitekirjan määrittäminen](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Vähittäismyyntikanavan edellytykset

- [Tietokoodit ja tietokoodiryhmät](info-codes-retail.md)
- [Vähittäismyynnin toimintoprofiilin määrittäminen](retail-functionality-profile.md)
- [Työntekijän osoitekirjan määrittäminen](new-address-book.md)
- [Aseta näyttöpohja](pos-screen-layouts.md)
- [Laiteaseman määrittäminen](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a>Puhelinkeskuskanavan edellytykset

- Puhelinkeskuksen parametrit
- [Puhelinkeskuksen tilaus- ja maksunpalautusmenetelmät](work-with-payments.md)
- [Puhelinkeskuksen toimitustilat ja kulut](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a>Online-kanavan edellytykset

- [Luo online-toimintoprofiili](online-functionality-profile.md)

## <a name="additional-resources"></a>Lisäresurssit

[Kanavien yleiskatsaus](channels-overview.md)

[Organisaatiot ja organisaatiohierarkiat – yleiskatsaus](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organisaatiohierarkioiden määrittäminen](channels-org-hierarchies.md)

[Yritysten luominen](channels-legal-entities.md)

[Vähittäismyyntikanavan määrittäminen](channel-setup-retail.md)
    
[Verkkokanavan määrittäminen](channel-setup-online.md)
