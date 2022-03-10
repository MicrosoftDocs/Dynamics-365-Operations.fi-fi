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
ms.openlocfilehash: d20f1c1d6e8fc83dd996b04bf0321a41f7b39290f306d1ac9f4fcd17514832e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721172"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Suoraan johdetut vahvistetut tilaukset käsitellään tarkistustyönkulussa.

Tietopankin numero: 4612450

## <a name="symptoms"></a>Oireet

Suoraan johdetut vahvistetut tilaukset käsitellään työnkulussa, jonka tilana on *Tarkistettavana*.

## <a name="resolution"></a>Ratkaisu

Kun muutosten seuranta on käytössä, *Tarkistettavana*-tila on määritetty vahvistetuille johdetuille tilauksille (alihankintaostotilaukset). Jos ostotilaus on johdettu (alihankintaostotilaus), se lähetetään vain työnkulkuun. Jos ostotilaus on vahvistettu suunniteltu ostotilaus, se hyväksytään automaattisesti, jotta suunnittelumoduuli ei luo uusia suunniteltuja tilauksia ostotilauksen ollessa edelleen *Luonnos*-tilassa.
