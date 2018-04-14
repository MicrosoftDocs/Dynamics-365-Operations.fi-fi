---
title: "Luottokirjeet ja tuontiperittävät"
description: "Tässä artikkelissa on yleisiä tietoja remburssista ja tuontiperittävistä. Molempia pankkitositteita käytetään usein valtioiden rajojen yli tapahtuvassa tavaroiden ostossa ja myynnissä."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankLCImport
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 18321
ms.assetid: 5c97ab81-632b-4043-a940-674bcb496c80
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3bab4b9981f58c133e8c5ed693e6ed345248809d
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="letters-of-credit-and-import-collections"></a><span data-ttu-id="86589-104">Luottokirjeet ja tuontiperittävät</span><span class="sxs-lookup"><span data-stu-id="86589-104">Letters of credit and import collections</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="86589-105">Tässä artikkelissa on yleisiä tietoja remburssista ja tuontiperittävistä.</span><span class="sxs-lookup"><span data-stu-id="86589-105">This article provides general information about letters of credit and import collections.</span></span> <span data-ttu-id="86589-106">Molempia pankkitositteita käytetään usein valtioiden rajojen yli tapahtuvassa tavaroiden ostossa ja myynnissä.</span><span class="sxs-lookup"><span data-stu-id="86589-106">Both types of bank document are often used for the purchase and sale of goods across international borders.</span></span>

<a name="letters-of-credit"></a><span data-ttu-id="86589-107">Luottokirjeet</span><span class="sxs-lookup"><span data-stu-id="86589-107">Letters of credit</span></span>
-----------------

<span data-ttu-id="86589-108">Rembursseja käytetään kansainvälisissä liiketoimissa varmistamaan, että maksut suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="86589-108">Letters of credit are used for international transactions and help guarantee that payments will be made.</span></span> <span data-ttu-id="86589-109">Remburssi on pankin antama sopimus, jossa pankki suostuu varmistamaan maksun ostajan puolesta, jos ostajan ja myyjän väliset ehdot täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="86589-109">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to guarantee payment on behalf of a buyer, provided that the terms of the agreement between the buyer and seller are met.</span></span> <span data-ttu-id="86589-110">Remburssi tunnetaan myös luottokirjeenä.</span><span class="sxs-lookup"><span data-stu-id="86589-110">A letter of credit is also referred to as a documentary credit (DC).</span></span>

<span data-ttu-id="86589-111">Tärkeässä remburssissa yritys on ostaja tai remburssin hakija.</span><span class="sxs-lookup"><span data-stu-id="86589-111">For an import letter of credit, the legal entity is the buyer or the applicant for the letter of credit.</span></span> <span data-ttu-id="86589-112">Vientiremburssissa yritys on myyjä tai remburssin edunsaaja.</span><span class="sxs-lookup"><span data-stu-id="86589-112">For an export letter of credit, the legal entity is the seller or the beneficiary of the letter of credit.</span></span> <span data-ttu-id="86589-113">Luottokirjeen osapuolet ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="86589-113">The following parties are involved in a letter of credit:</span></span>

-   <span data-ttu-id="86589-114">hakija (ostaja), joka aikoo maksaa tavarat</span><span class="sxs-lookup"><span data-stu-id="86589-114">The applicant (buyer) who intends to pay for the goods</span></span>
-   <span data-ttu-id="86589-115">saaja (myyjä), joka vastaanottaa maksun</span><span class="sxs-lookup"><span data-stu-id="86589-115">The beneficiary (seller) who will receive the payment</span></span>
-   <span data-ttu-id="86589-116">luottokirjeen myöntämä pankki</span><span class="sxs-lookup"><span data-stu-id="86589-116">The issuing bank that issues the letter of credit</span></span>
-   <span data-ttu-id="86589-117">välittäjäpankki, joka suorittaa liiketapahtuman hakijan puolesta.</span><span class="sxs-lookup"><span data-stu-id="86589-117">The advising bank that carries out the transaction on behalf of the applicant</span></span>

<span data-ttu-id="86589-118">Luottokirje sisältää kuvauksen tavaroista, mahdollisesti tarvittavat asiakirjat, lähetyspäivän sekä vanhentumispäivän, jonka jälkeen maksu peruuntuu.</span><span class="sxs-lookup"><span data-stu-id="86589-118">The letter of credit includes a description of the goods, any required documents, the date of shipment, and the expiration date after which payment won't be made.</span></span> <span data-ttu-id="86589-119">Viranomainen pankki kerää marginaalin remburssista.</span><span class="sxs-lookup"><span data-stu-id="86589-119">The issuing bank collects a margin for the letter of credit.</span></span> 

<span data-ttu-id="86589-120">Luottokirje voi olla **peruutettavissa** tai **peruuttamaton**.</span><span class="sxs-lookup"><span data-stu-id="86589-120">A letter of credit can be **revocable** or **irrevocable**.</span></span> <span data-ttu-id="86589-121">Luottokirje voi olla **siirrettävissä**, **ei-siirrettävissä** tai **automaattisesti uudistettava**.</span><span class="sxs-lookup"><span data-stu-id="86589-121">The nature of a letter of credit can be **transferable**, **non-transferable**, or **revolving**.</span></span> <span data-ttu-id="86589-122">Yleensä remburssi on peruuttamaton ja vahvistettu sopimus, jossa luvataan että maksu suoritetaan tietylle saajalle, kun täydellinen ja tarkka lähetysasiakirja on esitetty.</span><span class="sxs-lookup"><span data-stu-id="86589-122">Typically, a letter of credit is an irrevocable and confirmed agreement that payment will be made to a specific beneficiary upon submission of complete and accurate shipping documentation.</span></span>

## <a name="import-collections"></a><span data-ttu-id="86589-123">Tuontiperittävät</span><span class="sxs-lookup"><span data-stu-id="86589-123">Import collections</span></span>
<span data-ttu-id="86589-124">Tuontiperittävä on pankin ja viejän (myyjän) välinen sopimus, jossa pankki suostuu toimittamaan lähetysasiakirjan kansainväliselle tuojalle (ostaja).</span><span class="sxs-lookup"><span data-stu-id="86589-124">An import collection is an agreement between the bank and the exporter (seller), in which the bank agrees to deliver the shipping documentation to the international importer (buyer).</span></span> <span data-ttu-id="86589-125">Pankin odotetaan toimittavan lähetyskirja lähetettyjen tuotteiden käteismaksun vastaanoton tai maksun allekirjoitetun luonnoksen vastaanoton yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="86589-125">The bank is expected to deliver the shipping documentation upon receipt of payment for the shipped goods in cash, or upon receipt of a signed draft toward the payment.</span></span> 

<span data-ttu-id="86589-126">Tuontiperittävän avulla on mahdollista varmistaa, että myyjä saa maksun, kun ostaja saa tuotujen tavaroiden lähetysasiakirjat.</span><span class="sxs-lookup"><span data-stu-id="86589-126">An import collection helps guarantee that the seller is paid when the buyer collects the shipping documents to take delivery of the imported goods.</span></span>




