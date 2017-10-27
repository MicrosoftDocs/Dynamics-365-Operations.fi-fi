---
title: Dynamics 365 for Operations-version 1611 uudet ja muuttuneet ominaisuudet (marraskuu 2016)
description: "Tässä aiheessa käsitellään Microsoft Dynamics 365 for Operations -järjestelmän version 1611 uusia tai muuttuneita ominaisuuksia."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 221294
ms.assetid: 357931ed-f843-4bf5-bc85-0da3de0619ec
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 908f854e5ca50f4298110c08c87fefd9427b5cc9
ms.openlocfilehash: a0cf474aeff991f24fb7b879330065db2063cbe2
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="whats-new-or-changed-in-dynamics-365-for-operations-version-1611-november-2016"></a>Dynamics 365 for Operations-version 1611 uudet ja muuttuneet ominaisuudet (marraskuu 2016)

[!include[banner](../includes/banner.md)]


Tässä aiheessa käsitellään Microsoft Dynamics 365 for Operations -järjestelmän version 1611 uusia tai muuttuneita ominaisuuksia.

<a name="cost-accounting"></a>Kustannuslaskenta
---------------

<table>




<thead>
<tr class="header">
<th>Mitä voit tehdä</th>
<th>Miksi tämä on tärkeää</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kustannustason dimensioiden määrittäminen ja kustannustason dimension jäsenten tuominen.</td>
<td>Kustannustasoja käytetään kustannuslaskennassa kustannusten luokitteluun ja kustannusvirtojen dokumentointiin. Ensisijaiset kustannustasot tuodaan joko Microsoft Dynamics 365 for Operations -tietoyhdistimellä, jolla päätilit saadaan suoraan Operations-alustasta, tai käyttämällä yleistä tietoyhdistintä, jossa päätilit saadaan Microsoft Excelin kautta muuntyyppisistä lähdejärjestelmistä. Kun päätilit on tuotu kustannuslaskentaan, niitä käytetään kustannustason dimension jäseninä. Toissijaiset kustannustasot ovat käyttäjäkohtaisia ja niitä käytetään kohdistuksissa dokumentoimaan kustannusvirtoja.</td>
</tr>
<tr class="even">
<td>Kustannustason dimensioiden määrittäminen</td>
<td>Jos päätilejä ei voida jakaa konsernin yritysten välillä lakisääteisten kirjanpidon vaatimusten vuoksi, voit määrittää ne kustannuslaskentaan tuonnin jälkeen saadaksesi kokonaisvaltaisen näkymän koko organisaatioon.</td>
</tr>
<tr class="odd">
<td>Kustannusobjektin dimensioiden määrittäminen ja kustannusobjektin dimension jäsenten tuominen</td>
<td>Kustannusobjektit ovat mitä tahansa objektityyppejä, joille määritetään kustannuksia. Tyypillisiä kustannusobjekteja ovat tuotteet, projektit, resurssit, osastot, kustannuspaikat ja maantieteelliset alueet. Voit käyttää Microsoft Dynamics 365 for Operations -tietoyhdistintä saadaksesi taloushallinnon dimensiot ja arvot Operations-alustalta, tai yleistä tietoyhdistintä, jossa dimensiot ja arvot saadaan Excelin kautta muuntyyppisistä lähdejärjestelmistä. Esimerkiksi käytettäessä kustannuspaikan taloushallinnon dimensiota objektin dimensiona kaikki tuodut kustannuspaikat ovat kustannusobjektin dimensiojäseniä.</td>
</tr>
<tr class="even">
<td>Tilastodimensioiden määrittäminen tai tuominen</td>
<td>Tilastodimension jäsenet mitataan muina kuin rahayksiköinä, kuten koneen käyttötunteina, työntekijämääränä tai pinta-alana. Niitä käytetään tilinpäätöksessä tai kohdistuksien ja jakaumien perustana.</td>
</tr>
<tr class="odd">
<td>Tilastomittauksen lähdemallien luominen</td>
<td>Tilastomittauksen lähdemallia käytetään voi muunnettaessa Dynamics 365 for Operations -tietoja tilastomittauksiksi. Malli liitetään tiettyyn tilastodimension jäseneen. Mallit on esisuodatettu siten, että ne näyttävät vain taloushallinnon dimensioihin liittyvät taulukot.</td>
</tr>
<tr class="even">
<td>Kustannuslaskennan kirjanpidon luominen</td>
<td>Kustannuslaskennan kirjanpito on riippumaton kirjanpito, joka käyttää omaa kalenteria ja valuuttaa. Se on tärkeässä asemassa kaikkien kustannustapahtumien käsittelyssä. Esimerkiksi kustannuslaskennan kirjanpidon luokittelee kustannukset, jota perustuvat sen omiin kustannustasoihin ja kokoaa kustannukset, jotka perustuvat sen omiin objektin dimensioihin. Voit luoda kustannuslaskennan kirjanpitoja tarvittavan määrän hallinnan raportointiin eri näkökulmista.</td>
</tr>
<tr class="odd">
<td>Kustannusseurantayksiköiden luominen</td>
<td>Kustannusseurantayksiköt ovat kustannusrakenteen perusta, ja ne määrittävät kustannusvirran kustannuslaskennan kirjanpidossa. Ne täytyy liittää kustannusobjektin dimensioihin, joita ne edustavat kirjanpidossa.</td>
</tr>
<tr class="even">
<td>Kirjanpidon merkintöjen käsittely</td>
<td>Todellisen suorituskyvyn mittaamiseen tarvitaan tietoja. Tiedot tuodaan käyttämällä yhdistimiä, jotka määritetään kustannuslaskennan kirjanpidossa. Kun käsittelet kirjanpitotapahtumia, tiedot tuodaan lisäävästi.</td>
</tr>
<tr class="odd">
<td>Budjettivientien käsittely</td>
<td>Budjetoidun suorituskyvyn mittaamiseen tarvitaan tietoja. Tiedot tuodaan käyttämällä yhdistimiä, jotka määritetään kustannuslaskennan kirjanpidossa. Kun käsittelet budjetin tapahtumia, tiedot tuodaan lisäävästi.</td>
</tr>
<tr class="even">
<td>Voit luoda ja käyttää kustannustoimintakäytäntöjä.</td>
<td>Kustannustoimintakäytäntöjen avulla voit luokitella kustannukset kiinteisiin, muuttuviin tai osittain muuttuviin. Käytäntö perustuu sääntöön ja voimaantulopäivään. Oletusarvon mukaan kaikki kustannukset on merkitty luokittelemattomiksi siihen saakka kun käytät kustannustoimintakäytäntöjä ja lasket säännön vaikutukset. Laskennan jälkeen kustannukset luokitellaan.</td>
</tr>
<tr class="odd">
<td>Kustannusten seuranta</td>
<td>Kustannuslaskenta auttaa ymmärtämään kustannuskäytäntöjen vaikutusta, sillä sen avulla voidaan jäljittää kustannukset lähdearvoihin, ja käytettyjä sääntöjä, josta ne ovat peräisin. Tällä toiminnolla voidaan täysin jäljittää, milloin kustannukset suoritettiin, mitä kustannustyyppejä suoritettiin ja mitkä kustannustoimintasääntöjä sovellettiin.</td>
</tr>
<tr class="even">
<td>Dimensiohierarkioiden määrittäminen</td>
<td>Voit luoda dimensiohierarkioita luokittelua varten. Voit esimerkiksi määrittää luokitushierarkian, joka perustuu kustannustason dimensioon ja sen jäseniin. Vaihtoehtoisesti voit määrittää luokitushierarkian, joka perustuu kustannusobjektin dimensioon ja sen jäseniin. Raportointirakenteita käytetään seuraavissa tilanteissa:
<ul>
<li>Määrität kohdistukset, kustannushinnat ja kustannusten koontisäännöt.</li>
<li>Tarkastelet laskelmia työtilassa.</li>
<li>Määrität koostetietojen tarkastelun käyttöoikeudet.</li>
<li>Tarkastelet tietoja Excelissä.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Työtilassa tarkasteltavien tiliotteiden luominen</td>
<td>Työtilaa käyttämällä saat yleiskatsauksen todellisista ja budjetoiduista kustannuksista ja poikkeamista. Voit suodattaa tietoja kauden tai kustannustason mukaan. Työtila on suunniteltu kustannusseurannasta vastaavia päälliköitä varten. Se noudattaa käyttöoikeussääntöjä, jotka on määritetty dimensiohierarkioita varten.</td>
</tr>
<tr class="even">
<td>Luo raportteja Excelissä. <strong>Huomautus:</strong> Sinun on käytettävä Microsoft Excel 2016:tta.</td>
<td>Voit viedä kustannuslaskennan tietoja suoraan Exceliin tietoyksiköiden kautta ja käyttää Microsoft PivotTablea raporttien luomiseen.</td>
</tr>
</tbody>
</table>

## <a name="expense-management"></a>Matkalaskut
| Mitä voit tehdä                                                            | Miksi tämä on tärkeää                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Työntekijälle määritetty luottokortin tapahtumien määrittäminen uudelleen                     | Joissain tapauksissa poistetun työntekijän Active Directory -hakemistopalvelujen (D DS) tiliin käyttö on estetty, kun kirjattavat aktiiviset luottokorttitapahtumat tuodaan. Aiemmin ei voitu määrittää valtuutettua viittausta kulumerkinnälle tai liittää luottokorttitapahtumia kuluraporttiin. Nyt voit käyttää **Luottokorttitapahtumat**-sivua ja määrittää työntekijälle minkä tahansa luottokorttitapahtuman, vaikka työntekijä on poistettu. Kun olet siirtänyt luottokorttitapahtuman, tapahtuma voidaan valita kuluraporttiin ja maksaa kuluraportin hyväksynnän normaalimenettelyn kautta. |
| Uusien ja entisten työntekijöiden kulujen luottokorttitietojen muuttaminen | Voit muuttaa uusien ja entisten työntekijöiden kulujenhallinnan luottokorttitietoja. Aiemmin voitiin muuttaa aktiivisten työntekijöiden kulujen luottokorttitietoja.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Kuluraportin kopioiminen                                                    | Nyt voit kopioida aiemmat kulut luodessasi uuden kulun samaan kuluraporttiin. Voit kopioida kuluraportin ja siihen liittyvät kulut, jotka eivät ole luottokorttitapahtumia, uuteen kuluraporttiin. Sinun täytyy kuitenkin suorittaa kaikki tarvittavat erittelyt ja liittää tarvittavat kuitit määritettyjen kulukäytäntöjen ja luokkien mukaan. Voit lisätä luottokorttitapahtumia kuluraporttiin valitsemalla täsmäyttämättömien kulujen lisäämisen.                                                                                                                                                                                                                        |
| Kulujen joukkomuokkaus                                                        | Joitain luottokorttitapahtumia ei voi yhdistää kululuokkaan tai ne voi virheellisesti yhdistää tuonnin yhteydessä. Tässä tapauksessa työntekijöiden on vaihdettava liittyvä kululuokka manuaalisesti. Täsmäyttämättömiä kulujen hallinnan yhteydessä voit nyt joukkomuokata valittujen kulujen kululuokkia. Lisäksi tietyn kuluraportin valittuja kuluja hallittaessa voit joukkomuokata projektia ja lisätietoja.                                                                                                                                                                                    |
| Luottokorttitapahtumien vaihtokurssin vaihtaminen                     | Todellinen vaihtokurssi, jota käytetään luottokorttitapahtumiin, voi olla eri vaihtokurssi kuin järjestelmässä määritetty vaihtokurssi. Aiemmin työntekijät eivät voineet muuttaa vaihtokurssia luottokorttitapahtumalle, joka oli viety kulujenhallintaan. Nyt voit määrittää parametrin **Kuluraportin parametrit** -sivulla sallimaan vaihtokurssin muuttaminen luottokorttitapahtumille.                                                                                                                                                                                                                                            |
| Kulujen korruption vastainen todennuksen määrittäminen                            | Organisaation työntekijöillä voi olla liiketoimia valtion edustajien kanssa, ja joitain liiketoiminnan kuluja voidaan pitää lahjontana. Kulujenhallinnassa voit nyt määrittää korruption vastainen todennuksen, joka näkyy valituissa kululuokissa, kuten ateriat ja lahjat. Työntekijöiden on valittava, täyttävätkö kulut, joille on määritetty korruption vastainen todennus, organisaation käytäntöjen mukaiset kriteerit.                                                                                                                                                                                     |
| Manuaalisen syötön estäminen tietyissä kululuokissa          | Luottokorttitapahtumalle voidaan määrittää kululuokka, jota ei voi muuttaa. Esimerkki tällaisesta on viivästynyt luottokorttimaksu. Voit nyt määrittää kululuokan, jonka avulla voidaan luoda kuluja vain tuomalla. Tämä toiminto estää työntekijöitä luomasta luokkaan liittyviä kuluja manuaalisesti. Se ei salli luokan muuttamista tapahtumissa, jotka on tuotu ja jotka käyttävät tätä luokkaa.                                                                                                                                                                                   |
| Kuitin liittäminen useisiin kuluihin                                     | Kulujenhallintaan ladattu kuitti voi liittyä useisiin kuluihin. Aiemmin kuitti, joka liittyy useisiin kuluihin, piti ladata kerran kullekin kululle. Nyt voit liittää kuitin kuluun, joka on ladattu aiemmin ja liitetty toiseen kuluun samassa kuluraportissa. Jos lataat kuitin kuluraportin otsikkoon, voit valita vähintään yhden rivin, johon kuitti liitetään.                                                                                                                                                                                        |
| Tulevaisuuteen päivättyjen kulujen luominen                                              | Kun kopioit esimerkiksi kuluraportin, kulun tapahtumapäivämäärä voi olla tulevaisuudessa. Aiemmissa versioissa ei sallita kulujen päiväämistä tulevaisuuteen. Voit luoda ja tallentaa kuluja, joiden päiväys on tulevaisuudessa. Et kuitenkaan voi lähettää tulevaisuudessa päivättyä kulua.                                                                                                                                                                                                                                                                                                                                                                                 |
| Osavaltion/provinssin verojen kulujen määrittäminen                              | Maan tai alueen mukaan eri osavaltioiden ja provinssien kustannuksiin sovelletaan eri arvonlisäveroprosentteja. Voit nyt määrittää arvonlisäveron konfiguraatiot osavaltion tai provinssin tasolla, ei vain maan tai alueen tasolla. Jos jätät **Osavaltio/provinssi**-kentän tyhjäksi **Verokonfiguraatio** sivulla, arvonlisäveroryhmä koskee tietyn maan tai alueen kaikkia osavaltioita/provinsseja.                                                                                                                                                                                                                                       |
| Kulujen luottokorttityypin määrittäminen                                          | Aiemmin ei ollut käytössä sivua, jossa voit luoda uuden luottokorttityypin, esimerkiksi Visa, MasterCard tai AMEX, jota voitiin käyttää Kulujenhallinnassa. Voit nyt luoda Kulujenhallinnassa käytettävän luottokorttityypin. Sivun sijaitsee **Asetukset**-alueella **Laskelmat ja koodit** osassa.                                                                                                                                                                                                                                                                                                                                                 |
| Kuluraporttien monitasoisen hyväksynnän työnkulun määrittäminen                 | Kuluraporttien uusi työnkulku tukee monitasoista hyväksyntäprosessia. Työntekijät kirjoittavat väliaikaiset hyväksyjät ja lopulliset hyväksyjät kuluraportin luomisen yhteydessä. Työnkulku reitittää sitten kuluraportin väliaikaisille hyväksyjille ensin. Kun kuluraportti on hyväksytty, työnkulku reitittää sen lopullisille hyväksyjille lopullista hyväksyntää varten.                                                                                                                                                                                                                                                                                          |
| Muiden kuin kuluraporttiin liitettyjen kulujen luominen ja ylläpitäminen    | Käyttäjä voi nyt luoda ja ylläpitää kuluja (esimerkiksi liittämällä tai erittelemällä kuitteja tai määrittämällä vierailijat) luomatta ensin kuluraporttia. Yksi tai useampia kuluja voidaan valita ja lisätä uuteen kuluraporttiin ja lähettää hyväksyttäviksi. Uusi sivu kulujen ylläpitoa varten on kohdassa **Kulujenhallinta** &gt; **Omat kulut** &gt; **Kulut**.                                                                                                                                                                                                                                                       |

