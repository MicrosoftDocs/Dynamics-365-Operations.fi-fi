---
title: Sijaintiprofiili ei salli negatiivista varastoa, mutta negatiivinen käytettävissä oleva varasto sallitaan
description: Sijaintiprofiilin Salli negatiivinen varasto -asetuksena on Ei, mutta järjestelmä sallii silti negatiivisen käytettävissä olevan varaston.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026471"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a>Sijaintiprofiili ei salli negatiivista varastoa, mutta negatiivinen käytettävissä oleva varasto sallitaan

Tietopankin numero: 4613622

## <a name="symptoms"></a>Oireet

Sijaintiprofiilin **Salli negatiivinen varasto** -asetuksena on *Ei*, mutta järjestelmä sallii silti negatiivisen käytettävissä olevan varaston.

## <a name="example-scenario"></a>Esimerkkiskenaario

Valtion sääntelemien tapahtumien osalta järjestelmän on pystyttävä kirjaamaan negatiivinen varasto tappioiden kirjaamista varten. Haluat, että nimikkeellä voi olla negatiivinen varasto, mutta vain määritetyissä sijainneissa, kuten säiliöissä. Jos nimikemalliryhmä sallii negatiivisen varaston, sillä ei ole väliä, onko sijainti määritetty sallimaan negatiivinen varasto. Jos nimike on määritetty niin, että negatiivinen varasto ei ole sallittu, sijaintiprofiilin asetukset eivät vaikuta siihen.

## <a name="resolution"></a>Ratkaisu

Sijaintiprofiilin **Salli negatiivinen varasto** -asetus koskee vain varastoprosesseja, kuten keräilyä. Kuitenkin nimikkeen malliryhmät, jotka on asetettu sallimaan negatiivinen varasto, vaikuttavat kaikkiin inventoinnin- ja varastonhallintamoduuleihin, eikä sijaintiprofiili ohita asetusta.

Voit määrittää, saako varasto käyttää negatiivista varastoa. Määritä nimikemalliryhmät estämään negatiivinen fyysinen varasto ja määritä vain asianmukainen varasto sallimaan negatiivinen varasto.
