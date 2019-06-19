---
title: Laskun maksutapojen määrittäminen
description: Tässä aiheessa kuvataan, miten voit konfiguroida Dynamics 365 for Retailin tukemaan erilaisia laskun maksamiseen liittyviä tilanteita.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b7132dc9b3c78fa04fcfc38ea72b5678ad08deb2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564967"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="f4d36-103">Laskun maksutapojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f4d36-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f4d36-104">Dynamics 365 for Retailin Maksa lasku -toiminnallisuutta on laajennettu tukemaan seuraavia tilanteita:</span><span class="sxs-lookup"><span data-stu-id="f4d36-104">The Pay invoice functionality in Dynamics 365 for Retail has been expanded to support:</span></span>

- <span data-ttu-id="f4d36-105">Useiden myyntitilauslaskujen maksaminen yhdessä myyntipistetapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="f4d36-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="f4d36-106">Erilaisten asiakaslaskutyyppien, esimerkiksi vapaatekstilaskujen, projektiin perustuvien laskujen ja hyvityslaskujen, maksaminen.</span><span class="sxs-lookup"><span data-stu-id="f4d36-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="f4d36-107">Näiden ominaisuuksien käyttöönottamiseksi myymälöiden toimintoprofiili on määritettävä alla kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="f4d36-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="f4d36-108">Siirry kohtaan **Vähittäismyynti \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit** ja valitse profiili, joka on linkitetty myymälöihin, joita haluat muutoksen koskevan.</span><span class="sxs-lookup"><span data-stu-id="f4d36-108">Go to **Retail \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="f4d36-109">Määritä **Toiminnot**-välilehdessä seuraavat parametrit tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="f4d36-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="f4d36-110">**Myyntitilauslasku** – Valitse **Kyllä**, jotta käyttäjät voivat maksaa yhden tai useamman myyntitilaukseen perustuvan laskun yhdessä myyntipistetapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="f4d36-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="f4d36-111">**Vapaatekstilasku** – Valitse **Kyllä**, jotta käyttäjät voivat maksaa yhden tai useamman vapaatekstilaskun yhdessä myyntipistetapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="f4d36-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="f4d36-112">**Projektilasku** – Valitse **Kyllä**, jotta käyttäjät voivat maksaa yhden tai useamman projektiin perustuvan laskun yhdessä myyntipistetapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="f4d36-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="f4d36-113">**Myyntitilauksen hyvityslasku** – Valitse **Kyllä**, jotta käyttäjät voivat selvittää useita myyntitilaukseen perustuvia hyvityslaskuja avoimet laskut huomioiden tai käsitellä avoimen hyvityslaskun hyvityksen asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="f4d36-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="f4d36-114">Osittaisten summien maksua tai selvitystä ei vielä tueta.</span><span class="sxs-lookup"><span data-stu-id="f4d36-114">Payment or settlement of partial amounts is not yet supported.</span></span>
