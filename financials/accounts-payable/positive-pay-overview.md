---
title: Positive pay -yhteenveto
description: "Tässä artikkelissa on tietoja Positive pay -palvelusta, jonka avulla luodaan pankille esitettävä sähköinen luettelo sekeistä."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 1fd606817b06a05b9abaaedf20ea9872bd7edd5d
ms.openlocfilehash: cb4806a1f023c1e60311ff9d8facb4ef5717ad94
ms.lasthandoff: 03/31/2017


---

# <a name="positive-pay-overview"></a>Positive pay -yhteenveto

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on tietoja Positive pay -palvelusta, jonka avulla luodaan pankille esitettävä sähköinen luettelo sekeistä. 

Positive pay -palvelun avulla luodaan pankille esitettävä sähköinen luettelo sekeistä. Positive pay -tiedostot auttavat pankkeja estämään sekkipetoksia. Kun määrität Positive pay -toiminnon, sekeistä luodaan sähköinen luettelo aina, kun sekkejä tulostetaan. Kun sekki esitetään pankille, pankki vertaa sekkiä aiemmin lähetettyyn sekkiluetteloon. Jos sekki on sama kuin luettelossa, pankki selvittää sekin. Jos sekki ei vastaa luettelon sekkiä, pankki säilyttää sekin tarkistusta varten.

Positiivisesta maksusta käytetään myös nimitystä SafePay. 

Positiiviset maksutiedostot voivat sisältää luottamuksellisia tietoja maksun saajista ja sekkisummista. Varmista tämän vuoksi, että käytät riittäviä suojaustoimenpiteitä tiedostojen luontihetkestä pankin vastaanottoon asti. Positive pay -tiedostot ladataan verkkoselaimen latausohjeiden mukaisesti. 

Positive pay -tiedostot luodaan käyttämällä tietoyksiköitä. Ennen kuin voit luoda Positive pay -tiedoston, määritä XML-muuntomuodot, jotka kääntävät tiedot pankin käyttämään muotoon. 

Jokaiselle pankkitilille, jolle halutaan luoda Positive pay -tietoja, on määritettävä Positive pay -muoto. Kun olet luonut maksuja, voit luoda Positive pay -tiedoston yksittäiselle yritykselle ja yksittäiselle pankkitilille. Voit myös luoda Positive pay -tiedostoja useille yrityksille ja pankkitileille samalla kertaa. 

Kun positive pay -tiedostossa listatut sekit on maksettu, saat pankiltasi vahvistusnumeron. Tämän jälkeen voit vahvistaa Positive Pay -tiedoston Microsoft Dynamics 365 for Operationsissa. 

Jos haluat muuttaa Positive pay -tiedosto, voit kutsua sen takaisin. Jokaisen Positive pay -tiedostossa olevan sekin kenttä ilmaisee, onko Positive pay -tiedostoon sisältyvä sekki peruutettu.

Lisätietoja: [Määritä ja luo Positive Pay -tiedostoja](set-up-generate-positive-pay-files.md).




