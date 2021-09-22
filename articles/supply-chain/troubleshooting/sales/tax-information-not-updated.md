---
title: Verotietoja ei päivitetä, jos myyntitilauksen sijaintia muutetaan
description: Jos toimipaikkaa, varastoa tai toimitusositetta muutetaan myyntitilauksen otsikossa, tapauksen verotietoja ei päivitetä riveillä. Tämä on tehtävä manuaalisesti.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 77a73a787ff8a174c575f3b4f75694ded45d5712
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476232"
---
# <a name="tax-information-isnt-updated-if-location-on-a-sales-order-header-is-changed"></a>Verotietoja ei päivitetä, jos myyntitilauksen otsikon sijaintia muutetaan

## <a name="symptoms"></a>Oireet

Jos toimipaikkaa, varastoa tai toimitusositetta muutetaan myyntitilauksen otsikossa, tapauksen verotietoja ei päivitetä riveillä.

## <a name="resolution"></a>Ratkaisu

Tämä on suunniteltu ominaisuus. Ongelma ilmenee, koska toimitusosoitetta, toimipaikkaa ja varastoa ei muuteta automaattisesti rivitasolla. Ne on päivitettävä manuaalisesti.
