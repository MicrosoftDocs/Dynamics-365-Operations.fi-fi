---
title: Tuotteiden ja tuotevarianttien haku tilaustenkäsittelyn aikana
description: Käytä **Nimiketunnus** kenttää tuote- ja tuotevarianttihakuun luodessasi manuaalisesti ostotilausrivin tai myyntitilausrivin. Näin löydät nopeasti tuotevariantit, kun käytettävissä on vain konfiguraation merkkijono tai jokin tuotedimensioista.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRFullTextIndexField, MCRFullTextParameters, PurchTable, PurchTablePart, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 248534
ms.assetid: 99dd5ce1-0029-4f06-90e7-865e6d46d86e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6ff95b9e16d1a56dee13f67d0a3355f09cfc60b9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987176"
---
# <a name="search-for-products-and-product-variants-during-order-entry"></a>Tuotteiden ja tuotevarianttien haku tilaustenkäsittelyn aikana

[!include [banner](../includes/banner.md)]

Käytä **Nimiketunnus** kenttää tuote- ja tuotevarianttihakuun luodessasi manuaalisesti ostotilausrivin tai myyntitilausrivin.  Näin löydät nopeasti tuotevariantit, kun käytettävissä on vain konfiguraation merkkijono tai jokin tuotedimensioista.

Joskus liian suuri määrä jotain tuotetta saattaa aiheuttaa päänvaivaa, varsinkin jos myyt suuren määrän samankaltaisia tuotteita ja yrität muistaa niiden nimiketunnukset tai tuotteen hakunimet, kun yrität löytää oikean tuotteen lisätäksesi sen myyntitilaukseen. Voit käyttää ostotilausrivin tai myyntitilausrivin **Nimiketunnus**-kenttää hakukenttänä. Voit antaa osan tuotenimeä, numeroa tai dimensiota, jolloin hakutoiminto tuo näyttöön kaikki nimikkeet, jotka vastaavat hakusanaa.

## <a name="how-search-works"></a>Haun toiminta
Kun haet tuotteita tai tuotevariantteja, on tärkeää tietää, miten hakutoiminto löytää tuotteet, jotka vastaavat kirjoittamaasi tekstiä. Keskeiset hakusäännöt ovat seuraavat:

-   Hakutulokset palauttavat kaikki vastaavat tietueet riippumatta hakukentästä, johon hakuteksti kirjoitettiin.
-   Koko hakuteksti täytyy olla sopivassa tietueessa.
-   Haku löytää hakuehtojen perusteella vastaavuudet, vaikka hakuteksti olisi merkkijonon keskellä tietueessa. Sen ei tarvitse olla merkkijonon alussa.
-   Hakutekstiä käsitellään yhtenä merkkijonona, vaikka se sisältää välilyöntejä.

### <a name="examples"></a>Esimerkkejä

Seuraavissa esimerkeissä käytetään tuotteita ja tuotevariantteja havainnollistamaan, kuinka haku toteutetaan eri skenaarioissa. **Edellytys:** Valitse ensin **Myynti ja markkinointi &gt; Asetukset &gt; Haku &gt; Hakuparametrit &gt; Hakutyyppi** ja sitten **Täydellinen vastaavuus** -vaihtoehto.

| Tuotetyyppi     | Tuotteen nimi    | Näytä tuotenumero | Nimiketunnus | Konfiguraatio |
|------------------|-----------------|------------------------|-------------|---------------|
| Erillinen tuote | KaiutinMidRange | D0001                  | D0001       | Ei sovellu            |
| Tuotevariantti  | Aktiivinen kaiutin  | D0010:::Musta:         | D0010       | 000005        |
| Tuotevariantti  | Aktiivinen kaiutin  | D0010:::Valkoinen:         | D0010       | Valkoinen         |

Jos kirjoitat "kaiu" **Nimiketunnus**-kenttään, saat hakutuloksena kaikki edellä mainitut tuotteet. Jos kirjoitat "musta" **Nimiketunnus**-kenttään, hakutulokseksi tulee toinen tuote, koska sillä on teksti "musta" Näytä tuotenumero -kohdassa. Nämä kaksi esimerkkiä osoittavat, että haku ei koske vain kentän alkua, vaan vastine löytyy, vaikka hakuteksti löytyy merkkijonon keskeltä vastaavasta tietueesta.  

Jos kirjoitat "05", hakutulokseksi saadaan vain toinen tuotevariantti koska sillä on "05" Konfiguraatio-kohdassa. Se osoittaa, että haku koskee kaikkia valittuja kenttiä **Hakuehdot**-sivulla.  

Jos kirjoitat "kaiu 05", haku ei löydä yhtään tulosta. Tämä johtuu siitä, että hakutoiminto etsii koko tekstiä. Hakutoiminto yrittää löytää "kaiu" -vastaavuudet ja rajoittaa tulokset niihin, jotka sisältävät merkkijonon "05".  

