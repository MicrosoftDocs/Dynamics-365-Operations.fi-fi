---
title: Pääsuunnittelu luo suunniteltuja tilauksia haamutuotteita varten
description: Suunnitellut tilaukset luodaan haamutuotteita varten pääsuunnittelun suorittamisen jälkeen.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f3170bcb723e2d7483258bb0ecf786e62f2aa3d196745074c2ac554bc212ec55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742001"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Pääsuunnittelu luo suunniteltuja tilauksia haamutuotteita varten

Tietopankin numero: 4614729

## <a name="symptoms"></a>Oireet

Suunnitellut tilaukset luodaan haamutuotteita varten pääsuunnittelun suorittamisen jälkeen.

## <a name="resolution"></a>Ratkaisu

Vapautettujen tuotteiden **Haamu**-vaihtoehdon asetus määrittää tuoterakenteen oletusrivityypin. Kun **Haamu**-asetuksena on *Kyllä*, järjestelmä luo nimikkeelle edelleen suunnitellut tilaukset, mutta kunkin suunnitellun tilauksen **Suoraan johdettava tarve** -asetuksena on *Kyllä*. Siksi suunniteltua tuotantotilausta ei voi vahvistaa erillään. Sen sijaan se sisällytetään aina automaattisesti, kun päätuotantotilaus on vahvistettu. Lisäksi suunnitellun haamutilauksen tuoterakennerivit sisällytetään päätuotantotilauksen tuoterakenteeseen.
