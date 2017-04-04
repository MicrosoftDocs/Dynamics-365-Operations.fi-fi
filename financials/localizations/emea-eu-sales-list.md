---
title: "EU:n arvonlisäveron yhteenvetoilmoitus"
description: "Tässä artikkelissa on tietoja Euroopan unionin (EU) arvonlisäveron yhteenvetoilmoituksesta."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12811
ms.assetid: 89ffb659-b4a1-450a-9485-d56dd72829bb
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 1270c04262f66a38863a1938fa32195bfe0d2bbd
ms.lasthandoff: 03/31/2017


---

# <a name="eu-sales-list-reporting"></a>EU-myyntiluettelon raportointi

Tässä artikkelissa on tietoja Euroopan unionin (EU) arvonlisäveron yhteenvetoilmoituksesta.

<a name="eu-sales-list-reporting"></a>EU:n arvonlisäveron yhteenvetoilmoitus
-----------------------

Toimittajan, joka toimittaa EU:n sisällä tavaroita tai palveluita Euroopan Unionin (EU) sisällä sijaitseville yrityksille, on tehtävä ilmoitus EU-myynnistä (EU myyntiluettelo, ESL). Yleensä ESL on toimitettava veroviranomaisille viimeistään ESL:n kattaman ajanjakson päättymisen jälkeisen kuukauden viimeisenä päivänä. Toimittajan on ilmoitettava ESL:llä arvonlisäverotunnistenumeronsa ja sen on myös ilmoitettava asiakkaittain seuraavat tiedot:

-   EU-asiakkaan tunnistenumero
-   Toiseen jäsenvaltioon myytyjen tavaroiden ja palveluiden kokonaisarvo kyseisen kauden aikana. Toimittajan on myös eroteltavat yleinen tavaroiden toimittaminen kolmikantakaupasta. Kolmikantakauppa koskee tavaroiden suoraa toimittamista toimittajan toimittajalta asiakkaalle, kun molemmat osapuolet on rekisteröity muihin EU:n jäsenvaltioihin.

Käyttämällä ESL:ää kunkin EU-jäsenvaltion veroviranomaiset voivat tarkistaa, onko ALV maksettu kustakin EU-myyntitapahtumasta. Luetteloiden ja ALV-palautusten yhdistelmän avulla EU:n jäsenvaltiot voivat vaihtaa tietoa tavaravirroista EU:n sisällä.

## <a name="overview-of-the-eu-sales-list-reporting-process"></a>Yleiskatsaus EU:n arvonlisäveron yhteenvetoilmoitusprosessiin
Voit suorittaa seuraavat tehtävät EU:n arvonlisäveron yhteenvetoilmoituksen antamisessa:

