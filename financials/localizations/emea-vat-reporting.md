---
title: ALV-raportointi Euroopassa
description: "Tässä aiheessa on yleistietoja (ALV)-lauseen määrittämisestä ja muodostamisesta joissakin Euroopan maissa."
author: ShylaThompson
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266844
ms.assetid: 06798e29-6140-489e-9b4e-66b45b26be2b
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 84a639b25c64821e00ca4397f42f69298953e599
ms.lasthandoff: 03/31/2017


---

# <a name="vat-reporting-for-europe"></a>ALV-raportointi Euroopassa

Tässä aiheessa on yleistietoja (ALV)-lauseen määrittämisestä ja muodostamisesta joissakin Euroopan maissa.

Tämä ohjeaihe sisältää yleisen lähestymistavan ALV-ilmoituksen määrittämiseen ja luomiseen. Tämä lähestymistapa on yhteinen yrityksille seuraavissa maissa/alueilla:

-   Itävalta
-   Belgia
-   Tšekin tasavalta
-   Viro
-   Suomi
-   Saksa
-   Latvia
-   Liettua
-   Alankomaat
-   Ruotsi

## <a name="vat-statement-overview"></a>ALV-ilmoituksen yhteenveto
ALV-ilmoitus perustuu verotapahtumien summiin. ALV-ilmoituksen luomisprosessi kuuluu arvonlisäveron maksamisen prosessiin, joka toteutetaan Tilitä ja kirjaa arvonlisävero -toiminnon avulla. Tämä toiminto laskee arvonlisäveron, joka erääntyy tiettynä aikana. Tilityksen laskenta sisältää kirjatun arvonlisäveron valitulta tilityskaudelta verotapahtumille. ALV-ilmoituksen tietojen laskentaprosessi perustuu arvonlisäverokoodien ja arvonlisäveroilmoituksen koodien suhteeseen, jossa ALV-raporttikoodit vastaavat ALV-ilmoitusten ruutuja (tai XML-tunnisteita). Kullekin arvonlisäverokoodille arvonlisäveron raportointikoodit pitäisi määrittää kunkin tyyppiselle tapahtumalle, kuten verolliselle myynnille, verollisille ostoille tai verolliselle tuonnille. Näiden tapahtumien tyyppi on kuvattu [Arvonlisäverokoodit ALV-raportoinnissa](#Sales tax codes for VAT reporting) -osassa jäljempänä tässä ohjeaiheessa.

Jokaiselle arvonlisäveroilmoituksen koodille olisi määritettävä tietty raporttiasettelu. Samaan aikaan arvonlisäverokoodit on linkitetty tiettyyn arvonlisäveroviranomaiseen arvonlisäveron tilityskausien kautta. Jokaiselle arvonlisäveroviranomaiselle olisi määritettävä raporttiasettelu. Näin ollen ainoastaan raportointikoodeja, joilla on sama raporttiasettelu, joka on määritetty ALV-viranomaiselle arvonlisäverokoodin arvonlisäveron tilityskausissa, voidaan valita arvonlisäverokoodin raportin määrityksessä. Arvonlisäverotapahtuma, joka luodaan kirjatessa tilauksen tai päiväkirjan, sisältää arvonlisäverokoodin, arvonlisäveron lähteen, arvonlisäveron suunnan ja tapahtumasummat (veron peruste ja verosumma kirjanpitovaluuttana, ALV-valuutta ja tapahtumavaluutta). Perustuen verotapahtuman määritteiden yhdistelmään, tapahtumasummat koostavat kokonaissummat arvonlisäverokoodeille määritetyille arvonlisäveroilmoituksen koodeille. Seuraavassa on kuvattu tietojen suhdetta.

![Kaavio](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a>ALV-ilmoituksen asetukset
Voit luoda ALV-ilmoituksen määrittämällä seuraavat.

### <a name="sales-tax-authorities-for-vat-reporting"></a>Veroviranomaiset ALV-raportointia varten

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-authorities/). -->
Ennen kuin voit määrittää arvonlisäveroilmoituksen koodit, sinun on valittava oikea raporttiasettelu arvonlisäveroviranomaiselle. Valitse **Arvonlisäveroviranomaiset**-sivulla **Yleiset**-osassa **Raportin asettelu**. Tätä asettelua käytetään määrittäessäsi arvonlisäveroilmoituksen koodit.

### <a name="sales-tax-reporting-codes"></a>Arvonlisäveroilmoituksen koodit

ALV-ilmoituskoodit ovat ruutukoodeja ALV-ilmoituksessa tai tunnisteen nimiä XML-muodossa. Näitä koodeja käytetään keräämään ja valmistelemaan raportin summat. ALV-ilmoituksen sähköisen raportoinnin muotoa määrittäessäsi käytetään tulossummien nimiä. Voit luoda ja ylläpitää arvonlisäveroilmoituksen koodeja **Arvonlisäveroilmoituksen koodit** -sivulla. Jokaiselle koodille tulee määrittää raporttiasettelu. Kun olet luonut arvonlisäveroraportin koodit, voit valita koodeja **Arvonlisäverokoodit**-sivun **Raportin asetukset** -osassa. <!---For more information, see [Set up sales tax reporting codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-reporting-codes/) and [Sales tax reporting codes page (Field descriptions)](http://ax.help.dynamics.com/en/wiki/sales-tax-reporting-codes-page-field-descriptions/).-->

### <a name="sales-tax-codes-for-vat-reporting"></a>ALV-ilmoituksen arvonlisäverokoodit

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-codes/).--> Arvonlisäverotapahtumien perussummat ja verosummat voidaan koostaa ALV-ilmoituksen raportointikoodeista (XML-tunnisteista tai ilmoitusruuduista). Voit määrittää tämän liittämällä arvonlisäveroilmoituksen koodit arvonlisäverokoodien eri tapahtumalajeille **Arvonlisäverokoodit** -sivulla. Seuraavassa taulukossa kuvataan tapahtumatyypit arvonlisäverokoodien raporttiasetuksissa. Laskenta sisältää tapahtumia kaiken tyyppisille lähteille lukuun ottamatta arvonlisäveroa.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Tapahtumalaji</strong></td>
<td><strong>Tapahtumien kuvaus ja tapahtumatyypille laskettavat summat</strong></td>
</tr>
<tr class="even">
<td><strong>Verollinen myynti</strong></td>
<td>Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa/</li>
<li>Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Verovapaa myynti</strong></td>
<td>Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
<li>Myynti on vientiä (<strong>Veron suunta</strong> on <strong>Verovapaa myynti</strong>).</li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Maksettava arvonlisävero</strong></td>
<td>Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
<li>Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Verollinen hyvityslasku</strong></td>
<td>Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
<li>Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Verovapaa hyvityslasku</strong></td>
<td>Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
<li>Myynti on vientiä (<strong>Veron suunta</strong> on <strong>Verovapaa myynti</strong>).</li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Myyntihyvityslaskun arvonlisävero</strong></td>
<td>Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
<li>Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Verollinen osto</strong></td>
<td>Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
<li>Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Verovapaa osto</strong></td>
<td>Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
<li>Osto on tuontia (<strong>Veron suunta</strong> on <strong>Verovapaa osto</strong>).</li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Saatava arvonlisävero</strong></td>
<td>Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
<li>Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Verollinen ostohyvityslasku</strong></td>
<td>Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
<li>Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Verovapaa ostohyvityslasku</strong></td>
<td>Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
<li>Osto on tuontia (<strong>Veron suunta</strong> on <strong>Verovapaa osto</strong>).</li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Ostohyvityslaskun arvonlisävero</strong></td>
<td>Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
<li>Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Verollinen tuonti</strong></td>
<td>Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
<li><strong>Veron suunta</strong> on <strong>Käyttövero</strong></li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Verollinen tuonti vastakirjaus</strong></td>
<td>Verotapahtumien <strong>Veron perustesummien</strong> käänteinen summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
<li><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Verollinen tuontihyvitysmaksu</strong></td>
<td>Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
e<li><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Verollinen tuontihyvityslasku vastakirjaus</strong></td>
<td>Verotapahtumien <strong>Veron perustesummien</strong> käänteinen summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
<li>Veron suunta on <strong>Käyttövero</strong>.</li>
d<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Käyttövero</strong></td>
<td>Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
<li><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Käyttöveron vastakirjaus</strong></td>
<td>Verotapahtumien <strong>Verosummien</strong> käänteinen summa tapahtumille, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitussa kaudessa.</li>
<li><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</li>
<li>Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Edellä olevassa taulukossa oletetaan, että seuraavat ehdot täyttyvät: 
> -   Veron perustesumma on tapahtumasumma **Alkuperäinen summa kirjanpitovaluuttana** -kentästä.
> -   Veron summa on tapahtumasumma **Toteutunut arvonlisäverosumma kirjanpitovaluuttana** -kentästä.

### <a name="configure-the-er-model-and-format-for-the-report"></a>Raportin ER-mallin ja muodon määrittäminen

Voit käyttää sähköistä raportointia (ER) määrittääksesi ilmoituksia ja raportteja sekä viedäksesi tietoja eri sähköisissä muodoissa muuttamatta X++ -koodia. Lisätietoja:

-   [Sähköisen raportoinnin yleiskatsaus](/dynamics365/operations/dev-itpro/dev-itpro/analytics/general-electronic-reporting)
-   [Lataa sähköiset raportoinnin määritykset Lifecycle Services -palvelusta](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)
-   [Lokalisoinnin vaatimukset – GER-konfiguraation luominen](/dynamics365/operations/dev-itpro/analytics/electronic-reporting-configuration)

## <a name="countryspecific-resources-for-vat-statements"></a>ALV-ilmoitusten maakohtaiset resurssit
Kunkin maan ALV-ilmoituksen on täytettävä sen maan lainsäädännön vaatimukset. On olemassa ennalta määritetyt mallit ja muodot ALV-ilmoituksille seuraavassa taulukossa luetelluissa maissa.


| Maa tai alue        | Lisätiedot                                                          |
|----------------|---------------------------------------------------------------------------------|
| Itävalta        |  [ALV-ilmoituksen erittely, Itävalta](emea-aut-vat-statement-details.md)         |
| Belgia        |                                                                                 |
| Tšekin tasavalta |  [ALV-ilmoituksen tiedot, Tšekin tasavalta](emea-cze-vat-statement-details.md)   |
| Viro        |  [ALV-ilmoituksen erittely, Viro](emea-est-vat-statement-details.md) |
| Suomi        |                                                                                 |
| Saksa        |                                                                                 |
| Italia          | [ALV-ilmoituksen erittely, Italia](emea-ita-vat-statements-details.md)            |
| Latvia         | [ALV-ilmoituksen erittely, Latvia](emea-lva-vat-statement-details.md)           |
| Liettua      | [ALV-ilmoituksen erittely, Liettua](emea-ltu-vat-statement-details.md)         |
| Alankomaat    |                                                                                 |
| Ruotsi         |                                                                                 |




