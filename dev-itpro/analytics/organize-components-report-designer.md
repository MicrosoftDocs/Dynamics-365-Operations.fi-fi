---
title: "Järjestä Report Designerin raporttiosat"
description: "Kun olet suunnitellut rakennusosat ja luonut raportit, kyseiset objektit kannattaa järjestää niin, että käyttäjien on helppo löytää ne. Tässä artikkelissa käsitellään aiemmin luotujen Report Designerin raporttien, rakennusosien ja objektien järjestämistä."
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
ms.search.scope: Management Reporter, Core
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a8739f426c401aacbab56179bad429a231060f57
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="organize-report-components-in-report-designer"></a>Järjestä Report Designerin raporttiosat

[!include[banner](../includes/banner.md)]


Kun olet suunnitellut rakennusosat ja luonut raportit, kyseiset objektit kannattaa järjestää niin, että käyttäjien on helppo löytää ne. Tässä artikkelissa käsitellään aiemmin luotujen Report Designerin raporttien, rakennusosien ja objektien järjestämistä.

Voit nimetä uudelleen kansioita, raportteja, rakenneosia ja muita objekteja Report Designerissa. Uudelleennimetyn objektityypistä riippuen voit joutua päivittämään kyseisen objektin liitokset.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>Kansion tai rakenneosan nimeäminen uudelleen Report Designerissa
Report Designerissa voit nimetä uudelleen kansioita, raportin määrityksiä sekä rivi-, sarake- ja raportointipuumäärityksiä. **Huomautus:** Kun nimeät rakenneosan uudelleen, myös kyseistä rakenneosaa käyttävät raportin määritykset on päivitettävä. Muussa tapauksessa uutta raporttia ei voi luoda.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>Kansion tai rakenneosan nimeäminen uudelleen Report Designerissa

1.  Käytä Report Designerissa siirtymisruutua löytääksesi uudelleennimettävän kansion tai objektin.
2.  Valitse kansio tai objekti hiiren kakkospainikkeella ja valitse sitten **Nimeä uudelleen**. Siirtymisruudun **Nimi**-kenttä tulee käyttöön.
3.  Kirjoita uusi nimi ja paina sitten Enter-näppäintä.
4.  Jos rakenneosa on rivin määritys, sarakkeen määritys tai raportointipuun määritys, muut siihen liitetyt rakenneosat on päivitettävä. Valitse ensin vaiheessa 3 uudelleennimetty rakenneosa hiiren kakkospainikkeella, valitse sitten **Liitokset** ja valitse lopuksi luettelosta päivitettävä kohde.
5.  Toista vaihe 4, kunnes kaikki liitokset on päivitetty.

## <a name="create-and-manage-report-groups"></a>Reititysryhmien luonti ja hallinta
Voit ryhmitellä raporttimäärityksiä luodaksesi useita raportteja samanaikaisesti. Jos haluat luoda, muokata, poistaa ja luoda raporttiryhmiä, sinulla on oltava suunnittelijan tai järjestelmänvalvojan rooli. Käyttäjät, joilla on luontirooli, voivat luoda raporttiryhmiä. He voivat myös muokata käyttäjien raportin määritysten asetuksia raporttiryhmille.

### <a name="create-a-report-group"></a>Raporttiryhmän luonti

