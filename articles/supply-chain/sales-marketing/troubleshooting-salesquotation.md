---
title: Myyntitarjousten vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita myyntitarjousten käytössä voi esiintyä.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 67610a833be132399b2d47ae8c6b27119be9ce95
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427028"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="ad73f-103">Myyntitarjousten vianmääritys</span><span class="sxs-lookup"><span data-stu-id="ad73f-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="ad73f-104">Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita myyntitarjousten käytössä voi esiintyä.</span><span class="sxs-lookup"><span data-stu-id="ad73f-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="ad73f-105">En saa muutettua palvelunimikkeen myyntitarjouksen myyntimäärää.</span><span class="sxs-lookup"><span data-stu-id="ad73f-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ad73f-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="ad73f-106">Issue description</span></span>

<span data-ttu-id="ad73f-107">Jos yrität määrittää myyntimäärää (**SalesQty**) *Palvelu*-tyypin nimikkeelle myyntitarjouksen rivillä, saat viestin "Päivittäminen ei ole sallittua Määrä-kentän osalta".</span><span class="sxs-lookup"><span data-stu-id="ad73f-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ad73f-108">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ad73f-108">Issue resolution</span></span>

<span data-ttu-id="ad73f-109">Et voi määrittää myyntimäärää tuotteille, jotka ovat palvelunimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="ad73f-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="ad73f-110">Jos esimerkiksi tarjoat nimikkeen asentamisen palvelua, määrän tallentaminen ei ole järkevää, koska fyysistä nimikettä ei ole.</span><span class="sxs-lookup"><span data-stu-id="ad73f-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="ad73f-111">On vain palvelu.</span><span class="sxs-lookup"><span data-stu-id="ad73f-111">There is only a service.</span></span>

