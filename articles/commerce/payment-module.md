---
title: Maksumoduuli
description: Tässä artikkelissa on tietoja maksumoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
author: anupamar-ms
ms.date: 04/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: fa1482cb73a40df5f9bc9d3037196def71accf18
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279472"
---
# <a name="payment-module"></a>Maksumoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja maksumoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.

Maksumoduulin avulla asiakkaat voivat maksaa tilaukset käyttämällä luotto- tai maksukortteja. Maksun integroinnin tässä moduulissa tarjoaa Dynamics 365 -maksuyhdistin Adyenille. Lisätietoja maksuyhdistimen asentamisesta ja määrittämisestä on kohdassa [Dynamics 365 -maksuyhdistin Adyenille](dev-itpro/adyen-connector.md).  

Commerce-julkaisusta 10.0.14 eteenpäin maksumoduuli on myös integroitu Dynamics 365:n PayPal -maksuyhdistimen kanssa, jotta asiakkaat voivat maksaa tilauksista PayPalin kautta. Lisätietoja Dynamics 365:n Paypal -maksuyhdistimen asentamisesta ja määrittämisestä on kohdassa [Dynamics 365 -maksuyhdistin PayPalia varten](paypal.md). 

## <a name="dynamics-365-payment-connector-for-adyen"></a>Dynamics 365 -maksuyhdistin Adyenia varten 

Maksumoduuli isännöi Adyen-nimisen HTML-kehyksen (iframe) kautta tarjottuun maksuun liittyviä tietoja. Maksumoduuli toimii yhdessä Commerce Scale Unitin kanssa noutaakseen Adyen-maksuja koskevat tiedot. Osana Commerce Scale Unitin vuorovaikutusta maksumoduuli voi sallia, että laskutusosoite tiedot voidaan antaa joko iframe-muodossa Adyenin kautta tai erillisenä moduulina. Fabrikam-teeman laskutusosoite on otettu käyttöön erillisenä moduulina. Tämä lähestymistapa mahdollistaa muotoilun joustavuuden, koska osoiterivit voidaan muodostaa niin, että ne muistuttavat toimitusosoitteen rivejä.

Myös sisäänkirjautuneena olevat asiakkaat tallentavat maksatustietonsa. Maksutiedot ja laskutusosoite tallennetaan ja niitä hallitaan Adyen-maksuyhdistimen kautta.

Maksumoduuli kattaa kaikki tilauskulut, jotka eivät kuulu kanta-asiakkuuspisteiden tai lahjakortin piiriin. Jos tilauksen kokonaissumma on täysin kanta-asiakkuus pisteiden tai lahjakorttien hyvitysten peittämä, maksatusmoduuli piilotetaan ja asiakas voi tehdä tilauksen ilman sitä.

Adyen-yhdistin tukee myös asiakkaan vahvaa todennusta (SCA). Osa Euroopan unionin (EU) tarkistetusta maksupalveludirektiivistä (PSD2) edellyttää, että online-ostajat todennetaan verkko-ostoskokemuksensa ulkopuolella, kun he käyttävät sähköistä maksutapaa. Kassaprosessin aikana asiakkaat ohjataan pankkisivustolle, ja sitten todennuksen jälkeen heidät ohjataan takaisin Commerce-kassaprosessiin. Tämän uudelleenohjauksen aikana asiakkaan kassaprosessin aikana syötetyt tiedot (esimerkiksi toimitusosoite, toimitusvaihtoehdot, lahjakorttitiedot ja kanta-asiakastiedot) säilyvät ennallaan. Ennen kuin voit ottaa Adyen-maksuyhdistintoiminnon käyttöön, maksuyhteys on konfiguroitava SCA:lle Commerce Headquarters -sovelluksessa. Lisätietoja on kohdassa [vahva asiakastodennus käyttäen Adyen-sovellusta](adyen_redirect.md). Tämä ominaisuus otettiin käyttöön Commercen versiossa 10.0.12.

