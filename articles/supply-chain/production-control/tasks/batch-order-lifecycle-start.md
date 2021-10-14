---
title: Erän tilauksen elinkaari luomisesta käynnistämiseen
description: Tämä menettely käsittelee erätilauksen elinkaaren ensimmäistä osaa.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7ca259ca8f176cd5bc76081836adcb7d272972b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579253"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a>Erän tilauksen elinkaari luomisesta käynnistämiseen

[!include [banner](../../includes/banner.md)]

Tämä menettely käsittelee erätilauksen elinkaaren ensimmäistä osaa.

Luonnista, kustannusten arvioinnista ja ylituotantotyön ajoittamisesta erätilauksen todelliseen aloittamiseen.



Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. 



Jos menetelmä suoritetaan toisella tietojoukolla, edellytyksenä on, että vapautetussa tuotteessa on aktiviinen resepti- ja reittiversio.


## <a name="create-a-batch-order"></a>Erätilauksen luominen
1. Valitse Kaikki tuotantotilaukset.
2. Valitse Uusi erätilaus.
3. Syötä tai valitse arvo Nimiketunnus-kentässä.
4. Valitse Luo.
5. Suodata pikasuodattimella Tuotanto-kenttää arvolla b.

## <a name="view-production-formula-and-expected-co-products"></a>Näytä tuotantoresepti ja odotetut oheistuotteet
1. Valitse toimintoruudussa Tuotantotilaus.
2. Valitse Resepti.
3. Sulje sivu.
4. Valitse Oheistuotteet.
5. Sulje sivu.

## <a name="estimate-the-batch-order"></a>Arvioi erätilaus
1. Valitse Arvio.
2. Valitse OK.
3. Valitse toimintoruudussa Hallitse kustannuksia.
4. Valitse Näytä laskennan tiedot.
5. Sulje sivu.

## <a name="release-the-batch-order"></a>Vapauta erätilaus
1. Valitse toimintoruudussa Tuotantotilaus.
2. Valitse Vapauta.
3. Valitse OK.

## <a name="schedule-production-jobs"></a>Ajoita tuotantotyöt
1. Valitse toimintoruudussa Aikataulu.
2. Valitse Ajoita työt.
3. Valitse Rajallinen kapasiteetti -kentässä Ei.
4. Valitse Rajallinen materiaali -kentässä Ei.
5. Valitse OK.
6. Valitse toimintoruudussa Tuotantotilaus.
7. Valitse Kaikki työt.
8. Sulje sivu.

## <a name="start-the-batch-order"></a>Aloita erätilaus
1. Valitse Käynnistys.
2. Valitse Yleiset-välilehti.
3. Valitse Kirjaa keräysluettelo nyt -kentässä Ei.
4. Valitse OK.
5. Valitse toimintoruudussa Näytä.
6. Valitse Keräysluettelo.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Sulje sivu.
9. Sulje sivu.
10. Valitse Reitityskortti.
11. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
12. Sulje sivu.
13. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]