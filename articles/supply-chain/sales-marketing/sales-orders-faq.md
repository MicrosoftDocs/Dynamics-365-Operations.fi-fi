---
title: Myyntitilauksia koskevia usein kysyttyjä kysymyksiä
description: Tällä sivulla käsitellään usein kysyttyjä kysymyksiä, joita nousee esiin käytettäessä myyntitilauksia Dynamics 365 Supply Chain Managementissa.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d75022dcc476052040b16c9033cf5ff2a697ae6c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476219"
---
# <a name="sales-order-faqs"></a>Myyntitilauksen usein kysytyt kysymykset

Tällä sivulla käsitellään usein kysyttyjä kysymyksiä, joita nousee esiin käytettäessä myyntitilauksia Dynamics 365 Supply Chain Managementissa.

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Voinko linkittää ostotilauksen myyntitilaukseen kysynnän täyttämiseksi?

Voit luoda ostotilauksen myyntitilauksesta. Lisätietoja: [Ostotilauksen luominen myyntitilauksesta](/dynamics365/supply-chain/sales-marketing/tasks/create-purchase-order-sales-order).

## <a name="can-i-cancel-or-delete-a-sales-order-or-return-order"></a>Voinko peruuttaa tai poistaa myyntitilauksen tai palautustilauksen?

Voit peruuttaa vain myynti- ja palautustilauksia, jotka ovat tilassa *Luotu*. Lisätietoja: [Palautustilauksen peruuttaminen](/dynamics365/supply-chain/service-management/cancel-return-order).

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Voinko palauttaa poistetun laskutetun myyntitilauksen?

Jos laskutettu myyntitilaus poistettiin vahingossa, voit palauttaa sen tai tarkastella sen tietoja.

Valitse **Asiakastili \> Tapahtumat \> Alkuperäisasiakirja \> Tarkastele tietoja**. Etsi haluamasi lasku ja valitse se, jotta voit tarkastella sen tietoja. Näihin tietoihin sisältyvät myyntitilauksen viite. Myös myyntitilauksen tietojen käytön pitäisi olla mahdollista kyseiseltä sivulta.

## <a name="how-do-i-delete-orphaned-sales-order-records"></a>Miten poistan orvoiksi jääneitä myyntitilaustietueita?

Voit tyhjentää orvoksi jääneet myyntitilaustietueet suorittamalla säännöllisen *Myyntitilausten poisto* -tehtävän kummassa tahansa seuraavista paikoista:

- Myynti ja markkinointi \> Säännölliset tehtävät \> Tyhjennä \> Poista myyntitilaukset
- Vähittäismyynti ja kauppa \> Vähittäiskaupan ja kaupan IT \> Tyhjennä \> Poista myyntitilaukset

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Onko olemassa tapa laskea provisiot jo kirjatuista laskuista?

Supply Chain Management ei tällä hetkellä tue kirjattujen laskujen provisioiden laskemista.
