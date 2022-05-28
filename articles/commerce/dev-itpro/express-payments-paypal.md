---
title: PayPalin pikamaksujen määrittäminen
description: Tässä aiheessa kuvataan, kuinka määritetään PayPalin pikamaksut, jotta maksaminen nopeutuu Microsoft Dynamics 365 Commerce -ohjelmassa.
author: BrianShook
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 5fff17959e7ed9299df169c68b2ed07f6b7c7d2c
ms.sourcegitcommit: e4cc43b06ef3f0f562849e2c960025cb244d6017
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743568"
---
# <a name="configure-express-payments-for-paypal"></a>PayPalin pikamaksujen määrittäminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka määritetään PayPalin pikamaksut, jotta maksaminen nopeutuu Microsoft Dynamics 365 Commerce -ohjelmassa.

## <a name="key-terms"></a>Tärkeimmät termit

| Kausi | Kuvaus |
|---|---|
| PayPal Wallet | PayPal-liittimen tukema asiakaskokemus ja integrointi. Se tunnetaan myös PayPal-painikkeena. |
| Lompakko | Maksutyyppi, joka ei sisällä perinteisiä maksuominaisuuksia, kuten pankin tunnusnumeron (BIN) aluetta ja erääntymispäivää, joita käytetään erottamaan luotto- ja pankkikorttityypit toisistaan. |
| Pikamaksu | Commerce-moduuli, joka tukee nopeampaa uloskirjautumiskäyttämistä, kun käytössä on tuettuja maksutapoja. Tässä aiheessa käsitellään pikamaksumoduulin käyttöä PayPalin kanssa. |

Dynamics 365 Commerce tarjoaa valmiin PayPal Walletin integraation. Kun Dynamics 365 Payment Connector PayPalia varten on konfiguroitu, PayPal-painike näkyy valittavana maksutapana verkkotilauksen kassalla. Kun käyttäjät valitsevat PayPalin, heidät ohjataan suorittamaan maksu suoraan PayPalin kautta, minkä jälkeen heidät palautetaan verkkokauppaan viimeistelemään tilauksensa. PayPal-ostoskorin kassalla asiakkaat voivat käyttää maksutilitietojaan kassalomakkeen esitäyttöön, jotta he voivat suorittaa maksuprosessin nopeammin.

Commerce on lisännyt pikamaksumoduulin maksun nopeuttamiseksi. Maksupikamoduulia voidaan käyttää osassa, joka voidaan sisällyttää kassa- tai ostoskorisivulle. Kun PayPal on konfiguroitu, samaa Dynamics 365 Payment Connector PayPalia varten -liitinviitettä käytetään sekä maksun pikatoimintoa että normaalia kassatoimintoa varten.

## <a name="paypal-checkout-in-commerce"></a>PayPal-maksu Commercessa

### <a name="prerequisites"></a>Edellytykset

Määritä ympäristöllesi PayPal Wallet [Dynamics 365 Payment Connector PayPalia varten](../paypal.md) -kohdassa kuvatulla tavalla.

Jos käytät PayPalia vaihtoehtona tavallisessa maksuvirrassa (jossa käyttäjät syöttävät tilitietonsa manuaalisesti käyttämättä pikamaksun esitäyttötoimintoja), seuraa [maksumoduulin](../payment-module.md) määritysohjeita.

### <a name="payment-express-module-with-paypal"></a>PayPalin pikamaksumoduuli

Maksupikamoduuli toimii tukevien maksutapojen kanssa tarjotakseen sivuston asiakkaille mahdollisuuden siirtyä kassalle nopeammin täyttämällä maksupalvelun tilitiedot kassaprosessin aikana. Maksupikamoduuli käyttää määritettyä maksuliitintä, joka täyttää kassalomakkeen käyttäjätilin tiedoilla, kuten osoitteella, yhteystiedoilla ja valitulla maksutavalla.

Kun PayPal-pikakassaa käytetään ja käyttäjä valitsee PayPal-painikkeen kassasivun maksupikaosiossa, avautuu PayPal-maksun iFrame-ikkuna. Tämän jälkeen käyttäjä kirjautuu PayPal-tililleen ja käyttää tilin toimitusosoitetta, laskutusosoitetta, sähköpostiosoitetta ja PayPal-maksutapaa, jolla tapahtuma maksetaan.

Kun käyttäjä on suorittanut toimenpiteen PayPal-ikkunassa, käyttäjä ohjataan takaisin Commerce-sivuston kassasivulle, jolla kassalomake ja sen valitut tiedot on esitäytetty. Maksun pikatyökulussa palautettavalle toimitusosoitteelle ensimmäinen käytettävissä oleva toimitusvaihtoehto esitäytetään käyttäjälle. Tämän jälkeen käyttäjä voi tarkistaa tilauksen ja muuttaa kassatilauksen tietoja, ennen kuin hän valitsee tilauksen viimeistelyä varten **Tee tilaus**.

### <a name="add-the-payment-express-module-with-paypal-to-a-fragment"></a>Lisää PayPal-maksun pikamoduuli osaan

Voit lisätä PayPalin pikamaksumoduulin osaan Commercen sivustonmuodostimessa seuraavasti.

