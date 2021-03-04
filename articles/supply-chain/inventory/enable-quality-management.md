---
title: Laadunhallinnan yleiskuvaus
description: Tässä ohjeaiheessa kerrotaan, miten Dynamics 365 Supply Chain Managementin laadunhallinnan avulla voidaan parantaa toimitusketjun tuotteiden laatua.
author: perlynne
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1d7828e6bb9a3684c1d76e2cfac96174a8dfbf4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427145"
---
# <a name="quality-management-overview"></a>Laadunhallinnan yleiskuvaus

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten Dynamics 365 Supply Chain Managementin laadunhallinnan avulla voidaan parantaa toimitusketjun tuotteiden laatua.

Laadunhallinnan avulla voit hallita määrityksestä poikkeavien tuotteiden käsittelyaikaa niiden lähtöpisteestä riippumatta. Koska vianmääritystyypit linkitetään korjausraportointiin, Supply Chain Management voi ajoittaa ongelmien korjaustehtävät ja estää ongelmien toistuminen.

Määrityksistä poikkeamisen hallintatoiminnon lisäksi laadunhallinta sisältää toiminnon ongelmien seuraamiseen ongelmantyypin perusteella (myös sisäiset ongelmat) sekä lyhyt- tai pitkäaikaisen ratkaisun tunnistamiseen. Suorituskykyilmaisimia (KPI) koskevat tilastot antavat tietoja aiemmista määrityksistä poikkeamiseen liittyvistä ongelmista ja niiden korjaamiseen käytetyistä ratkaisuista. Voit tarkistaa historiallisten tietojen avulla, kuinka tehokkaita aiemmat laatutoimet ovat olleet, ja määrittää, mitkä toimet soveltuvat jatkossa käytettäviksi.

Kun määrität laatuliitoksen, Supply Chain Management voi luoda liiketoiminnan eri prosesseille, tapahtumille ja ehdoille laatutilauksia. Laatuliitos voi koskea tiettyä nimikettä, tiettyä nimikeryhmää tai kaikkia nimikkeitä.

## <a name="examples-of-the-use-of-quality-management"></a>Esimerkkejä laadunhallinnan käytöstä
Laadunhallinta on joustavaa ja se voidaan toteuttaa eri tavoin vastaamaan toimitusketjun työvaiheiden tiettyjen tasojen vaatimuksia. Seuraavassa esimerkissä käsitellään näiden ominaisuuksien mahdollisia käyttötapoja:

-   Laadunvalvontaprosessin käynnistäminen automaattisesti ennaltamääritettyjen ehtojen perusteella (kun tietyn toimittajan ostotilaus rekisteröidään varastossa).
-   Varaston esto tarkastuksen aikana, jotta varastoa, jota ei ole hyväksytty, ei käytetä (ostotilausmäärien täysi esto).
-   Nimikeotannan käyttö laatuliitoksen osana määritettäessä tarkastettavan fyysisen varaston tämän hetkistä määrää. Otanta voi perustua kiinteisiin määriin, prosenttiosuuteen tai täyteen rekisterikilpeen.

> [!NOTE]
> _Varastoprosessien laadunhallinta_ -ominaisuus laajentaa laadunhallinnan ominaisuuksia. Jos käytät tätä toimintoa, katso kohdasta [Varaston prosessien laadunhallinta](quality-management-for-warehouses-processes.md) esimerkkejä siitä, miten laadunhallinta toimii, kun se otetaan käyttöön.

-   Luo laatutilaukset osittaisille vastaanotoille. Tilauksen mukana fyysisesti vastaanotettuun määrään perustuva laatutilaus luodaan valitsemalla **Päivitettyä määrää kohden** -valintaruutu **Nimikeotanta**-lomakkeessa.
-   Testin pienimmän, suurimman ja tavoiteltavan arvon sisältävien testityyppien luominen sekä sellaisen määrää ja laatua vertailevan testin suorittaminen, jolla on ennalta määritetyt tarkistustulokset.
-   Hyväksyttävän laadun tason määrittäminen laadun mittaustoleranssien hallintaa varten.
-   Tarkastustyövaiheiden edellyttämien resurssien, kuten testausalueen tai testin mittavälineiden, määrittäminen.

## <a name="working-with-quality-associations"></a>Laatuliitosten käsitteleminen
Laatuliitosta käyttävä liiketoimintoprosessi voidaan liittää eri lähdeasiakirjoihin, kuten ostotilauksiin, myyntitilauksiin tai tuotantotilauksiin.

