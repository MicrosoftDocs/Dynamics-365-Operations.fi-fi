---
title: Yksi riveistä on jo kuormassa
description: Tällä sivulla selitetään, miksi virhesanoma "Yksi riveistä on jo kuormassa. Varastoon vapautus ei onnistu." virhesanoma on voinut ilmetä ja miten ongelma korjataan.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0bdfaed005b9c58f7bd5f87dd6dffe648de47261
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476278"
---
# <a name="one-of-the-lines-is-already-on-a-load"></a>Yksi riveistä on jo kuormassa

## <a name="symptoms"></a>Oireet

Kun käytät kuormanluontia ja lähetyksiä, voit saada seuraavan virhesanoman:

> Yksi riveistä on jo kuormassa. Vapautus varastoon ei onnistu.

Jos kuormat luodaan manuaalisesti tai jos prosessi määritetään siten, että kuormat on jo luotu ennen myyntitilausrivin kirjaamista, oletuksena on, että seuraava vapautus tehdään manuaalisesti ja että käytössä on kuorman reititys ja hinnoittelu.

Mahdollinen on myös skenaario, jossa varastoon yritetään tehdä automaattinen vapautus mutta aaltoprosessi ei luo työtä. Tämän vuoksi luodaan kuitenkin avoin lähetys tai kuorma. Tämä avoin lähetys tai kuorma estää seuraavat yritykset vapauttaa tilaus automaattisesti siihen asti, että avoin lähetys tai kuorma poistetaan tai aalto käsitellään uudelleen manuaalisesti.

## <a name="resolution"></a>Ratkaisu

Vapautus voidaan tehdä myyntitilaussivulta tai automaattinen vapautus myyntitilauksen vapautussivulta vain siinä tapauksessa, että yhtään kuormaa ei ole ennen vapautusta varastoon. Kuorma luodaan automaattisesti aallon käsittelyn jälkeen.
