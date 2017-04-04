---
title: Laskun kirjoittamisen takaraja
description: "Tässä artikkelissa kerrotaan, kuinka voit määrittää parametrit, joiden avulla lasketaan eräpäivät lähetettäville myynti- ja toimittajalaskuille Euroopan Unionissa (EU)."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustParameters, LedgerInvoiceIssueDueDateSetup_W
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10923
ms.assetid: 64ea3343-df94-4a52-b839-6328c8a282bd
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Iceland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 6121be0dd02659e4e8466b0c1381678be64fefc2
ms.lasthandoff: 03/31/2017


---

# <a name="invoice-issue-deadline"></a>Laskun kirjoittamisen takaraja

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
| Liittyvät asetustehtävät | **Päivämäärävälit**-sivulla määritetään päivämääräväli, jota käytetään laskemaan laskun eräpäivä. (Valitse **kirjanpidon**&gt;**Pääkirjanpidon asetukset**&gt;**päivä välein**.) - **Ulkomaankaupan parametrit** -sivulla Määritä Ulkomaankauppa ominaisuudet eri maita/alueita. (Valitse **vero**&gt;**asennus**&gt;**ulkomaankaupan**&gt;**Ulkomaankaupan parametrit**.) |

## <a name="invoice-issue-due-date-calculation-rule"></a>Laskuvirhe päivämäärän laskentasäännön takia
Käytä **Määritä laskusääntö laskun kirjoituspäivälle**-sivua määrittämään laskun kirjoituspäivän eräpäivän laskusäännön asettamalla päivämäärävälikoodin maa- / aluetyyppiin.

## <a name="date-control-parameters-for-customer-invoices-and-credit-notes"></a>Asiakaslaskujen ja hyvityslaskujen päivämäärien hallintaparametrit
Voit asettaa päivämäärän hallintaparametrit varmistamaan, että asiakkaiden laskut ja asiakastapahtumien hyvityslaskut luodaan määritellyn ajanjakson kuluttua siitä, kun toimitus on tapahtunut. Löydät nämä parametrit **laskun päivämäärän tarkistus** -alueelta **myyntireskontran parametrit** -sivulla.

## <a name="example"></a>Esimerkki
Microsoft Dynamics-365 toimintoihin lasketaan laskun ongelman määrittäminen eräpäivien sisäisessä ja EU: N toimitukset kuukauden jälkeen tarjonta on toimitettu 15 päivän, päivämäärävälin koodi- ja säännön luominen, jossa on seuraavat asetukset.

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

-   **Myyntitilaukset** – Kun luot myyntitilauksen ja kirjaat pakkausluettelon, laskun luonnin eräpäivä lasketaan ja päivitetään pakkausluettelossa. Eräpäivä lasketaan, joka liittyy maan tai alueen, joka on määritetty myyntitilauksen toimitusosoite päivämäärävälin perusteella. Kun kirjaat pakkausluettelon, voit tarkistaa laskun ongelma eräpäivä **Laskutus ongelma eräpäivä** kenttä **pakkausluettelon kirjauskansio** sivun. (Valitse **myynti- ja**&gt;**myynti**&gt;**tilauksen toimitus**&gt;**pakkausluettelon**.) Voit tarkastella kaikkien pakkausluetteloiden, jota ei ole laskutettu ja lasku niiden ongelma eräpäivät, edelleen **pakkausluetteloiden, joita ei ole laskutettu** sivulla. (Valitse **myynnin ja markkinoinnin**&gt;**myynti**&gt;**tilauksen toimitus**&gt;**pakkausluetteloita, joita ei ole laskutettu**.)
-   **Ostotilaukset** – Kun luot ostotilauksen ja kirjaat tuotteen vastaanoton, laskun luonnin eräpäivä lasketaan ja päivitetään tuotteen vastaanotossa. Määräpäivä lasketaan toimittajan ensisijaiseen osoitteeseen määritettyyn maahan/alueeseen liitetyn päivämäärävälin perusteella. Sen jälkeen kun olet kirjannut tuotteen vastaanoton, voit varmistaa laskun eräpäivän **laskun eräpäivä** -kentässä **tuotteen vastaanoton kirjauskansio**-sivulla. (Valitse **hankinta**&gt;**ostotilausten**&gt;**tuotteiden vastaanotosta**&gt;**tuotteen vastaanoton**.) Voit tarkastella kaikkien tuotteen vastaanottojen, jota ei ole laskutettu ja lasku niiden ongelma eräpäivät, edelleen **tuotteiden vastaanotot, joita ei ole laskutettu** sivulla. (Valitse **hankinta**&gt;**ostotilausten**&gt;**tuotteiden vastaanotosta**&gt;**tuotteen vastaanotot, joita ei ole laskutettu**.)

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
<td>Valitse <strong>järjestelmän hallinta</strong>&gt;<strong>asennus</strong>&gt;<strong>Licensing</strong>&gt;<strong>käyttöoikeuden konfiguraatio</strong>. Klikkaa <strong>kirjanpito</strong>-määritysavainta.</td>
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




