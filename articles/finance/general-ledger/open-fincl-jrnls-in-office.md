---
title: Talouskirjauskansiomallien avaaminen Officessa
description: Tässä aiheessa kuvataan ongelmia, joita saattaa ilmetä, kun luot mukautettuja talouskirjauskansioita Microsoft Excel ‑mallin avulla.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089454"
---
# <a name="open-financial-journal-templates-in-office"></a><span data-ttu-id="0d48f-103">Talouskirjauskansiomallien avaaminen Officessa</span><span class="sxs-lookup"><span data-stu-id="0d48f-103">Open financial journal templates in Office</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d48f-104">Tässä aiheessa kuvataan ongelmia, joita saattaa ilmetä, kun luot mukautettuja talouskirjauskansioita Microsoft Excel ‑mallin avulla.</span><span class="sxs-lookup"><span data-stu-id="0d48f-104">This topic describes issues that might occur when you create custom financial journals by using a Microsoft Excel template.</span></span>

## <a name="symptom"></a><span data-ttu-id="0d48f-105">Oire</span><span class="sxs-lookup"><span data-stu-id="0d48f-105">Symptom</span></span>

<span data-ttu-id="0d48f-106">Olet luonut mukautetun Excel-mallin talouskirjauskansioita varten, mutta se ei näy **Avaa rivit Excelissä** ‑valikossa.</span><span class="sxs-lookup"><span data-stu-id="0d48f-106">You created a custom Excel template for financial journals, but it doesn't appear on the **Open lines in Excel** menu.</span></span> <span data-ttu-id="0d48f-107">Vaihtoehtoisesti malli näkyy valikossa, mutta kun valitset sen, näyttöön avautuu toinen malli.</span><span class="sxs-lookup"><span data-stu-id="0d48f-107">Alternatively, it does appear on the menu, a different template is opened but when you select it.</span></span>

## <a name="resolution"></a><span data-ttu-id="0d48f-108">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="0d48f-108">Resolution</span></span>

<span data-ttu-id="0d48f-109">Oletusarvoinen Avaa Excelissä ‑toiminto määrittää nykyisen sivun juuritietolähteen (taulun) avulla, mitkä Office-mallit tai -tietoyksiköt näkyvät vaihtoehtoina **Avaa Excelissä** ‑valikossa.</span><span class="sxs-lookup"><span data-stu-id="0d48f-109">The default Open in Excel functionality uses the root data source (table) of the current page to determine which Office templates or data entities appear as options on the **Open in Excel** menu.</span></span> <span data-ttu-id="0d48f-110">Tämä toiminta ei sovi ihanteellisesti talouskirjauskansioille, koska ne käyttävät samoja tauluja (LedgerJournalTable ja LedgerJournalTrans) kuin monien muiden kirjauskansiotyyppien juuritietolähde.</span><span class="sxs-lookup"><span data-stu-id="0d48f-110">This behavior isn't an ideal experience for financial journals, because financial journals use the same tables (LedgerJournalTable and LedgerJournalTrans) as the root data source of many other types of journals.</span></span>

<span data-ttu-id="0d48f-111">Talouskirjauskansioiden kohdalla Avaa rivit Excelissä ‑toiminnon tarkoituksena on näyttää sille kirjauskansiolle suunnitellut mallit, jonka kontekstissa parhaillaan työskentelet, kuten yleiselle kirjauskansiolle tai maksukirjauskansiolle.</span><span class="sxs-lookup"><span data-stu-id="0d48f-111">For financial journals, the Open Lines in Excel functionality is intended to show templates that are designed for the journal that you're currently working in the context of, such as the general journal or a payment journal.</span></span> <span data-ttu-id="0d48f-112">Esimerkiksi toimittajan maksukirjauskansion kanssa käytettäväksi tarkoitettu malli on suunniteltu siten, että se pakottaa ensisijaisen tilisi käytön toimittajatilinä.</span><span class="sxs-lookup"><span data-stu-id="0d48f-112">For example, a template that is intended to be used with a vendor payment journal will be designed to enforce your primary account as a vendor account.</span></span>

<span data-ttu-id="0d48f-113">Jos haluat korottaa mallin niin, että se on käytettävissä **Avaa rivit Excelissä**‑ ja **Avaa Excelissä** ‑valikoissa, voit tehdä sen kehittäjänä helposti toteuttamalla **LedgerIJournalExcelTemplate**-liittymän ja laajentamalla **DocuTemplateRegistrationBase**-luokan.</span><span class="sxs-lookup"><span data-stu-id="0d48f-113">If you want to promote a template so that it's available on the **Open lines in Excel** and **Open in Excel** menus, an easy developer experience is to implement the **LedgerIJournalExcelTemplate** interface and extend the **DocuTemplateRegistrationBase** class.</span></span> <span data-ttu-id="0d48f-114">Järjestelmässä on toteutettu useita esimerkkejä tästä menetelmästä.</span><span class="sxs-lookup"><span data-stu-id="0d48f-114">Many examples of this approach are implemented in the system.</span></span> <span data-ttu-id="0d48f-115">Yksi esimerkki, jota voidaan käyttää viitteenä, on yleistä kirjauskansiota (tai päivittäistä kirjauskansiota) varten luotu **LedgerDailyJournalExcelTemplate**-liittymä.</span><span class="sxs-lookup"><span data-stu-id="0d48f-115">One example that can be used for reference is the **LedgerDailyJournalExcelTemplate** interface that was created for the general journal (or daily journal).</span></span>

<span data-ttu-id="0d48f-116">Kun mallille on toteutettu **LedgerIJournalExcelTemplate**-liittymä, **Avaa rivit Excelissä** ‑valikko suodattaa mallit kirjauskansion kirjauskansiotyypin mukaan ja näyttää vain mallit, jotka ovat käytettävissä tälle kirjauskansiolle.</span><span class="sxs-lookup"><span data-stu-id="0d48f-116">When the **LedgerIJournalExcelTemplate** interface is implemented for your template, the **Open Lines in Excel** menu will filter templates by the journal type of your journal and will show only the templates that are available for that journal.</span></span> <span data-ttu-id="0d48f-117">Liittymä tarjoaa myös vahvistusmenetelmän, jonka avulla varmistetaan, että kirjauskansion mallia ei voi avata, jos se ei vastaa tilityypin vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="0d48f-117">The interface also provides a validation method that ensures that a template can't be opened for a journal if it doesn't meet the account type requirements.</span></span> <span data-ttu-id="0d48f-118">Voit esimerkiksi määrittää, että tilityypin on oltava **Toimittaja** tai **Kirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="0d48f-118">For example, you can specify that the account type must be of the **Vendor** or **Ledger** type.</span></span>

<span data-ttu-id="0d48f-119">Lisätietoja tästä toiminnosta on kohdassa [Mallien lisääminen Avaa rivit Excelissä ‑valikkoon](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span><span class="sxs-lookup"><span data-stu-id="0d48f-119">For more information about this functionality, see [Add templates to the Open lines in Excel menu](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span></span>
