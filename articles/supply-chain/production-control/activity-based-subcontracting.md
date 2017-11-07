---
title: Toimintoperusteinen alihankinta
description: "Tässä aiheessa kuvataan yksityiskohtaisesti, miten alihankintatoimintoja voi käyttää lean-valmistuksen tuotantovirrassa."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 000bfcf5c3daea75fc257374dd471c62e94fbc16
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="activity-based-subcontracting"></a>Toimintoperusteinen alihankinta

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan yksityiskohtaisesti, miten alihankintatoimintoja voi käyttää lean-valmistuksen tuotantovirrassa.

Microsoft Dynamics 365 for Finance and Operationsissa on kaksi lähestymistapaa alihankintaan: tuotantotilaukset ja lean-valmistus. Lean-valmistuksen lähestymistavassa alihankintatyö on mallinnettu palveluna, joka liittyy tuotantovirran tehtävään. Kustannusryhmän tyyppi, jonka nimi on **Suora ulkoistaminen** on otettu käyttöön, ja alihankinnan palvelut eivät enää kuulu tuoterakenteeseen (BOM). Lean-valmistuksen kustannuslaskennan ratkaisuun on täysin integroitu alihankintatöiden kustannuslaskenta.

## <a name="production-flows-that-involve-subcontractors"></a>Tuotantovirrat, joihin liittyy alihankkijoita
Tuotantovirran perusperiaate ei muutu, kun tehtävät hoidetaan alihankintana. Materiaali virtaa edelleen sijaintien välillä prosessitoiminnot muuntavat materiaalia tuotteiksi ja siirtotehtävät siirtävät materiaaleja tai tuotteita paikasta toiseen. Voit mallintaa sijainteja ja työolut toimittajan hallitaan määrittämällä toimittajatilin varastoon tai resurssin resurssiryhmään.  

Näiden ominaisuuksien perusteella, lean-valmistus ei vaadi erityisiä ominaisuuksia, jotta se tukisi materiaalin ja tuotteiden virtoja. Kaikki mahdolliset skenaariot, joihin kuuluu toimittajia tuotannon tai kuljetuksen tarjoajina, voidaan mallintaa tuotantovirran ja tehtävien arkkitehtuurin perusteella.  

Esimerkiksi alihankkijan työskentelee supermarketissa, joka sijaitsee alihankkijan toimipisteessä. Kun käsittely-yksiköt tyhjennetään alihankkijalla, kanban-kortit palautetaan kokoonpano-soluun seuraavassa toimituksessa. Sitten alihankkijan supermarkettia täydennetään. Siirrot ja alihankkijalle ja alihankkijalta voidaan mallintaa eksplisiittisinä siirtotehtävinä, keräily- ja lähetysprosessin tukemiseksi. Jos fyysisen kuljetuksen tukemiseksi ei tarvita eksplisiittistä rekisteröintiä, kuljetustoiminnot voidaan jättää pois.  

Alihankkijaa voidaan käyttää tuotantovirran yleisen kapasiteetin kuormituksen tasaamiseen. Tuotantovirta on mallinnettu esimerkiksi ajoitettujen kanban-sääntöjen avulla. Suunnittelija käyttää kanban-aikataulua ajoittaakseen ja jakaakseen kuormituksen molemmille työsoluille pyydettäessä. Suunnittelija tarkkailee myös supermarketin konsolidoitua toimitusaikataulua **Toimitusaikataulu**-sivulla. Yhdessä tai useassa tuotantovirrassa voidaan mallintaa useita alihankkijoita, ja siellä voi olla useita kanban-sääntöjä, joiden avulla voidaan toimittaa samaa tuotetta samaan paikkaan eri tehtävien kautta. Suunnittelija voi muuntaa kanbanit vaihtoehtoisiksi kanban-säännöiksi, ajoittaakseen uudelleen vaihtoehtoiseen prosessiin kanbanin, joka on alun perin luotu sisäiseen tuotantoon. Itse asiassa työsolun alihankintaluonne ei vaikuta tuotantovirtaan ollenkaan. Sama toimintaperiaate koskee kahta rinnakkaista sisäistä työsolua tai kahta alihankintana suoritettavaa työsolua.   

