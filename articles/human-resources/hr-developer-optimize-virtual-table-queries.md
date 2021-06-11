---
title: Optimoi Dataversen virtuaalitaulukoiden kyselyt
description: Dataversen virtuaalitaulukyselyjen suorituskyvyn optimointi ja vianmääritys
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66fb9f2b50079b5eb4eb16da17b8a473d687d354
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054905"
---
# <a name="optimize-dataverse-virtual-table-queries"></a><span data-ttu-id="ddf4d-103">Optimoi Dataversen virtuaalitaulukoiden kyselyt</span><span class="sxs-lookup"><span data-stu-id="ddf4d-103">Optimize Dataverse virtual table queries</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="ddf4d-104">Varasto-otto</span><span class="sxs-lookup"><span data-stu-id="ddf4d-104">Issue</span></span>

### <a name="overview"></a><span data-ttu-id="ddf4d-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="ddf4d-105">Overview</span></span>

<span data-ttu-id="ddf4d-106">Kun käytät Dataversen virtuaalitauluja integrointien ja muiden tietoyhteyksien kehittämiseen Dynamics 365 Human Resourcesissa, virtuaalitauluihin liitetyissä kyselyissä ilmenee suorituskykyongelmia.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-106">When using Dataverse virtual tables to develop integrations and other data connections with Dynamics 365 Human Resources, you can experience performance issues with queries against the virtual tables.</span></span> <span data-ttu-id="ddf4d-107">Kyselyjen suorittaminen voi olla hidasta eri asiakkaiden tai liittymien välillä.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-107">The slow query execution can occur across various clients or interfaces.</span></span> <span data-ttu-id="ddf4d-108">Ongelma voi esimerkiksi esiintyä seuraavissa tilanteissa:</span><span class="sxs-lookup"><span data-stu-id="ddf4d-108">For example, you may experience the issue in the following circumstances:</span></span>

- <span data-ttu-id="ddf4d-109">Virtuaalitaulua kyseltäessä Dataversen www-ohjelmointirajapinnan kautta</span><span class="sxs-lookup"><span data-stu-id="ddf4d-109">When querying a virtual table through the Dataverse Web API</span></span>
- <span data-ttu-id="ddf4d-110">Kun Power App -sovellusta luodaan virtuaalitaulua vasten</span><span class="sxs-lookup"><span data-stu-id="ddf4d-110">When creating a Power App against a virtual table</span></span>
- <span data-ttu-id="ddf4d-111">Kun Power BI -raporttia rakennetaan virtuaalitaulussa</span><span class="sxs-lookup"><span data-stu-id="ddf4d-111">When building a Power BI report on a virtual table</span></span>

<span data-ttu-id="ddf4d-112">Kaikki nämä liittymät voivat tuoda esiin suorituskykyongelman.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-112">All these interfaces have the potential to surface the performance issue.</span></span>

<span data-ttu-id="ddf4d-113">Yksi henkilöstöhallinnon virtuaalitaulujen suorituskyvyn hidastamisista on taulun liittyvien Dataversen virtuaalitaulujen [siirtymisominaisuuksiin](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) liittyvät viiteavainsarakkeet.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-113">One cause of slow performance with Dataverse virtual tables for Human Resources is the foreign key columns of the virtual table related to the table's [navigation properties](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span></span> <span data-ttu-id="ddf4d-114">Kun virtuaalitaululle luodaan siirtymisominaisuudet, tauluun lisätään automaattisesti viiteavainsarake, joka vastaa liittyvän virtuaalitaulun avainsarakkeen arvoa.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-114">When navigation properties are created for a virtual table, a foreign key column is automatically added to the table to represent the value of the key for the related virtual table's key column.</span></span> <span data-ttu-id="ddf4d-115">Esimerkiksi **_mshr_fk_person_id_value** lisätään **mshr_hcmworkerbaseentity**-kohteeseen, jonka viiteavaimen ominaisuus on **mshr_dirpersonentity**-kohteesta.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-115">For example, the **_mshr_fk_person_id_value** column is added to the **mshr_hcmworkerbaseentity** entity with the foreign key property from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="ddf4d-116">Koska näiden viiteavainsarakkeiden arvoja ylläpidetään taulukossa, arvojen hakeminen voi vaikuttaa negatiivisesti kyselyn suorituskykyyn virtuaalitaulua vasten.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-116">Because of how the values for these foreign key columns are maintained in a table, fetching the values can have a negative impact on the performance of a query against the virtual table.</span></span>

