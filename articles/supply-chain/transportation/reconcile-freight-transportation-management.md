---
title: Rahdin täsmäytys kuljetustenhallinnassa
description: Tässä aiheessa käsitellään rahdin täsmäytysprosessia.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSFBDetailReconcile, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8472094ba532d531b15dc4e9f120646b2c3bbe96
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017296"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="4f7ba-103">Rahdin täsmäytys kuljetustenhallinnassa</span><span class="sxs-lookup"><span data-stu-id="4f7ba-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f7ba-104">Tässä aiheessa käsitellään rahdin täsmäytysprosessia.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="4f7ba-105">Rahti voidaan täsmäyttää manuaalisesti tai se voidaan määrittää tapahtumaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="4f7ba-106">Jos haluat käyttää rahdin automaattista täsmäytystä, sinun on määritettävä päätarkistus, jossa voit määrittää ehdot määrittämään automaattisesti täsmäytettävät rahtilaskut.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="4f7ba-107">Rahdin täsmäytysprosessi</span><span class="sxs-lookup"><span data-stu-id="4f7ba-107">The freight reconciliation process</span></span>
<span data-ttu-id="4f7ba-108">Kuljetusmaksut lasketaan hinnan laskennassa, joka on liitetty soveltuvaan rahdinkuljettajaan.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="4f7ba-109">Kun kuorma on vahvistettu, rahtilasku luodaan ja rahtitaksat siirretään siihen.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="4f7ba-110">Rahtitaksat jaetaan sekalaisina kuluina soveltuvaan lähdeasiakirjaan (ostotilaus, myyntitilaus ja/tai siirtotilaus) sen mukaan, mitä asetuksia tavallisen laskutusprosessin asetuksissa on käytetty.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="4f7ba-111">Rahdin täsmäytysprosessi voi alkaa heti, kun rahdinkuljettajan rahtilasku saadaan.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="4f7ba-112">Kyse voi olla sähköisestä laskusta tai paperilaskusta.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="4f7ba-113">Jos kyse on paperilaskusta, voit luoda sähköisen laskun käyttämällä rahtilaskua mallina.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="4f7ba-114">[![Rahdin täsmäytysprosessi](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="4f7ba-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="4f7ba-115">Manuaalinen täsmäytys</span><span class="sxs-lookup"><span data-stu-id="4f7ba-115">Manual reconciliation</span></span>
<span data-ttu-id="4f7ba-116">Jos olet täsmäyttämässä rahtia manuaalisesti, sinun on täsmäytettävä kukin laskun rivi rahtilaskun rivin tai laskutettavan kuorman rivien kanssa.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="4f7ba-117">Tämä täsmäytys tehdään **Rahtilaskun ja laskun täsmäytys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="4f7ba-118">Jos laskurivin summa ei täsmää rahtilaskun summan kanssa, valitse erolle täsmäytyssyy.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="4f7ba-119">Jos täsmäytyksellä on useita syitä, voit jakaa täsmäyttämättömät summan niiden kesken.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="4f7ba-120">Täsmäytyksen syy määrittää, miten eriävät summat kirjataan kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="4f7ba-121">Kun koko laskutussumma on täsmäytetty, se lähetetään hyväksytyksi, jonka jälkeen kirjauskansio kirjataan.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="4f7ba-122">Seuraavassa kuvassa on esitetty, kuinka voit luoda rahtilaskun ja suorittaa rahdin täsmäytyksen.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span> 
<span data-ttu-id="4f7ba-123">[![Rahdin täsmäytystehtävät](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="4f7ba-123">[![Freight reconcilation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="4f7ba-124">Automaattinen täsmäytys</span><span class="sxs-lookup"><span data-stu-id="4f7ba-124">Automatic reconciliation</span></span>
<span data-ttu-id="4f7ba-125">Jos haluat käyttää automaattista täsmäytystä, sinun on määritettävä täsmäytysaikataulu ja käytettävät laskut ja rahdinkuljettajat.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="4f7ba-126">Laskurivit ja rahtilaskut täsmäytetään päätarkistuksen ja rahtilaskun tyypin asetusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="4f7ba-127">Kun olet suorittanut automaattisen täsmäytyksen, sinun on käsiteltävä kaikki laskut, joita järjestelmä ei voi täsmäyttää.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="4f7ba-128">Nämä laskut on sitten käsiteltävä manuaalisesti ennen kaikkien laskujen kirjaamista maksettaviksi.</span><span class="sxs-lookup"><span data-stu-id="4f7ba-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>



