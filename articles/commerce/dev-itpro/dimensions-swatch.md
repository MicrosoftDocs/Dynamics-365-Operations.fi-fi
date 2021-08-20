---
title: Tuotedimensioarvojen konfiguroiminen näkymään väriruutuina
description: Tässä aiheessa kuvataan, miten tuotedimensioarvot voidaan konfiguroida väriruutuina Microsoft Dynamics 365 Commerce -pääkonttorissa.
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.20 update
ms.openlocfilehash: b1cef992b3d4e3889dd1d5dcc21a0d1ba3f55acc166f5003fc79f64fc54a8754
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764611"
---
# <a name="configure-product-dimension-values-to-appear-as-swatches"></a>Tuotedimensioarvojen konfiguroiminen näkymään väriruutuina

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten tuotedimensioarvot voidaan konfiguroida väriruutuina Microsoft Dynamics 365 Commerce -pääkonttorissa. Lisätietoja tuotteen dimensioista on kohdassa [Tuotedimensiot](../../supply-chain/pim/product-dimensions.md).

Dynamics 365 Commerce tukee koko-, tyyli- ja väridimensioiden käyttöä tuotemuuttujien erottamiseen toisistaan. Tuotedimensioilla on nimiä, jotka näkyvät tuotetietosivuilla, jotta tuotemuuttujat voidaan valita. Näitä nimiä ovat esimerkiksi "pieni", "keskikokoinen" ja "suuri" kokoja varten sekä värit "musta" ja "ruskea". Jos tuote tukee useita muunnelmia, kunkin tuotevariantin kuvan tarkasteleminen edellyttää useita valintoja. Näin ollen voi olla hidasta ja työlästä, kun asiakkaat selaavat ja valitsevat tuotemuuttumia.

Kun dimensiot näkyvät PDA-pidennyksissä, asiakkaat voivat esikatsella tuotteen vaihteluja visuaalisesti. Niiden avulla voit helposti selata monenlaisia värejä, kuvioita ja tekstuureja sekä tarkastella nopeasti eri tuotevariaatioyhdistelmiä.

Dimensioiden näyttödimensioiden avulla Commerce voi käyttää heksadesimaalikoodeja (hex) ja kuvia dimensioiden näyttämiseen väriruutuina. Lisäksi samankaltaisia dimensioita, kuten värejä, voidaan ryhmitellä tuoteluettelosivuille. Asiakas hakee esimerkiksi tuotteita, jotka ovat sinisiä. Jos siniset dimensioarvot on ryhmitelty yhteen, hakutulosluettelosivulla näkyy eri sävyiset siniset tuotteet. Dimensioiden ryhmittely parantaa merkittävästi tuotteen hienosäätökokemusta ja auttaa asiakkaita hakemaan lisää tuotteita yhden tuotehakukyselyn avulla.

> [!NOTE]
> Väriruutujen näyttödimensiot ovat käytettävissä Dynamics 365 Commercen versiosta 10.0.20.

Seuraavassa kuvassa on esimerkki, jossa värit näkyvät Commercen PDP:ssä väriruutuina.

![Esimerkki tuotetietosivulla väriruutuina näkyvistä väreistä.](../dev-itpro/media/swatch_pdp.png)

Seuraavassa kuvassa on esimerkki, jossa värit näkyvät Commercen hakutulosluettelusivulla väriruutuina.

![Esimerkki hakutulosluettelosivulla väriruutuina näkyvistä väreistä.](../dev-itpro/media/swatch_searchresults.PNG)

## <a name="enable-the-display-dimensions-as-swatches-feature-in-commerce-headquarters"></a>Näyttödimensioiden ottaminen käyttöön väriruutuominaisuuksina Commerce headquarters -sovelluksessa

Näyttödimensiot otetaan käyttöön väriruutuominaisuutena Commerce-pääkonttoriominaisuudessa valitsemalla **Työtilat \> Ominaisuuksien hallinta** ja ottamalla käyttöön **Ota käyttöön mekanismi ilmaisemaan dimensiot väriruutuna** -ominaisuus. Kun tämä ominaisuus on käytössä, kullekin dimensiolle lisätään kolme uutta kenttää Commerce-pääkonttorissa: **Heksakoodi**, **URL-osoite** (kuvia varten) ja **RefinerGroup**.

