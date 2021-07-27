---
title: Ostoskorikuvakemoduuli
description: Tässä ohjeaiheessa käsitellään ostoskorimoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e0238e9d464fc1d44cbc5091638ac7270d5b6ae3
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479301"
---
# <a name="cart-icon-module"></a>Ostoskorikuvakemoduuli

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä ohjeaiheessa käsitellään ostoskorimoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.

Ostoskorikuvakemoduuli edustaa koria sivun otsikkomoduulissa ja ilmaisee, kuinka monta nimikettä ostoskorissa on. Ostoskorikuvakemoduuli näyttää myös ostoskorin yhteenvedon (tunnetaan myös nimellä miniostoskori), kun hiiri viedään ostoskorikuvakkeen yli. Pienoiskori antaa käyttäjälle yhteenvedon ostoskorin nimikkeistä ilman, että sinun tarvitsee siirtyä ostoskorisivulle. Lisäksi se mahdollistaa myös käyttäjän siirtymisen suoraan kassasivulle, jos hän on tyytyväinen yhteenvetoon. Tämä vähentää sivusiirtymien määrää ja nopeuttaa uloskuittausta. 

Seuraavassa kuvassa näkyy esimerkki ostoskorin kuvakemoduulista, jossa näkyy pienoiskärry Fabrikam-otsikossa.

![Esimerkki ostoskorikuvakemoduulista.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Moduulin ominaisuudet

- **Näytä pienoiskori** – Jos valinta on tosi, tämä ominaisuus mahdollistaa ostoskorin yhteenvedon (pienoiskorin) näyttämisen, kun hiiri viedään ostoskorin kuvakkeen yli. Tätä toimintoa tuetaan vain työpöydän näkymäporteissa.

## <a name="module-properties-in-the-adventure-works-theme"></a>Moduulin ominaisuudet Adventure Works -teemassa

Adventure Works -teeman ostoskorikuvakemoduuli sisältää kaksi ylimääräistä paikkaa pienoiskoria varten. Nämä paikat ovat moduulimääritelmän laajennuksia.

- **Tyhjän ostosokorin kampanjat** – Tähän paikkaan voi lisätä sisältölohkomoduulin. Kun ostoskori on tyhjä, määritetty sisältölohkomoduuli näytetään. Sisältölohkomoduulia voidaan käyttää kampanjoille, markkinointisisällölle ja luokkasivujen linkeille, jotta asiakkaat voivat jatkaa ostosten tekemistä.
- **Kampanjasisältö** – Tätä paikkaa voidaan käyttää kampanjoiden esittelemiseen, esimerkiksi "Ilmainen toimitus yli 100 euron toimituksiin". Kampanjasisällön paikassa voidaan käyttää sisältölohko-, tekstilohko- ja kuvaluettelomoduuleja.

Seuraavassa kuvassa on esimerkki Adventure Works -teeman ostoskorikuvakemoduulista, joka näyttää kampanjasisältöä pienoiskorissa.

![Esimerkki ostoskorikuvakemoduulista Adventure Works -teemassa](./media/AW_minicart.PNG)

> [!IMPORTANT]
> Adventure Works -teeman paikat ovat käytettävissä Dynamics 365 Commerce -version 10.0.20 julkaisusta eteenpäin.

## <a name="add-a-cart-icon-module-to-a-page"></a>Ostoskorikuvakkeen lisääminen sivulle

Jos haluat lisätä ostoskorikuvakkeen moduulin, katso kohta [Otsikkomoduuli](author-header-module.md).

## <a name="additional-resources"></a>Lisäresurssit

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Maksumoduuli](payment-module.md)

[Toimitusosoitemoduuli](ship-address-module.md)

[Toimitusvaihtoehtomoduuli](delivery-options-module.md)

[Noudon tiedot -moduuli](pickup-info-module.md)

[Tilauksen tiedot -moduuli](order-confirmation-module.md)

[Lahjakorttimoduuli](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