## <a name="financial-management"></a>Taloushallinto
<table>




<thead>
<tr class="header">
<th>Mitä voit tehdä</th>
<th>Miksi tämä on tärkeää</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Käyttöomaisuuden arvon seuranta määrittelyn yhden "kirja"-käsitteen avulla</td>
<td>Aiemmin käyttöomaisuuserän arvojen seuraamiseen käytettiin kahdenlaisia arviointityyppejä: arvomallit ja poistokirjat. Nykyisessä versiossa nämä kaksi käsitettä on yhdistetty yhdeksi arviointikäsitteeksi, jonka nimi on "kirja". Kirjat toimivat sekä arvomalleina että poistokirjoina. Voit esimerkiksi poistaa käytöstä kirjauksen kirjanpitoon. Kirjat, jotka kirjataan pääkirjanpitoon, ovat yleensä yrityksen taloushallinnon raportointia varten. Kirjoja, joita ei kirjata pääkirjanpitoon, voidaan käyttää yleensä veroraportointia varten.</td>
</tr>
<tr class="even">
<td>Kirjanpidon tilinpäätöksen suorittaminen useille yrityksille</td>
<td>Voit nopeuttaa tilinpäätösprosessia suorittamalla tilinpäätöksen useille yrityksille yhteiseltä tilinpäätössivulta. Yritysryhmät voidaan määrittää, samoin asetukset, jotka pitää säilyttää seuraavaan vuoteen. Myös muita käytettävyyden parannuksia on tehty tilinpäätösprosessiin.</td>
</tr>
<tr class="odd">
<td>Kirjanpidon ulkomaanvaluutan uudelleenarvostukseen tehdyistä parannuksista saatavat hyödyt</td>
<td>Kirjanpidon ulkomaanvaluutan uudelleenarvostukseen on tehty seuraavat parannukset:
<ul>
<li>Päätiliin on lisätty vaihtokurssin tyyppi. Vaihtokurssin tyyppiä käytetään vaihtokurssin määrittämiseen valuutan uudelleenarvostuksen aikana. Jos vaihtokurssin tyyppiä ei ole määritetty, prosessi käyttää edelleen kirjanpidossa määritettyä vaihtokurssin tyyppiä.</li>
<li>Nyt on helpompaa määrittää päätilit ja valuutat, joille uudelleenarvostus suoritetaan.</li>
<li>Uudelleenarvostus voidaan suorittaa useille yrityksille.</li>
<li>Järjestelmä ylläpitää jokaisen uudelleenarvostusprosessin historiatietoja sekä myyntireskontran (AR) ja ostoreskontran (Ostoreskontran) uudelleenarvostusprosessien historiatietoja.</li>
<li>Prosessia suoritettaessa voit esikatsella uudelleenarvostuksen tuloksia. Esikatselu näyttää tulokset kaikkien yritysten osalta, joille prosessi on suoritettu. Voit kirjata esikatselusta kaikki juridiset henkilöt tai niiden osajoukon. Voit myös viedä esikatselu tulokset Exceliin.</li>
</ul></td>
</tr>
<tr class="even">
<td>Tapahtumien tarkastelu ylimääräisillä kirjanpitotasoilla</td>
<td><strong>Pääkirja</strong>-luettelosivulla ja <strong>Dimensioraportti</strong>-raportissa voit valita muut kirjanpitotasot, jotka on lisätty kirjanpitoon. Valitessasi lisäkirjanpitotasot, näiden kirjanpitotasojen oikaisut sisällytetään saldoihin luettelosivulla tai raporteissa.</td>
</tr>
<tr class="odd">
<td>Toimintaohjeiden liittäminen tilinpäätösmalliin</td>
<td>Aiemmin asiakirja voitiin liittää tehtävän valmistumisen jälkeen. Voit esimerkiksi liittää luodun raportin. Voit nyt liittää malliin dokumentointiohjeita. Dokumentointiohjeet kopioidaan jokaiseen tehtävään tilikauden aikataulussa siten, että tehtävän omistaja voi tarkastella tehtävän suorittamisohjeita.</td>
</tr>
<tr class="even">
<td>Konsernin sisäisen kirjanpidon asetusten määritys jaetulta sivulta</td>
<td><strong>Konsernin sisäisen kirjanpidon asetukset -sivu</strong>on jaettu, jotta organisaatio voi määrittää yritysparit, jotka voivat toimia keskenään. Lisäksi voit nyt lisätä lähdeyritykselle tapahtuman muualta kuin kohdeyrityksestä. Jos jompikumpi yritys voi määrittää konsernin sisäisen tapahtuman, vastavuoroinen pari pitää määrittää. Siksi kohdeyritys määritetään myös lähdeyritykseksi.</td>
</tr>
<tr class="odd">
<td>Budjettisuunnitelmien perusteluasiakirjojen lähettäminen</td>
<td>Voit luoda perustelumallitiedoston lisädokumentaationa kaikille pyydetyille budjettisummille. Käyttäjät voivat täyttää mallin tiedot ja liittää mallin budjetin suunnitelmaan siten, että sitä voidaan käyttää hyväksyntäprosessin aikana.</td>
</tr>
<tr class="even">
<td>Budjettitapahtumien lisäsääntöjen käyttöönotto</td>
<td>Jos kirjanpitoon on määritetty lisäsääntöjä, näitä sääntöjä voidaan käyttää budjettirekisteriin tehtäviin uusiin merkintöihin ja siirtoihin.</td>
</tr>
<tr class="odd">
<td>Ennakkomaksujen laskutuksen tehtävien parannetun näkyvyyden hyödyntäminen</td>
<td>Uudella <strong>Avoimet ennakkomaksut</strong> -luettelosivulla on tilannekuva ennakkomaksu laskutuksen tehtävien tilasta. Sivu tarjoaa Ostoreskontra-osastolle tietoja ostotilauksista, joilla on laskutettavia ennakkomaksu-arvoja, laskutettuja arvoja jotka pitää maksaa, ja maksettujen laskujen arvoja, joita täytyy käyttää vakiolaskuissa. Lisäksi vakiolaskuihin tehtävän maksettujen ennakkomaksulaskujen tietojen automaattisen käyttöönoton parannukset auttavat laskuttajia syöttämään tietoja tehokkaammin.</td>
</tr>
<tr class="even">
<td><strong>Toimittajayhteistyön laskutus</strong> -työtilan käyttäminen</td>
<td>Uusi <strong>Laskutus</strong>-työtilan <strong>Toimittajayhteistyö</strong>-alueella mahdollistaa ulkoisille toimittajille turvallisen pääsyn omia laskutietoihin. Esimerkiksi toimittajat voivat nähdä, onko lasku on maksettu ja lähettää oman laskun. Tämä muutos edistää tehokkaampaa ja ajantasaista tiedonsiirtoa alihankkijoiden kanssa. Laskuttajilla on vähemmän keskeytyksiä.</td>
</tr>
<tr class="odd">
<td>Yritysten vaihtaminen laskua syötettäessä</td>
<td>Parannusten ansiosta useiden yritysten laskuja kirjoittavat laskuttajat voivat vaihtaa nopeasti yritystä laskutussivuilta. Tämä toiminto säästää laskuttajien aikaa, koska ei tarvita enää uloskirjautumista nykyisen yrityksen tiedoista ja kirjautumista sisään eri yrityksen tietoihin. <strong>Yleinen laskukirjauskansio</strong> -sivun ja <strong>Toimittajan laskut</strong> -sivun avulla käyttäjät voivat vaihtaa yritystä tietojen syötön aikana.</td>
</tr>
<tr class="even">
<td>Yhdysvaltojen veroviraston (Internal Revenue Service, IRS) lomakkeen 1099 mukaisten yhdistetyn liittovaltion ja osavaltion arkistointiohjelman sähköisten tiedostojen tuki</td>
<td>Kun <strong>Yhdysvallat</strong>-määritysavain on käytössä, sähköinen 1099-ilmoitusprosessi tarjoaa muita toimintoja, jotka ovat IRS:n yhdistetyn liittovaltion ja osavaltion arkistointiohjelman mukaisia. IRS on laatinut ohjelman niin, että se toimittaa ilmoitetut tiedot sähköisesti ohjelmaa käyttäviin osavaltioihin.</td>
</tr>
<tr class="odd">
<td>Täsmäytysten oikaisut</td>
<td>Oikaisujen avulla laskuttajat voivat tehdä täsmäytykset tehokkaammin, koska kirjanpitäjät voivat mahdollistaa useiden kirjaamattomien maksujen maksamisen samalla laskulla.</td>
</tr>
<tr class="even">
<td>Yritystenvälinen näkymä</td>
<td>Keskitettyjen maksujen kirjanpitäjät voivat tarkastella erääntyneitä laskuja eri yrityksissä. <strong>Toimittajien maksut</strong>- ja <strong>Asiakasmaksut</strong>-työtilojen näkyvyys erääntyneisiin laskuihin on nyt parempi ja niiden hallinta helpompaa yritysten välisen näkyvyyden ja suodatuksen ansiosta, jotka kuuluvat keskitettyyn maksujen organisaatiohierarkiaan.</td>
</tr>
<tr class="odd">
<td><strong>Maksuliikenne</strong>-työtilan käyttö</td>
<td>Uusi <strong>Maksuliikenne</strong>-työtila auttaa seuraamaan yrityksiesi pankkitilejä ja niiden saldoja. Nykyisen ja odottavat saldot on heti saatavissa kaikilta tileiltä ja voit siirtyä takaisin tapahtumasta yksityiskohtaisiin tositteisiin. Näet myös kunkin pankkitilin historialliset saldotiedot tai yrityksen kaikkien tapahtumayhteenvedot sekä lyhyen että pitkän aikavälin näkymässä. Saat paremman käsityksen pankkitilin täsmäytyksessä, koska edellisen täsmäytyksen päivämäärä ilmoitetaan kullekin pankkitilille erikseen ja käytössä on myös ilmaisin käynnissä oleville täsmäytyksille.</td>
</tr>
<tr class="even">
<td>Sähköisten tiliotteiden tuominen kaikille yrityksille yhdellä kertaa</td>
<td>Voit tuoda sähköiset tiliotteet kaikille yrityksille yhdellä kertaa. Tiliotetiedostot voivat sisältää useiden pankkitilien ja yritysten tiliotteita ja zip-tiedostoissa voi olla useita tiliotetiedostoja. Yhdellä tuontiprosessilla voit käynnistää kaikkien yritysten raportoitujen pankkitilien täsmäytyksen. Tämän ominaisuuden avulla säästät aikaa, koska sinun ei tarvitse vaihtaa yritystä ja tuoda useita laskelmia. Voit suorittaa automaattisesti täsmäytyssäännöt kullekin yritykselle kaikki tuotujen laskelmien perusteella.</td>
</tr>
<tr class="odd">
<td>Arvostuksen seuranta</td>
<td>Yhdellä käyttöomaisuuserällä voi olla useita arvostuksia eri kirjanpidon sääntöjen mukaan ja haluttaessa se voi kirjata liittyvät tapahtumat kirjanpitoon. Nämä arvostuksia seurattiin aiemmin arvomalleista tai poistokirjoista. Voit seurata nyt näitä arvostuksia, joita nyt kutsutaan kirjoiksi, yhteisten kirjauskansioiden, kyselyiden ja raporttien avulla. Yhtenäinen käyttökokemus yksinkertaistaa käyttöönottoa ja vähentää käyttöliittymien määrää, joita kausittaiset prosessit edellyttävät.</td>
</tr>
<tr class="even">
<td>Yritystenvälisten poistojen suoritusten parannusten hyödyntäminen</td>
<td>Voit nyt aloittaa kaikkia yrityksiä koskevan käyttöomaisuuden poiston suorittamisen yhdeltä sivulta. Voit kirjata kirjauskansiot automaattisesti sen jälkeen, kun ne luodaan. Voit lähettää kirjauskansioiden luomisen ja kirjaamisen eräkäsittelyyn, jotta poisto suoritetaan taustalla. Nämä parannukset vähentävät tehottomuutta, koska sinun ei tarvitse aloittaa yksittäistä poiston suoritusta erikseen kullekin yritykselle. Parannuksen ansiosta käyttöomaisuuden keskitetty hallinta on tehokkaampaa.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Henkilöstöresurssien hallinta
| Mitä voit tehdä                                                                                | Miksi tämä on tärkeää                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Suoritustason kirjauskansioiden luominen                                                                  | Ennen kuin suoritat tarkastuksen, kerätään usein tietoja tehtävistä ja tapahtumista, jotka ovat vaikuttaneet onnistumiseesi työntekijänä tarkastelukauden aikana. Voit lisätä merkinnän suorituskyvyn kirjauskansioon dokumentoidaksesi nämä tehtävät ja tapahtumat. Voit myös liittää nämä tehtävät ja tapahtumat tavoitteeseen tai suorituskykyarvioon antaaksesi lisätietoja tarkistajalle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Yksityiskohtaisten tavoitteiden luominen                                                                    | Voit hallita tarkemmin tavoitteita, jotka olet määrittänyt. Voit luoda tavoitteiden mittaukset, linkittää suorituskyvyn kirjauskansion tapahtumat mittauksiin ja liittää ja tarkastella asiakirjoja. Voit tallentaa tavoitteet malleina ja käyttää niitä uudelleen pika-asetuksia varten.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Tarkempien suorituskykyarviointien luominen                                                      | Suoritustasoarvioinnit, joita virallisesti kutsutaan keskusteluiksi, ovat entistä joustavampia ja tukevat jatkuvaa palautetta ja virallisempia arviointeja. Voit noutaa aktiiviset tavoitteet ja kirjata niistä kommentteja ja lisätä osia omien osaamisalueiden tarkastelua varten. Muissa osissa voit lisätä tai tarkastella mittauksia, suorituskyvyn kirjauskansion tapahtumia, liitteitä ja hyväksyntiä, jotka liittyvät tarkasteluun.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Toimihierarkioiden lisääminen työnkulkuihin                                      | Voit liittää työnkulun toimihierarkiaan. Voit myös muokata työnkulkuvaiheet optimoidaksesi hyväksyntäprosessin yrityksen tarpeiden mukaisiksi. Voit määrittää tehokkaan hyväksyntärakenteen, joka sopii organisaatiosi käyttämiin eri raportointisuhteisiin.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Työnkulku tukee henkilökohtaisten tunnuslukujen (PIN) syöttämistä Työntekijän itsepalveluun. | Henkilöstöhallinnon (HR) työnkulkutoimintoja on laajennettu ja ne sisältävät nyt PIN-tuen. Työntekijät voivat lisätä ja muokata omaa PIN-koodiaan tehokkuuden lisäämiseksi. Henkilöstöhallinnon työntekijät voivat kuitenkin tarkistaa tietojen tarkkuuden ja kattavuuden, ennen kuin ne lisätään työntekijän tietueeseen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Tavoitemallien luominen ja käyttäminen lisättäessä uusia tavoitteita                                          | Voit luoda tavoitemalleja, jotka ovat yhteisiä useille yrityksen työntekijöille. Työntekijät voivat lisätä omia tavoitteitaan mallista, johtajat voivat lisätä malleja ryhmälleen ja henkilöstöhallinnon ryhmän jäsenet voivat lisätä tavoitteita työntekijöille kaikkialla yrityksessä.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Tavoiteryhmien luominen ja käyttäminen lisättäessä uusia tavoitteita                                             | Voit lisätä tavoitemalleja ryhmään ja sen avulla voit luoda vähintään yhden tavoitteen työntekijälle, ryhmälle, toimelle, osastolle tai yritykselle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Tarkistusprosessin tarkempi hallinta                                                     | Voit hallita tarkistusprosessia työnkulun avulla. Voit luoda tarkastelumalleja ja käyttää niitä arviointien luomiseen. Voit myös lisätä luokituksia tarkasteluun.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Määritä tarkastelukausien avulla tarkastelun aikaväli.                                    | Voit määrittää suorituskykyarvion ennustekauden, jolloin tarkastelun alkamis- ja päättymispäivät lisätään automaattisesti. Voit kuitenkin muuttaa näitä oletuspäivämäärien tarpeen mukaan.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Ota käyttöösi viisi uutta henkilöstöhallinnon Power BI -sisältöpakettia                                     | Henkilöstöorganisaatiot ja -päälliköt voivat analysoida seuraavia uusien sisältöpakettien avulla: työvoiman mittarit • demografiset erittelyt iän, sukupuolen ja siviilisäädyn perusteella • väsymissuhteiden vuosittainen vertailu ja luettelo työntekijöiden yrityksestä lähdön syistä • Tarkastella luetteloa avoimista toimista sekä vertailua avoimista ja suljetuista toimista Palkkiot ja edut • Vertailla tunti- ja kuukausipalkkaisia työntekijöitä • Tarkastella etuuksia käyttävien työntekijöiden määrää • Tarkastella työntekijöitä rekrytointi-työntekijätyypin perusteella • Analysoida hakijoita hakijamäärän, hakijoiden alkuperän ja hakijoiden kohteena olevien toimien perusteella Organisaatiokoulutus • kurssille ilmoittautuminen tilan mukaan • kurssille osallistuminen tilan mukaan • luettelo kurssille ilmoittautuneista työntekijöistä Työntekijöiden osaaminen ja kehitys • luettelo työntekijöiden osaamisesta • erittely osaamistyypeistä ryhmän jäsenen perusteella |

