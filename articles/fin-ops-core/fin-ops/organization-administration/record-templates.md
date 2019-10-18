---
title: Yleistä tietuemalleista
description: Tässä artikkelissa esitellään tietuemallien käsite ja tietuemallien käyttäminen tietoja jakavien tietueiden luomisessa.
author: pvillads
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a8f924a5c2dad45d2006240230b85592d56e676
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177623"
---
# <a name="record-templates-overview"></a>Yleistä tietuemalleista

[!include [banner](../includes/banner.md)]

Tässä artikkelissa esitellään tietuemallien käsite ja tietuemallien käyttäminen tietoja jakavien tietueiden luomisessa.

Tietuemallien avulla voit luoda tietueita nopeammin, mutta voit luoda tietuemalleja vain joillekin tietuetyypeille.

Esimerkki: Kuvittele, että syötät autonvuokrausta koskevia tietoja autonvuokrausyritykselle, joka sijaitsee San Franciscossa. Koska suurin osa asiakkaista asuu todennäköisesti San Franciscon alueella, olisi mukavaa, jos voisit täyttää automaattisesti arvot kentille **Osavaltio**, **Maa** ja **Kaupunki** vuokrauslomakkeessa.

> [!NOTE]
> Voit kohdistaa malleja vain alueisiin, joiden käyttöoikeus sinulla on. Kaikkien mallien otsikot ovat kuitenkin näkyvissä, kun luot uuden tietueen. Ne näkyvät myös muille käyttäjille, jos luot kaikkien käyttäjien käytettävissä olevia malleja. Varmista, että huomioit tämän nimetessäsi malleja. Älä esimerkiksi käytä nimiä, jotka sisältävät sanan "komissio", jos yrityksen joidenkin työntekijöiden palkka perustuu komissioihin ja tämä on luottamuksellista tietoa.

Jos lomakkeella, johon sinulla on käyttöoikeus, on yksi tai useampia malleja ja yrität luoda uuden tietueen lomakkeella, näkyville avautuu **Valitse malli kohteelle** -sivu. Kun valitset mallin luettelosta, järjestelmä luo uuden tietueen, joka sisältää valitsemaasi malliin perustuvat oletustiedot. Jos et halua käyttää malleja uusien tietueiden luomiseen, valitse **Valitse malli kohteelle** -sivulla **Älä kysy uudelleen** -valintaruutu. Voit tuoda mallinvalintaikkunan uudelleen näkyviin napsauttamalla mitä tahansa tietuetta hiiren kakkospainikkeella, kun valitset **Tietueen tiedot** ja tämän jälkeen **Näytä mallivalinta**.
