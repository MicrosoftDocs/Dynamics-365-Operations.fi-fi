---
title: EU:n arvonlisäveron yhteenvetoilmoitus
description: Tässä artikkelissa on tietoja Euroopan unionin (EU) arvonlisäveron yhteenvetoilmoituksesta.
author: EvgenyPopovMBS
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EUSalesList
audience: Application User
ms.reviewer: kfend
ms.custom: 12811
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8dfd3fafdfc011973b169516cd4e2d239751e96d
ms.sourcegitcommit: f5b156f2e5ca99ad05b3d6e4a5d118631fd3064e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/14/2022
ms.locfileid: "9012497"
---
# <a name="eu-sales-list-reporting"></a>EU-myyntiluettelon raportointi

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja Euroopan unionin (EU) arvonlisäveron yhteenvetoilmoituksesta.

## <a name="eu-sales-list-reporting"></a>EU:n arvonlisäveron yhteenvetoilmoitus

Toimittajan, joka toimittaa EU:n sisällä tavaroita tai palveluita Euroopan Unionin (EU) sisällä sijaitseville yrityksille, on tehtävä ilmoitus EU-myynnistä (EU myyntiluettelo, ESL). Yleensä ESL on toimitettava veroviranomaisille viimeistään ESL:n kattaman ajanjakson päättymisen jälkeisen kuukauden viimeisenä päivänä. Toimittajan on ilmoitettava ESL:llä arvonlisäverotunnistenumeronsa ja sen on myös ilmoitettava asiakkaittain seuraavat tiedot:

-   EU-asiakkaan tunnistenumero
-   Toiseen jäsenvaltioon myytyjen tavaroiden ja palveluiden kokonaisarvo kyseisen kauden aikana. Toimittajan on myös eroteltavat yleinen tavaroiden toimittaminen kolmikantakaupasta. Kolmikantakauppa koskee tavaroiden suoraa toimittamista toimittajan toimittajalta asiakkaalle, kun molemmat osapuolet on rekisteröity muihin EU:n jäsenvaltioihin.

Käyttämällä ESL:ää kunkin EU-jäsenvaltion veroviranomaiset voivat tarkistaa, onko ALV maksettu kustakin EU-myyntitapahtumasta. Luetteloiden ja ALV-palautusten yhdistelmän avulla EU:n jäsenvaltiot voivat vaihtaa tietoa tavaravirroista EU:n sisällä.

## <a name="overview-of-the-eu-sales-list-reporting-process"></a>Yleiskatsaus EU:n arvonlisäveron yhteenvetoilmoitusprosessiin
Voit suorittaa seuraavat tehtävät EU:n arvonlisäveron yhteenvetoilmoituksen antamisessa:

