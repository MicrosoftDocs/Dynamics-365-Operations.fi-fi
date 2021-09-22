---
title: Rekisterikilpeä ei voi siirtää, jos tyhjä varasto-otto ja tyhjä vastaanotto ovat sallittuna
description: Rekisterikilpeä ei voi siirtää, jos sarjanumerossa on tyhjä varasto-otto ja tyhjä vastaanotto sallittuna. Tämä korjataan tekemällä sarjanumerokentästä valinnainen.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0047f79aa417c8fc910447505f07963d014f54e7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476220"
---
# <a name="cant-move-license-plate-if-serial-number-has-blank-issue-and-blank-receipt-allowed"></a>Rekisterikilpeä ei voi siirtää, jos sarjanumerossa on tyhjä varasto-otto ja tyhjä vastaanotto sallittuna

## <a name="symptoms"></a>Oireet

Rekisterikilpeä ei voi siirtää **Siirto**-valikkovaihtoehdolla, jos sarjanumeron asetuksena seurantadimensioryhmässä on *Tyhjä varasto-otto sallitaan* ja *Tyhjä vastaanotto sallitaan* ja jos samassa sijainnissa on useita rekisterikilpiä, joista osalla on sarjanumero ja osalla ei.

## <a name="resolution"></a>Ratkaisu

Tämä ongelma korjataan muutoksilla, jotka otetaan käyttöön [KB 4571546:n](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687) avulla. Näillä muutoksilla **Sarjanumero**-kenttää muuttuu valinnaiseksi, kun tyhjä vastaanotto ja tyhjä varasto-otto sallitaan.
