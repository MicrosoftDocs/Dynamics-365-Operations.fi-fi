---
title: Varaston täydennyksen vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varaston täydennystä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
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
ms.openlocfilehash: 8dfb58c9156df106f58dfdc0ee2e0ef8defb9d9f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263201"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="5e771-103">Varaston täydennyksen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="5e771-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e771-104">Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varaston täydennystä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="5e771-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="5e771-105">Näyttöön tulee myös seuraava virhesanoma: "Työtä %1 ei voi vapauttaa, koska siinä on keskeneräinen täydennystyö.</span><span class="sxs-lookup"><span data-stu-id="5e771-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5e771-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="5e771-106">Issue description</span></span>

<span data-ttu-id="5e771-107">Keräilytyö estetään riippuvaisen täydennystyön vuoksi.</span><span class="sxs-lookup"><span data-stu-id="5e771-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5e771-108">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="5e771-108">Issue resolution</span></span>

<span data-ttu-id="5e771-109">Jos aaltokysynnän täydennystä käytettäessä keräilysijainti on täydennettävä lähdetilauksen kysynnän täyttämistä varten, järjestelmä luo sekä täydennystyön että keräilytyön.</span><span class="sxs-lookup"><span data-stu-id="5e771-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="5e771-110">Se kuitenkin estää keräilytyön täydennystyön valmistumiseen saakka.</span><span class="sxs-lookup"><span data-stu-id="5e771-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="5e771-111">Tämä on tarkoituksellista, sillä keräilysijainnissa ie ole riittävästi varastoa ellei täydennystyö valmistu.</span><span class="sxs-lookup"><span data-stu-id="5e771-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="5e771-112">Suorita täydennystyö ja käsittele sitten keräilytyö.</span><span class="sxs-lookup"><span data-stu-id="5e771-112">Complete the replenishment work, and then process the picking work.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]