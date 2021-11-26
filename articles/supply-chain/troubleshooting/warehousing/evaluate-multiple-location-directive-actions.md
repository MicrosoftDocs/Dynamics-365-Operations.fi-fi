---
title: Arvioi kaikki useiden varastointiyksiköiden sijaintidirektiivien toiminnot
description: Uusi ominaisuus on lisätty arvioimaan kaikki useiden varastointiyksikön sijaintidirektiivien toiminnot. Tämä sivu opastaa hankkimaan tietoja sen käyttöönotosta.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea265166902f85c2c09cae08ee6de5cd7094e1b4
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778399"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Usean varastointiyksikön vaihtoehto ei arvioi usean sijaintidirektiivin toimintoja

## <a name="symptoms"></a>Oireet

*Myyntitilaus*-työtilaustyötyypin ja *Asetus*-työtyypin sijaintidirektiivit eivät arvioi usean sijaintidirektiivin toimintoja, kun **Useita varastointiyksiköitä** -vaihtoehto on valittu. Vain ensimmäinen sijaintidirektiivin toiminto arvioidaan.

## <a name="resolution"></a>Ratkaisu

Versioon 10.0.15 on lisätty uusi toiminto, *Arvioi kaikki usean varastointiyksikön sijaintidirektiivien toiminnot* (katso [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Tämä toiminto arvioi kaikki usean varastointiyksikön sijaintidirektiivien toiminnot. Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä. Järjestelmänvalvojat voivat tarkistaa [Ominaisuuksien hallinta](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -sivulla toiminnon tilan sekä ottaa sen käyttöön tai poistaa sen käytöstä tarvittaessa.
