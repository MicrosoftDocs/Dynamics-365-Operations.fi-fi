---
title: Varastomäärää ei päivitetä riittämättömien tapahtumien vuoksi
description: Varastomäärää -1 % ei voida päivittää, koska nimikkeelle %2 ei ole riittävästi varastotapahtumia, joilla on määritetyt dimensiot.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88130a969039dd741c8ea4fbaabe81acf0e6fb6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476179"
---
# <a name="system-cant-update-inventory-quantity-because-of-insufficient-transactions"></a>Järjestelmä ei voi päivittää varastomäärää, koska tapahtumat eivät riitä

## <a name="symptoms"></a>Oireet

Tämä ongelma voi esiintyä, jos järjestelmä ei voi päivittää varastomäärää, koska varastotapahtumia, joilla on määritetyt dimensiot, ei ole tarpeeksi. Seuraava virhesanoma avautuu:

> Varastomäärää -%1 ei voi päivittää, sillä varastotapahtumia on liian vähän nimikkeelle %2 dimensioilla Koko=%3, Väri=%4, Lisäykset=%5, Toimipaikka=%6, Varasto=%7, Varasto=%8, Varaston tila=Käytettävissä, Rekisterikilpi=%9, Eränumero=%10 viitetunnusta %11 varten erätunnuksessa %12.

## <a name="resolution"></a>Ratkaisu

Varmista, että määrää ei ole varattu fyysisesti millään varastotapahtumalla. Nämä tapahtumat voivat esimerkiksi avata laatutilauksia, varastoestotilauksia tai toimitustilauksia.
