---
title: Ylläpitosopimuksen työnkulun yleiskuvaus
description: Tässä artikkelissa on yleiskuvaus ylläpitosopimuksen työnkulusta.
author: sorenva
ms.date: 05/07/2018
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c112e1816d7ede80e0e30fe318d159e22ab540b7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897426"
---
# <a name="subscription-workflow-overview"></a>Ylläpitosopimuksen työnkulun yleiskuvaus 

[!include [banner](../includes/banner.md)]


Olet vastuussa valoyrityksen ylläpitosopimuksista. Yrityksesi tarjoaa valotelineiden huollon ylläpitosopimuksia. Asiakas lähestyy yritystä ostaakseen valotelineen huollon ylläpitosopimuksen vuodeksi.

## <a name="setting-up-subscriptions"></a>Ylläpitosopimuksen määrittäminen

Ylläpitosopimuksen määrittäminen alkaa siitä, että luot ylläpitosopimusryhmän uudelle huoltosopimukselle tai tarkistat, että ylläpitosopimusryhmä on olemassa. Jos ylläpitosopimusryhmä on olemassa, se on määritettävä niin, että asiakasta laskutetaan kerran vuodessa ja että myyntituotto jaksotetaan kerran kuukaudessa. Lisätietoja nimikkeiden veroryhmien määrittämisestä on kohdassa [Ylläpitosopimusryhmien määrittäminen](set-up-subscription-groups.md).

Voit luoda ylläpitosopimuksen ylläpitosopimusryhmän luonnin jälkeen. Lisätietoja huollon ylläpitosopimusten luonnista on kohdassa [Huollon ylläpitosopimusten luominen ylläpitosopimusryhmästä](create-service-subscriptions-from-subscription-group.md).

## <a name="create-and-modify-subscription-transactions"></a>Ylläpitosopimustapahtumien luominen ja muokkaaminen

Ylläpitosopimuksen määrittämisen jälkeen voit luoda ylläpitosopimuksen maksutapahtuman ensimmäiselle laskutuskaudelle, joka on yksi vuosi. Tapahtumien tyyppi on **Säännöllinen**. Voit luoda siksi vain ylläpitosopimustapahtumia, joiden aloituspäivämäärä ja lopetuspäivämäärä vastaavat jaksoja, jotka on luotu aiemmin **Kausityypit**-lomakkeessa. Saat lisätietoja maksutapahtumista kohdasta [Ylläpitosopimuksen maksutapahtumien luominen](create-subscription-fee-transactions.md).

Muistat asiakkaan ylläpitosopimuksen määrittämisen jälkeen, että he neuvottelivat 10 prosentin alennuksen kaikista palvelutarjonnoista. Sinun on siis alennettava luomasi tapahtumamaksun hintaa.

Asiakas soittaa myöhemmin samana päivänä ja ilmoittaa, että samalla kun he yhä haluavat valotelineen huoltosopimuksen, he ovat aikeissa tuoda markkinoille uuden valotelineen myöhemmin tänä vuonna. Siksi he tarvitsevat huoltoa vain lokakuulle 2013 asti. Voit vähentää asiakkaan ylläpitosopimuskuukausien määrää luomalla uuden ylläpitosopimuksen maksutapahtuman, jonka tyyppi on **Vähennyspäivät**. Lisätietoja päivien vähentämisestä on kohdassa [Ylläpitosopimusmaksujen päivien vähentäminen](reduce-the-days-on-subscription-fees.md).

## <a name="invoice-and-accrue-subscription-transactions"></a>Ylläpitotapahtumien laskuttaminen ja jaksottaminen

Nyt ylläpitotapahtumien määritys on valmis ja voit laskuttaa ylläpitosopimuksen asiakkaalta. Lisätietoja ylläpitotilausten laskuttamisesta on kohdassa [Ylläpitosopimustapahtumien laskuttaminen](invoice-subscription-transactions.md).

Kaksi päivää myöhemmin asiakas soittaa ja haluaa ylläpitosopimuksen laskutettavan Yhdysvaltain dollareina eurojen sijaan. Luot siksi hyvityslaskun ja sen jälkeen uuden ylläpitotapahtuman oikeassa valuutassa. Lisätietoja ylläpitotilausten hyvityksistä on kohdassa [Ylläpitosopimustapahtumien hyvittäminen](credit-subscription-transactions.md).

Joka kuukauden lopussa jaksotat yhden kuukauden tuoton asiakkaan ylläpitosopimuksesta tulostilille ja KET-tileille. Lisätietoja ylläpitosopimusten tuottojen jaksottamisesta on kohdassa [Ylläpitosopimuksen tuoton jaksotus](accrue-subscription-revenue.md).

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]