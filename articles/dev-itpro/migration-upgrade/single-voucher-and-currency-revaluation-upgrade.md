---
title: "Yhden tositteen ja valuutan uudelleenarvostuksen päivittäminen"
description: "Jotkin organisaatiot kirjaavat kirjauskansioita, jotka sisältävät yhden tositteen, jolla on useampi asiakas tai toimittaja, ja käyttävät myös myynti- tai ostoreskontran ulkomaanvaluutan uudelleenarvostusprosessia. Tässä ohjeaiheessa kuvataan vaiheet, joita näiden organisaatioiden tulee seurata päivittäessään Microsoft Dynamics 365 for Operations -versioon 1611."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2c3ab22adc36d836ace69f4fc39aaff1e1292429
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a><span data-ttu-id="f73eb-104">Yhden tositteen ja valuutan uudelleenarvostuksen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="f73eb-104">Single voucher and currency revaluation upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f73eb-105">Jotkin organisaatiot kirjaavat kirjauskansioita, jotka sisältävät yhden tositteen, jolla on useampi asiakas tai toimittaja, ja käyttävät myös myynti- tai ostoreskontran ulkomaanvaluutan uudelleenarvostusprosessia.</span><span class="sxs-lookup"><span data-stu-id="f73eb-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="f73eb-106">Tässä ohjeaiheessa kuvataan vaiheet, joita näiden organisaatioiden tulee seurata päivittäessään Microsoft Dynamics 365 for Operations -versioon 1611.</span><span class="sxs-lookup"><span data-stu-id="f73eb-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="f73eb-107">Toimi seuraavasti, kun asennat päivityksen Microsoft Dynamics 365 for Operations -versioon 1611.</span><span class="sxs-lookup"><span data-stu-id="f73eb-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="f73eb-108">Ennen kuin päivität Dynamics 365 for Operationsin, suorita ulkomaanvaluutan uudelleenarvostusprosessi myynti- ja ostoreskontralle.</span><span class="sxs-lookup"><span data-stu-id="f73eb-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="f73eb-109">Määritä **Tapa**-kentän arvoksi **Laskupäivämäärä**.</span><span class="sxs-lookup"><span data-stu-id="f73eb-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="f73eb-110">Järjestelmä luo uudelleenarvostustapahtuman, joka kumoaa edellisen ulkomaanvaluutan uudelleenarvostuksen.</span><span class="sxs-lookup"><span data-stu-id="f73eb-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="f73eb-111">Siksi avoimet tapahtumat arvostetaan niiden alkuperäisessä kirjanpitovaluutassa.</span><span class="sxs-lookup"><span data-stu-id="f73eb-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="f73eb-112">Päivitä Dynamics 365 for Operations -versioon 1611.</span><span class="sxs-lookup"><span data-stu-id="f73eb-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="f73eb-113">Aja ulkomaanvaluutan uudelleenarvostus uudelleen osto- ja myyntireskontrassa.</span><span class="sxs-lookup"><span data-stu-id="f73eb-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="f73eb-114">Aseta tällä kertaa **Tapa**-kentän arvoksi **Vakio**.</span><span class="sxs-lookup"><span data-stu-id="f73eb-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="f73eb-115">Järjestelmä luo uuden uudelleenarvostustapahtuman, joka perustuu nykyisiin vaihtokursseihin.</span><span class="sxs-lookup"><span data-stu-id="f73eb-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="f73eb-116">Tähän tapahtumaan tallennetaan toteutumaton voitto/tappio ja oikea reskontrakirjanpitotili.</span><span class="sxs-lookup"><span data-stu-id="f73eb-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>





