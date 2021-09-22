---
title: Käytettävissä olevaa varastoa ei oteta huomioon erä-yllä-nimikkeiden osalta
description: Jotkut paikoitusmallit eivät ota huomioon kulloinkin käytettävissä olevaa varastoa erä-yllä-nimikkeiden osalta. Erä- tai sarjanumeron on oltava määritettynä kysyntätilauksessa.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: df5642b32f5e053144230eab3dbcf633f526279a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476228"
---
# <a name="slotting-templates-dont-consider-on-hand-inventory-for-batch-above-items"></a>Paikoitusmallit eivät ota huomioon käytettävissä olevaa varastoa erä-yllä-nimikkeiden osalta

## <a name="symptoms"></a>Oireet

Paikannusmallit, joilla on *Ota huomioon käytettävissä oleva varasto* -paikkaehto, eivät ota huomioon nykyistä käytettävissä olevaa varastoa *erä-yllä*-nimikkeille. Ne ottavat se huomioon vain, jos eränumero on määritetty myyntitilausrivillä.

Kun käytät alla *erä-alla*-nimikkeitä, nykyistä käytettävissä olevaa varastoa pidetään oletettuna.

Lisätietoja on kohdassa [Varastopaikoitus](/dynamics365/supply-chain/warehousing/warehouse-slotting).

## <a name="resolution"></a>Ratkaisu

Paikannusmallin otsikko voidaan määrittää *Tilattu*-, *Varattu*- tai *Vapautettu*-kysyntästrategialle. *Tilattu*-kysyntästrategiassa käytetään samoja varaushierarkian vaatimuksia, jotka koskevat varauksen tai varastoon vapautuksen prosesseja. Siksi erä- tai sarjanumero on määritettävä kysyntätilaukseen (myynti- tai siirtotilaus) niiden nimikkeiden osalta, joissa on *erä-yllä*- tai *erä-alla*-varaushierarkia.

Vaihtoehtoisesti *Varattu*-kysyntästrategian avulla voidaan valita erä- tai sarjanumero, ennen kuin varaston paikannustarve luodaan.
