---
title: Myyntitarjousten vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita myyntitarjousten käytössä voi esiintyä.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 09529ba729170be7281e2ae04008d3ba4a58e060
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824747"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="270e8-103">Myyntitarjousten vianmääritys</span><span class="sxs-lookup"><span data-stu-id="270e8-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="270e8-104">Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita myyntitarjousten käytössä voi esiintyä.</span><span class="sxs-lookup"><span data-stu-id="270e8-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="270e8-105">En saa muutettua palvelunimikkeen myyntitarjouksen myyntimäärää.</span><span class="sxs-lookup"><span data-stu-id="270e8-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="270e8-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="270e8-106">Issue description</span></span>

<span data-ttu-id="270e8-107">Jos yrität määrittää myyntimäärää (**SalesQty**) *Palvelu*-tyypin nimikkeelle myyntitarjouksen rivillä, saat viestin "Päivittäminen ei ole sallittua Määrä-kentän osalta".</span><span class="sxs-lookup"><span data-stu-id="270e8-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="270e8-108">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="270e8-108">Issue resolution</span></span>

<span data-ttu-id="270e8-109">Et voi määrittää myyntimäärää tuotteille, jotka ovat palvelunimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="270e8-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="270e8-110">Jos esimerkiksi tarjoat nimikkeen asentamisen palvelua, määrän tallentaminen ei ole järkevää, koska fyysistä nimikettä ei ole.</span><span class="sxs-lookup"><span data-stu-id="270e8-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="270e8-111">On vain palvelu.</span><span class="sxs-lookup"><span data-stu-id="270e8-111">There is only a service.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]