---
title: Maksutyypin pitää olla luottokortti -virhe myyntitilaussivulla
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun myyntitilaussivulla näkyy virhesanoma tilauksen synkronoinnin jälkeen.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 20f18507dee330fd1affedeee092b3dfa7cc10bc
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585304"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="6bc0c-103">Maksutyypin pitää olla luottokortti -virhe myyntitilaussivulla</span><span class="sxs-lookup"><span data-stu-id="6bc0c-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6bc0c-104">Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun myyntitilaussivulla näkyy virhesanoma tilauksen synkronoinnin jälkeen.</span><span class="sxs-lookup"><span data-stu-id="6bc0c-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="6bc0c-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="6bc0c-105">Description</span></span>

<span data-ttu-id="6bc0c-106">Kun avaat myyntitilaussivun tilauksen synkronoinnin jälkeen, näkyviin tulee seuraava virhesanoma: "Maksutyypin on oltava luottokortti, koska luottokortin numero on määritetty."</span><span class="sxs-lookup"><span data-stu-id="6bc0c-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![Maksutyypin on oltava luottokortti -virhe](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="6bc0c-108">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="6bc0c-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="6bc0c-109">Maksutyypin asetus Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="6bc0c-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="6bc0c-110">Siirry kohtaan **Myyntireskontra \> Maksujen asetukset \> Maksuehdot**.</span><span class="sxs-lookup"><span data-stu-id="6bc0c-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="6bc0c-111">Valitse maksuehdot vasemmanpuoleista siirtymispalkista.</span><span class="sxs-lookup"><span data-stu-id="6bc0c-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="6bc0c-112">Varmista **Maksutyyppi**-kentässä, että **Luottokortti** on valittu.</span><span class="sxs-lookup"><span data-stu-id="6bc0c-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6bc0c-113">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6bc0c-113">Additional resources</span></span>

[<span data-ttu-id="6bc0c-114">Online-myyntien ja -maksujen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="6bc0c-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)