1. Siirry sivustoon.
1. Valitse vasemmassa siirtymisruudussa **Osat** ja valitse sitten **Uusi**.
1. Valitse **Uusi osa** -valintaikkunassa **Pikamaksu**-moduuli ja anna sitten **Osan nimi** -kohdassa osalle nimi (esimerkiksi **Pikakassa**).
1. Valitse **OK**, kun haluat luoda osan.
1. Valitse ääriviivanäkymässä luomasi pikamaksumoduulin paikka.
1. Valitse ominaisuusruudusta **Otsikko**.
1. Kirjoita **Otsikko**-valintaikkunan **Otsikkoteksti**-kenttään otsikkoteksti, jonka haluat näyttää sivuston pikakassaosassa (esimerkiksi **Pikakassa**).
1. Valitse **Otsikkotaso**-kohdassa otsikkotaso (esimerkiksi **H2**).
1. Valitse **OK**.
1. Kirjoita tai muokkaa ominaisuusruudun **iFrame korkeus** -kentässä iFrame-elementin korkeutta (esimerkiksi **60**).
1. Määritä **Tuetut maksuvälinetyypit** -ominaisuuden kenttään **PayPal**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Lisää maksun pikaosa kassasivulle

Voit lisätä maksun pikaosan kassasivulle sivuston rakennustyökalussa seuraavasti.

1. Siirry sivustoon.
1. Valitse vasemmanpuoleisesta siirtymisruudusta **Sivut** ja valitse sitten sivuston kassasivu.
1. Jos haluat muokata sivua, valitse **Muokkaa**.
1. Valitse kolme pistettä (**...**) **Pääkohde**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.

    > [!NOTE]
    > Jos kassaosan sisältävä säilömoduuli on jo olemassa, siirrä maksun pikaosaa niin, että se näkyy nykyisen kassasäilön yläpuolella **Pääkohde**-paikassa. Tämän jälkeen maksun pikaosa muodostetaan normaalin kassasäilön yläpuolella. Jos haluat siirtää säilön moduulia ylös- tai alaspäin, valitse kolme pistettä (**...**) ja valitse sitten **Siirrä ylös** tai **Siirrä alas**.

1. Suosittelemme, että määrität ominaisuusasetukset **Säilö**-ominaisuusruudussa seuraavasti:

    - **Kontin asettelu** – Valitse **Pinottu**.
    - **Leveys** – Valitse **Täytä säilö**.
    - **Näytetyt alitasot** – Valitse **Kolme**.

1. Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää osa**.
1. Valitse **Valitse osa** -valintaikkunassa etsi ja valitse aiemmin luotu pikamaksuosa ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Lisää maksun pikaosa ostoskorisivulle

Voit lisätä maksun pikaosan ostoskorisivulle sivuston rakennustyökalussa seuraavasti.

1. Siirry sivustoon.
1. Valitse vasemmanpuoleisesta siirtymisruudusta **Sivut** ja valitse sitten sivuston ostoskorisivu.
1. Jos haluat muokata sivua, valitse **Muokkaa**.
1. Etsi **Pääkohde**-paikassa säilö, joka sisältää **Ostoskori**-moduulin. **Ostoskori**-moduuli sisältää **Pikamaksu**-paikan.
1. Valitse **Pikamaksu** -paikka, valitse kolme pistettä (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Pikamaksu**-moduuli ja valitse sitten **OK**.
1. Valitse ominaisuusruudun **Tuetut maksuvälinetyypit** -kentässä **Paypal**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.

### <a name="modes-of-delivery"></a>Toimitustavat

Kun maksupikamoduuli on määritetty käyttämään PayPalia, ensimmäinen toimitusvaihtoehto, joka palautetaan PayPal-tilille valitulle toimitusosoitteelle, esitäytetään. Käyttäjät voivat tarvittaessa muuttaa toimitusosoitetta.

Toimitustavan järjestys on määritetty Commerce headquarters -kanavan **Toimitustavat**-osiossa. Lisätietoja on kohdassa [Toimitustapojen määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Kassamoduuli käyttää myös toimitusvaihtoehtomoduulia, kun toimitustavat näytetään kassalla. Lisätietoja on kohdassa [Toimitusvaihtoehdot-moduuli](../delivery-options-module.md).

Toimitustavat lisätään Commerce headquarters -verkkomyymälän luetteloon. Valitse **Retail ja Commerce \> Kanavat \> Verkkokaupat** ja valitse sitten kaupan kanavan tunnus. Valitse sitten **Asetukset \> Toimitustavat**. Konfiguraatiossa näkyvät moduulien toimitustavat näkyvät sivustolla samalla tavalla. Voit lisätä tai poistaa vähittäismyyntikanavan tai tuotteen toimitustapoja valitsemalla toimintoruudusta **Hallitse toimitustapoja**.

## <a name="additional-resources"></a>Lisäresurssit

[Maksut – usein kysytyt kysymykset](payments-retail.md)

[Kassamoduuli](../add-checkout-module.md)

[Maksumoduuli](../payment-module.md)

[Määritä toimitustavat](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Toimitusvaihtoehtomoduuli](../delivery-options-module.md)
