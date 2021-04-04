---
title: Suodatuksen ja kyselysyntaksin lisäasetukset
description: Tässä ohjeaiheessa kuvataan suodatus- ja kyselyvaihtoehdot, jotka ovat käytettävissä, kun käytät Lisäsuodatus/-lajittelu-valintaikkunan vastaavuusoperaattoria Suodatinruudussa tai ruudukon sarakkeen otsikkosuodattimissa.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15805e24c46603afd34d40c5f94c1422b01cab4c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566063"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="5072d-103">Suodatuksen ja kyselysyntaksin lisäasetukset</span><span class="sxs-lookup"><span data-stu-id="5072d-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5072d-104">Tässä ohjeaiheessa kuvataan suodatus- ja kyselyvaihtoehdot, jotka ovat käytettävissä, kun käytät Lisäsuodatus/-lajittelu-valintaikkunan **vastaavuusoperaattoria** Suodatinruudussa tai ruudukon sarakkeen otsikkosuodattimissa.</span><span class="sxs-lookup"><span data-stu-id="5072d-104">This topic describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="5072d-105">Kyselyn lisäsyntaksi</span><span class="sxs-lookup"><span data-stu-id="5072d-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5072d-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="5072d-106">Syntax</span></span></th>
<th><span data-ttu-id="5072d-107">Selitys</span><span class="sxs-lookup"><span data-stu-id="5072d-107">Character description</span></span></th>
<th><span data-ttu-id="5072d-108">kuvaus</span><span class="sxs-lookup"><span data-stu-id="5072d-108">Description</span></span></th>
<th><span data-ttu-id="5072d-109">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="5072d-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5072d-110"><em>arvo</em></span><span class="sxs-lookup"><span data-stu-id="5072d-110"><em>value</em></span></span></td>
<td><span data-ttu-id="5072d-111">Yhtä suuri kuin syötettävä arvo</span><span class="sxs-lookup"><span data-stu-id="5072d-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="5072d-112">Kirjoita löydettävä arvo.</span><span class="sxs-lookup"><span data-stu-id="5072d-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="5072d-113"><strong>Smith</strong> etsii merkkijonon &quot;Smith&quot;.</span><span class="sxs-lookup"><span data-stu-id="5072d-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5072d-114">!<em>arvo</em> (huutomerkki)</span><span class="sxs-lookup"><span data-stu-id="5072d-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="5072d-115">Eri suuri kuin syötettävä arvo</span><span class="sxs-lookup"><span data-stu-id="5072d-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="5072d-116">Kirjoita huutomerkki ja sitten poisjätettävä arvo.</span><span class="sxs-lookup"><span data-stu-id="5072d-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="5072d-117"><strong>!Smith</strong> etsii kaikki arvot paitsi arvon &quot;Smith&quot;.</span><span class="sxs-lookup"><span data-stu-id="5072d-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5072d-118"><em>arvosta</em>..<em>arvoon</em> (kaksi pistettä)</span><span class="sxs-lookup"><span data-stu-id="5072d-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="5072d-119">Etsii arvot, jotka ovat kahden pisteen erottamien arvojen välissä</span><span class="sxs-lookup"><span data-stu-id="5072d-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="5072d-120">Kirjoita lähtöarvo, kaksi pistettä ja loppuarvo.</span><span class="sxs-lookup"><span data-stu-id="5072d-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="5072d-121"><strong>1..10</strong> löytää kaikki arvot yhdestä kymmeneen.</span><span class="sxs-lookup"><span data-stu-id="5072d-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="5072d-122"><strong>A..C</strong> hakee kuitenkin merkkijonokentässä kaikki arvot, jotka alkavat merkillä &quot;A&quot; tai &quot;B&quot;, ja arvot, jotka vastaavat tarkasti arvoa &quot;C&quot;.</span><span class="sxs-lookup"><span data-stu-id="5072d-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="5072d-123">Kysely ei löydä esimerkiksi arvoa &quot;Caa&quot;.</span><span class="sxs-lookup"><span data-stu-id="5072d-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="5072d-124">Jos haluat etsiä kaikki arvot väliltä &quot;A<em>&quot;–C&quot;</em>&quot;, kirjoita <strong>A..D</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5072d-125">..<em>arvo</em> (kaksi pistettä)</span><span class="sxs-lookup"><span data-stu-id="5072d-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="5072d-126">Etsii arvot, jotka ovat pienempiä tai yhtä suuria kuin syötetty arvo</span><span class="sxs-lookup"><span data-stu-id="5072d-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="5072d-127">Kirjoita kaksi pistettä ja sitten arvo.</span><span class="sxs-lookup"><span data-stu-id="5072d-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="5072d-128"><strong>..1000</strong> etsii kaikki numerot, jotka ovat pienempiä tai yhtä suuria kuin 1 000, kuten &quot;100&quot;, &quot;999,95&quot; ja &quot;1 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="5072d-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5072d-129"><em>arvo</em>..</span><span class="sxs-lookup"><span data-stu-id="5072d-129"><em>value</em>..</span></span> <span data-ttu-id="5072d-130">(kaksi pistettä)</span><span class="sxs-lookup"><span data-stu-id="5072d-130">(double period)</span></span></td>
<td><span data-ttu-id="5072d-131">Etsii arvot, jotka ovat suurempia tai yhtä suuria kuin syötetty arvo</span><span class="sxs-lookup"><span data-stu-id="5072d-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="5072d-132">Kirjoita arvo ja sitten kaksi pistettä.</span><span class="sxs-lookup"><span data-stu-id="5072d-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="5072d-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="5072d-133"><strong>1000..</strong></span></span> <span data-ttu-id="5072d-134">etsii kaikki numerot, jotka ovat suurempia tai yhtä suuria kuin &quot;1 000&quot;, kuten &quot;1 000,01&quot; ja &quot;1 000 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="5072d-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5072d-135">&gt;<em>arvo</em> (suurempi kuin -merkki)</span><span class="sxs-lookup"><span data-stu-id="5072d-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="5072d-136">Etsii syötettyä arvoa suuremmat arvot</span><span class="sxs-lookup"><span data-stu-id="5072d-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="5072d-137">Kirjoita suurempi kuin -merkki (<strong>&gt;</strong>) ja sen jälkeen arvo.</span><span class="sxs-lookup"><span data-stu-id="5072d-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="5072d-138"><strong>&gt;1000</strong> etsii kaikki numerot, jotka ovat suurempia kuin 1 000, kuten &quot;1 000,01&quot;, &quot;20 000&quot; ja &quot;1 000 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="5072d-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5072d-139">&lt;<em>arvo</em> (pienempi kuin -merkki)</span><span class="sxs-lookup"><span data-stu-id="5072d-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="5072d-140">Etsii syötettyä arvoa pienemmät arvot</span><span class="sxs-lookup"><span data-stu-id="5072d-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="5072d-141">Kirjoita pienempi kuin -merkki (<strong>&lt;</strong>) ja sen jälkeen arvo.</span><span class="sxs-lookup"><span data-stu-id="5072d-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="5072d-142"><strong>&lt;1000</strong> etsii kaikki numerot, jotka ovat pienempiä kuin 1 000, kuten &quot;999,99&quot;, &quot;1&quot; ja &quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="5072d-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5072d-143"><em>arvo</em>\* (tähti)</span><span class="sxs-lookup"><span data-stu-id="5072d-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="5072d-144">Alkaen syötetystä arvosta</span><span class="sxs-lookup"><span data-stu-id="5072d-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="5072d-145">Kirjoita alkuarvo ja sitten tähti (<strong>\*</strong>).</span><span class="sxs-lookup"><span data-stu-id="5072d-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="5072d-146"><strong>S\*</strong> etsii kaikki &quot;S&quot;-kirjaimella alkavat merkkijonot, kuten &quot;Savonlinna&quot;, &quot;Sydney&quot; ja &quot;San Francisco&quot;.</span><span class="sxs-lookup"><span data-stu-id="5072d-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5072d-147">\*<em>arvo</em> (tähti)</span><span class="sxs-lookup"><span data-stu-id="5072d-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="5072d-148">Päättyy syötettyyn arvoon</span><span class="sxs-lookup"><span data-stu-id="5072d-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="5072d-149">Kirjoita tähti ja sitten loppuarvo.</span><span class="sxs-lookup"><span data-stu-id="5072d-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="5072d-150"><strong>\*nen</strong> etsii kaikki merkkijonot, joiden viimeiset kirjaimet ovat &quot;nen&quot;, kuten &quot;pohjoinen&quot; ja &quot;koillinen&quot;.</span><span class="sxs-lookup"><span data-stu-id="5072d-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5072d-151">*<em>arvo</em>* (tähti)</span><span class="sxs-lookup"><span data-stu-id="5072d-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="5072d-152">Sisältää syötetyn arvon</span><span class="sxs-lookup"><span data-stu-id="5072d-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="5072d-153">Kirjoita tähti, sitten arvo ja sitten toinen tähti.</span><span class="sxs-lookup"><span data-stu-id="5072d-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="5072d-154"><strong>*ine*</strong> etsii kaikki merkkijonot, jotka sisältävät arvon &quot;ine&quot;, kuten &quot;pohjoinen&quot; ja &quot;koillinen&quot;.</span><span class="sxs-lookup"><span data-stu-id="5072d-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5072d-155">?</span><span class="sxs-lookup"><span data-stu-id="5072d-155">?</span></span> <span data-ttu-id="5072d-156">(kysymysmerkki)</span><span class="sxs-lookup"><span data-stu-id="5072d-156">(question mark)</span></span></td>
<td><span data-ttu-id="5072d-157">Merkkijonossa vähintään yksi tuntematon merkki.</span><span class="sxs-lookup"><span data-stu-id="5072d-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="5072d-158">Kirjoita kysymysmerkki arvossa tuntemattomien merkkien kohdalle.</span><span class="sxs-lookup"><span data-stu-id="5072d-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="5072d-159"><strong>Sa?ri</strong> etsii merkkijonot &quot;Saari&quot; ja &quot;Sauri&quot;.</span><span class="sxs-lookup"><span data-stu-id="5072d-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5072d-160"><em>arvo</em>,<em>arvo</em> (pilkku)</span><span class="sxs-lookup"><span data-stu-id="5072d-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="5072d-161">Vastaa pilkulla erotettuja arvoja</span><span class="sxs-lookup"><span data-stu-id="5072d-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="5072d-162">Kirjoita kaikki ehdot pilkuilla erotettuina.</span><span class="sxs-lookup"><span data-stu-id="5072d-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="5072d-163"><strong>A, D, F, G</strong> etsii ainoastaan arvot &quot;A&quot;, &quot;D&quot;, &quot;F&quot; ja &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="5072d-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="5072d-164"><strong>10, 20, 30, 100</strong> etsii ainoastaan arvot &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="5072d-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5072d-165">"" (kaksi lainausmerkkiä)</span><span class="sxs-lookup"><span data-stu-id="5072d-165">"" (two double quotes)</span></span></td>
<td><span data-ttu-id="5072d-166">Tyhjän arvon täsmäytys</span><span class="sxs-lookup"><span data-stu-id="5072d-166">Matching a blank value</span></span></td>
<td><span data-ttu-id="5072d-167">Voit suodattaa kentän tyhjät arvot syöttämällä kaksi peräkkäistä lainausmerkkiä.</span><span class="sxs-lookup"><span data-stu-id="5072d-167">Type two consecutive double quotes to filter for blank values in that field.</span></span></td>
<td><span data-ttu-id="5072d-168">Kaksi peräkkäistä lainausmerkkiä<strong>("</strong>") etsii rivejä, joilla ei ole arvoa nykyiselle sarakkeelle.</span><span class="sxs-lookup"><span data-stu-id="5072d-168">Two consecutive double quotes (<strong>""</strong>) finds rows with no value for the current column.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5072d-169">(<span class="code">Finance and Operations -kysely</span>) (Finance and Operations -kysely sulkeissa)</span><span class="sxs-lookup"><span data-stu-id="5072d-169">(<span class="code">Finance and Operations query</span>) (Finance and Operations query between parentheses)</span></span></td>
<td><span data-ttu-id="5072d-170">Vastaa määritettyä kyselyä.</span><span class="sxs-lookup"><span data-stu-id="5072d-170">Matching a defined query</span></span></td>
<td><span data-ttu-id="5072d-171">Kirjoita kysely SQL-lausekkeena sulkuihin käyttämällä Finance and Operations -kyselykieltä.</span><span class="sxs-lookup"><span data-stu-id="5072d-171">Type a query as an SQL statement between parentheses using the Finance and Operations query language.</span></span></td>
  <td><span data-ttu-id="5072d-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span><span class="sxs-lookup"><span data-stu-id="5072d-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span></span><br><br> 
       <span data-ttu-id="5072d-173">esimerkki syntakstista suodatusehdolle kentässä juuritietolähteestä sekä toisen tietolähteen kentästä (Kaikki asiakkaat -sivulle)</span><span class="sxs-lookup"><span data-stu-id="5072d-173">as an example of syntax for a filter condition on a field from the root datasource as well as a field from a different datasource (for the All customers page)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5072d-174">T</span><span class="sxs-lookup"><span data-stu-id="5072d-174">T</span></span></td>