-   Kerää tietoja EU:n sisäisistä myyntitapahtumista. EU:n sisäinen myyntitapahtuma voi olla myyntilasku, vapaatekstilasku, projektilasku tai toimittajan lasku. Tapahtuma tunnistetaan vastapuolen maan/alueen perusteella. Erilaiset EU:n sisäiset myyntitapahtumat kootaan EU:n arvonlisäveron yhteenvetoilmoitustaulukkoon, missä ne näkyvät yhteneväisessä muodossa. Jokainen tämän taulukon tietue edustaa yksittäistä tapahtumaa ja koostuu vastapuolen ALV-tunnisteesta ja toimitettujen tavaroiden ja palveluiden kokonaisarvosta.
-   (Valinnainen) Esikatsele **EU:n arvonlisäveron yhteenvetoilmoitus**. Voit esikatsella ja tarkastaa **EU:n arvonlisäveron yhteenvetoilmoituksen** annetulle kaudelle Microsoft Excelin työkirjana.
-   Luo **EU:n arvonlisäveron yhteenvetoilmoitus**. **EU:n arvonlisäveron yhteenvetoilmoitus** luodaan tietyssä muodossa olevana sähköisenä tiedostona. Kullakin EU:n jäsenmaalla on oma raporttimuotonsa. Yleensä **EU:n arvonlisäveron yhteenvetoilmoitus** sisältää perustiedot ilmoittavasta osapuolesta sekä toimitettujen tavaroiden ja palveluiden arvot. Tämä tieto ryhmitellään maan ja vastapuolen ALV-tunnisteen perusteella.
-   Sulje EU:n arvonlisäveron yhteenvetoilmoituskausi. Kun **EU:n arvonlisäveron yhteenvetoilmoitus** on luotu ja toimitettu viranomaisille, voit merkitä tietueet ESL-taulukossa merkinnällä **Suljettu**. Näitä tapahtumia ei enää oteta mukaan muihin raportteihin.

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
<td><strong>Määritä:</strong> Oikeushenkilö</td>
<td>Yrityksen ensisijainen osoitteen on oltava EU-jäsenvaltiossa. Sivulla <strong>Oikeushenkilöt</strong> (valitse <strong>Organisaation hallinto</strong> &gt; <strong>Organisaatiot</strong> &gt; <strong>Oikeushenkilö</strong>), valitse oikeushenkilö. Pikavälilehdellä <strong>Osoitteet,</strong>luo osoite, valitse maa/alue ja muut osoitteen komponentit, ja merkitse osoite merkinnällä <strong>Ensisijainen</strong>. Määritä pikavälilehden <strong>Verorekisteröinti</strong> kentässä <strong>Verorekisterinumero</strong> yrityksesi verorekisterinumero.</td>
</tr>
<tr class="even">
<td><strong>Asetus:</strong> Verovapautuksen tunnisteen parametrit</td>
<td>Määritä verovapautuksen tunnistenumeron parametrit <strong>Maan/alueen parametrit</strong> -sivulla (valitse <strong>Vero</strong> &gt; <strong>Asetukset</strong> &gt; <strong>Arvonlisävero</strong> &gt; <strong>Maan/alueen parametrit</strong>). Luo sivulla tietue kullekin maalle/alueelle, missä sinulla on vastapuolia ja määritä seuraavat tiedot:
<ul>
<li><strong>Maa/alue</strong> – Valitse maa/alue, johon verovapautuksen tunnistenumero liitetään.</li>
<li><strong>Arvonlisävero</strong> – Syötä valitun maan/alueen verovapautuksen tunnistenumero (ts. ALV-rekisterinumero tai verovapautuksen tunnistenumeron etuliite).</li>
<li><strong>Tarkista verovapautuksen tunnistenumero</strong> – Valitse tämä valintaruutu tarkistaaksesi valitun maan/alueen verovapautuksen tunnistenumero.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Määritys:</strong> ALV-rekisterinumerot</td>
<td>Luo vastapuolillesi ALV-rekisterinumeroita <strong>Kaikki asiakkaat</strong> -sivulla (siirry kohtaan <strong>Myynti ja markkinointi</strong> &gt; <strong>Asiakkaat</strong> &gt; <strong>Kaikki asiakkaat</strong>, valitse asiakastietue ja valitse sitten <strong>Asiakkaat</strong> &gt; <strong>Rekisteröintitunnukset</strong>) tai <strong>Toimittajat</strong>-sivulla (Siirry kohtaan <strong>Hankinta</strong> &gt; <strong>Toimittajat</strong> &gt; <strong>Toimittajat</strong>, valitse toimittajatietue ja valitse sitten <strong>Toimittajat</strong> &gt; <strong>Rekisteröintitunnukset</strong>). Luo tietue <strong>Yleistä</strong>-välilehden <strong>Rekisteröintitunnus</strong>-pikavälilehdessä ja määritä seuraavat tiedot:
<ul>
<li><strong>Rekisteröinnin tyyppi</strong> – Valitse vastapuolen maalle tai alueelle määritetty <strong>ALV-tunnus</strong>-rekisteröintiluokalle määritetty rekisteröintityyppi.</li>
<li><strong>Rekisteröintinumero</strong> – Anna vastapuolen ALV-rekisteröintinumero.</li>
<li><strong>Voimantulo</strong> – Valitse ALV-rekisterinumeron käyttöjakson alkamispäivä.</li>
</ul>  
Vaihtoehtoisesti voit luoda vastapuolillesi ALV-rekisterinumeron <strong>Verovapausnumerot</strong> -sivulla (siirry kohtaan <strong>Vero</strong> &gt; <strong>Asetukset</strong> &gt; <strong>Arvonlisävero</strong> &gt; <strong>Verovapausnumerot</strong>). Luo sivulle kutakin verovapausnumeroa kohti tietue ja määritä seuraavat tiedot:
<ul>
<li><strong>Maa/alue </strong>– Valitse vastapuolesi verorekisteröintimaa/alue.</li>
<li><strong>Verovapausnumero</strong> – Syöt vastapuolesi verovapausnumero.</li>
<li><strong>Yrityksen nimi</strong> – (Valinnainen) Syötä vastapuolen nimi.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Asetus: </strong>Vastapuolen verorekisteröinti</td>
<td>Määritä vastapuoltesi verorekisteröintitiedot joko <strong>Kaikki asiakkaat</strong> -sivulla (valitse <strong>Myynti ja markkinointi</strong> &gt; <strong>Asiakkaat</strong> &gt; <strong>Kaikki asiakkaat</strong>, valitse asiakkaan tietue ja napsauta sitten <strong>Asetukset</strong> &gt; <strong>Vaihda näyttö</strong> &gt; <strong>Tietonäkymä</strong>), tai valitse tietue <strong>Toimittajat</strong> -sivulla (valitse <strong>Hankinta</strong> &gt; <strong>Toimittajat</strong> &gt; <strong>Toimittajat</strong>, valitse toimittajan tietue ja napsauta sitten <strong>Asetukset</strong> &gt; <strong>Vaihda näyttö</strong> &gt; <strong>Tietonäkymä</strong>). Valitse ALV-rekisterinumero pikavälilehden <strong>Lasku ja toimitus</strong> kentässä <strong>ALV-rekisterinumero</strong>.</td>
</tr>
<tr class="odd">
<td><strong>Asetus: </strong>Arvonlisävero</td>
<td>Määritä verokoodit, jotka sisällytetään <strong>EU:n arvonlisäveron</strong> yhteenvetoilmoitukseen sivulla <strong>Arvonlisäverokoodit</strong> (valitse <strong>Vero</strong> &gt; <strong>Epäsuorat verot</strong> &gt; <strong>Arvonlisävero</strong> &gt; <strong>Arvonlisäverokoodit</strong>). Tyhjennä pikavälilehdellä <strong>Raportin asetukset</strong> jokaisen raporttiin sisällytettävän arvonlisäverokoodin kohdalla <strong>Poissuljettu </strong>-valintaruutu. Määritä arvonlisäverokoodit kohteille <strong>Nimikkeiden arvonlisäveroryhmät</strong> -sivulla (valitse <strong>Vero</strong> &gt; <strong>Epäsuorat verot</strong> &gt; <strong>Arvonlisävero</strong> &gt; <strong>Nimikkeiden arvonlisäveroryhmät</strong>). Valitse kullekin nimikkeen arvonlisäveroryhmälle arvo <strong>Raportointityyppi</strong>-kentässä. Valitsemasi arvo määrittää ESL-summan sarakkeen, johon rivin summa sisällytetään.
<ul>
<li><strong>Tyhjä</strong> – Rivisumma on sisällytetty <strong>Ei määritetty arvo</strong>-sarakkeeseen.</li>
<li><strong>Nimike</strong> – Rivisumma on sisällytetty <strong>Nimikkeen arvo</strong> -sarakkeeseen.</li>
<li><strong>Palvelu</strong> – Rivisumma on sisällytetty <strong>Palveluiden arvo</strong> -sarakkeeseen.</li>
<li><strong>Investointi</strong> – Rivisumma on sisällytetty <strong>Investoinnin arvo</strong> -sarakkeeseen. Tämä sarake koskee vain Belgiaa.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Asetus:</strong> ESL-raportoinnin konfiguraatiot</td>
<td>Tuo tai luo sähköisen raportoinnin konfiguraatiot ESL:lle. Lisätietoja sähköisen raportoinnin konfiguraatioiden luomisesta ja ylläpitämisestä on Sähköinen raportointi -dokumentaatiossa.</td>
</tr>
<tr class="odd">
<td><strong>Asetus: </strong>Yleiset parametrit</td>
<td>Määritä ESL-raportoinnin parametrit <strong>Ulkomaankaupan parametrit</strong> -sivulla (valitse <strong>Vero</strong> &gt; <strong>Asetukset</strong> &gt; <strong>Ulkomaankauppa</strong> &gt; <strong>Ulkomaankaupan parametrit</strong>). Määritä seuraavat parametrit:
<ul>
<li><strong>EU-myyntiluettelo</strong>-välilehti:
<ul>
<li><strong>Raportoi käteisalennus</strong> – Valitse tämä valintaruutu, jos käteisalennus tulisi sisällyttää arvoon, kun tapahtuma sisällytetään ESL:ään.</li>
<li><strong>Ostojen siirto</strong> – Valitse tämä valintaruutu, kun haluat sisällyttää ostot ESL:ään.</li>
<li><strong>Tiedostomuodon yhdistäminen</strong> – Valitse sähköisen raportoinnin muoto, jota käytetään, kun ESL:ää varten luodaan sähköinen tiedosto.</li>
<li><strong>Raporttimuodon yhdistäminen</strong> – Valitse sähköisen raportoinnin muoto, jota käytetään, kun ESL:ää varten luodaan esikatseluraportti.</li>
<li><strong>Pyöristyssäännöt</strong> – Määritä reaaliluku, jota käytetään pyöristyksessä. ESL-summat pyöristetään tämän luvun kerrannaiseen.</li>
<li><strong>Pyöristystapa</strong> – Valitse pyöristystapa, jota käytetään ESL-summia pyöristettäessä (<strong>Normaali</strong>, <strong>Alaspäin</strong>, tai <strong>Pyöristys</strong>).</li>
<li><strong>Käytä minimiarvoa</strong> – Valitse tämä valintaruutu, jos haluat summia, jotka ovat vähemmän kuin <strong>Pyöristyssääntö</strong>-lukuun ylöspäin pyöristettävä <strong>Pyöristyssääntö</strong>-luku.</li>
<li><strong>Desimaalien määrä</strong> – Määritä ESL:n summissa näytettävä desimaalien lukumäärä (sekä sähköisissä tiedostoissa että <strong>ESL-esikatseluraportissa</strong>).</li>
</ul></li>
<li><strong>Maan/alueen parametrit</strong> -välilehti: EU:n jäsenvaltioiden tunnistaminen. Luo sivulle kutakin jäsenvaltiota kohti tietue ja määritä seuraavat tiedot:
<ul>
<li><strong>Maa/alue</strong> – Valitse maa/alue.</li>
<li><strong>Maa-/aluetyyppi</strong> – Jos <strong>Maa-/alue</strong>-arvo on se maa tai alue, jossa yrityksesi on rekisteröity, valitse <strong>Kotimaa</strong>. Jos <strong>Maa/alue</strong> -arvo on muu jäsenvaltio kuin maa tai alue, jossa yrityksesi on rekisteröity, valitse <strong>EU</strong>. Jos <strong>Maa/alue</strong>-arvo ei ole&#39; EU:n jäsenvaltio, valitse <strong>Kolmas maa/alue</strong>.</li>
</ul></li>
<li><strong>Numerosarjat</strong>-välilehti: Rivillä, jolla <strong>Viite</strong>-arvo on <strong>EU-myyntiluettelo</strong>, valitse numerosarjan koodi.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Liittyvät tapahtumat</strong></td>
<td><ul>
<li>Rekisteröi myynti asiakkaalle toisessa EU:n jäsenvaltiossa.</li>
<li>Rekisteröi vapaatekstilasku asiakkaalle toisessa EU:n jäsenvaltiossa.</li>
<li>Rekisteröi projektilasku asiakkaalle toisessa EU:n jäsenvaltiossa.</li>
<li>Rekisteröi lasku toimittajalta asiakkaalle toisessa EU:n jäsenvaltiossa.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="working-with-the-esl"></a>ESL:n käyttäminen
### <a name="collecting-information-about-intra-community-trade-transactions"></a>Tietojen kerääminen EU:n sisäisistä myyntitapahtumista

