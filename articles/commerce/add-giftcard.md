---
title: Lahjakorttimoduuli
description: Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 41f808d671bf5e7425390484ea30470e044899d8
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661239"
---
# <a name="gift-card-module"></a>Lahjakorttimoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskuvaus

Lahjakortit ovat yleinen maksutapa, ja lahjakorttimoduulia voidaan käyttää kassamoduulissa hyväksymään lahjakortteja. Lahjakorttimoduuli tukee Dynamics 365-, SVS- ja Givex-lahjakortteja. SVS- ja Givex-lahjakortit lunastetaan Adyen-maksupalveluntarjoajan kautta.

Lisätietoja ulkoisten lahjakorttien, kuten SVS:n ja Givexin tuesta on ohjeaiheessa [Ulkoisten lahjakorttien tuki](./dev-itpro/gift-card.md)

Seuraavassa kuvassa on esimerkki lahjakorttimoduulista maksusivulla.

![Esimerkki lahjakorttimoduulista](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Moduulin ominaisuudet

- **Näytä lisäkentät** - Tämä ominaisuus määrittää, mitkä lahjakorttien kentät näytetään aina oletusarvoisesti näytettävän lahjakortin numeron lisäksi. Esimerkiksi jotkin lahjakortit tukevat henkilökohtaista tunnuslukua (PIN), ja toiset tukevat PIN-koodin ja vanhentumispäivämäärän näyttämistä. Vaihtoehtoisesti tämän ominaisuuden arvoksi voi määrittää "Ei mitään", jolloin näytetään vain lahjakortin numero eikä muita kenttiä näy.

Tuetut arvot:
-   PIN-koodi
-   Vanhentumispäivä
-   PIN-koodi ja vanhentumispäivä 
-   None

## <a name="site-settings-for-gift-card-modules"></a>Lahjakorttimoduulien toimipaikan asetukset

Kauppapaikan luomistyökalussa **Sivuston asetukset \> -laajennukset** -kohdassa on lahjakorttimoduulin asetus nimeltä **Tuettu lahjakorttityyppi**. Tämä asetus tukee kolmea arvoa:
- **Dynamics 365 -lahjakortti** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365 -lahjakorttien lunastamisen. Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.
- **SVS- ja Givex-lahjakortit** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain SVS- ja Givex-lahjakorttien lunastamisen. Tätä asetusta tuetaan kirjautuneiden ja anonyymien käyttäjien verkkokauppasivustossa.
- **Dynamics 365-, SVS- ja Givex-lahjakortit** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365-, SVS- ja Givex-lahjakorttien lunastamisen. Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.

## <a name="add-a-gift-card-module-to-a-page"></a>Lahjakorttimoduulin lisääminen sivulle

Lisätietoja lahjakorttimoduulin lisäämisestä kassasivulle ja tarvittavien ominaisuuksien määrittämisestä on kohdassa [Kassamoduuli.](add-checkout-module.md).

## <a name="additional-resources"></a>Lisäresurssit

[Ostoskorimoduuli](add-cart-module.md)

[Ostoskorikuvakemoduuli](cart-icon-module.md)

[Kassamoduuli](add-checkout-module.md)

[Maksumoduuli](payment-module.md)

[Toimitusosoitemoduuli](ship-address-module.md)

[Toimitusvaihtoehdot -moduuli](delivery-options-module.md)

[Tilauksen tiedot -moduuli](order-confirmation-module.md)

[Ulkoisten lahjakorttien tuki](./dev-itpro/gift-card.md)
