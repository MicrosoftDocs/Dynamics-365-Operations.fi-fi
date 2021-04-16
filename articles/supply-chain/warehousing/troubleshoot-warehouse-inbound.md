---
title: Saapuvien varastotoimintojen vianmääritys
description: Tässä aiheessa käsitellään sellaisten yleisten ongelmien korjaamista, joita voi esiintyä, kun saapuvia varastotoimintoja käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
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
ms.openlocfilehash: f0ea2ee208cdbb8f9fa6668bbcb6e15252a7c1b1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828223"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="f835b-103">Saapuvien varastotoimintojen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="f835b-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f835b-104">Tässä aiheessa käsitellään sellaisten yleisten ongelmien korjaamista, joita voi esiintyä, kun saapuvia varastotoimintoja käytetään Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="f835b-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="f835b-105">Seuraava virhesanoma avautui: Laatutilaus %1 on luotu.</span><span class="sxs-lookup"><span data-stu-id="f835b-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="f835b-106">Klusteriprofiilia ei löytynyt. Tarkista konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="f835b-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f835b-107">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="f835b-107">Issue description</span></span>

<span data-ttu-id="f835b-108">Tämä virhesanoma liittyy vastaanottoprosessiin, jossa laadunhallinta on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="f835b-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="f835b-109">Ympäristön määritysten mukaan virhesanoman luovan tapahtuman lisätiedot voivat auttaa korjaamaan ongelman.</span><span class="sxs-lookup"><span data-stu-id="f835b-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f835b-110">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f835b-110">Issue resolution</span></span>

<span data-ttu-id="f835b-111">Tarkista ensimmäiseksi [klusterikeräilyn](set-up-cluster-picking.md) määritys ja varmista, että klusteriprofiilit on määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="f835b-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="f835b-112">Et voi käyttää mobiililaitteen klusterikeräilyn valikkokohdetta, ellei klusteriprofiileja ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="f835b-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="f835b-113">Ympäristön mukaan on ehkä tarkistettava myös liittyvät määritykset.</span><span class="sxs-lookup"><span data-stu-id="f835b-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="f835b-114">Yhdistelmärekisterikilven vastaanottoa ei voi käyttää muussa kuin hyvityksen jakelukoodissa.</span><span class="sxs-lookup"><span data-stu-id="f835b-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f835b-115">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="f835b-115">Issue description</span></span>

<span data-ttu-id="f835b-116">Kun jakelukoodin **Toiminto**-kentän määrityksenä on *Hyvitys* tai *Hävikki*, voit käyttää [Yhdistelmärekisterikilven vastaanotto](mixed-license-plate-receiving.md) -valikkovaihtoehtoa palautettujen nimikkeiden käsittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="f835b-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f835b-117">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f835b-117">Issue resolution</span></span>

<span data-ttu-id="f835b-118">Microsoft on arvioinut ongelman ja määrittänyt, että se on ominaisuuden rajoitus.</span><span class="sxs-lookup"><span data-stu-id="f835b-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="f835b-119">Tällä hetkellä yhdistelmärekisterikilven vastaanotossa tuetaan vain [jakelukoodeja](../service-management/set-up-disposition-codes.md), joissa **Toiminto**-kentän asetuksena on *Hyvitys* tai *Hävikki*.</span><span class="sxs-lookup"><span data-stu-id="f835b-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="f835b-120">Kun kausittainen tuotteen vastaanottojen päivitystehtävä suoritetaan, vahvistamattomat ostotilaukset vahvistetaan.</span><span class="sxs-lookup"><span data-stu-id="f835b-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f835b-121">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="f835b-121">Issue description</span></span>

<span data-ttu-id="f835b-122">Kun olet suorittanut kausittaisen *Päivitä tuotteen vastaanotot* -tehtävän, järjestelmä vahvistaa automaattisesti vahvistamattomat ostotilaukset, joiden varastotapahtuman tila on *Rekisteröity*.</span><span class="sxs-lookup"><span data-stu-id="f835b-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f835b-123">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f835b-123">Issue resolution</span></span>

<span data-ttu-id="f835b-124">Uusi saapuvan kuorman käsittelyominaisuus *Kuormamäärien ylivastaanottaminen* korjaa tämän ongelman.</span><span class="sxs-lookup"><span data-stu-id="f835b-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="f835b-125">Ota tämä ominaisuus käyttöön siirtymällä [ominaisuuksien hallintaan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ottamalla seuraavat ominaisuudet käyttöön (alla olevassa järjestyksessä):</span><span class="sxs-lookup"><span data-stu-id="f835b-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="f835b-126">Liitä ostotilauksen varastotapahtumat kuorman kanssa</span><span class="sxs-lookup"><span data-stu-id="f835b-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="f835b-127">Kuormamääriä vastaanotettu liikaa</span><span class="sxs-lookup"><span data-stu-id="f835b-127">Over receipt of load quantities</span></span>

