---
title: Rahdin täsmäytys kuljetustenhallinnassa
description: Tässä artikkelissa käsitellään rahdin täsmäytysprosessia.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f92808f904ba93513e20b74bd2b597712cb93d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "344774"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="57819-103">Rahdin täsmäytys kuljetustenhallinnassa</span><span class="sxs-lookup"><span data-stu-id="57819-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57819-104">Tässä artikkelissa käsitellään rahdin täsmäytysprosessia.</span><span class="sxs-lookup"><span data-stu-id="57819-104">This article describes the freight reconciliation process.</span></span>

<span data-ttu-id="57819-105">Rahti voidaan täsmäyttää manuaalisesti tai se voidaan määrittää tapahtumaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="57819-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="57819-106">Jos haluat käyttää rahdin automaattista täsmäytystä, sinun on määritettävä päätarkistus, jossa voit määrittää ehdot määrittämään automaattisesti täsmäytettävät rahtilaskut.</span><span class="sxs-lookup"><span data-stu-id="57819-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="57819-107">Rahdin täsmäytysprosessi</span><span class="sxs-lookup"><span data-stu-id="57819-107">The freight reconciliation process</span></span>
<span data-ttu-id="57819-108">Kuljetusmaksut lasketaan hinnan laskennassa, joka on liitetty soveltuvaan rahdinkuljettajaan.</span><span class="sxs-lookup"><span data-stu-id="57819-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="57819-109">Kun kuorma on vahvistettu, rahtilasku luodaan ja rahtitaksat siirretään siihen.</span><span class="sxs-lookup"><span data-stu-id="57819-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="57819-110">Rahtitaksat jaetaan sekalaisina kuluina soveltuvaan lähdeasiakirjaan (ostotilaus, myyntitilaus ja/tai siirtotilaus) sen mukaan, mitä asetuksia tavallisen laskutusprosessin asetuksissa on käytetty.</span><span class="sxs-lookup"><span data-stu-id="57819-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="57819-111">Rahdin täsmäytysprosessi voi alkaa heti, kun rahdinkuljettajan rahtilasku saadaan.</span><span class="sxs-lookup"><span data-stu-id="57819-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="57819-112">Kyse voi olla sähköisestä laskusta tai paperilaskusta.</span><span class="sxs-lookup"><span data-stu-id="57819-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="57819-113">Jos kyse on paperilaskusta, voit luoda sähköisen laskun käyttämällä rahtilaskua mallina.</span><span class="sxs-lookup"><span data-stu-id="57819-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="57819-114">[![Rahdin täsmäytysprosessi](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="57819-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="57819-115">Manuaalinen täsmäytys</span><span class="sxs-lookup"><span data-stu-id="57819-115">Manual reconciliation</span></span>
<span data-ttu-id="57819-116">Jos olet täsmäyttämässä rahtia manuaalisesti, sinun on täsmäytettävä kukin laskun rivi rahtilaskun rivin tai laskutettavan kuorman rivien kanssa.</span><span class="sxs-lookup"><span data-stu-id="57819-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="57819-117">Tämä täsmäytys tehdään **Rahtilaskun ja laskun täsmäytys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="57819-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="57819-118">Jos laskurivin summa ei täsmää rahtilaskun summan kanssa, valitse erolle täsmäytyssyy.</span><span class="sxs-lookup"><span data-stu-id="57819-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="57819-119">Jos täsmäytyksellä on useita syitä, voit jakaa täsmäyttämättömät summan niiden kesken.</span><span class="sxs-lookup"><span data-stu-id="57819-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="57819-120">Täsmäytyksen syy määrittää, miten eriävät summat kirjataan kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="57819-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="57819-121">Kun koko laskutussumma on täsmäytetty, se lähetetään hyväksytyksi, jonka jälkeen kirjauskansio kirjataan.</span><span class="sxs-lookup"><span data-stu-id="57819-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="57819-122">Seuraavassa kuvassa on esitetty, kuinka voit luoda rahtilaskun ja suorittaa rahdin täsmäytyksen Microsoft Dynamics 365 for Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="57819-122">The following illustration shows how to generate a freight invoice and do freight reconciliation in Microsoft Dynamics 365 for Finance and Operations.</span></span> 
<span data-ttu-id="57819-123">[![Dynamics AX:n rahdin täsmäytystehtävät](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="57819-123">[![Freight reconcilation tasks in Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="57819-124">Automaattinen täsmäytys</span><span class="sxs-lookup"><span data-stu-id="57819-124">Automatic reconciliation</span></span>
<span data-ttu-id="57819-125">Jos haluat käyttää automaattista täsmäytystä, sinun on määritettävä täsmäytysaikataulu ja käytettävät laskut ja rahdinkuljettajat.</span><span class="sxs-lookup"><span data-stu-id="57819-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="57819-126">Laskurivit ja rahtilaskut täsmäytetään päätarkistuksen ja rahtilaskun tyypin asetusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="57819-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="57819-127">Kun olet suorittanut automaattisen täsmäytyksen, sinun on käsiteltävä kaikki laskut, joita järjestelmä ei voi täsmäyttää.</span><span class="sxs-lookup"><span data-stu-id="57819-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="57819-128">Nämä laskut on sitten käsiteltävä manuaalisesti ennen kaikkien laskujen kirjaamista maksettaviksi.</span><span class="sxs-lookup"><span data-stu-id="57819-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>



