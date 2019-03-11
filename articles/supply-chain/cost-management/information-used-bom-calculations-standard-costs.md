---
title: Standardikustannuksia sisältävissä tuoterakennelaskelmissa käytettävät tiedot
description: Tuoterakennelaskelmissa käytetään tietoja useista lähteistä valmistetun nimikkeen standardikustannusten laskemista varten. Näissä lähteissä on tietoja nimikkeistä, tuoterakenteiden reitityksistä, epäsuorien kustannusten laskentakaavoista sekä kustannuslaskelmaversiosta.
author: AndersGirke
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcGroup, BOMCalcTable, ProdParmBOMCalc
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 65571
ms.assetid: ca17e6dd-b16a-4bbc-8682-b16345ab9906
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ec6ffe41d6dae10693b1a1ebd6e5012c32bc2e6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "333757"
---
# <a name="information-used-in-bom-calculations-with-standard-costs"></a>Standardikustannuksia sisältävissä tuoterakennelaskelmissa käytettävät tiedot

[!include [banner](../includes/banner.md)]

Tuoterakennelaskelmissa käytetään tietoja useista lähteistä valmistetun nimikkeen standardikustannusten laskemista varten. Näissä lähteissä on tietoja nimikkeistä, tuoterakenteiden reitityksistä, epäsuorien kustannusten laskentakaavoista sekä kustannuslaskelmaversiosta.

Standardikustannuksen tuoterakennelaskelmassa käytettäviin ostetun nimikkeen tietoihin sisältyvät seuraavat tiedot:
-   Kustannus − Ostetun nimikkeen kustannustietoja ylläpidetään toimipaikkakohtaisissa kustannustietueissa standardikustannusten kustannuslaskelmaversiossa. Kullakin kustannustietueella on voimaantulopäivämäärä, ja käytettävä kustannustietue määräytyy tuoterakennelaskelman päivämäärän mukaan. Esimerkiksi tuoterakennelaskelmassa, jonka laskentapäivämäärä on tulevaisuudessa, voidaan käyttää odottavassa tilassa olevaa kustannustietuetta, jonka voimaantulopäivämäärä on tulevaisuudessa.
-   Kustannusryhmä − Ostetulle nimikkeelle määritetty kustannusryhmä toimii perustana valmistetun nimikkeen laskettujen kustannusten ryhmittelyssä.
-   Nimikkeen tuoterakennelaskelmaryhmään sisällytettyjen varoitusehtojen avulla voidaan tunnistaa tuoterakennelaskelman mahdolliset ongelmat. Näin voi olla, kun ostetun nimikkeen kustannukset ovat nolla, tuoterakenteen määrä on nolla tai kustannustietue on vanhentunut. Sovellettavat varoitusehdot voidaan ohittaa tuoterakennelaskentaa aloitettaessa.

Standardikustannuksen tuoterakennelaskelmassa käytettäviin valmistetun nimikkeen tietoihin sisältyvät seuraavat tiedot:
-   Vakiotilausmäärä varastoon − Nimikkeen vakiotilausmäärää varastossa käytetään kirjanpidon oletuseräkokona tuoterakennelaskelman vakiokustannusten kuoletuksessa. Kirjanpidon eräkoko kuvastaa myös tilausmäärän kerrointa, jos se on määritetty.
-   Nimikkeen tuoterakennelaskelmaryhmään sisällytettyjen varoitusehtojen avulla voidaan tunnistaa tuoterakennelaskelman mahdolliset ongelmat. Yksi esimerkki voisi olla, että valmistetulla nimikkeellä ei ole tuoterakennetta tai reittiä. Sovellettavat varoitusehdot voidaan ohittaa tuoterakennelaskentaa aloitettaessa.

