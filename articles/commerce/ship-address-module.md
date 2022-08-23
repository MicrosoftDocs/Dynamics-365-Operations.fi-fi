---
title: Toimitusosoitemoduuli
description: Tässä artikkelissa on tietoja toimitusosoitemoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
author: anupamar-ms
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 48e6909b4dac9722830a83ec3a63a58876768d7e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275002"
---
# <a name="shipping-address-module"></a>Toimitusosoitemoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan tietoja toimitusosoitemoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.

Toimitusosoitemoduulin avulla asiakkaat voivat lisätä tai valita tilauksen toimitusosoitteen kassatyönkulun aikana. Jos asiakas on kirjautunut sisään, kaikki kyseiselle asiakkaalle aiemmin tallennetut osoitteet näytetään ja asiakas voi valita niistä. Asiakas voi myös lisätä uuden osoitteen. Toimitusosoitemoduulia käytetään kaikissa tilauksen nimikkeissä, jotka edellyttävät toimitusta.

Toimitusosoitteen muodot voidaan määrittää kunkin maan tai alueen Commerce Headquarters -sovelluksessa, ja toimitusosoitemoduuli ottaa käyttöön maa-/aluekohtaiset säännöt.

Kun asiakkaat syöttävät toimitusosoitteen kassatyönkulun aikana, heillä on mahdollisuus tallentaa osoite ensisijaiseksi osoitteeksi. Tämä vaihtoehto näkyy vain, jos asiakas on kirjautunut sisään.

Vaikka tämä toimitusosoitemoduuli ei sisällä osoitteen vahvistusta, tämä toiminto voidaan toteuttaa mukautuksen avulla.

Seuraavassa kuvassa on esimerkki uudesta toimitusosoitemoduulista maksusivulla.

![Esimerkki toimitusosoitemoduulista maksusivulla.](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Moduulin ominaisuudet

| Ominaisuuden nimi | Arvot | kuvaus |
|---------------|--------|-------------|
| Otsikko | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Toimitusosoitemoduulin valinnainen otsikko. |
| Näytä osoitetyyppi | **Tosi** vai **Epätosi** | Jos tämän valinnaisen ominaisuuden arvo on **Tosi**, näkyviin tulee osoitetyyppi, esimerkiksi **koti** tai **yritys**. Jos osoitetyyppiä ei ole määritetty, osoite tallennetaan automaattisesti **tyypiksi**=**Muu**. |
| Ota automaattinen ehdotus käyttöön| **Tosi** vai **Epätosi** | Jos tämän valinnaisen ominaisuuden arvoksi määritetään **Tosi**, automaattisia osoite-ehdotuksia annetaan. Ehdotukset saadaan Bing Maps -palvelusta. Lisätietoja Bing Maps -integroinnin määrityksestä sivustossasi on [myymälän valitsinmoduulissa](store-selector.md). Tämä ominaisuus on käytettävissä Commerce-version 10.0.15 julkaisussa.|
|Automaattisen ehdotuksen vaihtoehdot| Numero| Jos automaattiset osoite-ehdotukset ovat käytössä, voit määrittää lisäasetuksia, kuten annettavien ehdotusten enimmäismäärän.|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>Lisää toimitusosoitemoduuli kassalle-sivulle ja määritä pakolliset ominaisuudet

Toimitusosoitemoduuli voidaan lisätä vain kassalle-moduuliin. Lisätietoja toimitusosoitemoduulin konfiguroinnista ja lisäämisestä kassalle-sivulle on kohdassa [kassalle-moduuli](add-checkout-module.md).

## <a name="additional-resources"></a>Lisäresurssit

[Ostoskorimoduuli](add-cart-module.md)

[Ostoskorikuvakemoduuli](cart-icon-module.md)

[Kassamoduuli](add-checkout-module.md)

[Maksumoduuli](payment-module.md)

[Toimitusvaihtoehtomoduuli](delivery-options-module.md)

[Noudon tiedot -moduuli](pickup-info-module.md)

[Tilauksen tiedot -moduuli](order-confirmation-module.md)

[Lahjakorttimoduuli](add-giftcard.md)

[Myymälän valitsinmoduuli](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
