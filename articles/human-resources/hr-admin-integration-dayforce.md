---
title: Dayforceen integroinnin määritys
description: Microsoft Dynamics 365 Human Resourcesin ja Ceridian Dayforcen välinen integrointi käyttää useita konfiguraation vaiheita, jotka on kuvattu tässä artikkelissa. Sekä Human Resourcesin että Dayforcen integrointi on määritettävä ennen kuin voit käsitellä palkka-ajoa.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85e7274b0e9c130e5c3426fd1fff98410f93e49a
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008838"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="1fad9-104">Dayforceen integroinnin määritys</span><span class="sxs-lookup"><span data-stu-id="1fad9-104">Configure integration with Dayforce</span></span>

<span data-ttu-id="1fad9-105">Microsoft Dynamics 365 Human Resourcesin ja Ceridian Dayforcen välinen integrointi käyttää useita konfiguraation vaiheita, jotka on kuvattu tässä artikkelissa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="1fad9-106">Sekä Human Resourcesin että Dayforcen integrointi on määritettävä ennen kuin voit käsitellä palkka-ajoa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="1fad9-107">Käytettäessä jotakin palvelua, kuten Dayforcea palkka-ajojen suorittamiseen, on otettava käyttöön integrointi Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="1fad9-108">Integrointi edellyttää tiettyjä tietoja Human Resourcesista.</span><span class="sxs-lookup"><span data-stu-id="1fad9-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="1fad9-109">Sinun on varmistettava, että Dayforceen yhdistetyt tiedot on konfiguroitu Human Resourcesissa siten, että ne tukevat integrointia.</span><span class="sxs-lookup"><span data-stu-id="1fad9-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="1fad9-110">Integraatio käyttää seuraavanlaisia laajoja tietoryhmiä:</span><span class="sxs-lookup"><span data-stu-id="1fad9-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="1fad9-111">Henkilöstöhallintotiedot</span><span class="sxs-lookup"><span data-stu-id="1fad9-111">Human resources data</span></span>
- <span data-ttu-id="1fad9-112">Kompensaatiotiedot</span><span class="sxs-lookup"><span data-stu-id="1fad9-112">Compensation data</span></span>
- <span data-ttu-id="1fad9-113">Palkanlaskentatietoja, kuten maksujaksot, maksukaudet ja ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="1fad9-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="1fad9-114">Työntekijän tiedot</span><span class="sxs-lookup"><span data-stu-id="1fad9-114">Worker data</span></span>

<span data-ttu-id="1fad9-115">Tässä artikkelissa kuvataan vaiheita, joita sinun on noudatettava ottaaksesi integroinnin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="1fad9-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="1fad9-116">Lisäksi kerrotaan minkä tyyppisiä tietoja ja konfigurointitietoja integrointi edellyttää.</span><span class="sxs-lookup"><span data-stu-id="1fad9-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="1fad9-117">Ota integraatio käyttöön</span><span class="sxs-lookup"><span data-stu-id="1fad9-117">Enable the integration</span></span>

<span data-ttu-id="1fad9-118">Ota integraatio käyttöön Human Resourcesissa ja lisää konfiguraatiotiedot muodostaaksesi yhteyden Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="1fad9-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="1fad9-119">Mikäli haluat kirjanpitotapahtuman, joka valmistetaan ja tuodaan Microsoft Dynamics 365 Financeen, sinun on määritettävä myös Microsoft Azure -tallennustili ja kirjoitettava Azure-tallennuksen yhteyden muodostuskomento Financeen.</span><span class="sxs-lookup"><span data-stu-id="1fad9-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="1fad9-120">Ota integrointi käyttöön Human Resourcesissa seuraavien vaiheiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="1fad9-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="1fad9-121">Valitse **Järjestelmänvalvoja**-sivulla **konfiguroinnin integrointi**.</span><span class="sxs-lookup"><span data-stu-id="1fad9-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="1fad9-122">Lisää File Transfer Protocol (FTP) -päätepiste ja suojattu FTP-kansiopolku.</span><span class="sxs-lookup"><span data-stu-id="1fad9-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="1fad9-123">Kirjoita sen käyttäjän käyttäjänimi ja salasana, joka voi käyttää suojattua FTP-päätepistettä ja kansiopolkua.</span><span class="sxs-lookup"><span data-stu-id="1fad9-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="1fad9-124">Testaa yhteys kuten vaadittu ja määritä **Ota käyttöön palkanmaksun integrointi** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="1fad9-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="1fad9-125">Kun integrointi otetaan käyttöön, tietojen viennin paketti ja tiedostot luodaan ja taajuus määritetään.</span><span class="sxs-lookup"><span data-stu-id="1fad9-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="1fad9-126">Voit muuttaa tätä taajuutta tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="1fad9-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="1fad9-127">Lisätietoja Azure-tallennustilien ja Azure-tallennusyhteyden yhteysmerkkijonoista seuraavissa Azure-artikkeleissa:</span><span class="sxs-lookup"><span data-stu-id="1fad9-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="1fad9-128">Lisätietoja Azure-tallennustileistä</span><span class="sxs-lookup"><span data-stu-id="1fad9-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="1fad9-129">Määritä Azure-tallennustilan yhteysmerkkijonot</span><span class="sxs-lookup"><span data-stu-id="1fad9-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="1fad9-130">Tekniset tiedot, kun palkanlaskennan integrointi on otettu käyttöön</span><span class="sxs-lookup"><span data-stu-id="1fad9-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="1fad9-131">Palkanlaskennan integroinnin käytöstäpoistamisella on kaksi pääasiallista vaikutusta:</span><span class="sxs-lookup"><span data-stu-id="1fad9-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="1fad9-132">Palkanlaskennan integroinnin vienti -niminen tietojen vientiprojekti luodaan.</span><span class="sxs-lookup"><span data-stu-id="1fad9-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="1fad9-133">Tämä projekti sisältää palkanhallinnan integrointiin tarvittavat yksiköt ja kentät.</span><span class="sxs-lookup"><span data-stu-id="1fad9-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="1fad9-134">Voit tutustua projektiin valitsemalla ensin **Järjestelmän hallinta**, sitten **Tietojen hallinta** -ruudun ja avaamalla lopuksi tietoprojektin projektiluettelosta.</span><span class="sxs-lookup"><span data-stu-id="1fad9-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="1fad9-135">Tämä erätyö suorittaa tietojen vientiprojektin, salaa tuloksena olevan tietopaketin ja siirtää tietopakettitiedoston SFTP-päätepisteeseen, joka on määritetty **Integroinnin määritys** -näytössä.</span><span class="sxs-lookup"><span data-stu-id="1fad9-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="1fad9-136">SFTP-päätepisteeseen siirretty tietopaketti salataan paketin yksilöllisellä avaimella.</span><span class="sxs-lookup"><span data-stu-id="1fad9-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="1fad9-137">Avain on Azure Key Vaultissa, jota vain Ceridian voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="1fad9-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="1fad9-138">Tietopaketin sisällön salausta ei voi purkaa eikä sisältöä tutkia.</span><span class="sxs-lookup"><span data-stu-id="1fad9-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="1fad9-139">Jos tietopaketin sisältöä on tarkasteltava, Palkanlaskennan integroinnin vienti -tietoprojekti on vietävä manuaalisesti, jonka jälkeen on ladattava ja avattava.</span><span class="sxs-lookup"><span data-stu-id="1fad9-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="1fad9-140">Manuaalisessa viennissä ei käytetä salausta eikä pakettia siirretä.</span><span class="sxs-lookup"><span data-stu-id="1fad9-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="1fad9-141">Määritä tietosi</span><span class="sxs-lookup"><span data-stu-id="1fad9-141">Configure your data</span></span> 

<span data-ttu-id="1fad9-142">Voidaksesi käsitellä palkanlaskentaa, sinun on määritettävä henkilöstöhallinnon tiedot Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="1fad9-143">On määritettävä organisaation tiedot, kuten työt ja toimet sekä edut ja kompensaatiotiedot.</span><span class="sxs-lookup"><span data-stu-id="1fad9-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="1fad9-144">Nämä tiedot sisältävät työllisyys-, palkka- ja vähennystiedot, jotka vaaditaan, jotta voidaan luoda työntekijän palkka.</span><span class="sxs-lookup"><span data-stu-id="1fad9-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="1fad9-145">Henkilöstöhallintotiedot</span><span class="sxs-lookup"><span data-stu-id="1fad9-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="1fad9-146">Edut</span><span class="sxs-lookup"><span data-stu-id="1fad9-146">Benefits</span></span> 

<span data-ttu-id="1fad9-147">Henkilöstöhallinto sisältää työkaluja, joiden avulla organisaation tarjoamia tai työntekijöitä varten käsittelemiä etuja, vähennyksiä ja työntekijöiden kompensaatiosuunnitelmia voi määrittää ja ylläpitää.</span><span class="sxs-lookup"><span data-stu-id="1fad9-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="1fad9-148">Luodessasi etuja, pidä mielessä seuraavat tiedot ja konfiguraatiot, joita käytetään Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="1fad9-149">Etusuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="1fad9-149">Benefit plans</span></span>

