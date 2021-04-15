---
title: Käyttöönoton usein kysytyt kysymykset
description: Tässä ohjeaiheessa on usein kysyttyjä kysymyksiä Dynamics 365 Human Resourcesin toteutusprojektin käyttöönotosta
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4a06da220fd90de91fb9091c41f35a1fb95442c3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804014"
---
# <a name="go-live-faq"></a><span data-ttu-id="f8263-103">Käyttöönoton usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="f8263-103">Go-live FAQ</span></span> 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f8263-104">Tässä ohjeaiheessa on usein kysyttyjä kysymyksiä Dynamics 365 Human Resourcesin toteutusprojektin käyttöönotosta</span><span class="sxs-lookup"><span data-stu-id="f8263-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="f8263-105">Milloin tuotantoympäristö voidaan määrittää ja pyytää?</span><span class="sxs-lookup"><span data-stu-id="f8263-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="f8263-106">Tuotantoympäristö otetaan yleensä käyttöön, kun seuraavat ehdot täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="f8263-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="f8263-107">Kaikkien mukautusten koodi on valmis.</span><span class="sxs-lookup"><span data-stu-id="f8263-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="f8263-108">Käyttäjän hyväksyntätestaus on valmis.</span><span class="sxs-lookup"><span data-stu-id="f8263-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="f8263-109">Asiakas on kuitannut ratkaisun.</span><span class="sxs-lookup"><span data-stu-id="f8263-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="f8263-110">Käyttöönoton estäviä ongelmia ei ole.</span><span class="sxs-lookup"><span data-stu-id="f8263-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="f8263-111">Jos tässä vaiheessa olevilla asiakkailla on oikeus Microsoft FastTrack -tiimin tukee, se tekee yhteistyössä projektiryhmän kanssa käyttöönottoarvioinnin.</span><span class="sxs-lookup"><span data-stu-id="f8263-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="f8263-112">Mitä edellytyksiä tuotantoympäristön käyttöönotolla on?</span><span class="sxs-lookup"><span data-stu-id="f8263-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="f8263-113">Edellytysluettelo on kohdassa [Käyttöönoton valmistelu](hr-admin-go-live-prepare.md).</span><span class="sxs-lookup"><span data-stu-id="f8263-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="f8263-114">Mitä käyttöönottoarviointi tarkoittaa?</span><span class="sxs-lookup"><span data-stu-id="f8263-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="f8263-115">Käyttöönottoarviointi sisältyy [Microsoft FastTrack -ohjelmaan](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span><span class="sxs-lookup"><span data-stu-id="f8263-115">The go-live assessment is part of the [Microsoft FastTrack program](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span></span> <span data-ttu-id="f8263-116">Arvioinnin aikana ratkaisuarkkitehti arvioi, onko toteutusprojekti niin valmis, että valmistelusiirto ja käyttöönotto onnistuvat.</span><span class="sxs-lookup"><span data-stu-id="f8263-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="f8263-117">Tämä arvio on tehtävä jokaisessa toteutusprojektissa, ja tuotantoympäristön käyttöönottoa voi pyytää vasta sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="f8263-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="f8263-118">Eristysympäristöt otetaan käyttöön Keski-Yhdysvaltojen palvelinkeskuksessa.</span><span class="sxs-lookup"><span data-stu-id="f8263-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="f8263-119">Tuotantoympäristöt halutaan sen sijaan ottaa käyttöön Länsi-Yhdysvaltojen palvelinkeskuksessa.</span><span class="sxs-lookup"><span data-stu-id="f8263-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="f8263-120">Onko Länsi-Yhdysvaltojen palvelinkeskuksen valinta tuotantomäärityksessä mahdollista?</span><span class="sxs-lookup"><span data-stu-id="f8263-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="f8263-121">LCS ei estä toisen palvelinkeskuksen valintaa, kun Human Resources -ympäristö otetaan käyttöön. Tätä ei kuitenkaan missään tapauksessa suositella.</span><span class="sxs-lookup"><span data-stu-id="f8263-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="f8263-122">Jos tuotantoympäristön halutaan olevan Länsi-Yhdysvaltojen palvelinkeskuksessa, eristysympäristöt on otettava ensin siirrettävä Länsi-Yhdysvaltojen palvelinkeskukseen, ja ne on testattava ja kuitattava siellä.</span><span class="sxs-lookup"><span data-stu-id="f8263-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="f8263-123">Lisätietoja oikean palvelinkeskuksen valitsemisesta on kohdassa [Verkon vaatimukset](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span><span class="sxs-lookup"><span data-stu-id="f8263-123">For information about selecting the correct datacenter, see [Network requirements](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="f8263-124">Minkälainen käyttöoikeustaso on Human Resources -ympäristöjen Azure-resursseissa?</span><span class="sxs-lookup"><span data-stu-id="f8263-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="f8263-125">Human Resources -ympäristöjen käyttöoikeudet ovat rajoitetut.</span><span class="sxs-lookup"><span data-stu-id="f8263-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="f8263-126">Virtuaalikoneen (VM) Microsoft Internet Information Servicesin (IIS) käyttö ei ole mahdollista.</span><span class="sxs-lookup"><span data-stu-id="f8263-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="f8263-127">Myöskään tietokantaa ei voi käyttää Microsoft SQL Server Management Studion kautta.</span><span class="sxs-lookup"><span data-stu-id="f8263-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="f8263-128">Vaikka Azure-resursseja tai Dynamics 365 Human Resources -ympäristöä ei voi käyttää suoraan, tietoja voi käyttää lisäominaisuuksilla.</span><span class="sxs-lookup"><span data-stu-id="f8263-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="f8263-129">Azure SQL -tietokanta voidaan ottaa käyttöön omassa Azure-vuokraajassa ja tiedot voidaan synkronoida BYOD (Bring Your Own Database) -ominaisuudella.</span><span class="sxs-lookup"><span data-stu-id="f8263-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="f8263-130">Lisätietoja on kohdassa [Oman tietokannan tuonti (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span><span class="sxs-lookup"><span data-stu-id="f8263-130">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span>

