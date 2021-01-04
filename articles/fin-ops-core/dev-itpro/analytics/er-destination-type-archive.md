---
title: ER-kohteen arkistotyyppi
description: Tässä ohjeaiheessa annetaan tietoja siitä, miten kullekin lähteviä asiakirjoja luomaan määritetty sähköisen raportoinnin (ER) muodon KANSIO- tai TIEDOSTO-komponentin arkistokohde määritetään.
author: NickSelin
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 3dee7ec614ec1372feaa1150f5e4ebb14c32f60e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679675"
---
# <a name="archive-er-destination-type"></a><span data-ttu-id="dfd2f-103">ER-kohteen arkistotyyppi</span><span class="sxs-lookup"><span data-stu-id="dfd2f-103">Archive ER destination type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dfd2f-104">Voit määrittää arkistokohteen kullekin lähteviä asiakirjoja luomaan määritetylle sähköisen raportoinnin (ER) muodon **Kansio**- tai **Tiedosto**-komponentille.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-104">You can configure an archive destination for each **Folder** or **File** component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="dfd2f-105">Luotu asiakirja tallennetaan ER-työluettelon tietueen liitteenä kohdeasetuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span> <span data-ttu-id="dfd2f-106">Voit tarkastella tuloksia kohteessa **Organisaation hallinta** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin työt**.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-106">To view the results, go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>

<span data-ttu-id="dfd2f-107">Voit lähettää tällä asetuksella luodun tulosteen Microsoft SharePoint -kansion tai Microsoft Azuren tallennustilaan.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-107">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="dfd2f-108">Lähetä tuloste valitun asiakirjatyypin mukaan määritettyyn kohteeseen valitsemalla **Käytössä**-asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-108">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="dfd2f-109">Valittavana on vain asiakirjatyyppejä, joiden ryhmäksi on valittu **Tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-109">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="dfd2f-110">Asiakirjojen [tyypit](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) määritetään valitsemalla **Organisaation hallinta** \> **Tiedoston hallinta** \> **Tiedostotyypit**.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-110">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="dfd2f-111">ER-kohteiden määritys on sama kuin tiedostonhallintajärjestelmän määritys.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-111">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="dfd2f-112">[![Tiedostotyypit-sivu](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="dfd2f-112">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="dfd2f-113">Sijainti määrittää, mihin tiedosto tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-113">The location determines where the file is saved.</span></span> <span data-ttu-id="dfd2f-114">Kun **Arkisto**-kohde on otettu käyttöön, tulokset voidaan tallentaa työarkistoon.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-114">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="dfd2f-115">Voit tarkastella tuloksia kohteessa **Organisaation hallinta** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin arkistoidut työt**.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-115">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="dfd2f-116">Valitse työarkiston tiedostotyyppi kohdassa **Organisaation hallinta** \> **Työtilat** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-116">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="dfd2f-117">Lisätietoja on kohdassa [Sähköisen raportoinnin (ER) kehyksen määrittäminen](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="dfd2f-117">For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="dfd2f-118">SharePoint</span><span class="sxs-lookup"><span data-stu-id="dfd2f-118">SharePoint</span></span>

<span data-ttu-id="dfd2f-119">Voit tallentaa tiedoston määritettyyn SharePoint-kansioon.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-119">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="dfd2f-120">SharePoint-oletuspalvelimen määritetään valitsemalla **Organisaation hallinto** \> **Tiedoston hallinta** \> **Tiedostonhallintaparametrit**.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-120">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="dfd2f-121">Määritä SharePoint-kansio **SharePoint**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-121">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="dfd2f-122">Tämän jälkeen voit valita sen kansioksi, johon ER-tuloste tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-122">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="dfd2f-123">**SharePoint**-sijainnin on oltava valittuna tässä asiakirjatyypissä.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-123">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="dfd2f-124">[![SharePoint-kansion valitseminen](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="dfd2f-124">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="dfd2f-125">Azuren tallennustila</span><span class="sxs-lookup"><span data-stu-id="dfd2f-125">Azure Storage</span></span>

<span data-ttu-id="dfd2f-126">Kun asiakirjatyypin sijainniksi on määritetty **Azure-tallennustila**, voit tallentaa tiedoston Azuren tallennustilaan.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-126">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

> [!NOTE] 
> <span data-ttu-id="dfd2f-127">ER-kehys tallentaa tiedostot pysyvästi Azure Blob -tallennustilaan toisin kuin tietojenhallintakehys, jolla on seitsemän päivän säilytyskäytäntö asiakirjoille, jotka on käsiteltävä.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-127">The ER framework permanently stores files in Azure Blob storage unlike the Data management framework that applies the seven-day retention policy for documents that must be processed.</span></span> <span data-ttu-id="dfd2f-128">Lisätietoja on kohdissa [Ohjelmointirajapinta viestin tilan hakemiselle](../data-entities/recurring-integrations.md#api-for-getting-message-status) ja [Tilan tarkistuksen ohjelmointirajapinta](../data-entities/data-management-api.md#status-check-api).</span><span class="sxs-lookup"><span data-stu-id="dfd2f-128">For more information, see [API for getting message status](../data-entities/recurring-integrations.md#api-for-getting-message-status) and [Status check API](../data-entities/data-management-api.md#status-check-api).</span></span> <span data-ttu-id="dfd2f-129">ER:ään liittyvät tiedostot tallennetaan Azure Blob -tallennustilaan sovellustaulun tietueiden liitteinä niin pitkäksi aikaa kuin on tarpeellista.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-129">The ER-related files will be stored in Azure Blob storage as attachments of application table records as long as necessary.</span></span> <span data-ttu-id="dfd2f-130">Yksittäinen tiedosto poistetaan Azure Blob -tallennustilasta yhdessä sen sovellustaulun tietueen kanssa, johon tiedosto on liitetty.</span><span class="sxs-lookup"><span data-stu-id="dfd2f-130">A single file will be deleted from Azure Blob storage along with the application table record that this file was attached to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dfd2f-131">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="dfd2f-131">Additional resources</span></span>

- [<span data-ttu-id="dfd2f-132">Sähköisen raportoinnin (ER) yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="dfd2f-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="dfd2f-133">Sähköisen raportoinnin (ER) kohteet</span><span class="sxs-lookup"><span data-stu-id="dfd2f-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="dfd2f-134">Asiakirjanhallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="dfd2f-134">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
