---
title: Kuormariviä ei voi luoda virheellisten varastodimensioiden vuoksi
description: Kun yrität vapauttaa palautusmyyntitilauksen varastoon, saatat saada virhesanoman virheellisistä varastodimensioista. Poista nämä tilausriviltä.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b02408b61b07b272a7e7d52004dc2492d60ef28c
ms.sourcegitcommit: 0d14c4a1e6cf533dd20463f1a84eae8f6d88f71b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119209"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Palautuksen myyntitilauksen kuormitusriviä ei voi luoda virheellisten varastodimensioiden vuoksi

## <a name="symptoms"></a>Oireet

Kun yrität vapauttaa palautusmyyntitilauksen varastoon, saatat saada seuraavan virhesanoman:

> Et voi luoda tälle tilausriville kuormariviä, koska se sisältää virheellisiä varastodimensioita. Et voi viitata varastodimensioihin, jotka sijaitsevat varaushierarkiassa sijaintidimension alla. Poista virheelliset dimensiot tilausriviltä.

## <a name="resolution"></a>Ratkaisu

Tuote ei valitettavasti tue myynnin palautusprosessin kuorman käsittelyä. Niinpä myyntitilauksen palautusta ei voi vapauttaa varastoon.

Myyntitilaustapahtumissa ei voi viitata varastodimensioihin, jotka sijaitsevat varaushierarkiassa **Sijainti**-dimension alla. Ongelman ratkaisu on virheellisten dimensioiden poistaminen tilausriviltä.
