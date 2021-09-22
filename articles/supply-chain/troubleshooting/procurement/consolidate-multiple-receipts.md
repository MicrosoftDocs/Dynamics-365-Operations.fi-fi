---
title: Et voi yhdistää useita tuotteiden vastaanottoja yhdeksi ostotilaukseksi
description: Useita tuotteiden vastaanottoja ei voi yhdistää yhdeksi ostotilaukseksi, jos eri tuotteiden vastaanottojen riveillä on eri kirjanpitopäivämäärät.
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
ms.openlocfilehash: 485306279281ceb55a140526f4216af35574af42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476197"
---
# <a name="you-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Et voi yhdistää useita tuotteiden vastaanottoja yhdeksi ostotilaukseksi

## <a name="symptoms"></a>Oireet

Useita tuotteiden vastaanottoja ei voi yhdistää yhdeksi ostotilaukseksi, jos eri tuotteiden vastaanottojen riveillä on eri kirjanpitopäivämäärät.

## <a name="resolution"></a>Ratkaisu

Aiemmissa  Dynamics 365 Supply Chain Managementin versioissa yhdistäminen sallittiin tässä tilanteessa. Käytäntö on kuitenkin altis virheille. Luotujen ostotilausrivien kirjanpitopäivämäärän ei pitäisi poiketa niiden tuotteen vastaanoton rivien kirjanpitopäivämäärästä, joiden perusteella ostotilausrivit luotiin. (Osto tilausrivien kirjanpitopäivämäärä vastaa ostotilauksen otsikon kirjanpitopäivämäärää.) Tämän vuoksi useiden tuotteiden vastaanottojen yhdistäminen yhdeksi ostotilaukseksi ei ole enää sallittua.

Kirjanpitopäivämäärää käytetään esimerkiksi budjettivarausten ja varausten osalta. Siksi se on säilytettävä siirryttäessä tuotteen vastaanotosta ostotilaukseen.
