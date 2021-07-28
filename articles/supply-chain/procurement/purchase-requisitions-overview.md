---
title: Ostoehdotusten yleiskatsaus
description: Tässä aiheessa kuvataan ostoehdotusten työnkulkua ja eri tiloja.
author: kamaybac
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqConsolidation, PurchReqCreate, PurchReqCreatePurchDetails, PurchReqCreatePurchListPage, PurchReqTable, PurchReqTableListPage, PurchReqConsolidationPartByVendor, PurchReqConsolidationLineDetail, PurchReqConsolidationCreate, PurchReqConsolidationBulkEdit, PurchReqConsolidationAddLine
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2174"
- intro-internal
ms.assetid: 77d07119-4d9f-4c0e-acbe-d319203571ab
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8bde73d424e72ad66c27decd11a3b866d02b48c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349791"
---
# <a name="purchase-requisition-overview"></a>Ostoehdotusten yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan ostoehdotusten työnkulkua ja eri tiloja.

Voit luoda ostoehdotuksia organisaatiosi käyttämille tuotteille riippuen siitä, kuinka organisaatiosi on asetettu. Ostoehdotus on sisäinen asiakirja, joka valtuuttaa hankintaosaston ostamaan nimikkeitä tai palveluita.  

Kun ostoehdotus on hyväksytty, sitä voidaan käyttää ostotilauksen luomiseen. Ostotilaukset ovat ulkoisia tiedostoja, joita hankintaosasto lähettää toimittajille.

## <a name="creating-purchase-requisitions"></a>Ostoehdotuksien luominen
Voit luoda ostoehdotuksen **Omat ostoehdotukset** -sivulla ja valita tarvitsemasi nimikkeet ja palvelut. Voit valita nimikkeet tuotteiden hankintaluettelosta, jonka organisaatiosi on luonut, tai voit pyytää nimikkeet, joita ei löydy luettelosta, valitsemalla hankintaluokan ja kirjoittamalla tuotteen tiedot.  

Ennen kuin ostoehdotus voidaan lähettää tarkistettavaksi, työnkulut on määritettävä. Työnkulun avulla voit siirtää ostoehdotuksen tarkistusprosessin läpi alkuperäisestä **Luonnos**-tilasta lopulliseen **Hyväksytty**-tilaan.

### <a name="purchase-requisition-statuses"></a>Ostoehdotusten tilat

Kun luot uuden ostotilauksen, sille määritetään tila. Jokaiselle ostoehdotusriville määritetään myös tila. Kun käyttäjä lähettää ostoehdotuksen työnkulkuun tarkistusta varten, ostoehdotuksen ja jokaisen ehdotusrivin tilaa päivitetään kun ne siirtyvät työnkulkuprosessin läpi.  

Voit määrittää ostoehdotuksen työnkulkuprosessin voi kierrättämään ostoehdotuksen tarkistuksen kautta yhtenä asiakirjana. Vaihtoehtoisesti ostoehdotuksen rivit voidaan reitittää yksittäin sopiville tarkistajille. Jos ostoehdotusrivit tarkastetaan yksitellen, kunkin rivin tilaa voi päivittää kun rivi kulkee tarkastusprosessi läpi. Kun kaikki rivit ovat käyneet läpi koko tarkastusprosessin, eikä ostoehdotuksella ole jäljellä tarkastustyövaiheita, hankintaehdotuksen yleinen tila päivitetään.

### <a name="purchase-requisition-workflow"></a>Ostoehdotuksen työnkulku

Seuraava kaavio kuvaa ostoehdotukselle ja sen riveille määritettäviä tiloja kun ne kulkevat työnkulkuprosessin läpi.  

