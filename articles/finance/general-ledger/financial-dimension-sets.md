---
title: Taloushallinnon dimensioyhdistelmät
description: Tässä aiheessa kuvataan taloushallinnon dimensioyhdistelmiä ja muutamia niiden käytön optimointivihjeitä.
author: yukonpeegs
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ba11be028ebeea140df93e2a07dbb463402e3ef0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021825"
---
# <a name="financial-dimension-sets"></a>Taloushallinnon dimensioyhdistelmät

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan taloushallinnon dimensioyhdistelmiä ja muutamia niiden käytön optimointivihjeitä.

Dimensioyhdistelmä on tilattu luettelo taloushallinnon dimensioista, joita voidaan käyttää kirjanpitotietojen yhteenvetoon käyttäjän määrittämällä tavalla. Dimensioyhdistelmien ensisijainen käyttö on pääyhdistelmän määrittämiseen.

Ainoa vakiodimensioyhdistelmä on dimensioyhdistelmä, joka sisältää vain päätilin.

**Taloushallinnon dimensioyhdistelmät** -sivulla voit luoda ja hallita taloushallinnon dimensioyhdistelmiä.

## <a name="dimension-set-balances"></a>Dimension asettamat saldot

Dimensioyhdistelmällä voi olla saldoja, jotka perustuvat sen taloushallinnon dimensioihin. Saldot löytyvät kirjanpidosta ja perustuvat dimensioyhdistelmän määritykseen. Saldojen yhteenveto tehdään kirjanpitotietojen perusteella, jotta niiden suorituskykyä voidaan parantaa niiden noutaessa (esimerkiksi kun pääkirja luodaan).

## <a name="create-balances"></a>Luo saldot

**Luo saldot** -painikkeella voit alustaa sellaisen dimensioyhdistelmän saldot, jossa ei ole saldoja.

> [!NOTE]
> On suositeltavaa rajoittaa saldojen dimensioyhdistelmien määrää, koska saldopäivitykset vaikuttavat kaikkiin kirjanpidon kirjaustapahtumiin.

## <a name="update-balances"></a>Päivitä saldot

**Päivitä saldot** -painikkeella voit sisällyttää saldoihin viimeisimmän kirjanpidon kirjaustehtävän. Saldopäivitykset ovat kevyitä toimintoja. Niiden täytyy käsitellä vain kirjanpidon kirjaustehtävää, joka on tapahtunut edellisen päivityksen jälkeen.

> [!NOTE]
> Päätaseen näyttö pakottaa päivityksen varmistamaan, että näkyvillä olevat saldot ovat ajan tasalla. Kannattaa käyttää toistuvaa erätyötä, jotta useimmin käytettyjen dimensioyhdistelmien päivitykset ovat nopeita. Näin voit vähentää päätasaldoon kuluvaa aikaa, jonka käyttäjien on odotettava.

## <a name="rebuild-balances"></a>Muodosta saldot uudelleen

**Muodosta uudelleen saldot** -painikkeella voit luoda saldot uudelleen tyhjästä. Näin voit varmistaa, että ne vastaavat kirjanpidon tietoja. Saldojen uudelleenrakentaminen edellyttää paljon käsittelyä, eikä sitä yleensä tarvitse tehdä.

> [!NOTE]
> Jos tilanne on skenaario, jossa saldot täytyy rakentaa säännöllisesti uudelleen, on suositeltavaa ottaa yhteyttä asiakastukeen. Asiakastuen avulla voit selvittää, miksi saldot eivät vastaa kirjanpidon tietoja.

## <a name="clear-balances"></a>Tyhjennä saldot

**Poista saldot** -painikkeella voit poistaa saldot ja lopettaa mahdolliset lisäpäivitykset. Dimensioyhdistelmä ei enää vaikuta kirjanpidon kirjaustapahtumiin.

Lisätietoja on kohdassa [Taloudelliset dimensiot](financial-dimensions.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
