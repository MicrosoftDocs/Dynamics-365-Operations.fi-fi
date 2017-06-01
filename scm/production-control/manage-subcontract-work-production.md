---
title: "Tuotannon alihankintatyön hallinta"
description: "Tässä ohjeaiheessa kerrotaan, miten alihankintatoimintoja hallitaan Microsoft Dynamics 365 for Operationsissa. Toisin sanoen siinä selitetään, miten toimittaja voi hallita tuotannon työvaiheita, jotka on kohdistettu resurssiin."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 582807f9f416d3e6e73226dfd2e22af2d6331acd
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="manage-subcontracting-work-in-production"></a>Tuotannon alihankintatyön hallinta

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa kerrotaan, miten alihankintatoimintoja hallitaan Microsoft Dynamics 365 for Operationsissa. Toisin sanoen siinä selitetään, miten toimittaja voi hallita tuotannon työvaiheita, jotka on kohdistettu resurssiin.

[Tuotantoprosessin](production-process-overview.md) töitä voivat tehdä resurssit, joita omistaa tai hallinnoi toimittajat. Yleensä toimittajan resursseja käytetään tasaamaan jaksoittaista suurempaa kysyntää, joka ylittää yhtiön omien resurssien kapasiteetin. Toimittaja voi myös pystyä tarjoamaan erityisiä [resurssin ominaisuuksia](resource-capabilities.md)tai resursseja alempaan hintaan.  

Toimittajan resursseista, joita käytetään tuotantoprosessissa, riippuen [reitillä](routes-operations.md) on usein logistista lisävaatimuksia, koska käytettävät materiaalit ja puolivalmisteet on ensin kuljetettava toimittajan toimipaikkaan. Sitten alihankinnan tulokset on kuljetettava joko sijaintiin, joka on kohdistettu seuraavaan työvaiheeseen tai valmiiden tuotteiden varastoon.  

Alihankintatoimintoja tai -toimenpiteitä käytettäessä ne vaikuttavat kaikkiin toimintovaiheisiin, tuotannossa tarvittavien toimintojen määritelmistä kustannuslaskentaan, ennusteisiin, suunnitteluun ja aikataulutukseen sekä materiaalien, puolivalmisteiden ja valmiiden tuotteiden logistiikan hallintaan. Lopuksi nämä resurssit edellyttävät omat kirjanpidon ja kustannusseurannan prosessinsa.  

Sisäisten resurssien kiinteä kustannushinta kohdistetaan yleensä ajanjaksolle. Sitä vastoin alihankintaresurssien kustannukset perustuvat liittyvän palvelun ostohintaan. Palvelu on määritetty toisena tuotteena ja sitä käytetään suorittamaan tietyn alihankintaoperaation hankinta- ja ostoprosesseihin.  

Tällä hetkellä on ei ole eksplisiittistä puolivalmisteiden käsitettä Microsoft Dynamics 365 for Operationsissa. Tuotantotilaukselle, joka edellyttää useita toimintoja muuntaakseen raaka-aineet valmiiksi tuotteeksi, valmis tuote kirjataan takaisin varastoon vain viimeisessä operaatiossa. Puolivalmiita tuotteita, jotka aiemmat toimet tuottavat, käsitellään keskeneräisenä työnä (KET), mutta niitä ei kirjata tai seurata varastossa. Vaikka voit jakaa reitit ja tuoterakenteet useisiin pienempiin yksiköihin, tämä lähestymistapa kasvattaa hallittavien tuotteiden, tuoterakenteiden ja reittien määrää.  

Tuotannon alihankintatyön mallintamiseen on kaksi tapaa. Nämä menetelmät eroavat siinä, miten alihankinnan prosessi voidaan mallintaa, miten puolivalmisteet esitetään prosessissa ja miten kustannusseuranta on hallittu.