### <a name="potential-symptoms"></a><span data-ttu-id="ddf4d-117">Mahdolliset oireet</span><span class="sxs-lookup"><span data-stu-id="ddf4d-117">Potential symptoms</span></span>

<span data-ttu-id="ddf4d-118">Tämä vaikutus voi olla esimerkiksi kyselyissä työntekijää (**mshr_hcmworkerentity**) tai perustyöntekijää (**mshr_hcmworkerbaseentity**) vastaan.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-118">An example where you may see this impact is in queries against the Worker (**mshr_hcmworkerentity**) or Base worker (**mshr_hcmworkerbaseentity**) entity.</span></span> <span data-ttu-id="ddf4d-119">Voit nähdä suorituskykyongelman itse monin eri tavoin:</span><span class="sxs-lookup"><span data-stu-id="ddf4d-119">You may see the performance issue manifest itself in a few different ways:</span></span>

- <span data-ttu-id="ddf4d-120">**Kyselyn suorittaminen on hidasta**: Kysely virtuaalitaulua vastaan saattaa palauttaa odotetut tulokset, mutta kyselyn suorittaminen kestää odotettua kauemmin.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-120">**Slow query execution**: The query against the virtual table may return the expected results, but take longer than expected to complete execution of the query.</span></span>
- <span data-ttu-id="ddf4d-121">**Kyselyn aikakatkaisu**: Kysely voi aikakatkaisua ja palauttaa seuraavan virheen: "ATunnuksen avulla soitettiin Finance and Operationsiin, mutta Finance and Operations palautti InternalServerError-tyypin virheen."</span><span class="sxs-lookup"><span data-stu-id="ddf4d-121">**Query timeout**: The query may time out and return the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type InternalServerError."</span></span>
- <span data-ttu-id="ddf4d-122">**Odottamaton virhe**: Kysely saattaa palauttaa virhetyypin 400. Näyttöön tulee seuraava sanoma: Odottamaton virhe.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-122">**Unexpected error**: The query may return an error type 400 with the following message: "An unexpected error occurred."</span></span>

  ![Virhetyyppi 400 HcmWorkerBaseEntityssä](./media/HcmWorkerBaseEntityErrorType400.png)

