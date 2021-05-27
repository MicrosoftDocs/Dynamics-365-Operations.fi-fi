---
title: Tietokenttien lisääminen verokonfiguraatioihin
description: Tässä ohjeaiheessa kerrotaan, miten veromäärityksiä mukautetaan lisäämällä tietokenttiä.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ebb186a4cb9ca61399909625233b579acd2c0ec5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022784"
---
# <a name="add-data-fields-in-tax-configurations"></a><span data-ttu-id="80fca-103">Tietokenttien lisääminen verokonfiguraatioihin</span><span class="sxs-lookup"><span data-stu-id="80fca-103">Add data fields in tax configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80fca-104">Tässä ohjeaiheessa kerrotaan, miten verokonfiguraatioita mukautetaan [käyttämällä verointegraatioon lisättyjä tietokenttiä](tax-service-add-data-fields-tax-integration-by-extension.md).</span><span class="sxs-lookup"><span data-stu-id="80fca-104">This topic explains how to customize tax configurations by using [data fields that are added in the tax integration](tax-service-add-data-fields-tax-integration-by-extension.md).</span></span>

## <a name="customize-the-tax-data-model"></a><span data-ttu-id="80fca-105">Veron tietomallin mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="80fca-105">Customize the tax data model</span></span>

1. <span data-ttu-id="80fca-106">Siirry Microsoft Dynamics 365 Financessa kohtaan **Sähköinen raportointi** \> **Verokonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="80fca-106">In Microsoft Dynamics 365 Finance, go to **Electronic Reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="80fca-107">Valitse määrityspuussa **Verotietomalli – Eurooppa**.</span><span class="sxs-lookup"><span data-stu-id="80fca-107">In the configuration tree, select **Tax Data Model - Europe**.</span></span> <span data-ttu-id="80fca-108">Valitse siten toimintoruudussa **Luo konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="80fca-108">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="80fca-109">Valitse avattavasta valintaikkunasta **Verotettavan asiakirjan malli, johdettu nimestä: Verotietomalli – Eurooppa, Microsoft** -vaihtoehto, kirjoita uuden verotietomallin nimi ja valitse sitten **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="80fca-109">In the drop-down dialog box, select the **Taxable document model derived from Name: Tax Data Model -- Europe, Microsoft** option, enter a name for the new tax data model, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="80fca-110">Valitse juuri luomasi verotietomalli ja valitse sitten toimintoruudussa **Suunnitteluohjelma**.</span><span class="sxs-lookup"><span data-stu-id="80fca-110">Select the tax data model that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="80fca-111">Laajenna tietomallipuu, valitse **Rivit** ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="80fca-111">Expand the data model tree, select **Lines**, and then select **New**.</span></span>
6. <span data-ttu-id="80fca-112">Kirjoita **Luo solmu** -valintaikkunaan nimi, määritä kohteen tyyppi ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="80fca-112">In the **Create node** dialog box, enter a name, specify the item type, and then select **Add**.</span></span>
7. <span data-ttu-id="80fca-113">Lisää tarvittavat sarakkeet.</span><span class="sxs-lookup"><span data-stu-id="80fca-113">Add any required columns.</span></span>
8. <span data-ttu-id="80fca-114">Valitse toimintoruudussa ensin **Tallenna** ja sitten **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="80fca-114">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="80fca-115">Sulje sivu ja tarkastele verotietomallin valmista versiota.</span><span class="sxs-lookup"><span data-stu-id="80fca-115">Close the page, and view the completed version of your tax data model.</span></span>

## <a name="customize-the-tax-configuration"></a><span data-ttu-id="80fca-116">Veromäärityksen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="80fca-116">Customize the tax configuration</span></span>

