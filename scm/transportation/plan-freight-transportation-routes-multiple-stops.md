---
title: "Useita pysähdyksiä sisältävän rahdinkuljetusreitin suunnittelu"
description: "Tässä artikkelissa käsitellään elementtejä, joilla kuljetusreittejä suunnitellaan Dynamics 365 for Finance and Operationsissa."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: e7965c094f91bcbcad21ecfa599f133a6e84f4f7
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Useita pysähdyksiä sisältävän rahdinkuljetusreitin suunnittelu
<a id="plan-freight-transportation-routes-with-multiple-stops" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Tässä artikkelissa käsitellään elementtejä, joilla kuljetusreittejä suunnitellaan Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa.

Voit käyttää reittisuunnitelmia ja reittioppaita, kun kuljetusreitit ovat monimutkaisia ja niissä on useita pysähdyksiä. Jos samaa reittiä käytetään säännöllisesti, voit määrittää aikataulutetun reitin.

## Reittisuunnitelmat
<a id="route-plans" class="xliff"></a>
Reittisuunnitelma sisältää reittisegmenttejä, joissa on tietoja reitin pysähdyskohdista, rahdinkuljettajista, joita kussakin segmentissä käytetään. Sinun on määritettävä reitin pysähdyskohdat keskuksina. Keskus voi olla toimittaja, varasto, asiakas tai jopa uudelleenkuormauspaikka, jossa vaihdat rahdinkuljettajaa. Voit määrittää kussakin segmentissä eri kuluille spot-kursseja. Seuraavassa on muutamia esimerkkejä:

-   Matkustuskulut tiettyyn segmenttiin
-   Hyödykkeiden keräilykulut
-   Hyödykkeiden jättömaksut

Jokaiseen reittisuunnitelmaan on liitettävä reittiopas.

## Reittioppaat
<a id="route-guides" class="xliff"></a>
Reittiopas määrittää kuorman täsmäytysehdot tietylle reittisuunnitelmalle. Voit esimerkiksi määrittää alkuperäkeskuksen ja kohdekeskuksen, kontin tilavuus- tai painorajat sekä lähetyksen rahdinkuljettajan, palvelun tai ryhmän. Reittioppaat ovat saatavilla **Hinnan ja reitin työtila** -sivulla, jossa kuormat ja reitit voidaan täsmäyttää manuaalisesti tai automaattisesti. Jos kyse on ajoitetun reitin reittioppaasta, se on saatavilla myös **Kuormituksen luonnin työtila** -sivulla.

## Ajoitetut reitit
<a id="scheduled-routes" class="xliff"></a>
Ajoitettu reitti on esimääritetty reitti, jossa on lähetyspäivämäärien aikataulu. Ajoitetut reitit ja ajoittamattomat reitit erona on tapa, jolla niihin määritetään kuormat. Jos määrität ajoittamattoman reitin Hinnan ja reitin työtila -sivulla, vain kuorma ja reittiopas vahvistetaan. Jos määrität ajoitetun reitin, myös tilausten ja keskusten päivämäärät ja osoitteet sekä reittisuunnitelman päivämäärä otetaan huomioon. Ajoitetun reitin kuormien manuaaliseen määrittämiseen ei tarvita Hinnan ja reitin työtila -sivulla. Voit sen sijaan ehdottaa Kuormituksen luonnin työtila -sivulla, että kuormat muodostetaan annetun ajoitetun reitin myyntilausten asiakasosoitteiden ja toimituspäivien perusteella. Ajoitettujen reittien reitityssuunnitelmassa on kiinteät alku- ja kohdekeskukset. Yleensä kaikissa segmenteissä on sama rahdinkuljettaja ja rahtipalvelu, mutta se ei ole välttämätöntä. Kohdekeskukset luodaan käyttämällä niiden asiakkaiden postinumeroita, joiden luona pysähdytään reitillä. Yhdelle reittisuunnitelmalle voidaan määrittää useita reittiajoituksia. Reittisuunnitelmaan on liitettävä reittiopas. Ajoitettujen reittien suunnitelma voidaan kuitenkin liittää vain yhteen reittioppaaseen. Reittiaikataululla luodaan vain todellisia reittejä **Reittiaikataulu**-sivulla. Voit käyttää oletuskuormamalleja ehdottamaan kuormia Kuormituksen luonnin työtila -sivulla.

## Kuormituksen luonnin työtila
<a id="load-building-workbench" class="xliff"></a>
Kuormituksen luonnin työtila -sivu ehdottaa kuormaa hakemalla asiakkaiden osoitteet ja toimituspäivät myyntitilauksista sekä käytettävissä olevat ajoitetut reitit. Oletusarvoisesti työtilassa annetaan reitin arvot. Voit kuitenkin valita aloituspäiväksi reitin aloituspäivää edeltävän päivämäärän. Kun kuormaa on ehdotettu, kaikkien avoimien myyntitilausten toimitusosoite ja toimituspäivä tarkistetaan. Toimitusosoitteen postinumero vastaa reittisuunnitelmassa olevan keskuksen postinumeroa ja jos toimituspäivä on ehdoissa valitulla alueella, myyntitilausta ehdotetaan kuormaan. Myös kuormamallin kapasiteetti otetaan huomioon. Kerrallaan ehdotetaan vain yhtä kuormaa. Jos sinulla on myyntitilaus, joka ei sisälly ehdotukseen, sinun on ehkä käytettävä eri kuormamallia (esimerkiksi suuremman kuorma-auton tai kontin kuormamallia) tai suunniteltava lisätoimitus.




