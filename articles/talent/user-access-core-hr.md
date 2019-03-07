---
title: Core HR:n käyttö onnistuu mutta Onboard- tai Attract-sovelluksen ei
description: Tässä ohjeaiheessa kerrotaan, miten voidaan ratkaista ongelma, jossa käyttäjä voi käyttää Microsoft Dynamics 365 for Talent Core HR:ää mutta ei Attract- tai Onboard-sovellusta.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304246"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="0c03e-103">Käyttäjä voi käyttää Core HR -sovellusta, mutta ei Onboard- tai Attract-sovellusta</span><span class="sxs-lookup"><span data-stu-id="0c03e-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0c03e-104">**Ympäristön tiedot**</span><span class="sxs-lookup"><span data-stu-id="0c03e-104">**Environment details**</span></span>

- <span data-ttu-id="0c03e-105">Käyttäjä A vastasi Microsoft Dynamics Lifecycle Servicesin (LCS) käyttöönotosta.</span><span class="sxs-lookup"><span data-stu-id="0c03e-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="0c03e-106">Käyttäjä A lisäksi käyttäjän B Microsoft Dynamics 365 for Talent Core HR:ään.</span><span class="sxs-lookup"><span data-stu-id="0c03e-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="0c03e-107">**Varasto-otto**</span><span class="sxs-lookup"><span data-stu-id="0c03e-107">**Issue**</span></span>

<span data-ttu-id="0c03e-108">Käyttäjä B voi käyttää Core HR:ää mutta ei Talent: Attract- tai Talent: Onboard -sovellusta.</span><span class="sxs-lookup"><span data-stu-id="0c03e-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="0c03e-109">Jos käyttäjä yrittää siirtyä **sovelluskokemukseen**, hän siirtyykin kokeiluympäristöön.</span><span class="sxs-lookup"><span data-stu-id="0c03e-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="0c03e-110">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="0c03e-110">**Solution**</span></span>

<span data-ttu-id="0c03e-111">Käyttäjälle B on määritettävä sen Microsoft PowerApps -ympäristön tarkasteluoikeudet, jonka käyttäjä A loi valmisteluprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="0c03e-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="0c03e-112">Lisätietoja on kohdan [Talentin valmistelu](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) osassa Ympäristön käyttöoikeuksien myöntäminen.</span><span class="sxs-lookup"><span data-stu-id="0c03e-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="0c03e-113">**Pitkäaikainen ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="0c03e-113">**Long-term solution**</span></span>

<span data-ttu-id="0c03e-114">Microsoft harkitsee soveltuvien Onboard- ja Attract-oikeuksien määrittämistä automaattisesti, kun käyttäjä lisätään Core HR:ään.</span><span class="sxs-lookup"><span data-stu-id="0c03e-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
