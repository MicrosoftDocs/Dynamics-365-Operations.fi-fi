---
title: Asynkroninen asiakkaan luontitila – Usein kysytyt kysymykset
description: Tässä artikkelissa on vastauksia Microsoft Dynamics 365 Commercen asynkronisen asiakkaan luontitilan usein kysyttyihin kysymyksiin.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: bd5741aeb3278f1d40d63bb02ca57571a907dc21
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474066"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>Asynkroninen asiakkaan luontitila – Usein kysytyt kysymykset

[!include [banner](includes/banner.md)]

Tässä artikkelissa on vastauksia Microsoft Dynamics 365 Commercen asynkronisen asiakkaan luontitilan usein kysyttyihin kysymyksiin.

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>Miksi en voi ottaa käyttöön Ota käyttöön asiakkaiden muokkaaminen asynkronisessa tilassa -ominaisuutta?

Seuraavat toiminnot on otettava käyttöön ennen **Ota käyttöön asiakkaiden muokkaaminen asynkronisessa tilassa** -ominaisuuden ottamista käyttöön:

- Asiakastilausten ja -tapahtumien suorituskyvyn parannukset
- Ota käyttöön laajennettu asynkronisen asiakkaan luonti
- Asynkronisen luomisen käyttöönotto asiakkaan osoitteissa

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>Miksi Commerce headquartersiin tehdyt reaaliaikaiset palvelukutsut ovat yhä käytettävissä, kun Ota käyttöön asiakkaiden muokkaaminen asynkronisessa tilassa -ominaisuus on otettu käyttöön?

Tämä ongelma ilmenee, kun Commerce Data Exchange (CDX) -töitä ei ole suoritettu, jotta kohteen tila ja muut kanavan metatiedot synkronoidaan kanavan kanssa. Varmista ennen skenaarion uudelleenyritystä, että seuraavat CDX-työt suoritetaan Commerce headquartersissa:

- 1110 (Yleinen konfiguraatio)
- 1010 (Asiakkaat)
- 1070 (Kanavan konfigurointi)

Commerce Scale Unitin (CSU) välimuistiin tallennetut tiedot eivät ehkä näy heti Commerce headquartersissa, kun CDX-työt on suoritettu.

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>Miksi Commerce headquarters ei näytä asiakkaan luontia tai päivityksiä myyntipisteestä (POS) tai sähköisen kaupankäyntiä kanavan kautta?

Varmista, että seuraavat toimenpiteet on suoritettu siinä järjestyksessä, jossa ne on lueteltu tässä.

1. Suorita CDX P-työ Commerce headquartersissa, jotta asynkronisten asiakkaiden tiedot tallennetaan **RETAILASYNCCUSTOMERV2**-, **RETAILASYNCADDRESSV2**-, **RETAILASYNCCUSTOMERCONTACT**-, **RETAILASYNCCUSTOMERAFFILIATION**- ja **RETAILASYNCCUSTOMERATTRIBUTEV2**-taulukkoihin Commerce headquartersissa.
1. Suorita **Synkronoi asiakkaat ja kanavapyynnöt** -erätyö Commerce headquartersissa. Kun erätyö on suoritettu onnistuneesti, kaikkien aiemmin mainituista taulukoista suoritettujen tietueiden **OnlineOperationCompleted**-kentän arvoksi määritetään **1**.
