---
title: Sivuston teeman valitseminen
description: Tässä ohjeaiheessa kuvataan, miten sivuston teema määritetään tai miten sitä muutetaan Microsoft Dynamics 365 Commerce -sovelluksessa.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: c54a3e9471fdeb56f27fe7c567c7cd7f0b7fd218
ms.sourcegitcommit: 2ef23dcd4e42362186b9951e675010d97d55c6bd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4556426"
---
# <a name="select-a-site-theme"></a>Sivuston teeman valitseminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kuvataan, miten sivuston teema määritetään tai miten sitä muutetaan Microsoft Dynamics 365 Commerce -sovelluksessa.

## <a name="overview"></a>Yleiskatsaus

Sivuston asettelu ja tyyli (esimerkiksi fontit, koot ja värit) määritetään valitsemasi teeman mukaan ja otetaan käyttöön sivustossa. Yrityksen kehittäjä luo ja ottaa käyttöön teeman. Yleiskatsaus teemoista on kohdassa [Teemojen yleiskatsaus](e-commerce-extensibility/theming.md). Lisätietoja teemojen luomisesta ja käyttöönotosta on kohdassa [Uuden teeman luominen](e-commerce-extensibility/create-theme.md).

Kun luot sivuston ensimmäisen kerran, se käyttää teemaa, jonka nimi on **Fabrikam**. Tämä oletusteema on osa Commercen moduulikirjastoa. Kun olet ottanut käyttöön muita teemoja sivustossa, voit määrittää sivuston siten, että se käyttää yhtä niistä.

## <a name="select-the-site-theme"></a>Sivuston teeman valitseminen

Voit valita sivustossa käytettävän teeman noudattamalla seuraavia ohjeita.

1. Siirry sivuston muokkausympäristössä sivustoon.
1. Siirry kohtaan **Sivuston hallinta** \> **Laajennettavuus**.
1. Valitse **Teema**-kohdassa teema avattavasta valikosta.
1. Jos haluat käyttää valittua teemaa sivustossa, valitse **Tallenna ja julkaise**.

> [!NOTE]
> Valitsemasi teema julkaistaan sivustoon heti, kun valitset **Tallenna ja julkaise** -kohdan **Laajennettavuus**-sivulla. Voit esikatsella teemaa sivustossa ennen sen käyttöönottoa käyttämällä kehitys- tai eristysympäristöä.

## <a name="additional-resources"></a>Lisäresurssit

[Logon lisääminen](add-logo.md)

[CSS-ohitustiedostojen parissa työskentely](css-override-files.md)

[Favicon-kuvakkeen lisääminen](add-favicon.md)

[Tervetuloviestin lisääminen](add-welcome-message.md)

[Copyright-ilmoituksen lisääminen](add-copyright-notice.md)

[Kielten lisääminen sivustoon](add-languages-to-site.md)

[Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi](add-telemetry.md)

[Teemojen yleiskatsaus](e-commerce-extensibility/theming.md)

[Uuden teeman luominen](e-commerce-extensibility/create-theme.md)

