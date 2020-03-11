---
title: Pankin tiliotteen tiedoston tuomisen vianmääritys
description: On tärkeää, että pankin tiliotetiedosto vastaa asetteluja, jotka ovat tuettuja Microsoft Dynamics 365 Financessa. Tiliotteiden tiukkojen standardien vuoksi suurin osa integraatioista toimii oikein. Kuitenkin joskus tiliotetiedostoa ei voi tuoda tai se sisältää virheellisiä tuloksia. Yleensä ongelmat johtuvat pienistä eroista tiliotetiedostossa. Tässä artikkelissa selitetään, miten nämä erot ja niistä johtuvat ongelmat korjataan.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5e7e6897f19dc0303ffbd3111f93669a91daa1b
ms.sourcegitcommit: 4f668b23f5bfc6d6502858850d2ed59d7a79cfbb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/14/2020
ms.locfileid: "3059373"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="e850a-107">Pankin tiliotteen tiedoston tuomisen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="e850a-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e850a-108">On tärkeää, että pankin tiliotetiedosto vastaa asetteluja, jotka ovat tuettuja Microsoft Dynamics 365 Financessa.</span><span class="sxs-lookup"><span data-stu-id="e850a-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="e850a-109">Tiliotteiden tiukkojen standardien vuoksi suurin osa integraatioista toimii oikein.</span><span class="sxs-lookup"><span data-stu-id="e850a-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="e850a-110">Kuitenkin joskus tiliotetiedostoa ei voi tuoda tai se sisältää virheellisiä tuloksia.</span><span class="sxs-lookup"><span data-stu-id="e850a-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="e850a-111">Yleensä ongelmat johtuvat pienistä eroista tiliotetiedostossa.</span><span class="sxs-lookup"><span data-stu-id="e850a-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="e850a-112">Tässä artikkelissa selitetään, miten nämä erot ja niistä johtuvat ongelmat korjataan.</span><span class="sxs-lookup"><span data-stu-id="e850a-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="e850a-113">Mikä virhe on kyseessä?</span><span class="sxs-lookup"><span data-stu-id="e850a-113">What is the error?</span></span>
------------------

