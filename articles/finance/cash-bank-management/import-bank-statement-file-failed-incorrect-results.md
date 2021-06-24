---
title: Pankin tiliotteen tiedoston tuomisen vianmääritys
description: On tärkeää, että pankin tiliotetiedosto vastaa asetteluja, jotka ovat tuettuja Microsoft Dynamics 365 Financessa. Tiliotteiden tiukkojen standardien vuoksi suurin osa integraatioista toimii oikein. Kuitenkin joskus tiliotetiedostoa ei voi tuoda tai se sisältää virheellisiä tuloksia. Yleensä ongelmat johtuvat pienistä eroista tiliotetiedostossa. Tässä artikkelissa selitetään, miten nämä erot ja niistä johtuvat ongelmat korjataan.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14f0e480b93e663f81db5a1edb2ae71b559bb05e
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188556"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="4de03-107">Pankin tiliotteen tiedoston tuomisen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="4de03-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4de03-108">On tärkeää, että pankin tiliotetiedosto vastaa asetteluja, jotka ovat tuettuja Microsoft Dynamics 365 Financessa.</span><span class="sxs-lookup"><span data-stu-id="4de03-108">It's important that the bank statement file from the bank matches the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="4de03-109">Tiliotteiden tiukkojen standardien vuoksi suurin osa integraatioista toimii oikein.</span><span class="sxs-lookup"><span data-stu-id="4de03-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="4de03-110">Kuitenkin joskus tiliotetiedostoa ei voi tuoda tai se sisältää virheellisiä tuloksia.</span><span class="sxs-lookup"><span data-stu-id="4de03-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="4de03-111">Yleensä ongelmat johtuvat pienistä eroista tiliotetiedostossa.</span><span class="sxs-lookup"><span data-stu-id="4de03-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="4de03-112">Tässä artikkelissa selitetään, miten nämä erot ja niistä johtuvat ongelmat korjataan.</span><span class="sxs-lookup"><span data-stu-id="4de03-112">This article explains how to fix these differences and resolve the issues.</span></span>

## <a name="what-is-the-error"></a><span data-ttu-id="4de03-113">Mikä virhe on kyseessä?</span><span class="sxs-lookup"><span data-stu-id="4de03-113">What is the error?</span></span>

<span data-ttu-id="4de03-114">Kun tiliotetiedoston tuontia on yritetty, siirry Tietojen hallinnan työhistoriaan ja sen suoritustietoihin löytääksesi virheen.</span><span class="sxs-lookup"><span data-stu-id="4de03-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="4de03-115">Virhe voi auttaa osoittamalla tiliotteeseen, saldoon tai tiliotteen riviin.</span><span class="sxs-lookup"><span data-stu-id="4de03-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="4de03-116">Se ei kuitenkaan todennäköisesti anna riittävästi tietoa, jotta ongelman aiheuttavan kentän tai elementin voisi tunnistaa.</span><span class="sxs-lookup"><span data-stu-id="4de03-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="4de03-117">Tuodut tiliotteet voivat olla päällekkäisiä vain yhdelle aikapisteelle.</span><span class="sxs-lookup"><span data-stu-id="4de03-117">Imported bank statements can overlap only for single a point in time.</span></span>  <span data-ttu-id="4de03-118">Jos esimerkiksi tiliote päättyy 1.1.2021 klo 00.00, seuraavan tiliotteen alkamispäivä voi olla 1.1.2021 klo 00:00.</span><span class="sxs-lookup"><span data-stu-id="4de03-118">For example, if a statement ends at 12:00 AM on January 1, 2021, then beginning date for the next statement can be 12:00 AM on Jarnuary 1, 2021 12:00:00 AM.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="4de03-119">Mitä ovat erot?</span><span class="sxs-lookup"><span data-stu-id="4de03-119">What are the differences?</span></span>
<span data-ttu-id="4de03-120">Vertaa pankkitiedoston asettelumääritystä Financen tuontimääritykseen ja kiinnitä huomiota kenttien ja elementtien eroihin.</span><span class="sxs-lookup"><span data-stu-id="4de03-120">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="4de03-121">Vertaa tiliotetiedostoa liittyvään Finance-näytetiedostoon.</span><span class="sxs-lookup"><span data-stu-id="4de03-121">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="4de03-122">ISO20022-tiedostoissa on erot helppo nähdä.</span><span class="sxs-lookup"><span data-stu-id="4de03-122">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="4de03-123">Tuotujen tililaskelmien aikavyöhyke-erot</span><span class="sxs-lookup"><span data-stu-id="4de03-123">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="4de03-124">Tuontitiedoston päivämäärän ja ajan arvot voivat poiketa Finance and Operationsin päivämäärä- ja aika-arvoista.</span><span class="sxs-lookup"><span data-stu-id="4de03-124">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="4de03-125">Voit estää tämän ristiriidan määrittämällä aikavyöhykeasetukset **Määritä tietolähteet** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4de03-125">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="4de03-126">Lisätietoja aikavyöhyke asetusten määrittämisestä on kohdassa [Pankin täsmäytyksen lisätuontiprosessin määrittäminen](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="4de03-126">For more information about entering a time zone preference, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>

