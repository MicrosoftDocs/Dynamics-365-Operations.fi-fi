---
title: Myyntipisteen varastohakutoiminto
description: Tässä artikkelissa kuvataan, miten myyntipisteen varastohakutoimintoa käytetään Dynamics 365 Commerce -myyntipisteessä tuotteiden käytettävissä olevan varaston saatavuuden tarkastelemiseksi myymälöissä ja varastoissa.
author: boycezhu
ms.date: 08/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: 01f10c348c61ffbcb30be26a57b3edd436aacc8f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850246"
---
# <a name="inventory-lookup-operation-in-pos"></a>Myyntipisteen varastohakutoiminto

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, miten myyntipisteen varastohakutoimintoa käytetään Dynamics 365 Commerce -myyntipisteessä tuotteiden käytettävissä olevan varaston saatavuuden tarkastelemiseksi myymälöissä ja varastoissa.

Tarkka koko organisaation kattava varastonäkymä auttaa myyntiedustajia tarjoamaan nopeaa ja tehokasta asiakaspalvelua. Tärkein hetki on se hetki, jolloin asiakas on valmis tekemään ostopäätöksen. On tärkeää, että myymälän kassojen käytettävissä on reaaliaikaiset tai lähes reaaliaikaiset varastotiedot, jotta he voivat luvata tuotteen toimituksen ja noudon tarkasti.

Commerce-myyntipisteen varaston hakutoiminnon avulla vähittäismyyjät voivat tehostaa toimintaa ja saada tietoa yhdistämällä myymälät Commerce-pääkonttorisovellukseen. Tämä toiminto tarjoaa tuotteiden saatavuuden näkymän myymälöiden ja varastojen välillä. Sen avulla jälleenmyyjät voivat myös tehostaa toimintaa ja kustannussäästöjä, sillä reaaliaikainen varastosuunnittelu paranee.

Kun varastohakutoiminto aloitetaan myyntipistesovelluksesta, kassanhoitaja syöttää numeronäppäimistön avulla tuotenumeron varastotietojen kyselyä varten. Jos syötetyllä tuotteella on variantteja, kassanhoitaja voi vaihtoehtoisesti valita dimensioita tai muita arvoja tarkistaakseen tietyn tuotevariantin varastotiedot.

## <a name="inventory-lookup-list-view-for-individual-products"></a>Yksittäisten tuotteiden varastohakuluettelon näkymä

Yksittäisen tuotteen varastohakutoiminto sisältää varastohakuluettelonäkymän, joka sisältää seuraavat sijaintiluettelon tuotetiedot:

- **Varasto** – viittaa tuotteen käytettävissä olevaan fyysiseen määrään.
- **Varattu** – viittaa pääkonttorista haettuun fyysiseen varattuun määrään.
- **Tilattu** – viittaa pääkonttorista haettuun yhteensä tilattuun määrään.
- **Yksikkö** – viittaa pääkonttorissa määritettyihin varaston mittayksikköihin.

Sijaintien luettelonäkymä sisältää kaikki myymälät ja varastot, jotka on konfiguroitu täyttämisryhmiin, joihin nykyinen myymälä on linkitetty, seuraavan esimerkin kuvan mukaisesti.

![Varastohakutoiminnon luettelonäkymä.](media/inventory-lookup-list-view.png)

> [!NOTE]
> Varmista, että nykyinen myymälä sisältyy asiaan liittyviin täyttämisryhmiin.

Myyntipisteen sovelluspalkissa ovat käytettävissä seuraavat toiminnot:

- **Lajittelu** – Tämän toimenpiteen avulla myyntipistekäyttäjä voi lajitella luettelonäkymän tiedot erilaisten ehtojen perusteella. Sijaintiin perustuva lajittelu on oletuslajitteluna.

    - **Maantieteellinen sijainti** (lähimmästä sijainnista kauimpaan sijaintiin sen perusteella, mikä on etäisyys nykyiseen myymälään)
    - **Nimi** (nousevassa tai laskevassa järjestyksessä)
    - **Myymälän numero** (nousevassa tai laskevassa järjestyksessä)
    - **Varasto** (laskevassa järjestyksessä)
    - **Varattu** (laskevassa järjestyksessä)
    - **Tilattu** (laskevassa järjestyksessä)

