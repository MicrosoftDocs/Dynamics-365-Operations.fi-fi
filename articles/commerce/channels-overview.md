---
title: Kanavien yleiskatsaus
description: Tässä artikkelissa on yleiskatsaus Microsoft Dynamics 365 Commercen kanavista.
author: samjarawan
ms.date: 01/27/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: af5089f0065610873360b2e2883928a43600caa9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884634"
---
# <a name="channels-overview"></a>Kanavien yleiskatsaus


[!include [banner](includes/banner.md)]

Tässä artikkelissa on yleiskatsaus Microsoft Dynamics 365 Commercen kanavista. Siinä on tietoja tehtävistä, jotka on suoritettava ennen kunkin kanavan määrittämistä ja sen jälkeen.

## <a name="types-of-channels"></a>Kanavatyypit

Dynamics 365 Commerce tukee kolmea kanavatyyppiä: vähittäismyynti-, puhelinkeskus- ja verkkokanavaa.

### <a name="retail-channels"></a>Vähittäismyyntikanavat

Vähittäismyyntikanavat tarkoittavat perinteisiä myymälöitä. Jokaisella myymälällä voi olla omat myyntipisteiden kassakoneet, tulo- ja kulutilit sekä oma henkilökunta. 

### <a name="call-center-channels"></a>Puhelinkeskuskanavat

Puhelinkeskuskanavat tarkoittavat puhelinkeskustilauksia ja asiakashallintaa.

### <a name="online-channels"></a>Online-kanavat

Verkkokanavat tarkoittavat sähköisen kaupankäynnin verkkokauppoja. Kun verkkokanava luodaan, sivusto on luotava Microsoft Dynamics 365 Commercen sivuston muodostintyökalulla tai jollain kolmannen osapuolen sähköisellä kaupankäyntiratkaisulla.

## <a name="channel-setup-basics"></a>Kanavan määritysten perusteet

Kanava määritetään Commerce-työkalulla. Kullakin kanavalla on omat maksutavat, hintaryhmät, tuotehierarkiat, valikoimat ja tuoteryhmät. Kun kanava on luotu, kanavassa myytävät tuotteet on määritettävä. Kullakin kanavatyypillä on yksilöllinen toimintojoukko, joka on ehkä määritettävä. Esimerkiksi vähittäismyyntikanavassa on määritettävä työntekijöitä, kassakoneita ja asiakkaita. Kun uusi kanava on luotu, se on määritettävä organisaatiohierarkiaan.

## <a name="channel-setup-prerequisites"></a>Kanava-asetusten edellytykset

Ennen kanavan määrittämistä on suoritettava joitakin kanavatyypin mukaisia ennakkotehtäviä. Lisätietoja on kohdassa [Kanava-asetusten edellytykset](channels-prerequisites.md).

## <a name="set-up-a-channel"></a>Kanavan määrittäminen

Kun edeltävät tehtävät on suoritettu, saat lisätietoja määrityksistä seuraavista linkeistä.

- [Vähittäismyyntikanavan määrittäminen](channel-setup-retail.md)
- [Puhelinkeskuskanavan määrittäminen](channel-setup-callcenter.md)
- [Verkkokanavan määrittäminen](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a>Lisäresurssit

[Kanava-asetusten edellytykset](channels-prerequisites.md)

[Vähittäismyyntikanavan määrittäminen](channel-setup-retail.md)
    
[Verkkokanavan määrittäminen](channel-setup-online.md)

[Puhelinkeskuskanavan määrittäminen](channel-setup-callcenter.md)

[Organisaatiohierarkioiden määrittäminen](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]