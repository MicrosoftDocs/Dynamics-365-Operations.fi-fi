---
title: Dynamics AX 7.0:n uudet ja muuttuneet ominaisuudet (helmikuu 2016)
description: Tässä artikkelissa käsitellään Microsoft Dynamics AX 7.0:n uusia tai muuttuneita ominaisuuksia. Tässä versiossa on sekä ympäristö- että sovellusominaisuuksia, ja se julkaistiin helmikuussa 2016.
author: sericks007
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 91243
ms.assetid: 515bc6e7-a85d-4995-95c6-6cab6c8aa0f9
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d81d20045c7b06de01a023d1a34ee653dd696ff1
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711317"
---
# <a name="whats-new-or-changed-in-dynamics-ax-70-february-2016"></a>Dynamics AX 7.0:n uudet ja muuttuneet ominaisuudet (helmikuu 2016)

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics AX 7.0:n uusia tai muuttuneita ominaisuuksia. Tässä versiossa on sekä ympäristö- että sovellusominaisuuksia, ja se julkaistiin helmikuussa 2016.

## <a name="cost-management"></a>Kustannushintojen hallinta

<table>
<thead>
<tr>
<th>Mitä voit tehdä?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miksi tämä on tärkeää?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Saat nopeasti yleiskuvan varastosaldosta, keskeneräisen työn (KET) varastosaldosta sekä mikä on valitun tilikauden saapuva ja lähtevä varasto.</td>
<td>Ei käytettävissä</td>
<td><strong>Kustannuslaskenta</strong>-työtilassa on osa, jossa valitun tilikauden varastoilmoitus tai KET-varastoilmoitus näkyy. Ilmoitus perustuu tietojoukon välimuistiin, joka oletusarvoisesti päivitetään 24 tunnin välein. Tietojoukon välimuisti voidaan määrittää siten, että käyttäjät voivat päivittää sen manuaalisesti reaaliaikaista raportointia varten. <strong>Kustannuslaskenta</strong>-työtilan <strong>Tietojen päivityksen tila</strong> näyttää, milloin välimuisti viimeksi päivitettiin.</td>
<td>Kustannusten vastuuhenkilöt haluavat tietää, suureneeko vai pieneneekö varasto- tai KET-varastosaldoilmoitus ajan mittaan. Luokittelemalla ilmoituksen operatiiviset tapahtumat kustannusten vastuuhenkilö saa yleiskuvan varaston liikkumisesta. Jos varasto tai KET-varasto arvioidaan standardikustannusten mukaan, myös rekisteröity yleinen varianssi on näkyvissä.</td>
</tr>
<tr>
<td>Käytä<strong> Kustannuslaskenta</strong>-moduulia.</td>
<td>Ei käytettävissä</td>
<td>Kustannustenhallinta otetaan käyttöön omana alueena. Kustannuksiin liittyvät määritykset ja näkemykset olivat aiemmin hajallaan inventoinnin- ja varastonhallinnassa, tuotannonhallinnasta ja ostoreskontrassa-</td>
<td>Koska kaikki kustannustenhallintaan liittyvät tehtävät on keskitetty yhteen moduuliin, kustannusten vastuuhenkilöiden on helpompi ylläpitää järjestelmää.</td>
</tr>
<tr>
<td>Varaston ja tuotannon kirjanpitoon liittyvät kirjaustyypit on päivitetty.</td>
<td><strong>InventPosting</strong>-, <strong>Resource</strong>-, <strong>ResourceGroup</strong>- ja <strong>ProductionGroup</strong>-lomakkeiden otsikoita ei ole aina kohdistettu käytettyihin <strong>LedgerPostingType</strong>-otsikkoihin. Otsikoissa käytettyjä termejä ei ole aina helppo ymmärtää.</td>
<td>Otsikot on päivitetty siten, että <strong>InventPosting</strong>-, <strong>Resource</strong>-, <strong>ResourceGroup</strong>- ja <strong>ProductionGroup</strong>-sivujen otsikot vastaavat käytettyjä <strong>LedgerPostingType</strong>-otsikoita. Lisäksi kaikki otsikot on nimetty uudelleen niin, että otsikot vastaavat operatiivisia tapahtumia. Huomaa, että kirjauslogiikkaa ei sinänsä ole muutettu.</td>
<td>Järjestelmän määrittäminen on helpottunut, koska uudet otsikot liittyvät tätä kirjaustyyppiä käyttäviin operatiivisiin tapahtumiin.</td>
</tr>
<tr>
<td>Tuo ostohinta, kustannukset tai myyntihinta Microsoft Excelistä kustannuslaskentaversioon tai vie ne sieltä.</td>
<td>Hintoja ja kustannuksia ei voi tuoda oikein kustannuslaskentaversioon, koska tietomalli edellyttää InventDim-tunnusta.</td>
<td>Tietoyksiköiden käyttöönotto mahdollistaa tuonti- ja vientitoiminnon käytön. Käyttäjät voivat tuoda hintoja tai kustannuksia tällä ominaisuudella kustannuslaskentaversiosta tai viedä niitä siihen.
<ul>
<li>Tuo koko hankintaosastolta saatu ensi vuoden ostohintaluettelo.</li>
<li>Siirrä kustannukset ja vakiomyyntihinnat pääkonttorista vähintään yhteen myyntiyritykseen yhdellä toiminnolla.</li>
</ul></td>
<td>Kustannusten vastuuhenkilöt voivat säästää tällä tavoin merkittävästi järjestelmän ylläpitoon kuluvaa aikaa, etenkin jos heidän on ylläpidettävä seuraavan tilikauden ennalta määritettyjä kustannuksia.</td>
</tr>
<tr>
<td>Saat nopeasti yleiskuvan varastosaldosta ja kustannusobjektin keskimääräisestä yksikkökustannuksesta.</td>
<td>Käyttäjän on avattava käytettävissä olevan varaston lomake ja valittava kustannusobjektia vastaavat varastodimensiot. Käyttäjän onkin tämän vuoksi tiedettävä, mitkä varastodimensiot on merkitty tietyn tuotteen kirjanpitovarastoksi.</td>
<td>Uusi <strong>Kustannusobjekti</strong>-sivu on otettu käyttöön. Tällä sivulla on näkyvissä oletusarvoisesti kaikki tuotteeseen liittyvät kustannusobjektit. Sivulla näkyy nykyinen varastomäärä, arvo ja kustannusobjektin keskimääräinen yksikkökustannus.</td>
<td>Se yksinkertaistaa joitakin toimintoja ja helpottaa kustannusten vastuuhenkilön toimintaa.</td>
</tr>
<tr>
<td>Käytä uutta <strong>Kustannusmerkinnät</strong>-sivua varastonhallinnan aikana.</td>
<td>Rekisteröityjen varastotapahtumien ja liittyvien tilitysten varastonhallinta voi olla monimutkaista, sillä samat tapahtuvat voivat olla fyysisiä tai rahoituksellisia.</td>
<td><strong>Kustannusmerkinnät</strong>-sivu on uusi varastotapahtumien tarkastelutapa.
<ul>
<li>Tapahtumat näytetään aikajärjestyksessä.</li>
<li>Vain kustannuksiin vaikuttavat tapahtumat ovat mukana.</li>
<li>Fyysisiä tai rahoituksellisia kustannuksia ei eroteta.</li>
<li>Fyysisiä tai rahoituksellisia määriä ei eroteta.</li>
<li>Kustannukset lisätään kasvavina.</li>
</ul></td>
<td>Kustannusten vastuuhenkilöt voivatkin säästää merkittävästi aikaa, kun heidän tehtävä varastonhallintatoimia tapahtumatasolla.</td>
</tr>
<tr>
<td>Voit tarkastella uuden <strong>Tuotannon KET-raportti</strong> -valintaruudun avulla tietyn tuotteen kumulatiivisten kustannusten yhteenvetoa.</td>
<td>Ei käytettävissä</td>
<td>KET-raportti sisältää yhteenvedon tietyn tuotantotilauksen KET-saldosta soveltuviin kustannusluokitteluihin ryhmiteltyinä. Kaaviosta näkee aikajärjestyksessä, miten operatiiviset kirjaukset ovat vaikuttaneet KET-saldoon.</td>
<td>Kustannusten vastuuhenkilöt säästävät merkittävästi aikaa, kun heidän on tiedettävä tietyn tuotantotilauksen tämän hetkinen KET-saldo tai kuinka paljon materiaalia tilauksessa on kulutettu.</td>
</tr>
<tr>
<td>Käytä tuotantotilauksissa käyttöönotettua kustannusvertailun näyttötoimintoa. Toiminto helpottaa tuotantotilaukseen liittyvien kustannusten vertailua.</td>
<td>Käyttäjä voi verrata vain arvioituja kustannuksia ja toteutuneita kustannuksia. Vertailun voidaan tehdä alimmalla tasolla.</td>
<td>Kustannusten vastuuhenkilöt voivat vertailla seuraavia tietoja kustannusten vertailutoiminnolla:
<ul>
<li>Aktiivinen kustannus vs. arvioitu kustannus = suunnitteluvarianssi</li>
<li>Arvioitu kustannus vs. toteutunut kustannus = tuotannon varianssi</li>
<li>Suunnitteluvarianssi + tuotannon varianssi = kokonaisvarianssi</li>
</ul>
Tämä toiminto toimii erillään tuotettuun nimikkeeseen määritetyistä kustannuslaskennan menetelmistä. Kaaviossa näkyy oletusarvoisesti kustannusvertailu kustannusryhmän tyypin mukaan. Käyttäjät voivat porautua kaaviossa yksityiskohtaisille tasoille.</td>
<td>Kustannusten vastuuhenkilöt tai tuotantopäälliköt voivat analysoida sen avulla, mistä tuotannon varianssit tulevat ja mikä niitä aiheuttaa.</td>
</tr>
</tbody>
</table>

## <a name="developer"></a>Kehittäjä

