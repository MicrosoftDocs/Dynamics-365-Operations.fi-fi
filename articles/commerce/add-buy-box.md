---
title: Ostoruutumoduuli
description: Tässä ohjeaiheessa on tietoja ostoruutumoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 095374c14cddf1ae3608ae1427a7144b3e7ca7b2
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269748"
---
# <a name="buy-box-module"></a>Ostoruutumoduuli


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja ostoruutumoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskatsaus

Termi *ostoruutu* viittaa yleensä tuotetietojen sivun alueeseen, joka on sivun yläosassa ja joka isännöi kaikkein tärkeimpiä tuotteen ostamisessa tarvittavia tietoja. (Alue, joka näkyy, kun sivu ladataan ensimmäisen kerran. Näin käyttäjien ei tarvitse vierittää sivua alaspäin nähdäkseen tiedot.)

Ostoruutumoduuli on erityinen säilö, jota käytetään kaikkien tuotetietosivun ostoruutualueella näkyvien moduulien isännöinnissä.

Tuotetietosivun URL-osoite sisältää tuotteen tunnuksen. Kaikki ostoruudun hahmontamisessa vaadittavat tiedot saadaan tästä tuotteen tunnuksesta. Jos tuotteen tunnusta ei ole annettu, ostoruutumoduulia ei hahmonneta sivulla oikein. Tämän vuoksi ostoruutumoduulia voidaan käyttää vain sivuilla, joilla on tuotekonteksti. Jos sitä halutaan käyttää sivulla, jolla ei ole tuotekontekstia (kuten aloitus- tai markkinointisivulla), sitä mukautettava lisää.

## <a name="buy-box-module-properties-and-slots"></a>Ostoruutumoduulin ominaisuudet ja paikat 

Ostoruutu jaetaan tuotetietosivulla kahteen alueeseen: media-alue vasemmalla ja sisältöalue oikealla. Oletusarvoisesti media-aluesarakkeen leveyden ja sisältöaluesarakkeen leveyden välinen suhde on 2:1. Mobiililaitteissa nämä kaksi aluetta pinotaan niin, että alueet näkyvät allekkain. Sarakeleveyksiä ja pinoamisjärjestystä voi mukauttaa teemojen avulla.

Ostoruutumoduuli hahmontaa tuotteen otsikon, kuvauksen, hinnan ja luokitukset. Lisäksi asiakkaat voivat valita sen avulla tuotevariantit, joilla on eri tuotemääritteet, kuten koko, tyyli ja väri. Kun tuotevariantti on valittuna, muut ostoruudun ominaisuudet (esimerkiksi tuotteen kuvaus ja kuvat) päivitetään muuttujan tietojen mukaisiksi. 

Asiakkaat voivat määrittää annetun määrävalitsimen avulla ostettavien nimikkeiden määrän. Sivuston asetuksissa voidaan määrittää suurin sallittu ostomäärä.

Asiakkaat voivat suorittaa ostoruudussa myös muita toimintoja, kuten lisätä tuotteen ostoskoriin tai toivelistalle ja valita noutosijainnin. Nämä toiminnot voidaan tehdä tuotteen tai tuotevariantin kohdalla. Jos asiakas haluaa lisätä tuotteen toivelistaan, hänen on oltava kirjautuneena sisään.

Teemojen avulla voidaan poistaa ostoruudun tuoteominaisuuksien ja toimintojen ohjausobjekteja tai muuttaa niiden järjestystä. 

## <a name="module-properties"></a>Moduulin ominaisuudet

- **Otsikon tunniste** – Tämä ominaisuus määrittää tuoteotsikon otsikon tunnisteen. Jos ostoruutu on sivun yläosassa, helppokäyttöisyysstandardit täyttyvät, kun tämän ominaisuuden arvona on **h1**. 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduulit, joita voidaan käyttää ostoruutumoduulissa

