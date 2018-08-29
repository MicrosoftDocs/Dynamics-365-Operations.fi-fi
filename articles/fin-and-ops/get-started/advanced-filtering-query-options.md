---
title: "Suodatuksen ja kyselyn lisäsyntaksi"
description: "Tässä ohjeaiheessa kuvataan suodatus- ja kyselyvaihtoehdot, jotka ovat käytettävissä, kun käytät Lisäsuodatus/-lajittelu-valintaikkunan **vastaavuus**operaattoria Suodatinruudussa tai ruudukon sarakkeen otsikkosuodattimissa."
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
ms.sourcegitcommit: edff2fba7e231ae52abf7828d55c1fe4841ccd7f
ms.openlocfilehash: 3e7127a9412dcf9324872c06fbf6cc3cf61bf063
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="a2a9d-103">Suodatuksen ja kyselysyntaksin lisäasetukset</span><span class="sxs-lookup"><span data-stu-id="a2a9d-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2a9d-104">Tässä ohjeaiheessa kuvataan suodatus- ja kyselyvaihtoehdot, jotka ovat käytettävissä, kun käytät Lisäsuodatus/-lajittelu-valintaikkunan **vastaavuus**operaattoria Suodatinruudussa tai ruudukon sarakkeen otsikkosuodattimissa.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-104">This article describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span> 

