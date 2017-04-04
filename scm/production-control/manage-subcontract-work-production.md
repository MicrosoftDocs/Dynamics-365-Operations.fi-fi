---
title: "Tuotanto alihankinnan työn hallinta"
description: "Tässä ohjeaiheessa kerrotaan, miten alihankintatoimintoja hallitaan Microsoft Dynamics-365 operaatioille. Toisin sanoen se kerrotaan miten toimittaja hallitsee tuotannon työvaiheita, jotka on Kohdistettu resurssi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 79430358bebd93fd96f1169d22737d3537dbfc08
ms.lasthandoff: 03/31/2017


---

# <a name="manage-subcontracting-work-in-production"></a>Tuotanto alihankinnan työn hallinta

Tässä ohjeaiheessa kerrotaan, miten alihankintatoimintoja hallitaan Microsoft Dynamics-365 operaatioille. Toisin sanoen se kerrotaan miten toimittaja hallitsee tuotannon työvaiheita, jotka on Kohdistettu resurssi.

- [Tuotantoprosessit](production-process-overview.md), resurssit, joita omistaa tai hallinnoi toimittajat voidaan tehdä työtä. Yleensä tason säännöllinen liian suuri kysyntä, joka surpasses yhtiön käytettävissä olevan kapasiteetin toimittajan resursseja käytetään omia resursseja. Toimittaja voi olla myös pystyvät tarjoamaan erityisiä [resurssin ominaisuudet](resource-capabilities.md)tai resurssien alempaan hintaan.  

Toimittajan resursseista, joita käytetään tuotantoprosessissa, riippuen [reitin](routes-operations.md) on usein logistista lisävaatimuksia, koska käytettävät materiaalit ja puolivalmisteet on ensin kuljetettava toimittajan sivustoon. Sitten alihankintana laskennan tulos on kuljetettava joko sijaintiin, joka on kohdistettu seuraavaan työvaiheeseen tai valmiiden tuotteiden varasto.  

Alihankinta toimintoja tai toimenpiteitä käytetään, kun ne vaikuttavat määritelmän ulkopuolelle toimet, joita tarvitaan tuotannon, Kustannuslaskenta, ennusteet, suunnittelu ja aikataulutus-aineet, puolivalmisteet ja valmiiden tuotteiden logistiikan hallintaan toiminnan kaikissa vaiheissa. Lopuksi nämä resurssit edellyttävät kirjanpitoa ja kustannusseuranta omissa prosesseissa.  

Sisäisten resurssien Kiinteä kustannushinta kohdistetaan yleensä ajan. Sitä vastoin alihankintana resurssien kustannukset perustuvat oleva ostohinta. Palvelu on määritetty toinen tuote ja hankintaan ja ostaa tietyn operaation alihankintana prosesseja käytetään.  

Tällä hetkellä on ei eksplisiittinen puolivalmisteet Microsoft Dynamics-365 toimintojen käsite. Tuotantotilaus, joka edellyttää useita toiminto muuntaa raaka-aineet valmiin tuotteen valmis tuote kirjataan takaisin vain varastossa edellisen toiminnon. Puolivalmiiden tuotteiden, jotka aiheuttavat aiempien toimien käsitellään keskeneräisten töiden (KET), mutta ne eivät ole kirjattu tai joita seurataan varastossa. Vaikka voit jakaa useisiin pienempiin reititysten ja -tuoterakenteiden tuoterakenteeseen, tuotteiden tuoterakenteita ja reittejä, jotka on hoidettava määrä kasvaa tätä lähestymistapaa.  

Alihankinta työtä tuotannon työvaiheiden mallinnusta varten kahdella tavalla. Nämä menetelmät eroavat siinä, miten, että alihankinnan prosessi voi mallintaa, puolivalmisteet esitetään prosessin, ja siten, että kustannusseuranta on hallittu.

-   Alihankinta reitityksen työvaiheen tuotantotilausten tai erätilaukset
    -   Palvelun tuotteen on oltava varastoitavan tuotteen ja sen on oltava osa tätä Tuoterakennetta.
    -   Tämä menetelmä tukee ensin ensin out (FIFO) tai vakiokustannus.
    -   Puolivalmisteet edustaa palvelutuote prosessissa.
    -   Kustannusseuranta varaa kustannukset, jotka liittyvät alihankintatöiden materiaalien kustannuksia.
-   Ajoneuvomerkkien Tuotantovirran tehtävät lean-tuotannon vuo-
    -   Ei ole varastoitu palvelutuote on palvelu ja se ei ole osa tätä Tuoterakennetta.
    -   Tämä menetelmä käyttää huoltosopimusten ostosopimuksia.
    -   Tässä menetelmässä jälkikustannuslaskennan.
    -   Tämän menetelmän avulla koottuja ja asynkronisia hankinnat. (Materiaalivirtojen on itsenäinen hankintojen prosessi).
    -   Kustannusseuranta varaa alihankintatöiden omien kustannusten erittely Block.

