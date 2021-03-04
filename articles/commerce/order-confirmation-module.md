---
title: Tilauksen vahvistusmoduuli
description: Tässä ohjeaiheessa on tietoja tilauksen vahvistusmoduuleista ja niiden käytämisestä Microsoft Dynamics 365 Commerce -sovelluksessa.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bf33ebf9c0c5136f40fcd7e1012988d186c4169b
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/07/2020
ms.locfileid: "4412134"
---
# <a name="order-confirmation-module"></a>Tilauksen vahvistusmoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja tilauksen vahvistusmoduuleista ja niiden käytämisestä Microsoft Dynamics 365 Commerce -sovelluksessa.

## <a name="overview"></a>Yleiskuvaus

Tilausvahvistus-moduulia käytetään näyttämään tilausvahvistuksen yksityiskohdat tilauksen tekemisen jälkeen. Se näyttää tilausvahvistuksen tunnuksen, tilauksen yhteystiedot ja muut tilaustiedot, kuten ostetut nimikkeet, maksutiedot, noutovaihtoehdot ja toimitustavan.

## <a name="order-confirmation-module-properties"></a>Tilauksen vahvistusmoduulin ominaisuudet

| Ominaisuuden nimi  | Arvot | Kuvaus |
|----------------|--------|-------------|
| Otsikko        | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Tilauksen vahvistusmoduulilla voi olla otsikko. Oletusarvoisesti otsikossa käytetään **H2**-otsikkotunnusta. Tunnuksen voi kuitenkin muuttaa, jotta helppokäyttötoimintojen vaatimukset täyttyvät. |
| Yhteyshenkilön puhelinnumero | Text | Tilaukseen liittyviin kysymyksiin voidaan antaa yhteyshenkilön numero. |
| Näytä noudon aikavälin tiedot | Tosi tai epätosi. | Tämä ominaisuus on käytettävissä Dynamics 365 Commerce -versiossa 10.0.15 ja uudemmissa versioissa. Jos arvo on Tosi, noudon aikavälin tiedot näytetään, jos ne on annettu noudettavalle nimikkeelle|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a>Moduulit, joita voidaan käyttää tilausvahvistussivulla

Kun luot tilausvahvistus-sivun, voit lisätä muita asiaankuuluvia moduuleja tilausvahvistus-moduulin lisäksi. Seuraavassa on muutamia esimerkkejä:

- **Suositukset-moduuli** – Suositusten moduuli voidaan lisätä tilausvahvistussivulle ehdottamaan asiakkaalle muita tuotteita.
- **Markkinointi moduulit** – Mikä tahansa markkinointimoduuli, josta näkyy markkinointisisältö, voidaan lisätä tilausvahvistus-sivulle.

## <a name="add-an-order-confirmation-module-to-a-page"></a>Tilausvahvistusmoduulin lisääminen sivulle

Voit lisätä tilausvahvistusmoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi**-kohtaan nimi **Tilauksen vahvistusmalli** ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.
1. Valitse **Oletussivu**-moduulin **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Tilausvahvistus** -moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna** ja esikatsele sitten mallia valitsemalla **Esikatselu**. Tilauksen vahvistusmoduulia ei hahmonneta, koska se vaatii tilauksen vahvistusnumeron.
1. Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Valitse **Valitse malli** -valintaikkunassa **Tilausvahvistus-malli**. Kirjoita **Sivun nimi** -kohtaan **Tilausvahvistus-sivu** ja valitse sitten **OK**.
1. Valitse **Oletussivu**-moduulin **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Tilausvahvistus** -moduuli ja valitse sitten **OK**.
1. Valitse tilauksen vahvistusmoduulin ominaisuusruudun kynäsymbolin vieressä **Otsikko**.
1. Anna **Otsikko**-valintaikkunan **Otsikon teksti** -kentästä otsikon tekstiksi **Tilausvahvistus** ja valitse sitten **OK**.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="additional-resources"></a>Lisäresurssit

[Ostoskorimoduuli](add-cart-module.md)

[Ostoskorikuvakemoduuli](cart-icon-module.md)

[Kassamoduuli](add-checkout-module.md)

[Maksumoduuli](payment-module.md)

[Toimitusosoitemoduuli](ship-address-module.md)

[Toimitusvaihtoehtomoduuli](delivery-options-module.md)

[Noudon tiedot -moduuli](pickup-info-module.md)

[Lahjakorttimoduuli](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]