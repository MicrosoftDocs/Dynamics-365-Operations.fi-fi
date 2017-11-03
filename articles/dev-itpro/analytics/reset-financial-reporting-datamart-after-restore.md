---
title: "Talousraportoinnin tietovaraston palauttaminen tietokannan palauttamisen jälkeen"
description: "Tässä ohjeaiheessa kerrotaan, miten talousraportoinnin tietovaraston palautetaan Microsoft Dynamics 365 for Finance and Operations -tietokannan palauttamisen jälkeen."
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6e3f78fb2f6528449d2a411225cd0e14ca33443e
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="e61ae-103">Talousraportoinnin tietovaraston palauttaminen tietokannan palauttamisen jälkeen</span><span class="sxs-lookup"><span data-stu-id="e61ae-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e61ae-104">Tässä ohjeaiheessa kerrotaan, miten talousraportoinnin tietovaraston palautetaan Microsoft Dynamics 365 for Finance and Operations -tietokannan palauttamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="e61ae-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="e61ae-105">Jos joskus palautat Finance and Operations -tietokannan varmuuskopiosta tai toisen ympäristön tietokannasta, sinun noudatettava tämän ohjeaiheen ohjeita. Tällä tavoin voit varmistaa, että raportin tietovarasto käyttää oikein palautettua Finance and Operations -tietokantaa.</span><span class="sxs-lookup"><span data-stu-id="e61ae-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
> [!Note] 
> <span data-ttu-id="e61ae-106">Tämän prosessin vaiheita tuetaan Dynamics 365 for Operationsin toukokuun 2016 -versiossa (sovelluksen koontiversio 7.0.1265.23014 ja raportoinnin koontiversio 7.0.10000.4) ja uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="e61ae-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="e61ae-107">Jos käytössä on Finance and Operationsin vanha versio, ota yhteys tukiryhmään.</span><span class="sxs-lookup"><span data-stu-id="e61ae-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="e61ae-108">Raporttimääritysten vieminen</span><span class="sxs-lookup"><span data-stu-id="e61ae-108">Export report definitions</span></span>
<span data-ttu-id="e61ae-109">Vie aluksi Report Designerin raporttirakenteet seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e61ae-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="e61ae-110">Siirry Report Designerissa kohtaan **Yritys** &gt; **Rakenneosaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="e61ae-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="e61ae-111">Valitse vietävä rakenneosaryhmä ja valitse sitten **Vie**.</span><span class="sxs-lookup"><span data-stu-id="e61ae-111">Select the building block group to export, and click **Export**.</span></span> 

    > [!Note] 
    > <span data-ttu-id="e61ae-112">Finance and Operations tukee vain yhtä **oletusarvoista** rakenneosaryhmää.</span><span class="sxs-lookup"><span data-stu-id="e61ae-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="e61ae-113">Valitse vietävät raporttimääritykset seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e61ae-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="e61ae-114">Voit viedä kaikki raporttien määritykset ja liittyvät rakenneosat valitsemalla **Valitse kaikki**.</span><span class="sxs-lookup"><span data-stu-id="e61ae-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="e61ae-115">Voit viedä tiettyjä raportti-, rivi-, sarake-, puu- ja dimensioyhdistelmiä valitsemalla kyseisen välilehden ja valitsemalla sitten vietävät kohteet.</span><span class="sxs-lookup"><span data-stu-id="e61ae-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="e61ae-116">Voit valita välilehdessä useita kohteita pitämällä Ctrl-näppäintä alhaalla. Kun valitset vietävät raportit, niihin liittyvät rivit, sarakkeet, puut ja dimensioyhdistelmät tulevat valituiksi.</span><span class="sxs-lookup"><span data-stu-id="e61ae-116">Press and hold the Ctrl key to select multiple items in a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="e61ae-117">Valitse **Vie**.</span><span class="sxs-lookup"><span data-stu-id="e61ae-117">Click **Export**.</span></span>
5.  <span data-ttu-id="e61ae-118">Anna tiedostonimi ja valitse turvallinen paikka, jonne viedyt raporttimääritykset tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="e61ae-118">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="e61ae-119">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e61ae-119">Click **Save**.</span></span>

