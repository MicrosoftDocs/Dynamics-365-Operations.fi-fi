---
title: Ostoskorikuvakemoduuli
description: Tässä ohjeaiheessa käsitellään ostoskorimoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ebc5cfa490a4c8538fd081aced0844ed01d63a26
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/07/2020
ms.locfileid: "4412130"
---
# <a name="cart-icon-module"></a>Ostoskorikuvakemoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään ostoskorimoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskuvaus

Ostoskorikuvakemoduuli edustaa koria sivun otsikkomoduulissa ja ilmaisee, kuinka monta nimikettä ostoskorissa on. Ostoskorikuvakemoduuli näyttää myös ostoskorin yhteenvedon (tunnetaan myös nimellä miniostoskori), kun hiiri viedään ostoskorikuvakkeen yli. Pienoiskori antaa käyttäjälle yhteenvedon ostoskorin nimikkeistä ilman, että sinun tarvitsee siirtyä ostoskorisivulle. Lisäksi se mahdollistaa myös käyttäjän siirtymisen suoraan kassasivulle, jos hän on tyytyväinen yhteenvetoon. Tämä vähentää sivusiirtymien määrää ja nopeuttaa uloskuittausta. 

> [!NOTE]
> Kortin kuvakemoduulin tuki on saatavana Dynamics 365 Commercen versiossa 10.0.11.

Seuraavassa kuvassa näkyy esimerkki ostoskorin kuvakemoduulista, jossa näkyy pienoiskärry Fabrikam-otsikossa.

![Esimerkki ostoskärrykuvakemoduulista](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Moduulin ominaisuudet

- **Näytä pienoiskori** – Jos valinta on tosi, tämä ominaisuus mahdollistaa ostoskorin yhteenvedon (pienoiskorin) näyttämisen, kun hiiri viedään ostoskorin kuvakkeen yli. Tätä toimintoa tuetaan vain työpöydän näkymäporteissa.

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