---
title: Konsernin sisäisten asiakastietojen synkronoiminen
description: Tässä aiheessa käsitellään konsernin sisäisten tilausten asiakastietojen synkronointia
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
ms.openlocfilehash: 1949cb69f22ade6b0e03a02c93ad78e8b7e550ae
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672798"
---
# <a name="synchronize-intercompany-customer-information"></a>Konsernin sisäisten asiakastietojen synkronoiminen

[!include [banner](../../includes/banner.md)]

Asiakastiedot synkronoidaan, jos **Asiakastiedot**-kenttä on käytössä, kun myyntitilaus luodaan tai kun asiakasta, toimittajaviitettä tai asiakkaan tilausnumeroa muutetaan.

Näiden synkronointikenttien arvojen muuttaminen on aina mahdollista. Tämän parametrin valitseminen antaa kuitenkin vain mahdollisuuden määrittää, kopioidaanko arvo muihin konsernin sisäisiin tilaukseen. Jos olet ottanut **Asiakastiedot**-kentän käyttöön, konsernin sisäisen myyntitilauksen muutos synkronoidaan konsernin sisäiseen ostotilaukseen. Jos olet lisäksi ottanut käyttöön **Asiakastiedot**-kentän, tiedot synkronoidaan takaisin myös alkuperäiseen myyntitilaukseen.

> [!NOTE]
> Jos olet ottanut käyttöön **Asiakastiedot**-kentän käyttöön sekä konsernin sisäisessä ostotilauksessa että konsernin sisäisessä myyntitilauksessa, yhden yrityksen työntekijän tekemät muutokset korvataan toisen yrityksen työntekijän samaan tilaukseen tekemillä muutoksilla.

Parhaan käytännön mukaisesti **Asiakastiedot**-kenttä otetaan käyttöön konsernin sisäisessä ostotilauksessa. Tällä tavoin synkronointi otetaan käyttöön alkuperäisen myyntitilauksen ja konsernin sisäisen ostotilauksen välillä sekä konsernin sisäisestä ostotilauksesta konsernin sisäiseen myyntitilaukseen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