## <a name="subcontracting-of-route-operations"></a>Reitityksen työvaiheen alihankinta
Haluat käyttää reitityksen työvaiheita tuotannon tai tilauksia, alihankinta, palvelutuote, jota käytetään palvelun hankintaan on oltava määritetty tulo **Service** tyyppi. Lisäksi sillä on oltava nimikemalliryhmä, jossa on **Varastotuote** -kohdasta vaihtoehto **varaston käytännön** määritetty **Kyllä**. Tämä vaihtoehto määrittää, onko tuote on laskettu tuotteen vastaanoton varaston (**Varastotuote** = **Kyllä**), tai siitä, onko tuote on kulut kirjataan voitto-ja tappio tilille (**Varastotuote** = **ei**). Vaikka tämä saattaa näyttää olevan ristiriitaisia, on perustuu siihen, että vain ne tuotteet, joita tämä käytäntö luo varastotapahtumia, joiden avulla voidaan kustannusseuranta suunniteltujen kustannusten ja selvittää todelliset kustannukset, kun tuotantotilaus on päättynyt.  

Huomioon suunnittelun ja kustannusten laskennassa, palvelu on lisättävä tuoterakenteeseen. Tuoterakenteen rivillä täytyy olla **toimittajan** tyyppi, ja se on tutkittava, jotka on kohdistettu huollon reitityksen työvaihe. Tämä reitityksen työvaihe on oltava kustannusresurssin ja, valitse resurssi resurssivaatimus **toimittajan**, joka yhdistää toiminnan ja niihin liittyvistä service vastaavan toimittajatilin tyyppi.  

Tätä määritystä käytetään, kun luodaan ostotilaus liittyvät palvelutuote tuotantotilauksen arvioinnin perusteella. Palvelu ostotilauksen käytetään ankkuri alihankintana toimintoja. Alihankkijalle annettu työ hallitaan **työn alihankintana** tuotannonohjaus-sivu. Alihankkijalle annettu työ voidaan toimittaa raaka-aineita ja lopulta puolivalmis tuote operaation valmistelussa toimittajalle. Sitä käytetään myös vastaanottamaan alihankintana toiminnan tuloksena olevan tuotteen Nimikkeen saapuminen, jossa palvelun tuotetta käytetään yksilöimään puolivalmiiden tuotteiden saapumisesta. Ostotilausrivin saapuessa tuotantotyövaiheen päivitetään valmiiksi.  

Tuotantotilauksen voi olla monissa toiminnoissa, ja kutakin toimintoa voidaan kohdistaa eri toimittajalle. Tämän vuoksi päästä päähän tuotantotilauksen voivat aiheuttaa useita ostotilauksia.