## <a name="transformations"></a><span data-ttu-id="4de03-127">Muunnokset</span><span class="sxs-lookup"><span data-stu-id="4de03-127">Transformations</span></span>
<span data-ttu-id="4de03-128">Yleensä muutokset on tehtävä johonkin kolmesta muunnoksesta.</span><span class="sxs-lookup"><span data-stu-id="4de03-128">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="4de03-129">Jokaisen muunnos on kirjoitettu tiettyyn standardiin.</span><span class="sxs-lookup"><span data-stu-id="4de03-129">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="4de03-130">Resurssin nimi</span><span class="sxs-lookup"><span data-stu-id="4de03-130">Resource name</span></span>                                         | <span data-ttu-id="4de03-131">Tiedostonimi</span><span class="sxs-lookup"><span data-stu-id="4de03-131">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="4de03-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="4de03-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="4de03-133">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="4de03-133">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="4de03-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="4de03-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="4de03-135">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="4de03-135">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="4de03-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="4de03-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="4de03-137">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="4de03-137">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="4de03-138">Muunnosten virheenkorjaus</span><span class="sxs-lookup"><span data-stu-id="4de03-138">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="4de03-139">Oikaise BAI2- ja MT940-tiedostot</span><span class="sxs-lookup"><span data-stu-id="4de03-139">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="4de03-140">BAI2- ja MT940-tiedostot ovat tekstiin perustuvia tiedostoja ja ne on oikaistava, jotta Extensible Stylesheet Language Transformation -kielen (XSLT) virheenkorjauksen voi ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4de03-140">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="4de03-141">Ohjelma tekee oikaisun, kun tiedosto tuodaan.</span><span class="sxs-lookup"><span data-stu-id="4de03-141">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="4de03-142">Luo XML-tiedosto ja kopioi siihen seuraava tekstinkatkelma.</span><span class="sxs-lookup"><span data-stu-id="4de03-142">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="4de03-143">Kopioi tiliotetiedoston sisältö ja liitä se XML-tiedostoon niin, että ne korvaavat **PASTESTATEMENTFILEHERE**-kohdan.</span><span class="sxs-lookup"><span data-stu-id="4de03-143">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="4de03-144">XSLT-virheenkorjaus</span><span class="sxs-lookup"><span data-stu-id="4de03-144">Debug the XSLT</span></span>

<span data-ttu-id="4de03-145">Lisätietoja on kohdassa <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="4de03-145">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="4de03-146">Käynnistä Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4de03-146">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="4de03-147">Luo konsolisovellus.</span><span class="sxs-lookup"><span data-stu-id="4de03-147">Create a console application.</span></span>
3.  <span data-ttu-id="4de03-148">Avaa haluamasi XSLT-muoto.</span><span class="sxs-lookup"><span data-stu-id="4de03-148">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="4de03-149">Valitse XSLT-muotoa ja sen ominaisuussivua.</span><span class="sxs-lookup"><span data-stu-id="4de03-149">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="4de03-150">Aseta syötteeksi tiliotetiedoston sijainti.</span><span class="sxs-lookup"><span data-stu-id="4de03-150">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="4de03-151">Määritä tulosteelle sijainti ja tiedostonimi.</span><span class="sxs-lookup"><span data-stu-id="4de03-151">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="4de03-152">Määritä tarvittavat katkaisukohdat.</span><span class="sxs-lookup"><span data-stu-id="4de03-152">Set the required break points.</span></span>
8.  <span data-ttu-id="4de03-153">Valitse valikosta **XML** &gt; **Aloita XSLT-virheenkorjaus**.</span><span class="sxs-lookup"><span data-stu-id="4de03-153">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="4de03-154">Muotoile XSLT-tuloste</span><span class="sxs-lookup"><span data-stu-id="4de03-154">Format the XSLT output</span></span>

