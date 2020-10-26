---
title: Myyntireskontran erääntymisraportti
description: Myyntireskontran erääntymisraportissa näkyy asiakkaiden erääntymissaldot päivämäärävälin tai erääntymiskauden mukaan lajiteltuna.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 062e8972c879d770cc4106c2811cd4c16fff0446
ms.sourcegitcommit: 25909c6ad3616e4f75a2fe006057dda18d7cc856
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974858"
---
# <a name="customer-aging-report"></a><span data-ttu-id="ff5e5-103">Myyntireskontran erääntymisraportti</span><span class="sxs-lookup"><span data-stu-id="ff5e5-103">Customer aging report</span></span> 

<span data-ttu-id="ff5e5-104">**Myyntireskontran erääntyminen** -raportissa näkyy asiakkaiden erääntymissaldot päivämäärävälin tai erääntymiskauden mukaan lajiteltuna.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="ff5e5-105">Seuraavat oletusparametrit näytetään, kun tämä raportti luodaan.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="ff5e5-106">Voit käyttää näitä parametreja suodattamaan raportissa näkyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="ff5e5-107">Lisätietoja on kohdassa [Valikoimien määrittäminen](set-up-collections.md).</span><span class="sxs-lookup"><span data-stu-id="ff5e5-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ff5e5-108">Kenttä</span><span class="sxs-lookup"><span data-stu-id="ff5e5-108">Field</span></span></p></th>
<th><p><span data-ttu-id="ff5e5-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="ff5e5-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff5e5-110"><strong>Laskutusluokka</strong></span><span class="sxs-lookup"><span data-stu-id="ff5e5-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5e5-111">Valitse vähintään yksi raporttiin sisällytettävä laskutusluokka.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="ff5e5-112">**Huomautus:** Tämä ohjausobjekti on käytettävissä vain, jos <STRONG>Julkinen sektori</STRONG> -määritysavain on valittu.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff5e5-113"><strong>Sisällytä tapahtumat, joilla ei ole laskutusluokkaa</strong></span><span class="sxs-lookup"><span data-stu-id="ff5e5-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5e5-114">Jos tämä valintaruutu on valittu, kaikki tapahtumat, joihin ei ole määritetty laskutusluokkaan, näytetään raportissa.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="ff5e5-115">**Huomautus:** Tämä ohjausobjekti on käytettävissä vain, jos <STRONG>Julkinen sektori</STRONG> -määritysavain on valittu.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff5e5-116"><strong>Erääntyy</strong></span><span class="sxs-lookup"><span data-stu-id="ff5e5-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5e5-117">Anna nykyisessä erääntymisjakaumassa käytetty päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff5e5-118"><strong>Tilanne</strong></span><span class="sxs-lookup"><span data-stu-id="ff5e5-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5e5-119">Anna päivämäärä, jonka asiakkaan saldoa tarkastellaan.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="ff5e5-120">Tätä kutsutaan myös tapahtumien katkaisupäivämääräksi.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff5e5-121"><strong>Aloituspäivä</strong></span><span class="sxs-lookup"><span data-stu-id="ff5e5-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5e5-122">Anna päivämäärä, joka kuuluu raporttiin sisällytettävään ensimmäiseen aikaväliin tai erääntymiskauteen.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff5e5-123"><strong>Kriteeri</strong></span><span class="sxs-lookup"><span data-stu-id="ff5e5-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5e5-124">Valitse päivämäärätyyppi, johon raportti perustuu.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="ff5e5-125"><strong>Tapahtumapäivä</strong> – Tapahtumien kirjauspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="ff5e5-126">Se voi olla esimerkiksi laskun päiväys, johon eräpäivän laskenta perustuu.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="ff5e5-127"><strong>Eräpäivä</strong> – tapahtumien eräpäivä, joka perustuu maksuehtoihin.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="ff5e5-128"><strong>Asiakirjan päivämäärä</strong> – käyttäjän määrittämä tiedoston päivämäärä, jota käytetään eräpäivän laskennan perusteena.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff5e5-129"><strong>Erääntymiskausimääritys</strong></span><span class="sxs-lookup"><span data-stu-id="ff5e5-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5e5-130">Valitse erääntymiskausimääritys.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-130">Select an aging period definition.</span></span> <span data-ttu-id="ff5e5-131"><strong>Väli</strong>-kenttä ei ole käytettävissä, jos valitset erääntymiskauden määritelmän.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="ff5e5-132">Tulostetussa raportissa ei voi käyttää erääntymiskausimäärityksiä, joissa on yli kuusi erääntymiskautta.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="ff5e5-133">**Huomautus:** erääntymiskaudet voidaan määrittää <STRONG>Erääntymiskausimääritykset</STRONG>-sivulla.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff5e5-134"><strong>Tulosta erääntymiskauden kuvaus</strong></span><span class="sxs-lookup"><span data-stu-id="ff5e5-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5e5-135">Valitse <strong>Kyllä</strong>, jos haluat sisällyttää raporttiin erääntymiskauden sarakkeiden yläosissa olevat kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="ff5e5-136">Tulosta raportti ilman sarakeotsikoita valitsemalla <strong>Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff5e5-137"><strong>Väli</strong></span><span class="sxs-lookup"><span data-stu-id="ff5e5-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5e5-138">Määritä käytettävä aikaväli kirjoittamalla kunkin kauden päivä tai kuukausi.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="ff5e5-139">Voit esimerkiksi tarkastella erääntymistietoja viikoittain kirjoittamalla tähän kenttään 7 ja valitsemalla <strong>Pv/kk</strong>-kentässä <strong>Päivä</strong>.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="ff5e5-140">**Huomautus::** Tähän kenttään kirjoittamaasi tietoa käytetään vain, jos et ole valinnut erääntymiskausimääritystä.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="ff5e5-141">Muussa tapauksessa tulostuksen suunta määritetään erääntymiskausimäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff5e5-142"><strong>Pv/kk</strong></span><span class="sxs-lookup"><span data-stu-id="ff5e5-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5e5-143">Valitse yksiköksi joko <strong>Päivä</strong> tai <strong>Kuukausi</strong>. Tämä yksikön avulla määritetään <strong>Väli</strong>-kentän kausi.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff5e5-144"><strong>Suunta</strong></span><span class="sxs-lookup"><span data-stu-id="ff5e5-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5e5-145">Valitse, lasketaanko menneiden vai tulevien kausien saldot ja kumman erääntymisraportti tulostetaan.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="ff5e5-146">Päivämäärät lasketaan suhteessa <strong>Saldo per</strong> -kentässä valitun päivämäärän mukaan.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="ff5e5-147">Valitse <strong>Taaksepäin</strong>, jos haluat näyttää menneiden kausien tiedot.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="ff5e5-148">Valitse <strong>Eteenpäin</strong>, jos haluat näyttää tulevien kausien tiedot.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>

