---
title: Vaarallisten aineiden yleiskatsaus
description: Tässä ohjeaiheessa on sellaisten vaarallisten aineiden käsittelyyn ja dokumentointiin liittyvien toimintojen yleiskatsaus, joita käytetään tuotetietojen hallinnassa ja varastonhallinnassa.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 227111f4703d9dc381270382dcb796874d7de937
ms.sourcegitcommit: c009ec75f53872272f11c92a1ce81a391e3845a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/18/2020
ms.locfileid: "3699609"
---
# <a name="hazardous-materials-overview"></a><span data-ttu-id="43d51-103">Vaarallisten aineiden yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="43d51-103">Hazardous materials overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43d51-104">Lähetys- ja kuljetusmääräysten noudattaminen edellyttää, että organisaatiot, jotka lähettävät vaarallisiksi aineiksi luokiteltuja materiaaleja, sisällyttävät lähetyksiin lisäasiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="43d51-104">To remain compliant with shipping and transport regulations, organizations that ship materials that are classified as dangerous goods must include additional paperwork with their shipments.</span></span> <span data-ttu-id="43d51-105">Vaarallisten aineiden toiminnon avulla asiakkaat voivat tallentaa vapautettuihin nimikkeisiin liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="43d51-105">The hazardous materials feature lets customers store information that is related to released items.</span></span> <span data-ttu-id="43d51-106">Näitä tietoja voidaan sitten käyttää lähetysdokumentaation valmisteluun.</span><span class="sxs-lookup"><span data-stu-id="43d51-106">This information can then be used to help prepare shipping documentation.</span></span> <span data-ttu-id="43d51-107">Vaarallisia aineita lähettävälä organisaatiolla on oltava omat lähetysprosessin hallintaan käytettävät prosessit ja menettelytavat.</span><span class="sxs-lookup"><span data-stu-id="43d51-107">An organization that ships dangerous goods must have its own processes and procedures for managing the shipping process.</span></span> <span data-ttu-id="43d51-108">Microsoft Dynamics 365 Supply Chain Management on vain työkalu, joka auttaa tarvittavien asiakirjojen luonnissa.</span><span class="sxs-lookup"><span data-stu-id="43d51-108">Microsoft Dynamics 365 Supply Chain Management is just a tool that can help generate the required documents.</span></span>

<span data-ttu-id="43d51-109">Seuraava kaavio sisältää vaarallisten aineiden toiminnon määrittämiseen ja käyttämiseen tarvittavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="43d51-109">The following diagram illustrates the steps needed to set up and use the hazardous materials feature.</span></span>

<span data-ttu-id="43d51-110">![Vaarallisten aineiden toiminnon määrittäminen ja käyttäminen](media/hazmat-overview.png "Vaarallisten aineiden toiminnon määrittäminen ja käyttäminen")</span><span class="sxs-lookup"><span data-stu-id="43d51-110">![Setup and use of the hazardous materials feature](media/hazmat-overview.png "Setup and use of the hazardous materials feature")</span></span>

<span data-ttu-id="43d51-111">Vaarallisten aineiden toiminto määritetään tuotetietojen hallinnassa, ja se sisältää asiakirjoja, jotka voidaan tulostaa varastonhallinnassa.</span><span class="sxs-lookup"><span data-stu-id="43d51-111">The hazardous materials feature is set up in Product information management and provides documents that can be printed through Warehouse management.</span></span> <span data-ttu-id="43d51-112">Ne ovatkin kaksi tärkeintä aluetta, joissa ominaisuuden toiminnot tarkastellaan ja määritetään ja joissa niitä käytetään.</span><span class="sxs-lookup"><span data-stu-id="43d51-112">Therefore, broadly speaking, those areas are the two main areas where you will review, set up, and use this feature's functionality:</span></span>

- <span data-ttu-id="43d51-113">**Tuotetietojen hallinta** – vapautetussa tuotteessa käytettävien koodien määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="43d51-113">**Product information management** – Set up the codes that will be applied to a released product.</span></span>
- <span data-ttu-id="43d51-114">**Varastonhallinta** – lähetykseen tulostettavien lähetyksen lisäasiakirjojen käyttäminen.</span><span class="sxs-lookup"><span data-stu-id="43d51-114">**Warehouse management** – Work with additional shipping documents that will be printed for shipments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="43d51-115">Supply Chain Managementin vaarallisten aineiden toiminnot muodostavat hyödyllisten tuotetietokenttien ja liittyvien toimintojen kokoelman, joka auttaa kirjaamaan vaarallisiin tuotteisiin liittyviä tietoja ja viittaamaan niihin.</span><span class="sxs-lookup"><span data-stu-id="43d51-115">The hazardous materials features in Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="43d51-116">Nämä toiminnot auttavat myös suunnittelemaan ja tulostamaan lähetysasiakirjoja, joissa on joitakin samoja tietoja lähetettävistä vaarallisista aineista.</span><span class="sxs-lookup"><span data-stu-id="43d51-116">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="43d51-117">Järjestelmä ei kuitenkaan automaattisesti takaa, että maan tai alueen kaikkia soveltuvia säädöksiä noudatetaan.</span><span class="sxs-lookup"><span data-stu-id="43d51-117">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="43d51-118">Vaikka nämä työkalut on tarkoitettu auttamaan yleisten määräysten noudattamisessa, ne eivät yksin riitä eikä ole takeita, että määräyksiä noudatetaan niiden avulla.</span><span class="sxs-lookup"><span data-stu-id="43d51-118">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="43d51-119">Organisaatio vastaa siitä, että se on tietoinen kaikissa käytössä olevista säädöksistä ja että se tekee tarvittavan niiden noudattamiseksi.</span><span class="sxs-lookup"><span data-stu-id="43d51-119">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="43d51-120">Tuotetietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="43d51-120">Product information management</span></span>

