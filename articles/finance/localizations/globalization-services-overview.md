---
title: Dynamics 365 -globalisointipalvelut
description: Tässä aiheessa on yleiskuvaus Microsoft Dynamics 365 -globalisointipalveluista.
author: JaneA07
manager: AnnBe
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8c6f3b7fb4dec0dffe55014e9e2d60620dc3b193
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893045"
---
# <a name="dynamics-365-globalization-services"></a><span data-ttu-id="0a388-103">Dynamics 365 -globalisointipalvelut</span><span class="sxs-lookup"><span data-stu-id="0a388-103">Dynamics 365 globalization services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a388-104">Seuraavat globalisointipalvelut voidaan konfiguroida laajentamaan joidenkin Microsoft Dynamics 365 -verkkopalvelun ominaisuuksia:</span><span class="sxs-lookup"><span data-stu-id="0a388-104">The following globalization services can be configured to extend the capabilities that exist in some Microsoft Dynamics 365 online services:</span></span>

- <span data-ttu-id="0a388-105">**Regulatory Configuration Service (RCS)** tukee erilaisten sähköisten tiedostojen ja raporttien konfiguroinnissa.</span><span class="sxs-lookup"><span data-stu-id="0a388-105">**Regulatory Configuration Service (RCS)** supports the configuration of different types of electronic documents and reports.</span></span> <span data-ttu-id="0a388-106">RCS tarjoaa sähköisen raportoinnin (ER) parannetun version, jossa konfigurointitietovarasto on erillinen palvelu.</span><span class="sxs-lookup"><span data-stu-id="0a388-106">RCS provides an enhanced version of the Electronic reporting (ER) designer where the configuration repository is a standalone service.</span></span> <span data-ttu-id="0a388-107">Lisätietoja on kohdassa [Regulatory Configuration Service](rcs-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0a388-107">For more information, see [Regulatory Configuration Service](rcs-overview.md).</span></span>
- <span data-ttu-id="0a388-108">**Sähköinen laskutus** kokoaa yhteen muunnosten, digitaalisten allekirjoitusten ja konfiguroitavia integrointien muotoja, joita voidaan konfiguroida ulkoisten Internet-palveluiden kanssa, mukaan lukien sertifikaattien ja vastausten käsittely.</span><span class="sxs-lookup"><span data-stu-id="0a388-108">**Electronic Invoicing** brings together configurable formats for transformations, digital signatures, and configurable integrations for connectivity with external web services, including certification and response handling.</span></span> <span data-ttu-id="0a388-109">Lisätietoja kohdassa [Sähköinen laskutus](e-invoicing-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0a388-109">For more information, see [Electronic Invoicing](e-invoicing-service-overview.md).</span></span>
- <span data-ttu-id="0a388-110">**Verojen laskenta** mahdollistaa joustavan suorituksen tukemalla useita verotunnuksia, verokoodin määrittämisen, veron laskentasuunnittelijan ja ajoaikaohjelman, jotka noudattavat monimutkaisia verosäädöksiä maailmanlaajuisesti.</span><span class="sxs-lookup"><span data-stu-id="0a388-110">**Tax Calculation** provides enhanced flexibility by supporting multiple tax IDs, tax code determination, the tax calculation designer, and a runtime engine to comply with complex tax regulations worldwide.</span></span> <span data-ttu-id="0a388-111">Lisätietoja on kohdassa [Verolaskenta](global-tax-calcuation-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0a388-111">For more information, see [Tax Calculation](global-tax-calcuation-service-overview.md).</span></span>

<span data-ttu-id="0a388-112">Nämä globalisointipalvelut tarjoavat ruudukkointegraation seuraavien Dynamics 365 -verkkopalveluiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="0a388-112">These globalization services provide out-of-box integration with the following Dynamics 365 online services.</span></span>

| <span data-ttu-id="0a388-113">Verkkopalvelut</span><span class="sxs-lookup"><span data-stu-id="0a388-113">Online service</span></span> | <span data-ttu-id="0a388-114">Sääntöjen konfigurointipalvelu</span><span class="sxs-lookup"><span data-stu-id="0a388-114">RCS</span></span> | <span data-ttu-id="0a388-115">Sähköinen laskutus</span><span class="sxs-lookup"><span data-stu-id="0a388-115">Electronic Invoicing</span></span> | <span data-ttu-id="0a388-116">Verolaskenta (esiversio)</span><span class="sxs-lookup"><span data-stu-id="0a388-116">Tax Calculation (Preview)</span></span> |
|----------------|-----|----------------------|---------------------------|
| <span data-ttu-id="0a388-117">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="0a388-117">Dynamics 365 Finance</span></span> | <span data-ttu-id="0a388-118">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0a388-118">Yes</span></span> | <span data-ttu-id="0a388-119">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0a388-119">Yes</span></span> | <span data-ttu-id="0a388-120">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0a388-120">Yes</span></span> | 
| <span data-ttu-id="0a388-121">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0a388-121">Dynamics 365 Supply Chain Management</span></span> | <span data-ttu-id="0a388-122">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0a388-122">Yes</span></span> | <span data-ttu-id="0a388-123">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0a388-123">Yes</span></span> | <span data-ttu-id="0a388-124">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0a388-124">Yes</span></span> | 
| <span data-ttu-id="0a388-125">Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="0a388-125">Dynamics 365 Project Operations</span></span> | <span data-ttu-id="0a388-126">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0a388-126">Yes</span></span> | <span data-ttu-id="0a388-127">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0a388-127">Yes</span></span> | <span data-ttu-id="0a388-128">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="0a388-128">Not applicable</span></span> | 
| <span data-ttu-id="0a388-129">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="0a388-129">Dynamics 365 Commerce</span></span> | <span data-ttu-id="0a388-130">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0a388-130">Yes</span></span> | <span data-ttu-id="0a388-131">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="0a388-131">Not applicable</span></span> | <span data-ttu-id="0a388-132">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="0a388-132">Not applicable</span></span> | 

> [!NOTE]
> <span data-ttu-id="0a388-133">Azuren maantieteellisten sijaintien (geos) saatavuuden erojen vuoksi RCS:lle tämän palvelun määritys saattaa aiheuttaa asiakastietojen siirtämisen sovellettavaan Dynamics 365 -verkkopalveluun valitun maantieteellisen alueen ulkopuolelle.</span><span class="sxs-lookup"><span data-stu-id="0a388-133">Because of differences in the availability of Azure geographic locations (geos) for RCS, configuration of this service might cause customer data to be transferred outside the geo that is selected for the applicable Dynamics 365 online service.</span></span> <span data-ttu-id="0a388-134">Lisätietoja on kohdassa [Dynamics 365 ja Power Platform: Saatavuus, tietojen sijainti, kieli ja localization](https://aka.ms/rcs/D365Productavailabilityguide).</span><span class="sxs-lookup"><span data-stu-id="0a388-134">For more information, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/rcs/D365Productavailabilityguide).</span></span>