Standardikustannuksen tuoterakennelaskelmassa käytettäviin tuoterakennetietoihin sisältyvät seuraavat tiedot:
-   Tuoterakenneversio − Valmistetulle nimikkeelle määritetyllä tuoterakenneversiolla on voimaantulo- ja vanhentumispäivämäärät sekä hyväksynnän ja käyttöönoton tila. Tuoterakenneversio voi olla yrityksenlaajuinen tai toimipaikkakohtainen, ja siinä voi valinnaisesti määrittää määrän keskeytyskohtia.
-   Tuoterakennerivin nimikkeen määrä − Tavallisesti komponentin tarvemäärä on muuttuva, mutta määrä voi olla myös vakio. Komponentin määrä ilmaistaan yleensä yhden päänimikkeen tuottamista varten, mutta desimaalitarkkuusnäkökohtien vuoksi määrän voi ilmaista 100:n tai 1 000:n nimikkeen tuottamista varten. Komponentin määrän voi myös laskea mittausten perusteella.
-   Tuoterakennerivin nimikehävikki − Komponentin suunniteltu hävikki voi olla muuttuva määrä tai vakio.
-   Tuoterakennerivin nimikkeen voimassaolopäivämäärät − Komponentilla voi olla voimaantulo- ja vanhentumispäivämäärät.
-   Tuoterakennerivin nimikkeen tuotantotyyppi − Kustannuslaskennan eräkoko vakiokustannusten kuoletusta varten määräytyy tuoterakennelaskelman määrän ja tilausta varten tehdyn hajotustilan perusteella, koska tuoterakennelaskelmassa oletetaan, että valmistettua komponenttia valmistetaan tarkka määrä vakiotilausmäärän asemesta.
-   Valmistetun nimikkeen alituoterakenne − Valmistetulla nimikkeellä voi valinnaisesti olla määritettynä tuoterakenneversio, jota voi käyttää nimikkeen nykyisen aktiivisen tuoterakenneversion asemesta tuoterakennelaskelmassa.
-   Valmistetun nimikkeen alireititys - Valmistetulla nimikkeellä voi valinnaisesti olla määritettynä reitti, jota voi käyttää nimikkeen nykyisen aktiivisen reitin asemesta tuoterakennelaskelmassa.
-   Työvaiheen numero ja työvaiheen hävikkiprosentit − Työvaiheen numero linkittää komponentin tiettyyn työvaiheeseen, ja työvaiheilla voi olla hävikkiprosentti. Linkin ansiosta tuoterakennelaskelmissa voidaan ottaa komponentin tarvemäärässä huomioon hävikkiprosentit sekä useista työvaiheista kertyvät kumulatiiviset hävikkiprosentit.
-   Tuoterakennerivin nimikkeen jättäminen pois kustannuslaskelmista − Komponentin voi jättää pois tuoterakennelaskelmista.

Standardikustannuksen tuoterakennelaskelmassa käytettäviin operatiivisten resurssien tietoihin sisältyvät seuraavat tiedot:
-   Tuntihinnat − Operatiiviseen resurssiin liittyvät tuntihinnat ilmaistaan asennus- ja suoritusajalle määritettyinä kustannusluokkina. Nämä kustannusluokat on määritettävä resurssiryhmille ja operatiivisille resursseille. Kustannusluokkaan liittyvät tuntihinnat voivat olla toimipaikkakohtaisia tai yrityksenlaajuisia.
-   Yksikkökohtaiset kustannukset − Joissakin valmistusympäristöissä operatiivisten resurssien kustannukset määritetään tuotettua yksikköä kohti. Tämä ilmaistaan erillisen määrää koskevan kustannusluokan avulla. Esimerkiksi määriin liittyviä kustannuksia voivat olla työvoiman urakkapalkat, tai maalin valmistaja voi määrittää operatiivisen resurssin kustannukset tuotettua litraa kohden.
-   Operatiivisten resurssien tietojen ohittaminen reitityksen työvaiheissa − Resurssien kustannusluokkatiedot periytyvät työvaiheisiin, missä ne voidaan ohittaa. Tuoterakennelaskelmissa käytetään kustannusluokkatietoja, jotka on määritetty reitityksen työvaiheissa.
-   Kustannusluokan kustannusryhmä − Kustannusluokalle määritetyn kustannusryhmän avulla voi ryhmitellä valmistetun nimikkeen lasketut kustannukset. Esimerkiksi laitteisiin ja työvoimaan liittyvät kustannukset tai asennusajan ja ajoajan kustannukset voidaan ryhmitellä eri kustannusryhmiin.

