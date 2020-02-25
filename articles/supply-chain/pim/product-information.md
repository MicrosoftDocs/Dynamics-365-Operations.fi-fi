---
title: Tuotetietojen yleiskatsaus
description: Tässä ohjeaiheessa on tietoja tuotetietojen hallinnasta. Tuotetietojen hallinta käyttää kaikissa yrityksissä jaettuja tuotteiden määritelmiä, luokituksia ja tunnisteita. Tämän lisäksi se käyttää liiketoimintaprosesseihin sopivia tuotteen erityismäärityksiä.
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdbff802ca85f7cc568efb8a1aacaf6f8fb2874a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003993"
---
# <a name="product-information-overview"></a>Tuotetietojen yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja tuotetietojen hallinnasta. Tuotetietojen hallinta käyttää kaikissa yrityksissä jaettuja tuotteiden määritelmiä, luokituksia ja tunnisteita. Tämän lisäksi se käyttää liiketoimintaprosesseihin sopivia tuotteen erityismäärityksiä. 

Tuotetiedot ovat keskeinen osa toimitusketju- ja kauppasovelluksia toimialasta riippumatta. Se viittaa prosesseihin ja tekniikkoihin, jotka keskittyvät hallitsemaan keskistetysti tuotetta koskevia tietoja (esimerkiksi kaikissa toimitusketjuissa). Tuotteen määritelmien, ohjeistuksen, määritteiden ja tunnisteiden jakaminen on äärimmäisen tärkeää. Liiketoimintaratkaisun eri moduuleissa tarvitaan tuotekohtaisia tietoja ja määrityksiä, jotta tiettyihin tuotteisiin, tuoteperheisiin tai tuoteluokkiin liittyviä liiketoimintaprosesseja voidaan hallita.

## <a name="product-definition"></a>Tuotemääritelmä

Tuote määritetään ensisijaisesti tuotenumeron, nimen ja kuvauksen perusteella. Tuotteen tai palvelun kuvaamiseen tarvitaan myös muita tietoja:

- Tuotteen tyyppi: nimike tai palvelu
- Tuotteen alatyyppi: erilliset tuotteet tai päätuotteet
- Tuotevarianttimallin määritelmä:

     - Tuotedimensiot ja dimensioryhmät
     - Tuotenimikkeistö
     - Tuotekonfiguraation mallit

- Tuotteen liitos vähintään yhteen luokkaan
- Tuotteen ja luokan määritteiden määritelmä
- Tuotekuvat
- Liitteet
- Mittayksiköt ja liittyvät muunnokset
- Kaikkien nimien ja kuvausten käännökset

## <a name="distribution-export-and-import-of-product-data"></a>Tuotetietojen jakelu, tuonti ja vienti

Tuotemääritelmä voidaan luoda Supply Chain Managementissa. Se voidaan myös tuoda tuotteen elinkaaren hallinta- (PLM), tuotteen tiedonhallinta- (PDM) tai tuotetietojen hallintajärjestelmästä (PIM). Kun käytössä on useita Supply Chain Management -esiintymiä, yhtä esiintymää käytetään yleensä muiden esiintymien tuotetietojen pääversiona. Tämän menetelmän tukena on suuri tietoyksikköjoukko, jonka avulla tuotteen määritelmätietoja voi viedä ja tuoda esiintymästä toiseen.

Supply Chain Management tukee tuotetietojen jakelua useisiin esiintymiin mahdollistamalla Common Data Servicen käytön. Tuotemääritelmät voidaan viedä Supply Chain Management -esiintymästä Common Data Serviceen. Tuotemääritelmillä voidaan sitten valmistella tuotetiedot muihin liiketoimintasovelluksiin, kuten Dynamics 365 Salesiin.

Huomaa, että dynaamisissa ja ketterissä organisaatioissa tuotetietojen tiedot vaihtuvat päivittäin. Tämän vuoksi tuotteen tarkkojen ja todenmukaisten tietojen ylläpito on jo sinällään tärkeä liiketoimintaprosessi.

## <a name="product-masters-and-product-variants"></a>Päätuotteet ja tuotevariantit

Koska tuotteet on voitava sopeuttaa nopeasti muuttuvissa tilanteissa vikkelästi asiakkaiden tarpeiden mukaisiksi, tuotemääritelmät koskevat erillisten tuotteiden sijaan tuotejoukkoja. Supply Chain Managementissa näitä yleisiä tuotteita kutsutaan *päätuotteiksi*. Päätuotteet sisältävät määritelmän ja säännöt, jotka määrittävät erilliset tuotteet kuvaillaan ja miten ne toimivat liiketoimintaprosesseissa. Näiden määritelmien perusteella voidaan luoda erillisiä tuotteita. Näitä erillisiä tuotteita kutsutaan *tuotevarianteiksi*.

Päätuote on liitetty tuotedimensioryhmään ja määritysmenetelmään liiketoimintasääntöjen määrittämiseksi. Tuotedimensiot (väri, koko, tyyli ja määritykset) ovat tietty määritejoukko, jolla voidaan määrittää ja seurata liittyvien tuotteiden toimintaa koko sovelluksessa. Näiden avulla käyttäjät voivat myös etsiä ja tunnistaa tuotteita.

