---
title: Määritä yrityksen pankkitilit ISO20022-tilisiirtoja varten
description: Näiden ohjeiden avulla voit määrittää SEPA-maksutiedoston luomisessa vaadittavat yrityskohtaiset pankkitilin tiedot.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca0f0af3cccd4110c3da1703112a5b0f29bd64ad
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988167"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="3301c-103">Määritä yrityksen pankkitilit ISO20022-tilisiirtoja varten</span><span class="sxs-lookup"><span data-stu-id="3301c-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3301c-104">Näiden ohjeiden avulla voit määrittää SEPA-maksutiedoston luomisessa vaadittavat yrityskohtaiset pankkitilin tiedot.</span><span class="sxs-lookup"><span data-stu-id="3301c-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="3301c-105">Voit määrittää ISO 20022 -pankkisiirtomuodon luomiseen vaadittavat tiedot, mutta muodosta riippuen voit joutua määrittämään muita tietoja, kuten yrityksen tunnuksen tai lajittelukoodin.</span><span class="sxs-lookup"><span data-stu-id="3301c-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="3301c-106">Tämän menettelyn luomisessa käytetty esittely-yritys on DEMF.</span><span class="sxs-lookup"><span data-stu-id="3301c-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="3301c-107">Tämä on toinen viidestä tehtävästä, joilla esitellään toimittajamaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="3301c-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="3301c-108">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="3301c-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="3301c-109">IBAN- ja SWIFT-koodin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3301c-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="3301c-110">Siirry kohtaan Maksuliikenteen hallinta > Pankkitilit.</span><span class="sxs-lookup"><span data-stu-id="3301c-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="3301c-111">Pikasuodattimen avulla voit suodattaa Pankkitili-kentän DEMF OPER -arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="3301c-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="3301c-112">Avaa pankkitilin tiedot valitsemalla DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="3301c-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="3301c-113">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="3301c-113">Click Edit.</span></span>
5. <span data-ttu-id="3301c-114">Laajenna Lisätunnus-osa.</span><span class="sxs-lookup"><span data-stu-id="3301c-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="3301c-115">Kirjoita IBAN-kenttään DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="3301c-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="3301c-116">Syötä SWIFT-koodi-kenttään DEUTDEFF.</span><span class="sxs-lookup"><span data-stu-id="3301c-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="3301c-117">Huomaa, ettei SWIFT\BIC ole pakollinen monissa maksumuodoissa; se on kuitenkin suositeltavaa rekisteröidä pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="3301c-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="3301c-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3301c-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="3301c-119">Yrityksen pankkitilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3301c-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="3301c-120">Siirry kohtaan Organisaation hallinto > Organisaatiot > Yritykset.</span><span class="sxs-lookup"><span data-stu-id="3301c-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="3301c-121">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="3301c-121">Click Edit.</span></span>
3. <span data-ttu-id="3301c-122">Laajenna Pankkitilitiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="3301c-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="3301c-123">Syötä tai valitse arvo Pankkitili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3301c-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="3301c-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3301c-124">Click Save.</span></span>