1. <span data-ttu-id="80fca-117">Siirry Financessa kohtaan **Sähköinen raportointi** \> **Verokonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="80fca-117">In Finance, go to **Electronic reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="80fca-118">Valitse määrityspuussa **Veromääritys – Eurooppa**.</span><span class="sxs-lookup"><span data-stu-id="80fca-118">In the configuration tree, select **Tax Configuration -- Europe**.</span></span> <span data-ttu-id="80fca-119">Valitse siten toimintoruudussa **Luo konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="80fca-119">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="80fca-120">Valitse avattavasta valintaikkunasta **Veropalvelun määritys, johdettu nimestä: Veromääritys – Eurooppa, Microsoft** -vaihtoehto, kirjoita uuden veromäärityksen nimi ja valitse sitten **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="80fca-120">In the drop-down dialog box, select the **Tax service configuration derived from Name: Tax Configuration -- Europe, Microsoft** option, enter a name for the new tax configuration, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="80fca-121">Valitse juuri luomasi veromääritys ja valitse sitten toimintoruudussa **Suunnitteluohjelma**.</span><span class="sxs-lookup"><span data-stu-id="80fca-121">Select the tax configuration that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="80fca-122">Valitse **Ominaisuudet**-osan **Tietomalli**-kentästä aiemmin luomasi mukautettu verotietomalli.</span><span class="sxs-lookup"><span data-stu-id="80fca-122">In the **Properties** section, in the **Data model** field, select the customized tax data model that you created earlier.</span></span>
6. <span data-ttu-id="80fca-123">Valitse **Tietomallin versio** -kentästä verotietomallin valmis versio.</span><span class="sxs-lookup"><span data-stu-id="80fca-123">In the **Data model version** field, select the completed version of the tax data model.</span></span>
7. <span data-ttu-id="80fca-124">Valitse **Lisää** ja lisää tarvittavat veromitat.</span><span class="sxs-lookup"><span data-stu-id="80fca-124">Select **Add**, and add the required tax measures.</span></span>
8. <span data-ttu-id="80fca-125">Valitse toimintoruudussa ensin **Tallenna** ja sitten **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="80fca-125">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="80fca-126">Sulje sivu ja tarkastele veromäärityksen valmista versiota.</span><span class="sxs-lookup"><span data-stu-id="80fca-126">Close page, and view the completed version of your tax configuration.</span></span>

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a><span data-ttu-id="80fca-127">Vero-ominaisuuksien toteuttaminen mukautetussa veromäärityksessä</span><span class="sxs-lookup"><span data-stu-id="80fca-127">Implement tax features in the customized tax configuration</span></span>

1. <span data-ttu-id="80fca-128">Siirry Regulatory Configuration Servicesissä (RCS) kohtaan **Globalisointiominaisuudet** \> **Vero**.</span><span class="sxs-lookup"><span data-stu-id="80fca-128">In Regulatory Configuration Service (RCS), go to **Globalization Features** \> **Tax**.</span></span>
2. <span data-ttu-id="80fca-129">Valitse **Lisää**, kirjoita uuden ominaisuuden tiedot ja valitse sitten **Luo ominaisuus**.</span><span class="sxs-lookup"><span data-stu-id="80fca-129">Select **Add**, enter information about the new feature, and then select **Create feature**.</span></span>
3. <span data-ttu-id="80fca-130">Valitse ominaisuus **Versiot**-välilehdessä ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="80fca-130">On the **Versions** tab, select the feature, and then select **Edit**.</span></span>
4. <span data-ttu-id="80fca-131">Valitse **Yleiset**-välilehden **Konfiguraatioversio**-kentästä mukautettu veromääritys ja -versio.</span><span class="sxs-lookup"><span data-stu-id="80fca-131">On the **General** tab, in the **Configuration version** field, select the customized tax configuration and version.</span></span>
5. <span data-ttu-id="80fca-132">Valitse **Sarakkeiden hallinta** -valintaikkunassa otsikko- ja rivisarakkeet, jotka haluat sisällyttää mukautettuun veromittaan, ja lisää ne sitten **Valitut sarakkeet** -luetteloon valitsemalla oikea nuolipainike.</span><span class="sxs-lookup"><span data-stu-id="80fca-132">In the **Manage columns** dialog box, select the header and line columns that you want to include in your customized tax measure, and then select the right arrow button to add them to the **Selected columns** list.</span></span>
