---
title: Kassamoduuli
description: Tässä ohjeaiheessa kuvataan, miten kassamoduuli lisätään sivulle ja miten pakolliset ominaisuudet määritetään.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cb32b014ac35e33db28d3dee03b01dfa43f5d6a5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980503"
---
# <a name="checkout-module"></a>Kassamoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kuvataan, miten kassamoduuli lisätään sivulle ja miten pakolliset ominaisuudet määritetään.

## <a name="overview"></a>Yleiskatsaus

Kassamoduuli on erityinen säilö, joka isännöi kaikkia sellaisia moduuleja, jotka tarvitaan tilauksen luomista varten. Se sisältää vaiheittaisen työnkulun, jota käyttämällä asiakas syöttää kaikki tarvittavat tiedot ostoa varten. Se taltioi toimitusosoitteen, toimitustavan ja laskutustiedot. Siinä on myös tilauksen yhteenveto ja muita asiakkaan tilaukseen liittyviä tietoja.

Kassamoduuli hahmontaa tiedot ostoskorin tunnuksen mukaan. Tämä ostoskorin tunnus tallennetaan selaimen evästeeksi. Ostoskorin tunnus on pakollinen, jotta kassamoduulin tiedot kuten tilauksen nimikkeet, kokonaissumma ja alennukset, voidaan hahmontaa. 

Seuraavassa kuvassa on esimerkki Fabrikam-kassamoduulista maksusivulla.

