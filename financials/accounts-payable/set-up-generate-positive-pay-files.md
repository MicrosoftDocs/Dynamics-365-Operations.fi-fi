---
title: "Positive pay -tiedostojen määrittäminen ja luominen"
description: "Tässä artikkelissa kuvataan Positive pay -toiminnon määrittämistä ja Positive pay -tiedostojen luomista."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f82ed69aaaf4d3345ef4e74a338124465dcf2358
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-and-generate-positive-pay-files"></a>Positive pay -tiedostojen määrittäminen ja luominen

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kuvataan Positive pay -toiminnon määrittämistä ja Positive pay -tiedostojen luomista. 

Määritä positiivinen maksu sähköisen luettelon luomiseksi pankille toimitettavista sekeistä. Kun sekki esitetään pankille, pankki vertaa sitä aiemmin lähetettyyn sekkiluetteloon. Jos sekki on sama kuin luettelossa, pankki selvittää sekin. Jos sekki ei vastaa luettelon sekkiä, pankki säilyttää sekin tarkistusta varten.

## <a name="security-for-positive-pay-files"></a>Positive pay -tiedostojen suojaus
Positiiviset maksutiedostot voivat sisältää luottamuksellisia tietoja maksun saajista ja sekkisummista. Varmista tämän vuoksi, että käytät riittäviä suojaustoimenpiteitä tiedostojen luontihetkestä pankin vastaanottoon asti. Positive pay -tiedostot ladataan selaimen määrittämään paikkaan. Positive pay -tiedostot saattavat sisältää henkilökohtaisia tietoja, joten on tärkeää, että vain valtuutetut käyttäjät voivat luoda ja tarkastella tietoja Microsoft Dynamics 365 for Operationsissa. Käytä tarvittavien oikeuksien määrittämisessä apuna seuraavaa taulukkoa.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tehtävä</th>
<th>Käyttöoikeus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Luo Positive pay -tiedostoja <strong>Pankkitilit</strong>-luettelosivulla tai <strong>Pankkitilit</strong>-sivulla.</td>
<td><ul>
<li><strong>Ylläpidä pankin Positive pay -tietoja</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>Luo Positive pay -tiedostoja useille yrityksille ja pankkitileille <strong>Luo Positive pay -tiedosto</strong> -sivulla.</td>
<td><ul>
<li><strong>Ylläpidä pankin Positive pay -tietoja</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tarkastele Positive pay -tiedostoja <strong>Positive pay -tiedoston yhteenveto</strong> -sivulla.</td>
<td><strong>Näytä pankin Positive pay -tiedot useita yrityksiä varten</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Vahvista pankin Positive pay -tiedosto <strong>Positive pay -tiedoston yhteenveto</strong> -sivulla.</td>
<td><strong>Vahvista Positive payment -tiedosto</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Peruuta pankin Positive pay -tiedosto <strong>Positive pay -tiedoston yhteenveto</strong> -sivulla.</td>
<td><strong>Peruuta Positive pay -tiedosto</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a>Positive pay -muodon määrittäminen
Positive pay -tiedostot luodaan käyttämällä tietoyksiköitä. Ennen Positive pay -tiedoston luomista on määritettävä muunnoksen syöttömuoto, jonka avulla sekkitiedot käännetään muotoon, jota pankki voi lukea. Voit luoda tiedostomuodon tunnuksen ja kuvauksen **Positive pay -muoto** -sivulla. Muunnoksen syöttömuodon on oltava XML-tiedostomuoto. Muoto riippuu käytettävästä muunnostiedostosta. Esimerkiksi määritetty Extensible Stylesheet Language Transformations (XSLT) -mallitiedosto käyttää **XML-Element**-muotoa. **Lataa tälle muunnokselle käytettävä tiedosto** -toiminnon avulla voit määrittää muunnostiedoston sijainnin pankin vaatimalle muodolle.