## <a name="configure-dimension-values-in-commerce-headquarters"></a>Dimensioarvojen konfiguroiminen Commerce headquarters -sovelluksessa

Näyttödimensiot väriruutuina -ominaisuus tukee koko-, tyyli- ja väridimensioita. Asianmukaisille dimensioille määritetyt heksakoodi- ja kuva-URL-arvot voidaan määrittää Commerce headquarters -sovelluksessa. Jos dimensiolle ei ole oletusarvoisesti annettu heksakoodia ja kuvan URL-arvoja, järjestelmä näyttää dimension nimitiedoston tekstin.

Konfiguraation voi tehdä seuraavilla tasoilla:

- **Dimensio** – Avaa Commerce Headquartersissa dimension sivu etsimällä **väriä**, **kokoa** tai **tyyliä**. Ruudukossa näkyvät kunkin sivun dimensioarvot. Voit hallita näyttöjärjestystä, heksakoodia ja kuvan URL-arvoja. Seuraavassa kuvassa on esimerkki **Värit** -sivun määrityksestä.

    ![Esimerkki dimensiomäärityksestä Värit-sivulla.](../dev-itpro/media/swatch_Color.PNG)

- **Dimensioryhmä** – Dynamics 365 Commercessa voit käyttää **RefinerGroup**-ominaisuutta dimensioryhmien luomiseen. Jos dimensioryhmät on määritetty, avaa haluamasi sivu etsimällä **Väriryhmä**, **Kokoryhmä** tai **Tyyliryhmä**. Jokaisella sivulla voit hallita heksakoodia, kuvan URL-osoitetta ja tarkentajaryhmän arvoja. Seuraavassa kuvassa on esimerkki **Väriryhmät**-sivun määrityksestä.

    ![Esimerkki dimensiomäärityksestä Väriryhmät-sivulla.](../dev-itpro/media/swatch_colorGroup.PNG)

- **Tuotedimensio (tuotteen luonnin aikana)** – Kun luot uuden tuotteen, voit syöttää dimensioarvot **Tuotedimensiot**-sivulla. Aiemmin luotujen tuotteiden osalta **Heksakoodi**-, **URL-osoite**- (kuvia varten) ja **RefinerGroup**-kentät on ehkä jo määritetty. Voit kuitenkin muuttaa arvoja tarpeen mukaan. Seuraavassa kuvassa on esimerkki **Tuotedimensiot**-sivun määrityksestä.

    ![Esimerkki dimensiomäärityksestä Tuotedimensiot-sivulla.](../dev-itpro/media/swatch_product_dimensions.PNG)

> [!NOTE]
> Heksakoodin ja kuvan URL-konfiguraatioiden hallintaprosessi noudattaa samaa kaavaa, jota käytetään dimensioiden näyttöjärjestyksen hallinnassa.

## <a name="configure-dimension-values-by-using-hex-codes"></a>Dimensioarvojen konfiguroiminen heksakoodeja käyttämällä

Useimpien väridimensioiden dimensioille on annettava heksakoodin väriarvo Commerce headquarters -dimensiosivuilla. Esimerkiksi mustan värin koodiksi tulee määrittää heksakoodiarvo **#00000**. Kun Commerce muodostaa sivustosivun, heksakoodia edustaa väriruutu.

Seuraavassa kuvassa on esimerkki siitä, missä väridimensiot on konfiguroitu heksakoodiarvoja käyttäen.

![Esimerkki dimensiomäärityksestä, joka käyttää heksakoodeja.](../dev-itpro/media/swatch_color_hexcode.png)

## <a name="configure-dimension-values-by-using-image-urls"></a>Dimensioarvojen konfiguroiminen kuvan URL-osoitteita käyttämällä

Jotkin väridimensiot edustavat malleja, eivät värejä. Esimerkiksi väridimensiota voidaan kuvata myös nimellä "leopardi". Tällöin voit edustaa väridimensioita tehokkaammin käyttämällä julkaistuja kuvia heksakoodien sijaan.