> [!NOTE]
> Adyen-maksuyhdistimessä maksumoduulin iframe-moduuli voidaan hahmontaa vain, jos Adyenin URL-osoite lisätään sivuston sallittujen luetteloon. Viimeistele tämä vaihe lisäämällä **\*.adyen.com** sivuston sisällön suojauskäytännön direktiiveihin **child-src**, **connect-src**, **img-src**, **script-src** ja **style-src**. Lisätietoja on kohdassa [Sisällön suojauskäytännön hallinta](manage-csp.md). 

Seuraavassa kuvassa on esimerkki lahjakortista, kanta-asiakkuudesta ja Adyen-maksumoduuleista maksusivulla.

![Esimerkki lahjakortista, kanta-asiakkuuspisteistä, Adyen-maksumoduuleista maksusivulla.](./media/ecommerce-payments.PNG)

## <a name="dynamics-365-payment-connector-for-paypal"></a>Dynamics 365 Payment Connector PayPalia varten

Commerce-versiosta 10.0.14 alkaen maksumoduuli on integroitu myös Dynamics 365:n PayPal-maksuyhdistimen kanssa. Lisätietoja tämän maksuyhdistimen asentamisesta ja määrittämisestä on kohdassa [Dynamics 365 -maksuyhdistin Paypalille](paypal.md).
 
Kassasivulla voit määrittää sekä Adyen- että PayPal-liittimet. Maksumoduulia on parannettu lisäominaisuuksilla, joiden avulla voidaan selvittää, mitä liitintä sen pitäisi käsitellä. Lisätietoja on seuraavan taulukon **Tuetut maksuvälinetyypit**- ja **On ensisijainen maksu** -moduuliominaisuuksissa.
  
Kun maksumoduuli on määritetty käyttämään PayPal-maksuliitintä, kassasivulla näkyy PayPal-painike. Kun asiakas on käynnistänyts en, maksumoduuli muodostaa PayPal-tietoja sisältävän iframen. Asiakas voi kirjautua sisään ja antaa PayPal-tietonsa tässä iframessa tapahtuman suorittamiseksi. Kun asiakas päättää maksaa PayPalilla, tilauksen jäljellä oleva saldo veloitetaan PayPalin kautta.

PayPal-maksuyhdistin ei edellytä laskutusosoitemoduulia, koska PayPal käsittelee kaikki laskutukseen liittyvät tiedot iframen sisällä. Toimitusosoite- ja toimitusvaihtoehdot -moduulit ovat kuitenkin pakollisia.

Seuraavassa kuvassa on esimerkki kahdesta maksumoduulista kassasivulla, joista toinen on määritetty Adyen-maksuyhdistimellä ja toinen PayPal-maksuyhdistimellä.
![Esimerkki Adyen- ja PayPal-maksumoduuleista maksusivulla.](./media/ecommerce-paypal.png)

Seuraavassa kuvassa on esimerkki PayPal-iframesta, joka on käynnistetty PayPal-painikkeen avulla. 
![Esimerkki Paypal-iframesta kassasivulla.](./media/ecommerce-paypal-iframe.png)

## <a name="payment-module-properties"></a>Maksumoduulin ominaisuudet

