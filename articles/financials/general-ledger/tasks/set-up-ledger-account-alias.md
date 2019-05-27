---
title: Määritä kirjanpitotilin alias
description: Tässä menettelyssä käsitellään, miten luodaan tilin tilinumeron antamisen pikavalintana toimiva tilin alias.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccountAlias
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ae075d7678ab15157a500c6ee5bd77e8211254a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562831"
---
# <a name="set-up-a-ledger-account-alias"></a><span data-ttu-id="9d734-103">Määritä kirjanpitotilin alias</span><span class="sxs-lookup"><span data-stu-id="9d734-103">Set up a ledger account alias</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9d734-104">Tässä menettelyssä käsitellään, miten luodaan tilin tilinumeron antamisen pikavalintana toimiva tilin alias.</span><span class="sxs-lookup"><span data-stu-id="9d734-104">This procedure shows how to create an account alias that provides a shortcut for entering an account number.</span></span> <span data-ttu-id="9d734-105">Menettely käyttää USMF-demotietoyritystä.</span><span class="sxs-lookup"><span data-stu-id="9d734-105">This procedure users demo data company USMF.</span></span>

1. <span data-ttu-id="9d734-106">Valitse Kirjanpito > Tilikartta > Tilit > Kirjanpitotilin alias.</span><span class="sxs-lookup"><span data-stu-id="9d734-106">Go to General ledger > Chart of accounts > Accounts > Ledger account alias.</span></span>
2. <span data-ttu-id="9d734-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d734-107">Click New.</span></span>
3. <span data-ttu-id="9d734-108">Kirjoita Kirjanpitotilin alias -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="9d734-108">In the Ledger account alias field, type a value.</span></span>
4. <span data-ttu-id="9d734-109">Valitse Tilirakenne-kentässä rakenne, johon tili ja dimensiot kuuluvat.</span><span class="sxs-lookup"><span data-stu-id="9d734-109">In the Account structure field, select the structure the account and dimensions belong to.</span></span>
5. <span data-ttu-id="9d734-110">Avaa haku napsauttamalla Yritys-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="9d734-110">In the Company field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9d734-111">Etsi ja valitse luettelosta yritys, jota alias koskee.</span><span class="sxs-lookup"><span data-stu-id="9d734-111">In the list, find and select the company that the alias applies to.</span></span>
7. <span data-ttu-id="9d734-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="9d734-112">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9d734-113">Määritä Kirjanpitotilin alias -kenttään tili ja dimensiot.</span><span class="sxs-lookup"><span data-stu-id="9d734-113">In the Ledger account alias definition field, specify the account and dimensions.</span></span>
    * <span data-ttu-id="9d734-114">Tilien ja dimensioiden tiedot täytetään pikavalintaa käytettäessä.</span><span class="sxs-lookup"><span data-stu-id="9d734-114">The account and dimensions will be populated when using the shortcut.</span></span>  
9. <span data-ttu-id="9d734-115">Valitse Alkuperäinen kohdistus -kentässä dimensio, joka on kohdistettuna aliasta käytettäessä.</span><span class="sxs-lookup"><span data-stu-id="9d734-115">In the Initial focus field, select the dimension that will have focus when the alias is used.</span></span>
    * <span data-ttu-id="9d734-116">Kun olet kirjoittanut pikavalinnan ja kun tilin ja dimensioiden tiedot on täytetty, alkuperäinen kohdistuskenttä on osoittimen kohdalla ja siirtyy siihen.</span><span class="sxs-lookup"><span data-stu-id="9d734-116">After you type the shortcut, and the account and dimensions are populated, the Initial focus field is where the cursor or focus will move to.</span></span>  

