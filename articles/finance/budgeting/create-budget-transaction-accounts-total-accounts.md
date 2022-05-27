---
title: Budjetin luominen tapahtumatileistä ja summatileistä
description: Tässä artikkelissa on summatileihin perustuvien budjettien luontiprosessin yleiskatsaus. Artikkelissa kerrotaan myös, miten summatilien budjetin hallinta otetaan käyttöön, jos budjetin hallinta vaaditaan.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: kfend
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33f7e49c56a5780644023b6b4fdcbc0937f7f90b
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714394"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>Budjetin luominen tapahtumatileistä ja summatileistä

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on summatileihin perustuvien budjettien luontiprosessin yleiskatsaus. Artikkelissa kerrotaan myös, miten summatilien budjetin hallinta otetaan käyttöön, jos budjetin hallinta vaaditaan.

Sekä budjettisuunnitelman että budjettirekisterimerkinnän asiakirjat mahdollistavat budjetoinnin päätileillä, joiden päätilin tyyppi on **Yhteensä**. Toteutuneet summat voidaan kirjata vain tapahtumien päätileille. 

Määritä kausittaiselle **Muodosta budjettisuunnitelma kirjanpidosta** -prosessille **Lähde**-välilehdessä ehdoksi päätilin **Yhteensä**-tyyppi. Tässä tapauksessa kukin pääsummatili sisällytetään kohdebudjettisuunnitelmaan. Summa on sama kuin valittujen päätilien alueen kokonaissumma. 

Voit aktivoida **Yhteensä**-tyypin päätilien budjetin hallinnan. Tätä toimintoa tuetaan kaikkien budjettiryhmien käytössä. Jokaiselle pääsummatilille budjettiryhmän osalta hallittava budjetti pitää luoda **Budjetin hallinnan konfiguraatio **-sivulla. Määrittämiesi ehtojen on sisällettävä pääsummatili ja tilialue. Voit nopeuttaa budjettiryhmien luontiprosessia käyttämällä budjetin hallintaryhmien tietoyksikköä. 

Jos budjetointia käytetään raportoinnissa, esimerkiksi tilinpäätöksessä, summatilin budjettisumma sisältää seuraavat summat:

-   kullekin tapahtumakirjanpitotilille summatilin aikavälinä luodut budjetit
-   suoraan summatilille syötetty budjettisumma.

Näin voidaan luoda summatilin aikavälille erilliset budjetit tärkeimpiä tapahtumatilejä varten ja lisätä sitten käytettävissä oleva budjettisumma summatilille.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
