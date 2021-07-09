---
title: Yleisen varastokirjanpidon tapahtumarekisteri
description: Tässä aiheessa kuvataan yleisiä varastokirjanpidon pääkirjoja, jotka on määritetty valuutan, kalenterin, kirjanpidon ja yrityksen liitoksen avulla.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273148"
---
# <a name="global-inventory-accounting-ledger"></a><span data-ttu-id="adf36-103">Yleisen varastokirjanpidon tapahtumarekisteri</span><span class="sxs-lookup"><span data-stu-id="adf36-103">Global Inventory Accounting ledger</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="adf36-104">Yleisessä varastokirjanpidossa on omat pääkirjansa.</span><span class="sxs-lookup"><span data-stu-id="adf36-104">Global Inventory Accounting has its own set of ledgers.</span></span> <span data-ttu-id="adf36-105">Aina kun asiaankuuluvan yrityksen varastoon liittyvä tapahtuma käsitellään, järjestelmä voi tarvittaessa ottaa tapahtuman huomioon missä tahansa määrässä yleisiä varastokirjanpitoja.</span><span class="sxs-lookup"><span data-stu-id="adf36-105">Each time an inventory-related transaction is processed for a relevant legal entity, the system can account for that transaction in any number of Global Inventory Accounting ledgers, as required.</span></span>

<span data-ttu-id="adf36-106">Kirjanpito on debet- ja kredit-mittarien luettelo.</span><span class="sxs-lookup"><span data-stu-id="adf36-106">A ledger is a register of debit and credit measures.</span></span> <span data-ttu-id="adf36-107">Nämä toimenpiteet luokitellaan kustannuselementtien ja alareskontran tilien avulla.</span><span class="sxs-lookup"><span data-stu-id="adf36-107">These measures are classified by using cost elements and subledger accounts.</span></span> <span data-ttu-id="adf36-108">Yleisiä varastokirjanpidon pääkirja määritetään valuutan, kalenterin, kirjanpidon ja yrityksen liitoksen avulla.</span><span class="sxs-lookup"><span data-stu-id="adf36-108">A Global Inventory Accounting ledger is defined by its combination of a currency, a calendar, a convention, and an association with a legal entity.</span></span>

<span data-ttu-id="adf36-109">Voit määrittää yleiset varastokirjanpitotilit pääkirjoissa seuraavasti **Yleinen varastokirjanpito \> Asennus \> Yleinen varastokirjanpidon pääkirjat**.</span><span class="sxs-lookup"><span data-stu-id="adf36-109">To set up your Global Inventory Accounting ledgers, go to **Global inventory accounting \> Setup \> Global inventory accounting ledgers**.</span></span> <span data-ttu-id="adf36-110">Määritä kullekin kirjanpidolle seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="adf36-110">For each ledger, set the following fields:</span></span>

