---
title: Talousraportoinnin tietovaraston osajoukon palauttaminen
description: "Tässä ohjeaiheessa kerrotaan, miten talousraportoinnin tietovaraston osajoukko palautetaan."
author: aolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0786d3377b914791106ef30455d676e5ab2ae03d
ms.openlocfilehash: c708fa18b8676d8ff57c26b3176a36d86df29387
ms.contentlocale: fi-fi
ms.lasthandoff: 12/07/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="a290b-103">Talousraportoinnin tietovaraston osajoukon palauttaminen</span><span class="sxs-lookup"><span data-stu-id="a290b-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a290b-104">Tässä ohjeaiheessa kerrotaan, miten seuraavien versioiden talousraportoinnin tietovaraston osajoukko palautetaan:</span><span class="sxs-lookup"><span data-stu-id="a290b-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="a290b-105">Microsoft Dynamics 365 for Finance and Operations: Taloushallinnon raportoinnin versio 7.2.6.0 ja uudempi</span><span class="sxs-lookup"><span data-stu-id="a290b-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="a290b-106">Microsoft Dynamics 365 for Finance and Operations: Taloushallinnon raportoinnin versio 7.0.10000.4 ja uudempi</span><span class="sxs-lookup"><span data-stu-id="a290b-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="a290b-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (paikallinen)</span><span class="sxs-lookup"><span data-stu-id="a290b-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="a290b-108">Saat Finance and Operationsin taloushallinnon raportoinnin version 7.2.6.0, kun lataat KB-artikkelin 4052514 osoitteesta <https://support.microsoft.com/en-us/help/4052514>.</span><span class="sxs-lookup"><span data-stu-id="a290b-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://support.microsoft.com/en-us/help/4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="a290b-109">Finance and Operationsin taloushallinnon raportoinnin version 7.2.6.0 ja uudemman version talousraportoinnin tietovaraston osajoukon palauttaminen</span><span class="sxs-lookup"><span data-stu-id="a290b-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="a290b-110">Talousraportoinnin tietovaraston osajoukon palauttaminen raportin suunnittelutoiminnosta</span><span class="sxs-lookup"><span data-stu-id="a290b-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="a290b-111">Tämän prosessin vaiheita tuetaan Finance and Operationsin taloushallinnon raportoinnin versiossa 7.2.6.0 ja uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="a290b-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="a290b-112">Jos käytössä on aiempi versio, ota yhteys tukitiimiin.</span><span class="sxs-lookup"><span data-stu-id="a290b-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="a290b-113">Tietyissä skenaarioissa talousraportoinnin tietovaraston osajoukko on ehkä palautettava.</span><span class="sxs-lookup"><span data-stu-id="a290b-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="a290b-114">Tämä tehtävä voidaan tehdä raportin suunnitteluohjelman käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="a290b-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="a290b-115">Seuraavassa on joitakin skenaarioita, joissa tietovaraston osajoukko on ehkä palautettava:</span><span class="sxs-lookup"><span data-stu-id="a290b-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="a290b-116">Finance and Operations -tietokanta on palautettu, mutta tietovaraston osajoukkoa ei.</span><span class="sxs-lookup"><span data-stu-id="a290b-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="a290b-117">Kauden tiedot ovat virheelliset.</span><span class="sxs-lookup"><span data-stu-id="a290b-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="a290b-118">Tuki kehottaa palauttamaan tietovaraston osajoukon vianmääritysvaiheen osana.</span><span class="sxs-lookup"><span data-stu-id="a290b-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="a290b-119">Tietovaraston osajoukon palautus on tehtävä ajankohtana, jona tietokannassa ei käsitellä paljon tietoja.</span><span class="sxs-lookup"><span data-stu-id="a290b-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="a290b-120">Taloushallinnon raportointi ei ole käytettävissä palautusprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="a290b-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="a290b-121">Tietovaraston osajoukon palauttaminen</span><span class="sxs-lookup"><span data-stu-id="a290b-121">Reset the data mart</span></span>

<span data-ttu-id="a290b-122">Voit palauttaa tietovaraston osajoukon valitsemalla raportin suunnitteluohjelman **Työkalut**-valikossa **Palauta tietovaraston osajoukko**.</span><span class="sxs-lookup"><span data-stu-id="a290b-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="a290b-123">Esiin tulevassa valintaikkunassa on kaksi osaa: **Tilastotiedot** ja **Palauta**.</span><span class="sxs-lookup"><span data-stu-id="a290b-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="a290b-124">[![Palauta tietovaraston osajoukko -valintaikkuna](./media/Statistics.png)](./media/Statistics.png)</span><span class="sxs-lookup"><span data-stu-id="a290b-124">[![Reset Data Mart dialog box](./media/Statistics.png)](./media/Statistics.png)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="a290b-125">Integrointiyritykset</span><span class="sxs-lookup"><span data-stu-id="a290b-125">Integration attempts</span></span>