<span data-ttu-id="43d51-121">Tuotetietojen hallinnassa on määritystaulukkojen joukko, jossa voit antaa erilaisten vaarallisten aineiden luetteloiden viitetiedot maa-, ilma- ja vesikuljetuksia varten.</span><span class="sxs-lookup"><span data-stu-id="43d51-121">Product information management provides a range of setup tables where you can enter reference information for the various dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="43d51-122">Tämän toiminnon kehittämisessä käytettiin seuraavia yleisiä määräyksiä:</span><span class="sxs-lookup"><span data-stu-id="43d51-122">The following common regulations were referenced when this functionality was developed:</span></span>

- <span data-ttu-id="43d51-123">**ADR** – Vaarallisten tavaroiden kansainväliseen maantiekuljetukseen liittyviä säädöksiä</span><span class="sxs-lookup"><span data-stu-id="43d51-123">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="43d51-124">**CFR 49** – Yhdysvaltojen vaarallisten tavaroiden kuljetusta koskevia säädöksiä</span><span class="sxs-lookup"><span data-stu-id="43d51-124">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="43d51-125">**IMDG** – Merenkulun kansainvälinen vaarallisten tavaroiden koodeksi (IMDG)</span><span class="sxs-lookup"><span data-stu-id="43d51-125">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="43d51-126">**IATA** – Kansainvälisin ilmakuljetusliiton (IATA) vaarallisten tavaroiden säädökset</span><span class="sxs-lookup"><span data-stu-id="43d51-126">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="43d51-127">Kukin määräysjoukko sisältää vaarallisten aineiden ja viitekoodien standardoidut luettelot.</span><span class="sxs-lookup"><span data-stu-id="43d51-127">Each set of regulations provides standardized lists of dangerous goods and reference codes.</span></span> <span data-ttu-id="43d51-128">Supply Chain Managementissa onkin näissä luetteloissa olevien yleisten koodien viitetaulukko.</span><span class="sxs-lookup"><span data-stu-id="43d51-128">Therefore, Supply Chain Management provides a reference table for the common codes on those lists.</span></span> <span data-ttu-id="43d51-129">Jokaisessa luettelossa on myös joitakin yksilöllisiä, määritettäviä koodeja.</span><span class="sxs-lookup"><span data-stu-id="43d51-129">Each list also has some unique codes that you can define.</span></span>

<span data-ttu-id="43d51-130">Lisätietoja vaarallisten aineiden määräysten ja arvojen määrittämisestä ja arvojen määrittämisestä tuotteisiin on seuraavissa ohjeaiheissa:</span><span class="sxs-lookup"><span data-stu-id="43d51-130">For more information about how to set up regulations and values for hazardous materials, and how to assign the values to relevant products, see the following topics:</span></span>

- [<span data-ttu-id="43d51-131">Vaarallisten aineiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="43d51-131">Set up hazardous materials</span></span>](hazmat-setup.md)
- [<span data-ttu-id="43d51-132">Tuotteiden, tilausten, lähetysten ja kuormien vaaralliset aineet</span><span class="sxs-lookup"><span data-stu-id="43d51-132">Hazardous materials in products, orders, shipments, and loads</span></span>](hazmat-items.md)

## <a name="warehouse-management"></a><span data-ttu-id="43d51-133">Varastonhallinta  </span><span class="sxs-lookup"><span data-stu-id="43d51-133">Warehouse management</span></span>

<span data-ttu-id="43d51-134">Kun lähetystä valmistellaan varastonhallinnassa, voit tulostaa useita uusia raportteja, joissa käytetään tuotetietojen hallinnassa määritettyjä tietoja.</span><span class="sxs-lookup"><span data-stu-id="43d51-134">When you prepare a shipment in Warehouse management, you will be able to print several new reports that use the information that you set up in Product information management.</span></span> <span data-ttu-id="43d51-135">Lisätietoja käytettävissä olevista raporteista ja niiden käyttämisestä on kohdassa [Vaarallisten aineiden kyselyt ja raportit](hazmat-reports.md).</span><span class="sxs-lookup"><span data-stu-id="43d51-135">For more information about the available reports and how to use them, see [Hazardous materials inquiries and reports](hazmat-reports.md).</span></span>