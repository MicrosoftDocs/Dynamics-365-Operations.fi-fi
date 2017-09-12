---
title: "Talousraportoinnin tietovaraston palauttaminen tietokannan palauttamisen jälkeen"
description: "Tässä ohjeaiheessa kerrotaan, miten talousraportoinnin tietovaraston palautetaan Microsoft Dynamics 365 for Finance and Operations -tietokannan palauttamisen jälkeen."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 08a420a776f47119a5dc47f9119545aa448ffdbd
ms.contentlocale: fi-fi
ms.lasthandoff: 08/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="2fae8-103">Talousraportoinnin tietovaraston palauttaminen tietokannan palauttamisen jälkeen</span><span class="sxs-lookup"><span data-stu-id="2fae8-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2fae8-104">Tässä ohjeaiheessa kerrotaan, miten talousraportoinnin tietovaraston palautetaan Microsoft Dynamics 365 for Finance and Operations -tietokannan palauttamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="2fae8-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="2fae8-105">Jos joskus palautat Finance and Operations -tietokannan varmuuskopiosta tai toisen ympäristön tietokannasta, sinun noudatettava tämän ohjeaiheen ohjeita. Tällä tavoin voit varmistaa, että raportin tietovarasto käyttää oikein palautettua Finance and Operations -tietokantaa.</span><span class="sxs-lookup"><span data-stu-id="2fae8-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> <span data-ttu-id="2fae8-106">Tämän prosessin vaiheita tuetaan Dynamics 365 for Operationsin toukokuun 2016 -versiossa (sovelluksen koontiversio 7.0.1265.23014 ja raportoinnin koontiversio 7.0.10000.4) ja uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="2fae8-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="2fae8-107">Jos käytössä on Finance and Operationsin vanha versio, ota yhteys tukiryhmään.</span><span class="sxs-lookup"><span data-stu-id="2fae8-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="2fae8-108">Raporttimääritysten vieminen</span><span class="sxs-lookup"><span data-stu-id="2fae8-108">Export report definitions</span></span>
<span data-ttu-id="2fae8-109">Vie aluksi Report Designerin raporttirakenteet seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="2fae8-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="2fae8-110">Siirry Report Designerissa kohtaan **Yritys** &gt; **Rakenneosaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="2fae8-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="2fae8-111">Valitse vietävä rakenneosaryhmä ja valitse sitten **Vie**.</span><span class="sxs-lookup"><span data-stu-id="2fae8-111">Select the building block group to export, and click **Export**.</span></span> 
    > [!Note] 
    > <span data-ttu-id="2fae8-112">Finance and Operations tukee vain yhtä **oletusarvoista** rakenneosaryhmää.</span><span class="sxs-lookup"><span data-stu-id="2fae8-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
3.  <span data-ttu-id="2fae8-113">Valitse vietävät raporttimääritykset seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="2fae8-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="2fae8-114">Voit viedä kaikki raporttien määritykset ja liittyvät rakenneosat valitsemalla **Valitse kaikki**.</span><span class="sxs-lookup"><span data-stu-id="2fae8-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="2fae8-115">Voit viedä tiettyjä raportti-, rivi-, sarake-, puu- ja dimensioyhdistelmiä valitsemalla kyseisen välilehden ja valitsemalla sitten vietävät kohteet.</span><span class="sxs-lookup"><span data-stu-id="2fae8-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="2fae8-116">Voit valita useita välilehden kohteita pitämällä Ctrl-näppäintä alhaalla.</span><span class="sxs-lookup"><span data-stu-id="2fae8-116">Press and hold the Ctrl key to select multiple items in a tab.</span></span> <span data-ttu-id="2fae8-117">Kun valitset vietävät raportit, liittyvät rivi-, sarake-, puu- ja dimensioyhdistelmät valitaan myös.</span><span class="sxs-lookup"><span data-stu-id="2fae8-117">When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="2fae8-118">Valitse **Vie**.</span><span class="sxs-lookup"><span data-stu-id="2fae8-118">Click **Export**.</span></span>
5.  <span data-ttu-id="2fae8-119">Anna tiedostonimi ja valitse turvallinen paikka, jonne viedyt raporttimääritykset tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="2fae8-119">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="2fae8-120">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2fae8-120">Click **Save**.</span></span>