<span data-ttu-id="a290b-126">**Integrointiyritykset**-ruudukossa on tieto siitä, miten monta kertaa järjestelmä on yrittänyt integroida tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="a290b-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="a290b-127">Järjestelmä yrittää integroida tietoja tiettyjen päivien ajan, jos ensimmäiset yritykset eivät onnistu.</span><span class="sxs-lookup"><span data-stu-id="a290b-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="a290b-128">Tiedät, että tietovaraston osajoukko on palautettava, jos yritysten määrä on 8 tai yli ja jos dimensioyhdistelmiä tai tapahtumatietueita on useita.</span><span class="sxs-lookup"><span data-stu-id="a290b-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="a290b-129">Tässä tapauksessa tietoja ei raportoida.</span><span class="sxs-lookup"><span data-stu-id="a290b-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="a290b-130">Tietojen tila</span><span class="sxs-lookup"><span data-stu-id="a290b-130">Data status</span></span>

<span data-ttu-id="a290b-131">**Tietojen tila** -ruudukossa on tietovaraston osajoukon tapahtumien, valuuttakurssien ja dimensioiden arvojen tilannevedos.</span><span class="sxs-lookup"><span data-stu-id="a290b-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="a290b-132">Jos käyttämättömiä tietueita on paljon, tietueita on luultavasti päivitetty useita kertoja.</span><span class="sxs-lookup"><span data-stu-id="a290b-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="a290b-133">Tämän vuoksi raporttien luonti voi hidastua.</span><span class="sxs-lookup"><span data-stu-id="a290b-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="a290b-134">Kohdistamattomat päätililuokat</span><span class="sxs-lookup"><span data-stu-id="a290b-134">Misaligned main account categories</span></span>