[![Ostoehdotuksen otsikon ja rivien tilat.](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)

### <a name="purchase-requisition-header-and-line-status-relationships"></a>Ostoehdotuksen otsikon ja rivien tilojen suhde

Ostoehdotuksen yleinen tila määritetään ostoehdotusrivien tilan mukaan. Siispä tarkistusprosessi on täytettävä kaikilla ostoehdotusriveillä ennen kuin koko ehdotuksen tarkistusprosessi on valmis. Seuraava taulukko kuvaa ostoehdotuksen otsikolle ja sen riveille määritettäviä tiloja kun ne kulkevat työnkulkuprosessin läpi.

<table>
<thead>
<tr class="header">
<th>Ostoehdotuksen tila</th>
<th>Ostoehdotuksen rivin tila</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Luonnos</td>
<td>Luonnos</td>
<td>Ostoehdotus ja ostoehdotusrivi on luotu, mutta niitä ei ole lähetetty tarkastettavaksi. Ostoehdotuksia ja ostoehdotusrivejä, joiden tila on <strong>Luonnos</strong>, voi muokata. Ostoehdotuksen tai ostoehdotusrivin tila voi olla <strong>Luonnos</strong> myös silloin, kun se on peruutettu mutta sitä ei ole lähetetty tarkistettavaksi. <strong>Huomautus:</strong> Voit lähettää tai peruuttaa ostoehdotuksen asiakirjatasolla. Et voi kuitenkaan lähettää tai peruuttaa yksittäistä ostoehdotusriviä.</td>
</tr>
<tr class="even">
<td>Tarkistuksessa</td>
<td><ul>
<li>Tarkistuksessa</li>
<li>Hylätty</li>
</ul></td>
<td>Jos työnkulku on määritetty reitittämään ostoehdotusrivit yksittäisille tarkastajille, kunkin rivin tila voi olla <strong>Tarkistuksessa</strong> tai <strong>Hylätty</strong>. Hankintaehdotuksen yleinen tila päivitetään, kun kaikki rivit ovat käyneet läpi koko tarkastusprosessin, eikä ostoehdotuksella ole jäljellä tarkastustyövaiheita.
<ul>
<li><strong>Tarkistuksessa</strong> – Ostoehdotusrivit on lähetetty tarkistettavaksi. Kun ostoehdotusrivin työnkulkuprosessi on valmis, rivi pysyy <strong>Tarkistuksessa</strong>-tilassa kunnes kaikki muut ostoehdotusrivit on tarkistettu.</li>
<li><strong>Hylätty</strong> – Ostoehdotusrivin on hylätty. Hylättyjä ostoehdotuksen rivejä voidaan muokata ja lähettää uudelleen.</li>
</ul>
Jos lähetät hylätyn ostoehdotusrivin uudelleen, tarkistusprosessi käynnistyy uudelleen kaikille ostoehdotuksen riveille, jotka ovat yhä tarkistuksessa. </br><strong>Huomautus:</strong> Voit peruuttaa jo lähetetyn ostoehdotuksen. Kun peruutat ostoehdotuksen, kaikki sen ostoehdotusrivit peruutetaan samalla. Peruutetut ostoehdotusrivit on mahdollista poistaa.</td>
</tr>
<tr class="odd">
<td>Hylätty</td>
<td>Hylätty</td>
<td>Ostoehdotus ja kaikki sen rivit on hylätty. Hylätyt ostoehdotukset ja ostoehdotusrivit on mahdollista lähettää uudelleen.</td>
</tr>
<tr class="even">
<td>Hyväksytty</td>
<td><ul>
<li>Hyväksytty</li>
<li>Peruutettu</li>
<li>Suljettu</li>
</ul></td>
<td>Kaikki ostoehdotusrivit ovat käyneet läpi koko tarkastusprosessin, eikä ostoehdotuksella ole jäljellä tarkastustyövaiheita.
<ul>
<li><strong>Hyväksytty</strong> – Ostoehdotusrivin tarkistus on valmis ja rivi on hyväksytty.</li>
<li><strong>Peruutettu</strong> – Ostoehdotusrivi on hyväksytty, mutta se on peruutettu tarpeettomana. Ainoastaan hyväksytyt ostoehdotusrivit on mahdollista peruuttaa.</li>
<li><strong>Suljettu</strong> – Ostoehdotusrivi on hyväksytty ja asiakirjat on luotu ostoehdotuksen käyttötarkoituksen mukaan.
<ul>
<li>Jos ostoehdotuksen tarkoitus on kulutus, ostoehdotusriville on luotu ostotilaus.</li>
<li>Jos ehdotuksen tarkoitus on täydennys, järjestelmä on luonut yhden tai useamman toteuttamisasiakirjan.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Peruutettu</td>
<td>Peruutettu</td>
<td>Ostoehdotus ja kaikki ostoehdotusrivit on peruutettu.</br> <strong>Huomautus:</strong> Jos et enää tarvitse ostoehdotusrivillä olevaa nimikettä, ostoehdotusrivi on peruutettava, jos se on jo hyväksytty. Ainoastaan hyväksytyt ostoehdotusrivit on mahdollista peruuttaa. Jos yksikään ostoehdotusrivi on vielä tarkistettavana, ostoehdotuksen yleinen tila on <strong>Tarkistettavana</strong>. Tässä tapauksessa voit peruuttaa ostoehdotuksen ja poistaa haluamasi ostoehdotusrivin.</td>
</tr>
<tr class="even">
<td>Suljettu</td>
<td><ul>
<li>Suljettu</li>
<li>Peruutettu</li>
</ul></td>
<td>Ostoehdotus on suljettu ja järjestelmä on luonut yhden tai useamman toteuttamisasiakirjan.
<ul>
<li><strong>Suljettu</strong> – Ostoehdotusrivi on hyväksytty ja asiakirjat on luotu ostoehdotuksen käyttötarkoituksen mukaan.
<ul>
<li>Jos ostoehdotuksen tarkoitus on kulutus, ostoehdotusriville on luotu ostotilaus.</li>
<li>Jos ehdotuksen tarkoitus on täydennys, järjestelmä on luonut yhden tai useamman toteuttamisasiakirjan.</li>
</ul></li>
<li><strong>Peruutettu</strong> – Ostoehdotusrivi on hyväksytty, mutta se on peruutettu tarpeettomana. Ainoastaan hyväksytyt ostoehdotusrivit on mahdollista peruuttaa.</li>
</ul>
<strong>Huomautus:</strong> Jos suljetulla ostoehdotusrivillä on nimike, jota ei enää tarvita, rivi on peruutettava ostoehdotusriville luodulta toteuttamisasiakirjalta.</td>
</tr>
</tbody>
</table>

## <a name="distributing-costs-to-multiple-financial-accounts"></a>Kustannusten jakaminen useisiin kirjanpitotileihin
Voit jakaa kustannukset tuotteesta, joka kuuluu ostoehdotukseen, useille kirjanpitotileille. Jos organisaatiossa käytetään dimensioita, kuten kustannuspaikkoja ja osastoja, voit jakaa tuotekustannukset dimensioista taloushallinnon tileille.

## <a name="requisition-purposes"></a>Ehdotuksen tarkoitukset
Ostoehdotuksen tarkoitukset tekevät ehdotuksien vaatimusten toteuttamisesta joustavampaa. Ehdotuksen luodessasi voit liittää yksi kahdesta tarkoituksesta siihen: kulutus tai täydennys. Riippuen ehdotuksen tarkoituksesta ja siitä, miten organisaatio on määritetty, ehdotuksen tarve voidaan täyttää ostotilauksella, siirtotilauksella, tuotantotilauksella tai kanbanilla.  

Hankintakäytännöissä voit hallita ostoehdotusten tarkoituksia, jotka ovat käytettävissä, kun ehdotus luodaan organisaatioosi.

### <a name="requisitions-that-have-a-purpose-of-consumption"></a>Ehdotukset, joiden tarkoituksena on kulutus

Ehdotus, jonka tarkoitus on kulutus esittää tarpeen nimikkeille tai palveluille, joita organisaatiosi käyttää sisäisesti. Tämän tyyppisellä ehdotuksella luotu kysyntä täytetään aina ostotilauksella. Jos Supply Chain Management on määritetty luomaan ostotilauksia automaattisesti, ostotilaukset luodaan, kun ostoehdotus hyväksytään.

### <a name="requisitions-that-have-a-purpose-of-replenishment"></a>Ehdotukset, joiden tarkoitus täydennys

Ehdotus, jonka tarkoitus on täydennys, edustaa varaston täydentämistä tarvittaessa. Voit esimerkiksi luoda tilauksen tuotteiden täydentämiseksi, jotta ne voidaan myydä määrätyssä vähittäismyyntipaikassa tiettyyn aikaan. Tämäntyyppisen ehdotuksen aikaansaama kysyntä voidaan täyttää ostotilauksella, siirtotilauksella, tuotantotilauksella tai kanbanilla.  

Kun ehdotuksen tarkoitus on täydennys, rahasumman sijaan kysyntä ilmaistaan määränä. Siksi varauskirjanpitoa, budjetinvalvontaa, liiketoimintasääntöjä käyttöomaisuuden määritykselle (BRAD), projektin kirjanpitoa ja mahdollisia muita liittyviä sääntöjä ei sovelleta. Vain sellaiset tuotteet, joita varastoidaan ja jotka on vapautettu määritetylle yritykselle, voivat täyttää täydennysehdotustarpeen. Täydennystä varten luotavissa ehdotuksissa käytettävät tuotteet voit määrittää **Täydennysluokan käyttöoikeuskäytäntöjen sääntö** -sivulla.  

Käyttääksesi ostoehdotuksia, joiden tarkoitus on täydennys, pääajoitus on määritettävä sisältämään ehdotustarpeen pääajoituksessa. Tämäntyyppisiin tarkoituksiin luotujen ehdotuksien toteutuskeinot määräytyvät automaattisesti tarjonnan säännöksien kautta, jotka on perustettu organisaatiosi artikkeleille ja suunniteltu käyttämällä pääaikatauluja.

## <a name="purchase-requisitions-and-requests-for-quotation"></a>Ostoehdotukset ja tarjouspyynnöt
Joissain tapauksissa on aloitettava tarjouspyyntöprosessi, jonka kautta tunnistat toimittajan ja ostoehdotuksessa pyydettyjen tuotteiden hinnan. Tarjouspyynnön voi luoda ostoehdotuksen ollessa tarkistettavana. Kun hyväksyt tarjouksen, tiedot toimittajasta, hinnasta ja niin edelleen siirretään ehdotukseen.  

Voit laittaa ostoehdotuksen pitoon valitsemalla **Pidossa**-valintaruudun **Ostoehdotuksen tiedot** -sivulla. Ostoehdotuksen käsittely voi jatkua vasta, kun poistat eston poistamalla tämän valintaruudun.  

> [!NOTE]
> Sähköisessä hankinnassa ostoehdotuksesi tarjouspyyntö voi antaa toimittajien lisätä vaihtoehtoisia rivejä. Tässä tapauksessa hyväksytyt vaihtoehdot näkyvät ostoehdotuksessa.

## <a name="demand-consolidation"></a>Kysynnän konsolidointi
Yhdistämällä useita ostoehdotusrivejä useista ostoehdotuksista voit lisätä neuvotteluvoimaa toimittajia kohtaan ja saavuttaa paremman hinnoittelun, pienemmät lähetys- ja käsittelykustannukset ja vähentää yleiskustannuksia.  

Ostoehdotusrivit ovat käytettävissä tarpeiden yhdistämiseen vain, jos seuraavat ehdot täyttyvät:

-   Ostoehdotus on hyväksytty.
-   Ostoehdotus täyttää ostokäytäntösäännön ehdot manuaalisen käsittelyn ja kysynnän konsolidoinnin osalta.

Hyväksytyt ostotilausrivit, jotka täyttävät manuaalisen käsittelyn ehdot näkyvät **Vapauta hyväksytyt ostoehdotukset** -sivulla. Jos ostoehdotusrivi vastaa myös kriteerien kysynnän konsolidointia, rivi voidaan lisätä konsolidointiehdotukseen.  

Konsolidointiehdotus on joukko ostoehdotusrivejä, jotka on ryhmitetty niin, että hankinnan ammattilainen voi neuvotella parhaan mahdollisen sopimuksen toimittajien kanssa. Ostoehdotusrivit, jonka olet valinnut konsolidointiehdotukseen näkyvät **Ostoehdotuksen konsolidointi** -sivulla. Voit muokata rivejä tällä sivulla, jos niihin on tehtävä muutoksia. Voit lisätä uusia rivejä tai poistaa olemassa olevia rivejä konsolidointiehdotuksesta.  

Kun olet lisännyt hankintarivejä konsolidointiehdotukseen ja tehnyt tarvitsemasi muutokset, voit luoda ostotilauksen konsolidoiduille ostoehdotusriveille.  

> [!NOTE]
> Muutokset, jotka teet ostoehdotusriviin **Ostoehdotuksen konsolidointi** -sivulla näkyvät luomassasi ostotilauksessa. Ostoehdotuksen rivi säilyy kuitenkin muuttumattomana ehdotuksessa, jotta historiatiedot säilyvät.  

Voidaksesi luoda ostotilauksen ostoehdotusriveille, joille ei ole valittavissa kysynnän konsolidointia tai joita ei ole valittu konsolidointiehdotukseen on käsiteltävä manuaalisesti.

### <a name="consolidating-purchase-requisition-lines"></a>Ostoehdotuksen rivien konsolidointi

Kysynnän konsolidoinnin prosessi alkaa kohdasta, jossa ostoehdotus hyväksytään työnkulussa, jos budjetin hallinta on määritetty organisaatiolle ja budjettivaraukset sekä alustavat varaukset on tallennettu. Seuraavassa kaaviossa on kuvattu prosessin kulku kysynnän konsolidoinnille.  

[![Kysynnän konsolidointiprosessin kulku.](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)  

Noudata seuraavia vaiheita, jos haluat konsolidoida ostoehdotusrivit.

1.  Tarkista hyväksytyt ehdotusrivit, jotka on käsitelty manuaalisesti ja jotka ovat oikeutettuja kysynnän konsolidointiin.
2.  Valitse konsolidointimahdollisuuteen lisättävät ostoehdotusrivit.
3.  Luo uusi konsolidointiehdotus tai lisää ehdotusrivit olemassa olevaan konsolidointiehdotukseen.
4.  Tee tarvittavat muutokset ehdotusriveille ja poista ehdotuksen rivinimikkeet, joita et halua enää sisällyttää konsolidointiehdotukseen.
5.  Luo ostotilaukset konsolidoiduille ehdotusriveille tai konsolidointiehdotuksen ostoehdotusriveille.


## <a name="additional-resources"></a>Lisäresurssit

[Luo kulutusehdotus](tasks/create-requisition-consumption.md)

[Ostoehdotuksen työnkulku](purchase-requisitions-workflow.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]