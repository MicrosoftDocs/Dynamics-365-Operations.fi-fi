---
title: Toimitusilmoituksen korjausta ei voi käsitellä
description: Jos yrität korjata toimitusilmoitusta, kun se on jo kirjattu, ilmenee virhe. Tällä sivulla kerrotaan, miten WMS-yhteensopivien nimikkeiden kirjattuja pakkausluetteloja korjataan.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bb0d827adff8abd8762bf2de844cad5574628e4b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476254"
---
# <a name="delivery-note-correction-cant-be-processed"></a>Toimitusilmoituksen korjausta ei voi käsitellä

## <a name="symptoms"></a>Oireet

Kirjattua toimitusilmoitusta ei voi peruuttaa, koska **Peruuta**-painike ei ole käytettävissä. Toimitusilmoitusta ei voi myöskään korjata. Jos yrität sitä, avautuu seuraava virhesanoma:

> Toimitusilmoituksen korjausta ei voi käsitellä. Toimitusilmoitus sisältää vain nimikkeet, jotka liittyvät varastonhallintaprosesseihin, koska toimitusilmoituksen korjaus ei tue niitä.

## <a name="resolution"></a>Ratkaisu

Varastonhallintajärjestelmää käyttävien nimikkeiden kirjattujen pakkausluetteloiden korjaaminen edellyttää, että kirjaaminen tehdään kuormasta eikä suoraan tilauksesta.
