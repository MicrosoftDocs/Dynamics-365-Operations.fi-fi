---
title: Dynamics 365 -globalisointipalvelut
description: Tässä aiheessa on yleiskuvaus Microsoft Dynamics 365 -globalisointipalveluista.
author: JaneA07
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
ms.openlocfilehash: 2ef942f7f6dac2c321a51800ade0bf25f2162304
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018804"
---
# <a name="dynamics-365-globalization-services"></a><span data-ttu-id="d0a98-103">Dynamics 365 -globalisointipalvelut</span><span class="sxs-lookup"><span data-stu-id="d0a98-103">Dynamics 365 globalization services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0a98-104">Seuraavat globalisointipalvelut voidaan konfiguroida laajentamaan joidenkin Microsoft Dynamics 365 -verkkopalvelun ominaisuuksia:</span><span class="sxs-lookup"><span data-stu-id="d0a98-104">The following globalization services can be configured to extend the capabilities that exist in some Microsoft Dynamics 365 online services:</span></span>

- <span data-ttu-id="d0a98-105">**Regulatory Configuration Service (RCS)** tukee erilaisten sähköisten tiedostojen ja raporttien konfiguroinnissa.</span><span class="sxs-lookup"><span data-stu-id="d0a98-105">**Regulatory Configuration Service (RCS)** supports the configuration of different types of electronic documents and reports.</span></span> <span data-ttu-id="d0a98-106">RCS tarjoaa sähköisen raportoinnin (ER) parannetun version, jossa konfigurointitietovarasto on erillinen palvelu.</span><span class="sxs-lookup"><span data-stu-id="d0a98-106">RCS provides an enhanced version of the Electronic reporting (ER) designer where the configuration repository is a standalone service.</span></span> <span data-ttu-id="d0a98-107">Lisätietoja on kohdassa [Regulatory Configuration Service](rcs-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d0a98-107">For more information, see [Regulatory Configuration Service](rcs-overview.md).</span></span>
- <span data-ttu-id="d0a98-108">**Sähköinen laskutus** kokoaa yhteen muunnosten, digitaalisten allekirjoitusten ja konfiguroitavia integrointien muotoja, joita voidaan konfiguroida ulkoisten Internet-palveluiden kanssa, mukaan lukien sertifikaattien ja vastausten käsittely.</span><span class="sxs-lookup"><span data-stu-id="d0a98-108">**Electronic Invoicing** brings together configurable formats for transformations, digital signatures, and configurable integrations for connectivity with external web services, including certification and response handling.</span></span> <span data-ttu-id="d0a98-109">Lisätietoja kohdassa [Sähköinen laskutus](e-invoicing-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d0a98-109">For more information, see [Electronic Invoicing](e-invoicing-service-overview.md).</span></span>
- <span data-ttu-id="d0a98-110">**Verojen laskenta** mahdollistaa joustavan suorituksen tukemalla useita verotunnuksia, verokoodin määrittämisen, veron laskentasuunnittelijan ja ajoaikaohjelman, jotka noudattavat monimutkaisia verosäädöksiä maailmanlaajuisesti.</span><span class="sxs-lookup"><span data-stu-id="d0a98-110">**Tax Calculation** provides enhanced flexibility by supporting multiple tax IDs, tax code determination, the tax calculation designer, and a runtime engine to comply with complex tax regulations worldwide.</span></span> <span data-ttu-id="d0a98-111">Lisätietoja on kohdassa [Verolaskenta](global-tax-calcuation-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d0a98-111">For more information, see [Tax Calculation](global-tax-calcuation-service-overview.md).</span></span>

<span data-ttu-id="d0a98-112">Nämä globalisointipalvelut tarjoavat ruudukkointegraation seuraavien Dynamics 365 -verkkopalveluiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="d0a98-112">These globalization services provide out-of-box integration with the following Dynamics 365 online services.</span></span>

| <span data-ttu-id="d0a98-113">Verkkopalvelut</span><span class="sxs-lookup"><span data-stu-id="d0a98-113">Online service</span></span> | <span data-ttu-id="d0a98-114">Sääntöjen konfigurointipalvelu</span><span class="sxs-lookup"><span data-stu-id="d0a98-114">RCS</span></span> | <span data-ttu-id="d0a98-115">Sähköinen laskutus</span><span class="sxs-lookup"><span data-stu-id="d0a98-115">Electronic Invoicing</span></span> | <span data-ttu-id="d0a98-116">Verolaskenta (esiversio)</span><span class="sxs-lookup"><span data-stu-id="d0a98-116">Tax Calculation (Preview)</span></span> |
|----------------|-----|----------------------|---------------------------|
| <span data-ttu-id="d0a98-117">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="d0a98-117">Dynamics 365 Finance</span></span> | <span data-ttu-id="d0a98-118">Kyllä</span><span class="sxs-lookup"><span data-stu-id="d0a98-118">Yes</span></span> | <span data-ttu-id="d0a98-119">Kyllä</span><span class="sxs-lookup"><span data-stu-id="d0a98-119">Yes</span></span> | <span data-ttu-id="d0a98-120">Kyllä</span><span class="sxs-lookup"><span data-stu-id="d0a98-120">Yes</span></span> | 
| <span data-ttu-id="d0a98-121">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d0a98-121">Dynamics 365 Supply Chain Management</span></span> | <span data-ttu-id="d0a98-122">Kyllä</span><span class="sxs-lookup"><span data-stu-id="d0a98-122">Yes</span></span> | <span data-ttu-id="d0a98-123">Kyllä</span><span class="sxs-lookup"><span data-stu-id="d0a98-123">Yes</span></span> | <span data-ttu-id="d0a98-124">Kyllä</span><span class="sxs-lookup"><span data-stu-id="d0a98-124">Yes</span></span> | 
| <span data-ttu-id="d0a98-125">Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="d0a98-125">Dynamics 365 Project Operations</span></span> | <span data-ttu-id="d0a98-126">Kyllä</span><span class="sxs-lookup"><span data-stu-id="d0a98-126">Yes</span></span> | <span data-ttu-id="d0a98-127">Kyllä</span><span class="sxs-lookup"><span data-stu-id="d0a98-127">Yes</span></span> | <span data-ttu-id="d0a98-128">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d0a98-128">Not applicable</span></span> | 
| <span data-ttu-id="d0a98-129">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d0a98-129">Dynamics 365 Commerce</span></span> | <span data-ttu-id="d0a98-130">Kyllä</span><span class="sxs-lookup"><span data-stu-id="d0a98-130">Yes</span></span> | <span data-ttu-id="d0a98-131">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d0a98-131">Not applicable</span></span> | <span data-ttu-id="d0a98-132">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d0a98-132">Not applicable</span></span> | 

> [!NOTE]
> <span data-ttu-id="d0a98-133">Azuren maantieteellisten sijaintien (geos) saatavuuden erojen vuoksi RCS:lle tämän palvelun määritys saattaa aiheuttaa asiakastietojen siirtämisen sovellettavaan Dynamics 365 -verkkopalveluun valitun maantieteellisen alueen ulkopuolelle.</span><span class="sxs-lookup"><span data-stu-id="d0a98-133">Because of differences in the availability of Azure geographic locations (geos) for RCS, configuration of this service might cause customer data to be transferred outside the geo that is selected for the applicable Dynamics 365 online service.</span></span> <span data-ttu-id="d0a98-134">Lisätietoja on kohdassa [Dynamics 365 ja Power Platform: Saatavuus, tietojen sijainti, kieli ja localization](https://aka.ms/rcs/D365Productavailabilityguide).</span><span class="sxs-lookup"><span data-stu-id="d0a98-134">For more information, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/rcs/D365Productavailabilityguide).</span></span>