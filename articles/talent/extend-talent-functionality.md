---
title: Microsoft Dynamics 365 for Talent -sovelluksen toimintojen laajentaminen
description: "Jos olet luonut jonkin Microsoft PowerApps -sovelluksen, voit käynnistää sovelluksen Microsoft Dynamics 365 for Talent -sovelluksen linkin avulla."
author: rschloma
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 51eb4288f5b6c732755007c1dcd8c4db090ccc0a
ms.contentlocale: fi-fi
ms.lasthandoff: 03/07/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="383f1-103">Microsoft Dynamics 365 for Talent -sovelluksen toimintojen laajentaminen</span><span class="sxs-lookup"><span data-stu-id="383f1-103">Extend the functionality of Microsoft Dynamics 365 for Talent</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="383f1-104">Jos olet luonut jonkin Microsoft PowerApps -sovelluksen, voit käynnistää sovelluksen Microsoft Dynamics 365 for Talent -sovelluksen linkin avulla.</span><span class="sxs-lookup"><span data-stu-id="383f1-104">If you’ve created any Microsoft PowerApps, you can start those applications from links within Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="383f1-105">Voit määrittää sovellusten käyttöoikeuden, kun olet määrittänyt tietyt tiedot Talent-sovelluksen määrityssivulla. Voit avata sivun **Järjestelmän hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="383f1-105">To set up access to your applications, you’ll need to set up some information in Talent on a configuration page that you can open from the **System administration** workspace.</span></span>

## <a name="configuring-embedded-powerapps-within-talent"></a><span data-ttu-id="383f1-106">Upotetun PowerApps-sovelluksen määrittäminen Talent-sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="383f1-106">Configuring embedded PowerApps within Talent</span></span>
<span data-ttu-id="383f1-107">Määritä Talent-sivut **Upotetun Microsoft PowerApps -sovelluksen määrittäminen** -sivulla ja aloita PowerApps-sovellusten käyttäminen.</span><span class="sxs-lookup"><span data-stu-id="383f1-107">Use the **Set embedded Microsoft PowerApps** page to configure Talent pages to start PowerApps applications.</span></span> <span data-ttu-id="383f1-108">Kun haluat avata **Upotetun Microsoft PowerApps -sovelluksen määrittäminen** -sivun, avaa **Järjestelmän hallinta** -työtila ja avaa sitten **Linkit**-välilehti. Valitse **Asetukset**-ryhmässä **Microsoft PowerApps**.</span><span class="sxs-lookup"><span data-stu-id="383f1-108">To open the **Set embedded Microsoft PowerApps** page, open the **System administration** workspace and then open the **Links** tab. Select **Microsoft PowerApps** from the **Setup** group.</span></span> 

<span data-ttu-id="383f1-109">Sivulla annetaan tai määritetään seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="383f1-109">The following information is entered or set on this page:</span></span> 

