---
title: Ruudukon ominaisuudet
description: Tässä aiheessa kuvataan useita ruudukon ohjausobjektin tehokkaita ominaisuuksia. Uudella ruudukkotoiminnolla on oltava käyttöoikeus näihin ominaisuuksiin.
author: jasongre
manager: AnnBe
ms.date: 01/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b49d7823f48bcc9cdbb56b87d5fa72d46ddfa15c
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019751"
---
# <a name="grid-capabilites"></a>Ruudukon ominaisuudet

[!include [banner](../includes/banner.md)]

Uusi ruudukon ohjausobjekti tarjoaa useita hyödyllisiä ja tehokkaita ominaisuuksia, joilla voidaan parantaa käyttäjien tuottavuutta, kehittää mielenkiintoisempia näkymiä tiedoillesi ja hankkia merkityksellisiä tietoja datastasi. Tämä artikkeli käsittelee seuraavia ominaisuuksia: 

-  Lasketaan kokonaissummia
-  Tietojen ryhmitteleminen
-  Järjestelmän ennakoiva kirjoitus
-  Matemaattisten lausekkeiden arviointi 

## <a name="calculating-totals"></a>Lasketaan kokonaissummia
Finance and Operations -sovelluksissa käyttäjät voivat tarkastella summia ruudukkojen numeeristen sarakkeiden alla. Nämä summat näkyvät alatunnisteosassa ruudukon alla. 

### <a name="showing-the-grid-footer"></a>Ruudukon alatunnisteen näyttäminen
Jokaisessa Finance and Operations -sovellusten taulukkoruudukossa on alatunnistealue ruudukon alla. Siinä voidaan esittää arvokkaita näytettäviin tietoihin liittyviä tietoja. Näitä tietoja ovat esimerkiksi: 
-  Taulukossa vallittuna olevien rivien määrä (kun vähintään kaksi tietuetta on valittuna)
-  Kokonaismäärät määritettyjen numeeristen sarakkeiden alla
-  Tietojoukon rivimäärä 

Tämä alatunniste on oletusarvoisesti piilotettuna, mutta sen voi helposti ottaa käyttöön. Jos haluat ruudukon alatunnisteen näkyviin, napsauta ruudukon sarakeotsikkoa hiiren kakkospainikkeella ja valitse **Näytä alatunniste** -asetus. Kun alatunniste on otettu käyttöön tietyssä ruudukossa, asetus muistetaan, kunnes käyttäjä valitsee alatunnisteen piilottamisen. Tämä voidaan tehdä napsauttamalla sarakeotsikkoa hiiren kakkospainikkeella ja valitsemalla **Piilota alatunniste**.  Huomaa, että **Näytä alatunniste / Piilota alatunniste** -toiminnon sijaintia on tarkoitus muuttaa tulevassa päivityksessä. 

### <a name="specifying-columns-with-totals"></a>Summia sisältävien sarakkeiden määritys
Tällä hetkellä sarakkeita ei määritetä näyttämään summia oletusarvoisesti. Sen sijaan tämä katsotaan yksivaiheiseksi määritystoiminnoksi, joka muistuttaa sarakkeiden leveyden muuttamista ruudukoissa. Kun määrität, että haluat nähdä sarakkeen summat, tämä asetus muistetaan, kun seuraavan kerran käyt sivulla.  

Sarake voidaan määrittää näyttämään summaa kahdella tavalla: 
1.  Napsauta sitä saraketta, jonka summan haluat nähdä, hiiren kakkospainikkeella ja valitse**Laske sarake yhteen**. Tämä toiminto tekee kolme asiaa. Ensinnäkin se muuttaa alatunnisteen näkyväksi. Toiseksi se tallentaa valintasi nähdä tämän sarakkeen summa. Kolmanneksi tämä toiminto aloittaa tämän sarakkeen ja kaikkien muiden sarakkeiden, joiden summa on määritetty laskettavaksi, summan laskemisen. Summan näkyviin tulon aika määräytyy suoraan yhteenlaskettavan tietojoukon kokoon.  

2.  Kun alatunniste on muutettu näkyväksi, voit vaihtoehtoisesti valita sarakkeen alla olevan alatunnistealueen **Näytä summa** -painiketta niiden sarakkeiden kohdalla, joiden summan haluat nähdä. Jos määritettyjä sarakkeita ei ole, **Näytä summa** -painike on näkyvissä kaikkien numeeristen sarakkeiden osalta. Kun vähintään yksi sarake on määritetty summia varten, **Näytä summa** -painikkeet ovat käytettävästi vain osoittamalla tai kohdistamalla. Tämä toiminto vain tallentaa valintasi summan näyttämiseksi tässä sarakkeessa tulevia sivuvierailujasi varten. Tämä tila ilmaistaan ajatusviiva, joka tulee näkyviin tämän sarakkeen alatunnisteen kohdalla (tai summa näkyy välittömästi, jos tietojoukko on riittävän pieni).

