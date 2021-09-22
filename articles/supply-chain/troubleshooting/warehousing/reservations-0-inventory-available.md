---
title: Varastovarauksia ei voi tehdä, koska käytettävissä on 0,00
description: Ilmenee virhe, jonka mukaan järjestelmä ei voi tehdä varauksia, koska varastossa on käytettävissä vain 0,00. Tämä ongelman syy on todennäköisesti avoin työ.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 75d72f7ee1bdecca5a087b75b1de9907b9d244ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476259"
---
# <a name="system-cant-make-reservations-because-000-are-available-in-the-inventory"></a>Järjestelmä ei voi tehdä varauksia, koska varastossa on käytettävissä 0,00

## <a name="symptoms"></a>Oireet

Tämä ongelma voi esiintyä, jos järjestelmä ei voi päivittää varastomäärää, koska varastotapahtumia, joilla on määritetyt dimensiot, ei ole tarpeeksi. Seuraava virhesanoma avautuu:

> Fyysinen varastosaldo Toimipaikka=%1, Varasto=%2, Varaston tila=käytettävissä, Eränumero=%3, Omistaja=%4: %5 ei voi varata, koska varastossa on vain 0,00 saatavana.

## <a name="resolution"></a>Ratkaisu

Tämä ongelman syy on todennäköisesti avoin työ. Voit joko suorittaa työn tai vastaanottaa ilman työn luontia. Varmista, että määrää ei ole varattu fyysisesti millään varastotapahtumalla. Nämä tapahtumat voivat esimerkiksi avata laatutilauksia, varastoestotilauksia tai toimitustilauksia.
