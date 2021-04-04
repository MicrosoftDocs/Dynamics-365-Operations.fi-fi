---
title: Huoltotilaukset
description: Huoltotilaus edustaa huoltoteknikon käyntiä asiakkaan toimipaikassa määritettynä päivänä.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26a1c693be9581bd26ad43c70a024b0a8115afdf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254236"
---
# <a name="service-orders"></a><span data-ttu-id="e1110-103">Huoltotilaukset</span><span class="sxs-lookup"><span data-stu-id="e1110-103">Service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e1110-104">Huoltotilaus edustaa huoltoteknikon käyntiä asiakkaan toimipaikassa määritettynä päivänä.</span><span class="sxs-lookup"><span data-stu-id="e1110-104">A service order represents a visit that a service technician makes to a customer site on a specific date.</span></span> <span data-ttu-id="e1110-105">Kukin huoltotilaus koostuu yhdestä tai useasta huoltotilausrivistä.</span><span class="sxs-lookup"><span data-stu-id="e1110-105">Each service order consists of one or more service order lines.</span></span> <span data-ttu-id="e1110-106">Huoltotilausrivit edustavat huoltoteknikon käyttämiä työtunteja sekä niihin liittyviä nimikkeitä, kuluja ja maksuja.</span><span class="sxs-lookup"><span data-stu-id="e1110-106">Service order lines represent the hours of work that must be performed by the service technician, and the related items, expenses, and fees.</span></span>

<span data-ttu-id="e1110-107">Voit liittää tehtäviä ja kohteita huoltotilausriviin.</span><span class="sxs-lookup"><span data-stu-id="e1110-107">You can attach tasks and objects to a service order line.</span></span> <span data-ttu-id="e1110-108">Voit sitten ryhmitellä huoltotilausrivit tehtävän tai kohteen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e1110-108">You can then group service order lines by task or by object.</span></span> <span data-ttu-id="e1110-109">Huoltotilausriviin voi myös liittää varastossa olevia nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="e1110-109">You can also attach items that are listed in inventory to service order lines.</span></span>

## <a name="create-service-orders"></a><span data-ttu-id="e1110-110">Huoltotilausten luominen</span><span class="sxs-lookup"><span data-stu-id="e1110-110">Create service orders</span></span>

<span data-ttu-id="e1110-111">Voit luoda huoltotilauksia huoltosopimuksen ja sen rivien perusteella.</span><span class="sxs-lookup"><span data-stu-id="e1110-111">You can create service orders based on a service agreement and the lines that are contained in that agreement.</span></span> <span data-ttu-id="e1110-112">Voit kuitenkin luoda huoltotilauksia, jotka liittyvät huoltosopimukseen, vain sillä kaudella, joka on määritetty sopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="e1110-112">However, you can create service orders that are associated with a service agreement only in the period that is specified in the agreement.</span></span> <span data-ttu-id="e1110-113">Esimerkiksi jos huoltosopimus on voimassa 2011 kalenterivuoden ajan, voit luoda huoltotilauksia sopimukselle 1.1.2011 – 31.12.2011.</span><span class="sxs-lookup"><span data-stu-id="e1110-113">For example, if a service agreement is valid for the 2011 calendar year, you can create service orders for the agreement from January 1, 2011, and December 31, 2011.</span></span>

<span data-ttu-id="e1110-114">Huoltotilauksia voi luoda myös erikseen liittämättä niitä huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="e1110-114">You can also create service orders individually, without associating them with an agreement.</span></span> <span data-ttu-id="e1110-115">Näitä huoltotilauksia voidaan käyttää ajoittamattomien tai kertaluontoisten huoltokäyntien käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="e1110-115">These service orders can be used to handle unscheduled or one-time service visits.</span></span> <span data-ttu-id="e1110-116">Jos asiakas esimerkiksi maaliskuussa päättää, että huoltosopimuksessa määritettyjen töiden lisäksi kaksi muuta laitetta on tarpeen huoltaa.</span><span class="sxs-lookup"><span data-stu-id="e1110-116">For example, in the month of March, your customer wants service to be performed on two machines, in addition to the machines that are specified in the service agreement.</span></span> <span data-ttu-id="e1110-117">Tätä tehtävää varten voit luoda huoltotilaukset liittämättä niitä sopimukseen.</span><span class="sxs-lookup"><span data-stu-id="e1110-117">For this task, you create service orders but do not associate them with an agreement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e1110-118">Luodaksesi huoltotilauksia, joita ei ole liitetty huoltosopimukseen, sinun on valittava <STRONG>Salli ilman huoltosopimusta</STRONG> -valintaruuti <STRONG>Huoltohallinnan parametrit</STRONG> -lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="e1110-118">To create service orders that are not associated with a service agreement, you must select the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form.</span></span></P>

