---
title: Lahjakorttimoduuli
description: Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7fc35c67a2d9b641f03f11ed5d06913e10d8e25b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347491"
---
# <a name="gift-card-module"></a>Lahjakorttimoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

Lahjakorttimoduuleja voi käyttää kassamoduuleissa lahjakorttien hyväksynnässä. Se on yleinen maksumuoto, jota käytetään sähköisen kaupankäynnin tapahtumissa. Lahjakorttimoduuli tukee Dynamics 365-, SVS- ja Givex-lahjakortteja. SVS- ja Givex-lahjakortit lunastetaan Adyen-maksupalveluntarjoajan kautta. Lisätietoja ulkoisten lahjakorttien, kuten SVS:n ja Givexin tuesta, on ohjeaiheessa [Ulkoisten lahjakorttien tuki](./dev-itpro/gift-card.md).

> [!NOTE]
> Tuki SVS- ja Givex-lahjakorttien lunastamiselle kassatyönkulussa on käytettävissä Dynamics 365 Commercen versiossa 10.0.11. 

Käytettävissä on seuraavat kaksi lahjakorttimoduulia:

- **Lahjakortti** – Tätä moduulia voi käyttää kassasivulla lunastettaessa lahjakortti maksuvälineenä. 
- **Lahjakortin saldon tarkistus** – Tätä moduulia voi käyttää millä tahansa sivulla, kun halutaan tarkistaa lahjakortin saldo. Tämä moduuli on käytettävissä Commercen versiossa 10.0.14 ja uudemmissa versioissa.

> [!NOTE]
> Lahjakortin saldontarkistusmoduulin tuki on saatavilla Dynamics 365 Commercen versiossa 10.0.14.

Seuraavassa kuvassa on esimerkki lahjakorttimoduulista maksusivulla.

