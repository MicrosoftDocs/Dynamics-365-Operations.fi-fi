---
title: Huollon mallit
description: Voit määrittää huoltosopimuksen mallina ja kopioida mallin rivit myöhemmin toiseen huoltosopimukseen tai huoltotilaukseen.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ade35eee21585aed2f542f4c977788aa3fe8804b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256132"
---
# <a name="service-templates"></a><span data-ttu-id="f6ca8-103">Huollon mallit</span><span class="sxs-lookup"><span data-stu-id="f6ca8-103">Service templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6ca8-104">Voit määrittää huoltosopimuksen mallina ja kopioida mallin rivit myöhemmin toiseen huoltosopimukseen tai huoltotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="f6ca8-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="f6ca8-105">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="f6ca8-105">Example</span></span>

<span data-ttu-id="f6ca8-106">Asiakas, joka hankkii teiltä huoltopalveluita, on identtiset huoltohissit viidessä eri paikassa.</span><span class="sxs-lookup"><span data-stu-id="f6ca8-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="f6ca8-107">Haluat määrittää tälle asiakkaalle viisi huoltosopimusta. Jokaiselle sijainnille tehdään oma sopimus.</span><span class="sxs-lookup"><span data-stu-id="f6ca8-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="f6ca8-108">Voit rajoittaa toistuvan työn määrää ja varmistaa, että huoltosopimusten määritystiedot ovat identtisiä, kun luot huoltosopimuksen ja määrität sen hissien huoltotyön malliksi.</span><span class="sxs-lookup"><span data-stu-id="f6ca8-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="f6ca8-109">Nyt voit kopioida mallin rivit viiteen uuteen huoltosopimukseen niin, että kukin huoltosopimus täytetään mallin riveillä.</span><span class="sxs-lookup"><span data-stu-id="f6ca8-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="f6ca8-110">Luo malli</span><span class="sxs-lookup"><span data-stu-id="f6ca8-110">Create a template</span></span>

<span data-ttu-id="f6ca8-111">Huoltomallin luonnin aikana luot ensin huoltosopimuksen ja sitten sille pakolliset rivit. Lopuksi liität huoltosopimuksen huoltomalliryhmään.</span><span class="sxs-lookup"><span data-stu-id="f6ca8-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="f6ca8-112">Huoltosopimus voidaan määrittää malliksi vain, jos siihen ei ole liitetty huoltotilauksia.</span><span class="sxs-lookup"><span data-stu-id="f6ca8-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="f6ca8-113">Huoltotilauksia ei myöskään voi luoda huoltosopimuksesta, joka on määritetty malliksi.</span><span class="sxs-lookup"><span data-stu-id="f6ca8-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="f6ca8-114">Kopioi mallirivit</span><span class="sxs-lookup"><span data-stu-id="f6ca8-114">Copy template lines</span></span>

<span data-ttu-id="f6ca8-115">Voit kopioida mallirivejä huoltomallista toiseen huoltosopimukseen tai huoltotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="f6ca8-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="f6ca8-116">Kun kopioit mallirivejä huoltotilauksiin tai huoltosopimuksiin, malliryhmät näytetään puunäkymässä, jossa kaikki ryhmät voidaan laajentaa.</span><span class="sxs-lookup"><span data-stu-id="f6ca8-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="f6ca8-117">Tässä näkymässä voit katsella kaikkia malleja ja mallipohjia.</span><span class="sxs-lookup"><span data-stu-id="f6ca8-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="f6ca8-118">Kopioitavien huoltomallin rivien määrittämistä helpottaa, jos olet ryhmitellyt mallit niiden käyttöä kuvaavilla nimillä.</span><span class="sxs-lookup"><span data-stu-id="f6ca8-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6ca8-119">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="f6ca8-119">Related topics</span></span>

[<span data-ttu-id="f6ca8-120">Huoltomallin rivien kopioiminen</span><span class="sxs-lookup"><span data-stu-id="f6ca8-120">Copy service templates lines</span></span>](copy-service-template-lines.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]