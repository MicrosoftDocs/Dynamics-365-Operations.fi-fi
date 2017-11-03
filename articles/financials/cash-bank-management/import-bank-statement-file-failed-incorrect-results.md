---
title: "Pankin tiliotteen tiedoston tuomisen vianmääritys"
description: "On tärkeää, että pankin tiliotetiedosto vastaa Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa tuettuja asetteluja. Tiliotteiden tiukkojen standardien vuoksi suurin osa integraatioista toimii oikein. Kuitenkin joskus tiliotetiedostoa ei voi tuoda tai se sisältää virheellisiä tuloksia. Yleensä ongelmat johtuvat pienistä eroista tiliotetiedostossa. Tässä artikkelissa selitetään, miten nämä erot ja niistä johtuvat ongelmat korjataan."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4feb77bf0031494dfd456c23c632a264c96f0e43
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="202cb-107">Pankin tiliotteen tiedoston tuomisen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="202cb-107">Bank statement file import troubleshooting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="202cb-108">On tärkeää, että pankin tiliotetiedosto vastaa Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa tuettuja asetteluja.</span><span class="sxs-lookup"><span data-stu-id="202cb-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Finance and Operations, Enterprise edition supports.</span></span> <span data-ttu-id="202cb-109">Tiliotteiden tiukkojen standardien vuoksi suurin osa integraatioista toimii oikein.</span><span class="sxs-lookup"><span data-stu-id="202cb-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="202cb-110">Kuitenkin joskus tiliotetiedostoa ei voi tuoda tai se sisältää virheellisiä tuloksia.</span><span class="sxs-lookup"><span data-stu-id="202cb-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="202cb-111">Yleensä ongelmat johtuvat pienistä eroista tiliotetiedostossa.</span><span class="sxs-lookup"><span data-stu-id="202cb-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="202cb-112">Tässä artikkelissa selitetään, miten nämä erot ja niistä johtuvat ongelmat korjataan.</span><span class="sxs-lookup"><span data-stu-id="202cb-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="202cb-113">Mikä virhe on kyseessä?</span><span class="sxs-lookup"><span data-stu-id="202cb-113">What is the error?</span></span>
------------------

<span data-ttu-id="202cb-114">Kun tiliotetiedoston tuontia on yritetty, siirry Tietojen hallinnan työhistoriaan ja sen suoritustietoihin löytääksesi virheen.</span><span class="sxs-lookup"><span data-stu-id="202cb-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="202cb-115">Virhe voi auttaa osoittamalla tiliotteeseen, saldoon tai tiliotteen riviin.</span><span class="sxs-lookup"><span data-stu-id="202cb-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="202cb-116">Se ei kuitenkaan todennäköisesti anna riittävästi tietoa, jotta ongelman aiheuttavan kentän tai elementin voisi tunnistaa.</span><span class="sxs-lookup"><span data-stu-id="202cb-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="202cb-117">Mitä ovat erot?</span><span class="sxs-lookup"><span data-stu-id="202cb-117">What are the differences?</span></span>
<span data-ttu-id="202cb-118">Vertaa pankkitiedoston asettelumääritystä Finance and Operationsin tuontimääritykseen ja kiinnitä huomiota kenttien ja elementtien eroihin.</span><span class="sxs-lookup"><span data-stu-id="202cb-118">Compare the bank file layout definition to the Finance and Operations import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="202cb-119">Vertaa tiliotetiedostoa liittyvään Finance and Operations -näytetiedostoon.</span><span class="sxs-lookup"><span data-stu-id="202cb-119">Compare the bank statement file to the related sample Finance and Operations file.</span></span> <span data-ttu-id="202cb-120">ISO20022-tiedostoissa on erot helppo nähdä.</span><span class="sxs-lookup"><span data-stu-id="202cb-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="transformations"></a><span data-ttu-id="202cb-121">Muunnokset</span><span class="sxs-lookup"><span data-stu-id="202cb-121">Transformations</span></span>
<span data-ttu-id="202cb-122">Yleensä muutokset on tehtävä johonkin kolmesta muunnoksesta.</span><span class="sxs-lookup"><span data-stu-id="202cb-122">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="202cb-123">Jokaisen muunnos on kirjoitettu tiettyyn standardiin.</span><span class="sxs-lookup"><span data-stu-id="202cb-123">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="202cb-124">Resurssin nimi</span><span class="sxs-lookup"><span data-stu-id="202cb-124">Resource name</span></span>                                         | <span data-ttu-id="202cb-125">Tiedostonimi</span><span class="sxs-lookup"><span data-stu-id="202cb-125">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="202cb-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="202cb-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="202cb-127">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="202cb-127">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="202cb-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="202cb-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="202cb-129">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="202cb-129">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="202cb-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="202cb-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="202cb-131">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="202cb-131">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="202cb-132">Muunnosten virheenkorjaus</span><span class="sxs-lookup"><span data-stu-id="202cb-132">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="202cb-133">Oikaise BAI2- ja MT940-tiedostot</span><span class="sxs-lookup"><span data-stu-id="202cb-133">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="202cb-134">BAI2- ja MT940-tiedostot ovat tekstiin perustuvia tiedostoja ja ne on oikaistava, jotta Extensible Stylesheet Language Transformation -kielen (XSLT) virheenkorjauksen voi ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="202cb-134">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="202cb-135">Ohjelma tekee oikaisun, kun tiedosto tuodaan.</span><span class="sxs-lookup"><span data-stu-id="202cb-135">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="202cb-136">Luo XML-tiedosto ja kopioi siihen seuraava tekstinkatkelma.</span><span class="sxs-lookup"><span data-stu-id="202cb-136">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="202cb-137">Kopioi tiliotetiedoston sisältö ja liitä se XML-tiedostoon niin, että ne korvaavat **PASTESTATEMENTFILEHERE**-kohdan.</span><span class="sxs-lookup"><span data-stu-id="202cb-137">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="202cb-138">XSLT-virheenkorjaus</span><span class="sxs-lookup"><span data-stu-id="202cb-138">Debug the XSLT</span></span>

