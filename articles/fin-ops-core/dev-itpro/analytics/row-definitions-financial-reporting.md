---
title: Talousraporttien suunnittelutoiminnon rivimääritykset
description: Rivin määritys on raporttiosa tai rakenneosa, joka määrittää talousraportin kunkin rivin sisällön.
author: aprilolson
manager: AnnBe
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
ms.openlocfilehash: dfce0f1622d45dcf77d91b71abbe9e33e8c91ad0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564028"
---
# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="6a798-103">Talousraporttien suunnittelutoiminnon rivimääritykset</span><span class="sxs-lookup"><span data-stu-id="6a798-103">Row definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a798-104">Rivin määritys on raporttiosa tai rakenneosa, joka määrittää talousraportin kunkin rivin sisällön.</span><span class="sxs-lookup"><span data-stu-id="6a798-104">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="6a798-105">Rivin määritys voidaan yhdistää sarakemääritykseen, raportointipuun määrityksiin ja raportin määrityksiin. Näin luodaan rakenneosaryhmä, jota voidaan käyttää useissa yrityksissä.</span><span class="sxs-lookup"><span data-stu-id="6a798-105">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

## <a name="create-a-row-definition"></a><span data-ttu-id="6a798-106">Rivimäärityksen luominen</span><span class="sxs-lookup"><span data-stu-id="6a798-106">Create a row definition</span></span>