Seuraavanlaisia tapahtumatyyppejä voidaan pitää EU:n sisäisinä myyntitapahtumina:

-   Myyntilaskut
-   Vapaatekstilaskut
-   Projektin laskut
-   Toimittajan laskut

Tapahtumaa pidetään EU:n sisäisenä myyntitapahtumana, jos tapahtuman toimitusosoite on EU:n jäsenmaassa. Tällaisille maille/alueille tulee olla tietue **Ulkomaankaupan parametrit** -sivun **Maa/alue** -välilehdellä, ja **Maa/alue** -arvo tulee asettaa arvoksi **EU**. EU:n sisäiset myyntitapahtumat merkitään **Luettelokoodi**-kenttään. Tämän kentän avulla voit myös erotella yleiset EU:n sisäiset myyntitapahtumat kolmikantakauppatapahtumista. Voit kerätä tietoja EU:n sisäisistä myyntitapahtumista **EU-myyntiluettelo**-sivulta (valitse **Vero** &gt; **Ilmoitukset** &gt; **Ulkomaankauppa** &gt; **EU-myyntiluettelo**) käyttämällä **Siirrä**-toimintoa. Tämän toiminnon avulla voit sisällyttää tapahtumat, joilla on eri raportointityypin summia (kuten nimikkeitä tai palveluita) tapahtumariveillä määritellyn nimikkeen alv-ryhmän perusteella. Voit myös käyttää muita suodattimia määritelläksesi, mitkä tapahtumat tulee sisällyttää. **Siirrä**-toiminto luo tietueen **EU-myyntiluettelo**-sivulle kutakin sisällytettyä EU:n sisäistä myyntitapahtumaa kohti, ja määrittää vastapuolen tilinumeron, maan/alueen, verovapausnumeron, laskun numeron ja päivämäärän, sekä rivien raportointityyppikohtaisen kokonaismäärän. Se myös kopioi **Luettelokoodi**-arvon tapahtumasta. Voit muuttaa tapahtuman luettelokoodin manuaalisesti **EU-myyntiluettelo**-sivulla. **Siirrä**-toiminto luo tietueita, joissa **Raportoinnin tila** -arvo on asetettu arvoksi **Sisällytetty**. Voit vahvistaa **EU-myyntiluettelo**-sivulle kerätyt tiedot käyttämällä **Vahvista**-toimintoa. Saat yksityiskohtaisia tietoja laskusta (myynnin suuntaa varten) käyttämällä **Yhteensä**-toimintoa.

