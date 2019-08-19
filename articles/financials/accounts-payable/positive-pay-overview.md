---
title: Positive pay -yhteenveto
description: Tässä artikkelissa on tietoja Positive pay -palvelusta, jonka avulla luodaan pankille esitettävä sähköinen luettelo sekeistä.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2ba23cf5afe9f007f5e32a75e918595929ad79a1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834606"
---
# <a name="positive-pay-overview"></a>Positive pay -yhteenveto

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja Positive pay -palvelusta, jonka avulla luodaan pankille esitettävä sähköinen luettelo sekeistä. 

Positive pay -palvelun avulla luodaan pankille esitettävä sähköinen luettelo sekeistä. Positive pay -tiedostot auttavat pankkeja estämään sekkipetoksia. Kun määrität Positive pay -toiminnon, sekeistä luodaan sähköinen luettelo aina, kun sekkejä tulostetaan. Kun sekki esitetään pankille, pankki vertaa sekkiä aiemmin lähetettyyn sekkiluetteloon. Jos sekki on sama kuin luettelossa, pankki selvittää sekin. Jos sekki ei vastaa luettelon sekkiä, pankki säilyttää sekin tarkistusta varten.

Positiivisesta maksusta käytetään myös nimitystä SafePay. 

Positiiviset maksutiedostot voivat sisältää luottamuksellisia tietoja maksun saajista ja sekkisummista. Varmista tämän vuoksi, että käytät riittäviä suojaustoimenpiteitä tiedostojen luontihetkestä pankin vastaanottoon asti. Positive pay -tiedostot ladataan verkkoselaimen latausohjeiden mukaisesti. 

Positive pay -tiedostot luodaan käyttämällä tietoyksiköitä. Ennen kuin voit luoda Positive pay -tiedoston, määritä XML-muuntomuodot, jotka kääntävät tiedot pankin käyttämään muotoon. 

Jokaiselle pankkitilille, jolle halutaan luoda Positive pay -tietoja, on määritettävä Positive pay -muoto. Kun olet luonut maksuja, voit luoda Positive pay -tiedoston yksittäiselle yritykselle ja yksittäiselle pankkitilille. Voit myös luoda Positive pay -tiedostoja useille yrityksille ja pankkitileille samalla kertaa. 

Kun positive pay -tiedostossa listatut sekit on maksettu, saat pankiltasi vahvistusnumeron. Voit sitten vahvistaa positive pay -tiedoston Microsoft Dynamics 365 for Finance and Operationsissa. 

Jos haluat muuttaa Positive pay -tiedosto, voit kutsua sen takaisin. Jokaisen Positive pay -tiedostossa olevan sekin kenttä ilmaisee, onko Positive pay -tiedostoon sisältyvä sekki peruutettu.

Lisätietoja: [Määritä ja luo Positive Pay -tiedostoja](set-up-generate-positive-pay-files.md).



