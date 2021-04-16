---
title: Varastonhallinnan varausten vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varastovarauksia käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828103"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="1ba4a-103">Varastonhallinnan varausten vianmääritys</span><span class="sxs-lookup"><span data-stu-id="1ba4a-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ba4a-104">Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varastovarauksia käytetään Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="1ba4a-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="1ba4a-105">Lisätietoja erä- ja sarjanumerorekisteröinnistä: [Varaston erä- ja sarjanumeroiden varaushierarkioiden vianmääritys](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="1ba4a-105">For topics that are related to batch and serial number registrations, see [Troubleshoot warehouse batch and serial reservation hierarchies](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="1ba4a-106">Seuraava virhesanoma avautuu: Varauksia ei voi poistaa, koska on luotu töitä, jotka ovat riippuvaisia niistä.</span><span class="sxs-lookup"><span data-stu-id="1ba4a-106">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="1ba4a-107">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="1ba4a-107">Issue description</span></span>

<span data-ttu-id="1ba4a-108">Myyntirivin varastoin varausta ei voi poistaa, koska rivillä on avoin työ.</span><span class="sxs-lookup"><span data-stu-id="1ba4a-108">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1ba4a-109">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="1ba4a-109">Issue resolution</span></span>

<span data-ttu-id="1ba4a-110">Selvitä, onko kyse avoimesta pakkausryhmän työstä ja siirrä nimike pakkausasemalta toiseen sijaintiin (kuten *lastausovelle*).</span><span class="sxs-lookup"><span data-stu-id="1ba4a-110">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="1ba4a-111">Selvitä **Työn luontihistorian loki**- ja **Työn tiedot** -sivuilta, mikä fyysisesti varaa varastoa, ja vapauta varaus sitten suorittamalla tai poistamalla työ.</span><span class="sxs-lookup"><span data-stu-id="1ba4a-111">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="1ba4a-112">Näytössä on seuraava virhesanoma: Varastomäärää -%1 ei voi päivittää, sillä varastotapahtumia on liian vähän nimikkeelle %2....</span><span class="sxs-lookup"><span data-stu-id="1ba4a-112">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="1ba4a-113">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="1ba4a-113">Issue description</span></span>

<span data-ttu-id="1ba4a-114">Tämä ongelma voi esiintyä, jos järjestelmä ei voi päivittää varastomäärää, koska varastotapahtumia, joilla on määritetyt dimensiot, ei ole tarpeeksi.</span><span class="sxs-lookup"><span data-stu-id="1ba4a-114">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="1ba4a-115">Virhesanoman koko teksti:</span><span class="sxs-lookup"><span data-stu-id="1ba4a-115">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="1ba4a-116">Varastomäärää -%1 ei voi päivittää, sillä varastotapahtumia on liian vähän nimikkeelle %2 dimensioilla Koko=%3, Väri=%4, Lisäykset=%5, Toimipaikka=%6, Varasto=%7, Varasto=%8, Varaston tila=Käytettävissä, Rekisterikilpi=%9, Eränumero=%10 viitetunnusta %11 varten erätunnuksessa %12.</span><span class="sxs-lookup"><span data-stu-id="1ba4a-116">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1ba4a-117">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="1ba4a-117">Issue resolution</span></span>

<span data-ttu-id="1ba4a-118">Varmista, että määrää ei ole varattu fyysisesti millään varastotapahtumalla.</span><span class="sxs-lookup"><span data-stu-id="1ba4a-118">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="1ba4a-119">Nämä tapahtumat voivat esimerkiksi avata laatutilauksia, varastoestotilauksia tai toimitustilauksia.</span><span class="sxs-lookup"><span data-stu-id="1ba4a-119">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="1ba4a-120">Seuraava virhesanoma avautuu: Fyysinen varastosaldo...ei voi varata, koska varastossa on vain 0,00 saatavana.</span><span class="sxs-lookup"><span data-stu-id="1ba4a-120">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="1ba4a-121">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="1ba4a-121">Issue description</span></span>

<span data-ttu-id="1ba4a-122">Tämä ongelma voi esiintyä, jos järjestelmä ei voi päivittää varastomäärää, koska varastotapahtumia, joilla on määritetyt dimensiot, ei ole tarpeeksi.</span><span class="sxs-lookup"><span data-stu-id="1ba4a-122">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="1ba4a-123">Virhesanoman koko teksti:</span><span class="sxs-lookup"><span data-stu-id="1ba4a-123">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="1ba4a-124">Fyysinen varastosaldo Toimipaikka=%1, Varasto=%2, Varaston tila=käytettävissä, Eränumero=%3, Omistaja=%4: %5 ei voi varata, koska varastossa on vain 0,00 saatavana.</span><span class="sxs-lookup"><span data-stu-id="1ba4a-124">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1ba4a-125">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="1ba4a-125">Issue resolution</span></span>

<span data-ttu-id="1ba4a-126">Tämä ongelman syy on todennäköisesti avoin työ.</span><span class="sxs-lookup"><span data-stu-id="1ba4a-126">This issue is probably caused by open work.</span></span> <span data-ttu-id="1ba4a-127">Voit joko suorittaa työn tai vastaanottaa ilman työn luontia.</span><span class="sxs-lookup"><span data-stu-id="1ba4a-127">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="1ba4a-128">Varmista, että määrää ei ole varattu fyysisesti millään varastotapahtumalla.</span><span class="sxs-lookup"><span data-stu-id="1ba4a-128">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="1ba4a-129">Nämä tapahtumat voivat esimerkiksi avata laatutilauksia, varastoestotilauksia tai toimitustilauksia.</span><span class="sxs-lookup"><span data-stu-id="1ba4a-129">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