| Mitä voit tehdä? | Dynamics AX 2012 | Dynamics AX 7.0 | Miksi tämä on tärkeää? |
|------------------|------------------|-----------------|------------------------|
| Luo monilla laitteilla käytettäviä verkkopohjaisia pilviratkaisuja. | Ei käytettävissä | Dynamics AX:n nykyinen versio perustuu uuteen verkkopohjaiseen asiakkaaseen ja asiakaskehykseen. | Saat käyttöösi seuraavan sukupolven ratkaisut, jotka voit tarjota myös käyttäjille. |
| Kehitä ratkaisuja Microsoft Visual Studion avulla. | Microsoft MorphX on tärkein kehitysympäristö, mutta osa kehitystyöstä tehdään Visual Studiossa. | Visual Studio on vain kehitysympäristö. | Tutut Dynamics AX 2012 -käsitteet ovat tallella, ja ne mukautuvat saumattomasti Visual Studion kehykseen ja paradigmoihin. Sen avulla yhteiskäyttö muiden .NET-kielten ja -projektien kanssa onnistuu tavalliseen tapaan. |
| Muodosta CIL (Common Intermediate Language) -kieli kaikille ominaisuuksille. | X++ käännetään pseudokoodiksi. | Uusi X++-kääntäjä muodostaa CIL-kielen kaikille ominaisuuksille. CIL on sama välikieli, jota muut .NET-pohjaiset kielet käyttävät. | CIL-kielen käyttö nopeuttaa toimintaa, sillä voi viitata tehokkaasti hallittujen dynaamisten linkkikirjastojen (DLL) luokkiin ja sitä voidaan käyttää monissa .NET-apuohjelmien työkaluissa. |
| Upota liiketoimintatietoja koskevia raportteja ja visualisointia Microsoft Dynamics AX -asiakasohjelmaan. | Ei käytettävissä | Luo erittäin intuitiivisia ja mukautuvia visualisointeja. | Saat käyttöösi liiketoimintatietoihin perustuvia yksityiskohtaisia, päätöksentekoa tukevia tietoja. |
| Integroi Microsoft Officen kanssa. | Ei käytettävissä | Uusia ominaisuuksia ovat esimerkiksi Excel Data Connector -sovellus, **Työkirjan suunnittelu** -sivu, ohjelmointirajapinnan vienti ja tiedostonhallinta. | Voit luoda tuottavuusratkaisuja käyttäjille. |
| Automatisoi muodostus, testaus ja käyttöönotto. | Osittain käytettävissä | Ota kehittäjätopologia käyttöön kehittäjän ja muodostuksen virtuaalikoneen avulla. Määritä muodostuksen virtuaalikone havaitsemaan ja muodostamaan moduuleja Visual Studio Onlinesta (VSO) ja suorittamaan testit. C\#- ja X++-moduulikäännöstä ja -viittauksia tuetaan. | Tämä tehostaa kehittäjän toimintaa, sillä testaus ja tarkistukset maksavat vähemmän ja vievät vähemmän aikaa. |
| Mukauta lisäyksillä ja laajennuksilla. | Laajennuksia ei ole käytettävissä. | Dynamics AX:n nykyisessä versiossa on uusi mukautusmalli. | Voit mukauttaa Microsoftin tai Microsoftin ulkopuolisten kumppanien lähettämien mallielementtien lähdekoodia ja metatietoja. |
| Voit luoda uusia ohjausobjekteja ja käyttöliittymäelementtejä X++:n ja modernin verkkokehyksen avulla. | Mukautettujen ohjausobjektien käyttö edellyttää ulkoisia kehyksiä, kuten Microsoft ActiveX:ää ja Windows Presentation Foundationia (WPF). | Ohjausobjektien luontia on helpotettu nykyisessä versiossa. X++-kehystä voidaan käyttää sovelluksen toiminnoissa ja liiketoimintalogiikassa. HTML- ja JavaScript-pohjainen asiakasohjelma puolestaan sallii modernin visualisoinnin. | Ohjausobjektien ulkoasu ja toiminta voidaan suunnitella vastaamaan Dynamics AX:n valmiita ohjausobjekteja. |
| Arvioi suorituskykyä ja säädä sitä uusilla työkaluilla. | PerfSDK, tietojen laajennuksen työkalusarja, jäljityksen jäsentimen verkkosovellus ja PerfTimer ei ole käytettävissä. | PerfSDK, tietojen laajennuksen työkalusarja, jäljityksen jäsentimen verkkosovellus ja PerfTimer ovat uusia ominaisuuksia. | Ohjelmankehityspaketin (SDK) avulla voit testata ja tarkistaa kaikkien keskeisten liiketoimintaprosessien suorituskyvyn suorittamalla yhden ja tarvittaessa monen käyttäjän testin. Tietojen laajennuksen työkalusarjan avulla voit laajentaa oikein kaikki suorituskykytestit, joissa päätietojen ja tapahtumatietojen on oltava oikein laajennettuina. Voit tarkistaa jäljityksen jäsentimellä yhden käyttäjän tai usean käyttäjän suorituskykytestin. PerfTimerin avulla näet, heikentääkö jokin kysely tai tietty menetelmäkutsu suorituskykyä. Niinpä sinun ei tarvitse jäljittää ja analysoida yksityiskohtaisesti. |
| Tuo päivitettävä näkymä näkyviin ODatan avulla. | Ei käytettävissä | Dynamics AX:n nykyinen versio ottaa käyttöön julkisen OData-palvelun päätepisteen, jolla voi käyttää Dynamics AX:n tietoja yhdenmukaisesti monenlaisista asiakasohjelmista. | Ratkaisusi voivat käyttää RESTful-palveluja, jakaa tietoja niin, että ne ovat löydettävissä, ja mahdollistaa laajan integroinnin HTTP-pinoprotokollan avulla. |
| Käytä Business Connectoria liiketoimintalogiikan tuottamiseen ja integraatioskenaarioiden tukemiseen. | Business Connectorin avulla voi kutsua X++-koodia hallitusta koodista. Suosituksena on käyttää Business connectoria vain liiketoimintalogiikan tuottamiseen C\#:ssa mutta ei integraatioskenaarioihin. | Business Connectoria ei enää tueta. Sisällöntuotantovaatimus perustuu siihen, että X++ käännetään hallittuun koodiin. Tämän vuoksi yhteiskäyttö on helpompaa. Integraatioskenaarioissa käytetään ODataa. | Business Connectoria ei voi käyttää jatkossa. |
| Valitse todellisten tietokantakenttien ja laajennettujen tietotyyppien (EDT) asteikko (desimaalien määrä). | Asteikko 16 on oletusasteikko eikä kehittäjä voi muuttaa sitä. | EDT-tyypeissä ja kentissä on nyt asteikko-ominaisuus, jota voidaan käyttöön yksittäisissä kentissä ja EDT-tyypeissä. Oletusasetus on 6 ei 16. | NCCI-taulujen (SQL:n muistissa oleva tuki) suorituskyky on parempi suurissa tilauksissa kuin pientä asteikkoa käytettäessä. Voit vaihtaa asteikkoa yksittäisten kenttien tarpeiden mukaan. |

## <a name="financial-management"></a>Taloushallinto

<table>
<thead>
<tr>
<th>Mitä voit tehdä?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miksi tämä on tärkeää?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Vie tilirakenteet Microsoft Exceliin.</td>
<td>Ei käytettävissä</td>
<td>Voit nyt valita tilirakenteen ja viedä sen Exceliin.</td>
<td>Useat asiakkaat ovat pyytäneet mahdollisuutta viedä tilirakenteet Exceliin, jossa niitä on helpompi suodattaa.</td>
</tr>
<tr>
<td>Voit tarkastella tilirakenteeseen liitettyjä kirjanpitoja ja säännön lisärakenteita yhdellä sivulla.</td>
<td> Käyttäjän on liikuttava useassa lomakkeessa, jos hän haluaa nähdä käytetyn kirjanpidon ja tilirakenteen.</td>
<td>Tilirakennesivulle on lisätty tietoruutuja.</td>
<td>Ne helpottavat tärkeiden tietojen käyttöä tilirakenteita määritettäessä ja muokattaessa.</td>
</tr>
<tr>
<td>Voit tarkastella tilikarttaan liitettyjä kirjanpitoja yhdellä sivulla.</td>
<td>Käyttäjän on siirryttävän kunkin yrityksen kohdalle avaamaan kirjanpitolomake, jos hän haluaa tarkastella kirjanpitoon määritettyä tilikarttaa.</td>
<td><strong>Tilikartta</strong>-sivulle on lisätty tietoruutuja.</td>
<td> Ne helpottavat tärkeiden tietojen käyttöä, kun tilikarttoja määritellään ja määritetään.</td>
</tr>
<tr>
<td>Voit tarkastella tilinpäätöserittelyn oikaisuja ja sulkemistapahtumia eri sarakkeissa <strong>Pääkirja</strong>-luettelosivulla.</td>
<td>Käyttäjä näkee molemmat tapahtumatyypit samassa sarakkeessa.</td>
<td><strong>Pääkirja</strong>-luettelosivulle on lisätty lisäparametri.</td>
<td>Sen ansiosta tiedot voidaan analysoida tiiviimmin. Lisäksi se on edellytys säännösten mukaiselle raportoinnille joissakin mailla ja joillakin alueilla.</td>
</tr>
<tr>
<td>Käytä uutta <strong>Yleiset kirjauskansiot</strong> -sivua.</td>
<td>Ei käytettävissä</td>
<td>Uudella <strong>Yleiset kirjauskansiot</strong> -sivulla kirjataan kirjauskansioita. Tämän sivun oikeudet lisätään <strong>Kirjanpitäjä</strong>-rooli.</td>
<td>Jaetun palvelun kirjanpitäjä voi kirjata kirjauskansioita eri yrityksiin lomakkeesta poistumatta tai yrityskontekstia vaihtamatta.</td>
</tr> 
<tr>
<td>Käytä uutta <strong>Kirjanpitolähteen hallinta </strong>-sivua.</td>
<td>Saatavilla Dynamics AX 2012 R3 CU10:sta alkaen.</td>
<td>Uusi <strong>Kirjanpitolähteen hallinta</strong> -sivu ja toiminnot, joilla voi siirtyä sivulta <strong>Pääkirja</strong>-luettelosivulle ja <strong>Tositetapahtumat</strong>-sivulle.</td>
<td>Mahdollistaa erittäin tarkan näkymän pääkirjan lähteen tai kirjauskansion kirjanpitomerkinnän tietoihin tai ad hoc -analyysin.</td>
</tr>
<tr>
<td>Lisää ylimääräisiä kirjanpitotasoja.</td>
<td>Ylimääräisten kirjanpitotasojen lisääminen oli kehittäjäkokemus.</td>
<td>Käytettävissä on nyt kymmenen kirjanpitotasoa.</td>
<td>Useimmat asiakkaat lisäävät ylimääräisiä kirjanpitotasoja.</td>
</tr>
<tr>
<td>Käytä Liittyvä tosite -vaihtoehtoa.</td>
<td>Ei käytettävissä</td>
<td>Liittyvä tosite -vaihtoehdon käyttäjät voivat tarkastella offset-yrityksen tositetta konsernin sisäisiä tapahtumia kirjattaessa. Käyttävät voivat napsauttaa liittyvissä tositteissa tietoja ja siirtyä nopeasti offset-yrityksen tositteeseen.</td>
<td>Konsernin sisäisiä tapahtumia kirjattaessa käyttäjät eivät näe offset-yrityksessä kirjattua tositetta eivätkä voi jäljittää sitä.</td>
</tr>
<tr>
<td>Tilikauden joukkosulkeminen</td>
<td>Ei käytettävissä</td>
<td>Käyttäjät voivat päivittää moduulin käyttöoikeuden ja muuttaa kauden tilaa samanaikaisesti useissa yrityksissä.</td>
<td>Ennen tätä ominaisuutta käyttäjien oli vaihdettava yritystä, johon he olivat kirjautuneet, siirryttävä kirjanpidon kalenterilomakkeeseen ja päivitettävä moduulin käyttöoikeus ja kauden tila manuaalisesti.</td>
</tr>
<tr>
<td>Oandan tarjoama vaihtokurssipalvelu.</td>
<td>Oandasta tuotavien vaihtokurssien vaihtokurssipalvelun määrittäminen oli kehittäjien idea.</td>
<td>Jos käyttäjillä on Oanda-tunnus, he voivat antaa sen vaihtokurssipalvelua määrittäessään.</td>
<td>Käyttäjät voivat hyödyntää tätä valmista toimintoa, jossa Oandan tarjoama vaihtokurssipalvelu tuodaan aikataulun mukaan.</td>
</tr>
<tr>
<td>Suodata raportteja (Management Reporter) dimensioiden, määritteiden, päivämäärien ja skenaarioiden perusteella.</td>
<td> Management Reporter -raporttien suodatuksessa hyödynnetään raportin rakennetta. Jos esimerkiksi käyttäjä, jolla on tarkasteluoikeudet, haluaa tarkastella eri päivämäärän raporttia, raportin suunnittelijan on tehtävä muutos.</td>
<td>Lisättyjen raporttiasetusten ansiosta käyttäjä voi käyttää erilaisia suodattamia raporttia tarkastellessaan. Uusi raportti muodostetaan sitten kyseisten suodattimien perusteella.</td>
<td>Talousraporttien käyttäjät voivat käyttää erilaisia dimensio-, päivämäärä-, määrite- ja skenaariosuodattimia ilman, että raportin rakennetta on päivitettävä.</td>
</tr>
<tr>
<td>Voit tarkastella raportteja (Management Reporter) Microsoft Dynamics AX -asiakasohjelmassa.</td>
<td>Management Reporterin raporttien näyttämiseen käytettiin erillistä verkkoasiakasohjelmaa.</td>
<td>Kaikkia talousraportteja voidaan käyttää Dynamics AX -asiakasohjelmassa. Käyttäjä valitsee tarkasteltavan raportin ja raportti avautuu asiakasohjelmassa.</td>
<td>Voit nyt tarkastella taloushallinnon raporttia ilman toisen asiakasohjelman tai sovelluksen avaamista.</td>
</tr>
<tr>
<td>Tulosta raportit (Management Reporter) Microsoft Dynamics AX -asiakasohjelmasta.</td>
<td>Raportti tulostamiseen käytetään selaimen tulostusasetuksia ja vain näkyvissä oleva osa tulostetaan.</td>
<td>Käyttäjä voi valita, kuinka tarkasti raportti näytetään ja sivun asetukset käyttämällä Dynamics AX -asiakasohjelman raportin tulostusasetusta.</td>
<td>Raportit tulostuvat käyttäjän odottamalla tavalla verkkosivun tulostamisen sijaan.</td>
</tr><tr>
<td>Voit analysoida taloushallinnon tietoja Power BI:n taloudellisen suorituskyvyn seurannan sisällön avulla.</td>
<td>Ei käytettävissä</td>
<td>Valitse PowerBI.comissa ensin <strong>tietojen hakeminen</strong> ja sitten <strong>Dynamics AX:n taloudellisen suorituskyvyn</strong> sisältöpaketti. Kun kirjoitat Dynamics AX -päätepisteesi URL-osoitteen, tietosi tulevat näkyviin koontinäyttöön.</td>
<td>Organisaatiot voivat ottaa kolmella tai neljällä napsautuksella käyttöön tärkeitä taloushallinnon tietoja sisältävän Power BI:n koontinäytön. Sisältöä voidaan mukauttaa organisaation mukaan.</td>
</tr>
<tr>
<td>Voit seurata tilikauden sulkemisprosesseja.</td>
<td>Ei käytettävissä</td>
<td>Sulkemismalleja ja aikatauluja voidaan luoda tilikauden sulkemismäärityksissä. Voit seurata <strong>Tilikauden sulkeminen</strong> -työtilassa sulkemisaikataulujen etenemistä useissa yrityksissä.</td>
<td>Tämän työtilan ansiosta ei tarvita manuaalisia järjestelmiä sulkemistoimintojen määrittämiseen, ajoittamiseen ja ilmoituksiin. Tämä puolestaan vähentää päivien määrää sulkemiseen.</td>
</tr>
<tr>
<td>Voit seurata budjetin tietoja ja toteutuneita tietoja sekä luoda kirjanpitoennusteita <strong>Kirjanpitobudjetit ja ennusteet</strong> -työtilassa. Voit luoda myös muita kyselylomakkeita.</td>
<td>Ei käytettävissä</td>
<td> Työtilaa voidaan käyttää Dynamics AX:n koontinäytöstä. Työtilassa on linkki monelle uudelle kyselysivulle: <strong>Toteutuneiden ja budjetoitujen tietojen yhteenveto</strong>, <strong>Budjetin hallinnan tilastojen yhteenveto</strong>, <strong>Budjettirekisterimerkinnät</strong> ja <strong>Budjettisuunnitelmat</strong>.</td>
<td>Budjetin tietoja on helppo käyttää uusien kyselysivujen avulla. Työtila yhdistää kaikki budjetin ylläpito- ja seurantatehtävät samaan paikkaan, jota budjetti- tai laskentapäälliköiden on helppo käyttää.</td>
</tr>
<tr>
<td>Voit luoda asetteluja budjettisuunnitelmille ja ennusteille.</td>
<td><strong>Budjettisuunnitelma</strong>-asiakirja näytetään luettelona rivejä, joissa taloushallinnon dimensioyhdistelmien voimaantulopäivämäärät ja summat. Käyttäjän on luotava Excel-malleja ja käytettävä niitä, jos hän haluaa tarkastella budjettisuunnitelman tietoja pivot-taulukossa.</td>
<td>Budjettisuunnitelmien ja ennusteiden käytössä olevien asettelujen määrää ei ole rajoitettu. Voit yhdistää asetteluun valitut taloushallinnon dimensiot, käyttäjän määrittämät sarakkeet ja muut rivimääritteet (kuten kommentit, projektit ja resurssit). Käyttäjät voivat vaihtaa käytössä olevaa budjettisuunnitelma-asiakirjan asettelua käytön aikana. Tietoja voi muokata kaikissa valituissa asetteluissa. Budjettisuunnittelun määrityksiä on yksinkertaistettu poistamalla skenaariorajoitukset, ja asettelun avulla voidaan määrittää, mitä tietoja voidaan tarkastella ja muokata budjettisuunnitelma-asiakirjan kussakin vaiheessa.</td>
<td>Niinpä budjettisuunnitelmia voikin luoda ja muokata joustavasti sekä Excelissä että Dynamics AX -asiakasohjelmassa. Excel-työkirjojen malleja voi luoda budjettisuunnitelman asetteluasetuksilla.</td>
</tr>
<tr>
<td>Tulosta <strong>Toimittajan laskutapahtumat</strong> -raportti käyttämällä <strong>Eritelty eräpäiväluettelo</strong> -raportin tietoja. Mukana on myös tiedot erääntyneistä päivistä.</td>
<td>Tulosta kaksi eri raporttia: <strong>Eritelty eräpäiväluettelo</strong> ja <strong>Toimittajan laskutapahtumat</strong>.</td>
<td>Kahden raportin tiedot on yhdistetty <strong>Toimittajan laskutapahtumat</strong> -raporttiin. <strong>Eritelty eräpäiväluettelo</strong> -raportti on vanhentunut.</td>
<td>Kahta erillistä mutta toisiinsa liittyvää raporttia ei tarvitse enää tulostaa.</td>
</tr>
<tr>
<td>Voit muodostaa raportteja suodaan PDF-muodossa.</td>
<td>Sinun on luotava ensin säännösten mukainen raportti yhdessä muodossa ja viedä se sitten PDF-muotoon.</td>
<td>PDF-muoto on säännösten mukaisten raporttien oletusmuoto.</td>
<td>Se varmistaa, että raportti näyttää samalta tietokoneen näytössä ja paperille tulostettuna.</td>
</tr>
<tr>
<td>Voit tilittää arvonlisäveron eräprosessina.</td>
<td>Ei käytettävissä</td>
<td>Voit määrittää <strong>Arvonlisäveron tilityskausi</strong> -sivulla, että tilitysprosessi suoritetaan erätilassa.</td>
<td>Jos kaudella on runsaasti verotapahtumia, tilitysprosessi voi viedä paljon aikaa, joten se kannattaa suorittaa taustalla eräprosessina.</td>
</tr>
</tbody>
</table>

