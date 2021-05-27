---
title: Kirjauskansioiden ja rivien asetusten palauttaminen
description: Tässä ohjeaiheessa kerrotaan, miksi kirjanpitoon syötettyä vastakirjausta ei ehkä sisällytetä kirjattuun tapahtumaan.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028560"
---
# <a name="reverse-settings-on-journals-and-lines"></a><span data-ttu-id="e19e3-103">Kirjauskansioiden ja rivien asetusten palauttaminen</span><span class="sxs-lookup"><span data-stu-id="e19e3-103">Reverse settings on journals and lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e19e3-104">Tässä ohjeaiheessa kerrotaan, miksi kirjanpitoon syötettyä vastakirjausta ei ehkä sisällytetä kirjattuun tapahtumaan.</span><span class="sxs-lookup"><span data-stu-id="e19e3-104">This topic addresses why a reversing entry that was entered on a general journal might not be included on the posted transaction.</span></span>  

## <a name="symptom"></a><span data-ttu-id="e19e3-105">Oire</span><span class="sxs-lookup"><span data-stu-id="e19e3-105">Symptom</span></span>

<span data-ttu-id="e19e3-106">Kirjanpito sisältää vastakirjauksen ja vastakirjauksen päivämäärän kirjauskansiossa.</span><span class="sxs-lookup"><span data-stu-id="e19e3-106">A general journal includes a reversing entry and reversing date on the journal.</span></span> <span data-ttu-id="e19e3-107">Kun kirjaat kirjauskansion, yhtäkään tositetta ei peruuteta.</span><span class="sxs-lookup"><span data-stu-id="e19e3-107">When you post the journal, none of the vouchers are reversed.</span></span> <span data-ttu-id="e19e3-108">Miksi tapahtuu näin?</span><span class="sxs-lookup"><span data-stu-id="e19e3-108">Why does this happen?</span></span>

## <a name="resolution"></a><span data-ttu-id="e19e3-109">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="e19e3-109">Resolution</span></span>

<span data-ttu-id="e19e3-110">Kun kirjauskansio kirjataan, peruutusprosessi etsii vain **Vastakirjaus**- ja **Vastakirjauksen päivämäärä** -asetukset tositteen **Rivit**-osassa.</span><span class="sxs-lookup"><span data-stu-id="e19e3-110">When the journal is posted, the reversing process looks only at the **Revering entry** and **Reversing date** settings on the **Lines** section of the voucher.</span></span> <span data-ttu-id="e19e3-111">Tämän menetelmän avulla kirjauskansio voi sisältää sekä peruutettaviksi merkittyjä että ei-peruutettavia tositteita.</span><span class="sxs-lookup"><span data-stu-id="e19e3-111">This approach allows a journal to include some vouchers that are marked for reversing, and others that are not.</span></span>

<span data-ttu-id="e19e3-112">Kirjauskansion arvoja käytetään oletusarvoina vain lisättäessä *uusia* rivejä.</span><span class="sxs-lookup"><span data-stu-id="e19e3-112">The values from the journal are only used as defaults when adding *new* lines.</span></span> <span data-ttu-id="e19e3-113">Kirjauskansion arvojen muuttaminen ei vaikuta aiemmin luotuihin riveihin.</span><span class="sxs-lookup"><span data-stu-id="e19e3-113">Changing the values on the journal doesn’t affect existing lines.</span></span> <span data-ttu-id="e19e3-114">Tässä esimerkissä tositerivit syötettiin ensin.</span><span class="sxs-lookup"><span data-stu-id="e19e3-114">In this example, the voucher lines were entered first.</span></span> <span data-ttu-id="e19e3-115">Kun syötät rivin tiedot ennen kirjauskansion määrittämistä peruutettavaksi, määritystä vastakirjauksena ja vastakirjauksen päivämääränä ei käytetä olemassa olevissa riveissä.</span><span class="sxs-lookup"><span data-stu-id="e19e3-115">When you enter the line detail before designating the journal as reversing, the designation as a reversing entry and date won't be applied to any existing lines.</span></span>

<span data-ttu-id="e19e3-116">Jos olemassa olevan rivin vastakirjausta tai vastakirjauksen päivämäärää muutetaan, muutos kohdistetaan myös muihin saman tositteen riveihin.</span><span class="sxs-lookup"><span data-stu-id="e19e3-116">Changing the reversing entry or reversing date on an existing line propagates that change to other lines in the same voucher.</span></span> <span data-ttu-id="e19e3-117">Suorituskyvyn parantamiseksi ruudukkoa ei päivitetä sen jälkeen, kun muutokset on lisätty muihin riveihin.</span><span class="sxs-lookup"><span data-stu-id="e19e3-117">To optimize performance, the grid is not refreshed after propagating changes to other Lines.</span></span> <span data-ttu-id="e19e3-118">Päivitetyt arvot tulevat näkyviin ruudukon päivittämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="e19e3-118">You can display the updated values by refreshing the grid.</span></span>


