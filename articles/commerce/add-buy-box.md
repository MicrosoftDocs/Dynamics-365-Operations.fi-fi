---
title: Ostoruutumoduuli
description: Tässä ohjeaiheessa on tietoja ostoruutumoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9780aabbac6d01d41dae526c7c06139eba07de4e
ms.sourcegitcommit: 074fe7e77feb795148c3daf2e6ccbb8a88679343
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/31/2020
ms.locfileid: "3645336"
---
# <a name="buy-box-module"></a>Ostoruutumoduuli

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä ohjeaiheessa on tietoja ostoruutumoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskatsaus

Termi *ostoruutu* viittaa yleensä tuotetietojen sivun alueeseen, joka on sivun yläosassa ja joka isännöi kaikkein tärkeimpiä tuotteen ostamisessa tarvittavia tietoja. (Alue, joka näkyy, kun sivu ladataan ensimmäisen kerran. Näin käyttäjien ei tarvitse vierittää sivua alaspäin nähdäkseen tiedot.)

Ostoruutumoduuli on erityinen säilö, jota käytetään kaikkien tuotetietosivun ostoruutualueella näkyvien moduulien isännöinnissä.

Tuotetietosivun URL-osoite sisältää tuotteen tunnuksen. Kaikki ostoruudun hahmontamisessa vaadittavat tiedot saadaan tästä tuotteen tunnuksesta. Jos tuotteen tunnusta ei ole annettu, ostoruutumoduulia ei hahmonneta sivulla oikein. Tämän vuoksi ostoruutumoduulia voidaan käyttää vain sivuilla, joilla on tuotekonteksti. Jos sitä halutaan käyttää sivulla, jolla ei ole tuotekontekstia (kuten aloitus- tai markkinointisivulla), sitä mukautettava lisää.

Seuraavassa kuvassa näkyy esimerkki ostoruutumoduulista tuotetietosivulla.