<span data-ttu-id="2fae8-121">Tiedosto voidaan kopioida tai ladata turvalliseen paikkaan. Tämän jälkeen se voidaan tuoda toiseen ympäristöön haluttuna ajankohtana.</span><span class="sxs-lookup"><span data-stu-id="2fae8-121">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="2fae8-122">Lisätietoja Microsoft Azure -tallennustilistä on kohdassa [Tietojen siirtäminen AzCopy-komentorivin apuohjelman avulla](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="2fae8-122">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="2fae8-123">Microsoft ei tarjoa tallennustiliä Finance and Operations -sopimuksen osana.</span><span class="sxs-lookup"><span data-stu-id="2fae8-123">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="2fae8-124">Osta tallennustili tai käytä erillisen Azure-tilauksen tallennustiliä.</span><span class="sxs-lookup"><span data-stu-id="2fae8-124">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="2fae8-125">Ota huomioon Azuren virtuaalikoneiden D-aseman toiminta.</span><span class="sxs-lookup"><span data-stu-id="2fae8-125">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="2fae8-126">Älä säilytä vietyjä rakenneosaryhmiä täällä pysyvästi.</span><span class="sxs-lookup"><span data-stu-id="2fae8-126">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="2fae8-127">Lisätietoja väliaikaisista asemista on kohdassa [Tietoja Windows Azuren virtuaalikoneiden väliaikaisesta asemasta](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="2fae8-127">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="2fae8-128">Palveluiden pysäyttäminen</span><span class="sxs-lookup"><span data-stu-id="2fae8-128">Stop services</span></span>
<span data-ttu-id="2fae8-129">Muodosta yhteys kaikkiin ympäristön tietokoneisiin etätyöpöydän avulla. Pysäytä seuraavat Windows-palvelut services.msc:n avulla:</span><span class="sxs-lookup"><span data-stu-id="2fae8-129">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="2fae8-130">WWW-julkaisupalvelu (kaikissa AOS-tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="2fae8-130">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="2fae8-131">Microsoft Dynamics 365 for Finance and Operationsin erähallintapalvelu (vain muissa kuin yksityisissä AOS-tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="2fae8-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="2fae8-132">Management Reporter 2012 Process Service (vain BI-tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="2fae8-132">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="2fae8-133">Näillä palveluilla on avoimet yhteydet Finance and Operations -tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="2fae8-133">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="2fae8-134">Palauta</span><span class="sxs-lookup"><span data-stu-id="2fae8-134">Reset</span></span>
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="2fae8-135">Uusimman MinorVersionDataUpgrade.zip-paketin etsiminen ja lataaminen</span><span class="sxs-lookup"><span data-stu-id="2fae8-135">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="2fae8-136">Etsi uudin MinorVersionDataUpgrade.zip-paketti ohjeaiheessa [Uusimman tietojen päivityksen käyttöönotettavan paketin lataaminen](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package) annettujen ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="2fae8-136">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> <span data-ttu-id="2fae8-137">Ohjeissa kerrotaan, miten tietojen päivityspaketin oikea versio etsitään ja ladataan.</span><span class="sxs-lookup"><span data-stu-id="2fae8-137">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="2fae8-138">Päivitystä ei tarvita MinorVersionDataUpgrade.zip-paketin lataamiseen.</span><span class="sxs-lookup"><span data-stu-id="2fae8-138">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="2fae8-139">MinorVersionDataUpgrade.zip-paketin noutamista varten tarvitsee tehdä vain Uusimman tietojen päivityksen käyttöönotettavan paketin lataaminen -osan vaiheet, ja muut ohjeaiheessa mainitut vaiheet voi jättää tekemättä.</span><span class="sxs-lookup"><span data-stu-id="2fae8-139">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

#### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="2fae8-140">Komentosarjojen suorittaminen Finance and Operations -tietokannassa</span><span class="sxs-lookup"><span data-stu-id="2fae8-140">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="2fae8-141">Suorita seuraavat komentosarjat Finance and Operations -tietokannassa (ei raportointitietokannassa).</span><span class="sxs-lookup"><span data-stu-id="2fae8-141">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="2fae8-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="2fae8-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="2fae8-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="2fae8-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="2fae8-144">Nämä komentosarjat varmistavat, että käyttäjien, roolien ja muutosten seurannan asetukset on määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="2fae8-144">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="2fae8-145">PowerShell-komennon suorittaminen tietokannan palauttamista varten</span><span class="sxs-lookup"><span data-stu-id="2fae8-145">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="2fae8-146">Suorita seuraava komento suoraan AOS-tietokoneessa, jos haluat palauttaa Finance and Operationsin ja raportoinnin väliset integrointiasetukset:</span><span class="sxs-lookup"><span data-stu-id="2fae8-146">Execute the following command, directly on the AOS computer, to reset the integration between Finance and Operations and financial reporting:</span></span>

1.  <span data-ttu-id="2fae8-147">Avaa Windows PowerShell järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="2fae8-147">Open Windows PowerShell as Administrator.</span></span>
2.  <span data-ttu-id="2fae8-148">Suorita: F:</span><span class="sxs-lookup"><span data-stu-id="2fae8-148">Execute: F:</span></span>
3.  <span data-ttu-id="2fae8-149">Suorita: cd F:\\MRApplicationService\\MRInstallDirectory</span><span class="sxs-lookup"><span data-stu-id="2fae8-149">Execute: cd F:\\MRApplicationService\\MRInstallDirectory</span></span>
4.  <span data-ttu-id="2fae8-150">Suorita: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span><span class="sxs-lookup"><span data-stu-id="2fae8-150">Execute: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span></span>
5.  <span data-ttu-id="2fae8-151">Suorita: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span><span class="sxs-lookup"><span data-stu-id="2fae8-151">Execute: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span></span>
    -   <span data-ttu-id="2fae8-152">Vahvista syöttämällä kirjain Y.</span><span class="sxs-lookup"><span data-stu-id="2fae8-152">You will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="2fae8-153">Parametrien selitys:</span><span class="sxs-lookup"><span data-stu-id="2fae8-153">Explanation of parameters:</span></span>

-   <span data-ttu-id="2fae8-154">Reason-parametrin sallitut arvot ovat SERVICING, BADDATA, OTHER.</span><span class="sxs-lookup"><span data-stu-id="2fae8-154">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="2fae8-155">ReasonDetail-parametri on vapaatekstikenttä.</span><span class="sxs-lookup"><span data-stu-id="2fae8-155">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="2fae8-156">Sekä reason että reasonDetail tallennetaan telemetria-/ympäristövalvonnassa.</span><span class="sxs-lookup"><span data-stu-id="2fae8-156">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="2fae8-157">Palveluiden käynnistäminen</span><span class="sxs-lookup"><span data-stu-id="2fae8-157">Start services</span></span>
<span data-ttu-id="2fae8-158">Käynnistä aiemmin pysäyttämäsi palvelut uudelleen services.msc:n avulla:</span><span class="sxs-lookup"><span data-stu-id="2fae8-158">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="2fae8-159">WWW-julkaisupalvelu (kaikissa AOS-tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="2fae8-159">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="2fae8-160">Microsoft Dynamics 365 for Finance and Operationsin erähallintapalvelu (vain muissa kuin yksityisissä AOS-tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="2fae8-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="2fae8-161">Management Reporter 2012 Process Service (vain BI-tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="2fae8-161">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="2fae8-162">Raporttimääritysten tuominen</span><span class="sxs-lookup"><span data-stu-id="2fae8-162">Import report definitions</span></span>
<span data-ttu-id="2fae8-163">Tuo raporttimallit Report Designerista viennin aikana luotua tiedostoa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="2fae8-163">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="2fae8-164">Siirry Report Designerissa kohtaan **Yritys** &gt; **Rakenneosaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="2fae8-164">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="2fae8-165">Valitse vietävä rakenneosaryhmä ja valitse sitten **Vie**.</span><span class="sxs-lookup"><span data-stu-id="2fae8-165">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="2fae8-166">Finance and Operations tukee vain yhtä **oletusarvoista** rakenneosaryhmää.</span><span class="sxs-lookup"><span data-stu-id="2fae8-166">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="2fae8-167">Valitse **oletusrakenneosa** ja valitse sitten **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="2fae8-167">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="2fae8-168">Valitse viedyt raporttimääritykset sisältävä tiedosto ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="2fae8-168">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="2fae8-169">Valitse Tuo-valintaikkunassa tuotavat raporttien määritykset.</span><span class="sxs-lookup"><span data-stu-id="2fae8-169">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="2fae8-170">Voit tuoda kaikki raporttien määritykset ja niitä tukevat rakenneosat valitsemalla **Valitse kaikki**.</span><span class="sxs-lookup"><span data-stu-id="2fae8-170">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="2fae8-171">Voit tuoda tiettyjä raportti-, rivi-, sarake-, puu- tai dimensioyhdistelmiä valitsemalla tuotavat raportti-, rivi-, sarake-, puu- tai dimensioyhdistelmät.</span><span class="sxs-lookup"><span data-stu-id="2fae8-171">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="2fae8-172">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="2fae8-172">Click **Import**.</span></span>





