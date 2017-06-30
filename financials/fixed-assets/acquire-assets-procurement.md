---
title: "Käyttöomaisuuden hankinta"
description: "Tässä artikkelissa kuvataan, kuinka tehdään käyttöomaisuuden ja ostoreskontran väliset integrointimääritykset, luodaan käyttöomaisuuserä automaattisesti ostotilauksesta tai laskusta tai kirjataan käyttöomaisuuserien hankinta- ja hankintaoikaisutapahtumat automaattisesti."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetParameters
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3481
ms.assetid: d4e73a3f-633b-48b2-b8db-7a4a59a4d7ec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: aa5598ddd0d397314b42c6ac0c1b0d02eb95ebb4
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="acquire-assets-through-procurement"></a>Käyttöomaisuuden hankinta

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kuvataan, kuinka tehdään käyttöomaisuuden ja ostoreskontran väliset integrointimääritykset, luodaan käyttöomaisuuserä automaattisesti ostotilauksesta tai laskusta tai kirjataan käyttöomaisuuserien hankinta- ja hankintaoikaisutapahtumat automaattisesti.

 Järjestelmä sisältää seuraavat menetelmät, joilla käyttöomaisuuserät ja ostoreskontra voidaan integroida. Samaa menetelmää on käytettävä kaikille käyttöomaisuuserille:
-   Luot käyttöomaisuuserän manuaalisesti, ennen kuin lisäät käyttöomaisuuserän numeron ostotilauksen tai toimittajan laskun riville. Käyttöomaisuuden hankintatapahtuma kirjataan automaattisesti, kun kirjaat toimittajan laskun. Tämä on oletusmenetelmä.
-   Luot käyttöomaisuuserän manuaalisesti, ennen kuin lisäät käyttöomaisuuserän numeron ostotilauksen tai toimittajan laskun riville. Käyttöomaisuuden hankintatapahtumaa ei kirjata, kun kirjaat toimittajan laskun.
-   Järjestelmä luo automaattisesti käyttöomaisuustietueen, kun kirjaat tuotteen vastaanoton tai toimittajan laskun, jonka Luo uusi käyttöomaisuuserä -valintaruutu on valittuna. Käyttöomaisuuden hankintatapahtuma kirjataan automaattisesti, kun kirjaat toimittajan laskun.
-   Järjestelmä luo automaattisesti käyttöomaisuustietueen, kun kirjaat tuotteen vastaanoton tai toimittajan laskun, jonka Luo uusi käyttöomaisuuserä -valintaruutu on valittuna. Käyttöomaisuuden hankintatapahtumaa ei kirjata, kun kirjaat toimittajan laskun.

Valitse ensimmäisestä kahdesta menetelmästä toinen, jos haluat luoda käyttöomaisuuserät manuaalisesti ja määrittää sitten käyttöomaisuuserän numeron ostotilaukseen tai toimittajan laskuun. Valitse kahdesta jälkimmäisestä menetelmästä toinen, jos haluat toimia joustavammin ja toisinaan luoda käyttöomaisuuserät manuaalisesti, toisinaan automaattisesti rivinimikkeiden käyttöomaisuustietojen perusteella. 

Luodaanpa käyttöomaisuuserät manuaalisesti tai joustavampaa tapaa noudattaen, joudut päättämään, voiko hankintatapahtuman kirjata vain käyttöomaisuuteen vai voiko sen kirjata toimittajan laskun kirjaamisen yhteydessä. Joissakin organisaatioissa suositaan sellaista menettelyä, että käyttäjät luovat hankinnan ja hankintatapahtumat manuaalisesti käyttöomaisuuteen manuaalisia kirjauskansiokirjauksia tai ehdotuksia käyttäen. 

Tässä ohjeaiheessa kutakin tapaa käsitellään seikkaperäisesti.

## <a name="methods-for-manually-creating-fixed-assets"></a> Menetelmät käyttöomaisuuserien manuaaliseen luomiseen
Jos Käyttöomaisuuden parametrit -lomakkeen Salli käyttöomaisuuden hankinta ostosta -valintaruutu on valittuna ja kirjaat toimittajan laskun, jonka riveille on lisätty käyttöomaisuuserän numero, hankinta kirjataan automaattisesti ja käyttöomaisuuden tilaksi vaihtuu Avoin. 

Jos hankintaa ei voi kirjata, voit joko lisätä hankintatapahtuman manuaalisesti käyttöomaisuuteen tai luoda useita hankintatapahtumia kerralla käyttämällä hankintaehdotusta Käyttöomaisuuden kirjauskansiossa.

> [!NOTE]                                                                                                                              
> Jos käyttöomaisuudet on määritetty rajaamaan hankintatapahtumien kirjaaminen tietylle käyttäjäryhmälle, hankintatapahtumien kirjaaminen laskuista edellyttää kuulumista kyseiseen käyttäjäryhmään.