1. <span data-ttu-id="6a798-107">Valitse Report Designerin siirtymisruudussa **Rivien määritykset**.</span><span class="sxs-lookup"><span data-stu-id="6a798-107">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="6a798-108">Valitse ensin **Tiedosto**-valikossa **Uusi** ja sitten **Rivin määritys**.</span><span class="sxs-lookup"><span data-stu-id="6a798-108">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="6a798-109">Lisätietoja kunkin solun sisällöstä on kohdassa [Rivin määrityksen solujen muokkaaminen](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="6a798-109">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="6a798-110">Rivin määrityksen avaaminen</span><span class="sxs-lookup"><span data-stu-id="6a798-110">Open a row definition</span></span>
1. <span data-ttu-id="6a798-111">Valitse Report Designerin siirtymisruudussa **Rivien määritykset**.</span><span class="sxs-lookup"><span data-stu-id="6a798-111">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="6a798-112">Napsauta avattavan rivin määrityksen nimeä hiiren kakkospainikkeella.</span><span class="sxs-lookup"><span data-stu-id="6a798-112">Double-click the name of the row definition to open.</span></span>
3. <span data-ttu-id="6a798-113">Voit tarkastella rivin määritykseen liittyviä rakenneosia napsauttamalla rivin määritystä hiiren kakkospainikkeella ja valitsemalla **Liitokset**.</span><span class="sxs-lookup"><span data-stu-id="6a798-113">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="6a798-114"> Rivin määrityksen sisältö</span><span class="sxs-lookup"><span data-stu-id="6a798-114">Contents of a row definition</span></span>
<span data-ttu-id="6a798-115">Rivin määritys voi sisältää enintään 20 000 taloushallinnon dimension riviä. Rivit voivat sisältää seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="6a798-115">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

- <span data-ttu-id="6a798-116">Kuvaava teksti, joka lisää raporttiin merkityksiä luomalla osan otsikoita, rivejä ja välilyöntejä, kuten **Käteinen** tai **Kokonaistuotto**.</span><span class="sxs-lookup"><span data-stu-id="6a798-116">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
- <span data-ttu-id="6a798-117">Linkkejä taloushallinnon tietoihin, jotka voivat sisältää Microsoft Dynamics 365 Financen dimensioarvoja.</span><span class="sxs-lookup"><span data-stu-id="6a798-117">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 Finance</span></span>

    > [!NOTE]
    > <span data-ttu-id="6a798-118">Voit määrittää rivimäärityksiä, kun haluat, että tietoja noudetaan taloushallinnon dimensiojärjestelmästä aina, kun raportti luodaan.</span><span class="sxs-lookup"><span data-stu-id="6a798-118">You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>

- <span data-ttu-id="6a798-119">Linkitettyihin taloushallinnon tietoihin perustuvien rivien yhteissummat ja kaavat.</span><span class="sxs-lookup"><span data-stu-id="6a798-119">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="6a798-120">Yleensä jokainen rivin määrityksen rivi sisältää jonkin seuraavaksi esitellyistä tietotyypeistä.</span><span class="sxs-lookup"><span data-stu-id="6a798-120">Usually, each row in a row definition contains one of the following types of information:</span></span>

- <span data-ttu-id="6a798-121">Viitteet taloushallinnon dimensioiden järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="6a798-121">References to the financial dimensions system</span></span>
- <span data-ttu-id="6a798-122">Tietoihin perustuvat yhteissummat tai laskelmat.</span><span class="sxs-lookup"><span data-stu-id="6a798-122">Totals or calculations that are based on the data</span></span>
- <span data-ttu-id="6a798-123">Muotoilu</span><span class="sxs-lookup"><span data-stu-id="6a798-123">Formatting</span></span>

<span data-ttu-id="6a798-124">Rivi määrityksen tiedot voidaan antaa kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="6a798-124">There are two methods for entering information in a row definition:</span></span>

- <span data-ttu-id="6a798-125">Anna rivin tiedot manuaalisesti uudessa rivin määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="6a798-125">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="6a798-126">Lisätietoja on kohdassa [Rivin määrityksen solujen muokkaaminen](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="6a798-126">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
- <span data-ttu-id="6a798-127">Hae rivitiedot Report Designerilla suoraan taloushallinnon dimensioista.</span><span class="sxs-lookup"><span data-stu-id="6a798-127">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="6a798-128">Lisätietoja on artikkelin [Muokkaa rivin määrityssoluja](modify-row-definition-cells-financial-reporting.md) kohdassa Liittyvät kaavat, rivit ja yksiköt.</span><span class="sxs-lookup"><span data-stu-id="6a798-128">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="6a798-129"> Dimensioiden lisääminen rivin määritykseen</span><span class="sxs-lookup"><span data-stu-id="6a798-129">Add dimensions in a row definition</span></span>
<span data-ttu-id="6a798-130">Dimensio on tietojen ja arvojen liitos.</span><span class="sxs-lookup"><span data-stu-id="6a798-130">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="6a798-131">Voit ryhmitellä tietoja ja arvoja Report Designerissa.</span><span class="sxs-lookup"><span data-stu-id="6a798-131">You can group data and values in report designer.</span></span> <span data-ttu-id="6a798-132">Voit sitten luokitella ja analysoida tapahtumia yksityiskohtaisemmin.</span><span class="sxs-lookup"><span data-stu-id="6a798-132">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="6a798-133">Voit lisätä rivin määritykseen useita rivejä samanaikaisesti **Lisää rivejä dimensioista** -valintaikkunan avulla.</span><span class="sxs-lookup"><span data-stu-id="6a798-133">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="6a798-134">Valintaikkunassa näkyy kunkin dimension yksi sarake.</span><span class="sxs-lookup"><span data-stu-id="6a798-134">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="6a798-135">Seuraavassa taulussa kuvataan tietoja, joilla kukin dimensio määritetään.</span><span class="sxs-lookup"><span data-stu-id="6a798-135">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="6a798-136">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="6a798-136">Option</span></span>                | <span data-ttu-id="6a798-137">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="6a798-137">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="6a798-138">Dimensio</span><span class="sxs-lookup"><span data-stu-id="6a798-138">Dimension</span></span>             | <span data-ttu-id="6a798-139">Malli, joka määrittää rivin määritykseen lisättävän dimension.</span><span class="sxs-lookup"><span data-stu-id="6a798-139">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="6a798-140">Tämä malli sisältää yhden et-merkin (&) tai numeromerkin (\#) jokaista dimension sijaintia kohti.</span><span class="sxs-lookup"><span data-stu-id="6a798-140">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="6a798-141">Yleensä et-merkkejä käytetään päätilin dimensioissa ja numeromerkkejä muissa dimensioissa.</span><span class="sxs-lookup"><span data-stu-id="6a798-141">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="6a798-142">Dimensioalueen alku</span><span class="sxs-lookup"><span data-stu-id="6a798-142">Dimension Range Start</span></span> | <span data-ttu-id="6a798-143">Rivimääritykseen lisättävän dimension ensimmäinen arvo.</span><span class="sxs-lookup"><span data-stu-id="6a798-143">The first value for this dimension to add to the row definition.</span></span> |
| <span data-ttu-id="6a798-144">Dimensioalueen loppu</span><span class="sxs-lookup"><span data-stu-id="6a798-144">Dimension Range End</span></span>   | <span data-ttu-id="6a798-145">Tämän dimension viimeinen arvo, joka lisätään rivin määritykseen.</span><span class="sxs-lookup"><span data-stu-id="6a798-145">The last value for this dimension to add to the row definition.</span></span> |

<span data-ttu-id="6a798-146">Seuraavien vaiheiden avulla voit lisätä dimensioita rivin määritykseen.</span><span class="sxs-lookup"><span data-stu-id="6a798-146">To add dimensions to a row definition, follow these steps.</span></span>

1. <span data-ttu-id="6a798-147">Valitse Report Designerissa **Rivien määritykset** ja avaa sitten muokattava rivin määritys.</span><span class="sxs-lookup"><span data-stu-id="6a798-147">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="6a798-148">Valitse **Muokkaa** -valikosta **Lisää rivejä dimensioista**.</span><span class="sxs-lookup"><span data-stu-id="6a798-148">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="6a798-149">Valitse **Lisää rivejä dimensioista**-valintaikkunan **Dimensiot**-rivillä rivin määritykseen siirrettävä dimension solu. Valitse sitten **Kaikki &&&**.</span><span class="sxs-lookup"><span data-stu-id="6a798-149">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4. <span data-ttu-id="6a798-150">Voit rajoittaa rivin määrityksen tiettyyn dimensioarvojen väliin antamalla **Dimensiovälin alku**-soluun dimension aloitusarvon ja **Dimensiovälin loppu** -soluun dimension lopetusarvon.</span><span class="sxs-lookup"><span data-stu-id="6a798-150">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="6a798-151">Jos haluat sisällyttää rivimääritykseen kaikki valitun dimension arvot, jätä nämä solut tyhjiksi.</span><span class="sxs-lookup"><span data-stu-id="6a798-151">To include all values for the selected dimension, leave these cells empty.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6a798-152">Yleismerkit (\* tai ?) dimensioalueissa eivät ehkä palauta kaikkia haluamiasi tuloksia, sillä tietojen lajittelutapa ERP-tietokannassa vaikuttaa tuloksiin.</span><span class="sxs-lookup"><span data-stu-id="6a798-152">Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>

5. <span data-ttu-id="6a798-153">Määritä **Aloittavan rivin koodi** -kenttään ensimmäisen rivin määritykseen lisättävän dimensioarvon rivikoodi.</span><span class="sxs-lookup"><span data-stu-id="6a798-153">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6. <span data-ttu-id="6a798-154">Määritä **Lisää kutakin riviä arvolla** -kenttään kahden peräkkäisen rivikoodin väli.</span><span class="sxs-lookup"><span data-stu-id="6a798-154">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="6a798-155">Jos esimerkiksi ensimmäisen rivin koodi on 100 ja lisäysarvo on 30, ensimmäisten uusien rivien koodit ovat 100, 130, 160, 190 ja 220.</span><span class="sxs-lookup"><span data-stu-id="6a798-155">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="6a798-156">Käytä lisäysarvoa, joka määrittää riittävästi tilaa uuden muotoilu- ja kaavarivien lisäämistä varten.</span><span class="sxs-lookup"><span data-stu-id="6a798-156">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7. <span data-ttu-id="6a798-157">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="6a798-157">Click **OK**.</span></span> <span data-ttu-id="6a798-158">Kullekin valitulle dimensioarvolle lisätään yksi rivi rivin määritykseen.</span><span class="sxs-lookup"><span data-stu-id="6a798-158">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="6a798-159"> Pyöristyksen oikaisu rivin määrityksessä</span><span class="sxs-lookup"><span data-stu-id="6a798-159">Adjust rounding in a row definition</span></span>
<span data-ttu-id="6a798-160">Jos taseessa on pyöristettyjä summia, kokonaissummat eivät ehkä täsmää.</span><span class="sxs-lookup"><span data-stu-id="6a798-160">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="6a798-161">Tämä ongelma voi esiintyä esimerkiksi silloin, kun käytät taseraportissa pyöritysasetusta ja pyöristys määritetään myös raportin määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="6a798-161">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="6a798-162">Voit täsmätä taseen summat käyttämällä rivin määrityksessä **Pyöristyksen oikaisu** -vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="6a798-162">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="6a798-163">Voit poistaa pyöristyksen käytöstä tai muokata sitä raportin määrityksen **Asetukset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="6a798-163">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="6a798-164">Seuraavassa taulukossa on esitetty, miten summat pyöristetään.</span><span class="sxs-lookup"><span data-stu-id="6a798-164">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="6a798-165">Rivien 100 ja 200 kokonaissummat ovat erilaiset tässä taulukossa, kun pyöristys ei ole käytössä.</span><span class="sxs-lookup"><span data-stu-id="6a798-165">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="6a798-166">Rivin koodi</span><span class="sxs-lookup"><span data-stu-id="6a798-166">Row code</span></span> | <span data-ttu-id="6a798-167">Summat ilman pyöristystä</span><span class="sxs-lookup"><span data-stu-id="6a798-167">Amounts without rounding</span></span> | <span data-ttu-id="6a798-168">Summat, jotka pyöristetään kokonaisiin tuhansiin</span><span class="sxs-lookup"><span data-stu-id="6a798-168">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="6a798-169">100</span><span class="sxs-lookup"><span data-stu-id="6a798-169">100</span></span>      | <span data-ttu-id="6a798-170">3,600</span><span class="sxs-lookup"><span data-stu-id="6a798-170">3,600</span></span>                    | <span data-ttu-id="6a798-171">4</span><span class="sxs-lookup"><span data-stu-id="6a798-171">4</span></span>                                       |
| <span data-ttu-id="6a798-172">200</span><span class="sxs-lookup"><span data-stu-id="6a798-172">200</span></span>      | <span data-ttu-id="6a798-173">3,700</span><span class="sxs-lookup"><span data-stu-id="6a798-173">3,700</span></span>                    | <span data-ttu-id="6a798-174">4</span><span class="sxs-lookup"><span data-stu-id="6a798-174">4</span></span>                                       |
| <span data-ttu-id="6a798-175">Yhteensä</span><span class="sxs-lookup"><span data-stu-id="6a798-175">Total</span></span>    | <span data-ttu-id="6a798-176">7,300</span><span class="sxs-lookup"><span data-stu-id="6a798-176">7,300</span></span>                    | <span data-ttu-id="6a798-177">8</span><span class="sxs-lookup"><span data-stu-id="6a798-177">8</span></span>                                       |

<span data-ttu-id="6a798-178">Voit oikaista taseen pyöristyksen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="6a798-178">To adjust rounding in a balance sheet, follow these steps.</span></span>

1. <span data-ttu-id="6a798-179">Valitse Report Designerissa **Rivien määritykset** ja avaa muokattava rivin määritys.</span><span class="sxs-lookup"><span data-stu-id="6a798-179">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="6a798-180">Valitse **Muokkaa**-valikosta **Pyöristysoikaisu**.</span><span class="sxs-lookup"><span data-stu-id="6a798-180">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3. <span data-ttu-id="6a798-181">Syötä **Pyöristyksen oikaisut** -valintaikkunaan seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6a798-181">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>

    - <span data-ttu-id="6a798-182">**Pyöristyksen oikaisurivi** – Sen rivin rivikoodi, joka on oikaistava taseen täsmäyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="6a798-182">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    - <span data-ttu-id="6a798-183">**Kaikkien käyttöomaisuuserien rivi** – Taseen kaikki käyttöomaisuuserät sisältävän rivin koodi.</span><span class="sxs-lookup"><span data-stu-id="6a798-183">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    - <span data-ttu-id="6a798-184">**Kaikkien velkojen ja pääoman rivi** – Taseen kaikki velat ja pääoman sisältävän rivin koodi.</span><span class="sxs-lookup"><span data-stu-id="6a798-184">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    - <span data-ttu-id="6a798-185">**Oikaisusumman raja** – Positiivinen kokonaisluku, joka määrittää automaattisten oikaisujen rajan.</span><span class="sxs-lookup"><span data-stu-id="6a798-185">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="6a798-186">Tätä summaa verrataan toteutuneen pyöristyseron absoluuttiseen arvoon.</span><span class="sxs-lookup"><span data-stu-id="6a798-186">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6a798-187">Nämä rivikoodit on linkitettävä taloushallinnon tietoihin.</span><span class="sxs-lookup"><span data-stu-id="6a798-187">These row codes must be linked to your financial data.</span></span> <span data-ttu-id="6a798-188">Toisin sanoen rivillä on oltava dimensioarvo **Linkki taloushallinnon dimensioihin** -solussa.</span><span class="sxs-lookup"><span data-stu-id="6a798-188">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="6a798-189">**Älä** tee viittausta kuvauksen riviin (**DESC**), laskettuun riviin (**CALC**) tai kokonaissumman riviin (**TOT**).</span><span class="sxs-lookup"><span data-stu-id="6a798-189">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="6a798-190">Taseen summat täsmäytetään nyt tasaisesti, kun pyöristys on päällä.</span><span class="sxs-lookup"><span data-stu-id="6a798-190">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="6a798-191">Oikaisun rajoitus perustuu raporttimääritykselle määritettyyn **Pyöristystarkkuus**-asetukseen.</span><span class="sxs-lookup"><span data-stu-id="6a798-191">The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="6a798-192">Jos esimerkiksi pyöristät raportin tuhansiksi ja annat **Oikaisusumman raja** -kentässä arvoksi **2**, näyttöön avautuu varoitussanoma, kun **Pyöristyksen oikaisurivi** -kentän arvo nousee tai laskee enemmän kuin 2 000.</span><span class="sxs-lookup"><span data-stu-id="6a798-192">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="6a798-193">Rivin ja sarakkeen tekstin muotoileminen</span><span class="sxs-lookup"><span data-stu-id="6a798-193">Format row and column text</span></span>
<span data-ttu-id="6a798-194">Voit mukauttaa raporttien ulkoasua muuttamalla fontteja ja muotoilemalla tekstiä.</span><span class="sxs-lookup"><span data-stu-id="6a798-194">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="6a798-195">Seuraavassa osassa kerrotaan, miten raporttien rivien ja sarakkeiden ulkoasua muotoillaan.</span><span class="sxs-lookup"><span data-stu-id="6a798-195">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="6a798-196">Fonttityylien hallinta</span><span class="sxs-lookup"><span data-stu-id="6a798-196">Manage font styles</span></span>

<span data-ttu-id="6a798-197">Voit luoda ja muokata raportin fonttityylejä.</span><span class="sxs-lookup"><span data-stu-id="6a798-197">You can create and modify font styles for your report.</span></span> <span data-ttu-id="6a798-198">Voit sitten käyttää näitä tyylejä asiakirjassa tai raportin tietyllä rivillä tai tietyssä sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="6a798-198">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="6a798-199"><strong>Luo fonttityyli</strong></span><span class="sxs-lookup"><span data-stu-id="6a798-199"><strong>Create a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="6a798-200">Valitse Report Designerin <strong>Muotoilu</strong>-valikosta <strong>Tyylit ja muotoilu</strong>.</span><span class="sxs-lookup"><span data-stu-id="6a798-200">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="6a798-201">Valitse <strong>Tyylit ja muotoilu</strong>-valintaikkunassa <strong>Uusi</strong> ja anna sitten uudelle tyylille yksilöllinen nimi.</span><span class="sxs-lookup"><span data-stu-id="6a798-201">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="6a798-202">Tee fonttia koskevat valinnat ja valitse <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="6a798-202">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="6a798-203"><strong>Fonttityylin muokkaaminen</strong></span><span class="sxs-lookup"><span data-stu-id="6a798-203"><strong>Modify a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="6a798-204">Valitse Report Designerin <strong>Muotoilu</strong>-valikosta <strong>Tyylit ja muotoilu</strong>.</span><span class="sxs-lookup"><span data-stu-id="6a798-204">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="6a798-205">Valitse muokattava tyyli <strong>Tyylit ja muotoilu</strong> -valintaikkunassa ja valitse sitten <strong>Muokkaa</strong>.</span><span class="sxs-lookup"><span data-stu-id="6a798-205">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="6a798-206">Tee fonttia koskevat valinnat ja valitse <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="6a798-206">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="6a798-207"><strong>Ota fonttityyli käyttöön</strong></span><span class="sxs-lookup"><span data-stu-id="6a798-207"><strong>Apply a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="6a798-208">Valitse Report Designerin määrityksessä tai sarakkeen määrityksessä tai ylä- tai alatunnisteissa vähintään yksi solu.</span><span class="sxs-lookup"><span data-stu-id="6a798-208">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="6a798-209">Valitse fonttityyli työkalurivin <strong>Tyyli</strong>-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="6a798-209">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="6a798-210">Rivin tekstin muotoileminen</span><span class="sxs-lookup"><span data-stu-id="6a798-210">Format row text</span></span>

<span data-ttu-id="6a798-211">Rivin määrityksessä määritetty muotoilu korvaa sarakkeen ja raportin määrityksessä määritetyn muotoilun.</span><span class="sxs-lookup"><span data-stu-id="6a798-211">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="6a798-212">Voit muokata tekstimuotoa muotoilun työkalurivin ohjausobjekteilla.</span><span class="sxs-lookup"><span data-stu-id="6a798-212">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="6a798-213">Nämä ohjausobjektit ovat Microsoft Windowsin vakio-ohjausobjekteja.</span><span class="sxs-lookup"><span data-stu-id="6a798-213">These controls are standard Microsoft Windows controls.</span></span>

1. <span data-ttu-id="6a798-214">Avaa raporttien suunnitteluohjelmassa rivimääritys, jota haluat muokata.</span><span class="sxs-lookup"><span data-stu-id="6a798-214">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="6a798-215">Valitse muokattavat solut.</span><span class="sxs-lookup"><span data-stu-id="6a798-215">Select the cells to format.</span></span> <span data-ttu-id="6a798-216">Voit valita useita soluja pitämällä Ctrl-näppäintä alhaalla valinnan aikana.</span><span class="sxs-lookup"><span data-stu-id="6a798-216">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3. <span data-ttu-id="6a798-217">Ota muoto käyttöön valitsemalla muodon työkalurivipainike.</span><span class="sxs-lookup"><span data-stu-id="6a798-217">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="6a798-218">Jos haluat esimerkiksi sisentää rivin, valitse rivi ja valitse sitten työkalurivin **Kasvata sisennystä** -kohta ![Kasvata sisennystä](media/indent.gif "Kasvata sisennystä").</span><span class="sxs-lookup"><span data-stu-id="6a798-218">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](media/indent.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="6a798-219">Sarakkeiden oikaisu raporttien suunnittelun yhteydessä</span><span class="sxs-lookup"><span data-stu-id="6a798-219">Adjust columns while you design reports</span></span>

<span data-ttu-id="6a798-220">Rivin määrityksen käsiteltävien sarakkeiden tarkasteleminen helpottuu oikaisemalla sarakkeen leveyttä ja piilottamalla (pienentämällä) tai näyttämällä sarakkeet näkymäruudussa.</span><span class="sxs-lookup"><span data-stu-id="6a798-220">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="6a798-221">Tekemäsi muutokset vaikuttavat sarakkeiden ulkoasuun vain näytössä.</span><span class="sxs-lookup"><span data-stu-id="6a798-221">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="6a798-222">Ne eivät vaikuta raporttien sarakemuotoiluun.</span><span class="sxs-lookup"><span data-stu-id="6a798-222">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="6a798-223">Sarakkeen leveyden muuttaminen näkymäruudussa</span><span class="sxs-lookup"><span data-stu-id="6a798-223">Change the width of a column in the view pane</span></span>

1. <span data-ttu-id="6a798-224">Avaa Report Designer -ohjelmassa muokattava rivin määritys.</span><span class="sxs-lookup"><span data-stu-id="6a798-224">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="6a798-225">Valitse **Muotoilu**-valikosta **Sarakkeen leveys**.</span><span class="sxs-lookup"><span data-stu-id="6a798-225">On the **Format** menu, select **Column Width**.</span></span>
3. <span data-ttu-id="6a798-226">Anna **Sarakkeen leveys** -valintaikkunassa arvo ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="6a798-226">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="6a798-227">Vaihtoehtoisesti voit muuttaa sarakkeen kokoa vetämällä sarakeotsikkosolun oikeaa reunaa.</span><span class="sxs-lookup"><span data-stu-id="6a798-227">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="6a798-228">Sarakkeiden piilottaminen näkymäruudussa</span><span class="sxs-lookup"><span data-stu-id="6a798-228">Hide columns in the view pane</span></span>

1. <span data-ttu-id="6a798-229">Avaa Report Designer -ohjelmassa muokattava rivin määritys.</span><span class="sxs-lookup"><span data-stu-id="6a798-229">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="6a798-230">Valitse piilotettavat sarakkeet.</span><span class="sxs-lookup"><span data-stu-id="6a798-230">Select the column or columns to minimize.</span></span>
3. <span data-ttu-id="6a798-231">Napsauta kohdetta hiiren kakkospainikkeella ja valitse sitten **Piilota**.</span><span class="sxs-lookup"><span data-stu-id="6a798-231">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="6a798-232">Kaikkien piilotettujen sarakkeiden näyttäminen näkymäruudussa</span><span class="sxs-lookup"><span data-stu-id="6a798-232">Show all hidden columns in the view pane</span></span>

1. <span data-ttu-id="6a798-233">Avaa Report Designer -ohjelmassa muokattava rivin määritys.</span><span class="sxs-lookup"><span data-stu-id="6a798-233">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="6a798-234">Napsauta näytettävää pienennettyä saraketta hiiren kakkospainikkeella ja valitse sitten **Tuo esiin**.</span><span class="sxs-lookup"><span data-stu-id="6a798-234">Right-click the minimized column to display, and then click **Unhide**.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="6a798-235">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6a798-235">Additional resources</span></span>

[<span data-ttu-id="6a798-236">Taloushallinnon raportointi</span><span class="sxs-lookup"><span data-stu-id="6a798-236">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]