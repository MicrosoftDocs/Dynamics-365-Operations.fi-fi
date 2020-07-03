---
title: Tilauksen tiedot -moduuli
description: Tässä ohjeaiheessa on tietoja tilauksen tietomoduuleista ja niiden käytöstä Microsoft Dynamics 365 Commercessa.
author: anupamar
manager: annbe
ms.date: 06/18/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2ec629d9fd027be01652351ab1c99001e063e30
ms.sourcegitcommit: 49656661c89c864e8e067259a601c3bbceb8bef4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/18/2020
ms.locfileid: "3464927"
---
# <a name="order-details-module"></a>Tilauksen tiedot -moduuli


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja tilauksen tietomoduuleista ja niiden käytöstä Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskatsaus

Tilaustiedot-moduulia käytetään näyttämään tilausvahvistuksen yksityiskohdat tilauksen tekemisen jälkeen. Se näyttää tilausvahvistuksen tunnuksen, tilauksen yhteystiedot ja muut tilaustiedot, kuten ostetut nimikkeet, maksutiedot ja toimitustavan.

## <a name="order-details-module-properties"></a>Tilauksen tietomoduulin ominaisuudet

| Ominaisuuden nimi  | Arvot | kuvaus |
|----------------|--------|-------------|
| Otsikko        | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Tilauksen tietomoduulilla voi olla otsikko. Oletusarvoisesti otsikossa käytetään **H2**-otsikkotunnusta. Tunnuksen voi kuitenkin muuttaa, jotta helppokäyttötoimintojen vaatimukset täyttyvät. |
| Yhteyshenkilön puhelinnumero | Text | Tilaukseen liittyviin kysymyksiin voidaan antaa yhteyshenkilön numero. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Moduulit, joita voidaan käyttää tilaustietosivulla

Kun luot tilaustiedot-sivun, voit lisätä muita asiaankuuluvia moduuleja tilaustiedot-moduulin lisäksi. Seuraavassa on muutamia esimerkkejä:

- **Suositukset-moduuli** – Suositusten moduuli voidaan lisätä tilaustietosivulle ehdottamaan asiakkaalle muita tuotteita.
- **Markkinointi moduulit** – Mikä tahansa markkinointimoduuli, josta näkyy markkinointisisältö, voidaan lisätä tilaustiedot-sivulle.

## <a name="add-an-order-details-module-to-a-page"></a>Tilaustietomoduulin lisääminen sivulle

Voit lisätä tilaustietomoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi**-kohtaan nimi **Tilauksen tietomalli** ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.
1. Valitse **Oletussivu**-moduulin **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Tilauksen tiedot** -moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**ja esikatsele sitten mallia valitsemalla **Esikatselu**. Tilauksen tietomoduulia ei tule hahmontaa, koska se vaatii tilauksen vahvistusnumeron.
1. Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Valitse **Valitse malli** -valintaikkunassa **Tilauksen tietomalli**. Kirjoita **Sivun nimi** -kohtaan **Tilauksen tietosivu** ja valitse sitten **OK**.
1. Valitse **Oletussivu**-moduulin **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Tilauksen tiedot** -moduuli ja valitse sitten **OK**.
1. Valitse tilauksen tietomoduulin ominaisuusruudun kynäsymbolin vieressä **Otsikko**.
1. Anna **Otsikko**-valintaikkunan **Otsikon teksti** -kentästä otsikon tekstiksi **Tilauksen tiedot** ja valitse sitten **OK**.
1. Valitse **Tallenna**ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)
