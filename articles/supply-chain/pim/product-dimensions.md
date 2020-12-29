---
title: Tuotedimensiot
description: 'Tuotedimensioita on neljä: väri, konfigurointi, koko, tyyli ja versio. Tuotedimensiot yhdistetään dimensioryhmiksi ja dimensioryhmät liitetään päätuotteisiin. Tuotedimensioiden yhdistelmät määrittävät sen, kuinka tuotevariantit määritetään.'
author: t-benebo
manager: tfehr
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle, EcoResVersionNameLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bdfd9482d30bd65cf84fae032df78e1243e05239
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426846"
---
# <a name="product-dimensions"></a>Tuotedimensiot

[!include [banner](../includes/banner.md)]

Tuotedimensioita on neljä: väri, konfigurointi, koko, tyyli ja versio. Tuotedimensiot yhdistetään dimensioryhmiksi ja dimensioryhmät liitetään päätuotteisiin. Tuotedimensioiden yhdistelmät määrittävät sen, kuinka tuotevariantit määritetään.

Tuotedimensiot ovat ominaisuuksia, joilla voidaan määrittää tuotemallin muuttuja. Voit käyttää tuotevarianttien määrittämiseen tuotedimensioiden yhdistelmiä. Sinun on määritettävä päätuotteelle vähintään yksi tuotedimensio, jotta voit luoda tuotevariantin.

## <a name="product-variants"></a>Tuotevariantit

Tuotemallin muuttujien kutsutaan myös nimikkeinä. Nimike on aineellinen tuote eikä tarkoita samaa kuin palvelu. Päätuotteen voi kuitenkin määrittää myös palvelutyypin kanssa. Käyttämällä Palvelu-tyyppiä voit määrittää tuotevariantit, jotka sisältävät palveluita. Voit esimerkiksi määrittää konsultointityölle päätuotteen ja tuotevariantit kokeneempien ja nuorempien konsulttien suorittamalle työlle.

## <a name="product-dimensions"></a>Tuotedimensiot

Tuotevariantit voidaan luoda tuotedimensioarvojen perusteella.

Koko-, väri- ja tyylidimensioiden tuotedimensioarvot voidaan määrittää seuraavissa sijainneissa:

- **Koko**-sivu (**tuotetietojen hallinta \> Määritys \> Dimensio ja varianttiryhmät \> Koot**)
- **Väri**-sivu (**Tuotetietojen hallinta \> Määritys \> Dimensio ja varianttiryhmät \> Värit**)
- **Tyyli**-sivu (**tuotetietojen hallinta \> Määritys \> Dimensio ja varianttiryhmät \> Tyylit**)

Konfiguraatiodimension tuotedimension arvot luodaan yleensä käyttämällä joko tuotekonfiguraatiota tai dimensioihin perustuvaa konfiguraatiota. 

Tuoteversiot luodaan yleensä tietyille versioille, kun tuote kehittyy elinkaarensa aikana. Tuoteversiot käsitellään yksityiskohtaisesti myöhemmin tässä ohjeaiheessa.

Tuotedimensioita voi luoda ja ylläpitää myös **Tuotedimensiot**-sivulla, jonka voi avata seuraavista sijainneista:

- Valitse **Tuotetietojen hallinta \> Tuotteet \> Päätuotteet**. Valitse toimintoruudussa **Tuotedimensiot**.
- Mene kohtaan **Tuotetietojen hallinta \> Tuotteet \> Kaikki tuotteet ja päätuotteet**. Valitse päätuote. Valitse toimintoruudussa **Tuotedimensiot**.
- Mene kohtaan **Tuotetietojen hallinta \> Vapautetut tuotteet**. Valitse päätuote. Valitse sitten toimintoruudun **Tuote**-välilehden **Päätuote**-ryhmässä **Tuotedimensiot**.

Tälle nimikkeelle luotavien varianttien lukumäärää rajoittaa mahdollisten tuotedimensioiden yhdistelmien määrä.

> [!TIP]
> Jos käytät tuotetta esimerkiksi tilausrivillä, voit valita tuotedimensiot määrittämään tuotevariantit, joita haluat käsitellä.

## <a name="example"></a>Esimerkki

Yritys myy farmarihousuja. *Farkut*-nimikkeessä on käytössä väri- ja koko-tuotedimensiot. Myytäviä farmarihousuja on kolmea eri väriä ja kuutta eri kokoa. Värit ovat sininen, musta ja ruskea. Koot ovat XS, S, M, L, XL ja XXL. Kaikki koot eivät ole saatavilla kolmessa värissä. Jos kaikki yhdistelmät olivat käytettävissä, olisi 18 eri farmarihousutyyppiä. Tässä esimerkissä tuotetaan kuitenkin vain seuraavat yhdeksän tuotevarianttia.

