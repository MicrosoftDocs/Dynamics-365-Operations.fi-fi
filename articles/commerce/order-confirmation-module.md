---
title: Tilauksen tiedot -moduuli
description: Tässä ohjeaiheessa on tietoja tilauksen tietomoduuleista ja niiden käytöstä Microsoft Dynamics 365 Commercessa.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026014"
---
# <a name="order-details-module"></a>Tilauksen tiedot -moduuli


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja tilauksen tietomoduuleista ja niiden käytöstä Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskatsaus

Tilaustiedot-moduulia käytetään näyttämään tilausvahvistuksen yksityiskohdat tilauksen tekemisen jälkeen. Se näyttää tilausvahvistuksen tunnuksen, tilauksen yhteystiedot ja muut tilaustiedot, kuten ostetut nimikkeet, maksutiedot ja toimitustavan.

## <a name="order-confirmation-module-properties"></a>Tilauksen vahvistusmoduulin ominaisuudet

| Ominaisuuden nimi  | Arvot | Kuvaus |
|----------------|--------|-------------|
| Otsikko        | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Tilauksen vahvistusmoduulilla voi olla otsikko. Oletusarvoisesti otsikossa käytetään **H2**-otsikkotunnusta. Tunnuksen voi kuitenkin muuttaa, jotta helppokäyttötoimintojen vaatimukset täyttyvät. |
| Yhteyshenkilön puhelinnumero | Text | Tilaukseen liittyviin kysymyksiin voidaan antaa yhteyshenkilön numero. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Moduulit, joita voidaan käyttää tilaustietosivulla

Kun luot tilaustiedot-sivun, voit lisätä muita asiaankuuluvia moduuleja tilaustiedot-moduulin lisäksi. Seuraavassa on muutamia esimerkkejä:

- **Suositukset-moduuli** – Suositusten moduuli voidaan lisätä tilaustietosivulle ehdottamaan asiakkaalle muita tuotteita.
- **Markkinointi moduulit** – Mikä tahansa markkinointimoduuli, josta näkyy markkinointisisältö, voidaan lisätä tilaustiedot-sivulle.

## <a name="create-an-order-details-page-module"></a>Tilaustietosivun moduulin luominen

1. Luo sivumalli, jonka nimi on **Tilaustiedot -malli**.
1. Lisää tilauksen tietomoduuli oletussivun **pääpaikkaan**.
1. Lisää tilauksen tietomoduuliin suositusten moduuli.
1. Tallenna ja esikatsele malli. Tilauksen tietomoduulia ei tule hahmontaa, koska se vaatii tilauksen vahvistusnumeron.
1. Kun mallin muokkaus on valmis, julkaise se.
1. Käytä juuri luotua tilauksen tietomallia, kun haluat luoda sivun nimeltä **Tilaustietosivu**.
1. Lisää sivun jäsennykseen oletussivu.
1. Lisää **Ylätunniste**-paikkaan ylätunnisteen osa.
1. Lisää **Alatunniste**-paikkaan alatunnisteen osa.
1. Lisää tilauksen tietomoduuli **pääpaikkaan**.
1. Lisää tilauksen tietomoduulin ominaisuusruudussa otsikko **Tilaustiedot**.
1. Lisää tilauksen tietomoduulin alle suositusten moduuli ja määritä se niin, että se käyttää **Uusi**- ja **Myyvimmät**-asetuksia.
1. Tallenna ja esikatsele sivu.
1. Kun sivun muokkaus on valmis, julkaise se.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)
