---
title: Ostoskorikuvakemoduuli
description: Tässä artikkelissa käsitellään ostoskorimoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: e35b0ee5341b8b5531ad2c80c868ca4c07ebd315
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280498"
---
# <a name="cart-icon-module"></a>Ostoskorikuvakemoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään ostoskorimoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.

Ostoskorikuvakemoduuli edustaa koria sivun otsikkomoduulissa ja ilmaisee, kuinka monta nimikettä ostoskorissa on. Ostoskorikuvakemoduuli näyttää myös ostoskorin yhteenvedon (tunnetaan myös nimellä miniostoskori), kun hiiri viedään ostoskorikuvakkeen yli. Pienoiskori antaa käyttäjälle yhteenvedon ostoskorin nimikkeistä ilman, että sinun tarvitsee siirtyä ostoskorisivulle. Lisäksi se mahdollistaa myös käyttäjän siirtymisen suoraan kassasivulle, jos hän on tyytyväinen yhteenvetoon. Tämä vähentää sivusiirtymien määrää ja nopeuttaa uloskuittausta. 

Seuraavassa kuvassa näkyy esimerkki ostoskorin kuvakemoduulista, jossa näkyy pienoiskärry Fabrikam-otsikossa.

![Esimerkki ostoskorikuvakemoduulista.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Moduulin ominaisuudet

- **Näytä pienoiskori** – Jos ominaisuuden arvoksi määritetään **Tosi**, ostoskorin yhteenvedon (pienoiskorin) näytetään, kun käyttäjä siirtää kohdistimen ostoskorikuvakkeen päälle. Tätä toimintoa tuetaan vain työpöydän näkymäporteissa.
- **Salli anonyymi siirtyminen kassalle** – Jos ominaisuuden arvoksi on määritetty **Tosi**, pienoiskori sallii käyttäjien, jotka eivät ole kirjautuneet sisään, siirtyä kassalle vieraana. Ominaisuus on saatavana Commercen versiossa 10.0.21 Commercen moduulikirjastopaketin osana.
- **Nimikkeiden järjestys** – Tämä ominaisuus määrittää järjestyksen, jossa nimikkeet näkyvät pienoiskorissa. Kun **Uudet nimikkeet lisätään luetteloon ensimmäiseksi** -vaihtoehto valitaan, uudet ostokoriin lisättävät nimikkeet näkyvät ensimmäisenä pienoiskorin nimikeluettelossa. Kun **Uudet nimikkeet lisätään luetteloon viimeiseksi** -oletusvaihtoehto valitaan, uudet ostokoriin lisättävät nimikkeet näkyvät viimeisenä pienoiskorin nimikeluettelossa. Ominaisuus on saatavana Commercen versiosta 10.0.21 alkaen Commercen moduulikirjastopaketin osana.

> [!IMPORTANT]
> **Salli anonyymi siirtyminen kassalle**- ja **Nimikkeiden järjestys** -ominaisuudet ovat saatavana Commercen versiosta 10.0.21 alkaen. Niitä varten on asennettava Commercen moduulikirjastopaketin versio 9.31.

## <a name="module-properties-and-slots-in-the-adventure-works-theme"></a>Moduulin ominaisuudet ja paikat Adventure Works -teemassa

Adventure Works -teeman ostoskorikuvakemoduuli sisältää kaksi ylimääräistä paikkaa pienoiskoria varten. Nämä paikat ovat moduulimääritelmän laajennuksia.

- **Tyhjän ostosokorin kampanjat** – Tähän paikkaan voi lisätä sisältölohkomoduulin. Kun ostoskori on tyhjä, määritetty sisältölohkomoduuli näytetään. Sisältölohkomoduulia voidaan käyttää kampanjoille, markkinointisisällölle ja luokkasivujen linkeille, jotta asiakkaat voivat jatkaa ostosten tekemistä.
- **Kampanjasisältö** – Tätä paikkaa voidaan käyttää kampanjoiden esittelemiseen, esimerkiksi "Ilmainen toimitus yli 100 euron toimituksiin". Kampanjasisällön paikassa voidaan käyttää sisältölohko-, tekstilohko- ja kuvaluettelomoduuleja.

Seuraavassa kuvassa on esimerkki Adventure Works -teeman ostoskorikuvakemoduulista, joka näyttää kampanjasisältöä pienoiskorissa.

![Esimerkki ostoskorikuvakemoduulista Adventure Works -teemassa](./media/AW_minicart.PNG)

> [!IMPORTANT]
> Adventure Works -teeman paikat ovat käytettävissä Dynamics 365 Commerce -version 10.0.20 julkaisusta eteenpäin.

## <a name="add-a-cart-icon-module-to-a-page"></a>Ostoskorikuvakkeen lisääminen sivulle

Jos haluat lisätä ostoskorikuvakkeen moduulin, katso kohta [Otsikkomoduuli](author-header-module.md).

## <a name="additional-resources"></a>Lisäresurssit

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Maksumoduuli](payment-module.md)

[Toimitusosoitemoduuli](ship-address-module.md)

[Toimitusvaihtoehtomoduuli](delivery-options-module.md)

[Noudon tiedot -moduuli](pickup-info-module.md)

[Tilauksen tiedot -moduuli](order-confirmation-module.md)

[Lahjakorttimoduuli](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
