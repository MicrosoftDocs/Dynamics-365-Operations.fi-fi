---
title: "Talousraporttien suunnittelutoiminnon rivimääritykset"
description: "Rivin määritys on raporttiosa tai rakenneosa, joka määrittää talousraportin kunkin rivin sisällön. Rivin määritys voidaan yhdistää sarakemääritykseen, raportointipuun määrityksiin ja raportin määrityksiin. Näin luodaan rakenneosaryhmä, jota voidaan käyttää useissa yrityksissä."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 770a1681e4fa9974b081d0c63a10eb1961f13014
ms.openlocfilehash: 6d4697af6f7467f25a461fae4e9320402f83b0e3
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Talousraporttien suunnittelutoiminnon rivimääritykset
<a id="row-definitions-in-financial-report-designer" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Rivin määritys on raporttiosa tai rakenneosa, joka määrittää talousraportin kunkin rivin sisällön. Rivin määritys voidaan yhdistää sarakemääritykseen, raportointipuun määrityksiin ja raportin määrityksiin. Näin luodaan rakenneosaryhmä, jota voidaan käyttää useissa yrityksissä.

Rivimäärityksen luominen
<a id="create-a-row-definition" class="xliff"></a>
-----------------------

1.  Valitse Report Designerin siirtymisruudussa **Rivien määritykset**.
2.  Valitse ensin **Tiedosto**-valikossa **Uusi** ja sitten **Rivin määritys**. Lisätietoja kunkin solun sisällöstä on kohdassa [Rivin määrityksen solujen muokkaaminen](modify-row-definition-cells-financial-reporting.md).

## Rivin määrityksen avaaminen
<a id="open-a-row-definition" class="xliff"></a>
1.  Valitse Report Designerin siirtymisruudussa **Rivien määritykset**.
2.  Napsauta avattavan rivin määrityksen nimeä hiiren kakkospainikkeella.
3.  Voit tarkastella rivin määritykseen liittyviä rakenneosia napsauttamalla rivin määritystä hiiren kakkospainikkeella ja valitsemalla **Liitokset**.

##  Rivin määrityksen sisältö
<a id="contents-of-a-row-definition" class="xliff"></a>
Rivin määritys voi sisältää enintään 20 000 taloushallinnon dimension riviä. Rivit voivat sisältää seuraavia tietoja:

-   Kuvaava teksti, joka lisää raporttiin merkityksiä luomalla osan otsikoita, rivejä ja välilyöntejä, kuten **Käteinen** tai **Kokonaistuotto**.
-   Linkkejä taloushallinnon tietoihin, jotka voivat sisältää Microsoft Dynamics 365 for Finance and Operations -ohjelman dimensioarvoja **Huomautus:** Voit määrittää rivin määrityksen, kun haluat noutaa tietoja taloushallinnon dimensioiden järjestelmästä aina raportin luomisen yhteydessä.
-   Linkitettyihin taloushallinnon tietoihin perustuvien rivien yhteissummat ja kaavat.

Yleensä jokainen rivin määrityksen rivi sisältää jonkin seuraavaksi esitellyistä tietotyypeistä.

-   Viitteet taloushallinnon dimensioiden järjestelmään.
-   Tietoihin perustuvat yhteissummat tai laskelmat.
-   Muotoilu

Rivi määrityksen tiedot voidaan antaa kahdella tavalla:

-   Anna rivin tiedot manuaalisesti uudessa rivin määrityksessä. Lisätietoja on kohdassa [Rivin määrityksen solujen muokkaaminen](modify-row-definition-cells-financial-reporting.md).
-   Hae rivitiedot Report Designerilla suoraan taloushallinnon dimensioista. Lisätietoja on artikkelin [Muokkaa rivin määrityssoluja](modify-row-definition-cells-financial-reporting.md) kohdassa Liittyvät kaavat, rivit ja yksiköt.

##  Dimensioiden lisääminen rivin määritykseen
<a id="add-dimensions-in-a-row-definition" class="xliff"></a>
Dimensio on tietojen ja arvojen liitos. Voit ryhmitellä tietoja ja arvoja Report Designerissa. Voit sitten luokitella ja analysoida tapahtumia yksityiskohtaisemmin. Voit lisätä rivin määritykseen useita rivejä samanaikaisesti **Lisää rivejä dimensioista** -valintaikkunan avulla. Valintaikkunassa näkyy kunkin dimension yksi sarake. Seuraavassa taulussa kuvataan tietoja, joilla kukin dimensio määritetään.

