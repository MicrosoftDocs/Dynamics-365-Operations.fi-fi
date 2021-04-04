---
title: Toistuvien tietovientien sovelluksen luomisen
description: Tässä artikkelissa esitellään, miten luodaan Microsoft Azure -logiikkasovellus, joka vie tietoja Microsoft Dynamics 365 Human Resourcesista toistuvalla aikataululla.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 5bc9b5c97f855f1d8eb44765c98473b69f96adec
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466974"
---
# <a name="create-a-recurring-data-export-app"></a><span data-ttu-id="ec1ed-103">Toistuvien tietovientien sovelluksen luomisen</span><span class="sxs-lookup"><span data-stu-id="ec1ed-103">Create a recurring data export app</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ec1ed-104">Tässä artikkelissa esitellään, miten luodaan Microsoft Azure -logiikkasovellus, joka vie tietoja Microsoft Dynamics 365 Human Resourcesista toistuvalla aikataululla.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-104">This article shows how to create a Microsoft Azure logic app that exports data from Microsoft Dynamics 365 Human Resources on a recurring schedule.</span></span> <span data-ttu-id="ec1ed-105">Opas hyödyntää Human Resourcesin DMF-paketin REST-sovellusohjelmointirajapintaa (API) tietojen viemiseen.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-105">The tutorial takes advantage of Human Resources' DMF package REST application programming interface (API) to export the data.</span></span> <span data-ttu-id="ec1ed-106">Kun tiedot on viety, logiikkasovellus tallentaa viedyn tietopaketin Microsoft OneDrive for Business -kansioon.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-106">After the data has been exported, the logic app saves the exported data package to a Microsoft OneDrive for Business folder.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="ec1ed-107">Liiketoimintaskenaario</span><span class="sxs-lookup"><span data-stu-id="ec1ed-107">Business scenario</span></span>

<span data-ttu-id="ec1ed-108">Yhdessä Microsoft Dynamics365 -integrointien tyypillisessä liiketoimintaskenaariossa tiedot on vietävä ketjussa jäljempänä olevaan järjestelmään toistuvalla aikataululla.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-108">In one typical business scenario for Microsoft Dynamics 365 integrations, data must be exported to a downstream system on a recurring schedule.</span></span> <span data-ttu-id="ec1ed-109">Tässä oppaassa esitellään, miten kaikki työntekijätietueet viedään Dynamics 365 Human Resourcesista ja tallennetaan työntekijäluetteloon OneDrive for Business -kansiossa.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-109">This tutorial shows how to export all worker records from Microsoft Dynamics 365 Human Resources and save the list of workers in a OneDrive for Business folder.</span></span>

> [!TIP]
> <span data-ttu-id="ec1ed-110">Tässä oppaassa vietävät tiedot ja vietyjen tietojen kohde ovat vain esimerkkejä.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-110">The specific data that is exported in this tutorial and the destination of the exported data are only examples.</span></span> <span data-ttu-id="ec1ed-111">Voit helposti muuttaa ne yrityksesi tarpeiden mukaisiksi.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-111">You can easily change them to meet your business needs.</span></span>

## <a name="technologies-used"></a><span data-ttu-id="ec1ed-112">Käytetyt teknologiat</span><span class="sxs-lookup"><span data-stu-id="ec1ed-112">Technologies used</span></span>

<span data-ttu-id="ec1ed-113">Tässä oppaassa käytetään seuraavia teknologioita:</span><span class="sxs-lookup"><span data-stu-id="ec1ed-113">This tutorial uses the following technologies:</span></span>

