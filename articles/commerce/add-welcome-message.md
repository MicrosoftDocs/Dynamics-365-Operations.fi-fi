---
title: Tervetuloviestin lisääminen
description: Tässä ohjeaiheessa kuvataan, miten tervetulosanoma lisätään Microsoft Dynamics 365 Commerce -sivustoon.
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797380"
---
# <a name="add-a-welcome-message"></a>Tervetuloviestin lisääminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kuvataan, miten tervetulosanoma lisätään Microsoft Dynamics 365 Commerce -sivustoon.

Sähköisen kaupankäynnin sivuston tervetulosanoma voi kertoa kävijöille meneillään olevista alennusmyynneistä, sivuston päivityksistä ja kausittaisista kokoelmista. Tervetulosanoma määritetään hälytysmoduulin avulla.

Hälytysmoduuli on lisättävä ylätunnisteosan **Virhe/tietosanomat**-paikkaan. Hälytysmoduulin avulla voit määrittää näkyvän tekstin, tekstin värin ja tasauksen. Sen avulla voit myös määrittää, voivatko sivuston vierailijat hylätä viestin.

Kun jaettuun ylätunnisteosaan lisätään tervetulosanoma, se näkyy jokaisella sivulla, jolla käytetään jaettua ylätunnisteen osaa.

Voit lisätä sivustoon tervetulosanoman seuraavasti.

1. Siirry sivustollesi Commerce-sivuston luontiohjelmassa.
1. Valitse **Osat**.
1. Valitse ylätunnisteosa, johon sanoma lisätään.
1. Laajenna jäsennyspuussa **Virhe-/tietosanomat**-kohta.
1. Valitse hälytysmoduuli ja valitse sitten **OK**. Jos hälytysmoduulia ei vielä ole, valitse ensin kolmen pisteen painike (**...**) **Virhe-/tietosanomat**-kohdan vieressä ja valitse sitten **Lisää moduuli**.
1. Valitse oikealla olevassa ominaisuusruudussa **Tiedot**-välilehden **Lisää tietolähde** -kohta ja valitse sitten **Sisältö**.
1. Kirjoita **Syöttöteksti**-kenttään tervetulosanoman teksti.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi ylätunnisteen osan, ja julkaise se valitsemalla **Julkaise**. 

Tervetulosanoma tulee nyt näkyviin jokaisen valittua ylätunnisteosaa käyttävän sivuston sivun yläosaan.

## <a name="additional-resources"></a>Lisäresurssit

[Logon lisääminen](add-logo.md)

[Sivuston teeman valitseminen](select-site-theme.md)

[CSS-ohitustiedostojen parissa työskentely](css-override-files.md)

[Favicon-kuvakkeen lisääminen](add-favicon.md)

[Copyright-ilmoituksen lisääminen](add-copyright-notice.md)

[Kielten lisääminen sivustoon](add-languages-to-site.md)

[Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