Jokaisessa laatuliitostietueessa määritetään joukko testejä, hyväksyttävän laadun taso ja otantasuunnitelma, jota käytetään muodostettavissa laatutilauksissa. Laatuliitostietue on määritettävä liiketoimintaprosessin jokaiselle muunnokselle. Voit esimerkiksi määrittää laatuliitoksen, joka muodostaa laatutilauksen, kun ostotilauksen tuotteen vastaanotto päivitetään. Toimeenpanosuunnitelma määritysten mukaisesti käynnistävä prosessi voidaan estää, jos laatutilaus on avoinna. Myös seuraavat prosessit, kuten ostotilauksen laskutus, voidaan estää.

**Huomautus:** Jos laatutilauksia on avoinna, varastomäärien otto estetään automaattisesti. **Nimikeotanta**-sivun **Täysi esto** -asetuksen mukaan laatu on joko laatutilauksen määrä tai lähdeasiakirjan rivin määrä.

Tietyn liiketoimintaprosessin laatuliitostietue tunnistaa tapahtuman ja ehdot, joille laatutilaus muodostetaan. Ehdot voivat olla joko toimipaikka- tai yrityskohtaisia. Tuhoavia testejä sisältävä laatutilaus voidaan muodostaa vain, kun tapahtumalla on käytettävissä oleva varasto.

Seuraavassa esimerkeissä käsitellään, miten laatuliitostietue määritetään kunkin liiketoimintaprosessin variaatioille. Seuraavassa taulussa on jokaisen esimerkin yhteenveto laatuliitostietueessa määritetyistä tapahtumista ja ehdoista.

<table>
<tbody>
<tr>
<th>Viitetyyppi</th>
<th>Tapahtumatyyppi</th>
<th>Suoritus</th>
<th>Tapahtuman esto</th>
<th>Tiedostoviite</th>
</tr>
<tr>
<td>Varasto</td>
<td>Ei käytettävissä</td>
<td>Ei käytettävissä</td>
<td>Ei mitään</td>
<td>Kaikki</td>
</tr>
<tr>
<td rowspan="7">Myynti</td>
<td rowspan="4">Keräysprosessi on ajoitettu</td>
<td rowspan="4">Ennen</td>
<td>Ei mitään</td>
<td rowspan="22">Tietty tunnus, ryhmä tai vain kaikki</td>
</tr>
<tr>
<td>Keräysprosessi</td>
</tr>
<tr>
<td>Pakkausluettelo</td>
</tr>
<tr>
<td>Lasku</td>
</tr>
<tr>
<td rowspan="3">Pakkausluettelo</td>
<td rowspan="3">Ennen</td>
<td>Ei mitään</td>
</tr>
<tr>
<td>Pakkausluettelo</td>
</tr>
<tr>
<td>Lasku</td>
</tr>
<tr>
<td rowspan="15">Osto</td>
<td rowspan="7">Vastaanottoluettelo</td>
<td rowspan="4">Ennen</td>
<td>Ei mitään</td>
</tr>
<tr>
<td>Vastaanottoluettelo</td>
</tr>
<tr>
<td>Tuotteen vastaanotto</td>
</tr>
<tr>
<td>Lasku</td>
</tr>
<tr>
<td rowspan="3">Jälkeen</td>
<td>Ei mitään</td>
</tr>
<tr>
<td>Tuotteen vastaanotto</td>
</tr>
<tr>
<td>Lasku</td>
</tr>
<tr>
<td rowspan="3">Rekisteröinti</td>
<td rowspan="3">Ei käytettävissä</td>
<td>Ei mitään</td>
</tr>
<tr>
<td>Tuotteen vastaanotto</td>
</tr>
<tr>
<td>Lasku</td>
</tr>
<tr>
<td rowspan="5">Tuotteen vastaanotto</td>
<td rowspan="3">Ennen</td>
<td>Ei mitään</td>
</tr>
<tr>
<td>Tuotteen vastaanotto</td>
</tr>
<tr>
<td>Lasku</td>
</tr>
<tr>
<td rowspan="2">Jälkeen</td>
<td>Ei mitään</td>
</tr>
<tr>
<td>Lasku</td>
</tr>
<tr>
<td rowspan="8">Tuotanto</td>
<td rowspan="3">Rekisteröinti</td>
<td rowspan="3">Ei käytettävissä</td>
<td>Ei mitään</td>
<td rowspan="12">Kaikki</td>
</tr>
<tr>
<td>Ilmoita valmiiksi</td>
</tr>
<tr>
<td>Lopeta</td>
</tr>
<tr>
<td rowspan="5">Ilmoita valmiiksi</td>
<td rowspan="3">Ennen</td>
<td>Ei mitään</td>
</tr>
<tr>
<td>Ilmoita valmiiksi</td>
</tr>
<tr>
<td>Lopeta</td>
</tr>
<tr>
<td rowspan="2">Jälkeen</td>
<td>Ei mitään</td>
</tr>
<tr>
<td>Lopeta</td>
</tr>
<tr>
<td rowspan="4">Karanteeni</td>
<td rowspan="3">Ilmoita valmiiksi</td>
<td rowspan="2">Ennen</td>
<td>Ilmoita valmiiksi</td>
</tr>
<tr>
<td>Lopeta</td>
</tr>
<tr>
<td>Jälkeen</td>
<td>Lopeta</td>
</tr>
<tr>
<td>Lopeta</td>
<td>Ennen</td>
<td>Lopeta</td>
</tr>
<tr>
<td rowspan="3">Reitityksen työvaihe</td>
<td rowspan="3">Ilmoita valmiiksi</td>
<td rowspan="2">Ennen</td>
<td>Ei mitään</td>
<td rowspan="3">Tietty tunnus, ryhmä tai kaikki tai ryhmäkohtainen, ryhmä tai kaikki</td>
</tr>
<tr>
<td>Ilmoita valmiiksi</td>
</tr>
<tr>
<td>Jälkeen</td>
<td>Ei mitään</td>
</tr>
<tr>
<td rowspan="3">Oheistuotteen tuotanto</td>
<td>Rekisteröinti</td>
<td>Ei käytettävissä</td>
<td rowspan="3">Ei mitään</td>
<td rowspan="3">Kaikki</td>
</tr>
<tr>
<td rowspan="2">Ilmoita valmiiksi</td>
<td>Ennen</td>
</tr>
<tr>
<td>Jälkeen</td>
</tr>
</tbody>
</table>

