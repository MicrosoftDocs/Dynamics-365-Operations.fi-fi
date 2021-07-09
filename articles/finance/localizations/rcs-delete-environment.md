---
title: Regulatory Configuration Service (RCS) ‑ poista RCS-ympäristö
description: Tässä ohjeaiheessa on tietoja siitä, miten RCS (Regulatory Configuration Service) -järjestelmänvalvoja voi poistaa RCS-ympäristön ja siihen liittyvät tiedot.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295815"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a><span data-ttu-id="98f2c-103">Regulatory Configuration Service (RCS) ‑ poista RCS-ympäristö</span><span class="sxs-lookup"><span data-stu-id="98f2c-103">Regulatory Configuration Service (RCS) - Delete an RCS environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98f2c-104">Tässä ohjeaiheessa on tietoja siitä, miten RCS (Regulatory Configuration Service) -järjestelmänvalvoja voi poistaa RCS-ympäristön ja siihen liittyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="98f2c-104">This topic explains how a Regulatory Configuration Service (RCS) system administrator can delete an RCS environment and related data.</span></span>

<span data-ttu-id="98f2c-105">Ennen kuin voit suorittaa tämän ohjeaiheen vaiheet, seuraavien edellytysten on toteuduttava:</span><span class="sxs-lookup"><span data-stu-id="98f2c-105">Before you can complete the procedure in this topic, the following prerequisites must be met:</span></span>

- <span data-ttu-id="98f2c-106">Sinulle on oltava määritetty **järjestelmänvalvojan** rooli RCS-ympäristöä varten.</span><span class="sxs-lookup"><span data-stu-id="98f2c-106">You must have the **System Admin** role assigned to you for the RCS environment.</span></span>
- <span data-ttu-id="98f2c-107">**Järjestelmänvalvojan** rooliin on oltava määritettynä **RCSDeleteEnvironmentDuty**-rooli.</span><span class="sxs-lookup"><span data-stu-id="98f2c-107">The **System Admin** role must have the **RCSDeleteEnvironmentDuty** role assigned to it.</span></span>

## <a name="delete-an-rcs-environment"></a><span data-ttu-id="98f2c-108">Poista RCS-ympäristö</span><span class="sxs-lookup"><span data-stu-id="98f2c-108">Delete an RCS environment</span></span>

1. <span data-ttu-id="98f2c-109">Avaa RCS ja valitse **Sähköinen raportointi** -työtilaruutu.</span><span class="sxs-lookup"><span data-stu-id="98f2c-109">Open RCS, and select the **Electronic reporting** workspace tile.</span></span>
2. <span data-ttu-id="98f2c-110">Valitse **Aiheeseen liittyviä linkkejä** -osassa **Poista RCS-ympäristö**.</span><span class="sxs-lookup"><span data-stu-id="98f2c-110">In the **Related links** section, select **Delete RCS environment**.</span></span>

    ![Poista RCS-ympäristön linkki Aiheeseen liittyviä linkkejä -osassa](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. <span data-ttu-id="98f2c-112">Tarkista näyttöön tulevassa valintaikkunassa ympäristön poistoalueen sanomat.</span><span class="sxs-lookup"><span data-stu-id="98f2c-112">In the dialog box that appears, review the messages about the scope of environment deletion.</span></span>

    ![Sanomat Poista RCS-ympäristö -valintaikkunassa](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > <span data-ttu-id="98f2c-114">RCS-ympäristön poistoa ei voi peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="98f2c-114">Deletion of an RCS environment can't be reversed.</span></span>
    >
    > <span data-ttu-id="98f2c-115">Toiminto poistaa valitun RCS-ympäristön ja siihen liittyvät tiedot, mukaan lukien toiminnot ja konfiguraatiot, jotka on tallennettu yleistietovarastoon.</span><span class="sxs-lookup"><span data-stu-id="98f2c-115">The operation deletes the selected RCS environment and any related data, including features and configurations that are stored in the Global repository.</span></span> <span data-ttu-id="98f2c-116">Muille organisaatioille jaetut toiminnot ja konfiguraatiot poistetaan, jos niillä ei ole riippuvuuksia.</span><span class="sxs-lookup"><span data-stu-id="98f2c-116">Features and configurations that are shared with other organizations will be unshared and deleted if they have no dependencies.</span></span> <span data-ttu-id="98f2c-117">Toiminnot ja konfiguraatiot, joista on riippuvuuksia, merkitään lopetetuiksi.</span><span class="sxs-lookup"><span data-stu-id="98f2c-117">Features and configurations that have dependencies will be marked as discontinued.</span></span>

4. <span data-ttu-id="98f2c-118">Kirjoita annettuun kenttään RCS-ympäristön yleinen yksilöivä tunnus (RCS-ympäristö), joka vahvistaa, että haluat poistaa sen.</span><span class="sxs-lookup"><span data-stu-id="98f2c-118">In the field that is provided, enter the globally unique identifier (GUID) of the RCS environment to confirm that you want to delete it.</span></span> <span data-ttu-id="98f2c-119">Ympäristön GUID on liitetty poistosanomaan.</span><span class="sxs-lookup"><span data-stu-id="98f2c-119">The environment's GUID is included in the deletion message.</span></span>
5. <span data-ttu-id="98f2c-120">Valitse **Poista ympäristö**.</span><span class="sxs-lookup"><span data-stu-id="98f2c-120">Select **Delete environment**.</span></span>
    
<span data-ttu-id="98f2c-121">RCS-ympäristösi ja kaikki siihen liittyvät tiedot poistetaan nyt.</span><span class="sxs-lookup"><span data-stu-id="98f2c-121">Your RCS environment and any related data are now deleted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="98f2c-122">Kun olet poistanut RCS-ympäristön, tietoja ei voi palauttaa.</span><span class="sxs-lookup"><span data-stu-id="98f2c-122">After you delete an RCS environment, there is no way to recover the data.</span></span> <span data-ttu-id="98f2c-123">Voit luoda uuden RCS-ympäristön missä tahansa käytettävissä olevalla RCS-alueella.</span><span class="sxs-lookup"><span data-stu-id="98f2c-123">A new RCS environment can be created in any available RCS region.</span></span>
