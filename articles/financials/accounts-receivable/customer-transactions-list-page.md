---
title: Asiakastapahtumien luettelosivu
description: "Tässä ohjeaiheessa on tietoja Microsoft Dynamics 365 for Finance and Operationsin asiakastapahtumien luettelosivusta."
author: mikefalkner
manager: aolson
ms.date: 08/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e828cb292ad48bb4690117b41589b25edcdf28bc
ms.contentlocale: fi-fi
ms.lasthandoff: 08/31/2018

---

# <a name="customer-transaction-list-page"></a><span data-ttu-id="84f29-103">Asiakastapahtumien luettelosivu</span><span class="sxs-lookup"><span data-stu-id="84f29-103">Customer transaction list page</span></span>

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a><span data-ttu-id="84f29-104">Näytä tilitykset</span><span class="sxs-lookup"><span data-stu-id="84f29-104">View settlements</span></span>

<span data-ttu-id="84f29-105">Toimintoruudun **Näytä tilitykset** -välilehdestä voi käyttää nopeasti tilityshistoriaa ja muita koko tilitystapahtumaa koskevia tietoja.</span><span class="sxs-lookup"><span data-stu-id="84f29-105">The **View settlements** tab on the action pane provides quick access to settlement history and more information about the whole settlement transaction.</span></span> <span data-ttu-id="84f29-106">Voit näyttää myös lisätapahtumat, jotka liittyvät valittuihin tapahtumiin joko siksi, että ne sisältyvät samaan tilitykseen, tai siksi, että ne ovat samassa maksukirjauskansiossa luotuja maksuja.</span><span class="sxs-lookup"><span data-stu-id="84f29-106">You can also show additional transactions that are related to the selected transaction, either because they were part of the same settlement or because they are payments that were created in the same payment journal.</span></span>

1. <span data-ttu-id="84f29-107">Valitse **Myyntireskontra \> Asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="84f29-107">Select **Accounts receivable \> Customers**.</span></span>
2. <span data-ttu-id="84f29-108">Valitse asiakas, jolla on tapahtumia, ja valitse sitten **Asiakas \> Tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="84f29-108">Select a customer that has transactions, and then select **Customer \> Transactions**.</span></span>
3. <span data-ttu-id="84f29-109">Valitse tarkasteltava tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="84f29-109">Select a transaction to research.</span></span>
4. <span data-ttu-id="84f29-110">Valitse toimintoruudussa **Näytä tilitykset** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="84f29-110">Select the **View settlements** tab on the action pane.</span></span>

    <span data-ttu-id="84f29-111">**Näytä tilitykset** -valintaikkunassa on valittu tapahtuma ja kaikki siihen täsmäytetyt asiakirjat.</span><span class="sxs-lookup"><span data-stu-id="84f29-111">The **View settlements** dialog box shows the selected transaction and all documents that have been settled against it.</span></span> <span data-ttu-id="84f29-112">Tämä valintaikkunan muistuttaa tilityshistorianäkymää, mutta se sisältää kaikki liittyvät asiakirjat.</span><span class="sxs-lookup"><span data-stu-id="84f29-112">This dialog box resembles the settlement history view, but it includes all related documents.</span></span> 

5. <span data-ttu-id="84f29-113">Tässä valintaikkunassa voi tehdä erilaisia tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="84f29-113">You can perform various tasks from this dialog box.</span></span> <span data-ttu-id="84f29-114">Valitse vähintään yksi tosite ja sitten jokin seuraavista valikoista:</span><span class="sxs-lookup"><span data-stu-id="84f29-114">Select one or more vouchers, and then select one of the following menus:</span></span>

   - <span data-ttu-id="84f29-115">**Näytä kirjanpito** – Kaikki valittuihin asiakirjoihin liittyvät tositteet tulevat näkyviin.</span><span class="sxs-lookup"><span data-stu-id="84f29-115">**View accounting** – All vouchers that are related to the selected documents appear.</span></span> <span data-ttu-id="84f29-116">Sulje valintaikkuna valitsemalla **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="84f29-116">Select **Close** to close the dialog box.</span></span>
   - <span data-ttu-id="84f29-117">**Vie** – vie valitus tositteet Microsoft Exceliin.</span><span class="sxs-lookup"><span data-stu-id="84f29-117">**Export** – Export the selected vouchers to Microsoft Excel.</span></span>
   - <span data-ttu-id="84f29-118">**Näytä liittyvät maksut** – Kaikki valittuun asiakirjaan liittyvät maksukirjauskansiossa luodut maksukirjauskansion tapahtumat tulevat näkyviin.</span><span class="sxs-lookup"><span data-stu-id="84f29-118">**View related payments** – All the payment journal transactions that were created in the payment journal that is related to the selected document appear.</span></span> <span data-ttu-id="84f29-119">Lisäksi kaikki kyseisiin maksuihin liittyvät tilitykset tulevat näkyviin.</span><span class="sxs-lookup"><span data-stu-id="84f29-119">In addition, all the settlements that are related to those payments appear.</span></span> <span data-ttu-id="84f29-120">Tämän valikon nimi vaihtuu nimeksi **Näytä tilitykset**.</span><span class="sxs-lookup"><span data-stu-id="84f29-120">The label of this menu also changes to **View settlements**.</span></span> <span data-ttu-id="84f29-121">Valitse **Näytä tilitykset**, jos haluat näyttää vain tapahtumat, jotka näytettiin, kun avasit **Näytä tilitykset** -valintaikkunan ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="84f29-121">Select **View settlements** to show only the transactions that were shown when you first opened the  **View settlements** dialog box.</span></span>
    - <span data-ttu-id="84f29-122">**Selvitä tapahtumat** – Tämä valikko avautuu, jos alun perin valittu asiakirja ei ole vielä kokonaan selvitetty.</span><span class="sxs-lookup"><span data-stu-id="84f29-122">**Settle transactions** – This menu appears if the original document that was selected wasn't fully settled.</span></span> <span data-ttu-id="84f29-123">Kun valitse sen, **Selvitä tapahtumat** -valintaikkuna avautuu, ja voit valita siinä selvitettävät tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="84f29-123">When you select it, the **Settle transactions** dialog box appears, where you can select transactions for settlement.</span></span>
    - <span data-ttu-id="84f29-124">**Kumoa tilitys** – Tämä valikko avautuu, jos alun perin valittu asiakirja on kokonaan selvitetty.</span><span class="sxs-lookup"><span data-stu-id="84f29-124">**Undo settlements** – This menu appears if the original document that was selected was fully settled.</span></span> <span data-ttu-id="84f29-125">Kun valitset sen, **Kumoa tilitykset** -valintaikkuna avautuu, ja voit kumota siinä kyseisen asiakirjan selvitykset.</span><span class="sxs-lookup"><span data-stu-id="84f29-125">When you select it, the **Undo settlements** dialog box appears, where you can undo the settlements that were done for that document.</span></span>
    