<span data-ttu-id="202cb-139">Lisätietoja on kohdassa <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="202cb-139">For more information, see <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="202cb-140">Käynnistä Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="202cb-140">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="202cb-141">Luo konsolisovellus.</span><span class="sxs-lookup"><span data-stu-id="202cb-141">Create a console application.</span></span>
3.  <span data-ttu-id="202cb-142">Avaa haluamasi XSLT-muoto.</span><span class="sxs-lookup"><span data-stu-id="202cb-142">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="202cb-143">Valitse XSLT-muotoa ja sen ominaisuussivua.</span><span class="sxs-lookup"><span data-stu-id="202cb-143">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="202cb-144">Aseta syötteeksi tiliotetiedoston sijainti.</span><span class="sxs-lookup"><span data-stu-id="202cb-144">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="202cb-145">Määritä tulosteelle sijainti ja tiedostonimi.</span><span class="sxs-lookup"><span data-stu-id="202cb-145">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="202cb-146">Määritä tarvittavat katkaisukohdat.</span><span class="sxs-lookup"><span data-stu-id="202cb-146">Set the required break points.</span></span>
8.  <span data-ttu-id="202cb-147">Valitse valikosta **XML** &gt; **Aloita XSLT-virheenkorjaus**.</span><span class="sxs-lookup"><span data-stu-id="202cb-147">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="202cb-148">Muotoile XSLT-tuloste</span><span class="sxs-lookup"><span data-stu-id="202cb-148">Format the XSLT output</span></span>

<span data-ttu-id="202cb-149">Kun muunnos ajetaan, se luo tiedoston, jonka voi avata Visual Studiossa.</span><span class="sxs-lookup"><span data-stu-id="202cb-149">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="202cb-150">Voit muotoilla tiedoston nopeasti Ctrl+A, Ctrl+K ja Ctrl+D -näppäinkomennoilla.</span><span class="sxs-lookup"><span data-stu-id="202cb-150">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="202cb-151">Muunnoksen oikaiseminen</span><span class="sxs-lookup"><span data-stu-id="202cb-151">Adjust the transformation</span></span>

<span data-ttu-id="202cb-152">Oikaise muunnos saadaksesi haluamasi kentän tai elementin tiliotetiedostoon.</span><span class="sxs-lookup"><span data-stu-id="202cb-152">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="202cb-153">Määritä sitten kyseinen kenttä tai elementti asiaankuuluvaan Finance and Operations -elementtiin.</span><span class="sxs-lookup"><span data-stu-id="202cb-153">Then map that field or element to the appropriate Finance and Operations element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="202cb-154">Debet/kredit-ilmaisin</span><span class="sxs-lookup"><span data-stu-id="202cb-154">Debit/credit indicator</span></span>

<span data-ttu-id="202cb-155">Toisinaan on mahdollista, että veloitukset on tuotu hyvityksinä ja hyvitykset veloituksina.</span><span class="sxs-lookup"><span data-stu-id="202cb-155">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="202cb-156">Tämän ongelman ratkaisemiseksi on muutettava asiaankuuluvaa XSLT:tä.</span><span class="sxs-lookup"><span data-stu-id="202cb-156">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="202cb-157">Jos tiliotteet ovat peräisin useasta pankista, varmista, että kaikissa käytetään samaa debet-/kredit-lähestymistapaa tai luo niille erilliset muunnokseet.</span><span class="sxs-lookup"><span data-stu-id="202cb-157">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="202cb-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator -malli</span><span class="sxs-lookup"><span data-stu-id="202cb-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="202cb-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit -malli</span><span class="sxs-lookup"><span data-stu-id="202cb-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="202cb-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator -malli</span><span class="sxs-lookup"><span data-stu-id="202cb-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="202cb-161">Esimerkkejä tiliotteiden muodoista ja teknisistä asetteluista</span><span class="sxs-lookup"><span data-stu-id="202cb-161">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="202cb-162">Seuraavassa taulukossa on esimerkkejä tuonnin lisäasetuksista pankkitilin täsmäytystietojen tuontitiedoston teknisistä asettelumäärityksistä sekä kolme esimerkkitiliotetiedostoa:</span><span class="sxs-lookup"><span data-stu-id="202cb-162">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="202cb-163">Voit ladata näytetiedostot ja tekniset asettelut täältä: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="202cb-163">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="202cb-164">Tekninen asettelumääritys</span><span class="sxs-lookup"><span data-stu-id="202cb-164">Technical layout definition</span></span>                             | <span data-ttu-id="202cb-165">Esimerkkitiliotetiedosto</span><span class="sxs-lookup"><span data-stu-id="202cb-165">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="202cb-166">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="202cb-166">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="202cb-167">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="202cb-167">MT940StatementExample</span></span>                |
| <span data-ttu-id="202cb-168">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="202cb-168">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="202cb-169">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="202cb-169">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="202cb-170">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="202cb-170">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="202cb-171">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="202cb-171">BAI2StatementExample</span></span>                 |