## <a name="foundation"></a>Säätiö

<table>
<thead>
<tr>
<th>Mitä voit tehdä?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miksi tämä on tärkeää?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Voit käyttää asiakasohjelmaa missä ja milloin tahansa.</td>
<td>AX 2012:n pöytäkoneen asiakasohjelma sisältää kaikki lomakkeet, mutta sitä voidaan käyttää vain Microsoft Windows -tietokoneissa ja se on asennettava. Työpöydän asiakasohjelman kanssa käytetään usein päätepalvelinta, jotta käyttö on mahdollista suuralueverkon (WAN) kautta. Yritysportaalin verkkoasiakasohjelmassa on vähemmän lomakkeita.</td>
<td>Kaksi AX 2012 -asiakasohjelmaa on korvattu yhdellä, standardipohjaisella verkkoasiakasohjelmalla, joka sisältää kaikki työpöytäasiakasohjelman toiminnot mutta jota voi käyttää yhtä joustavasti kuin yritysportaalin asiakasohjelmaa.</td>
<td>Kehitystyötä ei siten tarvitsee jakaa kahteen käyttöliittymäympäristöön. Päätepalvelinta ei tarvita, sillä käytössä on tavalliset verkkoliittymät.</td>
</tr>
<tr>
<td>Uusi tehtävän tallennustoiminto tehostaa toimintaa.</td>
<td>AX 2012:n tehtävän tallennustoimintoa varten oli käytettävä suoraan AOS (Application Object Server) -tietokonetta ja sitä varten tarvittiin laajennetut käyttöoikeudet. Käytössä ei myöskään ollut muokkaustoimintoja.</td>
<td>Uutta tehtävän tallennustoimintoa voi käyttää suoraan verkkoasiakasohjelmasta. Tehtävän tallennustoiminnon käyttöä varten ei tarvita järjestelmänvalvojan oikeuksia. Tallennettuja vaiheita voidaan katsoa live-muodossa tallennusaikana ja käyttöön on otettu uusia muokkaustoimintoja. Tehtävän tallennustoiminto tukee myös liiketoimintaprosessien mallintajan (BPM) skenaarioiden lisäksi muita skenaarioita.</td>
<td>Uuden tehtävän tallennustoiminnon käyttökokemus on sujuva, ja se mahdollistaa uudet Dynamics AX:n ominaisuudet. Osa ominaisuuksista on jo käytettävissä ja lisää on tulossa myöhemmin.</td>
</tr>
<tr>
<td>Työtilat auttavat käyttäjiä ymmärtämään, mitä töitä on tulossa.</td>
<td>Roolikeskukset tarjoavat yleisnäkymän tiedoista, jotka liittyvät käyttäjän työtehtävään yrityksessä tai organisaatiossa.</td>
<td>Työtilat ovat Dynamics AX:n uusi käsite, joka korvaa roolikeskukset ensisijaisina tapoina siirtyä tehtäviin ja tietyille sivuille. Ne sisältävät yhdellä sivulla liiketoimintatehtävän yleiskatsauksen ja auttavat käyttäjiä tiedostamaan nykyisen tilan, tulevan kuormituksen sekä prosessin tai käyttäjän suorituksen. Työtilat ovat hajautetumpia kuin AX 2012:n roolikeskukset, ja käyttäjällä voi olla usean työtilan käyttöoikeus.</td>
<td>Työtilojen on tarkoitus parantaa käyttäjän tuottavuutta. Kehittäjien on luotava työtila jokaiselle tuotteen tukemalle merkittävälle tehtävälle. AX 2012:n vanha roolikeskus korvataan yleensä useilla työtiloilla Dynamics AX:n nykyisessä versiossa.</td>
</tr>
<tr>
<td>Varmista, että lomakkeet sopivat selaimen näyttöön tai laitteen kokoon.</td>
<td>AX 2012:ssa lomakkeen sisältö aseteltiin tiukasti sarakkeisiin ja lomakkeen kokonaispituus tai -leveys määräytyi pääasiassa lomakkeen ohjausobjektien mukaan.</td>
<td>Koska uusin Dynamics AX painottuu verkkokäyttöön, lomakkeen mitat perustuvat nyt selaimen tai laitteen näytön kokoon. Ohjausobjekteja ja asetteluparametreja on muokattu tai lisätty vastaamaan paremmin näytön koon muutoksia.</td>
<td>Lomakkeen sisällön on reagoitava aiempaa paremmin, jotta selaimen tai laitteen käytössä olevaa korkeutta ja leveyttä voidaan käyttää optimaalisesti. Reagoitavuuden voi edellyttää lomakkeen mallinnuksen muuttamista.</td>
</tr>
<tr>
<td>Voit parantaa lomakkeen kehittämiskokemusta malleja käyttämällä.</td>
<td>Lomakemallit ovat lähtökohtia, joilla lomakkeita voi kehittää AX 2012:ssa lomaketyypin perusteella. Lomakkeen tyylin tarkistustoiminto on valinnainen apuohjelma, joka ilmoittaa, miten lomake poikkeaa sitä vastaavasta mallista.</td>
<td>Lomakemallit otettiin käyttöön Dynamics AX:n nykyisessä versiossa. Lomakemalleissa yhdistyvät lomakkeiden mallit ja lomakkeen tyylin tarkistustoiminto, jotka on integroitu tiukasti kehityskokemukseen. Mallit on määritetty lomaketasolla (kuten AX 2012) ja nyt on saatavana lisää alimalleja ryhmä- ja välilehtitasolla.</td>
<td>Malleja noudattavilla lomakkeilla on useita etuja, kuten yhdenmukainen käyttöliittymä, yksinkertaistettu kehityskokemus, helpotettu lomakkeen päivityspolku ja luottamus lomakkeen asettelun reagointiin.</td>
</tr>
</tbody>
</table>

## <a name="help"></a>Ohje

<table>
<thead>
<tr>
<th>Mitä voit tehdä?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miksi tämä on tärkeää?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Pääset käyttämään menettelyyn liittyviä ohjeita (tehtäväohjeita) ja käsitteellisiä ohjeaiheita valitsemalla <strong>Ohje</strong>.</td>
<td>AX 2012:n ohjejärjestelmä vie paikallisella verkkopalvelimella oleviin HTML-ohjeaiheisiin. Asiakkaat ja kumppanit voivat luoda oman ohjeensa.</td>
<td>Nykyisen Dynamics AX:n version ohjejärjestelmä näyttää tehtäväoppaat, joka on tallennettu Microsoft Dynamics Lifecycle Servicesin (LCS) BPM:ään. Ohjejärjestelmä näyttää myös Microsoftin ohjesivuston aiheet. Lisätietoja on <a href="help-overview.md" data-raw-source="[Help system](help-overview.md)">ohjejärjestelmässä</a> ja <a href="new-task-guides-available-february-2016.md" data-raw-source="[New task guides (February 2016)](new-task-guides-available-february-2016.md)">uusissa tehtäväoppaissa (helmikuu 2016)</a>.</td>
<td>Tehtäväoppaissa käsitellään vuorovaikutteisesti tehtävän tai liiketoimintaprosessin eri vaiheet. Voit ladata ja mukauttaa Microsoft toimittamia tehtäväohjeita. Aihe on nopea ja jousta tapa luoda, toimittaa ja päivittää tuotteiden ohjeita. Niinpä saatkin aina käyttöösi uusimmat tekniset tiedot.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Henkilöstöresurssien hallinta

