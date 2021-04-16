---
title: Positive pay -tiedostojen määrittäminen ja luominen
description: Tässä ohjeaiheessa käsitellään Positive pay -toiminnon määrittämistä ja Positive pay -tiedostojen luomista.
author: panolte
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 9f96e34b8d94f9e83afb39d6ad97aca85386b458
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830709"
---
# <a name="set-up-and-generate-positive-pay-files"></a><span data-ttu-id="479d0-103">Positive pay -tiedostojen määrittäminen ja luominen</span><span class="sxs-lookup"><span data-stu-id="479d0-103">Set up and generate positive pay files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="479d0-104">Tässä ohjeaiheessa käsitellään Positive pay -toiminnon määrittämistä ja Positive pay -tiedostojen luomista.</span><span class="sxs-lookup"><span data-stu-id="479d0-104">This topic explains how to set up positive pay and generate positive pay files.</span></span> 

<span data-ttu-id="479d0-105">Määritä positiivinen maksu sähköisen luettelon luomiseksi pankille toimitettavista sekeistä.</span><span class="sxs-lookup"><span data-stu-id="479d0-105">Set up positive pay to generate an electronic list of checks that is provided to the bank.</span></span> <span data-ttu-id="479d0-106">Kun sekki esitetään pankille, pankki vertaa sitä aiemmin lähetettyyn sekkiluetteloon.</span><span class="sxs-lookup"><span data-stu-id="479d0-106">Then, when a check is presented to the bank, the bank compares it with the list of checks.</span></span> <span data-ttu-id="479d0-107">Jos sekki on sama kuin luettelossa, pankki selvittää sekin.</span><span class="sxs-lookup"><span data-stu-id="479d0-107">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="479d0-108">Jos sekki ei vastaa luettelon sekkiä, pankki säilyttää sekin tarkistusta varten.</span><span class="sxs-lookup"><span data-stu-id="479d0-108">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