| Ominaisuuden nimi | Arvot | kuvaus |
|---------------|--------|-------------|
| Otsikko | Otsikon teksti | Maksumoduulin valinnainen otsikko. |
| Iframen korkeus | Pikseliä | Iframe-kentän korkeus kuvapisteinä. Korkeutta voi muuttaa tarvittaessa. |
| Näytä laskutusosoite | **Tosi** vai **Epätosi** | Jos tämän ominaisuuden arvo on **Tosi**, laskutusosoite näytetään Adyen-maksumoduulin iframe-ohjelman sisällä. Jos arvo on **Epätosi**, laskutusosoitetta ei näytetä Adyenissa, ja Commerce-käyttäjän on konfiguroitava moduuli näyttämään laskutusosoite kassasivulla. PayPal-maksuyhdistimelle tällä kentällä ei ole vaikutusta, koska laskutusosoite käsitellään täysin PayPalissa. |
| Maksun tyylin ohitus | CSS-tyylisivut (CSS) -koodi | Koska maksumoduulia isännöidään iframe-ohjelmassa, muotoiluominaisuus on rajallinen. Voit saavuttaa joitakin muotoiluja käyttämällä tätä ominaisuutta. Sivuston tyylien ohittaminen edellyttää, että liität CSS-koodin tämän ominaisuuden arvoksi. Sivuston muodostimen CSS-ohitukset ja tyylit eivät koske tätä moduulia. |
|Tuetut maksuvälinetyypit| Merkkijono| Jos useita maksuyhdistimiä on konfiguroitu, anna tuettu maksuvälinetyypin merkkijono, joka on määritetty Commerce Headquarters -sovelluksen maksuyhdistinkokoonpanossa (katso seuraava kuva). Jos tämä on tyhjä, oletusarvona on Adyen-maksuyhdistin. Lisätty Commercen versioon 10.0.14.|
|On ensisijainen maksu|  **Tosi** vai **Epätosi** | Jos arvo on **Tosi**, kaikki virhe sanomat luodaan kassasivun ensisijaisesta maksuliitännästä. Jos sekä Adyen- että PayPal-maksuyhdistimet on määritetty, määritä Adyen-arvoksi **Tosi**, joka lisättiin Commerce-versioon 10.0.14.|
|Käytä yhdistimen tunnusta| **Tosi** vai **Epätosi** | Käytä tätä ominaisuutta, jos sivustolle on määritetty useita maksuliittimiä. Jos **tosi**, liittimien on käytettävä maksukorrelaatiossa liittimen tunnusta.|
|Käytä selaimen joukon kielikoodia iFramessa|  **Tosi** vai **Epätosi** | (Vain Adyen) Jos **Tosi**, Adyen iFrame muodostaa kielen sivuston käyttäjän selaimen kontekstin perusteella, eikä sivustolle konfiguroitua Commerce-kanavan kielikoodia. Lisätty Commercen versioon 10.0.27.|

Seuraavassa kuvassa on esimerkki **Tuetut maksuvälinetyypit** -arvosta "PayPal" Commerce Headquarters -sovelluksen maksuyhdistinmäärityksissä.
![Esimerkki tuetuista maksuvälinetyypeistä Commerce Headquarters -sovelluksessa.](./media/ecommerce-paymenttendertypes.png)

## <a name="billing-address"></a>Laskutusosoite

Laskutusosoitemoduulia voidaan käyttää kassasivulla, jos Adyen-maksuyhdistimen laskutusosoiterivit eivät riittävän hyvin vastaa sivuston yleistä ulkoasua. 

Jos haluat käyttää laskutusosoitemoduulia kassasivulla, kun maksumoduuli on integroitu Adyen-maksuyhdistimen kanssa, määritä **Näytä laskutusosoite** -ominaisuuden arvoksi **Epätosi**, jotta varattua laskutusosoitemoduulia voidaan käyttää oletusarvoisen Adyen-laskutusosoitteen asemesta. Tässä tapauksessa sivuston tekijän tulee sisällyttää laskutusosoitemoduuli kassasivulle. Adyen-maksuyhdistin mahdollistaa myös toimitusosoitteen käyttämisen laskutusosoitteena, jotta voidaan minimoida sivuston käyttäjän vaiheiden määrä.

