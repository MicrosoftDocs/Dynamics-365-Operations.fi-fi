---
title: Varaston asetusten vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varastoja määritetään Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f2e111930431e908e5aaa2f08d04adbb2d952f0f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208108"
---
# <a name="troubleshoot-warehouse-setup"></a><span data-ttu-id="63b05-103">Varaston asetusten vianmääritys</span><span class="sxs-lookup"><span data-stu-id="63b05-103">Troubleshoot warehouse setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63b05-104">Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varastoja määritetään Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="63b05-104">This topic describes how to fix common issues that you might encounter while you set up warehouses in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-use-any-role-except-administrator-to-access-the-mobile-device-app-emulator"></a><span data-ttu-id="63b05-105">Mobiililaitteen sovelluksen emulaattoria voi käyttää vain, kun roolina on järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="63b05-105">I can't use any role except administrator to access the mobile device app emulator.</span></span>

### <a name="issue-description"></a><span data-ttu-id="63b05-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="63b05-106">Issue description</span></span>

<span data-ttu-id="63b05-107">Järjestelmänvalvojan rooli on ainoa, jolla mobiililaitteen sovelluksen emulaattoria voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="63b05-107">You can't any use role except the administrator tole to access the mobile device app emulator.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="63b05-108">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="63b05-108">Issue resolution</span></span>

<span data-ttu-id="63b05-109">Mobiililaitteen sovelluksen emulaattori on määritetty käytettäväksi vain järjestelmänvalvojan tilillä.</span><span class="sxs-lookup"><span data-stu-id="63b05-109">The mobile device app emulator is set to work only with the administrator account.</span></span> <span data-ttu-id="63b05-110">Testausta ja julkistamisprosessia varten kannattaa käyttää varsinaista varastosovellusta.</span><span class="sxs-lookup"><span data-stu-id="63b05-110">For all testing and live process purposes, we recommend that you use the warehouse app itself.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]