## <a name="methods-for-automatically-creating-fixed-assets"></a> Menetelmät käyttöomaisuuserien automaattiseen luomiseen
Kun kirjaat vastaanoton tuotteelle, jonka rivillä on valittuna Luo uusi käyttöomaisuuserä -asetus, luodaan uusi käyttöomaisuuserä, jonka tila on Ei vielä ostettu. Kun toimittajan lasku tämän jälkeen kirjataan uutta käyttöomaisuuserää käyttäen, uudelle käyttöomaisuudelle kirjataan hankintatapahtuma, ja käyttöomaisuuden tila muuttuu Avoin-tilaksi, jos käyttöomaisuudet on määritetty sallimaan käyttöomaisuuden hankinnat ostoreskontrasta, ja kuulut käyttäjäryhmään, jolle hankintatapahtumien kirjaaminen on sallittua. 

Jos Uusi käyttöomaisuuserä? -asetus ei ole valittu ostorivillä, kun kirjaat tuotteen vastaanoton, mutta oli valittuna toimittajan laskun kirjaamisen yhteydessä, uusi käyttöomaisuus luodaan ja hankitaan niin, että sen tila on Avoin, jos käyttöomaisuudet on määritetty sallimaan luonti ja hankinta. Uutta käyttöomaisuuserää ei luoda, kun kirjaat toimittajan laskun, jos erä oli jo luotu kun kirjasit tuotteen vastaanoton.

### <a name="capitalization-threshold"></a>Aktivointiraja

Kun käytät menetelmää, jossa käyttöomaisuus luodaan ja hankitaan automaattisesti, voit määrittää järjestelmän tarkistamaan, saavuttaako käyttöomaisuuserän ostosumma käyttöomaisuuden poistoille määritetyn kapitalisointikynnyksen. Jos saavuttaa, Poisto-asetus valitaan käyttöomaisuuden kirjasta, kun käyttöomaisuus luodaan ostoreskontrasta. 

Aktivointiraja on rahasumma, joka määrittää, poistetaanko summan ylittävät käyttöomaisuuserät. Jos esimerkiksi ostat käyttöomaisuuden, jonka ostohinta on pienempi kuin aktivointiraja, käyttöomaisuutta ei määritetä poistoja varten. Jos ostosumma puolestaan on yhtä suuri tai suurempi kuin määritetty raja, käyttöomaisuus määritetään poistoja varten. 

Voit määrittää aktivointirajan Käyttöomaisuusryhmät-lomakkeessa.

## <a name="scenario"></a>Skenaario
Seuraavassa skenaariossa käsitellään käyttöomaisuuden ja ostoreskontran integroinnin koko sykli. Mukana on esimerkkikokoonpano, ja myös hankintaehdotusten käyttämistä käsitellään. 

Tässä skenaariossa järjestelmä on määritetty seuraavalla tavalla:

-   Käyttöomaisuuserät luodaan automaattisesti tuotteen vastaanoton tai toimittajan laskun kirjaamisen yhteydessä, mutta käyttöomaisuudet on määritetty estämään hankintatapahtumien kirjaaminen ostoreskontrasta.
-   Tilit määritellään Tilin tyyppi -kentässä Nimikeryhmät-sivun Käyttöomaisuuden vastaanotto- ja Käyttöomaisuuden otto -tilityypeille.
-   Tietokoneet-ryhmän (COMP) aktivointiraja on 1 500.
-   Tehtäväsi on lisätä työntekijän käyttöön hankittavan uuden kannettavan tietokoneen ostotilaus, kirjata ostotilaus, varmistaa, että kuljetushenkilö kirjaa tuotteen vastaanoton, kirjata toimittajan lasku sekä varmistaa, että laskentahenkilö päivittää kannettavan tietokoneen käyttöomaisuuserän tilaksi Avoin.

Aloita lisäämällä kannettavan tietokoneen (hinta 1 600) tiedot Ostotilaus-sivulle. Valitse Käyttöomaisuudet-pikavälilehdeltä ostotilausriveille Uusi käyttöomaisuus? -valintaruutu, käyttöomaisuusryhmäksi COMP ja tallenna ostotilaus. 

Kun kannettava tietokone saapuu, kuljetushenkilö kirjaa kannettavan tietokoneen vastaanotetuksi lisäämällä ja kirjaamalla tuotteen vastaanoton. Kannettavan tietokoneen käyttöomaisuus luodaan ja sen tilaksi asetetaan Ei vielä ostettu. Summa ylittää aktivointirajan. Poisto-asetus valitaan siis kannettavan tietokoneen kirjoille. Seuraavat tapahtumat tapahtuivat.

| Kuvaus                               | Tili             | Debet    | Luotto   |
|-------------------------------------------|---------------------|----------|----------|
| Osto, tuotteen vastaanotto-osto        | Laskuttamattomat vastaanotot | 1 600,00 |          |
| Osto, tuotteen vastaanotto-oston vastatili | Jaksotetut ostot   |          | 1 600,00 |

