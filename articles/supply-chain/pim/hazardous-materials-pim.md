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
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: feee6b348ac1870295a894ad988278b23a3f30a3
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979037"
---
# <a name="hazardous-materials"></a><span data-ttu-id="166ff-103">Vaaralliset materiaalit</span><span class="sxs-lookup"><span data-stu-id="166ff-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="166ff-104">Vaarallisia aineita koskevat tiedot määritetään tuotetietojen hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="166ff-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="166ff-105">Tämä moduuli myös tarjoaa asiakirjoja, jotka voidaan tulostaa varastonhallinnan kautta.</span><span class="sxs-lookup"><span data-stu-id="166ff-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="166ff-106">Kun lähetät aineita, jotka luokitellaan vaaralliseksi tavaraksi, lähetysten mukana on toimitettava ylimääräistä paperityötä.</span><span class="sxs-lookup"><span data-stu-id="166ff-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="166ff-107">Vaarallisten aineiden toiminnon avulla asiakkaat voivat tallentaa luokittelutietoja ja liittää sen vapautettaviin nimikkeisiin.</span><span class="sxs-lookup"><span data-stu-id="166ff-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="166ff-108">Näitä tietoja voidaan sitten käyttää lähetysdokumentaation valmisteluun.</span><span class="sxs-lookup"><span data-stu-id="166ff-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="166ff-109">Microsoft Dynamics 365 Supply Chain Managementin vaarallisten aineiden toiminnot muodostavat hyödyllisten tuotetietokenttien ja liittyvien toimintojen kokoelman, joka auttaa kirjaamaan vaarallisiin tuotteisiin liittyviä tietoja ja viittaamaan niihin.</span><span class="sxs-lookup"><span data-stu-id="166ff-109">The hazardous materials features in Microsoft Dynamics 365 Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="166ff-110">Nämä toiminnot auttavat myös suunnittelemaan ja tulostamaan lähetysasiakirjoja, joissa on joitakin samoja tietoja lähetettävistä vaarallisista aineista.</span><span class="sxs-lookup"><span data-stu-id="166ff-110">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="166ff-111">Järjestelmä ei kuitenkaan automaattisesti takaa, että maan tai alueen kaikkia soveltuvia säädöksiä noudatetaan.</span><span class="sxs-lookup"><span data-stu-id="166ff-111">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="166ff-112">Vaikka nämä työkalut on tarkoitettu auttamaan yleisten määräysten noudattamisessa, ne eivät yksin riitä eikä ole takeita, että määräyksiä noudatetaan niiden avulla.</span><span class="sxs-lookup"><span data-stu-id="166ff-112">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="166ff-113">Organisaatio vastaa siitä, että se on tietoinen kaikissa käytössä olevista säädöksistä ja että se tekee tarvittavan niiden noudattamiseksi.</span><span class="sxs-lookup"><span data-stu-id="166ff-113">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

<span data-ttu-id="166ff-114">Ennen tämän toiminnon käyttöä on tehtävä seuraavat määritykset:</span><span class="sxs-lookup"><span data-stu-id="166ff-114">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="166ff-115">**Tuotetietojen hallinta:** Määritä koodit, joita voidaan soveltaa vapautettuihin tuotteisiin.</span><span class="sxs-lookup"><span data-stu-id="166ff-115">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="166ff-116">**Varastonhallinta:** Käytä ylimääräisiä lähetysasiakirjoja lähetystietojen tulostamiseen.</span><span class="sxs-lookup"><span data-stu-id="166ff-116">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="166ff-117">Tuotetietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="166ff-117">Product information management</span></span>

<span data-ttu-id="166ff-118">Tuotetietojen hallinnassa on määritystaulukkojen joukko, jossa voit lisätä viitetiedot, jotka annetaan vaarallisten tavaroiden luetteloissa maa-, ilma- ja vesikuljetuksia varten.</span><span class="sxs-lookup"><span data-stu-id="166ff-118">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="166ff-119">Tässä on joitakin säädöksiä, joihin usein viitataan:</span><span class="sxs-lookup"><span data-stu-id="166ff-119">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="166ff-120">**ADR** – Vaarallisten tavaroiden kansainväliseen maantiekuljetukseen liittyviä säädöksiä</span><span class="sxs-lookup"><span data-stu-id="166ff-120">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="166ff-121">**CFR 49** – Yhdysvaltojen vaarallisten tavaroiden kuljetusta koskevia säädöksiä</span><span class="sxs-lookup"><span data-stu-id="166ff-121">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="166ff-122">**IMDG** – Merenkulun kansainvälinen vaarallisten tavaroiden koodeksi (IMDG)</span><span class="sxs-lookup"><span data-stu-id="166ff-122">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="166ff-123">**IATA** – Kansainvälisin ilmakuljetusliiton (IATA) vaarallisten tavaroiden säädökset</span><span class="sxs-lookup"><span data-stu-id="166ff-123">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="166ff-124">Kussakin näistä säädöksistä on viitekoodeja sisältävät vaarallisten tavaroiden luettelo.</span><span class="sxs-lookup"><span data-stu-id="166ff-124">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="166ff-125">Kunkin kuljetustavan luettelot yhdistetään jaetuissa kansainvälisissä luokituksissa.</span><span class="sxs-lookup"><span data-stu-id="166ff-125">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="166ff-126">Supply Chain Management tarjoaa viitetaulukon näiden luettelojen jaetuille koodeille.</span><span class="sxs-lookup"><span data-stu-id="166ff-126">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="166ff-127">Kullakin luettelolla on myös joitakin yksilöllisiä koodeja, jotka voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="166ff-127">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="166ff-128">Voit aloittaa näiden tietojen määrittämisen luomalla säädöksen, jonka avulla voit määrittää alustavat parametrit.</span><span class="sxs-lookup"><span data-stu-id="166ff-128">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="166ff-129">Varastonhallinta</span><span class="sxs-lookup"><span data-stu-id="166ff-129">Warehouse management</span></span>

<span data-ttu-id="166ff-130">Lähetyksen valmistelun yhteydessä voi tulostaa useita uusia raportteja.</span><span class="sxs-lookup"><span data-stu-id="166ff-130">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="166ff-131">Näissä raporteissa käytetään tuotetietojen hallinnassa määritettyjä tietoja.</span><span class="sxs-lookup"><span data-stu-id="166ff-131">These reports use the information that you set up in Product information management.</span></span>
