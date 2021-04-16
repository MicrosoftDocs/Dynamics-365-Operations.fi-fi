---
title: Maksutavan määrittäminen ISO20022-suoraveloitusta varten
description: Näiden ohjeiden avulla voi määrittää asiakkaan ISO20022-suoraveloituksen tai minkä tahansa muun maksutyypin sähköisen raportoinnin avulla.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c6a692553867d7e8679099210dc44b9d9e4d0f1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838679"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="52ce7-103">Maksutavan määrittäminen ISO20022-suoraveloitusta varten</span><span class="sxs-lookup"><span data-stu-id="52ce7-103">Setup method of payment for ISO20022 direct debit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52ce7-104">Näiden ohjeiden avulla voi määrittää asiakkaan ISO20022-suoraveloituksen tai minkä tahansa muun maksutyypin sähköisen raportoinnin avulla.</span><span class="sxs-lookup"><span data-stu-id="52ce7-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="52ce7-105">Viennin muotokonfiguraatiot ja maksutilit on määritettävä ennen tämän tehtävän suorittamista.</span><span class="sxs-lookup"><span data-stu-id="52ce7-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="52ce7-106">Tämä menettelyn luomisessa käytettiin DEMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="52ce7-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="52ce7-107">Tämä on kolmas viidestä tehtävästä, joilla esitellään asiakasmaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="52ce7-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="52ce7-108">Siirry kohtaan Myyntireskontra > Maksujen asetukset > Maksutavat.</span><span class="sxs-lookup"><span data-stu-id="52ce7-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="52ce7-109">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="52ce7-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="52ce7-110">Voit esimerkiksi suodattaa Maksutapa-kenttää arvolla ELECTRONIC.</span><span class="sxs-lookup"><span data-stu-id="52ce7-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="52ce7-111">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="52ce7-111">Click Edit.</span></span>
4. <span data-ttu-id="52ce7-112">Syötä Maksutili-kenttään arvot DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="52ce7-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="52ce7-113">Laajenna Tiedostomuodot-osa.</span><span class="sxs-lookup"><span data-stu-id="52ce7-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="52ce7-114">Valitse Yleinen sähköinen raportointi -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="52ce7-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="52ce7-115">Syötä Vie muotokonfiguraatio -kenttään arvo tai valitse arvo.</span><span class="sxs-lookup"><span data-stu-id="52ce7-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="52ce7-116">Valitse luettelosta arvo ISO20022 Direct debit (DE).</span><span class="sxs-lookup"><span data-stu-id="52ce7-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="52ce7-117">Jos luettelo on tyhjä, tuotua ja aktiivista asiakkaan maksun viennin muotokonfiguraatiota ei ole.</span><span class="sxs-lookup"><span data-stu-id="52ce7-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="52ce7-118">Valitse Vaadi valtakirjaa -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="52ce7-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="52ce7-119">Valitse Vaadi valtakirjaa -parametri asiakkaan maksumuodoille, joissa vaaditaan valtakirjatiedot maksuviestissä, kuten SEPA-suoraveloitus.</span><span class="sxs-lookup"><span data-stu-id="52ce7-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="52ce7-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="52ce7-120">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]