## <a name="security-for-positive-pay-files"></a><span data-ttu-id="479d0-109">Positive pay -tiedostojen suojaus</span><span class="sxs-lookup"><span data-stu-id="479d0-109">Security for positive pay files</span></span>
<span data-ttu-id="479d0-110">Positiiviset maksutiedostot voivat sisältää luottamuksellisia tietoja maksun saajista ja sekkisummista.</span><span class="sxs-lookup"><span data-stu-id="479d0-110">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="479d0-111">Varmista tämän vuoksi, että käytät riittäviä suojaustoimenpiteitä tiedostojen luontihetkestä pankin vastaanottoon asti.</span><span class="sxs-lookup"><span data-stu-id="479d0-111">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="479d0-112">Positive pay -tiedostot ladataan selaimen määrittämään paikkaan.</span><span class="sxs-lookup"><span data-stu-id="479d0-112">Positive pay files are downloaded to the location that is specified by your web browser.</span></span> <span data-ttu-id="479d0-113">Positive pay -tiedostot saattavat sisältää henkilökohtaisia tietoja, joten on tärkeää, että vain valtuutetut käyttäjät voivat luoda ja tarkastella tietoja Microsoft Dynamics 365 Financessa.</span><span class="sxs-lookup"><span data-stu-id="479d0-113">Because positive pay files can contain sensitive information, it's important that only authorized users have access to generate and view this information in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="479d0-114">Käytä tarvittavien oikeuksien määrittämisessä apuna seuraavaa taulukkoa.</span><span class="sxs-lookup"><span data-stu-id="479d0-114">Use the following table to help you determine the privileges that are required.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="479d0-115">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="479d0-115">Task</span></span></th>
<th><span data-ttu-id="479d0-116">Käyttöoikeus</span><span class="sxs-lookup"><span data-stu-id="479d0-116">Privilege</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="479d0-117">Luo Positive pay -tiedostoja <strong>Pankkitilit</strong>-luettelosivulla tai <strong>Pankkitilit</strong>-sivulla.</span><span class="sxs-lookup"><span data-stu-id="479d0-117">Generate positive pay files from the <strong>Bank accounts</strong> list page or the <strong>Bank accounts</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="479d0-118"><strong>Ylläpidä pankin Positive pay -tietoja</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="479d0-118"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="479d0-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="479d0-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="479d0-120">Luo Positive pay -tiedostoja useille yrityksille ja pankkitileille <strong>Luo Positive pay -tiedosto</strong> -sivulla.</span><span class="sxs-lookup"><span data-stu-id="479d0-120">Generate positive pay files for multiple legal entities and bank accounts from the <strong>Generate a positive pay file</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="479d0-121"><strong>Ylläpidä pankin Positive pay -tietoja</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="479d0-121"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="479d0-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="479d0-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="479d0-123">Tarkastele Positive pay -tiedostoja <strong>Positive pay -tiedoston yhteenveto</strong> -sivulla.</span><span class="sxs-lookup"><span data-stu-id="479d0-123">View positive pay files on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="479d0-124"><strong>Näytä pankin Positive pay -tiedot useita yrityksiä varten</strong> (BankPositivePayView)</span><span class="sxs-lookup"><span data-stu-id="479d0-124"><strong>View bank positive pay information for multiple legal entities</strong> (BankPositivePayView)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="479d0-125">Vahvista pankin Positive pay -tiedosto <strong>Positive pay -tiedoston yhteenveto</strong> -sivulla.</span><span class="sxs-lookup"><span data-stu-id="479d0-125">Confirm a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="479d0-126"><strong>Vahvista Positive payment -tiedosto</strong> (BankPositivePayConfirm)</span><span class="sxs-lookup"><span data-stu-id="479d0-126"><strong>Confirm positive payment file</strong> (BankPositivePayConfirm)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="479d0-127">Peruuta pankin Positive pay -tiedosto <strong>Positive pay -tiedoston yhteenveto</strong> -sivulla.</span><span class="sxs-lookup"><span data-stu-id="479d0-127">Recall a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="479d0-128"><strong>Peruuta Positive pay -tiedosto</strong> (BankPositivePayRecall)</span><span class="sxs-lookup"><span data-stu-id="479d0-128"><strong>Recall positive pay file</strong> (BankPositivePayRecall)</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a><span data-ttu-id="479d0-129">Positive pay -muodon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="479d0-129">Set up a positive pay format</span></span>
<span data-ttu-id="479d0-130">Positive pay -tiedostot luodaan käyttämällä tietoyksiköitä.</span><span class="sxs-lookup"><span data-stu-id="479d0-130">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="479d0-131">Ennen Positive pay -tiedoston luomista on määritettävä muunnoksen syöttömuoto, jonka avulla sekkitiedot käännetään muotoon, jota pankki voi lukea.</span><span class="sxs-lookup"><span data-stu-id="479d0-131">Before you can generate a positive pay file, you must set up a transformation input format that will be used to translate the check information into a format that can communicate with the bank.</span></span> <span data-ttu-id="479d0-132">Voit luoda tiedostomuodon tunnuksen ja kuvauksen **Positive pay -muoto** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="479d0-132">On the **Positive pay format** page, you can create a file format identifier and a description.</span></span> <span data-ttu-id="479d0-133">Muunnoksen syöttömuodon on oltava XML-tiedostomuoto.</span><span class="sxs-lookup"><span data-stu-id="479d0-133">The transformation input format must be of the XML type.</span></span> <span data-ttu-id="479d0-134">Muoto riippuu käytettävästä muunnostiedostosta.</span><span class="sxs-lookup"><span data-stu-id="479d0-134">The specific format depends on the transformation file that you're using.</span></span> <span data-ttu-id="479d0-135">Esimerkiksi määritetty Extensible Stylesheet Language Transformations (XSLT) -mallitiedosto käyttää **XML-Element**-muotoa.</span><span class="sxs-lookup"><span data-stu-id="479d0-135">For example, the sample Extensible Stylesheet Language Transformations (XSLT) file that is provided uses the **XML-Element** format.</span></span> <span data-ttu-id="479d0-136">**Lataa tälle muunnokselle käytettävä tiedosto** -toiminnon avulla voit määrittää muunnostiedoston sijainnin pankin vaatimalle muodolle.</span><span class="sxs-lookup"><span data-stu-id="479d0-136">Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.</span></span>