Standardikustannuksen tuoterakennelaskelmassa käytettäviin reittitietoihin sisältyvät seuraavat tiedot:
-   Reittiversio - Valmistetulle nimikkeelle määritetyllä reittiversiolla on voimaantulo- ja vanhentumispäivämäärät sekä hyväksynnän ja käyttöönoton tila. Reittiversion on oltava toimipaikkakohtainen, ja siinä voi valinnaisesti määrittää määrän keskeytyskohtia.
-   Reitityksen työvaiheen aika − Ajoajan ja asennusajan voi määrittää erikseen. Aika tunteina ilmaistaan yleensä yhden päänimikkeen tuottamista varten, mutta desimaalitarkkuusnäkökohtien vuoksi määrän voi ilmaista 100:n tai 1 000:n nimikkeen tuottamista varten.
-   Toissijaisten resurssien reitityksen työvaiheen aika − Toissijaisella resurssilla on sama työvaiheen numero kuin ensisijaisella resurssilla ja sama reitityksen työvaiheen aika. Työvaiheessa saattaa olla määritetty esimerkiksi laite ensisijaiseksi resurssiksi ja työvoima sekä työkalut toissijaisiksi resursseiksi.
-   Reitityksen työvaiheen hävikkiprosentti − Tuoterakennelaskelmissa otetaan huomioon hävikkiprosentit sekä useista työvaiheista kertyvät kumulatiiviset hävikkiprosentit. Tämä koskee reitityksen työvaiheisiin tarvittavaa aikaa sekä työvaiheen numeroihin linkitettyjen komponenttien tarvemääriä.
-   Reitityksen työvaiheen kustannusluokat − Operatiivisten resurssien kustannusluokkatiedot periytyvät työvaiheisiin, missä ne voidaan ohittaa. Tuoterakennelaskelmissa käytetään kustannusluokkatietoja, jotka on määritetty reitityksen työvaiheissa.

Standardikustannuksen tuoterakennelaskelmassa käytettäviin valmistuksen yleiskustannustietoihin sisältyvät seuraavat tiedot:
-   Lisämaksu − Lisämaksun laskentakaava sisältää prosenttiarvon, kuten 100 prosenttia, joka liitetään tiettyyn kustannusryhmään, kuten työvoimaan.
-   Hinta − Hinnan laskentakaava sisältää yksikkökohtaisen summan, kuten 10,00 euroa per tunti, joka liitetään tiettyyn kustannusryhmään, kuten työvoimaan.
-   Aikaan perustuvat yleiskustannukset vai raaka-aineisiin perustuvat yleiskustannukset − Valmistuksen yleiskustannukset voi liittää reitityksen työvaiheisiin tai raaka-ainekomponentteihin.

Standardikustannuksen tuoterakennelaskelmassa käytettäviin kustannuslaskelmaversion tietoihin sisältyvät seuraavat tiedot:
-   Kustannuslaskelmatyyppi − Kustannuslaskelmaversion on sisällettävä standardikustannukset. Standardikustannuksia käyttäviä tuoterakennelaskelmia koskevat tietyt rajoitukset. Näissä rajoituksissa määritetään esimerkiksi se, että muut kulut on sisällytettävä yksikkökustannuksiin ja että tuoterakennelaskelman hajotustilan on oltava yksitasoinen.
-   Pakollinen varmistusmenettely − Kustannuslaskelmaversiossa voi määrittää varmistusmenettelyn pakolliseksi. Tällainen varmistusmenettely voi olla esimerkiksi määritetyn kustannuslaskelmaversion tai aktiivisten kustannustietueiden käyttäminen. Pakollinen varmistusmenettely koskee yleensä kustannuslaskelmaversiota, jossa kustannuspäivitykset toteutetaan lisäyspäivityksinä kahden version menetelmällä.
-   Odottavien kustannusten estomerkintä − Estomerkintä voi estää valmistettujen nimikkeiden odottavien kustannusten tuoterakennelaskelmat.
-   Määritetty voimaantulopäivämäärä − Määritettyä voimaantulopäivämäärää käytetään laskennan oletuspäivämääränä kaikissa tuoterakennelaskelmissa, joissa kustannuslaskelmaversiota käytetään.
-   Määritetty toimipaikka − Määritetty toimipaikka rajaa tuoterakennelaskelmat koskemaan yksittäistä toimipaikkaa.
-   Kustannusten on sisällyttävä kustannuslaskelmaversioon − Kustannusten on kuuluttava sisältöön. Sisältöön voi valinnaisesti sisällyttää myyntihinnat valmistettujen nimikkeiden ehdotettujen myyntihintojen laskemista varten.

Tuoterakennelaskentaa aloitettaessa voi määrittää useita tietolähteitä. Näihin kuuluvat toimipaikka, laskentapäivämäärä ja kustannuslaskelmaversio.





