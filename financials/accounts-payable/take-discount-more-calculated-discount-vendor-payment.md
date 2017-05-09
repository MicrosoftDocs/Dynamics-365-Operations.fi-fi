---
title: "Alennuksen käyttäminen, jonka summa on suurempi kuin toimittajan maksulle laskettu alennus"
description: "Tässä artikkelissa käydään läpi skenaario, jossa käteisalennuksen summa on suurempi kuin alennus, joka oli alunperin käytettävissä laskussa. Tämä skenaario on mahdollinen, jos organisaatio sopii toimittajan kanssa laskun summaa pienemmän summan maksamisesta."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 22ba73681faa509a5144517163cc173a1267a534
ms.lasthandoff: 03/31/2017


---

# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a>Alennuksen käyttäminen, jonka summa on suurempi kuin toimittajan maksulle laskettu alennus

[!include[banner](../includes/banner.md)]


Tässä artikkelissa käydään läpi skenaario, jossa käteisalennuksen summa on suurempi kuin alennus, joka oli alunperin käytettävissä laskussa. Tämä skenaario on mahdollinen, jos organisaatio sopii toimittajan kanssa laskun summaa pienemmän summan maksamisesta. 

Toimittaja 3051 antaa Fabrikamille 4 prosentin käteisalennuksen, jos lasku maksetaan seitsemän päivän kuluessa. April syöttää 29. kesäkuuta 1 000,00 arvoisen laskun. Toimittaja sallii Aprilin käyttää 60,00:n arvoista alennusta laskulle saatavilla olevan oletusalennuksen sijaan, joka on 40,00. April kirjaa kertamaksun käyttämällä Ostoreskontran maksukirjauskansiota. Hän syöttää maksulle toimittajan ja avaa sitten **Selvitä tapahtumat** -sivun. Hän merkitsee laskun ja muuttaa **Käteisalennussumma**-kentän arvoksi **60,00**.
| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valittu | Normaali            | Var-10040 | 3051    | 29.6.2015 | 29.7.2015 | 10040   | 1 000,00                       | USD      | 940,00           |

Alennustiedot näkyvät **Selvitä tapahtumat** -sivun alaosassa.
|                              |           |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 12.7.2015 |
| Käteisalennussumma         | 60,00     |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | 60,00     |

April kirjaa maksukirjauskansion. Lasku selvitetään täysin käyttäen 940,00 arvoista maksua ja 60,00 arvoista alennusta.




