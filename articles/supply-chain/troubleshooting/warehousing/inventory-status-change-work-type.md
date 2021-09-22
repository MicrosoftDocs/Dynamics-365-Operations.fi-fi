---
title: Varaston tilan muutosta ei voi valita työlajiksi
description: Et voi luoda työmalliriviä varaston tilanmuutokselle, koska tätä työlajia käyttävät vain järjestelmäprosessit. Valitse toinen työtyyppi.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ad7f26f3235d15779583f9cdadeb4e6dca16242a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476262"
---
# <a name="cant-select-inventory-status-change-in-the-work-type-column"></a>Varaston tilan muutosta ei voi valita Työlaji-sarakkeessa

## <a name="symptoms"></a>Oireet

Kun määrität Microsoft Dynamics 365 Supply Chain Managementia, seuraava virhesanoma saattaa avautua:

> Et voi luoda työmalliriviä varaston tilanmuutokselle, koska tämä työlaji ei ole kelvollinen. Valitse toinen työtyyppi.

## <a name="resolution"></a>Ratkaisu

Tämä on suunniteltu ominaisuus. Vain järjestelmäprosessit käyttävät *Varaston tilanmuutos* -työtyyppiä. Sitä ei voi määrittää. Koska työtyyppiluettelo on korjattu luettelointina, lisäkohteita ei voi suodattaa pois avattavasta **Työtyyppi**-valikosta.