<table>
<thead>
<tr>
<th>Mitä voit tehdä?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miksi tämä on tärkeää?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Voit siirtää osaamisalueet ja todisteet luokan osallistujille kurssin päätyttyä.</td>
<td>Prosessi on manuaalinen.</td>
<td>Kun kurssi on suoritettu, näkyviin tulee uusi vaihtoehto, jolla voidaan päivittää uudet osaamisalueet ja todistukset osallistujien tietoihin.</td>
<td>Se on uusi ja tehokas tapa päivittää työntekijän tietoja.</td>
</tr>
<tr>
<td>Voit tarkistaa työsuhteen nopeasti.</td>
<td>Prosessi on manuaalinen.</td>
<td>Henkilöstöosasto voi tarkistaa työsuhteen nopeasti käyttämällä työtilaa tai työntekijäsivua.</td>
<td>Henkilöstöosaston ei ole enää tarkista tarkistaa useilta sivuilta aloituspäivämäärää, esimiestä, toimessa tehtyjä kuukausia ja kompensaatiotietoja.</td>
</tr>
<tr>
<td>Anna työntekijöille mahdollisuus tarkastella, päivittää ja poistaa järjestelmän tietoja.</td>
<td>Käytössä, mutta näkymä ja päivitysmahdollisuus rajallisia.</td>
<td>Toiminto on otettu käyttöön ja työntekijät ja alihankkijat voivat tarkastella monenlaisia henkilötietoja. Työnkulkua voidaan käyttää myös tietoja luotaessa, päivitettäessä tai poistettaessa.</td>
<td>Työntekijät voivat tällä tavoin hallita omia tietojaan, olipa kyse osoite- tai yhteystietojen päivittämisestä, työhön hakemisesta, kyselylomakkeeseen vastaamisesta tai kuvan päivittämisestä. Kun työnkulku on otettu käyttöön, hyväksyjä voi tarkistaa tiedot tai ne hyväksytään automaattisesti. Tämä valinta perustuu liiketoimintaprosesseihin.</td>
</tr>
<tr>
<td>Esimiehet voivat tarkastella tai muokata työntekijän verotietoja.</td>
<td>Käytössä, mutta näkymä ja päivitysmahdollisuus rajallisia.</td>
<td>Esimiehet voivat määritys- ja suojausasetusten mukaisesti tarkastella tai muokata työntekijän tietoja.</td>
<td>Esimiehet pääsevät siis käyttämään työntekijän tärkeitä tietoja, joten he voivat tehdä parempia resursseja, suorituskykyä ja työntekijän kehittämistä koskevia päätöksiä.</td>
</tr>
<tr>
<td>Hyödynnä esimiehen itsepalvelutoimintoa.</td>
<td>Ei käytettävissä</td>
<td>Esimiehet voivat nyt lähettää uuden työntekijän palkkaus- (työntekijät ja alihankkijat), siirto- ja irtisanomispyynnöt (työsuhteen lopettaminen). Esimiehet voivat myös pyytää uutta toimea, pidentää toimen kestoa tai pyytää toimen muutosta.</td>
<td>Nämä skenaariot olivat aiemmin vain henkilöstöhallinnon käytössä. Näiden skenaarioiden käyttöönotto antaa tehokkaita työkaluja esimiesten käyttöön organisaatiossa. Optimaaliset työnkulut voidaan ottaa käyttöön sopivan tasoista arviointia ja hyväksymistä varten.</td>
</tr>
<tr>
<td>Voit käyttää kompensaatiokäsittelyn tuloksia.</td>
<td>Tuloksia ovat käytössä vain käsittelyhetkellä.</td>
<td>Kompensaatiokäsittelyn tuloksia voi nyt käyttää milloin tahansa prosessin suorittamisen jälkeen.</td>
<td>Tämä on erinomainen tapa tarkistaa prosessi ja prosessin tulokset. Samalla käyttöön saadaan kattava näkymä tiedoista ennen työntekijän tietojen päivittämistä.</td>
</tr>
<tr>
<td>Voit käyttää etukäsittelyn tuloksia.</td>
<td>Tuloksia ovat käytössä vain käsittelyhetkellä.</td>
<td>Etukäsittelyn tuloksia voi nyt käyttää milloin tahansa prosessin suorittamisen jälkeen.</td>
<td>Tällä tavoin saadaan kattava näkymä tiedoista, jotka on päivitetty edun rekisteröinnillä ja muuttuneilla kustannuksilla.</td>
</tr>
<tr>
<td>Voit tarkastella Voimaantulopäivä-aikajanan muutoksia.</td>
<td>Ei käytettävissä</td>
<td>Tätä vertailutyökalua voi käyttää työntekijöiden, toimien ja töiden vertailuun. Sen avulla saadaan kattava näkymä tietueiden välisistä muutoksista.</td>
<td>Sen avulla säästää aikaa, kun haluat tarkastella työntekijä-, toimi- ja työtietueissa ajan mittaan tapahtuneita muutoksia. Voit verrata sen avulla nopeasti tietueen kahta versiota tai kaikkia tietueita ajan mittaan.</td>
</tr>
<tr>
<td>Voit tarkastella työntekijöitä yrityskohtaisesti.</td>
<td>Prosessi tehdään manuaalisesti suodattamalla.</td>
<td>Työntekijä-ja alihankkijaluettelot suodatetaan automaattisesti sen yrityksen perusteella, johon olet kirjautunut.</td>
<td>Saat käyttöösi suodatetun näkymän sen yrityksen palveluksessa olevista työntekijöistä, johon olet kirjautunut. Jos haluat suodattamattoman näkymän kaikista työntekijöistä ja alihankkijoista, työntekijäluettelot ovat edelleen käytettävissä. Dynamics AX:n nykyisessä versiossa, järjestelmä ei vaihda yritystä luettelosta valitun työntekijän perusteella.</td>
</tr>
<tr>
<td>Voit päivittää kurssin osallistujaluettelon.</td>
<td>Ei käytettävissä</td>
<td>Kurssin osallistujia voi poistaa osallistujaluettelosta.</td>
<td>Saat käyttöösi kätevän tavan päivittää vahingossa ilmoittautuneet osallistujat.</td>
</tr>
<tr>
<td>Voit hallita kompensaatiotapahtumia ryhmänä.</td>
<td>Ei käytettävissä</td>
<td>Tämä toiminto tehostaa työntekijöiden kompensaatiomuutosten käsittelyä.</td>
<td>Se on yksinkertainen ja tehokas työntekijätietueiden päivitysprosessi, joka voidaan tehdä kompensaation työtilasta ja siihen liittyviltä sivuilta.</td>
</tr>
</tbody>
</table>

## <a name="inventory-management"></a>Varastonhallinta

Uusia ominaisuuksia ei ole lisätty.

## <a name="localization"></a>Lokalisointi

<table>
<thead>
<tr>
<th>Mitä voit tehdä?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miksi tämä on tärkeää?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Voit määrittää ja muodostaa sähköisiä asiakirjoja, jotka vastaavat eri maiden ja alueiden lakisääteisiä vaatimuksia.</td>
<td>Sähköiset asiakirjat koodataan pysyvästi X++- tai XSLT (Extensible Stylesheet Language Transformation) -muotoon. Muotoon tehtävät muutokset edellyttävät kehitystyötä. Tietojen ja muotoilun käyttöä ei ole eristetty. Muokata muodon kehittäminen edellyttää Microsoft Dynamics AX:n uutta hotfix-korjauspakettia, joka korvaa aiemman muodon. Kunkin muodon mukautetut muutokset on siirrettävä manuaalisesti Microsoft Dynamics AX:n uuden hotfix-korjauspaketin lähdekoodiin.</td>
<td>Sähköinen raportointi (ER) on uusi työkalu, jolla voi määrittää ja muodostaa kehittäjän sijaan yrityskäyttäjälle suunnattuja sähköisiä asiakirjoja. Voit määrittää sähköisellä raportoinnilla asiakirjamuotojen tietolähteeksi tietomallit, jotka ovat toimialakohtaisia ja Microsoft Dynamics AX -tietokannasta riippumattomia. Yrityskäyttäjä voi määrittää muodot näiden toimialakohtaisten tietomallien perusteella (esimerkiksi maksuja, Intrastat-raportteja tai veroilmoituksia varten). Käyttäjä määrittää muodot yksinkertaisilla, Exceliä muistuttavilla visuaalisilla työkaluilla. ER tukee tällä hetkellä teksti-, XML- ja Excel-muotoisten sähköisten asiakirjojen muodostamista. Nämä asiakirjat voidaan muodostaa samanaikaisesti ja pakata zip-tiedostoiksi. Tietomallit ja muodot tukevat versionhallintaa. Muodon versiolla voi olla voimassaolojaksot. Jokainen tietomalli tai muotoversio tallennetaan erilliseen määritykseen ja jaetaan kumppaneille ja asiakkaille LCS:n kautta. Kumppanit ja asiakkaat voivat mukauttaa Microsoftin tietomalleja ja muotoja tai luoda omansa. ER tallentaa kumppanin ja asiakkaan määritysmuutokset Microsoftin määritysten muutoksina, mikä yksinkertaistaa päivittämistä Microsoftin määritysten uusiin versioihin. Kun kumppanit käyttävät LCS:tä, he voivat myös jakaa tietomalli- ja muotomääritykset muiden kumppanien ja asiakkaiden kanssa, jotka voivat mukauttaa ja jakaa niitä. Muutosten mukauttamista ja helppoa päivitystä tuetaan koko mukautusketjussa.</td>
<td>ER yksinkertaistaa sähköisten asiakirjojen luontia, ylläpitoa ja päivitystä siten, että ne vastaavat eri maiden ja alueiden lakisääteisiä vaatimuksia. ER nopeuttaa ja helpottaa sähköisten asiakirjamuotojen luonti- tai muutosprosessia. Kehittäjien sijaan yrityskäyttäjät voivat tehdä nämä muutokset. ER nopeuttaa ja helpottaa tapaa, jolla kumppanit ja asiakkaat voivat päivittää mukautetut muodot Microsoftin tai muiden kumppanien julkaisemien muotojen uusiin versioihin. Sähköisen raportoinnin avulla Microsoftilla ja kumppaneilla on yksi yhteinen tapa jakaa sähköisten asiakirjojen määrityksen (LCS:n avulla) muille kumppaneille ja asiakkaille. Sähköisen raportoinnin ansiosta kumppanien ja asiakkaiden on helpompi mukauttaa, päivittää ja jakaa omien liiketoimintavaatimustensa mukaisia sähköisiä asiakirjamuotoja.</td>
</tr>
<tr>
<td>(MEX) Voit muodostaa Meksikon lainsäädännön edellyttämiä arvonlisävero eli ALV-raportteja.</td>
<td>Sinun on muodostettava <strong>myynnin ja ostojen arvonlisäverojen</strong> raportteja käyttämällä toteutumaton myynnin ALV -toimintoa, jotta käyttäjät voivat tunnistaa tilan perusteella, mitkä tapahtumat ovat toteutuneita ja mitkä toteutumattomia.</td>
<td><strong>Myynnin ja ostojen arvonlisäveron</strong> raportteja muokattiin ja suoritusperusteinen arvonlisävero otetaan niissä huomioon vain käyttämällä tiettyjä tilityskausia toteutumattomien ja toteutuneiden arvolisäverokoodien määrittämiseen.</td>
<td>Arvonlisäverokoodien määrityksiä on muutettava, ennen kuin käyttäjät voivat muodostaa nämä raportit oikein. Suoritusperusteinen arvonlisävero on pakollinen ominaisuus, ja käyttäjän on määritettävä erilliset tilityskaudet, toteutumaton ja toteutunut, jotta vastaavien alueiden tapahtumat voidaan tunnistaa.</td>
</tr>
<tr>
<td>(JPN) Voit hallita japanilaista käyttöomaisuuden nopeutetun poiston ilmoitusasiakirjaa.</td>
<td>Ei käytettävissä</td>
<td>Ilmoituksen tärkeät tiedot tallennetaan keskitetysti yhteen asiakirjaa, mikä parantaa ylläpitoa.</td>
<td>Asiakirjan vaatimustenmukaisuus ja helppo hallinta vähentävät ongelmia tilintarkastusten tai muiden tarkastusten aikana.</td>
</tr>
<tr>
<td>(JPN) Voit tarkistaa pankkitilin JBA-merkit.</td>
<td>Ei käytettävissä</td>
<td>Voit tarkistaa, että kana-nimikentissä on vain merkkejä, joiden käyttö JBA-pankkimuoto hyväksyy.</td>
<td>Tämän vuoksi käyttäjät kokevat vähemmän virheellisistä merkeistä johtuvia keskeytyksiä maksutiedoston muodostamisen aikana.</td>
</tr>
<tr>
<td>(JPN) Käyttöomaisuuden pyöristyseron kerääminen tilikauden lopussa Japanissa.</td>
<td>Ei käytettävissä</td>
<td>Voit valita <strong>Käyttöomaisuusparametrit</strong>-sivulla valitsetko kertymän tilikauden vai tilivuoden lopussa.</td>
<td>Tämä ominaisuuden voidaan valita joustavasti paikallisiin käytäntöihin sopiva menetelmä.</td>
</tr>
<tr>
<td>(JPN) Voit muodostaa Japanin yritysveroilmoituksen liitetaulujen 16-sarjan yhteenvetosumman käyttöomaisuuden päätyypin mukaan.</td>
<td>Ei käytettävissä</td>
<td>Voit valita käyttöomaisuuden arvomallissa yhteenvedon päätyypin mukaan. Tätä toimintoa käytetään oletusarvoisesti juuri luodussa käyttöomaisuudessa.</td>
<td>Koska suuryrityksissä on tuhansia käyttöomaisuuksia, yhteenvetoraportti pienentää merkittävästi muodostettavan raportin kokoa.</td>
</tr>
<tr>
<td>(JPN) Voit aloittaa japanilaisten käyttöomaisuuksien erityispoistovarauksien kohdistaminen seuraavasta tilikaudesta.</td>
<td>Ei käytettävissä</td>
<td>Jos käyttöomaisuuden arvomalleilla on soveltuva lisäpoistoprofiili, voit valita kohdistuksen aloittaminen seuraavasta tilikaudesta tai tilivuodesta.</td>
<td>Tämä ominaisuuden voidaan valita joustavasti paikallisiin käytäntöihin sopiva menetelmä.</td>
</tr>
<tr>
<td>(JPN) Voit muodostaa Japanin kulutusveroraportin, joka sisältää tarkistetut veroprosentit.</td>
<td>Kulutusveroraportti on käytettävissä, kun veroprosentti on 5 prosenttia.</td>
<td>Kulutusveroraportissa on osa korjatulle veroprosentille (joka voi olla esimerkiksi 8 prosenttia).</td>
<td>Hallitus ilmoitti juuri asettelun.</td>
</tr>
<tr>
<td>(EU) Määritä EU-myyntiluettelon pyöristysasetukset.</td>
<td>Eri maiden ja alueiden EU-myyntiluettelon raportoinnin pyöristysasetukset on koodattu X++- tai XSLT (Extensible Stylesheet Language Transformation) -kieleen.</td>
<td>Pyöristysasetukset on lisätty ulkomaankaupan parametreihin. Voit määrittää pyöristystarkkuuden, pyöristysmenetelmän, tulostuksen tarkkuuden ja pyöristystarkkuutta pienempien summien toiminnan.</td>
<td>Tämä yhtenäistää ja yksinkertaistaa EU-myyntiluettelon raportoinnin määrityksiä. Pyöristysasetusten säätäminen ei edellytä kehittäjien toimintoja.</td>
</tr>
<tr>
<td>(EU) Määritä käänteisen verotuksen soveltuvuussäännöt.</td>
<td>Käänteisen verotuksen soveltuvuussäännöt on koodattu kotimaan käänteiseen verotusskenaarioon. Sovellettavuusraja voidaan määritä nimikeryhmittäin. Toiminto on käytössä vain Isossa-Britanniassa.</td>
<td>Voit määrittää käänteisen verotuksen soveltuvuussäännöt asiakirjatyypeittäin (kuten osto- tai myyntitilaus, toimittajan lasku ja vapaatekstilasku) ja käänteisen verotusryhmän, joka yhdistää nimikkeet, nimikeryhmät sekä osto- ja myyntiluokat. Soveltuvuussäännöillä on voimaantulopäivämäärä. Voit myös merkitä yksittäisiä arvonlisäverokoodeja arvonlisäveroryhmissä soveltuviksi käänteiseen verotukseen. Myyntilaskuraportti oikaistaan edustamaan sovellettua käänteistä verovelvollisuutta. Toiminto on käytettävissä kaikissa Euroopan maissa ja kaikilla alueilla.</td>
<td>Tämä muutos yhtenäistää käänteisen verotuksen sovellettavuussääntöjen määritykset ja tukee Euroopan maiden ja alueiden kotimaisten käänteisen verotusääntöjen käyttöönottoa.</td>
</tr>
<tr>
<td>(DE) Luo saksalainen tarkistustiedosto – GDPdUGoBD</td>
<td>Käyttäjät voivat määrittää taulumääritykset, jotka sisältävät vietävät kirjanpitotiedot saksalaisten tilintarkastajien ja viranomaisten hyväksymässä muodossa.</td>
<td>Ominaisuus on toteutettu sähköisen raportoinnin määrityksenä. Toiminto on käytössä Saksassa ja Itävallassa.</td>
<td>Muutoksen ansiosta käyttäjällä on enemmän mahdollisuuksia tietojen muotoiluun ja muuntamiseen. Lisäksi käyttäjä käyttöönsä kaikki sähköisen raportoinnin määritysten elinkaaren hallinnan edut, kuten määritysten kätevä vaihtaminen ja versiointi.</td>
</tr>
<tr>
<td>(FR) Saldoluettelo ryhmän summatileille -raportti.</td>
<td>Saldoluettelo ryhmän summatileille -raportti toteutetaan SSRS-raporttina (LedgerAccountSum_FR).</td>
<td>Saldoluettelo ryhmän summatileille -raportti on toteutettu Management Reporter -raporttina, joka on käytettävissä LCS-kirjaston lokalisoitujen raporttien kansiossa.</td>
<td>Tämän vuoksi käyttäjät saavat käyttöönsä käytettyjen Management Reporter -raporttien mukautusten edut ja valinnanvapauden.</td>
</tr>
<tr>
<td>(EU) Maksuehdotus, osallistumishuomautus ja maksujen seurantaraportit.</td>
<td>Kaikki nämä raportit ja SSRS-raportit toteutetaan.</td>
<td>Nämä raportit on toteutettu Microsoft Excelissä käytettävinä Open XML -malleina.</td>
<td>Sähköisten maksujen määritykset sisältävät maksutiedostomuodon asetukset ja mallit. Tämän vuoksi käyttäjät saavat käyttöönsä sähköisen raportoinnin raporttien mukautusten edut ja valinnanvapauden.</td>
</tr>
<tr>
<td>(EU) Määritä Intrastatin pyöristysasetukset.</td>
<td>Eri maiden ja alueiden Intrastat-raportoinnin pyöristysasetukset on koodattu X++- tai XSLT (Extensible Stylesheet Language Transformation) -kieleen.</td>
<td>Pyöristysasetukset on lisätty ulkomaankaupan parametreihin. Voit määrittää pyöristystarkkuuden, pyöristysmenetelmän, tulostuksen tarkkuuden ja pyöristystarkkuutta pienempien summien toiminnan.</td>
<td>Tämä yhtenäistää ja yksinkertaistaa Intrastat-raportoinnin määrityksiä. Pyöristysasetusten säätäminen ei edellytä kehittäjien toimintoja.</td>
</tr>
<tr>
<td>(EU) Määritä luokkahierarkioiden Intrastat-kauppatavarakoodit.</td>
u<td>Intrastat-kauppatavarakoodit ovat erillinen luettelo. Vaikka kauppatavarakoodille on luokkahierarkiatyyppi, nämä kauppatavarakoodit voitiin palauttaa oletusasetuksiin Retail HQentissä ja myyntiluokissa.</td>
<td>Erillinen Intrastat-kauppatavarakoodien luettelo on yhdistetty tuotehierarkiatyypin kauppatavarakoodiin.</td>
<td>Tämä yhtenäistää kauppatavarakoodien määrittämistavan vapautetuille tuotteille ja luokille myynti- ja ostoasiakirjoissa.</td>
</tr>
<tr>
<td>(EU) Raportoi Intrastat-lisäyksiköiden määrä yksikön muuntoasetuksen avulla.</td>
<td>Intrastat-kauppatavarakoodissa on tekstikenttä lisäyksiköiden tunnistamiseen, ja<strong> Tuote</strong>-kortissa on kenttä lisäyksiköiden tunnistamiseen kilogrammoina.</td>
<td>Intrastat-kauppatavarakoodin lisäyksiköt valitaan yksikköluettelosta. Lisäyksiköiden määrä lasketaan yksikön muuntoasetusten avulla.</td>
<td>Tämä yhtenäistää tapahtumayksiköiden uudelleenlaskentaa lisäyksiköiksi.</td>
</tr>
<tr>
<td>(EU) Määritä toimitustavalle oletuskuljetustapa.</td>
<td>Ei käytettävissä</td>
<td>Oletuskuljetustavan kenttä on lisätty toimitustapaan.</td>
<td>Tämä yksinkertaistaa Intrastat-raportoinnin valmistelua.</td>
</tr>
<tr>
<td>(EU) Merkitse vapautettu tuote ei-Intrastat-raportoitavaksi.</td>
<td>Ei käytettävissä</td>
<td>Vaihtoehto nimikkeen poissulkemiseksi Intrastart-raportoinnista on lisätty vapautettuun tuotteeseen.</td>
<td>Tämä yksinkertaistaa Intrastat-raportoinnin valmistelua.</td>
</tr>
</tbody>
</table>

