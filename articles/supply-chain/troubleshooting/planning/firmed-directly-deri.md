---
title: Suoraan johdetut vahvistetut tilaukset käsitellään tarkistustyönkulussa.
description: Suoraan johdetut vahvistetut tilaukset käsitellään työnkulussa, jonka tilana on Tarkistettavana.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026481"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Suoraan johdetut vahvistetut tilaukset käsitellään tarkistustyönkulussa.

Tietopankin numero: 4612450

## <a name="symptoms"></a>Oireet

Suoraan johdetut vahvistetut tilaukset käsitellään työnkulussa, jonka tilana on *Tarkistettavana*.

## <a name="resolution"></a>Ratkaisu

Kun muutosten seuranta on käytössä, *Tarkistettavana*-tila on määritetty vahvistetuille johdetuille tilauksille (alihankintaostotilaukset). Jos ostotilaus on johdettu (alihankintaostotilaus), se lähetetään vain työnkulkuun. Jos ostotilaus on vahvistettu suunniteltu ostotilaus, se hyväksytään automaattisesti, jotta suunnittelumoduuli ei luo uusia suunniteltuja tilauksia ostotilauksen ollessa edelleen *Luonnos*-tilassa.