- **Suodata** – tämän toimenpiteen avulla myyntipistekäyttäjä voi tarkastella tietyn sijainnin suodatettuja tietoja.
- **Näytä myymälän käytettävyys** – tämän toimenpiteen avulla myyntipisteen käyttäjä voi tarkastella valitun myymälän tuotteen luvattavissa olevia määriä (ATP).
- **Näytä myymälän sijainti** – tämä toiminto avaa erillisen sivun, joka näyttää valitun myymälän karttanäkymän, osoitteen ja aukioloajat.
- **Nouto myymälästä** – tämä toiminto luo asiakastilauksen tuotteelle, joka noudetaan valitusta myymälästä, ja ohjaa käyttäjän tapahtumanäyttöön.
- **Lähetä tuote** – tämä toiminto luo asiakastilauksen tuotteelle, joka lähetetään valitusta myymälästä, ja ohjaa käyttäjän tapahtumanäyttöön.
- **Näytä kaikki variantit** - jos tuotteella on variantteja, tämä toimenpide siirtyy luettelonäkymästä matriisinäkymään, jossa näkyvät tuotteen kaikkien varianttien varastotiedot.
- **Lisää tapahtumaan** – tämä toiminto lisää tuotteen ostoskoriin ja ohjaa käyttäjän tapahtumanäyttöön.

> [!NOTE]
> Commercen versiossa 10.0.17 käyttöönotettu sijaintiin perustuva lajittelu näyttää nykyisen myymälän ensimmäisenä. Muissa sijainneissa sijainnin ja nykyisen myymälän välinen etäisyys määräytyy Commercen pääkonttorisovelluksessa määritettyjen koordinaattien (leveys- ja pituusasteet) mukaan. Myymälän sijaintitiedot määritetään myymälään liittyvän toimintayksikön ensisijaisessa osoitteessa. Jos varasto ei ole myymälässä, sijaintitiedot määritetään varaston osoitteessa. Ennen versiota 10.0.17 luettelonäkymässä näkyy aina nykyinen myymälä ensimmäisenä ja muut sijainnit lajitellaan aakkosjärjestyksessä.
>
> **Näytä myymälän käytettävyys**-, **Näytä myymälän sijainti**-, **Nouto myymälästä**- ja **Lähetä tuote** -toiminnot eivät ole käytettävissä muissa kuin myymälävarastoissa.

## <a name="inventory-lookup-matrix-view-for-variants"></a>Varianttien varastohaun matriisinäkymä

Jos päätuotteessa on variantteja, varastohakutoiminto sisältää myös dimensiopohjaisen matriisinäkymän, jossa näkyvät valitun sijainnin päätuotteen kaikkien varianttien varastojen käytettävyystiedot. Matriisinäkymä näyttää oletusarvoisesti nykyisen myymälän tiedot. Sovelluspalkin **Myymälä**-toiminnon avulla voit etsiä varastotietoja muista myymälöistä, jotka on konfiguroitu täyttämisryhmissä, johon nykyinen myymälä on linkitetty.

Seuraavassa esimerkkikuvassa näkyy myyntipisteen varastohakumatriisinäkymä.

![Varastohakutoiminnon matriisinäkymä.](media/inventory-lookup-matrix-view.png)

Matriisinäkymässä kukin solu edustaa yksittäistä varianttia ja näyttää oikeassa alakulmassa käytettävissä olevan varaston (käytettävissä olevan fyysisen) arvon sekä **varatun** (fyysisen varatun) arvon ja **tilatut** (tilattu yhteensä) arvot vasemmassa yläkulmassa. Seuraavassa taulukossa selitetään eri käytettävissä olevien arvojen merkitykset.

| Käytettävissä olevan varaston arvo                            | kuvaus |
|------------------------------------------|-------------|
| Numeerinen arvo, joka on suurempi kuin 0 (nolla) | Variantti on vapautettu valittuun sijaintiin, ja voit tehdä solussa lisätoimintoja. |
| **0** (nolla)                             | Variantti on vapautettu valittuun sijaintiin mutta nimike ei ole käytettävissä valitussa sijainnissa. Voit tehdä solussa muita toimia. |
| **–** tai passiivinen solu              | Varianttia ei ole vapautettu valittuun sijaintiin etkä voi tehdä solussa lisätoimintoja. |

Dimensioarvojen näyttöjärjestys matriisinäkymässä perustuu Commerce-pääkonttorin dimension näyttöjärjestyksen konfiguraatioon. Voit muuttaa dimension näyttöjärjestyksen konfiguraatiota valitsemalla uuden käytettävän dimension. 

Seuraavat toiminnot ovat käytettävissä matriisinäkymän solussa:

