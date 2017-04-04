---
title: "Tuotteiden ja tuotevarianttien haku tilaustenkäsittelyn aikana"
description: "Käytä <strong>Nimiketunnus </strong>kenttää tuote- ja tuotevarianttihakuun luodessasi manuaalisesti ostotilausrivin tai myyntitilausrivin.  Näin löydät nopeasti tuotevariantit, kun käytettävissä on vain konfiguraation merkkijono tai jokin tuotedimensioista."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: MCRFullTextIndexField, MCRFullTextParameters, PurchTable, SalesTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 248534
ms.assetid: 99dd5ce1-0029-4f06-90e7-865e6d46d86e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 5b0f3c1a853f8f5e61dedaf588b6f9d2da3a53b5
ms.lasthandoff: 03/31/2017


---

# <a name="search-for-products-and-product-variants-during-order-entry"></a>Tuotteiden ja tuotevarianttien haku tilaustenkäsittelyn aikana

Käytä <strong>Nimiketunnus </strong>kenttää tuote- ja tuotevarianttihakuun luodessasi manuaalisesti ostotilausrivin tai myyntitilausrivin.  Näin löydät nopeasti tuotevariantit, kun käytettävissä on vain konfiguraation merkkijono tai jokin tuotedimensioista.

Joskus ottaa liian paljon jotain ei ole paras tilanne on, ja varsinkin jos myyt määrän tuotteita, jotka ovat samanlaisia kuin yrität muistaa nimikenumerot tai Etsi tuotenimet myyntitilauksen laittaa oikean tuotteen löytämiseksi. Voit käyttää **Tavaraerän numero** kenttää myyntitilausrivin tai ostotilausrivin haku-kentän. Voit syöttää osan tuotenimeä, numeroa tai dimensiota, jolloin hakutoiminto tuo näyttöön kaikki nimikkeet, jotka vastaavat hakusanaa.

## <a name="how-search-works"></a>Haun toiminta
Kun etsit tuotteita tai tuotevariantteja, on tärkeää tietää, miten hakutoiminto löytää tuotteet, jotka vastaavat kirjoittamaasi tekstiä. Keskeiset hakusäännöt ovat seuraavat:

-   Hakutulokset palauttavat kaikki vastaavat tietueet riippumatta hakukentästä, johon hakuteksti kirjoitettiin.
-   Koko hakuteksti täytyy olla sopivassa tietueessa.
-   Haku löytää hakuehtojen perusteella vastaavuudet, vaikka hakuteksti olisi merkkijonon keskellä tietueessa. Sen ei tarvitse olla merkkijonon alussa.
-   Hakutekstiä käsitellään yhtenä merkkijonona, vaikka se sisältää välilyöntejä.

### <a name="examples"></a>Esimerkkejä

Seuraavissa esimerkeissä käytetään tuotteita ja tuotevariantteja havainnollistamaan, kuinka haku toteutetaan eri skenaarioissa. **Edellytys:** kohdassa **myynnin ja markkinoinnin &gt;asennus &gt;Etsi &gt;etsinnän oletusparametrit**&gt;**haun tyyppi**, valitse **täydellinen vastaavuus** vaihtoehto.

| Tuotetyyppi     | Tuotteen nimi    | Näytä tuotenumero | Nimiketunnus | Konfiguraatio |
|------------------|-----------------|------------------------|-------------|---------------|
| Erillinen tuote | KaiutinMidRange | D0001                  | D0001       | Ei saatavana            |
| Tuotevariantti  | Aktiivinen kaiutin  | D0010:::Musta:         | D0010       | 000005        |
| Tuotevariantti  | Aktiivinen kaiutin  | D0010:::Valkoinen:         | D0010       | Valkoinen         |

Jos kirjoitat "kaiu" **Nimiketunnus**-kenttään, saat hakutuloksena kaikki edellä mainitut tuotteet. Jos kirjoitat "musta" **Nimiketunnus**-kenttään, hakutulokseksi tulee toinen tuote, koska sillä on teksti "musta" Näytä tuotenumero -kohdassa. Nämä kaksi esimerkkiä osoittavat, että haku ei koske vain kentän alkua, vaan vastine löytyy, vaikka hakuteksti löytyy merkkijonon keskeltä vastaavasta tietueesta.  

Jos kirjoitat "05", hakutulokseksi saadaan vain toinen tuotevariantti koska sillä on "05" Konfiguraatio-kohdassa. Se osoittaa, että haku koskee kaikkia valittuja kenttiä **Hakuehdot**-sivulla.  

Jos kirjoitat "kaiu 05", haku ei löydä yhtään tulosta. Tämä johtuu siitä. että hakutoiminto etsii koko tekstiä. Hakutoiminto yrittää löytää "kaiu" -vastaavuudet ja rajoittaa tulokset niihin, jotka sisältävät merkkijonon "05".  

