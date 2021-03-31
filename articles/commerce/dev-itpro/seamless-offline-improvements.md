---
title: Lahjakortti- ja hyvityslaskutoimintojen saumaton offline-tilaan vaihtaminen
description: Tässä ohjeaiheessa on yleiskatsaus parannuksiin, jotka tarjoavat saumattoman offline-kytkimen tietyille maksutyypeille.
author: rubendel
manager: AnnBe
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 1ea46ae90dedcc3ad3c3b305bddeb4d98827353a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230665"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a><span data-ttu-id="b8bbd-103">Lahjakortti- ja hyvityslaskutoimintojen saumaton offline-tilaan vaihtaminen</span><span class="sxs-lookup"><span data-stu-id="b8bbd-103">Seamless offline switch for gift card and credit memo operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8bbd-104">Jos myyntipisteen laite menettää yhteyden kanavan tietokantaan, suurinta osa meneillään olevista myyntipistetoiminnoista ja -tapahtumista voidaan jatkaa sen jälkeen, kun kassanhoitaja vastaanottaa varoitussanoman yhteyden menettämisestä.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-104">If a point of sale (POS) device loses its connection to the channel database, most POS operations and transactions that were in progress can proceed after the cashier receives a warning message about the loss of connectivity.</span></span> <span data-ttu-id="b8bbd-105">Joissakin tapauksissa tapahtumilla on elementtejä, jotka edellyttävät reaaliaikaista palvelua. Näitä elementtejä ei tueta, jos myyntipiste on offline-tilassa.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-105">However, in some cases, transactions have elements that rely on the real-time service, and those elements aren't supported when the POS is offline.</span></span> <span data-ttu-id="b8bbd-106">Tässä ohjeaiheessa kuvataan joitakin toimintoja, jotka auttavat vähentämään menetetyn yhteyden vaikutusta näissä skenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-106">This topic describes some functionality that helps reduce the impact of lost connectivity in these scenarios.</span></span>

## <a name="completing-gift-card-transactions-in-offline-mode"></a><span data-ttu-id="b8bbd-107">Lahjakorttitapahtumien päättäminen offline-tilassa</span><span class="sxs-lookup"><span data-stu-id="b8bbd-107">Completing gift card transactions in offline mode</span></span>

<span data-ttu-id="b8bbd-108">Sisäiset lahja kortit vaativat reaaliaikaisen palvelun, koska lahjakorttien saldoa on ylläpidettävä keskitetysti Microsoft Dynamics 365 Commerce Headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-108">Internal gift cards depend on the real-time service, because the balance for the gift cards must be centrally maintained in Microsoft Dynamics 365 Commerce Headquarters.</span></span> <span data-ttu-id="b8bbd-109">Voit estää petokset tai synkronointiongelmat, jos lahjakortit lukitaan heti tapahtumaan lisäämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-109">To help prevent fraud or other synchronization issues, gift cards are locked as soon as they are added to a transaction.</span></span> <span data-ttu-id="b8bbd-110">Lukitustoiminnon avulla voidaan varmistaa, että lahjakorttia ei voi käyttää useilla päätteillä samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-110">The locking function ensures that a gift card can't be used on multiple terminals at the same time.</span></span> <span data-ttu-id="b8bbd-111">Kun tapahtuma on valmis, lahjakortti päivitetään ja sen lukitus poistetaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-111">When a transaction is completed, the gift card is updated and unlocked.</span></span>

<span data-ttu-id="b8bbd-112">Jos myyntipiste kuitenkin menettää yhteyden sen jälkeen, kun lahjakortti on lisätty tapahtumaan, lahjakorttia ei ehkä voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-112">However, if the POS loses connectivity after a gift card has been added to a transaction, the gift card can become unusable.</span></span> <span data-ttu-id="b8bbd-113">Voit estää tämän tilanteen Dynamics 365 Commercen parametrin avulla. Se mahdollistaa lahjakortin sisältämien tapahtumien suorittamisen myyntipisteen ollessa offline-tilassa.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-113">To help prevent this situation, Dynamics 365 Commerce has a parameter that enables transactions that include a gift card line to be completed while the POS is offline.</span></span> <span data-ttu-id="b8bbd-114">Kun tämä parametri on otettu käyttöön, lahjakorttitapahtumat, jotka ovat offline-tilassa, voidaan tallentaa yhdessä offline-tapahtumien kanssa. Ne synkronoidaan Commerce Headquarters -sovellukseen offline-tapahtumien synkronoinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-114">When this parameter is turned on, gift card transactions that are forced offline will be saved together with offline transactions, and they will be synced to Commerce Headquarters when the offline transactions are synced.</span></span> <span data-ttu-id="b8bbd-115">Synkronointi poistaa myös lahjakortin lukituksen, jotta sitä voidaan käyttää toisessa päätteessä.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-115">The synchronization will also unlock the gift card so that it can be used at another terminal.</span></span>

