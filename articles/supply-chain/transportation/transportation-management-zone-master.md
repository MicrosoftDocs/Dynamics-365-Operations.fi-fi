---
title: Kuljetustenhallinnan vyöhykkeen päätiedot
description: Tässä aiheessa käsitellään tapaa, jolla maantieteelliset sijainnit jaetaan kuljetustenhallinnassa vyöhykkeiksi.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSZoneMaster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-01-09
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 7347add052ec4a9540417a5aeea64ab623026954
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880735"
---
# <a name="transportation-management-zone-master"></a>Kuljetustenhallinnan vyöhykkeen päätiedot

[!include [banner](../includes/banner.md)]

Kuljetustenhallinnassa maantieteelliset sijainnit voidaan jakaa vyöhykkeiksi. Sijaintien jakamisesta vyöhykkeisiin on hyötyä seuraavissa:

- **Kuljetuksen hinnoittelun yksinkertaistaminen** – vyöhyketietoinen hinnoittelu voi olla yksinkertaisempaa kuin sijaintiin perustuva hinnoittelu etenkin silloin, kun kuljetussijainnit ovat hajallaan.
- **Kuormasuunnittelun optimointi** – kuormien konsolidointi vyöhykkeiden perusteella.
- **Reittisuunnittelun optimointi** – tiettyjen reittisuunnitelmien määrittäminen tiettyihin vyöhykkeisiin.

Vyöhykkeet määritetään kunkin vyöhykkeen määrittävän metatietokentän arvojen perustella. Tällaisia arvoja ovat esimerkiksi maa, postinumeroalue tai rahdinkuljetuspalvelu. Vyöhykemääritelmiä ei edellytetä, jos kuljetuksen hinnoittelussa ei käytetä vyöhykkeitä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