<span data-ttu-id="e850a-114">Kun tiliotetiedoston tuontia on yritetty, siirry Tietojen hallinnan työhistoriaan ja sen suoritustietoihin löytääksesi virheen.</span><span class="sxs-lookup"><span data-stu-id="e850a-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="e850a-115">Virhe voi auttaa osoittamalla tiliotteeseen, saldoon tai tiliotteen riviin.</span><span class="sxs-lookup"><span data-stu-id="e850a-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="e850a-116">Se ei kuitenkaan todennäköisesti anna riittävästi tietoa, jotta ongelman aiheuttavan kentän tai elementin voisi tunnistaa.</span><span class="sxs-lookup"><span data-stu-id="e850a-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="e850a-117">Mitä ovat erot?</span><span class="sxs-lookup"><span data-stu-id="e850a-117">What are the differences?</span></span>
<span data-ttu-id="e850a-118">Vertaa pankkitiedoston asettelumääritystä Financen tuontimääritykseen ja kiinnitä huomiota kenttien ja elementtien eroihin.</span><span class="sxs-lookup"><span data-stu-id="e850a-118">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="e850a-119">Vertaa tiliotetiedostoa liittyvään Finance-näytetiedostoon.</span><span class="sxs-lookup"><span data-stu-id="e850a-119">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="e850a-120">ISO20022-tiedostoissa on erot helppo nähdä.</span><span class="sxs-lookup"><span data-stu-id="e850a-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="e850a-121">Tuotujen tililaskelmien aikavyöhyke-erot</span><span class="sxs-lookup"><span data-stu-id="e850a-121">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="e850a-122">Tuontitiedoston päivämäärän ja ajan arvot voivat poiketa Finance and Operationsin päivämäärä- ja aika-arvoista.</span><span class="sxs-lookup"><span data-stu-id="e850a-122">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="e850a-123">Voit estää tämän ristiriidan määrittämällä aikavyöhykeasetukset **Määritä tietolähteet** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e850a-123">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="e850a-124">Lisätietoja aikavyöhyke asetusten määrittämisestä on kohdassa [Pankin täsmäytyksen lisätuontiprosessin määrittäminen](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="e850a-124">See [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md) for more information about entering a time zone preference.</span></span>

## <a name="transformations"></a><span data-ttu-id="e850a-125">Muunnokset</span><span class="sxs-lookup"><span data-stu-id="e850a-125">Transformations</span></span>
<span data-ttu-id="e850a-126">Yleensä muutokset on tehtävä johonkin kolmesta muunnoksesta.</span><span class="sxs-lookup"><span data-stu-id="e850a-126">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="e850a-127">Jokaisen muunnos on kirjoitettu tiettyyn standardiin.</span><span class="sxs-lookup"><span data-stu-id="e850a-127">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="e850a-128">Resurssin nimi</span><span class="sxs-lookup"><span data-stu-id="e850a-128">Resource name</span></span>                                         | <span data-ttu-id="e850a-129">Tiedostonimi</span><span class="sxs-lookup"><span data-stu-id="e850a-129">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="e850a-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="e850a-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="e850a-131">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="e850a-131">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="e850a-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="e850a-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="e850a-133">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="e850a-133">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="e850a-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="e850a-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="e850a-135">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="e850a-135">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="e850a-136">Muunnosten virheenkorjaus</span><span class="sxs-lookup"><span data-stu-id="e850a-136">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="e850a-137">Oikaise BAI2- ja MT940-tiedostot</span><span class="sxs-lookup"><span data-stu-id="e850a-137">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="e850a-138">BAI2- ja MT940-tiedostot ovat tekstiin perustuvia tiedostoja ja ne on oikaistava, jotta Extensible Stylesheet Language Transformation -kielen (XSLT) virheenkorjauksen voi ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="e850a-138">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="e850a-139">Ohjelma tekee oikaisun, kun tiedosto tuodaan.</span><span class="sxs-lookup"><span data-stu-id="e850a-139">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="e850a-140">Luo XML-tiedosto ja kopioi siihen seuraava tekstinkatkelma.</span><span class="sxs-lookup"><span data-stu-id="e850a-140">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="e850a-141">Kopioi tiliotetiedoston sisältö ja liitä se XML-tiedostoon niin, että ne korvaavat **PASTESTATEMENTFILEHERE**-kohdan.</span><span class="sxs-lookup"><span data-stu-id="e850a-141">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="e850a-142">XSLT-virheenkorjaus</span><span class="sxs-lookup"><span data-stu-id="e850a-142">Debug the XSLT</span></span>

<span data-ttu-id="e850a-143">Lisätietoja on kohdassa <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="e850a-143">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="e850a-144">Käynnistä Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e850a-144">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="e850a-145">Luo konsolisovellus.</span><span class="sxs-lookup"><span data-stu-id="e850a-145">Create a console application.</span></span>
3.  <span data-ttu-id="e850a-146">Avaa haluamasi XSLT-muoto.</span><span class="sxs-lookup"><span data-stu-id="e850a-146">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="e850a-147">Valitse XSLT-muotoa ja sen ominaisuussivua.</span><span class="sxs-lookup"><span data-stu-id="e850a-147">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="e850a-148">Aseta syötteeksi tiliotetiedoston sijainti.</span><span class="sxs-lookup"><span data-stu-id="e850a-148">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="e850a-149">Määritä tulosteelle sijainti ja tiedostonimi.</span><span class="sxs-lookup"><span data-stu-id="e850a-149">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="e850a-150">Määritä tarvittavat katkaisukohdat.</span><span class="sxs-lookup"><span data-stu-id="e850a-150">Set the required break points.</span></span>
8.  <span data-ttu-id="e850a-151">Valitse valikosta **XML** &gt; **Aloita XSLT-virheenkorjaus**.</span><span class="sxs-lookup"><span data-stu-id="e850a-151">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="e850a-152">Muotoile XSLT-tuloste</span><span class="sxs-lookup"><span data-stu-id="e850a-152">Format the XSLT output</span></span>

<span data-ttu-id="e850a-153">Kun muunnos ajetaan, se luo tiedoston, jonka voi avata Visual Studiossa.</span><span class="sxs-lookup"><span data-stu-id="e850a-153">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="e850a-154">Voit muotoilla tiedoston nopeasti Ctrl+A, Ctrl+K ja Ctrl+D -näppäinkomennoilla.</span><span class="sxs-lookup"><span data-stu-id="e850a-154">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="e850a-155">Muunnoksen oikaiseminen</span><span class="sxs-lookup"><span data-stu-id="e850a-155">Adjust the transformation</span></span>

<span data-ttu-id="e850a-156">Oikaise muunnos saadaksesi haluamasi kentän tai elementin tiliotetiedostoon.</span><span class="sxs-lookup"><span data-stu-id="e850a-156">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="e850a-157">Määritä sitten kyseinen kenttä tai elementti asiaankuuluvaan Finance-elementtiin.</span><span class="sxs-lookup"><span data-stu-id="e850a-157">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="e850a-158">Debet/kredit-ilmaisin</span><span class="sxs-lookup"><span data-stu-id="e850a-158">Debit/credit indicator</span></span>

<span data-ttu-id="e850a-159">Toisinaan on mahdollista, että veloitukset on tuotu hyvityksinä ja hyvitykset veloituksina.</span><span class="sxs-lookup"><span data-stu-id="e850a-159">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="e850a-160">Tämän ongelman ratkaisemiseksi on muutettava asiaankuuluvaa XSLT:tä.</span><span class="sxs-lookup"><span data-stu-id="e850a-160">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="e850a-161">Jos tiliotteet ovat peräisin useasta pankista, varmista, että kaikissa käytetään samaa debet-/kredit-lähestymistapaa tai luo niille erilliset muunnokseet.</span><span class="sxs-lookup"><span data-stu-id="e850a-161">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="e850a-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator -malli</span><span class="sxs-lookup"><span data-stu-id="e850a-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="e850a-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit -malli</span><span class="sxs-lookup"><span data-stu-id="e850a-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="e850a-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator -malli</span><span class="sxs-lookup"><span data-stu-id="e850a-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="e850a-165">Esimerkkejä tiliotteiden muodoista ja teknisistä asetteluista</span><span class="sxs-lookup"><span data-stu-id="e850a-165">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="e850a-166">Seuraavassa taulukossa on esimerkkejä tuonnin lisäasetuksista pankkitilin täsmäytystietojen tuontitiedoston teknisistä asettelumäärityksistä sekä kolme esimerkkitiliotetiedostoa:</span><span class="sxs-lookup"><span data-stu-id="e850a-166">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="e850a-167">Voit ladata esimerkkitiedostot ja tekniset asettelut täällä: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="e850a-167">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="e850a-168">Tekninen asettelumääritys</span><span class="sxs-lookup"><span data-stu-id="e850a-168">Technical layout definition</span></span>                             | <span data-ttu-id="e850a-169">Esimerkkitiliotetiedosto</span><span class="sxs-lookup"><span data-stu-id="e850a-169">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="e850a-170">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="e850a-170">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="e850a-171">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="e850a-171">MT940StatementExample</span></span>                |
| <span data-ttu-id="e850a-172">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="e850a-172">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="e850a-173">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="e850a-173">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="e850a-174">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="e850a-174">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="e850a-175">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="e850a-175">BAI2StatementExample</span></span>                 |





