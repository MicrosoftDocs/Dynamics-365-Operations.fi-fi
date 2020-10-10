---
title: Lahjakorttimoduuli
description: Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: fc47d590789c79c08af7555222aa7cc9409da23c
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817423"
---
# <a name="gift-card-module"></a>Lahjakorttimoduuli

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskuvaus

Lahjakorttimoduuleja voi käyttää kassamoduuleissa lahjakorttien hyväksynnässä. Se on yleinen maksumuoto, jota käytetään sähköisen kaupankäynnin tapahtumissa. Lahjakorttimoduuli tukee Dynamics 365-, SVS- ja Givex-lahjakortteja. SVS- ja Givex-lahjakortit lunastetaan Adyen-maksupalveluntarjoajan kautta. Lisätietoja ulkoisten lahjakorttien, kuten SVS:n ja Givexin tuesta, on ohjeaiheessa [Ulkoisten lahjakorttien tuki](./dev-itpro/gift-card.md).

> [!NOTE]
> Tuki SVS- ja Givex-lahjakorttien lunastamiselle kassatyönkulussa on käytettävissä Dynamics 365 Commercen versiossa 10.0.11. 

Käytettävissä on seuraavat kaksi lahjakorttimoduulia:

- **Lahjakortti** - Tätä moduulia voi käyttää kassasivulla lunastettaessa lahjakortti maksuvälineenä. 
- **Lahjakortin saldon tarkistus** - Tätä moduulia voi käyttää millä tahansa sivulla, kun halutaan tarkistaa lahjakortin saldo. Tämä moduuli on käytettävissä Commercen versiossa 10.0.14 ja uudemmissa versioissa.

> [!NOTE]
> Lahjakortin saldontarkistusmoduulin tuki on saatavilla Dynamics 365 Commercen versiossa 10.0.14.

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

> [!IMPORTANT]
> Nämä asetukset ovat käytettävissä Dynamics 365 Commercen versiossa 10.0.11-versiossa, ja niitä tarvitaan vain, jos tarvitset tukea SVS- tai Givex-lahjakorteille. Jos päivität vanhemmasta Dynamics 365 Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti. Ohjeet appsettings.json-tiedoston päivittämiseen: [SDK:n ja moduuliskirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

## <a name="add-a-gift-card-module-to-a-page"></a>Lahjakorttimoduulin lisääminen sivulle

Lisätietoja lahjakorttimoduulin lisäämisestä kassasivulle ja tarvittavien ominaisuuksien määrittämisestä on kohdassa [Kassamoduuli.](add-checkout-module.md).

## <a name="additional-resources"></a>Lisäresurssit

[Ostoskorimoduuli](add-cart-module.md)

[Ostoskorikuvakemoduuli](cart-icon-module.md)

[Kassamoduuli](add-checkout-module.md)

[Maksumoduuli](payment-module.md)

[Toimitusosoitemoduuli](ship-address-module.md)

[Toimitusvaihtoehtomoduuli](delivery-options-module.md)

[Tilauksen tiedot -moduuli](order-confirmation-module.md)

[Ulkoisten lahjakorttien tuki](./dev-itpro/gift-card.md)

[SDK:n ja moduulikirjaston päivitykset](e-commerce-extensibility/sdk-updates.md)