<span data-ttu-id="e1110-119">**Skenaario**</span><span class="sxs-lookup"><span data-stu-id="e1110-119">**Scenario**</span></span>

<span data-ttu-id="e1110-120">Seuraavassa kuvataan toinen tilanne, jossa kannattaa luoda huoltotilaus, jota ei ole liitetty huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="e1110-120">The following scenario describes another situation where it is useful to create a service order that is not associated with a service agreement.</span></span>

<span data-ttu-id="e1110-121">Yrityksen lähettäjä saa puhelun, jossa kerrotaan hissin tarvitsevan välitöntä huoltoa.</span><span class="sxs-lookup"><span data-stu-id="e1110-121">The company dispatcher receives a call requesting emergency service on an elevator.</span></span> <span data-ttu-id="e1110-122">Huoltosopimuksen ja projektin laatimiseen ei ole aikaa.</span><span class="sxs-lookup"><span data-stu-id="e1110-122">There is no time to set up a service agreement and a project for the service.</span></span> <span data-ttu-id="e1110-123">Tällöin lähettäjä luo huoltotilauksen suoraan **Huoltotilaukset**-lomakkeessa, liittää huoltotilauksen olemassa olevaan projektiin ja luo huoltotilausrivit.</span><span class="sxs-lookup"><span data-stu-id="e1110-123">Therefore, the dispatcher creates a service order directly in the **Service orders** form, attaches the service order to an existing project, and creates the service order lines.</span></span> <span data-ttu-id="e1110-124">Lähettäjä luo myös tehtävän tai kohteen suhteen aiemmin luotuun huoltotilaukseen ja kirjaa näin työt, jotka eivät liity huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="e1110-124">The dispatcher also creates a task or object relation for an existing service order, to record work that is not related to the service agreement.</span></span> <span data-ttu-id="e1110-125">Lisätietoja on kohdissa [Huoltotilausten luominen manuaalisesti](create-service-orders-manually.md) ja [Huoltotehtävän suhteiden luominen](create-service-task-relations.md).</span><span class="sxs-lookup"><span data-stu-id="e1110-125">For more information, see [Create service orders manually](create-service-orders-manually.md) and [Create service task relations](create-service-task-relations.md).</span></span>

## <a name="monitor-the-progress-of-service-orders"></a><span data-ttu-id="e1110-126">Huoltotilauksen tilanteen seuraaminen</span><span class="sxs-lookup"><span data-stu-id="e1110-126">Monitor the progress of service orders</span></span>

