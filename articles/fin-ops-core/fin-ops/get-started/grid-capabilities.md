---
title: Ruudukon ominaisuudet
description: Tässä aiheessa kuvataan useita ruudukon ohjausobjektin tehokkaita ominaisuuksia. Uudella ruudukkotoiminnolla on oltava käyttöoikeus näihin ominaisuuksiin.
author: jasongre
manager: AnnBe
ms.date: 04/10/2020
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
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 0fd0e15ea88e9f5f34d8dff82606a8d26616a16d
ms.sourcegitcommit: cd8a28be0acf31c547db1b8f6703dd4b0f62940c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2020
ms.locfileid: "3260457"
---
# <a name="grid-capabilities"></a>Ruudukon ominaisuudet

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Uusi ruudukon ohjausobjekti tarjoaa useita hyödyllisiä ja tehokkaita ominaisuuksia, joilla voidaan parantaa käyttäjien tuottavuutta, kehittää mielenkiintoisempia näkymiä tiedoillesi ja hankkia merkityksellisiä tietoja datastasi. Tämä artikkeli käsittelee seuraavia ominaisuuksia: 

-  Lasketaan kokonaissummia
-  Tietojen ryhmitteleminen
-  Järjestelmän ennakoiva kirjoitus
-  Matemaattisten lausekkeiden arviointi 

## <a name="calculating-totals"></a>Lasketaan kokonaissummia
Finance and Operations -sovelluksissa käyttäjät voivat tarkastella summia ruudukkojen numeeristen sarakkeiden alla. Nämä summat näkyvät alatunnisteosassa ruudukon alla. 

### <a name="showing-the-grid-footer"></a>Ruudukon alatunnisteen näyttäminen
Finance and Operations -sovellusten jokaisen taulukkomuotoisen ruudukon alaosassa on alatunnistealue. Alatunniste voi näyttää arvokkaita tietoja, jotka liittyvät ruudukossa näkyviin tietoihin. Seuraavassa on joitakin esimerkkejä näistä tiedoista:

- Taulukossa vallittuna olevien rivien määrä (kun vähintään kaksi tietuetta on valittuna)
- Kokonaismäärät määritettyjen numeeristen sarakkeiden alla
- Tietojoukon rivimäärä 

Tämä alatunniste on oletusarvoisesti piilotettuna, mutta sen voi helposti ottaa käyttöön. Jos haluat ruudukon alatunnisteen näkyviin, napsauta ruudukon sarakeotsikkoa hiiren kakkospainikkeella ja valitse **Näytä alatunniste** -asetus. Kun alatunniste on otettu käyttöön tietyssä ruudukossa, asetus muistetaan, kunnes käyttäjä valitsee alatunnisteen piilottamisen. Tämä voidaan tehdä napsauttamalla sarakeotsikkoa hiiren kakkospainikkeella ja valitsemalla **Piilota alatunniste**.  Huomaa, että **Näytä alatunniste / Piilota alatunniste** -toiminnon sijaintia on tarkoitus muuttaa tulevassa päivityksessä. 

### <a name="specifying-columns-with-totals"></a>Summia sisältävien sarakkeiden määritys
Tällä hetkellä sarakkeita ei määritetä näyttämään summia oletusarvoisesti. Sen sijaan tämä katsotaan yksivaiheiseksi määritystoiminnoksi, joka muistuttaa sarakkeiden leveyden muuttamista ruudukoissa. Kun määrität, että haluat nähdä sarakkeen summat, tämä asetus muistetaan, kun seuraavan kerran käyt sivulla.  

Sarake voidaan määrittää näyttämään summaa kahdella tavalla: 