Seuraavassa taulussa on lisätietoja laatutilausten muodostamisesta tietyntyyppisille prosesseille.
<div class="tableSection">

<table>
<tbody>
<tr>
<th>Prosessin tyyppi</th>
<th>Laatutilausten automaattinen luontiajankohta</th>
<th>Laatutilausten luontiajankohta, jos tuhoava testaus pakollinen</th>
<th>Ehdon tiedot</th>
<th>Manuaalisen luonnin tiedot</th>
</tr>
<tr>
<td>Ostotilaus</td>
<td>Ennen kuin vastaanotetun materiaalin vastaanottoluettelo tai tuotteen vastaanotto on kirjattu tai sen jälkeen</td>
<td>Vastaanotetun materiaalin tuotteen vastaanoton kirjauksen jälkeen, koska materiaalin on oltava käytettävissä tuhoavaa testausta varten</td>
<td>Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai toimittajaan tai näiden ehtojen yhdistelmään.</td>
<td>Manuaalisesti luotu ostotilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</td>
</tr>
<tr>
<td>Karanteenitilaus</td>
<td>Ennen karanteenitilauksen ilmoittamista valmiiksi tai päättyneeksi tai sen jälkeen</td>
<td>Tuhoavia testejä edellyttäviä laatutilauksia ei voi luoda. Karanteenitilaustoiminnon oletetaan käsittelevän tuhottavan materiaalin käsittelyn.</td>
<td>Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai toimittajaan tai näiden ehtojen yhdistelmään.</td>
<td>Manuaalisesti luotu ostotilaukseen viittaava karanteenitilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</td>
</tr>
<tr>
<td>Myyntitilaus</td>
<td>Ennen lähettävien nimikkeiden ajoitettua keräysprosessia tai pakkausluettelon päivitystä</td>
<td>Kaikissa vaiheissa</td>
<td>Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai asiakkaaseen tai näiden ehtojen yhdistelmään.</td>
<td>Manuaalisesti luotu myyntitilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</td>
</tr>
<tr>
<td>Tuotantotilaus</td>
<td>Ennen tuotantotilauksen valmiiksi raportointia tai sen jälkeen</td>
<td>Tuotantotilauksen valmiiksi raportoinnin jälkeen</td>
<td>Laatutilausvaatimus voi liittyä toimipaikkaan tai nimikkeeseen tai näiden ehtojen yhdistelmään.</td>
<td>Manuaalisesti luotu tuotantotilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</td>
</tr>
<tr>
<td>Tuotantotilaus, jossa on reitityksen työvaihe</td>
<td>Ennen työvaiheen raportin valmistumista tai sen jälkeen</td>
<td>Viimeisen työvaiheen tuotannon valmiiksi raportoinnin jälkeen</td>
<td>Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai operatiiviseen resurssiin tai näiden ehtojen yhdistelmään.</td>
<td>Manuaalisesti luotu reitityksen työvaiheeseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</td>
</tr>
<tr>
<td>Varasto</td>
<td>Laatutilausta ei voi luoda automaattisesti varastokirjauskansion tapahtumalle eikä siirtotilaustapahtumille.</td>
<td></td>
<td></td>
<td>Laatutilaus on luotava manuaalisesti nimikkeen varastomäärälle. Fyysistä käytettävissä olevaa varastoa edellytetään.</td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a>Laatutilauksen automaattisen luonnin esimerkkejä

