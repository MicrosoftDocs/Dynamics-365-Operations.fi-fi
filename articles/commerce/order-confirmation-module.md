---
title: Tilauksen vahvistusmoduuli
description: Tässä artikkelissa on tietoja tilauksen vahvistusmoduuleista ja niiden käyttämisestä Microsoft Dynamics 365 Commerce -sovelluksessa.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 6011c7e4713813a02fa8f812ea8981fd6fa0253f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269132"
---
# <a name="order-confirmation-module"></a>Tilauksen vahvistusmoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja tilauksen vahvistusmoduuleista ja niiden käyttämisestä Microsoft Dynamics 365 Commerce -sovelluksessa.

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
1. Valitse **Valitse moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.
1. Valitse **Oletussivu**-moduulin **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduuli** -valintaikkunassa **Tilausvahvistus** -moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna** ja esikatsele sitten mallia valitsemalla **Esikatselu**. Tilauksen vahvistusmoduulia ei hahmonneta, koska se vaatii tilauksen vahvistusnumeron.
1. Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Syötä **Luo uusi sivu** -dialogiruudussa, kohdan **Sivun nimi** alla, **Tilausvahvistussivu** ja valitse sitten **Seuraava**.
1. Valitse **Valitse malli** -kohdan alla **Tilausvahvistusmalli** ja valitse sitten **Seuraava**.
1. Valitse **Valitse asettelu** -kohdassa sivun asettelu (esimerkiksi **Joustava asettelu**) ja valitse sitten **Seuraava**.
1. Tarkista sivun konfigurointi kohdassa **Tarkista ja viimeistele**. Jos haluat muokata sivun tietoja, valitse **Takaisin**. Jos sivun tiedot ovat oikein, valitse **Luo sivu**. 
1. Valitse **Oletussivu**-moduulin **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduuli** -valintaikkunassa **Tilausvahvistus** -moduuli ja valitse sitten **OK**.
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
