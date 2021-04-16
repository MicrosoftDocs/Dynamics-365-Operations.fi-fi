---
title: Kustannustasodimension jäsenten yhdistäminen yhteiseen dimension jäsenten joukkoon
description: Yhdistämällä eri kustannustason dimension jäsenet joukoksi kustannustason dimensiojäsenet yhdistät tiedot yleiseen muotoon analyysitarkoituksiin.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember, CAMDimensionMapping
audience: Application User
ms.reviewer: roschlom
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3ce207b74c9515c72f4fce7680ee9eea50edd0f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810147"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>Kustannustasodimension jäsenten yhdistäminen yhteiseen dimension jäsenten joukkoon

[!include [banner](../includes/banner.md)]

Yhdistämällä eri kustannustason dimension jäsenet joukoksi kustannustason dimensiojäsenet yhdistät tiedot yleiseen muotoon analyysitarkoituksiin.

Maailmanlaajuisilla yrityksillä, jotka noudattavat lakisääteisiä vaatimuksia, voi olla useita tilikarttoja käytössä. Kun kustannustason dimension jäsenet tuodaan eri tilikartoista, lopputuloksena voi olla sekalainen tilijoukko. Tilit saattavat todellisuudessa olla samantyyppisiä, ja niiden kustannukset halutaan kohdistaa ja analysoida yhteisen muodon mukaisesti.

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>Kustannustason dimension jäsenten yhdistäminen yhteisen muodon mukaan
Seuraavassa esimerkissä esitetään, kuinka kustannusten vastuuhenkilö voi luoda uuden kustannustason dimension kustannuslaskentaan, joka yhdistää kustannustason dimension jäsenet Yhdysvaltojen tilikartan rakenteesta ja Ranskan tilikartan rakenteesta kustannustason dimension jäsenten yhteiseksi joukoksi. Kustannustason dimension jäsenten yhteistä joukkoa voidaan käyttää analysoitaessa kustannusten tietoja kahdesta yrityksestä kustannuslaskennan kirjanpidossa.

| Lähde: US Tilikartta                                          | Lähde: Ranska tilikartta                                          | Uusi kustannustason dimension jäsenten joukko                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Yhdysvaltojen tilikartasta tuodut kustannustason dimensiojäsenet | Ranskan tilikartasta tuodut kustannustason dimensiojäsenet | Yhdysvallan ja Ranskan yhdistetty kustannustason dimension jäsenten joukko |
| 5001: Myynti                                                           | 5001: Myynti ja mainonta                                               | 5000: Myynti ja mainonta                                             |
| 5030: Mainonta                                                     | 6390: Varasto-ostot\*                                                    | 7000: puhtaanapitokulut                                                 |
| 7001: puhtaanapitokulut                                               | 7001: Matkakulut                                                      | 7001: Matkakulut                                                   |

\* Varaston ostotilauksen kustannus Ranskan kustannustason dimension jäsenellä ei ole määritetty.

## <a name="currency-conversion"></a>Valuuttamuunnos
Eri tilikartat,, joita käytetään, voivat määrittää eri valuuttoja. Tässä tapauksessa muista määrittää valuuttamuunnoksen, jolloin kustannustiedot käsitellään oikeassa valuutassa,määritetyn kustannuslaskennan kirjanpidon mukaan jossa käytetään kustannustason dimensiojäsenet. Edellisessä esimerkissä, jos käytettyinä Yhdysvaltain dollarin (USD) kustannuslaskennan kirjanpitoon, sinun on luotava valuutan muuntaminen USD-euro (EUR) tapahtumien käsittelyyn yhdistetyille kustannustason dimensiojäsenet.

## <a name="update-mappings-at-any-time"></a>Päivitä yhdistämiset koska tahansa
Voit päivittää yhdistetyt kustannustason dimension määritykset milloin tahansa. Määritykset eivät ole päivämääräpohjaisia, koska muutokset vaikuttavat seuraavan kerran, kun käsittelet kustannustapahtumat tai suorittaa kustannuslaskelman.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]