<td><span data-ttu-id="5072d-175">Tämän päivän päivämäärä</span><span class="sxs-lookup"><span data-stu-id="5072d-175">Today's date</span></span></td>
<td><span data-ttu-id="5072d-176">Kirjoita <strong>T</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-176">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="5072d-177"><strong>T</strong> vastaa kuluvaa päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="5072d-177"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5072d-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong>-metodi sulkeissa)</span><span class="sxs-lookup"><span data-stu-id="5072d-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="5072d-179"><strong>SysQueryRangeUtil</strong>-metodin parametrien määrittämän arvon tai arvoalueen vastaavuus</span><span class="sxs-lookup"><span data-stu-id="5072d-179">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="5072d-180">Kirjoita <strong>SysQueryRangeUtil</strong>-metodi parametreilla, jotka määrittävät arvon tai arvoalueen.</span><span class="sxs-lookup"><span data-stu-id="5072d-180">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="5072d-181">Napsauta <strong>Myyntireskontra</strong> &gt; <strong>Laskut</strong> &gt; <strong>Avoimet asiakaslaskut</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-181">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="5072d-182">Avaa <strong>Kysely</strong>-sivu painamalla Ctrl+Vaihto+F3.</span><span class="sxs-lookup"><span data-stu-id="5072d-182">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="5072d-183">Valitse <strong>Alue</strong>-välilehdessä <strong>Lisää</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-183">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="5072d-184">Valitse <strong>Taulu</strong>-kentästä <strong>Avoimet asiakastapahtumat</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-184">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="5072d-185">Valitse <strong>Kenttä</strong>-kentästä <strong>Eräpäivä</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-185">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="5072d-186">Kirjoita <strong>Ehdot</strong>-kenttään <strong>(yearRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-186">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="5072d-187">Napsauta <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-187">Click <strong>OK</strong>.</span></span> <span data-ttu-id="5072d-188">Luettelosivu päivittyy ja näyttää luettelon syöttämääsi ehtoa vastaavista laskuista.</span><span class="sxs-lookup"><span data-stu-id="5072d-188">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="5072d-189">Tässä esimerkissä näkyvät edellisten kahden vuoden aikana erääntyneet laskut.</span><span class="sxs-lookup"><span data-stu-id="5072d-189">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="5072d-190">Lisätietoja <strong>SysQueryRangeUtil</strong>-päivämäärämetodeista ja useita esimerkkejä on seuraavan osan taulussa.</span><span class="sxs-lookup"><span data-stu-id="5072d-190">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="5072d-191">SysQueryRangeUtil-metodeja käyttävien päivämääräkyselyjen lisäasetukset</span><span class="sxs-lookup"><span data-stu-id="5072d-191">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5072d-192">Tapa</span><span class="sxs-lookup"><span data-stu-id="5072d-192">Method</span></span></th>
<th><span data-ttu-id="5072d-193">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="5072d-193">Description</span></span></th>
<th><span data-ttu-id="5072d-194">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="5072d-194">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5072d-195">Päivä (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="5072d-195">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="5072d-196">Etsii päivämäärän suhteessa istunnon päivämäärään.</span><span class="sxs-lookup"><span data-stu-id="5072d-196">Find a date relative to the session date.</span></span> <span data-ttu-id="5072d-197">Positiivisia arvoja ovat tulevat päivämäärät ja negatiivisia menneet päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="5072d-197">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="5072d-198"><strong>Huomenna</strong> – kirjoita <strong>(Day(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-198"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="5072d-199"><strong>Tänään</strong> – kirjoita <strong>(Day(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-199"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="5072d-200"><strong>Eilen</strong> – kirjoita <strong>(Day(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-200"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="5072d-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="5072d-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="5072d-202">Etsii päivämääräalueen suhteessa istunnon päivämäärään.</span><span class="sxs-lookup"><span data-stu-id="5072d-202">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="5072d-203">Positiivisia arvoja ovat tulevat päivämäärät ja negatiivisia menneet päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="5072d-203">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="5072d-204"><strong>Edelliset 30 päivää</strong> – kirjoita <strong>(DayRange(-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-204"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="5072d-205"><strong>Edelliset ja seuraavat 30 päivää</strong> – kirjoita <strong>(DayRange(-30,30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-205"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="5072d-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="5072d-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="5072d-207">Etsii kaikki määritetyn suhteellisen päivämäärän jälkeiset päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="5072d-207">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="5072d-208"><strong>Yli 30 päivän kuluttua tästä päivästä</strong> – kirjoita <strong>(GreaterThanDate(30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-208"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="5072d-209">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="5072d-209">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="5072d-210">Etsii kaikki kuluvan ajan jälkeiset päivämäärä- ja aikamerkinnät.</span><span class="sxs-lookup"><span data-stu-id="5072d-210">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="5072d-211"><strong>Kaikki tulevat päivämäärät/ajat</strong> – kirjoita <strong>(GreaterThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-211"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="5072d-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="5072d-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="5072d-213">Etsii kaikki määritettyä suhteellista päivämäärää edeltävät päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="5072d-213">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="5072d-214"><strong>Alle seitsemän päivää tästä päivästä</strong> – kirjoita <strong>(LessThanDate(7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-214"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="5072d-215">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="5072d-215">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="5072d-216">Etsii kaikki kuluvaa aikaa edeltävät päivämäärä- ja aikamerkinnät.</span><span class="sxs-lookup"><span data-stu-id="5072d-216">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="5072d-217"><strong>Kaikki aiemmat päivämäärät/-ajat</strong> – kirjoita <strong>(LessThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-217"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="5072d-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="5072d-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="5072d-219">Etsii päivämäärävälin kuukausien perusteella suhteessa kuluvaan kuukauteen.</span><span class="sxs-lookup"><span data-stu-id="5072d-219">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="5072d-220"><strong>Edelliset kaksi kuukautta</strong> – kirjoita <strong>(MonthRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-220"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="5072d-221"><strong>Seuraavat kolme kuukautta</strong> – kirjoita <strong>(MonthRange(0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-221"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="5072d-222">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="5072d-222">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="5072d-223">Etsii päivämäärävälin vuosien perusteella suhteessa kuluvaan vuoteen.</span><span class="sxs-lookup"><span data-stu-id="5072d-223">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="5072d-224"><strong>Seuraava vuosi</strong> – kirjoita <strong>(YearRange(0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-224"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="5072d-225"><strong>Edellinen vuosi</strong> – kirjoita <strong>(YearRange(-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="5072d-225"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]