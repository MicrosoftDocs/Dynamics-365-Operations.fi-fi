---
title: Varauksia ei voi poistaa, kun tilaus peruutetaan
description: 'Et voi peruuttaa myyntitilausta, ennen kuin siihen liittyvät työt on peruutettu ja palautettu. Voit tehdä tämän noudattamalla seuraavaa kolmea ohjetta:'
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
ms.openlocfilehash: a8d947e64568246dba5eff3c21fd3920b6494b73
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476239"
---
# <a name="reservations-cannot-be-removed-when-canceling-an-order"></a>Varauksia ei voi poistaa, kun tilaus peruutetaan

## <a name="symptoms"></a>Oireet

Jos myyntitilaukseen liittyy töitä ja yrität peruuttaa tilauksen, näyttöön tulee seuraava virhesanoma:

> Varauksia ei voi poistaa, koska luotuna on niistä riippuvaisia töitä.

Et voi peruuttaa myyntitilausta, ennen kuin työ on peruutettu ja palautettu. Tämä vaatimus on pätee, vaikka myyntitilaukseen liittyvä työ olisi suljettu.

## <a name="resolution"></a>Ratkaisu

Ongelma korjataan seuraavasti:

1. Peruuta työ ja siirrä varasto takaisin haluttuun sijaintiin. Siirry asianomaiseen myyntitilauksen kuormaan ja valitse joko **Vähennä kerättävää määrää** kuormarivillä tai **Palauta työ** toimintoruudussa.

    Työn tila on nyt *Peruutettu*, ja uusi varastosiirtotyö luodaan ja käsitellään automaattisesti, jotta varastonimikkeet palautetaan sijaintiin, joka kuvattiin palautuksen yhteydessä.

2. Poista kuorma. Myös lähetys poistetaan.

3. Nyt on pitäisi olla mahdollista siirtyä takaisin myyntitilaukseen ja perua se.