## <a name="manufacturing"></a>Valmistus

| Mitä voit tehdä? | Dynamics AX 2012 |
|------------------|------------------|
| Voit suorittaa tuotantotilausten materiaalin saatavuustarkistuksen erillisellä sivulla, joka avataan **Tuotannon hallinta** -työtilasta. | Ei käytettävissä |
| Voit käynnistää tuotantotyöt ja raportoidaan niiden edistymisen uudella **Työkorttilaite**-sivulla. | **Työn rekisteröinti**-lomake on tarkoitettu ensisijaisesti suuriin näyttöihin ja käyttöliittymää käytetään yleensä hiirellä. |

## <a name="master-planning-and-forecasting"></a>Pääsuunnittelu ja ennusteet

| Mitä voit tehdä? | Dynamics AX 2012 | Dynamics AX 7.0 | Miksi tämä on tärkeää? |
|------------------|------------------|-----------------|------------------------|
| Voit varoittaa käyttäjää, jos myynti- tai tuotantotilaus ei ole valmis toimitettavaksi ajoitettuun päivään mennessä. | Pääsuunnittelun luomia varoituksia kutsutaan *viivästyssanomiksi*. *Futuuri* on kahden osapuolen välinen sopimus ostaa tai myydä kohde-etuutta sopimushetkellä sovittuun hintaan (*futuurin hinta*), vaikka toimitus ja maksu tapahtuvat tulevaisuudessa (*toimituspäivä*). | *Viivästyssanomien* ja *viivästyspäivien* niminä on nyt *lasketut viiveet* ja *viivästyspäivät*. | AX 2012:n käytetyt termit olivat epätarkkoja ja johtivat virheellisiin käännöksiin. |
| Saat nopeasti tietoja pääsuunnittelun tilasta, kiireellisistä suunnitelluista tilauksista ja suunnitelluista tilauksista, jotka aiheuttavat viivästyksiä. | Tiedot ovat käytettävissä, mutta ne sijaitsevat useissa lomakkeissa. | **Pääsuunnittelu**-työtilaan on kerätty yhteen seuraavat tiedot: viimeksi suoritetun pääsuunnittelun valmistusajankohta, mahdolliset virheet, kiireelliset suunnitellut tilaukset ja viivästyksiä aiheuttavat suunnitellut tilaukset. | Tämä työtilan yhteenveto on hyödyllinen, sillä olennaiset tiedot auttavat ohjaamaan pääsuunnittelua ja tehostamaan toimintaa. |
| Voit päivittää kysynnän ennusteita Excelissä. | Ei käytettävissä | Voit hyödyntää saumatonta Excel-integrointia, kun annat kysynnän ennusteita, teet niihin päivityksiä ja poistat niitä. | Tämä tehostaa toimintaa ja parantaa tuottavuutta. |
| Voit arvioida tulevaa kysyntää ja luoda kysynnän ennusteita aiempien tapahtumatietojen perusteella. | Microsoft Dynamics AX 2012 R3:ssa kysynnän ennusteet luodaan Microsoft SQL Server Analysis Servicen ennustemalleilla. | Voit arvioida tulevan kysynnän hyödyntämällä tehokasta ja laajennettavaa pilvipalvelua, Microsoft Azuren automaattianalyysipalvelua. Automaattianalyysipalvelua on helppo käyttää ja sen ennustemallit on helppo laajentaa asiakkaan tarpeita vastaavaksi. Palvelu valitsee parhaiten sopivan mallin vertailemalla ja antaa suorituskykyilmaisimet (KPI:t) ennusteen tarkkuuden laskemiseen. | Voit luoda entistä tarkempia ennusteita automaattianalyysipalvelun tekniikoilla. |
| Voit käyttää pääsuunnitteluajon liittyvien toimintojen visuaalista yhteenvetoa tilauspäivän ja -määrän optimointiin. | Toimintokaavion yhteenveto on käytettävissä, mutta siinä näkyy kaikki liittyvät toiminnot. Kun toimintoja käytetään, ne häviävät heti näkyvistä. | Toimintokaavio on parempi yhteenveto. Voit valita siinä asetukset, jolla näkyviin saadaan vain käytetyt toiminnot ja suoraan liittyvät toiminnot. Kun toimintoja käytetään, ne jäävät näkyviin himmennettyinä. Näin ollen myös yhteenveto säilyy. Toimintokaavion on lisätty lisätietoja, jotka näyttävät tiedot yhdellä sivulla. | Tämä parantaa tuottavuutta, sillä voit keskittyä vain liittyviin toimintoihin. |

## <a name="procurement-and-sourcing"></a>Hankinta