![Esimerkki ostoruutumoduulista](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a>Ostoruutumoduulin ominaisuudet ja paikat 

Ostoruutu jaetaan tuotetietosivulla kahteen alueeseen: media-alue vasemmalla ja sisältöalue oikealla. Oletusarvoisesti media-aluesarakkeen leveyden ja sisältöaluesarakkeen leveyden välinen suhde on 2:1. Mobiililaitteissa nämä kaksi aluetta pinotaan niin, että alueet näkyvät allekkain. Sarakeleveyksiä ja pinoamisjärjestystä voi mukauttaa teemojen avulla.

Ostoruutumoduuli hahmontaa tuotteen otsikon, kuvauksen, hinnan ja luokitukset. Lisäksi asiakkaat voivat valita sen avulla tuotevariantit, joilla on eri tuotemääritteet, kuten koko, tyyli ja väri. Kun tuotevariantti on valittuna, muut ostoruudun ominaisuudet (esimerkiksi tuotteen kuvaus ja kuvat) päivitetään muuttujan tietojen mukaisiksi. 

Asiakkaat voivat määrittää annetun määrävalitsimen avulla ostettavien nimikkeiden määrän. Sivuston asetuksissa voidaan määrittää suurin sallittu ostomäärä.

Asiakkaat voivat suorittaa ostoruudussa myös muita toimintoja, kuten lisätä tuotteen ostoskoriin tai toivelistalle ja valita noutosijainnin. Nämä toiminnot voidaan tehdä tuotteen tai tuotevariantin kohdalla. Jos asiakas haluaa lisätä tuotteen toivelistaan, hänen on oltava kirjautuneena sisään.

Teemojen avulla voidaan poistaa ostoruudun tuoteominaisuuksien ja toimintojen ohjausobjekteja tai muuttaa niiden järjestystä. 

## <a name="module-properties"></a>Moduulin ominaisuudet

- **Otsikon tunniste** – Tämä ominaisuus määrittää tuoteotsikon otsikon tunnisteen. Jos ostoruutu on sivun yläosassa, helppokäyttöisyysstandardit täyttyvät, kun tämän ominaisuuden arvona on **h1**. 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduulit, joita voidaan käyttää ostoruutumoduulissa

- **Mediavalikoima** – Tämän moduulin avulla esitellään tuotteen kuvat tuotetietosivulla. Lisätietoja tästä moduulista on kohdassa [Mediavalikoimamoduuli](mediagallery-module.md).
- **Myymälän valitsin** – Tämä moduuli näyttää luettelon lähellä olevista myymälöistä, joista nimikkeen voi noutaa. Käyttäjät voivat etsiä lähellä olevia myymälöitä antamalla sijainnin. Lisätietoja tästä moduulista on kohdassa [Myymälävalitsinmoduuli](store-selector.md).

## <a name="buy-box-module-settings"></a>Ostoruutumoduulin asetukset

Seuraavat ostoruutumoduuliasetukset voidaan määrittää valitsemalla **Sivuston asetukset \> Laajennukset**:

- **Ostoskorin rivien maksimimäärä** – Tätä ominaisuutta käytetään määrittämään kunkin ostoskoriin lisättävän nimikkeen enimmäismäärä. Jälleenmyyjä voi esimerkiksi päättää, että yhdessä tapahtumassa voidaan myydä vain 10 kappaletta kutakin tuotetta.
- **Varasto** – lisätietoja varastoasetusten ottamisesta käyttöön on kohdassa [Varastoasetusten käyttäminen](inventory-settings.md).
- **Lisää ostoskoriin** - Tämän ominaisuuden avulla määritetään, mitä tapahtuu, kun nimike on lisätty ostoskoriin. Mahdolliset arvot ovat **Siirry ostoskoriin**, **Älä siirry ostoskoriin** ja **Näytä ilmoitukset**. Kun arvoksi on määritetty **Siirry ostoskoriin**, käyttäjät lähetetään ostoskorisivulle, kun he lisäävät nimikkeen. Kun arvoksi on määritetty **Älä siirry ostoskoriin**, käyttäjiä ei lähetetä ostoskorisivulle, kun he lisäävät nimikkeen. Kun arvoksi on määritetty **Näytä ilmoitukset**, käyttäjille näytetään vahvistusilmoitus ja he voivat jatkaa selaamista tuotteen tiedot -sivulla. 

    Seuraavassa kuvassa on esimerkki Siirretty ostoskoriin -vahvistusilmoituksesta Fabrikam-sivustolla.

    ![Esimerkki ilmoitusmoduulista](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit -käyttö

Ostoruutumoduuli hakee tuotetiedot Commerce Scale Unitin ohjelmistorajapintojen (API) avulla. Tuotetietosivulla olevaa tuotteen tunnusta käytetään kaikkien tietojen noutamisessa.

## <a name="add-a-buy-box-module-to-a-page"></a>Ostoruutumoduulin lisääminen sivulle

Voit lisätä ostoruutumoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Sivun osat** ja **Uusi** luodaksesi uuden osan.
1. Valitse **Uusi sivun osa** -valintaikkunassa **Ostoruutu**-moduuli.
1. Kirjoita **Sivun osan nimi** -kohtaan **Ostoruudun osa** ja valitse sitten **OK**.
1. Valitse ostoruutumoduulissa **Mediavalikoima**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Mediavalikoima**-moduuli ja valitse sitten **OK**.
1. Valitse ostoruutumoduulissa **Myymälävalitsin**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Myymälävalitsin**-moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.
1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **PDP-malli** ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.
1. Valitse oletussivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää sivun osa**.
1. Valitse **Valitse sivun osa** -valintaikkunassa **Ostoruutuosa**, jonka loit aiemmin ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Valitse **Valitse malli** -valintaikkunassa **PDP-malli**-pohja. Kirjoita **Sivun nimi** -kohtaan **PDP-sivu** ja valitse sitten **OK**.
1. Valitse uudella sivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää sivun osa**.
1. Valitse **Valitse sivun osa** -valintaikkunassa **Ostoruutuosa**, jonka loit aiemmin ja valitse sitten **OK**.
1. Tallenna ja esikatsele sivu. Lisää **?productid=&lt;tuotteen tunnus&gt;** -kyselymerkkijonoparametri esikatselusivun URL-osoitteeseen. Näin tuotekontekstia käytetään esikatselusivun lataamiseen ja käsittelemiseen.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**. Tuotetietosivulla näkyy ostoruutu.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Myymälän valitsinmoduuli](store-selector.md)

[Mediavalikoimamoduuli](media-gallery-module.md)

[Konttimoduuli](add-container-module.md)

[Ostoskorimoduuli](add-cart-module.md)

[Ostoskorikuvakemoduuli](cart-icon-module.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)

[Vähittäismyyntikanavien varaston käytettävyyden laskeminen](calculated-inventory-retail-channels.md)
