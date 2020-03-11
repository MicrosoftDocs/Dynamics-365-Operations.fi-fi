---
title: Commerce-hierarkiat
description: Tässä artikkelissa käsitellään Dynamics 365 Commercen hierarkioita.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e1b9fc647ccaa3caeec0d0e3a8594fd6a2a8be0f
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070733"
---
# <a name="commerce-hierarchies"></a>Commerce-hierarkiat

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään Dynamics 365 Commercen hierarkioita.

Voit luoda kategoriahierarkian kanavien kautta myymiesi tuotteiden organisoimiseksi. Tuotehierarkioiden avulla voit luokitella tai ryhmitellä tuotteita. Tuotteiden avulla voit luoda edelleen tuotevalikoimia ja asiakkaiden kanta-asiakasohjelmia. Voit myös määrittää tuotteiden määritteitä ja ominaisuuksia sekä hinnoittelurakenteen, sisällyttää tuotteita kampanjoihin ja käyttää niitä raportoinnissa. Voit luoda yhden luokkahierarkian edustamaan kaikkia organisaatiosi tuotteita sekä luokkia ja käyttää sitten tätä luokkahierarkiaa useisiin tarkoituksiin. Voit myös vaihtoehtoisesti luoda useita luokkahierarkioita erikoistarkoituksiin, kuten tuotteiden myynninedistämiseen. Tuotehierarkiaa luotaessa on määritettävä luokkahierarkian tarkoituksen määrittävä luokkahierarkian tyyppi. Esimerkiksi kun tuotteita selataan luokittain verkossa tai myyntipisteissä, viittaukset koskevat vain tuotehierarkioita, joiden tyypiksi on määritetty **Kaupan siirtymishierarkia**.

## <a name="hierarchy-types"></a>Hierarkiatyypit

Seuraavassa taulukossa on kuvattu käytettävissä olevia luokkahierarkioiden tyyppejä ja niiden tarkoitusta.

| Luokkahierarkian tyyppi       | Tarkoitus |
|-------------------------------|---------|
| Tuotehierarkia      | Valitse tämä hierarkiatyyppi, jos haluat määrittää organisaatiollesi yleisen tuotehierarkian. Tätä hierarkiatyyppiä voi käyttää markkinoinnissa, hinnoittelussa ja kampanjoissa, raportoinnissa sekä valikoiman suunnittelussa. Vain yksi tuotehierarkia voidaan määrittää tälle hierarkiatyypille. |
| Lisähierarkia | Tätä hierarkiatyyppiä voi käyttää muissa luotavissa luokkahierarkioissa. Esimerkiksi keväisin järjestetään usein uimapukukampanjoita. Liitä silloin uima-asutuotteet erilliseen luokkahierarkiaan ja käytä kampanjahinnoittelua eri tuoteluokkiin. |
| Siirtymishierarkia   | Tämän hierarkiatyypin avulla voit ryhmitellä ja järjestää tuotteita luokiksi niin, että niitä voidaan selata verkossa tai myyntipisteessä. |

Jäsentelemällä tuotteita luokkahierarkian avulla voit määrittää ja ylläpitää tuotemääritteitä ja -ominaisuuksia luokkatasolla. Nämä määritteet ja ominaisuudet sisältävät tuotedimensioiden asetukset sekä myyntipisteasetukset. Luokkiin määritettävät tuotteet perivät määrittämäsi määritteet ja ominaisuudet automaattisesti. Voit myös kopioida minkä tahansa tuotteen ominaisuusasetukset useisiin valitun luokan tuotteisiin samanaikaisesti.