1.  Valitse Report Designerin siirtymisruudussa **Raporttiryhmät**.
2.  Avaa uusi raporttiryhmä katseluohjelman ikkunassa valitsemalla **Tiedosto**-valikossa **Uusi** &gt; **Raporttiryhmän määritys**. Voit vaihtoehtoisesti napsauttaa työkalurivillä **Raporttiryhmä**-painiketta ![Raporttiryhmä](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Raporttiryhmä").
3.  Valitse **Raporttiryhmä**-välilehti. Ohittaaksesi yksittäisiä raportin määrityksiä koskevat tiedot tätä raporttia luotaessa, valitse **Ohita yritys-, tiedot- ja päivä-määritykset yksittäisten raporttimääritysten** valintaruuduissa. Yrityksen nimi, tietojen taso, alustava asetus ja päivämäärätiedot täytetään automaattisesti, mutta voit tehdä päivityksiä.
4.  Jos haluat luoda useita raportointivaluutan näyttäviä raportteja, valitse **Sisällytä kaikki raportointivaluutat** -valintaruutu. Voit sitten käyttää useita näkymiä valitsemalla **Valuutta**-painikkeen verkkokatseluohjelmassa, kun katsot raporttia.
5.  Valitse raporttiryhmään sisällytettävät raportit valitsemalla **Ryhmän raportit** -kentässä **Lisää**. Jos haluat valita useita raportteja **Lisää**-valintaikkunassa, pidä Ctrl-näppäintä painettuna valitessasi raportteja. Kun olet valinnut raportit, valitse **OK**.
6.  Tallenna uusi raporttiryhmä valitsemalla **Tiedosto** &gt; **Tallenna**.

### <a name="modify-a-report-group"></a>Raporttiryhmän muokkaaminen

1.  Valitse Report Designerin siirtymisruudussa **Raporttiryhmät**.
2.  Kaksoisnapsauta muokattavaa raporttiryhmää.
3.  Tee tarvittavat muutokset **Raporttiryhmä**-välilehdessä.
4.  Tallenna muokattu raporttiryhmä valitsemalla **Tiedosto**-valikossa **Tallenna**. Vaihtoehtoisesti voi napsauttaa työkalurivillä **Tallenna**-painiketta ![Tallenna](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Tallenna").

**Huomautus:** Jos olet ajoittanut raporttien luonnin tapahtumaan tietyin väliajoin, voit ohittaa nämä asetukset ja luoda raportin heti.

### <a name="generate-a-report-group-report"></a>Raporttiryhmän raportin luonti

1.  Valitse Report Designerin siirtymisruudussa **Raporttiryhmät**.
2.  Avaa luotava raporttiryhmä.
3.  Luo raportteja napsauttamalla **Luo raportti** -painiketta ![Luo raportti](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Luo raportti").

### <a name="delete-a-report-group"></a>Raporttiryhmän poistaminen

1.  Valitse Report Designerin siirtymisruudussa **Raporttiryhmät**.
2.  Napsauta poistettavaa raporttiryhmää hiiren kakkospainikkeella ja valitse sitten **Poista**.
3.  Kun vahvistussanoma avautuu, valitse **Kyllä**.

## <a name="report-group-tab-controls"></a>Raporttiryhmä-välilehden ohjausobjektit
Seuraavassa taulukossa käsitellään **Raporttiryhmä**-välilehden ohjausobjekteja.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ohjausobjekti</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Yritys-, tiedot- ja päivä-määritysten ohittaminen yksittäisistä raporttimäärityksistä</td>
<td>Valitse tämä valintaruutu ohittaaksesi tähän raporttiryhmään kuuluvien raporttien yksittäiset raporttimääritykset vain näiden raporttien luonnissa.</td>
</tr>
<tr class="even">
<td>Yrityksen nimi</td>
<td>Valitse yritys, jota käytetään raporteissa.</td>
</tr>
<tr class="odd">
<td>Erittelytaso</td>
<td>Määritä raporttien yksityiskohtien taso.
<ul>
<li><strong>Taloushallinto</strong>− Korkean tason yhteenvetoraportti. Et voi porautua tileihin ja dimensioihin lukuun ottamatta niitä tilejä ja dimensioita, jotka on lisätty raportointipuun kautta.</li>
<li><strong>Rahoitus &amp; Tili</strong>− Raportti, joka sisältää korkean tason yhteenveto- ja tilitietoja.</li>
<li><strong>Rahoitus, Tili &amp; Tapahtuma</strong>− Raportti, joka sisältää korkean tason yhteenveto- ja tapahtumatietoja.</li>
</ul></td>
</tr>
<tr class="even">
<td>Alustava</td>
<td>Määritä raportteihin sisältyvät tehtävätyypit.
<ul>
<li><strong>Vain kirjatut tapahtumat</strong> – sisällytä vain ne tapahtumat ja saldot, jotka on kirjattu taloushallinnon tietoihin.</li>
<li><strong>Kirjatut ja kirjaamattomat tapahtumat</strong> – sisällytä kaikki taloushallinnon tietoihin merkityt ja kirjat tapahtumat ja saldot.</li>
<li><strong>Vain kirjaamattomat tapahtumat</strong> – sisällytä taloushallinnon tietoihin merkityt mutta vielä kirjaamattomat tapahtumat.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Sisällytetään kaikki raportointivaluutat</td>
<td>Mahdolliset Microsoft Dynamics ERP -järjestelmässä määritetyt lisäraportointivaluutat on lueteltu täällä. Valitsemalla tämän valintaruudun voit luoda lisäraportteja annetuissa valuutoissa. Voit tarkastella raportteja verkkokatseluohjelmassa napsauttamalla <strong>Valuutta</strong>-painiketta ja valitsemalla valuutan.</td>
</tr>
<tr class="even">
<td>Päivämäärätietoa ei ole tallennettu raportin määrityksiin</td>
<td><ul>
<li>Perusjakso</li>
<li>Perusvuosi</li>
<li>Raportin ajanjakso</li>
</ul>
Vain oletusarvoiset perusjaksoasetukset tallennetaan raportin määrityksiin.</td>
</tr>
<tr class="odd">
<td>Päivämäärätiedot on tallennettu raportin määrityksiin</td>
<td><ul>
<li>Raporttipäivämäärä</li>
<li>Oletusperuskausi</li>
</ul></td>
</tr>
<tr class="even">
<td>Raportit ryhmässä</td>
<td>Lisää, poista ja tilaa uudelleen raporttiryhmän raportteja.
<ul>
<li>Jos haluat lisätä raporttiryhmälle raporttimäärityksiä, avaa raporttiryhmä kaksoisnapsauttamalla sitä ja valitse sitten <strong>Lisää</strong>. Valitse raporttiryhmään sisällytettävät raportit ja valitse sitten <strong>OK</strong>.</li>
<li>Poista raportti raporttiryhmästä valitsemalla se ja napsauttamalla <strong>Poista</strong>.</li>
<li>Voit muokata raporttien luontijärjestystä valitsemalla ensin raportin luettelosta ja sitten <strong>Siirrä ylöspäin</strong> tai <strong>Siirrä alaspäin</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Lisätietoja
--------

[Taloushallinnan raportointi](financial-reporting-intro.md)




