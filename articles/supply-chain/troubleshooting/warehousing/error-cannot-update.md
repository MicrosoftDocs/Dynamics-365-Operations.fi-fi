---
title: Virhe tapahtuu, kun sijainti valitaan keräysluettelon rekisteröinnin aikana
description: Virhe tapahtuu, kun sijainti valitaan keräysluettelon rekisteröinnin aikana.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: da5905fb7ed1e890c85e891843379aa07de3279bd8972d6fc57136aa703c9ea4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762791"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a>Virhe tapahtuu, kun sijainti valitaan keräysluettelon rekisteröinnin aikana

Tietopankin numero: 4613106

## <a name="symptoms"></a>Oireet

Tämä ongelma ilmenee, kun järjestelmä on määritetty varaamaan myyntitilaukset automaattisesti. Jos yrität valita keräysluettelon rekisteröintirivin sijainnin, näkyviin tulee seuraava virhesanoma käytettäessä varastonhallinnan (WMS) varausprosesseja:

> Määrää ei voi päivittää uusilla dimensioilla

Tämä ongelma voi ilmetä, koska käytettävissä oleva varasto ei riitä määritettyyn sijaintiin.

## <a name="resolution"></a>Ratkaisu

Järjestelmä käyttäytyy suunnitellulla tavalla.

Varastotason varausprosessia käytettäessä, jos käyttövarastoa ei varata kaikille varastodimensiotasoille eikä käyttövarastoa ole tarpeeksi määritetyssä sijainnissa, on suositeltavaa käyttää keräilyrivin manuaalista varausprosessia. Tämän jälkeen voit jakaa kaikkien käytettävissä olevien varastomäärien alemmat varaukset, kuten sijainnin, *Varaa erä* -toiminnolla.
