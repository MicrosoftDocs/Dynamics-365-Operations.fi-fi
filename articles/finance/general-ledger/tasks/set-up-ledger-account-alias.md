---
title: Määritä kirjanpitotilin alias
description: Tässä menettelyssä käsitellään, miten luodaan tilin tilinumeron antamisen pikavalintana toimiva tilin alias.
author: aprilolson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAccountAlias
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf5a0f233971fd7b84bb85c43bb0c0d585f0945a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838786"
---
# <a name="set-up-a-ledger-account-alias"></a><span data-ttu-id="34f7d-103">Määritä kirjanpitotilin alias</span><span class="sxs-lookup"><span data-stu-id="34f7d-103">Set up a ledger account alias</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34f7d-104">Tässä menettelyssä käsitellään, miten luodaan tilin tilinumeron antamisen pikavalintana toimiva tilin alias.</span><span class="sxs-lookup"><span data-stu-id="34f7d-104">This procedure shows how to create an account alias that provides a shortcut for entering an account number.</span></span> <span data-ttu-id="34f7d-105">Menettely käyttää USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="34f7d-105">This procedure uses demo data company USMF.</span></span>

1. <span data-ttu-id="34f7d-106">Valitse Kirjanpito > Tilikartta > Tilit > Kirjanpitotilin alias.</span><span class="sxs-lookup"><span data-stu-id="34f7d-106">Go to General ledger > Chart of accounts > Accounts > Ledger account alias.</span></span>
2. <span data-ttu-id="34f7d-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="34f7d-107">Click New.</span></span>
3. <span data-ttu-id="34f7d-108">Kirjoita Kirjanpitotilin alias -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="34f7d-108">In the Ledger account alias field, type a value.</span></span>
4. <span data-ttu-id="34f7d-109">Valitse Tilirakenne-kentässä rakenne, johon tili ja dimensiot kuuluvat.</span><span class="sxs-lookup"><span data-stu-id="34f7d-109">In the Account structure field, select the structure the account and dimensions belong to.</span></span>
5. <span data-ttu-id="34f7d-110">Avaa haku napsauttamalla Yritys-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="34f7d-110">In the Company field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="34f7d-111">Etsi ja valitse luettelosta yritys, jota alias koskee.</span><span class="sxs-lookup"><span data-stu-id="34f7d-111">In the list, find and select the company that the alias applies to.</span></span>
7. <span data-ttu-id="34f7d-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="34f7d-112">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="34f7d-113">Määritä Kirjanpitotilin alias -kenttään tili ja dimensiot.</span><span class="sxs-lookup"><span data-stu-id="34f7d-113">In the Ledger account alias definition field, specify the account and dimensions.</span></span>
    * <span data-ttu-id="34f7d-114">Tilien ja dimensioiden tiedot täytetään pikavalintaa käytettäessä.</span><span class="sxs-lookup"><span data-stu-id="34f7d-114">The account and dimensions will be populated when using the shortcut.</span></span>  
9. <span data-ttu-id="34f7d-115">Valitse Alkuperäinen kohdistus -kentässä dimensio, joka on kohdistettuna aliasta käytettäessä.</span><span class="sxs-lookup"><span data-stu-id="34f7d-115">In the Initial focus field, select the dimension that will have focus when the alias is used.</span></span>
    * <span data-ttu-id="34f7d-116">Kun olet kirjoittanut pikavalinnan ja kun tilin ja dimensioiden tiedot on täytetty, alkuperäinen kohdistuskenttä on osoittimen kohdalla ja siirtyy siihen.</span><span class="sxs-lookup"><span data-stu-id="34f7d-116">After you type the shortcut, and the account and dimensions are populated, the Initial focus field is where the cursor or focus will move to.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]