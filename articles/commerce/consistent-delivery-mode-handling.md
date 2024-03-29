---
title: Ota käyttöön yhdenmukainen toimitustilan käsittely sähköisen kaupankäynnin kanavissa
description: Tässä artikkelissa kuvataan, kuinka yhdenmukainen toimitustavan käsittely otetaan käyttöön, jotta voidaan käsitellä mahdollisia Microsoft Dynamics 365 Commercen sähköisen kaupan kanavien kulutyönkulkuihin liittyviä ongelmia.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 43450c9d380bd57c234bb1c9acfbe296ab115f14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279647"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Ota käyttöön yhdenmukainen toimitustilan käsittely sähköisen kaupankäynnin kanavissa 

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka yhdenmukainen toimitustavan käsittely otetaan käyttöön, jotta voidaan käsitellä mahdollisia Microsoft Dynamics 365 Commercen sähköisen kaupan kanavien kulutyönkulkuihin liittyviä ongelmia.

Dynamics 365 Commercessa ei-luokiteltuja otsikkotason maksuja ei oletusarvoisesti sovelleta sähköisen kaupan kanavissa. Tämä saattaa aiheuttaa verkkokaupan kanavaan yhden tai molemmat seuraavista ongelmista:

- Ei-luokiteltuja otsikkotason veloituksia ei tule näkyviin.
- Toimitustapojen veloitukset eivät ole yhdenmukaisia toimitustavan valinnan ja uloskuittauksen tilausyhteenvedon välillä.

Voit korjata nämä ongelmat ottamalla käyttöön **Ota käyttöön yhdenmukainen toimitustilan käsittely kanavassa** -ominaisuus. Tämän ominaisuuden avulla voit varmistaa, että ei-luokitellut otsikkotason kulut näkyvät sähköisen kaupan kanavissa ja että myyntitilauksen toimitustiedot käsitellään yhdenmukaisesti samassa pyyntötyönkulussa.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Ota käyttöön Ota käyttöön yhdenmukainen toimitustilan käsittely kanavassa -ominaisuus

Ota **Ota käyttöön yhdenmukainen toimitustilan käsittely kanavassa** -ominaisuus käyttöön Commerce Headquartersissa noudattamalla seuraavia ohjeita.

1. Avaa **Ominaisuuksien hallinta** -työtila (**Järjestelmän hallinta \> Työtilat \> Ominaisuuksien hallinta**).
1. Etsi käytettävissä olevien ominaisuuksien luettelosta ja valitse **Ota käyttöön yhdenmukainen toimitustilan käsittely kanavassa**.
1. Valitse oikeanpuoleisesta ruudusta **Ota käyttöön nyt**.