Jos teet virheen, etkä enää halua nähdä tietyn sarakkeen summaa, napsauta sitä hiiren kakkospainikkeella ja valitse **Piilota summa** tai valitse **Piilota summa** -painike kyseisen sarakkeen alatunnisteesta. Tämä valinta tallennetaan myös tulevia sivuvierailuja varten. 

### <a name="calculating-totals"></a>Lasketaan kokonaissummia
Kun tulet sivulle, jolla alatunniste on näkyvissä ja sarakkeita on jo määritetty summia varten, summat saattavat näkyä alatunnisteessa. Näkyminen riippuu sivun tietojoukon koosta. Jos tietojoukko on riittävän pieni, summat ja tietojoukon rivien määrä näytetään automaattisesti. Jos alatunnisteessa on ajatusviivoja niiden sarakkeiden alla, jotka on määritetty summia varten, tietojoukko on liian suuri sille, että järjestelmä pystyisi näyttämään summat välittömästi. Tällöin summien laskeminen vaatii erillisiä toimia. Nämä summat saadaan laskettua napsauttamalla alatunnisteen **Laske**-painiketta tai napsauttamalla hiiren kakkospainikkeella haluttua saraketta ja valitsemalla **Laske sarake yhteen**.  

Jos laskeminen kestää liian kauan, voit peruuttaa toiminnon valitsemalla **Peruuta**-painikkeen. Joskus tietojoukko on kuitenkin liian suuri summien laskemiseen (organisaation määrittämä raja) ja sinua pyydetään suodattamaan tietosi tarkemmin.

Kokonaissummat päivittyvät automaattisesti, kun päivität, poistat tai luot rivejä tietojoukossa.  

## <a name="grouping-data"></a>Tietojen ryhmitteleminen
Yrityskäyttäjien on usein suoritettava tiedoille ad-hoc-analyyseja. Vaikka tämä voidaan tehdä viemällä tiedot Microsoft Exceliin ja käyttämällä pivot-taulukoita, käyttäjät voivat taulukkoruudukkojen **Ryhmittely**-ominaisuuksilla järjestää tietonsa mielenkiintoisilla tavoilla Finance and Operations -sovelluksia käyttäen. Koska tämä toiminto laajentaa **Summat**-toimintoa, **Ryhmittely** mahdollistaa myös merkityksellisten tietojen hankkimisen datasta tarjoamalla ryhmätason välisummia.

Jos haluat käyttää tätä toimintoa, napsauta hiiren kakkospainikkeella saraketta, jota haluat käyttää ryhmittelyperusteena ja valitse **Ryhmittele tämän sarakkeen perusteella**. Tämä toiminto lajittelee tiedot valitun sarakkeen mukaan, lisää uuden ryhmittelyperustesarakkeen ruudukon alkuun ja lisää otsikkorivit kunkin ryhmän alkuun. Nämä otsikkorivit sisältävät seuraavat tiedot kustakin ryhmästä: 
-  Ryhmän tietojen arvo 
-  Sarakeotsikko. Tästä tulee erityisen hyödyllistä, kun useita ryhmittelytasoja tuetaan.  
-  Tämän ryhmän tietorivien määrä
-  Kaikkien summattavaksi määritettyjen sarakkeiden välisummat

Kun [Tallennetut näkymät](saved-views.md) ovat käytössä, tämä ryhmittely voidaan tallentaa mukautuksen mukaan osana nopean käytön näkymää seuraavaa sivuvierailua varten.  

Jos valitset **Ryhmittele tämän sarakkeen perusteella** jossakin muussa sarakkeessa, alkuperäinen ryhmittely korvataan, koska versiossa 10.0.9 / Platform update 33 tuetaan vain yhtä ryhmittelytasoa.

Voit kumota ruudukon ryhmittelyn napsauttamalla ryhmittelysaraketta hiiren kakkospainikkeella ja valitsemalla **Pura ryhmittely**.  


## <a name="evaluating-math-expressions"></a>Matemaattisten lausekkeiden arviointi
Käyttäjä voi syöttää matemaattisia kaavoja tuottavuuden tehostamiseksi ruudukon numeerisiin soluihin sen sijaan, että hänen tarvitsisi suorittaa laskenta järjestelmän ulkopuolisessa sovelluksessa. Voit esimerkiksi syöttää **=15\*4** ja käyttää tabulaattoria kentästä poistumiseen. Järjestelmä arvioi lausekkeen ja asettaa kentän arvoksi 60.

Jos haluat, että järjestelmä tunnistaa arvon lausekkeena, aloita arvo yhtäsuuruusmerkillä (**=**). Lisä tietoja tuetuista operaattoreista ja syntaksista on kohdassa [Tuetut matemaattiset symbolit](http://redhivesoftware.github.io/math-expression-evaluator/#supported-maths-symbols).  
