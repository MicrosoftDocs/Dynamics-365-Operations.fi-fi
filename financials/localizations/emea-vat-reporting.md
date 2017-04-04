---
title: ALV-raportoinnin Euroopassa
description: "Tässä aiheessa on yleistietoja asettaminen ja joissakin Euroopan maissa arvonlisävero (ALV)-lauseen muodostaminen."
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

# <a name="vat-reporting-for-europe"></a>ALV-raportoinnin Euroopassa

Tässä aiheessa on yleistietoja asettaminen ja joissakin Euroopan maissa arvonlisävero (ALV)-lauseen muodostaminen.

Tämä ohjeaihe sisältää yleisen lähestymistavan määrittäminen ja ALV-ilmoitus luodaan. Tämä lähestymistapa on yleistä oikeushenkilöiden seuraavissa maissa/alueilla:

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
ALV-ilmoituksessa ALV-tapahtumien summat perustuvat. ALV-ilmoituksen pääpiirteittäin kuuluu arvonlisäveron maksamisen aikana, joka toteutetaan-selvitettyjen ja kirjaa ALV-toimintoa. Tämä funktio laskee arvonlisävero, joka erääntyy tiettynä ajanjaksona. Tilityksen laskenta sisältää kirjatun arvonlisäveron valitulta tilityskaudelta valittuun tilityskauteen. ALV-ilmoituksen tiedot lasketaan prosessin perustuu arvonlisäverokoodit ja arvonlisäveroilmoituksen koodit, jossa ALV-raporttien koodit vastaavat ALV lauseita ruutuihin (tai XML-tunnisteet) välinen suhde. Kunkin arvonlisäverokoodin Arvonlisäveron koodit pitäisi määrittää kunkin tyyppisen liiketoimen Verollinen myynti, kuten veron ostoihin verollisen tuonnin. Näiden tapahtumien tyyppi on kuvattu [arvonlisäverokoodit ALV-raportoinnissa](#Sales tax codes for VAT reporting) jäljempänä tässä ohjeaiheessa olevassa osassa.

Jokaisen arvonlisäveroilmoituksen koodin olisi määritettävä raportissa tiettyä sarakeasettelua. Samaan aikaan arvonlisäverokoodit on linkitetty tiettyyn Arvonlisäveroviranomaisen arvonlisäveron tilityskaudet kautta. Jokaiselle arvonlisäveroviranomaiselle olisi määritettävä raportin asettelua. Näin ollen ainoastaan raportointikoodeja, joilla on sama raporttiasettelu, jossa on määritetty ALV-viranomaisen arvonlisäverokoodin arvonlisäveron tilityskausia Arvonlisäveron voidaan valita arvonlisäverokoodin raportin määritykseen. Kirjatessa tilauksen tai päiväkirjasta, luo arvonlisäverotapahtuman sisältää arvonlisäveron, arvonlisäveron lähteen, arvonlisäveron suunta ja tapahtumasummat (veron peruste ja ALV-summa-kirjanpitovaluutta ja valuutan ALV tapahtumavaluutta). Perusteella vero tapahtuman määritteiden yhdistelmä, tapahtumasummat laatia kokonaissummat arvonlisäveroilmoituksen koodit, jotka on määritetty arvonlisäverokoodit. Seuraavassa kuvassa näkyy tietojen suhteen.

![kaavio](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a>ALV-ilmoituksen asetukset
Voit luoda ALV-ilmoitusta on määritettävä seuraavasti.

### <a name="sales-tax-authorities-for-vat-reporting"></a>Veroviranomaiselle ALV-raportointia varten

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-authorities/). -->
Ennen kuin voit määrittää arvonlisäveroilmoituksen koodit, sinun on valittava oikea asettelu arvonlisäveroviranomaiselle. - **Arvonlisäveroviranomaisten**, sivu **yleisen** -osassa **raporttiasettelu**. Tämä asettelu, jota käytetään määrittäessäsi arvonlisäveroilmoituksen koodit.

### <a name="sales-tax-reporting-codes"></a>Arvonlisäveroilmoituksen koodit

ALV-Ilmoituskoodit ovat koodit, ALV-ilmoituksen tai tunnisteen nimet XML-muodossa. Näitä koodeja käytetään keräämään ja valmistella raportin summat. Sähköisen ALV-ilmoituksen raportin muoto määrittäessäsi yhteenlaskettu tulos nimiä käytetään. Voit luoda ja ylläpitää arvonlisäveroilmoituksen koodit **arvonlisäveroilmoituksen koodit** sivulla. Jokaiselle koodille tulee määrittää raporttiasettelu. Kun olet luonut arvonlisäveroilmoituksen koodit, voit valita koodit **raportin asetukset** jakso **arvonlisäverokoodien** sivun. <!---For more information, see [Set up sales tax reporting codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-reporting-codes/) and [Sales tax reporting codes page (Field descriptions)](http://ax.help.dynamics.com/en/wiki/sales-tax-reporting-codes-page-field-descriptions/).-->

### <a name="sales-tax-codes-for-vat-reporting"></a>Arvonlisäverokoodit ALV-raportointia varten

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-codes/).-->Perustaa määrät ja ALV-summat ALV-tapahtumia voidaan koota raportointikoodit ALV-ilmoituksen (XML-tunnisteita tai ilmoituksen ruutuihin). Voit määrittää tämän liittämällä arvonlisäveroilmoituksen koodit eri tapahtumalajien arvonlisäverokoodin ilmoituskoodit **arvonlisäverokoodien** sivulla. Seuraavassa taulukossa kuvataan raportin arvonlisäverokoodeja asetukset kauppatapahtuman luonteet. Laskenta sisältää kaiken tyyppisiä lähteitä, lukuun ottamatta arvonlisäveroa tapahtumat.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Transaction type</strong></td>
<td><strong>Tapahtumat ja summat lasketaan tapahtuman tyypin kuvaus</strong></td>
</tr>
<tr class="even">
<td><strong>Verollinen myynti</strong></td>
<td>Summa <strong>veron perustesummaan</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valittu kausi tai</li>
<li>Myynnistä on kotimaan (<strong>arvonlisäveron suunta</strong> on <strong>ALV-velat</strong>).</li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Veroton myynti</strong></td>
<td>Summa <strong>veron perustesummaan</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
<li>Myydään vienti (<strong>arvonlisäveron suunta</strong> on <strong>Verovapaa myynti</strong>).</li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sales tax payable</strong></td>
<td>Summa <strong>ALV-summat</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
<li>Myynnistä on kotimaan (<strong>arvonlisäveron suunta</strong> on <strong>ALV-velat</strong>).</li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Taxable sales credit note</strong></td>
<td>Summa <strong>veron perustesummaan</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
<li>Myynnistä on kotimaan (<strong>arvonlisäveron suunta</strong> on <strong>ALV-velat</strong>).</li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Faksin Verovapaa hyvityslasku</strong></td>
<td>Summa <strong>veron perustesummaan</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
<li>Myydään vienti (<strong>arvonlisäveron suunta</strong> on <strong>Verovapaa myynti</strong>).</li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Sales tax on sales credit note</strong></td>
<td>Summa <strong>ALV-summat</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
<li>Myynnistä on kotimaan (<strong>arvonlisäveron suunta</strong> on <strong>ALV-velat</strong>).</li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable purchases</strong></td>
<td>Summa <strong>veron perustesummaan</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
<li>Osto on kotimaa (<strong>arvonlisäveron suunta</strong> on <strong>ALV-saatavat</strong>).</li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Tax-free purchase</strong></td>
<td>Summa <strong>veron perustesummaan</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
<li>Osto on tuo (<strong>arvonlisäveron suunta</strong> on <strong>Verovapaa osto</strong>).</li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sales tax receivable</strong></td>
<td>Summa <strong>ALV-summat</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
<li>Osto on kotimaa (<strong>arvonlisäveron suunta</strong> on <strong>ALV-saatavat</strong>).</li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Taxable purchase credit note</strong></td>
<td>Summa <strong>veron perustesummaan</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
<li>Osto on kotimaa (<strong>arvonlisäveron suunta</strong> on <strong>ALV-saatavat</strong>).</li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Tax exempt purchase credit note</strong></td>
<td>Summa <strong>veron perustesummaan</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
<li>Osto on tuo (<strong>arvonlisäveron suunta</strong> on <strong>Verovapaa osto</strong>).</li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Sales tax on purchase credit note</strong></td>
<td>Summa <strong>ALV-summat</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
<li>Osto on kotimaa (<strong>arvonlisäveron suunta</strong> on <strong>ALV-saatavat</strong>).</li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable import</strong></td>
<td>Summa <strong>veron perustesummaan</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
<li><strong>Veron suunta</strong> on <strong>Käytä veroa</strong></li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset taxable import</strong></td>
<td>Palautettu summa <strong>veron perustesummaan</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
<li><strong>Veron suunta</strong> on <strong>Käytä veroa</strong>.</li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable import credit note</strong></td>
<td>Summa <strong>veron perustesummaan</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
e<li><strong>Veron suunta</strong> on <strong>Käytä veroa</strong>.</li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset taxable import credit note</strong></td>
<td>Palautettu summa <strong>veron perustesummaan</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
<li>Veron suunta on <strong>Käytä veroa</strong>.</li>
d<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Use tax</strong></td>
<td>Summa <strong>ALV-summat</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
<li><strong>Veron suunta</strong> on <strong>Käytä veroa</strong>.</li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset use tax</strong></td>
<td>Palautettu summa <strong>ALV-summat</strong>, verotapahtumat, jotka täyttävät seuraavat edellytykset:
<ul>
<li>Tapahtumapäivä on valitulla kaudella.</li>
<li><strong>Veron suunta</strong> on <strong>Käytä veroa</strong>.</li>
<li>Tapahtuman <strong>veron perusteeseen</strong> tai <strong>vero</strong>&gt; 0.</li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Edellä olevassa taulukossa oletetaan, että seuraavat ehdot täyttyvät: 
> -   Veron perusteeseen on tapahtumasumman **alkuperästä kirjanpitovaluuttana** kenttä.
> -   ALV-summa on siirtymä summasta **todellinen arvonlisäverosumma kirjanpitovaluuttana** kenttä.

### <a name="configure-the-er-model-and-format-for-the-report"></a>ER-mallin ja raportin muodon määrittäminen

Voit käyttää sähköisen raportoinnin (ER) lauseita ja raportin ja viedä tietoja eri sähköisessä muodossa muuttamatta X ++-koodia. Lisätietoja:

-   [Sähköisen raportoinnin yleiskatsaus](/dynamics365/operations/dev-itpro/dev-itpro/analytics/general-electronic-reporting)
-   [Lataa sähköiset raportoinnin määritykset Lifecycle Services -palvelusta](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)
-   [Lokalisoinnin vaatimukset – GER-konfiguraation luominen](/dynamics365/operations/dev-itpro/analytics/electronic-reporting-configuration)

## <a name="countryspecific-resources-for-vat-statements"></a>ALV-ilmoitusten Countryspecific resurssit
ALV-ilmoituksen kunkin maan on täytettävä sen maan lainsäädännön vaatimukset. On ennalta määritetyt mallit ja muodot ALV-ilmoitusten seuraavassa taulukossa lueteltuihin maihin.


| Maa tai alue        | Lisätiedot                                                          |
|----------------|---------------------------------------------------------------------------------|
| Itävalta        |  [ALV-ilmoituksen erittely Itävalta](emea-aut-vat-statement-details.md)         |
| Belgia        |                                                                                 |
| Tšekin tasavalta |  [Tsekin tasavallan ALV tiliotteen tiedot](emea-cze-vat-statement-details.md)   |
| Viro        |  [ALV-ilmoituksen erittely Viro](emea-est-vat-statement-details.md) |
| Suomi        |                                                                                 |
| Saksa        |                                                                                 |
| Italia          | [Italian ALV tiliotteen tiedot](emea-ita-vat-statements-details.md)            |
| Latvia         | [ALV-ilmoituksen erittely Latvia](emea-lva-vat-statement-details.md)           |
| Liettua      | [ALV-ilmoituksen erittely Liettua](emea-ltu-vat-statement-details.md)         |
| Alankomaat    |                                                                                 |
| Ruotsi         |                                                                                 |




