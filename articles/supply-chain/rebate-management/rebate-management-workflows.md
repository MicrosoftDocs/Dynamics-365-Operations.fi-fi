---
title: Ostohyvitysten hallintasopimuksen työnkulut
description: Tässä ohjeaiheessa on tietoja sopimusten hyväksymis- ja aktivointityönkulun määrittäminen ostohyvitysten hallintasopimuksia varten.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 16f1c56ecd69f4dc7bfd80e74d3f35147cc173d6
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5919816"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="ba22f-103">Ostohyvitysten hallintasopimuksen työnkulut</span><span class="sxs-lookup"><span data-stu-id="ba22f-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba22f-104">Ostohyvitysten hallinnassa voit hyväksyä ostohyvityssopimuksia samalla työnkulkuympäristöllä kuin muut Finance and Operations -sovellukset.</span><span class="sxs-lookup"><span data-stu-id="ba22f-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="ba22f-105">Jokaiseen työnkulkuun liittyy kaksi työprosessia:</span><span class="sxs-lookup"><span data-stu-id="ba22f-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="ba22f-106">Yksi työnkulun elementti aktivoi sopimuksen, jotta käyttäjä tai työnkulkuprosessi voi hyväksyä tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="ba22f-106">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>
- <span data-ttu-id="ba22f-107">Yksi työnkulun elementeistä hyväksyy sopimuksen.</span><span class="sxs-lookup"><span data-stu-id="ba22f-107">One element of the workflow approves the deal.</span></span>

<span data-ttu-id="ba22f-108">Ennen ostohyvityssopimuksen käyttöä sen on oltava aktiivinen **Ostohyvityksen hallinta** -moduulissa.</span><span class="sxs-lookup"><span data-stu-id="ba22f-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="ba22f-109">Voit aktivoida sopimuksen luomalla ja konfiguroimalla *ostohyvityksen hallintasopimuksen työnkulun*.</span><span class="sxs-lookup"><span data-stu-id="ba22f-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="ba22f-110">Kun työnkulku on aktivoitu ostohyvitysten hallinnassa, käyttäjät eivät voi hyväksyä tarjouksia manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="ba22f-110">After a workflow is activated for Rebate management, users can't manually approve deals.</span></span> <span data-ttu-id="ba22f-111">Työnkulkua on käytettävä aina.</span><span class="sxs-lookup"><span data-stu-id="ba22f-111">The workflow must be always used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="ba22f-112">Ostohyvitysten hallintasopimuksen työnkulkujen luonti ja hallinta</span><span class="sxs-lookup"><span data-stu-id="ba22f-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="ba22f-113">Voit käyttää ostohyvityksen hallintasopimuksen työnkulkuja kohdassa **Ostohyvitysten hallinta \> Asetukset \> Ostohyvitysten hallinnan työnkulut**.</span><span class="sxs-lookup"><span data-stu-id="ba22f-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="ba22f-114">Siinä voit tarkastella, luoda ja päivittää työnkulkuja tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="ba22f-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="ba22f-115">Vain yksi tämän tyyppinen työnkulku voi olla aktiivinen kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="ba22f-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="ba22f-116">Lisätietoja työnkuluista, **Ostohyvityksen hallinnan työnkulut** -sivun käyttämisestä ja työnkulkujen luomisesta on [työnkulkujärjestelmän yhteenvedossa](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) sekä siihen liittyvissä ohjeaiheissa.</span><span class="sxs-lookup"><span data-stu-id="ba22f-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="ba22f-117">Työnkulun käyttäminen sopimuksen aktivoimiseen</span><span class="sxs-lookup"><span data-stu-id="ba22f-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="ba22f-118">Voit aktivoida sopimuksen työnkulun kautta avaamalla sopimuksen (esimerkiksi **Kaikki ostohyvityksen hallintasopimukset** -sivulla).</span><span class="sxs-lookup"><span data-stu-id="ba22f-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="ba22f-119">Valitse siten toimintoruudussa **Työnkulku \> Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="ba22f-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="ba22f-120">Kun uusi sopimus on käsitelty ja hyväksytty työnkulun kautta, se on aktiivinen ja valmis käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="ba22f-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="ba22f-121">Kun sopimus on aktivoitu, et voi muuttaa sen asetuksia.</span><span class="sxs-lookup"><span data-stu-id="ba22f-121">After a deal has been activated, you can't change its setup.</span></span> <span data-ttu-id="ba22f-122">Jos haluat muuttaa aktiivista sopimusta, poista se käytöstä ja luo sitten uusi sopimus.</span><span class="sxs-lookup"><span data-stu-id="ba22f-122">If you must change an active deal, inactivate it, and then create a new deal.</span></span> <span data-ttu-id="ba22f-123">Jos uusi sopimus muistuttaa vanhaa sopimusta, voit luoda sen kopioimalla vanhan sopimuksen.</span><span class="sxs-lookup"><span data-stu-id="ba22f-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>
