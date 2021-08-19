---
title: Talousraporttien suunnittelutoiminnon rivimääritykset
description: Rivin määritys on raporttiosa tai rakenneosa, joka määrittää talousraportin kunkin rivin sisällön.
author: aprilolson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e175d1e3de1f5db31de9c4600c8a5935f0cb11a9d39bc0f4e142edf5fc00ce86
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745909"
---
# <a name="row-definitions-in-financial-report-designer"></a>Talousraporttien suunnittelutoiminnon rivimääritykset

[!include [banner](../includes/banner.md)]

Rivin määritys on raporttiosa tai rakenneosa, joka määrittää talousraportin kunkin rivin sisällön. Rivin määritys voidaan yhdistää sarakemääritykseen, raportointipuun määrityksiin ja raportin määrityksiin. Näin luodaan rakenneosaryhmä, jota voidaan käyttää useissa yrityksissä.

## <a name="create-a-row-definition"></a>Rivimäärityksen luominen

1. Valitse Report Designerin siirtymisruudussa **Rivien määritykset**.
2. Valitse ensin **Tiedosto**-valikossa **Uusi** ja sitten **Rivin määritys**. Lisätietoja kunkin solun sisällöstä on kohdassa [Rivin määrityksen solujen muokkaaminen](modify-row-definition-cells-financial-reporting.md).

## <a name="open-a-row-definition"></a>Rivin määrityksen avaaminen
1. Valitse Report Designerin siirtymisruudussa **Rivien määritykset**.
2. Napsauta avattavan rivin määrityksen nimeä hiiren kakkospainikkeella.
3. Voit tarkastella rivin määritykseen liittyviä rakenneosia napsauttamalla rivin määritystä hiiren kakkospainikkeella ja valitsemalla **Liitokset**.

## <a name="contents-of-a-row-definition"></a> Rivin määrityksen sisältö
Rivin määritys voi sisältää enintään 20 000 taloushallinnon dimension riviä. Rivit voivat sisältää seuraavia tietoja:

- Kuvaava teksti, joka lisää raporttiin merkityksiä luomalla osan otsikoita, rivejä ja välilyöntejä, kuten **Käteinen** tai **Kokonaistuotto**.
- Linkkejä taloushallinnon tietoihin, jotka voivat sisältää Microsoft Dynamics 365 Financen dimensioarvoja.

    > [!NOTE]
    > Voit määrittää rivimäärityksiä, kun haluat, että tietoja noudetaan taloushallinnon dimensiojärjestelmästä aina, kun raportti luodaan.

- Linkitettyihin taloushallinnon tietoihin perustuvien rivien yhteissummat ja kaavat.

Yleensä jokainen rivin määrityksen rivi sisältää jonkin seuraavaksi esitellyistä tietotyypeistä.

- Viitteet taloushallinnon dimensioiden järjestelmään.
- Tietoihin perustuvat yhteissummat tai laskelmat.
- Muotoilu

Rivi määrityksen tiedot voidaan antaa kahdella tavalla:

- Anna rivin tiedot manuaalisesti uudessa rivin määrityksessä. Lisätietoja on kohdassa [Rivin määrityksen solujen muokkaaminen](modify-row-definition-cells-financial-reporting.md).
- Hae rivitiedot Report Designerilla suoraan taloushallinnon dimensioista. Lisätietoja on artikkelin [Muokkaa rivin määrityssoluja](modify-row-definition-cells-financial-reporting.md) kohdassa Liittyvät kaavat, rivit ja yksiköt.

## <a name="add-dimensions-in-a-row-definition"></a> Dimensioiden lisääminen rivin määritykseen
Dimensio on tietojen ja arvojen liitos. Voit ryhmitellä tietoja ja arvoja Report Designerissa. Voit sitten luokitella ja analysoida tapahtumia yksityiskohtaisemmin. Voit lisätä rivin määritykseen useita rivejä samanaikaisesti **Lisää rivejä dimensioista** -valintaikkunan avulla. Valintaikkunassa näkyy kunkin dimension yksi sarake. Seuraavassa taulussa kuvataan tietoja, joilla kukin dimensio määritetään.