- <span data-ttu-id="ddf4d-124">**Ylikuormitus** Kysely voi käyttää palvelinresursseja liian paljon, ja siitä tulee vain osa välityspalvelinta.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-124">**Throttling**: The query may overuse server resources, and become subject to throttling.</span></span> <span data-ttu-id="ddf4d-125">Tässä tapauksessa kysely palauttaa seuraavan virheen: "Tunnus haettiin Finance and Operationskutsua varten, mutta Finance and Operations palautti virheen, tyyppi 429."</span><span class="sxs-lookup"><span data-stu-id="ddf4d-125">In this case, the query returns the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type 429."</span></span> <span data-ttu-id="ddf4d-126">Lisätietoja henkilöstöhallinnon rajoittamisesta on kohdassa [rajoitusten usein kysytyt kysymykset](./hr-admin-integration-throttling-faq.md).</span><span class="sxs-lookup"><span data-stu-id="ddf4d-126">For more information in throttling in Human Resources, see [Throttling FAQ](./hr-admin-integration-throttling-faq.md).</span></span>

  ![Virhetyyppi 429 HcmWorkerBaseEntityssä](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a><span data-ttu-id="ddf4d-128">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ddf4d-128">Resolution</span></span>

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a><span data-ttu-id="ddf4d-129">Kyselyyn sisältyvien sarakkeiden määrän rajoittaminen</span><span class="sxs-lookup"><span data-stu-id="ddf4d-129">Limit the number of columns included in your data query</span></span>

<span data-ttu-id="ddf4d-130">Virtuaalitaulujen avulla yksi menetelmistä, joilla on paras mahdollisuus parantaa kyselyn suorituskykyä, on kyselystä valittujen sarakkeiden määrän rajoittaminen.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-130">With virtual tables, one of the methods with the greatest potential to improve query performance is to limit the number of columns selected in the query.</span></span> <span data-ttu-id="ddf4d-131">Yleisohje kyselyn suorituskyvyn optimointiin on se, että kyselyssä palautetut sarakkeet rajataan vain tarvitsemiisi ominaisuuksiin.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-131">The general guidance for optimizing query performance is to limit the columns returned in your query to only those properties that you need.</span></span> <span data-ttu-id="ddf4d-132">Tämä koskee erityisesti virtuaalitaulujen viiteavainsarakkeita.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-132">This is particularly true with the foreign key columns on virtual tables.</span></span> <span data-ttu-id="ddf4d-133">Jos et tarvitse integroinnin tai raportin viiteavainsarakkeiden arvoja, valitse vain haluamasi sarakkeet ilman viiteavainsarakkeita rakenteen avulla.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-133">If you don't need the values in the foreign key columns for your integration or report, then structure the query to select only the columns you need, excluding the foreign key columns.</span></span>

#### <a name="selecting-columns-in-an-odata-query"></a><span data-ttu-id="ddf4d-134">Sarakkeiden valitseminen OData-kyselyssä</span><span class="sxs-lookup"><span data-stu-id="ddf4d-134">Selecting columns in an OData query</span></span>

<span data-ttu-id="ddf4d-135">Kun kyselet virtuaalitaulua Dataversen www-ohjelmointirajapinnan kautta, voit rajoittaa kyselyyn sisältyvien sarakkeiden määrää käyttämällä **$select**-järjestelmän kyselyasetusta ja määrittää sarakkeet, joita varten tulokset on palautettava.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-135">When querying a virtual table through the Dataverse Web API, you can limit the number of columns included in the query by using the **$select** system query option, and define the columns for which you need results returned.</span></span> <span data-ttu-id="ddf4d-136">Voit parantaa suorituskykyä sulkemalla pois viiteavainsarakkeet (joissa on **_mshr_FK_**-etuliite) kyselystä.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-136">To maximize performance, exclude foreign key columns (those with the **_mshr_FK_** prefix) from the query.</span></span>

<span data-ttu-id="ddf4d-137">Esimerkiksi seuraava kysely ennusteyksikköä **mshr_hcmworkerbaseentity**-kohdetta vastaan sisältää vain kyselylausekkeen **$select** sisällä olevat sarakkeet ilman viiteavainarvoja.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-137">For example, the following query against the **mshr_hcmworkerbaseentity** entity will include only the columns included in the **$select** query option clause, excluding foreign key values.</span></span> <span data-ttu-id="ddf4d-138">Tämä parantaa merkittävästi suorituskykyä kyselyssä, joka sisältää kaikki taulusarakkeet.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-138">This provides significant improvements in performance over a query that includes all table columns.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="ddf4d-139">Ehdotus, jonka mukaan valittujen sarakkeiden määrää rajataan, koskee myös **$expand**-asetusta, kun kyselyä laajennetaan liittyviin virtuaalitauluihin siirtymisominaisuuksien avulla.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-139">The recommendation to limit the number of columns selected also applies when using the **$expand** query option to expand the query to related virtual tables through navigation properties.</span></span> <span data-ttu-id="ddf4d-140">Seuraava kysely sisältää esimerkiksi sarakkeet **mshr_hcmworkerbaseentity**-yksikköön, jonka laajennetut sarakkeet ovat peräisin **mshr_dirpersonentity**-yksiköstä.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-140">For example, the following query includes columns from the **mshr_hcmworkerbaseentity** entity with expanded columns from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="ddf4d-141">Huomaa, että **$select**-asetus sisältyy myös **$expand**-kyselyasetuslausekkeeseen.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-141">Note that the **$select** query option is also included in the **$expand** query option clause.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="ddf4d-142">Kun käytät tätä menetelmää, kun tietoja noudetaan **$select**-kyselylausekkeen **$expand**-kyselyvaihtoehdolla, suorituskyky yleensä paranee, kun yksiköiden välinen siirtymiskyky on monisuuntainen.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-142">When using this method of retrieving data with the **$select** query option in the **$expand** query option clause, you will typically see greater performance improvements when the navigation property between the entities is a many-to-one relationship.</span></span> <span data-ttu-id="ddf4d-143">Kyselyiden suoritusaika ei ehkä ole sama, kun yksi moneen -suhdetta laajennetaan.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-143">You may not see the same decrease in query execution time when expanding a one-to-many relationship.</span></span> <span data-ttu-id="ddf4d-144">Lisätietoja Dataverse-virtuaalitaulujen suhdemäärityksestä on kohdassa [Taulun suhteet](/powerapps/maker/data-platform/create-edit-entity-relationships).</span><span class="sxs-lookup"><span data-stu-id="ddf4d-144">For more information on relationship definition for Dataverse virtual tables, see [Table relationships](/powerapps/maker/data-platform/create-edit-entity-relationships).</span></span>

<span data-ttu-id="ddf4d-145">Lisätietoja Dataverse-www-ohjelmointirajapinnan **$select** ja **$expand** -asetusten käyttämisestä on kohdassa [Liittyvien yksikkötietueiden hakeminen kyselyn avulla](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span><span class="sxs-lookup"><span data-stu-id="ddf4d-145">For more information on using the **$select** and **$expand** system query options in the Dataverse Web API, see [Retrieve related entity records with a query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span></span>

#### <a name="selecting-columns-in-power-bi"></a><span data-ttu-id="ddf4d-146">Sarakkeiden valitseminen Power BIssä</span><span class="sxs-lookup"><span data-stu-id="ddf4d-146">Selecting columns in Power BI</span></span>

<span data-ttu-id="ddf4d-147">Jos Power BI -raportin luominen Dataverse-virtuaalitauluun hidastaa suorituskykyä, voit parantaa suorituskykyä sulkemalla viitesarakkeet pois valituista sarakkeista raporttia varten valitusta taulusta.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-147">If you experience any of the aforementioned indications of slow performance when building a Power BI report against a Dataverse virtual table, you can improve the performance by excluding foreign key columns from the columns selected from the table for the report.</span></span> <span data-ttu-id="ddf4d-148">Jos esimerkiksi luot raportin Power BI Desktopilla toimittajayksikölle **mshr_hcmworkerbaseentity**, voit valita raporttikyselyyn sisällytettävät sarakkeet seuraavien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-148">For example, if you are using Power BI Desktop to create a report against the **mshr_hcmworkerbaseentity** entity, you can use the following steps to select the columns you want included in the report query.</span></span>

1. <span data-ttu-id="ddf4d-149">Valitse  Power BI Desktopssa **Hae tiedot** -toimintonauhan avattavasta valikosta **Lisää...** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-149">In Power BI Desktop, select **More...** from the **Get data** drop-down list on the action ribbon.</span></span>
2. <span data-ttu-id="ddf4d-150">Kirjoita **Hae tiedot** -ikkunassa hakuruutuun **Common Data Service** ja valitse **Common Data Service** -liitin ja valitse **Yhdistä**.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-150">In the **Get Data** window, enter **Common Data Service** in the search box, select the **Common Data Service** connector, and select **Connect**.</span></span>
3. <span data-ttu-id="ddf4d-151">Kirjoita Common Data Service -ikkunan **Palvelimen URL** -kenttään Dataverse-ympäristösi organisaatio-URI ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-151">In the **Server Url** field of the Common Data Service window, enter the organization URI for your Dataverse environment, and select **OK**.</span></span>
  
   ![Anna Dataverse -ympäristösi URI](./media/PowerBIDataverseURLSetup.png)
  
4. <span data-ttu-id="ddf4d-153">Laajenna Navigointi-ikkunanssa **Yksiköt**-solmu.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-153">In the Navigator window, expand the **Entities** node.</span></span>
5. <span data-ttu-id="ddf4d-154">Kirjoita hakuruutuun **mshr_hcmworkerbaseentity** ja valitse yksikkö.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-154">In the search box, enter **mshr_hcmworkerbaseentity**, and select the entity.</span></span>
6. <span data-ttu-id="ddf4d-155">Valitse **Muuta tiedot**.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-155">Select **Transform Data**.</span></span>
7. <span data-ttu-id="ddf4d-156">Valitse Power Query -editori-ikkunassa **Laajennettu editori**.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-156">In the Power Query Editor window, select **Advanced Editor**.</span></span>
8. <span data-ttu-id="ddf4d-157">Päivitä kysely **Laajennettu editori** -ikkunassa niin, että se näyttää alla olevalta, lisäämällä tai poistamalla sarakkeita taulukkoon tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-157">In the **Advanced Editor** window, update the query to look like the below, adding or removing any columns to the array as needed.</span></span>

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Kyselyn päivittäminen Power Query -editorin laajennetulla editorilla](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. <span data-ttu-id="ddf4d-159">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-159">Select **Done**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="ddf4d-160">Jos olet aiemmin saanut kyselyltä virhetyypin 429 ennen päivitystä, sinun on ehkä odotettava uudelleenyrityskauden päättymistä ennen kyselyn päivittämistä.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-160">If you previously received an error of type 429 from the query prior to updating, you may need to wait for the retry period prior to refreshing the query for it to complete successully.</span></span>

10. <span data-ttu-id="ddf4d-161">Valitse **Sulje & ota käyttöön** Power Query -editorin toimintonauhassa.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-161">Click **Close & Apply** on the Power Query Editor action ribbon.</span></span>

<span data-ttu-id="ddf4d-162">Tämän jälkeen voit alkaa rakentaa Power BI -raporttia virtuaalitaulusta valittuihin sarakkeisiin.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-162">You're then able to begin building your Power BI report against the columns selected from the virtual table.</span></span>

#### <a name="selecting-columns-in-power-apps"></a><span data-ttu-id="ddf4d-163">Sarakkeiden valitseminen Power Appsssä</span><span class="sxs-lookup"><span data-stu-id="ddf4d-163">Selecting columns in Power Apps</span></span>

<span data-ttu-id="ddf4d-164">Kuten Dataversen www-ohjelmointirajapinnan kyselyissä ja Power BIssä, ja voit parantaa Dataversen virtuaalitauluihin perustuvien Power Appsin kyselyjen suorituskykyä sulkemalla pois sovelluksesi toisiinsa liittyvien taulujen sarakkeet.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-164">Similar to Dataverse Web API queries and Power BI, you can improve query performance for Power Apps based on Dataverse virtual tables by excluding columns of related tables from your app.</span></span> <span data-ttu-id="ddf4d-165">Jos sivuun liittyvän taulun sarakkeita on sisällytetty, tietojen hakemista varten muodostettu URL-osoite sisältää liittyvän taulun viiteavaimen ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-165">If any columns from a related table have been included on a page, then the request URL constructed to fetch the data will include foreign key properties of the related table.</span></span> <span data-ttu-id="ddf4d-166">Kuten edellä olevassa [OData-kyselyn sarakkeiden valinnassa](#selecting-columns-in-power-apps), suorituskyky vähenee aiheuttaen lisää tietohakuja.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-166">This, as in the examples of [Selecting columns in an OData Query](#selecting-columns-in-power-apps) above, reduces performance by causing additional data lookups.</span></span>

<span data-ttu-id="ddf4d-167">Voit toimia näin varmistamalla, ettei Power Appin mihinkään tietolomakkeeseen ole sisällytetty liittyvien taulujen tietokenttiä.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-167">To work around this, you can validate that no data fields from related tables have been included on any data form of your Power App.</span></span>

1. <span data-ttu-id="ddf4d-168">Valitse puunäkymäruudusta näytön tietolomake.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-168">In the Tree view pane, select the data form for the screen.</span></span>
2. <span data-ttu-id="ddf4d-169">Valitse **Kentät**-ominaisuuden **Ominaisuudet**-ruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-169">In the **Properties** pane, select **Edit** on the **Fields** property.</span></span>
3. <span data-ttu-id="ddf4d-170">Varmista **tieto** ruudussa, että mikään valituista kentistä ei ole tietolähteen virtuaalitaulun kenttiä.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-170">In the **Data** pane, verify that none of the selected fields are fields of the virtual table of the data source.</span></span>

<span data-ttu-id="ddf4d-171">Jos jokin sovellukseen sisältyvän sivun tietokentistä esimerkiksi viittaa toiseen tauluun, kuten **ThisItem.Worker.Name**, jossa **työntekijä** on liittyvä taulu, tietojen hakeminen voi vähentää suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-171">For example, if one of the data fields included on a page in the app references another table, such as **ThisItem.Worker.Name**, where **Worker** is the related table, there is a potential for reduced performance in fetching the data.</span></span>

<span data-ttu-id="ddf4d-172">[Power Apps -valvontaruudulla](/powerapps/maker/monitor-overview) voit varmistaa, että kyselyyn sisällytetään vain tarvitsemiasi sarakkeita, kun Power App -sovelluksen tiedot hankitaan.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-172">You can use the [Power Apps Monitor](/powerapps/maker/monitor-overview) to ensure that only the columns you need are being included in the query to get the data for the Power App.</span></span> <span data-ttu-id="ddf4d-173">Kun tarkastelet getRows-toimintoon suunniteltua URL-osoitetta, voit varmistaa, että sovelluksesi sarakkeet noudetaan mahdollisimman helposti.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-173">You can view the URL constructed for the getRows operation to ensure the columns you have selected for your app will be optimal for retrieving the data.</span></span>

![GetData-toiminnon analysoiminen Power Apps Monitorin avulla](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a><span data-ttu-id="ddf4d-175">Tietokyselyn suodattaminen</span><span class="sxs-lookup"><span data-stu-id="ddf4d-175">Filtering the data query</span></span>

<span data-ttu-id="ddf4d-176">Toinen tapa parantaa kyselyn suoritustehoa on rajoittaa kyselyn tuloksissa palautettujen tietueiden määrää.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-176">Another method for improving query execution performance is to limit the number of records returned in the query results.</span></span> <span data-ttu-id="ddf4d-177">Voit tehdä tämän suodattamalla tulokset, jotta voit varmistaa, että vastaanotat vain tarvitsemasi tietueet.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-177">You can do this by filtering the results to ensure that you are only receiving the records you need.</span></span>

<span data-ttu-id="ddf4d-178">Lisätietoja kyselytietojen suodatuksesta on [suodatustuloksissa](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results).</span><span class="sxs-lookup"><span data-stu-id="ddf4d-178">See [Filter results](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for more information on filtering query data.</span></span>

### <a name="limiting-the-page-size-of-the-query"></a><span data-ttu-id="ddf4d-179">Kyselyn sivun koon rajoittaminen</span><span class="sxs-lookup"><span data-stu-id="ddf4d-179">Limiting the page size of the query</span></span>

<span data-ttu-id="ddf4d-180">Jos käytät suuria tietojoukkoja, voit jakaa kyselyn tulokset useiksi sivuiksi lisäämällä haluamasi `odata.maxpagesize`-otsikon tietokyselyihin.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-180">If you're working with large data sets, you can divide query results into multiple pages by adding the `odata.maxpagesize` preference header to data queries.</span></span>

<span data-ttu-id="ddf4d-181">Lisätietoja sivutus-osasta on kohdassa [Sivulle palautettavan yksiköiden määrittäminen](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span><span class="sxs-lookup"><span data-stu-id="ddf4d-181">For more information on paging, see [Specify the number of entities to return in a page](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span></span>

## <a name="see-also"></a><span data-ttu-id="ddf4d-182">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="ddf4d-182">See also</span></span>

- [<span data-ttu-id="ddf4d-183">Määritä Dataverse -virtuaalitaulukot</span><span class="sxs-lookup"><span data-stu-id="ddf4d-183">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)
- [<span data-ttu-id="ddf4d-184">Human Resources -virtuaalitaulukoiden usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="ddf4d-184">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)
- [<span data-ttu-id="ddf4d-185">Rajoittamisen usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="ddf4d-185">Throttling FAQ</span></span>](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]