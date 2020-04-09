---
title: Työnkulkuhistorian tarkasteleminen
description: Tässä aiheessa kuvataan vaiheet, joiden avulla voit tarkastella työnkulkujärjestelmään käsiteltäväksi ja hyväksyttäväksi lähetetyn asiakirjan tilaa.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd5b8d9f3fd2edab50b52a8345f254ebc6b31d0a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140395"
---
# <a name="view-workflow-history"></a><span data-ttu-id="55f8b-103">Työnkulkuhistorian tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="55f8b-103">View workflow history</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="55f8b-104">Tässä aiheessa kuvataan vaiheet, joiden avulla voit tarkastella työnkulkujärjestelmään käsiteltäväksi ja hyväksyttäväksi lähetetyn asiakirjan tilaa.</span><span class="sxs-lookup"><span data-stu-id="55f8b-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="55f8b-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="55f8b-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="55f8b-106">Siirry kohtaan **Siirtymisruutu > Moduulit > Yhteiset > Kyselyt > Työnkulku > Työnkulkuhistoria**.</span><span class="sxs-lookup"><span data-stu-id="55f8b-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="55f8b-107">Tämän lomakkeen avulla voit tarkastella työnkulkujärjestelmään käsiteltäväksi ja hyväksyttäväksi lähetetyn asiakirjan tilaa.</span><span class="sxs-lookup"><span data-stu-id="55f8b-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="55f8b-108">**Esiintymän tunnus** on asiakirjaa käsittelevän tai käsitelleen työnkulun esiintymän tunnuskoodi.</span><span class="sxs-lookup"><span data-stu-id="55f8b-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="55f8b-109">**Tila** on asiakirjan työnkulun tila.</span><span class="sxs-lookup"><span data-stu-id="55f8b-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="55f8b-110">**Työnkulun tunnus** on asiakirjaa käsittelevän tai käsitelleen työnkulun tunnuskoodi.</span><span class="sxs-lookup"><span data-stu-id="55f8b-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="55f8b-111">**Asiakirja** on asiakirjan tunnuskoodi.</span><span class="sxs-lookup"><span data-stu-id="55f8b-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="55f8b-112">**Asiakirjatyyppi** on käsiteltäväksi lähetetyn asiakirjan tyyppi.</span><span class="sxs-lookup"><span data-stu-id="55f8b-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="55f8b-113">**Työnkulku** on asiakirjaa käsittelevän tai käsitelleen työnkulun nimi.</span><span class="sxs-lookup"><span data-stu-id="55f8b-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="55f8b-114">**Versio** on asiakirjaa käsittelevän tai käsitelleen työnkulun versionumero.</span><span class="sxs-lookup"><span data-stu-id="55f8b-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="55f8b-115">**Luonnin päivämäärä ja aika** on asiakirjan lähetyspäivämäärä ja -aika.</span><span class="sxs-lookup"><span data-stu-id="55f8b-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="55f8b-116">**Kulunut aika** on asiakirjan lähetyksestä kulunut aika.</span><span class="sxs-lookup"><span data-stu-id="55f8b-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="55f8b-117">Voit jatkaa **Jatka**-painikkeella valitun asiakirjan työnkulkuprosessia.</span><span class="sxs-lookup"><span data-stu-id="55f8b-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="55f8b-118">Voit peruuttaa **Peruuta**-painikkeella valitun asiakirjan, jolloin sitä ei käsitellä.</span><span class="sxs-lookup"><span data-stu-id="55f8b-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="55f8b-119">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="55f8b-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="55f8b-120">Varmista, että **Työnimikkeet**-osa on laajennettu.</span><span class="sxs-lookup"><span data-stu-id="55f8b-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="55f8b-121">Voit tarkastella tässä osassa valittuun asiakirjaan liitettyjä työnimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="55f8b-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="55f8b-122">Tehtävä on ehkä esimerkiksi suoritettava loppuun tai asiakirja on ehkä hyväksyttävä.</span><span class="sxs-lookup"><span data-stu-id="55f8b-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="55f8b-123">**Määritä uudelleen** -painike avaa valintaikkunan, jossa voit määrittää työnimikkeen uudelleen toiselle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="55f8b-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="55f8b-124">Varmista, että **Seurantatiedot**-osa on laajennettu.</span><span class="sxs-lookup"><span data-stu-id="55f8b-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="55f8b-125">Voit tarkastella tässä osassa valitun asiakirjan työnkulkuhistoriaa.</span><span class="sxs-lookup"><span data-stu-id="55f8b-125">In this section you can view the workflow history of the selected document.</span></span>  

