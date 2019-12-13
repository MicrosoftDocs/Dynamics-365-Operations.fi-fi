---
title: Ostoruutumoduuli
description: Tässä ohjeaiheessa on tietoja ostoruutumoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 11/11/2019
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
ms.openlocfilehash: e86b1881e6829ccc33f36ada453af20c1815a2fa
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811138"
---
# <a name="buy-box-module"></a>Ostoruutumoduuli

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja ostoruutumoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskatsaus

Termi *ostoruutu* viittaa yleensä tuotetietojen sivun alueeseen, joka on sivun yläosassa ja joka isännöi kaikkein tärkeimpiä tuotteen ostamisessa tarvittavia tietoja. (Alue, joka näkyy, kun sivu ladataan ensimmäisen kerran. Näin käyttäjien ei tarvitse vierittää sivua alaspäin nähdäkseen tiedot.)

Ostoruutumoduuli on erityinen säilö, jota käytetään kaikkien tuotetietosivun ostoruutualueella näkyvien moduulien isännöinnissä.

Tuotetietosivun URL-osoite sisältää tuotteen tunnuksen. Kaikki ostoruudun hahmontamisessa vaadittavat tiedot saadaan tästä tuotteen tunnuksesta. Jos tuotteen tunnusta ei ole annettu, ostoruutumoduulia ei hahmonneta sivulla oikein. Tämän vuoksi ostoruutumoduulia ei voi käyttää sivulla, jolla ei ole tuotteen kontekstia (esimerkiksi aloitussivulla tai markkinointisivulla).

## <a name="buy-box-module-properties-and-slots"></a>Ostoruutumoduulin ominaisuudet ja paikat 

Ostoruutumoduuli on säilö, joka ohjaa joitakin perusominaisuuksia, kuten leveyttä. Leveysasetus määrittää, onko säilön sisässä olevien moduulien mahduttava säilöön vai ovatko ne näytön levyisiä.

Ostoruutu jaetaan tuotetietosivulla kahteen alueeseen: media-alue vasemmalla ja sisältöalue oikealla. Paikat edustavat näitä kahta aluetta ostoruutumoduulissa. Kukin paikka on esimääritetty hyväksymään vain tietyt paikan tukemat moduulit. Esimerkiksi **Media**-paikka tukee vain mediavalikoimamoduulia.

Oletusarvoisesti sarakkeiden leveyden suhde media-alueella ja sisältöalueella on 2:1. Teema voi kuitenkin korvata sarakkeiden leveydet. Lisäksi mobiililaitteissa nämä kaksi aluetta pinotaan niin, että alueet näkyvät allekkain.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduulit, joita voidaan käyttää ostoruutumoduulissa

- **Mediavalikoima** – Tämän moduulin avulla esitellään tuotteen kuvat tuotetietosivulla. Moduuli voi tukea yhtä kuvaa tai useita kuvia. Se tukee myös pikkukuvia. Pikkukuvat voivat olla vaakasuuntaisesti (rivinä kuvan alla) tai pystysuuntaisesti (pystyrivinä kuvan vieressä). Mediavalikoimamoduuli voidaan lisätä **Media**-paikkaan ostoruutumoduulissa. Se tukee tällä hetkellä vain kuvia ja videoita.
- **Tuotteen nimi** – Tämä moduuli näyttää tuotteen nimen tuotetietosivulla. Oletusarvoisesti käytetään **H1**-otsikkotunnusta. Otsikkotunnuksen voi kuitenkin muuttaa tarvittaessa.
- **Tuoteluokitus** – Tämä moduuli näyttää luokituksen tähtinä tuotteen asiakasarvioiden perusteella. Ostoruutumoduuli hakee kaikkien tuotteiden arvioinnit arviointipalvelusta.
- **Tuotteen hinta** – Tässä moduulissa näkyy tuotteen hinta. Hinta sisältää aiemmat hinnat ja alennukset.
- **Tuotteen kuvaus** – Tässä moduulissa näkyy tuotteen kuvaus.
- **Tuotteen määritys** – Tässä moduulissa näkyvät tuotteen koko, tyyli ja mitat. Mittojen valitsimet voidaan pinota pystysuuntaisesti tai ne voivat olla rinnakkain. Kun tuotevariantti on valittuna, muut ostoruudun ominaisuudet (esimerkiksi tuotteen kuvaus ja kuvat) päivitetään muuttujan tietojen mukaisiksi.
- **Tuotteen määrä** – Tätä moduulia käytetään tuotteen määrän määrittämiseen. Asetus rajoittaa ostoskoriin lisättävän tuotteen tai muuttujan määrää.
- **Lisää ostoskoriin** – Tätä moduulia käytetään Lisää ostoskoriin -toiminnon suorittamisessa. Ostoskoriin voi lisätä vain tuotteen tai variantin. Toisin sanoen päätuotetta ei voi lisätä ostoskoriin. Moduulissa on **Siirry ostoskoriin** -ominaisuus, jonka sivuston tekijä voi määrittää. Kun tämän ominaisuuden arvoksi on määritetty **Tosi**, käyttäjä siirretään ostoskorisivulle aina, kun Lisää ostoskoriin -toiminto käynnistetään. Kun arvoksi on määritetty **Epätosi**, asiakas voi jatkaa tuotetietosivun selaamista nimikkeiden ostoskoriin lisäämisen jälkeen.
- **Lisää toivomuslistaan** – Tätä moduulia käytetään nimikkeen lisäämisessä asiakkaan toivomuslistaan. Toivomuslistaan voi lisätä vain tuotteen tai variantin. Lisäksi asiakkaan on oltava kirjautuneena sivustoon. Moduuli sisältää virheenkäsittelylogiikkaa, joka varmistaa, että molemmat ehdot täyttyvät.
- **Etsi myymälässä** – Tämä moduuli käynnistää Osta verkosta, nouda myymälästä -työnkulun.
- **Nouda myymälästä** – Tämä moduuli näyttää luettelon lähellä olevista myymälöistä, joista nimikkeen voi noutaa. Oletusarvon mukaan tämä moduuli näyttää myymälät, jotka sijaitsevat 50 mailin päässä asiakkaasta. Arvoa voi kuitenkin muuttaa moduulissa. Kunkin myymälän varasto tarkistetaan, jos varaston tarkistustoiminto on käytössä, ja näkyvissä on soveltuva varastossa- tai varasto tyhjä -viesti.
- **Myymälän haku Bing Mapsin avulla** – Tätä moduulia voi käyttää Nouda myymälästä -moduulin sisässä. Sen avulla asiakkaat voivat hakea myymälöitä syöttämällä sijainnin. Bing Maps -geokoodauksen ohjelmointirajapintaa käytetään tietyn sijainnin muuntamisessa leveys- ja pituusasteiksi. Jos tätä moduulia käytetään, vain asiakkaan nykyisen sijainnin lähellä olevat myymälät näytetään, eikä asiakas voi hakea toista sijaintia.
- **Sisällöntäyteinen lohko** – Tämä moduuli voi näyttää viestin, jonka sivuston tekijä tai jälleenmyyjä haluaa näyttää ostoruudussa. Viesti voi olla esimerkiksi jompikumpi seuraavista: Jos tilaamisessa on ongelmia, soita numeroon 1-800-FABRIKAM tai Ilmainen toimitus tilauksille, joiden arvo ylittää 100 $. Sisällönhallintajärjestelmä (CMS) ohjaa viestintää.

