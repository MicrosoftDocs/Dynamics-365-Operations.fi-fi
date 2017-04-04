---
title: "Mixed mode suunnittelu - Yhdistä erillinen-, prosessi- ja lean hankinta"
description: "Tässä artikkelissa on tietoja monijärjestelmäsuunnittelusta. Monijärjestelmäsuunnittelussa toimitusketjun voi mallintaa materiaalivirran perusteella. Varmistaa, että Microsoft Dynamics-365 toiminnoissa (kanbanit, tuotantotilauksia, ostotilauksia, tilauksia tai siirtotilauksia), materiaalin kulkua noudattaa mallit, vaikka tarjonta käytäntö, joka on valittu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d635421112f6d1e79a47090de3ffc4178b36b132
ms.lasthandoff: 03/31/2017


---

# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Mixed mode suunnittelu - Yhdistä erillinen-, prosessi- ja lean hankinta

Tässä artikkelissa on tietoja monijärjestelmäsuunnittelusta. Monijärjestelmäsuunnittelussa toimitusketjun voi mallintaa materiaalivirran perusteella. Varmistaa, että Microsoft Dynamics-365 toiminnoissa (kanbanit, tuotantotilauksia, ostotilauksia, tilauksia tai siirtotilauksia), materiaalin kulkua noudattaa mallit, vaikka tarjonta käytäntö, joka on valittu. 

Voit valita tuotteen tarjoamiselle yleisen strategian tuoterakenteesta riippumatta.  

Sinulla voi esimerkiksi olla kokoonpanossa kanban-ohjaus, jossa materiaalit hankitaan kokoonpanoalueelle tuotantotilausten, kanbaneiden, siirtojen, erätilausten tai minkä tahansa muun toimitusketjusi ominaisuuksiin soveltuvan yhdistelmän perusteella, mutta sinulla on silti täysi näkyvyys kaikkiin toimittajiin. Tämä ominaisuus johtaa optimoituihin toimitusketjun prosesseihin ja parannettuun toimitusketjuasi koskevaan näkyvyyteen.  

Toimituskäytäntöjen pääajoituksessa käytettävä rakeisuus riippuu kattavuusdimensioina käyttöön otetuista varastodimensioista. Kun haluat ottaa käyttöön pääajoituksen ohjaamaan erityyppisten sijaintien täydennystä ja toimituksia (esimerkiksi erottamalla tuotannon eri tuotantoyksiköihin tai erottamalla erityyppisten materiaalien ja valmiiden tuotteiden varastot), suosittelemme, että otat käyttöön Toimipaikka ja varasto -asetuksen kattavuusdimensioina. Vaihtoehtoisesti, Varasto voidaan jättää pois kattavuusdimensioista. Siinä tapauksessa, käyttäessäsi varastonhallinnan lisätoimintoja, kaikkia varaston sisäisiä siirtoja ohjaa varastossa tehtävä työ, kun taas kaikkia varastojen välisiä siirtoja ohjaavat otto-kanbanit.

## <a name="supply-policies"></a>Toimituskäytännöt
Dynamics 365 sekatilan suunnittelun toimintoja valvoo tuote on toimitettu ja, perustuvat suoritukset, miten johdetut tarpeet (materiaalien tuoterakenteen nimikkeiden kulutuksen \[Tuoterakenteen\]) on annettu. Järjestelmä hankkii automaattisesti tarpeita vastaavat materiaalit tilaustyypin perusteella.  

Toimituskäytäntöjä voidaan määrittää tuotetasolla tai millä tahansa tarpeisiisi soveltuvalla rakeisuudella. Voit määrittää toimituskäytäntöjesi rakeisuuden**Tilauksen oletusasetukset ** -sivulla.  

Toimituskäytäntöjä voidaan ohjata tuote-, nimikedimensio- (konfiguraatio, väri ja koko), toimipaikka- ja varastokohtaisesti. Tämä määritys asetetaan **Nimikkeen kattavuus** -sivulla.  

Oletusmuotoinen tilaustyyppi ohjaa, mitä tilausten pääsuunnittelu luo.  

Riippumatta siitä, miten on mallinnettu toimitusketjun Dynamics 365 työvaiheiden tukee oman yhdistelmän ostokäytännöt. Sinulla voi olla kanbaneista lähtöisin olevia tuotantotilauksia. Vaihtoehtoisesti sinulla voi olla erätilaus, joka vaatii siirroilla tai kanbaneilla toimitetun tuotteen.  

Työvaiheiden 365 Dynamics varmistaa, materiaalivirtojen noudattaa malli.  

Materiaalit keräilevä varasto määritetään dynaamisesti suorituksen aikana, kun toimituskäytäntö on määritetty.  

Yleensä kanbaneita ei luoda tuleville päiville, koska kanbaneilla on lyhyt elinkaari. Pystyäksemme säilyttämään täyden näkymän toimitusketjuun, olemme luoneet uuden suunnittelukonseptin nimeltä "suunniteltu kanban", jota käytetään johdettujen tarpeiden laskemiseen ja joka takaa, että tarpeet hankitaan samaan logiikkaan perustuen kuin varsinaista kanbania luotaessa.  

Sama logiikka sisältyy kaikkiin muihin toimitusketjukäytäntöjen tyyppeihin. Näin ollen, pitkän aikavälin materiaalisuunnittelu perustuu samaan logiikkaan, jonka odotat olevan käytössä varsinaisissa tilauksissa, kun tuotanto ja toimitus on hyväksytty.

## <a name="materials-allocation-crosssupply-policy--resource-consumption-on-boms"></a>Materiaalin jako crosssupply käytännön – luonnonvarojen tuoterakenteissa
Resurssin kulutus on tärkeä toiminto. Resurssien kulutuksen avulla materiaalit keräävä varasto voidaan valita dynaamisesti toimituskäytännön (tilaustyyppi) perusteella. Se myös helpottaa perustietojen ylläpitämistä.  

Resurssien kulutus edellyttää, että varasto, josta materiaalit kerätään, määritetään tuotteen toimitustavan perusteella. Toisin sanoen, järjestelmä löytää suorituksen aikana resurssit, joita tulee käyttää valmistuksessa. Järjestelmä valitsee sitten keräävän varaston näihin resursseihin perustuen.  

Toimituskäytännöstä riippumattomien töiden ollessa kyseessä sinun ei tarvitse muuttaa tuoterakenteen tietoja, jos toimitus muuttuu. Ad-hoc muutokset Dynamics 365 toimintojen varmistaa, että materiaalit ovat Orpotermit oikean varastosta.

## <a name="process-manufacturing--the-production-type"></a>Prosessituotanto – tuotantotyyppi
Sekatila koko joustavuutta on suositeltavaa käyttää tyypin tuotannon tuoterakenteiden kaikkien tuotteiden. Sitten voit tuotantotilauksia, kanbanit, siirtotilaukset tai ostotilausten toimittamaan tuotteen. Prosessituotannon ollessa kyseessä, sinun on käytettävä tuotantotyyppejä **Resepti**, **Oheistuote**, **Sivutuote**, tai **Suunnittelunimike**. Kanbaneita ja tuotantotilauksia ei voida käyttää näille tuotantotyypeille.


