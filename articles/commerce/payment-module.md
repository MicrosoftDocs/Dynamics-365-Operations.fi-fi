---
title: Maksumoduuli
description: Tässä ohjeaiheessa on tietoja maksumoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
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
ms.openlocfilehash: 4267391edaf70ec645933b2c5c08a72735f52894
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818323"
---
# <a name="payment-module"></a>Maksumoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja maksumoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.

## <a name="overview"></a>Yhteenveto

Maksumoduulin avulla asiakkaat voivat maksaa tilaukset käyttämällä luotto- tai maksukortteja. Maksun integroinnin tässä moduulissa tarjoaa Dynamics 365 -maksuyhdistin Adyenille. Lisätietoja maksuyhdistimen asentamisesta ja määrittämisestä on kohdassa [Dynamics 365 -maksuyhdistin Adyenille](dev-itpro/adyen-connector.md).

Maksumoduuli isännöi Adyen-nimisen HTML-kehyksen (iframe) kautta tarjottuun maksuun liittyviä tietoja. Maksumoduuli toimii yhdessä Commerce Scale Unitin kanssa noutaakseen Adyen-maksuja koskevat tiedot. Osana Commerce Scale Unitin vuorovaikutusta maksumoduuli voi sallia, että laskutusosoite tiedot voidaan antaa joko iframe-muodossa tai erillisenä moduulina. Fabrikam-teeman laskutusosoite näkyy erillisessä moduulissa. Tämä lähestymistapa mahdollistaa muotoilun joustavuuden, koska osoiterivit voidaan muodostaa niin, että ne muistuttavat toimitusosoitteen rivejä.

Myös sisäänkirjautuneena olevat asiakkaat tallentavat maksatustietonsa. Maksutiedot ja laskutusosoite tallennetaan ja niitä hallitaan Adyen-maksuyhdistimen kautta.

Maksumoduuli kattaa kaikki tilauskulut, jotka eivät kuulu kanta-asiakkuuspisteiden tai lahjakortin piiriin. Jos tilauksen kokonaissumma on täysin kanta-asiakkuus pisteiden tai lahjakorttien hyvitysten peittämä, maksatusmoduuli piilotetaan ja asiakas voi tehdä tilauksen ilman sitä.

Adyen-yhdistin tukee myös asiakkaan vahvaa todennusta (SCA). Osa Euroopan unionin (EU) maksupalveludirektiivistä 2.0 (PSD2.0) edellyttää, että online-ostajat todennetaan verkko-ostoskokemuksensa ulkopuolella, kun he käyttävät sähköistä maksutapaa. Kassatyönkulun aikana asiakkaat ohjataan pankkisivustolle. Sitten todennuksen jälkeen ne ohjataan takaisin Commerce Checkout -työnkulkuun. Tämän uudelleenohjauksen aikana asiakkaan kassatyönkulkuun syötetyt tiedot (esimerkiksi toimitusosoite, toimitusvaihtoehdot, lahjakorttitiedot ja kanta-asiakastiedot) säilyvät ennallaan. Ennen kuin voit ottaa tämän toiminnon käyttöön, maksuyhteys on konfiguroitava SCA:lle Commerce Headquarters -sovelluksessa. Lisätietoja on kohdassa [vahva asiakastodennus käyttäen Adyen-sovellusta](adyen_redirect.md).

Seuraavassa kuvassa on esimerkki lahjakortista, kanta-asiakkuudesta ja maksumoduuleista maksusivulla.

![Esimerkki lahjakortista, kanta-asiakkuudesta ja maksumoduuleista maksusivulla](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a>Maksumoduulin ominaisuudet

| Ominaisuuden nimi | Arvot | kuvaus |
|---------------|--------|-------------|
| Otsikko | Otsikon teksti | Maksumoduulin valinnainen otsikko. |
| Iframen korkeus | Pikseliä | Iframe-kentän korkeus kuvapisteinä. Korkeutta voi muuttaa tarvittaessa. |
| Näytä laskutusosoite | **Tosi** vai **Epätosi** | Jos tämän ominaisuuden arvo on **Tosi**, laskutusosoite näytetään Adyen-maksumoduulin iframe-ohjelman sisällä. Jos arvo on **Epätosi**, laskutusosoitetta ei näytetä Adyenissa, ja Commerce-käyttäjän on konfiguroitava moduuli näyttämään laskutusosoite kassasivulla. |
| Maksun tyylin ohitus | CSS-tyylisivut (CSS) -koodi | Koska maksumoduulia isännöidään iframe-ohjelmassa, muotoiluominaisuus on rajallinen. Voit saavuttaa joitakin muotoiluja käyttämällä tätä ominaisuutta. Sivuston tyylien ohittaminen edellyttää, että liität CSS-koodin tämän ominaisuuden arvoksi. Sivuston muodostimen CSS-ohitukset ja tyylit eivät koske tätä moduulia. |

## <a name="billing-address"></a>Laskutusosoite

Maksumoduulin avulla asiakkaat voivat antaa laskutusosoitteen maksutiedoille. Sen avulla he voivat myös käyttää toimitusosoitetta laskutusosoitteena, jotta kassatyönkulku sujuisi helpommin ja nopeammin. Jos **Näytä laskutusosoite** -ominaisuuden arvo on **Epätosi**, maksumoduuli tulee määrittää kassalle-sivulla.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Lisää maksumoduuli kassasivulle ja määritä pakolliset ominaisuudet

Maksumoduuli voidaan lisätä vain kassalle-moduuliin. Lisätietoja maksumoduulin määrittämisestä kassasivulle on kohdassa [Kassamoduuli](add-checkout-module.md).

## <a name="additional-resources"></a>Lisäresurssit

[Ostoskorimoduuli](add-cart-module.md)

[Ostoskorikuvakemoduuli](cart-icon-module.md)

[Kassamoduuli](add-checkout-module.md)

[Toimitusosoitemoduuli](ship-address-module.md)

[Toimitusvaihtoehdot -moduuli](delivery-options-module.md)

[Tilauksen tiedot -moduuli](order-confirmation-module.md)

[Lahjakorttimoduuli](add-giftcard.md)

[Dynamics 365 -maksuyhdistin Adyenia varten](dev-itpro/adyen-connector.md)

[Asiakkaan vahva todennus Adyen-yhdistimellä](adyen_redirect.md)
