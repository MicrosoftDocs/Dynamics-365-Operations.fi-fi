---
title: Asiakasluottoryhmät
description: Tässä ohjeaiheessa on tietoja asiakasluottoryhmistä
author: mikefalkner
manager: AnnBe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1ddf41d88d085b102a7d69eeeff0ec463d8b4137
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442733"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="36c05-103">Asiakasluottoryhmät</span><span class="sxs-lookup"><span data-stu-id="36c05-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36c05-104">Voit määrittää asiakasryhmiä, joilla on jaettu luottoraja.</span><span class="sxs-lookup"><span data-stu-id="36c05-104">You can define groups of customers who have a shared credit limit.</span></span> <span data-ttu-id="36c05-105">Lisäksi otetaan huomioon myyntilaskutilille määritetty yksittäinen luottoraja.</span><span class="sxs-lookup"><span data-stu-id="36c05-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="36c05-106">Asiakasluottoryhmään voidaan valita jäseniä eri yrityksistä.</span><span class="sxs-lookup"><span data-stu-id="36c05-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="36c05-107">Kun lisäät asiakkaan asiakasluottoryhmän asiakasluetteloon, kunkin asiakkaan luottorajan vanhentumispäivä muutetaan ryhmälle määritetyksi vanhentumispäiväksi.</span><span class="sxs-lookup"><span data-stu-id="36c05-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="36c05-108">Voit määrittää asiakasluottoryhmiä **Asiakasluottoryhmät**-sivulla (**Luotonhallinta \> Asiakasluottoryhmät \> Asiakasluottoryhmät**).</span><span class="sxs-lookup"><span data-stu-id="36c05-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="36c05-109">Anna **Ryhmän numero**- ja **Kuvaus**-kenttiin ryhmän tunniste ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="36c05-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="36c05-110">Anna **Luottoraja**- ja **Valuutta**-kenttiin luottoraja ja valuutta, jotka käytetään, kun järjestelmä tarkistaa jonkin ryhmän jäsenen luottorajan.</span><span class="sxs-lookup"><span data-stu-id="36c05-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="36c05-111">Anna **Luottoraja päivämäärään** -kenttään päivämäärä, jolloin luottoraja vanhenee.</span><span class="sxs-lookup"><span data-stu-id="36c05-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="36c05-112">Asiakasluottoryhmillä on oltava vanhentumispäivä.</span><span class="sxs-lookup"><span data-stu-id="36c05-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="36c05-113">Kun asiakasluottoryhmä on määritetty, voit lisätä siihen asiakkaita määrittämällä niiden yrityksen ja asiakkaan tilitunnuksen.</span><span class="sxs-lookup"><span data-stu-id="36c05-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="36c05-114">Kun lisäät uuden asiakkaan asiakasluottoryhmään, järjestelmä hakee saman asiakkaan tiliä kaikista yrityksistä ja pyytää sinua lisäämään sen asiakasluottoryhmään.</span><span class="sxs-lookup"><span data-stu-id="36c05-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="36c05-115">Voit tarkastella **Erääntyneet saldot** -valikossa kaikkien asiakasluottoryhmän laskutusasiakkaiden erääntymissaldon tietoja.</span><span class="sxs-lookup"><span data-stu-id="36c05-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="36c05-116">**Erääntymissaldo**-sivulla on laskutusasiakastilien erääntyneiden saldojen yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="36c05-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>