Jokainen kuva on ladattava Commercen sivustonmuodostimeen ja julkaistava. Kirjoita sitten julkaistun kuvan URL-osoite commerce headquarters -dimension sivuille. Jos dimensio on valittu näytettäväksi väriruutuna, mutta heksakoodia ei ole määritetty, Commerce tekee kuvahaun, kun se muodostaa sivun. Jos kuvahaku epäonnistuu, Commerce näyttää dimension nimitiedoston tekstin.

Seuraavassa kuvassa on esimerkki, jossa käytetään kuvan URL-osoitteita **Värit** -sivun määrityksessä.

![Esimerkki dimensiomäärityksestä, joka käyttää kuvan URL-osoitteita.](../dev-itpro/media/swatch_color_urls.PNG)

Mediamallin avulla voit määrittää kuvien URL-osoitteita, aivan samoin kuin tuote- ja luokkakuvien osalta. Kun kuvia ladataan sivustonmuodostajaan, tiedostonimeä kuvaavien käytäntöjen ja tiedostopolkujen on oltava yhdenmukaisia.

Seuraavassa kuvassa on esimerkki, jossa käytetään kuvan URL-osoitteita mediasisältömallin määrityksessä.

![Esimerkki mediamallin määrityksestä.](../dev-itpro/media/swatch_media_template.PNG)

## <a name="configure-dimension-values-by-using-both-hex-codes-and-image-urls"></a>Dimensioarvojen konfiguroiminen sekä heksakoodeja että kuvan URL-osoitteita käyttämällä

Useimpien väridimensioiden osalta voit määrittää sekä heksakoodeja että kuvien URL-osoitteita. Commerce renderoinnin varalogiikka hakee automaattisesti joko heksakoodin tai kuvan URL-osoitteen, joka näyttää väriruudun. Kun määrität väridimensioita käyttämällä sekä heksakoodeja että kuvien URL-osoitteita, voit helpottaa kuvien hallintaa, kun värien määrä on suuri.

Seuraavassa kuvassa on esimerkki, jossa käytetään sekä heksakoodeja että kuvan URL-osoitteita **Värit** -sivun määrityksessä.

![Esimerkki dimensiomäärityksestä, joka käyttää sekä heksakoodeja että kuvan URL-osoitteita.](../dev-itpro/media/swatch_color_hexandimage.png)

## <a name="configure-refiner-groups"></a>Tarkentajaryhmien määrittäminen

Kun määrität dimensioarvolle heksakoodin tai kuvan URL-osoitteen, voit määrittää arvon myös **RefinerGroup**-kenttään. Tässä kentässä määritetään dimensio, jota on käytettävä samankaltaisten dimensioarvojen ryhmittelemiseksi tarkentajakokemuksessa.

Jos väridimensioarvot ovat esimerkiksi sininen, siniruudullinen, vaalean sininen ja tummansininen, kukin arvo on yhdistetty eri heksakoodiin tai kuvan URL-osoitteeseen. Siksi jokainen arvo näkyy eri värinä asianmukaisten tuotteiden PPP-korteissa ja tuotekortissa. Jos kuitenkin liität kaikki nämä väridimensioarvot **Sinisen** **RefinerGroup**-arvoon, haku siniset tuotteet luovat luettelosivun hakutuloksia tuotteista, joiden dimensioväriarvot ovat sininen, siniruudullinen, vaaleansininen ja tummansininen.

Seuraavassa kuvassa on esitetty Commerce headquarters -kohteen **Väri**- ja **RefinerGroup**-ominaisuuksien suhde.

![Esimerkki tarkentajaryhmän hallinnasta.](../dev-itpro/media/swatch_refiner_group.png)

## <a name="manage-images-in-commerce-site-builder"></a>Hallitse kuvia Commercen sivuston muodostimessa

Jos dimensioarvoissa käytetään kuvien URL-osoitteita, vastaavat kuvat on ladattava Commercen sivustonmuodostimeen. Kunkin kuvan sijainnin tulisi vastata Commerce Headquartersin kuvalle määritettyä tiedostonimeä ja kansiopolkua. Kuvatiedostot on ladattava asianmukaisiin luokan sijainteihin sivustonmuodostajassa. Esimerkiksi värikuvat on ladattava **Väri**-luokkakansioon. Lisätietoja kuvien lataamisesta sivustonmuodostimen on kohdassa [Kuvien lataaminen](../dam-upload-images.md).