## <a name="localizations"></a>Lokalisoinnit
<table>




<thead>
<tr class="header">
<th>Mitä voit tehdä</th>
<th>Miksi tämä on tärkeää</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lokalisoinnit ovat saatavina 18 muussa maassa:
<ul>
<li>Itävalta</li>
<li>Belgia</li>
<li>Brasilia</li>
<li>Kiina</li>
<li>Tšekin tasavalta</li>
<li>Viro</li>
<li>Suomi</li>
<li>Unkari</li>
<li>Italia</li>
<li>Latvia</li>
<li>Liettua</li>
<li>Norja</li>
<li>Puola</li>
<li>Saudi-Arabia</li>
<li>Espanja</li>
<li>Ruotsi</li>
<li>Sveitsi</li>
<li>Thaimaa</li>
</ul>
Seuraavissa maissa tarvitaan myös Retail-lokalisointia. Retail-lokalisointia ei ole vielä suoritettu näissä maissa ja sen ajankohdaksi on suunniteltu vasta v. 2017 H1:
<ul>
<li>Brasilia</li>
<li>Tšekin tasavalta</li>
<li>Viro</li>
<li>Unkari</li>
<li>Latvia</li>
<li>Liettua</li>
<li>Malesia</li>
<li>Puola</li>
<li>Ruotsi</li>
</ul></td>
<td>Dynamics 365 for Operations on saatavana 18 muussa maassa. Helpottaaksemme lokalisointia ja konfigurointia säännösten mukaisia sähköinen raportointitoimintoja on muutettu sähköisten raportoinnin (ER) konfiguraatioiksi, ja jotkut säännösten mukaiset Microsoft SQL Server Reporting Services (SSRS)-raportit on muunnettu sähköisen raportoinnin konfiguraatioiksi, jotka käyttävät Excel-malleja. Muunnetut toiminnot on erityisesti mainittu myöhemmin tässä taulukossa.</td>
</tr>
<tr class="even">
<td>Japani – Ryhmän käyttöomaisuuserät tulostettaessa lomake 26 ja siihen liitetyt taulukot.</td>
<td>Lomake 26 on toimitettava jokaiseen kaupunkiin, jossa yhtiö toimii. Tulostettaessa lomaketta 26 käyttöomaisuuserät voidaan automaattisesti ryhmitellä ja lajitella sijainnin mukaan, mikä säästää työaikaa.</td>
</tr>
<tr class="odd">
<td>Japan – Katso nopeutetun ja lisäpoistojen summat profiilissa.</td>
<td>Profiili voi antaa tarkan arvion nopeutetun ja lisäpoiston summista.</td>
</tr>
<tr class="even">
<td>Japani – Ennakonpidätyksen vaiheittainen laskenta.</td>
<td>Japanin valtion edellyttää, että ennakonpidätys lasketaan vaiheittain maksusumman perusteella.</td>
</tr>
<tr class="odd">
<td>Japanilainen – Yritysten suurten rakennusten postinumerotiedoston tuonti.</td>
<td>Viranomaisten tietyille yritysten suurille rakennuksille myöntämän postinumeron tiedosto voidaan tuoda järjestelmään. Osoite voidaan sitten johtaa postinumerosta.</td>
</tr>
<tr class="even">
<td>Japani– Käyttöomaisuuden odotusjakson määrittäminen.</td>
<td>Odotusjaksojen avulla käyttäjä voi keskeyttää käyttöomaisuuden poiston tietyn jakson ajaksi. Tämä toiminto on säädösten mukaan pakollinen.</td>
</tr>
<tr class="odd">
<td>Eurooppa – Arvonlisäveron (ALV) rekisteröintinumeron määrittäminen toisen osapuolen osoitteeseen käyttämällä Rekisteröintitunnus-kehikkoa.</td>
<td>Voit määrittää ALV-rekisterinumeron toisen osapuolen osoitteelle rekisteröintitunnusten kehikon ja uuden <strong>ALV-tunnus</strong> -rekisteröintiluokan avulla.</td>
</tr>
<tr class="even">
<td>Suomi – Määritä asiakkaan asiakasnumero toisen osapuolen osoitteelle käyttämällä Rekisteröintitunnus-kehikkoa.</td>
<td>Voit määrittää tullin asiakasnumeron osapuolen osoitteelle rekisteröintitunnusten kehikon ja uuden <strong>Tullin asiakasnumero</strong> -rekisteröintiluokan avulla.</td>
</tr>
<tr class="odd">
<td>Ranska – Myyntilaskujen tulostaminen Ranskan asettelun mukaisesti.</td>
<td>Myyntilaskun tuloste oikaistaan niin, että se vastaa ranskalaisia vaatimuksia.</td>
</tr>
<tr class="even">
<td>Ranska – Tilikauden mukaisen kronologinen asiakirjojen numeroinnin pakottaminen</td>
<td>Ranskalaiset myyntilaskujen numerointivaatimukset voidaan täyttää määrittämällä tilikausikohtaiset numerojaksot myyntilaskuille.</td>
</tr>
<tr class="odd">
<td>Itävallan lokalisointi – ER-konfiguraatiot</td>
<td><ul>
<li>Itävallan EU-myyntiluettelon XML-muoto</li>
<li>Itävallan Intrastat-muoto</li>
<li>Itävallan ISO20022-tilisiirron maksumuoto</li>
<li>Itävallan ISO20022-suoraveloituksen maksumuoto</li>
<li>Itävallan EDIFACT PAYMUL -muoto</li>
<li>Itävallan ALV-ilmoitus</li>
</ul></td>
</tr>
<tr class="even">
<td>Belgian lokalisointi – ER-konfiguraatiot</td>
<td><ul>
<li>Belgian BLWI-muoto</li>
<li>Belgian EU-myyntiluettelon XML-muoto</li>
<li>Belgian käyttöomaisuusraportti Belgia</li>
<li>Belgian Intervat-muoto</li>
<li>Belgian Intrastat-muoto</li>
<li>Belgian laskutusliikevaihtoraportti</li>
<li>Belgian kirjanpidon tapahtumien vientimuoto</li>
<li>Belgian SWIFT-toimittajan maksumuoto</li>
<li>Belgian CODA -tiliotteen tuontimuoto</li>
<li>Belgian ISO20022-tilisiirron maksumuoto</li>
<li>Belgian ISO20022-suoraveloituksen maksumuoto</li>
</ul></td>
</tr>
<tr class="odd">
<td>Brasilian lokalisointi – ER-konfiguraatiot</td>
<td><ul>
<li>Brasilian GIA SP</li>
<li>Brasilian GIA-ST</li>
</ul></td>
</tr>
<tr class="even">
<td>Tšekin tasavallan lokalisointi – ER-konfiguraatiot</td>
<td><ul>
<li>Tšekin tasavallan EU-myyntiluettelon XML-muoto</li>
<li>Tšekin tasavallan Intrastat-muoto</li>
<li>Tšekin tasavallan ALV-ilmoitus</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kiinan lokalisointi – ER-konfiguraatiot</td>
<td><ul>
<li>Kiinan myyntireskontran erääntymisraportin muoto</li>
<li>Kiinan asiakkaan erääntyneen summan analyysiraportti</li>
<li>Kiinan ostoreskontran erääntymisraportin muoto</li>
<li>Kiinan myyjän erääntyneen summan analyysiraportti</li>
<li>Kiinan saatavien maksuraportin erääntymisanalyysimuoto</li>
<li>Kiinan pääkirjan raporttimuoto</li>
<li>Kiinan kirjanpitotilin saldon raporttimuoto</li>
<li>Kiinan toimittajasaldon raporttimuoto</li>
<li>Kiinan GBT-tiedosto</li>
<li>Golden tax -veron vientitiedoston muoto</li>
<li>Kiinan tuotannon kulutuksen varianssiraportti muoto</li>
</ul></td>
</tr>
<tr class="even">
<td>Viron lokalisointi – ER-konfiguraatiot</td>
<td><ul>
<li>Viron EU-myyntiluettelon XML-muoto</li>
<li>Viron Intrastat-muoto</li>
<li>Viron varaston uudelleenluokittelun raportti</li>
<li>Viron ISO20022-tilisiirron maksumuoto</li>
<li>Viron asiakkaan ja toimittajan saldoilmoitusraportti</li>
<li>Viron ALV-ilmoitus</li>
</ul></td>
</tr>
<tr class="odd">
<td>Suomen lokalisointi – ER-konfiguraatiot</td>
<td><ul>
<li>Suomen EU-myyntiluettelon TXT-muoto</li>
<li>Suomen Intrastat-muoto</li>
<li>Suomen ISO20022-tilisiirron maksumuoto</li>
</ul></td>
</tr>
<tr class="even">
<td>Unkarin lokalisointi – ER-konfiguraatiot</td>
<td><ul>
<li>Unkarin EU-myyntiluettelon XML-muoto</li>
<li>Unkarin Intrastat-muoto</li>
<li>Unkarin yksinkertaistettu Intrastat-muoto</li>
<li>Unkarin laskuluettelon vientimuoto.</li>
<li>Unkarin ALV-ilmoitus</li>
<li>Unkarin eritelty ALV-ilmoitus</li>
<li>Unkarin varastolaskelma</li>
<li>Unkarin MultiCash-maksumuoto</li>
</ul></td>
</tr>
<tr class="odd">
<td>Italian lokalisointi – ER-konfiguraatiot</td>
<td><ul>
<li>Italian Intrastat-muoto</li>
<li>Italian projektilaskun muoto</li>
<li>Italian myyntilaskun muoto</li>
<li>Italian ISO20022-tilisiirron maksumuoto</li>
<li>Italian ISO20022-suoraveloituksen maksumuoto</li>
<li>Italian RIBA-maksukehotuksen maksusuorituksen muoto</li>
<li>Italian kotimaisten verotapahtumien raportti</li>
<li>Italian mustan listan raportti</li>
<li>Italian Modello770-raportti</li>
<li>Italian vuosittaisen veroviestinnän raportti</li>
</ul></td>
</tr>
<tr class="even">
<td>Latvian lokalisointi – ER-konfiguraatiot</td>
<td><ul>
<li>Kassakuittien käyttöraportti (LV)</li>
<li>Latvian EU-myyntiluettelon TXT-muoto</li>
<li>Latvian EU-myyntiluettelon oikaisujen XML-muoto</li>
<li>Latvian Intrastat (A) -muoto</li>
<li>Latvian Intrastat (B) -muoto</li>
<li>Latvian inventointiluettelo</li>
<li>Latvian inventointi-ilmoitus</li>
<li>Latvian varaston siirtotapahtuma</li>
<li>Latvian sisäisen siirron toimitusilmoitus</li>
<li>Latvian varaston uudelleenluokitteluasiakirja</li>
<li>Latvian ISO20022-tilisiirron maksumuoto</li>
<li>Latvian ALV-ilmoitus</li>
</ul></td>
</tr>
<tr class="odd">
<td>Liettuan lokalisointi – ER-konfiguraatiot</td>
<td><ul>
<li>Liettuan EU-myyntiluettelon XML-muoto</li>
<li>Liettuan Intrastat-muoto</li>
<li>Liettuan varastolaskelma</li>
<li>Liettuan ISO20022-tilisiirron maksumuoto</li>
<li>Liettuan asiakkaan ja toimittajan väliset täsmäytysraportti</li>
<li>Liettuan ALV-ilmoitus</li>
</ul></td>
</tr>
<tr class="even">
<td>Norjan lokalisointi – ER-konfiguraatiot</td>
<td><ul>
<li>Norjan maksukehotuksen letter-paperikoko</li>
<li>Norjan AutoGiro-maksumuoto</li>
<li>Norjan AvtaleGiro- asiakkaan maksun muoto</li>
<li>Norjan eFaktura- asiakkaan maksun muoto</li>
<li>Norjan ISO20022-tilisiirron maksumuoto</li>
<li>Norjan NETS-maksumuoto</li>
</ul></td>
</tr>
<tr class="odd">
<td>Puolan lokalisointi – ER-konfiguraatiot</td>
<td><ul>
<li>Puolan Intrastat-muoto</li>
<li>Puolan varastoasiakirjat</li>
<li>Puolan varaston uudelleenluokitteluasiakirja</li>
<li>Puolan MultiCash-maksumuoto</li>
<li>Puolan MultiCash- ulkomaanmaksun muoto</li>
<li>Puolan asiakkaan ja toimittajan saldovahvistusraportti</li>
</ul></td>
</tr>
<tr class="even">
<td>Saudi-Arabian lokalisointi – ER-konfiguraatiot</td>
<td>Saudi-Arabian pankin maahantuontikustannusten sekalaisten kulujen kohdistusmuoto</td>
</tr>
<tr class="odd">
<td>Espanjan lokalisointi – ER-konfiguraatiot</td>
<td><ul>
<li>Espanjan EU-myyntiluettelon TXT-muoto</li>
<li>Espanjan Intrastat-muoto</li>
<li>Espanjan projektilaskun muoto</li>
<li>Espanjan myyntilaskun muoto</li>
<li>Espanjan ISO20022-tilisiirron maksumuoto</li>
<li>Espanjan ISO20022-suoraveloituksen maksumuoto</li>
<li>Espanjan alv-rekisterikirjan muoto</li>
<li>Espanjan alv-rekisterikirjan yhteenvedon muoto</li>
<li>Espanjan ilmoitus 347 vienti ASCII-muotoon</li>
<li>Espanjan ilmoitus 347 -raportti</li>
</ul></td>
</tr>
<tr class="even">
<td>Ruotsin lokalisointi – ER-konfiguraatiot</td>
<td><ul>
<li>Ruotsin Intrastat-muoto</li>
<li>Ruotsin Bankgirot Autogiro- asiakkaan maksun muoto</li>
<li>Ruotsin Bankgirot -toimittajamaksujen muoto</li>
<li>Ruotsin SWIFT-toimittajan maksumuoto</li>
<li>Ruotsin SIE-vientimuoto</li>
<li>Ruotsin ISO20022-tilisiirron maksumuoto</li>
</ul></td>
</tr>
<tr class="odd">
<td>Sveitsin lokalisointi – ER-konfiguraatiot</td>
<td><ul>
<li>Sveitsin DebitDirect-maksumuoto</li>
<li>Sveitsin LSV-suoramaksumuoto</li>
<li>Sveitsin ISO20022-tilisiirron maksumuoto</li>
<li>Sveitsin ISO20022-suoramaksumuoto</li>
<li>Sveitsin ESR -tiliotteen tuontimuoto</li>
</ul></td>
</tr>
<tr class="even">
<td>Saksa – Toimittajamaksujen vienti DTAZV-muodossa</td>
<td>Saksa edellyttää DTAZV-muotoa ulkomaan muotomäärityksessä, joka edustaa määritysten mukaista tilisiirtoviestiä (toimittajan maksu) rajat ylittävälle maksulle Saksasta ulkomaisessa pankissa olevalle tilille tai ulkomaan valuutassa olevalle maksulle kotimaiseen tiliin. 
</td>
</tr>
</tbody>
</table>