- <span data-ttu-id="adf36-111">**Nimi** – Anna kirjanpidon nimi.</span><span class="sxs-lookup"><span data-stu-id="adf36-111">**Name** – Enter the name of the ledger.</span></span>
- <span data-ttu-id="adf36-112">**Kuvaus** – anna kirjanpitojen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="adf36-112">**Description** – Enter a description of the ledger.</span></span>
- <span data-ttu-id="adf36-113">**Tilikausikalenteri** – Määritä kirjanpidon tilikausikalenteri.</span><span class="sxs-lookup"><span data-stu-id="adf36-113">**Fiscal calendar** – Specify the fiscal calendar for the ledger.</span></span>
- <span data-ttu-id="adf36-114">**Valuutan ja vaihtokurssin tyyppi** – Tämän pikavälilehden kenttien avulla voit valita kirjanpidon valuutan sekä vaihtokurssityypin.</span><span class="sxs-lookup"><span data-stu-id="adf36-114">**Currency and exchange rate type** – Use the fields on this FastTab to select the accounting currency that the ledger uses, and the exchange rate type.</span></span> <span data-ttu-id="adf36-115">Valittava valuutta voi olla eri kuin valuutta, jota yritys käyttää.</span><span class="sxs-lookup"><span data-stu-id="adf36-115">The currency that you select can differ from the currency that the legal entity uses.</span></span> <span data-ttu-id="adf36-116">Yleisessä varastokirjanpidossa käyttäjät voivat määrittää niin monta kustannuslaskentakirjanpitoa kuin ne edellyttävät.</span><span class="sxs-lookup"><span data-stu-id="adf36-116">In Global Inventory Accounting, users can define as many costing ledgers as they require.</span></span> <span data-ttu-id="adf36-117">Yleinen varastokirjanpito tukee varastolaskentaa useina valuuttoina ja useina arvostuksena.</span><span class="sxs-lookup"><span data-stu-id="adf36-117">Global Inventory Accounting supports inventory accounting in multiple currencies and in multiple valuations.</span></span> <span data-ttu-id="adf36-118">Määritä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="adf36-118">Set the following fields:</span></span>

    - <span data-ttu-id="adf36-119">**Valuutta** – Valitse kustannuslaskentavaluutta, jota varastoon liittyviä arvoja ylläpidetään.</span><span class="sxs-lookup"><span data-stu-id="adf36-119">**Currency** – Select the costing currency that inventory-related values are maintained in.</span></span> <span data-ttu-id="adf36-120">Arvoja ovat varastoarvo, myytyjen tuotteiden kustannukset, kuljetettava varasto ja kaikenlaiset poikkeamat.</span><span class="sxs-lookup"><span data-stu-id="adf36-120">These values include the inventory value, cost of goods sold, inventory in transit, and all kinds of variance.</span></span>
    - <span data-ttu-id="adf36-121">**Vaihtokurssityyppi** – Valitse valuuttakurssi, jota järjestelmän tulisi käyttää tapahtuman määrän muuntamiseen tapahtumavaluutassa ja tuotteiden vakiokustannukset laskentavaluutaksi.</span><span class="sxs-lookup"><span data-stu-id="adf36-121">**Exchange rate type** – Select the exchange rate that the system should use to convert the transaction amount in the transaction currency and the standard cost of the items into the costing currency.</span></span>

- <span data-ttu-id="adf36-122">**Käytännön nimi** – Määritä käytäntö.</span><span class="sxs-lookup"><span data-stu-id="adf36-122">**Convention name** – Specify a convention.</span></span> <span data-ttu-id="adf36-123">Kokous on kokoelma käytäntöjä, jotka määrittävät, miten kustannukset otetaan huomioon tässä kirjanpidossa.</span><span class="sxs-lookup"><span data-stu-id="adf36-123">A convention is a collection of policies that establish how costs will be accounted in this ledger.</span></span>
- <span data-ttu-id="adf36-124">**Yritys** – Kirjanpito ottaa huomioon valitulle yritykselle kirjatut asiakirjat.</span><span class="sxs-lookup"><span data-stu-id="adf36-124">**Legal entity** – The ledger will account the documents that are posted to the selected legal entity.</span></span>
- <span data-ttu-id="adf36-125">**Pohjustus** – Valitse, käsitelläänkö ennen kirjanpidon luomista luodut varastotapahtumat kirjanpidon valuutan ja tapahtuman mukaan.</span><span class="sxs-lookup"><span data-stu-id="adf36-125">**Priming** – Select whether inventory transactions that were created before the ledger was created should be processed according to the currency and convention in the ledger.</span></span> <span data-ttu-id="adf36-126">Valitse jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="adf36-126">Select one of the following values:</span></span>

    - <span data-ttu-id="adf36-127">**Käytössä** – Kirjanpidon tulisi käsitellä tapahtumat, jotka on luotu ennen kirjanpidon luomista.</span><span class="sxs-lookup"><span data-stu-id="adf36-127">**Activated** – The ledger should process transactions that were created before the ledger was created.</span></span>
    - <span data-ttu-id="adf36-128">**Poissa käytöstä** – Kirjanpidon tulisi käsitellä vain tapahtumat, jotka on luotu kirjanpidon luomisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="adf36-128">**Deactivated** – The ledger should process only transactions that are created after the ledger was created.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="adf36-129">**Et** voi palata käyttämään tätä kenttää uusien tiedostojen lisäämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="adf36-129">You will **not** be able to come back and set this field after you enter new documents.</span></span>

- <span data-ttu-id="adf36-130">**Tila** – Järjestelmä määrittää vasta luotujen kirjanpitojen tilaksi automaattisesti *Valmis*.</span><span class="sxs-lookup"><span data-stu-id="adf36-130">**Status** – The system automatically sets the status of newly created ledgers to *Prepare*.</span></span>