## <a name="example-xslt-file-for-positive-pay-file"></a><span data-ttu-id="479d0-137">Esimerkki: Positive pay -tiedosto XSLT-tiedostona</span><span class="sxs-lookup"><span data-stu-id="479d0-137">Example: XSLT file for positive pay file</span></span>

```xml
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
  <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
  <xsl:template match="/">
    <xsl:value-of select="'
'" />
    <Document>
      <xsl:value-of select="'
'" />
      <!--Header Begin-->
      <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
      <xsl:value-of select="'
'" />
      <!--Header End-->
      <xsl:for-each select="Document/BANKPOSITIVEPAYEXPORTENTITY">
        <!--Cheque Detail begin-->
        <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
        <xsl:value-of select="','" />
        <xsl:choose>
          <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
            <xsl:value-of select='string("Yes")'/>
          </xsl:when>
          <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
            <xsl:value-of select='string("No")'/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select='string(" ")'/>
          </xsl:otherwise>
        </xsl:choose>
        <xsl:value-of select="','" />
        <xsl:value-of select='string("Payment")'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='TRANSDATE/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='CHEQUENUM/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='AMOUNTCUR/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='string("BOA-#1812")'/>
        <xsl:value-of select="','" />
        <xsl:choose>
          <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
            <xsl:value-of select='VENDGROUP/text()'/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select='CUSTGROUP/text()'/>
          </xsl:otherwise>
        </xsl:choose>
        <xsl:value-of select="','" />
        <xsl:value-of select='TRANSDATE/text()'/>
        <xsl:value-of select="'
'" />
      </xsl:for-each>
    </Document>
  </xsl:template>
</xsl:stylesheet>
```

> [!NOTE]
> <span data-ttu-id="479d0-138">XSLT-tiedoston XML-nimien on vastattava XML-solmujen kirjainkokoa.</span><span class="sxs-lookup"><span data-stu-id="479d0-138">XML names in the XSLT must match the casing of the nodes in the XML.</span></span> <span data-ttu-id="479d0-139">Sekä XSLT- että XML-tiedostoissa kirjainkoolla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="479d0-139">Both the XSLT and XML files are case sensitive.</span></span> 

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a><span data-ttu-id="479d0-140">Positive pay -muodon määrittäminen pankkitileille</span><span class="sxs-lookup"><span data-stu-id="479d0-140">Assign the positive pay format to a bank account</span></span>
<span data-ttu-id="479d0-141">Jokaiselle pankkitilille, jolle haluat luoda Positive pay -tiedot, on määritettävä edellisessä toimenpiteessä määritetty Positive pay -muoto.</span><span class="sxs-lookup"><span data-stu-id="479d0-141">For each bank account that you want to generate positive pay information for, you must assign the positive pay format that you specified in the previous section.</span></span> <span data-ttu-id="479d0-142">Valitse **Pankkitilit**-sivulla Positive pay -muoto, joka vastaa pankkitiliä.</span><span class="sxs-lookup"><span data-stu-id="479d0-142">On the **Bank accounts** page, select the positive pay format that corresponds to the bank account.</span></span> <span data-ttu-id="479d0-143">Lisää **Positive pay -aloituspäivä** -kenttään ensimmäinen päivämäärä, jona Positive pay -tiedostot luodaan.</span><span class="sxs-lookup"><span data-stu-id="479d0-143">In the **Positive pay start date** field, enter the first date to generate positive pay files.</span></span> <span data-ttu-id="479d0-144">On tärkeää, että tähän kenttään määritetään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="479d0-144">It's important that you enter a date in this field.</span></span> <span data-ttu-id="479d0-145">Muussa tapauksessa ensimmäinen luomasi Positive pay -tiedosto sisältää kaikki pankkitilille luodut sekit.</span><span class="sxs-lookup"><span data-stu-id="479d0-145">Otherwise, the first positive pay file that you generate will include all checks that have ever been created for this bank account.</span></span>