### <a name="electronic-reporting"></a>Sähköinen raportointi

| Mitä voit tehdä                                                                                                                                                                                                                                                                                     | Miksi tämä on tärkeää                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sähköisen raportoinnin ER-raporttien konfigurointi tietojen lisäämiseksi useissa tiedostomuodoissa Tiedostonhallinnan tietovarastosta luotaviin sähköisiin viesteihin.                                                                                                                                                              | ER-raportit voivat lisätäi tietoja Tiedostonhallinnan tietovarastosta luotaviin sähköisiin viesteihin. Liiketoiminta-asiakirjan liitteet voidaan lisätä lakisääteisten vaatimusten mukaan sähköisiin viesteihin, jotka luodaan asiakirjaa varten. Tällä hetkellä liitteet voidaan lisätä luotavaan XML-sanomaan MIME-muodossa. Vaihtoehtoisesti liitteet voidaan lisätä luotuun binaarisanomaan Base64-muodossa.                                                                      |
| Sähköisen raportoinnin ER-raporttien konfigurointi sähköisten asiakirjojen luomiseksi Excel-, Microsoft Word- tai PDF-muodossa.                                                                                                                                                                                                      | Yhdellä konfiguroinnilla sähköisen raportoinnin ER-raportit luovat sähköisiä asiakirjoja kolmessa eri tiedostomuodossa: OPENXML-laskentataulukko- (Excel), Word- ja XML-muodoissa (XFDF) (PDF). Käyttäjät voivat valita tiedostomuodon lisäämällä muotomallin ER-raporttiin Excel-, Word- tai PDF-tiedostona.                                                                                                                                                                                                                                                                       |
| Sähköisen raportoinnin ER-raporttien konfigurointi tietojen lisäämiseksi OPENXML-laskentataulukkomuodossa luotujen sähköisten asiakirjojen ylä- ja alatunnisteisiin ja sivunvaihtojen määrittämiseksi.                                                                                                                               | ER-raportit voivat lisätä liiketoimintatietoja ylä-ja alatunnisteisiin ja määrittää, missä sivunvaihdot suoritetaan. Näin raportit voivat tukea luotujen asiakirjojen sivujen staattisia ylä- ja alaosia. Ne voivat myös tukevat asiakirjojen lakisääteisten vaatimusten mukaista sivutusta.                                                                                                                                                                                                             |
| Sähköisen raportoinnin ER-raporttien konfigurointi siten, että tuloste lähetetään sähköpostiviestinä ja liiketoimintatietoja ja ER-logiikkaa (lausekkeet) käytetään suoritushetkellä sähköpostiosoitteen määrittämiseen.                                                                                                    | Aiemmin ER-kohteen konfiguroinnissa voitiin määrittää tulosteen vastaanottajan sähköpostiosoite suunnittelun aikana. Voit nyt määrittää lausekkeen ER-muodossa. Lauseke voidaan valita kohteeseen sähköpostiosoitteen lähteeksi kuhunkin muotokonfiguraatioon ja kuhunkin tulosteen komponenttiin (kansioon tai tiedostoon) erikseen. Siksi suoritettaessa ER-raporttia kukin luotava tiedosto voidaan lähettää eri vastaanottajalle ja sähköpostiosoite voidaan määrittää ER-logiikan ja liiketoimintatietojen perusteella. |
| ER-raporttien kohteen määrittäminen siten, että tuloste lähetetään Microsoft SharePoint-kansioon joko uudelleennimettynä tiedostona tai nykyisen tiedoston uutena versiona ja siten, että liiketoimintatietoja voidaan käyttää Microsoft Power BI -kehikossa raporttina tai tietojoukkona.                 | Määrittäessäsi ER-raportteja voi nyt helposti (ilman koodausta) valmistella pyydetyt liiketoimintatiedot siten, että niitä voidaan käyttää Power BI -kehikosta. Suoritettaessa näitä ER-raportteja voi antaa Power BI -kehikon jossa on tarvittavat liiketoimintatiedot ja/tai Excel-raportit, jotka ovat käytettävissä. Jos ajoitat raportin toimimaan toistuvassa tilassa, voit määrittää ajoitetun liiketoimintatietojen lähetyksen Dynamics 365 for Operationsista Power BI:hin tukemaan Power BI -pohjaisten raporttien päivitettyä lähetysaikataulua.                             |
| ER-raporttien määrittäminen käytettäviksi osana sähköistä tiedostoa, joka on luotu aiemmin tietolähteeksi asiakirjan luomista varten.                                                                                                                                             | Voit määrittää ER-raportteja, jotka luovat tulosteen tekstimuodossa asiakirjan rivien inventointia varten. Näitä tietoja voidaan sitten käyttää asiakirjan muissa osissa ja luoda uusia rivejä, jotka sisältävät yhteenvetotietoja. Yhteenvetotiedot (summat ja numerot) voidaan laskea ja tulostaa sähköisiksi tiedostoiksi, jotka luodaan ilman muita tietojen muuntamista. Toiminto parantaa raportin suorituksen suorituskykyä ja helpottaa määritetyn ER-muodon tulevaa ylläpitoa.    |
| ER-raporttien määrittäminen tiedostotunnisteen määrittämiseksi sähköisiin asiakirjoihin, jotka on luotu tekstimuodossa.                                                                                                                                                                                 | Voit määrittää ER-raportteja luomaan tulosteet tekstimuodossa, jotta ne voidaan tallentaa tiedostona, jolla on tietty tunniste. Voit määrittää .txt-oletustunnisteen lisäksi esimerkiksi .csv- ja .prn-tiedostotunnisteet tiedostomuodon määrityksen mukaisesti.                                                                                                                                                                                                                                                                             |
| ER-mallin erikoisversioon perustuvien uusien ER-raporttien luominen                                                                                                                                                                                                                          | Aiemmin luotaessa uutta ER-muotoa ainoastaan valitun ER-malliin uusinta versiota voitiin käyttää tiedostomuodon tietolähteenä. Voit valita minkä tahansa käytettävissä olevan valitun ER-mallin version. Tämän ominaisuuden avulla voit ylläpitää kuluvan vuoden ER-raportteja ja suunnitella uuden ER-mallin version samanaikaisesti seuraavaa vuotta varten.                                                                                                                                                                                          |
| Tietolähteiden ja muotojen/mallien haku tekstin tai valitun tiedon perusteella yhdellä napautuksella. Pohjustusristiriitojen ja konfiguraatioiden välisten ristiriitojen ratkaiseminen ennakoivasti ER-raporttien määrittäminen luomaan useita vahvistusviestejä havaituista virheistä, kunnes raportin suoritus pysäytetään. | Useat ER-kehikon käyttäjäkokemuksen (UX) parannukset auttavat käyttäjiä käyttämään sähköistä raportointia tehokkaasti ja helposti.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **ER**-työtilan näyttäminen Power BI -raporteissa                                                                                                                                                                                                                                                      | Käyttäjät voivat määrittää **ER-työtila**-sivun sisältämään uusia valikkovaihtoehtoja ja tapahtumaruutua, jotka suorittaa virtaa Power BI -pohjaisia raportteja.                                                                                                                                                                                                                                                                                                                                                                                                                       |