Seuraavaksi kirjataan toimittajan lasku kannettavasta tietokoneesta. Kannettavan tietokoneen tila ei muutu, koska käyttöomaisuudet on määritetty estämään käyttöomaisuuden hankintatapahtuman kirjaaminen toimittajan laskun kirjaamisen yhteydessä. Luo uusi käyttöomaisuuserä -vaihtoehto oli valittuna toimittajan laskun kirjaamisen yhteydessä. Käytetty tili on siis Käyttöomaisuuden vastaanotto. Käyttöomaisuuden otto -tiliä ei käytetty, koska hankintaa ei ole kirjattu; tiliä käytetään myöhemmin, kun organisaation laskentahenkilö kirjaa hankintatapahtuman käyttöomaisuuteen hankintaehdotuksia käyttäen. 

Seuraavat tapahtumat tapahtuivat.

| Kuvaus                               | Tili             | Debet    | Luotto   |
|-------------------------------------------|---------------------|----------|----------|
| Osto, tuotteen vastaanotto-oston vastatili | Jaksotetut ostot   | 1 600,00 |          |
| Toimittajan saldo                            | Ostoreskontra    |          | 1 600,00 |
| Ostot, käyttöomaisuuden vastaanotto             | Tietokoneen kulut    | 1 600,00 |          |
| Osto, tuotteen vastaanotto-osto        | Laskuttamattomat vastaanotot |          | 1 600,00 |

Lopuksi kirjanpitäjä tarkistaa kaikki käyttöomaisuudet, joiden tila on Ei vielä ostettu. Uusi kannettavan tietokoneen käyttöomaisuus siis tarkistetaan. Kirjanpitäjä avaa sitten Hankintaehdotus-sivun Käyttöomaisuuden kirjauskansioriveiltä ja luo hankintatapahtumat kaikille käyttöomaisuuserille, joille on kirjattu lasku, mutta joiden tila on edelleen Ei vielä ostettu. Kun kirjauskansio kirjataan, kannettavan tietokoneen käyttöomaisuuserän tilaksi muutetaan Avoin. Käyttöomaisuuden osto -tiliä hyvitetään ja omaisuuden hankintatiliä veloitetaan. 

Seuraavassa luettelossa on tämän skenaarion muunnelmia:

-   Jos käyttöomaisuudet on määritetty sallimaan käyttöomaisuuden hankintatapahtumien kirjaaminen toimittajan laskujen kirjaamisen yhteydessä, laskentahenkilön ei tarvitse käyttää hankintaehdotuksia käyttöomaisuudessa, koska järjestelmä luo hankintatapahtuman. Toimittajan laskun kirjaamisen yhteydessä päivitetään niin ikään eri tilejä. Tietokonekulun sijaan käyttöomaisuuden vastaanoton varastotiliä veloitetaan, jonka lisäksi luodaan kaksi lisätapahtumaa: käyttöomaisuuden hankintatiliä veloitetaan ja käyttöomaisuuden oton varastotiliä hyvitetään.
-   Jos Luo uusi käyttöomaisuuserä -asetus ei ole valittuna, kun tuotteen vastaanotto kirjataan, kyseisellä hetkellä ei luoda uutta erää. Jos valitset Luo uusi käyttöomaisuuserä -valintaruudun ennen toimittajan laskun kirjaamista, käyttöomaisuus luodaan ja sen tilaksi määritetään Ei vielä ostettu. Jos toimittajan laskujen kirjaamisen yhteydessä kirjataan myös hankintatapahtumat, tila on Avoin.
-   Jos kannettavan tietokoneen kustannus on 1 400 eikä 1 600, aktivointiraja ei ylity. Käyttöomaisuus luodaan, ja Poisto-asetus poistetaan.
-   Jos laskurekisteriä käytetään, nouda tosite käyttämällä laskurekisterin kirjaamisen jälkeen Laskun hyväksyntä -kirjauskansiosivua, linkitä ostotilaus toimittajan laskuun, valitse Luo uusi käyttöomaisuuserä -asetus ja kirjaa toimittajan lasku. Jos kuulut käyttäjäryhmään, jolle hankintatapahtumien luominen on sallittua, hankinta luodaan ja käyttöomaisuuden tilaksi määritetään Avoin.
-   Jos vain osa määrästä vastaanotetaan, ensimmäiselle toimittajan laskulle ei muodosteta käyttöomaisuuden hankintaa käyttäjäryhmän rajoitusten vuoksi. Hankinnan kirjaaminen tilatun määrän täydentävälle toiselle toimittajan laskulle edellyttää, että hankintatapahtuma on lisätty aiemmin ensimmäiselle laskulle ja että kuulut käyttäjäryhmään, jolle hankintojen kirjaaminen on sallittua.


Lisätietoja on ohjeaiheessa [Käyttöomaisuuden integrointi](fixed-asset-integration.md).




