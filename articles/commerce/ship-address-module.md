---
title: Toimitusosoitemoduuli
description: Tässä ohjeaiheessa on tietoja toimitusosoitemoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
author: anupamar-ms
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: fd48a04612159cbe29a2cc7cafea1c9c4c8745b4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795426"
---
# <a name="shipping-address-module"></a>Toimitusosoitemoduuli

[!include [banner](includes/banner.md)]

Tässä aiheessa kuvataan tietoja toimitusosoitemoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.

Toimitusosoitemoduulin avulla asiakkaat voivat lisätä tai valita tilauksen toimitusosoitteen kassatyönkulun aikana. Jos asiakas on kirjautunut sisään, kaikki kyseiselle asiakkaalle aiemmin tallennetut osoitteet näytetään ja asiakas voi valita niistä. Asiakas voi myös lisätä uuden osoitteen. Toimitusosoitemoduulia käytetään kaikissa tilauksen nimikkeissä, jotka edellyttävät toimitusta.

Toimitusosoitteen muodot voidaan määrittää kunkin maan tai alueen Commerce Headquarters -sovelluksessa, ja toimitusosoitemoduuli ottaa käyttöön maa-/aluekohtaiset säännöt.

Kun asiakkaat syöttävät toimitusosoitteen kassatyönkulun aikana, heillä on mahdollisuus tallentaa osoite ensisijaiseksi osoitteeksi. Tämä vaihtoehto näkyy vain, jos asiakas on kirjautunut sisään.

Vaikka tämä toimitusosoitemoduuli ei sisällä osoitteen vahvistusta, tämä toiminto voidaan toteuttaa mukautuksen avulla.

Seuraavassa kuvassa on esimerkki uudesta toimitusosoitemoduulista maksusivulla.

![Esimerkki toimitusosoitemoduulista Kassalle-sivulla](./media/ecommerce-shippingaddress.PNG)

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