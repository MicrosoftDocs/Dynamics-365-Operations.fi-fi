---
title: Kanavien yhdistäminen sähköisen kaupankäynnin sivustoihin
description: Tässä artikkelissa kuvataan joitakin yleisimpiä Microsoft Dynamics 365 Commerce -ohjelman kanavan määritysskenaarioita, joita voidaan ekstrapoloida useimpien muiden liiketoimintavaatimusten osalta.
author: samjarawan
ms.date: 05/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 94c43df26e8d6e55a5b6d459b65066d5873e1063
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902760"
---
# <a name="map-channels-to-e-commerce-sites"></a>Kanavien yhdistäminen sähköisen kaupankäynnin sivustoihin

Tässä artikkelissa kuvataan joitakin yleisimpiä Microsoft Dynamics 365 Commerce -ohjelman kanavan määritysskenaarioita, joita voidaan ekstrapoloida useimpien muiden liiketoimintavaatimusten osalta.

Dynamics 365 Commerce tukee useita liiketoimintaskenaarioita , joita käytetään [online-kanavien](#channels) määrityksessä, joissa on määritetty tuote, hinta ja alennukset [sähköisen kaupankäynnin sivuston](#e-commerce-sites) kokemuksille asiakkaille.

Tämä artikkeli kattaa seuraavat skenaariot:

- **Yksikielinen kanava, jolla on yksi sähköisen kaupankäynnin sivuston kokemus.** Tämä skenaario voi koskea esimerkiksi yksittäistä brändisivustoa, joka on määritetty Yhdysvaltain englanninkielisille markkina-alueille.
- **Monikielinen kanava, jolla on yksi lokalisoitu sivuston kokemus.** Tämä skenaario voi koskea esimerkiksi yksittäistä brändisivustoa, joka on määritetty Kanadaan ranskankieliselle ja englanninkieliselle tuelle. Tässä skenaariossa eri kieliä valitsevilla käyttäjillä on sama sivustokokemus, mutta se on lokalisoitu käyttäjän valitulle kielelle.
- **Monikielinen kanava, jolla on eri sivuston kokemus kieltä kohden.** Tämä skenaario voi koskea esimerkiksi yksittäistä brändisivustoa, joka on määritetty Kanadaan ranskankieliselle ja englanninkieliselle tuelle. Tässä skenaariossa jokaisella kielellä on yksilöllinen sivustokokemus.
- **Useita kanavia (yksikielinen ja/tai monikielinen), joissa on yksi lokalisoitu sivustokokemus.** Tämä skenaario voi koskea esimerkiksi yksittäistä brändisivustoa, joka on määritetty Australiaan ja Uuteen-Seelantiin. Tässä skenaariossa kummallakin maalla on sama sivustokokemus englanniksi, mutta kullekin maalle on konfiguroitu erilaisia tuotteita, valuuttoja, hintoja, alennuksia ja lähetystapoja.
- **Useita kanavia (yksikielinen ja/tai monikielinen), joissa on eri sivustokokemus kanavaa kohden.** Tämä skenaario voi koskea esimerkiksi yksittäistä brändisivustoa, joka on määritetty Australiaan, Kanadaan ja Saksaan useille kielille. Tässä skenaariossa kullakin maalla on yksilöllinen sivustokokemus, joka on konfiguroitu erilaisilla tuotteilla, valuutoilla, hinnoilla, alennuksilla ja lähetystavoilla.

## <a name="channels"></a>Kanavat

Kanava (tunnetaan myös verkkokauppana tai verkkokanavana) edustaa verkkokaupan myymälää, jota käytetään tuotteiden, hinnoittelun, alennusten, kielien, maksutapojen, toimitustapojen, täyttämiskeskuksen ja muiden sähköisen kaupankäynnin asiakkaiden käytettävissä olevien verkkokokemusten hallinnassa. Kanavat luodaan ja niitä hallitaan Commerce Headquarters -sovelluksessa, ja ne on yhdistetty yhteen [yritykseen](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json#legal-entities). Yritys sijaitsee yleensä yhdessä maassa, jossa kanava edellyttää veroilmoitusta, ja sen voi konfiguroida vain yhdellä valuutalla.

Lisätietoja kanavista on [Kanavien esittely](channels-overview.md) -kohdan ohjeaiheessa. Lisätietoja online-kanavan luomisesta on kohdassa [Online-kanavan määritys](channel-setup-online.md).

Seuraavassa Commerce headquarters -esimerkissä näytetään online-kanavien oletusarvot, jotka on otettu käyttöön Dynamics 365 Commerce -ohjelmassa, jos esittelytietovaihtoehto on valittu.

![Commerce headquartersin oletusarvoiset esittelytietokanavat.](media/channel-mapping-1.png)

## <a name="e-commerce-sites"></a>Sähköisen kaupankäynnin sivustot

Sähköinen kaupankäynti -sivusto sisältää joukon sivuja, joita asiakkaat käyttävät selaamiseen ja ostamiseen. Sähköisen kaupankäynnin sivustoja hallitaan Commercen sivuston muodostimessa.

Lisätietoja sivustojen luomisesta ja hallinnasta sivuston muodostimessa on kohdassa [Sähköisen kaupankäynnin sivuston yleiskuvaus](online-store-overview.md).

## <a name="common-channel-mapping-scenarios"></a>Kanavan yleiset määritysskenaariot

Dynamics 365 Commerce tukee monenlaisia kanava määritysskenaarioita. Seuraavat kanavan määritysskenaariot ovat vain osajoukko kaikista mahdollisista kanavamäärityksistä. Ne on tarkoitettu oppaaksi, joka auttaa suunnittelemaan kaikki yksilölliset liiketoimintaskenaariot. Fiktiivistä Adventure Works -urheilutarvikemyymälää käytetään kunkin skenaarion esimerkkinä Dynamics 365 Commerce -demotietojen kanssa.

### <a name="single-language-channel-that-has-a-single-e-commerce-site-experience"></a>Yksikielinen kanava, jolla on yksi sähköisen kaupankäynnin sivuston kokemus.

Perusskenaariossa yhdellä kanavalla on vain yksi kieli myyntiä varten yksillä markkinoilla. Esimerkki tästä skenaariosta on Adventure Works -verkkomyymälä, joka on määritetty vain Yhdysvaltojen englanninkieliselle markkina-alueelle.

Seuraavassa esimerkkikuvassa on Commerce headquartersin kanavamääritys. Tässä konfiguraatiossa online-kanava tukee vain yhtä kieltä (**en-us**), yhtä valuuttaa (**USD**) ja yhtä liiketoimintayksikköä (**usrt**), jota käytetään veroraporteissa.

![Commerce headquarters -sovelluksessa korostetut Adventure Works -verkkokaupan yritys-, valuutta- ja kieliarvot.](media/channel-mapping-3.png)

Yksittäinen online-kanava voidaan määrittää yhteen verkkokaupan sivustoon sivuston muodostimessa. Lisätietoja uuden sivuston luomisesta ja sen liittämisestä kanavaan on tämän artikkelin kohdassa [Kanavan liittäminen sivustoon sivuston muodostimessa](#map-a-channel-to-a-site-in-site-builder).

### <a name="multi-language-channel-that-has-a-single-localized-site-experience"></a>Monikielinen kanava, jolla on yksi lokalisoitu sivuston kokemus

Tässä skenaariossa yksi kanava tukee useita kieliä. Siksi tuotenimet, kuvaukset ja määritteet voidaan lokalisoida Commerce Headquarters -sovelluksessa. Jotta saat täysin lokalisoidun sivustokokemuksen, sivuston markkinointisisällön voi myös lokalisoida Commercen sivuston muodostimessa.

Tämän skenaarion rajoitus on se, että yksi kanava voidaan konfiguroida vain yhdellä valuutalla, yhdellä yrityksellä sekä yhdellä tuote- ja hintajoukolla. Tämä konfigurointi toimii parhaiten maissa, joissa on yksi valuutta ja useita kieliä (esimerkiksi Kanada, jossa on englanti ja ranska), yksi yritys ja yksi tuote- ja hintajoukko.

Kanavan eri kielet voidaan konfiguroida omalla toimialuenimellään. `www.adventure-works.ca`-toimialue voidaan konfiguroida esimerkiksi Kanadan englanninkieliseksi versioksi, ja `www.adventure-works-fr.ca`-toimialueen voi konfiguroida Kanadan ranskankieliseksi versioksi. Vaihtoehtoisesti kanavan eri kielet voidaan konfiguroida yhdessä toimialueessa, ja sitten kullekin kielelle voidaan käyttää eri polkua. `www.adventure-works.ca`-toimialue voidaan konfiguroida esimerkiksi Kanadan englanninkieliseksi versioksi, ja sitten `www.adventure-works.ca/fr`-polkua voidaan käyttää Kanadan ranskankieliselle versiolle. [Maantieteellisen sijainnin tunnistus](geo-detection-redirection.md) on myös mahdollista määrittää, jotta käyttäjä voidaan ohjata automaattisesti oikeaan sivustoon käyttäjän sijainnin perusteella.

Lisätietoja siitä, miten asiakkaat voivat vaihtaa kieliä manuaalisesti, on tämän artikkelin [Sivuston valitsinmoduulin lisääminen ja määritys](#add-and-configure-the-site-picker-module). Lisätietoja lokalisoitujen sivujen ja osien mukauttamisesta on kohdassa [Useita kanavia ja kieliä sisältävän sivuston sisällön hallinta](#manage-site-content-that-has-multiple-channels-and-languages).

### <a name="multi-language-channel-that-has-a-different-site-experience-per-language"></a>Monikielinen kanava, jolla on eri sivuston kokemus kieltä kohden

Voit käyttää skenaariota, jossa yksi kanava tukee useita kieliä, mutta kullekin kielelle muodostetaan täysin erilainen sivustokokemus. Suositeltava menetelmä tämän skenaarion toteuttamiseen on käyttää [sivun muuttujia](#implement-page-variants-for-each-language) yhdessä sivustossa.

Toinen tapa on luoda uusi sähköisen kaupankäynnin sivusto jokaiselle sivuston muodostimen kielelle ja yhdistää kukin sivusto sitten yksittäiseen verkkokanavaan ja kieleen. Tuloksena on yksi online-kanava, joka on yhdistetty useisiin sähköisen kaupankäynnin sivustoihin, yksi kutakin kieltä kohden. Tämä usean sivuston menetelmä edellyttää lisähallintaresursseja, koska sivuston muodostimessa on hallittavana useita sivustoita.

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-single-localized-site-experience"></a>Useita kanavia (yksikielinen ja/tai monikielinen), joissa on yksi lokalisoitu sivustokokemus

Brändisivusto voi edellyttää useita verkkokanavia aluetta kohden tukeakseen eri valuuttaa, tuotejoukkoa ja hintajoukkoa kullekin kanavalle yhdessä sivustossa. Esimerkiksi Adventure Works -sivustossa voi olla Kanadan markkinoille verkkokanava, jolla on useita kieliä, yksi kanava Yhdysvaltain markkinoille yhdellä kielellä sekä kanava saksankielisille markkinoille yhdellä kielellä. Tässä skenaariossa jokainen online-kanava konfiguroitaan alueen tietylle yritykselle, ja sillä voi olla sama tuotejoukko kuin muillakin kanavilla on, näiden tuotteiden osajoukko tai eri tuotejoukko. Kullakin kanavalla on myös omat hinnat alueen valuutassa, verot, alennukset ja lähetystilat.

Tässä skenaariossa kukin markkina-alue voidaan konfiguroida omalla toimialuenimellään. `www.adventure-works.com`-toimialue voidaan konfiguroida esimerkiksi Yhdysvaltojen markkinoille, ja `www.adventure-works.de`-toimialueen voi konfiguroida Saksan markkinoille. Vaihtoehtoisesti jokainen markkina-alue voidaan konfiguroida käyttämään eri polkua. `www.adventure-works.com`-toimialue voidaan konfiguroida esimerkiksi Yhdysvaltojen markkinoille, ja sitten `www.adventure-works.com/de`-polkua voidaan käyttää Saksan markkinoille. [Maantieteellisen sijainnin tunnistus](geo-detection-redirection.md) on myös mahdollista määrittää, jotta käyttäjät voidaan ohjata automaattisesti oikeaan sivustoon alueensa perusteella.

Voit myös määrittää, että sivustosi tarjoaa avattavan luettelon, jonka avulla käyttäjät voivat vaihtaa tietylle markkina-alueelle manuaalisesti. Lisätietoja on tämän artikkelin kohdassa [Sivuston valitsinmoduulin lisääminen ja määritys](#add-and-configure-the-site-picker-module).

Lisätietoja useiden kanavien määrittämisestä yhdessä sivustossa on kohdassa [Sähköisen kaupankäynnin sivuston useiden kanavien määritys](#configure-multiple-channels-on-an-e-commerce-site).

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-different-site-experience-per-channel"></a>Useita kanavia (yksikielinen ja/tai monikielinen), joissa on eri sivustokokemus kanavaa kohden

Haluat ehkä luoda useita kanavia yhdelle brändille eri alueilla, ja saatat haluta, että jokaisella alueella on erilainen sivustokokemus. Tämän skenaarion voi toteuttaa kahdella tavalla:

- Käytä [sivustomuuttujia](#implement-page-variants-for-each-language).
- Määritä jokaiselle online-kanavalle oma sivustosi sivuston muodostimessa ja liitä kukin sivusto sitten eri online-kanavaan ja kieleen. Tämä menetelmä edellyttää lisähallintaresursseja, koska sivuston muodostimessa on hallittavana useita sivustoita.

## <a name="cross-channel-sharing"></a>Kanavienvälinen jakaminen

Kanavienvälinen jakaminen on hyödyllistä silloin, kun useat kanavat voivat jakaa sisältöä samassa sivustossa. Esimerkiksi vähittäismyyjä, jolla on useita yhteen sivustoon ryhmiteltyjä brändejä ja myymälöitä, voi jakaa osan sisällöstä joidenkin tai kaikkien myymälöiden kanssa. Jaettu sisältö voi sisältää käyttöehtojen, maksuehtojen, toimitustapojen ja usein kysyttyjen kysymysten sivuja. Lisätietoja on kohdassa [Kanavien välisen jakamisen ottaminen käyttöön ja käyttäminen](cross-channel-sharing.md).

## <a name="map-a-channel-to-a-site-in-site-builder"></a>Kanavan liittäminen sivustoon sivuston muodostimessa

Sivustoja voi luoda ja konfiguroida käyttämään eri online-kanavia monella eri tavalla.

### <a name="create-a-new-site"></a>Luo uusi sivusto

Voit luoda eri sivuston muodostimelle uuden sivuston valitsemalla **Sivustot**-luettelosivun ja valitsemalla **Uusi sivusto**. Tämän jälkeen voit valita näyttöön tulevassa **Uusi sivusto** -valintaikkunassa sivuston oletuskanavan ja kielen seuraavan esimerkin mukaisesti.

![Uuden kanavan luominen sivuston muodostimessa.](media/channel-mapping-4.png)

Tällä tavalla luotava sivusto on tyhjä, eikä se sisällä sivuja (esimerkiksi aloitussivua, luokkasivuja ja tuotesivuja).

Katso lisätietoja kohdasta [Luo sähköisen kaupankäynnin sivusto](create-ecommerce-site.md).

### <a name="create-a-new-site-by-using-the-site-copy-operation"></a>Uuden sivuston luominen sivuston kopiointitoiminnon avulla

Sen sijaan, että luot aivan uuden tyhjän sivuston edellisessä osiossa kuvatulla tavalla, parempi käytäntö on aloittaa kopiosta yhdestä Commerce-moduulikirjastossa olevista aloitussivustoista, kuten Fabrikam- tai Adventure Works -sivustosta.

Jos haluat kopioida aiemmin luodun sivuston, siirry sivuston muodostimen **Sivustot**-luettelosivulle ja valitse **Kopioi sivusto**. Tämän jälkeen voit valita lähdetoimipaikan ja määrittää kohdetoimipaikan nimen näyttöön tulevassa **Kopioi sivusto** -valintaikkunassa.

Tässä vaiheessa sivuston oletusarvoista online-kanavaa ja kieltä ei voi vielä valita. Nämä ominaisuudet voi kuitenkin määrittää sen jälkeen, kun sivuston kopiointitoiminto on valmis. Kun valitset sivuston ensin sivuston muodostimen **Sivustot**-luettelosivulla, näyttöön tulee **Määritä sivusto** -valintaikkuna, jossa voit valita oletuskanavan ja -kielen.

Lisätietoja sivuston kopiointitoiminnosta on kohdassa [Sähköisen kaupankäynnin sivuston kopioiminen](copy-ecommerce-site.md).

### <a name="manage-an-existing-site-channel"></a>Aiemmin luodun sivustokanavan hallinta

Kun sivusto on konfiguroitu kanavan avulla, voit hallita ja päivittää kanavaa sivuston muodostimessa valitun sivuston kautta kohdassa **Sivuston asetukset \> Kanavat**, kuten seuraavassa esimerkissä näkyy.

![Kanavan kartoituksen hallinta sivuston muodostimessa.](media/channel-mapping-7.png)

## <a name="support-multiple-sites-in-a-single-tenant"></a>Usean sivustojen tuki yhdessä vuokraajassa

Useita brändisivustoja voi olla yhdessä vuokraajassa. Seuraavassa esimerkissä havainnollistetaan kolme erilaista brändisivustoa (Adventure Works, Adventure Works Business ja Fabrikam), joista jokainen on yhdistetty eri yksittäiseen verkkokanavaan.

![Sivuston muodostimen sivustoluettelo.](media/channel-mapping-8.png)

## <a name="configure-a-single-domain-name-with-paths-for-multiple-sites"></a>Yhden toimialueen nimen konfiguroiminen poluilla useille sivustoille

Yhtä toimialueen nimeä voidaan käyttää useissa sivustoissa, ja polkuja voidaan käyttää sivustojen tai kielten erottamiseen. `www.mycompany.com`-toimialue on määritetty esimerkiksi kahdelle eri sähköisen kaupankäynnin sivuston toimialueelle: yksi Fabrikamille ja toinen Adventure Worksille. Tällöin Fabrikamin sivustolle voidaan käyttää oletuspolkua (`www.mycompany.com`) eli tyhjää polkua, ja Adventure Works -sivustossa voidaan käyttää toista polkua (esimerkiksi `www.mycompany.com/adventureworks`). Toinen vaihtoehto on käyttää mukautettua polkua (esimerkiksi `www.mycompany.com/fabrikam`) Fabrikamin sivuston oletuspolun asemesta.

Voit myös käyttää kussakin sivustossa eri toimialuenimiä (esimerkiksi `www.adventure-works.com` ja `www.fabrikam.com`). Polkuja voidaan sitten käyttää eri kielillä ja alueilla (esimerkiksi `www.adventure-works.com/fr-ca` Kanadan ranskalle).

## <a name="configure-multiple-languages-on-a-site"></a>Usean kielen konfiguroiminen sivustossa

Kieliä voi määrittää sähköisen kaupankäynnin sivustolle sivuston muodostimessa kohdassa **Sivuston asetukset \> Kanavat**. Seuraavassa esimerkissä kukin kieli on määritetty käyttämällä polun aluekohtaisia asetuksia, joten jokaisella kielellä on yksilöllinen URL-osoite.

![Usean kielen konfiguroiminen sivustossa.](media/channel-mapping-10.png)

Jos haluat lisätä uuden kanavan kielen, valitse **Sivuston asetukset \> Kanavat** ja valitse kanavan linkki. Valitse lisättävä kanava ja aluekohtaiset asetukset valitsemalla **Lisää aluekohtaiset asetukset** oikeanpuoleisesta ruudusta. Määritä sitten valitun kanavan polku.

### <a name="add-and-configure-the-site-picker-module"></a>Sivuston valitsinmoduulin lisääminen ja konfiguroiminen

Kun olet konfiguroinut sivuston, jossa on useita kieliä ja tai kanavia, haluat ehkä lisätä kielenvalitsimen sivuston ylätunnisteeseen, jotta käyttäjät voivat valita kielensä tai maansa manuaalisesti. Moduulikirjaston [otsikkomoduulissa](author-header-module.md) on sisäinen tuki, jonka avulla käyttäjät voivat valita kielen [sivuston valitsinmoduulin](site-selector.md) avulla. Sivuston valitsinmoduuli voidaan lisätä otsikkomoduuliin otsikko-osassa.

Lisätietoja sivuston valitsinmoduulin lisäämisestä ja määrityksestä on kohdassa [Sivuston valitsinmoduuli](site-selector.md).

### <a name="implement-page-variants-for-each-language"></a>Ota sivun muuttujat käyttöön kullekin kielelle

Tässä skenaariossa on vain yksi kanava, mutta kieliä on useita. Voit muuttaa valitun kielen perusteella sivun ulkoasua luomalla sivulle muuttujan. Sen jälkeen voit lisätä lokalisoitua sisältöä muuttujaan.

Kun olet avannut sivun sivuston muodostimessa ja valitset oikeassa yläkulmassa olevan linkin, jossa näkyy nykyinen kanava ja kieli, kanavan ja kielen valitsin tulee näkyviin seuraavan esimerkin mukaisesti. Jos haluat ohittaa nykyisen kielen sivun, valitse toinen alue ja valitse sitten **Muuta**. Voit vaihtaa kanavaa myös, jos [hallitset sivustoa, jossa on useita kanavia ja kieliä](#manage-site-content-that has-multiple-channels-and-languages).

![Sivun kielen vaihtaminen sivuston muodostimessa.](media/channel-mapping-14.png)

Jos valitun sivun tai osan muuttujaa ei ole vielä luotu, näyttöön tulee varoitussanoma seuraavan esimerkin mukaisesti. Valitse tässä tapauksessa **Luo sivun variantti** -linkki sanoman tekstistä. Näyttöön tulevassa valintaikkunassa on vaihtoehtoja, joiden avulla voit aloittaa kopiolla aiemmin luodusta muuttujasta tai luoda mallista uuden sivun.

![Kehote luoda sivumuuttuja sivuston muodostimessa](media/channel-mapping-16.png)

Jos et luo muuttujaa, alkuperäinen sivu muodostetaan ja siinä näkyy asianmukainen kieli moduulin merkkijonoja ja tuotetietoja varten Commerce headquartersista. Jos sivun otsikko tai muu markkinointisisältö on kuitenkin määritetty suoraan oletussivumoduuleissa, tekstin merkkijonot säilyvät alkuperäisellä kielellä.

Sen sijaan, että loisit kunkin sivun ja osan manuaalisesti, voit viedä kunkin sivun ja osan XML Localization Interchange File Format (XLIFF) -tiedostoon, joka voidaan sitten lähettää lokalisointia varten. Kun kukin XLIFF on lokalisoitu, sen voi tuoda lokalisoituna sivumuuttujana. Jos haluat viedä XLIFF-tiedoston sivulta tai osasta sivuston muodostimessa tai tuoda XLIFF-tiedoston sivulle tai osaan, valitse **Lokalisointi** komentopalkista. Valitse sitten joko **Vie XLIFF** tai **Tuo XLIFF** seuraavan esimerkin mukaisesti.

![Tuo tai vie sivu tai osa XLIFF-muodossa.](media/channel-mapping-18.png)

## <a name="manage-site-content-that-has-multiple-channels-and-languages"></a>Hallitse sisältöä sivustossa, jossa on useita kanavia ja kieliä

Sivusto, jossa on useita kanavia ja/tai kieliä, tallentaa kunkin sivun ja osan yksilöllisen variantin kullekin kanavan ja kielen yhdistelmälle. Näin sivumuuttujat voivat sisältää lokalisoituja tietoja, mutta voit myös joustavasti muuttaa tietyn variantin sivun ulkoasua.

Lisätietoja sivumuuttujien käyttämisestä on tämän artikkelin [Ota sivun muuttujat käyttöön kullekin kielelle](#implement-page-variants-for-each-language) -osassa.

## <a name="configure-multiple-channels-on-an-e-commerce-site"></a>Sähköisen kaupankäynnin sivuston useiden kanavien määritys

Voit lisätä kanavia sivuston muodostimessa sähköisen kaupankäynnin sivustoon valitsemalla **Sivuston asetukset \> Kanavat** ja valitsemalla **Lisää kanava**. Sitten näkyviin tulevasta **Lisää kanava** -valintaikkunasta voit valita online-kanavan ja oletusarvoiset aluekohtaiset asetukset.

## <a name="additional-resources"></a>Lisäresurssit

[Kanavien yleiskatsaus](channels-overview.md)

[Online-kanavan määrittäminen](channel-setup-online.md)

[Organisaatiot ja organisaatiohierarkiat – yleiskatsaus](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md)

[Maantieteellisen sijainnin tunnistuksen ja uudelleenohjauksen määritys](geo-detection-redirection.md)

[Kanavienvälisen jakamisen käyttöönottaminen ja käyttäminen](cross-channel-sharing.md)

[Sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md)

[Sähköisen kaupankäynnin sivuston kopioiminen](copy-ecommerce-site.md)

[Sivuston valitsinmoduuli](site-selector.md)
