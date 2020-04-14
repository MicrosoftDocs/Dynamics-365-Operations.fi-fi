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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 860873a1fd61d52f642774e69d48c5ef6c7465a9
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146833"
---
# <a name="deactivate-a-production-flow-version"></a>Poista tuotantovirran version aktivointi

[!include [banner](../../includes/banner.md)]

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