Seuraavassa kuvassa on esimerkki, jossa palvelimeen **lataa tiedostoja** -valintaikkunaa käytetään kuvien lataamiseen sivustonmuodostimen mediakirjastoon. Se korostaa **Koko**-, **Väri**- ja **Tyyli**-luokat, jotka ovat valittavissa.

![Esimerkki kuvatiedostoluokista lataamisen aikana sivuston muodostimen mediakirjastoon lataamisen aikana.](../dev-itpro/media/swatch_sitebuilder.png)

## <a name="enable-swatch-display-on-e-commerce-site-pages"></a>Ota käyttöön väriruutunäyttö sähköisen kaupankäynnin -verkkosivustoilla

Ennen kuin väriruudut voivat näkyä verkkokaupan verkkosivuilla, jotka edellyttävät dimension valintaa, kuten PDP:t ja luettelosivut, sinun on määritettävä dimensiosivustoasetukset Commerce headquartersissa. Lisätietoja on kohdassa [Dimensioiden sivustoasetusten käyttäminen](../dimension-settings.md).

Lisäksi sinun tulisi ottaa käyttöön **Sisällytä tuotemääritteet hakutuloksiin** -ominaisuus hakutulosmoduuleille. Jos sivustosi käyttää mukautettuja luokkasivuja, sinun on päivitettävä näillä sivuilla käytettävät hakutulosmoduulit niin, että **Sisällytä tuotemääritteet hakutulosominaisuuksiin** -ominaisuus on käytössä. Lisätietoja on kohdassa [Hakutulokset-moduuli](../search-result-module.md).

## <a name="inventory-awareness-on-swatches"></a>Väriruutujen varastotietoisuus

Väriruuduissa on valinnainen ominaisuus, joilla näytetään tuotevariantin värin tai dimension varastosaatavuus. Tuotetta myydään esimerkiksi erikokoisena, mutta jotkin koot ovat loppuneet varastosta. Tässä tapauksessa varastosta loppuneiden tuotteiden väriruudut hahmonnetaan eri tavalla, mikä ilmaisee, ettei niitä ole saatavana. Tämä ominaisuus auttaa vähentämään napsautuksia, jotka asiakkaiden on tehtävä tuotteen saatavuuden selvittämiseksi.

Väriruudun varastosaatavuuden ominaisuus voidaan määrittää käyttämään sekä PDP- että haku- tai luokkaluettelosivuja, joissa väriruudut näytetään. Se aktivoidaan määrittämällä **Päivitä media dimensiota valittaessa** -ominaisuuden arvoksi **Tosi** [mediavalikoimamoduulissa](../media-gallery-module.md). Tämä asetus antaa mahdollisuuden mediavalikoiman kuvien päivittämiseen, kun dimensiot valitaan. 

> [!IMPORTANT]
> Väriruudun varastosaatavuusominaisuus on saatavana Commercen versiosta 10.0.21 alkaen. Se edellyttää Commercen moduulikirjastopaketin 9.31 asentamista.

Seuraavassa kuvassa on esimerkki varastotietoisuudesta PDP-sivun kokoväriruuduissa.

![Esimerkki varastotietoisuudesta PDP-sivun kokoväriruuduissa](../dev-itpro/media/swatch_inventory.png)

## <a name="display-swatches-in-pos-and-other-channels"></a>Väriruutujen näyttäminen myyntipisteissä ja muissa kanavissa

Commercella ei tällä hetkellä ole käytössä valmiita paketteja, jotka tukisivat myyntipisteen ja muiden kanavien väriruutujen näyttämistä. Väriruutujen näyttötoiminto voidaan toteuttaa laajennuksena, koska kanavan ohjelmointirajapinnat palauttavat heksakoodit ja kuvan URL-osoitteet, jotka ovat pakollisia muodostuksen jälkeen.

## <a name="additional-resources"></a>Lisäresurssit

[Hakutulosmoduuli](../search-result-module.md)

[Dimensioiden toimipaikka-asetusten kohdistaminen](../dimension-settings.md)

[Tuotedimensiot](../../supply-chain/pim/product-dimensions.md)

[Lataa kuva palvelimeen](../dam-upload-images.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