- **Mediavalikoima** – Tämän moduulin avulla esitellään tuotteen kuvat tuotetietosivulla. Moduuli voi tukea yhtä kuvaa tai useita kuvia. Se tukee myös pikkukuvia. Pikkukuvat voivat olla vaakasuuntaisesti (rivinä kuvan alla) tai pystysuuntaisesti (pystyrivinä kuvan vieressä). Mediavalikoimamoduuli voidaan lisätä **Media**-paikkaan ostoruutumoduulissa. Se tukee tällä hetkellä vain kuvia. 
- **Myymälän valitsin** – Tämä moduuli näyttää luettelon lähellä olevista myymälöistä, joista nimikkeen voi noutaa. Käyttäjät voivat etsiä lähellä olevia myymälöitä antamalla sijainnin. Lisätietoja tästä moduulista on kohdassa [Kaupan valitsinmoduuli](store-selector.md).

## <a name="buy-box-module-settings"></a>Ostoruutumoduulin asetukset

Ostoruutumoduulissa on kolme asetusta, jotka voidaan määrittää valitsemalla **Sivuston asetukset \> Laajennukset**:

- **Maksimimäärä** – Tätä ominaisuutta käytetään määrittämään kunkin ostoskoriin lisättävän nimikkeen enimmäismäärä. Jälleenmyyjä voi esimerkiksi päättää, että yhdessä tapahtumassa voidaan myydä vain 10 kappaletta kutakin tuotetta.
- **Varaston tarkistus** – Kun arvoksi on asetettu **Tosi**, nimike lisätään ostoskoriin vasta, kun ostoruutumoduuli varmistaa, että nimikettä on varastossa. Tämä varaston tarkistus tehdään skenaarioissa, joissa nimike toimitetaan, että skenaarioissa, joissa se noudetaan myymälästä. Jos arvoksi on määritetty **Epätosi**, varaston tarkistus tehdään vasta, kun nimike on lisätty ostoskoriin ja tilaus on tehty. Lisätietoja varastoasetusten määrittämisestä taustaohjelmassa on kohdassa [Varaston käytettävyyden laskeminen vähittäismyyntikanaville](calculated-inventory-retail-channels.md).

- **Varaston puskuri** – Tällä ominaisuudella määritetään varaston puskurimäärä. Varastoa ylläpidetään reaaliaikaisesti. Jos useat asiakkaat tekevät tilauksia, todellisen varastomäärän ylläpitäminen voi olla vaikeaa. Kun varaston tarkistus tehdään ja varasto on pienempi kuin puskurisumma, tuotetta käsitellään kuin se olisi loppunut varastosta. Kun myynti tapahtuu nopeasti useiden kanavien kautta eikä varastomäärä ole täysin synkronoitu, on pienempi riski siitä, että nimikettä ei ole varastossa myynnin hetkellä.

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit -käyttö

Ostoruutumoduuli hakee tuotetiedot Commerce Scale Unitin ohjelmistorajapintojen avulla. Tuotetietosivulla olevaa tuotteen tunnusta käytetään kaikkien tietojen noutamisessa.

## <a name="add-a-buy-box-module-to-a-page"></a>Ostoruutumoduulin lisääminen sivulle

Voit lisätä ostoruutumoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Luo osa nimeltä **Ostoruutuosa** ja lisää siihen ostoruutumoduuli.
1. Lisää ostoruutumoduuliin **Media**-paikkaan mediavalikoimamoduuli.
1. Lisää myymälän valitsinmoduuli ostoruutumoduulin **Myymälän valitsin** -paikkaan.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.
1. Luo tuotetietosivulla malli ja anna sen nimeksi **PDP-malli**.
1. Lisää oletussivu.
1. Lisää ostoruutuosa oletussivun **pääpaikkaan**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Käytä juuri luotua mallia, kun haluat luoda sivun nimeltä **PDP-sivu**.
1. Lisää ostoruutuosa uuden sivun **pääpaikkaan**.
1. Tallenna ja esikatsele sivu. Lisää **?productid=&lt;tuotteen tunnus&gt;** -kyselymerkkijonoparametri esikatselusivun URL-osoitteeseen. Näin tuotekontekstia käytetään esikatselusivun lataamiseen ja käsittelemiseen.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**. Tuotetietosivulla näkyy ostoruutu.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Myymälän valitsinmoduuli](store-selector.md)

[Konttimoduuli](add-container-module.md)

[Ostoskorimoduuli](add-cart-module.md)

[Ostoskorikuvakemoduuli](cart-icon-module.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)

[Vähittäismyyntikanavien varaston käytettävyyden laskeminen](calculated-inventory-retail-channels.md)
