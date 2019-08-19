---
title: Yhden tositteen ja valuutan uudelleenarvostuksen päivittäminen
description: Jotkin organisaatiot kirjaavat kirjauskansioita, jotka sisältävät yhden tositteen, jolla on useampi asiakas tai toimittaja, ja käyttävät myös myynti- tai ostoreskontran ulkomaanvaluutan uudelleenarvostusprosessia. Tässä ohjeaiheessa kuvataan vaiheet, joita näiden organisaatioiden tulee seurata päivittäessään Microsoft Dynamics 365 for Operationsin versioon 1611.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b76354d0b8bb89e09e861e013a0c680c36b6537d
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851678"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="5126d-104">Yhden tositteen kirjauskansioiden ja valuutan uudelleenarvostusten päivittäminen</span><span class="sxs-lookup"><span data-stu-id="5126d-104">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5126d-105">Jotkin organisaatiot kirjaavat kirjauskansioita, jotka sisältävät yhden tositteen, jolla on useampi asiakas tai toimittaja, ja käyttävät myös myynti- tai ostoreskontran ulkomaanvaluutan uudelleenarvostusprosessia.</span><span class="sxs-lookup"><span data-stu-id="5126d-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="5126d-106">Tässä ohjeaiheessa kuvataan vaiheet, joita näiden organisaatioiden tulee seurata päivittäessään Microsoft Dynamics 365 for Operationsin versioon 1611.</span><span class="sxs-lookup"><span data-stu-id="5126d-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="5126d-107">Tee päivitys Microsoft Dynamics 365 for Operationsin versioon 1611 seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="5126d-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="5126d-108">Ennen kuin päivität Dynamics 365 for Operationsiin, suorita ulkomaanvaluutan uudelleenarvostusprosessi myynti- ja ostoreskontralle.</span><span class="sxs-lookup"><span data-stu-id="5126d-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="5126d-109">Määritä **Tapa**-kentän arvoksi **Laskupäivämäärä**.</span><span class="sxs-lookup"><span data-stu-id="5126d-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="5126d-110">Järjestelmä luo uudelleenarvostustapahtuman, joka kumoaa edellisen ulkomaanvaluutan uudelleenarvostuksen.</span><span class="sxs-lookup"><span data-stu-id="5126d-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="5126d-111">Siksi avoimet tapahtumat arvostetaan niiden alkuperäisessä kirjanpitovaluutassa.</span><span class="sxs-lookup"><span data-stu-id="5126d-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="5126d-112">Päivitys Dynamics 365 for Operationsin versioon 1611.</span><span class="sxs-lookup"><span data-stu-id="5126d-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="5126d-113">Aja ulkomaanvaluutan uudelleenarvostus uudelleen osto- ja myyntireskontrassa.</span><span class="sxs-lookup"><span data-stu-id="5126d-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="5126d-114">Aseta tällä kertaa **Tapa**-kentän arvoksi **Vakio**.</span><span class="sxs-lookup"><span data-stu-id="5126d-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="5126d-115">Järjestelmä luo uuden uudelleenarvostustapahtuman, joka perustuu nykyisiin vaihtokursseihin.</span><span class="sxs-lookup"><span data-stu-id="5126d-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="5126d-116">Tähän tapahtumaan tallennetaan toteutumaton voitto/tappio ja oikea reskontrakirjanpitotili.</span><span class="sxs-lookup"><span data-stu-id="5126d-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>




