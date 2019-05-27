---
title: Laskun kirjoittamisen takaraja
description: Tässä artikkelissa kerrotaan, kuinka voit määrittää parametrit, joiden avulla lasketaan eräpäivät lähetettäville myynti- ja toimittajalaskuille Euroopan Unionissa (EU).
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, LedgerInvoiceIssueDueDateSetup_W
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10923
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Iceland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c6a8b4c187678d01a3c61818bb7c300f12555a3
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537863"
---
# <a name="invoice-issue-deadline"></a>Laskun kirjoittamisen takaraja

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, kuinka voit määrittää parametrit, joiden avulla lasketaan eräpäivät lähetettäville myynti- ja toimittajalaskuille Euroopan Unionissa (EU).

Euroopan unionin (EU) direktiivi 45/2010 ja muut direktiivit edellyttävät, että EU:n sisäiset lähetykset (intra-EU lähetykset) on laskutettava joko toimituksen jälkeisen kuun viidentenätoista päivänä tai sitä aikasemmin. Samanaikaisesti, jokaisella EU-maalla voi olla erilaisia laskutuksen takarajoja kotimaan toimituksille. Laskun eräpäivä-toiminnolla voit asettaa päivämäärävälin maiden / kuntien mukaan. Tällöin kaikissa toimituksissa tiettyyn maahan / alueelle tai sieltä pois, laskun eräpäivän päivämäärä lasketaan käyttämällä sääntöjä, jotka ovat määritettyjä tietylle päivämäärävälille. Lisäksi, saat kaikki pakkausluettelot, joissa on tietty laskun eräpäivä, voit suodattaa laskun eräpäivän mukaan kausittaisen myyntilaskutuksen aikan ja hallita myyntilaskun päivämäärää laskun kirjauksen yhteydessä. Voit määrittää päivämääräväli koodin ja sitten asettaa laskusäännön laskun kirjoituspäivälle määrittämällä päivämääräväli koodin maa- / aluetyyppiin. Laskentasääntöä käytetään määräpäivän laskemiseksi julkaistaville laskuille seuraavissa tapahtumissa:

-   EU:n sisäiset lähetykset
-   Kotimaan toimitukset EU-jäsenvaltiossa

Voit myös luoda päivämäärän tarkistukset varmistamaan, että asiakkaiden laskut ja asiakastapahtumien hyvityslaskut luodaan määritellyn ajanjakson kuluttua siitä, kun toimitus on tapahtunut.

## <a name="prerequisites"></a>Edellytykset
Seuraavassa taulukossa on esitetty ne edellytykset, joiden on oltava kohdallaan, ennen kuin laskun eräpäivän päivämäärän toimintoja voi käyttää.

| Luokka            | Edellytys                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Maa/alue      | Yrityksen ensisijainen osoitteen on oltava EU-jäsenvaltiossa.                                                                                                                                                                                                                                                                                                                    |
| Liittyvät asetustehtävät | **Päivämäärävälit**-sivulla määritetään päivämääräväli, jota käytetään laskemaan laskun eräpäivä. (Valitse **Kirjanpito** &gt; **Kirjanpidon asetukset** &gt; **Päivämäärävälit**.) Määritä **Ulkomaankaupan parametrit** -sivulla ulkomaankaupan ominaisuudet eri maille/alueille. (Valitse **Verot** &gt; **Asetukset** &gt; **Ulkomaankauppa** &gt; **Ulkomaankaupan parametrit**.) |

## <a name="invoice-issue-due-date-calculation-rule"></a>Laskuvirhe päivämäärän laskentasäännön takia
Käytä **Määritä laskusääntö laskun kirjoituspäivälle**-sivua määrittämään laskun kirjoituspäivän eräpäivän laskusäännön asettamalla päivämäärävälikoodin maa- / aluetyyppiin.

## <a name="date-control-parameters-for-customer-invoices-and-credit-notes"></a>Asiakaslaskujen ja hyvityslaskujen päivämäärien hallintaparametrit
Voit asettaa päivämäärän hallintaparametrit varmistamaan, että asiakkaiden laskut ja asiakastapahtumien hyvityslaskut luodaan määritellyn ajanjakson kuluttua siitä, kun toimitus on tapahtunut. Löydät nämä parametrit **laskun päivämäärän tarkistus** -alueelta **myyntireskontran parametrit** -sivulla.

## <a name="example"></a>Esimerkki
Määritä Microsoft Dynamics 365 for Finance and Operations laskemaan laskun kirjoittamisen eräpäivät EU:n sisäisiin toimituksiin, toimitusta seuraavan kuun 15. päivänä, luomalla päivämäärävälin koodi ja laskemissääntö seuraavilla asetuksilla:

### <a name="date-interval-code"></a>Päivämäärävälin koodi

| Kenttä                                                           | Arvo                           |
|-----------------------------------------------------------------|---------------------------------|
| Päivämäärävälin koodi                                              | 15-NM                           |
| Kuvaus                                                     | Seuraavan kuukauden viidestoista päivä |
| Ennen (**Päivämäärään**-kenttäryhmässä)                         | Kuukausi                           |
| Aloita / Lopeta (**Päivämäärään**-kenttäryhmässä)                      | Lopeta                             |
| +/- (**Päivämäärään**-kenttäryhmässä)                            | 15                              |
| Päivät, kuukaudet, vuodet tai kaudet (**Päivämäärään**-kenttäryhmässä) | Päivää                            |

