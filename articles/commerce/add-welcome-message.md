---
title: Tervetuloviestin lisääminen
description: Tässä ohjeaiheessa kuvataan, miten tervetulosanoma lisätään Microsoft Dynamics 365 Commerce -sivustoon.
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 25a4e91646916b03c8a138fc713577f429ab633c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697379"
---
# <a name="add-a-welcome-message"></a>Tervetuloviestin lisääminen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kuvataan, miten tervetulosanoma lisätään Microsoft Dynamics 365 Commerce -sivustoon.

## <a name="overview"></a>Yleiskatsaus

Sähköisen kaupankäynnin sivuston tervetulosanoma voi kertoa kävijöille meneillään olevista alennusmyynneistä, sivuston päivityksistä ja kausittaisista kokoelmista. Tervetulosanoma määritetään hälytysmoduulin avulla.

Hälytysmoduuli on lisättävä ylätunnisteosan **Virhe/tietosanomat**-paikkaan. Hälytysmoduulin avulla voit määrittää näkyvän tekstin, tekstin värin ja tasauksen. Sen avulla voit myös määrittää, voivatko sivuston vierailijat hylätä viestin.

Kun jaettuun ylätunnisteosaan lisätään tervetulosanoma, se näkyy jokaisella sivulla, jolla käytetään jaettua ylätunnisteen osaa.

Voit lisätä sivustoon tervetulosanoman seuraavasti.

1. Siirry Dynamics 365 Commerce -sovelluksessa sivustoosi.
1. Valitse **Osat**.
1. Valitse ylätunnisteosa, johon sanoma lisätään.
1. Laajenna jäsennyspuussa **Virhe-/tietosanomat**-kohta.
1. Valitse hälytysmoduuli.

    Jos hälytysmoduulia ei vielä ole, valitse kolmen pisteen painike (**...**) **Virhe-/tietosanomat**-kohdan vieressä ja valitse sitten **Lisää moduuli**. Valitse hälytysmoduuli ja valitse sitten **OK**.

1. Valitse oikealla olevassa ominaisuusruudussa **Tiedot**-välilehden **Lisää tietolähde** -kohta ja valitse sitten **Sisältö**.
1. Kirjoita **Syöttöteksti**-kenttään tervetulosanoman teksti.
1. Tallenna ylätunnisteosa, kirjaa se sisään ja julkaise se.

Tervetulosanoma tulee nyt näkyviin jokaisen valittua ylätunnisteosaa käyttävän sivuston sivun yläosaan.

## <a name="additional-resources"></a>Lisäresurssit

[Logon lisääminen](add-logo.md)

[Sivuston teeman valitseminen](select-site-theme.md)

[Favicon-kuvakkeen lisääminen](add-favicon.md)

[Copyright-ilmoituksen lisääminen](add-copyright-notice.md)

[Kielten lisääminen sivustoon](add-languages-to-site.md)

[Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi](add-telemetry.md)