## <a name="payroll"></a>Palkanlaskenta
<table>




<thead>
<tr class="header">
<th>Mitä voit tehdä</th>
<th>Miksi tämä on tärkeää</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Maksutietueiden ja palkanlaskennan prosessien konfigurointi toiminnolla, joka vastaa Microsoft Dynamics AX 2012 R3:n <strong>Palkanlaskenta</strong>-moduulin toimintoa</td>
<td>Voit määrittää ja käsitellä Yhdysvaltojen palkanlaskennan käyttämällä ominaisuusjoukkoa, joka vastaa AX 2012 R3: n ominaisuusjoukko-toimintoa.
<ul>
<li>Voi määrittää maksujaksot ja maksukaudet, työjaksot ja työkaudet, ansiokoodit ja ansiokoodiryhmät, aikataulut, lomatyypit ja jaksotussuunnitelmat.</li>
<li>Voit myös määrittää toimien ja työntekijöidenetujen ja verojen pakolliset vähennykset ja palkanlaskentatiedot raportointia ja analysointia varten.</li>
<li>Voit määrittää ja hallita palkanpidätysten ja verojen vähennyksiä ja niihin liittyviä hallinnollisia kuluja.</li>
</ul></td>
</tr>
<tr class="even">
<td>Maksukauden prosessin valvominen ja käsittely käyttämällä uutta <strong>Palkanlaskennan hallinta </strong> -työtilaa.</td>
<td>Voit nyt helposti valvoa palkanlaskennan käsittelyä. Palkanlaskentakoordinaattorit voivat nopeasti nähdä ansio- ja maksuilmoituksia, jotka edellyttävät toimia, jotta maksuajo on valmis ja tarkka. <strong>Palkanlaskennan hallinta </strong>-työtilan avulla käyttäjät voivat seurata sekä suorittaa prosessit päästä päähän yhdestä työtilasta.</td>
</tr>
<tr class="odd">
<td>Palkanlaskennan Positive pay -tiedoston luominen</td>
<td>Maksuliikenteen hallinnan Positive Pay -toiminnoille on uusi tunniste palkanlaskennan maksua varten. Erilliset valikkovaihtoehdot on lisätty ydinprosessiin, jotta palkanlaskentakohtainen konfigurointi on mahdollinen. Toiminto on samanlainen kuin Positive pay -ydintoiminto, joka julkaistiin Microsoft Dynamics AX-sovellusversion 7.0.1 kanssa (toukokuu 2016). Tunnisteen ansiosta palkanlaskentatiedot on kokonaan eristetty muista Positive pay -tapahtumista. Eristämisen ansiosta voidaan taata, että ainoastaan Palkanlaskenta-käyttäjät voivat käyttää ja näkevät palkanlaskentaan liittyvät tiedot.</td>
</tr>
<tr class="even">
<td>Tulojen laskelmarivien tuominen ulkoisesta lähteestä käyttämällä uutta ansioilmoitusrivi- tietoyksikköä</td>
<td>Tärkeän uuden tietoyksikön avulla voidaan ulkoinen aikajärjestelmä ja ansiolaskentajärjestelmät integroida. Tietoyksikkö tuo ansioiden ilmoitusrivit ja suorittaa saman oletuslogiikan, jonka käyttäjä antoi suoraan ansioilmoitukseen. Tuonnin jälkeen rivit liitetään automaattisesti haluamaasi ansioilmoitus-asiakirjaan. Jos haluamasi ansioilmoitus-asiakirjaa ei ole, asiakirja luodaan automaattisesti.</td>
</tr>
</tbody>
</table>

## <a name="planning-and-scheduling"></a>Suunnittelu ja ajoitus
| Mitä voit tehdä                                                                                                                                                                                                      | Miksi tämä on tärkeää                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Määritä tilauksen oletusasetukset myynneille ja ostoille, jotka perustuvat tuotteen päätietueessa käytössä oleviin aktiivisiin tuotedimensioihin. Näin voit määrittää tilauksen oletusasetukset varastointiyksikölle (SKU) tai osittaiselle varastointiyksikölle. | Voit määrittää tilauksen oletusasetukset, joita käytetään tuotedimensioon tai tuotedimensioyhdistelmään. **Esimerkki** Myyt tuotteen, jonka nimi on Polo-t-paita. Tuotteesta on saatavana kaksi väriä: vihreä ja sininen. Siitä on saatavana myös kaksi kokovaihtoehtoa: S ja M. Polo-t-paidan aktiiviset tuotedimensiot ovat väri ja koko. Voit estää kaikkien vihreiden Polo-t-paitojen ostot riippumatta koosta. |

## <a name="product-master-data"></a>Päätuotetiedot
<table>




<thead>
<tr class="header">
<th>Mitä voit tehdä</th>
<th>Miksi tämä on tärkeää</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tilauksen oletusasetusten ja toimipaikkakohtaisten tilausasetusten määrittäminen samanaikaisesti samalla sivulla</td>
<td>Tämän toiminnon ansiosta saadaan parempi yleiskuva nimikkeen asetuksista.</td>
</tr>
<tr class="even">
<td>Tuotevarianttinimikkeistön luominen</td>
<td>Voit sisällyttää elementtejä, kuten tuotedimensiot, määritteet ja ominaisuudet, tuotevariantin numeroihin. Kun luot myyntitilauksen tai ostotilauksen, löydät nopeasti tietyt tuotevariantit.</td>
</tr>
<tr class="odd">
<td>Tuotteiden ja tuotevarianttien haku myynti- ja ostoskenaarioista</td>
<td>Myyntirivillä tai tilausrivejä luotaessa voit etsiä tuotteita käyttämällä tuotedimensioita ja mitä tahansa tuotenumeroita lukuun ottamatta yleisiä kauppanimikenumeroita (GTIN) ja viivakoodeja. Haku on tekstihaku, joka korvaa aiemmin "alkaa"-haun, jota käytetään myynnin ja ostojen hakuluettelosta. Tämän ominaisuuden avulla voit etsiä tuoteryhmän, jolla on samanlaisia ominaisuuksia tai yhden tuotteen, jolla on yksilöivä ominaisuuksia. Voit ottaa toiminnon käyttöön valitsemalla <strong>Ota tuotteiden haku käyttöön</strong> -parametrin <strong>Hakuparametrit</strong>-sivulla.</td>
</tr>
<tr class="even">
<td>Tuotemallin muuttujan määrittäminen suoraan luodessasi myynti- tai ostotapahtuman. Vaihtoehtoisesti voit valita asianmukaisen dimensioyhdistelmien luettelon.</td>
<td>Tämä toiminto on tarkoitettu tuottavuuden parantamiseksi. <strong>Esimerkki</strong> Myyt tuotteen, jonka nimi on Polo-t-paita. Tuotteesta on saatavana kaksi väriä: vihreä ja sininen. Siitä on saatavana myös kaksi kokovaihtoehtoa: S ja M. Polo-t-paidan aktiiviset tuotedimensiot ovat väri ja koko. Kun syötät myyntiriville Polo t-paidan, jonka väri on vihreä ja koko S, et tarvitse kirjoittaa tietoja <strong>Nimiketunnus</strong>-, <strong>Väri</strong>- ja <strong>Koko</strong>-kenttiin. Voit luoda rivin noudattamalla jotain seuraavista:
<ul>
<li>Valitse <strong>Nimiketunnus</strong> -kenttä, anna tuotevariantin numero, värin tai koon arvo. Haun avulla voit etsiä myytävän variantin ja luoda myyntirivin.</li>
<li>Syötä <strong>Nimiketunnus</strong>-kenttään nimikkeen numero. Siirry mihin tahansa tuotedimensio-kenttään. <strong>tuotedimensio</strong>-hakuun tulevat kaikki vapautetut dimensioyhdistelmät, jotka sopivat Polo t-paitaan. Voit valita kerralla tuotevariantin, jonka haluat myydä.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Määrittää, näytetäänkö tuotenumero tapahtumasivuilla</td>
<td>Tapahtumasivuilla, kuten myyntitilaukset ja ostotilaukset, näkyvät vain <strong>nimiketunnus</strong>- ja <strong>tuotenimi</strong>-kentät. Voit tarkastella <strong>tuotenumero</strong>-kenttää valitsemalla <strong>Näytä tuotenumero lomakkeissa</strong>-parametrin kohdassa <strong>tuotetietojen hallintaparametrit</strong>.</td>
</tr>
</tbody>
</table>

## <a name="project-management-and-accounting"></a>Projektinhallinta ja kirjanpito
| Mitä voit tehdä                                                                                                           | Miksi tämä on tärkeää                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Myöhäinen-valinnan käyttö kirjattaessa erän laskuehdotukset eränä                                                            | Projektin kirjanpitäjä voi määrittää erätyön poimimaan automaattisesti laskuehdotukset kirjaukseen, jos, ehdotukset täyttävät erätyölle määritetyt ehdot. Tämä toiminto parantaa automaattista laskun kirjaamista, koska erätyö voidaan suorittaa jatkuvasti ja noutaa ehdotukset kirjausta varten automaattisesti. |
| Power BI -työpöydän analyysin luominen                                                                                     | Liiketoimintatietojen (BI) sisällön projektikohtaiset ja resurssiin liittyvät tiedot voidaan luoda helposti Power BI -työpöydällä.                                                                                                                                                                                                       |
| Ostotilauksen ennakkomaksujen käyttö ja sisällyttäminen oikein projektien arviointiprosessiin                               | Projektin ostotilausten ennakkomaksut on käsiteltävä ennen maksujen lähettämistä toimittajille. Näiden ennakkomaksulaskut näkyvät projektin arvio/kirjausprosessissa **kiinteähintainen**-projektityypissä.                                                                                           |
| Kustannusten ja tuoton arvioiden ja nimiketarpeiden käyttö ja hallinta suoraan työrakenteesta | Voit hallita määritetyn WBS-tehtävän kustannusarvioita, tuottoarvioita ja nimiketarpeita tehtävän tiedot-valintaikkunassa WBS-suunnittelunäkymässä.                                                                                                                                                                 |
| Rahoituslähteen valinta maksukirjauskansioissa                                                                                    | Jos projektisopimuksella on useita rahoituslähteitä, voit valita tietyn rahoituslähteen, kun maksut kirjataan. Jos et valitse tiettyä rahoituslähdettä, rahoitussääntöjä, jotka on määritetty sopimuksessa, käytetään maksun kohdistukseen.                                                                   |
| Projektilaskelmien avaaminen Excelissä                                                                                         | Kirjanpitopäivitysten ja budjettipäivitysten uusien tietoyksiköiden avulla voit avata projektiraporttitiedot Excelissä ja luoda analyysin Exceliin-toiminnon avulla.                                                                                                                                                                           |
| Ainoastaan yhden määritysavaimen käyttäminen projektinhallinnan ja kirjanpidon (PMA) toimintoja käytettäessä                       | Projekteihin liittyvät konfigurointiavaimet on korvattu yhdellä projektin konfigurointiavaimella, joka ottaa käyttöön PMA-toiminnot.                                                                                                                                                                                                       |