![Esimerkki kassamoduulista](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>Kassamoduulin ominaisuudet

Kassamoduuli näyttää tilauksen yhteenvedon ja tilauksen tekemiseen tarvittavat toiminnot. Kaikkien tilauksen tekemiseen tarvittavien asiakastietojen keräämistä varten kassamoduuliin on lisättävä lisämoduuleja. Niinpä vähittäismyyjät voivat lisätä mukautettuja moduuleja kassatyönkulkuun tai jättää niitä pois omien tarpeiden mukaan.

| Ominaisuuden nimi | Arvot | kuvaus |
|----------------|--------|-------------|
| Kassalle-osan otsikko | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Kassamoduuliin otsikko. |
| Tilauksen yhteenvedon otsikko | Otsikon teksti | Moduulin tilausyhteenveto-osan otsikko. |
| Ostoskorin rivinimikkeiden otsikko | Otsikon teksti | Kassalle-moduulissa näkyvien ostoskorien rivinimikkeiden otsikko. |
| Näytä online-nimikkeen lähetyskulut | **Tosi** vai **Epätosi** | Jos tämän ominaisuuden arvo on **Tosi**, rivinimikkeisiin sovellettavat toimituskulut näytetään ostoskoririveillä. Jos **otsikkomaksu, jossa ei ole suhteellinen jako** -ominaisuutta, on käytössä Commerce Headquarters -sovelluksessa, toimituskuluja käytetään otsikkotasolla, ei rivitasolla. Tämä ominaisuus lisättiin Commercen versioon 10.0.13. |

## <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moduulit, joita voidaan käyttää kassamoduulissa

- **Toimitusosoite** – Tämän moduulin avulla asiakas voi lisätä tai valita tilauksen toimitusosoitteen. Lisätietoja tästä moduulista on kohdassa [Toimitusosoitemoduuli](ship-address-module.md).

    Seuraavassa kuvassa on esimerkki toimitusosoitemoduulista maksusivulla.

    ![Esimerkki toimitusosoitemoduulista](./media/ecommerce-shippingaddress.PNG)

- **Toimitusvaihtoehdot** – Tämän moduulin avulla asiakas voi valita tilauksen toimituksen tilan. Lisätietoja tästä moduulista on kohdassa [Toimitusvaihtoehdot -moduuli](delivery-options-module.md).

    Seuraavassa kuvassa on esimerkki toimitusvaihtoehdot-moduulista maksusivulla.
 
    ![Esimerkki toimitusvaihtoehdot-moduulista](./media/ecommerce-deliveryoptions.PNG)

- **Kassa-osan säilö** – Tämä moduuli on säilö, jonka sisään asetetaan useita moduuleja. Ne luovat osan kassatyönkulun sisälle. Tähän säilöön voi asettaa esimerkiksi kaikki maksuun liittyvät moduulit, jolloin ne näkyvät yhtenä osana. Tämä moduuli vaikuttaa vain työnkulun asetteluun.

- **Lahjakortti** – Tämän moduulin avulla asiakas voi maksaa tilauksen käyttämällä lahjakorttia. Lisätietoja tästä moduulista on kohdassa [Lahjakorttimoduuli](add-giftcard.md).

- **Kanta-asiakkuuspisteet** – Tämän moduulin avulla asiakas voi maksaa tilauksen käyttämällä kanta-asiakkuuspisteitä. Se sisältää yhteenvedon käytettävissä olevista ja vanhenevista pisteistä. Sen avulla asiakas voi valita lunastettavien pisteiden määrän. Jos asiakas ei ole kirjautunut sisään tai ei ole kanta-asiakasohjelman jäsen tai jos ostoskorin kokonaissumma on 0 (nolla), tämä moduuli piilotetaan automaattisesti.

- **Maksu** – Tämän moduulin avulla asiakas voi maksaa tilauksen käyttämällä luotto- tai maksukorttia. Asiakkaat voivat myös määrittää laskutusosoitteen valitsemalleen maksutavalle. Lisätietoja tästä moduulista on kohdassa [Maksumoduuli](payment-module.md).

    Seuraavassa kuvassa on esimerkki lahjakortista, kanta-asiakkuuspisteistä, maksumoduuleista maksusivulla.

    ![Esimerkki lahjakortista, kanta-asiakkuuspisteistä, maksumoduuleista maksusivulla](./media/ecommerce-payments.PNG)

- **Yhteystiedot** – Tämän moduulin avulla asiakas voi lisätä tai muuttaa tilauksen yhteystietoja (sähköpostiosoitetta).

- **Tekstilohko** – Tämä moduuli sisältää kaiken viestinnän, jota sisällönhallintajärjestelmä (CMS) ohjaa. Viestintää voi olla esimerkiksi seuraava viesti: Jos tilaamisessa on ongelmia, soita numeroon 1-800-Fabrikam. 

- **Kassan käyttöehdot** – Tässä moduulissa näkyy RTF-teksti, joka sisältää käyttöehdot sekä asiakkaan syötön valintaruudun. Valintaruutu on valinnainen ja konfiguroitavissa. Moduuli ottaa syötteen talteen, ja sitä voidaan käyttää tarkistuksena ennen tilauksen tekemistä, mutta se ei sisälly tilauksen yhteenvetotietoihin. Tämä moduuli voidaan lisätä kassalaatikkoon, kassaosastolaatikkoon tai käyttöehdot-kohtaan liiketoiminnan tarpeiden mukaan. Jos se lisätään kassalaatikkoon tai kassaosastolaatikkopaikkaan, se näkyy vaiheena kassalle mentäessä. Jos se lisätään käyttöehdot-paikkaan, se näkyy tilauksen teko -painikkeen lähellä.

    Seuraavassa kuvassa on esimerkki käyttöehdoista maksusivulla.

    ![Esimerkki käyttöehdoista kassalla](./media/ecommerce-checkout-terms.PNG)

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit -käyttö

Useimmat kassatiedot, kuten toimitusosoite ja toimitustapa, tallennetaan ostoskoriin. Niitä käsitellään tilauksen osana. Ainoa poikkeus on luottokorttitiedot. Nämä tiedot käsitellään suoraan Adyen-maksuyhdistimen avulla. Maksu on valtuutettu, mutta sitä ei veloiteta, ennen kuin tilaus on täytetty.

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>Lisää kassamoduuli sivulle ja määritä pakolliset ominaisuudet

Voit lisätä kassamoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Osat** ja **Uusi** luodaksesi uuden osan.
1. Valitse **Uusi osa** -valintaikkunassa **Kassa**-moduuli.
1. Kirjoita **Osan nimi** -kohtaan **Kassaosa** ja valitse sitten **OK**.
1. Valitse **Kassamoduuli**-paikka.
1. Valitse oikealla olevassa ominaisuudet-ruudussa kynäsymboli, kirjoita otsikko tekstikenttään ja valitse sitten valintamerkkisymboli.
1. Valitse **Kassatiedot**-paikassa kolmen pisteen painike (**…**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Toimitusosoite**, **Toimitusasetukset**, **Kassaosiokontti** ja **Yhteystieto**-moduulit ja valitse sitten **OK**.
1. Valitse **Kassaosiokontti**-moduulissa kolmen pisteen painike (**…**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunan **Lahjakortti**-, **Kanta-asiakkuus**- ja **Maksu**-moduulit ja valitse sitten **OK**. Tällä tavoin varmistat, että kaikki maksutavat näkyvät yhdessä osassa.
1. Lisää **Käyttöehdot**-moduuliin **Kassan käyttöehdot** -moduuli, jos se on tarpeen. Määritä moduulin ominaisuudet -ruudussa käyttöehtojen teksti tarpeen mukaan.
1. Valitse **Tallenna** ja esikatsele sitten osaa valitsemalla **Esikatselu**. Joitakin moduuleista ei ehkä hahmonneta esikatselussa, koska niissä ei ole ostoskorikontekstia.
1. Valitse **Lopeta muokkaus** tallentaaksesi osan ja valitse sitten **Julkaise** julkaistaksesi sen.
1. Luo malli, joka käyttää uutta kassaosaa.
1. Luo kassasivu, joka käyttää uutta mallia.

## <a name="additional-resources"></a>Lisäresurssit

[Ostoskorimoduuli](add-cart-module.md)

[Ostoskorikuvakemoduuli](cart-icon-module.md)

[Maksumoduuli](payment-module.md)

[Toimitusosoitemoduuli](ship-address-module.md)

[Toimitusvaihtoehtomoduuli](delivery-options-module.md)

[Noudon tiedot -moduuli](pickup-info-module.md)

[Tilauksen tiedot -moduuli](order-confirmation-module.md)

[Lahjakorttimoduuli](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]