- Napsauta sitä saraketta, jonka summan haluat nähdä, hiiren kakkospainikkeella ja valitse **Laske sarake yhteen**. Tämä toiminto aiheuttaa seuraavat kolme tapahtumaa:

    1. Alatunniste tulee näkyviin. 
    2. Tämän sarakkeen katseluasetus tallennetaan. 
    3. Aloitetaan summan laskeminen tässä sarakkeessa ja kaikissa muissa sarakkeissa, joiden summa on määritetty laskettavaksi. Aika, joka vaaditaan näyttämään kokonaissummat, riippuu käytettävän tietokannan koosta.

- Kun alatunniste on näkyvissä, valitse **Näytä summa** sen sarakkeen alatunnistealueella, jonka summan haluat nähdä. Jos määritettyjä sarakkeita ei ole, **Näytä summa** -painike on käytettävissä kaikkien numeeristen sarakkeiden osalta. 

    Kun vähintään yksi sarake on määritetty summia varten, **Näytä summa** -painikkeet ovat käytettävästi vain osoittamalla tai kohdistamalla. **Näytä summa** -painikkeen valintatoiminto vain tallentaa tämän sarakkeen summan katselun asetukset niin, että asetuksia käytetään sivulla myös myöhemmin. Alatunnisteessa tämä tila ilmaistaan ajatusviivalla, joka näkyy sarakkeessa. (Vaihtoehtoisesti, jos tietojoukko on tarpeeksi pieni, summa näytetään heti.)

Jos teet virheen, etkä enää halua nähdä tietyn sarakkeen summaa, napsauta sitä hiiren kakkospainikkeella ja valitse **Piilota summa** tai valitse **Piilota summa** -painike kyseisen sarakkeen alatunnisteesta. Tämä valinta tallennetaan myös tulevia sivuvierailuja varten. 

### <a name="calculating-totals"></a>Lasketaan kokonaissummia
Kun tulet sivulle, jolla alatunniste on näkyvissä ja sarakkeita on jo määritetty summia varten, summat saattavat näkyä alatunnisteessa. Näkyminen riippuu sivun tietojoukon koosta. Jos tietojoukko on riittävän pieni, summat ja tietojoukon rivien määrä näytetään automaattisesti. Jos alatunnisteessa on ajatusviivoja niiden sarakkeiden alla, jotka on määritetty summia varten, tietojoukko on liian suuri sille, että järjestelmä pystyisi näyttämään summat välittömästi. Tällöin summien laskeminen vaatii erillisiä toimia. Nämä summat saadaan laskettua napsauttamalla alatunnisteen **Laske**-painiketta tai napsauttamalla hiiren kakkospainikkeella haluttua saraketta ja valitsemalla **Laske sarake yhteen**.  

Jos laskeminen kestää liian kauan, voit peruuttaa toiminnon valitsemalla **Peruuta**-painikkeen. Joskus tietojoukko on kuitenkin liian suuri summien laskemiseen (organisaation määrittämä raja) ja sinua pyydetään suodattamaan tietosi tarkemmin.

Kokonaissummat päivittyvät automaattisesti, kun päivität, poistat tai luot rivejä tietojoukossa.  

## <a name="grouping-data"></a>Tietojen ryhmitteleminen
Yrityskäyttäjien on usein suoritettava tiedoille ad-hoc-analyyseja. Vaikka tämä voidaan tehdä viemällä tiedot Microsoft Exceliin ja käyttämällä pivot-taulukoita, käyttäjät voivat taulukkoruudukkojen **Ryhmittely**-ominaisuuksilla järjestää tietonsa mielenkiintoisilla tavoilla Finance and Operations -sovelluksia käyttäen. Koska tämä toiminto laajentaa **Summat**-toimintoa, **Ryhmittely** mahdollistaa myös merkityksellisten tietojen hankkimisen datasta tarjoamalla ryhmätason välisummia.