Kuten muutkin tuotantovirran tehtävät, alihankintana suoritettavat tehtävät voivat kuluttaa ja täydentää varastoituja, varastoimattomia (keskeneräinen työ \[KET\]) ja puolivalmiita materiaaleja ja tuotteita. Kaikissa tapauksissa alihankintana hankittavien tehtävien ajoituksen ja suorittamisen prosessit ovat samat. Lisäksi nämä prosessoivat samoja kohteita kuin sisäisen työn prosessit.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Alihankintana hankittavien tehtävien ostoprosessi (palvelut)
Alihankintana hankittavien tehtävien ostoprosessi perustuu fyysiseen materiaalivirtaan, jonka kanban-työn edistyminen rekisteröi: esimerkiksi Käynnistä tai Viimeistele. Esimerkiksi taloushallinnon työnkulku – alihankintatöiden kustannus – on sekundaarinen työnkulku, joka seuraa fyysistä virtaa. Samaan aikaan ostoprosessi on riippumaton prosessi, joka mahdollistaa ostoasiakirjojen manuaalisen muuttamisen jokaisessa vaiheessa. Tässä on alihankintana hankittavien tehtävien ostoprosessi:

1.  Luo ostosopimus. Ostosopimus luodaan palvelulle ja se yhdistetään tuotantovirran tehtävään.
2.  Luo ostotilaus. Oston vapautustilaus voidaan luoda palvelulle perustuen ajoitettuihin kanban-töihin. Saman palvelun työt voidaan ryhmitellä ostotilauksen riveille päivän, viikon tai kuukauden mukaan. Ostotilausrivit voidaan luoda milloin tahansa kanban-töiden luonnin jälkeen. Ostotilausrivit voidaan luoda jopa tämän jälkeen. Yleensä tämä vaihtoehto valitaan, jos alihankkija tarjoaa palveluita ilman lisäilmoitusta, vain alihankkijan vastaanottamien tai kanbanien tai kanban-korttien perusteella. Tässä tapauksessa ostotilauksen ja laskun väliset poikkeamat voidaan minimoida.
3.  Luo kanban-kortit, materiaalit ja keräysluettelo lähettääksesi ne alihankkijalle, jotta alihankkija voi valmistautua käsittelyyn. Tuotantovirran yksityiskohtaisen mallinnuksen perusteella valmistelu tapahtuu prosessin toimintojen kanban-taulussa käyttämällä keräysluetteloa ja valmistelutoimintoa. Vaihtoehtoisesti valmistelu tehdään siirtotöiden kanban-taulussa käyttäen keräysluetteloa ja käynnistystä tai viimeistelyä. Varastoiduille materiaalille molempia prosesseja voi tukea varastonhallintajärjestelmän keräysprosessi ja toimitusprosessi. Tarvittaessa voidaan luoda rahtikirja.
4.  Luo kanban-käsittely-yksiköt ja kanban-kortit. Käsittelyn jälkeen kortit palautetaan alihankkijalta. Kortit sisältävät yleensä toimitusilmoituksen, joka määrittää fyysisen materiaalin, joka on toimitettu. Viittausta annetut palveluihin ei tarvita. Materiaalin tai tuotteen saapuminen asiakkaalle rekisteröidään kanban-tauluun kanban-korteista riippuen. (Käytetään joko prosessitehtävien kanban-taulua tai siirtotöiden kanban-taulua mallinnetuista toiminnoista riippuen.).
5.  Luo vastaanoton ohje. Vastaanoton ohjeella voidaan korvata pakkausluettelo vastaanotetuista palveluista. Vastaanoton ohjeita voi luoda alihankinnan tehtävän valmiiden kanban-töiden perusteella valitulle ajanjaksolle. Kullekin työn vastaanotolle voidaan luoda ohjeet liittyvälle ostotilausriville. Vastaanoton ohje voidaan tulostaa ja lähettää alihankkijalle vastaanoton vahvistuksena.
6.  Luo lasku.

Prosessi päättyy, kun alihankkijaa laskutetaan kuluneelta kaudelta. Laskun vastaavuus tehdään vastaanoton ohjeiden mukaan. Koska vastaanoton ohjeet edustavat materiaalin tarkkaa fyysistä vastaanottamista, kolmisuuntaista vastaavuutta on yksinkertaistettu.

