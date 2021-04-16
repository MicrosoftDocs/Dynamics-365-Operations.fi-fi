---
title: Kuljetustenhallinnan tilat
description: Tässä aiheessa käsitellään kuljetuksen tilan luontia ja kyseisen tilan yhdistämistä rahdinkuljettajan tilaan.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3a2b9e50dddf0f015cdd3f16d6d93fcc03d464d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807605"
---
# <a name="transportation-management-statuses"></a>Kuljetustenhallinnan tilat

[!include [banner](../includes/banner.md)]

Määritä kuljetuksen tilan pääkoodit selventämään rahdinkuljettajien antamat koodit. Tällä tavoin rahdinkuljettajat voidaan integroida antamaan tila. Kuljetuksen päätilakoodille annettava kuljetuksen tila voi auttaa seuraamaan kuorman, lähetyksen tai kontin tilaa. Kuorman, lähetyksen tai kontin tietty kuljetuksen tila voidaan päivittää vain tietoja integroimalla eikä manuaalisesti käyttöliittymässä.

## <a name="create-a-transportation-status"></a>Kuljetuksen tilan luominen

Kuljetuksen tila luodaan seuraavasti:

1. Valitse **Kuljetustenhallinta \> Asetukset \> Kuljetuksen tilan päätiedot**.
1. Luo uudet kuljetuksen tilan päätiedot valitsemalla **Uusi**.
1. Kirjoita **Kuljetuksen tilan päätiedot** -kenttään yksilöivä kuljetuksen tilan koodi.
1. Valitse **Kuljetustyyppi**-kentässä kuljetuksen tyypiksi joko *Rahdinkuljettaja* tai *Keskus*.
1. Anna nimi ja kuljetuksen tila.
1. Sulje sivu.

## <a name="map-a-transportation-status-to-a-carrier-status"></a>Kuljetuksen tilan yhdistäminen rahdinkuljettajan tilaan

Kuljetuksen tila yhdistetään rahdinkuljettajan tilaan seuraavasti:

1. Valitse **Kuljetustenhallinta \> Asetukset \> Rahdinkuljettajat \> Rahdinkuljettajan kuljettajan tila**.
1. Yhdistä rahdinkuljettajan koodi kuljetuksen tilan pääkoodiin valitsemalla **Uusi**.
1. Valitse rahdinkuljettajan ja rahdinkuljetuspalvelun yksilöivä tunnus.
1. Valitse kuljetuksen tilakoodi, jonka haluat määrittää valitun lähetyksen rahdinkuljettajan koodille.
1. Anna lähetyksen rahdinkuljettajan käyttämä ulkoinen koodi.
1. Sulje sivu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]