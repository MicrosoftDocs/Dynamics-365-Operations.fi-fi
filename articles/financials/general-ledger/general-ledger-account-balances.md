---
title: Kirjanpitotilin saldot
description: 'Tässä artikkelissa esitellään kirjanpitotilien saldojen kaksi erilaista tarkastelutapaa: Pääkirja-luettelosivu ja talousraportit. Artikkelissa kerrotaan myös, miten dimensioyhdistelmän saldot päivitetään.'
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13191
ms.assetid: ea3650ac-34a0-4516-b75b-801c2164107d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee35db478663f3a5ab114ec133115eccc40b143c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839156"
---
# <a name="general-ledger-account-balances"></a><span data-ttu-id="6a58c-104">Kirjanpitotilin saldot</span><span class="sxs-lookup"><span data-stu-id="6a58c-104">General ledger account balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a58c-105">Tässä artikkelissa esitellään kirjanpitotilien saldojen kaksi erilaista tarkastelutapaa: Pääkirja-luettelosivu ja talousraportit.</span><span class="sxs-lookup"><span data-stu-id="6a58c-105">This article explains two ways to view general ledger account balances -  the Trial balance list page and financial reports.</span></span> <span data-ttu-id="6a58c-106">Artikkelissa kerrotaan myös, miten dimensioyhdistelmän saldot päivitetään.</span><span class="sxs-lookup"><span data-stu-id="6a58c-106">It also discusses how to update dimension set balances.</span></span>

<span data-ttu-id="6a58c-107">Käyttäjät voivat tarkastella saldoja kirjanpidossa monin eri tavoin.</span><span class="sxs-lookup"><span data-stu-id="6a58c-107">There are a variety of ways users can view balances in the general ledger.</span></span> <span data-ttu-id="6a58c-108">Yleisimpiä vaihtoehtoja ovat:</span><span class="sxs-lookup"><span data-stu-id="6a58c-108">Some of the most common options are:</span></span>

-   <span data-ttu-id="6a58c-109">Pääkirja</span><span class="sxs-lookup"><span data-stu-id="6a58c-109">Trial balance</span></span>
-   <span data-ttu-id="6a58c-110">Talousraportit</span><span class="sxs-lookup"><span data-stu-id="6a58c-110">Financial reports</span></span>
-   <span data-ttu-id="6a58c-111">Tositetapahtumat</span><span class="sxs-lookup"><span data-stu-id="6a58c-111">Voucher transactions</span></span>
-   <span data-ttu-id="6a58c-112">Kirjanpitoraportit</span><span class="sxs-lookup"><span data-stu-id="6a58c-112">Ledger reports</span></span>

<span data-ttu-id="6a58c-113">Yleisinpiä tapoja ovat pääkirjan luettelosivu ja tilinpäätökset.</span><span class="sxs-lookup"><span data-stu-id="6a58c-113">The most common ways are the trial balance list page and financial reports.</span></span>

## <a name="trial-balance"></a><span data-ttu-id="6a58c-114">Pääkirja</span><span class="sxs-lookup"><span data-stu-id="6a58c-114">Trial balance</span></span>
<span data-ttu-id="6a58c-115">Pääkirja on luettelosivu, jossa näkyvät kaikki tilin ja/tai dimensioiden saldot tietyn ajanjakson aikana.</span><span class="sxs-lookup"><span data-stu-id="6a58c-115">The trial balance is a list page that shows all of the balances of an account and/or dimensions for a given period of time.</span></span> <span data-ttu-id="6a58c-116">Kun pääkirja avataan saldot päivitetään päivämäärille ja ominaisuuksille, jotka on määritetty parametreissa.</span><span class="sxs-lookup"><span data-stu-id="6a58c-116">When the trial balance is first opened it refreshes with the balances for the dates and properties that are set in the Parameters.</span></span> <span data-ttu-id="6a58c-117">Ominaisuudet, joita voidaan muuttaa parametreissa ovat päivämäärät, kirjanpitotasot, kuinka alkusaldojen halutaan näyttävän ja mitä sulkemisen tapahtumatyyppejä näytetään.</span><span class="sxs-lookup"><span data-stu-id="6a58c-117">Properties that can be changed in Parameters are the dates, posting layer, how they want opening balances to appear, and what closing transaction types to show.</span></span> 

<span data-ttu-id="6a58c-118">Kun käyttäjä muuttaa parametrejä, saldot päivitetään.</span><span class="sxs-lookup"><span data-stu-id="6a58c-118">When a user changes the parameters the balances are refreshed.</span></span> <span data-ttu-id="6a58c-119">Käyttäjän voivat myös valita, minkä dimensioyhdistelmän saldoja he haluavat tarkastella ja näytetäänkö jokainen dimensio eri sarakkeissa.</span><span class="sxs-lookup"><span data-stu-id="6a58c-119">The user can also pick what dimension set they want to view balances for and whether each of the dimensions show in separate columns.</span></span> 

<span data-ttu-id="6a58c-120">Käyttäjät voivat mennä saldoja alaspäin tarkastelemaan tapahtumia, joista saldo muodostuu.</span><span class="sxs-lookup"><span data-stu-id="6a58c-120">Users can drill down on the balances to view the transactions that make up the balance.</span></span>    

<span data-ttu-id="6a58c-121">Lisätietoja on kohdassa [Näytä talousraportit](view-financial-reports.md).</span><span class="sxs-lookup"><span data-stu-id="6a58c-121">For more information, see [View financial reports](view-financial-reports.md).</span></span>