Jos haluat käyttää tätä toimintoa, napsauta hiiren kakkospainikkeella saraketta, jota haluat käyttää ryhmittelyperusteena ja valitse **Ryhmittele tämän sarakkeen perusteella**. Tämä toiminto lajittelee tiedot valitun sarakkeen mukaan, lisää uuden ryhmittelyperustesarakkeen ruudukon alkuun ja lisää otsikkorivit kunkin ryhmän alkuun. Nämä otsikkorivit sisältävät seuraavat tiedot kustakin ryhmästä: 
-  Ryhmän tietojen arvo 
-  Sarakeotsikko (nämä tiedot ovat erityisen hyödyllisiä silloin, kun tuetaan useita ryhmittelytasoja.)
-  Tämän ryhmän tietorivien määrä
-  Kaikkien summattavaksi määritettyjen sarakkeiden välisummat

Kun [Tallennetut näkymät](saved-views.md) ovat käytössä, tämä ryhmittely voidaan tallentaa mukautuksen mukaan osana nopean käytön näkymää seuraavaa sivuvierailua varten.  

Jos valitset **Ryhmittele tämän sarakkeen perusteella** jossakin muussa sarakkeessa, alkuperäinen ryhmittely korvataan, koska versiossa 10.0.9 ja Platform updatessa 33 tuetaan vain yhtä ryhmittelytasoa.

Voit kumota ruudukon ryhmittelyn napsauttamalla ryhmittelysaraketta hiiren kakkospainikkeella ja valitsemalla **Pura ryhmittely**.  


## <a name="evaluating-math-expressions"></a>Matemaattisten lausekkeiden arviointi
Tuottavuutta tehostaakseen käyttäjät voivat antaa matemaattisia kaavoja ruudukon numeerisiin soluihin. Heidän ei tarvitse tehdä laskelmia järjestelmän ulkopuolisissa sovelluksissa. Jos esimerkiksi syötät **=15\*4** ja painat sitten **sarkainnäppäintä** ja siirryt pois kentästä, järjestelmä arvioi lausekkeen ja tallentaa kentän arvoksi **60**.

Jos haluat, että järjestelmä tunnistaa arvon lausekkeena, aloita arvo yhtäsuuruusmerkillä (**=**). Lisätietoja tuetuista operaattoreista ja syntaksista on kohdassa [Tuetut matemaattiset symbolit](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Miten otan uuden ruudukonhallinnan käyttöön omassa ympäristössäni? 

**10.0.9/Platform-päivitys 33 ja** uudemmat **Uusi ruudukonhallinta** -toiminto on käytettävissä suoraan ominaisuuksienhallinnassa missä tahansa ympäristössä. Kuten muutkin julkiset esikatseluominaisuudet, tämän toiminnon ottaminen käyttöön tuotannossa edellyttää [Lisäkäyttöehdot-sopimusta](https://go.microsoft.com/fwlink/?linkid=2105274).  

**10.0.8/Platform-päivitys 32 ja 10.0.7/Platform-päivitys 31** aiemmat **Uusi ruudukonhallinta** -ominaisuus voidaan ottaa käyttöön Tier 1 (Dev/Test)- ja Tier 2 (eristysympäristö) -ympäristöissä, jotta voit tarjota lisätestejä ja rakennemuutoksia noudattamalla seuraavia ohjeita.

1.  **Ota pikapäivitys käyttöön**: Suorita seuraava SQL-lause: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLIReactGridEnableFeature', 1, 0, 5637144576);`

2. **Palauta IIS** tyhjentääksesi staattisen välimuistin. 

3.  **Etsi ominaisuus**: Siirry **Ominaisuuksien hallinta** -työtilaan. Jos **Uusi ruudukonhallinta** -ohjausobjekti ei näy kaikkien ominaisuuksien luettelossa, valitse **Tarkista päivitykset**.   

4.  **Ota ominaisuus käyttöön**: Etsi **Uusi ruudukonhallinta** -ominaisuus ominaisuuksien luettelosta ja napsauta **Ota käyttöön nyt** tietoruudussa. Huomaa, että selaimen päivitys on pakollinen. 

Kaikki myöhemmät käyttäjäistunnot alkavat, kun uusi ruudukonhallinta on käytössä.