| Mitä voit tehdä? | Dynamics AX 2012 | Dynamics AX 7.0 | Miksi tämä on tärkeää? |
|------------------|------------------|-----------------|------------------------|
| Saat **Ostotilauksen valmistelu** -työtilassa nopeasti tiedot valmisteltavien ostotilausten tilasta. | Ei tueta | **Ostotilauksen valmistelu** -työtilassa on yhteenveto tilauksista niiden luontihetkestä luonnoksina työnkulun hyväksyntävaiheiden kautta vahvistukseen. | Osto-osaston ei enää tarvitse etsiä tietoja useilta sivuilta, vaan osasto voi käyttää työtilan yhteenvetoa. |
| Saat **Ostotilauksen vastaanotto ja seuranta** -työtilasta nopeasti tietoa vastaanottoa odottavista ostotilauksista, mikä helpottaa seurantaa. | Ei tueta | **Ostotilauksen vastaanotto ja seuranta** -työtilassa on yhteenveto vastaanottoja tai lähetyksiä odottavista vahvistetuista ostotilauksista. Työtilassa on myös luettelo eräpäivän jälkeisistä ja odottavista vastaanotoista, mikä auttaa ennakoimaan toimittajan tarkistusta ja seurantaa. Lisäksi työtilassa on luettelot ostotilauksista, joiden saapuminen varastoon on rekisteröity, mikä auttaa varmistamaan, että vastaanotto kirjataan. Tarkistettavana on myös ostotilauksen palautukset, joita ei ole vielä lähetetty. | Osto-osasto voi hyödyntää työtilan yhteenvetoa. sillä olennaiset tiedot auttavat ohjaamaan seurantaa ja tehostamaan toimintaa. |
| Voit lähettää ostotilaukset vahvistettaviksi Dynamics AX -asiakasohjelman ylläpitämään toimittajaportaalin. Toimittaja voi sitten hyväksyä tai hylätä ostotilaukset. | Ei tueta | Toimittajat voivat vastaanottaa hyväksyttävät tai hylättävät ostotilaukset toimittajaportaalissa. Lisäksi toimittajat näkevät portaalissa yhteenvedon kaikista tilin hyväksytyistä ostotilauksista. Ostoedustaja voi lähettää toimittajalle pyynnön ostotilauksen vahvistuksesta. Toimittajan on oltava Dynamics AX:n Microsoft Azure Active Directory (Azure AD) -käyttäjä ja toimittajan yhteyshenkilö. Hänellä on myös oltava tarkoituksenmukainen käyttöoikeusrooli. | Osto-osaston kannalta etuna on paperitöiden ja ostotilausten vastausten manuaalisen seurannan väheneminen, koska tämä tapahtuu nyt suoraan järjestelmässä. Koska asiakas ja toimittaja käyttävät samaa lähdettä, väärinymmärryksiä on vähemmän. |

## <a name="projects"></a>Projektit

| Mitä voit tehdä? | Dynamics AX 2012 | Dynamics AX 7.0 | Miksi tämä on tärkeää? |
|------------------|------------------|-----------------|------------------------|
| Voit varata työntekijöitä projektin resursseiksi. | Resurssien tavoin myös työntekijöitä voidaan varata suoraan projekteihin. | Valmistus- ja tuotantoresurssit tallennetaan Kuormituskeskus-tauluun, jossa voidaan nyt varata työntekijöitä projektin resursseiksi. | Projekteja varattaessa tarvitsee varata vain resursseja. |

## <a name="retail-sales-marketing-and-customer-service"></a>Vähittäismyynti, markkinointi ja asiakaspalvelu

### <a name="retail-hq"></a>Retail HQ

Microsoft Azuren ylläpitämä Retail HQ:n verkkoasiakasohjelma mahdollistaa kaikenlaisten kaupankäyntitoimintojen keskitetyn hallinnan ja täydellisen näkyvyyden.

<table>
<thead>
<tr>
<th>Mitä voit tehdä?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miksi tämä on tärkeää?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Voit tehdä myynninedistämistoimintoja.</td>
<td>Näiden tietojen hallinta edellyttää useiden lomakkeiden käyttöä:
<ul>
<li>Luokkien hallinta</li>
<li>Tuotehallinta</li>
<li>Kanavan tuotemääritteet</li>
<li>Valikoimat</li>
<li>Luettelon hallinta</li>
<li>Myyntirakenteet</li>
<li>Hinnat &amp; alennukset</li>
</ul></td>
<td><strong>Luokka- ja tuotehallinta</strong> -työtilassa voi tehdä seuraavia toimintoja:
<ul>
<li>Toimintojen hallinta.</li>
<li>Valikoiman elinkaaren seuranta.</li>
<li>Vapautettujen tuotteiden hallinta.</li>
</ul>
<strong>Hintojen ja alennusten hallinnan työtilassa</strong> voi tehdä seuraavia toimintoja:
<ul>
<li>Hinnan ja alennuksen hallinta tietyssä kanavassa ja luokassa.</li>
<li>Luokan hintasäännön hallinta.</li>
<li>Hinta- ja alennusprioriteetit, joilla voidaan määrittää hintaryhmien ja alennusten prioriteetit ohjaamaan niiden käyttöjärjestystä..</li>
<li>Liitoksen ja luetteloalennuksen hallinta.</li>
</ul>
<strong>Luettelon hallinta</strong> -työtilassa voi tehdä seuraavia toimintoja:
<ul>
<li>Aktiivisten luetteloiden yhteenveto.</li>
<li>Luettelon elinkaaren seuranta yhdessä paikassa.</li>
</ul></td>
<td><ul>
<li>Työtilat tehostavat työntekijöiden toimintaa ja tuottavuutta, sillä he voivat hallita keskitetysti myynninedistämisrooliin liittyviä tehtäviä ja toimintoja.</li>
<li>Hinnan ja alennuksen prioriteettitoiminnolla asiakkaat voivat ohjata paremmin hintojen ja alennusten käyttöä. Toiminto mahdollistaa myös uudet skenaariot, joissa korkeammat myymälähinnat ohittavat vakiohinnat.</li>
</ul></td>
</tr>
<tr>
<td>Voit hallita vähittäismyyntikanavan käyttöönottoja ja työvaiheita.</td>
<td>Käyttäjän on avattava useita lomakkeita seuraavia tehtäviä varten:
<ul>
<li>Uusien kanavien ja liittyvien yksiköiden luonti ja määrittäminen.</li>
<li>Myymälän päivittäisten tehtävien hallinta.</li>
<li>Vähittäismyyntitapahtumien käsittely Microsoft Dynamics AX:ssa, vähittäismyynnin laskelmien muodostaminen sekä Microsoft Dynamics AX:n varaston ja myyntitietojen päivittäminen.</li>
</ul>
</td>
<td>Voit suorittaa seuraavat tehtävät <strong>Kanavan käyttöönotto</strong> -työtilassa:
<ul>
<li>Uusien kanavien ja liittyvien yksiköiden luonti.</li>
<li>Vähittäismyymälän määritysten etenemisen seuranta.</li>
<li>Tehtävän valmistumiseen tarvittavien vaiheiden tekeminen tai tietojen antaminen.</li>
<li>Laitteiden tilan seuranta sekä MPOS (Retail Modern POS) -ohjelman tarkistaminen, lataaminen ja asentaminen suoraan myymälöihin.</li>
<li>Kaikkien aiheeseen liittyvien sivujen käyttö.</li>
</ul>Voit suorittaa seuraavat tehtävät 
<strong>Vähittäismyymälän hallinta</strong> -työtilassa:
<ul>
<li>Työntekijöiden ja työntekijöiden myyntipisteen käyttöoikeuksien hallinta.</li>
<li>Tietyn myymälän tai myymäläryhmän tilan seuranta.</li>
<li>MPOS-ohjelman tarkistaminen, lataaminen ja asennus suoraan myymälöihin.</li>
<li>Raporttien tulostaminen ja liittyvien sivujen käyttö.</li>
</ul>Voit suorittaa seuraavat tehtävät 
<strong>Vähittäismyymälän myyntitiedot</strong> -työtilassa:
<ul>
<li>Annetun kanavan laskelmien luonti, laskenta ja kirjaus.</li>
<li>Varaston päivitys erätöitä ajoittamalla sekä laskelmien laskenta ja kirjaus.</li>
<li>Avoimien laskelmien seuranta.</li>
<li>Tietyn myymälän tai myymäläryhmän tilan seuranta.</li>
<li>Raporttien tulostaminen ja kaikkien liittyvien sivujen käyttö nopeasti.</li>
</ul></td>
<td>Työtilat tehostavat työntekijöiden toimintaa ja tuottavuutta, sillä he voivat hallita keskitetysti useimpia kanavan käyttöönottoon, myymälän hallintaan ja myyntitietoihin liittyviä tehtäviä ja toimintoja.</td>
</tr>
<tr>
<td>Voit hallita vähittäismyynnin IT-toimintoja.</td>
<td>Käyttäjän on avattava useita lomakkeita.</td>
<td><strong>Vähittäismyynnin IT</strong> -työtilassa voi tehdä tietyn kanavan Commerce Data Exchange -kyselyjä yhdellä sivulla, joten voit suorittaa seuraavat tehtävät:
<ul>
<li>Latausistunnot</li>
<li>Palvelimeen tehtävät latausistunnot</li>
<li>Epäonnistuneiden istuntojen seuranta sekä niiden käynnistäminen ja suorittaminen uudelleen.</li>
<li>Tulevien töiden tarkastelu tai suorittaminen.</li>
</ul></td>
<td>Työtilat tehostavat työntekijöiden toimintaa ja tuottavuutta, sillä he voivat hallita keskitetysti vähittäismyynnin IT-toimintoihin liittyviä tehtäviä ja toimintoja.</td>
</tr>
<tr>
<td>Voit tuoda ja viedä tietoja tietoyksiköiden avulla.</td>
<td>AX 2012 tulee valmiin Microsoft Dynamics Retail Management System (RMS) -järjestelmän siirtoa tietojen tuonti- ja vientiympäristön kautta.</td>
<td>Vähittäismyynnin tietoyksiköt on laajennettu tukemaan kaikkia vähittäismyyntiin liittyviä pää- ja viitetietoja. Lisäksi tietoyksiköiden tukea koko Dynamics AX -ratkaisussa on parannettu.</td>
<td>Asiakkaat voivat käyttää tietoyksiköitä tuodessaan ja viedessään metatietoperusteisia tietoja. OData-yksiköiden avulla asiakkaat voivat myös integroida Dynamics AX:n kolmannen osapuolen sovellusten kanssa.</td>
</tr>
<tr>
<td>Voit suorittaa älykkäitä analyyseja Microsoft Dynamics AX:n ja myyntipisteen asiakasohjelmien yritystietoraporteista.</td>
<td>Käytettävissä on yli 25 taustaraporttia ja viisi kanavaraporttia.</td>
<td>Käytettävissä on yli 30 taustaraporttia ja 10 kanavaraporttia.</td>
<td>Asiakkaat saavat näistä raporteista lisää yritystietoja, joiden avulla voidaan ennustaa trendejä, paljastaa yksityiskohtaista tietoja ja toimia jatkuvasti mahdollisimman tehokkaasti.</td>
</tr>
<tr>
<td>Voit analysoida vähittäismyyntikanavan myyntitietoja Power BI:n Retail Channel Performance -sisällön avulla.</td>
<td>Ei käytettävissä</td>
<td>Valitse PowerBI.comissa ensin <strong>tietojen hakeminen</strong> ja sitten <strong>Dynamics AX:n Retail Channel Performance</strong> -sisältöpaketti. Kun kirjoitat Dynamics AX -päätepisteesi URL-osoitteen, tietosi tulevat näkyviin koontinäyttöön.</td>
<td>Organisaatiot voivat ottaa kolmella tai neljällä napsautuksella käyttöön tärkeitä taloushallinnon tietoja sisältävän Power BI:n koontinäytön. Sisältöä voidaan mukauttaa organisaation mukaan. Käyttäjät voivat myös upottaa Power BI -koontinäyttöruudut omaan mukautettuun Dynamics AX:n työtilaan, jolloin analyysitiedot ovat käytettävissä yhdellä silmäyksellä.</td>
</tr>
<tr>
<td>Voit määrittää kuluttajan käyttöoikeudet.</td>
<td>Ei käytettävissä</td>
<td>Asiakkaat voivat valita, ovatko myyntipisteen toiminnot kuluttajien käytettävissä. Retail Server käyttää käyttöoikeuksia ohjelmointirajapinnan kutsuissa.</td>
<td>Tämä mahdollistaa kuluttajatasoisten käyttöoikeuksien määrittämisen.</td>
</tr>
<tr>
<td>Voit hallita ja vahvistaa yksikön määrityksiä.</td>
<td>Ei käytettävissä</td>
<td>Määritystenhallinta- ja tarkistustoiminnolla voidaan käyttää seuraavia toimintoja:
<ul>
<li>Määritystietojen joukkolataus</li>
<li>Liiketoimintayksikön tarkistus</li>
</ul></td>
<td>Tämä mahdollistaa määritysten käynnistämisen sekä eri määrityselementtien määritysten tilan ja valmistusasteen tarkistamisen.</td>
</tr>
</tbody>
</table>

### <a name="retail-hardware-station"></a>Retail-laiteasema

| Mitä voit tehdä? | Dynamics AX 2012 | Dynamics AX 7.0 | Miksi tämä on tärkeää? |
|------------------|------------------|-----------------|------------------------|
| Voit mahdollistaa sen, että myyntipistelaitteista voidaan muodostaa yhteys oheislaitteisiin, kuten tulostimiin, kassakoneisiin tai maksulaitteisiin. | MPOS-laitteistoprofiilin avulla määritetään käytettävät laitteet. | Lisätty laiteprofiili tukee erilaisia laitteita eri asemissa. Uusi laiteasemaprofiili tukee kunkin laiteaseman yksilöllistä päätetunnusta, kun sähköisiä rahansiirtotapahtumia käsitellään. Sähköisen rahansiirron tuki on yhdistetty laiteasemaan, mikä vähentää MPOS-ohjelman käyttöä sähköisten rahansiirtomaksujen käsittelyssä. | Tämä mahdollistaa entistä joustavammat toteutustavat. Se myös parantaa tietoturvaa ja vähentää luottokorttitietojen näkyvyyttä. |

### <a name="retail-server-and-data-management"></a>Retail Server ja tietojen hallinta

