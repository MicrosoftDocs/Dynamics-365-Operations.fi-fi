---
title: Puolivuotiskauden poistomenetelmä -metodologia
description: Tässä artikkelissa kuvataan menetelmä, jota käyttöomaisuus käyttää poiston laskennassa puolivuotisen sopimuksen avulla. Se laskee kuuden kuukauden poiston käyttöomaisuuserän ensimmäisen ja viimeisen vuoden huollon aikana.
author: moaamer
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: fac20f7a31eca7922ed079f9554437f28448620d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879592"
---
# <a name="half-year-depreciation-convention-methodology"></a>Puolivuotiskauden poistomenetelmä -metodologia

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä artikkelissa kuvaillaan menetelmää, jota käytetään käyttöomaisuudessa laskettaessa poistot puolivuotisen sopimuksen avulla. Puolivuotinen sopimus laskee kuuden kuukauden poiston käyttöomaisuuserän ensimmäisen ja viimeisen vuoden aikana. Lisätietoja poistomenetelmistä kohdassa [Poistomenetelmät ja -käytännöt](Fixed-asset-depreciation-conventions.md). 

Kun käytät kuuden kuukauden poistomenetelmää, järjestelmä käyttää hankintavuotta tai vuotta, jolloin käyttö omaisuuserä on otettu käyttöön, laskee sen jälkeen viiden vuoden poiston kyseiselle vuodelle ja lisää summaan kuusi kuukautta. Tämän prosessin havainnollistamiseksi on otettava huomioon käyttöomaisuus, jonka hankintahinta on 50 000 ja joka on otettu käyttöön vuoden 2020 huhtikuussa. Oletetaan myös, että käyttöomaisuuserän käyttöikä on viisi vuotta.

Ensimmäinen huoltovuosi päättyy joulu kuussa 2020, mikä tarkoittaa, että käyttöomaisuuserän viiden vuoden käyttöikä päättyy vuoden 2024 joulukuussa. Puolen vuoden poistomenetelmä lisää käyttöomaisuuserän käyttöikään kuusi kuukautta, mikä tarkoittaa, että sen käyttöikä päättyy vuoden 2025 kesäkuussa. 

> Vuosittainen poisto 50 000/5 = 10 000 kuukauden poisto 10 000/12 = 833,33 <br>
> Ensimmäisen vuoden poisto 10 000/2 = 5 000 ja sitä seuraava kuukausittainen poisto 5 000/9 = 555,56

   [![Puolen vuoden poistomenetelmän poistoaikataulu.](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)

Puolivuotisen sopimuksen lisäämät laajennetut poistokaudet lisäävät poistojen täsmällisempää jakautumista. Kuuden kuukauden menetelmä edustaa poistokuluja tasaisemmin. Se on hyödyllinen tuloslaskelman raportoinnissa.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
