---
title: Edistyneeseen varastonhallintaan päivittämisen ja siirtymisen vianmääritys
description: Tässä aiheessa käsitellään yleisten edistyneeseen varastonhallintaan päivittämisen ja siirtymisen ongelmien korjaamista.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: dc1c487a608c2e165f5f12aed344cb89fe8d41e1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993871"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="ebd83-103">Edistyneeseen varastonhallintaan päivittämisen ja siirtymisen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="ebd83-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebd83-104">Tässä aiheessa käsitellään yleisten edistyneeseen varastonhallintaan päivittämisen ja siirtymisen ongelmien korjaamista.</span><span class="sxs-lookup"><span data-stu-id="ebd83-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="ebd83-105">Seuraava virhesanoma avautuu: java.security.cert.certPathValidatorException: Sertifiointipolun luottamusankkuria ei löytynyt.</span><span class="sxs-lookup"><span data-stu-id="ebd83-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ebd83-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="ebd83-106">Issue description</span></span>

<span data-ttu-id="ebd83-107">Tämä virhesanoma avautuu varastointisovelluksessa, koska itse allekirjoitettuihin varmenteisiin ei tueta paikallisissa Android 8+ -ympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="ebd83-107">You receive this error message in the warehouse app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ebd83-108">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ebd83-108">Issue resolution</span></span>

<span data-ttu-id="ebd83-109">Käytä ulkoista (julkista) varmenteiden myöntäjää.</span><span class="sxs-lookup"><span data-stu-id="ebd83-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="ebd83-110">Tämän varastointisovelluksen ongelman korjaus on saatavana versiossa 1.9.0.0.</span><span class="sxs-lookup"><span data-stu-id="ebd83-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="ebd83-111">Lisätietoja tästä ongelmasta ja sen korjaamisesta on kohdassa [Varastosovelluksen yhteysongelmien vianmääritys](troubleshoot-warehouse-app-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ebd83-111">For more information about this issue and how to fix it, see [Troubleshoot warehouse app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="ebd83-112">Mikä on hyväksytty prosessi siirryttäessä perusvarastoinnista edistyneeseen varastointiin?</span><span class="sxs-lookup"><span data-stu-id="ebd83-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="ebd83-113">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="ebd83-113">Issue description</span></span>

<span data-ttu-id="ebd83-114">Tällä hetkellä käytössä on erilaisten varastojen hallinta ja perusvarastotoiminnot, ja haluat siirtyä edistyneeseen varastointiin, jossa hyödynnetään mobiililaitteita, aaltoja ja työtä.</span><span class="sxs-lookup"><span data-stu-id="ebd83-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="ebd83-115">Tätä siirtoa yritettäessä on kuitenkin ongelmia.</span><span class="sxs-lookup"><span data-stu-id="ebd83-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="ebd83-116">Tuotteita ei voi esimerkiksi muuttaa niin, että ne käyttävät varastodimensioita (toimipaikkaa, varastoa ja sijaintia), koska tuotteisiin kohdistuu tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="ebd83-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="ebd83-117">Tämän vuoksi on opittava hyväksytty prosessi siirryttäessä perusvarastoinnista edistyneeseen varastointiin.</span><span class="sxs-lookup"><span data-stu-id="ebd83-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ebd83-118">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ebd83-118">Issue resolution</span></span>

<span data-ttu-id="ebd83-119">Lisätietoja perusvarastoinnista edistyneeseen varastointiin siirtymisestä on seuraavissa blogikirjoituksissa ja asiakirjoissa:</span><span class="sxs-lookup"><span data-stu-id="ebd83-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="ebd83-120">Aiemmin luotujen nimikkeiden ja varastojen varastonhallintaprosessin ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="ebd83-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="ebd83-121">Microsoft Dynamics AX WMS:n siirto uuteen R3-varastointi- ja kuljetustoimintoon</span><span class="sxs-lookup"><span data-stu-id="ebd83-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="ebd83-122">WMSI-/WMS2-nimikkeen siirto</span><span class="sxs-lookup"><span data-stu-id="ebd83-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="ebd83-123">Varastonhallinnan päivittäminen Microsoft Dynamics AX 2012:sta Supply Chain Managementiin</span><span class="sxs-lookup"><span data-stu-id="ebd83-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)