## <a name="configuring-activities-for-subcontracting"></a>Alihankinnan tehtävien määrittäminen
Seuraavissa osissa kuvataan alihankinnan tehtävien määrittäminen.

### <a name="subcontracted-services"></a>Alihankintapalvelut

Maksunimikkeen, jota käytetään toimintoperusteisessa alihankinnassa, on oltava tuote, jolla on seuraavat ominaisuudet:

-   **Tuotetyyppi:** Palvelu
-   **Varastomalliryhmä:** Varastoimaton

Tämä vaatimus pakottaa FIFO-varastomallin käytön. **Huomautus:** Tuotteiden kustannuslaskenta vaatii, että palvelun vakiokustannukset määritellään. Ostosopimus toimittajan kanssa on pakollinen. Muutoin palvelua ei voi käyttää toimintoperusteiseen alihankintaan.

### <a name="subcontracted-process-activities"></a>Alihankintana suoritettavat prosessitoiminnot

Voit määrittää prosessitoiminnon alihankintana hankittavaksi tehtäväksi seuraavien ohjeiden mukaisesti.

1.  Määritä alihankintana suoritettava työsolu. Jotta voisit määrittää työsolun alihankintana, sinun on luotava **Toimittaja**-tyypin resurssi ja liittää se työsoluun (resurssiryhmään). Suorituksenaikaisen **Suora ulkoistaminen** -kustannusryhmätyypin kustannusluokka pitää määrittää työsolulle. Kustannusluokkia asetuksille ja määrälle ei tarvita.
2.  Kun prosessitehtävä on luotu ja liitetty alihankintatöiden soluun, tehtävälle on määritettävä palvelu ennen kuin tuotantovirran versio voidaan aktivoida. Suoritat tämän vaiheen **Tehtävän** **tiedot** -sivulla. Toimille, jotka liittyvät alihankintatöiden soluun, näytetään **Palvelun ehdot** -pikavälilehti. Lisää tässä pikavälilehdessä oletuspalvelu, joka koskee kaikkia tuotoksen nimikkeitä. Jos tietyt tuotosnimikkeet vaativat eri palveluja tai eri palvelun laskentaparametreja (esim. eri palvelusuhde), voit lisätä muita palveluja tehtävään.

## <a name="subcontracted-transfer-activities"></a>Alihankintana suoritettavat siirtotoiminnot
Siirtotehtävä määritetään samoin kuin alihankintana hankittavat tehtävät, riippuen siirtotehtävän **Rahdinkuljettaja** -asetuksesta. Valittavissa ovat seuraavat vaihtoehdot:

-   **Lähettäjä** – Tehtävä on alihankintana, jos siirtoa varastosta hallitsee toimittaja (varaston ominaisuuden määrityksen mukaan). Kaikissa palveluiden valituissa ostosopimuksissa pitää olla sama toimittajatunnus fyysisenä varastona.
-   **Vastaanottaja** – Tehtävä on alihankintana, jos siirtoa varastoon hallitsee toimittaja (varaston ominaisuuden määrityksen mukaan). Kaikissa palveluiden valituissa ostosopimuksissa pitää olla sama toimittajatunnus fyysisenä varastona.
-   **Rahdinkuljettaja** – Tehtävän suorittaa alihankintana mikä tahansa toimittaja, joka tarjoaa kyseistä palvelua. Jotta rahdinkuljettaja olisi kelvollinen, rahdinkuljettaja on luotava varastonhallintaa varten ja sillä on oltava määritetty toimittajatili.

Prosessitehtäville sinun on määritettävä oletuspalvelu alihankintana suoritettaville siirtotehtäville **Palvelun ehdot** -pikavälilehdessä **Tehtävän** **tiedot** -sivulla.

## <a name="service-quantity-calculation"></a>Palvelumäärän laskenta
Koko ostoprosessi perustuu palvelun nimikeviitteeseen. Tämä nimikeviittaus mitataan palvelun mittayksikössä. Palvelut mitataan yleensä palveluiden määränä (yksikköinä) tai aikana. Voit laskea palvelumäärän rekisteröityjen kanban-töiden valmistumisten perusteella seuraavilla tavoilla:

-   **Laskenta, joka perustuu töiden määrään** – yksi kanban-työ vastaa *n* palveluyksikköä riippumatta toimitetusta tuotteen määrästä. Lean-valmistuksessa yksi työ vastaa yhtä käsittely-yksikköä. Tätä laskentamenetelmää sovelletaan kaikkiin palveluihin, joissa on kiinteä hinta per käsittely-yksikkö. Tätä menetelmää sovelletaan tämän vuoksi yleensä siirtotehtäviin. Kuitenkin sitä voidaan käyttää myös prosessitehtäviin, jotka käsittelevät kokonaisia käsittely-yksiköitä.
-   **Laskenta, joka perustuu tuotteen määrään** – palvelun määrä on suhteessa tuotteen määrään, joka on suunniteltu/toimitettu. Kun toimitettavaa tuotteen määrää lasketaan, virheelliset määrät voidaan sisällyttää tai jättää pois. Tätä laskentamenetelmää sovelletaan kaikissa tapauksissa,, joissa palvelun yksikköhinta käsiteltyä tuotetta kohden on sovittu.
-   **Laskenta, joka perustuu tehtäväaikaan** – teoreettiset tehtäväajat lasketaan tehtävän käsittelyajan, yhteensä käsitellyn määrän käsitellyn tuotteen tuotantokapasiteetin suhteen perusteella. Tämä laskentamenetelmää koskee palveluja, jotka on maksettu tuntiperusteisesti ja joiden aika vaihtelee jokaista käsiteltyä tuotetta kohden.

## <a name="cost-accounting-of-subcontracted-services"></a>Alihankintapalvelujen kustannuslaskenta
Kun kirjataan vastaanoton ohje tai toimittajan pakkausluettelo ostotilaukselle, joka luotiin tuotantovirtaa varten (toisin sanoen ostotilaus, joka luotiin alihankintatehtävien kanban-töiden perusteella), vastaanoton arvo lisätään kirjanpidossa tuotantovirran KET-tileille. Myös laskujen poikkeamat lisätään kirjanpidossa tuotantovirtaan. Alihankkijalle annetun työn kustannusluokka on otettu käyttöön. Tämä kustannusluokka mahdollistaa sellaisen alihankkijalle annetun työn avoimen seurannan, joka on kohdistettu KET-töihin ja joka kulutetaan yhden kauden aikana.  

Lean-valmistuksen jälkikustannuslaskenta kustannuslaskennan kauden lopussa laskee sellaisten tuotteiden todelliset vaihtelut, jotka on valmistettu tuotantovirrasta kustannuslaskentakauden aikana.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Siirtojen mallintaminen alihankintatehtävinä
Usein kuljetusta pidetään tuottamattomana ja ajatellaan, että se ei tuo lisäarvoa. Kuitenkin verrattaessa alihankinnan kustannuksia sisäisen tuotannon kustannuksiin kuljetustoiminnan lisäkustannukset on otettava huomioon. Tuotantovirran, joka ulottuu useisiin sijainteihin ja vaatii kuljetuspalveluja, olisi mallinnettava kuljetuskustannukset osana tuotteen asiakastoimituksen osana. 

Lean-valmistuksen toimintoperusteisen alihankinnan avulla voit integroida rahdinkuljettajat ja kuljetuspalveluiden tarjoajat, jotka siirtävät materiaaleja ja tuotteita tuotantovirran sijaintien välillä. Mallintamalla siirtotehtävän voit määrittää rahdinkuljettajan tai toimittajan. Siirtotehtävä/-työ perustuu palveluun ja ostosopimukseen, ja voit luoda ostotilauksia ja vastaanoton ohjeita töiden varsinaisen siirron perusteella. Tämä toiminto on sama kuin alihankintaprosessin tehtävien toiminnallisuus.  

Siksi Dynamics 365 for Finance and Operations tukee nyt tuoterakennelaskentaa, joka sisällyttää kuljetuspalvelut, liittyvien ostotilausten luonnin, integroidun vastaanoton rekisteröinnin ja kuljetuspalveluiden kustannusten integroinnin tuotantovirran kustannuslaskentaan.




