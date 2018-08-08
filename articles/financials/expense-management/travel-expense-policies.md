---
title: "Määritä kulukäytännöt"
description: "Voit määrittää kulukäytännöt, joita työntekijöiden on noudatettava kirjatessaan ja lähettäessään kuluraportteja ja matkustusehdotuksia Microsoft Dynamics 365 for Finance and Operationsissa."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 04eaff110fea021ddee32be650be540894eb703b
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---

# <a name="expense-policies"></a><span data-ttu-id="3f505-103">Kulukäytännöt</span><span class="sxs-lookup"><span data-stu-id="3f505-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f505-104">Voit määrittää käytäntöjä tai sääntöjä, joita työntekijöiden on noudatettava kirjatessaan ja lähettäessään kuluraportteja ja matkustusehdotuksia.</span><span class="sxs-lookup"><span data-stu-id="3f505-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="3f505-105">Kulukäytäntöjen käyttöönotto auttaa hallitsemaan kuluja tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="3f505-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="3f505-106">Voit esimerkiksi määrittää käytännön, jonka mukaan hotellikulut New Yorkissa yötä kohti eivät saa ylittää 250 Yhdysvaltain dollaria.</span><span class="sxs-lookup"><span data-stu-id="3f505-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="3f505-107">Jos työntekijä lähettää kuluraportin tai matkustusehdotuksen, jonka huoneen hinta ylittää tämän summan, järjestelmä ilmoittaa</span><span class="sxs-lookup"><span data-stu-id="3f505-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="3f505-108">työntekijälle, että kulukäytännön summa on ylitetty.</span><span class="sxs-lookup"><span data-stu-id="3f505-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="3f505-109">Voit määrittää työntekijälle lähetettävän viestin, kun</span><span class="sxs-lookup"><span data-stu-id="3f505-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="3f505-110">määrität käytännön.</span><span class="sxs-lookup"><span data-stu-id="3f505-110">define the policy.</span></span>      
        
<span data-ttu-id="3f505-111">Voit määrittää kolmenlaisia käytäntöjä:</span><span class="sxs-lookup"><span data-stu-id="3f505-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="3f505-112">Varoitus – antaa työntekijän lähettää kuluraportin tai matkustusehdotuksen, mutta kulu merkitään kaikille hyväksyjille ja</span><span class="sxs-lookup"><span data-stu-id="3f505-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="3f505-113">myöhempää raportointia varten.</span><span class="sxs-lookup"><span data-stu-id="3f505-113">for later reporting.</span></span>        

- <span data-ttu-id="3f505-114">Virhe – edellyttää, että työntekijä muuttaa kulua vastaamaan käytäntöä ennen kuluraportin tai matkustusehdotuksen lähettämistä.</span><span class="sxs-lookup"><span data-stu-id="3f505-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
  - <span data-ttu-id="3f505-115">Peruse – edellyttää, että työntekijä tai esimies antaa käytännön summan ylittämiselle perusteen ennen kuluraportin tai matkustusehdotuksen lähettämistä.</span><span class="sxs-lookup"><span data-stu-id="3f505-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        
 
  <span data-ttu-id="3f505-116">Voit myös määrittää päivämäärävälin, jonka aikana kulukäytännöt ovat voimassa.</span><span class="sxs-lookup"><span data-stu-id="3f505-116">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="3f505-117">Esimerkiksi lentojen hinta Tanskan</span><span class="sxs-lookup"><span data-stu-id="3f505-117">For example, airline fares for flights between Denmark</span></span>      
  <span data-ttu-id="3f505-118">ja New Yorkin välillä voi olla kallis vilkkaimpana loma-aikana.</span><span class="sxs-lookup"><span data-stu-id="3f505-118">and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="3f505-119">Voit määrittää lentokulujen säännön rajoittamaan</span><span class="sxs-lookup"><span data-stu-id="3f505-119">You can define a flight expense rule that restricts the</span></span>      
  <span data-ttu-id="3f505-120">New Yorkiin suuntautuvien lentojen hinnaksi enintään 5 000 DDK. Voit lisäksi määrittää, että tämä sääntö on voimassa toukokuun 15. päivän ja</span><span class="sxs-lookup"><span data-stu-id="3f505-120">cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and</span></span>      
  <span data-ttu-id="3f505-121">syyskuun 15. päivän välisenä aikana.</span><span class="sxs-lookup"><span data-stu-id="3f505-121">September 15.</span></span>

