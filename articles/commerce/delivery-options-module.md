---
title: Toimitusvaihtoehdot -moduuli
description: Tässä ohjeaiheessa on tietoja toimitusvaihtoehtomoduuleista ja niiden määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
author: anupamar-ms
ms.date: 02/24/2022
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
ms.openlocfilehash: 9b9a7ad05974b98511cfc582af62c19c5fb4dbf5
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349791"
---
# <a name="delivery-options-module"></a>Toimitusvaihtoehtomoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja toimitusvaihtoehtomoduuleista ja niiden määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.

Toimitusasetukset-moduulien avulla asiakkaat valitsevat toimitustavan, kuten lähetys tai nouto verkossa tehdylle tilaukselleen. Toimitusosoite on pakollinen, jotta lähetystapa voidaan määrittää. Jos toimitusosoite muuttuu, toimitusvaihtoehdot on noudettava uudelleen. Jos tilauksessa on vain myymälästä noudettavia nimikkeitä, tämä moduuli piilotetaan automaattisesti.

Lisätietoja toimitustapojen määrittämisestä on ohjeaiheissa [Online-kanavan määrittäminen](channel-setup-online.md) ja [Toimitustapojen määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Kullakin toimitustilalla voi olla siihen liittyvä maksu. Lisätietoja verkkokaupan maksujen määrittämisestä on kohdassa [Monikanavaiset edistyneet automaattiset veloitukset](omni-auto-charges.md).

Commercen version 10.0.13 toimitusvaihtoehdot-moduuli on päivitetty siten, että se tukee **otsikkokulut ilman suhteellisuutta**- ja **lähetystoiminnot rivikuluina** -ominaisuuksia. Jos suhteutus on poistettu käytöstä, on odotettavissa, että verkkokaupan työnkulku ei salli sekalaista toimitusta ostoskorin nimikkeille (eli jotkin nimikkeet valitaan lähetettäväksi, mutta toiset valitaan noudettavaksi). **Otsikkoveloitukset ilman suhteutusta** -ominaisuus edellyttää, että **Ota käyttöön yhdenmukainen toimitustilan käsittelykanava** -lippu on käytössä Commerce Headquarters -sovelluksessa. Kun ominaisuuden lippu on käytössä, lähetysmaksut joko otetaan käyttöön joko otsikkotasolla tai rivitasolla riippuen Commerce Headquarters -kokoonpanosta.

Fabrikam-teema tukee moniosaista toimitustapaa, jossa tietyt nimikkeet valitaan lähetystä varten, mutta toiset valitaan noutoa varten. Tässä tilassa kuljetusmaksut jaetaan kaikille nimikkeille, jotka on valittu toimitustapaa varten. Jos haluat käyttää moniosaista toimitustapaa, sinun on ensin konfiguroitava **Otsikon kulut suhteutettuna** -ominaisuus Commerce Headquarters -sovelluksessa. Lisätietoja tästä konfiguraatiosta on kohdassa [Kohdista otsikkoveloitukset myyntirivien mukaisiksi](pro-rate-charges-matching-lines.md).

Jos rivinimikkeisiin sovelletaan kuljetusmaksuja, ne voidaan näyttää kunkin nimikkeen ostoskorissa. Tämä toiminto edellyttää, että **Näytä lähetyskulut rivinimikkeellä** -ominaisuus otetaan käyttöön sekä ostoskori- että kassalle-moduulissa. Lisätietoja on kohdissa [Ostoskorimoduuli](add-cart-module.md) ja [Kassamoduuli](add-checkout-module.md).

Seuraavassa kuvassa on esimerkki toimitusvaihtoehdot-moduulista maksusivulla.

![Esimerkki toimitusvaihtoehdot-moduulista maksusivulla.](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a>Toimitusvaihtoehdot-moduulin ominaisuudet

| Ominaisuus | Arvot | kuvaus |
|----------|--------|-------------|
| Otsikko | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Toimitusasetukset-moduulin valinnainen otsikko. |
| Mukautetun CSS-luokan nimi | Teksti | Mukautetun CSS-tyylisivut (CSS)-luokan nimi, jota käytetään tarvittaessa tämän moduulin muodostamiseen. |
| Toimitustavan suodatus -vaihtoehto | **Älä Suodata** tai **Ei-lähetys-tilat** | Arvo, joka määrittää, suodatetaanko toimitusasetukset-moduulissa kaikki muut kuin lähetyksen toimitustilat. |
| Toimitusvaihtoehdon automaattinen valinta | **Älä suodata**, **Valitse toimitusvaihto automaattisesti ja näytä yhteenveto** tai **Valitse toimitusvaihto automaattisesti ja älä näytä yhteenvetoa** | Tämä ominaisuus käyttää automaattisesti ensimmäistä käytettävissä olevaa toimitusvaihtoehtoa uloskuittaukseen ilman, että käyttäjän pitää valita se. Sitä tulee käyttää vain, jos toimitusvaihtoehtoja on yksi. Tätä ominaisuutta tuetaan Commerce-version 10.0.19 julkaisusta alkaen. |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a>Lisää toimitusvaihtoehdot-moduuli kassalle-sivulle ja määritä pakolliset ominaisuudet

Toimitusvaihtoehdot-moduuli voidaan lisätä vain kassalle-moduuliin. Lisätietoja toimitusasetukset-moduulin konfiguroinnista ja lisäämisestä kassalle-sivulle on kohdassa [kassalle-moduuli](add-checkout-module.md).

> [!NOTE]
> Toimitusten käsittely saattaa olla ristiriitainen tai verkkokauppakanavasi ei ehkä näytä ei-luokiteltuja otsikkotason maksuja. Ohjeita näiden ongelmien korjaamisesta on kohdassa [Ota käyttöön yhdenmukainen toimitustilan käsittely sähköisen kaupankäynnin kanavissa](consistent-delivery-mode-handling.md).

## <a name="additional-resources"></a>Lisäresurssit

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Maksumoduuli](payment-module.md)

[Toimitusosoitemoduuli](ship-address-module.md)

[Noudon tiedot -moduuli](pickup-info-module.md)

[Tilauksen tiedot -moduuli](order-confirmation-module.md)

[Lahjakorttimoduuli](add-giftcard.md)

[Online-kanavan määritys](channel-setup-online.md)

[Omnikanavan automaattiset etukäteisveloitukset](omni-auto-charges.md)

[Otsikon kulujen suhteellinen jakaminen vastaaville myyntiriveille](pro-rate-charges-matching-lines.md)

[Määritä toimitustavat](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
