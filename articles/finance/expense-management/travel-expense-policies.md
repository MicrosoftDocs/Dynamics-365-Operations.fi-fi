---
title: Määritä kulukäytännöt
description: Voit määrittää kulukäytäntöjä, joita työntekijöidesi on noudatettava kirjatessaan ja lähettäessään kuluraportteja ja matkustusehdotuksia Microsoft Dynamics 365 Financessa.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7d3b4a8f6cf74bb1fe7e53a4dfdd607f604e16e3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187449"
---
# <a name="define-expense-policies"></a><span data-ttu-id="41aae-103">Määritä kulukäytännöt</span><span class="sxs-lookup"><span data-stu-id="41aae-103">Define expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41aae-104">Voit määrittää käytäntöjä tai sääntöjä, joita työntekijöiden on noudatettava kirjatessaan ja lähettäessään kuluraportteja ja matkustusehdotuksia.</span><span class="sxs-lookup"><span data-stu-id="41aae-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="41aae-105">Kulukäytäntöjen käyttöönotto auttaa hallitsemaan kuluja tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="41aae-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="41aae-106">Voit esimerkiksi määrittää käytännön, jonka mukaan hotellikulut New Yorkissa yötä kohti eivät saa ylittää 250 Yhdysvaltain dollaria.</span><span class="sxs-lookup"><span data-stu-id="41aae-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="41aae-107">Jos työntekijä lähettää kuluraportin tai matkustusehdotuksen, jonka huoneen hinta ylittää tämän summan, järjestelmä ilmoittaa</span><span class="sxs-lookup"><span data-stu-id="41aae-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="41aae-108">työntekijälle, että kulukäytännön summa on ylitetty.</span><span class="sxs-lookup"><span data-stu-id="41aae-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="41aae-109">Voit määrittää työntekijälle lähetettävän viestin, kun</span><span class="sxs-lookup"><span data-stu-id="41aae-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="41aae-110">määrität käytännön.</span><span class="sxs-lookup"><span data-stu-id="41aae-110">define the policy.</span></span>      
        
<span data-ttu-id="41aae-111">Voit määrittää kolmenlaisia käytäntöjä:</span><span class="sxs-lookup"><span data-stu-id="41aae-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="41aae-112">Varoitus – antaa työntekijän lähettää kuluraportin tai matkustusehdotuksen, mutta kulu merkitään kaikille hyväksyjille ja</span><span class="sxs-lookup"><span data-stu-id="41aae-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="41aae-113">myöhempää raportointia varten.</span><span class="sxs-lookup"><span data-stu-id="41aae-113">for later reporting.</span></span>        

- <span data-ttu-id="41aae-114">Virhe – edellyttää, että työntekijä muuttaa kulua vastaamaan käytäntöä ennen kuluraportin tai matkustusehdotuksen lähettämistä.</span><span class="sxs-lookup"><span data-stu-id="41aae-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="41aae-115">Peruse – edellyttää, että työntekijä tai esimies antaa käytännön summan ylittämiselle perusteen ennen kuluraportin tai matkustusehdotuksen lähettämistä.</span><span class="sxs-lookup"><span data-stu-id="41aae-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="41aae-116">Käytännön vinkkejä</span><span class="sxs-lookup"><span data-stu-id="41aae-116">Policy tips</span></span>
<span data-ttu-id="41aae-117">Seuraavassa on muutamia ehdotuksia, jotka voivat auttaa sinua uusien kulujen hallintakäytäntöjen luomisessa.</span><span class="sxs-lookup"><span data-stu-id="41aae-117">Here are a few suggestions that can assist you whe creating new policies for expense management.</span></span> 
* <span data-ttu-id="41aae-118">Käytännöt ovat riippuvaisia voimaantulopäivästä, eivätkä ne tule voimaan, jos käytäntö luodaan sen päivämäärän jälkeen, jolloin kulu on syntynyt.</span><span class="sxs-lookup"><span data-stu-id="41aae-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="41aae-119">Jos esimerkiksi olet luomassa uutta käytäntöä, jonka mukaan $50 enimmäisateriakustannukset ovat voimassa, kaikkia eilisestä lähtien määritettyjä kuluja ei tarkisteta tätä käytäntöä vasten.</span><span class="sxs-lookup"><span data-stu-id="41aae-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="41aae-120">Kun luot käytännön kululuokalle, joka voidaan määrittää, harkitse kulujen rivityypin ehdon lisäämistä.</span><span class="sxs-lookup"><span data-stu-id="41aae-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="41aae-121">Jotkin käytännöt, kuten kuittauksen vaatiminen, eivät ehkä ole järkeviä eriteltyjä rivejä varten, ja niitä tulisi käyttää vain otsikkorivillä tai ei-eriteltyjen rivien yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="41aae-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="41aae-122">Käytäntöjen arvioiminen</span><span class="sxs-lookup"><span data-stu-id="41aae-122">When to evaluate policies</span></span>

<span data-ttu-id="41aae-123">Kulujenhallinnan parametreissa voit joko arvioida kulunhallintakäytäntöjä, kun rivi tallennetaan tai kun kuluraportti lähetetään.</span><span class="sxs-lookup"><span data-stu-id="41aae-123">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="41aae-124">Jos päätät arvioida, milloin rivi tallennetaan, tämä varmistaa, että käyttäjillä on aiemmin ollut näkyvyyttä, jotta he voivat täyttää kuluraportin kerralla.</span><span class="sxs-lookup"><span data-stu-id="41aae-124">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="41aae-125">Muussa tapauksessa voit viivyttää käytännön arviointia ja säästää aikaa, jos oikeellisuustarkistus tapahtuu lopussa, työn kulkuun lähettämisen aikana.</span><span class="sxs-lookup"><span data-stu-id="41aae-125">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>