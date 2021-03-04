---
title: Käyttäjä voi käyttää henkilöstöhallintosovellusta, mutta ei Onboardia tai Attractia
description: Tässä ohjeaiheessa kerrotaan, miten voidaan ratkaista ongelma, jossa käyttäjä voi käyttää Microsoft Dynamics 365 Talent - Human Resourcesia mutta ei Attractia tai Onboardia.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461026"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a>Käyttäjä voi käyttää henkilöstöhallintosovellusta, mutta ei Onboardia tai Attractia

[!include [banner](includes/banner.md)]

**Ympäristön tiedot**

- Käyttäjä A vastasi Microsoft Dynamics Lifecycle Servicesin (LCS) käyttöönotosta.
- Käyttäjä A lisäsi käyttäjän B käyttäjäksi Microsoft Dynamics 365 Human Resources:ään.

**Lähetä**

Käyttäjä B voi käyttää Human Resourcesia mutta ei Talent: Attract- tai Talent: Onboard -sovellusta. Jos käyttäjä yrittää siirtyä **sovelluskokemukseen**, hän siirtyykin kokeiluympäristöön.

**Ratkaisu**

Käyttäjälle B on määritettävä sen Microsoft Power Apps -ympäristön tarkasteluoikeudet, jonka käyttäjä A loi valmisteluprosessin aikana.

Lisätietoja on kohdan [Talentin valmistelu](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) osassa Ympäristön käyttöoikeuksien myöntäminen.

**Pitkäaikainen ratkaisu**

Microsoft harkitsee soveltuvien Onboard- ja Attract-oikeuksien määrittämistä automaattisesti, kun käyttäjä lisätään Human Resourceen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]