-   Kerää tietoja EU:n sisäisistä myyntitapahtumista. EU:n sisäinen myyntitapahtuma voi olla myyntilasku, vapaatekstilasku, projektilasku tai toimittajan lasku. Tapahtuma tunnistetaan vastapuolen maan/alueen perusteella. Erilaiset EU:n sisäiset myyntitapahtumat kootaan EU:n arvonlisäveron yhteenvetoilmoitustaulukkoon, missä ne näkyvät yhteneväisessä muodossa. Jokainen tämän taulukon tietue edustaa yksittäistä tapahtumaa ja koostuu vastapuolen ALV-tunnisteesta ja toimitettujen tavaroiden ja palveluiden kokonaisarvosta.
-   (Valinnainen) Esikatsele **EU:n arvonlisäveron yhteenvetoilmoitus**. Voit esikatsella ja tarkastaa **EU:n arvonlisäveron yhteenvetoilmoituksen** annetulle kaudelle Microsoft Excel -työkirjan muodossa.
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
<td>Yrityksen ensisijainen osoitteen on oltava EU-jäsenvaltiossa. - <strong>Oikeushenkilöt</strong> sivu (Valitse <strong>organisaation hallinta</strong>&gt;<strong>organisaatiot</strong>&gt;<strong>oikeussubjektien</strong>), valitse juridisen henkilön. Pikavälilehdellä <strong>Osoitteet,</strong>luo osoite, valitse maa/alue ja muut osoitteen komponentit, ja merkitse osoite merkinnällä <strong>Ensisijainen</strong>. Määritä pikavälilehden <strong>Verorekisteröinti</strong> kentässä <strong>Verorekisterinumero</strong> yrityksesi verorekisterinumero.</td>
</tr>
<tr class="even">
<td><strong>Asetus:</strong> Verovapautuksen tunnisteen parametrit</td>
<td>Y-tunnistetietoparametrit määrittää <strong>maan/alueen parametrit</strong> sivu (Valitse <strong>vero</strong>&gt;<strong>asennus</strong>&gt;<strong>arvonlisäveron</strong>&gt;<strong>maan/alueen parametrit</strong>). Luo sivulla tietue kullekin maalle/alueelle, missä sinulla on vastapuolia ja määritä seuraavat tiedot:
<ul>
<li><strong>Maa/alue</strong> – Valitse maa/alue, johon verovapautuksen tunnistenumero liitetään.</li>
<li><strong>Arvonlisävero</strong> – Syötä valitun maan/alueen verovapautuksen tunnistenumero (ts. verovapautuksen tunnistenumeron etuliite).</li>
<li><strong>Tarkista verovapautuksen tunnistenumero</strong> – Valitse tämä valintaruutu tarkistaaksesi valitun maan/alueen verovapautuksen tunnistenumero.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Asetus: </strong>Verovapausnumerot</td>
<td>Luoda ALV-tunnukset, että vastapuolet <strong>Verovapausnumerot</strong> sivu (Valitse <strong>vero</strong>&gt;<strong>asennus</strong>&gt;<strong>arvonlisäveron</strong>&gt;<strong>Verovapausnumerot</strong>). Luo sivulle kutakin verovapausnumeroa kohti tietue ja määritä seuraavat tiedot:
<ul>
<li><strong>Maa/alue </strong>– Valitse vastapuolesi verorekisteröintimaa/alue.</li>
<li><strong>Verovapausnumero</strong> – Syöt vastapuolesi verovapausnumero.</li>
<li><strong>Yrityksen nimi</strong> – (Valinnainen) Syötä vastapuolen nimi.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Asetus: </strong>Vastapuolen verorekisteröinti</td>
<td>Rekisteröinti verotietoja että vastapuolten joko määrittää <strong>kaikille asiakkaille</strong> sivun (valitsemalla <strong>myynnin ja markkinoinnin</strong>&gt;<strong>asiakkaiden</strong>&gt;<strong>kaikille asiakkaille</strong>asiakastietue ja valitse sitten <strong>asetukset</strong>&gt;<strong>näkymän muuttaminen</strong>&gt;<strong>tiedot-näkymässä</strong>) tai <strong>toimittajien</strong> sivun (Valitse <strong>hankinta</strong>&gt;<strong>toimittajien</strong>&gt;<strong>toimittajien</strong>toimittajatietue ja valitse sitten <strong>asetukset</strong>&gt;<strong>näkymän muuttaminen</strong>&gt;<strong>tiedot-näkymässä</strong>). Valitse verovapausnumero pikavälilehden <strong>Lasku ja toimitus</strong> kentässä <strong>Verovapausnumero</strong>.</td>
</tr>
<tr class="odd">
<td><strong>Asetus: </strong>Arvonlisävero</td>
<td>Verokoodit määrittää sisällytettävät <strong>EU-myyntiluettelo</strong> kertomuksen <strong>arvonlisäverokoodit</strong> sivu (Valitse <strong>vero</strong>&gt;<strong>välilliset verot</strong>&gt;<strong>arvonlisäveron</strong>&gt;<strong>arvonlisäverokoodit</strong>). Tyhjennä pikavälilehdellä <strong>Raportin asetukset</strong> jokaisen raporttiin sisällytettävän arvonlisäverokoodin kohdalla <strong>Poissuljettu </strong>-valintaruutu. Kohteita arvonlisäveron parametrit määritetään <strong>nimikkeen arvonlisäveroryhmät</strong> sivu (Valitse <strong>vero</strong>&gt;<strong>välillisten verojen</strong>&gt;<strong>arvonlisäveron</strong>&gt;<strong>nimikkeen arvonlisäveroryhmät</strong>). Valitse kullekin nimikkeen arvonlisäveroryhmälle arvo <strong>Raportointityyppi</strong>-kentässä. Valitsemasi arvo määrittää ESL-summan sarakkeen, johon rivin summa sisällytetään.
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
<td>ESL raportointi parametrien määrittäminen <strong>Ulkomaankaupan parametrit</strong> sivu (Valitse <strong>vero</strong>&gt;<strong>asennus</strong>&gt;<strong>ulkomaankaupan</strong>&gt;<strong>Ulkomaankaupan parametrit</strong>). Määritä seuraavat parametrit:
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
<li><strong>Maa-/aluetyyppi</strong> – Jos <strong>Maa-/alue</strong>-arvo on se maa tai alue, jossa yrityksesi on rekisteröity, valitse <strong>Kotimaa</strong>. Jos <strong>Maa/alue</strong> -arvo on muu jäsenvaltio kuin maa tai alue, jossa yrityksesi on rekisteröity, valitse <strong>EU</strong>. Jos <strong>Maa/alue</strong>-arvo ei ole EU:n jäsenvaltio, valitse <strong>Kolmas maa/alue</strong>.</li>
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

