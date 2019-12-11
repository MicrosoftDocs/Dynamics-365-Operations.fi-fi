---
title: Tilauksen vahvistusmoduuli
description: Tässä ohjeaiheessa on tietoja tilauksen vahvistusmoduuleista ja niiden luomisesta Microsoft Dynamics 365 Commerce -sovellukseen.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698323"
---
# <a name="order-confirmation-module"></a>Tilauksen vahvistusmoduuli

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja tilauksen vahvistusmoduuleista ja niiden luomisesta Microsoft Dynamics 365 Commerce -sovellukseen.

## <a name="overview"></a>Yleiskatsaus

Tilauksen vahvistusmoduulin avulla näytetään vahvistussanoma tilausvahvistussivulla tilauksen asettamisen jälkeen. Tilauksen vahvistusmoduulissa on tilauksen vahvistusnumero sekä uloskuittauksen aikana annettu asiakkaan sähköpostiosoite.

Jos tilaus tehdään uloskuittauksen aikana, tilauksen vahvistusnumero ja asiakkaan sähköpostiosoite välitetään tilausvahvistussivulle kyselymerkkijonona sivun URL-osoitteessa. Tilauksen vahvistusmoduuli vastaanottaa nämä tiedot ja hahmontaa tilauksen tilan tilausvahvistussivulle. Tilauksen vahvistusmoduuli vaatii tämän sivun kontekstin, jotta tilauksen tila voidaan antaa.

## <a name="order-confirmation-module-properties"></a>Tilauksen vahvistusmoduulin ominaisuudet

| Ominaisuuden nimi | Arvot | Kuvaus |
|---------------|--------|-------------|
| Otsikko       | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Tilauksen vahvistusmoduulilla voi olla otsikko. Oletusarvoisesti otsikossa käytetään **H2**-otsikkotunnusta. Tunnuksen voi kuitenkin muuttaa, jotta helppokäyttötoimintojen vaatimukset täyttyvät. |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a>Moduulit, joita voidaan käyttää tilausvahvistussivun moduulissa 

- **Suositukset** – Suositusten moduuli voidaan asettaa tilausvahvistussivulle ehdottamaan asiakkaalle muita tuotteita.
- **Markkinointi** – Markkinointimoduuli voi lisätä markkinointisisältöä tilausvahvistussivulle.

## <a name="create-an-order-confirmation-page-module"></a>Tilausvahvistussivun moduulin luominen

1. Luo sivumalli, jonka nimi on **Tilausvahvistusmalli**.
1. Lisää tilauksen vahvistusmoduuli oletussivun **pääpaikkaan**.
1. Lisää tilauksen vahvistusmoduuliin suositusten moduuli.
1. Tallenna ja esikatsele malli. Tilauksen vahvistusmoduulia ei tule hahmontaa, koska se vaatii tilauksen vahvistusnumeron.
1. Kirjaa malli sisään ja julkaise se.
1. Käytä juuri luotua tilauksen vahvistusmallia, kun haluat luoda sivun nimeltä **Tilausvahvistussivu**.
1. Lisää sivun jäsennykseen oletussivu.
1. Lisää **Ylätunniste**-paikkaan ylätunnisteen osa.
1. Lisää **Alatunniste**-paikkaan alatunnisteen osa.
1. Lisää tilauksen vahvistusmoduuli **pääpaikkaan**.
1. Lisää tilauksen vahvistusmoduulin ominaisuusruudussa otsikon **tilausvahvistus**.
1. Lisää tilauksen vahvistusmoduulin alle suositusten moduuli ja määritä se niin, että se käyttää **Uusi**- ja **Myyvimmät**-asetuksia.
1. Tallenna ja esikatsele sivu, kirjaa se sisään ja julkaise se.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)
