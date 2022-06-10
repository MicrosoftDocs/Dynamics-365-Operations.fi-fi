---
title: Usein kysytyt kysymykset B2B-sivustojen Commerce-luetteloista
description: Tämä ohjeaihe sisältää vastauksia usein kysyttyihin Microsoft Dynamics 365 Commerce -luetteloiden kysymyksiin.
author: ashishmsft
ms.date: 05/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 5bdc7dfcb0e48aa85db2db4d178c5bf62ea0411b
ms.sourcegitcommit: bca0cb730307948368a9aabe322cf963688ed8b1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/19/2022
ms.locfileid: "8782859"
---
# <a name="commerce-catalogs-for-b2b-faq"></a>Usein kysytyt kysymykset B2B-sivustojen Commerce-luetteloista

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tämä ohjeaihe sisältää vastauksia usein kysyttyihin Microsoft Dynamics 365 Commerce -[B2B-luetteloiden](catalogs-b2b-sites.md) kysymyksiin.

## <a name="why-cant-i-configure-a-catalog-specific-navigation-hierarchy-or-see-an-option-to-associate-a-customer-hierarchy"></a>Miksi luettelokohtaista siirtymishierarkiaa ei voi konfiguroida tai ei voi nähdä asiakashierarkian liittämisvaihtoehtoa?

Varmista, että **Ota käyttöön usean luettelon käyttö vähittäismyyntikanavissa** -toiminto on otettu käyttöön Commerce Headquartersin **ominaisuuksien hallinnan** työtilassa. Varmista myös, että ympäristösi käytössä on Commerce versiota 10.0.27 tai sitä myöhempää versiota.

## <a name="can-i-view-the-catalog-specific-hierarchy-and-enrich-category-pages-in-commerce-site-builder"></a>Voinko tarkastella luettelokohtaisia hierarkiaa ja rikastaa luokkasivuja Commercen sivustonmuodostimessa?

Kyllä, Commercen sivustonmuodostimen käyttäjät, joilla on sivustonmuodostimessa **Tuotteet**-sivun käyttöoikeudet, voivat valita luettelon ja tarkastella luettelokohtaista hierarkiaa. **Tuotteet**-sivulla käyttäjät voivat myös rikastaa luettelon tietyn luokan luokkasivua. Lisätietoja on kohdassa [Luokan saapumissivun täydentäminen](enrich-category-page.md). Jos haluat käyttää luettelokohtaista rikastusta, on suositeltavaa, että kyseisessä luettelossa on erillinen ja yksilöllinen siirtymishierarkia.

## <a name="can-a-b2b-shopper-purchase-from-multiple-catalogs-in-a-single-checkout"></a>Voiko B2B-ostajaa ostaa useista luetteloista yhdessä kassatapahtumassa?

Kyllä, ostot useista luetteloista yhdessä kassatapahtumassa ovat sallittuja. B2B-ostajat voivat käyttää ostoskärrynäkymän luetteloilmaisinta määrittämään, mitkä nimikkeet on lisätty mistäkin luetteloista.

## <a name="if-a-b2b-shopper-purchases-the-same-item-from-different-catalogs-what-is-the-expected-behavior"></a>Jos B2B-ostaja ostaa saman nimikkeen eri luetteloista, mikä on odotettu toimintatapa?

Vaikka käyttäjällä saattaa olla käyttöoikeus useisiin luetteloihin tietyn ajan sisällä, näiden luetteloiden tuotteiden oletus on se, että tuoteluettelot ovat toisensa poissulkevia. Toisin sanoen sama tuote ei saisi olla useamman kuin yhden luettelon osa tietyn käyttäjän osalta.

Jos kuitenkin ilmenee tilanne, jossa sama tuote kuuluu useaan luetteloon, järjestelmä ylläpitää useita ostoskärryrivejä tälle tuotteelle. Kutakin luetteloa varten on erillinen rivi. Samaa tuotetta kahdesta eri luettelosta ei yhdistetä kassatapahtumassa.

## <a name="when-a-b2b-shopper-is-shopping-is-there-any-validation-for-catalog-availability"></a>Kun B2B-ostaja ostaa tekee ostoksia, onko luettelon käytettävyydelle oikeellisuustarkistusta?