Voit rajoittaa hakutulosten lukumäärää käyttämällä **Tulosten määrä**-kenttää **Myynti ja markkinointi &gt; Asetukset &gt; Haku &gt; Hakuparametrit** -sivulla. Jos tämän kentän arvoksi määritetään 0, kaikki hakutulokset palautetaan. Jos esimerkiksi määrität arvoksi 10, toiminto palauttaa enintään 10 hakutulosta.

## <a name="configure-the-product-search"></a>Tuotehaun määrittäminen
Ennen kuin voit käyttää tuote- ja tuotevarianttihakua, määritä tuotehakutoiminto seuraavasti. [![tuotehaun määrittämisen 3 vaihetta\_AXAppFall](./media/3-steps-to-configure-product-search_axappfall.png)](./media/3-steps-to-configure-product-search_axappfall.png)

### <a name="step-1-include-all-the-relevant-product-and-product-variant-identifiers-and-dimensions-in-the-search-criteria"></a>Vaihe 1: Sisällytä kaikki tarvittavat tuotteen ja tuotevariantin tunnukset ja dimensiot hakuehtoihin

Esimerkkejä tuotteen ja tuotevariantin tunnuksista ja dimensioista, joiden perusteella tuotetta voidaan hakea, ovat: **tuotenimi, nimiketunnus**, **Näytä tuotenumero, väri, koko, malli, hakunimi jne.**.  

Siirry **Myynti ja markkinointi &gt; Asetukset &gt; Haku &gt; Hakuehdot** -sivulle. **Hakuehdot**-sivulla voit määrittää asiakkaan, prospektin ja tuotehaun ehdot. Varmista, että käytät tuotehakuehtoja sivun suodatuksessa. Voit tehdä tämän siirtymällä kohtaan **Tuote** sivun valikossa.  

Voit lisätä näytön tuotenumeron hakuehtoihin napsauttamalla **Uusi** sivun valikosta. Tämä lisää uuden tietueen **Hakuehdot**-ruudukkoon. Avaa **Kentän nimi** -sarakkeen haku ja valitse **DisplayProductNumber**. Lisää tuotteen konfiguraatio hakuehtoihin luomalla uusi tietue **Hakuehdot** -ruudukossa ja valitse **configId** **Kentän nimi** -sarakkeessa. Luo samalla tavalla tietue **Kentän nimi** **InventColorId** väri-dimensiolle, **InventSizeId** koko-dimensiolle ja **InventStyleId** malli-dimensiolle.

### <a name="step-2-populate-the-database-table-that-is-used-for-product-search"></a>Vaihe 2: Täytä tietokantataulu, jota käytetään tuotehaussa

Valitse **Hakuehdot** -sivulla **Päivitä hakutiedot** -painike. Varmista **Päivitä hakutiedot** -valintaikkunassa, että **Lähde** arvoksi on määritetty **Tuote** ja valitse sitten **OK**. Järjestelmä kerää kaikki hakuehdot yhteen taulukkoon vaiheessa 1 määritettyjen hakuehtojen mukaisesti. Jos sinulla on suuri määrä tuotteita ja tuotevariantteja, tämä toiminto voi kestää melko pitkään ja näyttöön voi tulla varoitus. On suositeltavaa, että ajoitat hakutaulun täytön eräpalvelimessa aikaan, jolloin palvelin ei ole varattu.  

Tuotehaku ei tuota oikeita tuloksia ennen kuin taulukko täytetään. Jos haku ei tuota tuloksia, varmista, että taulukko on täytetty.  

Taulukossa on täytettävä vain kun hakuehdot muutetaan. Äskettäin julkaistut tuotteet ja tuotevariantit lisätään automaattisesti taulukkoon. Poistetut tuotteet ja tuotevariantit poistetaan automaattisesti taulukosta.

### <a name="step-3-enable-the-lookup-for-product-search-on-sales-and-purchase-order-lines"></a>Vaihe 3: Ota tuotehaku käyttöön myynti- ja ostotilausriveillä

Voit ottaa tämän toiminnon käyttöön valitsemalla ensin **Myynti ja markkinointi &gt; Asetukset &gt; Haku &gt; Hakuparametrit** ja määrittämällä sitten **Ota tuotteiden haku käyttöön** -arvoksi **Kyllä** **Yleistä**-välilehdessä.  

Myyntitilausrivin syötön oletusasetuksena on avata **Tuotehaku** -sivu, kun alat kirjoittaa **Nimiketunnus** kenttään ja painat **sarkainnäppäintä**. **Tuotehaku**-sivu vaihtaa kontekstia tilausrivin luonnin yhteydessä ja voi vaikuttaa tarpeettoman rajoittavalta. Jos haluat saada hakutulokset hakukentän avulla etkä halua vaihtaa kontekstia tilausrivin luonnin yhteydessä, voit käyttää sen sijaan varsinaista hakutoimintoa. Jos haet tuotetta tai tuotevarianttia valitsematta mitään hakukentässä ja painat **sarkainnäppäintä**, **Tuotehaku**-sivu avautuu.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]