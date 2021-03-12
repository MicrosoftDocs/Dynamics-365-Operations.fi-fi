---
title: Sähköisen kaupan digitaaliset lahjakortit
description: Tässä aiheessa kuvataan, kuinka digitaaliset lahjakortit toimivat sähköisen kaupankäynnin Microsoft Dynamics 365 Commerce -käyttöönotossa. Lisäksi siinä on yleiskatsaus tärkeistä konfigurointivaiheista.
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 5a88bef72e13b7b0d948bfd7617cb1dbbcd9ce49
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982663"
---
# <a name="e-commerce-digital-gift-cards"></a>Sähköisen kaupan digitaaliset lahjakortit

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä aiheessa kuvataan, kuinka digitaaliset lahjakortit toimivat sähköisen kaupankäynnin Microsoft Dynamics 365 Commerce -käyttöönotossa. Lisäksi siinä on yleiskatsaus tärkeistä konfigurointivaiheista.

Dynamics 365 Commercessa digitaalisten lahjakorttien osto noudattaa samaa työnkulkua kuin muiden järjestelmän tuotteiden osto. Muita moduuleita ei tarvitse konfiguroida. Jos ostoskoriin on lisätty useita lahjakortteja, lahjakorttinimikkeitä ei yhdistetä yhdelle myyntiriville. Tämä toimintatapa on pakollinen, koska jokainen myyntirivi laskutetaan erillisellä lahjakortin numerolla.

Digitaalisten lahjakorttien ostoa tuetaan Dynamics 365 Commercen versiossa 10.0.16 ja sitä myöhemmissä versioissa.

Seuraavassa kuvassa on esimerkki Fabrikam-verkkokauppasivuston digitaalisen lahjakortin tuotetietosivusta (PDP).

