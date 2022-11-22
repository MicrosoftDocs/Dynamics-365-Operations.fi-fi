---
title: Summa on suurempi kuin toimittajan maksulle laskettu alennus
description: Tässä artikkelissa käydään läpi skenaario, jossa käteisalennuksen summa on suurempi kuin alennus, joka oli alunperin käytettävissä laskussa. Tämä skenaario on mahdollinen, jos organisaatio sopii toimittajan kanssa laskun summaa pienemmän summan maksamisesta.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd74c6677f80a9075449908411350f1c81b95b02
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778354"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a>Summa on suurempi kuin toimittajan maksulle laskettu alennus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käydään läpi skenaario, jossa käteisalennuksen summa on suurempi kuin alennus, joka oli alunperin käytettävissä laskussa. Tämä skenaario on mahdollinen, jos organisaatio sopii toimittajan kanssa laskun summaa pienemmän summan maksamisesta. 

Toimittaja 3051 antaa Fabrikamille 4 prosentin käteisalennuksen, jos lasku maksetaan seitsemän päivän kuluessa. April syöttää 29. kesäkuuta 1 000,00 arvoisen laskun. Toimittaja sallii Aprilin käyttää 60,00:n arvoista alennusta laskulle saatavilla olevan oletusalennuksen sijaan, joka on 40,00. April kirjaa kertamaksun käyttämällä Ostoreskontran maksukirjauskansiota. Hän syöttää maksulle toimittajan ja avaa sitten **Selvitä tapahtumat** -sivun. Hän merkitsee laskun ja muuttaa **Käteisalennussumma**-kentän arvoksi **60,00**.

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valittu | Normaali            | Var-10040 | 3051    | 29.6.2020 | 29.7.2020 | 10040   | 1,000.00                       | USD      | 940,00           |

Alennustiedot näkyvät **Selvitä tapahtumat** -sivun alaosassa.

| Kenttä                        | Arvo     |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 12.7.2020 |
| Käteisalennussumma         | 60.00     |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | 60,00     |

April kirjaa maksukirjauskansion. Lasku selvitetään täysin käyttäen 940,00 arvoista maksua ja 60,00 arvoista alennusta.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