| Väri | Koko |
|-------|------|
| Sininen  | XS   |
| Sininen  | L    |
| Sininen  | M    |
| Musta | M    |
| Musta | L    |
| Musta | XL   |
| Ruskea | L    |
| Ruskea | XL   |
| Ruskea | XXL  |

## <a name="the-version-product-dimension"></a>Version tuotedimensio

Versio on tuotedimensio, jonka on tarkoitus auttaa ylläpitämään ja seuraamaan useita tuotteen versioita koko toimitusketjussa. Version seuranta on tärkeää sellaisten valmistajien menestykselle, jotka toimivat maailmassa, jossa tuotteen elinkaari lyhenee jatkuvasti, laatu- ja luotettavuusvaatimukset ovat entistä suurempia ja tuoteturvallisuutta painotetaan entistä enemmän.

Vakiotuotedimensiona versio toimii samalla tavalla kuin aiemmat tuotedimensiot (koko, tyyli, väri ja konfigurointi). Siksi sitä voidaan käyttää myös muihin tarkoituksiin tuoteversioiden seurannan lisäksi.

### <a name="turn-on-the-version-dimension"></a><a name="enable-version-dim"></a>Ota käyttöön version tuotedimensio

#### <a name="before-you-turn-on-the-version-dimension"></a>Ennen kuin otat käyttöön version tuotedimension

Kun otat version dimension käyttöön, jotkin toiminnot voivat katketa tai lakata toimimasta odotetulla tavalla, jos olet asentanut muita ratkaisuja, jotka lisäävät mukautuksia varastodimensioihin. Jotta versiodimensio olisi täysin toimiva, sinun on ehkä päivitettävä nämä ratkaisut niin, että ne sisällyttävät versiodimension viitevarastodimensioihin.

Kun testaat ratkaisujasi, jotka ovat yhteensopivia versiodimension kanssa, etsi seuraavia elementtejä:

1. **Toiminnot:** ennen kaikkea varastodimensioiden mukautukset on arvioitava sen varmistamiseksi, että ne voivat toimia yhdessä versiodimension kanssa.
1. **Viittaukset varastodimensioihin:** Varo viittauksia varastodimensioihin (eli paikkoihin, joihin dimensioihin on nimenomaisesti viitattu). Viittausten kohteeseen `InventDimId` pitäisi toimia heti, mutta varo viittauksia tyyliin tai väriin. Tarkista esimerkiksi seuraavat seikat:

    - API-kutsut laajennetuissa luokissa
    - Kaikki viittaukset tiettyihin varastodimensioihin laajennuskoodissa (tämän koodin täytyy kelluttaa versiodimensio yhdessä tyyli-, väri- ja kokodimensioiden kanssa.)

1. **Viittaukset vanhentuneisiin API-kutsuihin:** Microsoft on yrittänyt tehdä versiodimensiosta mahdollisimman vähän vanhentuneita sovellusliittymiä. Muutamat vanhentuneet API-liittymät antavat varoituksen, kun **tuotteen dimensioversion** konfigurointiavain otetaan käyttöön. Kutsut näihin API-rajapintoihin on korjattava laajennetuista ratkaisuistasi, ennen kuin otat käyttöön tuotantojärjestelmän versiodimension. Tässä ovat versiokohtaiset vanhentuneet API-liittymät:

    - RetailTransactionServiceInventory::getProductRecordId
    - EcoResProductNumberIdentifiedProductVariantEntity::find
    - EGAISAlcoholProduction_RU::findByItemDim
    - PCVariantConfiguration::findByProductMasterAndDimensions

1. **Kartat:** Jos kaikki kartat käyttävät varastodimensioita, näiden karttojen vastaava suhdemääritys on päivitettävä, jotta ne sisällyttävät version dimension. Etsi laajennetusta mallista tai taulukkolaajennuksista tauluja, joiden kentissä on varastodimensioita.
1. **Microsoft Dynamics 365 Commerce -toiminnot:** Kun se on otettu käyttöön, versiodimensio tulee näkyviin koko Commerce-kohtaisen koodin sisään Dynamics 365 Supply Chain Managementissa. Versiodimensiota ei kuitenkaan vielä tueta Commerce-kanavatietokannassa tai myyntipisteen (POS) tai sähköisen kaupankäynnin sovelluksissa. Nämä Commerce-kohtaiset sovellukset eivät tue käyttäjiä, jotka myyvät/lähettävät tai palauttavat/vastaanottavat varastoa versiodimension perusteella. Varaston saatavuushakufunktiot eivät erota varastoa Commerce-sovellusten versiodimensioiden perusteella. Tämä toiminta muistuttaa config-dimension nykyistä toimintaa kautta koko Commercen.

