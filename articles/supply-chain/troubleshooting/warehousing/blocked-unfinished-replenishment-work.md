---
title: Keräystyö estynyt keskeneräisen täydennystyön vuoksi
description: Keräilytyö voi olla estynyt riippuvaisen täydennystyön vuoksi. Suorita täydennystyö ja käsittele sitten keräilytyö.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 53b50d1e3e2d7bb64e78514affe80076ddcb9052
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476274"
---
# <a name="picking-work-cant-be-unblocked-because-of-unfinished-replenishment-work"></a>Keräystyön estoa ei voi poistaa keskeneräisen täydennystyön vuoksi

## <a name="symptoms"></a>Oireet

Kun käytetään kysynnän aaltotäydennystä, keräystyö voi estyä riippuvaisen täydennystyön vuoksi. Jos keräilysijainti on täydennettävä lähdetilauksen kysynnän täyttämistä varten, järjestelmä luo sekä täydennystyön että keräilytyön. Se kuitenkin estää keräystyön, kunnes täydennystyö on suoritettu, ja seuraava virhesanoma tulee näkyviin:

> Työn %1 estoa ei voi avata, koska siihen liittyy keskeneräisiä täydennystöitä.

## <a name="resolution"></a>Ratkaisu

Tämä on tarkoituksellista, sillä keräilysijainnissa ie ole riittävästi varastoa ellei täydennystyö valmistu. Suorita täydennystyö ja käsittele sitten keräilytyö.