## <a name="configuration-technologies"></a>Määritysmenetelmät

Valittavana on kolme määritysmenetelmää:

- Ennalta määritetyt variantit on määritetty ennalta määritetyissä tuotedimensioissa. Variantin määritys sisältää tietyn voimassaolevan dimensioyhdistelmän, kuten värin, tyylin ja koon, määritelmän. Kullakin yhdistelmällä saadaan erillinen tuotevariantti.
- Dimensioihin perustuvaa konfiguraatiota käytetään yleensä tuotantoskenaarioissa, ja siinä voi käyttää kokoonpanodimensiota tuoterakenteiden määritelmässä. Kun tietty kokoonpano on valittu, järjestelmä käyttää kyseisessä kokoonpanossa voimassaolevaa tuoterakennerivien alijoukkoa suunnitteluun ja tuotantoon. Tätä kutsutaan *yleiseksi tuoterakenteeksi*, koska yhtä jaettua tuoterakennetta käytetään tuotteen kaikissa kokoonpanoissa.
- Poissulkeva konfiguraatio ilmoittaa tuotemääritysmallissa kaikki mahdolliset määritteet ja komponentit, jotka tarvitaan, jotta tuotteen kaikki mahdolliset mallit voitaisiin kuvata yhdessä mallissa. Määriteyhdistelmien rajoitukset voidaan ilmoittaa säännönmukaisina lausekkeina tai taulukkoperusteisina rajoituksina. Määritysmallit ja konfiguroinnit ovat entistäkin tärkeämpiä tuotetietojen hallinnassa, ja niitä käytetään kaikilla toimialoilla.

Supply Chain Managementin käyttöönottoa suunniteltaessa on erittäin tärkeää valita liiketoimintaprosessille oikea määritysmenetelmä. Tuotetta ei voi muuntaa mallista toiseen käyttöönoton jälkeen.

## <a name="product-variant-model-definition-workspace"></a>Tuotevarianttimallin määritelmän työtila

**Tuotevarianttimallin määritelmän** työtilassa on päätuotteiden yleiskatsaus. Siinä näkyy myös tietyille yrityksille vapautettujen päätuotteiden ja niihin liittyvien varianttien tila.

## <a name="released-products"></a>Vapautetut tuotteet

Tietylle yritykselle vapautettuja tuotteita kutsutaan *vapautetuiksi tuotteiksi*. Tuotteet voidaan julkaista joukkona yhdelle yritykselle tai useille yrityksille samanaikaisesti. Koska erilaisia ominaisuuksia ja määritteitä on ehkä lisättävä yrityskohtaisesti tuotteisiin, voit seurata **vapautetun tuotteen ylläpidon** työtilassa kunkin yrityksen tai yrityksen aliorganisaatioiden äskettäin vapautettuja tuotteita ja viimeistellä ne

### <a name="released-product-maintenance-workspace"></a>Vapautetun tuotteen ylläpidon työtila

Voit määrittää **Vapautetun tuotteen ylläpito** -työtilan **Määritä oma työtila** -valikkovaihtoehdossa. Valitse luokkahierarkiaa ja suodata työtila luokan mukaan. Voit muokata liittyvän tuotteen tietoja työtilassa. Voit myös määrittää päivinä **Lähiaikoina julkaistut tuotteet**- ja **Pysäytetyt julkaistut tuotteet** -vaihtoehtojen aikarajat.

Työtilassa on yhteenvetoruudut ja kaksi luetteloa. **Avoimet tapaukset** -luettelossa on muutostapaukset, joissa on valitussa tuotehierarkialuokassa tuotteita, jotka eivät ole valmiita ja suljettuja. **Lähiaikoina julkaistut** -luettelossa on tuotteet, jotka on vapautettu työtilan määrityksissä määritetyn aikarajan sisällä. Luettelon jokaiselle nimikkeelle suoritetaan oikeellisuustarkoitus ja tämän tarkistuksen tila on näkyvissä. Tila voi ilmaista, että yrityksen edellyttämiä määrityksiä ei ole suoritettu. Voit käyttää suoraan luettelosta **Vapautetun tuotteen tiedot**-, **Tuotemääritteen ylläpito**-, **Tuoteluokan ylläpito**-, **Tilauksen oletusasetukset**- ja **Tekstin käännökset** -sivuja ja viimeistellä tuotteen tarvittavat määritykset.

### <a name="manually-creating-a-new-released-product"></a>Uuden vapautetun tuotteen luominen manuaalisesti

Voit luoda vapautetun tuotteen manuaalisesti yhdellä ajolla sen mukaan, miten organisaation liiketoimintaprosessit ja tämän toiminnon käyttöön liittyvät säännöt on määritetty. Tämä toiminto luo uuden tuotteen ja julkaisee sen automaattisesti nykyiseen yritykseen. Voit luoda uuden tuotteen **Vapautetut tuotteet** **vapautetun tuotteen ylläpidon** työtilassa tai **Vapautettu tuote** -luettelosivulla.
