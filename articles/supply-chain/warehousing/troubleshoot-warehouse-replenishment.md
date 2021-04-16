---
title: Varaston täydennyksen vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varaston täydennystä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
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
ms.openlocfilehash: 8940f729e1115405e8d6e50eccc92d9fffe37f3e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828079"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="92112-103">Varaston täydennyksen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="92112-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92112-104">Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varaston täydennystä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="92112-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="92112-105">Näyttöön tulee myös seuraava virhesanoma: "Työtä %1 ei voi vapauttaa, koska siinä on keskeneräinen täydennystyö.</span><span class="sxs-lookup"><span data-stu-id="92112-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="92112-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="92112-106">Issue description</span></span>

<span data-ttu-id="92112-107">Keräilytyö estetään riippuvaisen täydennystyön vuoksi.</span><span class="sxs-lookup"><span data-stu-id="92112-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="92112-108">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="92112-108">Issue resolution</span></span>

<span data-ttu-id="92112-109">Jos aaltokysynnän täydennystä käytettäessä keräilysijainti on täydennettävä lähdetilauksen kysynnän täyttämistä varten, järjestelmä luo sekä täydennystyön että keräilytyön.</span><span class="sxs-lookup"><span data-stu-id="92112-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="92112-110">Se kuitenkin estää keräilytyön täydennystyön valmistumiseen saakka.</span><span class="sxs-lookup"><span data-stu-id="92112-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="92112-111">Tämä on tarkoituksellista, sillä keräilysijainnissa ie ole riittävästi varastoa ellei täydennystyö valmistu.</span><span class="sxs-lookup"><span data-stu-id="92112-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="92112-112">Suorita täydennystyö ja käsittele sitten keräilytyö.</span><span class="sxs-lookup"><span data-stu-id="92112-112">Complete the replenishment work, and then process the picking work.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]