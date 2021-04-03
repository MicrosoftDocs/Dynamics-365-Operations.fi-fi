---
title: EU-saapumistodistus
description: Tässä artikkelissa on tietoja Euroopan unionin (EU) saapumistodistuksista.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1f763bb818bbbbb4ced1ce03f175df725cebc4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243564"
---
# <a name="eu-entry-certificates"></a>EU-saapumistodistukset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja Euroopan unionin (EU) saapumistodistuksista.

Voit suorittaa seuraavat Euroopan unionin (EU) saapumistodistuksen tehtävät:

-   Luo ja julkaise EU-saapumistodistus yhdessä pakkausluettelon tai myyntilaskun kanssa nimikkeiden tai palveluiden toimittamiseksi EU-maihin tai EU-alueille.
-   Vastaanota EU-asiakkaan allekirjoittama merkinnän varmenne.
-   Lataa allekirjoitettu EU-saapumistodistus, joka on vastaanotettu joko asiakkaalta tai kolmannelta osapuolelta, joka on vastuussa nimikkeiden toimittamisesta asiakkaalle.
-   Liitä ladattu EU-merkinnän sertifikaatti myyntilaskuun.
-   Päivitä ladatun EU-merkinnän varmenteen tila.

## <a name="prerequisites"></a>Edellytykset
Seuraavassa taulukossa esitellään edellytykset, joiden on täytyttävä ennen aloittamista.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Luokka</th>
<th>Edellytys</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Maa/alue</td>
<td>Yrityksen ensisijainen osoitteen on oltava EU-jäsenvaltiossa.</td>
</tr>
<tr class="even">
<td>Liittyvät määritystehtävät</td>
<td><ul>
<li>Valitse <strong>Myyntireskontran parametrit</strong> -sivulla vaihtoehdot <strong>Ota käyttöön merkinnän varmenteen hallinta</strong> ja <strong>Ota käyttöön merkinnän varmenteen myöntäminen</strong>.</li>
<li>Valitse <strong>Asiakkaat</strong>-sivun <strong>Lasku ja toimitus</strong> -pikavälilehdessä <strong>Merkinnän varmenne tarvitaan</strong> osoittamaan, että EU-saapumistodistus on pakollinen asiakkaalle. Myönnä asiakkaalle yrityksen EU-saapumisilmoitus valitsemalla <strong>Myönnä merkinnän varmenne</strong>.</li>
<li>Valitse <strong>Myyntireskontran parametrit</strong> -sivulla <strong>Merkinnän varmenne</strong> -viitteeksi numerosarjakoodi.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Liittyvät tapahtumat</td>
<td><ul>
<li>Luo asiakastili.</li>
<li>Luo myyntitilaus.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a>EU-saapumistodistuksen luominen, rekisteröidään ja lataaminen
Voit luoda EU-merkinnän varmenne automaattisesti vai manuaalisesti. EU-merkinnän sertifikaatti luodaan ja tulostetaan automaattisesti, kun kirjaat pakkausluettelon tai asiakkaan laskun käyttämällä **Pakkausluettelon kirjaus**- tai **Laskun kirjaus** -sivua. Voit luoda tai uudelleentulostaa EU-saapumistodistuksen manuaalisesti asiakaslaskulle **Laskukirjauskansio**-sivulla. Voit myös antaa **Merkinnän varmenteen tosite** -sivulla tietoja kolmannen osapuolen myöntämästä EU-saapumistodistuksesta.

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a>EU-saapumistodistuksen luominen automaattisesti tai manuaalisesti

Voit luoda EU-saapumistodistuksia automaattisesti pakkausluettelon avulla **Kaikki myyntitilaukset** -sivulla tai laskun avulla **Myyntitilaus**-sivulla. Voit luoda EU-saapumistodistuksen manuaalisesti laskun avulla **Laskukirjauskansio**-sivulla. Laskun todistuksen tila on kuitenkin muutettava ennen EU-saapumistodistuksen luontia manuaalisesti.

### <a name="registering-an-eu-entry-certificate"></a>EU-saapumistodistuksen rekisteröinti

Jos rekisteröinti on pakollinen, voit rekisteröidä kolmannen osapuolen myöntämän EU-saapumistodistuksen **Merkinnän varmenteen tosite** -sivulla.

### <a name="uploading-a-received-eu-entry-certificate"></a>Vastaanotetun EU-saapumistodistuksen lataaminen

Lataa EU-asiakkaan allekirjoittama EU-saapumistodistus **Liitteet**-sivulla. Kun todistus on ladattu, voit liittää sen laskuun näyttönä nimikkeiden toimituksesta. Tämä näyttö on pakollinen, jos on tehtävä lasku, joka ei sisällä arvonlisäveroa (ALV). Sitä käytetään myös tilintarkastuksen aikana.

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a>Valinnainen: Todistuksen tilan ja laskun tulostustilan päivittäminen

Voit päivittää saapumistodistuksen tilan ja myyntilaskun tulostustilan **Laskukirjauskansio**-sivulla.

## <a name="technical-information-for-system-administrators"></a>Teknisiä tietoja järjestelmänvalvojille
Jos sinulla ei ole niiden sivujen käyttöoikeutta, joita käytetään tämän tehtävän suorittamiseen, ota yhteys järjestelmänvalvojaan ja anna seuraavassa taulukossa näkyvät tiedot.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Luokka</th>
<th>Edellytys</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Käyttöoikeusroolit ja velvollisuudet</td>
<td>Jos haluat määrittää ja luoda EU-merkinnän varmenteita nimikkeille tai palveluille, sinun on oltava sellaisen käyttöoikeusroolin jäsen, johon sisältyy seuraavat tehtävät:
<ul>
<li><strong>Myyntireskontran käsittelijä</strong> (CustInvoiceAccountsReceivableClerk)</li>
<li><strong>Asiakaspalvelun edustaja</strong> (TradeCustomerServiceRepresentative)</li>
<li><strong>Myyjä</strong> (TradeSalesClerk)</li>
<li><strong>Kuljetushenkilö</strong> (InventShippingClerk)</li>
</ul></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]