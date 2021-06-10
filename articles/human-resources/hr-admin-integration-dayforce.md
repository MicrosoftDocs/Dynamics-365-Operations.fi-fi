---
title: Dayforceen integroinnin määritys
description: Microsoft Dynamics 365 Human Resourcesin ja Ceridian Dayforcen välinen integrointi käyttää useita konfiguraation vaiheita, jotka on kuvattu tässä artikkelissa. Sekä Human Resourcesin että Dayforcen integrointi on määritettävä ennen kuin voit käsitellä palkka-ajoa.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d150daa92fe79cf6620ce5ddf1a01f369c64053
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051494"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="c36b5-104">Dayforceen integroinnin määritys</span><span class="sxs-lookup"><span data-stu-id="c36b5-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c36b5-105">Microsoft Dynamics 365 Human Resourcesin ja Ceridian Dayforcen välinen integrointi käyttää useita konfiguraation vaiheita, jotka on kuvattu tässä artikkelissa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="c36b5-106">Sekä Human Resourcesin että Dayforcen integrointi on määritettävä ennen kuin voit käsitellä palkka-ajoa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="c36b5-107">Käytettäessä jotakin palvelua, kuten Dayforcea palkka-ajojen suorittamiseen, on otettava käyttöön integrointi Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="c36b5-108">Integrointi edellyttää tiettyjä tietoja Human Resourcesista.</span><span class="sxs-lookup"><span data-stu-id="c36b5-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="c36b5-109">Sinun on varmistettava, että Dayforceen yhdistetyt tiedot on konfiguroitu Human Resourcesissa siten, että ne tukevat integrointia.</span><span class="sxs-lookup"><span data-stu-id="c36b5-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="c36b5-110">Integraatio käyttää seuraavanlaisia laajoja tietoryhmiä:</span><span class="sxs-lookup"><span data-stu-id="c36b5-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="c36b5-111">Henkilöstöhallintotiedot</span><span class="sxs-lookup"><span data-stu-id="c36b5-111">Human resources data</span></span>
- <span data-ttu-id="c36b5-112">Kompensaatiotiedot</span><span class="sxs-lookup"><span data-stu-id="c36b5-112">Compensation data</span></span>
- <span data-ttu-id="c36b5-113">Palkanlaskentatietoja, kuten maksujaksot, maksukaudet ja ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="c36b5-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="c36b5-114">Työntekijän tiedot</span><span class="sxs-lookup"><span data-stu-id="c36b5-114">Worker data</span></span>

<span data-ttu-id="c36b5-115">Tässä artikkelissa kuvataan vaiheita, joita sinun on noudatettava ottaaksesi integroinnin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="c36b5-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="c36b5-116">Lisäksi kerrotaan minkä tyyppisiä tietoja ja konfigurointitietoja integrointi edellyttää.</span><span class="sxs-lookup"><span data-stu-id="c36b5-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="c36b5-117">Ota integraatio käyttöön</span><span class="sxs-lookup"><span data-stu-id="c36b5-117">Enable the integration</span></span>

<span data-ttu-id="c36b5-118">Ota integraatio käyttöön Human Resourcesissa ja lisää konfiguraatiotiedot muodostaaksesi yhteyden Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="c36b5-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="c36b5-119">Mikäli haluat kirjanpitotapahtuman, joka valmistetaan ja tuodaan Microsoft Dynamics 365 Financeen, sinun on määritettävä myös Microsoft Azure -tallennustili ja kirjoitettava Azure-tallennuksen yhteyden muodostuskomento Financeen.</span><span class="sxs-lookup"><span data-stu-id="c36b5-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="c36b5-120">Ota integrointi käyttöön Human Resourcesissa seuraavien vaiheiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="c36b5-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="c36b5-121">Valitse **Järjestelmänvalvoja**-sivulla **konfiguroinnin integrointi**.</span><span class="sxs-lookup"><span data-stu-id="c36b5-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="c36b5-122">Lisää File Transfer Protocol (FTP) -päätepiste ja suojattu FTP-kansiopolku.</span><span class="sxs-lookup"><span data-stu-id="c36b5-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="c36b5-123">Kirjoita sen käyttäjän käyttäjänimi ja salasana, joka voi käyttää suojattua FTP-päätepistettä ja kansiopolkua.</span><span class="sxs-lookup"><span data-stu-id="c36b5-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="c36b5-124">Testaa yhteys kuten vaadittu ja määritä **Ota käyttöön palkanmaksun integrointi** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="c36b5-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="c36b5-125">Kun integrointi otetaan käyttöön, tietojen viennin paketti ja tiedostot luodaan ja taajuus määritetään.</span><span class="sxs-lookup"><span data-stu-id="c36b5-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="c36b5-126">Voit muuttaa tätä taajuutta tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="c36b5-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="c36b5-127">Lisätietoja Azure-tallennustilien ja Azure-tallennusyhteyden yhteysmerkkijonoista seuraavissa Azure-artikkeleissa:</span><span class="sxs-lookup"><span data-stu-id="c36b5-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="c36b5-128">Lisätietoja Azure-tallennustileistä</span><span class="sxs-lookup"><span data-stu-id="c36b5-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="c36b5-129">Määritä Azure-tallennustilan yhteysmerkkijonot</span><span class="sxs-lookup"><span data-stu-id="c36b5-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="c36b5-130">Tekniset tiedot, kun palkanlaskennan integrointi on otettu käyttöön</span><span class="sxs-lookup"><span data-stu-id="c36b5-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="c36b5-131">Palkanlaskennan integroinnin käytöstäpoistamisella on kaksi pääasiallista vaikutusta:</span><span class="sxs-lookup"><span data-stu-id="c36b5-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="c36b5-132">Palkanlaskennan integroinnin vienti -niminen tietojen vientiprojekti luodaan.</span><span class="sxs-lookup"><span data-stu-id="c36b5-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="c36b5-133">Tämä projekti sisältää palkanhallinnan integrointiin tarvittavat yksiköt ja kentät.</span><span class="sxs-lookup"><span data-stu-id="c36b5-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="c36b5-134">Voit tutustua projektiin valitsemalla ensin **Järjestelmän hallinta**, sitten **Tietojen hallinta** -ruudun ja avaamalla lopuksi tietoprojektin projektiluettelosta.</span><span class="sxs-lookup"><span data-stu-id="c36b5-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="c36b5-135">Tämä erätyö suorittaa tietojen vientiprojektin, salaa tuloksena olevan tietopaketin ja siirtää tietopakettitiedoston SFTP-päätepisteeseen, joka on määritetty **Integroinnin määritys** -näytössä.</span><span class="sxs-lookup"><span data-stu-id="c36b5-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="c36b5-136">SFTP-päätepisteeseen siirretty tietopaketti salataan paketin yksilöllisellä avaimella.</span><span class="sxs-lookup"><span data-stu-id="c36b5-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="c36b5-137">Avain on Azure Key Vaultissa, jota vain Ceridian voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="c36b5-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="c36b5-138">Tietopaketin sisällön salausta ei voi purkaa eikä sisältöä tutkia.</span><span class="sxs-lookup"><span data-stu-id="c36b5-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="c36b5-139">Jos tietopaketin sisältöä on tarkasteltava, Palkanlaskennan integroinnin vienti -tietoprojekti on vietävä manuaalisesti, jonka jälkeen on ladattava ja avattava.</span><span class="sxs-lookup"><span data-stu-id="c36b5-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="c36b5-140">Manuaalisessa viennissä ei käytetä salausta eikä pakettia siirretä.</span><span class="sxs-lookup"><span data-stu-id="c36b5-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="c36b5-141">Jos integroinnin tiedostot lähetetään Dynamics 365 Human Resources UAT- tai eristysympäristöstä Ceridian Dayforce -testiympäristöön, voit käyttää seuraavaa key vault -URL-osoitetta: https://payrollintegrationprod.vault.azure.net.</span><span class="sxs-lookup"><span data-stu-id="c36b5-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="c36b5-142">Määritä tietosi</span><span class="sxs-lookup"><span data-stu-id="c36b5-142">Configure your data</span></span> 

<span data-ttu-id="c36b5-143">Voidaksesi käsitellä palkanlaskentaa, sinun on määritettävä henkilöstöhallinnon tiedot Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="c36b5-144">On määritettävä organisaation tiedot, kuten työt ja toimet sekä edut ja kompensaatiotiedot.</span><span class="sxs-lookup"><span data-stu-id="c36b5-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="c36b5-145">Nämä tiedot sisältävät työllisyys-, palkka- ja vähennystiedot, jotka vaaditaan, jotta voidaan luoda työntekijän palkka.</span><span class="sxs-lookup"><span data-stu-id="c36b5-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="c36b5-146">Henkilöstöhallintotiedot</span><span class="sxs-lookup"><span data-stu-id="c36b5-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="c36b5-147">Edut</span><span class="sxs-lookup"><span data-stu-id="c36b5-147">Benefits</span></span> 

<span data-ttu-id="c36b5-148">Henkilöstöhallinto sisältää työkaluja, joiden avulla organisaation tarjoamia tai työntekijöitä varten käsittelemiä etuja, vähennyksiä ja työntekijöiden kompensaatiosuunnitelmia voi määrittää ja ylläpitää.</span><span class="sxs-lookup"><span data-stu-id="c36b5-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="c36b5-149">Luodessasi etuja, pidä mielessä seuraavat tiedot ja konfiguraatiot, joita käytetään Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="c36b5-150">Etusuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="c36b5-150">Benefit plans</span></span>

