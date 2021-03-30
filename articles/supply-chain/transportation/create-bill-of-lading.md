---
title: Rahtikirjan luonti
description: Tässä aiheessa kuvataan, miten luot rahtikirjoja, kun käytät varastonhallintaprosesseja.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31e6ce3fd65263d6df248322ca149afa5f750cb7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206892"
---
# <a name="create-a-bill-of-lading"></a><span data-ttu-id="74f8f-103">Rahtikirjan luonti</span><span class="sxs-lookup"><span data-stu-id="74f8f-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74f8f-104">Tässä aiheessa kuvataan, miten luot rahtikirjoja, kun käytät varastonhallintaprosesseja.</span><span class="sxs-lookup"><span data-stu-id="74f8f-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="74f8f-105">Rahtikirja on lakisääteinen tosite nimikkeiden lähettäjän ja kuljettajan välillä.</span><span class="sxs-lookup"><span data-stu-id="74f8f-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="74f8f-106">Asiakirja liitetään toimitettuihin nimikkeisiin ja se toimii lähetyksen vastaanottokuittina, kun nimikkeet toimitetaan kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="74f8f-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="74f8f-107">Jos käytät varastonhallintaa, rahtikirjoja voi luoda kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="74f8f-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="74f8f-108">Luo raportti manuaalisesti käyttämällä **Rahtikirja**-sivua.</span><span class="sxs-lookup"><span data-stu-id="74f8f-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="74f8f-109">Luo raportti **Kuormasuunnittelun työtilassa**.</span><span class="sxs-lookup"><span data-stu-id="74f8f-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="74f8f-110">Jos luot rahtikirjan **Kuormasuunnittelun työtilassa**, kuorman tilan on oltava **Toimitettu**.</span><span class="sxs-lookup"><span data-stu-id="74f8f-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="74f8f-111">Jos kuormassa on useampi kuin yksi toimitus, rahtikirjan luodaan jokaista toimitusta varten.</span><span class="sxs-lookup"><span data-stu-id="74f8f-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="74f8f-112">Rahtikirjan luomisen jälkeen voit tehdä muutoksia siihen **Rahtikirja**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="74f8f-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="74f8f-113">Päärahtikirja</span><span class="sxs-lookup"><span data-stu-id="74f8f-113">Master bill of lading</span></span>
<span data-ttu-id="74f8f-114">Voit luoda päärahtikirjan, kun kuormassa on useampi kuin yksi lähetys</span><span class="sxs-lookup"><span data-stu-id="74f8f-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="74f8f-115">Siinä on sama asettelu ja samat tiedot kuin rahtikirjassa, mutta se sisältää yhteenvedon kaikkien lähetysten sisällöstä.</span><span class="sxs-lookup"><span data-stu-id="74f8f-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="74f8f-116">Jos **Luo päärahtikirja, kun kuormassa on useampi kuin yksi lähetys** -asetukseksi on määritetty **Kyllä** **Kuljetustenhallintaparametrit**-sivulla, päärahtikirja luodaan automaattisesti, jos luot rahtikirjan **Kuormasuunnittelun työtilassa** ja lähetyksiä on useampi.</span><span class="sxs-lookup"><span data-stu-id="74f8f-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="74f8f-117">Voit ladata myös rahtikirjojen luettelon valitsemalla **Aiheeseen liittyviä tietoja** &gt; **Rahtikirja**.</span><span class="sxs-lookup"><span data-stu-id="74f8f-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="74f8f-118">Jos olet luomassa rahtikirjat manuaalisesti, voit luoda päärahtikirjan **Rahtikirja**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="74f8f-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]