-   Tuotantotilausten tai erätilausten reittioperaatioiden alihankinta
    -   Palvelutuotteen on oltava varastoitava tuote ja sen on oltava osa tuoterakennetta.
    -   Tämä menetelmä tukee FIFO- tai vakiokustannusmenetelmää.
    -   Puolivalmisteita edustaa palvelutuote prosessissa.
    -   Kustannusseuranta varaa kustannukset, jotka liittyvät alihankintatöiden materiaalien kustannuksiin.
-   Tuotantovirran tehtävien alihankinta lean-tuotantovirrassa
    -   Palvelu on ei-varastoitu palvelutuote ja se ei ole osa tuoterakennetta.
    -   Tämä menetelmä käyttää ostosopimuksia palvelusopimuksina.
    -   Tässä menetelmässä käytetään jälkikustannuslaskentaa.
    -   Tämän menetelmä sallii koostetun ja asynkronisen hankinnan. (Materiaalivirrat ovat riippumattomia hankintaprosessista.)
    -   Kustannusseuranta varaa alihankintatyöt omassa kustannuserittelyn lohkossaan.

## <a name="subcontracting-of-route-operations"></a>Reititystehtävien alihankinta
Jotta voisit käyttää reititystehtävien alihankintaa tuotanto- tai erätilauksille, palvelutuote, jota käytetään palvelun hankintaan, on määritettävä **Palvelu** -tyypin tuotteeksi. Lisäksi sillä on oltava nimikemalliryhmä, jossa on **Varastotuote**-vaihtoehto kohdassa **Varastokäytäntö** arvolla **Kyllä**. Tämä vaihtoehto määrittää, lasketaanko tuote varastoksi tuotteen vastaanotossa (**Varastotuote** = **Kyllä**), vai merkitäänkö tuote voitto-ja tappiotilille (**Varastotuote** = **Ei**). Vaikka tämä saattaa näyttää olevan ristiriitaista, se perustuu siihen, että vain ne tuotteet, joita tämä käytäntö koskee, luovat varastotapahtumia, joita voidaan käyttää kustannusseurannassa suunniteltujen kustannusten laskentaan ja selvittämään todelliset kustannukset, kun tuotantotilaus on päättynyt.  

Jotta tämä otettaisiin huomioon suunnittelun ja kustannusten laskennassa, palvelu on lisättävä tuoterakenteeseen. Tuoterakenteen rivin täytyy olla **Toimittaja**-tyyppiä, ja se on kohdistettava reittitehtävään, johon palvelu on kohdistettu. Tällä reitityksen työvaiheella on oltava kustannusresurssi ja resurssivaatimus, jotka viittaavat **Toimittaja**-tyypin resurssiin, joka yhdistää toiminnan ja liittyvän palvelun vastaavan toimittajatiliin.  

Kun tätä määritystä käytetään, luodaan ostotilaus liittyvälle palvelutuotteelle tuotantotilauksen arvioinnin perusteella. Palvelun ostotilausta käytetään alihankintatoimintojen ankkurina. Alihankkijalle annettua työtä hallitaan tuotannonohjauksen **Alihankkijalle annettu työ** -luettelosivulla. Alihankkijalle annettua työtä käytetään toimittamaan raaka-aineita, ja lopulta puolivalmis tuote toimittajalle operaation valmistelussa. Sitä käytetään myös vastaanottamaan alihankintatoiminnan tuloksena olevan tuotteen nimikkeen saapuminen, jossa palvelutuotetta käytetään yksilöimään puolivalmiin tuotteen saapuminen. Ostotilausrivin saapuessa tuotantotyövaihe päivitetään valmiiksi.  

Tuotantotilauksella voi olla monta toimintoa, ja kukin toiminto voidaan kohdistaa eri toimittajalle. Tämän vuoksi päästä-päähän-tuotantotilaus voi aiheuttaa useita ostotilauksia.