Kuten maksumoduulit, **Tuetut maksuvälinetyypit** -ominaisuus on lisätty Commerce-versiossa 10.0.14 laskutusosoitemoduuliin. Tämän ominaisuuden arvon on oltava sama kuin maksumoduulissa annettu arvo, jotta sen avulla voidaan varmistaa, että ne toimivat yhdessä. Adyen-maksuliittimen osalta sekä maksumoduulin että laskutusosoitemoduulin pitäisi jättää tämä arvo tyhjäksi (oletustila). PayPal-liitännässä ei tarvita erillistä laskutusosoitemoduulia. Muuntyyppisten maksuyhdistimien osalta merkkijono on annettava määritettynä Commerce Headquarters -sovelluksessa.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Lisää maksumoduuli kassasivulle ja määritä pakolliset ominaisuudet

Maksumoduuli voidaan lisätä vain kassalle-moduuliin. Lisätietoja maksumoduulin määrittämisestä kassasivulle on kohdassa [Kassamoduuli](add-checkout-module.md).

## <a name="configure-the-adyen-and-paypal-payment-connectors-when-both-are-used"></a>Adyen- ja PayPal-maksuliittimien konfiguroiminen, kun molempia käytetään

Jos sivustosi käytössä on sekä Adyen- että PayPal-maksuliittimet, lisää kullekin liittimelle maksumoduulit kassamoduuliin ja määritä sitten kunkin moduulin ominaisuudet noudattamalla seuraavia vaiheita Commerce-sivustonmuodostimessa.

1. Noudata seuraavia vaiheita PayPal-maksumoduulin ominaisuusruudussa:

    1. Määritä **Tuetut maksuvälinetyypit** -ominaisuuden kenttään **PayPal**.
    1. Poista **On ensisijainen maksutapa** -ominaisuuden valintaruudun valinta.
    1. Valitse **Käytä yhdistimen tunnusta** -ominaisuuden valintaruutu.

1. Noudata seuraavia vaiheita Adyen-maksumoduulin ominaisuusruudussa:

    1. Jätä **Tuetut maksuvälinetyypit** -ominaisuuden kenttä tyhjäksi.
    1. Valitse **On ensisijainen maksutapa** -ominaisuuden valintaruutu.
    1. Valitse **Käytä yhdistimen tunnusta** -ominaisuuden valintaruutu.

> [!NOTE]
> Kun määrität yhdessä käytettävät Adyen- ja PayPal-liittimet, **Dynamics 365 Payment Connector – Adyen** -konfiguraation on oltava ensimmäisenä online-kanavan **Maksutilit**-yhdistinkonfiguraatiossa Commerce Headquartersissa. Voit vahvistaa liittimien järjestyksen tai muuttaa sitä valitsemalla **Online-myymälät** ja sitten sivuston kanavan. Varmista sitten **Maksutilit**-pikavälilehden **Asetukset**-välilehden **Yhdistin**-kohdasta, että **Dynamics 365 Payment Connector – Adyen** -konfiguraatio on ensimmäisessä kohdassa (ylimmällä rivillä) ja että **Dynamics 365 Payment Connector – PayPal** -konfiguraatio on toisella rivillä. Lisää tai poista liittimiä tarpeen mukaan niiden järjestämistä varten.

## <a name="additional-resources"></a>Lisäresurssit

[Ostoskorimoduuli](add-cart-module.md)

[Ostoskorikuvakemoduuli](cart-icon-module.md)

[Kassamoduuli](add-checkout-module.md)

[Toimitusosoitemoduuli](ship-address-module.md)

[Toimitusvaihtoehtomoduuli](delivery-options-module.md)

[Noudon tiedot -moduuli](pickup-info-module.md)

[Tilauksen tiedot -moduuli](order-confirmation-module.md)

[Lahjakorttimoduuli](add-giftcard.md)

[Dynamics 365 -maksuyhdistin Adyenia varten](dev-itpro/adyen-connector.md)

[Dynamics 365 -maksuyhdistin PayPalia varten](paypal.md)

[Asiakkaan vahva todennus Adyen-yhdistimellä](adyen_redirect.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