- <span data-ttu-id="f8263-131">Valittuja yksiköitä voi synkronoida Dataverse -tietokantaan Dataverse -integraation avulla.</span><span class="sxs-lookup"><span data-stu-id="f8263-131">You can use Dataverse integration to synchronize select entities into the Dataverse database.</span></span> <span data-ttu-id="f8263-132">Lisätietoja: [Dataverse-taulut](hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="f8263-132">For more information, see [Dataverse tables](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="f8263-133">Kuinka usein tuotantotietokanta varmuuskopioidaan?</span><span class="sxs-lookup"><span data-stu-id="f8263-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="f8263-134">Tietokannat suojataan automaattisilla varmuuskopioilla, jotka tehdään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="f8263-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="f8263-135">Varmuuskopion tyyppi</span><span class="sxs-lookup"><span data-stu-id="f8263-135">Type of backup</span></span> | <span data-ttu-id="f8263-136">Tiheys</span><span class="sxs-lookup"><span data-stu-id="f8263-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="f8263-137">Koko tietokannan varmuuskopio</span><span class="sxs-lookup"><span data-stu-id="f8263-137">Full database backup</span></span> | <span data-ttu-id="f8263-138">Viikoittain</span><span class="sxs-lookup"><span data-stu-id="f8263-138">Weekly</span></span> |
| <span data-ttu-id="f8263-139">Differentiaalisen tietokannan varmuuskopio</span><span class="sxs-lookup"><span data-stu-id="f8263-139">Differential database backup</span></span> | <span data-ttu-id="f8263-140">12–24 tunnin välein</span><span class="sxs-lookup"><span data-stu-id="f8263-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="f8263-141">Tapahtumalokin varmuuskopio</span><span class="sxs-lookup"><span data-stu-id="f8263-141">Transaction log backup</span></span> | <span data-ttu-id="f8263-142">5–10 minuutin välein</span><span class="sxs-lookup"><span data-stu-id="f8263-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="f8263-143">Microsoft säilyttää riittävät varmuuskopiot, jotta tiettyyn ajankohtaan palauttaminen onnistuu 14 päivän ajalta.</span><span class="sxs-lookup"><span data-stu-id="f8263-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last 14 days.</span></span> 

<span data-ttu-id="f8263-144">Lisätietoja on kohdassa  [Tietoja SQL-tietokannan automaattisista varmuuskopioinneista](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span><span class="sxs-lookup"><span data-stu-id="f8263-144">For more information, see [Learn about automatic SQL Database backups](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="f8263-145">Voiko tuotantotietokannan varmuuskopion kopiota pyytää?</span><span class="sxs-lookup"><span data-stu-id="f8263-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="f8263-146">Nro</span><span class="sxs-lookup"><span data-stu-id="f8263-146">No.</span></span> <span data-ttu-id="f8263-147">Sen sijaan voidaan lähettää tietokannan päivityspalvelupyyntö tuotantoympäristön kopioinnista eristysympäristöön.</span><span class="sxs-lookup"><span data-stu-id="f8263-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="f8263-148">Azure SQL -tietokanta voidaan ottaa käyttöön omassa Azure-vuokraajassa ja tiedot voidaan synkronoida BYOD-ominaisuudella tuotantoympäristöstä.</span><span class="sxs-lookup"><span data-stu-id="f8263-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="f8263-149">Lisätietoja on kohdassa [Oman tietokannan tuonti (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span><span class="sxs-lookup"><span data-stu-id="f8263-149">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="f8263-150">Miten eristysympäristön siirretään tuotantoympäristöön käyttöönottoa varten?</span><span class="sxs-lookup"><span data-stu-id="f8263-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="f8263-151">Koska ympäristöä ei voi siirtää eristysympäristöstä tuotantoympäristöön kopiointiominaisuudella, tiedot on siirrettävä tuotantoympäristöön tietopakettien avulla.</span><span class="sxs-lookup"><span data-stu-id="f8263-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="f8263-152">Projektin aikana kannattaa ylläpitää selkeää luetteloa eristysympäristössä määritetyistä yksiköistä.</span><span class="sxs-lookup"><span data-stu-id="f8263-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="f8263-153">Tämän jälkeen testataan käyttöönottoon tarvittavien tietopakettien valmistelusiirtoprosessia ja siirtoa.</span><span class="sxs-lookup"><span data-stu-id="f8263-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="f8263-154">Mahdolliset tietopaketit on siirrettävä manuaalisesti tuotantoympäristöön, kun käyttöönottoon ollaan valmiita.</span><span class="sxs-lookup"><span data-stu-id="f8263-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="f8263-155">Miten toimitaan, jos tuotantoympäristö ei ole käytettävissä?</span><span class="sxs-lookup"><span data-stu-id="f8263-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="f8263-156">Lisätietoja tuotannon käyttökatkoksen ilmoittamisprosessista on kohdassa [Tuotantokatkoksesta ilmoittaminen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span><span class="sxs-lookup"><span data-stu-id="f8263-156">To report a Production outage, follow the process described in [Report a production outage](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="f8263-157">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="f8263-157">See also</span></span>

 [<span data-ttu-id="f8263-158">Käyttöönoton valmistelu</span><span class="sxs-lookup"><span data-stu-id="f8263-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]