> - <span data-ttu-id="383f1-110">Kunkin PowerApps-sovelluksen kuvaava nimi tai tunnus.</span><span class="sxs-lookup"><span data-stu-id="383f1-110">A descriptive name or identifier for each PowerApps application.</span></span>
> - <span data-ttu-id="383f1-111">Kunkin Talent-sivulle lisättävän sovellusten yksilövä tunnus (GUID).</span><span class="sxs-lookup"><span data-stu-id="383f1-111">A unique identifier (GUID) for each application that you add to a Talent page.</span></span> <span data-ttu-id="383f1-112">Sovelluksen tunnus on PowerApps-sivustossa osoitteessa [powerapps.com](http://powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="383f1-112">The app ID is available on the PowerApps site, [powerapps.com](http://powerapps.com/).</span></span> 
> - <span data-ttu-id="383f1-113">Sivu, jonka avulla käyttävät voivat avata sovelluksen tai raportin.</span><span class="sxs-lookup"><span data-stu-id="383f1-113">The page from which users can open an application or report.</span></span> <span data-ttu-id="383f1-114">Kaikki Talent-sivut eivät tue upotettuja PowerApps-sovelluksia ja Power BI -raportteja.</span><span class="sxs-lookup"><span data-stu-id="383f1-114">Not all Talent pages support embedded PowerApps and Power BI reports.</span></span> 

 > [!NOTE]
 >  <span data-ttu-id="383f1-115">Anna sivun sisäinen nimi sivun yläosassa olevan näyttönimen sijaan.</span><span class="sxs-lookup"><span data-stu-id="383f1-115">Enter the internal name of the page, rather than the display name that appears at the top of the page.</span></span> <span data-ttu-id="383f1-116">Löydät sisäisen nimen avaamalla sivun, jonka sisäistä nimeä etsit, ja napsauttamalla hiiren kakkospainikkeella mitä tahansa sivun kohtaa.</span><span class="sxs-lookup"><span data-stu-id="383f1-116">To find the internal name, open the page that you need the internal name of, and right-click anywhere on the page.</span></span> <span data-ttu-id="383f1-117">Kun valikko avautuu, valitse **Lomaketiedot**-kohta osoittamalla sitä.</span><span class="sxs-lookup"><span data-stu-id="383f1-117">When the menu opens, hover over the **Form information** item.</span></span> <span data-ttu-id="383f1-118">Sisäisen lomakkeen nimi näkyy valikon **Lomaketiedot**-kohdan vieressä.</span><span class="sxs-lookup"><span data-stu-id="383f1-118">The internal form name is displayed next to the **Form information** item in the menu.</span></span>
 
> - <span data-ttu-id="383f1-119">Määritä lomakkeen ohjausobjekti, josta sovellus voi hakee kontekstitiedot.</span><span class="sxs-lookup"><span data-stu-id="383f1-119">Specify the form control from which the application can retrieve context data.</span></span> <span data-ttu-id="383f1-120">Sovelluksessa voidaan käyttää esimerkiksi työntekijää koskevia tietoja.</span><span class="sxs-lookup"><span data-stu-id="383f1-120">For example, an application might use data about a worker.</span></span> <span data-ttu-id="383f1-121">Jos syötät **Konteksti**-kenttään **Työntekijä**-sivun, sovelluksen käynnistyessä avautuu **Työntekijä**-sivu.</span><span class="sxs-lookup"><span data-stu-id="383f1-121">If you enter the **Worker** page in the **Context** field, the **Worker** page will open when you start the application.</span></span> <span data-ttu-id="383f1-122">**Konteksti-kenttään** ei ole pakko syöttää tietoja.</span><span class="sxs-lookup"><span data-stu-id="383f1-122">An entry in the **Context field** is optional.</span></span> 
> - <span data-ttu-id="383f1-123">Määritä sen valintaikkunan koko, jossa PowerApps-sovellus suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="383f1-123">Set the size of the dialog box on which the PowerApps application will run.</span></span> <span data-ttu-id="383f1-124">Valintaikkunoiden koko on määritetty pieneksi tai suureksi sovelluksen puhelimen tai suuremman laitteen käyttöliittymässä suorittamisen optimoimista varten.</span><span class="sxs-lookup"><span data-stu-id="383f1-124">The dialog boxes are designated as “small” or “large” to optimize the user interface when your application for running on a phone or a larger device, respectively.</span></span> 

<span data-ttu-id="383f1-125">Voit määrittää myös oikeushenkilöt, joiden käytettävissä sovellus on, tai määrittää sovelluksen kaikkien oikeushenkilöiden käyttöön.</span><span class="sxs-lookup"><span data-stu-id="383f1-125">You can also specify which legal entities an application will be available for, or you can make it available to all your legal entities.</span></span> <span data-ttu-id="383f1-126">Oletusarvoisesti PowerApps-sovellukset ovat kaikkien oikeushenkilöiden käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="383f1-126">By default, your PowerApps applications are available to all legal entities.</span></span>

## <a name="opening-an-application"></a><span data-ttu-id="383f1-127">Sovelluksen avaaminen</span><span class="sxs-lookup"><span data-stu-id="383f1-127">Opening an application</span></span>
<span data-ttu-id="383f1-128">Kun upotetut PowerApps-sovellukset on määritetty, Talent-sovelluksen sivuille lisätään määrittämiesi sovellusten linkit.</span><span class="sxs-lookup"><span data-stu-id="383f1-128">When you’ve configured embedded PowerApps applications, links to the applications that you specified will be added to the pages within Talent.</span></span> <span data-ttu-id="383f1-129">Valitse linkki, kun haluat avata sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="383f1-129">Click a link to open an application.</span></span> 