#### <a name="turn-on-the-version-dimension"></a>Ota käyttöön version tuotedimensio

Ennen kuin käytät versiodimensiota, se on otettava käyttöön järjestelmässä. Tämä tehtävä edellyttää järjestelmänvalvojan käyttöoikeuksia.

1. Valitse **Järjestelmänvalvoja \> Työtilat \> Ominaisuuksien hallinta**.
1. Ota käyttöön ominaisuus, jonka nimi on *Tuotedimension versio*. (Lisätietoja on kohdassa [Toiminnon hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Aseta järjestelmä [ylläpitotilaan](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**.
1. Laajenna **Konfigurointiavaimet**-välilehdessä **kauppa** ja valitse **tuotedimensioversio**-valintaruutu.
1. Poista [ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) käytöstä.

### <a name="areas-where-the-version-dimension-isnt-supported"></a>Alueet, joilla versiodimensiota ei tueta

Seuraavat alueet eivät tue versiodimensiota, koska tämän dimension käyttöönotto aiheuttaa muutoksia:

- Kustannuskohteen kuukausittainen tiliote
- Kustannusobjektiraportin välimuisti
- MCR-myynnin tilastotiedot nimikettä kohden
- Toimittajan tuoteluettelot
- EcoResProductDimensionGroupEntity

Lisäksi Commercen tilauksen luonti- ja tilausten käsittelytoiminnot (esimerkiksi POS-, puhelukeskus- ja verkkokauppatilaukset) eivät tue versiodimensiota. Vahvistettua aikataulua ei ole määritetty, kun Commercen tilauksia tuetaan.

### <a name="functional-characteristics-of-the-version-dimension"></a>Versiodimension toiminnalliset ominaisuudet

Versiodimensio toimii muiden tuotedimensioiden tapaan. Koska se kuitenkin on luonteeltaan erityinen ja koska sen tarkoituksena on ylläpitää ja jäljittää useita tuotteen versioita, se käyttäytyy hieman eri tavoin. Tässä joitain eroja ja yhtäläisyyksiä:

- **Versioryhmää ei ole.**

    Vaikka ryhmien käsite on määritetty koon, värin ja tyylin (väriryhmä, kokoryhmä ja tyyliryhmä) mukaan, versioryhmä käsitettä ei ole olemassa. Ryhmien avulla voit määrittää ennalta sovellettavat arvot niin, että kun esimerkiksi määrität tuotteelle väriryhmän, tuote voi käyttää kaikkia kyseisen väriryhmän värejä. Tätä käsitettä ei sovelleta versiodimensioon, koska tuotteen versiot eivät ole ennalta määriteltyjä tuotteen luonnin yhteydessä. Sen sijaan versiot luodaan tuotteen elinkaaren aikana, koska niitä tarvitaan. Jos tuotteen muoto, sovitus ja toiminto pysyvät samoina, luot uuden version uuden tuotteen asemesta.

- **Tuotevarianttiehdotukset toimivat tällä hetkellä.**

    Tuotevarianttiehdotukset luovat ehdotuksia kaikille version dimensioarvoille aivan kuten muidenkin dimensioiden osalta. Versioitujen tuotteiden luomis- ja julkaisuprosessi on sama kuin muissa dimensioissa käytettävät tuotteet. Kun luot versioidun tuotteen, ensimmäinen versio (V1) luodaan tuotedimensioksi ja muuttujat vapautetaan. Kun tuote muuttuu ja uusi versio tarvitaan, uusi versioarvo (V2) lisätään ja tarvittavat variantit vapautetaan. Ei ole odotettavissa, että kaikki versiot (V1, V2 ja V3) luodaan etukäteen tuotteelle.

> [!IMPORTANT]
> Jos otat käyttöön version dimension ja käytät sitä, jotkin varastodimensioihin viittaavat ratkaisut voivat lakata toimimasta odotetulla tavalla. Voit vahvistaa ja korjata nämä ongelmat ottamalla yhteyttä ohjelmistotoimittajaan (ISV) haavoittuvuuden sisältävissä ratkaisuissa. Lisätietoja on kohdassa [versiodimension ottaminen käyttöön](#enable-version-dim).