Retail Serverin ja tietojen hallinnan avulla kuluttajat ja yritykset voivat luoda monikanavaisen ostoskokemuksen verkko-, myymälä- ja puhelinkeskuskanavissa.

<table>
<thead>
<tr>
<th>Mitä voit tehdä?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miksi tämä on tärkeää?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Voit muodostaa yhteyden kanavan liiketoimintatiedot tallentavaan CRT-tietokantaan CRT-palvelujen avulla.</td>
<td>OData V3:n tuki.</td>
<td>OData V4:n tuki.</td>
<td>Tämä auttaa asiakasta pysymään ajan tasalla OData-standardeista. Lisäksi myymälä-, mobiili- ja verkkokanavien myynnin integrointi luo vankan, monikanavaisen kokemuksen.</td>
</tr>
<tr>
<td>Tukee vähittäismyyntipalveluja ylläpidettävänä palvelujoukkona.</td>
<td>Sähköisen kaupankäynnin ohjelmointirajapintaa ei tueta Retail Serverin kautta.</td>
<td>Verkkoskenaarioiden tueksi sähköisen kaupankäynnin ohjelmointirajapinta on nyt saatavana Retail Serverin kautta.</td>
<td>Tällä tavoin käyttöön saadaan ylläpidetyt ja skaalautuvat sähköisen kaupan palvelut, joita voidaan käyttää kolmannen osapuolen myymälöissä.</td>
</tr>
<tr>
<td>Voit siirtää tietoja Microsoft Dynamics AX:n taustatoimintojen ja kanavien välillä Commerce Data Exchangen avulla.</td>
<td>Commerce Data Exchange -järjestelmä siirtää tietoja Microsoft Dynamics AX:n ja jälleenmyyntikanavien, kuten verkkokauppojen tai perinteisten myymälöiden, välillä. Lisätietoja on kohdassa <a href="/dynamicsax-2012/appuser-itpro/commerce-data-exchange">Commerce Data Exchange [AX 2012]</a>.</td>
<td>Vaikka Microsoft Dynamics AX 2012 CU8:n kanssa on toiminnallinen pariteetti, ota seuraavat seikat huomioon:
<ul>
<li>Commerce Data Exchange on uudistettu toimimaan pilviympäristössä.</li>
<li>Asynkroninen palvelu käyttää kanavan tietokantaa tietokannan suoralla käyttöoikeudella.</li>
<li>Commerce Data Exchange: Real-time Service -palvelua ylläpidetään mukautettuna Microsoft Dynamics AX -palveluna.</li>
<li>MPOS hallitsee paikallisten tietokantojen ja Retail Serverin välistä synkronointia.</li>
</ul></td>
<td>Commerce Data Exchange on uudistettu toimimaan pilviympäristössä. Se hallitsee edelleen Microsoft Dynamics AX:n ja jälleenmyyntikanavien, kuten verkkokauppojen tai perinteisten myymälöiden, välistä tiedonsiirtoa.</td>
</tr>
<tr>
<td>Tukee käyttövalmista, osittain integroitua kanavien välistä maksujen käsittelyä maksujen SDK:n avulla.</td>
<td>AX 2012 sisältää seuraavat toiminnot:
<ul>
<li>Kaikkien kanavien tuki: myyntipiste, sähköinen kaupankäynti ja puhelinkeskus.</li>
<li>Tuki, kun kortti on käytössä ja kun kortti ei ole käytössä.</li>
<li>Maksun hyväksymissivu.</li>
<li>LS5300:n ja MX925 malli:n oheislaitetuki mallikoodina Retail SDK:ssa.</li>
</ul></td>
<td>Dynamics AX:n nykyinen versio tukee kaikkia nykyisiä Microsoft Dynamics AX for Retail 2012:n luotto- ja maksukorttitoimintoja sekä neljää uutta parannusta.</td>
<td>Asiakas voi nyt käsitellä maksujen luotto- tai maksukorttitapahtumat.</td>
</tr>
<tr>
<td>Voit aktivoida laitteita Microsoft-tilillä (Microsoft Azure Active Directory (Azure AD)).</td>
<td>Ei käytettävissä</td>
<td>Sisältää seuraavat toiminnot:
<ul>
<li>Azure AD -pohjaisen aktivoinnin laajennettu suojaus pilviympäristössä.</li>
<li>Tunnusten hallinnan laajennettu suojaus.</li>
<li>Aktivoinnin aikaista luotettavuutta, vianmääritystä ja virhesanomia parannettu</li>
<li>Yksinkertaistetut aktivointiin liittyvät IT-hallinnan tehtävät.</li>
<li>Uhkamallin uudistus ja korjatut suojausongelmat.</li>
</ul></td>
<td>Käytössä on seuraavat edut:
<ul>
<li>Suojausta on laajennettu Azure AD:n ja laitetunnuksen avulla (tunnusta käyttävät RS-kutsu, käyttökohtainen sovellustallennus).</li>
<li>MPOS:n luvattoman etäkäytön lopettaminen (laitteen käytön estäminen).</li>
<li>MPOS-laitteiden seuranta PCI-vaatimustenmukaisuutta varten.</li>
<li>Fyysisten laitteiden yhdistäminen liiketoimintayksikköön (rekisteri) laitetunnuksella.</li>
<li>Asetusten alustaminen, jossa MPOS toimii sujuvasti (numerosarjat ja laiteprofiilit) MPOS-ohjelman ensimmäisenä vaiheena.</li>
<li>Laitetietojen raportointi pääkonttorista.</li>
</ul></td>
</tr>
<tr>
<td>Voit hallita monipuolista mediasisältöä, kun sisältöä tuotetaan ja välitetään mediavalikoiman kautta.</td>
<td>Ei käytettävissä</td>
<td><ul>
<li>Kuvien latauksen sekä tarkastelun, hallinnan ja poiston tuki mediavalikoimasta. Kuvat voivat olla ulkoisesti ylläpidettyjä tai Retail-ylläpidettyjä kuvia.</li>
<li>Kuvan latauksen ja avauksen tukeminen yksikkösivuilta (esimerkiksi <strong>Tuotteet</strong> ja <strong>Luettelot</strong>) linkittämällä kuva valikoimasta tai lataamalla se työpöydältä.</li>
<li>Kuvien optimoitu pikkukuvaa varten, mukautettu koko ja alkuperäinen.</li>
<li>Yksiköiden joukkolinkitys käyttämällä joukkoliitännän mallia ja taustatöitä.</li>
<li>Microsoft Excelin integrointi korvaa nimeämiskäytäntöjen ja ennalta määritettyjen polkujen määriteryhmärajoituksen.</li>
<li>Paikallisten kuvien tuki ja kuvien henkilötietosisällön, kuten Retail-ylläpidettyjen työntekijä- ja asiakaskuvien, suojaaminen.</li>
</ul></td>
<td><ul>
<li>Ulkoisesti ylläpidettyihin kuviin liittyvät kipupisteet otetaan huomioon, joten edestakaista toimintaa ei ole ja hallinta tapahtuu yhdessä paikassa.</li>
<li>Ladattujen ja ulkoisesti ylläpidettyjen kuvien tehokas sisällönhallinta mediavalikoiman avulla. Suodatustoiminnot helpottavat kuvien etsimistä.</li>
<li>Ulkoisesti ylläpidettyjen kuvien ja yksiköiden, kuten tuotteiden ja luetteloiden, välille voi luoda helposti joukkoliitoksia.</li>
<li>Retail-ylläpidetyn kuvatallennuksen tuki ja kätevä päivitys Excel-integroinnin ansiosta.</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="rich-clientele-experience"></a>Monipuolinen asiakaskokemus

Retail mahdollistaa kokonaisvaltaiset mobiilikokemuksen missä ja milloin tahansa, millä tahansa laitteella. Tämä toiminto laajentaa ostos- ja myymäläkokemukset kaikkiin kanaviin.

<table>
<thead>
<tr>
<th>Mitä voit tehdä?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miksi tämä on tärkeää?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Voit hakea, selata, etsiä tai tarkistaa tuotteita, lisätä tuotteita ostokoriin, hyväksyä maksun ja siirtyä kassalle käyttämällä intuitiivista, kosketuskäyttöistä, monipuolista ja kokonaisvaltaista MPOS-käyttäjäkokemusta.</td>
<td>AX 2012 mahdollistaa seuraavat toiminnot:
<ul>
<li>Myynnin, palautusten ja mitätöintien suorittaminen.</li>
<li>Asiakastilausten luominen, muokkaaminen ja noutaminen.</li>
<li>Vuoro- ja kassatoimintojen suorittaminen.</li>
<li>Tilausten noutaminen ja vastaanottaminen sekä varaston inventointien suorittaminen.</li>
<li>Myymäläraporttien näyttäminen.</li>
</ul></td>
<td>Toiminnallinen pariteetti AX 2012 MPOS:n kanssa. Siihen kuuluvat seuraavat toiminnot:
<ul>
<li>Asiakashalu kaikissa myymälöissä ja kanavissa.</li>
<li>Mahdollisuus luoda asiakastilauksia Real-time Service -palvelua käyttämättä.</li>
<li>Parantanut laitteen aktivointityönkulku, tila ja virhesanomat.</li>
<li>Laajennettavuuden parannukset, kuten kirjausta edeltävät käynnistimet ja mukautusta parantava tehtävätuki.</li>
</ul></td>
<td>Myyntihenkilöstö voi käsitellä myyntitapahtumia ja asiakastilauksia sekä suorittaa päivittäisiä työtehtäviä ja varaston hallintaa mobiililaitteilla kaikkialla myymälässä.</td>
</tr>
<tr>
<td>Voit käynnistää myyntipisteen verkkosovelluksena pilvimyyntipisteen kautta</td>
<td>Ei käytettävissä</td>
<td>Toiminnallinen pariteetti MPOS:n kanssa. Siihen kuuluvat seuraavat toiminnot:
<ul>
<li>Laitteen aktivointi AAD:llä</li>
<li>Reagoiva asettelu</li>
<li>Edgen, Internet Explorerin ja Chromen tuki.</li>
</ul></td>
<td>Käytössä on verkkosovellusmyyntipiste, jonka on toiminnallisesti yhteensopiva MPOS:n kanssa ja jota voi käyttää eri ympäristössä ja selaimissa ilman käyttöönottokustannuksia.</td>
</tr>
<tr>
<td>Voit integroida sisällönhallintajärjestelmät ja luoda monikanavaisen sähköisen kaupankäyntisivuston.</td>
<td>Microsoft SharePointia ja kolmannen osapuolen Storefront-ympäristöjä tuetaan.</td>
<td>Sisältää kolmannen osapuolen Storefront-ympäristöjä tukevan sähköisen kaupankäyntiympäristön. Ympäristössä on seuraavat ominaisuudet:
<ul>
<li>Monipuolinen kuluttajaohjelmointirajapinta.</li>
<li>Todennuksen integrointi mihin tahansa kolmannen osapuolen OpenID-palveluntarjoajaan.</li>
<li>Maksun integrointi.</li>
</ul></td>
<td>Asiakkaat voivat nyt käyttää joustavasti valitsemaansa sisällönhallintajärjestelmää:</td>
</tr>
<tr>
<td>Voit tavoittaa kohdeasiakkaat postimyyntiluetteloiden avulla ja yksinkertaistaa työvaiheita nopealla tilaustenkäsittelyllä, avustetulla myynnillä ja toteutuksella käyttämällä puhelinkeskusta.</td>
<td><ul>
<li>Puhelinkeskuskanava</li>
<li>Postimyyntiluettelot</li>
<li>Nopea tilaustenkäsittely ja avustettu myynti</li>
<li>Parannettu tilauksen täyttäminen</li>
<li>Asiakaspalvelu</li>
<li>Integroitu hinnoittelu sekä kampanjat ja alennukset</li>
</ul></td>
<td>Käytettävissä toiminnallinen pariteetti AX 2012 Call Center -ratkaisun kanssa; poikkeuksena hinnan ohitukset.</td>
<td>Puhelinkeskukset ovat vähittäismyyntikanava, jossa työntekijät voivat vastaanottaa asiakkaiden tilaukset puhelimitse ja luoda myyntitilaukset.</td>
</tr>
</tbody>
</table>

### <a name="commerce-essentials"></a>Commerce-perustiedot

Vähittäismyyntiin ja kaupankäyntiin keskittyvä määritysvaihtoehto auttaa yksinkertaistamaan vähittäismyynnin käyttöönottoja.

