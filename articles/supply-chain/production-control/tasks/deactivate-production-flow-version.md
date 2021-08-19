---
title: Poista tuotantovirran version aktivointi
description: Kun aktiivista tuotantovirran versiota ei enää tarvita, se voidaan poistaa käytöstä.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 488f5d9e1137be2686f3f3056f4c4543766a16799a2f0484c3c4f0f9f3d456ad
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726774"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]