---
title: Jäljellä olevan määrän peruuttaminen siirtää ostotilauksen vahvistettuun tilaan
description: Jos jäännösmäärä peruutetaan ostotilauksessa, jossa muutoksenhallinta on otettu käyttöön, ostotilaus siirtyy tilaan Vahvistettu.
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
ms.openlocfilehash: 1d8b331bc5699487dff3491d65daa36293f3212f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476240"
---
# <a name="cancelling-delivery-remainder-moves-purchase-order-to-a-confirmed-state"></a>Jäljellä olevan määrän peruuttaminen siirtää ostotilauksen vahvistettuun tilaan

## <a name="symptoms"></a>Oireet

Kun kyseessä on ostotilaus, johon sovelletaan muutoksenhallintaa ja ainoana muutoksena on jäännösmäärän peruuttaminen vähintään yhdellä rivillä, ostotilaus siirtyy suoraan *Vahvistettu*-tilaan, kun se hyväksytään, eikä kirjauskansiota luoda.

## <a name="resolution"></a>Ratkaisu

Jäännösmäärän peruuttaminen ei vaikuta vahvistuskirjauskansion sisältöön. Tätä toimintoa pitäisi käyttää, kun rivi on vastaanotettu osittain ja jäännösmäärän laatu on peruutettava prosessivaiheessa, joka seuraa toimittajan antamaa vahvistusta ostotilaukselle.

Jos tämän pitäisi näkyä ostotilausvahvistuksessa, määrää pitäisi muokata ostotilausrivillä, jotta vahvistusta vaaditaan. Jos rivillä ei taas ole vastaanotettu mitään, määrän voi poistaa. Tällöin vaaditaan uusi vahvistus.
