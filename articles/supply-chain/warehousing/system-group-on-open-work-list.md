---
title: Järjestelmän ryhmittely avoimessa työluettelossa
description: Tässä aiheessa kuvataan avoimen työluettelon suodattamista mobiililaitteella.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05b697cce8ecb9ece282fc659ab4d97c4b747c5e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426937"
---
# <a name="system-grouping-on-an-open-work-list"></a>Järjestelmän ryhmittely avoimessa työluettelossa

[!include [banner](../includes/banner.md)]

Järjestelmän ryhmittelykentän avulla voit suodattaa avoimen työluettelon muokkaamatta mobiililaitteen valikkovaihtoehtoa.
Järjestelmän ryhmittelyä voidaan käyttää työluettelon suodattamisessa yhden työn otsikkokentässä. Et voi käyttää järjestelmän ryhmittelyä online-tason kentissä.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Järjestelmän ryhmittelyn määrittely avoimessa työluettelossa
Suorita seuraavat vaiheet järjestelmän ryhmittelyn määrittelemiseksi avoimessa työluettelossa.

-   Valitse mobiililaitteen valikkovaihtoehdoista **Tila: epäsuora** ja **Tehtävän koodi: Näytä avoin työluettelo**. Valittaviksi tulevat seuraavat vaihtoehdot. Nämä asetukset ovat pakollisia järjestelmän ryhmittelemiseksi avoimessa työluettelossa. 

|        Vaihtoehto         |                                                                                                                                                                                                                                                                         kuvaus                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Salli järjestelmän ryhmittely |                                                                                                                                                                                                                                                 Mahdollistaa järjestelmän ryhmittelyn valitun työluettelon valikon kohteelle.                                                                                                                                                                                                                                                  |
| Järjestelmän ryhmittelykenttä | Käytettävissä vain, jos <strong>Järjestelmän työn salliminen</strong> on määritetty <strong>Kyllä</strong>. Valitse kenttä, joka määrittää, miten poimintatyö ryhmitellään työntekijälle. Esimerkiksi jos valitset <strong>ShipmentId</strong>-kentän, työntekijä skannaa lähetystunnuksen keräilytyön ryhmittelemiseksi. Tämän jälkeen kaikki lähetyksen työt on määritetty työntekijälle. Tämä kenttä edellyttää, että luot valikkovaihtoehdon, jolla voi käyttää aiemmin luotua järjestelmän ryhmittelemää työtä. Ilmoita työntekijälle skannattavat kohteet <strong>Järjestelmän ryhmittelyotsikko</strong> -kentässä. |
| Järjestelmän ryhmittelyotsikko |                       Käytettävissä vain, jos <strong>Järjestelmän työn salliminen</strong> on määritetty <strong>Kyllä</strong>. Kirjoita tiedot työntekijälle siitä, mitä tulisi skannata, kun poimintatyö ryhmitellään. Jos esimerkiksi käytät <strong>ShipmentId</strong>-kenttää keräilytöiden ryhmittelemiseen lähetyksen mukaan, voit kirjoittaa kenttään Lähetyksen tunnus. Tämä kenttä edellyttää, että luot valikkovaihtoehdon, jolla voi käyttää aiemmin luotua järjestelmän ryhmittelemää työtä. Sinun on myös valittava ryhmiteltävä kenttä <strong>Järjestelmän ryhmittely</strong> -kentässä.                       |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]