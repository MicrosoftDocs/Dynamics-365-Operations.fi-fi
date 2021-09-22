---
title: Pakkausluetteloa ei voi peruuttaa sen jälkeen, kun se on kirjattu tilauksesta
description: Kun keräily- ja lähetysprosessit on otettu käyttöön varastonhallintajärjestelmässä, pakkausluettelo ei voi peruuttaa, kun se on kirjattu myyntitilauksesta. Tämä sivu tarjoaa kiertomahdollisuuden.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d20e66e2721560b8409eb63c3546a79adc188c7c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476281"
---
# <a name="cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Pakkausluetteloa ei voi peruuttaa sen jälkeen, kun se on kirjattu myyntitilauksesta

## <a name="symptoms"></a>Oireet

Kun keräily- ja lähetysprosessit on otettu käyttöön edistyneessä varastonhallintajärjestelmässä, pakkausluetteloa ei voi peruuttaa, kun se on kirjattu myyntitilauksesta.

## <a name="resolution"></a>Ratkaisu

Varastonhallintajärjestelmää käyttävien nimikkeiden kirjattujen pakkausluetteloiden korjaaminen edellyttää, että kirjaaminen tehdään kuormasta eikä tilauksesta. Microsoft on arvioinut ongelman ja määrittänyt, että se on ominaisuuden rajoitus.  

Yleisesti ottaen myyntitilauksen, joka on kerätty ja lähetetty varastonhallintaprosesseilla, pakkausluettelopäivitys voidaan tehdä kuormituksesta tai lähetyksestä ja itse myyntitilausasiakirjasta. Jos myyntitilauksen pakkausluettelopäivitys kuitenkin tehdään myyntitilausasiakirjasta, pakkausluettelon palautusta ei voi edelläänkään tehdä kuormasta tai myyntitilauksesta. Tämän vuoksi kannattaa käyttää pakkausluettelon kirjaamista kuormasta. Siinä tapauksessa kuormasta tehtävä peruutus otetaan käyttöön.
