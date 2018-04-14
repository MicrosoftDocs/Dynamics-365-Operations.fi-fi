--- 
title: "Määritä yrityksen pankkitilit ISO20022-tilisiirtoja varten"
description: "Näiden ohjeiden avulla voit määrittää SEPA-maksutiedoston luomisessa vaadittavat yrityskohtaiset pankkitilin tiedot."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 50cc79c076feac17b945c632d584e99b808d00ad
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="34fe7-103">Määritä yrityksen pankkitilit ISO20022-tilisiirtoja varten</span><span class="sxs-lookup"><span data-stu-id="34fe7-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34fe7-104">Näiden ohjeiden avulla voit määrittää SEPA-maksutiedoston luomisessa vaadittavat yrityskohtaiset pankkitilin tiedot.</span><span class="sxs-lookup"><span data-stu-id="34fe7-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="34fe7-105">Voit määrittää ISO 20022 -pankkisiirtomuodon luomiseen vaadittavat tiedot, mutta muodosta riippuen voit joutua määrittämään muita tietoja, kuten yrityksen tunnuksen tai lajittelukoodin.</span><span class="sxs-lookup"><span data-stu-id="34fe7-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="34fe7-106">Tämän menettelyn luomisessa käytetty esittely-yritys on DEMF.</span><span class="sxs-lookup"><span data-stu-id="34fe7-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="34fe7-107">Tämä on toinen viidestä tehtävästä, joilla esitellään toimittajamaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="34fe7-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="34fe7-108">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="34fe7-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="34fe7-109">IBAN- ja SWIFT-koodin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="34fe7-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="34fe7-110">Siirry kohtaan Maksuliikenteen hallinta > Pankkitilit.</span><span class="sxs-lookup"><span data-stu-id="34fe7-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="34fe7-111">Pikasuodattimen avulla voit suodattaa Pankkitili-kentän DEMF OPER -arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="34fe7-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="34fe7-112">Avaa pankkitilin tiedot valitsemalla DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="34fe7-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="34fe7-113">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="34fe7-113">Click Edit.</span></span>
5. <span data-ttu-id="34fe7-114">Laajenna Lisätunnus-osa.</span><span class="sxs-lookup"><span data-stu-id="34fe7-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="34fe7-115">Kirjoita IBAN-kenttään DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="34fe7-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="34fe7-116">Syötä SWIFT-koodi-kenttään DEUTDEFF.</span><span class="sxs-lookup"><span data-stu-id="34fe7-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="34fe7-117">Huomaa, ettei SWIFT\BIC ole pakollinen monissa maksumuodoissa; se on kuitenkin suositeltavaa rekisteröidä pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="34fe7-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="34fe7-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="34fe7-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="34fe7-119">Yrityksen pankkitilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="34fe7-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="34fe7-120">Siirry kohtaan Organisaation hallinto > Organisaatiot > Yritykset.</span><span class="sxs-lookup"><span data-stu-id="34fe7-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="34fe7-121">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="34fe7-121">Click Edit.</span></span>
3. <span data-ttu-id="34fe7-122">Laajenna Pankkitilitiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="34fe7-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="34fe7-123">Syötä tai valitse arvo Pankkitili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="34fe7-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="34fe7-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="34fe7-124">Click Save.</span></span>


