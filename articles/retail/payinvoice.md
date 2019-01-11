---
title: "Laskun maksutapojen määrittäminen"
description: "Tässä ohjeaiheessa kuvataan, miten voit määrittää Dynamics 365 for Retailin tukemaan laskun maksamiseen liittyviä erilaisia tilanteita."
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: b7132dc9b3c78fa04fcfc38ea72b5678ad08deb2
ms.contentlocale: fi-fi
ms.lasthandoff: 01/04/2019

---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="e5ceb-103">Laskun maksutapojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e5ceb-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e5ceb-104">Dynamics 365 for Retailin Maksa lasku -toiminnallisuutta on laajennettu tukemaan seuraavia tilanteita:</span><span class="sxs-lookup"><span data-stu-id="e5ceb-104">The Pay invoice functionality in Dynamics 365 for Retail has been expanded to support:</span></span>

- <span data-ttu-id="e5ceb-105">Useiden myyntitilauslaskujen maksaminen yhdessä myyntipistetapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="e5ceb-106">Erilaisten asiakaslaskutyyppien, esimerkiksi vapaatekstilaskujen, projektiin perustuvien laskujen ja hyvityslaskujen, maksaminen.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="e5ceb-107">Näiden ominaisuuksien käyttöönottamiseksi myymälöiden toimintoprofiili on määritettävä alla kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="e5ceb-108">Siirry kohtaan **Vähittäismyynti \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit** ja valitse profiili, joka on linkitetty myymälöihin, joita haluat muutoksen koskevan.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-108">Go to **Retail \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="e5ceb-109">Määritä **Toiminnot**-välilehdessä seuraavat parametrit tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="e5ceb-110">**Myyntitilauslasku** – Valitse **Kyllä**, jotta käyttäjät voivat maksaa yhden tai useamman myyntitilaukseen perustuvan laskun yhdessä myyntipistetapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="e5ceb-111">**Vapaatekstilasku** – Valitse **Kyllä**, jotta käyttäjät voivat maksaa yhden tai useamman vapaatekstilaskun yhdessä myyntipistetapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="e5ceb-112">**Projektilasku** – Valitse **Kyllä**, jotta käyttäjät voivat maksaa yhden tai useamman projektiin perustuvan laskun yhdessä myyntipistetapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="e5ceb-113">**Myyntitilauksen hyvityslasku** – Valitse **Kyllä**, jotta käyttäjät voivat selvittää useita myyntitilaukseen perustuvia hyvityslaskuja avoimet laskut huomioiden tai käsitellä avoimen hyvityslaskun hyvityksen asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="e5ceb-114">Osittaisten summien maksua tai selvitystä ei vielä tueta.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-114">Payment or settlement of partial amounts is not yet supported.</span></span>