Voit rajoittaa hakutulosten lukumäärä **tulosten määrä** kenttä **myynnin ja markkinoinnin &gt;asennus &gt;Etsi &gt;etsinnän oletusparametrit** sivun. Jos tämän kentän arvoksi määritetään 0, kaikki hakutulokset palautetaan. Jos esimerkiksi määrität arvoksi 10, toiminto palauttaa enintään 10 hakutulosta.

## <a name="configure-the-product-search"></a>Tuotehaun määrittäminen
Ennen kuin voit käyttää tuote- ja tuotevarianttihakua, määritä tuotehakutoiminto seuraavasti. [![3 vaiheet, voit määrittää tuotehaku\_AXAppFall](./media/3-steps-to-configure-product-search_axappfall.png)](./media/3-steps-to-configure-product-search_axappfall.png)

### <a name="step-1-include-all-the-relevant-product-and-product-variant-identifiers-and-dimensions-in-the-search-criteria"></a>Vaihe 1: Sisällytä kaikki tarvittavat tuotteen ja tuotevariantin tunnukset ja dimensiot hakuehtoihin

Esimerkkejä tuotteen ja tuotevariantin tunnuksista ja dimensioista, joiden perusteella tuotetta voidaan hakea, ovat: **tuotenimi, nimiketunnus**, **Näytä tuotenumero, väri, koko, malli, hakunimi jne.**.  

Siirry **myynnin ja markkinoinnin &gt;asennus &gt;Etsi &gt;hakuehdot** sivulla. **Hakuehdot**-sivulla voit määrittää asiakkaan, prospektin ja tuotehaun ehdot. Varmista, että käytät tuotehakuehtoja sivun suodatuksessa. Voit tehdä tämän siirtymällä kohtaan **Tuote** sivun valikossa.  

Näyttää tuotteen numeron lisääminen hakuehdot, valitse **uusi** sivun valikosta. Tämä lisää uuden tietueen **hakuehdot** ruudukko. Avaa **Kentän nimi** -sarakkeen haku ja valitse **DisplayProductNumber**. Lisää hakuehtoja tuotteen kokoonpano, Luo uusi tietue ** hakuehdot ** ruudukko ja valita **configId** - **kenttänimi** sarakkeen. Luo samalla tavalla tietue **Kentän nimi** **InventColorId** väri-dimensiolle, **InventSizeId** koko-dimensiolle ja **InventStyleId** malli-dimensiolle.

### <a name="step-2-populate-the-database-table-that-is-used-for-product-search"></a>Vaihe 2: Täytä tietokantataulu, jota käytetään tuotehaussa

Valitse **Hakuehdot** -sivulla **Päivitä hakutiedot** -painike. Varmista **Päivitä hakutiedot** -valintaikkunassa, että **Lähde** arvoksi on määritettu **Tuote** ja valitse sitten **OK**. Järjestelmä keräämään kaikki hakuehdot täyttäviä vaiheessa 1 määritetty samassa taulukossa. Jos sinulla on paljon Tuoteluettelo ja tuotevariantit, tämä toiminto voi olla melko pitkä ja näyttöön saattaa tulla varoitus. On suositeltavaa, että ajoitat hakutaulun täytön eräpalvelimessa aikaan, jolloin palvelin ei ole varattu.  

Tuotehaku ei tuota oikeita tuloksia ennen kuin taulukko täytetään. Jos haku ei tuota tuloksia, varmista, että taulukko on täytetty.  

Taulukossa on täytettävä vain kun hakuehdot muutetaan. Äskettäin julkaistut tuotteet ja tuotevariantit lisätään automaattisesti taulukkoon. Poistetut tuotteet ja tuotevariantit poistetaan automaattisesti taulukosta.

### <a name="step-3-enable-the-lookup-for-product-search-on-sales-and-purchase-order-lines"></a>Vaihe 3: Ota tuotehaku käyttöön myynti- ja ostotilausriveillä

Ottaa tämän toiminnon käyttöön siirtymällä **myynnin ja markkinoinnin &gt;asennus &gt;Etsi &gt;etsinnän oletusparametrit** ja **Ota haku haku**, **Kyllä** - **yleisen** välilehti.  

Myyntitilausrivin syötön oletusasetuksena on avata **Tuotehaku** -sivu, kun alat kirjoittaa **Nimiketunnus** kenttään ja painat **Välilehti**-näppäintä. **Tuotehaku**-sivu vaihtaa kontekstia tilausrivin luonnin yhteydessä ja voi vaikuttaa tarpeettoman rajoittavalta. Jos haluat saada hakutulokset hakukentän avulla etkä halua vaihtaa kontekstia tilausrivin luonnin yhteydessä, voit käyttää sen sijaan varsinaista hakutoimintoa. Jos haet tuotetta tai tuotevarianttia valitsematta mitään hakukentässä ja painat **Välilehti**-näppäintä, **Tuotehaku**-sivu tulee näyttöön.