<span data-ttu-id="e1110-127">Huoltotilauksille voi määrittää vaihejärjestelmän ja syykoodit, joilla voidaan seurata huoltotilausten etenemistä yrityksen eri työryhmissä ja työprosesseissa.</span><span class="sxs-lookup"><span data-stu-id="e1110-127">To monitor the progress of a sales order through the different teams and work processes, you can set up a system of stages and reason codes for service orders.</span></span> <span data-ttu-id="e1110-128">Voit määrittää kullekin vaiheelle sallitut toiminnot.</span><span class="sxs-lookup"><span data-stu-id="e1110-128">For each stage, you can specify the actions that are allowed.</span></span> <span data-ttu-id="e1110-129">Lisätietoja on kohdassa [Syykoodien luominen](create-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e1110-129">For more information, see [Create reason codes](create-reason-codes.md).</span></span>

<span data-ttu-id="e1110-130">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="e1110-130">**Example**</span></span>

<span data-ttu-id="e1110-131">Lähettäjä hyväksyy huoltotilauksen.</span><span class="sxs-lookup"><span data-stu-id="e1110-131">A service order is approved by the dispatcher.</span></span> <span data-ttu-id="e1110-132">Lähettäjä päivittää huoltotilauksen vaiheen ja määrittää syykoodin, joka ilmaisee, että huoltotilaus on vapautettu huoltoteknikolle.</span><span class="sxs-lookup"><span data-stu-id="e1110-132">The dispatcher updates the stage of the service order and specifies a reason code that indicates that the service order has been released to the service technician.</span></span> <span data-ttu-id="e1110-133">Teknikko siirtyy asiakkaan toimipisteeseen ja suorittaa huollon.</span><span class="sxs-lookup"><span data-stu-id="e1110-133">The technician goes to the customer site and performs the service.</span></span>

## <a name="specify-item-requirements-for-service-orders"></a><span data-ttu-id="e1110-134">Nimiketarpeiden määrittäminen huoltotilauksiin</span><span class="sxs-lookup"><span data-stu-id="e1110-134">Specify item requirements for service orders</span></span>

<span data-ttu-id="e1110-135">Voit määrittää varastonimikkeet, joita tarvitaan huoltotilauksissa.</span><span class="sxs-lookup"><span data-stu-id="e1110-135">You can specify the inventory items that are required for service orders.</span></span> <span data-ttu-id="e1110-136">Huoltotilaus on kuitenkin liitettävä projektiin.</span><span class="sxs-lookup"><span data-stu-id="e1110-136">However, the service order must be associated with a project.</span></span> <span data-ttu-id="e1110-137">Palvelutilausten nimikevaatimukset käsitellään projektin kautta.</span><span class="sxs-lookup"><span data-stu-id="e1110-137">Item requirements for service orders are processed through a project.</span></span> 

<span data-ttu-id="e1110-138">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="e1110-138">**Example**</span></span>

<span data-ttu-id="e1110-139">Lähettäjä käsittelee huoltosopimuksesta luodut huoltotilaukset.</span><span class="sxs-lookup"><span data-stu-id="e1110-139">The service orders that are created from the service agreement are processed by the dispatcher.</span></span> <span data-ttu-id="e1110-140">Ensimmäisestä huoltotilauksesta lähettäjä havaitsee, että huoltoteknikko tarvitsee tärkeän varaosan, jota ei ole käytettävissä olevassa varastossa.</span><span class="sxs-lookup"><span data-stu-id="e1110-140">For the first service order, the dispatcher realizes that the service technician requires an important spare part that is not in the on-hand inventory.</span></span> <span data-ttu-id="e1110-141">Tällöin lähettäjä luo varaosan nimiketarpeen suoraan huoltotilauksesta.</span><span class="sxs-lookup"><span data-stu-id="e1110-141">Therefore, the dispatcher creates an item requirement for the spare part directly from the service order.</span></span>

## <a name="move-and-post-lines"></a><span data-ttu-id="e1110-142">Rivien siirtäminen ja kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="e1110-142">Move and post lines</span></span>

<span data-ttu-id="e1110-143">Huoltoteknikko palaa huoltokäynniltä ja päivittää muutokset huoltotilausriveihin.</span><span class="sxs-lookup"><span data-stu-id="e1110-143">A service technician returns from a service visit, and then modifies and updates the service order lines.</span></span> <span data-ttu-id="e1110-144">Huoltokäynnillään teknikko suoritti huoltotyön, joka oli ajoitettu suoritettavaksi seuraavalla huoltokäynnillä.</span><span class="sxs-lookup"><span data-stu-id="e1110-144">During the service visit, the technician performed a service job that was scheduled for the next service visit.</span></span> <span data-ttu-id="e1110-145">Siksi teknikko siirtää rivejä seuraavasta huoltokäynnistä nykyiseen huoltokäyntiin.</span><span class="sxs-lookup"><span data-stu-id="e1110-145">Therefore, the technician moves the lines from the next service visit to the current service visit.</span></span> <span data-ttu-id="e1110-146">Tämän jälkeen teknikko kirjaa huoltotilauksen.</span><span class="sxs-lookup"><span data-stu-id="e1110-146">The technician then posts the service order.</span></span> <span data-ttu-id="e1110-147">Lisätietoja on kohdassa [Huoltotilausrivien siirtäminen](move-service-order-lines.md).</span><span class="sxs-lookup"><span data-stu-id="e1110-147">For more information, see [Move service order lines](move-service-order-lines.md).</span></span>

## <a name="cancel-service-orders"></a><span data-ttu-id="e1110-148">Peruuta huoltotilaukset</span><span class="sxs-lookup"><span data-stu-id="e1110-148">Cancel service orders</span></span>

<span data-ttu-id="e1110-149">Yksi tammikuussa luoduista huoltotilauksista on tarpeeton, sillä työ on peruutettu.</span><span class="sxs-lookup"><span data-stu-id="e1110-149">One of the other service orders that was generated for the month of January becomes obsolete, because the job is canceled.</span></span> <span data-ttu-id="e1110-150">Siksi huollon lähettäjä peruuttaa huoltotilauksen.</span><span class="sxs-lookup"><span data-stu-id="e1110-150">Therefore, the service dispatcher cancels the service order.</span></span> <span data-ttu-id="e1110-151">Lisätietoja on kohdassa [Huoltotilausten peruuttaminen](cancel-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="e1110-151">For more information, see [Cancel service orders](cancel-service-orders.md).</span></span>

## <a name="post-from-projects"></a><span data-ttu-id="e1110-152">Kirjaaminen projekteista</span><span class="sxs-lookup"><span data-stu-id="e1110-152">Post from projects</span></span>

<span data-ttu-id="e1110-153">Lähettäjä haluaa kirjata kaikki tiettyyn projektiin liittyvät huoltotilaukset kunkin viikon lopussa.</span><span class="sxs-lookup"><span data-stu-id="e1110-153">At the end of each week, the dispatcher wants to post all service orders that are attached to a specific project.</span></span> <span data-ttu-id="e1110-154">Siksi lähettäjä etsii projektin **Projektit**-lomakkeesta ja kirjaa huoltotilaukset, jotka on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="e1110-154">Therefore, the dispatcher locates the relevant project in the **Projects** form and posts the service orders that have been completed.</span></span> <span data-ttu-id="e1110-155">Lisätietoja on kohdassa [Huoltotilausten kirjaaminen (luokkalomake)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="e1110-155">For more information, see [Post service orders (class form)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).</span></span>

## <a name="delete-service-orders"></a><span data-ttu-id="e1110-156">Poista huoltotilaukset</span><span class="sxs-lookup"><span data-stu-id="e1110-156">Delete service orders</span></span>

<span data-ttu-id="e1110-157">Vuoden toisen puolikkaan aikana asiakas päättää, että huoltokäyntejä on liian harvoin.</span><span class="sxs-lookup"><span data-stu-id="e1110-157">During the second half of the year, your customer decides that the service visits are too infrequent.</span></span> <span data-ttu-id="e1110-158">Huoltosopimuksen jäljellä olevalle ajalle on luotava uusi huoltokäyntien sarja, jossa käyntejä on useammin.</span><span class="sxs-lookup"><span data-stu-id="e1110-158">You must create a new, more frequent series of service visits for the remaining time on the service agreement.</span></span> <span data-ttu-id="e1110-159">Tällöin jäljellä olevat huoltotilaukset on poistettava ja niiden tilalle on luotava uudet huoltotilaukset.</span><span class="sxs-lookup"><span data-stu-id="e1110-159">Therefore, you must delete the existing service orders and create new service orders.</span></span> <span data-ttu-id="e1110-160">Lisätietoja on kohdassa [Huoltotilausten poistaminen](delete-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="e1110-160">For more information, see [Delete service orders](delete-service-orders.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e1110-161">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="e1110-161">See also</span></span>

<span data-ttu-id="e1110-162">[Palvelutilaukset (lomake)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="e1110-162">[Service orders (form)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]