- **Myy nyt** – tämä toiminto lisää valitun variantin ostoskoriin ja ohjaa käyttäjän tapahtumanäyttöön.
- **Nouto myymälästä** – tämä toiminto luo asiakastilauksen valitulle variantille, joka noudetaan valitusta myymälästä, ja ohjaa käyttäjän tapahtumanäyttöön.
- **Lähetä tuote** – tämä toiminto luo asiakastilauksen valitulle variantille, joka lähetetään valitusta myymälästä, ja ohjaa käyttäjän tapahtumanäyttöön.
- **Käytettävyys** – tämä toiminto vie käyttäjän erilliselle sivulle, jossa näkyvät valitun myymälän valitun muuttujan ATP-määrät.
- **Näytä kaikki sijainnit** – tämä toiminto siirtyy varaston vakiomuotoiseen varaston käytettävyyden luettelonäkymään, jossa näkyvät valitun muuttujan varastotiedot.
- **Näytä tuotetiedot** - tämä toimenpide ohjaa käyttäjän valitun muuttujan tuotetietosivulle (PDP).

## <a name="access-inventory-lookup-from-other-pages-in-pos"></a>Varastohaun käyttö myyntipisteen muilla sivuilla

Myyntipisteen käyttäjät voivat käyttää varastohakutoimintoa muilla myyntipisteen sivuilla.

Seuraavassa esimerkkikuvassa näkyy myyntipisteen varastohaun tulokset tuotetietosivulta.

![Varastohaku tuotetietosivulta.](media/inventory-lookup-from-product-details-page.png)

Päätuotteen tuotetietosivulla voidaan käynnistää varaston hakumatriisinäkymä käyttämällä sovelluspalkin **Näytä kaikki muuttujat** -toimintoa, joka sisältää nykyisen myymälän varaston käytettävyystiedot tuotteen kaikkien muuttuja varten. Tuotetietosivu näyttää yksittäisen tuotteen käytettävissä olevan varaston (käytettävissä olevan fyysisen) arvon nykyisessä myymälässä. Lisäksi voit valita **Muiden myymälöiden varasto** -linkin ja käynnistää varastohakutoiminnon, jonka avulla voit tarkistaa tuotteen käytettävyyden muissa myymälöissä tai varastoissa.

> [!NOTE]
> **Näytä kaikki variantit** -toiminto tuotetietosivulla on käytettävissä vain niillä päätuotteilla, joilla on variantteja. Se ei ole käytettävissä tietyissä tuotteissa tai myyntirakenteissa.

Voit määrittää varastohakutoiminnon näkymään painikeruudukon linkkinä myyntipisteen tapahtumanäytössä. Kun käyttäjä valitsee konfiguroinnin jälkeen ostoskorin rivin ja valitsee sitten **Varastohaku**-painikkeen, näkyviin tulee valitun tuotteen varastohakuluettelonäkymä. Lisätietoja painikeruudukoiden määrittämisestä myyntipisteen näytön asettelun suunnittelutyökalun avulla on kohdassa [Myyntipistekäyttöliittymän visuaaliset kokoonpanot](pos-screen-layouts.md).

## <a name="inventory-lookup-with-channel-side-calculation"></a>Varastohaku kanavanpuoleisella laskennalla

Commerce-versiossa 10.0.9 ja sitä aiemmissa versioissa **käytettävissä oleva fyysinen** -arvo varastohakutoiminnossa haetaan Commerce-pääkonttorista reaaliaikaisen huoltokutsun avulla. Commerce-versiossa versiossa 10.0.10 ja sitä myöhemmässä versiossa voit määrittää myyntipisteen varastohakutoiminnon käyttämään Commerce-palvelimen kanavanpuolen laskentaa käytettävissä olevan fyysisen arvon määrittämiseen. Tämä arvo voi antaa käyttövarastosta luotettavamman ja tarkemman arvion. Tämä saadaan ottamalla huomioon ne tapahtumatiedot, joita ei ole vielä synkronoitu pääkonttoriin. Lisätietoja kanavanpuoleisen varaston laskemisesta ja siihen liittyvästä pääkonttorin myyntipisteen konfiguraatiosta on kohdassa [Vähittäismyyntikanavien varaston käytettävyyden laskeminen](calculated-inventory-retail-channels.md).

## <a name="additional-resources"></a>Lisäresurssit

[Myyntipistekäyttöliittymän visuaaliset kokoonpanot](pos-screen-layouts.md)

[Vähittäismyyntikanavien varaston käytettävyyden laskeminen](calculated-inventory-retail-channels.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
