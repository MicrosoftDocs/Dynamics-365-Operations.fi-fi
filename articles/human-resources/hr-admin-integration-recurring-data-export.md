---
title: Toistuvien tietovientien sovelluksen luomisen
description: Tässä artikkelissa esitellään, miten luodaan Microsoft Azure -logiikkasovellus, joka vie tietoja Microsoft Dynamics 365 Human Resourcesista toistuvalla aikataululla.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cef9e7f78646a4a5794eb14a9f1ad355768480644504c548afbb32e23fff4cd5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744867"
---
# <a name="create-a-recurring-data-export-app"></a>Toistuvien tietovientien sovelluksen luomisen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa esitellään, miten luodaan Microsoft Azure -logiikkasovellus, joka vie tietoja Microsoft Dynamics 365 Human Resourcesista toistuvalla aikataululla. Opas hyödyntää Human Resourcesin DMF-paketin REST-sovellusohjelmointirajapintaa (API) tietojen viemiseen. Kun tiedot on viety, logiikkasovellus tallentaa viedyn tietopaketin Microsoft OneDrive for Business -kansioon.

## <a name="business-scenario"></a>Liiketoimintaskenaario

Yhdessä Microsoft Dynamics365 -integrointien tyypillisessä liiketoimintaskenaariossa tiedot on vietävä ketjussa jäljempänä olevaan järjestelmään toistuvalla aikataululla. Tässä oppaassa esitellään, miten kaikki työntekijätietueet viedään Dynamics 365 Human Resourcesista ja tallennetaan työntekijäluetteloon OneDrive for Business -kansiossa.

> [!TIP]
> Tässä oppaassa vietävät tiedot ja vietyjen tietojen kohde ovat vain esimerkkejä. Voit helposti muuttaa ne yrityksesi tarpeiden mukaisiksi.

## <a name="technologies-used"></a>Käytetyt teknologiat

Tässä oppaassa käytetään seuraavia teknologioita:

- **[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – Vietävien työntekijöiden päätietolähde.
- **[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – Teknologia, joka vastaa toistuvan viennin järjestelyistä ja ajoituksesta.

    - **[Yhdistimet](/azure/connectors/apis-list)** – Teknologia, jota käytetään logiikkasovelluksen yhdistämiseen tarvittaviin päätepisteisiin.

        - [HTTP ja Azure AD](/connectors/webcontents/) -yhdistin
        - [OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness) -yhdistin

- **[DMF-paketin REST API](../fin-ops-core/dev-itpro/data-entities/data-management-api.md)** – Teknologia, jota käytetään viennin käynnistämiseen ja sen edistymisen seurantaan.
- **[OneDrive for Business](https://onedrive.live.com/about/business/)** – Vietävien työntekijöiden kohde.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin aloitat tämän oppaan mukaisen harjoituksen, seuraavien edellytysten on täytyttävä:

- Human Resources -ympäristö, jolla on järjestelmänvalvojatason käyttöoikeudet ympäristössä
- [Azure-tilaus](https://azure.microsoft.com/free/) logiikkasovelluksen isännöintiä varten

## <a name="the-exercise"></a>Harjoitus

Tämän harjoituksen lopussa sinulla on Human Resources -ympäristöösi ja OneDrive for Business -tiliisi yhdistetty logiikkasovellus. Logiikkasovellus vie tietopaketin Human Resourcesista, odottaa viennin valmistumista, lataa viedyn tietopaketin ja tallentaa tietopaketin määrittämääsi OneDrive for Business -kansioon.

Valmis logiikkasovellus muistuttaa seuraavaa kuvaa.

![Logiikkasovelluksen yleiskuva.](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a>Vaihe 1: Luo tietojen vientiprojekti Human Resourcesissa

Luo Human Resourcesissa tietojen vientiprojekti, joka vie työntekijöitä. Anna projektille nimi **Vie työntekijät** ja varmista, että asetuksen **Luo tietopaketti** arvona on **Kyllä**. Lisää projektiin yksittäinen yksikkö (**Työntekijä**) ja valitse muoto, jossa vienti suoritetaan. (Tässä oppaassa käytetään Microsoft Excel -muotoa.)

![Vie työntekijät -tietoprojekti.](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> Muista tietojen vientiprojektin nimi. Tarvitset sitä, kun luot logiikkasovelluksen seuraavassa vaiheessa.

### <a name="step-2-create-the-logic-app"></a>Vaihe 2: Luo logiikkasovellus

Tämän harjoituksen keskeisin osa on logiikkasovellus.

1. Luo logiikkasovellus Azure-portaalissa.

    ![Logiikkasovelluksen luontisivu.](media/integration-logic-app-creation-1.png)

2. Aloita Logic Apps Designer tyhjällä logiikkasovelluksella.
3. Lisää [Toistuvan aikataulun käynnistin](/azure/connectors/connectors-native-recurrence) suorittamaan sovellus 24 tunnin välein (tai valitsemasi aikataulun mukaan).

    ![Toistuvuuden valintaikkuna.](media/integration-logic-app-recurrence-step.png)

4. Kutsu [ExportToPackage](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API aikatauluttamaan tietopakettisi vienti.

    1. Käytä HTTP ja Azure AD -yhdistimen **Aktivoi HTTP-pyyntö** -toimintoa.

        - **Perusresurssin URL:** Human Resources -ympäristösi URL-osoite (älä sisällytä polku-/nimitilatietoja).
        - **Azure AD -resurssin URI:** `http://hr.talent.dynamics.com`

        > [!NOTE]
        > Human Resources -palvelussa ei vielä ole yhdistintä, joka saisi näkyviin kaikki DMF-paketin REST API:t (esim. **ExportToPackage**). Sen sijaan ohjelmointirajapintoja on kutsuttava raaoilla HTTP-pyynnöillä HTTP ja Azure AD -yhdistimen kautta. Tämä yhdistin käyttää Azure Active Directorya (Azure AD) Human Resources -todennukseen ja valtuutukseen.

        ![HTTP ja Azure AD -yhdistin.](media/integration-logic-app-http-aad-connector-step.png)

    2. Kirjaudu Human Resources -ympäristöösi HTTP ja Azure AD -yhdistimen kautta.
    3. Määritä HTTP:n **KIRJAA**-pyyntö kutsuaksesi DMF REST API:n **ExportToPackage**.

        - **Menetelmä:** KIRJAA
        - **Pyynnön URL-osoite:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
        - **Pyynnön teksti:**

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Aktivoi HTTP-pyyntötoiminto.](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > Sinun saattaa kannattaa nimetä kukin vaihe uudelleen, jotta se on merkityksellisempi kuin oletusnimi **Aktivoi HTTP-pyyntö**. Voit esimerkiksi nimetä tämän vaiheen uudelleen muotoon **ExportToPackage**.

5. [Alusta muuttuja](/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) tallentaaksesi **ExportToPackage**-pyynnön suoritustilan.

    ![Alusta muuttujatoiminto.](media/integration-logic-app-initialize-variable-step.png)

6. Odota, kunnes tietojen viennin suoritustila on **Onnistui**.

    1. Lisää [Kunnes-silmukka](/azure/logic-apps/logic-apps-control-flow-loops#until-loop), joka toistuu, kunnes **ExecutionStatus**-muuttujan arvo on **Onnistui**.
    2. Lisää **Viive**-toiminto, joka odottaa viisi sekuntia, ennen kuin se kysyy viennin kulloistakin suoritustilaa.

        ![Kunnes-silmukan kontti.](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > Määritä raja-arvoksi **15**, jos haluat odottaa enintään 75 sekuntia (15 toistoa × 5 sekuntia) viennin valmistumiseen. Jos vientisi vaatii enemmän aikaa, säädä raja-arvoa sen mukaan.        

    3. Lisää **Aktivoi HTTP-pyyntö** -toiminto kutsumaan DMF REST API [GetExecutionSummaryStatus](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) ja asettamaan **ExecutionStatus**-muuttujan arvoksi **GetExecutionSummaryStatus**-vastauksen tulos.

        > Tässä esimerkissä ei suoriteta virheiden tarkistusta. Ohjelmointirajapinta **GetExecutionSummaryStatus** voi palauttaa epäonnistuneita päätetiloja (eli muita tiloja kuin **Onnistui**). Lisätietoja on kohdassa [API-dokumentaatio](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).

        - **Menetelmä:** KIRJAA
        - **Pyynnön URL-osoite:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
        - **Pyynnön teksti** body('Invoke\_an\_HTTP\_request')?['value']

            > [!NOTE]
            > Sinun on ehkä syötettävä **Pyynnön teksti** -arvo joko suunnitteluohjelman koodinäkymässä tai toimintoeditorissa.

        ![Aktivoi HTTP-pyyntötoiminto 2.](media/integration-logic-app-get-execution-status-step.png)

        ![Muuttujatoiminnon määrittäminen.](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > **Määritä muuttuja** -toiminnon arvo (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) eroaa **Aktivoi HTTP-pyyntö 2** -tekstin arvosta, vaikka suunnitteluohjelma näyttää arvot samalla tavalla.

7. Hae viedyn paketin URL-latausosoite.

    - Lisää **Aktivoi HTTP-pyyntö** -toiminto kutsuaksesi DMF REST-API:n [getexportdpackageurl](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST-API-liittymään.

        - **Menetelmä:** KIRJAA
        - **Pyynnön URL-osoite:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
        - **Pyynnön teksti:** {"executionId": body('GetExportedPackageURL')?['value']}

        ![GetExportedPackageURL-toiminto.](media/integration-logic-app-get-exported-package-step.png)

8. Lataa viety paketti.

    - Lisää HTTP:n **HAE** -pyyntö (sisäinen [HTTP-yhdistintoiminto](/azure/connectors/connectors-native-http)), joka lataa paketin edellisessä vaiheessa palautetusta URL-osoitteesta.

        - **Menetelmä:** HAE
        - **URI:** body('Invoke\_an\_HTTP\_request\_3').value

            > [!NOTE]
            > Sinun on ehkä syötettävä **URI**-arvo joko suunnitteluohjelman koodinäkymässä tai toimintoeditorissa.

        ![HTTP GET -toiminto.](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > Tämä pyyntö ei edellytä lisätodennusta, **getexportdpackageurl**-API:n palauttama URL-osoite sisältää jaetun käytön allekirjoitustunnuksen, joka myöntää käyttöoikeuden ladattuun tiedostoon.

9. Tallenna ladattu paketti käyttäen[OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness) -yhdistintä.

    - Lisää OneDrive for Business [Luo tiedosto](/connectors/onedriveforbusinessconnector/#create-file) -toiminto.
    - Muodosta yhteys OneDrive for Business -tiliisi tarpeen mukaan.

        - **Kansiopolku:** Valitsemasi kansio
        - **Tiedoston nimi:** työntekijä\_package.zip
        - **Tiedoston sisältö:** Edellisen vaiheen teksti (dynaaminen sisältö)

        ![Luo tiedosto -toiminto.](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a>Vaihe 3: Testaa logiikkasovelllus

Testaa logiikkasovelluksesi valitsemalla suunnitteluohjelman **Suorita**-painike. Näet, että logiikkaohjelman vaiheita aletaan suorittaa. 30–40 sekunnin kuluttua logiikkasovelluksen suorittamisen pitäisi loppua, ja OneDrive for Business -kansiossasi pitäisi nyt olla uusi viedyt työntekijät sisältävä pakettitiedosto.

Jos jossakin vaiheessa ilmenee virhe, valitse kyseinen vaihe suunnitteluohjelmassa ja tutki sen kentät **Syötteet** ja **Tuotokset**. Korjaa virheet ja muuta vaihetta tarpeen mukaan virheiden korjaamiseksi.

Seuraavassa kuvassa näytetään, miltä Logic Apps Designer näyttää, kun kaikki logiikkasovelluksen vaiheet suoritetaan onnistuneesti.

![Onnistunut logiikkasovelluksen suoritus.](media/integration-logic-app-successful-run.png)

## <a name="summary"></a>Yhteenveto

Tässä oppaassa tutustuit logiikkasovelluksen käyttöön tietojen viemiseen Human Resourcesista ja vietyjen tietojen tallentamiseen OneDrive for Business -kansioon. Voit muokata tämän oppaan vaiheita yrityksesi tarpeiden mukaan.




[!INCLUDE[footer-include](../includes/footer-banner.md)]