### <a name="purchasing"></a>Osto

Jos asetat ostoissa **Tapahtumatyyppi**-kentän arvoksi **Tuotteen vastaanotto** ja **Suoritus**-kentän arvoksi **Jälkeen** **Laatuliitokset**-sivulla, saat seuraavat tulokset: 

- Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään **Kyllä**, laatutilaus luodaan jokaista vastaanottoa varten ostotilauksen perusteella, jolloin otetaan huomioon vastaanotettu määrä sekä nimikeotannan asetukset. Joka kerta, kun määrä vastaanotetaan ostotilauksen perusteella, luodaaan uusia laatutilauksia juuri saadun määrän perusteella.
- Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään **Ei**, laatutilaus luodaan ensimmäistä vastaanottoa varten ostotilauksen perusteella, jolloin otetaan huomioon vastaanotettu määrä. Lisäksi jäljelle jäävän määrän perusteella luodaan seurantadimensioiden mukaan vähintään yksi laatutilaus. Laatutilauksia ei luoda ostotilauksen perusteella seuraavien vastaanottojen osalta.

### <a name="production"></a>Tuotantoympäristö

Jos asetat tuotannossa **Tapahtumatyyppi**-kentän arvoksi **Ilmoita valmiiksi** ja **Suoritus**-kentän arvoksi **Jälkeen** **Laatuliitokset**-sivulla, saat seuraavat tulokset:

- Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään **Kyllä**, laatutilaus luodaan jokaisen valmiin määrän ja nimikeotannan asetusten perusteella. Joka kerta, kun määrä ilmoitetaan valmiiksi tuotantotilauksen perusteella, luodaaan uusia laatutilauksia juuri valmiiksi saadun määrän perusteella. Tämä luontilogiikka on yhdenmukainen oston kanssa.
- Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään **Ei**, laatutilaus luodaan valmiiksi saadun määrän perusteella ensimmäisellä kerralla, kun määrä ilmoitetaan valmiiksi. Lisäksi jäljelle jäävän määrän perusteella luodaan nimikeotannan seurantadimensioiden mukaan vähintään yksi laatutilaus. Seuraaville valmiille määrille ei luoda laatutilauksia.

