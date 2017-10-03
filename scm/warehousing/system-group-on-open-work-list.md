---
title: "Järjestelmän ryhmittely avoimessa työluettelossa"
description: "Tässä aiheessa kuvataan avoimen työluettelon suodattamista mobiililaitteella."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: dbf0e49b1156c54cd37bbbe57ca564cdbc45fb2d
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017

---

# <a name="system-grouping-on-an-open-work-list"></a>Järjestelmän ryhmittely avoimessa työluettelossa

[!include[banner](../includes/banner.md)]

Järjestelmän ryhmittelykentän avulla voit suodattaa avoimen työluettelon muokkaamatta mobiililaitteen valikkovaihtoehtoa.
Järjestelmän ryhmittelyä voidaan käyttää työluettelon suodattamisessa yhden työn otsikkokentässä. Et voi käyttää järjestelmän ryhmittelyä online-tason kentissä.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Järjestelmän ryhmittelyn määrittely avoimessa työluettelossa
Suorita seuraavat vaiheet järjestelmän ryhmittelyn määrittelemiseksi avoimessa työluettelossa.

-   Valitse mobiililaitteen valikkovaihtoehdoista **Tila: epäsuora** ja **Tehtävän koodi: Näytä avoin työluettelo**. Valittaviksi tulevat seuraavat vaihtoehdot. Nämä asetukset ovat pakollisia järjestelmän ryhmittelemiseksi avoimessa työluettelossa. 

| Vaihtoehto        | kuvaus   | 
| ------------- | ------------- |
| Salli järjestelmän ryhmittely   | Mahdollistaa järjestelmän ryhmittelyn valitun työluettelon valikon kohteelle.| 
| Järjestelmän ryhmittelykenttä   | Käytettävissä vain, jos **Järjestelmän työn salliminen** on määritetty **Kyllä**. Valitse kenttä, joka määrittää, miten poimintatyö ryhmitellään työntekijälle. Esimerkiksi jos valitset **ShipmentId**-kentän, työntekijä skannaa lähetystunnuksen keräilytyön ryhmittelemiseksi. Tämän jälkeen kaikki lähetyksen työt on määritetty työntekijälle. Tämä kenttä edellyttää, että luot valikkovaihtoehdon, jolla voi käyttää aiemmin luotua järjestelmän ryhmittelemää työtä. Ilmoita työntekijälle skannattavat kohteet **Järjestelmän ryhmittelyotsikko** -kentässä. |
| Järjestelmän ryhmittelyotsikko   | Käytettävissä vain, jos **Järjestelmän työn salliminen** on määritetty **Kyllä**. Kirjoita tiedot työntekijälle siitä, mitä tulisi skannata, kun poimintatyö ryhmitellään. Jos esimerkiksi käytät **ShipmentId**-kenttää keräilytöiden ryhmittelemiseen lähetyksen mukaan, voit kirjoittaa kenttään Lähetyksen tunnus. Tämä kenttä edellyttää, että luot valikkovaihtoehdon, jolla voi käyttää aiemmin luotua järjestelmän ryhmittelemää työtä. Sinun on myös valittava ryhmiteltävä kenttä **Järjestelmän ryhmittely** -kentässä.|

