---
title: Peruutetut ostotilaukset näkyvät työtilan luonnosluettelossa
description: Peruutetut ostotilaukset näkyvät ostotilausten valmistelutyötilan luonnosluettelossa
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f1dc23cd7e5b4b99cb7a9440d7d4666d8396511f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476250"
---
# <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-workspace"></a>Peruutetut ostotilaukset näkyvät työtilan luonnosluettelossa

## <a name="symptoms"></a>Oireet

Kun olet peruuttanut *Vahvistettu*-tilassa olleita ostotilauksia, peruutetut ostotilaukset näkyvät edelleen ostotilausluonnosten luettelossa **Ostotilausten valmistelu** -työtilassa.

## <a name="resolution"></a>Ratkaisu

Tämä ongelma ilmenee vain sellaisten ostotilausten osalta, joihin sovelletaan muutoksenhallintaa. Se johtuu siitä, että peruutus tulkitaan muutokseksi, joka on hyväksyttävä. Järjestelmä voi suorittaa hyväksynnän automaattisesti. siksi prosessina on peruutetun ostotilauksen lähettäminen hyväksymisen työnkulkuun, jotta se voi siirtyä *Hyväksytty*-tilaan. Tässä vaiheessa ostotilaus ei enää näy **Ostotilausten valmistelu** -työtilan ostotilausluonnosten luettelossa.
