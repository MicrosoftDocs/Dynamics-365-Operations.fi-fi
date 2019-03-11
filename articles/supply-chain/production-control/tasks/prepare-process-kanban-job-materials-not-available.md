---
title: Prosessin kanban-työn valmisteleminen kun materiaalit eivät ole käytettävissä työsolulle
description: Tässä menettelyssä keskitytään prosessin kanban-töiden valmisteluun, kun osa työsolun materiaalista ei ole valmiina. Materiaalit on siis kerättävä varastosta.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7e7eb46bda13ef7e72189f921686a9889a8773c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "339898"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>Prosessin kanban-työn valmisteleminen kun materiaalit eivät ole käytettävissä työsolulle

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä keskitytään prosessin kanban-töiden valmisteluun, kun osa työsolun materiaalista ei ole valmiina. Materiaalit on siis kerättävä varastosta. Valmistele prosessin kanban-työ kun materiaalit ovat käytettävissä työsolulle -menettely on tämän menettelyn luomisen edellytys. Tämä menettely on tarkoitettu koneenkäyttäjille. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.

1. Siirry kohtaan Tuotannonhallinta > Kanban > Prosessitöiden kanban-taulu.
2. Avaa haku valitsemalla Työsolu-kentässä avattavan valikon painike.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse työsolu 1250.  
4. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse kanban 000356.  
5. Etsi haluamasi tietue luettelosta ja valitse se.
    * Poista luettelossa rivin 4 valinta. Tai valitse rivi 4, jos Käsittele prosessin kanban-työ, kun materiaalit ovat käytettävissä -tehtävä ei ole valmis.  
6. Ota käyttöön Keräysluettelo-osan laajennus.
    * Jos toimituksen tilan yhteydessä on Ei kirjausta -kuvake, työsolun nimikkeestä P0002 puuttuu 48 kappaletta.  

## <a name="transfer-materials-to-work-cell"></a>Materiaalien siirtäminen työsoluun
1. Ota käyttöön Siirtotyöt-osan laajennus.
2. Pikasuodattimen avulla voit suodattaa Nimiketunnus-kentän arvon P0002 mukaan.
3. Etsi haluamasi tietue luettelosta ja valitse se.
4. Valitse Käynnistys.
    * Siirto on meneillään.  
5. Valitse Valmis.
    * Nimike P0002 on nyt käytettävissä kanban-työnä keräysluettelossa. Voit siis alkaa valmistella kanbania ja tarvittavia materiaaleja.  
6. Valitse Valmistele.
    * Huomaa, että työn tilan kuvake osoittaa työn olevan valmis.  