<table>
<tbody>
<tr>
<th>Laatumääritys</th>
<th>Päivitettyä määrää kohden</th>
<th>Seurantadimension mukaan</th>
<th>Tulos</th>
</tr>
<tr>
<td>Prosenttiosuus: 10 %</td>
<td>Kyllä</td>
<td>
<p>Eränumero: Ei</p>
<p>Sarjanumero: Ei</p>
</td>
<td>
<p>Tilausmäärä: 100</p>
<ol>
<li>Ilmoita valmiiksi 30:n osalta
<ul>
<li>Laatutilaus #1 määrälle 3 (10 prosenttia 30:stä)</li>
</ul>
</li>
<li>Ilmoita valmiiksi 70:n osalta
<ul>
<li>Laatutilaus #2 määrälle 7 (10 % jäljellä olevasta tilausmäärästä eli 70:stä)</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Kiinteä määrä: 1</td>
<td>Ei</td>
<td>
<p>Eränumero: Ei</p>
<p>Sarjanumero: Ei</p>
</td>
<td>Tilausmäärä: 100
<ol>
<li>Ilmoita valmiiksi 30:n osalta
<ul>
<li>Laatutilaus #1 määrälle 1 (ensimmäiselle valmiiksi ilmoitetulle määrälle, jolla on kiinteä arvo 1)</li>
<li>Laatutilaus #2 määrälle 1 (jäljelle olevalle määrälle, jolla on edelleen kiinteä arvo 1)</li>
</ul>
</li>
<li>Ilmoita valmiiksi 10:n osalta
<ul>
<li>Laatutilauksia ei luota.</li>
</ul>
</li>
<li>Ilmoita valmiiksi 60:n osalta
<ul>
<li>Laatutilauksia ei luota.</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Kiinteä määrä: 1</td>
<td>Kyllä</td>
<td>
<p>Eränumero: Kyllä</p>
<p>Sarjanumero: Kyllä</p>
</td>
<td>
<p>Tilausmäärä: 10</p>
<ol>
<li>Ilmoita valmiiksi 3:n osalta: 1 erässä #b1, #s1; 1 erässä #b2, #s2; ja 1 erässä #b3, #s3
<ul>
<li>Laatutilaus #1 määrälle 1 erästä #b1, sarjanumero #s1</li>
<li>Laatutilaus #2 määrälle 1 erästä #b2, sarjanumero #s2</li>
<li>Laatutilaus #3 määrälle 1 erästä #b3, sarjanumero #s3</li>
</ul>
</li>
<li>Ilmoita valmiiksi 2:n osalta: 1 erässä #b4, #s4; ja 1 erässä #b5, #s5
<ul>
<li>Laatutilaus #4 määrälle 1 erästä #b4, sarjanumero #s4</li>
<li>Laatutilaus #5 määrälle 1 erästä #b5, sarjanumero #s5</li>
</ul>
</li>
</ol>
<p><strong>Huomautus:</strong> Erää voidaan käyttää uudelleen.</p>
</td>
</tr>
<tr>
<td>Kiinteä määrä: 2</td>
<td>Ei</td>
<td>
<p>Eränumero: Kyllä</p>
<p>Sarjanumero: Kyllä</p>
</td>
<td>
<p>Tilausmäärä: 10</p>
<ol>
<li>Ilmoita valmiiksi 4:n osalta: 1 erässä #b1, #s1; 1 erässä #b2, #s2; 1 erässä #b3, #s3 ja 1 erässä #b4, #s4
<ul>
<li>Laatutilaus #1 määrälle 1 erästä #b1, sarjanumero #s1</li>
<li>Laatutilaus #2 määrälle 1 erästä #b2, sarjanumero #s2</li>
<li>Laatutilaus #3 määrälle 1 erästä #b3, sarjanumero #s3</li>
<li>Laatutilaus #4 määrälle 1 erästä #b4, sarjanumero #s4</li>
</ul>
<ul>
<li>Laatutilaus #5 määrälle 2 ilman viittausta erä- ja sarjanumeroon</li>
</ul>
</li>
<li>Ilmoita valmiiksi 6:n osalta: 1 erässä #b5, #s5; 1 erässä #b6, #s6; 1 erässä #b7, #s7; 1 erässä #b8, #s8; 1 erässä #b9, #s9; ja 1 erässä #b10, #s10
<ul>
<li>Laatutilauksia ei luota.</li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> *Varastoprosessien laadunhallinta* -ominaisuus lisää laatutilausten käsittelytoiminnot tuotannoille, joiden **Tapahtumatyyppi** on *Ilmoita valmiiksi* ja **Suorittamiseksi** on määritetty *Jälkeen*, sekä ostoille, joiden **Tapahtumatyyppi** on määritetty *Rekisteröimiseksi*. Lue lisätietoja kohdasta [Laadunhallinta varastoprosesseja varten](quality-management-for-warehouses-processes.md).

