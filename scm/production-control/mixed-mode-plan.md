---
title: "Monijärjestelmäsuunnittelu: erillisen, prosessi- ja Lean-hankinnan yhdistäminen"
description: "Tässä artikkelissa on tietoja monijärjestelmäsuunnittelusta. Monijärjestelmäsuunnittelussa toimitusketjun voi mallintaa materiaalivirran perusteella. Microsoft Dynamics 365 for Operations varmistaa, että materiaalivirta seuraa malleja valitusta toimituskäytännöstä huolimatta (kanbanit, tuotantotilaukset, erätilaukset tai siirtotilaukset)."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e63dd046587f29947c45b12a878ce7108bb1621e
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Monijärjestelmäsuunnittelu: erillisen, prosessi- ja Lean-hankinnan yhdistäminen

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on tietoja monijärjestelmäsuunnittelusta. Monijärjestelmäsuunnittelussa toimitusketjun voi mallintaa materiaalivirran perusteella. Microsoft Dynamics 365 for Operations varmistaa, että materiaalivirta seuraa malleja valitusta toimituskäytännöstä huolimatta (kanbanit, tuotantotilaukset, erätilaukset tai siirtotilaukset). 

Voit valita tuotteen tarjoamiselle yleisen strategian tuoterakenteesta riippumatta.  

Sinulla voi esimerkiksi olla kokoonpanossa kanban-ohjaus, jossa materiaalit hankitaan kokoonpanoalueelle tuotantotilausten, kanbaneiden, siirtojen, erätilausten tai minkä tahansa muun toimitusketjusi ominaisuuksiin soveltuvan yhdistelmän perusteella, mutta sinulla on silti täysi näkyvyys kaikkiin toimittajiin. Tämä ominaisuus johtaa optimoituihin toimitusketjun prosesseihin ja parannettuun toimitusketjuasi koskevaan näkyvyyteen.  

Toimituskäytäntöjen pääajoituksessa käytettävä rakeisuus riippuu kattavuusdimensioina käyttöön otetuista varastodimensioista. Kun haluat ottaa käyttöön pääajoituksen ohjaamaan erityyppisten sijaintien täydennystä ja toimituksia (esimerkiksi erottamalla tuotannon eri tuotantoyksiköihin tai erottamalla erityyppisten materiaalien ja valmiiden tuotteiden varastot), suosittelemme, että otat käyttöön Toimipaikka ja varasto -asetuksen kattavuusdimensioina. Vaihtoehtoisesti, Varasto voidaan jättää pois kattavuusdimensioista. Siinä tapauksessa, käyttäessäsi varastonhallinnan lisätoimintoja, kaikkia varaston sisäisiä siirtoja ohjaa varastossa tehtävä työ, kun taas kaikkia varastojen välisiä siirtoja ohjaavat otto-kanbanit.

## <a name="supply-policies"></a>Toimituskäytännöt
Microsoft Dynamics 365 for Operationsin monijärjestelmäsuunnittelu ohjaa sitä, miten tuote toimitetaan ja toimituksen perusteella, miten johdetut tarpeet (nimikkeiden kulutus tuoterakenteesta \[BOM\]) luodaan. Järjestelmä hankkii automaattisesti tarpeita vastaavat materiaalit tilaustyypin perusteella.  

Toimituskäytäntöjä voidaan määrittää tuotetasolla tai millä tahansa tarpeisiisi soveltuvalla rakeisuudella. Voit määrittää toimituskäytäntöjesi rakeisuuden**Tilauksen oletusasetukset** -sivulla.  

Toimituskäytäntöjä voidaan ohjata tuote-, nimikedimensio- (konfiguraatio, väri ja koko), toimipaikka- ja varastokohtaisesti. Tämä määritys asetetaan **Nimikkeen kattavuus** -sivulla.  

Oletusmuotoinen tilaustyyppi ohjaa, mitä tilausten pääsuunnittelu luo.  

Toimitusketjun mallinnustavasta riippumatta, Dynamics 365 for Operations tukee toimituskäytäntöyhdistelmiäsi. Sinulla voi olla kanbaneista lähtöisin olevia tuotantotilauksia. Vaihtoehtoisesti sinulla voi olla erätilaus, joka vaatii siirroilla tai kanbaneilla toimitetun tuotteen.  

Dynamics 365 for Operations varmistaa, että materiaalivirta seuraa mallia.  

Materiaalit keräilevä varasto määritetään dynaamisesti suorituksen aikana, kun toimituskäytäntö on määritetty.  

Yleensä kanbaneita ei luoda tuleville päiville, koska kanbaneilla on lyhyt elinkaari. Pystyäksemme säilyttämään täyden näkymän toimitusketjuun, olemme luoneet uuden suunnittelukonseptin nimeltä "suunniteltu kanban", jota käytetään johdettujen tarpeiden laskemiseen ja joka takaa, että tarpeet hankitaan samaan logiikkaan perustuen kuin varsinaista kanbania luotaessa.  

Sama logiikka sisältyy kaikkiin muihin toimitusketjukäytäntöjen tyyppeihin. Näin ollen, pitkän aikavälin materiaalisuunnittelu perustuu samaan logiikkaan, jonka odotat olevan käytössä varsinaisissa tilauksissa, kun tuotanto ja toimitus on hyväksytty.

## <a name="materials-allocation-crosssupply-policy--resource-consumption-on-boms"></a>Materiaalien kohdistamisen poikkituotannon käytäntö – Resurssien kulutus tuoterakenteissa
Resurssien kulutus on tärkeä toiminto. Resurssien kulutuksen avulla materiaalit keräävä varasto voidaan valita dynaamisesti toimituskäytännön (tilaustyyppi) perusteella. Se myös helpottaa perustietojen ylläpitämistä.  

Resurssien kulutus edellyttää, että varasto, josta materiaalit kerätään, määritetään tuotteen toimitustavan perusteella. Toisin sanoen, järjestelmä löytää suorituksen aikana resurssit, joita tulee käyttää valmistuksessa. Järjestelmä valitsee sitten keräävän varaston näihin resursseihin perustuen.  

Toimituskäytännöstä riippumattomien töiden ollessa kyseessä sinun ei tarvitse muuttaa tuoterakenteen tietoja, jos toimitus muuttuu. Yksittäisten muutosten tapauksessa Dynamics 365 for Operations varmistaa, että materiaalit hankitaan oikeasta varastosta.

## <a name="process-manufacturing--the-production-type"></a>Prosessituotanto – tuotantotyyppi
Hyödyntääksesi täyden joustavuuden monijärjestelmätilassa suosittelemme, että käytät tuotantotyyppisiä tuoterakenteita kaikille tuotteille. Voit sitten käyttää tuotantotilauksia, kanbaneita, siirtotilauksia tai ostotilauksia tuotteen toimitukseen. Prosessituotannon ollessa kyseessä, sinun on käytettävä tuotantotyyppejä **Resepti**, **Oheistuote**, **Sivutuote**, tai **Suunnittelunimike**. Kanbaneita ja tuotantotilauksia ei voida käyttää näille tuotantotyypeille.




