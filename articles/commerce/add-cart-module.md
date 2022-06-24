---
title: Ostoskorimoduuli
description: Tässä artikkelissa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.openlocfilehash: c4023857f13830449eaa19f8513799ece97729d8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866053"
---
# <a name="cart-module"></a>Ostoskorimoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

Ostokorimoduuli näyttää ostoskoriin lisätyt nimikkeet ennen asiakkaan siirtymistä kassalle. Moduuli näyttää myös tilauksen yhteenvedon ja asiakas voi käyttää tarjouskoodeja tai poistaa niitä.

Ostoskorimoduuli tukee kirjautuneiden kassan käyttämistä kirjautuneena ja vieraana. Se tukee myös **Jatka ostoksia** -linkkejä. Voit määrittää tämän linkin reitin valitsemalla **Sivuston asetukset \> Laajennukset \> Reitit**.

Ostoskorimoduuli esittää tiedot ostoskorin tunnuksen mukaan, joka on koko sivuston käytettävissä oleva selaineväste. 

Seuraavassa kuvassa on esimerkki Fabrikam-sivuston ostoskärrysivusta.

![Esimerkki ostoskorimoduulista Fabrikam-sivustolla.](./media/cart2.PNG)

Seuraavassa kuvassa on esimerkki Fabrikam-sivuston ostoskärrysivusta. Tässä esimerkissä rivinimikkeelle on käsittelymaksu.

![Esimerkki ostoskorimoduulista, jossa on käsittelymaksu rivinimikkeelle.](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a>Ostoskorimoduulin ominaisuudet ja paikat

| Ominaisuus | Arvot | kuvaus |
|----------------|--------|-------------|
| Otsikko | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Otsikko ostoskorille, kuten Ostoskassi tai Ostoskorin nimikkeet. |
| Näytä Loppunut varastosta -virheet | **Tosi** vai **Epätosi** | Jos tämän ominaisuuden arvo on **Tosi**, ostoskori-sivulla näkyvät varastoon liittyvät virheet. On suositeltavaa määrittää tämän ominaisuuden arvoksi **Tosi**, jos varastotarkistuksia käytetään toimipaikassa. |
| Näytä rivinimikkeiden kuljetusmaksut | **Tosi** vai **Epätosi** | Jos tämän ominaisuuden arvo on **Tosi**, ostoskorin rivinimikkeissä näkyy kuljetusmaksut, jos nämä tiedot ovat käytettävissä. Tämä toiminto ei ole tuettu Fabrikam-teemassa, koska käyttäjät valitsevat lähetyksen vain kassavirrasta. Tämä toiminto voidaan kuitenkin ottaa käyttöön muissa työnkuluissa, jos se on sovellettavissa. |
| Näytä käytettävissä olevat kampanjat| **Tosi** vai **Epätosi** | Jos ominaisuuden arvoksi määritetään **Tosi**, ostoskorissa näkyvät käytettävissä olevat kampanja-tarjoukset kärryssä olevien nimikkeiden mukaan. Tämä ominaisuus on saatavana Dynamics 365 Commercen versiossa 10.0.16. |

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduulit, joita voidaan käyttää ostoskorimoduulissa

- **Tekstilohko** – Tämä moduuli tukee mukautettua viestintää ostoskorimoduulissa. Sisällönhallintajärjestelmä (CMS) ohjaa viestintää. Voit lisätä minkä tahansa viestin, esimerkiksi Jos tilauksessa on ongelmia, soita numeroon 1-800-Fabrikam.
- **Myymälän valitsin** – Tämä moduuli näyttää luettelon lähellä olevista myymälöistä, joista nimikkeen voi noutaa. Käyttäjät voivat etsiä lähellä olevia myymälöitä antamalla sijainnin. Lisätietoja tästä moduulista on kohdassa [Kaupan valitsinmoduuli](store-selector.md).

## <a name="module-properties"></a>Moduulin ominaisuudet

Seuraavat ostoskorimoduuliasetukset voidaan määrittää valitsemalla **Sivuston asetukset \> Laajennukset**:

- **Maksimimäärä** – Tätä ominaisuutta käytetään määrittämään kunkin ostoskoriin lisättävän nimikkeen enimmäismäärä. Jälleenmyyjä voi esimerkiksi päättää, että yhdessä tapahtumassa voidaan myydä vain 10 kappaletta kutakin tuotetta.
- **Varasto** – lisätietoja varastoasetusten ottamisesta käyttöön on kohdassa [Varastoasetusten käyttäminen](inventory-settings.md).
- **Jatka ostoksia** – Tällä ominaisuudella määritetään **Jatka ostoksia** -linkin reitti. Reitti voidaan konfiguroida sivuston tasolla, jolloin jälleenmyyjät voivat ohjata asiakkaan takaisin kotisivulle tai mille tahansa muulle sivuston sivulle.

> [!IMPORTANT]
> Dynamics 365 Commerce versiossa 10.0.14 ja sitä uudemmissa versioissa nimikkeet kerätään ostoskoriin Commercen pääkonttoriversion verkkokaupan verkkotoimintoprofiilissa määritettyjen asetusten perusteella. Lisätietoja verkkotoimintoprofiilin luomisesta ja koostamiseen tarvittavien ominaisuuksien määrittämisestä on kohdassa [Verkkotoimintoprofiilin luominen](online-functionality-profile.md).

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit -käyttö

Ostoskorimoduuli hakee tuotetiedot Commerce Scale Unitin ohjelmistorajapintojen avulla. Selaimen evästeen ostoskorin tunnusta käytetään kaikkien tuotetietojen noutamisessa Commerce Scale Unitista.

## <a name="add-a-cart-module-to-a-page"></a>Ostoskorimoduulin lisääminen sivulle

Voit lisätä ostoskorimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Osat** ja **Uusi** luodaksesi uuden osan.
1. Valitse **Valitse katkelma** -valintaikkunassa **Ostoskori**-moduuli.
1. Kirjoita **Osan nimi** -kohtaan **Ostoskorin osa** ja valitse sitten **OK**.
1. Valitse **Ostoskori**-paikka.
1. Valitse oikealla olevassa ominaisuudet-ruudussa kynäsymboli, kirjoita otsikko tekstikenttään ja valitse sitten valintamerkkisymboli.
1. Valitse kolme pistettä (**...**) **Ostoskori**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduuli** -valintaikkunassa **Myymälävalitsin**-moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.
1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan mallin nimi.
1. Valitse jäsennyspuussa **Tekstiosa**-paikka. Valitse kolme pistettä (**...**) ja valitse sitten **Lisää osa**.
1. Valitse **Valitse osa** -valintaikkunassa **Ostoskorin osa** ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Valitse **Valitse malli** -valintaikkunassa malli, jonka loit aiemmin, lisää sivun nimi ja valitse sitten **OK**.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="additional-resources"></a>Lisäresurssit

[Ostoskorikuvakemoduuli](cart-icon-module.md)

[Kassamoduuli](add-checkout-module.md)

[Maksumoduuli](payment-module.md)

[Toimitusosoitemoduuli](ship-address-module.md)

[Toimitusvaihtoehtomoduuli](delivery-options-module.md)

[Noudon tiedot -moduuli](pickup-info-module.md)

[Tilauksen tiedot -moduuli](order-confirmation-module.md)

[Lahjakorttimoduuli](add-giftcard.md)

[Vähittäismyyntikanavien varaston käytettävyyden laskeminen](calculated-inventory-retail-channels.md)

[Luo online-toimintoprofiili](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
