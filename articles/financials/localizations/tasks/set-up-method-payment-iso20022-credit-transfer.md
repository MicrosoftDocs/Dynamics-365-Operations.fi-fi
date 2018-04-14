--- 
title: "Maksutavan määrittäminen ISO20022-tilisiirtoja varten"
description: "Näiden ohjeiden avulla voi määrittää toimittajan ISO20022-tilisiirron tai minkä tahansa muun maksutyypin luomaan tiedostoja sähköisen raportoinnin avulla."
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
ms.openlocfilehash: 6c45324b1523e29aa5c6274b289fa823bf66ea12
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="45b36-103">Maksutavan määrittäminen ISO20022-tilisiirtoja varten</span><span class="sxs-lookup"><span data-stu-id="45b36-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="45b36-104">Näiden ohjeiden avulla voi määrittää toimittajan ISO20022-tilisiirron tai minkä tahansa muun maksutyypin luomaan tiedostoja sähköisen raportoinnin avulla.</span><span class="sxs-lookup"><span data-stu-id="45b36-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="45b36-105">Viennin muotokonfiguraatiot ja maksutilit on määritettävä ennen tämän tehtävän suorittamista.</span><span class="sxs-lookup"><span data-stu-id="45b36-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="45b36-106">Tämän tehtävän luomisessa käytettiin esittelytietojen DEMF-yritystä.</span><span class="sxs-lookup"><span data-stu-id="45b36-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="45b36-107">Tämä on kolmas viidestä tehtävästä, joilla esitellään toimittajamaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="45b36-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="45b36-108">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="45b36-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="45b36-109">Siirry kohtaan Ostoreskontra > Maksun asetukset > Maksutavat.</span><span class="sxs-lookup"><span data-stu-id="45b36-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="45b36-110">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="45b36-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="45b36-111">Voit esimerkiksi suodattaa Maksutapa-kenttää arvolla SEPA CT.</span><span class="sxs-lookup"><span data-stu-id="45b36-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="45b36-112">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="45b36-112">Click Edit.</span></span>
4. <span data-ttu-id="45b36-113">Valitse Kausi-kentässä Yhteensä.</span><span class="sxs-lookup"><span data-stu-id="45b36-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="45b36-114">Valitse Maksutyyppi-kentässä Sähköinen maksu.</span><span class="sxs-lookup"><span data-stu-id="45b36-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="45b36-115">Laajenna Tiedostomuodot-osa.</span><span class="sxs-lookup"><span data-stu-id="45b36-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="45b36-116">Valitse Yleinen sähköinen raportointi -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="45b36-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="45b36-117">Syötä Vie muotokonfiguraatio -kenttään arvo tai valitse arvo.</span><span class="sxs-lookup"><span data-stu-id="45b36-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="45b36-118">Valitse luettelosta arvo ISO20022 - tilisiirto (DE).</span><span class="sxs-lookup"><span data-stu-id="45b36-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="45b36-119">Jos luettelo on tyhjä, tuotua ja aktiivista toimittajan maksun viennin muotokonfiguraatiota ei ole.</span><span class="sxs-lookup"><span data-stu-id="45b36-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="45b36-120">Valitse Tilityyppi-kentässä Pankki.</span><span class="sxs-lookup"><span data-stu-id="45b36-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="45b36-121">Syötä Maksutili-kenttään arvot DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="45b36-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="45b36-122">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="45b36-122">Click Save.</span></span>


