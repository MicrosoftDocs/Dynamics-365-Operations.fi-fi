---
title: Kanavan määrittämisen edellytykset
description: Tässä artikkelissa on yleiskatsaus Microsoft Dynamics 365 Commercen kanava-asetusten edellytyksistä.
author: samjarawan
ms.date: 02/21/2020
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
ms.openlocfilehash: 98ca2dc4691534853467c1680890199d08bc4e79
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282292"
---
# <a name="channel-setup-prerequisites"></a>Kanavan määrittämisen edellytykset

[!include [banner](includes/banner.md)]

Tässä artikkelissa on yleiskatsaus Microsoft Dynamics 365 Commercen kanava-asetusten edellytyksistä.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
