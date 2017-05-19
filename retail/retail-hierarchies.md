---
title: "Vähittäismyyntihierarkiat"
description: "Tässä artikkelissa kuvataan Microsoft Dynamics AX:n vähittäismyyntihierarkioita."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 4dc4fdfa8abf65ba13f5c94042a8eb28a3d7c046
ms.contentlocale: fi-fi
ms.lasthandoff: 04/26/2017


---

# <a name="retail-hierarchies"></a>Vähittäismyyntihierarkiat

[!include[banner](includes/banner.md)]


Tässä artikkelissa kuvataan Microsoft Dynamics AX:n vähittäismyyntihierarkioita.

Voit luoda vähittäismyyntiluokan hierarkian, jonka avulla voit järjestää vähittäismyyntikanavissa myymiäsi tuotteita. Vähittäismyynnin tuotehierarkioiden avulla voit luokitella tai ryhmitellä tuotteita. Tuotteiden avulla voit luoda edelleen tuotevalikoimia ja asiakkaiden kanta-asiakasohjelmia. Voit myös määrittää tuotteiden määritteitä ja ominaisuuksia sekä hinnoittelurakenteen, sisällyttää tuotteita kampanjoihin ja käyttää niitä raportoinnissa. Voit luoda yhden vähittäismyynnin luokkahierarkian edustamaan kaikkia organisaatiosi tuotteita ja luokkia ja käyttää sitten tätä luokkahierarkiaa useisiin tarkoituksiin. Voit myös vaihtoehtoisesti luoda useita vähittäismyynnin luokkahierarkioita erikoistarkoituksiin, kuten tuotekampanjoihin. Vähittäismyynnin tuotehierarkiaa luotaessa on määritettävä luokkahierarkian tarkoituksen määrittävä luokkahierarkian tyyppi. Esimerkiksi kun tuotteita selataan luokittain verkossa tai myyntipisteissä, viittaukset koskevat vain tuotehierarkioita, joiden tyypiksi on määritetty **Vähittäismyynnin siirtymishierarkia**.

## <a name="retail-hierarchy-types"></a>Vähittäismyyntihierarkian tyypit
Seuraavassa taulukossa on kuvattu käytettävissä olevia vähittäismyynnin luokkahierarkioiden tyyppejä ja niiden tarkoitusta.

| Luokkahierarkian tyyppi       | Tarkoitus                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vähittäismyynnin tuotehierarkia      | Valitse tämä hierarkiatyyppi, jos haluat määrittää organisaatiollesi yleisen tuotehierarkian. Tätä hierarkiatyyppiä voi käyttää markkinoinnissa, hinnoittelussa ja kampanjoissa, raportoinnissa sekä valikoiman suunnittelussa. Vain yksi vähittäismyynnin tuotehierarkia voidaan määrittää tälle hierarkiatyypille.                                       |
| Vähittäismyynnin lisähierarkia | Tätä hierarkiatyyppiä voi käyttää muissa luotavissa vähittäismyynnin luokkahierarkioissa. Esimerkiksi keväisin järjestetään usein uimapukukampanjoita. Liitä silloin uima-asutuotteet erilliseen luokkahierarkiaan ja käytä kampanjahinnoittelua eri tuoteluokkiin. |
| Vähittäismyynnin siirtymishierarkia   | Tämän hierarkiatyypin avulla voit ryhmitellä ja järjestää tuotteita luokiksi niin, että niitä voidaan selata verkossa tai myyntipisteessä.                                                                                                                                                                                       |

Jäsentelemällä tuotteita vähittäismyynnin luokkahierarkian avulla voit määrittää ja ylläpitää tuotemääritteitä ja -ominaisuuksia luokkatasolla. Nämä määritteet ja ominaisuudet sisältävät tuotedimensioiden asetukset sekä myyntipisteasetukset. Luokkiin määritettävät tuotteet perivät määrittämäsi määritteet ja ominaisuudet automaattisesti. Voit myös kopioida minkä tahansa tuotteen ominaisuusasetukset useisiin valitun luokan tuotteisiin samanaikaisesti.




