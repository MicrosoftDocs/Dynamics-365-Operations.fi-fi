---
title: Määritä automaattiset tuotesuositukset
description: Tämä menettely päivittää yksikkösäilän tiedot, joita käyttää tuotesuosituksista vastaava automaattianalyysijärjestelmää, ja ottaa sitten käyttöön tuotesuositukset myyntipisteiden asiakasohjelmissa.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BIMeasurementDeployManagementEntityStore, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 700af913f18e23c66db53a92033def06818af1ec
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "348523"
---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="4c00f-103">Määritä automaattiset tuotesuositukset</span><span class="sxs-lookup"><span data-stu-id="4c00f-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4c00f-104">Tämä menettely päivittää yksikkösäilän tiedot, joita käyttää tuotesuosituksista vastaava automaattianalyysijärjestelmää, ja ottaa sitten käyttöön tuotesuositukset myyntipisteiden asiakasohjelmissa.</span><span class="sxs-lookup"><span data-stu-id="4c00f-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="4c00f-105">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="4c00f-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="4c00f-106">Valitse Järjestelmän hallinta > Asetukset > Yksikkösäilö.</span><span class="sxs-lookup"><span data-stu-id="4c00f-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="4c00f-107">Etsi tietue "RetailSales" luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="4c00f-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="4c00f-108">Valitse Päivitä.</span><span class="sxs-lookup"><span data-stu-id="4c00f-108">Click Refresh.</span></span>
4. <span data-ttu-id="4c00f-109">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4c00f-109">Click OK.</span></span>
5. <span data-ttu-id="4c00f-110">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c00f-110">Close the page.</span></span>
6. <span data-ttu-id="4c00f-111">Siirry kohtaan Vähittäismyynti ja kauppa > Pääkonttorin asetukset > Parametrit > Vähittäismyyntiparametrit.</span><span class="sxs-lookup"><span data-stu-id="4c00f-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="4c00f-112">Valitse Automaattianalyysi-välilehti.</span><span class="sxs-lookup"><span data-stu-id="4c00f-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="4c00f-113">Valitse Ota tuotesuositukset käyttöön -kentän arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="4c00f-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="4c00f-114">Jos näyttöön tulee sanoma "Suositusmalleja ei voitu noutaa", se johtuu siitä, että olet päivittänyt yksikkösäilön hiljattain eikä järjestelmä ole vielä käsitellyt uusia tietoja.</span><span class="sxs-lookup"><span data-stu-id="4c00f-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="4c00f-115">Odota 2-3 tuntia ja yritä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="4c00f-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="4c00f-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4c00f-116">Click Save.</span></span>
10. <span data-ttu-id="4c00f-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c00f-117">Close the page.</span></span>

