---
title: Määritä huoltotilausvaiheet
description: Määritä huoltotilausvaiheet.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30f6a6afa6ab91bed41bb19b8312dc7e25bd2478
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "366762"
---
# <a name="set-up-service-order-stages"></a><span data-ttu-id="8ad80-103">Määritä huoltotilausvaiheet</span><span class="sxs-lookup"><span data-stu-id="8ad80-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="8ad80-104">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltotilaukset** \> **Huollon vaiheet**.</span><span class="sxs-lookup"><span data-stu-id="8ad80-104">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="8ad80-105">Luo uusi tietue painamalla CTRL+N.</span><span class="sxs-lookup"><span data-stu-id="8ad80-105">Press CTRL+N to create a new record.</span></span>

3.  <span data-ttu-id="8ad80-106">Määritä **Huollon vaihe**- ja **Kuvaus**-kenttiin huollon vaiheen tunnus ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="8ad80-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="8ad80-107">Valitse vaiheen asianmukaiset parametrit.</span><span class="sxs-lookup"><span data-stu-id="8ad80-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="8ad80-108">Valitse nykyisen vaiheen päävaihe tai jätä **Ylärakenne**-kenttä tyhjäksi, jos vaihe on vaiheasetusten alkuvaihe.</span><span class="sxs-lookup"><span data-stu-id="8ad80-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8ad80-109">Kun olet tallentanut vaiheen, <STRONG>Ylärakenne</STRONG>-kenttää ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="8ad80-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="8ad80-110">Sen sijaan voit poistaa tietueen ja luoda sen uudelleen niin, että <STRONG>Ylärakenne</STRONG>-kentässä on eri valinta.</span><span class="sxs-lookup"><span data-stu-id="8ad80-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="8ad80-111">Lisäksi voit luoda vain yhden vaiheen, jonka <STRONG>Ylärakenne</STRONG>-kenttä on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="8ad80-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="8ad80-112">Toisin sanoen vain yksi alkuvaihe sallitaan.</span><span class="sxs-lookup"><span data-stu-id="8ad80-112">That is, only one initial stage is permitted.</span></span></P>


  