<a name="advanced-query-syntax"></a><span data-ttu-id="a2a9d-105">Kyselyn lisäsyntaksi</span><span class="sxs-lookup"><span data-stu-id="a2a9d-105">Advanced query syntax</span></span>
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
<th><span data-ttu-id="a2a9d-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="a2a9d-106">Syntax</span></span></th>
<th><span data-ttu-id="a2a9d-107">Selitys</span><span class="sxs-lookup"><span data-stu-id="a2a9d-107">Character description</span></span></th>
<th><span data-ttu-id="a2a9d-108">kuvaus</span><span class="sxs-lookup"><span data-stu-id="a2a9d-108">Description</span></span></th>
<th><span data-ttu-id="a2a9d-109">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="a2a9d-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a2a9d-110"><em>arvo</em></span><span class="sxs-lookup"><span data-stu-id="a2a9d-110"><em>value</em></span></span></td>
<td><span data-ttu-id="a2a9d-111">Yhtä suuri kuin syötettävä arvo</span><span class="sxs-lookup"><span data-stu-id="a2a9d-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="a2a9d-112">Kirjoita löydettävä arvo.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="a2a9d-113"><strong>Smith</strong> etsii merkkijonon &quot;Smith&quot;.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2a9d-114">!<em>arvo</em> (huutomerkki)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="a2a9d-115">Eri suuri kuin syötettävä arvo</span><span class="sxs-lookup"><span data-stu-id="a2a9d-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="a2a9d-116">Kirjoita huutomerkki ja sitten poisjätettävä arvo.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="a2a9d-117"><strong>!Smith</strong> etsii kaikki arvot paitsi arvon &quot;Smith&quot;.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a2a9d-118"><em>arvosta</em>..<em>arvoon</em> (kaksi pistettä)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="a2a9d-119">Etsii arvot, jotka ovat kahden pisteen erottamien arvojen välissä</span><span class="sxs-lookup"><span data-stu-id="a2a9d-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="a2a9d-120">Kirjoita lähtöarvo, kaksi pistettä ja loppuarvo.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="a2a9d-121"><strong>1..10</strong> löytää kaikki arvot yhdestä kymmeneen.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="a2a9d-122"><strong>A..C</strong> hakee kuitenkin merkkijonokentässä kaikki arvot, jotka alkavat merkillä &quot;A&quot; tai &quot;B&quot;, ja arvot, jotka vastaavat tarkasti arvoa &quot;C&quot;.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="a2a9d-123">Kysely ei löydä esimerkiksi arvoa Ca.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-123">For example, this query won&#39;t find &quot;Ca&quot;.</span></span> <span data-ttu-id="a2a9d-124">Jos haluat etsiä kaikki arvot väliltä &quot;A<em>&quot;–C&quot;</em>&quot;, kirjoita <strong>A..D</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2a9d-125">..<em>arvo</em> (kaksi pistettä)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="a2a9d-126">Etsii arvot, jotka ovat pienempiä tai yhtä suuria kuin syötetty arvo</span><span class="sxs-lookup"><span data-stu-id="a2a9d-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="a2a9d-127">Kirjoita kaksi pistettä ja sitten arvo.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="a2a9d-128"><strong>..1000</strong> etsii kaikki numerot, jotka ovat pienempiä tai yhtä suuria kuin 1 000, kuten &quot;100&quot;, &quot;999,95&quot; ja &quot;1 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a2a9d-129"><em>arvo</em>..</span><span class="sxs-lookup"><span data-stu-id="a2a9d-129"><em>value</em>..</span></span> <span data-ttu-id="a2a9d-130">(kaksi pistettä)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-130">(double period)</span></span></td>
<td><span data-ttu-id="a2a9d-131">Etsii arvot, jotka ovat suurempia tai yhtä suuria kuin syötetty arvo</span><span class="sxs-lookup"><span data-stu-id="a2a9d-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="a2a9d-132">Kirjoita arvo ja sitten kaksi pistettä.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="a2a9d-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="a2a9d-133"><strong>1000..</strong></span></span> <span data-ttu-id="a2a9d-134">etsii kaikki numerot, jotka ovat suurempia tai yhtä suuria kuin &quot;1 000&quot;, kuten &quot;1 000,01&quot; ja &quot;1 000 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2a9d-135">&gt;<em>arvo</em> (suurempi kuin -merkki)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="a2a9d-136">Etsii syötettyä arvoa suuremmat arvot</span><span class="sxs-lookup"><span data-stu-id="a2a9d-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="a2a9d-137">Kirjoita suurempi kuin -merkki (<strong>&gt;</strong>) ja sen jälkeen arvo.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="a2a9d-138"><strong>&gt;1000</strong> etsii kaikki numerot, jotka ovat suurempia kuin 1 000, kuten &quot;1 000,01&quot;, &quot;20 000&quot; ja &quot;1 000 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a2a9d-139">&lt;<em>arvo</em> (pienempi kuin -merkki)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="a2a9d-140">Etsii syötettyä arvoa pienemmät arvot</span><span class="sxs-lookup"><span data-stu-id="a2a9d-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="a2a9d-141">Kirjoita pienempi kuin -merkki (<strong>&lt;</strong>) ja sen jälkeen arvo.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="a2a9d-142"><strong>&lt;1000</strong> etsii kaikki numerot, jotka ovat pienempiä kuin 1 000, kuten &quot;999,99&quot;, &quot;1&quot; ja &quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2a9d-143"><em>arvo</em>\* (tähti)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="a2a9d-144">Alkaen syötetystä arvosta</span><span class="sxs-lookup"><span data-stu-id="a2a9d-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="a2a9d-145">Kirjoita alkuarvo ja sitten tähti (<strong><em></strong>).</span><span class="sxs-lookup"><span data-stu-id="a2a9d-145">Type the starting value and then an asterisk (<strong><em></strong>).</span></span></td>
<td><span data-ttu-id="a2a9d-146"><strong>S</em></strong> etsii kaikki S-kirjaimella alkavat merkkijonot, kuten Savonlinna, Sydney ja San Francisco.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-146"><strong>S</em></strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a2a9d-147"><em><em>arvo</em> (tähti)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-147"><em><em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="a2a9d-148">Päättyy syötettyyn arvoon</span><span class="sxs-lookup"><span data-stu-id="a2a9d-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="a2a9d-149">Kirjoita tähti ja sitten loppuarvo.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="a2a9d-150"><strong></em>\*nen</strong> etsii kaikki merkkijonot, joiden viimeiset kirjaimet ovat nen, kuten pohjoinen ja koillinen.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-150"><strong></em>east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2a9d-151"><em><em>arvo</em></em> (tähti)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-151"><em><em>value</em></em> (asterisk)</span></span></td>
<td><span data-ttu-id="a2a9d-152">Sisältää syötetyn arvon</span><span class="sxs-lookup"><span data-stu-id="a2a9d-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="a2a9d-153">Kirjoita tähti, sitten arvo ja sitten toinen tähti.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="a2a9d-154"><strong><em>ine</em></strong> etsii kaikki merkkijonot, jotka sisältävät arvon &quot;ine&quot;, kuten &quot;pohjoinen&quot; ja &quot;koillinen&quot;.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-154"><strong><em>th</em></strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a2a9d-155">?</span><span class="sxs-lookup"><span data-stu-id="a2a9d-155">?</span></span> <span data-ttu-id="a2a9d-156">(kysymysmerkki)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-156">(question mark)</span></span></td>
<td><span data-ttu-id="a2a9d-157">Merkkijonossa vähintään yksi tuntematon merkki.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="a2a9d-158">Kirjoita kysymysmerkki arvossa tuntemattomien merkkien kohdalle.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="a2a9d-159"><strong>Sa?ri</strong> etsii merkkijonot &quot;Saari&quot; ja &quot;Sauri&quot;.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2a9d-160"><em>arvo</em>,<em>arvo</em> (pilkku)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="a2a9d-161">Vastaa pilkulla erotettuja arvoja</span><span class="sxs-lookup"><span data-stu-id="a2a9d-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="a2a9d-162">Kirjoita kaikki ehdot pilkuilla erotettuina.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="a2a9d-163"><strong>A, D, F, G</strong> etsii ainoastaan arvot &quot;A&quot;, &quot;D&quot;, &quot;F&quot; ja &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="a2a9d-164"><strong>10, 20, 30, 100</strong> etsii ainoastaan arvot &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a2a9d-165">(<span class="code">SQL-lause</span>) (SQL-lause sulkeissa)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-165">(<span class="code">SQL statement</span>) (SQL statement between parentheses)</span></span></td>
<td><span data-ttu-id="a2a9d-166">Vastaa määritettyä kyselyä.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-166">Matching a defined query</span></span></td>
<td><span data-ttu-id="a2a9d-167">Kirjoita kysely SQL-lausekkeena sulkeiden sisälle.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-167">Type a query as an SQL statement between parentheses.</span></span></td>
<td><span data-ttu-id="a2a9d-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span><span class="sxs-lookup"><span data-stu-id="a2a9d-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2a9d-169">T</span><span class="sxs-lookup"><span data-stu-id="a2a9d-169">T</span></span></td>
<td><span data-ttu-id="a2a9d-170">Tämän päivän päivämäärä</span><span class="sxs-lookup"><span data-stu-id="a2a9d-170">Today&#39;s date</span></span></td>
<td><span data-ttu-id="a2a9d-171">Kirjoita <strong>T</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-171">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="a2a9d-172"><strong>T</strong> vastaa kuluvaa päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-172"><strong>T</strong> matches today&#39;s date.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a2a9d-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong>-metodi sulkeissa)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="a2a9d-174"><strong>SysQueryRangeUtil</strong>-metodin parametrien määrittämän arvon tai arvoalueen vastaavuus</span><span class="sxs-lookup"><span data-stu-id="a2a9d-174">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="a2a9d-175">Kirjoita <strong>SysQueryRangeUtil</strong>-metodi parametreilla, jotka määrittävät arvon tai arvoalueen.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-175">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td><ol>
<li><span data-ttu-id="a2a9d-176">Napsauta <strong>Myyntireskontra</strong> &gt; <strong>Laskut</strong> &gt; <strong>Avoimet asiakaslaskut</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-176">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="a2a9d-177">Avaa <strong>Kysely</strong>-sivu painamalla Ctrl+Vaihto+F3.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-177">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="a2a9d-178">Valitse <strong>Alue</strong>-välilehdessä <strong>Lisää</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-178">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="a2a9d-179">Valitse <strong>Taulu</strong>-kentästä <strong>Avoimet asiakastapahtumat</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-179">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="a2a9d-180">Valitse <strong>Kenttä</strong>-kentästä <strong>Eräpäivä</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-180">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="a2a9d-181">Kirjoita <strong>Ehdot</strong>-kenttään <strong>(yearRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-181">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="a2a9d-182">Napsauta <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-182">Click <strong>OK</strong>.</span></span> <span data-ttu-id="a2a9d-183">Luettelosivu päivittyy ja näyttää luettelon syöttämääsi ehtoa vastaavista laskuista.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-183">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="a2a9d-184">Tässä esimerkissä näkyvät edellisten kahden vuoden aikana erääntyneet laskut.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-184">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="a2a9d-185">Lisätietoja <strong>SysQueryRangeUtil</strong>-päivämäärämetodeista ja useita esimerkkejä on seuraavan osan taulussa.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-185">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="a2a9d-186">SysQueryRangeUtil-metodeja käyttävien päivämääräkyselyjen lisäasetukset</span><span class="sxs-lookup"><span data-stu-id="a2a9d-186">Advanced date queries that use SysQueryRangeUtil methods</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a2a9d-187">Tapa</span><span class="sxs-lookup"><span data-stu-id="a2a9d-187">Method</span></span></th>
<th><span data-ttu-id="a2a9d-188">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="a2a9d-188">Description</span></span></th>
<th><span data-ttu-id="a2a9d-189">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="a2a9d-189">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a2a9d-190">Päivä (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-190">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="a2a9d-191">Etsii päivämäärän suhteessa istunnon päivämäärään.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-191">Find a date relative to the session date.</span></span> <span data-ttu-id="a2a9d-192">Positiivisia arvoja ovat tulevat päivämäärät ja negatiivisia menneet päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-192">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td><ul>
<li><span data-ttu-id="a2a9d-193"><strong>Huomenna</strong> – kirjoita <strong>(Day(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-193"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="a2a9d-194"><strong>Tänään</strong> – kirjoita <strong>(Day(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-194"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="a2a9d-195"><strong>Eilen</strong> – kirjoita <strong>(Day(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-195"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2a9d-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="a2a9d-197">Etsii päivämääräalueen suhteessa istunnon päivämäärään.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-197">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="a2a9d-198">Positiivisia arvoja ovat tulevat päivämäärät ja negatiivisia menneet päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-198">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td><ul>
<li><span data-ttu-id="a2a9d-199"><strong>Edelliset 30 päivää</strong> – kirjoita <strong>(DayRange(-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-199"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="a2a9d-200"><strong>Edelliset ja seuraavat 30 päivää</strong> – kirjoita <strong>(DayRange(-30,30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-200"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a2a9d-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="a2a9d-202">Etsii kaikki määritetyn suhteellisen päivämäärän jälkeiset päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-202">Find all dates after the specified relative date.</span></span></td>
<td><ul>
<li><span data-ttu-id="a2a9d-203"><strong>Yli 30 päivän kuluttua tästä päivästä</strong> – kirjoita <strong>(GreaterThanDate(30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-203"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2a9d-204">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="a2a9d-204">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="a2a9d-205">Etsii kaikki kuluvan ajan jälkeiset päivämäärä- ja aikamerkinnät.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-205">Find all date/time entries after the current time.</span></span></td>
<td><ul>
<li><span data-ttu-id="a2a9d-206"><strong>Kaikki tulevat päivämäärät/ajat</strong> – kirjoita <strong>(GreaterThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-206"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a2a9d-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="a2a9d-208">Etsii kaikki määritettyä suhteellista päivämäärää edeltävät päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-208">Find all dates before the specified relative date.</span></span></td>
<td><ul>
<li><span data-ttu-id="a2a9d-209"><strong>Alle seitsemän päivää tästä päivästä</strong> – kirjoita <strong>(LessThanDate(7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-209"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2a9d-210">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="a2a9d-210">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="a2a9d-211">Etsii kaikki kuluvaa aikaa edeltävät päivämäärä- ja aikamerkinnät.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-211">Find all date/time entries before the current time.</span></span></td>
<td><ul>
<li><span data-ttu-id="a2a9d-212"><strong>Kaikki aiemmat päivämäärät/-ajat</strong> – kirjoita <strong>(LessThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-212"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a2a9d-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="a2a9d-214">Etsii päivämäärävälin kuukausien perusteella suhteessa kuluvaan kuukauteen.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-214">Find a range of dates, based on months relative to the current month.</span></span></td>
<td><ul>
<li><span data-ttu-id="a2a9d-215"><strong>Edelliset kaksi kuukautta</strong> – kirjoita <strong>(MonthRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-215"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="a2a9d-216"><strong>Seuraavat kolme kuukautta</strong> – kirjoita <strong>(MonthRange(0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-216"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2a9d-217">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="a2a9d-217">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="a2a9d-218">Etsii päivämäärävälin vuosien perusteella suhteessa kuluvaan vuoteen.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-218">Find a range of dates, based on years relative to the current year.</span></span></td>
<td><ul>
<li><span data-ttu-id="a2a9d-219"><strong>Seuraava vuosi</strong> – kirjoita <strong>(YearRange(0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-219"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="a2a9d-220"><strong>Edellinen vuosi</strong> – kirjoita <strong>(YearRange(-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2a9d-220"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