## <a name="assign-a-number-sequence-for-positive-pay-files"></a><span data-ttu-id="479d0-146">Numerojärjestyksen määrittäminen Positive pay -tiedostoille</span><span class="sxs-lookup"><span data-stu-id="479d0-146">Assign a number sequence for positive pay files</span></span>
<span data-ttu-id="479d0-147">Jokaisella positive pay -tiedostolla on oltava yksilöivä numero.</span><span class="sxs-lookup"><span data-stu-id="479d0-147">Each positive pay file must have a unique number.</span></span> <span data-ttu-id="479d0-148">Luo numerojärjestys Positive pay -tiedostoille **Maksuliikennetiedot**-sivun **Numerojärjestykset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="479d0-148">Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.</span></span>

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a><span data-ttu-id="479d0-149">Positive pay -tiedoston luominen yksittäiselle pankkitilille</span><span class="sxs-lookup"><span data-stu-id="479d0-149">Generate a positive pay file for a single bank account</span></span>
<span data-ttu-id="479d0-150">Voit luoda Positive pay -tiedoston yksittäiselle yritykselle ja pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="479d0-150">You can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="479d0-151">Seuraavassa osassa on tietoja Positive pay -tiedostojen luomisesta useille yrityksille ja pankkitileille samalla kertaa.</span><span class="sxs-lookup"><span data-stu-id="479d0-151">For information about how to generate positive pay files for multiple legal entities and bank accounts at the same time, see the next section.</span></span> <span data-ttu-id="479d0-152">Jos haluat luoda Positive pay -tiedoston yksittäiselle yritykselle ja yksittäiselle pankkitilille, avaa **Luo Positive pay -tiedosto** -valintaikkuna **Pankkitilit**-sivulta.</span><span class="sxs-lookup"><span data-stu-id="479d0-152">To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page.</span></span> <span data-ttu-id="479d0-153">Kirjoita **Katkaisupäivämäärä**-kenttään viimeinen sekin päivämäärä, joka otetaan mukaan Positive pay -tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="479d0-153">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="479d0-154">Tiedosto sisältää kaikki sekit, joita ei ole sisällytetty Positive pay -tiedostoon sekin päivämäärään saakka.</span><span class="sxs-lookup"><span data-stu-id="479d0-154">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a><span data-ttu-id="479d0-155">Positive pay -tiedoston luominen useille pankkitileille</span><span class="sxs-lookup"><span data-stu-id="479d0-155">Generate a positive pay file for multiple bank accounts</span></span>
<span data-ttu-id="479d0-156">Luo Positive pay -tiedostoja useille yrityksille ja pankkitileille kausittaisen **Luo Positive pay -tiedosto** -tehtävän avulla.</span><span class="sxs-lookup"><span data-stu-id="479d0-156">To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task.</span></span> <span data-ttu-id="479d0-157">Valitse tiedostolle Positive pay -muoto ja määritä, luodaanko tiedosto kaikille yrityksille vai vain valitulle yritykselle.</span><span class="sxs-lookup"><span data-stu-id="479d0-157">Select the positive pay format for the file, and specify whether to generate the file for all legal entities or for a selected legal entity.</span></span> <span data-ttu-id="479d0-158">Voit myös luoda Positive pay -tiedoston kaikille pankkitileille, joissa käytetään määritettyä Positive pay -muotoa,tai vain valitulle pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="479d0-158">You can also generate the positive pay file for all bank accounts that use the specified positive pay format or for a selected bank account.</span></span> <span data-ttu-id="479d0-159">Kirjoita **Katkaisupäivämäärä**-kenttään viimeinen sekin päivämäärä, joka otetaan mukaan Positive pay -tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="479d0-159">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="479d0-160">Tiedosto sisältää kaikki sekit, joita ei ole sisällytetty Positive pay -tiedostoon sekin päivämäärään saakka.</span><span class="sxs-lookup"><span data-stu-id="479d0-160">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="view-the-results-of-positive-pay-file-generation"></a><span data-ttu-id="479d0-161">Positive pay -tiedoston luonnin tulosten tarkastelu</span><span class="sxs-lookup"><span data-stu-id="479d0-161">View the results of positive pay file generation</span></span>
<span data-ttu-id="479d0-162">Kun Positive pay -tiedosto on luotu, voit tarkastella tuloksia **Positive pay -tiedoston yhteenveto** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="479d0-162">After the positive pay file is generated, you can view the results on the **Positive pay file summary** page.</span></span> <span data-ttu-id="479d0-163">Jos haluat tarkastella yksittäisten sekkien tietoja, käytä **Positive pay -tiedosto** -tietosivua.</span><span class="sxs-lookup"><span data-stu-id="479d0-163">To view the details of the individual checks, use the **Positive pay file** details page.</span></span>

