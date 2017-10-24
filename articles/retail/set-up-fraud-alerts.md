---
title: "Määritä petoshälytyksiä"
description: "Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää säännöt, jotka hälyttävät asiakaspalvelun edustajalle, kun tilausten käsittelyn aikana havaitaan mahdollisia vilpillisiä tietoja. Voit määrittää erityisiä koodeja, joilla automaattisesti tai manuaalisesti asetetaan epäilyttävät tilaukset pitoon."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-fraud-alerts"></a><span data-ttu-id="a9f0a-104">Määritä petoshälytyksiä</span><span class="sxs-lookup"><span data-stu-id="a9f0a-104">Set up fraud alerts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a9f0a-105">Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää säännöt, jotka hälyttävät asiakaspalvelun edustajalle, kun tilausten käsittelyn aikana havaitaan mahdollisia vilpillisiä tietoja.</span><span class="sxs-lookup"><span data-stu-id="a9f0a-105">This topic explains how to set up rules to alert customer service representatives of potentially fraudulent information when orders are processed.</span></span> <span data-ttu-id="a9f0a-106">Voit määrittää erityisiä koodeja, joilla automaattisesti tai manuaalisesti asetetaan epäilyttävät tilaukset pitoon.</span><span class="sxs-lookup"><span data-stu-id="a9f0a-106">You can define specific codes to use to automatically or manually put suspicious orders on hold.</span></span> 

<span data-ttu-id="a9f0a-107">Ennen kuin määrität ja käytät petosten tarkistussääntöjä, salli petosten tarkistaminen ja määritä petostarkistusten perusarvot puhelinkeskusparametreissa.</span><span class="sxs-lookup"><span data-stu-id="a9f0a-107">Before you set up and use fraud checking rules, you must enable fraud checking and define the basic fraud checking values in the call center parameters.</span></span> <span data-ttu-id="a9f0a-108">Petossääntöjä on kahdenlaisia:</span><span class="sxs-lookup"><span data-stu-id="a9f0a-108">There are two types of fraud rules:</span></span>

-   <span data-ttu-id="a9f0a-109">**Staattiset säännöt** käyttää tiettyä arvoa, kuten mustalle listalle asetettua puhelinnumeroa.</span><span class="sxs-lookup"><span data-stu-id="a9f0a-109">**Static rules** use a specific value, such as a phone number that has been blacklisted.</span></span>
-   <span data-ttu-id="a9f0a-110">**Dynaamiset säännöt** voivat koostua muuttujista ja ehdoista.</span><span class="sxs-lookup"><span data-stu-id="a9f0a-110">**Dynamic rules** can be composed from variables and conditions.</span></span>

<span data-ttu-id="a9f0a-111">Ennen kuin luot dynaamisen säännön, sinun on luotava muuttujat ja ehdot, jotka määrittävät, ketä sääntö koskee ja milloin sääntöä käytetään.</span><span class="sxs-lookup"><span data-stu-id="a9f0a-111">Before you create a dynamic rule, you must create the variables and conditions that define who the rule applies to and when the rule should be applied.</span></span> <span data-ttu-id="a9f0a-112">Voit esimerkiksi luoda säännön, joka edellyttää, että kun asiakas 1202 tekee vähintään 1 000,00 arvoisen tilauksen, myyntitilaus tulee asettaa pitoon, kunnes asiakkaan maksu voidaan varmistaa.</span><span class="sxs-lookup"><span data-stu-id="a9f0a-112">For example, you want to create a rule to require that any sales order that customer 1202 places that is worth 1,000.00 or more be put on hold until the customer payment can be verified.</span></span> <span data-ttu-id="a9f0a-113">Tässä tapauksessa muuttujat ovat asiakas 1202 ja tilauksen kokonaissumma 1 000,00.</span><span class="sxs-lookup"><span data-stu-id="a9f0a-113">In this case, the variables are customer 1202 and an order total of 1,000.00.</span></span> <span data-ttu-id="a9f0a-114">Ehto määrittää, että jos asiakas 1202 suorittaa tilauksen ja tilauksen kokonaissumma on yhtä suuri tai enemmän kuin 1 000,00, myyntitilaus on asetettava pitoon, kunnes asiakkaan maksu voidaan vahvistaa.</span><span class="sxs-lookup"><span data-stu-id="a9f0a-114">The condition specifies that if customer 1202 places an order, and the total amount of the order is equal to or more than 1,000.00, the sales order must be put on hold until the customer payment can be verified.</span></span>




