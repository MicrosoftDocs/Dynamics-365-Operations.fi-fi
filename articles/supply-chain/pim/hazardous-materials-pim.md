---
title: Vaaralliset materiaalit
description: Tässä ohjeaiheessa annetaan tietoa vaarallisten aineiden asiakirjoista ja tiedoista, jotka tallennetaan ympäristöösi.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5006f06d90ddcc314a51878e9e21337de7d493e7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208457"
---
# <a name="hazardous-materials"></a><span data-ttu-id="edcce-103">Vaaralliset materiaalit</span><span class="sxs-lookup"><span data-stu-id="edcce-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="edcce-104">Vaarallisia aineita koskevat tiedot määritetään tuotetietojen hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="edcce-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="edcce-105">Tämä moduuli myös tarjoaa asiakirjoja, jotka voidaan tulostaa varastonhallinnan kautta.</span><span class="sxs-lookup"><span data-stu-id="edcce-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="edcce-106">Kun lähetät aineita, jotka luokitellaan vaaralliseksi tavaraksi, lähetysten mukana on toimitettava ylimääräistä paperityötä.</span><span class="sxs-lookup"><span data-stu-id="edcce-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="edcce-107">Vaarallisten aineiden toiminnon avulla asiakkaat voivat tallentaa luokittelutietoja ja liittää sen vapautettaviin nimikkeisiin.</span><span class="sxs-lookup"><span data-stu-id="edcce-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="edcce-108">Näitä tietoja voidaan sitten käyttää lähetysdokumentaation valmisteluun.</span><span class="sxs-lookup"><span data-stu-id="edcce-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="edcce-109">Vaarallisten tavaroiden lähetysten hallintaa varten Microsoft Dynamics 365 Supply Chain Management antaa sinun määrittää tuotteisiin liittyviä ylimääräisiä viitetietoja.</span><span class="sxs-lookup"><span data-stu-id="edcce-109">To help manage shipments of dangerous goods, Microsoft Dynamics 365 Supply Chain Management lets you set up additional reference information that is related to products.</span></span> <span data-ttu-id="edcce-110">Voit myös määrittää ylimääräisiä toimitusasiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="edcce-110">You can also set up additional shipment documents.</span></span> <span data-ttu-id="edcce-111">Järjestelmä ei kuitenkaan ole automaattisesti maan tai alueen säädösten mukainen.</span><span class="sxs-lookup"><span data-stu-id="edcce-111">However, the system isn't automatically compliant with your country's or region's regulations.</span></span> <span data-ttu-id="edcce-112">Sen sijaan se on työkalu, joka voi auttaa ohjelmaa yleisellä tasolla.</span><span class="sxs-lookup"><span data-stu-id="edcce-112">Instead, it's a tool that can help your overall program.</span></span>

<span data-ttu-id="edcce-113">Ennen tämän toiminnon käyttöä on tehtävä seuraavat määritykset:</span><span class="sxs-lookup"><span data-stu-id="edcce-113">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="edcce-114">**Tuotetietojen hallinta:** Määritä koodit, joita voidaan soveltaa vapautettuihin tuotteisiin.</span><span class="sxs-lookup"><span data-stu-id="edcce-114">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="edcce-115">**Varastonhallinta:** Käytä ylimääräisiä lähetysasiakirjoja lähetystietojen tulostamiseen.</span><span class="sxs-lookup"><span data-stu-id="edcce-115">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="edcce-116">Tuotetietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="edcce-116">Product information management</span></span>

<span data-ttu-id="edcce-117">Tuotetietojen hallinnassa on määritystaulukkojen joukko, jossa voit lisätä viitetiedot, jotka annetaan vaarallisten tavaroiden luetteloissa maa-, ilma- ja vesikuljetuksia varten.</span><span class="sxs-lookup"><span data-stu-id="edcce-117">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="edcce-118">Tässä on joitakin säädöksiä, joihin usein viitataan:</span><span class="sxs-lookup"><span data-stu-id="edcce-118">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="edcce-119">**ADR** – Vaarallisten tavaroiden kansainväliseen maantiekuljetukseen liittyviä säädöksiä</span><span class="sxs-lookup"><span data-stu-id="edcce-119">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="edcce-120">**CFR 49** – Yhdysvaltojen vaarallisten tavaroiden kuljetusta koskevia säädöksiä</span><span class="sxs-lookup"><span data-stu-id="edcce-120">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="edcce-121">**IMDG** – Merenkulun kansainvälinen vaarallisten tavaroiden koodeksi (IMDG)</span><span class="sxs-lookup"><span data-stu-id="edcce-121">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="edcce-122">**IATA** – Kansainvälisin ilmakuljetusliiton (IATA) vaarallisten tavaroiden säädökset</span><span class="sxs-lookup"><span data-stu-id="edcce-122">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="edcce-123">Kussakin näistä säädöksistä on viitekoodeja sisältävät vaarallisten tavaroiden luettelo.</span><span class="sxs-lookup"><span data-stu-id="edcce-123">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="edcce-124">Kunkin kuljetustavan luettelot yhdistetään jaetuissa kansainvälisissä luokituksissa.</span><span class="sxs-lookup"><span data-stu-id="edcce-124">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="edcce-125">Supply Chain Management tarjoaa viitetaulukon näiden luettelojen jaetuille koodeille.</span><span class="sxs-lookup"><span data-stu-id="edcce-125">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="edcce-126">Kullakin luettelolla on myös joitakin yksilöllisiä koodeja, jotka voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="edcce-126">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="edcce-127">Voit aloittaa näiden tietojen määrittämisen luomalla säädöksen, jonka avulla voit määrittää alustavat parametrit.</span><span class="sxs-lookup"><span data-stu-id="edcce-127">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="edcce-128">Varastonhallinta</span><span class="sxs-lookup"><span data-stu-id="edcce-128">Warehouse management</span></span>

<span data-ttu-id="edcce-129">Lähetyksen valmistelun yhteydessä voi tulostaa useita uusia raportteja.</span><span class="sxs-lookup"><span data-stu-id="edcce-129">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="edcce-130">Näissä raporteissa käytetään tuotetietojen hallinnassa määritettyjä tietoja.</span><span class="sxs-lookup"><span data-stu-id="edcce-130">These reports use the information that you set up in Product information management.</span></span>