## <a name="confirm-a-positive-pay-file"></a><span data-ttu-id="479d0-164">Vahvista Positive pay -tiedosto</span><span class="sxs-lookup"><span data-stu-id="479d0-164">Confirm a positive pay file</span></span>
<span data-ttu-id="479d0-165">Kun positive pay -tiedostossa listatut sekit on maksettu, saat pankiltasi vahvistusnumeron.</span><span class="sxs-lookup"><span data-stu-id="479d0-165">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="479d0-166">Tämän jälkeen voit vahvistaa Positive pay -tiedoston.</span><span class="sxs-lookup"><span data-stu-id="479d0-166">You can then confirm the positive pay file.</span></span> <span data-ttu-id="479d0-167">Valitse **Positive pay -tiedoston yhteenveto** -sivulla Positive pay -tiedosto, jonka tila on **Luotu**, ja valitse sitten **Anna vahvistus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="479d0-167">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action.</span></span> <span data-ttu-id="479d0-168">Kun vahvistat Positive pay -tiedoston, pankilta saamasi vahvistusnumero tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="479d0-168">When you confirm a positive pay file, the confirmation number that you received from the bank is recorded.</span></span>

## <a name="recall-a-positive-pay-file"></a><span data-ttu-id="479d0-169">Peruuta Positive pay -tiedosto</span><span class="sxs-lookup"><span data-stu-id="479d0-169">Recall a positive pay file</span></span>
<span data-ttu-id="479d0-170">Jos haluat muuttaa Positive pay -tiedosto, voit kutsua sen takaisin.</span><span class="sxs-lookup"><span data-stu-id="479d0-170">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="479d0-171">Valitse **Positive pay -tiedoston yhteenveto** -sivulla Positive pay -tiedosto, jonka tila on **Luotu**, ja valitse sitten **Peruuta**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="479d0-171">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action.</span></span> <span data-ttu-id="479d0-172">Jokaisen Positive pay -tiedostossa olevan sekin kenttä ilmaisee, onko Positive pay -tiedostoon sisältyvä sekki peruutettu.</span><span class="sxs-lookup"><span data-stu-id="479d0-172">For each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span> <span data-ttu-id="479d0-173">Tämän jälkeen voit luoda uuden Positive pay -tiedoston, joka sisältää peruutetun sekin.</span><span class="sxs-lookup"><span data-stu-id="479d0-173">You can then create a new positive pay file that includes the check that was recalled.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