- <span data-ttu-id="1fad9-150">Suunnitelma (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-150">Plan (required)</span></span>
- <span data-ttu-id="1fad9-151">Tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-151">Type (required)</span></span>
- <span data-ttu-id="1fad9-152">Palkanlaskennan vaikutus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-152">Payroll impact (required)</span></span>
- <span data-ttu-id="1fad9-153">Palauta velvoitteet</span><span class="sxs-lookup"><span data-stu-id="1fad9-153">Recover arrears</span></span>
- <span data-ttu-id="1fad9-154">Vähennysmenetelmä</span><span class="sxs-lookup"><span data-stu-id="1fad9-154">Deduction method</span></span>
- <span data-ttu-id="1fad9-155">Vähennyksen prioriteetti</span><span class="sxs-lookup"><span data-stu-id="1fad9-155">Deduction priority</span></span>
- <span data-ttu-id="1fad9-156">Rajaa kausi</span><span class="sxs-lookup"><span data-stu-id="1fad9-156">Limit period</span></span>
- <span data-ttu-id="1fad9-157">Rajasumma</span><span class="sxs-lookup"><span data-stu-id="1fad9-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="1fad9-158">Edut</span><span class="sxs-lookup"><span data-stu-id="1fad9-158">Benefits</span></span>

- <span data-ttu-id="1fad9-159">Suunnitelma (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-159">Plan (required)</span></span>
- <span data-ttu-id="1fad9-160">Tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-160">Type (required)</span></span>
- <span data-ttu-id="1fad9-161">Vaihtoehto (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-161">Option (required)</span></span>
- <span data-ttu-id="1fad9-162">Edun tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-162">Benefit ID (required)</span></span>
- <span data-ttu-id="1fad9-163">Tiheys</span><span class="sxs-lookup"><span data-stu-id="1fad9-163">Frequency</span></span>
- <span data-ttu-id="1fad9-164">Peruste</span><span class="sxs-lookup"><span data-stu-id="1fad9-164">Basis</span></span>
- <span data-ttu-id="1fad9-165">Summa tai hinta</span><span class="sxs-lookup"><span data-stu-id="1fad9-165">Amount or rate</span></span>
- <span data-ttu-id="1fad9-166">Ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="1fad9-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="1fad9-167">Tuetut maksutiheydet</span><span class="sxs-lookup"><span data-stu-id="1fad9-167">Supported frequencies</span></span> 

- <span data-ttu-id="1fad9-168">Viikoittain</span><span class="sxs-lookup"><span data-stu-id="1fad9-168">Weekly</span></span>
- <span data-ttu-id="1fad9-169">Kahden viikon välein</span><span class="sxs-lookup"><span data-stu-id="1fad9-169">Bi-weekly</span></span>
- <span data-ttu-id="1fad9-170">Joka toinen kuukausi</span><span class="sxs-lookup"><span data-stu-id="1fad9-170">Semi-monthly</span></span>
- <span data-ttu-id="1fad9-171">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="1fad9-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="1fad9-172">Tuetut pohjat</span><span class="sxs-lookup"><span data-stu-id="1fad9-172">Supported bases</span></span> 

- <span data-ttu-id="1fad9-173">Kiinteä summa</span><span class="sxs-lookup"><span data-stu-id="1fad9-173">Fixed amount</span></span>
- <span data-ttu-id="1fad9-174">Ansioiden prosenttiosuus</span><span class="sxs-lookup"><span data-stu-id="1fad9-174">Percent of earnings</span></span>
- <span data-ttu-id="1fad9-175">Tuottavat tunnit</span><span class="sxs-lookup"><span data-stu-id="1fad9-175">Productive hours</span></span>

<span data-ttu-id="1fad9-176">Dayforce luo seuraavat vähennykset, jotka perustuvat palkanlaskennan vaikutukseen, joka on määritelty etusuunnitelmassa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="1fad9-177">Valinta Human Resourcesissa</span><span class="sxs-lookup"><span data-stu-id="1fad9-177">Selection in Human Resources</span></span>        | <span data-ttu-id="1fad9-178">Tulos Dayforcessa</span><span class="sxs-lookup"><span data-stu-id="1fad9-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="1fad9-179">Ei ole</span><span class="sxs-lookup"><span data-stu-id="1fad9-179">None</span></span>                       | <span data-ttu-id="1fad9-180">Vähennyksiä ei luoda.</span><span class="sxs-lookup"><span data-stu-id="1fad9-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="1fad9-181">Vain vähennys</span><span class="sxs-lookup"><span data-stu-id="1fad9-181">Deduction only</span></span>             | <span data-ttu-id="1fad9-182">Työntekijävähennys on luotu.</span><span class="sxs-lookup"><span data-stu-id="1fad9-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="1fad9-183">Vain osuus</span><span class="sxs-lookup"><span data-stu-id="1fad9-183">Contribution only</span></span>          | <span data-ttu-id="1fad9-184">Työnantajavähennys on luotu.</span><span class="sxs-lookup"><span data-stu-id="1fad9-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="1fad9-185">Vähennys ja osuus</span><span class="sxs-lookup"><span data-stu-id="1fad9-185">Deduction and contribution</span></span> | <span data-ttu-id="1fad9-186">Työntekijän ja työnantajan vähennykset luodaan.</span><span class="sxs-lookup"><span data-stu-id="1fad9-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="1fad9-187">Lisätietoja etuohjelman määrittämisestä ja hallitsemisesta seuraavissa artikkeleissa:</span><span class="sxs-lookup"><span data-stu-id="1fad9-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="1fad9-188">Työsuhde-etuusohjelman toteuttaminen</span><span class="sxs-lookup"><span data-stu-id="1fad9-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="1fad9-189">Luo uusi etu</span><span class="sxs-lookup"><span data-stu-id="1fad9-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="1fad9-190">Määritä edun oikeutussäännöt ja -käytännöt</span><span class="sxs-lookup"><span data-stu-id="1fad9-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="1fad9-191">Rekisteröi etuja työntekijöille ja poista niitä</span><span class="sxs-lookup"><span data-stu-id="1fad9-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="1fad9-192">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="1fad9-192">Compensation</span></span> 

<span data-ttu-id="1fad9-193">Kompensaationhallinnan avulla ohjataan peruspalkan ja palkkioiden maksamista.</span><span class="sxs-lookup"><span data-stu-id="1fad9-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="1fad9-194">Työntekijän kiinteän peruspalkan ja bonusten korotuksia hallitaan kiinteän kompensaatiosuunnitelmien avulla.</span><span class="sxs-lookup"><span data-stu-id="1fad9-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="1fad9-195">Bonusmaksujen, suorituskykypalkkioiden, optioiden, lahjoitusten sekä muiden kannusteiden maksamista hallitaan muuttuvan kompensaation suunnitelmien avulla.</span><span class="sxs-lookup"><span data-stu-id="1fad9-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="1fad9-196">Dayforce käyttää kompensaatiotietoja laskeakseen työntekijän tunti- tai vuosihinnan.</span><span class="sxs-lookup"><span data-stu-id="1fad9-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="1fad9-197">Kiinteät kompensaatiosuunnitelmat ja palkkojen muunnokset vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="1fad9-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="1fad9-198">Työntekijöiden täytyy olla liitettynä kiinteään kompensaatiosuunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="1fad9-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="1fad9-199">Katso lisätietoja kompensaatiosuunnitelmista seuraavista artikkeleista:</span><span class="sxs-lookup"><span data-stu-id="1fad9-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="1fad9-200">Kiinteiden kompensaatiosuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="1fad9-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="1fad9-201">Muuttuvien kompensaatiosuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="1fad9-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="1fad9-202">Palkka- ja kompensaatiorakenteen ja -suunnitelmien kehittäminen</span><span class="sxs-lookup"><span data-stu-id="1fad9-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="1fad9-203">Kompensaation käsittely</span><span class="sxs-lookup"><span data-stu-id="1fad9-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="1fad9-204">Kompensaatioprosessin määrittäminen ja tulosten laskeminen</span><span class="sxs-lookup"><span data-stu-id="1fad9-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="1fad9-205">Työntekijän rekisteröiminen kiinteän kompensaation suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="1fad9-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="1fad9-206">Työntekijän rekisteröiminen muuttuvan kompensaation suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="1fad9-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="1fad9-207">Työt</span><span class="sxs-lookup"><span data-stu-id="1fad9-207">Jobs</span></span> 

<span data-ttu-id="1fad9-208">Työ sisältää tehtäviä ja vastuita, joita työn suorittajalta edellytetään.</span><span class="sxs-lookup"><span data-stu-id="1fad9-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="1fad9-209">Lisätietoja on seuraavissa artikkeleissa:</span><span class="sxs-lookup"><span data-stu-id="1fad9-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="1fad9-210">Työn komponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1fad9-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="1fad9-211">Uusien töiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1fad9-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="1fad9-212">Toimet</span><span class="sxs-lookup"><span data-stu-id="1fad9-212">Positions</span></span>

<span data-ttu-id="1fad9-213">Toimi on työn yksittäinen esiintymä.</span><span class="sxs-lookup"><span data-stu-id="1fad9-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="1fad9-214">Esimerkiksi toimi Myyntipäällikkö (Itä) on yksi Myyntipäällikkö-työhön liittyvistä toimista.</span><span class="sxs-lookup"><span data-stu-id="1fad9-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="1fad9-215">Osastolla on toimi.</span><span class="sxs-lookup"><span data-stu-id="1fad9-215">A position exists in a department.</span></span> <span data-ttu-id="1fad9-216">Vain yksi työntekijä voidaan liittää yhteen toimeen.</span><span class="sxs-lookup"><span data-stu-id="1fad9-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="1fad9-217">Muista seuraavat tiedot ja määritykset, kun määrität toimia:</span><span class="sxs-lookup"><span data-stu-id="1fad9-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="1fad9-218">Toimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-218">Position (required)</span></span>
- <span data-ttu-id="1fad9-219">Kuvaus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-219">Description (required)</span></span>
- <span data-ttu-id="1fad9-220">Työ (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-220">Job (required)</span></span>
- <span data-ttu-id="1fad9-221">Osasto (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-221">Department (required)</span></span>
- <span data-ttu-id="1fad9-222">Toimen tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-222">Position type (required)</span></span>
- <span data-ttu-id="1fad9-223">Kokopäiväinen (FTE)</span><span class="sxs-lookup"><span data-stu-id="1fad9-223">Full-time equivalent</span></span>
- <span data-ttu-id="1fad9-224">Vuosittaiset vakiotunnit (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="1fad9-225">Yrityksen maksama (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="1fad9-226">Maksujakson (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-226">Pay cycle (required)</span></span>
- <span data-ttu-id="1fad9-227">Oletusarvo taloushallinnon dimensio – kustannuspaikka (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="1fad9-228">Työntekijän määritys – työntekijä, tehtävän alkamisaika, tehtävän lopetusaika, syykoodi</span><span class="sxs-lookup"><span data-stu-id="1fad9-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="1fad9-229">Mikäli useita toimia samalla osastolla liittyy samaan työhön, ne yhdistetään yhteen toimeen Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="1fad9-230">Lisätietoja on seuraavissa artikkeleissa:</span><span class="sxs-lookup"><span data-stu-id="1fad9-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="1fad9-231">Työvoiman järjestäminen osastojen, töiden ja toimien avulla</span><span class="sxs-lookup"><span data-stu-id="1fad9-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="1fad9-232">Toimien määritys</span><span class="sxs-lookup"><span data-stu-id="1fad9-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="1fad9-233">Osastot</span><span class="sxs-lookup"><span data-stu-id="1fad9-233">Departments</span></span>

<span data-ttu-id="1fad9-234">Osasto on toimintayksikkö, joka vastaa organisaation luokkaa tai liiketoiminta-aluetta.</span><span class="sxs-lookup"><span data-stu-id="1fad9-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="1fad9-235">Osasto on vastuussa määrätystä organisaation alueesta, kuten myynnistä, kirjanpidosta tai henkilöstöhallinnosta.</span><span class="sxs-lookup"><span data-stu-id="1fad9-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="1fad9-236">Voit käyttää osastoja toiminnallisia alueita koskevaan raportointiin.</span><span class="sxs-lookup"><span data-stu-id="1fad9-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="1fad9-237">Osastot voivat olla tulosvastuullisia.</span><span class="sxs-lookup"><span data-stu-id="1fad9-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="1fad9-238">Lisätietoja on seuraavissa artikkeleissa:</span><span class="sxs-lookup"><span data-stu-id="1fad9-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="1fad9-239">Osaston luominen ja liittäminen osastohierarkiaan</span><span class="sxs-lookup"><span data-stu-id="1fad9-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="1fad9-240">Määritä uudet osastot</span><span class="sxs-lookup"><span data-stu-id="1fad9-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="1fad9-241">Maksujaksot ja maksukaudet</span><span class="sxs-lookup"><span data-stu-id="1fad9-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="1fad9-242">Palkkajakso määrittää kuinka usein palkkalistoja käytetään, ja minä tiettyinä päivinä työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="1fad9-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="1fad9-243">Esimerkiksi palkkajakso voi olla kuukausittainen ja työntekijöille voidaan maksaa kuukauden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="1fad9-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="1fad9-244">Vaihtoehtoisesti palkkajakso voi olla viikoittainen ja työntekijöille voidaan maksaa tiistaina palkkajakson päätyttyä.</span><span class="sxs-lookup"><span data-stu-id="1fad9-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="1fad9-245">Palkkajaksot on osoitettu toimiin, jotta voidaan valvoa milloin näissä tehtävissä oleville työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="1fad9-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="1fad9-246">Luotuasi palkkajaksoja, voit luoda maksukausia kullekin jaksolle.</span><span class="sxs-lookup"><span data-stu-id="1fad9-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="1fad9-247">Jokaisella palkkakaudella on maksun oletuspäivämäärä, joka perustuu antamiisi tietoihin.</span><span class="sxs-lookup"><span data-stu-id="1fad9-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="1fad9-248">Voit kuitenkin muokata maksun oletuspäivämäärää salliaksesi poikkeuksia, kuten kun maksupäivämäärä osuu vapaapäivälle.</span><span class="sxs-lookup"><span data-stu-id="1fad9-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="1fad9-249">Dayforcessa käytetään seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="1fad9-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="1fad9-250">Maksujakson (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-250">Pay cycle (required)</span></span>
- <span data-ttu-id="1fad9-251">Maksujakson tiheys (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="1fad9-252">Kauden alkamispäivä (ensimmäinen palkkakausi vaaditaan)</span><span class="sxs-lookup"><span data-stu-id="1fad9-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="1fad9-253">Oletusmaksupäivä (ensimmäinen palkkakausi vaaditaan)</span><span class="sxs-lookup"><span data-stu-id="1fad9-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="1fad9-254">Nämä tiedot on integroitu Dayforce-palkkaryhmien kanssa ja eriteltynä eriteltyinä maittain tai alueittain kullekin maksujaksolle.</span><span class="sxs-lookup"><span data-stu-id="1fad9-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="1fad9-255">Ennen integraatiota on luotava vähintään yksi palkkakausi.</span><span class="sxs-lookup"><span data-stu-id="1fad9-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="1fad9-256">Dayforce luo maksuryhmäkalentereita ja maksupäiviä, jotka perustuvat ensimmäisen palkkakauden alkamispäivämäärään ja määritetty oletusmaksupäivä on asetettu Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="1fad9-257">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="1fad9-257">Earning codes</span></span>

<span data-ttu-id="1fad9-258">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="1fad9-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="1fad9-259">Tunnuksissa on erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="1fad9-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="1fad9-260">Dayforcessa käytetään seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="1fad9-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="1fad9-261">Ansiokoodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-261">Earning Code (required)</span></span>
- <span data-ttu-id="1fad9-262">kuvaus</span><span class="sxs-lookup"><span data-stu-id="1fad9-262">Description</span></span>
- <span data-ttu-id="1fad9-263">Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="1fad9-263">Unit of measure</span></span>
- <span data-ttu-id="1fad9-264">Tuottava</span><span class="sxs-lookup"><span data-stu-id="1fad9-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="1fad9-265">Työntekijän tiedot</span><span class="sxs-lookup"><span data-stu-id="1fad9-265">Worker data</span></span>

<span data-ttu-id="1fad9-266">Tietueet eri työntekijöille, joita sinulla on ovat tärkeitä henkilöstöhallinnossa ja palkanlaskentajärjestelmissä.</span><span class="sxs-lookup"><span data-stu-id="1fad9-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="1fad9-267">Tietueisiin lisättäviä tietoja käytetään työntekijöiden ja henkilökohtaisten tietojen seurannassa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="1fad9-268">Voit ylläpitää työntekijöille seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="1fad9-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="1fad9-269">**Perustiedot** – Ylläpidä työntekijän perustietoja, kuten yhteystiedot, demografiatiedot, tunnistetiedot, perheen tiedot, asevelvollisuuden tila, ekspatriaatin tiedot ja omat yhteyshenkilöt ja hätäyhteyshenkilöt.</span><span class="sxs-lookup"><span data-stu-id="1fad9-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="1fad9-270">**Työsuhde** – Ylläpidä tietoja työntekijän työsuhteesta, kuten yrityksen tai organisaation kytköksistä, toimen määrityksestä, aloitus- ja päättymispäivämääristä, työkelpoisuudesta, työehdoista, eläkkestä, lomista ja uudelleensijoittumisesta.</span><span class="sxs-lookup"><span data-stu-id="1fad9-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="1fad9-271">**Lomat ja poissaolot** –Ylläpidä tietoa työntekijän poissaoloista, kuten työaikakalentereista, poissaolotapahtumista ja poissaoloasetuksista.</span><span class="sxs-lookup"><span data-stu-id="1fad9-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="1fad9-272">**Kompensaatio ja palkanlaskenta** – Ylläpidä työntekijän kompensaatiosuunnitelmien tietoja ja palkanlaskentatietoja, kuten suunnitelmien toteutuminen, palkkiot, suorituskyky, provisio, verotiedot, eläkkeelle jääminen ja palkan vähennykset.</span><span class="sxs-lookup"><span data-stu-id="1fad9-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="1fad9-273">Kirjoittaessasi työntekijätietoja, pidä mielessä seuraavat tiedot ja konfiguraatiot, joita käytetään Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="1fad9-274">Yleistiedot</span><span class="sxs-lookup"><span data-stu-id="1fad9-274">General information</span></span>

- <span data-ttu-id="1fad9-275">Henkilönumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-275">Personnel number (required)</span></span>
- <span data-ttu-id="1fad9-276">Etunimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-276">First name (required)</span></span>
- <span data-ttu-id="1fad9-277">Sukunimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-277">Last name (required)</span></span>
- <span data-ttu-id="1fad9-278">Toinen nimi</span><span class="sxs-lookup"><span data-stu-id="1fad9-278">Middle name</span></span>
- <span data-ttu-id="1fad9-279">Ikälisäpäivä</span><span class="sxs-lookup"><span data-stu-id="1fad9-279">Seniority date</span></span>
- <span data-ttu-id="1fad9-280">Tunnetaan nimellä</span><span class="sxs-lookup"><span data-stu-id="1fad9-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="1fad9-281">Henkilökohtaiset tiedot</span><span class="sxs-lookup"><span data-stu-id="1fad9-281">Personal information</span></span>

- <span data-ttu-id="1fad9-282">Siviilisääty (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-282">Marital status (required)</span></span>
- <span data-ttu-id="1fad9-283">Syntymäpäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-283">Birth date (required)</span></span>
- <span data-ttu-id="1fad9-284">Sukupuoli (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-284">Gender (required)</span></span>
- <span data-ttu-id="1fad9-285">Henkilö on invalidi</span><span class="sxs-lookup"><span data-stu-id="1fad9-285">Person with disabilities</span></span>
- <span data-ttu-id="1fad9-286">Kansalaisuus, maa, alue (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="1fad9-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="1fad9-287">Osoitetiedot</span><span class="sxs-lookup"><span data-stu-id="1fad9-287">Address information</span></span>

- <span data-ttu-id="1fad9-288">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-288">Primary (required)</span></span>
- <span data-ttu-id="1fad9-289">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-289">Country/region (required)</span></span>
- <span data-ttu-id="1fad9-290">Postinumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-290">Postal code (required)</span></span>
- <span data-ttu-id="1fad9-291">Kadunnumero (pakollinen) (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="1fad9-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="1fad9-292">Rakennusta koskeva lisätieto (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="1fad9-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="1fad9-293">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-293">City (required)</span></span>
- <span data-ttu-id="1fad9-294">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-294">State (required)</span></span>
- <span data-ttu-id="1fad9-295">Lääni (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="1fad9-296">Yhteystiedot</span><span class="sxs-lookup"><span data-stu-id="1fad9-296">Contact information</span></span> 

- <span data-ttu-id="1fad9-297">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-297">Primary (required)</span></span>
- <span data-ttu-id="1fad9-298">Yhteystiedon numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-298">Contact number (required)</span></span>
- <span data-ttu-id="1fad9-299">Alanumero</span><span class="sxs-lookup"><span data-stu-id="1fad9-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="1fad9-300">Palkanlaskentatiedot ja ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="1fad9-300">Payroll information and earning codes</span></span>

<span data-ttu-id="1fad9-301">Työntekijöille voidaan antaa erityisiä tuloja tietyllä maksutaajuudella ja toivotulla maksutavalla.</span><span class="sxs-lookup"><span data-stu-id="1fad9-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="1fad9-302">Seuraavia kenttiä käytetään Dayforcessa sen varmistamiseksi, että näitä määrityksiä ja asetuksia käytetään.</span><span class="sxs-lookup"><span data-stu-id="1fad9-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="1fad9-303">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="1fad9-303">Earning codes</span></span>

- <span data-ttu-id="1fad9-304">Toimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-304">Position (required)</span></span>
- <span data-ttu-id="1fad9-305">Ansiokoodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-305">Earning Code (required)</span></span>
- <span data-ttu-id="1fad9-306">Taajuus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-306">Frequency (required)</span></span>
- <span data-ttu-id="1fad9-307">Summa (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="1fad9-308">Palkanlaskentatiedot</span><span class="sxs-lookup"><span data-stu-id="1fad9-308">Payroll information</span></span>

- <span data-ttu-id="1fad9-309">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="1fad9-309">Payment Method</span></span>
- <span data-ttu-id="1fad9-310">Talousalue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-310">Economic Region (required)</span></span>
- <span data-ttu-id="1fad9-311">Työsuhde-etujen tunnus</span><span class="sxs-lookup"><span data-stu-id="1fad9-311">Employee Benefits ID</span></span>
- <span data-ttu-id="1fad9-312">Kansallinen/alueellinen tunnusnumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-312">National ID Number (required)</span></span>
- <span data-ttu-id="1fad9-313">Sotilaspalveluksen numero</span><span class="sxs-lookup"><span data-stu-id="1fad9-313">Military Service Number</span></span>
- <span data-ttu-id="1fad9-314">Vuoron tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-314">Shift ID (required)</span></span>
- <span data-ttu-id="1fad9-315">Veronumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-315">Tax Number (required)</span></span>
- <span data-ttu-id="1fad9-316">Ammattijärjestön tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-316">Union ID (required)</span></span>
- <span data-ttu-id="1fad9-317">Työpäivän tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-317">Work Day ID (required)</span></span>
- <span data-ttu-id="1fad9-318">Työluvan numero</span><span class="sxs-lookup"><span data-stu-id="1fad9-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="1fad9-319">Maksutavoista Meksiko tukee seuraavia: **Käteinen**, **shekki** (yrityksen fyysinen shekki) ja **sähköinen maksu**.</span><span class="sxs-lookup"><span data-stu-id="1fad9-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="1fad9-320">Mikäli maksutapaa ei ole määritetty, **shekki** on oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="1fad9-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="1fad9-321">Työsuhteen tiedot</span><span class="sxs-lookup"><span data-stu-id="1fad9-321">Employment details</span></span>

<span data-ttu-id="1fad9-322">Työntekijöiden yksityiskohtaista historiaa käytetään keskeisenä informaationa, jolla saadaan työntekijän palkkaus, irtisanominen ja rekrytointitilastot Dayforcesta.</span><span class="sxs-lookup"><span data-stu-id="1fad9-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="1fad9-323">Dayforce tukee kerrallaan vain yhtä aktiivisen työntekijän tietuetta.</span><span class="sxs-lookup"><span data-stu-id="1fad9-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="1fad9-324">Työsuhteen alkamispäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-324">Employment start date (required)</span></span>
- <span data-ttu-id="1fad9-325">Työsuhteen päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="1fad9-325">Employment end date</span></span>
- <span data-ttu-id="1fad9-326">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="1fad9-326">Start date</span></span>
- <span data-ttu-id="1fad9-327">Muutettu aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="1fad9-327">Adjusted start date</span></span>
- <span data-ttu-id="1fad9-328">Työsuhteen päättymispäivä (pakollinen päättyessä)</span><span class="sxs-lookup"><span data-stu-id="1fad9-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="1fad9-329">Työsuhteen päättymissyy (pakollinen päättyessä)</span><span class="sxs-lookup"><span data-stu-id="1fad9-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="1fad9-330">Seuraavien tietojen avulla lasketaan työntekijän tärkeimmät päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="1fad9-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="1fad9-331">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="1fad9-331">Human Resources</span></span>                | <span data-ttu-id="1fad9-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1fad9-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fad9-333">Viimeisimmän työhönoton päivämäärä</span><span class="sxs-lookup"><span data-stu-id="1fad9-333">Most recent hire date</span></span> | <span data-ttu-id="1fad9-334">Työntekijän työsuhteen alku voimassa olevassa työhistoriatietueessa</span><span class="sxs-lookup"><span data-stu-id="1fad9-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="1fad9-335">Työsuhteen loppumispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="1fad9-335">Termination date</span></span>      | <span data-ttu-id="1fad9-336">Työntekijän työsuhteen loppu voimassa olevassa työhistoriatietueessa</span><span class="sxs-lookup"><span data-stu-id="1fad9-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="1fad9-337">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="1fad9-337">Start date</span></span>            | <span data-ttu-id="1fad9-338">Muutettu alkamispäivämäärä, alkamispäivämäärä tai työsuhteen alku ei-aktiivisessa työsuhteen historiatietueessa</span><span class="sxs-lookup"><span data-stu-id="1fad9-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="1fad9-339">Alkuperäinen työsuhteen alkamispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="1fad9-339">Original hire date</span></span>    | <span data-ttu-id="1fad9-340">Varhaisin työhistoriatietueen työsuhteen alku</span><span class="sxs-lookup"><span data-stu-id="1fad9-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="1fad9-341">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="1fad9-341">Compensation</span></span>

<span data-ttu-id="1fad9-342">Kiinteän kompensaatiosuunnitelmaan tulee liittää jokaisen työntekijän ensisijainen toimi koko työsuhteen ajalla.</span><span class="sxs-lookup"><span data-stu-id="1fad9-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="1fad9-343">Ajanjakso alkaa siitä päivämäärästä, jona työntekijä palkattiin (tai työsuhteen alkamispäivämäärä) ja jatkuu, kunnes työsuhde loppuu.</span><span class="sxs-lookup"><span data-stu-id="1fad9-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="1fad9-344">Voimaantulopäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-344">Effective Date (required)</span></span>
- <span data-ttu-id="1fad9-345">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="1fad9-345">Expiration date</span></span>
- <span data-ttu-id="1fad9-346">Palkkio (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-346">Pay Rate (required)</span></span>
- <span data-ttu-id="1fad9-347">Palkkion muunnokset (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="1fad9-348">Vuosittainen arvo (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="1fad9-349">Tunnittainen arvo (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="1fad9-350">Mikäli tuntityöntekijällä on useita toimia, ensisijaisen toimen kiinteä kompensaation tuodaan Dayforceen työntekijätason hinta-/peruspalkkana.</span><span class="sxs-lookup"><span data-stu-id="1fad9-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="1fad9-351">Ei-ensisijaisten toimien tuntihinta tallennetaan Dayforcen vastaavaan sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="1fad9-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="1fad9-352">Mikäli palkallisella työntekijällä on useita toimia, kumulatiivinen tuntihinta ja vuosittainen palkka kaikista aktiivisista toimista johdetaan ja käytetään työntekijätason hinta-/peruspalkkana.</span><span class="sxs-lookup"><span data-stu-id="1fad9-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="1fad9-353">Tunnusnumerot</span><span class="sxs-lookup"><span data-stu-id="1fad9-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="1fad9-354">Sosiaaliturvan tunniste</span><span class="sxs-lookup"><span data-stu-id="1fad9-354">Social Security identifier</span></span> 

<span data-ttu-id="1fad9-355">Jokaisella työntekijä on oltava yksi ensisijainen tunnus.</span><span class="sxs-lookup"><span data-stu-id="1fad9-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="1fad9-356">Tunnuksen on oltava **SSN**-tunnus.</span><span class="sxs-lookup"><span data-stu-id="1fad9-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="1fad9-357">Dayforcessa se johdetaan automaattisesti työntekijän sosiaaliturvatunnuksesta, jota tarvitaan työsuhdetta solmittaessa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="1fad9-358">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-358">Primary (required)</span></span>
- <span data-ttu-id="1fad9-359">Tunnuksen tyyppi = "Henkilötunnus"</span><span class="sxs-lookup"><span data-stu-id="1fad9-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="1fad9-360">Myöntämispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="1fad9-360">Issued Date</span></span>
- <span data-ttu-id="1fad9-361">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="1fad9-361">Expiration Date</span></span>

<span data-ttu-id="1fad9-362">Työntekijät voi määrittää useita tunnistenumeroita **SSN**-tunnuksesta (henkilötunnus).</span><span class="sxs-lookup"><span data-stu-id="1fad9-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="1fad9-363">Tietue, joka on merkitty **Ensisijainen** on integroitu Dayforceen, riippumatta siitä, onko numero aktiivinen tai vanhentunut.</span><span class="sxs-lookup"><span data-stu-id="1fad9-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="1fad9-364">Pankkitilit ja suoritukset</span><span class="sxs-lookup"><span data-stu-id="1fad9-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="1fad9-365">Voimassa olevat pankkitilitiedot on kirjattava kaikille työntekijöille, jotka haluavat, että hänelle maksetaan pankkisiirtona.</span><span class="sxs-lookup"><span data-stu-id="1fad9-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="1fad9-366">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="1fad9-366">Human Resources</span></span>                         | <span data-ttu-id="1fad9-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1fad9-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fad9-368">Pankkitilin numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="1fad9-369">SWIFT-koodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-369">SWIFT code (required)</span></span>          | <span data-ttu-id="1fad9-370">**Pankkitunnus**-kenttä, jota käytetään, kun käsitellään palkkalistoja Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="1fad9-371">Sivuliikkeen numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="1fad9-372">Pankkitilin tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-372">Bank account type (required)</span></span>   | <span data-ttu-id="1fad9-373">**Tilityyppi**-kenttä, jota käytetään, kun käsitellään palkkalistoja Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="1fad9-374">Tuetut arvot sisältävät kohdat **Tarkistus** ja **Palkanlaskenta**.</span><span class="sxs-lookup"><span data-stu-id="1fad9-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="1fad9-375">Työntekijät, jotka haluavat, että heille maksetaan pankkisiirtona, on toimitettava linkki jäännöstilille, joka kuuluu oikeushenkilölle, jolla on ensisijainen osoite Meksikossa ja jolla on voimassa oleva tili meksikolaisessa pankissa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="1fad9-376">Kaikki muut jäljellä olevat tilit jätetään huomiotta.</span><span class="sxs-lookup"><span data-stu-id="1fad9-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="1fad9-377">Osoitetiedot</span><span class="sxs-lookup"><span data-stu-id="1fad9-377">Address information</span></span>

<span data-ttu-id="1fad9-378">Jokaisella työntekijällä on oltava yksi ensisijainen toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="1fad9-378">Every employee must have one primary location.</span></span> <span data-ttu-id="1fad9-379">Dayforcessa tätä sijaintia käytetään määrittämään työntekijän ensisijainen oleskelulupa verotusta varten.</span><span class="sxs-lookup"><span data-stu-id="1fad9-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="1fad9-380">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-380">Primary (required)</span></span>
- <span data-ttu-id="1fad9-381">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-381">Country/region (required)</span></span>
- <span data-ttu-id="1fad9-382">Postinumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="1fad9-383">Katuosoite (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-383">Street (required)</span></span>
- <span data-ttu-id="1fad9-384">Kadunnumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-384">Street Number (required)</span></span>
- <span data-ttu-id="1fad9-385">Rakennusta koskeva lisätieto</span><span class="sxs-lookup"><span data-stu-id="1fad9-385">Building Complement</span></span>
- <span data-ttu-id="1fad9-386">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-386">City (required)</span></span>
- <span data-ttu-id="1fad9-387">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-387">State (required)</span></span>
- <span data-ttu-id="1fad9-388">Lääni (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="1fad9-389">Määritä tiedot luodaksesi palkkalistoja Yhdysvalloissa ja Kanadassa</span><span class="sxs-lookup"><span data-stu-id="1fad9-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="1fad9-390">Jos luot maksuja työntekijöille, jotka ovat Yhdysvalloissa ja Kanadassa, seuraavat seikat on määritettävä:</span><span class="sxs-lookup"><span data-stu-id="1fad9-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="1fad9-391">Toimia varten vaaditaan osastot.</span><span class="sxs-lookup"><span data-stu-id="1fad9-391">Departments are required on positions.</span></span>
- <span data-ttu-id="1fad9-392">Kustannuspaikat on määritettävä taloushallinnon dimensioina ja niiden pitää olla ensimmäisenä osana merkkijonoa oletusarvoisessa taloushallinnon dimensiossa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="1fad9-393">Voit määrittää Human Resourcesin edellyttämään, että toimet määrittävät osaston.</span><span class="sxs-lookup"><span data-stu-id="1fad9-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="1fad9-394">Tehdäksesi tämän valitse **Henkilöstöhallinnon jaetut toimet > Toimet > Edellytä osastoja toimissa**.</span><span class="sxs-lookup"><span data-stu-id="1fad9-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="1fad9-395">Suosittelemme, että tämä asetus otetaan käyttöön integrointia varten.</span><span class="sxs-lookup"><span data-stu-id="1fad9-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="1fad9-396">Työtyypit</span><span class="sxs-lookup"><span data-stu-id="1fad9-396">Job types</span></span>

<span data-ttu-id="1fad9-397">Työtyyppien avulla voi luokitella samankaltaisia töitä.</span><span class="sxs-lookup"><span data-stu-id="1fad9-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="1fad9-398">Työlajit ovat pakollisia palkanlaskennan käsittelemiseksi Yhdysvalloissa ja Kanadassa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="1fad9-399">Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka.</span><span class="sxs-lookup"><span data-stu-id="1fad9-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="1fad9-400">Työlajit on yhdistetty Dayforceen maksulajeina, jotka ilmaisevat, onko työntekijällä tuntipalkka vai kuukausipalkka.</span><span class="sxs-lookup"><span data-stu-id="1fad9-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="1fad9-401">Tarvitaan seuraavat työlajit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="1fad9-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="1fad9-402">Työlaji</span><span class="sxs-lookup"><span data-stu-id="1fad9-402">Job type</span></span>   | <span data-ttu-id="1fad9-403">kuvaus</span><span class="sxs-lookup"><span data-stu-id="1fad9-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="1fad9-404">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="1fad9-404">Hourly</span></span>     | <span data-ttu-id="1fad9-405">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="1fad9-405">Hourly</span></span>      |
| <span data-ttu-id="1fad9-406">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="1fad9-406">Salaried</span></span>   | <span data-ttu-id="1fad9-407">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="1fad9-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="1fad9-408">Toimityypit</span><span class="sxs-lookup"><span data-stu-id="1fad9-408">Position types</span></span> 

<span data-ttu-id="1fad9-409">Voit käyttää toimityyppejä kuvaamaan, onko toimi kokoaikainen, osa-aikainen vai jokin muu.</span><span class="sxs-lookup"><span data-stu-id="1fad9-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="1fad9-410">Toimityypit on yhdistetty Dayforceen maksuluokkina, jotka ilmaisevat, onko työntekijä koko- vai osa-aikainen.</span><span class="sxs-lookup"><span data-stu-id="1fad9-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="1fad9-411">Tarvitaan seuraavat toimityypit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="1fad9-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="1fad9-412">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="1fad9-412">Position type</span></span>   | <span data-ttu-id="1fad9-413">kuvaus</span><span class="sxs-lookup"><span data-stu-id="1fad9-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="1fad9-414">Kokoaikainen</span><span class="sxs-lookup"><span data-stu-id="1fad9-414">Full-time</span></span>       | <span data-ttu-id="1fad9-415">Kokopäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-415">Full time employee</span></span> |
| <span data-ttu-id="1fad9-416">Osa-aikainen</span><span class="sxs-lookup"><span data-stu-id="1fad9-416">Part-time</span></span>       | <span data-ttu-id="1fad9-417">Osapäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="1fad9-418">Syykoodit</span><span class="sxs-lookup"><span data-stu-id="1fad9-418">Reason codes</span></span>

<span data-ttu-id="1fad9-419">Syykoodit antavat tietoja työntekijän tilasta</span><span class="sxs-lookup"><span data-stu-id="1fad9-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="1fad9-420">Syykoodit määritetään Dayforceen tilan syinä, jotka ilmaisevat muutokset työntekijän toimessa tai työsuhteessa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="1fad9-421">Tarvitaan seuraavat syykoodit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="1fad9-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="1fad9-422">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="1fad9-422">Reason code</span></span>    | <span data-ttu-id="1fad9-423">kuvaus</span><span class="sxs-lookup"><span data-stu-id="1fad9-423">Description</span></span>      | <span data-ttu-id="1fad9-424">Soveltuvat skenaariot</span><span class="sxs-lookup"><span data-stu-id="1fad9-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="1fad9-425">EROAMINEN</span><span class="sxs-lookup"><span data-stu-id="1fad9-425">RESIGNATION</span></span>    | <span data-ttu-id="1fad9-426">Eroaminen</span><span class="sxs-lookup"><span data-stu-id="1fad9-426">Resignation</span></span>      | <span data-ttu-id="1fad9-427">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-427">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-428">IRTISANOMINEN</span><span class="sxs-lookup"><span data-stu-id="1fad9-428">TERMINATION</span></span>    | <span data-ttu-id="1fad9-429">Irtisanominen</span><span class="sxs-lookup"><span data-stu-id="1fad9-429">Termination</span></span>      | <span data-ttu-id="1fad9-430">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-430">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-431">ELÄKKEELLE SIIRTYMINEN</span><span class="sxs-lookup"><span data-stu-id="1fad9-431">RETIREMENT</span></span>     | <span data-ttu-id="1fad9-432">Eläkkeelle siirtyminen</span><span class="sxs-lookup"><span data-stu-id="1fad9-432">Retirement</span></span>       | <span data-ttu-id="1fad9-433">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-433">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-434">MUU</span><span class="sxs-lookup"><span data-stu-id="1fad9-434">OTHER</span></span>          | <span data-ttu-id="1fad9-435">Muut syyt</span><span class="sxs-lookup"><span data-stu-id="1fad9-435">Other Reasons</span></span>    | <span data-ttu-id="1fad9-436">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-436">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-437">KUOLEMA</span><span class="sxs-lookup"><span data-stu-id="1fad9-437">DEATH</span></span>          | <span data-ttu-id="1fad9-438">Kuolema</span><span class="sxs-lookup"><span data-stu-id="1fad9-438">Death</span></span>            | <span data-ttu-id="1fad9-439">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-439">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-440">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="1fad9-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="1fad9-441">Virkavapaa</span><span class="sxs-lookup"><span data-stu-id="1fad9-441">Leave of Absence</span></span> | <span data-ttu-id="1fad9-442">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-442">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-443">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="1fad9-443">CONTRACTEND</span></span>    | <span data-ttu-id="1fad9-444">Sopimuksen päättyminen</span><span class="sxs-lookup"><span data-stu-id="1fad9-444">End of Contract</span></span>  | <span data-ttu-id="1fad9-445">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-445">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-446">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="1fad9-446">SALARYCHANGE</span></span>   | <span data-ttu-id="1fad9-447">Palkan muutos</span><span class="sxs-lookup"><span data-stu-id="1fad9-447">Change of Salary</span></span> | <span data-ttu-id="1fad9-448">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="1fad9-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="1fad9-449">Siviilisääty</span><span class="sxs-lookup"><span data-stu-id="1fad9-449">Marital status</span></span>

<span data-ttu-id="1fad9-450">Siviilisääty on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="1fad9-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="1fad9-451">Seuraavassa taulukossa kuvataan, miten siviilisääty liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="1fad9-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="1fad9-452">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="1fad9-452">Human Resources</span></span>                 | <span data-ttu-id="1fad9-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1fad9-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="1fad9-454">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="1fad9-454">Married</span></span>                | <span data-ttu-id="1fad9-455">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="1fad9-455">Married</span></span>              |
| <span data-ttu-id="1fad9-456">Yksi</span><span class="sxs-lookup"><span data-stu-id="1fad9-456">Single</span></span>                 | <span data-ttu-id="1fad9-457">Yksi</span><span class="sxs-lookup"><span data-stu-id="1fad9-457">Single</span></span>               |
| <span data-ttu-id="1fad9-458">Leski</span><span class="sxs-lookup"><span data-stu-id="1fad9-458">Widowed</span></span>                | <span data-ttu-id="1fad9-459">Leski</span><span class="sxs-lookup"><span data-stu-id="1fad9-459">Widowed</span></span>              |
| <span data-ttu-id="1fad9-460">Eronnut</span><span class="sxs-lookup"><span data-stu-id="1fad9-460">Divorced</span></span>               | <span data-ttu-id="1fad9-461">Eronnut</span><span class="sxs-lookup"><span data-stu-id="1fad9-461">Divorced</span></span>             |
| <span data-ttu-id="1fad9-462">Rekisteröity suhde</span><span class="sxs-lookup"><span data-stu-id="1fad9-462">Registered Partnership</span></span> | <span data-ttu-id="1fad9-463">Kotimainen kumppanuus</span><span class="sxs-lookup"><span data-stu-id="1fad9-463">Domestic Partnership</span></span> |
| <span data-ttu-id="1fad9-464">None</span><span class="sxs-lookup"><span data-stu-id="1fad9-464">None</span></span>                   | <span data-ttu-id="1fad9-465">None</span><span class="sxs-lookup"><span data-stu-id="1fad9-465">None</span></span>                 |
| <span data-ttu-id="1fad9-466">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="1fad9-466">Cohabiting</span></span>             | <span data-ttu-id="1fad9-467">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="1fad9-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="1fad9-468">Sukupuoli</span><span class="sxs-lookup"><span data-stu-id="1fad9-468">Gender</span></span>

<span data-ttu-id="1fad9-469">Sukupuolinimitykset on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="1fad9-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="1fad9-470">Seuraavassa taulukossa kuvataan, miten sukupuolinimitykset liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="1fad9-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="1fad9-471">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="1fad9-471">Human Resources</span></span>       | <span data-ttu-id="1fad9-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1fad9-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="1fad9-473">Mies</span><span class="sxs-lookup"><span data-stu-id="1fad9-473">Male</span></span>         | <span data-ttu-id="1fad9-474">Mies</span><span class="sxs-lookup"><span data-stu-id="1fad9-474">Male</span></span>            |
| <span data-ttu-id="1fad9-475">Nainen</span><span class="sxs-lookup"><span data-stu-id="1fad9-475">Female</span></span>       | <span data-ttu-id="1fad9-476">Nainen</span><span class="sxs-lookup"><span data-stu-id="1fad9-476">Female</span></span>          |
| <span data-ttu-id="1fad9-477">Yksilöimätön</span><span class="sxs-lookup"><span data-stu-id="1fad9-477">Non-specific</span></span> | <span data-ttu-id="1fad9-478">*Ei tueta*</span><span class="sxs-lookup"><span data-stu-id="1fad9-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="1fad9-479">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="1fad9-479">Earning codes</span></span>

<span data-ttu-id="1fad9-480">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="1fad9-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="1fad9-481">Tunnukset kattavat erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="1fad9-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="1fad9-482">Mikäli käytetään ei-tuettua taajuutta **Jokainen palkka** -taajuutta käytetään oletusarvon mukaan laskelmissa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="1fad9-483">Tuetut maksutaajuudet</span><span class="sxs-lookup"><span data-stu-id="1fad9-483">Supported frequencies</span></span>

- <span data-ttu-id="1fad9-484">Kaikki</span><span class="sxs-lookup"><span data-stu-id="1fad9-484">All</span></span>
- <span data-ttu-id="1fad9-485">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="1fad9-485">EVERYPAY</span></span>
- <span data-ttu-id="1fad9-486">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="1fad9-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="1fad9-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="1fad9-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="1fad9-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="1fad9-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="1fad9-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-489">1OFMTH</span></span>
- <span data-ttu-id="1fad9-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-490">LASTOFMTH</span></span>
- <span data-ttu-id="1fad9-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-491">2OFMTH</span></span>
- <span data-ttu-id="1fad9-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-492">3OFMTH</span></span>
- <span data-ttu-id="1fad9-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-493">4OFMTH</span></span>
- <span data-ttu-id="1fad9-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-494">5OFMTH</span></span>
- <span data-ttu-id="1fad9-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-495">1N2OFMTH</span></span>
- <span data-ttu-id="1fad9-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-496">3N4OFMTH</span></span>
- <span data-ttu-id="1fad9-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-497">1N3OFMTH</span></span>
- <span data-ttu-id="1fad9-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-498">1N4OFMTH</span></span>
- <span data-ttu-id="1fad9-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-499">2N3OFMTH</span></span>
- <span data-ttu-id="1fad9-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-500">2N4OFMTH</span></span>
- <span data-ttu-id="1fad9-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="1fad9-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="1fad9-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="1fad9-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="1fad9-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="1fad9-506">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="1fad9-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="1fad9-507">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="1fad9-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="1fad9-508">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="1fad9-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="1fad9-509">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="1fad9-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="1fad9-510">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="1fad9-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="1fad9-511">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="1fad9-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="1fad9-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="1fad9-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="1fad9-513">Osoitteet</span><span class="sxs-lookup"><span data-stu-id="1fad9-513">Addresses</span></span>

<span data-ttu-id="1fad9-514">Määriteltyjen maiden tai alueiden, valtioiden ja läänin (kuntien) koodien tunnistaminen edellyttää tiettyjä muotoja, joita Dayforce ja maassa tai alueella olevat toimijat pystyvät tunnistamaan.</span><span class="sxs-lookup"><span data-stu-id="1fad9-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="1fad9-515">Vaikka kaupunkien muoto on joustava, jokainen paikkakunta täytyy liittää osavaltioon.</span><span class="sxs-lookup"><span data-stu-id="1fad9-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="1fad9-516">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="1fad9-516">Human Resources</span></span>          | <span data-ttu-id="1fad9-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1fad9-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="1fad9-518">Maa/alue</span><span class="sxs-lookup"><span data-stu-id="1fad9-518">Country/Region</span></span>  | <span data-ttu-id="1fad9-519">Maakoodi</span><span class="sxs-lookup"><span data-stu-id="1fad9-519">Country Code</span></span>          |
| <span data-ttu-id="1fad9-520">Postinumero</span><span class="sxs-lookup"><span data-stu-id="1fad9-520">Zip/Postal Code</span></span> | <span data-ttu-id="1fad9-521">Postinumero</span><span class="sxs-lookup"><span data-stu-id="1fad9-521">Postal Code</span></span>           |
| <span data-ttu-id="1fad9-522">Alue</span><span class="sxs-lookup"><span data-stu-id="1fad9-522">State</span></span>           | <span data-ttu-id="1fad9-523">Aluekoodi</span><span class="sxs-lookup"><span data-stu-id="1fad9-523">State Code</span></span>            |
| <span data-ttu-id="1fad9-524">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="1fad9-524">City</span></span>            | <span data-ttu-id="1fad9-525">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="1fad9-525">City</span></span>                  |
| <span data-ttu-id="1fad9-526">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="1fad9-526">County</span></span>          | <span data-ttu-id="1fad9-527">Lääni (kunta)</span><span class="sxs-lookup"><span data-stu-id="1fad9-527">County (Municipality)</span></span> |
| <span data-ttu-id="1fad9-528">Katu</span><span class="sxs-lookup"><span data-stu-id="1fad9-528">Street</span></span>          | <span data-ttu-id="1fad9-529">Osoiterivi 1</span><span class="sxs-lookup"><span data-stu-id="1fad9-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="1fad9-530">Verotusalueet</span><span class="sxs-lookup"><span data-stu-id="1fad9-530">Tax regions</span></span>

<span data-ttu-id="1fad9-531">Verotusalueita käytetään palkanlaskennan muodostamisessa käytettävän veron määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="1fad9-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="1fad9-532">ALV-alueet yhdistetään Dayforceen toimipaikan osoitteina.</span><span class="sxs-lookup"><span data-stu-id="1fad9-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="1fad9-533">Oletusarvoinen verotusalue on liitettävä työntekijän aktiiviseen toimeen.</span><span class="sxs-lookup"><span data-stu-id="1fad9-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="1fad9-534">Verotusalue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-534">Tax region (required)</span></span>
- <span data-ttu-id="1fad9-535">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-535">Country/Region (required)</span></span>
- <span data-ttu-id="1fad9-536">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-536">State (required)</span></span>
- <span data-ttu-id="1fad9-537">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="1fad9-537">County</span></span> 
- <span data-ttu-id="1fad9-538">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="1fad9-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="1fad9-539">Määritä tietosi tuottaaksesi palkkalistoja Meksikossa</span><span class="sxs-lookup"><span data-stu-id="1fad9-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="1fad9-540">Jos luot maksuja työntekijöille, jotka ovat Meksikossa, seuraavat seikat on määritettävä:</span><span class="sxs-lookup"><span data-stu-id="1fad9-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="1fad9-541">Toimia varten vaaditaan osastot.</span><span class="sxs-lookup"><span data-stu-id="1fad9-541">Departments are required on positions.</span></span>
- <span data-ttu-id="1fad9-542">Kustannuspaikat on määritettävä taloushallinnon dimensioina ja niiden pitää olla ensimmäisenä osana merkkijonoa oletusarvoisessa taloushallinnon dimensiossa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="1fad9-543">Työtyypit</span><span class="sxs-lookup"><span data-stu-id="1fad9-543">Job types</span></span>

<span data-ttu-id="1fad9-544">Työtyyppien avulla voi luokitella samankaltaisia töitä.</span><span class="sxs-lookup"><span data-stu-id="1fad9-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="1fad9-545">Työlajit ovat pakollisia palkkalistojen käsittelemiseen Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="1fad9-546">Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka.</span><span class="sxs-lookup"><span data-stu-id="1fad9-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="1fad9-547">Työlajit on yhdistetty Dayforceen maksulajeina, jotka ilmaisevat, onko työntekijällä tuntipalkka vai kuukausipalkka.</span><span class="sxs-lookup"><span data-stu-id="1fad9-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="1fad9-548">Tarvitaan seuraavat työlajit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="1fad9-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="1fad9-549">Työlaji</span><span class="sxs-lookup"><span data-stu-id="1fad9-549">Job type</span></span>   | <span data-ttu-id="1fad9-550">kuvaus</span><span class="sxs-lookup"><span data-stu-id="1fad9-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="1fad9-551">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="1fad9-551">Hourly</span></span>     | <span data-ttu-id="1fad9-552">MX tunneittain</span><span class="sxs-lookup"><span data-stu-id="1fad9-552">MX Hourly</span></span>   |
| <span data-ttu-id="1fad9-553">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="1fad9-553">Salaried</span></span>   | <span data-ttu-id="1fad9-554">MX kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="1fad9-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="1fad9-555">Toimityypit</span><span class="sxs-lookup"><span data-stu-id="1fad9-555">Position types</span></span> 

<span data-ttu-id="1fad9-556">Voit käyttää toimityyppejä kuvaamaan, onko toimi kokoaikainen, osa-aikainen vai jokin muu.</span><span class="sxs-lookup"><span data-stu-id="1fad9-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="1fad9-557">Toimityypit on yhdistetty Dayforceen maksuluokkina, jotka ilmaisevat, onko työntekijä koko- vai osa-aikainen.</span><span class="sxs-lookup"><span data-stu-id="1fad9-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="1fad9-558">Tarvitaan seuraavat toimityypit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="1fad9-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="1fad9-559">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="1fad9-559">Position type</span></span>   | <span data-ttu-id="1fad9-560">kuvaus</span><span class="sxs-lookup"><span data-stu-id="1fad9-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="1fad9-561">Kokoaikainen</span><span class="sxs-lookup"><span data-stu-id="1fad9-561">Full-time</span></span>       | <span data-ttu-id="1fad9-562">Kokopäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-562">Full time employee</span></span> |
| <span data-ttu-id="1fad9-563">Osa-aikainen</span><span class="sxs-lookup"><span data-stu-id="1fad9-563">Part-time</span></span>       | <span data-ttu-id="1fad9-564">Osapäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="1fad9-565">Syykoodit</span><span class="sxs-lookup"><span data-stu-id="1fad9-565">Reason codes</span></span>

<span data-ttu-id="1fad9-566">Syykoodit antavat tietoja työntekijän tilasta</span><span class="sxs-lookup"><span data-stu-id="1fad9-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="1fad9-567">Syykoodit määritetään Dayforceen tilan syinä, jotka ilmaisevat muutokset työntekijän toimessa tai työsuhteessa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="1fad9-568">Tarvitaan seuraavat syykoodit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="1fad9-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="1fad9-569">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="1fad9-569">Reason code</span></span>            | <span data-ttu-id="1fad9-570">kuvaus</span><span class="sxs-lookup"><span data-stu-id="1fad9-570">Description</span></span>                    | <span data-ttu-id="1fad9-571">Soveltuvat skenaariot</span><span class="sxs-lookup"><span data-stu-id="1fad9-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="1fad9-572">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="1fad9-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="1fad9-573">Lähtö ennen ensimmäistä palkanlaskentaa</span><span class="sxs-lookup"><span data-stu-id="1fad9-573">Departure before first payroll</span></span> | <span data-ttu-id="1fad9-574">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-574">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-575">EROAMINEN</span><span class="sxs-lookup"><span data-stu-id="1fad9-575">RESIGNATION</span></span>            | <span data-ttu-id="1fad9-576">Eroaminen</span><span class="sxs-lookup"><span data-stu-id="1fad9-576">Resignation</span></span>                    | <span data-ttu-id="1fad9-577">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-577">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-578">ELÄKE</span><span class="sxs-lookup"><span data-stu-id="1fad9-578">PENSION</span></span>                | <span data-ttu-id="1fad9-579">Eläke</span><span class="sxs-lookup"><span data-stu-id="1fad9-579">Pension</span></span>                        | <span data-ttu-id="1fad9-580">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-580">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-581">IRTISANOMINEN</span><span class="sxs-lookup"><span data-stu-id="1fad9-581">TERMINATION</span></span>            | <span data-ttu-id="1fad9-582">Irtisanominen</span><span class="sxs-lookup"><span data-stu-id="1fad9-582">Termination</span></span>                    | <span data-ttu-id="1fad9-583">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-583">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-584">ELÄKKEELLE SIIRTYMINEN</span><span class="sxs-lookup"><span data-stu-id="1fad9-584">RETIREMENT</span></span>             | <span data-ttu-id="1fad9-585">Eläkkeelle siirtyminen</span><span class="sxs-lookup"><span data-stu-id="1fad9-585">Retirement</span></span>                     | <span data-ttu-id="1fad9-586">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-586">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-587">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="1fad9-587">ABSENTEE</span></span>               | <span data-ttu-id="1fad9-588">Absentee</span><span class="sxs-lookup"><span data-stu-id="1fad9-588">Absentee</span></span>                       | <span data-ttu-id="1fad9-589">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-589">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-590">MUU</span><span class="sxs-lookup"><span data-stu-id="1fad9-590">OTHER</span></span>                  | <span data-ttu-id="1fad9-591">Muut syyt</span><span class="sxs-lookup"><span data-stu-id="1fad9-591">Other Reasons</span></span>                  | <span data-ttu-id="1fad9-592">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-592">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-593">SULKEMINEN</span><span class="sxs-lookup"><span data-stu-id="1fad9-593">CLOSURE</span></span>                | <span data-ttu-id="1fad9-594">Liiketoiminnan sulkeminen</span><span class="sxs-lookup"><span data-stu-id="1fad9-594">Business Closure</span></span>               | <span data-ttu-id="1fad9-595">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-595">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-596">KUOLEMA</span><span class="sxs-lookup"><span data-stu-id="1fad9-596">DEATH</span></span>                  | <span data-ttu-id="1fad9-597">Kuolema</span><span class="sxs-lookup"><span data-stu-id="1fad9-597">Death</span></span>                          | <span data-ttu-id="1fad9-598">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-598">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-599">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="1fad9-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="1fad9-600">Virkavapaa</span><span class="sxs-lookup"><span data-stu-id="1fad9-600">Leave of Absence</span></span>               | <span data-ttu-id="1fad9-601">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-601">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-602">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="1fad9-602">CONTRACTEND</span></span>            | <span data-ttu-id="1fad9-603">Sopimuksen päättyminen</span><span class="sxs-lookup"><span data-stu-id="1fad9-603">End of Contract</span></span>                | <span data-ttu-id="1fad9-604">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="1fad9-604">Terminate worker</span></span>     |
| <span data-ttu-id="1fad9-605">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="1fad9-605">SALARYCHANGE</span></span>           | <span data-ttu-id="1fad9-606">Palkan muutos</span><span class="sxs-lookup"><span data-stu-id="1fad9-606">Change of Salary</span></span>               | <span data-ttu-id="1fad9-607">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="1fad9-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="1fad9-608">Työehdot</span><span class="sxs-lookup"><span data-stu-id="1fad9-608">Terms of employment</span></span>

<span data-ttu-id="1fad9-609">Työehtoja voidaan käyttää, kun luodaan työehtoluokkia.</span><span class="sxs-lookup"><span data-stu-id="1fad9-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="1fad9-610">Ehdot määritetään Dayforceen työsuhteen mittarin arvoina.</span><span class="sxs-lookup"><span data-stu-id="1fad9-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="1fad9-611">Seuraavat työsuhteen ja kuvaukset termit ovat pakollisia.</span><span class="sxs-lookup"><span data-stu-id="1fad9-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="1fad9-612">Työehdot</span><span class="sxs-lookup"><span data-stu-id="1fad9-612">Terms of employment</span></span>   | <span data-ttu-id="1fad9-613">kuvaus</span><span class="sxs-lookup"><span data-stu-id="1fad9-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="1fad9-614">Säännöllinen</span><span class="sxs-lookup"><span data-stu-id="1fad9-614">Regular</span></span>               | <span data-ttu-id="1fad9-615">Säännöllinen</span><span class="sxs-lookup"><span data-stu-id="1fad9-615">Regular</span></span>     |
| <span data-ttu-id="1fad9-616">Suora</span><span class="sxs-lookup"><span data-stu-id="1fad9-616">Direct</span></span>                | <span data-ttu-id="1fad9-617">Suora</span><span class="sxs-lookup"><span data-stu-id="1fad9-617">Direct</span></span>      |
| <span data-ttu-id="1fad9-618">Harjoittelujakso</span><span class="sxs-lookup"><span data-stu-id="1fad9-618">Internship</span></span>            | <span data-ttu-id="1fad9-619">Harjoittelujakso</span><span class="sxs-lookup"><span data-stu-id="1fad9-619">Internship</span></span>  |
| <span data-ttu-id="1fad9-620">Pysyvä</span><span class="sxs-lookup"><span data-stu-id="1fad9-620">Permanent</span></span>             | <span data-ttu-id="1fad9-621">Pysyvä</span><span class="sxs-lookup"><span data-stu-id="1fad9-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="1fad9-622">Siviilisääty</span><span class="sxs-lookup"><span data-stu-id="1fad9-622">Marital status</span></span>

<span data-ttu-id="1fad9-623">Siviilisääty on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="1fad9-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="1fad9-624">Seuraavassa taulukossa kuvataan, miten siviilisääty liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="1fad9-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="1fad9-625">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="1fad9-625">Human Resources</span></span>                 | <span data-ttu-id="1fad9-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1fad9-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="1fad9-627">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="1fad9-627">Married</span></span>                | <span data-ttu-id="1fad9-628">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="1fad9-628">Married</span></span>                   |
| <span data-ttu-id="1fad9-629">Yksi</span><span class="sxs-lookup"><span data-stu-id="1fad9-629">Single</span></span>                 | <span data-ttu-id="1fad9-630">Yksi</span><span class="sxs-lookup"><span data-stu-id="1fad9-630">Single</span></span>                    |
| <span data-ttu-id="1fad9-631">Leski</span><span class="sxs-lookup"><span data-stu-id="1fad9-631">Widowed</span></span>                | <span data-ttu-id="1fad9-632">Leski</span><span class="sxs-lookup"><span data-stu-id="1fad9-632">Widowed</span></span>                   |
| <span data-ttu-id="1fad9-633">Eronnut</span><span class="sxs-lookup"><span data-stu-id="1fad9-633">Divorced</span></span>               | <span data-ttu-id="1fad9-634">Eronnut</span><span class="sxs-lookup"><span data-stu-id="1fad9-634">Divorced</span></span>                  |
| <span data-ttu-id="1fad9-635">Rekisteröity suhde</span><span class="sxs-lookup"><span data-stu-id="1fad9-635">Registered Partnership</span></span> | <span data-ttu-id="1fad9-636">Kotimainen kumppanuus</span><span class="sxs-lookup"><span data-stu-id="1fad9-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="1fad9-637">None</span><span class="sxs-lookup"><span data-stu-id="1fad9-637">None</span></span>                   | <span data-ttu-id="1fad9-638">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="1fad9-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="1fad9-639">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="1fad9-639">Cohabiting</span></span>             | <span data-ttu-id="1fad9-640">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="1fad9-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="1fad9-641">Sukupuoli</span><span class="sxs-lookup"><span data-stu-id="1fad9-641">Gender</span></span>

<span data-ttu-id="1fad9-642">Sukupuolinimitykset on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="1fad9-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="1fad9-643">Seuraavassa taulukossa kuvataan, miten sukupuolinimitykset liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="1fad9-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="1fad9-644">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="1fad9-644">Human Resources</span></span>       | <span data-ttu-id="1fad9-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1fad9-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="1fad9-646">Mies</span><span class="sxs-lookup"><span data-stu-id="1fad9-646">Male</span></span>         | <span data-ttu-id="1fad9-647">Mies</span><span class="sxs-lookup"><span data-stu-id="1fad9-647">Male</span></span>                      |
| <span data-ttu-id="1fad9-648">Nainen</span><span class="sxs-lookup"><span data-stu-id="1fad9-648">Female</span></span>       | <span data-ttu-id="1fad9-649">Nainen</span><span class="sxs-lookup"><span data-stu-id="1fad9-649">Female</span></span>                    |
| <span data-ttu-id="1fad9-650">Yksilöimätön</span><span class="sxs-lookup"><span data-stu-id="1fad9-650">Non-specific</span></span> | <span data-ttu-id="1fad9-651">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="1fad9-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="1fad9-652">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="1fad9-652">Payment method</span></span>

<span data-ttu-id="1fad9-653">Maksutavat antavat työntekijälle ja yritykselle keinon kuvata, miten työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="1fad9-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="1fad9-654">Maksutavat on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="1fad9-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="1fad9-655">Seuraavassa taulukossa kuvataan, miten maksutavat liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="1fad9-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="1fad9-656">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="1fad9-656">Human Resources</span></span>             | <span data-ttu-id="1fad9-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1fad9-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="1fad9-658">Maksu</span><span class="sxs-lookup"><span data-stu-id="1fad9-658">Cash</span></span>               | <span data-ttu-id="1fad9-659">Maksu</span><span class="sxs-lookup"><span data-stu-id="1fad9-659">Cash</span></span>                      |
| <span data-ttu-id="1fad9-660">Sähköinen maksu</span><span class="sxs-lookup"><span data-stu-id="1fad9-660">Electronic Payment</span></span> | <span data-ttu-id="1fad9-661">Tapahtumien siirto</span><span class="sxs-lookup"><span data-stu-id="1fad9-661">Transfer</span></span>                  |
| <span data-ttu-id="1fad9-662">Tarkistus</span><span class="sxs-lookup"><span data-stu-id="1fad9-662">Check</span></span>              | <span data-ttu-id="1fad9-663">Sekki</span><span class="sxs-lookup"><span data-stu-id="1fad9-663">Cheque</span></span>                    |
| <span data-ttu-id="1fad9-664">Pankkivekseli</span><span class="sxs-lookup"><span data-stu-id="1fad9-664">Bank Draft</span></span>         | <span data-ttu-id="1fad9-665">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="1fad9-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="1fad9-666">Muu</span><span class="sxs-lookup"><span data-stu-id="1fad9-666">Other</span></span>              | <span data-ttu-id="1fad9-667">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="1fad9-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="1fad9-668">Pankkitilin tyyppi</span><span class="sxs-lookup"><span data-stu-id="1fad9-668">Bank account type</span></span>

<span data-ttu-id="1fad9-669">Pankkitilin tyyppejä käytetään sähköisissä maksuissa työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="1fad9-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="1fad9-670">Pankin tilityypit yhdistetään Dayforceen tilinsiirtämisen tietoina.</span><span class="sxs-lookup"><span data-stu-id="1fad9-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="1fad9-671">Pankkitilin tyypit ovat tarvittaessa käännettyjä ja hyväksytty arvoiksi sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="1fad9-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="1fad9-672">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="1fad9-672">Human Resources</span></span>            | <span data-ttu-id="1fad9-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1fad9-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="1fad9-674">Käyttötili</span><span class="sxs-lookup"><span data-stu-id="1fad9-674">Checking Account</span></span>  | <span data-ttu-id="1fad9-675">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="1fad9-675">CheckingAccount</span></span>           |
| <span data-ttu-id="1fad9-676">Palkanlaskennan tili</span><span class="sxs-lookup"><span data-stu-id="1fad9-676">Payroll Account</span></span>   | <span data-ttu-id="1fad9-677">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="1fad9-677">PayrollAccount</span></span>            |
| <span data-ttu-id="1fad9-678">Säästötili</span><span class="sxs-lookup"><span data-stu-id="1fad9-678">Savings Account</span></span>   | <span data-ttu-id="1fad9-679">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="1fad9-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="1fad9-680">BankGirot-tili</span><span class="sxs-lookup"><span data-stu-id="1fad9-680">BankGirot account</span></span> | <span data-ttu-id="1fad9-681">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="1fad9-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="1fad9-682">PlusGirot-tili</span><span class="sxs-lookup"><span data-stu-id="1fad9-682">PlusGirot account</span></span> | <span data-ttu-id="1fad9-683">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="1fad9-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="1fad9-684">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="1fad9-684">Earning codes</span></span>

<span data-ttu-id="1fad9-685">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="1fad9-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="1fad9-686">Tunnukset kattavat erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="1fad9-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="1fad9-687">Mikäli käytetään ei-tuettua taajuutta **Jokainen palkka** -taajuutta käytetään oletusarvon mukaan laskelmissa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="1fad9-688">Tuetut maksutaajuudet</span><span class="sxs-lookup"><span data-stu-id="1fad9-688">Supported frequencies</span></span>

- <span data-ttu-id="1fad9-689">Kaikki</span><span class="sxs-lookup"><span data-stu-id="1fad9-689">All</span></span>
- <span data-ttu-id="1fad9-690">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="1fad9-690">EVERYPAY</span></span>
- <span data-ttu-id="1fad9-691">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="1fad9-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="1fad9-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="1fad9-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="1fad9-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="1fad9-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="1fad9-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-694">1OFMTH</span></span>
- <span data-ttu-id="1fad9-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-695">LASTOFMTH</span></span>
- <span data-ttu-id="1fad9-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-696">2OFMTH</span></span>
- <span data-ttu-id="1fad9-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-697">3OFMTH</span></span>
- <span data-ttu-id="1fad9-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-698">4OFMTH</span></span>
- <span data-ttu-id="1fad9-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-699">5OFMTH</span></span>
- <span data-ttu-id="1fad9-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-700">1N2OFMTH</span></span>
- <span data-ttu-id="1fad9-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-701">3N4OFMTH</span></span>
- <span data-ttu-id="1fad9-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-702">1N3OFMTH</span></span>
- <span data-ttu-id="1fad9-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-703">1N4OFMTH</span></span>
- <span data-ttu-id="1fad9-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-704">2N3OFMTH</span></span>
- <span data-ttu-id="1fad9-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-705">2N4OFMTH</span></span>
- <span data-ttu-id="1fad9-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="1fad9-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="1fad9-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="1fad9-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="1fad9-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1fad9-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="1fad9-711">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="1fad9-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="1fad9-712">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="1fad9-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="1fad9-713">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="1fad9-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="1fad9-714">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="1fad9-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="1fad9-715">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="1fad9-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="1fad9-716">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="1fad9-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="1fad9-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="1fad9-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="1fad9-718">Osoitteet</span><span class="sxs-lookup"><span data-stu-id="1fad9-718">Addresses</span></span>

<span data-ttu-id="1fad9-719">Määriteltyjen maiden tai alueiden, valtioiden ja läänin (kuntien) koodien tunnistaminen edellyttää tiettyjä muotoja, joita Dayforce ja maassa tai alueella olevat toimijat pystyvät tunnistamaan.</span><span class="sxs-lookup"><span data-stu-id="1fad9-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="1fad9-720">Vaikka kaupunkien muoto on joustava, jokainen paikkakunta täytyy liittää osavaltioon.</span><span class="sxs-lookup"><span data-stu-id="1fad9-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="1fad9-721">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="1fad9-721">Human Resources</span></span>              | <span data-ttu-id="1fad9-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1fad9-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="1fad9-723">Maa/alue</span><span class="sxs-lookup"><span data-stu-id="1fad9-723">Country/Region</span></span>      | <span data-ttu-id="1fad9-724">Maakoodi</span><span class="sxs-lookup"><span data-stu-id="1fad9-724">Country Code</span></span>          |
| <span data-ttu-id="1fad9-725">Postinumero</span><span class="sxs-lookup"><span data-stu-id="1fad9-725">Zip/Postal Code</span></span>     | <span data-ttu-id="1fad9-726">Postinumero</span><span class="sxs-lookup"><span data-stu-id="1fad9-726">Postal Code</span></span>           |
| <span data-ttu-id="1fad9-727">Alue</span><span class="sxs-lookup"><span data-stu-id="1fad9-727">State</span></span>               | <span data-ttu-id="1fad9-728">Aluekoodi</span><span class="sxs-lookup"><span data-stu-id="1fad9-728">State Code</span></span>            |
| <span data-ttu-id="1fad9-729">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="1fad9-729">City</span></span>                | <span data-ttu-id="1fad9-730">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="1fad9-730">City</span></span>                  |
| <span data-ttu-id="1fad9-731">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="1fad9-731">County</span></span>              | <span data-ttu-id="1fad9-732">Lääni (kunta)</span><span class="sxs-lookup"><span data-stu-id="1fad9-732">County (Municipality)</span></span> |
| <span data-ttu-id="1fad9-733">Katu</span><span class="sxs-lookup"><span data-stu-id="1fad9-733">Street</span></span>              | <span data-ttu-id="1fad9-734">Osoiterivi 1</span><span class="sxs-lookup"><span data-stu-id="1fad9-734">Address Line 1</span></span>        |
| <span data-ttu-id="1fad9-735">Kadunnumero</span><span class="sxs-lookup"><span data-stu-id="1fad9-735">Street Number</span></span>       | <span data-ttu-id="1fad9-736">Osoiterivi 2</span><span class="sxs-lookup"><span data-stu-id="1fad9-736">Address Line 2</span></span>        |
| <span data-ttu-id="1fad9-737">Rakennusta koskeva lisätieto</span><span class="sxs-lookup"><span data-stu-id="1fad9-737">Building Complement</span></span> | <span data-ttu-id="1fad9-738">Osoiterivi 5</span><span class="sxs-lookup"><span data-stu-id="1fad9-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="1fad9-739">Passin numero</span><span class="sxs-lookup"><span data-stu-id="1fad9-739">Passport number</span></span>

<span data-ttu-id="1fad9-740">Työntekijät voivat ilmoittaa passin tiedot.</span><span class="sxs-lookup"><span data-stu-id="1fad9-740">Employees can declare passport information.</span></span> <span data-ttu-id="1fad9-741">Tämä tietoa on **Passi**-tunnustyyppiä ja se on integroitu Dayforceen osaksi työntekijän Meksikon liittyvää tietoa.</span><span class="sxs-lookup"><span data-stu-id="1fad9-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="1fad9-742">Tunnustyyppi = "Passi"</span><span class="sxs-lookup"><span data-stu-id="1fad9-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="1fad9-743">Myöntämispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="1fad9-743">Issued Date</span></span>
- <span data-ttu-id="1fad9-744">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="1fad9-744">Expiration Date</span></span>

<span data-ttu-id="1fad9-745">Työntekijät voi määrittää useita tunnistenumeroita **Passi**-tunnuksesta.</span><span class="sxs-lookup"><span data-stu-id="1fad9-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="1fad9-746">Vain nykyiset aktiiviset passitapahtumat integroidaan Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="1fad9-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="1fad9-747">Mikäli kaikki passitapahtumat ovat vanhentuneet, passi, joka on viimeksi myönnetty on integroitu Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="1fad9-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
