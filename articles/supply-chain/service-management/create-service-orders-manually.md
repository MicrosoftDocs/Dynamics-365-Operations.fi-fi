---
title: Huoltotilausten luominen manuaalisesti
description: Voit luoda huoltotilauksia manuaalisesti huoltosopimuksen tai **Huoltotilaukset**-lomakkeen avulla.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72b600bc59119a6304fa043240a34051435f8691
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470950"
---
# <a name="create-service-orders-manually"></a><span data-ttu-id="d52a4-103">Huoltotilausten luominen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="d52a4-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d52a4-104">Voit luoda huoltotilauksia manuaalisesti huoltosopimuksen tai **Huoltotilaukset**-lomakkeen avulla.</span><span class="sxs-lookup"><span data-stu-id="d52a4-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="d52a4-105">Voit luoda huoltotilauksen myös projektista.</span><span class="sxs-lookup"><span data-stu-id="d52a4-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="d52a4-106">Voit luoda huoltotilauksia automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="d52a4-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="d52a4-107">Huoltotilauksen luominen manuaalisesti huoltosopimuksesta</span><span class="sxs-lookup"><span data-stu-id="d52a4-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="d52a4-108">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltosopimukset** \> **Huoltosopimukset**.</span><span class="sxs-lookup"><span data-stu-id="d52a4-108">Select **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="d52a4-109">Valitse huoltosopimus tai luo uusi huoltosopimus.</span><span class="sxs-lookup"><span data-stu-id="d52a4-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="d52a4-110">Valitse **Toimita**-välilehteä ja valitse sitten **Luo**-ryhmästä **Suunnitellut huoltotilaukset** avataksesi **Luo huoltotilaukset** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="d52a4-110">Select the **Deliver** tab and in the **Create** group select **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="d52a4-111">Huoltotilauksen luominen manuaalisesti Huoltotilaukset-lomakkeessa</span><span class="sxs-lookup"><span data-stu-id="d52a4-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="d52a4-112">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="d52a4-112">Select **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="d52a4-113">Valitse **Uusi** luodaksesi uuden palvelutilauksen.</span><span class="sxs-lookup"><span data-stu-id="d52a4-113">Select **New** to create a new service order.</span></span>

