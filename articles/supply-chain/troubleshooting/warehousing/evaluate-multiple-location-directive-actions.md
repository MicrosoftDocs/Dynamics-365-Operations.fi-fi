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
ms.openlocfilehash: 2d5f7cf548eb6c18d9700c73ef084f197b78542e
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102960"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Usean varastointiyksikön vaihtoehto ei arvioi usean sijaintidirektiivin toimintoja

## <a name="symptoms"></a>Oireet

*Myyntitilaus*-työtilaustyötyypin ja *Asetus*-työtyypin sijaintidirektiivit eivät arvioi usean sijaintidirektiivin toimintoja, kun **Useita varastointiyksiköitä** -vaihtoehto on valittu. Vain ensimmäinen sijaintidirektiivin toiminto arvioidaan.

## <a name="resolution"></a>Ratkaisu

Versioon 10.0.15 on lisätty uusi toiminto, *Arvioi kaikki usean varastointiyksikön sijaintidirektiivien toiminnot* (katso [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Tämä toiminto arvioi kaikki usean varastointiyksikön sijaintidirektiivien toiminnot. Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä.  Supply Chain Managementin versiosta 10.0.25 alkaen tämä toiminto on pakollinen, eikä sitä voi poistaa käytöstä. Järjestelmänvalvojat voivat tarkistaa [Ominaisuuksien hallinta](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -sivulla toiminnon tilan sekä ottaa sen käyttöön tai poistaa sen käytöstä tarvittaessa.