<span data-ttu-id="f835b-128">Lisätietoja on kohdassa [Kirjattujen tuotemäärien kirjaaminen ostotilauksiin](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="f835b-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a><span data-ttu-id="f835b-129">Kun rekisteröin saapuvia tilauksia, näyttöön tulee seuraava virhesanoma: Määrä ei kelpaa.</span><span class="sxs-lookup"><span data-stu-id="f835b-129">When I register inbound orders, I receive the following error message: "The quantity is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f835b-130">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="f835b-130">Issue description</span></span>

<span data-ttu-id="f835b-131">Jos saapuvien tilausten rekisteröimiseen käytettävässä mobiililaitteen valikkokohteessa on määritetty **rekisterikilpien ryhmittelykäytäntö** -kentän arvoksi *Käyttäjän määrittämä*, näkyviin tulee virhesanoma (Määrä ei kelpaa) etkä voi tehdä rekisteröintiä valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="f835b-131">If the **License plate grouping policy** field is set to *User defined* for a mobile device menu item that is used to register inbound orders, you receive an error message ("The quantity is not valid"), and you can't complete the registration.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="f835b-132">Ongelman syy</span><span class="sxs-lookup"><span data-stu-id="f835b-132">Issue cause</span></span>

<span data-ttu-id="f835b-133">Kun *Käyttäjän määrittämä* -arvoa käytetään rekisterikilpien ryhmittelykäytäntönä, järjestelmä jakaa saapuvan varaston erillisiksi rekisterikilviksi, kuten yksikköjärjestysryhmä määrittää.</span><span class="sxs-lookup"><span data-stu-id="f835b-133">When *User defined* is used as a license plate grouping policy, the system splits the incoming inventory into separate license plates, as indicated by the unit sequence group.</span></span> <span data-ttu-id="f835b-134">Jos vastaanotettavan nimikkeen jäljittämiseen käytetään erä- tai sarjanumeroita, kunkin erän tai sarja määrät on määritettävä rekisteröityä rekisterikilpeä kohden.</span><span class="sxs-lookup"><span data-stu-id="f835b-134">If batch or serial numbers are used to track the item that is being received, the quantities of each batch or serial must be specified per license plate that is registered.</span></span> <span data-ttu-id="f835b-135">Jos rekisterikilvelle määritetty määrä ylittää määrän, joka on vielä vastaanotettava nykyisille dimensioille, näyttöön tulee virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="f835b-135">If the quantity that is specified for a license plate exceeds the quantity that must still be received for the current dimensions, you receive the error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f835b-136">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f835b-136">Issue resolution</span></span>

<span data-ttu-id="f835b-137">Kun rekisteröit nimikkeen käyttämällä kannettavan laitteen valikkonimikettä, jossa **Rekisterikilpien ryhmittelykäytäntö** -kentän arvoksi on määritetty *Käyttäjän määrittämä*, järjestelmä saattaa edellyttää, että vahvistat tai määrität rekisterikilpinumerot, eränumerot tai sarjanumerot.</span><span class="sxs-lookup"><span data-stu-id="f835b-137">When you register an item by using a mobile device menu item where the **License plate grouping policy** field is set to *User defined*, the system might require that you confirm or enter license plate numbers, batch numbers, or serial numbers.</span></span>

<span data-ttu-id="f835b-138">Järjestelmä näyttää rekisterikilven vahvistussivulla määrän, joka on varattu nykyiselle rekisterikilvelle.</span><span class="sxs-lookup"><span data-stu-id="f835b-138">On the license plate confirmation page, the system will show the quantity that is allocated for the current license plate.</span></span> <span data-ttu-id="f835b-139">Järjestelmä näyttää erä- tai sarjavahvistussivuilla määrän, joka on edelleen vastaanotettava nykyiselle rekisterikilvelle.</span><span class="sxs-lookup"><span data-stu-id="f835b-139">On the batch or serial confirmation pages, the system will show the quantity that must still be received on the current license plate.</span></span> <span data-ttu-id="f835b-140">Siihen sisältyy myös kenttä, johon voit syöttää rekisteröitävän määrän tätä rekisterikilven ja erä- tai sarjanumeron yhdistelmää varten.</span><span class="sxs-lookup"><span data-stu-id="f835b-140">It will also include a field where you can enter the quantity to register for that combination of license plate and batch or serial number.</span></span> <span data-ttu-id="f835b-141">Varmista tässä tapauksessa, että rekisterikilvelle rekisteröitävä määrä ei ylitä vielä vastaanotettavaa määrää.</span><span class="sxs-lookup"><span data-stu-id="f835b-141">In this case, make sure that the quantity that is being registered for the license plate doesn't exceed the quantity that must still be received.</span></span>

<span data-ttu-id="f835b-142">Vaihtoehtoisesti, jos saapuvan tilauksen rekisteröinnissä luodaan liian monta rekisterikilpeä, **Rekisterikilpien ryhmittelykäytäntö** -kentän arvoksi voidaan muuttaa *Rekisterikilpien ryhmittely*, nimikkeelle voi määrittää uuden yksikköjärjestysryhmän tai yksikköjärjestysryhmän **Rekisterikilpien ryhmittely** -vaihtoehdon aktivointi voidaan poistaa käytöstä.</span><span class="sxs-lookup"><span data-stu-id="f835b-142">Alternatively, if too many license plates are being generated on inbound order registration, the value of the **License plate grouping policy** field can be changed to *License plate grouping*, a new unit sequence group can be assigned to the item, or the **License plate grouping** option for the unit sequence group can be inactivated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