## <a name="quality-management-pages"></a>Laadunhallinnan sivut
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Sivu</th>
<th>kuvaus</th>
<th>Esimerkki</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Laatuliitokset</td>
<td>Katso artikkelin edelliset osat.</td>
<td>Laatuliitos määrittää kaikki seuraavat muodostettavan laatutilauksen tiedot:
<ul>
<li>Tapahtuma</li>
<li>Nimikkeissä suoritettavat testit</li>
<li>Hyväksyttävän laadun taso</li>
<li>Otantasuunnitelma</li>
</ul>
Laatuliitos on määritettävä kutakin sellaista liiketoimintaprosessin muutosta varten, joka edellyttää automaattista laatutilausten luontia. Laatutilaus voidaan esimerkiksi muodostaa ostotilausten, karanteenitilausten, myyntitilausten ja tuotantotilausten liiketoimintaprosesseille.</td>
</tr>
<tr class="even">
<td>Testit</td>
<td>Voit määrittää ja tarkastella tällä sivulla yksittäisiä testejä, joiden mukaan määräytyy, ovatko tuotteet laatuvaatimusten mukaisia. Voit määrittää testiryhmälle vähintään yhden yksittäisen testin. Siinä tapauksessa määrität myös testikohtaiset tiedot, kuten hyväksyttävät mitta-arvot. Mitta-arvoja käytetään määrällisissä testeissä, kun taas laadullisissa testeissä käytetään testimuuttujia.
<ul>
<li>Määrällisen testin testityyppi on <strong>Kokonaisluku</strong> tai <strong>Nimellinen</strong>. Lisäksi siihen on määritetty mittayksikkö. Laatumääritykset ja testitulokset ilmaistaan numeroina.</li>
<li>Laadullisen testin testityyppi on <strong>Vaihtoehto</strong>. Laadullista testiä varten tarvitaan lisätietoja mitattavasta testimuuttujasta ja sen numeroiduista vaihtoehdoista. Laatumääritykset ja testitulokset ilmaistaan tuloksen perusteella.</li>
</ul></td>
<td>Teollisuusyritys suorittaa ostamalleen materiaalille kaksi testiä: materiaalin laatua koskevan määrällisen testin ja pakkausvahinkoja koskevan laadullisen testin. Yritys määrittää laadullisen testin lisätiedoiksi testimuuttujan (vioittunut pakkaus) ja sen mahdolliset tulokset. Yritys määrittää <strong>Testiryhmät</strong>-sivulla kaksi testiä testiryhmään. Lisäksi testikohtaiset tiedot määritetään. Testiryhmä määritetään laatutilaukseen, jotta yritys voi raportoida näiden kahden testin testitulokset.</td>
</tr>
<tr class="odd">
<td>Testiryhmät</td>
<td>Voit määrittää, muokata ja tarkastella tällä sivulla testiryhmiä ja testiryhmälle määritettyjä yksittäisiä testejä. Yläruudussa näkyvät testiryhmät, ja alaruudussa näkyvät valitulle testiryhmälle määritetyt testit. Voit määrittää testiryhmälle useita käytäntöjä, kuten otantasuunnitelman, hyväksytyn laatutason ja tuhoavan testin tarpeen. Kun määrität testiryhmään yksittäisen testin, määrität samalla lisätietoja, kuten järjestyksen, asiakirjat ja voimassaolopäivät. Määrällisessä testissä määritetään myös hyväksyttävät mitta-arvot. Laadullisessa testissä tietoja ovat testimuuttuja ja oletustulos. Laatutilaukseen määritetty testiryhmä määrittää oletustestit, jotka tietylle nimikkeelle on suoritettava. Voit kuitenkin lisätä, muuttaa ja poistaa laatutilauksen testejä. Laatutilauksen jokaisen testin tulokset raportoidaan.</td>
<td>Tuotantoyritys määrittää testiryhmän kutakin laatuvaatimusversiotaan varten. Eri testiryhmät edustavat eroja otantasuunnitelmissa, yhdessä suoritettavissa testeissä, hyväksytyissä mitta-arvoissa ja muissa seikoissa. Määrällisissä testeissä eroja on hyväksyttävissä mitta-arvoissa. Jotta yritys voisi ottaa laatuvaatimuksensa käyttöön, se määrittää kullekin säännölle testiryhmän automaattista laatutilausten luontia varten <strong>Laatuliitokset</strong>-sivulla. Lisäksi se määrittää testiryhmän manuaalisesti luoduille laatutilauksille.</td>
</tr>
<tr class="even">
<td>Nimikkeen laaturyhmät</td>
<td>Voit määrittää, muokata ja tarkastella tällä sivulla nimikkeitä, jotka on määritetty nimikkeelle määritettyihin laaturyhmiin. Laaturyhmän avulla voidaan määrittää nimikkeiden yhteisiä testausvaatimuksia. Kun olet määrittänyt testivaatimukset <strong>Testiryhmät</strong>-sivulla, voit määrittää laatutilausten automaattisen luonnin säännöt. Prosessin yksinkertaistamiseksi sääntöjä ei määritetä yksittäisille nimikkeille. Sen sijaan <strong>Laatuliitokset</strong>-sivulla määritetään laaturyhmän säännöt. Voit myös määrittää valitun laaturyhmän <strong>Nimikkeen laaturyhmät</strong> -sivulla kyseiseen ryhmään liittyvät nimikkeet. Voit myös määrittää valitun nimikkeen <strong>Nimikkeen laaturyhmät</strong> -sivulla kyseiseen nimikkeeseen liittyvät laaturyhmät.</td>
<td>Teollisuusyritys ostaa useita eri raaka-aineita, joilla on samat testausvaatimukset tulevaa tarkistusta varten. Yritys määrittää ensin laaturyhmän ja sitten nimiketunnukset, jotka liittyvät kyseisen ryhmän raaka-aineisiin. Yritys ostaa myöhemmin uutta raaka-ainetta, jolla on samat testausvaatimukset. Yritys ei määritä uudelle raaka-aineelle uusia testausvaatimuksia vaan lisää uuden materiaalin nimiketunnuksen aiemmin luotuun laaturyhmään. Sama teollisuusyritys myös tuottaa nimikkeitä, joilla on samat tuotannon testausvaatimukset, sekä lähettää nimikkeitä, joilla on samat vaatimukset lähetystä edeltävien testien suorittamiseksi. Yritys määrittää ensin kaksi laaturyhmää lisää ja sitten kumpaankin soveltuvat nimiketunnukset.</td>
</tr>
<tr class="odd">
<td>Testimuuttujat</td>
<td>Voit määrittää ja tarkastella tällä sivulla laadulliseen testiin liitettyjä muuttujia. Jokaiselle muuttujalle määritetään numeroitu tulos, joka ilmaisee mahdollisen vaihtoehdon. Testit määritetään <strong>Testit</strong>-sivulla. Laadullisten testien testityypiksi on valittava <strong>Vaihtoehto</strong>. Määritä yksittäisen testin testimuuttuja <strong>Testiryhmät</strong>-sivulla.</td>
<td>Pikkuleipiä valmistava teollisuusyritys tarkastaa lopputuotteen testillä. Tarkastuksessa on useita muuttujia. Ensimmäinen muuttuja on maku, jonka mahdollisia tuloksia ovat hyvä ja paha. Toinen muuttuja on väri, jonka mahdollisia tuloksia ovat liian tumma, liian vaalea ja oikea.</td>
</tr>
<tr class="even">
<td>Testimuuttujien tulokset</td>
<td>Voit määrittää, muokata ja tarkastella tällä sivulla laadulliseen testiin liittyvän testimuuttujan mahdollisia testituloksia. Kunkin tuloksen tilaksi määritetään joko <strong>hyväksytty</strong> tai <strong>hylätty</strong>. Jokaiselle <strong>Testit</strong>-sivulla määritetylle laadulliselle testille on määritettävä muuttuja ja tulokset. (Laadullisten testien tyypiksi on määritetty <strong>Vaihtoehto</strong> <strong>Testit</strong>-sivulla.) Käytä <strong>Testiryhmät</strong>-sivua määrittääksesi yksittäisen laadullisen testin testimuuttujan ja oletustuloksen.</td>
<td>Pikkuleipiä valmistava teollisuusyritys tarkastaa lopputuotteen testillä. Tarkastuksessa on useita muuttujia. Ensimmäinen muuttuja on maku, jonka mahdollisia tuloksia ovat hyvä ja paha. Toinen muuttuja on väri, jonka mahdollisia tuloksia ovat liian tumma, liian vaalea ja oikea. Kunkin tuloksen tilaksi määritetään <strong>hyväksytty</strong> tai <strong>hylätty</strong>. Kunkin muuttujan tarkastuksen aikana tarkastaja raportoi testin tuloksen valitsemalla yhden tuloksista.</td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a>Lisäresurssit
--------

[Laadunhallintaprosessit](quality-management-processes.md)

[Määrityksistä poikkeamisen hallinta](enable-nonconformance-management.md)

[Laadunhallinta varastoprosesseja varten](quality-management-for-warehouses-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]