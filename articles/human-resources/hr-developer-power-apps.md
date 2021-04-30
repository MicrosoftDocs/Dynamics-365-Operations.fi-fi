---
title: Talentin laajentaminen Power Appsin ja Power Automaten avulla
description: Tämä artikkeli käsittelee Microsoft Power Appsia ja Microsoft Power Automate'ta käyttäviä Microsoft Dynamics 365 Human Resourcesin laajennusesimerkkejä.
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b5032c0996ef0dfb80a129deb32b4526794ca228
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892150"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="8717d-103">Laajentaminen Power Appsin ja Power Automaten avulla</span><span class="sxs-lookup"><span data-stu-id="8717d-103">Extend with Power Apps and Power Automate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8717d-104">Tämä artikkeli käsittelee Microsoft Power Appsia ja Microsoft Power Automate'ta käyttäviä Microsoft Dynamics 365 Human Resourcesin laajennusesimerkkejä.</span><span class="sxs-lookup"><span data-stu-id="8717d-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="8717d-105">Voit tuoda kumpaankin esimerkkiin liitetyt ratkaisupaketin Power Apps-ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="8717d-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="8717d-106">Voit sitten käyttää paketteja joka ohjeena tai lähtökohtana, jonka avulla toteutat organisaatioon sopivia skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="8717d-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8717d-107">Jos haluat käyttää tässä ohjeaiheessa kuvattuja malleja ja sovelluksia sellaisenaan, varmista testaamalla, että ne kattavat kaikki toteutukseen kuuluvat skenaariot.</span><span class="sxs-lookup"><span data-stu-id="8717d-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8717d-108">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="8717d-108">Prerequisites</span></span>

- <span data-ttu-id="8717d-109">Pakettien tuontia varten käyttäjät tarvitsevat **Ympäristön tekijä** -käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="8717d-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="8717d-110">Sovellusten vientiä ja tuontia varten käyttäjillä on oltava Power Apps-palvelupaketin 2 käyttöoikeus tai Power Apps -palvelupaketin 2 kokeiluversion käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="8717d-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-microsoft-365-power-automate"></a><span data-ttu-id="8717d-111">Microsoft 365 -integrointi, Power Automate</span><span class="sxs-lookup"><span data-stu-id="8717d-111">Integration with Microsoft 365, Power Automate</span></span>

<span data-ttu-id="8717d-112">**Microsoft 365 -integrointi** -sovelluksella voi purkaa kirjautuneiden käyttäjien tiimitiedot Microsoft 365:stä.</span><span class="sxs-lookup"><span data-stu-id="8717d-112">The **Integration with Microsoft 365** app can be used to extract team information for signed-in users from Microsoft 365.</span></span> <span data-ttu-id="8717d-113">Siinä viitataan henkilöstöhallinnon työntekijöihin, jotta työntekijöiden tunnistetyypit voidaan poimia.</span><span class="sxs-lookup"><span data-stu-id="8717d-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="8717d-114">Esimiehet voivat tarkistaa työntekijän tunnustyyppien vanhentumispäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="8717d-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="8717d-115">He voivat myös lähettää sähköpostimuistutuksen, jos työntekijätunnuksen tyyppi on umpeutumassa.</span><span class="sxs-lookup"><span data-stu-id="8717d-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="8717d-116">Power Automate integroituu Power Appsin kanssa tämän muistutuksen lähettämiseen.</span><span class="sxs-lookup"><span data-stu-id="8717d-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="8717d-117">Vahvistus lähetetään takaisin Power Appsiin Power Automatesta, kun muistutus lähetetään.</span><span class="sxs-lookup"><span data-stu-id="8717d-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="8717d-118">Tunnustyyppejä ovat ajokortti, passi ja muut hyväksyttävät henkilöllisyystodistusmuodot.</span><span class="sxs-lookup"><span data-stu-id="8717d-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="8717d-119">Voit laajentaa tätä sovellusta muihin tilanteisiin.</span><span class="sxs-lookup"><span data-stu-id="8717d-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="8717d-120">Voit käyttää sitä esimerkiksi näyttämään ryhmän lomatiedot, kalenteritapahtumat ja kaikki ryhmäkohtaiset tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="8717d-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="8717d-121">Voit ladata **Microsoft 365 -integrointi, Power Automate** -sovelluksen Microsoft Download Centerin kohdasta [Microsoft 365 -integrointi](https://go.microsoft.com/fwlink/?linkid=2081787).</span><span class="sxs-lookup"><span data-stu-id="8717d-121">To download the **Integration with Microsoft 365, Power Automate** app, go to [Integration with Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="8717d-122">Power Automate – SQL-yhteys ja toteutus</span><span class="sxs-lookup"><span data-stu-id="8717d-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="8717d-123">**Power Automate – SQL-yhteys ja toteutus** -malli muodostaa yhteyden Microsoft SQL Serveriin ja mahdollistaa SQL-kyselyjen suorittamisen.</span><span class="sxs-lookup"><span data-stu-id="8717d-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="8717d-124">Vaikka tämä malli lukee ja päivittää SQL-tauluja, voit laajentaa ja käyttää sitä muissa skenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="8717d-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="8717d-125">Sen avulla voit esimerkiksi täyttää valmistelutaulu Dataversessä SQL Serverin tietueilla sekä synkronoida valmistelutaulu säännöllisesti käyttämällä SQL Serverin lisäävää työntöä.</span><span class="sxs-lookup"><span data-stu-id="8717d-125">For example, you can use it to fill a staging table in Dataverse with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="8717d-126">Edistynyt kysely on integroitu virtauksen kanssa, jotta tietojen muuntaminen ja lisäävä työntö voidaan ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="8717d-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="8717d-127">Voit ladata **Power Automate – SQL-yhteys ja toteutus** -mallin Microsoft Download Centerin kohdassa [Power Automate – SQL-yhteys ja toteutus](https://go.microsoft.com/fwlink/?linkid=2081789).</span><span class="sxs-lookup"><span data-stu-id="8717d-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8717d-128">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8717d-128">Additional resources</span></span>

[<span data-ttu-id="8717d-129">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="8717d-129">The Microsoft Power Platform</span></span>](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]