## <a name="subcontracting-of-production-flow-activities"></a>Ajoneuvomerkkien Tuotantovirran tehtävät
[Lean-valmistuksen](lean-manufacturing-overview.md)ratkaisun mallit alihankinta työtä palveluna, joka liittyy toiminta [tuotantovirran](http://ax.help.dynamics.com/en/wiki/create-a-production-flow-version/) (tehtävä oppaan ohjeaiheessa). Siksi tämäntyyppinen alihankinta on niin sanottu [toimintoperusteisen alihankinta.](activity-based-subcontracting.md) Erityisen kustannusten tyyppi, **suora ulkoistaminen**, on otettu käyttöön, ja alihankinnan palvelut eivät kuulu valmiiden tavaroiden Tuoterakenne. Lean-valmistuksen käytettäessä kaikki tehtävät määritellään kanbanit, jotka voidaan liittää yksi tai useita Tuotantovirran tehtävät. Tähän mennessä, että selitys kuulostaa aivan kuten tuotantotilausten selitys. Tämän vuoksi tuotantotilausten on aina päättyy valmiin tuotteen, voit luoda kanbanit toimittamaan puolivalmis tuote. Sinun ei tarvitse ottaa käyttöön uuden tuotteen ja Tuoterakenteen taso.  

Kanban-säännöt voivat olla erittäin dynaaminen, koska olet malli tuotantovirran muunnelmia saman tuotteen toimittamisesta. Kun käytät lean alihankinta materiaalivirtojen ja rahoituksen kulku erotetaan tiukasti. Kaikki materiaalivirtojen edustaa kanban-toimintaa. Palvelun tuotteiden ja palvelujen vastaanotto kirjaukset ostotilaukset voidaan automatisoida, tuotantovirran kanban-töiden tilan perusteella. Kanban-työt voidaan aloittaa ja jopa ennen ostotilausten luomista suoritettu. Alihankinta-asiakirjat (osto ja tavaran vastaanotto-palvelun) voidaan koota ajan ja palvelu. Tämän vuoksi ostoasiakirjojen rivien määrä voidaan säilyttää pieni jopa hyvin toistuvia toimintoja, jossa valmistajat tarjoavat Alihankintapalvelujen single-nappula vuo.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Alihankinta-tuotantovirran mallinnuksen

- [Lean-tuotannon virtaus](lean-manufacturing-modeling-lean-organization.md), prosessin toimintaa voidaan määrittää alihankintana, kun se on varattu työsolun (resource group), joka on yhden toimittajan resurssia. Työsolu on alihankintana, kun aktiivinen ostosopimuksen rivin, joka sisältää huoltonimikkeen ja palvelun hinta on linkitettävä liittyvän prosessin toimintaa. Huoltosopimuksen tehtävän määrittävät myös tuotteen kanban-työn määrä ja tästä johtuva palvelun määrä laskennan suhde. Voit valita, tuleeko palvelun määrä lasketaan työt, hyvän tuotteen määrä, joka ilmoitetaan töissä tai yhteensä tuotteen määrä (tämä kokonaismäärä sisältää hukkatavaraksi tuotteet) määrän perusteella.  

Siirto toimintoja voidaan määrittää myös alihankintana. Määritelmästä ilmenee implisiittisesti valitessasi vastuullisen osapuolen lähetys, siirto-toiminto. Kun valitset **lähettäjän** tai **vastaanottaja**, jos vastaava lähde tai kohde varasto on toimittajan hallita varastoa, tehtävän katsotaan alihankintana. Kun valitset **kuljettajan**, tehtävä aina alihankintana. Alihankinnan prosessin toimintojen, kuten alihankintana Siirtotehtävä on yhdistettävä huoltosopimuksen ennen tuotantovirran voidaan aktivoida.

### <a name="backflush-costing"></a>Jälkikustannuslaskenta

Kustannuslaskenta, alihankintatöiden on täysin integroitu (jälkikustannuslaskennan) ratkaisun lean-valmistuksen kustannuslaskennan. Kun palvelun osto-vastaanotto kirjataan tai kun palvelun kustannukset kohdistetaan tuotantovirran. Jälkikustannuslaskenta, Alihankintapalvelujen varianssi lasketaan kuittaamalla alihankinta lohkon vastaanotetuksi ja laskutetuksi palvelun todelliset määrät vastaanotettujen tuotteiden vakiokustannukset.

## <a name="material-supply-for-subcontracted-operations"></a>Alihankintatoimintoja materiaalin toimittamisesta
Puolivalmisteet ja muu oheismateriaali on siirrettävä paikkaan, jossa työ suoritetaan fyysisesti. Käytettäessä alihankintatoimintoja ja toiminnan siirto liittyy usein toimittajan toiminut sivustoon Lisää liikennettä. Varaamalla alihankintana toiminnan tuoterakenteen materiaali kielessä materiaalin täytyy valmistella Kohdistettu resurssi resurssiryhmään syötteen sijainnissa. Pääsuunnittelu tai sitten lean-täydennyksen valmistelee materiaalia kyseiseen sijaintiin.  

Varasto, joka sijaitsee osoitteessa sivuston toimittajan-malli on paras käytäntö määrittää toimittajan hallita varaston teollisuudessa. Voit määrittää toimittajan hallita varaston helposti luomalla uuden varaston ja määrittämällä toimittajatili. Asiakirjojen kyseistä materiaalia on siirrettävä toimittajalle ennen kuin toiminto voidaan suorittaa, tulee varata toimittajan hallita varasto, jolla on resurssin resurssiryhmän varastoa.  

Voit käyttää useita strategioita täydennettävää tässä varastossa materiaali:

-   Siirtotilaukset
-   Siirtokirjauskansiot
-   Otto-kanbanit
-   Suorien ostojen toimittajan sijainti

Puolivalmisteet ovat poikkeus tähän sääntöön. Puolivalmisteet siirretään olet rajoitettu näihin asetuksiin:

-   Tuotanto-ja erätilaukset puolivalmisteet voi siirtää vain loogisesti-keräysluettelokirjauskansion avulla **työn alihankintana** sivulla. Tämän lehden Luo toimitusilmoituksen asiakirja, jonka avulla voidaan siirtää puolivalmiita ja raaka-aineen toimittajalle.
-   Tuotantovirtojen alihankintana operaatioille puolivalmisteet siirretään dokumentoitu vastaanoton peruuttaminen tai tuotannon kanbanien toimittaja paikassa. Eksplisiittinen Siirtotehtävä malliin, voit lopettaa kanssa muita Siirtotehtävä Tuotanto-kanban.

**Huomautus:** yhden tuotantotilauksen tuotantoreitityksen ei cross useita sivustoja. Tämä sääntö pätee myös Alihankkijalle annettu työ. Siksi varastot, jotka edustavat sijainnit on määritetty samaan sivustoon kuin sisäiset resurssit, joita käytetään reitin toimittajan hallitaan materiaali. Tuotantovirtojen voivat liikennöidä sivustot, vaikka ne ei voi kuljettaa puolivalmisteet yksi sivustosta toiseen, koska kyseinen toiminta edellyttää kustannusten kontekstin muutos.  

Yleensä tulos varasto ja sijainti alihankintana resurssiryhmän suoraan kohdistuvat varasto ja sijainti reititys- tai työnkulun toiminnon seuraavaan vaiheeseen. Tämä asennusohjelma auttaa vähentämään työn raportointi, joka ilmenee tai numeron siirto Lisää Toiminnot, jotka on mallinnettu.


