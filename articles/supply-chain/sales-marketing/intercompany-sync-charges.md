---
title: Konsernin sisäisten kulujen synkronoiminen
description: Tässä artikkelissa käsitellään konsernin sisäisten kulujen synkronointia
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e7b3de3d7da7be6c1c8b5c3842862e7bccd78277
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857283"
---
# <a name="synchronize-intercompany-charges"></a>Konsernin sisäisten kulujen synkronoiminen

[!include [banner](../../includes/banner.md)]

Kulut synkronoidaan vain konsernin sisäisen myyntitilauksen ja konsernin sisäisen ostotilauksen välillä, ja synkronointi tapahtuu aina.

Jos **Salli hinnan muokkaus** -kenttä on valittu konsernin sisäisessä ostotilauksessa tai myyntitilauksessa, kulu voidaan lisätä manuaalisesti konsernin sisäiseen myyntitilaukseen tai ostotilaukseen. Muussa tapauksessa se ei ole mahdollista.

Jos **Salli hinnan muokkaus** -kenttää ei ole valittu konsernin sisäisessä myyntitilauksessa, kulua ei voi lisätä manuaalisesti konsernin sisäiseen myyntitilaukseen.

Jos **Salli hinnan muokkaus** -kenttää ei ole valittu konsernin sisäisessä ostotilauksessa, kulua ei voi lisätä konsernin ostotilauksessa.

Jos **Salli hinnan muutos** -kenttä on otettu käyttöön sekä konsernin sisäisessä ostotilauksessa että konsernin sisäisessä myyntitilauksessa, kuluja voi lisätä molempiin tilauksiin. Tämä voi kuitenkin aiheuttaa sen, että kuluja lisätään virheellisesti.

Paras tapa välttää tämäntyyppiset ristiriidat on sallia kulujen lisääminen joko konsernin sisäiseen myyntitilaukseen tai konsernin sisäiseen ostotilaukseen, mutta ei molempiin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