| Vaihtoehto                | Kuvaus                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dimensio             | Malli, joka määrittää rivin määritykseen lisättävän dimension. Tämä malli sisältää yhden et-merkin (&) tai numeromerkin (\#) jokaista dimension sijaintia kohti. Yleensä et-merkkejä käytetään päätilin dimensioissa ja numeromerkkejä muissa dimensioissa. |
| Dimensiovälin alku | Tämän dimension ensimmäinen arvo, joka lisätään rivin määritykseen.                                                                                                                                                                                                                 |
| Dimensiovälin loppu   | Tämän dimension viimeinen arvo, joka lisätään rivin määritykseen.                                                                                                                                                                                                                  |

Seuraavien vaiheiden avulla voit lisätä dimensioita rivin määritykseen.

1.  Valitse Report Designerissa **Rivien määritykset** ja avaa sitten muokattava rivin määritys.
2.  Valitse **Muokkaa** -valikosta **Lisää rivejä dimensioista**.
3.  Valitse **Lisää rivejä dimensioista**-valintaikkunan **Dimensiot**-rivillä rivin määritykseen siirrettävä dimension solu. Valitse sitten **Kaikki &&&**.
4.  Voit rajoittaa rivin määrityksen tiettyyn dimensioarvojen väliin antamalla **Dimensiovälin alku**-soluun dimension aloitusarvon ja **Dimensiovälin loppu** -soluun dimension lopetusarvon. Jos haluat sisällyttää kaikki valitun dimension arvot, jätä nämä solut tyhjäksi. **Huomautus:** Dimensioalueilla käytettävät yleismerkit (\* tai ?) eivät välttämättä palauta kaikkia haluttuja tuloksia sen mukaan, miten ERP-tietokanta kokoaa tiedot.
5.  Määritä **Aloittavan rivin koodi** -kenttään ensimmäisen rivin määritykseen lisättävän dimensioarvon rivikoodi.
6.  Määritä **Lisää kutakin riviä arvolla** -kenttään kahden peräkkäisen rivikoodin väli. Jos esimerkiksi ensimmäisen rivin koodi on 100 ja lisäysarvo on 30, ensimmäisten uusien rivien koodit ovat 100, 130, 160, 190 ja 220. Käytä lisäysarvoa, joka määrittää riittävästi tilaa uuden muotoilu- ja kaavarivien lisäämistä varten.
7.  Napsauta **OK**. Kullekin valitulle dimensioarvolle lisätään yksi rivi rivin määritykseen.

##  Pyöristyksen oikaisu rivin määrityksessä
<a id="adjust-rounding-in-a-row-definition" class="xliff"></a>
Jos taseessa on pyöristettyjä summia, kokonaissummat eivät ehkä täsmää. Tämä ongelma voi esiintyä esimerkiksi silloin, kun käytät taseraportissa pyöritysasetusta ja pyöristys määritetään myös raportin määrityksessä. Voit täsmätä taseen summat käyttämällä rivin määrityksessä **Pyöristyksen oikaisu** -vaihtoehtoa. Voit poistaa pyöristyksen käytöstä tai muokata sitä raportin määrityksen **Asetukset**-välilehdessä. Seuraavassa taulukossa on esitetty, miten summat pyöristetään. Rivien 100 ja 200 kokonaissummat ovat erilaiset tässä taulukossa, kun pyöristys ei ole käytössä.

| Rivin koodi | Summat ilman pyöristystä | Summat, jotka pyöristetään kokonaisiin tuhansiin |
|----------|--------------------------|-----------------------------------------|
| 100      | 3,600                    | 4                                       |
| 200      | 3,700                    | 4                                       |
| Yhteensä    | 7,300                    | 8                                       |

Voit oikaista taseen pyöristyksen seuraavasti.

1.  Valitse Report Designerissa **Rivien määritykset** ja avaa muokattava rivin määritys.
2.  Valitse **Muokkaa**-valikosta **Pyöristyksen oikaisu**.
3.  Syötä **Pyöristyksen oikaisut** -valintaikkunaan seuraavat arvot:
    -   **Pyöristyksen oikaisurivi** – Sen rivin rivikoodi, joka on oikaistava taseen täsmäyttämiseksi.
    -   **Kaikkien käyttöomaisuuserien rivi** – Taseen kaikki käyttöomaisuuserät sisältävän rivin koodi.
    -   **Kaikkien velkojen ja pääoman rivi** – Taseen kaikki velat ja pääoman sisältävän rivin koodi.
    -   **Oikaisusumman raja** – Positiivinen kokonaisluku, joka määrittää automaattisten oikaisujen rajan. Tätä summaa verrataan toteutuneen pyöristyseron absoluuttiseen arvoon.

    **Huomautus:** Nämä rivin koodit on linkitettävä taloushallinnon tietoihin. Toisin sanoen rivillä on oltava dimensioarvo **Linkki taloushallinnon dimensioon** -solussa. **Älä** tee viittausta kuvauksen riviin (**DESC**), laskettuun riviin (**CALC**) tai kokonaissumman riviin (**TOT**).

Taseen summat täsmäytetään nyt tasaisesti, kun pyöristys on päällä. **Huomautus:** Oikaisun raja otetaan käyttöön raportin määritykselle määritetyn **Pyöristystarkkuus**-vaihtoehdon perusteella. Jos esimerkiksi pyöristät raportin tuhansiksi ja annat **Oikaisusumman raja** -kentässä arvoksi **2**, näyttöön avautuu varoitussanoma, kun **Pyöristyksen oikaisurivi** -kentän arvo nousee tai laskee enemmän kuin 2 000.

## Rivin ja sarakkeen tekstin muotoileminen
<a id="format-row-and-column-text" class="xliff"></a>
Voit mukauttaa raporttien ulkoasua muuttamalla fontteja ja muotoilemalla tekstiä. Seuraavassa osassa kerrotaan, miten raporttien rivien ja sarakkeiden ulkoasua muotoillaan.

### Fonttityylien hallinta
<a id="manage-font-styles" class="xliff"></a>

Voit luoda ja muokata raportin fonttityylejä. Voit sitten käyttää näitä tyylejä asiakirjassa tai raportin tietyllä rivillä tai tietyssä sarakkeessa.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Luo fonttityyli</td>
<td><ol>
<li>Valitse Report Designerin <strong>Muotoilu</strong>-valikosta <strong>Tyylit ja muotoilu</strong>.</li>
<li>Valitse <strong>Tyylit ja muotoilu</strong> -valintaikkunassa <strong>Uusi</strong> ja anna uudelle tyylille yksilöivä nimi.</li>
<li>Valitse fontit ja valitse sitten <strong>OK</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Muokkaa fonttityyliä</td>
<td><ol>
<li>Valitse Report Designerin <strong>Muotoilu</strong>-valikosta <strong>Tyylit ja muotoilu</strong>.</li>
<li>Valitse ensin muokattava tyyli <strong>Tyylit ja muotoilu</strong> -valintaikkunassa ja sitten <strong>Muokkaa</strong>.</li>
<li>Valitse fontit ja valitse sitten <strong>OK</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Ota fonttityyli käyttöön</td>
<td><ol>
<li>Valitse Report Designerin määrityksessä tai sarakkeen määrityksessä tai ylä- tai alatunnisteissa vähintään yksi solu.</li>
<li>Valitse työkalurivin <strong>Tyyli</strong>-luettelosta fonttityyli.</li>
</ol></td>
</tr>
</tbody>
</table>

### Rivin tekstin muotoileminen
<a id="format-row-text" class="xliff"></a>

Rivin määrityksessä määritetty muotoilu korvaa sarakkeen ja raportin määrityksessä määritetyn muotoilun. Voit muokata tekstimuotoa muotoilun työkalurivin ohjausobjekteilla. Nämä ohjausobjektit ovat Microsoft Windowsin vakio-ohjausobjekteja.

1.  Avaa Report Designer -ohjelmassa muokattava rivin määritys.
2.  Valitse muokattavat solut. Voit valita useita soluja pitämällä Ctrl-näppäintä alhaalla valinnan aikana.
3.  Ota muoto käyttöön valitsemalla muodon työkalurivipainike. Jos haluat esimerkiksi sisentää rivin, valitse ensin rivi ja sitten työkalurivin **Kasvata sisennystä** ![Kasvata sisennystä](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Kasvata sisennystä").

### Sarakkeiden oikaisu raporttien suunnittelun yhteydessä
<a id="adjust-columns-while-you-design-reports" class="xliff"></a>

Rivin määrityksen käsiteltävien sarakkeiden tarkasteleminen helpottuu oikaisemalla sarakkeen leveyttä ja piilottamalla (pienentämällä) tai näyttämällä sarakkeet näkymäruudussa. Tekemäsi muutokset vaikuttavat sarakkeiden ulkoasuun vain näytössä. Ne eivät vaikuta raporttien sarakemuotoiluun.

### Sarakkeen leveyden muuttaminen näkymäruudussa
<a id="change-the-width-of-a-column-in-the-view-pane" class="xliff"></a>

1.  Avaa Report Designer -ohjelmassa muokattava rivin määritys.
2.  Valitse **Muotoilu**-valikosta **Sarakkeen leveys**.
3.  Anna **Sarakkeen leveys** -valintaikkunassa arvo ja valitse sitten **OK**. Vaihtoehtoisesti voit muuttaa sarakkeen kokoa vetämällä sarakeotsikkosolun oikeaa reunaa.

### Sarakkeiden piilottaminen näkymäruudussa
<a id="hide-columns-in-the-view-pane" class="xliff"></a>

1.  Avaa Report Designer -ohjelmassa muokattava rivin määritys.
2.  Valitse sarake tai sarakkeet pienennystä varten.
3.  Napsauta kohdetta hiiren kakkospainikkeella ja valitse sitten **Piilota**.

### Kaikkien piilotettujen sarakkeiden näyttäminen näkymäruudussa
<a id="show-all-hidden-columns-in-the-view-pane" class="xliff"></a>

1.  Avaa Report Designer -ohjelmassa muokattava rivin määritys.
2.  Napsauta näytettävää pienennettyä saraketta hiiren kakkospainikkeella ja valitse sitten **Tuo esiin**.


Lisätietoja
<a id="see-also" class="xliff"></a>
--------

[Taloushallinnan raportointi](financial-reporting-intro.md)