Tapahtumaa pidetään EU:n sisäisenä myyntitapahtumana, jos tapahtuman toimitusosoite on EU:n jäsenmaassa. Tällaisille maille/alueille tulee olla tietue **Ulkomaankaupan parametrit** -sivun **Maa/alue** -välilehdellä, ja **Maa/alue** -arvo tulee asettaa arvoksi **EU**. EU:n sisäiset myyntitapahtumat merkitään **Luettelokoodi**-kenttään. Tämän kentän avulla voit myös erotella yleiset EU:n sisäiset myyntitapahtumat kolmikantakauppatapahtumista. Voit kerätä tietoja yhteisön sisäisen kaupan tapahtumista **EU-myyntiluettelo** sivun (Valitse **vero**&gt;**ilmoitukset**&gt;**Ulkomaankauppa**&gt;**EU-myyntiluettelo**) avulla **siirtää** funktio. Tämän toiminnon avulla voit sisällyttää tapahtumat, joilla on eri raportointityypin summia (kuten nimikkeitä tai palveluita) tapahtumariveillä määritellyn nimikkeen alv-ryhmän perusteella. Voit myös käyttää muita suodattimia määritelläksesi, mitkä tapahtumat tulee sisällyttää. **Siirrä**-toiminto luo tietueen **EU-myyntiluettelo**-sivulle kutakin sisällytettyä EU:n sisäistä myyntitapahtumaa kohti, ja määrittää vastapuolen tilinumeron, maan/alueen, verovapausnumeron, laskun numeron ja päivämäärän, sekä rivien raportointityyppikohtaisen kokonaismäärän. Se myös kopioi **Luettelokoodi**-arvon tapahtumasta. Voit muuttaa tapahtuman luettelokoodin manuaalisesti **EU-myyntiluettelo**-sivulla. **Siirrä**-toiminto luo tietueita, joissa **Raportoinnin tila** -arvo on asetettu arvoksi **Sisällytetty**. Voit vahvistaa **EU-myyntiluettelo **-sivulle kerätyt tiedot käyttämällä **Vahvista**-toimintoa.

### <a name="generating-the-eu-sales-list-report"></a>EU:n arvonlisäveron yhteenvetoilmoituksen luominen

Voit luoda **EU:n arvonlisäveron yhteenvetoilmoituksen** käyttämällä **Raportointi**-toimintoa **EU-myyntiluettelo **-sivulla. Tämän toiminnon avulla voit valita raportointikauden ja käyttää suodattimia sisällytettävien ESL-tietueiden määrittämiseen. Voit lisäksi määrittää muita maa/aluekohtaisia parametreja. Voit myös halutessasi luoda esikatseluraportin, sähköisen tiedoston tai molemmat. **Raportointi**-toiminto käyttää **Ulkomaankaupan parametrit **-sivulla määriteltyjä raportti- ja tiedostomuotoasetuksia. Yleensä **EU:n arvonlisäveron yhteenvetoilmoitus** koostuu erillisistä riveistä, joilla luetellaan tarvikkeiden vastapuolen maa/aluekohtaiset kokonaismäärät, verovapausnumeron ja raportointityypin (kolmikantakauppatapahtumat sisältyvät tähän). Luotuasi **EU:n arvonlisäveron yhteenvetoilmoituksen** tietylle ajanjaksolle, voit merkitä raportille sisältyvät ESL-tietueet asettamalla **Raportoinnin tila** -arvoksi **Raportoitu**. Aseta tämä tila käyttämällä **Merkitse raportoiduksi **-toimintoa **EU-myyntiluettelo**-sivulla.

### <a name="closing-the-eu-sales-list-reporting-period"></a>EU:n arvonlisäveron yhteenvetoilmoituskauden sulkeminen

Saatettuasi tietyn kauden raportointiprosessin päätökseen (esimerkiksi, kun veroviranomaiset ovat hyväksyneet **EU:n arvonlisäveron yhteenvetoilmoituksen**), voit merkitä raporttiin sisältyneet kauden ESL-tietueet asettamalla **Raportoinnin tila** -arvoksi **Suljettu**. Aseta tämä tila käyttämällä **Merkitse suljetuksi **-toimintoa **EU-myyntiluettelo**-sivulla. Jos palautat kauden sulkemisen, voit merkitä ESL-tietueet asettamalla **Raportoinnin tilan** arvoksi **Sisällytetty**. Nämä tietueet voidaan sitten sisällyttää uudelleen **EU:n arvonlisäveron yhteenvetoilmoituksella**. Aseta tämä tila käyttämällä **Merkitse** **sisällytetyksi **-toimintoa **EU-myyntiluettelo**-sivulla.


