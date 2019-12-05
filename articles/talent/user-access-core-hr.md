---
title: Käyttäjä voi käyttää Core HR:ää, mutta ei Onboardia tai Attractia
description: Tässä ohjeaiheessa kerrotaan, miten voidaan ratkaista ongelma, jossa käyttäjä voi käyttää Microsoft Dynamics 365 Talent - Core HR:ää mutta ei Attractia tai Onboardia.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a86936d756d8375761ce50c9d9bf33dc638dfad
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772916"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a>Käyttäjä voi käyttää Core HR:ää, mutta ei Onboardia tai Attractia

[!include [banner](includes/banner.md)]

**Ympäristön tiedot**

- Käyttäjä A vastasi Microsoft Dynamics Lifecycle Servicesin (LCS) käyttöönotosta.
- Käyttäjä A lisäsi käyttäjän B käyttäjäksi Microsoft Dynamics 365 Talent: Core HR:ään.

**Lähetä**

Käyttäjä B voi käyttää Core HR:ää mutta ei Talent: Attract- tai Talent: Onboard -sovellusta. Jos käyttäjä yrittää siirtyä **sovelluskokemukseen**, hän siirtyykin kokeiluympäristöön.

**Ratkaisu**

Käyttäjälle B on määritettävä sen Microsoft Power Apps -ympäristön tarkasteluoikeudet, jonka käyttäjä A loi valmisteluprosessin aikana.

Lisätietoja on kohdan [Talentin valmistelu](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) osassa Ympäristön käyttöoikeuksien myöntäminen.

**Pitkäaikainen ratkaisu**

Microsoft harkitsee soveltuvien Onboard- ja Attract-oikeuksien määrittämistä automaattisesti, kun käyttäjä lisätään Core HR:ään.