| Mitä voit tehdä? | Dynamics AX 2012 | Dynamics AX 7.0 | Miksi tämä on tärkeää? |
|------------------|------------------|-----------------|------------------------|
| Voit käyttää Commerce-perutustietojen koontinäyttöä. | Käytettävissä on aluesivu, josta on linkit valikkovaihtoehtoihin. | Commerce-perustietojen koontinäytössä on linkit toistuviin tehtäviin, mukaan lukien linkit työtiloihin, Power BI -verkko-ohjausobjektiin, suosikkeihin, viimeksi käytetyille sivuille ja nykyisiin työnimikkeisiin. | Laajennettu koontinäyttö tehostaa työntekijöiden toimintaa. Se on myös joustava lähtökohta kaikille vähittäismyyntitehtäville. |
| Voit käyttää tilimuutoksia tietoyksiköiden avulla. | Tilin muutokset viedään tiedostojärjestelmän kansioon. | Tilin muutokset voidaan käyttää tietoyksiköiden kautta. | Tämä ominaisuuden avulla tietoja voi siirtää joustavammin erillisten järjestelmien välillä. Toimintoa voidaan laajentaa myös OData-sovelluksilla. |
| Voit käyttää pilvipalvelumyyntipistettä ja MPOS:ää. | Vain yrityksen myyntipiste (EPOS) on heti käyttövalmis. | MPOS ja pilvipalvelumyyntipiste korvaavat EPOS-asiakasohjelman. Myös sähköinen kaupankäyntikanavan on lisätty oletuksena Commerce-perustietoihin. | Tämä toiminto tukee aiempaa paremmin kanavan välitöntä käyttöä nopeasti käyttöönotettavissa myyntipisteasiakasohjelmissa. |
| Voit toteuttaa kaksitasoisen arkkitehtuurin ja ylläpitää sitä. | Tietojen tuonti- ja vientiympäristön avulla voit siirtää tietoja AX 2012:n ja kolmannen osapuolen järjestelmien välillä. | Tietoyksiköt on luotu laajentamaan kaksitasoisen arkkitehtuurin tukea. | Tietoyksiköt ja OData-sovellukset muodostavat abstraktiotason, joka helpottaa kaksitasoisten skenaarioiden toteuttamista ja ylläpitämistä. |
| Voit yksinkertaistaa lomakkeita. | Käyttöliittymän yksinkertaistaminen edellyttää mukautettua koodia. | Lomake- tai valikkolaajennukset mahdollistavat standardoidun käyttöliittymän yksinkertaistamisen. | Tämä toiminto nopeuttaa ja yksinkertaistaa tapaa, jolla lomakkeita voi mukauttaa jälleenmyyjän tarpeiden mukaan. |

### <a name="pos-task-recorder"></a>Myyntipistetehtävän tallennus

<table>
<thead>
<tr>
<th>Mitä voit tehdä?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miksi tämä on tärkeää?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Voit luoda ja jakaa Modern POS:n tehtäväoppaita ja asiakirjoja.</td>
<td>Ei käytettävissä</td>
<td>MPOS:n tehtävän tallennus tukee seuraavia ominaisuuksia:
<ul>
<li>MPOS:ssa suoritettavien erilaisten tehtävien tehtävän tallennuksen luonti.</li>
<li>Vaiheet ja näyttökuvat sisältävän asiakirjan luonti ja sen liittäminen liiketoimintamallin solmuun.</li>
</ul></td>
<td>Kumppanit ja riippumattomat ohjelmistotoimittajat voi mukauttaa MPOS:ää ja toimittaa käyttäjille koulutusasiakirjat.</td>
</tr>
</tbody>
</table>

### <a name="extensibility"></a>Laajennettavuus

<table>
<thead>
<tr>
<th>Mitä voit tehdä?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miksi tämä on tärkeää?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Voit tukea laajennettavia ja helposti käyttöönotettavia Retail-komponentteja pääkonttorissa, puhelinkeskuksessa, sähköisessä kaupankäynnissä ja myyntipisteessä.</td>
<td>Komponentteja voi laajentaa Retail SDK:lla. Pakkaus- ja käyttöönottotoimintoja ei tueta.</td>
<td>Hook-laajennustoimintoja on parannettu eri komponenteissa koodin eristämisen ja toimivuuden parantamiseksi. Tämä koskee esimerkiksi seuraavia ominaisuuksia:
<ul>
<li>Työnkulku, tehtävä ja työvaihe.</li>
<li>Käynnistämistä edeltävät ja sen jälkeiset kohdat, joissa työnkulkua on helppo laajentaa.</li>
<li>Sovelluksen ja työvaiheen käynnistimet.</li>
</ul>
Lisäksi käytössä on ympäristö, jossa voit muodostaa ja pakata nämä komponentit MSBuildin avulla ja ottaa sitten mukautuksen käyttöön sujuvasti Microsoft Dynamics Lifecycle Servicesin (LCS-palvelun) kautta.</td>
<td>Jälleenmyyjillä on erityisvaatimuksia, jotka perustuvat vertikaalisiin markkinoihin ja toiminnan maatieteelliseen sijaintiin. Koska käyttöympäristön laajentaminen on helppoa, käyttö helpottuu vertikaalimarkkinoilla ja eri markkina-alueilla. Koska Retail on myös erittäin jaettu arkkitehtuuri, käyttöönoton sujuvuus parantaa huomattavasti tuottavuutta.</td>
</tr>
</tbody>
</table>

### <a name="lifecycle-management"></a>Elinkaaren hallinta

Lifecycle Services (LCS) koostuu palveluista, joilla asiakkaat ja kumppanit voivat hallita järjestelmän elinkaarta rekisteröitymisestä päivittäisiin työvaiheisiin.

<table>
<thead>
<tr>
<th>Mitä voit tehdä?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miksi tämä on tärkeää?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Voit hallita ohjelmaa käyttöönoton pilvipalveluilla.</td>
<td>Ei käytettävissä</td>
<td>Pilvipalveluissa voidaan ottaa käyttöön seuraavat topologiat:
<ul>
<li>Yhden Retail-paketin kokeilutopologia.</li>
<li>Monen paketin suuren käytettävyyden Retail-topologia.</li>
<li>Kehittäjätopologia Retail SDK:n kanssa.</li>
</ul>
Käytössä on parannettu vähän toimia vaativa asiakasohjelmakomponenttiasennus, joka suoritetaan itsepalveluasennuksena:
<ul>
<li>Retail Modern POS.</li>
<li>Retail Hardware Station.</li>
<li>Mukautettujen pakettien lataus- ja jakelutuki itsepalveluasennuksen kautta.</li>
</ul></td>
<td>Käyttöönoton pilvipalvelun edut:
<ul>
<li>Retail HQ -komponenttien merkittävästi yksinkertaistettu käyttöönotto.</li>
<li>Alkuperäinen käyttöönotto julkisessa Microsoft Azure -pilvessä.</li>
<li>Myymäläkomponenttien itsepalveluasennuksen parannukset helpottavat määrityksiä</li>
</ul></td>
</tr>
<tr>
<td>Voit seurata järjestelmän kuntoa sekä selvittää virheet ja ongelmat.</td>
<td>Tämä toiminto edellyttää <a href="https://www.microsoft.com/en-us/download/details.aspx?id=58205">System Center 2012 Management Pack for Microsoft Dynamics AX 2012 R3 CU8 Retailia</a>.</td>
<td>Retail-komponenttien seuranta ja vianmääritys on nyt käytettävissä LCS:n <strong>Operatiivisia tietoja</strong> -koontinäytössä.</td>
<td><strong>Operatiivisia tietoja</strong> -koontinäyttö on pilvipohjainen seurantaportaali, jonka ansiosta SCOM (System Center Operations Manager) -infrastruktuuria ei tarvitse asentaa.</td>
</tr>
<tr>
<td>Voit luoda, määrittää, ladata ja asentaa Retail Hardware Stationin ja laitteet itsepalvelutoiminnolla.</td>
<td>Käyttämällä asennuksen paketointityökalua ja yritysportaalia käyttäjä voi suorittaa kaikkien tietyssä tietokoneessa tarvittavien komponenttien automatisoidun asennuksen ja määrityksen määritetyn topologian mukaisesti.</td>
<td>Koska asennuspaketteja on vain kaksi, toinen MPOS-asiakasohjelmalle ja toinen Retail Hardware Station -komponentille, itsepalvelutoiminto on vähentänyt työmäärää, joka tarvitaan eri tasoilla näiden asiakasohjelmakomponenttien asentamiseen.</td>
<td>Itsepalvelun tarkoituksena on pitää vaatimukset mahdollisimman vähäisinä ja varmistaa, että asennus on käyttäjälle mahdollisimman helppoa.</td>
</tr>
</tbody>
</table>

## <a name="sales"></a>Myynti

<table>
<thead>
<tr>
<th>Mitä voit tehdä?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miksi tämä on tärkeää?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Saat nopeasti yhteenvedon toimitusvaihtoehdoista, kun lupaat tilauksen asiakkaille.</td>
<td>Kun tuotteella on saatavuusrajoituksia ja vähintään yhden asiakkaan tilauksessa olevan tuotteen pyydettyä toimituspäivää ei voida toteuttaa, luvattu tilaustehtävä muuttuu haasteeksi. Etsiessään vaihtoehtoja, joilla voidaan ohittaa saatavuuteen ja lähetysaikaan liittyvät ongelmat siten, että asiakkaan pyytämä päivämäärä voidaan toteuttaa tai että asiakkaalle voidaan tarjota luotettava ja hyväksyttävä toimitusratkaisu, tilauksen käsittelijän on ehkä avattava useita lomakkeita, joissa jokaisessa on vain osa tarvittavista tiedoista. Tarkemmin sanottuna yhdessä lomakkeessa on tiedot eri toimipaikoissa käytettävissä olevasta määrästä ja toisessa konsernin sisäinen käytettävissä oleva määrä. Kolmannessa lomakkeessa käyttäjät voivat laskea ensimmäisen mahdollisen päivä toimipaikka ja variantti kerrallaan, kun taas neljännessä lomakkeessa on toimituksen tilausten tiedot. Käyttäjä ei voikaan olla varma siitä, että hän on ottanut huomioon kaikki soveltuvat vaihtoehdot sen sijaan, että valitsisi välittömästi ratkaisun, joka ei ole paras mahdollinen. Käyttäjät eivät myöskään tunne toimivansa tehokkaasti, sillä luvatun tilauksen työnkulussa tapahtuu useita useiden sivujen avaamisesta ja sulkemisesta sekä tietojen ja vaihtoehtojen yhdistämisestä aiheutuvia keskeytyksiä.</td>
<td>Toimituspäivän laskentaan aiemmin luotuihin algoritmeihin perustuva <strong>Toimitusvaihtoehdot</strong>-sivulla on uusi tilauksen koskevien lupausten käyttökokemus:
<ul>
<li>Olennaiset tiedot kerätään useilta sivuilta yhteen paikkaan.</li>
<li>Valittavissa on valmiita vaihtoehtoisia toimituspaketteja, kuten toimipaikan, varaston, variantin ja kuljetuksen yhdistelmätila, joka perustuu nopeimman toimituksen (ensimmäinen mahdollinen päivämäärä) ehtoon, jonka käyttäjä voi valita.</li>
<li>Käyttäjä voi valita vaihtoehtoja simulointiliittymästä ja siirtää ne myyntitilausriville.</li>
</ul></td>
<td>Yritysten, joiden tavoitteena on erinomainen asiakaspalvelu mutta jotka ovat sitoutuneet varaston optimointistrategiaan, on pystyttävä lupaan tilaukset luotettavasti ja kilpailukykyisesti. Heidän asiakkaittensa liiketoiminta kuitenkin edellyttää, että tuotteet ovat käytettävissä ajoissa. <strong>Toimitusvaihtoehdot</strong>-tehtäväsivu nopeuttaa ja helpottaa tilauksen lupaustehtävää. Lisäksi sen avulla voidaan tunnistaa ja suositella järjestelmällisesti paras mahdollinen vaihtoehtoinen tilauksen toimituspäivä. Ja kaiken tämän voi tehdä yhdessä vuorovaikutteisessa paikassa.</td>
</tr>
</tbody>
</table>

## <a name="service-management"></a>Huoltohallinta

Uusia ominaisuuksia ei ole lisätty.

## <a name="transportation-management"></a>Kuljetustenhallinta

Uusia ominaisuuksia ei ole lisätty.

## <a name="travel-and-expense"></a>Matkalaskut

Uusia ominaisuuksia ei ole lisätty.

## <a name="warehouse-management"></a>Varastonhallinta  

| Mitä voit tehdä? | Dynamics AX 2012 | Dynamics AX 7.0 | Miksi tämä on tärkeää? |
|------------------|------------------|-----------------|------------------------|
| Voit ladata, asentaa ja määrittää varaston mobiililaiteportaalin. | Voit ladata, asentaa ja määrittää portaalin Microsoft Dynamics AX:n asennuksen aikana tavalliseen tapaan. Se on suunniteltu otettavaksi käyttöön ja määritettäväksi itsenäisesti paikan päällä. | Voit ladata erillisen asennusohjelman Varastonhallinta-valikkovaihtoehdon avulla. Se on suunniteltu otettavaksi käyttöön ja määritettäväksi itsenäisesti paikan päällä. | Kun määrität mobiililaitetoiminnon, varaston mobiililaiteportaali on asennettava ja määritettävä paikallisesti, jonka jälkeen on muodostettava yhteys pilvipalveluna käytettävään Dynamics AX:ään. |

## <a name="additional-resources"></a>Lisäresurssit

[Finance and Operationsin aloitussivun uudet ominaisuudet ja muutokset](whats-new-changed.md)

[Uudet tehtäväoppaat (helmikuu 2016)](new-task-guides-available-february-2016.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
