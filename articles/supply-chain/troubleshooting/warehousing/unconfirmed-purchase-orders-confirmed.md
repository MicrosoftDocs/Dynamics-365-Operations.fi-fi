---
title: Tuotereseptien päivitystehtävä vahvistaa vahvistamattomia tilauksia
description: Kun Päivitä tuotereseptit on suoritettu, järjestelmä vahvistaa vahvistamattomat tilaukset, joiden tilana on Rekisteröity. Tutustu ominaisuuteen, joka korjaa tämän ongelman.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 171a978efc6b55b92f429381e72036cb1b3296c6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476193"
---
# <a name="unconfirmed-purchase-orders-are-confirmed-after-running-update-product-receipts"></a>Vahvistamattomat ostotilaukset vahvistetaan tuotteen vastaanottojen päivittämisen jälkeen

## <a name="symptoms"></a>Oireet

Kun olet suorittanut kausittaisen *Päivitä tuotteen vastaanotot* -tehtävän, järjestelmä vahvistaa automaattisesti vahvistamattomat ostotilaukset, joiden varastotapahtuman tila on *Rekisteröity*.

## <a name="resolution"></a>Ratkaisu

Uusi saapuvan kuorman käsittelyominaisuus *Kuormamäärien ylivastaanottaminen* korjaa tämän ongelman. Ota tämä ominaisuus käyttöön siirtymällä [Ominaisuuksien hallinta](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) -työtilaan ja ottamalla seuraavat ominaisuudet käyttöön alla olevassa järjestyksessä:

1. Liitä ostotilauksen varastotapahtumat kuorman kanssa
2. Kuormamääriä vastaanotettu liikaa

Lisätietoja on kohdassa [Kirjattujen tuotemäärien kirjaaminen ostotilauksiin](/dynamics365/supply-chain/warehousing/inbound-load-handling).