<span data-ttu-id="a290b-135">Jos käytössä on Microsoft Dynamics 365 for Finance and Operationsin taloushallinnon raportoinnin versiota 7.2.1 aiempi versio, tietovaraston osajoukko on ehkä palautettava, jos annat tileille uudet nimet ja siirrät tilejä tililuokasta toiseen.</span><span class="sxs-lookup"><span data-stu-id="a290b-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="a290b-136">Näiden toimintojen vuoksi päätililuokista voi tulla kohdistamattomia.</span><span class="sxs-lookup"><span data-stu-id="a290b-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="a290b-137">**Kohdistamattomat päätililuokat** -kenttä osoittaa, onko tämä ongelma ajankohtainen.</span><span class="sxs-lookup"><span data-stu-id="a290b-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="a290b-138">Finance and Operationsin taloushallinnon raportoinnin version 7.2.6.0 tietovaraston osajoukon palauttaminen</span><span class="sxs-lookup"><span data-stu-id="a290b-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="a290b-139">Voit palauttaa tietovaraston osajoukon Finance and Operationsin taloushallinnon raportoinnin versiossa 7.2.6.0 ja aiemmissa versioissa valitsemalla **Palauta tietovaraston osajoukko** -valintaikkunassa **Palauta tietovaraston osajoukko** -valintaruutu ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="a290b-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="a290b-140">Palauta tietovaraston osajoukko vain ajoitetun käyttökatkon aikana.</span><span class="sxs-lookup"><span data-stu-id="a290b-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="a290b-141">[![Palauta tietovaraston osajoukko -valintaruutu](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="a290b-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="a290b-142">Tietovaraston osajoukon palauttaminen ja syyn valitseminen Microsoft Dynamics 365 for Finance and Operationsin taloushallinnon raportoinnin versiossa 7.3.0</span><span class="sxs-lookup"><span data-stu-id="a290b-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="a290b-143">Jos tietovaraston osajoukon palauttaminen on mielestäsi välttämätöntä, valitse **Palauta tietovaraston osajoukko** -valintaruutu ja valitse sitten **Syy**-kentässä syy.</span><span class="sxs-lookup"><span data-stu-id="a290b-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="a290b-144">Käytettävissä ovat seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="a290b-144">The following options are available:</span></span>

- <span data-ttu-id="a290b-145">**Puuttuvat tai virheelliset tiedot** – Tilastotietojen perusteella olet sitä mieltä, että tietoja saattaa puuttua.</span><span class="sxs-lookup"><span data-stu-id="a290b-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="a290b-146">Ennen kuin jatkat, suosittelemme pääsyyn selvittämistä tuen kanssa.</span><span class="sxs-lookup"><span data-stu-id="a290b-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="a290b-147">**Palauta tietokanta** – Finance and Operations -tietokanta on palautettu, mutta taloushallinnon raportoinnin tietovaraston osajoukkoa ei.</span><span class="sxs-lookup"><span data-stu-id="a290b-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="a290b-148">**Muu** – Olet palauttamassa tietovaraston osajoukkoa jonkin muun syyn vuoksi.</span><span class="sxs-lookup"><span data-stu-id="a290b-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="a290b-149">Jos epäilet, että jossakin on ongelma, ota yhteys tukeen asian selvittämistä varten.</span><span class="sxs-lookup"><span data-stu-id="a290b-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

> [!NOTE]
> <span data-ttu-id="a290b-150">Varmista, että kaikki aiemmat tehtävät on integroitu, ennen kuin suoritat prosessin vaiheet.</span><span class="sxs-lookup"><span data-stu-id="a290b-150">Verify that all existing tasks have finished integrating before you complete the steps.</span></span> <span data-ttu-id="a290b-151">Voit tarkistaa integroinnin tilan valitsemalla **Työkalut** &gt; **Integroinnin tila**.</span><span class="sxs-lookup"><span data-stu-id="a290b-151">You can view the status of the integration by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="a290b-152">Poista käyttäjät ja yritykset</span><span class="sxs-lookup"><span data-stu-id="a290b-152">Clear users and companies</span></span>

<span data-ttu-id="a290b-153">Valitse **Poista käyttäjät ja yritykset** -valintaruutu, jos palautit tietokannan ja teit sen jälkeen muutoksia käyttäjien tai yritysten tietoihin.</span><span class="sxs-lookup"><span data-stu-id="a290b-153">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="a290b-154">Tämän valintaruudun valinnan tulisi olla ajankohtaista vain harvoin.</span><span class="sxs-lookup"><span data-stu-id="a290b-154">You should rarely have to select this check box.</span></span>

<span data-ttu-id="a290b-155">Kun palautusprosessi voidaan aloittaa, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a290b-155">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="a290b-156">Näyttöön tulee kehote, jossa pyydetään vahvistamaan, että kaikki on valmista prosessin aloittamista varten.</span><span class="sxs-lookup"><span data-stu-id="a290b-156">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="a290b-157">Ota huomioon, että taloushallinnon raportointi ei ole käytettävissä palauttamisen ja sen jälkeen tapahtuvan aloitustietojen integroinnin aikana.</span><span class="sxs-lookup"><span data-stu-id="a290b-157">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="a290b-158">Jos haluat tarkistaa integroinnin tilan, valitse **Työkalut** &gt; **Integroinnin tila**. Tämän jälkeen näet integroinnin edellisen suoritusajankohdan ja tilan.</span><span class="sxs-lookup"><span data-stu-id="a290b-158">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="a290b-159">[![Integroinnin tilan tarkasteleminen](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="a290b-159">[![View the status of the integration](./media/Integration.png)](./media/Integration.png)</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="a290b-160">Finance and Operationsin taloushallinnon raportoinnin version 7.0.10000.4 ja uudemman version talousraportoinnin tietovaraston osajoukon palauttaminen</span><span class="sxs-lookup"><span data-stu-id="a290b-160">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="a290b-161">Jos joskus palautat Finance and Operations -tietokannan varmuuskopiosta tai toisen ympäristön tietokannasta, sinun noudatettava tämän osan ohjeita. Tällä tavoin voit varmistaa, että taloushallinnon raportoinnin tietovaraston osajoukko käyttää oikein palautettua Finance and Operations -tietokantaa.</span><span class="sxs-lookup"><span data-stu-id="a290b-161">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="a290b-162">Tämän prosessin vaiheita tuetaan Microsoft Dynamics AX -sovelluksen versiossa 7.0.1 (toukokuu 2016) (sovelluksen versio 7.0.1265.23014 ja taloushallinnon raportoinnin versio 7.0.10000.4) ja uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="a290b-162">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="a290b-163">Jos käytössä on Finance and Operationsin aiempi versio, ota yhteys tukeen.</span><span class="sxs-lookup"><span data-stu-id="a290b-163">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="a290b-164">Raporttimääritysten vieminen</span><span class="sxs-lookup"><span data-stu-id="a290b-164">Export report definitions</span></span>

<span data-ttu-id="a290b-165">Vie ensin raportin rakenteet raportin suunnitteluohjelmasta näiden ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="a290b-165">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="a290b-166">Valitse raportin suunnitteluohjelmassa **Yritys** &gt; **Rakenneosaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="a290b-166">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="a290b-167">Valitse vietävä rakenneosaryhmä ja valitse sitten **Vie**.</span><span class="sxs-lookup"><span data-stu-id="a290b-167">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a290b-168">Finance and Operations tukee vain yhtä **oletusarvoista** rakenneosaryhmää.</span><span class="sxs-lookup"><span data-stu-id="a290b-168">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="a290b-169">Valitse vietävät raporttimääritykset seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="a290b-169">Select the report definitions to export:</span></span>

    - <span data-ttu-id="a290b-170">Jos haluat viedä kaikki raporttimääritykset ja niihin liittyvät rakenneosat, valitse **Valitse kaikki**.</span><span class="sxs-lookup"><span data-stu-id="a290b-170">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="a290b-171">Voit viedä tiettyjä raportti-, rivi-, sarake-, puu- ja dimensioyhdistelmiä valitsemalla kyseisen välilehden ja valitsemalla sitten vietävät kohteet.</span><span class="sxs-lookup"><span data-stu-id="a290b-171">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="a290b-172">Voit valita välilehdessä useita kohteita pitämällä Ctrl-näppäintä alhaalla. Kun valitset vietävät raportit, niihin liittyvät rivit, sarakkeet, puut ja dimensioyhdistelmät tulevat valituiksi.</span><span class="sxs-lookup"><span data-stu-id="a290b-172">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="a290b-173">Valitse **Vie**.</span><span class="sxs-lookup"><span data-stu-id="a290b-173">Select **Export**.</span></span>
5. <span data-ttu-id="a290b-174">Anna tiedostonimi ja valitse turvallinen paikka, jonne viedyt raporttimääritykset tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="a290b-174">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="a290b-175">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a290b-175">Select **Save**.</span></span>

<span data-ttu-id="a290b-176">Voit kopioida tai ladata tiedoston turvalliseen paikkaan.</span><span class="sxs-lookup"><span data-stu-id="a290b-176">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="a290b-177">Näin tiedosto voidaan tuoda toiseen ympäristöön myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="a290b-177">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="a290b-178">Lisätietoja Microsoft Azure -tallennustilin käyttämisestä on kohdassa [Tietojen siirtäminen AzCopy-komentorivin apuohjelman avulla](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="a290b-178">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="a290b-179">Microsoft ei tarjoa tallennustiliä Finance and Operations -sopimuksen osana.</span><span class="sxs-lookup"><span data-stu-id="a290b-179">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="a290b-180">Osta tallennustili tai käytä erillisen Azure-tilauksen tallennustiliä.</span><span class="sxs-lookup"><span data-stu-id="a290b-180">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="a290b-181">Ota huomioon Azuren virtuaalikoneiden D-aseman toiminta.</span><span class="sxs-lookup"><span data-stu-id="a290b-181">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="a290b-182">Älä tallenna vietyjä rakenneosaryhmiä pysyvästi D-asemalle. Lisätietoja väliaikaisista asemista on kohdassa [Tietoja Windows Azuren virtuaalikoneiden väliaikaisesta asemasta](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="a290b-182">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="a290b-183">Palveluiden pysäyttäminen</span><span class="sxs-lookup"><span data-stu-id="a290b-183">Stop services</span></span>

<span data-ttu-id="a290b-184">Seuraavilla Microsoft Windows -palveluilla on avoimet yhteydet Finance and Operations -tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="a290b-184">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="a290b-185">Tämän vuoksi kaikkiin ympäristön tietokoneisiin on muodostettava yhteys Microsoftin etätyöpöydän avulla. Palvelut pysäytetään services.msc:n avulla.</span><span class="sxs-lookup"><span data-stu-id="a290b-185">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="a290b-186">WWW-julkaisupalvelu (kaikissa AOS (Application Object Server -palvelimet) -tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="a290b-186">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="a290b-187">Microsoft Dynamics 365 for Finance and Operationsin erähallintapalvelu (vain muissa kuin yksityisissä AOS-tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="a290b-187">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="a290b-188">Management Reporter 2012 Process Service (vain BI (Business intelligence) -tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="a290b-188">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="a290b-189">Palauta</span><span class="sxs-lookup"><span data-stu-id="a290b-189">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="a290b-190">Uusimman MinorVersionDataUpgrade.zip-paketin lataaminen</span><span class="sxs-lookup"><span data-stu-id="a290b-190">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="a290b-191">Lataa uusin MinorVersionDataUpgrade.zip-paketti.</span><span class="sxs-lookup"><span data-stu-id="a290b-191">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="a290b-192">Lisätietoja oikean tietojen päivityspakettiversion etsimisestä ja lataamisesta on kohdassa [Uusimman tietojen päivityksen käyttöönotettavan paketin lataaminen](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span><span class="sxs-lookup"><span data-stu-id="a290b-192">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="a290b-193">MinorVersionDataUpgrade.zip-paketin lataaminen ei edellytä päivitystä.</span><span class="sxs-lookup"><span data-stu-id="a290b-193">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="a290b-194">Seuraa siis ohjeaiheen Uusimman tietojen päivityksen käyttöönotettavan paketin lataaminen -osan vaiheita.</span><span class="sxs-lookup"><span data-stu-id="a290b-194">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="a290b-195">Voit ohittaa ohjeaiheen muut vaiheet.</span><span class="sxs-lookup"><span data-stu-id="a290b-195">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="a290b-196">Komentosarjojen suorittaminen Finance and Operations -tietokannassa</span><span class="sxs-lookup"><span data-stu-id="a290b-196">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="a290b-197">Suorita seuraavat komentosarjat Finance and Operations -tietokannassa (ei taloushallinnon raportointitietokannassa):</span><span class="sxs-lookup"><span data-stu-id="a290b-197">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="a290b-198">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="a290b-198">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="a290b-199">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="a290b-199">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="a290b-200">Näiden komentosarjojen avulla voidaan varmistaa, että käyttäjien, roolien ja muutosten seurannan asetukset on määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="a290b-200">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="a290b-201">Tietokannan palauttaminen Windows PowerShell -komennon suorittamisen avulla</span><span class="sxs-lookup"><span data-stu-id="a290b-201">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="a290b-202">Käynnistä Microsoft Windows PowerShell AOS-tietokoneessa järjestelmänvalvojana ja suorita seuraavat komennot, jos haluat palauttaa Finance and Operationsin ja taloushallinnon raportoinnin väliset integrointiasetukset.</span><span class="sxs-lookup"><span data-stu-id="a290b-202">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="a290b-203">Seuraavassa esitellään **Reset-DatamartIntegration** -komennon parametrit:</span><span class="sxs-lookup"><span data-stu-id="a290b-203">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="a290b-204">**-Reason**-parametrin sallitut arvot ovat **SERVICING**, **BADDATA** ja **OTHER**.</span><span class="sxs-lookup"><span data-stu-id="a290b-204">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="a290b-205">**-ReasonDetail**-parametri on vapaatekstikenttä.</span><span class="sxs-lookup"><span data-stu-id="a290b-205">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="a290b-206">Sekä reason että reason detail tallennetaan telemetria-/ympäristövalvonnassa.</span><span class="sxs-lookup"><span data-stu-id="a290b-206">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="a290b-207">Kun olet suorittanut komennot, sinua pyydetään vahvistamaan tietokannan palauttaminen syöttämällä **Y**.</span><span class="sxs-lookup"><span data-stu-id="a290b-207">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="a290b-208">Palveluiden käynnistäminen uudelleen</span><span class="sxs-lookup"><span data-stu-id="a290b-208">Restart services</span></span>

<span data-ttu-id="a290b-209">Käynnistä aiemmin pysäyttämäsi palvelut uudelleen services.msc:n avulla:</span><span class="sxs-lookup"><span data-stu-id="a290b-209">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="a290b-210">WWW-julkaisupalvelu (kaikissa AOS-tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="a290b-210">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="a290b-211">Microsoft Dynamics 365 for Finance and Operationsin erähallintapalvelu (vain muissa kuin yksityisissä AOS-tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="a290b-211">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="a290b-212">Management Reporter 2012 Process Service (vain BI-tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="a290b-212">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="a290b-213">Raporttimääritysten tuominen</span><span class="sxs-lookup"><span data-stu-id="a290b-213">Import report definitions</span></span>

<span data-ttu-id="a290b-214">Tuo raportin rakenteet raportin luontiohjelmasta käyttämällä viennin aikana luodun tiedoston avulla.</span><span class="sxs-lookup"><span data-stu-id="a290b-214">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="a290b-215">Valitse raportin suunnitteluohjelmassa **Yritys** &gt; **Rakenneosaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="a290b-215">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="a290b-216">Valitse vietävä rakenneosaryhmä ja valitse sitten **Vie**.</span><span class="sxs-lookup"><span data-stu-id="a290b-216">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a290b-217">Finance and Operations tukee vain yhtä **oletusarvoista** rakenneosaryhmää.</span><span class="sxs-lookup"><span data-stu-id="a290b-217">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="a290b-218">Valitse **oletusrakenneosa** ja valitse sitten **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="a290b-218">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="a290b-219">Valitse viedyt raporttimääritykset sisältävä tiedosto ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="a290b-219">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="a290b-220">Valitse **Tuo**-valintaikkunassa tuotavat raporttimääritykset:</span><span class="sxs-lookup"><span data-stu-id="a290b-220">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="a290b-221">Jos haluat tuoda kaikki raporttimääritykset ja niihin liittyvät rakenneosat, valitse **Valitse kaikki**.</span><span class="sxs-lookup"><span data-stu-id="a290b-221">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="a290b-222">Jos haluat tuoda tietyt raportit, rivit, sarakkeet, puut tai dimensioyhdistelmät, valitse tuotavat raportit, rivit, sarakkeet, puut tai dimensioyhdistelmät.</span><span class="sxs-lookup"><span data-stu-id="a290b-222">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="a290b-223">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="a290b-223">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="a290b-224">Finance and Operationsin (paikallinen) taloushallinnon raportoinnin tietovaraston osajoukon palauttaminen</span><span class="sxs-lookup"><span data-stu-id="a290b-224">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="a290b-225">Pyydä kaikkia käyttäjiä poistumaan raportin suunnitteluohjelmasta ja Finance and Operationsin taloushallinnon raportoinnin alueesta.</span><span class="sxs-lookup"><span data-stu-id="a290b-225">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="a290b-226">Suorita seuraava komentosarja taloushallinnon raportoinnin tietokannassa (MRDB).</span><span class="sxs-lookup"><span data-stu-id="a290b-226">Run the following script against the Financial reporting database (MRDB).</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. <span data-ttu-id="a290b-227">Katkaise tai poista FINANCIALREPORTS-taulukon kaikki tietueet Finance and Operations -tietokannassa (AXDB).</span><span class="sxs-lookup"><span data-stu-id="a290b-227">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="a290b-228">Katkaise tai poista FINANCIALREPORTVERSION-taulukon kaikki tietueet, jos taulukko on Finance and Operations -tietokannassa.</span><span class="sxs-lookup"><span data-stu-id="a290b-228">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="a290b-229">Jos Finance and Operations -tietokannassa ei ole tätä taulukkoa, ohita tämä vaihe.</span><span class="sxs-lookup"><span data-stu-id="a290b-229">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="a290b-230">Suorita **ResetDatamart.sql**-komentosarja taloushallinnon raportoinnin tietokannassa.</span><span class="sxs-lookup"><span data-stu-id="a290b-230">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="a290b-231">Tämä komentosarja poistaa tietovaraston osajoukon integroinnin käytöstä, poistaa kaikki tietovaraston osajoukon tiedot ja ottaa lopuksi tietovaraston osajoukon integroinnin uudelleen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="a290b-231">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. <span data-ttu-id="a290b-232">Palauttamisen jälkeen voit tarkistaa tietojen uudelleenlataamisen manuaalisesti, kun suoritat seuraavan kyselyn taloushallinnon raportoinnin tietokannassa.</span><span class="sxs-lookup"><span data-stu-id="a290b-232">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="a290b-233">Varmista, että kaikilla riveillä on **LastRunTime**-arvo ja että **StateType**-kohdan arvoksi on annettu **5**.</span><span class="sxs-lookup"><span data-stu-id="a290b-233">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="a290b-234">**StateType**-kohdan arvo **5** osoittaa, että tietojen uudelleenlataaminen onnistui.</span><span class="sxs-lookup"><span data-stu-id="a290b-234">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="a290b-235">Arvo **7** osoittaa vikatilan.</span><span class="sxs-lookup"><span data-stu-id="a290b-235">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="a290b-236">Joskus organisaatiohierarkian määrityksellä on tämä tila ensimmäisen suorituskerran jälkeen.</span><span class="sxs-lookup"><span data-stu-id="a290b-236">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="a290b-237">Virhetilan tulisi ratketa automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="a290b-237">However, the faulted state but should be automatically resolved.</span></span>

