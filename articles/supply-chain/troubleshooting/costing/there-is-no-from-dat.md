---
title: Päivämäärästä-arvoa ei ole Nimikkeen hinta -sivun Aktiiviset hinnat -välilehdessä
description: Päivämäärästä-arvoa ei ole Nimikkeen hinta -sivun Aktiiviset hinnat -välilehdessä.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026488"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>Päivämäärästä-arvoa ei ole Nimikkeen hinta -sivun Aktiiviset hinnat -välilehdessä

Tietopankin numero: 4613548

## <a name="symptoms"></a>Oireet

**Päivämäärästä-arvoa** ei ole **Nimikkeen hinta** -sivun **Aktiiviset hinnat** -välilehdessä.

## <a name="resolution"></a>Ratkaisu

Odottavassa hinnassa määritettyä **Päivämäärästä**-arvoa (voimaantulopäivämäärä) ei siirretä aktiiviseen hintaan.

Kun nimikkeen kustannustietue lisätään ensimmäisen kerran, sen tila on *Odottaa* ja siinä on voimaantulopäivämäärä. Kun aktivoit nimikkeen kustannustietueen, tilaksi päivitetään *Aktiivinen* ja voimaantulopäivä päivitetään aktivointipäiväksi. Siksi aktiivisen hinnan aktivointipäivämäärä on aina todellinen aktivointipäivämäärä.

Lisätietoja on kohdassa [Kustannuslaskelmaversiot](../../cost-management/costing-versions.md).
