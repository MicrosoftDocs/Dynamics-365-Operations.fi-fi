---
title: Materiaalien siirtäminen kanban-töiden yhteydessä
description: Tässä menettelyssä keskitytään otto-kanbaneihin materiaalien siirtämiseksi.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46009f09f6e843c45f50351963ad01419e24a878
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831839"
---
# <a name="transfer-materials-with-kanban-jobs"></a>Materiaalien siirtäminen kanban-töiden yhteydessä

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä keskitytään otto-kanbaneihin materiaalien siirtämiseksi. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu varastotyöntekijälle.


## <a name="display-transfer-jobs"></a>Siirtotöiden näyttäminen
1. Siirry kohtaan Tuotannonhallinta > Kanban > Siirtotöiden Kanban-taulu.
2. Laajenna tai tiivistä Suodattimet-osa.
    * Suodattimet-osassa voit määrittää, mitkä työt näkyvät suodatettaessa tuotantovirran, tehtävän nimen, lähetysvaraston ja -sijainnin ja vastaanottovaraston ja -sijainnin mukaan.  
3. Syötä Varastosta-kenttään 11.
4. Syötä Varastoon-kenttään arvo 12.

## <a name="start-a-transfer-job"></a>Aloita siirtotyö
1. Poista luettelosta mahdollisen valitun rivin valinta.
2. Valitse luettelosta rivi 4.
    * Valitse ensimmäisen työ, jonka tila on Ei Suunniteltu. Varmista, että tämä on ainoa valittu työ.  
3. Valitse Käynnistys.
    * Huomaa, että kuvake osoittaa työn alkaneen.  

## <a name="select-a-second-transfer-job-and-change-quantity"></a>Toisen siirtotyön valitseminen ja määrän muuttaminen
1. Etsi haluamasi tietue luettelosta ja valitse se.
    * Voit valita useita töitä, mutta valitse tässä vaiheessa rivi 5.  
2. Etsi haluamasi tietue luettelosta ja valitse se.
    * Varmista, että edellisen vaiheen työ on ainoa valittuna oleva. Poista muiden töiden valinta.  
3. Merkitse Työn määrä- kentän arvo muistiin myöhempää käyttöä varten
4. Määritä Työn määrä -kenttään arvo 30.
    * Huomaa varoitus! 30 on liikaa siirrettäväksi. Kanban-säännön asetusten perusteella voit siirtää vain alkuperäisen määrän.  
5. Käytä aiempaa Työn määrä -kentän arvoa
    * Määritä työn määräksi edellinen arvo.  

## <a name="start-the-second-transfer-job"></a>Toisen siirtotyön aloittaminen
1. Valitse Käynnistys.
    * Nyt rivillä 5 olevan työn siirto alkaa.  

## <a name="complete-both-transfer-jobs"></a>Molempien siirtotöiden suorittaminen
1. Valitse luettelosta rivi 4.
    * Nyt on valittuna kaksi siirtotyötä rivillä 4 ja 5.  
2. Valitse Valmis.
    * Molempien töiden siirto suoritetaan.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]