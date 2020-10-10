---
title: Toimitusosoitemoduuli
description: Tässä ohjeaiheessa on tietoja toimitusosoitemoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 7233b23020e6c82f39981d530095642902461807
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818395"
---
# <a name="shipping-address-module"></a>Toimitusosoitemoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja toimitusosoitemoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.

## <a name="overview"></a>Yhteenveto

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

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>Lisää toimitusosoitemoduuli kassalle-sivulle ja määritä pakolliset ominaisuudet

Toimitusosoitemoduuli voidaan lisätä vain kassalle-moduuliin. Lisätietoja toimitusosoitemoduulin konfiguroinnista ja lisäämisestä kassalle-sivulle on kohdassa [kassalle-moduuli](add-checkout-module.md).

## <a name="additional-resources"></a>Lisäresurssit

[Ostoskorimoduuli](add-cart-module.md)

[Ostoskorikuvakemoduuli](cart-icon-module.md)

[Kassamoduuli](add-checkout-module.md)

[Maksumoduuli](payment-module.md)

[Toimitusvaihtoehdot -moduuli](delivery-options-module.md)

[Tilauksen tiedot -moduuli](order-confirmation-module.md)

[Lahjakorttimoduuli](add-giftcard.md)