- <span data-ttu-id="c36b5-151">Suunnitelma (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-151">Plan (required)</span></span>
- <span data-ttu-id="c36b5-152">Tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-152">Type (required)</span></span>
- <span data-ttu-id="c36b5-153">Palkanlaskennan vaikutus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-153">Payroll impact (required)</span></span>
- <span data-ttu-id="c36b5-154">Palauta velvoitteet</span><span class="sxs-lookup"><span data-stu-id="c36b5-154">Recover arrears</span></span>
- <span data-ttu-id="c36b5-155">Vähennysmenetelmä</span><span class="sxs-lookup"><span data-stu-id="c36b5-155">Deduction method</span></span>
- <span data-ttu-id="c36b5-156">Vähennyksen prioriteetti</span><span class="sxs-lookup"><span data-stu-id="c36b5-156">Deduction priority</span></span>
- <span data-ttu-id="c36b5-157">Rajaa kausi</span><span class="sxs-lookup"><span data-stu-id="c36b5-157">Limit period</span></span>
- <span data-ttu-id="c36b5-158">Rajasumma</span><span class="sxs-lookup"><span data-stu-id="c36b5-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="c36b5-159">Edut</span><span class="sxs-lookup"><span data-stu-id="c36b5-159">Benefits</span></span>

- <span data-ttu-id="c36b5-160">Suunnitelma (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-160">Plan (required)</span></span>
- <span data-ttu-id="c36b5-161">Tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-161">Type (required)</span></span>
- <span data-ttu-id="c36b5-162">Vaihtoehto (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-162">Option (required)</span></span>
- <span data-ttu-id="c36b5-163">Edun tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-163">Benefit ID (required)</span></span>
- <span data-ttu-id="c36b5-164">Tiheys</span><span class="sxs-lookup"><span data-stu-id="c36b5-164">Frequency</span></span>
- <span data-ttu-id="c36b5-165">Peruste</span><span class="sxs-lookup"><span data-stu-id="c36b5-165">Basis</span></span>
- <span data-ttu-id="c36b5-166">Summa tai hinta</span><span class="sxs-lookup"><span data-stu-id="c36b5-166">Amount or rate</span></span>
- <span data-ttu-id="c36b5-167">Ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="c36b5-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="c36b5-168">Tuetut maksutiheydet</span><span class="sxs-lookup"><span data-stu-id="c36b5-168">Supported frequencies</span></span> 

- <span data-ttu-id="c36b5-169">Viikoittain</span><span class="sxs-lookup"><span data-stu-id="c36b5-169">Weekly</span></span>
- <span data-ttu-id="c36b5-170">Kahden viikon välein</span><span class="sxs-lookup"><span data-stu-id="c36b5-170">Bi-weekly</span></span>
- <span data-ttu-id="c36b5-171">Joka toinen kuukausi</span><span class="sxs-lookup"><span data-stu-id="c36b5-171">Semi-monthly</span></span>
- <span data-ttu-id="c36b5-172">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="c36b5-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="c36b5-173">Tuetut pohjat</span><span class="sxs-lookup"><span data-stu-id="c36b5-173">Supported bases</span></span> 

- <span data-ttu-id="c36b5-174">Kiinteä summa</span><span class="sxs-lookup"><span data-stu-id="c36b5-174">Fixed amount</span></span>
- <span data-ttu-id="c36b5-175">Ansioiden prosenttiosuus</span><span class="sxs-lookup"><span data-stu-id="c36b5-175">Percent of earnings</span></span>
- <span data-ttu-id="c36b5-176">Tuottavat tunnit</span><span class="sxs-lookup"><span data-stu-id="c36b5-176">Productive hours</span></span>

<span data-ttu-id="c36b5-177">Dayforce luo seuraavat vähennykset, jotka perustuvat palkanlaskennan vaikutukseen, joka on määritelty etusuunnitelmassa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="c36b5-178">Valinta Human Resourcesissa</span><span class="sxs-lookup"><span data-stu-id="c36b5-178">Selection in Human Resources</span></span>        | <span data-ttu-id="c36b5-179">Tulos Dayforcessa</span><span class="sxs-lookup"><span data-stu-id="c36b5-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="c36b5-180">Ei ole</span><span class="sxs-lookup"><span data-stu-id="c36b5-180">None</span></span>                       | <span data-ttu-id="c36b5-181">Vähennyksiä ei luoda.</span><span class="sxs-lookup"><span data-stu-id="c36b5-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="c36b5-182">Vain vähennys</span><span class="sxs-lookup"><span data-stu-id="c36b5-182">Deduction only</span></span>             | <span data-ttu-id="c36b5-183">Työntekijävähennys on luotu.</span><span class="sxs-lookup"><span data-stu-id="c36b5-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="c36b5-184">Vain osuus</span><span class="sxs-lookup"><span data-stu-id="c36b5-184">Contribution only</span></span>          | <span data-ttu-id="c36b5-185">Työnantajavähennys on luotu.</span><span class="sxs-lookup"><span data-stu-id="c36b5-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="c36b5-186">Vähennys ja osuus</span><span class="sxs-lookup"><span data-stu-id="c36b5-186">Deduction and contribution</span></span> | <span data-ttu-id="c36b5-187">Työntekijän ja työnantajan vähennykset luodaan.</span><span class="sxs-lookup"><span data-stu-id="c36b5-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="c36b5-188">Lisätietoja etuohjelman määrittämisestä ja hallitsemisesta seuraavissa artikkeleissa:</span><span class="sxs-lookup"><span data-stu-id="c36b5-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="c36b5-189">Työsuhde-etuusohjelman toteuttaminen</span><span class="sxs-lookup"><span data-stu-id="c36b5-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="c36b5-190">Luo uusi etu</span><span class="sxs-lookup"><span data-stu-id="c36b5-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="c36b5-191">Määritä edun oikeutussäännöt ja -käytännöt</span><span class="sxs-lookup"><span data-stu-id="c36b5-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="c36b5-192">Rekisteröi etuja työntekijöille ja poista niitä</span><span class="sxs-lookup"><span data-stu-id="c36b5-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="c36b5-193">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="c36b5-193">Compensation</span></span> 

<span data-ttu-id="c36b5-194">Kompensaationhallinnan avulla ohjataan peruspalkan ja palkkioiden maksamista.</span><span class="sxs-lookup"><span data-stu-id="c36b5-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="c36b5-195">Työntekijän kiinteän peruspalkan ja bonusten korotuksia hallitaan kiinteän kompensaatiosuunnitelmien avulla.</span><span class="sxs-lookup"><span data-stu-id="c36b5-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="c36b5-196">Bonusmaksujen, suorituskykypalkkioiden, optioiden, lahjoitusten sekä muiden kannusteiden maksamista hallitaan muuttuvan kompensaation suunnitelmien avulla.</span><span class="sxs-lookup"><span data-stu-id="c36b5-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="c36b5-197">Dayforce käyttää kompensaatiotietoja laskeakseen työntekijän tunti- tai vuosihinnan.</span><span class="sxs-lookup"><span data-stu-id="c36b5-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="c36b5-198">Kiinteät kompensaatiosuunnitelmat ja palkkojen muunnokset vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="c36b5-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="c36b5-199">Työntekijöiden täytyy olla liitettynä kiinteään kompensaatiosuunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="c36b5-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="c36b5-200">Katso lisätietoja kompensaatiosuunnitelmista seuraavista artikkeleista:</span><span class="sxs-lookup"><span data-stu-id="c36b5-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="c36b5-201">Kiinteiden kompensaatiosuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="c36b5-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="c36b5-202">Muuttuvien kompensaatiosuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="c36b5-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="c36b5-203">Palkka- ja kompensaatiorakenteen ja -suunnitelmien kehittäminen</span><span class="sxs-lookup"><span data-stu-id="c36b5-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="c36b5-204">Kompensaation käsittely</span><span class="sxs-lookup"><span data-stu-id="c36b5-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="c36b5-205">Kompensaatioprosessin määrittäminen ja tulosten laskeminen</span><span class="sxs-lookup"><span data-stu-id="c36b5-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="c36b5-206">Työntekijän rekisteröiminen kiinteän kompensaation suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="c36b5-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="c36b5-207">Työntekijän rekisteröiminen muuttuvan kompensaation suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="c36b5-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="c36b5-208">Työt</span><span class="sxs-lookup"><span data-stu-id="c36b5-208">Jobs</span></span> 

<span data-ttu-id="c36b5-209">Työ sisältää tehtäviä ja vastuita, joita työn suorittajalta edellytetään.</span><span class="sxs-lookup"><span data-stu-id="c36b5-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="c36b5-210">Lisätietoja on seuraavissa artikkeleissa:</span><span class="sxs-lookup"><span data-stu-id="c36b5-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="c36b5-211">Työn komponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c36b5-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="c36b5-212">Uusien töiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c36b5-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="c36b5-213">Toimet</span><span class="sxs-lookup"><span data-stu-id="c36b5-213">Positions</span></span>

<span data-ttu-id="c36b5-214">Toimi on työn yksittäinen esiintymä.</span><span class="sxs-lookup"><span data-stu-id="c36b5-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="c36b5-215">Esimerkiksi toimi Myyntipäällikkö (Itä) on yksi Myyntipäällikkö-työhön liittyvistä toimista.</span><span class="sxs-lookup"><span data-stu-id="c36b5-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="c36b5-216">Osastolla on toimi.</span><span class="sxs-lookup"><span data-stu-id="c36b5-216">A position exists in a department.</span></span> <span data-ttu-id="c36b5-217">Vain yksi työntekijä voidaan liittää yhteen toimeen.</span><span class="sxs-lookup"><span data-stu-id="c36b5-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="c36b5-218">Muista seuraavat tiedot ja määritykset, kun määrität toimia:</span><span class="sxs-lookup"><span data-stu-id="c36b5-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="c36b5-219">Toimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-219">Position (required)</span></span>
- <span data-ttu-id="c36b5-220">Kuvaus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-220">Description (required)</span></span>
- <span data-ttu-id="c36b5-221">Työ (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-221">Job (required)</span></span>
- <span data-ttu-id="c36b5-222">Osasto (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-222">Department (required)</span></span>
- <span data-ttu-id="c36b5-223">Toimen tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-223">Position type (required)</span></span>
- <span data-ttu-id="c36b5-224">Kokopäiväinen (FTE)</span><span class="sxs-lookup"><span data-stu-id="c36b5-224">Full-time equivalent</span></span>
- <span data-ttu-id="c36b5-225">Vuosittaiset vakiotunnit (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="c36b5-226">Yrityksen maksama (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="c36b5-227">Maksujakson (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-227">Pay cycle (required)</span></span>
- <span data-ttu-id="c36b5-228">Oletusarvo taloushallinnon dimensio – kustannuspaikka (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="c36b5-229">Työntekijän määritys – työntekijä, tehtävän alkamisaika, tehtävän lopetusaika, syykoodi</span><span class="sxs-lookup"><span data-stu-id="c36b5-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="c36b5-230">Mikäli useita toimia samalla osastolla liittyy samaan työhön, ne yhdistetään yhteen toimeen Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="c36b5-231">Lisätietoja on seuraavissa artikkeleissa:</span><span class="sxs-lookup"><span data-stu-id="c36b5-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="c36b5-232">Työvoiman järjestäminen osastojen, töiden ja toimien avulla</span><span class="sxs-lookup"><span data-stu-id="c36b5-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="c36b5-233">Toimien määritys</span><span class="sxs-lookup"><span data-stu-id="c36b5-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="c36b5-234">Osastot</span><span class="sxs-lookup"><span data-stu-id="c36b5-234">Departments</span></span>

<span data-ttu-id="c36b5-235">Osasto on toimintayksikkö, joka vastaa organisaation luokkaa tai liiketoiminta-aluetta.</span><span class="sxs-lookup"><span data-stu-id="c36b5-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="c36b5-236">Osasto on vastuussa määrätystä organisaation alueesta, kuten myynnistä, kirjanpidosta tai henkilöstöhallinnosta.</span><span class="sxs-lookup"><span data-stu-id="c36b5-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="c36b5-237">Voit käyttää osastoja toiminnallisia alueita koskevaan raportointiin.</span><span class="sxs-lookup"><span data-stu-id="c36b5-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="c36b5-238">Osastot voivat olla tulosvastuullisia.</span><span class="sxs-lookup"><span data-stu-id="c36b5-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="c36b5-239">Lisätietoja on seuraavissa artikkeleissa:</span><span class="sxs-lookup"><span data-stu-id="c36b5-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="c36b5-240">Osaston luominen ja liittäminen osastohierarkiaan</span><span class="sxs-lookup"><span data-stu-id="c36b5-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="c36b5-241">Määritä uudet osastot</span><span class="sxs-lookup"><span data-stu-id="c36b5-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="c36b5-242">Maksujaksot ja maksukaudet</span><span class="sxs-lookup"><span data-stu-id="c36b5-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="c36b5-243">Palkkajakso määrittää kuinka usein palkkalistoja käytetään, ja minä tiettyinä päivinä työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="c36b5-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="c36b5-244">Esimerkiksi palkkajakso voi olla kuukausittainen ja työntekijöille voidaan maksaa kuukauden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="c36b5-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="c36b5-245">Vaihtoehtoisesti palkkajakso voi olla viikoittainen ja työntekijöille voidaan maksaa tiistaina palkkajakson päätyttyä.</span><span class="sxs-lookup"><span data-stu-id="c36b5-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="c36b5-246">Palkkajaksot on osoitettu toimiin, jotta voidaan valvoa milloin näissä tehtävissä oleville työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="c36b5-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="c36b5-247">Luotuasi palkkajaksoja, voit luoda maksukausia kullekin jaksolle.</span><span class="sxs-lookup"><span data-stu-id="c36b5-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="c36b5-248">Jokaisella palkkakaudella on maksun oletuspäivämäärä, joka perustuu antamiisi tietoihin.</span><span class="sxs-lookup"><span data-stu-id="c36b5-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="c36b5-249">Voit kuitenkin muokata maksun oletuspäivämäärää salliaksesi poikkeuksia, kuten kun maksupäivämäärä osuu vapaapäivälle.</span><span class="sxs-lookup"><span data-stu-id="c36b5-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="c36b5-250">Dayforcessa käytetään seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="c36b5-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="c36b5-251">Maksujakson (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-251">Pay cycle (required)</span></span>
- <span data-ttu-id="c36b5-252">Maksujakson tiheys (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="c36b5-253">Kauden alkamispäivä (ensimmäinen palkkakausi vaaditaan)</span><span class="sxs-lookup"><span data-stu-id="c36b5-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="c36b5-254">Oletusmaksupäivä (ensimmäinen palkkakausi vaaditaan)</span><span class="sxs-lookup"><span data-stu-id="c36b5-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="c36b5-255">Nämä tiedot on integroitu Dayforce-palkkaryhmien kanssa ja eriteltynä eriteltyinä maittain tai alueittain kullekin maksujaksolle.</span><span class="sxs-lookup"><span data-stu-id="c36b5-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="c36b5-256">Ennen integraatiota on luotava vähintään yksi palkkakausi.</span><span class="sxs-lookup"><span data-stu-id="c36b5-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="c36b5-257">Dayforce luo maksuryhmäkalentereita ja maksupäiviä, jotka perustuvat ensimmäisen palkkakauden alkamispäivämäärään ja määritetty oletusmaksupäivä on asetettu Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="c36b5-258">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="c36b5-258">Earning codes</span></span>

<span data-ttu-id="c36b5-259">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="c36b5-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c36b5-260">Tunnuksissa on erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="c36b5-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="c36b5-261">Dayforcessa käytetään seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="c36b5-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="c36b5-262">Ansiokoodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-262">Earning Code (required)</span></span>
- <span data-ttu-id="c36b5-263">kuvaus</span><span class="sxs-lookup"><span data-stu-id="c36b5-263">Description</span></span>
- <span data-ttu-id="c36b5-264">Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="c36b5-264">Unit of measure</span></span>
- <span data-ttu-id="c36b5-265">Tuottava</span><span class="sxs-lookup"><span data-stu-id="c36b5-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="c36b5-266">Työntekijän tiedot</span><span class="sxs-lookup"><span data-stu-id="c36b5-266">Worker data</span></span>

<span data-ttu-id="c36b5-267">Tietueet eri työntekijöille, joita sinulla on ovat tärkeitä henkilöstöhallinnossa ja palkanlaskentajärjestelmissä.</span><span class="sxs-lookup"><span data-stu-id="c36b5-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="c36b5-268">Tietueisiin lisättäviä tietoja käytetään työntekijöiden ja henkilökohtaisten tietojen seurannassa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="c36b5-269">Voit ylläpitää työntekijöille seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="c36b5-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="c36b5-270">**Perustiedot** – Ylläpidä työntekijän perustietoja, kuten yhteystiedot, demografiatiedot, tunnistetiedot, perheen tiedot, asevelvollisuuden tila, ekspatriaatin tiedot ja omat yhteyshenkilöt ja hätäyhteyshenkilöt.</span><span class="sxs-lookup"><span data-stu-id="c36b5-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="c36b5-271">**Työsuhde** – Ylläpidä tietoja työntekijän työsuhteesta, kuten yrityksen tai organisaation kytköksistä, toimen määrityksestä, aloitus- ja päättymispäivämääristä, työkelpoisuudesta, työehdoista, eläkkestä, lomista ja uudelleensijoittumisesta.</span><span class="sxs-lookup"><span data-stu-id="c36b5-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="c36b5-272">**Lomat ja poissaolot** –Ylläpidä tietoa työntekijän poissaoloista, kuten työaikakalentereista, poissaolotapahtumista ja poissaoloasetuksista.</span><span class="sxs-lookup"><span data-stu-id="c36b5-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="c36b5-273">**Kompensaatio ja palkanlaskenta** – Ylläpidä työntekijän kompensaatiosuunnitelmien tietoja ja palkanlaskentatietoja, kuten suunnitelmien toteutuminen, palkkiot, suorituskyky, provisio, verotiedot, eläkkeelle jääminen ja palkan vähennykset.</span><span class="sxs-lookup"><span data-stu-id="c36b5-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="c36b5-274">Kirjoittaessasi työntekijätietoja, pidä mielessä seuraavat tiedot ja konfiguraatiot, joita käytetään Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="c36b5-275">Yleistiedot</span><span class="sxs-lookup"><span data-stu-id="c36b5-275">General information</span></span>

- <span data-ttu-id="c36b5-276">Henkilönumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-276">Personnel number (required)</span></span>
- <span data-ttu-id="c36b5-277">Etunimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-277">First name (required)</span></span>
- <span data-ttu-id="c36b5-278">Sukunimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-278">Last name (required)</span></span>
- <span data-ttu-id="c36b5-279">Toinen nimi</span><span class="sxs-lookup"><span data-stu-id="c36b5-279">Middle name</span></span>
- <span data-ttu-id="c36b5-280">Ikälisäpäivä</span><span class="sxs-lookup"><span data-stu-id="c36b5-280">Seniority date</span></span>
- <span data-ttu-id="c36b5-281">Tunnetaan nimellä</span><span class="sxs-lookup"><span data-stu-id="c36b5-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="c36b5-282">Henkilökohtaiset tiedot</span><span class="sxs-lookup"><span data-stu-id="c36b5-282">Personal information</span></span>

- <span data-ttu-id="c36b5-283">Siviilisääty (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-283">Marital status (required)</span></span>
- <span data-ttu-id="c36b5-284">Syntymäpäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-284">Birth date (required)</span></span>
- <span data-ttu-id="c36b5-285">Sukupuoli (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-285">Gender (required)</span></span>
- <span data-ttu-id="c36b5-286">Henkilö on invalidi</span><span class="sxs-lookup"><span data-stu-id="c36b5-286">Person with disabilities</span></span>
- <span data-ttu-id="c36b5-287">Kansalaisuus, maa, alue (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="c36b5-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="c36b5-288">Osoitetiedot</span><span class="sxs-lookup"><span data-stu-id="c36b5-288">Address information</span></span>

- <span data-ttu-id="c36b5-289">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-289">Primary (required)</span></span>
- <span data-ttu-id="c36b5-290">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-290">Country/region (required)</span></span>
- <span data-ttu-id="c36b5-291">Postinumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-291">Postal code (required)</span></span>
- <span data-ttu-id="c36b5-292">Kadunnumero (pakollinen) (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="c36b5-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="c36b5-293">Rakennusta koskeva lisätieto (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="c36b5-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="c36b5-294">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-294">City (required)</span></span>
- <span data-ttu-id="c36b5-295">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-295">State (required)</span></span>
- <span data-ttu-id="c36b5-296">Lääni (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="c36b5-297">Yhteystiedot</span><span class="sxs-lookup"><span data-stu-id="c36b5-297">Contact information</span></span> 

- <span data-ttu-id="c36b5-298">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-298">Primary (required)</span></span>
- <span data-ttu-id="c36b5-299">Yhteystiedon numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-299">Contact number (required)</span></span>
- <span data-ttu-id="c36b5-300">Alanumero</span><span class="sxs-lookup"><span data-stu-id="c36b5-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="c36b5-301">Palkanlaskentatiedot ja ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="c36b5-301">Payroll information and earning codes</span></span>

<span data-ttu-id="c36b5-302">Työntekijöille voidaan antaa erityisiä tuloja tietyllä maksutaajuudella ja toivotulla maksutavalla.</span><span class="sxs-lookup"><span data-stu-id="c36b5-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="c36b5-303">Seuraavia kenttiä käytetään Dayforcessa sen varmistamiseksi, että näitä määrityksiä ja asetuksia käytetään.</span><span class="sxs-lookup"><span data-stu-id="c36b5-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="c36b5-304">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="c36b5-304">Earning codes</span></span>

- <span data-ttu-id="c36b5-305">Toimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-305">Position (required)</span></span>
- <span data-ttu-id="c36b5-306">Ansiokoodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-306">Earning Code (required)</span></span>
- <span data-ttu-id="c36b5-307">Taajuus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-307">Frequency (required)</span></span>
- <span data-ttu-id="c36b5-308">Summa (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="c36b5-309">Palkanlaskentatiedot</span><span class="sxs-lookup"><span data-stu-id="c36b5-309">Payroll information</span></span>

- <span data-ttu-id="c36b5-310">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="c36b5-310">Payment Method</span></span>
- <span data-ttu-id="c36b5-311">Talousalue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-311">Economic Region (required)</span></span>
- <span data-ttu-id="c36b5-312">Työsuhde-etujen tunnus</span><span class="sxs-lookup"><span data-stu-id="c36b5-312">Employee Benefits ID</span></span>
- <span data-ttu-id="c36b5-313">Kansallinen/alueellinen tunnusnumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-313">National ID Number (required)</span></span>
- <span data-ttu-id="c36b5-314">Sotilaspalveluksen numero</span><span class="sxs-lookup"><span data-stu-id="c36b5-314">Military Service Number</span></span>
- <span data-ttu-id="c36b5-315">Vuoron tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-315">Shift ID (required)</span></span>
- <span data-ttu-id="c36b5-316">Veronumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-316">Tax Number (required)</span></span>
- <span data-ttu-id="c36b5-317">Ammattijärjestön tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-317">Union ID (required)</span></span>
- <span data-ttu-id="c36b5-318">Työpäivän tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-318">Work Day ID (required)</span></span>
- <span data-ttu-id="c36b5-319">Työluvan numero</span><span class="sxs-lookup"><span data-stu-id="c36b5-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="c36b5-320">Maksutavoista Meksiko tukee seuraavia: **Käteinen**, **shekki** (yrityksen fyysinen shekki) ja **sähköinen maksu**.</span><span class="sxs-lookup"><span data-stu-id="c36b5-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="c36b5-321">Mikäli maksutapaa ei ole määritetty, **shekki** on oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="c36b5-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="c36b5-322">Työsuhteen tiedot</span><span class="sxs-lookup"><span data-stu-id="c36b5-322">Employment details</span></span>

<span data-ttu-id="c36b5-323">Työntekijöiden yksityiskohtaista historiaa käytetään keskeisenä informaationa, jolla saadaan työntekijän palkkaus, irtisanominen ja rekrytointitilastot Dayforcesta.</span><span class="sxs-lookup"><span data-stu-id="c36b5-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="c36b5-324">Dayforce tukee kerrallaan vain yhtä aktiivisen työntekijän tietuetta.</span><span class="sxs-lookup"><span data-stu-id="c36b5-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="c36b5-325">Työsuhteen alkamispäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-325">Employment start date (required)</span></span>
- <span data-ttu-id="c36b5-326">Työsuhteen päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="c36b5-326">Employment end date</span></span>
- <span data-ttu-id="c36b5-327">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="c36b5-327">Start date</span></span>
- <span data-ttu-id="c36b5-328">Muutettu aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="c36b5-328">Adjusted start date</span></span>
- <span data-ttu-id="c36b5-329">Työsuhteen päättymispäivä (pakollinen päättyessä)</span><span class="sxs-lookup"><span data-stu-id="c36b5-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="c36b5-330">Työsuhteen päättymissyy (pakollinen päättyessä)</span><span class="sxs-lookup"><span data-stu-id="c36b5-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="c36b5-331">Seuraavien tietojen avulla lasketaan työntekijän tärkeimmät päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="c36b5-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="c36b5-332">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="c36b5-332">Human Resources</span></span>                | <span data-ttu-id="c36b5-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c36b5-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c36b5-334">Viimeisimmän työhönoton päivämäärä</span><span class="sxs-lookup"><span data-stu-id="c36b5-334">Most recent hire date</span></span> | <span data-ttu-id="c36b5-335">Työntekijän työsuhteen alku voimassa olevassa työhistoriatietueessa</span><span class="sxs-lookup"><span data-stu-id="c36b5-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="c36b5-336">Työsuhteen loppumispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="c36b5-336">Termination date</span></span>      | <span data-ttu-id="c36b5-337">Työntekijän työsuhteen loppu voimassa olevassa työhistoriatietueessa</span><span class="sxs-lookup"><span data-stu-id="c36b5-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="c36b5-338">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="c36b5-338">Start date</span></span>            | <span data-ttu-id="c36b5-339">Muutettu alkamispäivämäärä, alkamispäivämäärä tai työsuhteen alku ei-aktiivisessa työsuhteen historiatietueessa</span><span class="sxs-lookup"><span data-stu-id="c36b5-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="c36b5-340">Alkuperäinen työsuhteen alkamispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="c36b5-340">Original hire date</span></span>    | <span data-ttu-id="c36b5-341">Varhaisin työhistoriatietueen työsuhteen alku</span><span class="sxs-lookup"><span data-stu-id="c36b5-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="c36b5-342">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="c36b5-342">Compensation</span></span>

<span data-ttu-id="c36b5-343">Kiinteän kompensaatiosuunnitelmaan tulee liittää jokaisen työntekijän ensisijainen toimi koko työsuhteen ajalla.</span><span class="sxs-lookup"><span data-stu-id="c36b5-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="c36b5-344">Ajanjakso alkaa siitä päivämäärästä, jona työntekijä palkattiin (tai työsuhteen alkamispäivämäärä) ja jatkuu, kunnes työsuhde loppuu.</span><span class="sxs-lookup"><span data-stu-id="c36b5-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="c36b5-345">Voimaantulopäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-345">Effective Date (required)</span></span>
- <span data-ttu-id="c36b5-346">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="c36b5-346">Expiration date</span></span>
- <span data-ttu-id="c36b5-347">Palkkio (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-347">Pay Rate (required)</span></span>
- <span data-ttu-id="c36b5-348">Palkkion muunnokset (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="c36b5-349">Vuosittainen arvo (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="c36b5-350">Tunnittainen arvo (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="c36b5-351">Mikäli tuntityöntekijällä on useita toimia, ensisijaisen toimen kiinteä kompensaation tuodaan Dayforceen työntekijätason hinta-/peruspalkkana.</span><span class="sxs-lookup"><span data-stu-id="c36b5-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="c36b5-352">Ei-ensisijaisten toimien tuntihinta tallennetaan Dayforcen vastaavaan sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="c36b5-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="c36b5-353">Mikäli palkallisella työntekijällä on useita toimia, kumulatiivinen tuntihinta ja vuosittainen palkka kaikista aktiivisista toimista johdetaan ja käytetään työntekijätason hinta-/peruspalkkana.</span><span class="sxs-lookup"><span data-stu-id="c36b5-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="c36b5-354">Tunnusnumerot</span><span class="sxs-lookup"><span data-stu-id="c36b5-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="c36b5-355">Sosiaaliturvan tunniste</span><span class="sxs-lookup"><span data-stu-id="c36b5-355">Social Security identifier</span></span> 

<span data-ttu-id="c36b5-356">Jokaisella työntekijä on oltava yksi ensisijainen tunnus.</span><span class="sxs-lookup"><span data-stu-id="c36b5-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="c36b5-357">Tunnuksen on oltava **SSN**-tunnus.</span><span class="sxs-lookup"><span data-stu-id="c36b5-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="c36b5-358">Dayforcessa se johdetaan automaattisesti työntekijän sosiaaliturvatunnuksesta, jota tarvitaan työsuhdetta solmittaessa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="c36b5-359">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-359">Primary (required)</span></span>
- <span data-ttu-id="c36b5-360">Tunnuksen tyyppi = "Henkilötunnus"</span><span class="sxs-lookup"><span data-stu-id="c36b5-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="c36b5-361">Myöntämispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="c36b5-361">Issued Date</span></span>
- <span data-ttu-id="c36b5-362">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="c36b5-362">Expiration Date</span></span>

<span data-ttu-id="c36b5-363">Työntekijät voi määrittää useita tunnistenumeroita **SSN**-tunnuksesta (henkilötunnus).</span><span class="sxs-lookup"><span data-stu-id="c36b5-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="c36b5-364">Tietue, joka on merkitty **Ensisijainen** on integroitu Dayforceen, riippumatta siitä, onko numero aktiivinen tai vanhentunut.</span><span class="sxs-lookup"><span data-stu-id="c36b5-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="c36b5-365">Pankkitilit ja suoritukset</span><span class="sxs-lookup"><span data-stu-id="c36b5-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="c36b5-366">Voimassa olevat pankkitilitiedot on kirjattava kaikille työntekijöille, jotka haluavat, että hänelle maksetaan pankkisiirtona.</span><span class="sxs-lookup"><span data-stu-id="c36b5-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="c36b5-367">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="c36b5-367">Human Resources</span></span>                         | <span data-ttu-id="c36b5-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c36b5-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c36b5-369">Pankkitilin numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="c36b5-370">SWIFT-koodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-370">SWIFT code (required)</span></span>          | <span data-ttu-id="c36b5-371">**Pankkitunnus**-kenttä, jota käytetään, kun käsitellään palkkalistoja Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="c36b5-372">Sivuliikkeen numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="c36b5-373">Pankkitilin tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-373">Bank account type (required)</span></span>   | <span data-ttu-id="c36b5-374">**Tilityyppi**-kenttä, jota käytetään, kun käsitellään palkkalistoja Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="c36b5-375">Tuetut arvot sisältävät kohdat **Tarkistus** ja **Palkanlaskenta**.</span><span class="sxs-lookup"><span data-stu-id="c36b5-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="c36b5-376">Työntekijät, jotka haluavat, että heille maksetaan pankkisiirtona, on toimitettava linkki jäännöstilille, joka kuuluu oikeushenkilölle, jolla on ensisijainen osoite Meksikossa ja jolla on voimassa oleva tili meksikolaisessa pankissa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="c36b5-377">Kaikki muut jäljellä olevat tilit jätetään huomiotta.</span><span class="sxs-lookup"><span data-stu-id="c36b5-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="c36b5-378">Osoitetiedot</span><span class="sxs-lookup"><span data-stu-id="c36b5-378">Address information</span></span>

<span data-ttu-id="c36b5-379">Jokaisella työntekijällä on oltava yksi ensisijainen toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="c36b5-379">Every employee must have one primary location.</span></span> <span data-ttu-id="c36b5-380">Dayforcessa tätä sijaintia käytetään määrittämään työntekijän ensisijainen oleskelulupa verotusta varten.</span><span class="sxs-lookup"><span data-stu-id="c36b5-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="c36b5-381">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-381">Primary (required)</span></span>
- <span data-ttu-id="c36b5-382">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-382">Country/region (required)</span></span>
- <span data-ttu-id="c36b5-383">Postinumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="c36b5-384">Katuosoite (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-384">Street (required)</span></span>
- <span data-ttu-id="c36b5-385">Kadunnumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-385">Street Number (required)</span></span>
- <span data-ttu-id="c36b5-386">Rakennusta koskeva lisätieto</span><span class="sxs-lookup"><span data-stu-id="c36b5-386">Building Complement</span></span>
- <span data-ttu-id="c36b5-387">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-387">City (required)</span></span>
- <span data-ttu-id="c36b5-388">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-388">State (required)</span></span>
- <span data-ttu-id="c36b5-389">Lääni (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="c36b5-390">Määritä tiedot luodaksesi palkkalistoja Yhdysvalloissa ja Kanadassa</span><span class="sxs-lookup"><span data-stu-id="c36b5-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="c36b5-391">Jos luot maksuja työntekijöille, jotka ovat Yhdysvalloissa ja Kanadassa, seuraavat seikat on määritettävä:</span><span class="sxs-lookup"><span data-stu-id="c36b5-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="c36b5-392">Toimia varten vaaditaan osastot.</span><span class="sxs-lookup"><span data-stu-id="c36b5-392">Departments are required on positions.</span></span>
- <span data-ttu-id="c36b5-393">Kustannuspaikat on määritettävä taloushallinnon dimensioina ja niiden pitää olla ensimmäisenä osana merkkijonoa oletusarvoisessa taloushallinnon dimensiossa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="c36b5-394">Voit määrittää Human Resourcesin edellyttämään, että toimet määrittävät osaston.</span><span class="sxs-lookup"><span data-stu-id="c36b5-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="c36b5-395">Tehdäksesi tämän valitse **Henkilöstöhallinnon jaetut toimet > Toimet > Edellytä osastoja toimissa**.</span><span class="sxs-lookup"><span data-stu-id="c36b5-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="c36b5-396">Suosittelemme, että tämä asetus otetaan käyttöön integrointia varten.</span><span class="sxs-lookup"><span data-stu-id="c36b5-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="c36b5-397">Työtyypit</span><span class="sxs-lookup"><span data-stu-id="c36b5-397">Job types</span></span>

<span data-ttu-id="c36b5-398">Työtyyppien avulla voi luokitella samankaltaisia töitä.</span><span class="sxs-lookup"><span data-stu-id="c36b5-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="c36b5-399">Työlajit ovat pakollisia palkanlaskennan käsittelemiseksi Yhdysvalloissa ja Kanadassa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="c36b5-400">Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka.</span><span class="sxs-lookup"><span data-stu-id="c36b5-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="c36b5-401">Työlajit on yhdistetty Dayforceen maksulajeina, jotka ilmaisevat, onko työntekijällä tuntipalkka vai kuukausipalkka.</span><span class="sxs-lookup"><span data-stu-id="c36b5-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="c36b5-402">Tarvitaan seuraavat työlajit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="c36b5-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="c36b5-403">Työlaji</span><span class="sxs-lookup"><span data-stu-id="c36b5-403">Job type</span></span>   | <span data-ttu-id="c36b5-404">kuvaus</span><span class="sxs-lookup"><span data-stu-id="c36b5-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="c36b5-405">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="c36b5-405">Hourly</span></span>     | <span data-ttu-id="c36b5-406">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="c36b5-406">Hourly</span></span>      |
| <span data-ttu-id="c36b5-407">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="c36b5-407">Salaried</span></span>   | <span data-ttu-id="c36b5-408">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="c36b5-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="c36b5-409">Toimityypit</span><span class="sxs-lookup"><span data-stu-id="c36b5-409">Position types</span></span> 

<span data-ttu-id="c36b5-410">Voit käyttää toimityyppejä kuvaamaan, onko toimi kokoaikainen, osa-aikainen vai jokin muu.</span><span class="sxs-lookup"><span data-stu-id="c36b5-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="c36b5-411">Toimityypit on yhdistetty Dayforceen maksuluokkina, jotka ilmaisevat, onko työntekijä koko- vai osa-aikainen.</span><span class="sxs-lookup"><span data-stu-id="c36b5-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="c36b5-412">Tarvitaan seuraavat toimityypit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="c36b5-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="c36b5-413">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="c36b5-413">Position type</span></span>   | <span data-ttu-id="c36b5-414">kuvaus</span><span class="sxs-lookup"><span data-stu-id="c36b5-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="c36b5-415">Kokoaikainen</span><span class="sxs-lookup"><span data-stu-id="c36b5-415">Full-time</span></span>       | <span data-ttu-id="c36b5-416">Kokopäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-416">Full time employee</span></span> |
| <span data-ttu-id="c36b5-417">Osa-aikainen</span><span class="sxs-lookup"><span data-stu-id="c36b5-417">Part-time</span></span>       | <span data-ttu-id="c36b5-418">Osapäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="c36b5-419">Syykoodit</span><span class="sxs-lookup"><span data-stu-id="c36b5-419">Reason codes</span></span>

<span data-ttu-id="c36b5-420">Syykoodit antavat tietoja työntekijän tilasta</span><span class="sxs-lookup"><span data-stu-id="c36b5-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="c36b5-421">Syykoodit määritetään Dayforceen tilan syinä, jotka ilmaisevat muutokset työntekijän toimessa tai työsuhteessa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="c36b5-422">Tarvitaan seuraavat syykoodit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="c36b5-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="c36b5-423">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="c36b5-423">Reason code</span></span>    | <span data-ttu-id="c36b5-424">kuvaus</span><span class="sxs-lookup"><span data-stu-id="c36b5-424">Description</span></span>      | <span data-ttu-id="c36b5-425">Soveltuvat skenaariot</span><span class="sxs-lookup"><span data-stu-id="c36b5-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="c36b5-426">EROAMINEN</span><span class="sxs-lookup"><span data-stu-id="c36b5-426">RESIGNATION</span></span>    | <span data-ttu-id="c36b5-427">Eroaminen</span><span class="sxs-lookup"><span data-stu-id="c36b5-427">Resignation</span></span>      | <span data-ttu-id="c36b5-428">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-428">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-429">IRTISANOMINEN</span><span class="sxs-lookup"><span data-stu-id="c36b5-429">TERMINATION</span></span>    | <span data-ttu-id="c36b5-430">Irtisanominen</span><span class="sxs-lookup"><span data-stu-id="c36b5-430">Termination</span></span>      | <span data-ttu-id="c36b5-431">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-431">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-432">ELÄKKEELLE SIIRTYMINEN</span><span class="sxs-lookup"><span data-stu-id="c36b5-432">RETIREMENT</span></span>     | <span data-ttu-id="c36b5-433">Eläkkeelle siirtyminen</span><span class="sxs-lookup"><span data-stu-id="c36b5-433">Retirement</span></span>       | <span data-ttu-id="c36b5-434">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-434">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-435">MUU</span><span class="sxs-lookup"><span data-stu-id="c36b5-435">OTHER</span></span>          | <span data-ttu-id="c36b5-436">Muut syyt</span><span class="sxs-lookup"><span data-stu-id="c36b5-436">Other Reasons</span></span>    | <span data-ttu-id="c36b5-437">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-437">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-438">KUOLEMA</span><span class="sxs-lookup"><span data-stu-id="c36b5-438">DEATH</span></span>          | <span data-ttu-id="c36b5-439">Kuolema</span><span class="sxs-lookup"><span data-stu-id="c36b5-439">Death</span></span>            | <span data-ttu-id="c36b5-440">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-440">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-441">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="c36b5-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="c36b5-442">Virkavapaa</span><span class="sxs-lookup"><span data-stu-id="c36b5-442">Leave of Absence</span></span> | <span data-ttu-id="c36b5-443">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-443">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-444">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="c36b5-444">CONTRACTEND</span></span>    | <span data-ttu-id="c36b5-445">Sopimuksen päättyminen</span><span class="sxs-lookup"><span data-stu-id="c36b5-445">End of Contract</span></span>  | <span data-ttu-id="c36b5-446">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-446">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-447">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="c36b5-447">SALARYCHANGE</span></span>   | <span data-ttu-id="c36b5-448">Palkan muutos</span><span class="sxs-lookup"><span data-stu-id="c36b5-448">Change of Salary</span></span> | <span data-ttu-id="c36b5-449">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="c36b5-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="c36b5-450">Siviilisääty</span><span class="sxs-lookup"><span data-stu-id="c36b5-450">Marital status</span></span>

<span data-ttu-id="c36b5-451">Siviilisääty on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="c36b5-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c36b5-452">Seuraavassa taulukossa kuvataan, miten siviilisääty liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="c36b5-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="c36b5-453">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="c36b5-453">Human Resources</span></span>                 | <span data-ttu-id="c36b5-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c36b5-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="c36b5-455">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="c36b5-455">Married</span></span>                | <span data-ttu-id="c36b5-456">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="c36b5-456">Married</span></span>              |
| <span data-ttu-id="c36b5-457">Yksi</span><span class="sxs-lookup"><span data-stu-id="c36b5-457">Single</span></span>                 | <span data-ttu-id="c36b5-458">Yksi</span><span class="sxs-lookup"><span data-stu-id="c36b5-458">Single</span></span>               |
| <span data-ttu-id="c36b5-459">Leski</span><span class="sxs-lookup"><span data-stu-id="c36b5-459">Widowed</span></span>                | <span data-ttu-id="c36b5-460">Leski</span><span class="sxs-lookup"><span data-stu-id="c36b5-460">Widowed</span></span>              |
| <span data-ttu-id="c36b5-461">Eronnut</span><span class="sxs-lookup"><span data-stu-id="c36b5-461">Divorced</span></span>               | <span data-ttu-id="c36b5-462">Eronnut</span><span class="sxs-lookup"><span data-stu-id="c36b5-462">Divorced</span></span>             |
| <span data-ttu-id="c36b5-463">Rekisteröity suhde</span><span class="sxs-lookup"><span data-stu-id="c36b5-463">Registered Partnership</span></span> | <span data-ttu-id="c36b5-464">Kotimainen kumppanuus</span><span class="sxs-lookup"><span data-stu-id="c36b5-464">Domestic Partnership</span></span> |
| <span data-ttu-id="c36b5-465">None</span><span class="sxs-lookup"><span data-stu-id="c36b5-465">None</span></span>                   | <span data-ttu-id="c36b5-466">None</span><span class="sxs-lookup"><span data-stu-id="c36b5-466">None</span></span>                 |
| <span data-ttu-id="c36b5-467">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="c36b5-467">Cohabiting</span></span>             | <span data-ttu-id="c36b5-468">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="c36b5-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="c36b5-469">Sukupuoli</span><span class="sxs-lookup"><span data-stu-id="c36b5-469">Gender</span></span>

<span data-ttu-id="c36b5-470">Sukupuolinimitykset on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="c36b5-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c36b5-471">Seuraavassa taulukossa kuvataan, miten sukupuolinimitykset liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="c36b5-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="c36b5-472">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="c36b5-472">Human Resources</span></span>       | <span data-ttu-id="c36b5-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c36b5-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="c36b5-474">Mies</span><span class="sxs-lookup"><span data-stu-id="c36b5-474">Male</span></span>         | <span data-ttu-id="c36b5-475">Mies</span><span class="sxs-lookup"><span data-stu-id="c36b5-475">Male</span></span>            |
| <span data-ttu-id="c36b5-476">Nainen</span><span class="sxs-lookup"><span data-stu-id="c36b5-476">Female</span></span>       | <span data-ttu-id="c36b5-477">Nainen</span><span class="sxs-lookup"><span data-stu-id="c36b5-477">Female</span></span>          |
| <span data-ttu-id="c36b5-478">Yksilöimätön</span><span class="sxs-lookup"><span data-stu-id="c36b5-478">Non-specific</span></span> | <span data-ttu-id="c36b5-479">*Ei tueta*</span><span class="sxs-lookup"><span data-stu-id="c36b5-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="c36b5-480">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="c36b5-480">Earning codes</span></span>

<span data-ttu-id="c36b5-481">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="c36b5-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c36b5-482">Tunnukset kattavat erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="c36b5-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="c36b5-483">Mikäli käytetään ei-tuettua taajuutta **Jokainen palkka** -taajuutta käytetään oletusarvon mukaan laskelmissa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="c36b5-484">Tuetut maksutaajuudet</span><span class="sxs-lookup"><span data-stu-id="c36b5-484">Supported frequencies</span></span>

- <span data-ttu-id="c36b5-485">Kaikki</span><span class="sxs-lookup"><span data-stu-id="c36b5-485">All</span></span>
- <span data-ttu-id="c36b5-486">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="c36b5-486">EVERYPAY</span></span>
- <span data-ttu-id="c36b5-487">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="c36b5-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="c36b5-488">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="c36b5-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="c36b5-489">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="c36b5-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="c36b5-490">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-490">1OFMTH</span></span>
- <span data-ttu-id="c36b5-491">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-491">LASTOFMTH</span></span>
- <span data-ttu-id="c36b5-492">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-492">2OFMTH</span></span>
- <span data-ttu-id="c36b5-493">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-493">3OFMTH</span></span>
- <span data-ttu-id="c36b5-494">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-494">4OFMTH</span></span>
- <span data-ttu-id="c36b5-495">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-495">5OFMTH</span></span>
- <span data-ttu-id="c36b5-496">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-496">1N2OFMTH</span></span>
- <span data-ttu-id="c36b5-497">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-497">3N4OFMTH</span></span>
- <span data-ttu-id="c36b5-498">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-498">1N3OFMTH</span></span>
- <span data-ttu-id="c36b5-499">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-499">1N4OFMTH</span></span>
- <span data-ttu-id="c36b5-500">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-500">2N3OFMTH</span></span>
- <span data-ttu-id="c36b5-501">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-501">2N4OFMTH</span></span>
- <span data-ttu-id="c36b5-502">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="c36b5-503">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="c36b5-504">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="c36b5-505">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="c36b5-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="c36b5-507">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="c36b5-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="c36b5-508">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="c36b5-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="c36b5-509">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="c36b5-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="c36b5-510">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="c36b5-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="c36b5-511">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="c36b5-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="c36b5-512">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c36b5-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="c36b5-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c36b5-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="c36b5-514">Osoitteet</span><span class="sxs-lookup"><span data-stu-id="c36b5-514">Addresses</span></span>

<span data-ttu-id="c36b5-515">Määriteltyjen maiden tai alueiden, valtioiden ja läänin (kuntien) koodien tunnistaminen edellyttää tiettyjä muotoja, joita Dayforce ja maassa tai alueella olevat toimijat pystyvät tunnistamaan.</span><span class="sxs-lookup"><span data-stu-id="c36b5-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="c36b5-516">Vaikka kaupunkien muoto on joustava, jokainen paikkakunta täytyy liittää osavaltioon.</span><span class="sxs-lookup"><span data-stu-id="c36b5-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="c36b5-517">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="c36b5-517">Human Resources</span></span>          | <span data-ttu-id="c36b5-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c36b5-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="c36b5-519">Maa/alue</span><span class="sxs-lookup"><span data-stu-id="c36b5-519">Country/Region</span></span>  | <span data-ttu-id="c36b5-520">Maakoodi</span><span class="sxs-lookup"><span data-stu-id="c36b5-520">Country Code</span></span>          |
| <span data-ttu-id="c36b5-521">Postinumero</span><span class="sxs-lookup"><span data-stu-id="c36b5-521">Zip/Postal Code</span></span> | <span data-ttu-id="c36b5-522">Postinumero</span><span class="sxs-lookup"><span data-stu-id="c36b5-522">Postal Code</span></span>           |
| <span data-ttu-id="c36b5-523">Alue</span><span class="sxs-lookup"><span data-stu-id="c36b5-523">State</span></span>           | <span data-ttu-id="c36b5-524">Aluekoodi</span><span class="sxs-lookup"><span data-stu-id="c36b5-524">State Code</span></span>            |
| <span data-ttu-id="c36b5-525">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="c36b5-525">City</span></span>            | <span data-ttu-id="c36b5-526">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="c36b5-526">City</span></span>                  |
| <span data-ttu-id="c36b5-527">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="c36b5-527">County</span></span>          | <span data-ttu-id="c36b5-528">Lääni (kunta)</span><span class="sxs-lookup"><span data-stu-id="c36b5-528">County (Municipality)</span></span> |
| <span data-ttu-id="c36b5-529">Katu</span><span class="sxs-lookup"><span data-stu-id="c36b5-529">Street</span></span>          | <span data-ttu-id="c36b5-530">Osoiterivi 1</span><span class="sxs-lookup"><span data-stu-id="c36b5-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="c36b5-531">Verotusalueet</span><span class="sxs-lookup"><span data-stu-id="c36b5-531">Tax regions</span></span>

<span data-ttu-id="c36b5-532">Verotusalueita käytetään palkanlaskennan muodostamisessa käytettävän veron määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="c36b5-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="c36b5-533">ALV-alueet yhdistetään Dayforceen toimipaikan osoitteina.</span><span class="sxs-lookup"><span data-stu-id="c36b5-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="c36b5-534">Oletusarvoinen verotusalue on liitettävä työntekijän aktiiviseen toimeen.</span><span class="sxs-lookup"><span data-stu-id="c36b5-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="c36b5-535">Verotusalue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-535">Tax region (required)</span></span>
- <span data-ttu-id="c36b5-536">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-536">Country/Region (required)</span></span>
- <span data-ttu-id="c36b5-537">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-537">State (required)</span></span>
- <span data-ttu-id="c36b5-538">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="c36b5-538">County</span></span> 
- <span data-ttu-id="c36b5-539">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="c36b5-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="c36b5-540">Määritä tietosi tuottaaksesi palkkalistoja Meksikossa</span><span class="sxs-lookup"><span data-stu-id="c36b5-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="c36b5-541">Jos luot maksuja työntekijöille, jotka ovat Meksikossa, seuraavat seikat on määritettävä:</span><span class="sxs-lookup"><span data-stu-id="c36b5-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="c36b5-542">Toimia varten vaaditaan osastot.</span><span class="sxs-lookup"><span data-stu-id="c36b5-542">Departments are required on positions.</span></span>
- <span data-ttu-id="c36b5-543">Kustannuspaikat on määritettävä taloushallinnon dimensioina ja niiden pitää olla ensimmäisenä osana merkkijonoa oletusarvoisessa taloushallinnon dimensiossa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="c36b5-544">Työtyypit</span><span class="sxs-lookup"><span data-stu-id="c36b5-544">Job types</span></span>

<span data-ttu-id="c36b5-545">Työtyyppien avulla voi luokitella samankaltaisia töitä.</span><span class="sxs-lookup"><span data-stu-id="c36b5-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="c36b5-546">Työlajit ovat pakollisia palkkalistojen käsittelemiseen Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="c36b5-547">Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka.</span><span class="sxs-lookup"><span data-stu-id="c36b5-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="c36b5-548">Työlajit on yhdistetty Dayforceen maksulajeina, jotka ilmaisevat, onko työntekijällä tuntipalkka vai kuukausipalkka.</span><span class="sxs-lookup"><span data-stu-id="c36b5-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="c36b5-549">Tarvitaan seuraavat työlajit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="c36b5-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="c36b5-550">Työlaji</span><span class="sxs-lookup"><span data-stu-id="c36b5-550">Job type</span></span>   | <span data-ttu-id="c36b5-551">kuvaus</span><span class="sxs-lookup"><span data-stu-id="c36b5-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="c36b5-552">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="c36b5-552">Hourly</span></span>     | <span data-ttu-id="c36b5-553">MX tunneittain</span><span class="sxs-lookup"><span data-stu-id="c36b5-553">MX Hourly</span></span>   |
| <span data-ttu-id="c36b5-554">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="c36b5-554">Salaried</span></span>   | <span data-ttu-id="c36b5-555">MX kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="c36b5-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="c36b5-556">Toimityypit</span><span class="sxs-lookup"><span data-stu-id="c36b5-556">Position types</span></span> 

<span data-ttu-id="c36b5-557">Voit käyttää toimityyppejä kuvaamaan, onko toimi kokoaikainen, osa-aikainen vai jokin muu.</span><span class="sxs-lookup"><span data-stu-id="c36b5-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="c36b5-558">Toimityypit on yhdistetty Dayforceen maksuluokkina, jotka ilmaisevat, onko työntekijä koko- vai osa-aikainen.</span><span class="sxs-lookup"><span data-stu-id="c36b5-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="c36b5-559">Tarvitaan seuraavat toimityypit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="c36b5-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="c36b5-560">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="c36b5-560">Position type</span></span>   | <span data-ttu-id="c36b5-561">kuvaus</span><span class="sxs-lookup"><span data-stu-id="c36b5-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="c36b5-562">Kokoaikainen</span><span class="sxs-lookup"><span data-stu-id="c36b5-562">Full-time</span></span>       | <span data-ttu-id="c36b5-563">Kokopäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-563">Full time employee</span></span> |
| <span data-ttu-id="c36b5-564">Osa-aikainen</span><span class="sxs-lookup"><span data-stu-id="c36b5-564">Part-time</span></span>       | <span data-ttu-id="c36b5-565">Osapäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="c36b5-566">Syykoodit</span><span class="sxs-lookup"><span data-stu-id="c36b5-566">Reason codes</span></span>

<span data-ttu-id="c36b5-567">Syykoodit antavat tietoja työntekijän tilasta</span><span class="sxs-lookup"><span data-stu-id="c36b5-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="c36b5-568">Syykoodit määritetään Dayforceen tilan syinä, jotka ilmaisevat muutokset työntekijän toimessa tai työsuhteessa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="c36b5-569">Tarvitaan seuraavat syykoodit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="c36b5-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="c36b5-570">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="c36b5-570">Reason code</span></span>            | <span data-ttu-id="c36b5-571">kuvaus</span><span class="sxs-lookup"><span data-stu-id="c36b5-571">Description</span></span>                    | <span data-ttu-id="c36b5-572">Soveltuvat skenaariot</span><span class="sxs-lookup"><span data-stu-id="c36b5-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="c36b5-573">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="c36b5-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="c36b5-574">Lähtö ennen ensimmäistä palkanlaskentaa</span><span class="sxs-lookup"><span data-stu-id="c36b5-574">Departure before first payroll</span></span> | <span data-ttu-id="c36b5-575">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-575">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-576">EROAMINEN</span><span class="sxs-lookup"><span data-stu-id="c36b5-576">RESIGNATION</span></span>            | <span data-ttu-id="c36b5-577">Eroaminen</span><span class="sxs-lookup"><span data-stu-id="c36b5-577">Resignation</span></span>                    | <span data-ttu-id="c36b5-578">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-578">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-579">ELÄKE</span><span class="sxs-lookup"><span data-stu-id="c36b5-579">PENSION</span></span>                | <span data-ttu-id="c36b5-580">Eläke</span><span class="sxs-lookup"><span data-stu-id="c36b5-580">Pension</span></span>                        | <span data-ttu-id="c36b5-581">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-581">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-582">IRTISANOMINEN</span><span class="sxs-lookup"><span data-stu-id="c36b5-582">TERMINATION</span></span>            | <span data-ttu-id="c36b5-583">Irtisanominen</span><span class="sxs-lookup"><span data-stu-id="c36b5-583">Termination</span></span>                    | <span data-ttu-id="c36b5-584">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-584">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-585">ELÄKKEELLE SIIRTYMINEN</span><span class="sxs-lookup"><span data-stu-id="c36b5-585">RETIREMENT</span></span>             | <span data-ttu-id="c36b5-586">Eläkkeelle siirtyminen</span><span class="sxs-lookup"><span data-stu-id="c36b5-586">Retirement</span></span>                     | <span data-ttu-id="c36b5-587">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-587">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-588">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="c36b5-588">ABSENTEE</span></span>               | <span data-ttu-id="c36b5-589">Absentee</span><span class="sxs-lookup"><span data-stu-id="c36b5-589">Absentee</span></span>                       | <span data-ttu-id="c36b5-590">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-590">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-591">MUU</span><span class="sxs-lookup"><span data-stu-id="c36b5-591">OTHER</span></span>                  | <span data-ttu-id="c36b5-592">Muut syyt</span><span class="sxs-lookup"><span data-stu-id="c36b5-592">Other Reasons</span></span>                  | <span data-ttu-id="c36b5-593">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-593">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-594">SULKEMINEN</span><span class="sxs-lookup"><span data-stu-id="c36b5-594">CLOSURE</span></span>                | <span data-ttu-id="c36b5-595">Liiketoiminnan sulkeminen</span><span class="sxs-lookup"><span data-stu-id="c36b5-595">Business Closure</span></span>               | <span data-ttu-id="c36b5-596">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-596">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-597">KUOLEMA</span><span class="sxs-lookup"><span data-stu-id="c36b5-597">DEATH</span></span>                  | <span data-ttu-id="c36b5-598">Kuolema</span><span class="sxs-lookup"><span data-stu-id="c36b5-598">Death</span></span>                          | <span data-ttu-id="c36b5-599">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-599">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-600">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="c36b5-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="c36b5-601">Virkavapaa</span><span class="sxs-lookup"><span data-stu-id="c36b5-601">Leave of Absence</span></span>               | <span data-ttu-id="c36b5-602">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-602">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-603">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="c36b5-603">CONTRACTEND</span></span>            | <span data-ttu-id="c36b5-604">Sopimuksen päättyminen</span><span class="sxs-lookup"><span data-stu-id="c36b5-604">End of Contract</span></span>                | <span data-ttu-id="c36b5-605">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="c36b5-605">Terminate worker</span></span>     |
| <span data-ttu-id="c36b5-606">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="c36b5-606">SALARYCHANGE</span></span>           | <span data-ttu-id="c36b5-607">Palkan muutos</span><span class="sxs-lookup"><span data-stu-id="c36b5-607">Change of Salary</span></span>               | <span data-ttu-id="c36b5-608">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="c36b5-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="c36b5-609">Työehdot</span><span class="sxs-lookup"><span data-stu-id="c36b5-609">Terms of employment</span></span>

<span data-ttu-id="c36b5-610">Työehtoja voidaan käyttää, kun luodaan työehtoluokkia.</span><span class="sxs-lookup"><span data-stu-id="c36b5-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="c36b5-611">Ehdot määritetään Dayforceen työsuhteen mittarin arvoina.</span><span class="sxs-lookup"><span data-stu-id="c36b5-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="c36b5-612">Seuraavat työsuhteen ja kuvaukset termit ovat pakollisia.</span><span class="sxs-lookup"><span data-stu-id="c36b5-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="c36b5-613">Työehdot</span><span class="sxs-lookup"><span data-stu-id="c36b5-613">Terms of employment</span></span>   | <span data-ttu-id="c36b5-614">kuvaus</span><span class="sxs-lookup"><span data-stu-id="c36b5-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="c36b5-615">Säännöllinen</span><span class="sxs-lookup"><span data-stu-id="c36b5-615">Regular</span></span>               | <span data-ttu-id="c36b5-616">Säännöllinen</span><span class="sxs-lookup"><span data-stu-id="c36b5-616">Regular</span></span>     |
| <span data-ttu-id="c36b5-617">Suora</span><span class="sxs-lookup"><span data-stu-id="c36b5-617">Direct</span></span>                | <span data-ttu-id="c36b5-618">Suora</span><span class="sxs-lookup"><span data-stu-id="c36b5-618">Direct</span></span>      |
| <span data-ttu-id="c36b5-619">Harjoittelujakso</span><span class="sxs-lookup"><span data-stu-id="c36b5-619">Internship</span></span>            | <span data-ttu-id="c36b5-620">Harjoittelujakso</span><span class="sxs-lookup"><span data-stu-id="c36b5-620">Internship</span></span>  |
| <span data-ttu-id="c36b5-621">Pysyvä</span><span class="sxs-lookup"><span data-stu-id="c36b5-621">Permanent</span></span>             | <span data-ttu-id="c36b5-622">Pysyvä</span><span class="sxs-lookup"><span data-stu-id="c36b5-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="c36b5-623">Siviilisääty</span><span class="sxs-lookup"><span data-stu-id="c36b5-623">Marital status</span></span>

<span data-ttu-id="c36b5-624">Siviilisääty on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="c36b5-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c36b5-625">Seuraavassa taulukossa kuvataan, miten siviilisääty liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="c36b5-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="c36b5-626">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="c36b5-626">Human Resources</span></span>                 | <span data-ttu-id="c36b5-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c36b5-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="c36b5-628">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="c36b5-628">Married</span></span>                | <span data-ttu-id="c36b5-629">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="c36b5-629">Married</span></span>                   |
| <span data-ttu-id="c36b5-630">Yksi</span><span class="sxs-lookup"><span data-stu-id="c36b5-630">Single</span></span>                 | <span data-ttu-id="c36b5-631">Yksi</span><span class="sxs-lookup"><span data-stu-id="c36b5-631">Single</span></span>                    |
| <span data-ttu-id="c36b5-632">Leski</span><span class="sxs-lookup"><span data-stu-id="c36b5-632">Widowed</span></span>                | <span data-ttu-id="c36b5-633">Leski</span><span class="sxs-lookup"><span data-stu-id="c36b5-633">Widowed</span></span>                   |
| <span data-ttu-id="c36b5-634">Eronnut</span><span class="sxs-lookup"><span data-stu-id="c36b5-634">Divorced</span></span>               | <span data-ttu-id="c36b5-635">Eronnut</span><span class="sxs-lookup"><span data-stu-id="c36b5-635">Divorced</span></span>                  |
| <span data-ttu-id="c36b5-636">Rekisteröity suhde</span><span class="sxs-lookup"><span data-stu-id="c36b5-636">Registered Partnership</span></span> | <span data-ttu-id="c36b5-637">Kotimainen kumppanuus</span><span class="sxs-lookup"><span data-stu-id="c36b5-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="c36b5-638">None</span><span class="sxs-lookup"><span data-stu-id="c36b5-638">None</span></span>                   | <span data-ttu-id="c36b5-639">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="c36b5-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c36b5-640">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="c36b5-640">Cohabiting</span></span>             | <span data-ttu-id="c36b5-641">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="c36b5-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="c36b5-642">Sukupuoli</span><span class="sxs-lookup"><span data-stu-id="c36b5-642">Gender</span></span>

<span data-ttu-id="c36b5-643">Sukupuolinimitykset on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="c36b5-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c36b5-644">Seuraavassa taulukossa kuvataan, miten sukupuolinimitykset liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="c36b5-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="c36b5-645">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="c36b5-645">Human Resources</span></span>       | <span data-ttu-id="c36b5-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c36b5-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="c36b5-647">Mies</span><span class="sxs-lookup"><span data-stu-id="c36b5-647">Male</span></span>         | <span data-ttu-id="c36b5-648">Mies</span><span class="sxs-lookup"><span data-stu-id="c36b5-648">Male</span></span>                      |
| <span data-ttu-id="c36b5-649">Nainen</span><span class="sxs-lookup"><span data-stu-id="c36b5-649">Female</span></span>       | <span data-ttu-id="c36b5-650">Nainen</span><span class="sxs-lookup"><span data-stu-id="c36b5-650">Female</span></span>                    |
| <span data-ttu-id="c36b5-651">Yksilöimätön</span><span class="sxs-lookup"><span data-stu-id="c36b5-651">Non-specific</span></span> | <span data-ttu-id="c36b5-652">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="c36b5-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="c36b5-653">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="c36b5-653">Payment method</span></span>

<span data-ttu-id="c36b5-654">Maksutavat antavat työntekijälle ja yritykselle keinon kuvata, miten työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="c36b5-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="c36b5-655">Maksutavat on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="c36b5-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c36b5-656">Seuraavassa taulukossa kuvataan, miten maksutavat liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="c36b5-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="c36b5-657">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="c36b5-657">Human Resources</span></span>             | <span data-ttu-id="c36b5-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c36b5-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="c36b5-659">Maksu</span><span class="sxs-lookup"><span data-stu-id="c36b5-659">Cash</span></span>               | <span data-ttu-id="c36b5-660">Maksu</span><span class="sxs-lookup"><span data-stu-id="c36b5-660">Cash</span></span>                      |
| <span data-ttu-id="c36b5-661">Sähköinen maksu</span><span class="sxs-lookup"><span data-stu-id="c36b5-661">Electronic Payment</span></span> | <span data-ttu-id="c36b5-662">Tapahtumien siirto</span><span class="sxs-lookup"><span data-stu-id="c36b5-662">Transfer</span></span>                  |
| <span data-ttu-id="c36b5-663">Tarkistus</span><span class="sxs-lookup"><span data-stu-id="c36b5-663">Check</span></span>              | <span data-ttu-id="c36b5-664">Sekki</span><span class="sxs-lookup"><span data-stu-id="c36b5-664">Cheque</span></span>                    |
| <span data-ttu-id="c36b5-665">Pankkivekseli</span><span class="sxs-lookup"><span data-stu-id="c36b5-665">Bank Draft</span></span>         | <span data-ttu-id="c36b5-666">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="c36b5-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c36b5-667">Muu</span><span class="sxs-lookup"><span data-stu-id="c36b5-667">Other</span></span>              | <span data-ttu-id="c36b5-668">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="c36b5-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="c36b5-669">Pankkitilin tyyppi</span><span class="sxs-lookup"><span data-stu-id="c36b5-669">Bank account type</span></span>

<span data-ttu-id="c36b5-670">Pankkitilin tyyppejä käytetään sähköisissä maksuissa työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="c36b5-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="c36b5-671">Pankin tilityypit yhdistetään Dayforceen tilinsiirtämisen tietoina.</span><span class="sxs-lookup"><span data-stu-id="c36b5-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="c36b5-672">Pankkitilin tyypit ovat tarvittaessa käännettyjä ja hyväksytty arvoiksi sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="c36b5-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="c36b5-673">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="c36b5-673">Human Resources</span></span>            | <span data-ttu-id="c36b5-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c36b5-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="c36b5-675">Käyttötili</span><span class="sxs-lookup"><span data-stu-id="c36b5-675">Checking Account</span></span>  | <span data-ttu-id="c36b5-676">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="c36b5-676">CheckingAccount</span></span>           |
| <span data-ttu-id="c36b5-677">Palkanlaskennan tili</span><span class="sxs-lookup"><span data-stu-id="c36b5-677">Payroll Account</span></span>   | <span data-ttu-id="c36b5-678">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="c36b5-678">PayrollAccount</span></span>            |
| <span data-ttu-id="c36b5-679">Säästötili</span><span class="sxs-lookup"><span data-stu-id="c36b5-679">Savings Account</span></span>   | <span data-ttu-id="c36b5-680">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="c36b5-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c36b5-681">BankGirot-tili</span><span class="sxs-lookup"><span data-stu-id="c36b5-681">BankGirot account</span></span> | <span data-ttu-id="c36b5-682">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="c36b5-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c36b5-683">PlusGirot-tili</span><span class="sxs-lookup"><span data-stu-id="c36b5-683">PlusGirot account</span></span> | <span data-ttu-id="c36b5-684">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="c36b5-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="c36b5-685">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="c36b5-685">Earning codes</span></span>

<span data-ttu-id="c36b5-686">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="c36b5-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c36b5-687">Tunnukset kattavat erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="c36b5-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="c36b5-688">Mikäli käytetään ei-tuettua taajuutta **Jokainen palkka** -taajuutta käytetään oletusarvon mukaan laskelmissa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="c36b5-689">Tuetut maksutaajuudet</span><span class="sxs-lookup"><span data-stu-id="c36b5-689">Supported frequencies</span></span>

- <span data-ttu-id="c36b5-690">Kaikki</span><span class="sxs-lookup"><span data-stu-id="c36b5-690">All</span></span>
- <span data-ttu-id="c36b5-691">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="c36b5-691">EVERYPAY</span></span>
- <span data-ttu-id="c36b5-692">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="c36b5-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="c36b5-693">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="c36b5-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="c36b5-694">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="c36b5-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="c36b5-695">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-695">1OFMTH</span></span>
- <span data-ttu-id="c36b5-696">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-696">LASTOFMTH</span></span>
- <span data-ttu-id="c36b5-697">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-697">2OFMTH</span></span>
- <span data-ttu-id="c36b5-698">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-698">3OFMTH</span></span>
- <span data-ttu-id="c36b5-699">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-699">4OFMTH</span></span>
- <span data-ttu-id="c36b5-700">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-700">5OFMTH</span></span>
- <span data-ttu-id="c36b5-701">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-701">1N2OFMTH</span></span>
- <span data-ttu-id="c36b5-702">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-702">3N4OFMTH</span></span>
- <span data-ttu-id="c36b5-703">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-703">1N3OFMTH</span></span>
- <span data-ttu-id="c36b5-704">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-704">1N4OFMTH</span></span>
- <span data-ttu-id="c36b5-705">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-705">2N3OFMTH</span></span>
- <span data-ttu-id="c36b5-706">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-706">2N4OFMTH</span></span>
- <span data-ttu-id="c36b5-707">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="c36b5-708">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="c36b5-709">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="c36b5-710">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="c36b5-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c36b5-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="c36b5-712">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="c36b5-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="c36b5-713">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="c36b5-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="c36b5-714">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="c36b5-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="c36b5-715">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="c36b5-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="c36b5-716">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="c36b5-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="c36b5-717">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c36b5-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="c36b5-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c36b5-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="c36b5-719">Osoitteet</span><span class="sxs-lookup"><span data-stu-id="c36b5-719">Addresses</span></span>

<span data-ttu-id="c36b5-720">Määriteltyjen maiden tai alueiden, valtioiden ja läänin (kuntien) koodien tunnistaminen edellyttää tiettyjä muotoja, joita Dayforce ja maassa tai alueella olevat toimijat pystyvät tunnistamaan.</span><span class="sxs-lookup"><span data-stu-id="c36b5-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="c36b5-721">Vaikka kaupunkien muoto on joustava, jokainen paikkakunta täytyy liittää osavaltioon.</span><span class="sxs-lookup"><span data-stu-id="c36b5-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="c36b5-722">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="c36b5-722">Human Resources</span></span>              | <span data-ttu-id="c36b5-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c36b5-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="c36b5-724">Maa/alue</span><span class="sxs-lookup"><span data-stu-id="c36b5-724">Country/Region</span></span>      | <span data-ttu-id="c36b5-725">Maakoodi</span><span class="sxs-lookup"><span data-stu-id="c36b5-725">Country Code</span></span>          |
| <span data-ttu-id="c36b5-726">Postinumero</span><span class="sxs-lookup"><span data-stu-id="c36b5-726">Zip/Postal Code</span></span>     | <span data-ttu-id="c36b5-727">Postinumero</span><span class="sxs-lookup"><span data-stu-id="c36b5-727">Postal Code</span></span>           |
| <span data-ttu-id="c36b5-728">Alue</span><span class="sxs-lookup"><span data-stu-id="c36b5-728">State</span></span>               | <span data-ttu-id="c36b5-729">Aluekoodi</span><span class="sxs-lookup"><span data-stu-id="c36b5-729">State Code</span></span>            |
| <span data-ttu-id="c36b5-730">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="c36b5-730">City</span></span>                | <span data-ttu-id="c36b5-731">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="c36b5-731">City</span></span>                  |
| <span data-ttu-id="c36b5-732">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="c36b5-732">County</span></span>              | <span data-ttu-id="c36b5-733">Lääni (kunta)</span><span class="sxs-lookup"><span data-stu-id="c36b5-733">County (Municipality)</span></span> |
| <span data-ttu-id="c36b5-734">Katu</span><span class="sxs-lookup"><span data-stu-id="c36b5-734">Street</span></span>              | <span data-ttu-id="c36b5-735">Osoiterivi 1</span><span class="sxs-lookup"><span data-stu-id="c36b5-735">Address Line 1</span></span>        |
| <span data-ttu-id="c36b5-736">Kadunnumero</span><span class="sxs-lookup"><span data-stu-id="c36b5-736">Street Number</span></span>       | <span data-ttu-id="c36b5-737">Osoiterivi 2</span><span class="sxs-lookup"><span data-stu-id="c36b5-737">Address Line 2</span></span>        |
| <span data-ttu-id="c36b5-738">Rakennusta koskeva lisätieto</span><span class="sxs-lookup"><span data-stu-id="c36b5-738">Building Complement</span></span> | <span data-ttu-id="c36b5-739">Osoiterivi 5</span><span class="sxs-lookup"><span data-stu-id="c36b5-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="c36b5-740">Passin numero</span><span class="sxs-lookup"><span data-stu-id="c36b5-740">Passport number</span></span>

<span data-ttu-id="c36b5-741">Työntekijät voivat ilmoittaa passin tiedot.</span><span class="sxs-lookup"><span data-stu-id="c36b5-741">Employees can declare passport information.</span></span> <span data-ttu-id="c36b5-742">Tämä tietoa on **Passi**-tunnustyyppiä ja se on integroitu Dayforceen osaksi työntekijän Meksikon liittyvää tietoa.</span><span class="sxs-lookup"><span data-stu-id="c36b5-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="c36b5-743">Tunnustyyppi = "Passi"</span><span class="sxs-lookup"><span data-stu-id="c36b5-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="c36b5-744">Myöntämispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="c36b5-744">Issued Date</span></span>
- <span data-ttu-id="c36b5-745">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="c36b5-745">Expiration Date</span></span>

<span data-ttu-id="c36b5-746">Työntekijät voi määrittää useita tunnistenumeroita **Passi**-tunnuksesta.</span><span class="sxs-lookup"><span data-stu-id="c36b5-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="c36b5-747">Vain nykyiset aktiiviset passitapahtumat integroidaan Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="c36b5-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="c36b5-748">Mikäli kaikki passitapahtumat ovat vanhentuneet, passi, joka on viimeksi myönnetty on integroitu Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="c36b5-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]