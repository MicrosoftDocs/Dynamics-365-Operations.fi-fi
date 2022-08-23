---
title: Sivuston teeman valitseminen
description: Tässä artikkelissa kuvataan, miten sivuston teema määritetään tai miten sitä muutetaan Microsoft Dynamics 365 Commerce -sovelluksessa.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 3b7b3e8d6fd75a31bf9830c50b5c641ab3e62ab3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286780"
---
# <a name="select-a-site-theme"></a>Sivuston teeman valitseminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, miten sivuston teema määritetään tai miten sitä muutetaan Microsoft Dynamics 365 Commerce -sovelluksessa.

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

[Copyright-ilmoituksen lisääminen](add-copyright-notice.md)

[Kielten lisääminen sivustoon](add-languages-to-site.md)

[Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi](add-telemetry.md)

[Teemojen yleiskatsaus](e-commerce-extensibility/theming.md)

[Uuden teeman luominen](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
