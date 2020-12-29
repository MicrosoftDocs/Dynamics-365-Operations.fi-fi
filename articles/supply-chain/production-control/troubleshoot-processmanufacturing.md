---
title: Prosessivalmistuksen vianmääritys
description: Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita prosessivalmistuksen käytössä voi esiintyä.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 63993fca2164301d31dbfa1474a4cf5eb16273e6
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516771"
---
# <a name="troubleshoot-process-manufacturing"></a>Prosessivalmistuksen vianmääritys

Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita prosessivalmistuksen käytössä voi esiintyä.

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a>Kun työkorttilaitetta käytetään raportoimaan osittainen määrä tuotantotilauksen viimeisessä työssä, kaikki kyseisen tilauksen aiemmat työt, joiden tilana on keskeneräinen, päättyvät automaattisesti.

Tämä on suunniteltu ominaisuus. **Ilmoita valmiiksi** -välilehden **Tuotantotilauksen oletusarvot** -sivulla on **Tee reitityksen loppumerkintä** -niminen vaihtoehto. Jos tämän aiheen asetuksena on *Kyllä*, reittikortin kirjauskansio kirjataan kun työntekijä käyttää työkorttilaitetta ja työkorttipäätettä viimeisimmän toiminnon ilmoittamiseen. Tämä kirjauskansio kirjaa kaikki toiminnot valmiiksi ja lopettaa kaikki tuotantotyöt. Kun **Tee reitityksen loppumerkintä** -asetuksena on *Kyllä*, järjestelmä ei ota huomioon työn tilaa, jonka työntekijä valitsi, kun tämä ilmoitti viimeisimmän toiminnon. Järjestelmä ei myöskään ota huomioon, ilmoittaako työntekijä täyden vai osittaisen määrän.

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a>Kun varaston sulkemista yritetään, seurauksena on seuraava varoitussanoma: Jälkikustannuslaskentaa ei suoriteta päivämäärällä %1, jolla kohdistuskauden loppu on rekisteröity.

Jos versiota 10.0.13 edeltävissä versioissa ei käytetä lean-tuotannon kustannuslaskentaan, seuraava virheellinen varoitussanoma annetaan varastoa suljettaessa:

> Olet sulkemassa varaston päivämäärällä %1. Jälkikustannuslaskentaa ei suoriteta päivämäärällä %1, jolla kohdistuskauden loppu on rekisteröity. Muista suorittaa jälkikustannuslaskentaa päivämäärällä %1, jolla kohdistuskausi päättyy. Varastojen arvostus, myytyjen tuotteiden kustannukset ja varianssit eivät ehkä ole oikein alareskontrassa tai kirjanpidossa, kunnes tämä on suoritettu.

Tämä ongelma on korjattu versiosta 10.0.13 alkaen. Lisätietoja on artikkelissa [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).