### <a name="generating-the-eu-sales-list-report"></a>EU:n arvonlisäveron yhteenvetoilmoituksen luominen

Voit luoda **EU:n arvonlisäveron yhteenvetoilmoituksen** käyttämällä **Raportointi**-toimintoa **EU-myyntiluettelo**-sivulla. Tämän toiminnon avulla voit valita raportointikauden ja käyttää suodattimia sisällytettävien ESL-tietueiden määrittämiseen. Voit lisäksi määrittää muita maa/aluekohtaisia parametreja. Voit myös halutessasi luoda esikatseluraportin, sähköisen tiedoston tai molemmat. **Raportointi**-toiminto käyttää **Ulkomaankaupan parametrit**-sivulla määriteltyjä raportti- ja tiedostomuotoasetuksia. Yleensä **EU:n arvonlisäveron yhteenvetoilmoitus** koostuu erillisistä riveistä, joilla luetellaan tarvikkeiden vastapuolen maa/aluekohtaiset kokonaismäärät, verovapausnumeron ja raportointityypin (kolmikantakauppatapahtumat sisältyvät tähän). Luotuasi **EU:n arvonlisäveron yhteenvetoilmoituksen** tietylle ajanjaksolle, voit merkitä raportille sisältyvät ESL-tietueet asettamalla **Raportoinnin tila** -arvoksi **Raportoitu**. Aseta tämä tila käyttämällä **Merkitse raportoiduksi**-toimintoa **EU-myyntiluettelo**-sivulla.

