---
title: Maksutavan määrittäminen ISO20022-tilisiirtoja varten
description: Näiden ohjeiden avulla voi määrittää toimittajan ISO20022-tilisiirron tai minkä tahansa muun maksutyypin luomaan tiedostoja sähköisen raportoinnin avulla.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92bc314e69628f2a287ba7c9a7c2d3d73a0bfd33
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988099"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="21d0c-103">Maksutavan määrittäminen ISO20022-tilisiirtoja varten</span><span class="sxs-lookup"><span data-stu-id="21d0c-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="21d0c-104">Näiden ohjeiden avulla voi määrittää toimittajan ISO20022-tilisiirron tai minkä tahansa muun maksutyypin luomaan tiedostoja sähköisen raportoinnin avulla.</span><span class="sxs-lookup"><span data-stu-id="21d0c-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="21d0c-105">Viennin muotokonfiguraatiot ja maksutilit on määritettävä ennen tämän tehtävän suorittamista.</span><span class="sxs-lookup"><span data-stu-id="21d0c-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="21d0c-106">Tämän tehtävän luomisessa käytettiin esittelytietojen DEMF-yritystä.</span><span class="sxs-lookup"><span data-stu-id="21d0c-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="21d0c-107">Tämä on kolmas viidestä tehtävästä, joilla esitellään toimittajamaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="21d0c-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="21d0c-108">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="21d0c-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="21d0c-109">Siirry kohtaan Ostoreskontra > Maksun asetukset > Maksutavat.</span><span class="sxs-lookup"><span data-stu-id="21d0c-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="21d0c-110">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="21d0c-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="21d0c-111">Voit esimerkiksi suodattaa Maksutapa-kenttää arvolla SEPA CT.</span><span class="sxs-lookup"><span data-stu-id="21d0c-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="21d0c-112">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="21d0c-112">Click Edit.</span></span>
4. <span data-ttu-id="21d0c-113">Valitse Kausi-kentässä Yhteensä.</span><span class="sxs-lookup"><span data-stu-id="21d0c-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="21d0c-114">Valitse Maksutyyppi-kentässä Sähköinen maksu.</span><span class="sxs-lookup"><span data-stu-id="21d0c-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="21d0c-115">Laajenna Tiedostomuodot-osa.</span><span class="sxs-lookup"><span data-stu-id="21d0c-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="21d0c-116">Valitse Yleinen sähköinen raportointi -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="21d0c-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="21d0c-117">Syötä Vie muotokonfiguraatio -kenttään arvo tai valitse arvo.</span><span class="sxs-lookup"><span data-stu-id="21d0c-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="21d0c-118">Valitse luettelosta arvo ISO20022 - tilisiirto (DE).</span><span class="sxs-lookup"><span data-stu-id="21d0c-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="21d0c-119">Jos luettelo on tyhjä, tuotua ja aktiivista toimittajan maksun viennin muotokonfiguraatiota ei ole.</span><span class="sxs-lookup"><span data-stu-id="21d0c-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="21d0c-120">Valitse Tilityyppi-kentässä Pankki.</span><span class="sxs-lookup"><span data-stu-id="21d0c-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="21d0c-121">Syötä Maksutili-kenttään arvot DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="21d0c-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="21d0c-122">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="21d0c-122">Click Save.</span></span>

