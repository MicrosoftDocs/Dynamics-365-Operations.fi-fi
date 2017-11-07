---
title: "Suodatuksen ja kyselyn lisäsyntaksi"
description: "Tässä artikkelissa on kuvattu suodatus- ja kyselyvaihtoehtoja, jotka ovat käytettävissä, kun käytät Lisäsuodatus/-lajittelu-valintaikkunan \"vastaa kohdetta\" -operaattoria."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 616366009ce7bf7135704e980becc331617cf5af
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="advanced-filtering-and-query-syntax"></a>Suodatuksen ja kyselyn lisäsyntaksi

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on kuvattu suodatus- ja kyselyvaihtoehtoja, jotka ovat käytettävissä, kun käytät Lisäsuodatus/-lajittelu-valintaikkunan "vastaa kohdetta" -operaattoria.

<a name="advanced-query-syntax"></a>Kyselyn lisäsyntaksi
---------------------

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Syntaksi</th>
<th>Selitys</th>
<th>kuvaus</th>
<th>Esimerkki</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>arvo</em></td>
<td>Yhtä suuri kuin syötettävä arvo</td>
<td>Kirjoita löydettävä arvo.</td>
<td><strong>Smith</strong> etsii merkkijonon &quot;Smith&quot;.</td>
</tr>
<tr class="even">
<td>!<em>arvo</em> (huutomerkki)</td>
<td>Eri suuri kuin syötettävä arvo</td>
<td>Kirjoita huutomerkki ja sitten poisjätettävä arvo.</td>
<td><strong>!Smith</strong> etsii kaikki arvot paitsi arvon &quot;Smith&quot;.</td>
</tr>
<tr class="odd">
<td><em>arvosta</em>..<em>arvoon</em> (kaksi pistettä)</td>
<td>Etsii arvot, jotka ovat kahden pisteen erottamien arvojen välissä</td>
<td>Kirjoita lähtöarvo, kaksi pistettä ja loppuarvo.</td>
<td><strong>1..10</strong> löytää kaikki arvot yhdestä kymmeneen. <strong>A..C</strong> hakee kuitenkin merkkijonokentässä kaikki arvot, jotka alkavat merkillä &quot;A&quot; tai &quot;B&quot;, ja arvot, jotka vastaavat tarkasti arvoa &quot;C&quot;. Kysely ei löydä esimerkiksi arvoa &quot;Caa&quot;. Jos haluat etsiä kaikki arvot väliltä &quot;A*&quot;–C&quot;*&quot;, kirjoita <strong>A..D</strong>.</td>
</tr>
<tr class="even">
<td>..<em>arvo</em> (kaksi pistettä)</td>
<td>Etsii arvot, jotka ovat pienempiä tai yhtä suuria kuin syötetty arvo</td>
<td>Kirjoita kaksi pistettä ja sitten arvo.</td>
<td><strong>..1000</strong> etsii kaikki numerot, jotka ovat pienempiä tai yhtä suuria kuin 1 000, kuten &quot;100&quot;, &quot;999,95&quot; ja &quot;1 000&quot;.</td>
</tr>
<tr class="odd">
<td><em>arvo</em>.. (kaksi pistettä)</td>
<td>Etsii arvot, jotka ovat suurempia tai yhtä suuria kuin syötetty arvo</td>
<td>Kirjoita arvo ja sitten kaksi pistettä.</td>
<td><strong>1000..</strong> etsii kaikki numerot, jotka ovat suurempia tai yhtä suuria kuin &quot;1 000&quot;, kuten &quot;1 000,01&quot; ja &quot;1 000 000&quot;.</td>
</tr>
<tr class="even">
<td>&gt;<em>arvo</em> (suurempi kuin -merkki)</td>
<td>Etsii syötettyä arvoa suuremmat arvot</td>
<td>Kirjoita suurempi kuin -merkki (<strong>&gt;</strong>) ja sen jälkeen arvo.</td>
<td><strong>&gt;1000</strong> etsii kaikki numerot, jotka ovat suurempia kuin 1 000, kuten &quot;1 000,01&quot;, &quot;20 000&quot; ja &quot;1 000 000&quot;.</td>
</tr>
<tr class="odd">
<td>&lt;<em>arvo</em> (pienempi kuin -merkki)</td>
<td>Etsii syötettyä arvoa pienemmät arvot</td>
<td>Kirjoita pienempi kuin -merkki (<strong>&lt;</strong>) ja sen jälkeen arvo.</td>
<td><strong>&lt;1000</strong> etsii kaikki numerot, jotka ovat pienempiä kuin 1 000, kuten &quot;999,99&quot;, &quot;1&quot; ja &quot;-200&quot;.</td>
</tr>
<tr class="even">
<td><em>arvo</em>* (tähti)</td>
<td>Alkaen syötetystä arvosta</td>
<td>Kirjoita alkuarvo ja sitten tähti (<strong>*</strong>).</td>
<td><strong>S*</strong> etsii kaikki &quot;S&quot;-kirjaimella alkavat merkkijonot, kuten &quot;Savonlinna&quot;, &quot;Sydney&quot; ja &quot;San Francisco&quot;.</td>
</tr>
<tr class="odd">
<td>*<em>arvo</em> (tähti)</td>
<td>Päättyy syötettyyn arvoon</td>
<td>Kirjoita tähti ja sitten loppuarvo.</td>
<td><strong>*nen</strong> etsii kaikki merkkijonot, joiden viimeiset kirjaimet ovat &quot;nen&quot;, kuten &quot;pohjoinen&quot; ja &quot;koillinen&quot;.</td>
</tr>
<tr class="even">
<td>*<em>arvo</em>* (tähti)</td>
<td>Sisältää syötetyn arvon</td>
<td>Kirjoita tähti, sitten arvo ja sitten toinen tähti.</td>
<td><strong>*ine*</strong> etsii kaikki merkkijonot, jotka sisältävät arvon &quot;ine&quot;, kuten &quot;pohjoinen&quot; ja &quot;koillinen&quot;.</td>
</tr>
<tr class="odd">
<td>? (kysymysmerkki)</td>
<td>Merkkijonossa vähintään yksi tuntematon merkki.</td>
<td>Kirjoita kysymysmerkki arvossa tuntemattomien merkkien kohdalle.</td>
<td><strong>Sa?ri</strong> etsii merkkijonot &quot;Saari&quot; ja &quot;Sauri&quot;.</td>
</tr>
<tr class="even">
<td><em>arvo</em>,<em>arvo</em> (pilkku)</td>
<td>Vastaa pilkulla erotettuja arvoja</td>
<td>Kirjoita kaikki ehdot pilkuilla erotettuina.</td>
<td><strong>A, D, F, G</strong> etsii ainoastaan arvot &quot;A&quot;, &quot;D&quot;, &quot;F&quot; ja &quot;G&quot;. <strong>10, 20, 30, 100</strong> etsii ainoastaan arvot &quot;10, 20, 30, 100&quot;.</td>
</tr>
<tr class="odd">
<td>(<span class="code">SQL-lause</span>) (SQL-lause sulkeissa)</td>
<td>Vastaa määritettyä kyselyä.</td>
<td>Kirjoita kysely SQL-lausekkeena sulkeiden sisälle.</td>
<td><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></td>
</tr>
<tr class="even">
<td>T</td>
<td>Tämän päivän päivämäärä</td>
<td>Kirjoita <strong>T</strong>.</td>
<td><strong>T</strong> vastaa kuluvaa päivämäärää.</td>
</tr>
<tr class="odd">
<td>(methodName(parameters)) (<strong>SysQueryRangeUtil</strong>-metodi sulkeissa)</td>
<td><strong>SysQueryRangeUtil</strong>-metodin parametrien määrittämän arvon tai arvoalueen vastaavuus</td>
<td>Kirjoita <strong>SysQueryRangeUtil</strong>-metodi parametreilla, jotka määrittävät arvon tai arvoalueen.</td>
<td><ol>
<li>Napsauta <strong>Myyntireskontra</strong> &gt; <strong>Laskut</strong> &gt; <strong>Avoimet asiakaslaskut</strong>.</li>
<li>Avaa <strong>Kysely</strong>-sivu painamalla Ctrl+Vaihto+F3.</li>
<li>Valitse <strong>Alue</strong>-välilehdessä <strong>Lisää</strong>.</li>
<li>Valitse <strong>Taulu</strong>-kentästä <strong>Avoimet asiakastapahtumat</strong>.</li>
<li>Valitse <strong>Kenttä</strong>-kentästä <strong>Eräpäivä</strong>.</li>
<li>Kirjoita <strong>Ehdot</strong>-kenttään <strong>(yearRange(-2,0))</strong>.</li>
<li>Napsauta <strong>OK</strong>. Luettelosivu päivittyy ja näyttää luettelon syöttämääsi ehtoa vastaavista laskuista. Tässä esimerkissä näkyvät edellisten kahden vuoden aikana erääntyneet laskut.</li>
</ol>
Lisätietoja <strong>SysQueryRangeUtil</strong>-päivämäärämetodeista ja useita esimerkkejä on seuraavan osan taulussa.</td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>SysQueryRangeUtil-metodeja käyttävien päivämääräkyselyjen lisäasetukset
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tapa</th>
<th>Kuvaus</th>
<th>Esimerkki</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Päivä (_relativeDays=0)</td>
<td>Etsii päivämäärän suhteessa istunnon päivämäärään. Positiivisia arvoja ovat tulevat päivämäärät ja negatiivisia menneet päivämäärät.</td>
<td><ul>
<li><strong>Huomenna</strong> – kirjoita <strong>(Day(1))</strong>.</li>
<li><strong>Tänään</strong> – kirjoita <strong>(Day(0))</strong>.</li>
<li><strong>Eilen</strong> – kirjoita <strong>(Day(-1))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>Etsii päivämääräalueen suhteessa istunnon päivämäärään. Positiivisia arvoja ovat tulevat päivämäärät ja negatiivisia menneet päivämäärät.</td>
<td><ul>
<li><strong>Edelliset 30 päivää</strong> – kirjoita <strong>(DayRange(-30,0))</strong>.</li>
<li><strong>Edelliset ja seuraavat 30 päivää</strong> – kirjoita <strong>(DayRange(-30,30))</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>Etsii kaikki määritetyn suhteellisen päivämäärän jälkeiset päivämäärät.</td>
<td><ul>
<li><strong>Yli 30 päivän kuluttua tästä päivästä</strong> – kirjoita <strong>(GreaterThanDate(30))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>GreaterThanUtcNow ()</td>
<td>Etsii kaikki kuluvan ajan jälkeiset päivämäärä- ja aikamerkinnät.</td>
<td><ul>
<li><strong>Kaikki tulevat päivämäärät/ajat</strong> – kirjoita <strong>(GreaterThanUtcNow())</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>Etsii kaikki määritettyä suhteellista päivämäärää edeltävät päivämäärät.</td>
<td><ul>
<li><strong>Alle seitsemän päivää tästä päivästä</strong> – kirjoita <strong>(LessThanDate(7))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>LessThanUtcNow ()</td>
<td>Etsii kaikki kuluvaa aikaa edeltävät päivämäärä- ja aikamerkinnät.</td>
<td><ul>
<li><strong>Kaikki aiemmat päivämäärät/-ajat</strong> – kirjoita <strong>(LessThanUtcNow())</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Etsii päivämäärävälin kuukausien perusteella suhteessa kuluvaan kuukauteen.</td>
<td><ul>
<li><strong>Edelliset kaksi kuukautta</strong> – kirjoita <strong>(MonthRange(-2,0))</strong>.</li>
<li><strong>Seuraavat kolme kuukautta</strong> – kirjoita <strong>(MonthRange(0,3))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Etsii päivämäärävälin vuosien perusteella suhteessa kuluvaan vuoteen.</td>
<td><ul>
<li><strong>Seuraava vuosi</strong> – kirjoita <strong>(YearRange(0, 1))</strong>.</li>
<li><strong>Edellinen vuosi</strong> – kirjoita <strong>(YearRange(-1,0))</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>






