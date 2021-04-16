---
title: Varaston asetusten vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varastoja määritetään Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8d1ed8e3b6f13f83e3c870b17b423cf42ad0ecc1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828055"
---
# <a name="troubleshoot-warehouse-setup"></a><span data-ttu-id="ab332-103">Varaston asetusten vianmääritys</span><span class="sxs-lookup"><span data-stu-id="ab332-103">Troubleshoot warehouse setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab332-104">Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varastoja määritetään Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="ab332-104">This topic describes how to fix common issues that you might encounter while you set up warehouses in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-use-any-role-except-administrator-to-access-the-mobile-device-app-emulator"></a><span data-ttu-id="ab332-105">Mobiililaitteen sovelluksen emulaattoria voi käyttää vain, kun roolina on järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="ab332-105">I can't use any role except administrator to access the mobile device app emulator.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ab332-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="ab332-106">Issue description</span></span>

<span data-ttu-id="ab332-107">Järjestelmänvalvojan rooli on ainoa, jolla mobiililaitteen sovelluksen emulaattoria voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="ab332-107">You can't any use role except the administrator tole to access the mobile device app emulator.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ab332-108">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ab332-108">Issue resolution</span></span>

<span data-ttu-id="ab332-109">Mobiililaitteen sovelluksen emulaattori on määritetty käytettäväksi vain järjestelmänvalvojan tilillä.</span><span class="sxs-lookup"><span data-stu-id="ab332-109">The mobile device app emulator is set to work only with the administrator account.</span></span> <span data-ttu-id="ab332-110">Testausta ja julkistamisprosessia varten kannattaa käyttää varsinaista varastonhallinnan mobiilisovellusta.</span><span class="sxs-lookup"><span data-stu-id="ab332-110">For all testing and live process purposes, we recommend that you use the Warehouse Management mobile app itself.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]