### <a name="invoice-issue-due-date-calculation-rule"></a>Laskuvirhe päivämäärän laskentasäännön takia

| Kenttä               | Arvo                                                     |
|---------------------|-----------------------------------------------------------|
| Maa-/aluetyyppi | **EU**                                                    |
| Alkamispäivä          | Määritä päivämäärä, milloin nykyinen asetusrivi tulee voimaan. |
| Päivämäärävälin koodi  | **15-NM**                                                 |

## <a name="next-steps"></a>Seuraavat vaiheet
Kun olet lopettanut laskujen kirjoittamisen eräpäiväparametrien määrittämisen, voit luoda ja kirjata seuraavat tapahtumat, jolloin laskujen kirjoittamisen eräpäivät lasketaan ja päivitetään automaattisesti.

-   **Myyntitilaukset** – Kun luot myyntitilauksen ja kirjaat pakkausluettelon, laskun luonnin eräpäivä lasketaan ja päivitetään pakkausluettelossa. Määräpäivä lasketaan myyntitilauksen toimitusosoitteeseen määritettyyn maahan/alueeseen liitetyn päivämäärävälin perusteella. Sen jälkeen kun olet kirjannut pakkausluettelon, voit varmistaa laskun eräpäivän **Laskun kirjoittamisen eräpäivä** -kentässä **Pakkausluettelo-kirjauskansio**-sivulla. (Valitse **Myynti ja markkinointi** &gt; **Myyntitilaus** &gt; **Tilauksen toimitus** &gt; **Pakkausluettelo**.) Voit tarkastella kaikkia laskuttamattomia pakkausluetteloita ja niiden laskuille määritettyjä eräpäiviä **Laskuttamattomat pakkausluettelot** -sivulla. (Valitse **Myynti ja markkinointi** &gt; **Myyntitilaus** &gt; **Tilauksen toimitus** &gt; **Laskuttamattomat pakkausluettelot**.)
-   **Ostotilaukset** – Kun luot ostotilauksen ja kirjaat tuotteen vastaanoton, laskun luonnin eräpäivä lasketaan ja päivitetään tuotteen vastaanotossa. Määräpäivä lasketaan toimittajan ensisijaiseen osoitteeseen määritettyyn maahan/alueeseen liitetyn päivämäärävälin perusteella. Sen jälkeen kun olet kirjannut tuotteen vastaanoton, voit varmistaa laskun eräpäivän **laskun eräpäivä** -kentässä **tuotteen vastaanoton kirjauskansio**-sivulla. (Valitse **Hankinta** &gt; **Ostotilaukset** &gt; **Vastaanotetaan tuotteita** &gt; **Tuotteen vastaanotto**.) Voit tarkastella kaikkia laskuttamattomia vastaanottokuitteja ja niiden laskuille määritettyjä eräpäiviä **Laskuttamattomat tuotevastaanotot** -sivulla. (Valitse **Hankinta** &gt; **Ostotilaukset** &gt; **Vastaanotetaan tuotteita** &gt; **Laskuttamattomat tuotevastaanotot**.)

## <a name="technical-information-for-system-administrators"></a>Teknisiä tietoja järjestelmänvalvojille
Jos sinulla ei ole pääsyä niiden sivujen käyttöön, joita käytetään tässä artikkelissa kuvattujen tehtävien suorittamiseen, ota yhteys järjestelmänvalvojaan ja anna tiedot, jotka näkyvät seuraavassa taulukossa.

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
<td>Configuration Keys</td>
<td>Klikkaa <strong>Järjestelmän hallinta</strong> &gt; <strong>Asetukset</strong> &gt; <strong>Käyttöoikeudet</strong> &gt; <strong>Käyttöoikeuden konfiguraatio</strong>. Klikkaa <strong>kirjanpito</strong>-määritysavainta.</td>
</tr>
<tr class="even">
<td>Käyttöoikeusroolit ja velvollisuudet</td>
<td>Suorittaaksesi tämän tehtävän, sinun on oltava sellaisen käyttöoikeusroolin jäsen, johon sisältyy seuraavat tehtävät:
<ul>
<li><strong>CustInvoiceInvoiceAndCashProcessEnable</strong> (Ota käyttöön laskutus- ja käteisvaraprosessit)</li>
<li><strong>VendInvoiceInvoicePaymentProcessEnable</strong> (Ota käyttöön laskutus- ja maksuprosessi)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Käyttöoikeusroolit ja oikeudet</td>
<td>Suorittaaksesi tämän tehtävän, sinun on oltava sellaisen käyttöoikeusroolin jäsen, johon sisältyy seuraavat oikeudet:
<ul>
<li><strong>CustPackingSlipJournalView</strong> (Näytä myyntipakkausluettelot)</li>
<li><strong>VendPackingSlipJournalView</strong> (Näytä tuotteen vastaanoton kirjauskansio ostotilauksesta)</li>
<li><strong>LedgerInvoiceIssueDueDateSetupMaintain_W</strong> (Laske laskun kirjoittamisen eräpäivät)</li>
</ul></td>
</tr>
</tbody>
</table>