<span data-ttu-id="ff5e5-149">**Huomautus::** Tähän kenttään kirjoittamaasi tietoa käytetään vain, jos et ole valinnut erääntymiskausimääritystä.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-149">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff5e5-150"><strong>Tietoja</strong></span><span class="sxs-lookup"><span data-stu-id="ff5e5-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5e5-151">Valitse luetteloon tapahtumat, jotka sisällytetään raportissa näytettäviin saldoihin.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff5e5-152"><strong>Sisällytä summat tapahtumavaluutassa</strong></span><span class="sxs-lookup"><span data-stu-id="ff5e5-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5e5-153">Valitse summien sisällyttäminen tapahtumavaluutassa kirjanpitovaluuttana olevien summien lisäksi.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="ff5e5-154">Jos valintaruutua ei ole valittu, raportin summat näytetään vain kirjanpitovaluuttana.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff5e5-155"><strong>Negatiivinen saldo</strong></span><span class="sxs-lookup"><span data-stu-id="ff5e5-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5e5-156">Valitse niiden asiakastilien sisällyttäminen, joilla on negatiivinen saldo.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff5e5-157"><strong>Jätä nollasaldoiset tilit pois</strong></span><span class="sxs-lookup"><span data-stu-id="ff5e5-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5e5-158">Valitse niiden asiakastilien pois jättäminen, joilla on nollasaldo.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff5e5-159"><strong>Maksujen positiointi</strong></span><span class="sxs-lookup"><span data-stu-id="ff5e5-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5e5-160">Valitse selvittämättömien maksujen näyttäminen.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="ff5e5-161">Ne näytetään raportin ensimmäisessä sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="ff5e5-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>