## <a name="buy-box-module-settings"></a>Ostoruutumoduulin asetukset

Ostoruutumoduuleilla on seuraavat kolme määritettävää asetusta:

- **Maksimimäärä** – Kunkin ostoskoriin lisättävän nimikkeen enimmäismäärä. Jälleenmyyjä voi esimerkiksi päättää, että yhdessä tapahtumassa voidaan myydä vain 10 kappaletta kutakin tuotetta.
- **Varaston tarkistus** – Kun arvoksi on asetettu **Tosi**, nimike lisätään ostoskoriin vasta, kun ostoruutumoduuli varmistaa, että nimikettä on varastossa. Tämä varaston tarkistus tehdään sekä skenaarioissa, joissa nimike toimitetaan, että skenaarioissa, joissa se noudetaan myymälästä. Jos arvoksi on määritetty **Epätosi**, varaston tarkistus tehdään vasta, kun nimike on lisätty ostoskoriin ja tilaus on tehty.
- **Varaston puskuri** – Varastoa ylläpidetään reaaliaikaisesti. Jos useat asiakkaat tekevät tilauksia, todellisen varastomäärän ylläpitäminen voi olla vaikeaa. Tämän vuoksi varastolle voidaan määrittää puskuri. Kun varaston tarkistus tehdään ja varasto on pienempi kuin puskurisumma, tuotetta käsitellään kuin se olisi loppunut varastosta. Kun myynti tapahtuu nopeasti useiden kanavien kautta eikä varastomäärää ole täysin synkronoitu, on pienempi riski sille, että nimikettä ei ole varastossa myynnin hetkellä.

## <a name="retail-server-interaction"></a>Vähittäismyynnin palvelimen vuorovaikutus

Ostoruutumoduuli hakee tuotetiedot vähittäismyynnin palvelimen ohjelmistorajapintojen avulla. Tuotetietosivulla olevaa tuotteen tunnusta käytetään kaikkien tietojen noutamisessa.

## <a name="add-a-buy-box-module-to-a-page"></a>Ostoruutumoduulin lisääminen sivulle

Voit lisätä ostoruutumoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Luo osa nimeltä **Ostoruutuosa** ja lisää siihen ostoruutumoduuli.
1. Lisää ostoruutumoduuliin **Media**-paikkaan mediavalikoimamoduuli.
1. Lisää ostoruutumoduulin **Sisältö**-paikkaan seuraavat moduulit: tuotteen nimi, tuotteen arviointi, tuotteen hinta, tuotteen kuvaus, tuotteen määritys, lisäys ostoskoriin, lisää toivomuslistaan ja etsi myymälästä. Voit järjestää **Sisältö**-paikan moduulit uudelleen halutun asettelun saavuttamiseksi.
1. Valitse Etsi myymälä -moduulista. Lisää Nouda myymälästä -moduuli tämän moduulin sisällä olevaan paikkaan.
1. Lisää Myymälän haku Bing Maps -moduuli Nouda myymälästä -moduulin sisällä olevaan paikkaan.
1. Kirjaa sivu sisään ja julkaise se.
1. Luo tuotetietosivulla malli ja anna sen nimeksi **PDP-malli**.
1. Lisää oletussivu.
1. Lisää ostoruutuosa oletussivun **pääpaikkaan**.
1. Tallenna malli, kirjaa se sisään ja julkaise se.
1. Käytä juuri luotua mallia, kun haluat luoda sivun nimeltä **PDP-sivu**.
1. Lisää ostoruutuosa uuden sivun **pääpaikkaan**.
1. Tallenna ja esikatsele sivu. Lisää **?productid=&lt;tuotteen tunnus&gt;** -kyselymerkkijonoparametri esikatselusivun URL-osoitteeseen. Näin tuotekontekstia käytetään esikatselusivun lataamiseen ja käsittelemiseen.
1. Kirjaa sivu sisään ja julkaise se. Tuotetietosivulla näkyy ostoruutu.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)