3.  <span data-ttu-id="d52a4-114">Luo huoltotilauksen huoltotilausrivit.</span><span class="sxs-lookup"><span data-stu-id="d52a4-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="d52a4-115">Jos <STRONG>Salli ilman huoltosopimusta</STRONG> -valintaruutu on valittuna <STRONG>Huoltohallintaparametrit</STRONG>-lomakkeessa, voit kirjata huoltotilausrivien tapahtumat liittämättä huoltotilausta huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="d52a4-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="d52a4-116">Jos valintaruutu ei ole valittuna, sinun on liitettävä manuaalisesti luotu huoltotilaus projektiin ennen huoltotilausrivien kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="d52a4-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="d52a4-117">Huoltotilauksen luominen projektista</span><span class="sxs-lookup"><span data-stu-id="d52a4-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="d52a4-118">Avaa **Projektinhallinta ja kirjanpito** \> **Yleinen** \> **Projektit** \> **Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="d52a4-118">Go to **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="d52a4-119">Valitse **Projektit**-lomakkeen **Toimintoruutu**-osiosta **Hallinta**-välilehti \> valitse **Huolto** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="d52a4-119">In the **Projects** form, on the **Action Pane**, select the **Manage** tab \> select **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="d52a4-120">Noudata aiempia ohjeita, jotka koskevat huoltotilauksen luomista manuaalisesti **Huoltotilaukset**-lomakkeen avulla.</span><span class="sxs-lookup"><span data-stu-id="d52a4-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="d52a4-121">**Projektitunnus**-kentässä näkyy projektin viite.</span><span class="sxs-lookup"><span data-stu-id="d52a4-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="d52a4-122">Jos <STRONG>Salli ilman huoltosopimusta</STRONG> -valintaruutu on valittuna <STRONG>Huoltohallintaparametrit</STRONG>-lomakkeessa, voit kirjata huoltotilausrivien tapahtumat liittämättä huoltotilausta huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="d52a4-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="d52a4-123">Jos valintaruutu ei ole valittuna, sinun on liitettävä manuaalisesti luotu huoltotilaus projektiin ennen huoltotilausrivien kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="d52a4-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="d52a4-124">Huoltotilauksen luominen myyntitilauslomakkeesta</span><span class="sxs-lookup"><span data-stu-id="d52a4-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="d52a4-125">Voit luoda huoltotilauksen **Myyntitilaukset**-lomakkeesta käyttämällä **Luo uusi huoltotilaus myyntitilauksen perusteella** -ohjattua toimintoa.</span><span class="sxs-lookup"><span data-stu-id="d52a4-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="d52a4-126">Avaa **Myynti ja markkinointi** \> **Yleinen** \> **Myyntitilaukset** \> **Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="d52a4-126">Go to **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="d52a4-127">Avaa asianmukainen myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="d52a4-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="d52a4-128">Valitse **Myyntitilaus**-välilehdestä **Huoltotilaus** käynnistääksesi ohjatun **Luo uusi huoltotilaus myyntitilauksen perusteella** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="d52a4-128">On the **Sales order** tab, select **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="d52a4-129">Valitse **Seuraava \>** ja noudata sitten seuraavia ohjeita **Valitse sopimus huoltotilaukselle** -sivulla:</span><span class="sxs-lookup"><span data-stu-id="d52a4-129">Select **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="d52a4-130">Valitse **Huoltosopimus**-kentässä huoltosopimus, johon uusi huoltotilaus liittyy.</span><span class="sxs-lookup"><span data-stu-id="d52a4-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="d52a4-131">Valinnainen: Liitä huoltotilaus tiettyyn projektiin käyttämällä **Projektin tunnus** -kenttää.</span><span class="sxs-lookup"><span data-stu-id="d52a4-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="d52a4-132">Valitse **Seuraava \>** ja noudata sitten seuraavia ohjeita **Luo huoltotilaus** -sivulla:</span><span class="sxs-lookup"><span data-stu-id="d52a4-132">Select **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="d52a4-133">Määritä huoltokutsun alkamispäivämäärä ja -aika **Ensisijainen huoltoaika** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="d52a4-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="d52a4-134">Valinnainen: Muokkaa **Kuvaus**-kentässä olevaa tekstiä.</span><span class="sxs-lookup"><span data-stu-id="d52a4-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="d52a4-135">Oletusarvon mukaan teksti on kuvaus edellisellä sivulla valitsemastasi huoltosopimuksesta.</span><span class="sxs-lookup"><span data-stu-id="d52a4-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="d52a4-136">Valitse **Vastuuhenkilö**-kentässä sen työntekijän tunnus, joka vastaa sopimuksesta. Valitse myös asiakkaan ensisijainen huoltoteknikko, jos se on tiedossasi.</span><span class="sxs-lookup"><span data-stu-id="d52a4-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="d52a4-137">Valitse **Yhteystunnus**-kentässä sitä asiakasyrityksen työntekijää edustava tunnus, johon tätä huoltotilausta koskevissa asioissa tulee ottaa yhteyttä.</span><span class="sxs-lookup"><span data-stu-id="d52a4-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="d52a4-138">Valitse **Seuraava \>** ja sitten **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="d52a4-138">Select **Next \>**, and then select **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="d52a4-139">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="d52a4-139">See also</span></span>

[<span data-ttu-id="d52a4-140">Huoltotilaukset</span><span class="sxs-lookup"><span data-stu-id="d52a4-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="d52a4-141">Huoltotilausten luominen automaattisesti</span><span class="sxs-lookup"><span data-stu-id="d52a4-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="d52a4-142">[Huoltotilausten luominen (luokkalomake)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="d52a4-142">[Create service orders (class form)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]