---
title: Toimittajien maksujen luominen ja tuonti ISO20022-maksumuodossa
description: Näiden ohjeiden avulla voit luoda maksurivit toimittajan maksukirjauskansioon sekä luoda toimittajan maksutiedostot ISO2022-pankkisiirtoesimerkin avulla.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b589d64a4446420164175b41f435cf48daac01a9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "340542"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="4eca2-103">Toimittajien maksujen luominen ja tuonti ISO20022-maksumuodossa</span><span class="sxs-lookup"><span data-stu-id="4eca2-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4eca2-104">Tässä ohjeaiheessa käsitellään, miten voit luoda maksurivit toimittajan maksukirjauskansioon sekä luoda toimittajan maksutiedostot ISO2022-pankkisiirtoesimerkin avulla.</span><span class="sxs-lookup"><span data-stu-id="4eca2-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="4eca2-105">Tämä on viides viidestä tehtävästä, joilla esitellään toimittajamaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="4eca2-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="4eca2-106">Käytä tämän esimerkin täyttämiseen DEMF-demotietoja.</span><span class="sxs-lookup"><span data-stu-id="4eca2-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="4eca2-107">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="4eca2-107">Example</span></span>

1.  <span data-ttu-id="4eca2-108">Valitse **Ostoreskontra > Maksut > Maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="4eca2-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.  <span data-ttu-id="4eca2-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4eca2-109">Click **New**.</span></span>
3.  <span data-ttu-id="4eca2-110">Anna tai valitse arvo **Nimi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="4eca2-110">In the **Name** field, enter or select a value.</span></span>
4.  <span data-ttu-id="4eca2-111">Valitse**Rivit > Maksuehdotus -> Luo maksuehdotus**.</span><span class="sxs-lookup"><span data-stu-id="4eca2-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.  <span data-ttu-id="4eca2-112">Laajenna **Sisällytettävät tietueet** -osa.</span><span class="sxs-lookup"><span data-stu-id="4eca2-112">Expand the **Records to include** section.</span></span>
6.  <span data-ttu-id="4eca2-113">Valitse **Suodatin**.</span><span class="sxs-lookup"><span data-stu-id="4eca2-113">Click **Filter**.</span></span>
7.  <span data-ttu-id="4eca2-114">Valitse luettelossa **Toimittajat-taulukon** ja **Toimittajan tili -kentän** rivi.</span><span class="sxs-lookup"><span data-stu-id="4eca2-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.  <span data-ttu-id="4eca2-115">Anna tai valitse arvo **Ehdot**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="4eca2-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="4eca2-116">Voit käyttää kaikkia maksettavien toimittajatapahtumien valintaehtoja, tässä esimerkissä toimittajan tilinä käytetään arvoa DE-001.</span><span class="sxs-lookup"><span data-stu-id="4eca2-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12. <span data-ttu-id="4eca2-117">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="4eca2-117">Click **OK**.</span></span>
13. <span data-ttu-id="4eca2-118">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="4eca2-118">Click **OK**.</span></span>
14. <span data-ttu-id="4eca2-119">Valitse **Luo maksut**.</span><span class="sxs-lookup"><span data-stu-id="4eca2-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="4eca2-120">Luo ISO20022-maksutiedosto.</span><span class="sxs-lookup"><span data-stu-id="4eca2-120">Generate an ISO20022 payment file.</span></span>
    1.  <span data-ttu-id="4eca2-121">Valitse **Muodosta maksut**.</span><span class="sxs-lookup"><span data-stu-id="4eca2-121">Click **Generate payments**.</span></span>
    2.  <span data-ttu-id="4eca2-122">Anna tai valitse arvo **Maksutapa**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="4eca2-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.  <span data-ttu-id="4eca2-123">Kirjoita arvo **Tiedostonimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4eca2-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="4eca2-124">Koska tässä merkissä käytetään EUR-maksua, muodostettu tiedosto on SEPA-yhteensopiva.</span><span class="sxs-lookup"><span data-stu-id="4eca2-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="4eca2-125">Maksuja voidaan luoda muilla valuutoilla myös ISO20022-tilisiirtona ja muina toimittaja maksumuotoina.</span><span class="sxs-lookup"><span data-stu-id="4eca2-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.  <span data-ttu-id="4eca2-126">Anna tai valitse arvo **Pankkitili**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="4eca2-126">In the **Bank account** field, enter or select a value.</span></span>