## <a name="retail-and-commerce"></a>Vähittäismyynti ja kauppa
### <a name="advanced-warehouse-management-in-a-retail-store"></a>Varastonhallinnan lisätoiminnot vähittäismyymälässä

Vähittäismyyjät voivat käyttää varastonhallinnan (WHS) lisätoimintoja varastoissaan ja tehdä myyntipisteen (POS) toimintojen tarvitsemat päivitykset nykyiseen myyntipisteeseen. Kannettavan ratkaisun prosessit toimivat myymälässä ja varastoissa. Kaikki nykyisen Retail-myymälävaraston prosessit ja mikä tahansa myyntipisteen prosessit, jotka luovat tai päivittävät varastotapahtumia, päivitetään niin, että ne käyttävät varastonhallintaa käyttävien varastojen erityisvaatimuksia.

| Mitä voit tehdä                                                                       | Miksi tämä on tärkeää                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Käytettävissä olevan varaston haku myyntipisteen avulla varastonhallintaa käyttävissä myymälöissä.                     | Kun teet hakua varastosta, prosessin tulee toimia samalla tavalla kuin aiemmin. Haun pitää näyttää kaikki käytettävissä olevat määrät varaston tasolla eikä ottaa huomioon sijaintia, varaston tilaa tai varastorekisterinumeron pituutta. |
| Tuotteen vastaanoton käsittely myyntipisteen avulla varastonhallintaa käyttävään myymälään tehtävää siirtotilausta varten | Saat siirtotilaukset myyntipisteessä varastonhallintaa käyttävään myymälään ja nimikkeille. Käyttäjän tulisi valita vastaanottosijainnit ja pitäisi pystyä antamaan varastorekisterinumeron tunnus vastaanottorivien automaattista täyttöä varten.    |
| Tuotteen vastaanoton käsittely myyntipisteen avulla varastonhallintaa käyttävään myymälään tehtävää ostotilausta varten | Saat ostotilaukset myyntipisteessä varastonhallintaa käyttävään myymälään ja nimikkeille. Käyttäjän tulisi valita vastaanottosijainnit ja pitäisi pystyä antamaan varastorekisterinumeron tunnus vastaanottorivien automaattista täyttöä varten.    |
| Käytä myyntipisteitä tuotteiden lähetyksen prosessointiin varastonhallintaa käyttävästä myymälästä.               | Voit rekisteröidä siirrot myyntipisteessä varastonhallintaa käyttävään myymälään ja nimikkeille. Käyttäjällä on mahdollisuus valita sijainnit, josta tilaus lähetetään, varaston tilan luodaan automaattisesti ja varastorekisterinumerot ohitetaan.         |

### <a name="enable-seamless-omni-channel-commerce"></a>Yhtenäisen monikanavaisen kaupan mahdollistaminen

Yhtenäinen monikanavainen kauppa viittaa tilausten käsittelemiseen ja hallintaan kivijalkakaupoissa, online-kaupoissa, puhelinkeskuksissa ja mobiilikaupankäynnissä. Tähän versioon on tehty seuraavat sijoitukset tällä alueella:

-   Sähköisen kaupankäynnin verkkojulkisivuja koskevat parannukset
-   Uusi kuluttajille suunnattu mobiilisovellus, joka mahdollistaa tuotteen etsimisen, tilinhallinnan ja verkko-ostokset

| Mitä voit tehdä                                                                                                                                                                                                                                                                   | Miksi tämä on tärkeää                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kuluttajat: Kuluttajille suunnatun mobiilisovelluksen nykyinen versio mahdollistaa Seuraavat ominaisuudet: tuotehaku, luokkien selaustoiminto, ostoskoriin lisääminen ja siirtyminen kassalle vieraana. Vähittäismyyjät voivat myös käyttää yrityksen tuotemerkkiä sovelluksessa ja luoda tuotepaketin Android- ja iOS-sovelluskauppoihin. | Vähittäismyyjät voivat helposti luoda asiakkaille suunnatun sovelluksen, jonka avulla asiakkaat voivat selata ja etsiä tuotteita ja hankkia tuotteet vieraana mobiililaitteellaan.                      |
| Asiakkaan toivomuslistat verkkokauppajulkisivuille                                                                                                                                                                                                                             | Riippumattomat toimittajat voivat käyttää toivomuslistojen hallintaa siten, että käyttäjät voivat luoda ja hallita useita toivomuslistoja omassa verkkokauppajulkisivussaan ja tarkastella/käyttää listoja myyntipisteessään. |
| Asynkroninen asiakkaan luominen verkkokauppajulkisivujen kautta                                                                                                                                                                                                                  | Riippumattomat ohjelmistotoimittajat voivat nyt luoda asiakastilejä myös silloin, kun Commerce Data Exchange: Real-time Service ei ole käytettävissä.                                                                        |
| Kanavatuotteiden julkaiseminen Retail Serveristä kolmannen osapuolen verkkokauppajulkisivulle                                                                                                                                                                                                           | Retail Server tukee palvelulta palvelulle -todennusta. Itsenäiset ohjelmiston myyjät (ISV) voivat hyödyntää kanavan tuotteiden julkaisemista Retail Serveriltä kolmannen osapuolen verkkokauppajulkisivuille.               |

### <a name="extensibility"></a>Laajennettavuus

-   Commerce runtime -projektit on eristetty Retail SDK:sta.
-   Entistä helpompi käyttöönotto ja ylläpito Microsoft-komponenttipakettien ja ohjelmistotoimittajan pakettien ansiosta myyntipisteille, Retail Serverille, tietokannolle, maksuille ja laiteasemille.

| Mitä voit tehdä                                                                                                                 | Miksi tämä on tärkeää                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CRT/Retail-Server: vähittäismyyjät tai itsenäiset ohjelmiston myyjät (ISV) voivat laajentaa CRT:tä laajennuslinkkien avulla. Sisäisten koodien muutokset eivät ole tuettuja enää. | Jatkuvan integroinnin ja jatkuvan käyttöönoton mahdollistamiseksi sisäiset koodien muutokset on kokonaan estettävä. Tukee myös korjaustiedostojen helppoa käyttöä ilman CRT-komponenttien koodin yhdistämistä ja käyttöönottoa. |

### <a name="personalized-product-recommendations"></a>Mukautetut tuotesuositukset

| Mitä voit tehdä                                                                                                                                                                                                                                                                        | Miksi tämä on tärkeää                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tarkastele mukautettuja tuotesuosituksia usealla myyntipisteen kosketuspisteellä määrittääksesi, mistä asiakas haluaa ostohistorian, toiveluettelon ja muiden asiakkaiden verkko- ja kivijalkakauppaostosten perusteella. | Mukautetut tuotesuositukset auttavat kauppiaita, joilla on suuri tuotevalikoima, auttamaan asiakkaitaan tuotteiden löytämisessä ja antavat myyntiedustajille mahdolliset älykkäämpään myyntityöhön. Esittämällä tuotesuosituksia, jotka on kohdistettu asiakkaan kiinnostuksen kohteisiin, kauppiaat parantaa myyntiään ja tehostaa asiakaspidätystä. Microsoft Dynamics 365 for Retailin tuotesuositukset toimivat kognitiivisten palveluiden ja Microsoft Azuren koneoppimisen avulla. |

### <a name="pos-task-recorder"></a>Myyntipistetehtävän tallennus

| Mitä voit tehdä                                                                                                                                                                                                  | Miksi tämä on tärkeää                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vähittäismyyjät voivat käyttää myyntipisteen tehtävän tallennusta tuottamaan koulutusmateriaalia, liiketoimintaprosessien mallintajan (BPM) kaavioita, ja luomaan ohjesisältöä tuottavuuden parantamiseksi ja sovellusten parempaa analysointia ja suunnittelua varten. | Jatkuvan integroinnin ja jatkuvan käyttöönoton mahdollistamiseksi sisäiset muutokset on kokonaan estettävä. Tukee myös korjaustiedostojen helppoa käyttöä ilman CRT-komponenttien koodin yhdistämistä ja käyttöönottoa. |
| Käytönaikainen tuki myyntipisteissä                                                                                                                                                                                           | Kassanhoitaja/esimies saa reaaliaikaista tukea myyntipisteestä liiketoimintaprosessia varten ilman kontekstin vaihtoa.                                                                                                           |

### <a name="store-system-providing-a-seamless-on-premises-store-experience"></a>Myymäläjärjestelmä: mahdollistaa yhtenäisen paikallisen myymäläkokemuksen

Myymäläjärjestelmä on käyttöönoton valinta jälleenmyyjille. Sen avulla voidaan suorittaa sarja myymälän toimintoja paikallisessa myymälässä, Microsoftin julkisessa pilvessä tai asiakkaan omassa yksityisessä pilvessä. Tämän version laajuus koskee vain myymälöitä. Tukeaksemme paremmin ympäristöjä, joissa on hidas ja epäluotettava verkkoyhteys meidän on tarjottava vaihtoehto vähittäismyyjille kanavatietokannan ja Retail Serverin käyttöön myymälässä. He voivat jatkaa ydinliiketoimintaansa silloinkin, kun yhteyttä pääkonttoriin ei ole. Tietopisteiden perusteella, joihin sisältyi suunnitteluryhmän keskusteluita, asiakaskyselyn tuloksia ja kilpailijan analyyseja, määritimme seuraavan ratkaisulaajuuden parhaiten soveltuvaksi kohdeasiakkaille:

-   Omatoiminen ohjelmistopaketti on käytettävissä myymäläjärjestelmässä.
-   Perusasennus on yhtä käyttöönottoa varten, mutta mukautettu käyttöönotto sallitaan.
-   Mahdollistaa helpon käyttöönoton / itse tehtävän huollon.
-   Retail Server ja myymälän tietokanta ovat myymälässä ovat Async Client -palvelun kanssa.
-   Myymälän Retail Serverillä on suora yhteys pääkonttorin Application Object Serveriin (AOS) myymäläjärjestelmää varten.
-   Tukee päätteiden välistä yhteysskenaarioita, jos yhteyttä pääkonttoriin ei ole.
-   Retail Modern POS- ja Cloud POS-sovelluksella on jatkuva yhteys myymälän Retail Serveriin.
-   Tukee Retail Modern POS- ja Cloud POS -sovellusta, jos yhteyttä pääkonttoriin ei ole.
-   Tukee Retail Modern POS -sovelluksen omaa offline-tietokantaa (joka on eristetty jokaisesta Retail Modern POS -instanssista), jos yhteyttä pääkonttoriin ei ole.
-   Todennus perustuu palvelulta palvelulle -todennukseen ainoastaan myymäläjärjestelmässä.
-   Reaaliaikaisia huoltokutsuja ei tueta, jos Internet-yhteyttä ei ole.
-   Retail Modern POS -sovelluksen suoraa tietokantayhteyttä kanavatietokantaan ei tueta.
-   Mahdollistaa telemetrian/valvonnan

| Mitä voit tehdä                                                                                                                                       | Miksi tämä on tärkeää                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Jälleenmyyjä lataa myymäläjärjestelmän omatoimisen asennusohjelman kanavatietokantasivulta Dynamics AX -pääkonttorista ja lataa määritystiedoston.   | Jälleenmyyjä voi ladata omatoimisen ohjelmistopaketin sujuvasti.                                          |
| Jälleenmyyjä asentaa myymäläjärjestelmän omatoimisen asennusohjelman avulla.                                                                                 | Jälleenmyyjä voi asentaa myymäläjärjestelmän omatoimisen ohjelmistopaketin avulla.                                |
| IT-päällikkö määrittää myymäläjärjestelmän Dynamics 365 for Operations -järjestelmään (kanavatietokanta, kanavaprofiili, myymälä ja käyttöönotettava paketti).             | IT-päällikkö voi määrittää myymäläjärjestelmän helposti ja tehokkaasti.                                       |
| Jälleenmyyjä käyttää Retail Modern POS -sovellusta paikallisessa myymälässä ja voi tehdä reaaliaikaista toimintoja, kuten kirjoittaa lahjakortteja, kun yhteys on käytettävissä. | Jälleenmyyjä voi suorittaa reaaliaikaisia toimenpiteitä myymäläjärjestelmästä, kun yhteys on käytettävissä.                |
| Jälleenmyyjä voi synkronoida tietoja paikallisesta myymäläjärjestelmästä pääkonttoriin, kun yhteys on käytettävissä.                                                      | Jälleenmyyjä voi synkronoida toimenpiteitä myymäläjärjestelmästä/-järjestelmään, kun yhteys on käytettävissä.                              |
| Jälleenmyyjällä voi olla suojattu yhteys paikallisen myymäläjärjestelmän ja pääkonttorin välillä.                                                                 | Jälleenmyyjä voi muodostaa suojatun yhteyden myymäläjärjestelmästä, kun yhteys on käytettävissä.                     |
| IT-päällikkö ja Microsoft Operations voivat valvoa ja raportoida paikalliseen myymäläjärjestelmään (diagnostiikan ja raportoinnin muutoksia).                   | IT-päällikkö ja Microsoft Operations voi valvoa myymäläjärjestelmää turvallisesti ja määrittää viat tehokkaasti. |

