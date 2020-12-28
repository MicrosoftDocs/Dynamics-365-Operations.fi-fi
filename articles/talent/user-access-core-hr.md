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
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a><span data-ttu-id="b9be9-103">Käyttäjä voi käyttää henkilöstöhallintosovellusta, mutta ei Onboardia tai Attractia</span><span class="sxs-lookup"><span data-stu-id="b9be9-103">User can access Human Resources but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b9be9-104">**Ympäristön tiedot**</span><span class="sxs-lookup"><span data-stu-id="b9be9-104">**Environment details**</span></span>

- <span data-ttu-id="b9be9-105">Käyttäjä A vastasi Microsoft Dynamics Lifecycle Servicesin (LCS) käyttöönotosta.</span><span class="sxs-lookup"><span data-stu-id="b9be9-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="b9be9-106">Käyttäjä A lisäsi käyttäjän B käyttäjäksi Microsoft Dynamics 365 Human Resources:ään.</span><span class="sxs-lookup"><span data-stu-id="b9be9-106">User A added user B as a user to Microsoft Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="b9be9-107">**Lähetä**</span><span class="sxs-lookup"><span data-stu-id="b9be9-107">**Issue**</span></span>

<span data-ttu-id="b9be9-108">Käyttäjä B voi käyttää Human Resourcesia mutta ei Talent: Attract- tai Talent: Onboard -sovellusta.</span><span class="sxs-lookup"><span data-stu-id="b9be9-108">User B can access Human Resources, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="b9be9-109">Jos käyttäjä yrittää siirtyä **sovelluskokemukseen**, hän siirtyykin kokeiluympäristöön.</span><span class="sxs-lookup"><span data-stu-id="b9be9-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="b9be9-110">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="b9be9-110">**Solution**</span></span>

<span data-ttu-id="b9be9-111">Käyttäjälle B on määritettävä sen Microsoft Power Apps -ympäristön tarkasteluoikeudet, jonka käyttäjä A loi valmisteluprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="b9be9-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="b9be9-112">Lisätietoja on kohdan [Talentin valmistelu](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) osassa Ympäristön käyttöoikeuksien myöntäminen.</span><span class="sxs-lookup"><span data-stu-id="b9be9-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="b9be9-113">**Pitkäaikainen ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="b9be9-113">**Long-term solution**</span></span>

<span data-ttu-id="b9be9-114">Microsoft harkitsee soveltuvien Onboard- ja Attract-oikeuksien määrittämistä automaattisesti, kun käyttäjä lisätään Human Resourceen.</span><span class="sxs-lookup"><span data-stu-id="b9be9-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Human Resources.</span></span>
