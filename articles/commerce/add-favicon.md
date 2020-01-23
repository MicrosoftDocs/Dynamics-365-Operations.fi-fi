---
title: Favicon-kuvakkeen lisääminen
description: Tässä ohjeaiheessa kerrotaan, kuinka favicon-kuvake lisätään sivustoon.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 18e12cbe46650fcf024a56b6de9a8cb2903d2bf8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914568"
---
# <a name="add-a-favicon"></a>Favicon-kuvakkeen lisääminen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka favicon-kuvake lisätään sivustoon.

## <a name="overview"></a>Yleiskatsaus

Favicon on pieni grafiikkatiedosto, joka näkyy selaimen välilehdessä, osoitepalkissa, selaushistoriassa sekä muissa paikoissa, kuten kirjanmerkeissä tai suosikeissa. Suosittelemme, että lisäät favicon-kuvakkeen sivustoon, koska se edustaa ja vahvistaa omaa tuotemerkkiä ja auttaa sivuston erottumisessa muista sivustoista, joilla asiakkaat käyvät.

Voit lisätä useita eri kokoisia favicon-kuvakkeita ja erilaisia favicon-tiedostoja sivustoon. Tässä ohjeaiheessa kerrotaan, miten voit lisätä yhden favicon-kohteen. Samaa prosessia ja sijaintia käytetään useiden favicon-kohteiden lisäämisessä.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Lataa favicon sivuston resurssikokoelmaan

Lataa favicon sivuston resurssikokoelmaan seuraavasti.

1. Siirry kohtaan **Resurssit \> Lataa \> Lataa resurssit**.
1. Etsi ja valitse favicon paikallisessa tiedostojärjestelmässä.
1. Kirjoita otsikko ja valitse **OK**. 
1. Kopioi oikealla olevaan ominaisuusruutuun favicon-tiedoston julkinen URL-osoite.

> [!NOTE]
> Jos et valitse **Julkaise resurssit lataamisen jälkeen** -vaihtoehtoa, palaa **Resurssit**-sivulle ja julkaise favicon myöhemmin manuaalisesti.

## <a name="create-the-html-for-the-favicon"></a>Luo favicon-tiedostolle HTML-koodia

Jos haluat luoda favicon-tiedostolle HTML-koodia, käytä seuraavaa HTML-katkelmaa. Korvaa **href**-määritteessä **"Public\_URL\_for\_your\_favicon"** aiemmin kopioimallasi julkisella URL-osoitteella.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a>Lisää favicon-tiedostoon HTML-koodia sivuston \<head\>-elementissä

Jos haluat lisätä favicon-tiedoston sivustoon, käytä samaa menetelmää, jonka avulla lisäät minkä tahansa HTML- tai komentosarjan **\<head\>**-elementtiin sivuston sivuilla.

## <a name="additional-resources"></a>Lisäresurssit

[Logon lisääminen](add-logo.md)

[Sivuston teeman valitseminen](select-site-theme.md)

[CSS-ohitustiedostojen parissa työskentely](css-override-files.md)

[Tervetuloviestin lisääminen](add-welcome-message.md)

[Copyright-ilmoituksen lisääminen](add-copyright-notice.md)

[Kielten lisääminen sivustoon](add-languages-to-site.md)

[Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi](add-telemetry.md)

