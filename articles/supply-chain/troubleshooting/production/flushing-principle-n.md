---
title: Tuoterakennerivien materiaaliottosäännön asetuksia ei ole noudateta
description: Tuoterakennerivien materiaaliottosäännön asetuksia ei ole noudateta.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026475"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a><span data-ttu-id="51ec6-103">Tuoterakennerivien materiaaliottosäännön asetuksia ei ole noudateta</span><span class="sxs-lookup"><span data-stu-id="51ec6-103">Flushing principle settings on BOM lines aren't respected</span></span>

<span data-ttu-id="51ec6-104">Tietopankin numero: 4612725</span><span class="sxs-lookup"><span data-stu-id="51ec6-104">KB number: 4612725</span></span>

## <a name="symptoms"></a><span data-ttu-id="51ec6-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="51ec6-105">Symptoms</span></span>

<span data-ttu-id="51ec6-106">Tämä ongelma ilmenee, kun **Automaattinen tuoterakennekulutus** -kenttä **Automaattinen päivitys** -välilehdellä **Tuotannonhallinnan parametrit** -sivulla määritetään arvoon *Materiaaliottosääntö*.</span><span class="sxs-lookup"><span data-stu-id="51ec6-106">This issue occurs when the **Automatic BOM consumption** field on the **Automatic update** tab of the **Production control parameters** page is set to *Flushing principle*.</span></span> <span data-ttu-id="51ec6-107">Tämä asetus ilmaisee, että kaikki tuoterakennerivit tulee kuluttaa automaattisesti, kun ostotilaus vastaanotetaan.</span><span class="sxs-lookup"><span data-stu-id="51ec6-107">This setting indicates that all bill of materials (BOM) lines should automatically be consumed when a purchase order is received.</span></span> <span data-ttu-id="51ec6-108">Jos tuoterakennerivien **Materiaaliottosääntö**-kentän arvoksi on nimenomaisesti määritetty *Manuaalinen*, voit odottaa, ettei tuoterakennerivejä kuluteta automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="51ec6-108">If the **Flushing principle** field on BOM lines is explicitly set to *Manual*, you might expect that the BOM lines won't automatically be consumed.</span></span> <span data-ttu-id="51ec6-109">Kuitenkin kun tämä ongelma ilmenee, tuoterakennerivit, joissa **Materiaaliottosääntö**-kentän arvoksi on määritetty *Manuaalinen*, kulutetaan automaattisesti joka tapauksessa.</span><span class="sxs-lookup"><span data-stu-id="51ec6-109">However, when this issue occurs, BOM lines where the **Flushing principle** field is set to *Manual* are automatically consumed anyway.</span></span>

## <a name="resolution"></a><span data-ttu-id="51ec6-110">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="51ec6-110">Resolution</span></span>

<span data-ttu-id="51ec6-111">Jos tämä ongelma ilmenee, tuotannonhallintaparametrit voidaan määrittää ohittamaan tuoterakennerivien **Materiaaliottosääntö**-asetus.</span><span class="sxs-lookup"><span data-stu-id="51ec6-111">If you're experiencing this issue, your production control parameters might be set up to override the **Flushing principle** setting on BOM lines.</span></span> <span data-ttu-id="51ec6-112">Tarkista **Tuotannonhallinnan parametrit** -sivun **Automaattinen päivitys** -välilehdessä **Automaattinen tuoterakennekulutus** -arvo.</span><span class="sxs-lookup"><span data-stu-id="51ec6-112">On the **Production control parameters** page, on the **Automatic update** tab, check the value of the **Automatic BOM consumption** field.</span></span> <span data-ttu-id="51ec6-113">Jos asetukseksi on määritetty *Aina*, järjestelmä ohittaa kaikkien tuoterakennerivien **Materiaaliottosääntö**-asetuksen ja tyhjentää rivit aina.</span><span class="sxs-lookup"><span data-stu-id="51ec6-113">If it's set to *Always*, the system will disregard the **Flushing principle** setting on all BOM lines and will always flush the lines.</span></span> <span data-ttu-id="51ec6-114">Jos haluat, että järjestelmä noudattaa tuoterakennerivien **Materiaaliottosääntö**-asetusta, muuta **Automaattinen tuoterakennekulutus** -kentän arvoksi *Materiaaliottosääntö*.</span><span class="sxs-lookup"><span data-stu-id="51ec6-114">To make the system respect the **Flushing principle** setting on BOM lines, change the value of the **Automatic BOM consumption** field to *Flushing principle*.</span></span>