<span data-ttu-id="4de03-155">Kun muunnos ajetaan, se luo tiedoston, jonka voi avata Visual Studiossa.</span><span class="sxs-lookup"><span data-stu-id="4de03-155">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="4de03-156">Voit muotoilla tiedoston nopeasti Ctrl+A, Ctrl+K ja Ctrl+D -näppäinkomennoilla.</span><span class="sxs-lookup"><span data-stu-id="4de03-156">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="4de03-157">Muunnoksen oikaiseminen</span><span class="sxs-lookup"><span data-stu-id="4de03-157">Adjust the transformation</span></span>

<span data-ttu-id="4de03-158">Oikaise muunnos saadaksesi haluamasi kentän tai elementin tiliotetiedostoon.</span><span class="sxs-lookup"><span data-stu-id="4de03-158">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="4de03-159">Määritä sitten kyseinen kenttä tai elementti asiaankuuluvaan Finance-elementtiin.</span><span class="sxs-lookup"><span data-stu-id="4de03-159">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="4de03-160">Debet/kredit-ilmaisin</span><span class="sxs-lookup"><span data-stu-id="4de03-160">Debit/credit indicator</span></span>

<span data-ttu-id="4de03-161">Toisinaan on mahdollista, että veloitukset on tuotu hyvityksinä ja hyvitykset veloituksina.</span><span class="sxs-lookup"><span data-stu-id="4de03-161">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="4de03-162">Tämän ongelman ratkaisemiseksi on muutettava asiaankuuluvaa XSLT:tä.</span><span class="sxs-lookup"><span data-stu-id="4de03-162">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="4de03-163">Jos tiliotteet ovat peräisin useasta pankista, varmista, että kaikissa käytetään samaa debet-/kredit-lähestymistapaa tai luo niille erilliset muunnokseet.</span><span class="sxs-lookup"><span data-stu-id="4de03-163">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="4de03-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator -malli</span><span class="sxs-lookup"><span data-stu-id="4de03-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="4de03-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit -malli</span><span class="sxs-lookup"><span data-stu-id="4de03-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="4de03-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator -malli</span><span class="sxs-lookup"><span data-stu-id="4de03-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="4de03-167">Esimerkkejä tiliotteiden muodoista ja teknisistä asetteluista</span><span class="sxs-lookup"><span data-stu-id="4de03-167">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="4de03-168">Seuraavassa taulukossa on esimerkkejä tuonnin lisäasetuksista pankkitilin täsmäytystietojen tuontitiedoston teknisistä asettelumäärityksistä sekä kolme esimerkkitiliotetiedostoa:</span><span class="sxs-lookup"><span data-stu-id="4de03-168">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="4de03-169">Voit ladata esimerkkitiedostot ja tekniset asettelut täällä: [Tuontitiedoston esimerkit](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="4de03-169">You can download the example files and technical layouts here: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="4de03-170">Tekninen asettelumääritys</span><span class="sxs-lookup"><span data-stu-id="4de03-170">Technical layout definition</span></span>                             | <span data-ttu-id="4de03-171">Esimerkkitiliotetiedosto</span><span class="sxs-lookup"><span data-stu-id="4de03-171">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="4de03-172">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="4de03-172">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="4de03-173">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="4de03-173">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="4de03-174">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="4de03-174">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="4de03-175">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="4de03-175">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="4de03-176">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="4de03-176">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="4de03-177">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="4de03-177">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
