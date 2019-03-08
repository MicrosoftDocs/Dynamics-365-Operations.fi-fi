---
title: Poista tuotantovirran version aktivointi
description: Kun aktiivista tuotantovirran versiota ei enää tarvita, se voidaan poistaa käytöstä.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091cafd02bd568323e586373fc8b0f983afee343
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "340749"
---
# <a name="deactivate-a-production-flow-version"></a>Poista tuotantovirran version aktivointi

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kun aktiivista tuotantovirran versiota ei enää tarvita, se voidaan poistaa käytöstä. Käytä tätä vaihtoehtoa vain, jos kaikki kanban-säännöt ja aktiviteetit ovat päättyneet, eikä niitä aktivoida uudelleen. Huomaa, että kaikkien tämän tuotantovirran versioon liittyvien kanban-sääntöjen päättymispäivämääräksi asetetaan nykyinen päivämäärä ja kellonaika. 

Jos haluat muokata aktiivisen tuotantovirran versiota, harkitse vanhentumispäivämäärän asettamista on aktiiviselle versiolle, jonka jälkeen voit luoda uuden version. Näin voit jatkaa antaa tuotantosi jatkua samalla, kun valmistelet uutta versiota ja siihen liittyviä kanban-sääntöjä. 

Jotta aktiivisen tuotantovirran versio voisi poistaa käytöstä, sille on määritettävä vanhentumispäivämäärä. Tavallaan siis käytöstä poistaminen on enemmänkin poikkeus kuin sääntö. 

Tätä menettelyä varten tarvitset tuotantovirran, jolla on käytöstä poistettava versio. Älä tee tätä tuotantoympäristössä, jos et ole täysin varma, että versio on täysin tarpeeton.


## <a name="deactivate-a-production-flow-version"></a>Poista tuotantovirran version aktivointi
1. Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Valitse Poista käytöstä.
    * Älä jatka, jos et ole täysin varma, että tämän tuotantovirran versio on vanhentunut. Valitsemalla Ok asetat kaikki aktiiviset kanban-säännöt vanhentuneeksi; kaikki tämän tuotantovirran version tuotanto- ja täydennysaktiviteetit pysäytetään välittömästi.  
6. Valitse OK.