Kyllä. B2B-ostaja voi jatkaa kassatapahtumaan vain, jos kaikki ostoskärryn nimikkeet ovat peräisin sallituista luetteloista. Jos jokin ostoskorinimikkeet ovat vanhentuneista tai takaisin vedetyistä luetteloista, nimikkeet poistetaan ja käyttäjälle ilmoitetaan.

## <a name="during-the-shopping-experience-are-search-and-product-discovery-including-related-and-recommended-product-collections-catalog-specific"></a>Ovatko ostoskokemuksen aikana haku ja tuotteiden löytäminen (mukaan lukien liittyvät ja suositeltavat tuotekokoelmat) luettelokohtaisia?

Kyllä. Kun käyttäjä valitsee tietyn luettelon, koko ostossiirtymästä tulee luettelokohtainen. Se tarkoittaa myös tuotteiden löytymiskokemuksia, kuten hakuehdotuksia, hakutuloksia, luokkatuloksia, tarkentajia, hinnoitteluja, määritteitä ja suositeltuja tuotteita (kuten uudet, myydyimmät, trendaavat, usein ostettuja yhdessä ja liittyvät tuotteet).

## <a name="can-a-b2b-shopper-purchase-from-the-default-assortment-catalogid0"></a>Voiko B2B-ostaja ostaa oletusvalikoimasta (catalogID=0)?

Ei, B2B-ostaja ei voi ostaa oletusvalikoimasta. Valikoima on tarkoitettu vain nimettömään selailuun. Jos B2B-ostajalta puuttuu luettelomäärityksiä (hallintoa odottavat päivitykset), he eivät voi tarkastella luetteloita, joista he voisivat valita, eikä luokkahierarkiaa näy.

## <a name="can-marketing-content-be-curated-for-a-product-that-is-specific-to-a-catalog"></a>Voiko markkinointisisällön kuratoida luettelokohtaista tuotetta varten?

Tällä hetkellä tuotteen rikastusta tuetaan vain sivuston ja kanavan tasoilla. Toisin sanoen, jos tuote on rikastettu, se on jaettu useisiin luetteloihin, ja tuotteen vastaava tuotetietosivu (PDP) muodostetaan samalla tavalla kaikkien tietyn sivuston tuoteluetteloiden välillä.

## <a name="is-catalog-support-available-for-both-b2b-and-business-to-consumer-b2c-online-channels"></a>Onko luettelotuki käytettävissä sekä B2B- että B2C-verkkokanavissa?

Tällä hetkellä Commerce-luetteloiden on tarkoitus toimia vain B2B-kanavien kanssa.

## <a name="can-we-set-up-catalog-specific-upsellcross-sell-items"></a>Voinko määrittää luettelokohtaisia lisämyynti- ja liittyviä nimikkeitä?

Tällä hetkellä vain liittyvien tuotteiden toiminnallisuutta tuetaan. Lisä- ja ristiinmyyntinimikekonfiguraatiot ovat kuitenkin käytettävissä puhelinkeskuksissa.

Lisäksi seuraavia ominaisuuksia tuetaan vain puhelinkeskuksissa:

- Luettelon lähdekoodit
- Lähteen tunnus kustannusten ja vastausprosenttien seuraamiseen
- Luettelokohtaiset tilausten ja nimikkeiden komentosarjat
- Luettelosivujen analyysi
- Luettelopyynnöt
- Maksusuunnitelmat
- Lähdekoodeihin perustuvat maksuttomat tuotteet

## <a name="can-we-use-catalog-source-codes-for-b2b-orders-through-the-e-commerce-portal"></a>Voiko luettelon lähdekoodeja käyttää B2B-tilauksille sähköisen kauppaportaalin kautta?

Ei Luettelon lähdekoodeja tuetaan vain puhelinkeskuskanavien osalta.

## <a name="additional-resources"></a>Lisäresurssit

[Commerce-luetteloiden luominen B2B-sivustoja varten](catalogs-b2b-sites.md)

[Commerce-luetteloiden laajennettavuusvaikutus B2B-mukautuksia varten](catalogs-b2b-sites-dev.md)
