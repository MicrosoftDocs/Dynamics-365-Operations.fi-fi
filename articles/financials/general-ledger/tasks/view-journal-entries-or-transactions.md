---
title: Kirjauskansiovientien tai tapahtumien näyttäminen
description: Näiden ohjeiden avulla voit käyttää tositetapahtumien kyselyä kirjauskansiovientien tai tapahtumien hakua varten.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, LedgerTransVoucher, LedgerTransBase, Originaldocuments
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c72ea9b7b706e1dbd8e4261534f098589535886
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916181"
---
# <a name="view-journal-entries-or-transactions"></a><span data-ttu-id="d6c64-103">Kirjauskansiovientien tai tapahtumien näyttäminen</span><span class="sxs-lookup"><span data-stu-id="d6c64-103">View journal entries or transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d6c64-104">Näiden ohjeiden avulla voit käyttää tositetapahtumien kyselyä kirjauskansiovientien tai tapahtumien hakua varten.</span><span class="sxs-lookup"><span data-stu-id="d6c64-104">This procedure shows how to use the Voucher transactions inquiry to search for journal entries or transactions.</span></span>

1. <span data-ttu-id="d6c64-105">Siirry kohtaan **siirtymisruutu > Moduulit > Kirjanpito > Kyselyt ja raportit > Tositetapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="d6c64-105">Go to **Navigation pane > Modules > General ledger > Inquiries and reports > Voucher transactions**.</span></span>
2. <span data-ttu-id="d6c64-106">Voit tehdä kenttä, jolle haluat määrittää suodatusehdon.</span><span class="sxs-lookup"><span data-stu-id="d6c64-106">Select the field for which you want to define a filter criteria.</span></span>
3. <span data-ttu-id="d6c64-107">Kirjoita valitun kentän suodatusehdot.</span><span class="sxs-lookup"><span data-stu-id="d6c64-107">Enter your filter critieria for the selected field.</span></span> <span data-ttu-id="d6c64-108">Voit suodattaa yksittäisellä arvolla tai alueella.</span><span class="sxs-lookup"><span data-stu-id="d6c64-108">You could filter on a single value or a range.</span></span> <span data-ttu-id="d6c64-109">Kun määrität alueen, varmista, että käytät oikeaa syntaksia.</span><span class="sxs-lookup"><span data-stu-id="d6c64-109">When defining a range, make sure the correct syntax is used.</span></span> <span data-ttu-id="d6c64-110">Arvot on erotettava toisistaan kahdella pisteellä (..).</span><span class="sxs-lookup"><span data-stu-id="d6c64-110">The values should be separated by a double period (..).</span></span>  
4. <span data-ttu-id="d6c64-111">Valitse **Liitokset**-välilehti ja lisää suodatettavia taulukoita.</span><span class="sxs-lookup"><span data-stu-id="d6c64-111">Click the **Joins** tab to add additional tables from which to filter.</span></span>
5. <span data-ttu-id="d6c64-112">Valitse puusta **Tables/General journal entry**.</span><span class="sxs-lookup"><span data-stu-id="d6c64-112">In the tree, select **Tables/General journal entry**.</span></span>
6. <span data-ttu-id="d6c64-113">Valitse **Lisää taulukon liitos**.</span><span class="sxs-lookup"><span data-stu-id="d6c64-113">Click **Add table join**.</span></span>
7. <span data-ttu-id="d6c64-114">Valitse **Peruuta**, jos et halua lisätä taulukkoa.</span><span class="sxs-lookup"><span data-stu-id="d6c64-114">Click **Cancel** if you decide not to add an additional table.</span></span>
8. <span data-ttu-id="d6c64-115">Valitse **Alue**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="d6c64-115">Click the **Range** tab.</span></span>
9. <span data-ttu-id="d6c64-116">Suorita kysely valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6c64-116">Click **OK** to run the query.</span></span>
10. <span data-ttu-id="d6c64-117">Valitse toimintoruudussa **Tapahtuman alkuperä**.</span><span class="sxs-lookup"><span data-stu-id="d6c64-117">On the Action pane, click **Transaction origin**.</span></span> <span data-ttu-id="d6c64-118">Ruudukon eri painikkeita voidaan käyttää valitun tositetietueen lisätietojen tarkasteluun.</span><span class="sxs-lookup"><span data-stu-id="d6c64-118">Various buttons about the grid can be used to research additional information about the selected record of the voucher.</span></span> <span data-ttu-id="d6c64-119">Jotkin painikkeet eivät ole käytettävissä tapahtumatyypistä ja tapahtuman ominaisuuksista riippuen.</span><span class="sxs-lookup"><span data-stu-id="d6c64-119">Some buttons may not be available, depending on the type of transaction and characteristics of the transaction.</span></span>
11. <span data-ttu-id="d6c64-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d6c64-120">Close the page.</span></span>
12. <span data-ttu-id="d6c64-121">Valitse toimintoruudussa **Alkuperäinen tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="d6c64-121">On the Action pane, Click **Original document**.</span></span>
13. <span data-ttu-id="d6c64-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d6c64-122">Close the page.</span></span>

