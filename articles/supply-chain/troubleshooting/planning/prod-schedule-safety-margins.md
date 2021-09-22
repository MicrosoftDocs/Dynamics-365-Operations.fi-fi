---
title: Tuotannon ajoituksessa ei huomioida varmuusmarginaaleja
description: Tuotannon ajoitus ei ota huomioon varmuusmarginaaleja, jotka on määritetty tarvekohdistetun nimikkeen kattavuudessa
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 738296b7570ded0a4ee806e4445204a68e6a08c8
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476207"
---
# <a name="production-scheduling-doesnt-consider-the-safety-margins"></a>Tuotannon ajoituksessa ei huomioida varmuusmarginaaleja

## <a name="symptoms"></a>Oireet

Pääsuunnittelu ottaa varmuusmarginaalit huomioon. Varmuusmarginaalit kuitenkin ohitetaan, kun suunnittelut tuotantotilaukset ajoitetaan.

## <a name="resolution"></a>Ratkaisu

Marginaalit otetaan huomioon vain pääsuunnittelun aikana mutta ei manuaalisen ajoituksen aikana. Marginaalit suunnitellaan toimimaan puskureina suunnitteluvaiheen aikana tuomaan varsinaiseen prosessiin pelivaraa.

Halutun tuloksen saa poistamalla marginaalin. Reititys on päivitettävä sisältämään toivottu aika (esimerkiksi jonotusaikana): Pääsuunnittelun ja manuaalisen ajoituksen tuloksen pitäisi sitten olla sama.