<span data-ttu-id="e61ae-120">Tiedosto voidaan kopioida tai ladata turvalliseen paikkaan. Tämän jälkeen se voidaan tuoda toiseen ympäristöön haluttuna ajankohtana.</span><span class="sxs-lookup"><span data-stu-id="e61ae-120">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="e61ae-121">Lisätietoja Microsoft Azure -tallennustilistä on kohdassa [Tietojen siirtäminen AzCopy-komentorivin apuohjelman avulla](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="e61ae-121">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="e61ae-122">Microsoft ei tarjoa tallennustiliä Finance and Operations -sopimuksen osana.</span><span class="sxs-lookup"><span data-stu-id="e61ae-122">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="e61ae-123">Osta tallennustili tai käytä erillisen Azure-tilauksen tallennustiliä.</span><span class="sxs-lookup"><span data-stu-id="e61ae-123">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="e61ae-124">Ota huomioon Azuren virtuaalikoneiden D-aseman toiminta.</span><span class="sxs-lookup"><span data-stu-id="e61ae-124">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="e61ae-125">Älä säilytä vietyjä rakenneosaryhmiä täällä pysyvästi.</span><span class="sxs-lookup"><span data-stu-id="e61ae-125">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="e61ae-126">Lisätietoja väliaikaisista asemista on kohdassa [Tietoja Windows Azuren virtuaalikoneiden väliaikaisesta asemasta](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="e61ae-126">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="e61ae-127">Palveluiden pysäyttäminen</span><span class="sxs-lookup"><span data-stu-id="e61ae-127">Stop services</span></span>
<span data-ttu-id="e61ae-128">Muodosta yhteys kaikkiin ympäristön tietokoneisiin etätyöpöydän avulla. Pysäytä seuraavat Windows-palvelut services.msc:n avulla:</span><span class="sxs-lookup"><span data-stu-id="e61ae-128">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="e61ae-129">WWW-julkaisupalvelu (kaikissa AOS-tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="e61ae-129">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="e61ae-130">Microsoft Dynamics 365 for Finance and Operationsin erähallintapalvelu (vain muissa kuin yksityisissä AOS-tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="e61ae-130">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="e61ae-131">Management Reporter 2012 Process Service (vain BI-tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="e61ae-131">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="e61ae-132">Näillä palveluilla on avoimet yhteydet Finance and Operations -tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="e61ae-132">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="e61ae-133">Palauta</span><span class="sxs-lookup"><span data-stu-id="e61ae-133">Reset</span></span>
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="e61ae-134">Uusimman MinorVersionDataUpgrade.zip-paketin etsiminen ja lataaminen</span><span class="sxs-lookup"><span data-stu-id="e61ae-134">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="e61ae-135">Etsi uudin MinorVersionDataUpgrade.zip-paketti ohjeaiheessa [Uusimman tietojen päivityksen käyttöönotettavan paketin lataaminen](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages) annettujen ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e61ae-135">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="e61ae-136">Ohjeissa kerrotaan, miten tietojen päivityspaketin oikea versio etsitään ja ladataan.</span><span class="sxs-lookup"><span data-stu-id="e61ae-136">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="e61ae-137">Päivitystä ei tarvita MinorVersionDataUpgrade.zip-paketin lataamiseen.</span><span class="sxs-lookup"><span data-stu-id="e61ae-137">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="e61ae-138">MinorVersionDataUpgrade.zip-paketin noutamista varten tarvitsee tehdä vain Uusimman tietojen päivityksen käyttöönotettavan paketin lataaminen -osan vaiheet, ja muut ohjeaiheessa mainitut vaiheet voi jättää tekemättä.</span><span class="sxs-lookup"><span data-stu-id="e61ae-138">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="e61ae-139">Komentosarjojen suorittaminen Finance and Operations -tietokannassa</span><span class="sxs-lookup"><span data-stu-id="e61ae-139">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="e61ae-140">Suorita seuraavat komentosarjat Finance and Operations -tietokannassa (ei raportointitietokannassa).</span><span class="sxs-lookup"><span data-stu-id="e61ae-140">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="e61ae-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="e61ae-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="e61ae-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="e61ae-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="e61ae-143">Nämä komentosarjat varmistavat, että käyttäjien, roolien ja muutosten seurannan asetukset on määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="e61ae-143">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="e61ae-144">PowerShell-komennon suorittaminen tietokannan palauttamista varten</span><span class="sxs-lookup"><span data-stu-id="e61ae-144">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="e61ae-145">Suorita seuraava PowerShell-komento järjstelmänvalvojana suoraan AOS-tietokoneessa, jos haluat palauttaa Finance and Operationsin ja raportoinnin väliset integrointiasetukset:</span><span class="sxs-lookup"><span data-stu-id="e61ae-145">On the AOS computer, execute the following commands in PowerShell as an Administrator to reset the integration between Finance and Operations and financial reporting:</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> <span data-ttu-id="e61ae-146">Vahvista syöttämällä kirjain Y komennon suorittamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="e61ae-146">After executing the commands, you will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="e61ae-147">Parametrien selitys:</span><span class="sxs-lookup"><span data-stu-id="e61ae-147">Explanation of parameters:</span></span>

-   <span data-ttu-id="e61ae-148">Reason-parametrin sallitut arvot ovat SERVICING, BADDATA, OTHER.</span><span class="sxs-lookup"><span data-stu-id="e61ae-148">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="e61ae-149">ReasonDetail-parametri on vapaatekstikenttä.</span><span class="sxs-lookup"><span data-stu-id="e61ae-149">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="e61ae-150">Sekä reason että reasonDetail tallennetaan telemetria-/ympäristövalvonnassa.</span><span class="sxs-lookup"><span data-stu-id="e61ae-150">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="e61ae-151">Palveluiden käynnistäminen</span><span class="sxs-lookup"><span data-stu-id="e61ae-151">Start services</span></span>
<span data-ttu-id="e61ae-152">Käynnistä aiemmin pysäyttämäsi palvelut uudelleen services.msc:n avulla:</span><span class="sxs-lookup"><span data-stu-id="e61ae-152">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="e61ae-153">WWW-julkaisupalvelu (kaikissa AOS-tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="e61ae-153">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="e61ae-154">Microsoft Dynamics 365 for Finance and Operationsin erähallintapalvelu (vain muissa kuin yksityisissä AOS-tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="e61ae-154">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="e61ae-155">Management Reporter 2012 Process Service (vain BI-tietokoneissa)</span><span class="sxs-lookup"><span data-stu-id="e61ae-155">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="e61ae-156">Raporttimääritysten tuominen</span><span class="sxs-lookup"><span data-stu-id="e61ae-156">Import report definitions</span></span>
<span data-ttu-id="e61ae-157">Tuo raporttimallit Report Designerista viennin aikana luotua tiedostoa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e61ae-157">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="e61ae-158">Siirry Report Designerissa kohtaan **Yritys** &gt; **Rakenneosaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="e61ae-158">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="e61ae-159">Valitse vietävä rakenneosaryhmä ja valitse sitten **Vie**.</span><span class="sxs-lookup"><span data-stu-id="e61ae-159">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="e61ae-160">Finance and Operations tukee vain yhtä **oletusarvoista** rakenneosaryhmää.</span><span class="sxs-lookup"><span data-stu-id="e61ae-160">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="e61ae-161">Valitse **oletusrakenneosa** ja valitse sitten **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="e61ae-161">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="e61ae-162">Valitse viedyt raporttimääritykset sisältävä tiedosto ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="e61ae-162">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="e61ae-163">Valitse Tuo-valintaikkunassa tuotavat raporttien määritykset.</span><span class="sxs-lookup"><span data-stu-id="e61ae-163">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="e61ae-164">Voit tuoda kaikki raporttien määritykset ja niitä tukevat rakenneosat valitsemalla **Valitse kaikki**.</span><span class="sxs-lookup"><span data-stu-id="e61ae-164">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="e61ae-165">Voit tuoda tiettyjä raportti-, rivi-, sarake-, puu- tai dimensioyhdistelmiä valitsemalla tuotavat raportti-, rivi-, sarake-, puu- tai dimensioyhdistelmät.</span><span class="sxs-lookup"><span data-stu-id="e61ae-165">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="e61ae-166">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="e61ae-166">Click **Import**.</span></span>