## <a name="subcontracting-of-production-flow-activities"></a>Tuotantovirran tehtävien alihankinta
[Lean-valmistuksen](lean-manufacturing-overview.md) lähestymistavassa alihankintatyö on mallinnettu palveluna, joka liittyy [tuotantovirran](http://ax.help.dynamics.com/en/wiki/create-a-production-flow-version/) tehtävään (tehtäväoppaan aihe). Siksi tämäntyyppinen alihankinta on niin sanottu [toimintoperusteisen alihankinta.](activity-based-subcontracting.md) Kustannusryhmän tyyppi, jonka nimi on **Suora ulkoistaminen** on otettu käyttöön, ja alihankinnan palvelut eivät enää kuulu valmiiden tuotteiden tuoterakenteeseen (BOM). Lean-valmistusta käytettäessä kaikki tehtävät määritellään kanbaneina, jotka voidaan liittää yhteen tai useampaan tuotantovirran tehtävään. Tähän mennessä selitys kuulostaa aivan samalta kuin tuotantotilauksissa. Mutta siinä missä tuotantotilausten on aina päätyttävä valmiiseen tuotteeseen, voit luoda kanbaneita tukemaan puolivalmiita tuotteita. Sinun ei tarvitse ottaa käyttöön uutta tuotetta ja tuoterakenteen tasoa.  

Koska kanban-säännöt voivat olla erittäin dynaamisia, voit mallintaa saman tuotteen toimittamisen variantteja tuotantovirrassa. Kun käytät lean-alihankintaa, materiaalivirta ja taloushallinnon työnkulku erotetaan tiukasti toisistaan. Kaikki materiaalivirta esitetään kanban-toimintoina. Palvelutuotteiden ja näiden palvelujen vastaanottokirjauksien ostotilaukset voidaan automatisoida tuotantovirran kanban-töiden tilan perusteella. Kanban-työt voidaan aloittaa ja suorittaa jopa ennen ostotilausten luomista. Alihankinta-asiakirjat (ostotilaus ja palvelun oston vastaanotto) voidaan koostaa ajanjakson ja palvelun mukaan. Tämän vuoksi ostoasiakirjojen ja niiden rivien määrä voidaan säilyttää pienenä jopa hyvin toistuvissa toiminnoissa, jossa toimittajat tarjoavat alihankintapalveluja yhden vaiheen työnkulun avulla.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Alihankinnan mallinnus tuotantovirrassa

[Lean-tuotantovirrassa](lean-manufacturing-modeling-lean-organization.md) prosessintoiminto voidaan määrittää alihankintana, kun se on varattu työsolulle (resurssiryhmälle), jolla on yhden toimittajan resurssi. Kun työsolu on alihankintana, liittyvät prosessin toiminnot on linkitettävä ostosopimuksen rivin, joka sisältää palvelunimikkeen ja palvelun hinnan. Tehtävän palvelusopimus määrittää myös laskennan suhteen tuotteen kanban-työn tuotteen määrän ja tästä johtuvan palvelun määrän välillä. Voit valita, lasketaanko palvelun määrä töiden määrän, töille raportoidun hyvän tuotteen määrän vai tuotteen kokonaismäärän mukaan (tämä kokonaismäärä sisältää hukkatavaratuotteet).  

Siirtotoiminnot voidaan määrittää myös alihankintana. Tämä määritelmä ilmenee implisiittisesti valitessasi vastuullisen osapuolen lähettämiselle siirtotoiminnossa. Kun valitset **Huolitsija** tai **Vastaanottaja** ja jos vastaava lähde- tai kohdevarasto on toimittajan hallitsema varasto, tehtävä katsotaan alihankinnaksi. Kun valitset **Rahdinkuljettaja**, tehtävä on aina alihankintana. Alihankinnan prosessin toimintojen tavoin alihankintana suoritettava siirtotehtävä on yhdistettävä palvelusopimukseen ennen kuin tuotantovirta voidaan aktivoida.

### <a name="backflush-costing"></a>Jälkikustannuslaskenta

Lean-valmistuksen kustannuslaskennan ratkaisuun on täysin integroitu alihankintatöiden kustannuslaskenta (jälkikustannuslaskenta). Kun palvelun ostotilauksen vastaanotto kirjataan tai kun laskutus suoritetaan, palvelun kustannukset kohdistetaan tuotantovirtaan. Jälkikustannuslaskennalle alihankintapalvelujen varianssi lasketaan kuittaamalla vastaanotettujen tuotteiden vakiokustannuksen alihankintalohko toteutuneita vastaanotettuja ja laskutettuja palvelun määriä vasten.

## <a name="material-supply-for-subcontracted-operations"></a>Alihankintatoimintojen materiaalin toimittaminen
Puolivalmisteet ja muu liittyvä materiaali on siirrettävä paikkaan, jossa työ suoritetaan fyysisesti. Käytettäessä alihankintatoimintoja ja -tehtäviä, tämä siirto liittyy usein lisäkuljetukseen toimittajan toimipaikkaan. Varaamalla alihankinnan toimintoon tuoterakenteessa materiaalia, ilmoitat, että materiaali täytyy valmistella kohdistetun resurssin resurssiryhmän syötesijainnissa. Pääsuunnittelu tai lean-täydennys valmistelee materiaalin sitten kyseiseen sijaintiin.  

Toimittajan toimipaikassa sijaitsevan varaston mallintamisen paras käytäntö on määrittää toimittajan hallinnoima fyysinen varasto. Voit helposti määrittää toimittajan hallitsema varaston luomalla uuden varaston ja määrittämällä toimittajatilin. Kirjataksesi, että materiaali on siirrettävä toimittajalle ennen kuin toiminto voidaan suorittaa, sinun tulee varata toimittajan hallitsema varasto resurssia hallitsevan resurssiryhmän syötevarastoon.  

Voit käyttää useita strategioita täydentämään materiaalia tässä varastossa:

-   Siirtotilaukset
-   Siirtokirjauskansiot
-   Otto-kanbanit
-   Suora osto toimittajan sijaintiin

Puolivalmisteet ovat poikkeus tähän sääntöön. Puolivalmisteiden siirrossa olet rajoitettu näihin vaihtoehtoihin:

-   Tuotanto-ja erätilauksissa puolivalmisteet voidaan siirtää vain loogisesti keräysluettelokirjauskansion avulla **Alihankkijalle annettu työ** -luettelosivulla. Tämä kirjauskansio luo toimitusilmoitusasiakirjan, jonka avulla voidaan siirtää puolivalmiita tuotteita ja raaka-aineita toimittajalle.
-   Tuotantovirtojen alihankintaoperaatioille puolivalmisteiden siirto dokumentoidaan otto- tai tuotanto-kanbanien vastaanotossa toimittajan sijainnissa. Voit mallintaa eksplisiittisen siirtotehtävän lopettamalla tuotanto-kanbanin ylimääräisen siirtotehtävän avulla.

**Huomautus:** Yhden tuotantotilauksen tuotantoreititys ei voi koskea useita toimipaikkoja. Tämä sääntö pätee myös alihankkijalle annettuun työhön. Siksi varastot, jotka edustavat toimittajan hallinnoimia materiaalien sijainteja, pitää määrittää samaan toimipaikkaan kuin sisäiset resurssit, joita käytetään kyseisessä reitityksessä. Vaikka tuotantovirrat voivat kulkea useiden toimipaikkojen kautta, ne eivät voi kuljettaa puolivalmisteita toimipaikasta toiseen, koska kyseinen toiminta edellyttää kustannusten kontekstin muutoksen.  

Yleensä tulosvarasto ja alihankinnan resurssiryhmän sijainti on suoraan kohdistettu tuotantovirran tai reitityksen seuraavan vaiheen varastoon ja sijaintiin. Tämä määritys auttaa vähentämään työn raportointia tai mallinnettavien ylimääräisten siirtotehtävien määrää.