<span data-ttu-id="b8bbd-116">Jos haluat, että toiminto voi tehdä lahjakorttitapahtumat offline-tilaan siirtymisen jälkeen, siirry **Kirjaus**-välilehteen **Commerce-parametrit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-116">To enable the functionality to conclude gift card transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="b8bbd-117">Etsi tässä välilehdessä **Lahjakortti**-pikavälilehti ja määritä **Salli lahjakorttitapahtumien päättäminen offline-tilassa** -kohdan arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-117">On that tab, locate the **Gift card** fasttab and set **Allow concluding gift card transactions in offline mode** to **Yes**.</span></span>

![Offline-lahjakortin asetus](../media/gift.png)

<span data-ttu-id="b8bbd-119">Commerce-parametrit ovat yleensä välimuistissa.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-119">Commerce parameters are typically cached.</span></span> <span data-ttu-id="b8bbd-120">Siksi tämän parametrin päivittämisen ja jakeluaikataulun kanavaan synkronoinnin aloittamisen jälkeen muutoksen voimaantulo voi kestää jopa 24 tuntia.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-120">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="b8bbd-121">Jos haluat, että muutos tulee voimaan heti, nollaa Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="b8bbd-121">To make the change effective immediately, reset Microsoft Internet Information Services (IIS).</span></span>

## <a name="completing-credit-memo-transactions-in-offline-mode"></a><span data-ttu-id="b8bbd-122">Hyvitystapahtumien päättäminen offline-tilassa</span><span class="sxs-lookup"><span data-stu-id="b8bbd-122">Completing credit memo transactions in offline mode</span></span>

<span data-ttu-id="b8bbd-123">Hyvityslaskuja ylläpidetään keskitetysti Commerce Headquarters -sovelluksessa sisäisten lahjakorttien tapaan.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-123">Like internal gift cards, credit memos are centrally maintained in Commerce Headquarters.</span></span> <span data-ttu-id="b8bbd-124">Commerce sisältää parametrin, jonka avulla hyvityslaskutapahtumat voidaan tehdä valmiiksi myyntipisteen ollessa offline-tilassa.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-124">Commerce has a parameter that enables credit memo transactions to be completed while the POS is offline.</span></span> <span data-ttu-id="b8bbd-125">Tämä parametri toimii kuten edellisessä osassa mainittu lahjakorttiparametri.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-125">This parameter works like the gift card parameter that was mentioned in the previous section.</span></span> <span data-ttu-id="b8bbd-126">Kun parametri on otettu käyttöön, offline-tilassa käytössä olevat hyvityslaskutapahtumat synkronoidaan takaisin kanavan tietokantaan yhdessä niiden tapahtumien kanssa, jotka suoritettiin myyntipisteen ollessa offline-tilassa.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-126">When the parameter is turned on, credit memo transactions that are forced offline will be synced back to the channel database, together with other transactions that were performed while the POS was offline.</span></span>

<span data-ttu-id="b8bbd-127">Jos haluat, että toiminto voi tehdä hyvityslaskutapahtumat offline-tilaan siirtymisen jälkeen, siirry **Kirjaus**-välilehteen **Commerce-parametrit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-127">To enable the functionality to conclude credit memo transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="b8bbd-128">Etsi tässä välilehdessä **Hyvityslasku**-pikavälilehti ja määritä **Salli hyvityslaskutapahtumien päättäminen offline-tilassa** -kohdan arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-128">On that tab, locate the **Credit memo** fasttab and set **Allow concluding credit memo transactions in offline mode** to **Yes**.</span></span>

![Offline-hyvityslaskun asetus](../media/creditmemo.png)

<span data-ttu-id="b8bbd-130">Commerce-parametrit ovat yleensä välimuistissa.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-130">Commerce parameters are typically cached.</span></span> <span data-ttu-id="b8bbd-131">Siksi tämän parametrin päivittämisen ja jakeluaikataulun kanavaan synkronoinnin aloittamisen jälkeen muutoksen voimaantulo voi kestää jopa 24 tuntia.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-131">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="b8bbd-132">Jos haluat, että muutos on voimassa heti, nollaa IIS.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-132">To make the change effective immediately, reset IIS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8bbd-133">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="b8bbd-133">Related topics</span></span>

- [<span data-ttu-id="b8bbd-134">Myyntipistetoiminto offline-tilassa</span><span class="sxs-lookup"><span data-stu-id="b8bbd-134">Offline point of sale (POS) functionality</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-offline-functionality)
- [<span data-ttu-id="b8bbd-135">Myyntipisteen toiminnot (POS) verkossa ja paikallisesti</span><span class="sxs-lookup"><span data-stu-id="b8bbd-135">Online and offline point of sale (POS) operations</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]