---
title: ER-kohteen arkistotyyppi
description: Tässä ohjeaiheessa annetaan tietoja siitä, miten kullekin lähteviä asiakirjoja luomaan määritetty sähköisen raportoinnin (ER) muodon KANSIO- tai TIEDOSTO-komponentin arkistokohde määritetään.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8797a68507a5116c6adbf1f2d805838fa507958c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745582"
---
# <a name="archive-destination"></a><span data-ttu-id="be040-103">Arkistokohde</span><span class="sxs-lookup"><span data-stu-id="be040-103">Archive destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be040-104">Voit määrittää arkistokohteen kullekin lähteviä asiakirjoja luomaan määritetylle sähköisen raportoinnin (ER) muodon KANSIO- tai TIEDOSTO-komponentille.</span><span class="sxs-lookup"><span data-stu-id="be040-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="be040-105">Luotu asiakirja tallennetaan ER-työluettelon tietueen liitteenä kohdeasetuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="be040-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="be040-106">Voit lähettää tällä asetuksella luodun tulosteen Microsoft SharePoint -kansion tai Microsoft Azuren tallennustilaan.</span><span class="sxs-lookup"><span data-stu-id="be040-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="be040-107">Lähetä tuloste valitun asiakirjatyypin mukaan määritettyyn kohteeseen valitsemalla **Käytössä**-asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="be040-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="be040-108">Valittavana on vain asiakirjatyyppejä, joiden ryhmäksi on valittu **Tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="be040-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="be040-109">Asiakirjojen [tyypit](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) määritetään valitsemalla **Organisaation hallinta** \> **Tiedoston hallinta** \> **Tiedostotyypit**.</span><span class="sxs-lookup"><span data-stu-id="be040-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="be040-110">ER-kohteiden määritys on sama kuin tiedostonhallintajärjestelmän määritys.</span><span class="sxs-lookup"><span data-stu-id="be040-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="be040-111">[![Tiedostotyypit-sivu](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="be040-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="be040-112">Sijainti määrittää, mihin tiedosto tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="be040-112">The location determines where the file is saved.</span></span> <span data-ttu-id="be040-113">Kun **Arkisto**-kohde on otettu käyttöön, tulokset voidaan tallentaa työarkistoon.</span><span class="sxs-lookup"><span data-stu-id="be040-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="be040-114">Voit tarkastella tuloksia kohteessa **Organisaation hallinta** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin arkistoidut työt**.</span><span class="sxs-lookup"><span data-stu-id="be040-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="be040-115">Valitse työarkiston tiedostotyyppi kohdassa **Organisaation hallinta** \> **Työtilat** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="be040-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="be040-116">Lisätietoja on kohdassa [Sähköisen raportoinnin (ER) kehyksen määrittäminen](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup)</span><span class="sxs-lookup"><span data-stu-id="be040-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="be040-117">SharePoint</span><span class="sxs-lookup"><span data-stu-id="be040-117">SharePoint</span></span>

<span data-ttu-id="be040-118">Voit tallentaa tiedoston määritettyyn SharePoint-kansioon.</span><span class="sxs-lookup"><span data-stu-id="be040-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="be040-119">SharePoint-oletuspalvelimen määritetään valitsemalla **Organisaation hallinto** \> **Tiedoston hallinta** \> **Tiedostonhallintaparametrit**.</span><span class="sxs-lookup"><span data-stu-id="be040-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="be040-120">Määritä SharePoint-kansio **SharePoint**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="be040-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="be040-121">Tämän jälkeen voit valita sen kansioksi, johon ER-tuloste tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="be040-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="be040-122">**SharePoint**-sijainnin on oltava valittuna tässä asiakirjatyypissä.</span><span class="sxs-lookup"><span data-stu-id="be040-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="be040-123">[![SharePoint-kansion valitseminen](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="be040-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="be040-124">Azuren tallennustila</span><span class="sxs-lookup"><span data-stu-id="be040-124">Azure Storage</span></span>

<span data-ttu-id="be040-125">Kun asiakirjatyypin sijainniksi on määritetty **Azure-tallennustila**, voit tallentaa tiedoston Azuren tallennustilaan.</span><span class="sxs-lookup"><span data-stu-id="be040-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be040-126">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="be040-126">Additional resources</span></span>

- [<span data-ttu-id="be040-127">Sähköisen raportoinnin (ER) yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="be040-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="be040-128">Sähköisen raportoinnin (ER) kohteet</span><span class="sxs-lookup"><span data-stu-id="be040-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="be040-129">Asiakirjanhallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="be040-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