### <a name="universal-windows-platform-app-for-retail-modern-pos"></a>Universaalin Windows -ympäristön sovellukset Retail Modern POS -sovellukselle

Tällä hetkellä Retail Modern POS on käytettävissä vain Windows 8.1 -sovelluksena pöytätietokoneille ja tableteille sekä Cloud POS -pilvimyyntipisteversiona pöytätietokoneen tai tabletin selaimeen. Retail Moderns POS muunnetaan tässä tuotejulkaisussa Universal Windows Platform (UWP) -sovellukseksi. Muutoksen ansiosta Retail Modern POS toimii kaikissa Windows 10 -laitteissa (pöytätietokoneessa, tabletissa tai puhelimessa) ja voi vaihtaa näkymää Continuumia tukevien laitteiden kanssa.

| Mitä voit tehdä                                                   | Miksi tämä on tärkeää                                                                                     |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Tärkeän myyntipistetoiminnon käyttöönotto pienikokoisissa SFF-laitteissa | Retail POS -toiminto on käytettävissä puhelimissa ja muissa pienikokoisissa SFF-laitteissa, joissa on Windows 10. |

## <a name="supply-chain-management"></a>Toimitusketjun hallinta
### <a name="consignment-inventory"></a>Tavaralähetysvarasto

| Mitä voit tehdä                                                                                                                                                                | Miksi tämä on tärkeää                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Toimittajana voi varastoida raaka-aineita asiakkaan varastossa. Asiakkaana voit lykätä todellisen oston kunnes raaka-aineita tarvitaan tuotannossa. | Raaka-aineiden varastointi voi aiheuttaa suuria kustannuksia. Käyttämällä tavaralähetysvarastoa toimittaja varastoi raaka-aineet asiakkaan varastoon. Asiakas voit lykätä todellisen oston kunnes raaka-aineita tarvitaan tuotannossa. Raaka-aineet tilataan ja vastaanotetaan tavaralähetysvaraston täydennystilauksella. Täydennystilaus tallentaa fyysiset tapahtumat mutta ei vaikuta kirjanpitoon. Voit erottaa asiakkaan omistamat varastonimikkeet toimittajan omistamista varastonimikkeistä, käyttämällä omistaja-varastodimensiota. Varaston omistajuuden vaihtumista käsittelee kirjauskansion prosessi, joka käsittelee raaka-aineiden omistajuuden siirtoa toimittajan varastosta asiakkaan varastoon. Tämä prosessi käynnistää tuotteen ostotilauksen ja vastaanoton luomisen. **Huomautus:** Toiminto on rajoitettu tuotannon raaka-aineiden saapuviin lähetyksiin. Sitä ei ole integroitu varastonhallintaan (WHS) eikä kuljetustenhallintaan (TMS). |
| Toimittaja saa tiedon luovutetun varaston määrästä, joka siirretään asiakkaalle                                                                      | Voidakseen laskuttaa asiakasta toimittaja tarvitsee tiedot raaka-aineista, jotka on ostettu luovutetusta varastosta, ja ostopäivämäärän. Toimittaja voi myös valvoa asiakkaan toimipaikalla käytettävissä olevaa varastoa toimittajayhteistyöliittymällä.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Toimittajan omistaman varaston siirtäminen siirtokirjauskansion avulla                                                                                                                       | Jotta toimittajan omistamaa varastoa voidaan seurata, fyysinen sijainti järjestelmässä pitää pystyä kirjaamaan. Käyttämällä siirtokirjauskansiota voit tallentaa varaston fyysisen siirtämisen, kuten siirto varastopaikasta toiseen varastopaikkaan.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Toimittajan omistaman varaston oikaisu siirtokirjauskansion avulla                                                                                                                     | On tärkeää pitää järjestelmän käytettävissä oleva varasto synkronoituna todellinen fyysisen varaston kanssa. Toimittajan omistama varasto voidaan oikaista käyttämällä inventointiprosesseja, kuten määrän muutos ja inventoinnin kirjauskansio.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Lisätietoja Dynamics 365 for Operations -järjestelmän tavaralähetyksen tuesta                                                                                                         | Lisätietoja tavaralähetysprosessien tuesta on kohdassa [Tavaralähetys](../../supply-chain/inventory/consignment.md), [Tavaralähetyksen määrittäminen](../../supply-chain/inventory/set-up-consignment.md), [Luo tavaralähetyksen täydennystilaus (tehtäväopas)](../../supply-chain/inventory/tasks/create-consignment-replenishment-order.md) ja [Tavaralähetysvaraston omistajuuden muuttaminen tuotannon kysynnän perusteella (tehtäväopas)](../../supply-chain/inventory/tasks/change-ownership-consignment.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

### <a name="vendor-collaboration-previously-known-as-the-vendor-portal"></a>Toimittajayhteistyö (aiemmin Toimittajaportaali)

| Mitä voit tehdä                                                                      | Miksi tämä on tärkeää                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Toimittajat voivat vastata kullekin ostotilausriville ja ehdottaa muutoksia.           | Joissakin tapauksissa toimittajat haluavat hyväksyä joitakin ostotilausrivejä mutta hylätä joitakin niistä. Toimittajat voivat nyt hallita ostotilausrivejä yksitellen. Kunkin rivi voi olla hylätty, hyväksytty tai hyväksytty muutosten kera. Esimerkiksi toimittaja voi muuttaa toimituspäivämäärä, jakaa toimituksen ja määrän tai ehdottaa vaihtoehtoista nimikettä.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Toimittajat voivat ylläpitää yhteyshenkilöiden tietoja.                                 | Toimittajat voivat ylläpitää oman yrityksen yhteystietoja. Näitä tietoja ovat nimet, sähköpostiosoitteet ja puhelinnumerot. Tämän toiminnon käyttöoikeus myönnetään tarkoituksenmukaisen käyttöoikeusroolin kautta.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Voit jakaa toimittajien kanssa asiakirjat, jotka liittyvät ostotilauksiin.                    | Kun asiakirja on jaettava toimittajan kanssa, kuten vaatimuksia koskeva asiakirja, on kätevää linkittää asiakirja ostotilaukseen. Toimittajan voi jakaa huomautukset ja liitteet asiakkaan kanssa linkittämällä asiakirjan hänen ostotilaukseen tekemään vastaukseen. Tiedostonhallinta on pohjana oleva tukirakenne, ja toimittajien kanssa voidaan jakaa vain huomautukset ja liitteet, jotka luokitellaan "ulkoisiksi".                                                                                                                                                                                                                                                                                                                              |
| Käyttöoikeuksien antaminen uusille toimittajakäyttäjille                                                          | Jos toimittaja käyttää toimittajayhteistyöliittymää, heillä on käytössään yhtenäinen uusien käyttäjätilien pyyntötapa, kun uudet yhteyshenkilöt edellyttävät toimittajayhteistyön käyttöoikeuksia. Hankintojen asiantuntijat voivat lähettää yhteyshenkilön käyttäjätilipyynnön toimittajan organisaatiolle. Toimittajan yhteyshenkilö, joka on jo toimittajayhteistyön käyttäjä, voi myös lähettää tämäntyyppisen pyynnön. Pyyntö luo lopulta Dynamics 365 for Operations -järjestelmään uuden käyttäjän, jolla on toimittajakohtaiset käyttöoikeusroolit. Se mahdollistaa myös pyynnön Microsoft Azure B2B -yritysportaalille valmistella käyttäjälle uusi Azure Active Directory (Azure AD) -käyttäjätili. Toimittajat voivat myös pyytää tiettyä toimittajan käyttäjätilien poistoa käytöstä tai suojausroolien muokkaamista. |
| Lisätietoja Dynamics 365 for Operations -järjestelmän toimittajayhteistyön tuesta | Lisätietoja toimittajayhteistyöstä on kohdassa [Toimittajayhteistyö ulkoisten toimittajien kanssa](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md), [Toimittajayhteistyö asiakkaiden kanssa](../../supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations.md), [Toimittajayhteistyön käyttäjien hallinta](../../supply-chain/procurement/manage-vendor-collaboration-users.md), [Määritä ja ylläpidä toimittajayhteistyötä](../../supply-chain/procurement/set-up-maintain-vendor-collaboration.md) ja [ Toimittajayhteistyön laskutustyötila](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md).                                                         |

### <a name="intercompany-order-processing"></a>Konsernin sisäisten tilausten käsittely

<table>




<thead>
<tr class="header">
<th>Mitä voit tehdä</th>
<th>Miksi tämä on tärkeää</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Määritä suoraan myyntitilausriveillä, mistä ja miten kysyntä hankitaan. <strong>Esimerkki</strong> Luo myyntitilausrivi ja määritä toimitustyypiksi suoratoimitus. Ensisijainen toimittaja lisätään myyntitilauksen riville hankintapisteenä.</td>
<td>Tilauksen oton työnkulkua on parannettu merkittävästi. Voit nyt määrittää suoraan myyntitilausriveillä, mistä ja miten kysyntä hankitaan. Et tarvitse enää odottaa, kunnes kaikki rivit on lisätty myyntitilaukseen. Myyntitilausrivien uusien asetusten avulla voi määrittää toimitustyypin kun määrität toimittajan. Kun toimittaja liitetään myyntitilausriveihin, tilausketjut luodaan toimittajan toimitusta varten.
<ul>
<li>Toimittaja voi olla konsernin sisäinen toimittaja, joka käyttää sisäistä ostotilausta ja myyntitilausta tai ulkoinen toimittaja, joka käyttää ulkoista ostotilausta.</li>
<li>Toimitustyyppi voi olla <strong>Suoratoimitus</strong> tai <strong>Varasto</strong>. <strong>Varasto</strong>-toimitustyyppi ilmaisee, että toimittajan on toimitettava paikalliseen varastoon ennen asiakkaalle toimittamista.</li>
</ul></td>
</tr>
<tr class="even">
<td>Tilauksen toimituslupauksen luominen myyntitilauksen riveiltä <strong>Esimerkki</strong> Luo myyntitilausrivi, joka hankitaan konsernitoimittajalta. Poistu riviltä. Toimituspäivät lasketaan hankintayrityksen saatavuuden mukaisesti.</td>
<td>Luodessasi uusia hankintatietoja käyttävä myyntitilausrivejä, toimituspäivämäärät lasketaan <strong>Toimituspäivän</strong> tarkistuksen perusteella. Esimerkiksi jos konsernitoimittaja valitaan, saatavuus hankintayrityksessä lasketaan. Tällöin tilausketjut luodaan automaattisesti myyntitilausrivien ohella. Tämän toiminnon avulla taataan, että toimituspäivät tulevat näkyviin hankintayrityksessä siten, että luvattavissa oleva määrä (ATP) profiilit voivat käsitellä odotettuja vaatimuksia suoraan myyntitilauksia luotaessa.</td>
</tr>
<tr class="odd">
<td>Tuotteen saatavuuden tarkistaminen kaikissa hankintasijainneissa ja parhaan hankintavaihtoehdon valinta</td>
<td><strong>Toimitusvaihtoehdot</strong>-sivu on suunniteltu uudelleen ja sisältää nyt kaikki arvokkat tiedot sisäisistä ja ulkoisista toimittajista. Näihin tietoihin kuuluvat hankintavaihtoehdot toimittajan hankintoja varten. Toimitustilaa valittaessa järjestelmä laskee parhaat toimituspäivämäärät. Voit valita suoraan asiakkaan kannattaa parhaan vaihtoehdon ja käyttää sitä jokaiselle myyntitilausriville.</td>
</tr>
</tbody>
</table>

### <a name="warehouse-enhancements-for-high-volume-distribution-centers"></a>Varaston parannukset suurille jakelukeskuksille

| Mitä voit tehdä                                                              | Miksi tämä on tärkeää                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Työn luominen sen jälkeen, kun tavarat on pakattu pakkausasemassa               | Tämä ominaisuus on hyödyllinen manuaalinen pakkaustyön jälkeen odottaville prosesseille (kuten pakkaus kuormalavalle, laaduntarkastus, lähetysten yhdistäminen tai muutokset latauslaitureihin). Uuden **Pakatun kontin keräily** -työtyypin ansiosta voit mallintaa näitä tehtäviä käyttämällä erillisiä työrivejä. Voit nyt mallintaa pakkausasemat ja luoda työn pakkauksen jälkeen. Tämän työn avulla voidaan järjestää pakattujen varastojen siirrot.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Konttien ryhmittäminen pakkausasemalla                                     | Tämän ominaisuuden ansiosta voidaan ryhmitellä useita pakkauksia yhteen konttiin tai pakkausaseman varastorekisterinumeroon. Esimerkiksi sähköisen kaupankäynnin/tukkukaupan toimija voi ryhmitellä esimerkiksi 100 erikseen pakattua pakettia yhteen konttiin (kuten kuormalavaan tai häkkiin). Tämä kontti voidaan siirtää, asettaa väliaikaiseen sijaintiin tai lastata yhden työohjeen kautta, jonka työntekijä luo skannaamalla yhden viivakoodin (varastorekisterinumeron) yhdistetystä kontista. Tämä toiminto minimoi työtapahtumat, jotka tarvitaan pienempien pakattujen konttien siirtoon. Katso lisätietoja kohdasta [Uuden mobiililaitteen valikkovaihtoehdon luominen varastorekisterinumeron yhdistämistä varten (tehtäväopas)](../../supply-chain/warehousing/tasks/create-mobile-device-license-plate-consolidation.md).                                                                                                                                                                                                                                                                                                                                                                                            |
| Pakattujen konttien vapautuskäytännön luominen                               | Kontin vapautuksen käynnistämä työ voidaan luoda automaattisesti tai manuaalisesti. Jos toiminto on automaattinen, työ luodaan suljettaessa kontti käyttämällä sijaintidirektiiviä ja työmallin kehystä. Kun vapautus on manuaalinen, pakkaaja voit päättää, luodaanko työ yhdelle kontille tai konttiryhmälle. Tämä toiminto pienentää riskiä, että suljetut kontit keräillään ja siirretään, ennen kuin ne ovat valmiita siirrettäviksi pakkausasemasta. Sen avulla voidaan myös vapauttaa muita kuin järjestelmän ohjaamia ryhmiä.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Lyhyen keräilyn uudelleenkohdistus                                                   | Tuki on lisätty lyhyttä keräilyprosessia varten, jotta liikekumppani, joka ei voi kerätä tavaroita ja haluaa täyttää tilauksen, kun nimike, jota tarvitaan, on saatavana muussa sijainnissa. Voit käyttää automaattista uudelleenkohdistusprosessia, jossa tavarat noudetaan toisesta sijainnista, jos ne ovat saatavilla, samojen sijaintidirektiivien avulla. Vaihtoehtoisesti manuaalista uudelleenkohdistamista käytettäessä mobiililaite näyttää sijaintiluettelon ja käytettävissä oleva määrän. Varastotyöntekijä voi valita, mistä sijainnista varastoa käytetään. Nämä kaksi menetelmää voidaan määrittää erikseen tai yhdistää yhdeksi komennoksi varastotyöntekijöiden valikkoon. Kun käytetään manuaalista uudelleenkohdistusta, varastotyöntekijä voi valita lyhyen keräilyn nimikkeen useista sijainneista. Lisätietoja on kohdassa [Nimikkeen uudelleenkohdistussääntöjen määrittäminen lyhyttä keräilyä varten (tehtäväopas)](../../supply-chain/warehousing/tasks/set-up-short-picking-item-reallocation.md).                                                                                                                                                                                          |
| Työhön liitetyn varaston siirto                             | Voit nyt tehdä työhön liitetyn varaston siirron. Tämä toiminto voi olla hyödyllinen, jos esimerkiksi työntekijä haluaa vapauttaa tilaa saapuvien laiturilla ja siirtää rekisteröityjä kuormalavoja, jotka odottavat siirtoa toiseen saapuvien nimikkeiden sijaintiin. Lastauslaituri tyhjenee ja voit ottaa vastaan lisäkuorman tuotteita, ja siirretyn varaston tiedot päivittyvät uudella poistotiedolla. Tämän ominaisuuden avulla voidaan myös vapauttaa tilaa keräilysijainneista siirtämällä varastoa, johon on liitetty töitä, ja luoda tilaa täydennystä varten. Sen avulla voit myös siirtää kuorman jostain väliaikaisesta sijainnista toiseen menettämättä lastaustyötä, jotka on luotu. Näin toiminnon avulla voidaan optimoida saapuvien trukkien lastaukseen tarvittava aika. Voit siirtää varaston, joka on varattu myyntitilauksille, siirtotilauksille, siirtotilausten vastaanottokuittauksille ja ostotilauksille. Siirto estetään, jos se voi aiheuttaa rivien katkeamisen. Esimerkiksi jo työrivillä on 100 kpl tiettyä nimikettä, et voi siirtää vain 30 kappaletta nimikettä toiseen sijaintiin. |
| Varastorekisterinumeroiden, joihin on liitetty työtä, yhdistäminen                    | Voit yhdistää varastorekisterinumeroita, joihin on liitetty lähteviä töitä. Esimerkiksi kun keräily on jaettu useiksi työkappaleiksi, voi olla hyödyllistä sallia varastorekisterinumeroiden yhdistäminen, kun ne on toimitettu väliaikaiseen sijaintiin. Varastorekisterinumerot voidaan yhdistää vain, jos ne ovat samassa paikassa, kuuluvat samaan kuormaan ja niillä on samat lähetystiedot.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Täydennykseen liitetyn keräilytyön lukitseminen rivitasolla | Nyt voit lukita työn rivitasolla otsikkotason sijaan, jotta työntekijät voivat täyttää keräilyrivit, joita ei ole lukittu kysynnän täydennyksen mukaan. Tukkukauppias, jolla on suuria myyntitilauksia, tai jälleenmyyjä, jolla on suuria myyntitilauksia tai täydennyssiirtotilauksia, voi sallia keräilytyön aloitettavaksi kaikilla riveillä, joita täydennystyö ei koske. Keräilyn- ja täydennystyö voidaan suorittaa sitten rinnakkain. Tämä toiminto voidaan määrittää niin, että voit valita, lukitaanko työ otsikkotasolla vai rivitasolla. Molempia menetelmiä voidaan käyttää ja luoda menetelmän mukainen työmalli. Työmalliin on määritetty otsikko- tai rivimääritys, mutta voit muuttaa sen suoraan luotuun työhön.                                                                                                                                                                                                                                                                                                                                                                      |
| Työn peruuttaminen mobiililaitteella                                      | Nyt voit peruuttaa työn mobiililaitteella, kysynnän täydennyksellä tai ilman. Aiemmin piti käyttää paikallisa resursseja. Tämä toiminto otetaan käyttöön luomalla mobiilililaite-valikkokohde, joka tilaksi on määritetty  **Epäsuora** ja tehtävän koodiksi määritetty **Peruuta työ**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |

### <a name="warehouse-operation-enhancements"></a>Varaston työvaiheiden parannukset

| Mitä voit tehdä                    | Miksi tämä on tärkeää                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eri konttityyppien mallit   | Voit haluta käyttää eri konttityyppejä varaston optimointiin ja muihin tarkoituksiin. Uudella konttityyppillä on kontin tyyppien fyysiset ominaisuudet. Voit liittää varstorekisterinumeroihin tietyn konttityyppin ja käyttää sijainnin varastointirajaa. Esimerkiksi tämän toiminnon avulla voit määrittää sallitun kuormalavojen määrän (tai muun konttityyppin) tietyssä sijainnissa. Kontin tyypit on myös lisätty yksikön sarjaryhmiin, jotta kontin oletustyypit voidaan lisätä vastaanottoprosessiin. Konttityyppiä voidaan käyttää saapuvien ja lähtevien sijaintidirektiivien yhteydessä. Niitä voidaan myös käytää käytettävissä olevan varaston näkymässä, jotta voit määrittää, kuinka monta konttityyppiä on tällä hetkellä tallenettuna. Lisätietoja on blogikirjoituksessa [Varastonhallintaprosessien edistäminen käyttämällä konttityyppiin liitettyjä varastorekisterinumeroita](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/20/use-of-license-plates-associated-with-a-container-type-to-drive-warehouse-management-processes/). Blogikirjoituksessa kuvataan Microsoft Dynamics AX 2012:en päivitystä, mutta sama tuki on nyt lisätty Dynamics 365 for Operations -järjestelmään.                                                                                                                                                                                                                                                                                                                         |
| Käännettävät lähetykset                 | Varastossa pitää ollaa valmius käsitellä muutoksia myöhässä. Esimerkiksi jotkut tuotteet voivat olla vahingoittuneet eikä niitä voi toimittaa. Asiakas voi myös esittää myöhäisen tilauksen peruutus- tai muutospyynnön. Dynamics 365 for Operations -järjestelmän avulla voit nyt palauttaa lähetyksen. Tämän vuoksi voit peruuttaa pakkausluettelon, niin että voit päivittää siihen oikeat määrät myöhemmin. Vastaavasti saapuvasta tuotevirrasta voit peruuttaa tuotteen vastaanotot siten, että voidaan luoda päivitetyt versiot.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Yhdistetyillä nimikkeillä täytettyjen kuormalavojen käyttö | Voit nyt vastaanottaa ja rekisteröidä "yhdistettyjen nimikkeiden" kuormalavan. Yhdistetyllä kuormalavalla on eri nimikkeitä, joka on koottu yhdestä tai useasta ostotilauksesta tai -riveiltä samalle kuormalavalle. Kaikki rekisteröinnit voidaan koota samaan kohdevarastorekisterinumeroon. Tämä prosessi on käytössä kaikkialla varaston mobiililaitteissa. Esimerkiksi yhdistetty kuormalava saapuu varastoon, vastaanottoassistentti tunnistaa nimikkeet ja määrät ennen kuormalavalla ennen sen siirtoa määrättyyn sijaintiin. Sijoitussijainnit tunnistetaan työmalleista tai sijaintidirektiiveistä. Jos sijoitussijainnit jakautuvat useille nimikkeille, joilla on kiinteät sijainnit, tämä toiminto luo yhtä monta työriviä kuin yhdistetyssä kuormalavassa on on eri nimikkeitä. Tämän ominaisuuden avulla rekisteröinti ja vastaanotettujen yhdistettyjen kuormalavojen sijoittaminen on nopeampaa ja joustavampaa. Lisätietoja on blogikirjoituksessa [Vastaanota ja rekisteröi kuormalava, jossa on yhdistettyjä lähdeasiakirjarivejä, käyttämällä yhtä varastorekisterinumeroa](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/13/receive-and-register-a-pallet-with-mixed-source-document-lines-using-1-license-plate-purchase-order-matching/) ja yhdistetyn kuormalavan tuen tietoja kohdassa [Uusimpien kumulatiivisen päivitysten ilmoittaminen](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/30/whats-new-in-cu11-for-wms-and-tms/). Blogikirjoituksessa kuvataan Microsoft Dynamics AX 2012:en päivitystä, mutta sama tuki on nyt lisätty Dynamics 365 for Operations -järjestelmään. |

### <a name="minor-feature-enhancements-in-supply-chain-management"></a>Pienemmät toimintojen parannukset toimitusketjun hallinnassa

<table>




<thead>
<tr class="header">
<th>Mitä voit tehdä</th>
<th>Miksi tämä on tärkeää</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Uusien tietoyksiköiden käyttäminen tuonnissa ja viennissä</td>
<td>Voit tuoda ja viedä tietoja näiden tietoyksiköiden avulla:
<ul>
<li>Rahtilasku</li>
<li>Käytettävissä oleva yhdistelmä varaston ja varastotilan mukaan</li>
<li>Varaston kulut</li>
<li>Tarjous</li>
</ul></td>
</tr>
<tr class="even">
<td>Vuorovaikutteisten ajoitusskenaarioiden kehittäminen parannetun Gantt-ohjauksen avulla</td>
<td>Parannetulla Gantt-ohjauksella voit kehittää uusia vuorovaikutteisia ajoitusskenaarioita ja toimittaa parannettuja sovellusohjelmaliittymien luetteloja, joiden avulla voidaan mukauttaa tehtävien ulkoasua. Seuraavassa on joitakin uusia sovellusohjelmaliittymiä (API):
<ul>
<li>Tehtävien pystysuorat vedä ja pudota -toiminnot</li>
<li>Lisää tai poista tehtäviä</li>
<li>Varattu-kausien esikatselu yhteenvetopalkissa</li>
<li>Tehtävän reunan värin ja tyylin muuttaminen</li>
<li>Taulukon tekstin värin, tyylin ja taustan muuttaminen</li>
</ul></td>
</tr>
<tr class="odd">
<td>Materiaali- ja resurssisuunnittelun parannettu käsittely</td>
<td>Joitain parannuksia on tehty materiaali- ja resurssisuunnitteluun:
<ul>
<li>Toimitusmarginaalia voidaan käsitellä, kun nimike on käytettävissä.</li>
<li>Toimituspäivä voidaan poistaa, kun suunnitellut tilaukset vahvistetaan.</li>
<li>Tilausten valmistumista voidaan priorisoida varmuusvaraston kustannuksella.</li>
<li>Estetään suunniteltujen tilausten ajoitus menneisyyteen.</li>
</ul></td>
</tr>
<tr class="even">
<td>Tuotannon toteutuneen kulutuksen raportointi ja varaston tilan tarkastelu</td>
<td>Voit tarkastella tuotannon toteutunutta kulutusta. Lisäksi voit tarkistaa varaston tilan uudesta <strong>Näytä varaston tila</strong> -valintaruudusta, jotka on lisätty <strong>Siirto</strong>-kohtaan valikkokohdassa <strong>Työn luominen</strong>.</td>
</tr>
<tr class="odd">
<td>Tilavuuspainon laskeminen, jos yrityksesi rahdinkuljettajan kustannukset perustuvat tilavuuspainoon.</td>
<td>Uusi TMS-hinnanlaskenta on lisätty tilavuuspainon laskemista varten.</td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Lisätietoja
--------

[Uudet ja muuttuneet ominaisuudet](whats-new-changed.md)