![Esimerkki lahjakorttimoduulista.](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Moduulin ominaisuudet

- **Näytä lisäkentät** – Tämä ominaisuus määrittää, mitkä lahjakorttien kentät näytetään aina oletusarvoisesti näytettävän lahjakortin numeron lisäksi. Esimerkiksi jotkin lahjakortit tukevat henkilökohtaista tunnuslukua (PIN), ja toiset tukevat PIN-koodin ja vanhentumispäivämäärän näyttämistä. Vaihtoehtoisesti tämän ominaisuuden arvoksi voi määrittää "Ei mitään", jolloin näytetään vain lahjakortin numero eikä muita kenttiä näy.

Tuetut arvot:
-   PIN-koodi
-   Vanhentumispäivä
-   PIN-koodi ja vanhentumispäivä 
-   None

## <a name="site-settings-for-gift-card-modules"></a>Lahjakorttimoduulien toimipaikan asetukset

Kauppapaikan luomistyökalussa **Sivuston asetukset \> -laajennukset** -kohdassa on lahjakorttimoduulin asetus nimeltä **Tuettu lahjakorttityyppi**. Tämä asetus tukee kolmea arvoa:
- **Dynamics 365 -lahjakortti** – Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365 -lahjakorttien lunastamisen. Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.
- **SVS- ja Givex-lahjakortit** – Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain SVS- ja Givex-lahjakorttien lunastamisen. Tätä asetusta tuetaan kirjautuneiden ja anonyymien käyttäjien verkkokauppasivustossa.
- **Dynamics 365-, SVS- ja Givex-lahjakortit** – Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365-, SVS- ja Givex-lahjakorttien lunastamisen. Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.

> [!IMPORTANT]
> Nämä asetukset ovat käytettävissä Dynamics 365 Commercen versiossa 10.0.11-versiossa, ja niitä tarvitaan vain, jos tarvitset tukea SVS- tai Givex-lahjakorteille. Jos päivität vanhemmasta Dynamics 365 Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti. Ohjeet appsettings.json-tiedoston päivittämiseen: [SDK:n ja moduuliskirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a>Sisäisten lahjakorttien laajennus sähköisen kaupankäynnin verkkokauppoihin

Sisäiset lahjakortit eivät ole oletusarvoisesti optimoituja sähköisen kaupankäynnin verkkokauppoja varten. Siksi ennen kuin sallit sisäisillä lahjakorteilla maksamisen, ne on määritettävä laajennuksilla, jotta ne ovat suojatumpia. Ennen sisäisten lahjakorttien käyttöä tuotannossa on hyvä laajentaa seuraavia lahjakorttialueita:

- **Lahjakortin numero** – Numerosarjojen avulla luodaan lahjakorttien numerot sisäisille lahjakorteille. Koska numerosarjoja voidaan helposti ennakoida, lahjakorttien numeroiden luontia tulisi laajentaa siten, että myönnettyjen lahjakorttien numeroissa käytetään satunnaisia, kryptografisesti suojattuja merkkijonoja.
- **GetBalance** – **GetBalance**-ohjelmointirajapintaa käytetään lahjakorttien saldojen etsimiseen. Oletusarvon mukaan tämä ohjelmointirajapinta on julkinen. Jos PIN-koodia ei tarvita lahjakorttien saldojen etsimiseen, on mahdollista, että väsytyshyökkäykset saattavat käyttää **GetBalance**-ohjelmointirajapintaa etsiäkseen niiden lahjakorttien numeroita, joissa on saldoa. Kun otat käyttöön molemmat sisäisten lahjakorttien ja ohjelmointirajapinnan rajoittamisen PIN-vaatimukset käyttöön, voit pienentää riskiä.
- **PIN** – Sisäiset lahjakortit eivät oletusarvoisesti tue PIN-koodia. Laajenna sisäiset lahjakortit niin, että saldojen etsimiseen tarvitaan PIN-koodi. Näitä toimintoja voidaan käyttää myös lahjakorttien lukitsemaan sen jälkeen, kun PIN-koodia on yritetty kirjoittaa virheellisesti monta kertaa peräkkäin.

## <a name="enable-gift-card-payments-for-guest-checkout"></a>Lahjakorttimaksujen käyttöönotto vieraan uloskuittausta varten

Oletusarvon mukaan lahjakorttimaksut eivät ole käytössä vieraan (anonyymi) uloskuittauksessa. Ne otetaan käyttöön seuraavasti.

1. Siirry Commerce headquartersissa kohtaan **Retail ja Commerce \> Kanavan asetukset \> Myyntipisteen asetukset \> Myyntipiste \> Myyntipistetoiminnot**.
1. Valitse ja pidä valittuna (tai valitse hiiren kakkospainikkeella) ruudukon otsikko ja valitse sitten **Lisää sarakkeita**.
1. Valitse **Lisää sarakkeita** -valintaikkunassa **AllowAnonymousAccess**-valintaruutu.
1. Valitse **Päivitä**.
1. Toiminnoille **520** (lahjakortin saldo) ja **214**, määritä **AllowAnonymousAccess**-arvoksi **1**.
1. Valitse **Tallenna**.
1. Suorita **1090**-ajoitustoiminto, kun synkronoit muutokset kanavatietokannan kanssa. 

## <a name="add-a-gift-card-module-to-a-page"></a>Lahjakorttimoduulin lisääminen sivulle

Lisätietoja lahjakorttimoduulin lisäämisestä kassasivulle ja tarvittavien ominaisuuksien määrittämisestä on kohdassa [Kassamoduuli.](add-checkout-module.md).

## <a name="additional-resources"></a>Lisäresurssit

[Ostoskorimoduuli](add-cart-module.md)

[Ostoskorikuvakemoduuli](cart-icon-module.md)

[Kassamoduuli](add-checkout-module.md)

[Maksumoduuli](payment-module.md)

[Toimitusosoitemoduuli](ship-address-module.md)

[Toimitusvaihtoehtomoduuli](delivery-options-module.md)

[Noudon tiedot -moduuli](pickup-info-module.md)

[Tilauksen tiedot -moduuli](order-confirmation-module.md)

[Ulkoisten lahjakorttien tuki](./dev-itpro/gift-card.md)

[SDK:n ja moduulikirjaston päivitykset](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