## <a name="example-xslt-file-for-positive-pay-file"></a>Esimerkki: Positive pay -tiedosto XSLT-tiedostona
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
          <xsl:for-each select="Document/BankPositivePayExportEntity">
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

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a>Positive pay -muodon määrittäminen pankkitileille
Jokaiselle pankkitilille, jolle haluat luoda Positive pay -tiedot, on määritettävä edellisessä toimenpiteessä määritetty Positive pay -muoto. Valitse **Pankkitilit**-sivulla Positive pay -muoto, joka vastaa pankkitiliä. Lisää **Positive pay -aloituspäivä** -kenttään ensimmäinen päivämäärä, jona Positive pay -tiedostot luodaan. On tärkeää, että tähän kenttään määritetään päivämäärä. Muussa tapauksessa ensimmäinen luomasi Positive pay -tiedosto sisältää kaikki pankkitilille luodut sekit.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Numerojärjestyksen määrittäminen Positive pay -tiedostoille
Jokaisella positive pay -tiedostolla on oltava yksilöivä numero. Luo numerojärjestys Positive pay -tiedostoille **Maksuliikennetiedot**-sivun **Numerojärjestykset**-välilehdessä.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Positive pay -tiedoston luominen yksittäiselle pankkitilille
Voit luoda Positive pay -tiedoston yksittäiselle yritykselle ja pankkitilille. Seuraavassa osassa on tietoja Positive pay -tiedostojen luomisesta useille yrityksille ja pankkitileille samalla kertaa. Jos haluat luoda Positive pay -tiedoston yksittäiselle yritykselle ja yksittäiselle pankkitilille, avaa **Luo Positive pay -tiedosto** -valintaikkuna **Pankkitilit**-sivulta. Kirjoita **Katkaisupäivämäärä**-kenttään viimeinen sekin päivämäärä, joka otetaan mukaan Positive pay -tiedostoon. Tiedosto sisältää kaikki sekit, joita ei ole sisällytetty Positive pay -tiedostoon sekin päivämäärään saakka.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Positive pay -tiedoston luominen useille pankkitileille
Luo Positive pay -tiedostoja useille yrityksille ja pankkitileille kausittaisen **Luo Positive pay -tiedosto** -tehtävän avulla. Valitse tiedostolle Positive pay -muoto ja määritä, luodaanko tiedosto kaikille yrityksille vai vain valitulle yritykselle. Voit myös luoda Positive pay -tiedoston kaikille pankkitileille, joissa käytetään määritettyä Positive pay -muotoa,tai vain valitulle pankkitilille. Kirjoita **Katkaisupäivämäärä**-kenttään viimeinen sekin päivämäärä, joka otetaan mukaan Positive pay -tiedostoon. Tiedosto sisältää kaikki sekit, joita ei ole sisällytetty Positive pay -tiedostoon sekin päivämäärään saakka.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Positive pay -tiedoston luonnin tulosten tarkastelu
Kun Positive pay -tiedosto on luotu, voit tarkastella tuloksia **Positive pay -tiedoston yhteenveto** -sivulla. Jos haluat tarkastella yksittäisten sekkien tietoja, käytä **Positive pay -tiedosto** -tietosivua.

## <a name="confirm-a-positive-pay-file"></a>Vahvista Positive pay -tiedosto
Kun positive pay -tiedostossa listatut sekit on maksettu, saat pankiltasi vahvistusnumeron. Tämän jälkeen voit vahvistaa Positive pay -tiedoston. Valitse **Positive pay -tiedoston yhteenveto** -sivulla Positive pay -tiedosto, jonka tila on **Luotu**, ja valitse sitten **Anna vahvistus** -toiminto. Kun vahvistat Positive pay -tiedoston, pankilta saamasi vahvistusnumero tallennetaan.

## <a name="recall-a-positive-pay-file"></a>Peruuta Positive pay -tiedosto
Jos haluat muuttaa Positive pay -tiedosto, voit kutsua sen takaisin. Valitse **Positive pay -tiedoston yhteenveto** -sivulla Positive pay -tiedosto, jonka tila on **Luotu**, ja valitse sitten **Peruuta**-toiminto. Jokaisen Positive pay -tiedostossa olevan sekin kenttä ilmaisee, onko Positive pay -tiedostoon sisältyvä sekki peruutettu. Tämän jälkeen voit luoda uuden Positive pay -tiedoston, joka sisältää peruutetun sekin.