### <a name="closing-the-eu-sales-list-reporting-period"></a>EU:n arvonlisäveron yhteenvetoilmoituskauden sulkeminen

Saatettuasi tietyn kauden raportointiprosessin päätökseen (esimerkiksi, kun veroviranomaiset ovat hyväksyneet **EU:n arvonlisäveron yhteenvetoilmoituksen**), voit merkitä raporttiin sisältyneet kauden ESL-tietueet asettamalla **Raportoinnin tila** -arvoksi **Suljettu**. Aseta tämä tila käyttämällä **Merkitse suljetuksi**-toimintoa **EU-myyntiluettelo**-sivulla. Jos palautat kauden sulkemisen, voit merkitä ESL-tietueet asettamalla **Raportoinnin tilan** arvoksi **Sisällytetty**. Nämä tietueet voidaan sitten sisällyttää uudelleen **EU:n arvonlisäveron yhteenvetoilmoituksella**. Aseta tämä tila käyttämällä **Merkitse** **sisällytetyksi**-toimintoa **EU-myyntiluettelo**-sivulla.

## <a name="list-of-country-specific-topics"></a>Luettelo maakohtaisista aiheista

| Maa tai alue          | Linkitä      |
|------------------|-----------|
| Itävalta          | [Itävallan EU-myyntiluettelo](emea-aut-eu-sales-list.md)| 
| Belgia          |[Belgian EU-myyntiluettelo](emea-bel-eu-sales-list.md)|
| Tšekin tasavalta          |[Tšekin tasavallan EU-myyntiluettelo](emea-cze-eu-sales-list.md)|
| Tanska          |[Tanskan EU-myyntiluettelo](emea-dnk-eu-sales-list.md)|
| Viro          |[Viron EU-myyntiluettelo](emea-est-eu-sales-list.md)|
| Suomi          |[Suomen EU-myyntiluettelo](emea-fin-eu-sales-list.md)|
| Ranska          |[Ranskan EU-myyntiluettelo](emea-fra-eu-sales-list.md)|
| Saksa          |[Saksan EU-myyntiluettelo](emea-deu-eu-sales-list.md)|
| Unkari          |[Unkarin EU-myyntiluettelo](emea-hun-eu-sales-list.md)|
| Latvia          |[Latvian EU-myyntiluettelo](emea-lva-eu-sales-list.md)|
| Liettua          |[Liettuan EU-myyntiluettelo](emea-ltu-eu-sales-list.md)|
| Alankomaat          |[Alankomaiden EU-myyntiluettelo](emea-nl-eu-sales-list.md)|
| Puola          |[Puolan EU-myyntiluettelo](emea-pol-eu-sales-list.md)|
| Espanja          |[Espanjan EU-myyntiluettelo (raportti 349)](emea-esp-sales-list.md)|
| Ruotsi          |[Ruotsin EU-myyntiluettelo](emea-swe-eu-sales-list.md)|
| Yhdistynyt kuningaskunta (Pohjois-Irlanti)          |[Yhdistyneen kuningaskunnan (Pohjois-Irlannin) EU-myyntiluettelo](emea-uk-eu-sales-list.md)|


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
