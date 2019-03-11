---
title: Tilikauden joukkosulkeminen
description: Tässä toimintaohjeessa kuvataan, miten kausi asetetaan pitoon tai pysyvästi suljetuksi useammalle yritykselle kerralla.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2988b7ab0837cc9a3e4f1c4eaf3fe6e219fa721
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "311378"
---
# <a name="mass-financial-period-close"></a>Tilikauden joukkosulkeminen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä toimintaohjeessa kuvataan, miten kausi asetetaan pitoon tai pysyvästi suljetuksi useammalle yritykselle kerralla. Lisäksi tehtävässä näytetään, miten käyttäjäryhmän kirjaukset voi rajoittaa tiettyihin moduuleihin.

1. Valitse Kirjanpito > Kausi suljettu > Kirjanpidon kalenterit.
    * Huomaa, että luettelossa näytettävät yritykset riippuvat sivulla valitusta vuosikalenterista. Vain valittua vuosikalenteria käyttävät yritykset näytetään.  
2. Valitse Muokkaa.
3. Valitse kausi, jonka tilaa haluat muokata.
4. Valitse yritykset, joiden tilan haluat päivittää.
    * Voit valita kaikki yritykset nopeasti valitsemalla valintaruudun ruudukon vasemmalla puolella.  
5. Valitse Päivitä moduulien käyttöoikeudet määrittääksesi tietyn moduulin kirjausoikeudet.
    * Moduulin tilan voi myös päivittää yksitellen muokkaamalla tietueita ruudukossa. Painike on hyödyllinen, kun haluat päivittää usean yrityksen tietueet nopeasti.  
6. Valitse Sovellusmoduulissa päivitettävä moduuli. Klikkaa Valitse.
7. Valitse Käyttöoikeustaso-kohtaan Kaikki, Ei mitään tai tietty käyttäjäryhmä. Klikkaa Valitse.
    * Kaikki ilmaisee, että kaikilla käyttäjillä, joilla on moduulin muokkausoikeudet, voivat tehdä kirjauksia avoimena kautena. Ei mitään ilmaisee, että käyttäjät eivät saa kirjata moduuliin avoimena kautena. Tietty käyttäjäryhmä ilmaisee, että vain ryhmän jäsenet voivat kirjata moduuliin avoimena kautena.  
8. Valitse Päivitä.
9. Päivitä tila valitsemalla toinen kausi.
10. Valitse yritykset, joiden kauden tilan haluat päivittää.
11. Valitse Päivitä kauden tila ja aseta tilaksi Pidossa tai Suljettu pysyvästi.
    * Avoin ilmaisee, että jos käyttäjällä on käyttöoikeus, hän voi tehdä kirjauksia kauteen. Pidossa-tila tarkoittaa, että kaudelle ei voi tehdä kirjauksia, mutta se voidaan avata uudelleen. Suljettu pysyvästi -tila tarkoittaa, että kausi on suljettu, eikä sitä voi avata uudelleen. Oikaisuja ei voi kirjata. Kauden sulkemista pysyvästi ei suositella, ennen kuin kaikki oikaisut ja tarkistukset ovat valmiita.  
12. Valitse Päivitä.