- <span data-ttu-id="ec1ed-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – Vietävien työntekijöiden päätietolähde.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – The master data source for workers that will be exported.</span></span>
- <span data-ttu-id="ec1ed-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – Teknologia, joka vastaa toistuvan viennin järjestelyistä ja ajoituksesta.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – The technology that provides orchestration and scheduling of the recurring export.</span></span>

    - <span data-ttu-id="ec1ed-116">**[Yhdistimet](https://docs.microsoft.com/azure/connectors/apis-list)** – Teknologia, jota käytetään logiikkasovelluksen yhdistämiseen tarvittaviin päätepisteisiin.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-116">**[Connectors](https://docs.microsoft.com/azure/connectors/apis-list)** – The technology that is used to connect the logic app to the required endpoints.</span></span>

        - <span data-ttu-id="ec1ed-117">[HTTP ja Azure AD](https://docs.microsoft.com/connectors/webcontents/) -yhdistin</span><span class="sxs-lookup"><span data-stu-id="ec1ed-117">[HTTP with Azure AD](https://docs.microsoft.com/connectors/webcontents/) connector</span></span>
        - <span data-ttu-id="ec1ed-118">[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) -yhdistin</span><span class="sxs-lookup"><span data-stu-id="ec1ed-118">[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector</span></span>

- <span data-ttu-id="ec1ed-119">**[DMF-paketin REST API](../dev-itpro/data-entities/data-management-api.md)** – Teknologia, jota käytetään viennin käynnistämiseen ja sen edistymisen seurantaan.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-119">**[DMF package REST API](../dev-itpro/data-entities/data-management-api.md)** – The technology that is used to trigger the export and monitor its progress.</span></span>
- <span data-ttu-id="ec1ed-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – Vietävien työntekijöiden kohde.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – The destination for the exported workers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ec1ed-121">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="ec1ed-121">Prerequisites</span></span>

<span data-ttu-id="ec1ed-122">Ennen kuin aloitat tämän oppaan mukaisen harjoituksen, seuraavien edellytysten on täytyttävä:</span><span class="sxs-lookup"><span data-stu-id="ec1ed-122">Before you begin the exercise in this tutorial, you must have the following items:</span></span>

- <span data-ttu-id="ec1ed-123">Human Resources -ympäristö, jolla on järjestelmänvalvojatason käyttöoikeudet ympäristössä</span><span class="sxs-lookup"><span data-stu-id="ec1ed-123">A Human Resources environment that has admin-level permissions in the environment</span></span>
- <span data-ttu-id="ec1ed-124">[Azure-tilaus](https://azure.microsoft.com/free/) logiikkasovelluksen isännöintiä varten</span><span class="sxs-lookup"><span data-stu-id="ec1ed-124">An [Azure subscription](https://azure.microsoft.com/free/) to host the logic app</span></span>

## <a name="the-exercise"></a><span data-ttu-id="ec1ed-125">Harjoitus</span><span class="sxs-lookup"><span data-stu-id="ec1ed-125">The exercise</span></span>

<span data-ttu-id="ec1ed-126">Tämän harjoituksen lopussa sinulla on Human Resources -ympäristöösi ja OneDrive for Business -tiliisi yhdistetty logiikkasovellus.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-126">At the end of this exercise, you will have a logic app that is connected to your Human Resources environment and your OneDrive for Business account.</span></span> <span data-ttu-id="ec1ed-127">Logiikkasovellus vie tietopaketin Human Resourcesista, odottaa viennin valmistumista, lataa viedyn tietopaketin ja tallentaa tietopaketin määrittämääsi OneDrive for Business -kansioon.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-127">The logic app will export a data package from Human Resources, wait for the export to be completed, download the exported data package, and save the data package in the OneDrive for Business folder that you specified.</span></span>

<span data-ttu-id="ec1ed-128">Valmis logiikkasovellus muistuttaa seuraavaa kuvaa.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-128">The completed logic app will resemble the following illustration.</span></span>

![Logiikansovelluksen yleiskuva](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a><span data-ttu-id="ec1ed-130">Vaihe 1: Luo tietojen vientiprojekti Human Resourcesissa</span><span class="sxs-lookup"><span data-stu-id="ec1ed-130">Step 1: Create a data export project in Human Resources</span></span>

<span data-ttu-id="ec1ed-131">Luo Human Resourcesissa tietojen vientiprojekti, joka vie työntekijöitä.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-131">In Human Resources, create a data export project that exports workers.</span></span> <span data-ttu-id="ec1ed-132">Anna projektille nimi **Vie työntekijät** ja varmista, että asetuksen **Luo tietopaketti** arvona on **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-132">Name the project **Export Workers**, and make sure that the **Generate data package** option is set to **Yes**.</span></span> <span data-ttu-id="ec1ed-133">Lisää projektiin yksittäinen yksikkö (**Työntekijä**) ja valitse muoto, jossa vienti suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-133">Add a single entity (**Worker**) to the project, and select the format to export in.</span></span> <span data-ttu-id="ec1ed-134">(Tässä oppaassa käytetään Microsoft Excel -muotoa.)</span><span class="sxs-lookup"><span data-stu-id="ec1ed-134">(Microsoft Excel format is used in this tutorial.)</span></span>

![Vie työntekijät -tietoprojekti](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> <span data-ttu-id="ec1ed-136">Muista tietojen vientiprojektin nimi.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-136">Remember the name of the data export project.</span></span> <span data-ttu-id="ec1ed-137">Tarvitset sitä, kun luot logiikkasovelluksen seuraavassa vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-137">You will need it when you create the logic app in the next step.</span></span>

### <a name="step-2-create-the-logic-app"></a><span data-ttu-id="ec1ed-138">Vaihe 2: Luo logiikkasovellus</span><span class="sxs-lookup"><span data-stu-id="ec1ed-138">Step 2: Create the logic app</span></span>

<span data-ttu-id="ec1ed-139">Tämän harjoituksen keskeisin osa on logiikkasovellus.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-139">The bulk of the exercise involves creating the logic app.</span></span>

1. <span data-ttu-id="ec1ed-140">Luo logiikkasovellus Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-140">In the Azure portal, create a logic app.</span></span>

    ![Logiikkasovelluksen luontisivu](media/integration-logic-app-creation-1.png)

2. <span data-ttu-id="ec1ed-142">Aloita Logic Apps Designer tyhjällä logiikkasovelluksella.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-142">In the Logic Apps Designer, start with a blank logic app.</span></span>
3. <span data-ttu-id="ec1ed-143">Lisää [Toistuvan aikataulun käynnistin](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) suorittamaan sovellus 24 tunnin välein (tai valitsemasi aikataulun mukaan).</span><span class="sxs-lookup"><span data-stu-id="ec1ed-143">Add a [Recurrence Schedule trigger](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) to run the logic app every 24 hours (or according to a schedule of your choice).</span></span>

    ![Toistuvuuden valintaikkuna](media/integration-logic-app-recurrence-step.png)

4. <span data-ttu-id="ec1ed-145">Kutsu [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API aikatauluttamaan tietopakettisi vienti.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-145">Call the [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API to schedule the export of your data package.</span></span>

    1. <span data-ttu-id="ec1ed-146">Käytä HTTP ja Azure AD -yhdistimen **Aktivoi HTTP-pyyntö** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-146">Use the **Invoke an HTTP request** action from the HTTP with Azure AD connector.</span></span>

        - <span data-ttu-id="ec1ed-147">**Perusresurssin URL:** Human Resources -ympäristösi URL-osoite (älä sisällytä polku-/nimitilatietoja).</span><span class="sxs-lookup"><span data-stu-id="ec1ed-147">**Base Resource URL:** The URL of your Human Resources environment (Don't include path/namespace information.)</span></span>
        - <span data-ttu-id="ec1ed-148">**Azure AD -resurssin URI:** `http://hr.talent.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="ec1ed-148">**Azure AD Resource URI:** `http://hr.talent.dynamics.com`</span></span>

        > [!NOTE]
        > <span data-ttu-id="ec1ed-149">Human Resources -palvelussa ei vielä ole yhdistintä, joka saisi näkyviin kaikki DMF-paketin REST API:t (esim. **ExportToPackage**).</span><span class="sxs-lookup"><span data-stu-id="ec1ed-149">The Human Resources service doesn't yet provide a connector that exposes all the APIs that make up the DMF package REST API, such as **ExportToPackage**.</span></span> <span data-ttu-id="ec1ed-150">Sen sijaan ohjelmointirajapintoja on kutsuttava raaoilla HTTP-pyynnöillä HTTP ja Azure AD -yhdistimen kautta.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-150">Instead, you must call the APIs by using raw HTTPS requests through the HTTP with Azure AD connector.</span></span> <span data-ttu-id="ec1ed-151">Tämä yhdistin käyttää Azure Active Directorya (Azure AD) Human Resources -todennukseen ja valtuutukseen.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-151">This connector uses Azure Active Directory (Azure AD) for authentication and authorization to Human Resources.</span></span>

        ![HTTP ja Azure AD -yhdistin](media/integration-logic-app-http-aad-connector-step.png)

    2. <span data-ttu-id="ec1ed-153">Kirjaudu Human Resources -ympäristöösi HTTP ja Azure AD -yhdistimen kautta.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-153">Sign in to your Human Resources environment through the HTTP with Azure AD connector.</span></span>
    3. <span data-ttu-id="ec1ed-154">Määritä HTTP:n **KIRJAA**-pyyntö kutsuaksesi DMF REST API:n **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-154">Set up an HTTP **POST** request to call the **ExportToPackage** DMF REST API.</span></span>

        - <span data-ttu-id="ec1ed-155">**Menetelmä:** KIRJAA</span><span class="sxs-lookup"><span data-stu-id="ec1ed-155">**Method:** POST</span></span>
        - <span data-ttu-id="ec1ed-156">**Pyynnön URL-osoite:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="ec1ed-156">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span></span>
        - <span data-ttu-id="ec1ed-157">**Pyynnön teksti:**</span><span class="sxs-lookup"><span data-stu-id="ec1ed-157">**Body of the request:**</span></span>

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Aktivoi HTTP-pyyntötoiminto](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > <span data-ttu-id="ec1ed-159">Sinun saattaa kannattaa nimetä kukin vaihe uudelleen, jotta se on merkityksellisempi kuin oletusnimi **Aktivoi HTTP-pyyntö**.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-159">You might want to rename each step so that it's more meaningful than the default name, **Invoke an HTTP request**.</span></span> <span data-ttu-id="ec1ed-160">Voit esimerkiksi nimetä tämän vaiheen uudelleen muotoon **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-160">For example, you can rename this step **ExportToPackage**.</span></span>

5. <span data-ttu-id="ec1ed-161">[Alusta muuttuja](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) tallentaaksesi **ExportToPackage**-pyynnön suoritustilan.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-161">[Initialize a variable](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) to store the execution status of the **ExportToPackage** request.</span></span>

    ![Alusta muuttujatoiminto](media/integration-logic-app-initialize-variable-step.png)

6. <span data-ttu-id="ec1ed-163">Odota, kunnes tietojen viennin suoritustila on **Onnistui**.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-163">Wait until the execution status of the data export is **Succeeded**.</span></span>

    1. <span data-ttu-id="ec1ed-164">Lisää [Kunnes-silmukka](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop), joka toistuu, kunnes **ExecutionStatus**-muuttujan arvo on **Onnistui**.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-164">Add an [Until loop](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) that repeats until the value of the **ExecutionStatus** variable is **Succeeded**.</span></span>
    2. <span data-ttu-id="ec1ed-165">Lisää **Viive**-toiminto, joka odottaa viisi sekuntia, ennen kuin se kysyy viennin kulloistakin suoritustilaa.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-165">Add a **Delay** action that waits five seconds before it polls for the current execution status of the export.</span></span>

        ![Kunnes-silmukan kontti](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > <span data-ttu-id="ec1ed-167">Määritä raja-arvoksi **15**, jos haluat odottaa enintään 75 sekuntia (15 toistoa × 5 sekuntia) viennin valmistumiseen.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-167">Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="ec1ed-168">Jos vientisi vaatii enemmän aikaa, säädä raja-arvoa sen mukaan.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-168">If your export takes more time, adjust the limit count as appropriate.</span></span>        

    3. <span data-ttu-id="ec1ed-169">Lisää **Aktivoi HTTP-pyyntö** -toiminto kutsumaan DMF REST API [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) ja asettamaan **ExecutionStatus**-muuttujan arvoksi **GetExecutionSummaryStatus**-vastauksen tulos.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-169">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>

        > <span data-ttu-id="ec1ed-170">Tässä esimerkissä ei suoriteta virheiden tarkistusta.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-170">This sample doesn't do error checking.</span></span> <span data-ttu-id="ec1ed-171">Ohjelmointirajapinta **GetExecutionSummaryStatus** voi palauttaa epäonnistuneita päätetiloja (eli muita tiloja kuin **Onnistui**).</span><span class="sxs-lookup"><span data-stu-id="ec1ed-171">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="ec1ed-172">Lisätietoja on kohdassa [API-dokumentaatio](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span><span class="sxs-lookup"><span data-stu-id="ec1ed-172">For more information, see the [API documentation](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

        - <span data-ttu-id="ec1ed-173">**Menetelmä:** KIRJAA</span><span class="sxs-lookup"><span data-stu-id="ec1ed-173">**Method:** POST</span></span>
        - <span data-ttu-id="ec1ed-174">**Pyynnön URL-osoite:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="ec1ed-174">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span></span>
        - <span data-ttu-id="ec1ed-175">**Pyynnön teksti** body('Invoke\_an\_HTTP\_request')?['value']</span><span class="sxs-lookup"><span data-stu-id="ec1ed-175">**Body of the request:** body('Invoke\_an\_HTTP\_request')?['value']</span></span>

            > [!NOTE]
            > <span data-ttu-id="ec1ed-176">Sinun on ehkä syötettävä **Pyynnön teksti** -arvo joko suunnitteluohjelman koodinäkymässä tai toimintoeditorissa.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-176">You might have to enter the **Body of the request** value either in code view or in the function editor in the designer.</span></span>

        ![Aktivoi HTTP-pyyntötoiminto 2](media/integration-logic-app-get-execution-status-step.png)

        ![Muuttujatoiminnon määrittäminen](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > <span data-ttu-id="ec1ed-179">**Määritä muuttuja** -toiminnon arvo (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) eroaa **Aktivoi HTTP-pyyntö 2** -tekstin arvosta, vaikka suunnitteluohjelma näyttää arvot samalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-179">The value for the **Set variable** action (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) will differ from the value for the **Invoke an HTTP request 2** body value, even though the designer will show the values in the same way.</span></span>

7. <span data-ttu-id="ec1ed-180">Hae viedyn paketin URL-latausosoite.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-180">Get the download URL of the exported package.</span></span>

    - <span data-ttu-id="ec1ed-181">Lisää **Aktivoi HTTP-pyyntö** -toiminto kutsuaksesi DMF REST-API:n [getexportdpackageurl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST-API-liittymään.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-181">Add an **Invoke HTTP request** action to call the [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span></span>

        - <span data-ttu-id="ec1ed-182">**Menetelmä:** KIRJAA</span><span class="sxs-lookup"><span data-stu-id="ec1ed-182">**Method:** POST</span></span>
        - <span data-ttu-id="ec1ed-183">**Pyynnön URL-osoite:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="ec1ed-183">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span></span>
        - <span data-ttu-id="ec1ed-184">**Pyynnön teksti:** {"executionId": body('GetExportedPackageURL')?['value']}</span><span class="sxs-lookup"><span data-stu-id="ec1ed-184">**Body of the request:** {"executionId": body('GetExportedPackageURL')?['value']}</span></span>

        ![GetExportedPackageURL-toiminto](media/integration-logic-app-get-exported-package-step.png)

8. <span data-ttu-id="ec1ed-186">Lataa viety paketti.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-186">Download the exported package.</span></span>

    - <span data-ttu-id="ec1ed-187">Lisää HTTP:n **HAE** -pyyntö (sisäinen [HTTP-yhdistintoiminto](https://docs.microsoft.com/azure/connectors/connectors-native-http)), joka lataa paketin edellisessä vaiheessa palautetusta URL-osoitteesta.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-187">Add an HTTP **GET** request (a built-in [HTTP connector action](https://docs.microsoft.com/azure/connectors/connectors-native-http)) to download the package from the URL that was returned in the previous step.</span></span>

        - <span data-ttu-id="ec1ed-188">**Menetelmä:** HAE</span><span class="sxs-lookup"><span data-stu-id="ec1ed-188">**Method:** GET</span></span>
        - <span data-ttu-id="ec1ed-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span><span class="sxs-lookup"><span data-stu-id="ec1ed-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="ec1ed-190">Sinun on ehkä syötettävä **URI**-arvo joko suunnitteluohjelman koodinäkymässä tai toimintoeditorissa.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-190">You might have to enter the **URI** value either in code view or in the function editor in the designer.</span></span>

        ![HTTP HAE -toiminto](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > <span data-ttu-id="ec1ed-192">Tämä pyyntö ei edellytä lisätodennusta, **getexportdpackageurl**-API:n palauttama URL-osoite sisältää jaetun käytön allekirjoitustunnuksen, joka myöntää käyttöoikeuden ladattuun tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-192">This request doesn't require any additional authentication, because the URL that the **GetExportedPackageUrl** API returns includes a shared access signatures token that grants access to download the file.</span></span>

9. <span data-ttu-id="ec1ed-193">Tallenna ladattu paketti käyttäen[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) -yhdistintä.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-193">Save the downloaded package by using the [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector.</span></span>

    - <span data-ttu-id="ec1ed-194">Lisää OneDrive for Business [Luo tiedosto](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) -toiminto.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-194">Add a OneDrive for Business [Create File](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) action.</span></span>
    - <span data-ttu-id="ec1ed-195">Muodosta yhteys OneDrive for Business -tiliisi tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-195">Connect to your OneDrive for Business account, as required.</span></span>

        - <span data-ttu-id="ec1ed-196">**Kansiopolku:** Valitsemasi kansio</span><span class="sxs-lookup"><span data-stu-id="ec1ed-196">**Folder Path:** A folder of your choice</span></span>
        - <span data-ttu-id="ec1ed-197">**Tiedoston nimi:** työntekijä\_package.zip</span><span class="sxs-lookup"><span data-stu-id="ec1ed-197">**File Name:** worker\_package.zip</span></span>
        - <span data-ttu-id="ec1ed-198">**Tiedoston sisältö:** Edellisen vaiheen teksti (dynaaminen sisältö)</span><span class="sxs-lookup"><span data-stu-id="ec1ed-198">**File Content:** The body from the previous step (dynamic content)</span></span>

        ![Luo tiedosto -toiminto](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a><span data-ttu-id="ec1ed-200">Vaihe 3: Testaa logiikkasovelllus</span><span class="sxs-lookup"><span data-stu-id="ec1ed-200">Step 3: Test the logic app</span></span>

<span data-ttu-id="ec1ed-201">Testaa logiikkasovelluksesi valitsemalla suunnitteluohjelman **Suorita**-painike.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-201">To test your logic app, select the **Run** button in the designer.</span></span> <span data-ttu-id="ec1ed-202">Näet, että logiikkaohjelman vaiheita aletaan suorittaa.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-202">You will see that the steps of the logic app start to run.</span></span> <span data-ttu-id="ec1ed-203">30–40 sekunnin kuluttua logiikkasovelluksen suorittamisen pitäisi loppua, ja OneDrive for Business -kansiossasi pitäisi nyt olla uusi viedyt työntekijät sisältävä pakettitiedosto.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-203">After 30 to 40 seconds, the logic app should finish running, and your OneDrive for Business folder should include a new package file that contains the exported workers.</span></span>

<span data-ttu-id="ec1ed-204">Jos jossakin vaiheessa ilmenee virhe, valitse kyseinen vaihe suunnitteluohjelmassa ja tutki sen kentät **Syötteet** ja **Tuotokset**.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-204">If a failure is reported for any step, select the failed step in the designer, and examine the **Inputs** and **Outputs** fields for it.</span></span> <span data-ttu-id="ec1ed-205">Korjaa virheet ja muuta vaihetta tarpeen mukaan virheiden korjaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-205">Debug and adjust the step as required to correct the errors.</span></span>

<span data-ttu-id="ec1ed-206">Seuraavassa kuvassa näytetään, miltä Logic Apps Designer näyttää, kun kaikki logiikkasovelluksen vaiheet suoritetaan onnistuneesti.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-206">The following illustration shows what the Logic Apps Designer looks like when all the steps of the logic app run successfully.</span></span>

![Onnistunut logiikkasovelluksen suoritus](media/integration-logic-app-successful-run.png)

## <a name="summary"></a><span data-ttu-id="ec1ed-208">Yhteenveto</span><span class="sxs-lookup"><span data-stu-id="ec1ed-208">Summary</span></span>

<span data-ttu-id="ec1ed-209">Tässä oppaassa tutustuit logiikkasovelluksen käyttöön tietojen viemiseen Human Resourcesista ja vietyjen tietojen tallentamiseen OneDrive for Business -kansioon.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-209">In this tutorial, you learned how to use a logic app to export data from Human Resources and save the exported data to a OneDrive for Business folder.</span></span> <span data-ttu-id="ec1ed-210">Voit muokata tämän oppaan vaiheita yrityksesi tarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-210">You can modify the steps of this tutorial as required to suit your business needs.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]