| Vaihtoehto                | Kuvaus |
|-----------------------|-------------|
| Dimensio             | Malli, joka määrittää rivin määritykseen lisättävän dimension. Tämä malli sisältää yhden et-merkin (&) tai numeromerkin (\#) jokaista dimension sijaintia kohti. Yleensä et-merkkejä käytetään päätilin dimensioissa ja numeromerkkejä muissa dimensioissa. |
| Dimensioalueen alku | Rivimääritykseen lisättävän dimension ensimmäinen arvo. |
| Dimensioalueen loppu   | Tämän dimension viimeinen arvo, joka lisätään rivin määritykseen. |

Seuraavien vaiheiden avulla voit lisätä dimensioita rivin määritykseen.

1. Valitse Report Designerissa **Rivien määritykset** ja avaa sitten muokattava rivin määritys.
2. Valitse **Muokkaa** -valikosta **Lisää rivejä dimensioista**.
3. Valitse **Lisää rivejä dimensioista**-valintaikkunan **Dimensiot**-rivillä rivin määritykseen siirrettävä dimension solu. Valitse sitten **Kaikki &&&**.
4. Voit rajoittaa rivin määrityksen tiettyyn dimensioarvojen väliin antamalla **Dimensiovälin alku**-soluun dimension aloitusarvon ja **Dimensiovälin loppu** -soluun dimension lopetusarvon. Jos haluat sisällyttää rivimääritykseen kaikki valitun dimension arvot, jätä nämä solut tyhjiksi.

    > [!NOTE]
    > Yleismerkit (\* tai ?) dimensioalueissa eivät ehkä palauta kaikkia haluamiasi tuloksia, sillä tietojen lajittelutapa ERP-tietokannassa vaikuttaa tuloksiin.

5. Määritä **Aloittavan rivin koodi** -kenttään ensimmäisen rivin määritykseen lisättävän dimensioarvon rivikoodi.
6. Määritä **Lisää kutakin riviä arvolla** -kenttään kahden peräkkäisen rivikoodin väli. Jos esimerkiksi ensimmäisen rivin koodi on 100 ja lisäysarvo on 30, ensimmäisten uusien rivien koodit ovat 100, 130, 160, 190 ja 220. Käytä lisäysarvoa, joka määrittää riittävästi tilaa uuden muotoilu- ja kaavarivien lisäämistä varten.
7. Napsauta **OK**. Kullekin valitulle dimensioarvolle lisätään yksi rivi rivin määritykseen.

## <a name="adjust-rounding-in-a-row-definition"></a> Pyöristyksen oikaisu rivin määrityksessä
Jos taseessa on pyöristettyjä summia, kokonaissummat eivät ehkä täsmää. Tämä ongelma voi esiintyä esimerkiksi silloin, kun käytät taseraportissa pyöritysasetusta ja pyöristys määritetään myös raportin määrityksessä. Voit täsmätä taseen summat käyttämällä rivin määrityksessä **Pyöristyksen oikaisu** -vaihtoehtoa. Voit poistaa pyöristyksen käytöstä tai muokata sitä raportin määrityksen **Asetukset**-välilehdessä. Seuraavassa taulukossa on esitetty, miten summat pyöristetään. Rivien 100 ja 200 kokonaissummat ovat erilaiset tässä taulukossa, kun pyöristys ei ole käytössä.

| Rivin koodi | Summat ilman pyöristystä | Summat, jotka pyöristetään kokonaisiin tuhansiin |
|----------|--------------------------|-----------------------------------------|
| 100      | 3,600                    | 4                                       |
| 200      | 3,700                    | 4                                       |
| Yhteensä    | 7,300                    | 8                                       |

Voit oikaista taseen pyöristyksen seuraavasti.

1. Valitse Report Designerissa **Rivien määritykset** ja avaa muokattava rivin määritys.
2. Valitse **Muokkaa**-valikosta **Pyöristysoikaisu**.
3. Syötä **Pyöristyksen oikaisut** -valintaikkunaan seuraavat arvot:

    - **Pyöristyksen oikaisurivi** – Sen rivin rivikoodi, joka on oikaistava taseen täsmäyttämiseksi.
    - **Kaikkien käyttöomaisuuserien rivi** – Taseen kaikki käyttöomaisuuserät sisältävän rivin koodi.
    - **Kaikkien velkojen ja pääoman rivi** – Taseen kaikki velat ja pääoman sisältävän rivin koodi.
    - **Oikaisusumman raja** – Positiivinen kokonaisluku, joka määrittää automaattisten oikaisujen rajan. Tätä summaa verrataan toteutuneen pyöristyseron absoluuttiseen arvoon.

    > [!NOTE]
    > Nämä rivikoodit on linkitettävä taloushallinnon tietoihin. Toisin sanoen rivillä on oltava dimensioarvo **Linkki taloushallinnon dimensioihin** -solussa. **Älä** tee viittausta kuvauksen riviin (**DESC**), laskettuun riviin (**CALC**) tai kokonaissumman riviin (**TOT**).

Taseen summat täsmäytetään nyt tasaisesti, kun pyöristys on päällä.

> [!NOTE]
> Oikaisun rajoitus perustuu raporttimääritykselle määritettyyn **Pyöristystarkkuus**-asetukseen. Jos esimerkiksi pyöristät raportin tuhansiksi ja annat **Oikaisusumman raja** -kentässä arvoksi **2**, näyttöön avautuu varoitussanoma, kun **Pyöristyksen oikaisurivi** -kentän arvo nousee tai laskee enemmän kuin 2 000.

## <a name="format-row-and-column-text"></a>Rivin ja sarakkeen tekstin muotoileminen
Voit mukauttaa raporttien ulkoasua muuttamalla fontteja ja muotoilemalla tekstiä. Seuraavassa osassa kerrotaan, miten raporttien rivien ja sarakkeiden ulkoasua muotoillaan.

### <a name="manage-font-styles"></a>Fonttityylien hallinta

Voit luoda ja muokata raportin fonttityylejä. Voit sitten käyttää näitä tyylejä asiakirjassa tai raportin tietyllä rivillä tai tietyssä sarakkeessa.

<table>
<tbody>
<tr>
<td><strong>Luo fonttityyli</strong></td>
<td>
<ol>
<li>Valitse Report Designerin <strong>Muotoilu</strong>-valikosta <strong>Tyylit ja muotoilu</strong>.</li>
<li>Valitse <strong>Tyylit ja muotoilu</strong>-valintaikkunassa <strong>Uusi</strong> ja anna sitten uudelle tyylille yksilöllinen nimi.</li>
<li>Tee fonttia koskevat valinnat ja valitse <strong>OK</strong>.</li>
</ol>
</td>
</tr>
<tr>
<td><strong>Fonttityylin muokkaaminen</strong></td>
<td>
<ol>
<li>Valitse Report Designerin <strong>Muotoilu</strong>-valikosta <strong>Tyylit ja muotoilu</strong>.</li>
<li>Valitse muokattava tyyli <strong>Tyylit ja muotoilu</strong> -valintaikkunassa ja valitse sitten <strong>Muokkaa</strong>.</li>
<li>Tee fonttia koskevat valinnat ja valitse <strong>OK</strong>.</li>
</ol>
</td>
</tr>
<tr>
<td><strong>Ota fonttityyli käyttöön</strong></td>
<td>
<ol>
<li>Valitse Report Designerin määrityksessä tai sarakkeen määrityksessä tai ylä- tai alatunnisteissa vähintään yksi solu.</li>
<li>Valitse fonttityyli työkalurivin <strong>Tyyli</strong>-luettelosta.</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>Rivin tekstin muotoileminen

Rivin määrityksessä määritetty muotoilu korvaa sarakkeen ja raportin määrityksessä määritetyn muotoilun. Voit muokata tekstimuotoa muotoilun työkalurivin ohjausobjekteilla. Nämä ohjausobjektit ovat Microsoft Windowsin vakio-ohjausobjekteja.

1. Avaa raporttien suunnitteluohjelmassa rivimääritys, jota haluat muokata.
2. Valitse muokattavat solut. Voit valita useita soluja pitämällä Ctrl-näppäintä alhaalla valinnan aikana.
3. Ota muoto käyttöön valitsemalla muodon työkalurivipainike. Jos haluat esimerkiksi sisentää rivin, valitse rivi ja valitse sitten **Kasvata sisennystä** ![Kasvata sisennystä.](media/indent.gif "Kasvata sisennystä") työkaluriviltä.

### <a name="adjust-columns-while-you-design-reports"></a>Sarakkeiden oikaisu raporttien suunnittelun yhteydessä

Rivin määrityksen käsiteltävien sarakkeiden tarkasteleminen helpottuu oikaisemalla sarakkeen leveyttä ja piilottamalla (pienentämällä) tai näyttämällä sarakkeet näkymäruudussa. Tekemäsi muutokset vaikuttavat sarakkeiden ulkoasuun vain näytössä. Ne eivät vaikuta raporttien sarakemuotoiluun.

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>Sarakkeen leveyden muuttaminen näkymäruudussa

1. Avaa Report Designer -ohjelmassa muokattava rivin määritys.
2. Valitse **Muotoilu**-valikosta **Sarakkeen leveys**.
3. Anna **Sarakkeen leveys** -valintaikkunassa arvo ja valitse sitten **OK**. Vaihtoehtoisesti voit muuttaa sarakkeen kokoa vetämällä sarakeotsikkosolun oikeaa reunaa.

### <a name="hide-columns-in-the-view-pane"></a>Sarakkeiden piilottaminen näkymäruudussa

1. Avaa Report Designer -ohjelmassa muokattava rivin määritys.
2. Valitse piilotettavat sarakkeet.
3. Napsauta kohdetta hiiren kakkospainikkeella ja valitse sitten **Piilota**.

### <a name="show-all-hidden-columns-in-the-view-pane"></a>Kaikkien piilotettujen sarakkeiden näyttäminen näkymäruudussa

1. Avaa Report Designer -ohjelmassa muokattava rivin määritys.
2. Napsauta näytettävää pienennettyä saraketta hiiren kakkospainikkeella ja valitse sitten **Tuo esiin**.


## <a name="additional-resources"></a>Lisäresurssit

[Taloushallinnon raportointi](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]