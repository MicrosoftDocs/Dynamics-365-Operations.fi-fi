---
title: Commerce-keskustelumoduulin proaktiiviset keskusteluparametrit
description: Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Commercen Commerce-keskustelumoduulien ennakoivista keskusteluparametreista.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: f3cff89a25ff84414e7fdd32cbb26404c2080187
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691057"
---
# <a name="commerce-chat-module-proactive-chat-parameters"></a>Commerce-keskustelumoduulin proaktiiviset keskusteluparametrit

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan Customer Servicen monikanavan ja Commerce-keskustelun ja Power Virtual Agents -keskustelumoduulien Commerce-keskustelun ennakoivista keskusteluparametreista Microsoft Dynamics 365 Commercessa.

## <a name="proactive-chat-properties"></a>Ennakoivat keskusteluominaisuudet

Ennakoivat keskusteluominaisuudet sijaitsevat Customer Servicen monikanavan ja Commerce-keskustelun ja Power Virtual Agents -moduulien Commerce-keskustelun ominaisuusruudussa Commerce-sivuston muodostimessa.

> [!NOTE]
> Oletusarvoisesti kaikki ennakoivat keskusteluominaisuudet luettelossa ovat tyhjiä. Lue lisää ominaisuuksista ja määritä niitä vain tarpeen mukaan. Näin vähennetään virheellisien ennakoivien keskusteluiden käynnistymistä.

### <a name="proactive-chat"></a>Ennakoiva keskustelu

| Kutsumanimi | Kuvaus | Oletusarvo |
|---------------|-------------|---------------|
| Käytössä | Aktivoi asiakkaita ennakoivasti eri käynnistimien perusteella. | Ei käytössä |
| Keskustelun tervehdys | Tervehdyssanoma, jota käytetään, kun ennakoiva keskustelu käynnistyy. | Tyhjä |

### <a name="wait-time-proactive-chat"></a>Odotusaika (ennakoiva keskustelu)

| Kutsumanimi | Kuvaus |
|---------------|-------------|
| Odotusaika (sekuntia) | Aika (sekunteina), jonka sivuston käyttäjät viettävät sivustossa ennen ennakoivat keskustelun käynnistymistä. |
| Keskustelun tervehdys | Tervehdyssanoma, jota käytetään, kun ennakoiva keskustelu käynnistyy. |

### <a name="number-of-page-visits-proactive-chat"></a>Sivulla vierailujen määrä (ennakoiva keskustelu)

| Kutsumanimi | Kuvaus |
|---------------|-------------|
| Sivulla vierailujen määrä | Sivulla vierailujen määrä ennen ennakoivat keskustelun käynnistymistä. Sivuston käyttäjien on ensin hyväksyttävä eväste hyväksyntäbannerin kehotteessa. |
| Keskustelun tervehdys | Tervehdyssanoma, jota käytetään, kun ennakoiva keskustelu käynnistyy. |

### <a name="specific-pages-proactive-chat"></a>Tietyt sivut (ennakoiva keskustelu)

| Kutsumanimi | Kuvaus |
|---------------|-------------|
| Sivu(t) | Luettelo sivuista, jotka käynnistävät ennakoivan keskustelun vierailun jälkeen. |
| Keskustelun tervehdys | Tervehdyssanoma, jota käytetään, kun ennakoiva keskustelu käynnistyy. |

### <a name="from-specific-pages-proactive-chat"></a>Tietyiltä sivuilta (ennakoiva keskustelu)

| Kutsumanimi | Kuvaus |
|---------------|-------------|
| Sivu(t) | Luettelo sivuista, jotka käynnistävät ennakoivan keskustelun käyttäjän siirtyessä niiltä pois. |
| Keskustelun tervehdys | Tervehdyssanoma, jota käytetään, kun ennakoiva keskustelu käynnistyy. |

### <a name="specific-countryregion-proactive-chat"></a>Tietty maa/alue (ennakoiva keskustelu)

| Kutsumanimi | Kuvaus |
|---------------|-------------|
| Maakoodi | Määritetyissä maissa tai määritetyillä alueilla vierailevat käyttäjät käynnistävät ennakoivan keskustelun. Maa-/aluekoodien tulee olla kaksi isoa kirjainta (esimerkiksi **US**). |
| Keskustelun tervehdys | Tervehdyssanoma, jota käytetään, kun ennakoiva keskustelu käynnistyy. |

### <a name="date-range-proactive-chat"></a>Päivämääräalue (ennakoiva keskustelu)

| Kutsumanimi | Kuvaus |
|---------------|-------------|
| Aloituspäivä (pp/kk/vvvv) | Päivämäärä, jonka aikana tai jonka jälkeen ennakoiva keskustelu käynnistyy. |
| Päättymispäivä (pp/kk/vvvv) | Päivämäärä, jota ennen tai jonka aikana ennakoiva keskustelu käynnistyy. |
| Keskustelun tervehdys | Tervehdyssanoma, jota käytetään, kun ennakoiva keskustelu käynnistyy. |

### <a name="total-amount-in-cart-proactive-chat"></a>Ostoskorin kokonaissumma (ennakoiva keskustelu)

| Kutsumanimi | Kuvaus |
|---------------|-------------|
| Pienin arvo | Ostoskorin pienin rahasumma (sisältyvä), joka käynnistää ennakoivan keskustelun käyttäjien vieraillessa ostoskorisivulla. |
| Suurin arvo | Ostoskorin suurin rahasumma (sisältyvä), joka käynnistää ennakoivan keskustelun käyttäjien vieraillessa ostoskorisivulla. |
|Keskustelun tervehdys | Tervehdyssanoma, jota käytetään, kun ennakoiva keskustelu käynnistyy. |

### <a name="total-number-of-items-in-cart-proactive-chat"></a>Ostoskorin nimikkeiden kokonaismäärä (ennakoiva keskustelu)

| Kutsumanimi | Kuvaus |
|---------------|-------------|
| Pienin arvo | Nimikkeiden vähimmäismäärä (sisältyvä), joka käynnistää ennakoivan keskustelun käyttäjien vieraillessa ostoskorisivulla. |
| Suurin arvo | Nimikkeiden enimmäismäärä (sisältyvä), joka käynnistää ennakoivan keskustelun käyttäjien vieraillessa ostoskorisivulla. |
| Keskustelun tervehdys | Tervehdyssanoma, jota käytetään, kun ennakoiva keskustelu käynnistyy. |

### <a name="specific-products-in-cart-proactive-chat"></a>Ostoskorin tietyt tuotteet (ennakoiva keskustelu)

| Kutsumanimi | Kuvaus |
|---------------|-------------|
| Tuotetunnus/varastointiyksikkö | Niiden tuotetunnusten/varastointiyksikkönumeroiden luettelo, jotka käynnistävät ennakoivan keskustelun käyttäjien vieraillessa ostoskorisivulla. |
| Keskustelun tervehdys | Tervehdyssanoma, jota käytetään, kun ennakoiva keskustelu käynnistyy. |

## <a name="additional-resources"></a>Lisäresurssit

[Commerce-keskusteluominaisuuksien yleiskatsaus](commerce-chat-overview.md)

[Commerce-keskustelu ja Customer Servicen monikanava -moduuli](commerce-chat-module.md)

[Commerce-keskustelu ja Power Virtual Agents -moduuli](chat-module-pva.md)
