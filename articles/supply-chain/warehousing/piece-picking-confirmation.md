---
title: "Kappaleen keräilyvahvistus"
description: "Tässä ohjeaiheessa kerrotaan kappaleen keräilyvahvistuksen määrittämisestä ja käyttämisestä mobiililaitteessa."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 62b637b81a522c353067248deea79cfbf98518e9
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="piece-picking-confirmation"></a>Kappaleen keräilyvahvistus

[!include[banner](../includes/banner.md)]

Kappalekeräilyssä voit vahvistaa mobiililaitteessa varaston jokaisen kappaleen keräily- tai inventointityön avulla. Voit vahvistaa keräilyssä käsiteltävän työn määrän kerättävään työhön määritettyyn määrään saakka. Voit skannata inventointityössä inventoitavan varaston ja seurata kokonaismäärää.

Kun otat kappalekeräilyn käyttöön, tuotevahvistus valitaan automaattisesti. Kun työn tyyppinä on keräys, kappaleiden enimmäismäärä otetaan käyttöön. Tällä tavoin voit määrittää työprosessin aikana vahvistettavien kappaleiden enimmäismäärän. Enimmäismäärä perustuu käsiteltävänä olevaan nykyiseen työyksikköön. Enimmäismäärää ei voi määrittää, jos työtyyppinä on inventointi.

Voit käyttää myös skannattuun viivakoodin liitettyä määrää ja mittayksikköä. Tämä saapuvien ja lähtevien virtojen työ sisältää yhdistetyn rekisterikilven vastaanoton, ostotilausnimikkeen, siirtotilausnimikkeen ja kuormanimikkeen. Se toimii myös kappalekeräilyssä, jossa viivakoodin skannaus lisää määrän vahvistettujen kappaleiden kokonaismäärään muuntamalla mittayksikön viivakoodin ja työyksikön välillä. Jos viivakoodin mittayksikköä inventoitaessa vahvistetaan, että määrä on sallittu sarjaryhmän inventoinnissa, määrä lisätään kokonaismäärään.

## <a name="where-it-applies"></a>Käyttö

Kappalekeräilyä voi käyttää kaikissa inventointitöissä ja kaikenlaisten työtyyppien ensimmäisellä keräyksessä. Kappalekeräystä ei voi käyttää, jos nimikettä ohjataan sarjanumeroilla tai jos se on tuotanto- tai kanban-keräily rekisterikilpisijainnista ja jos nimike on määritetty väliaikaiseen varastoon.

## <a name="set-up-piece-picking"></a>Kappalekeräilyn määrittäminen

1.  Avaa mobiililaitteen valikossa työn vahvistuksen määrityslomake: Varastonhallinta > **Varastonhallinta** > **Asetukset** > **Mobiililaite** > **Mobiililaitteen valikkovaihtoehdot**. 
2. Avaa mobiililaitteen valikossa Työn vahvistusasetukset.

Seuraavat asetukset ovat valittavissa, kun työtyyppinä on keräily tai inventointi.

| Vaihtoehto        | kuvaus   | 
| ------------- | ------------- |
| Kappaleen keräilyvahvistus   | Käytettävissä, kun työtyyppinä on keräily tai inventointi. Tuotteen vahvistus valitaan automaattisesti. Jokainen varastokappale voidaan vahvistaa mobiililaitteessa. | 
| Kappaleiden enimmäismäärä     | Käytettävissä keräilytyössä, jos kappalekeräilyn vahvistus on otettu käyttöön. Määrittää rajan vahvistettavien kappaleiden määrälle. |  