![Esimerkki digitaalisen lahjakortin PDP-sivuta Fabrikamin verkkokauppasivustossa](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a>Digitaalisten lahjakorttien ominaisuuden käyttöönottaminen Commerce headquarters -sovelluksessa

Jotta digitaalisten lahjakorttien ostotyönkulku toimisi Dynamics 365 Commercessa, **lahjakortin ostamisen verkkokauppatoiminnon** on oltava käytössä Commerce headquarters -sovelluksessa. Seuraavassa kuvassa on Commerce Headquarters -sovelluksen **Ominaisuuden hallinta** -työtilassa näkyvä toiminto.

![Ominaisuuden hallinta -työtila Commerce headquarters -sovelluksessa](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a>Digitaalisten lahjakorttien määrittäminen Commerce headquarters -sovelluksessa

Digitaalisten lahjakorttien tuotteet pitää määrittää Commerce headquarters -sovelluksessa. Prosessi muistuttaa muiden tuotteiden prosessia. Seuraavat tärkeät vaiheet liittyvät kuitenkin oston lahjakorttien konfigurointiin. Lisätietoja tuotteiden luomisesta ja konfiguroinnista on kohdassa [Uuden tuotteen luominen Commercessa](create-new-product-commerce.md).

- Kun konfiguroit digitaalisia lahjakorttituotteita **Uusi tuote** -valintaikkunassa, määritä **Tuotetyyppi**-kentän arvoksi **Palvelu**. (Voit avata valintaikkunan valitsemalla **Retail ja commerce \> Tuotteet ja luokat \> Tuotteet luokittain** ja sitten **Uusi**.) **Palvelu**-tyypin tuotteiden varastosaldoa ei tarkistetaan tilausta tehtäessä. Lisätietoja on kohdassa [Uuden tuotteen luominen](create-new-product-commerce.md#create-a-new-product).
- **Commercen parametrit** -sivun **Kirjaus**-välilehden **Lahjakortttituote**-kentän arvoksi on määritettävä **Digitaalinen lahjakortti** seuraavan kuvan mukaisesti. Jos tuote on ulkoinen lahjakortti, lisätietoja on kohdassa [Ulkoisten lahjakorttien tuki](./dev-itpro/gift-card.md).

    ![Lahjakorttituotteen kenttä Commerce headquarters -sovelluksessa](./media/PostGiftcard.png)

- Jos lahjakortin on tuettava useita ennalta määritettyjä summia (esimerkiksi 25 $, 50 $, ja 100 $), määritä ennalta määritetyt summat **Koko**-dimension avulla. Kukin ennalta määritetty summa on variantti. Lisätietoja on kohdassa [Tuotedimensiot](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json).
- Jos asiakkaiden on pystyttävä määrittämään lahjakortille mukautettu summa, määritä ensin muuttuja, joka sallii mukautetun summan. Avaa seuraavaksi tuote **Luokan julkaistut tuotteet** -sivulla ja määritä sitten **Commerce**-pikavälilehdellä **Syötä hinta** -kentän arvoksi **Uusi hinta on näppäiltävä** seuraavan kuvan mukaisesti. Tällä asetuksella varmistetaan, että asiakkaat voivat syöttää hinnan, kun he selaavat tuotetta PDP-sivulla.

    ![Syötä hinta -kenttä Commerce headquarters -sovelluksessa](./media/KeyInPrice.png)

- Digitaalisten lahjakorttien toimitustavaksi on määritettävä **Sähköinen**. Valitse **Toimitustavat**-sivulla (**Retail ja Commerce \> Kanavan asetukset \> Toimitustavat**) **Sähköinen**-toimitustapa luetteloruudussa ja lisää digitaalinen lahjakorttituote ruudukkoon **Tuotteet**-pikavälilehdessä seuraavan kuvan mukaisesti. Lisätietoja on kohdassa [Toimitustapojen määrittäminen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

    ![Digitaaliset lahjakorttituotteet Commerce headquarters -sovelluksen Toimitustapa-sivulla](./media/ElectronicMode.PNG)

- Varmista, että Commerce Headquarters -sovelluksen verkkosäilöön on luotu ja liitetty online-toimintoprofiili. Määritä toimintoprofiilissa **Koostetuotteet**-asetuksen arvoksi **Kyllä**. Tällä asetuksella varmistetaan, että kaikki nimikkeet lahjakortteja lukuun ottamatta yhdistetään. Lisätietoja on kohdassa [Online-toimintoprofiilin luominen](online-functionality-profile.md).
- Voit varmistaa, että asiakkaat saavat sähköpostiviestin lahjakortin laskutuksen jälkeen, luomalla **Sähköposti-ilmoituksen profiili** -sivulle uuden sähköposti-ilmoitustyypin ja valitsemalla **Sähköposti-ilmoitustyyppi**-kentän arvoksi **Myönnä lahjakortti**. Lisätietoja on ohjeaiheessa [Sähköposti-ilmoitusprofiilin määrittäminen](email-notification-profiles.md).

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a>Tuotekuvien lisääminen Commercen sivustonmuodostimen mediakirjastoon

Digitaalisten lahjakorttituotteiden tuotekuvat on lisättävä Commercen sivustomuodostimen mediakirjastoon. Varmista, että lahjakorttien kuvatiedostojen tiedostonimet noudattavat sivuston tuotekuvien nimeämiskäytäntöjä. Lisätietoja on kohdassa [Kuvien lataaminen palvelimeen](dam-upload-images.md).

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a>Mukautetun summan konfiguroiminen digitaalista lahjakorttia varten Commercen sivustomuodostimessa

Jos digitaalinen lahjakortti on määritetty sallimaan mukautettu summa, tämä toiminto on otettava käyttöön myös sivuston PDP-sivuilla käytettävässä [ostoruutumoduulissa](add-buy-box.md). Ostoruutumoduuli tukee moduulien konfiguraatiota mukautettujen summien sallimista varten. Voit myös määrittää mukautettujen summien sallitut vähimmäis- ja enimmäissummat.

Voit määrittää mukautetun summan digitaalista lahjakorttia varten Commercen sivustomuodostimessa seuraavasti.

1. Siirry sivuston PDP-sivulla käytettävään ostoruutumoduuliin. Tämä ostoruutumoduuli voi olla toteutettuna katkelmassa, mallissa tai sivulla.
1. Valitse **Muokkaa**.
1. Valitse oikealla olevasta ominaisuusruudusta **Salli mukautettu hinta** -valintaruutu.
1. Valinnainen: Voit määrittää mukautettujen summien vähimmäis- ja enimmäissummat kirjoittamalla summat **Vähimmäishinta**- ja **Enimmäishinta**-kenttiin.
1. Valitse **Viimeistele muokkaus** ja sitten **Julkaise**.

## <a name="additional-resources"></a>Lisäresurssit

[Ostoruutumoduuli](add-buy-box.md)

[Kassamoduuli](add-checkout-module.md)

[Ostoskorimoduuli](add-cart-module.md)

[Uuden tuotteen luominen Commercessa](create-new-product-commerce.md)

[Määritä toimitustavat](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Tuotedimensiot](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)

[Sähköposti-ilmoitusprofiilin määrittäminen](email-notification-profiles.md)

[Luo online-toimintoprofiili](online-functionality-profile.md)

[Ulkoisten lahjakorttien tuki](./dev-itpro/gift-card.md)
