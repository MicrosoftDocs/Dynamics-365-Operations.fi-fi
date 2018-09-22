---
title: Toimittajatapahtumien luettelosivu
description: "Tässä ohjeaiheessa on tietoja Microsoft Dynamics 365 for Finance and Operationsin toimittajatapahtumien luettelosivusta."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 1ef7d97f059801f2fb2c0d451546b57055208f81
ms.contentlocale: fi-fi
ms.lasthandoff: 08/31/2018

---

# <a name="vendor-transaction-list-page"></a><span data-ttu-id="e1300-103">Toimittajatapahtumien luettelosivu</span><span class="sxs-lookup"><span data-stu-id="e1300-103">Vendor transaction list page</span></span>

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a><span data-ttu-id="e1300-104">Näytä tilitykset</span><span class="sxs-lookup"><span data-stu-id="e1300-104">View settlements</span></span>

<span data-ttu-id="e1300-105">Toimintoruudun **Näytä tilitykset** -välilehdestä voi käyttää nopeasti tilityshistoriaa ja muita koko tilitystapahtumaa koskevia tietoja.</span><span class="sxs-lookup"><span data-stu-id="e1300-105">The **View settlements** tab on the action pane provides quick access to settlement history and more information about the whole settlement transaction.</span></span> <span data-ttu-id="e1300-106">Voit näyttää myös lisätapahtumat, jotka liittyvät valittuihin tapahtumiin joko siksi, että ne sisältyvät samaan tilitykseen, tai siksi, että ne ovat samassa maksukirjauskansiossa luotuja maksuja.</span><span class="sxs-lookup"><span data-stu-id="e1300-106">You can also show additional transactions that are related to the selected transaction, either because they were part of the same settlement or because they are payments that were created in the same payment journal.</span></span>

1. <span data-ttu-id="e1300-107">Valitse **Ostoreskontra \> Kaikki toimittajat**.</span><span class="sxs-lookup"><span data-stu-id="e1300-107">Select **Accounts payable \> All vendors**.</span></span>
2. <span data-ttu-id="e1300-108">Valitse toimittaja, jolla on tapahtumia, ja valitse sitten **Toimittaja \> Tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="e1300-108">Select a vendor that has transactions, and then select **Vendor \> Transactions**.</span></span>
3. <span data-ttu-id="e1300-109">Valitse tarkasteltava tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="e1300-109">Select a transaction to research.</span></span>
4. <span data-ttu-id="e1300-110">Valitse toimintoruudussa **Näytä tilitykset** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="e1300-110">Select the **View settlements** tab on the action pane.</span></span>

    <span data-ttu-id="e1300-111">Avautuvassa **Näytä tilitykset** -valintaikkunassa on valittu tapahtuma ja kaikki siihen täsmäytetyt asiakirjat.</span><span class="sxs-lookup"><span data-stu-id="e1300-111">The **View settlements** dialog box opens and shows the selected transaction and all documents that are settled against it.</span></span> <span data-ttu-id="e1300-112">Tämä valintaikkunan muistuttaa tilityshistorianäkymää, mutta se sisältää kaikki liittyvät asiakirjat.</span><span class="sxs-lookup"><span data-stu-id="e1300-112">This dialog box resembles the settlement history view, but it includes all related documents.</span></span>

5. <span data-ttu-id="e1300-113">Tässä valintaikkunassa voi tehdä erilaisia tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="e1300-113">You can perform various tasks from this dialog box.</span></span> <span data-ttu-id="e1300-114">Valitse vähintään yksi tosite ja sitten jokin seuraavista valikoista:</span><span class="sxs-lookup"><span data-stu-id="e1300-114">Select one or more vouchers, and then select one of the following menus:</span></span>

   - <span data-ttu-id="e1300-115">**Näytä kirjanpito** – Kaikki valittuihin asiakirjoihin liittyvät tositteet tulevat näkyviin.</span><span class="sxs-lookup"><span data-stu-id="e1300-115">**View accounting** – All vouchers that are related to the selected documents appear.</span></span> <span data-ttu-id="e1300-116">Sulje valintaikkuna valitsemalla **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="e1300-116">Select **Close** to close the dialog box.</span></span>
   - <span data-ttu-id="e1300-117">**Vie** – vie valitus tositteet Microsoft Exceliin.</span><span class="sxs-lookup"><span data-stu-id="e1300-117">**Export** – Export the selected vouchers to Microsoft Excel.</span></span>
   - <span data-ttu-id="e1300-118">**Näytä liittyvät maksut** – Kaikki valittuun asiakirjaan liittyvät maksukirjauskansiossa luodut maksukirjauskansion tapahtumat tulevat näkyviin.</span><span class="sxs-lookup"><span data-stu-id="e1300-118">**View related payments** – All the payment journal transactions that were created in the payment journal that is related to the selected document appear.</span></span> <span data-ttu-id="e1300-119">Lisäksi kaikki kyseisiin maksuihin liittyvät tilitykset tulevat näkyviin.</span><span class="sxs-lookup"><span data-stu-id="e1300-119">In addition, all the settlements that are related to those payments appear.</span></span> <span data-ttu-id="e1300-120">Tämän valikon nimi vaihtuu nimeksi **Näytä tilitykset**.</span><span class="sxs-lookup"><span data-stu-id="e1300-120">The label of this menu also changes to **View settlements**.</span></span> <span data-ttu-id="e1300-121">Valitse **Näytä tilitykset**, jos haluat näyttää vain tapahtumat, jotka näytettiin, kun avasit **Näytä tilitykset** -valintaikkunan ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="e1300-121">Select **View settlements** to show only the transactions that were shown when you first opened the  **View settlements** dialog box.</span></span>
    - <span data-ttu-id="e1300-122">**Selvitä tapahtumat** – Tämä valikko avautuu, jos alun perin valittu asiakirja ei ole vielä kokonaan selvitetty.</span><span class="sxs-lookup"><span data-stu-id="e1300-122">**Settle transactions** – This menu appears if the original document that was selected wasn't fully settled.</span></span> <span data-ttu-id="e1300-123">Kun valitse sen, **Selvitä tapahtumat** -valintaikkuna avautuu, ja voit valita siinä selvitettävät tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="e1300-123">When you select it, the **Settle transactions** dialog box appears, where you can select transactions for settlement.</span></span>
    - <span data-ttu-id="e1300-124">**Kumoa tilitys** – Tämä valikko avautuu, jos alun perin valittu asiakirja on kokonaan selvitetty.</span><span class="sxs-lookup"><span data-stu-id="e1300-124">**Undo settlements** – This menu appears if the original document that was selected was fully settled.</span></span> <span data-ttu-id="e1300-125">Kun valitset sen, **Kumoa tilitykset** -valintaikkuna avautuu, ja voit kumota siinä kyseisen asiakirjan selvitykset.</span><span class="sxs-lookup"><span data-stu-id="e1300-125">When you select it, the **Undo settlements** dialog box appears, where you can undo the settlements that were done for that document.</span></span>

