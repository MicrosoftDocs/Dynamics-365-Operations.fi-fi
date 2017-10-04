---
title: "Analytiikan lisääminen työtiloihin Power BI Embeddedin avulla"
description: "Tässä ohjeaiheessa kerrotaan, miten Power BI -raportti upotetaan työtilan Analytiikka-välilehteen."
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations, Platform, UnifiedOperations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.intro: Platform update 8
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: e819aafbdf55fbc2a6dc996d275244de1e11d89b
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a>Analytiikan lisääminen työtiloihin Power BI Embeddedin avulla

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Ominaisuutta tuetaan Dynamics 365 for Finance and Operationsin versiossa 7.2 ja sitä uudemmissa versioissa.

# <a name="introduction"></a>Johdanto
Tässä ohjeaiheessa kerrotaan, miten Microsoft Power BI -raportti upotetaan työtilan **Analytiikka**-välilehteen. Tässä esimerkissä Kuljetuskaluston hallinta -sovelluksen **Varausten hallinta** -työtila laajennetaan upottamaan analyysityötila **Analytiikka**-välilehteen.

# <a name="prerequisites"></a>Edellytykset
+ Ympäristön päivityksessä 8 tai sitä uudemmassa päivityksessä käytössä olevan kehitysympäristön käyttö.
+ Microsoft Power BI Desktopilla luotu analyysiraportti (.pbix-tiedosto), jonka tietomallin lähteenä on Yksikkösäilö-tietokanta.

# <a name="overview"></a>Yleiskuvaus
Riippumatta siitä laajennatko aiemmin luodun sovellustyötilan vai otatko käyttöön oman uuden työtilan, voit käyttää upotettuja analyysinäkymiä ja saada niiden kautta hyödyllistä ja vuorovaikutteista tietoa liiketoimintatiedoista. Analyysityötilan välilehti lisätään neljässä vaiheessa.

1. Lisää .pbix-tiedosto Dynamics 365 -resurssina.
2. Määritä analyysityötilan välilehti.
3. Upota .pbix-resurssi työtilan välilehteen.
4. Valinnainen: Lisää laajennuksia näkymää mukauttamalla.

> [!NOTE]
> Lisätietoja analyysiraporttien luomisesta on ohjeaiheessa [Power BI Desktopin käytön aloittaminen](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/). Tällä sivulla on tietoja tavoista, joilla voit luoda vaikuttavia analyysiraporttiratkaisuja.

# <a name="add-a-pbix-file-as-a-resource"></a>.pbix-tiedoston lisääminen resurssina
Ennen aloittamista on luotava tai haettava työtilaan upotettava Power BI -raportti. Lisätietoja analyysiraporttien luomisesta on ohjeaiheessa [Power BI Desktopin käytön aloittaminen](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).
 
Lisää .pbix-tiedosto Visual Studio -projektin artefakti.

1. Luo uusi projekti sopivassa mallissa-
2. Valitse ratkaisunhallinnassa projekti, napsauta hiiren kakkospainikkeella ja valitse sitten **Lisää** > **Uusi nimike**.
3. Valitse **Lisää uusi nimike** -valintaikkunan **Toimintojen artefaktit** -kohdassa **Resurssi**-malli.
4. Anna nimi, jolla viitataan X++-metatietojen raporttiin ja valitse sitten **Lisää**.

    ![Lisää uusi nimike -valintaikkuna](media/analytical-workspace-add.png)

5. Etsi analyysiraportin määritelmän sisältävä .pbix-tiedosto ja valitse sitten **Avaa**.

    ![Valitse resurssitiedosto -valintaikkuna](media/analytical-workspace-select-resource.png)
  
Nyt kun .pbix-tiedosto on lisätty Dynamics 365 -resurssina, voit upottaa raportteja työtiloihin ja lisätä suoria linkkejä valikkovaihtoehtojen avulla.

# <a name="add-a-tab-control-to-an-application-workspace"></a>Välilehtiohjausobjektin lisääminen sovelluksen työtilaan
Tässä esimerkissä Kuljetuskaluston hallinta -mallin **Varausten hallinta** -työtilaa laajennetaan lisäämällä **Analytiikka**-välilehti **FMClerkWorkspace**-lomakkeen määritelmään.
 
Seuraavassa kuvassa näytetään, miltä **FMClerkWorkspace**-lomake näyttää Microsoft Visual Studion suunnittelutoiminnossa.

![FMClerkWorkspace-lomake ennen muutoksia](media/analytical-workspace-definition-before.png)

Laajenna **Varausten hallinta** -työtilan lomakemääritystä seuraavien ohjeiden mukaisesti.

1. Laajenna suunnittelumääritelmä avaamalla lomakkeen suunnittelutila.
2. Valitse suunnittelumäärityksessä ylin elementti, jonka nimi on **Rakenne | Kuvio: työtila toiminnassa**.
3. Napsauta hiiren kakkospainikkeella, valitse **Uusi** > **Välilehti** ja lisää uusi **FormTabControl1**-niminen ohjausobjekti.
4. Valitse lomakkeen suunnittelutilassa **FormTabControl1**.
5. Napsauta hiiren kakkospainikkeella ja lisää uusi välilehtisivu valitsemalla **Uusi välilehtisivu**.
6. Anna välilehtisivulla uusi merkityksellinen nimi, kuten **Työtila**.
7. Valitse lomakkeen suunnittelutilassa **FormTabControl1**.
8. Napsauta hiiren kakkospainikkeella ja valitse sitten **Uusi välilehtisivu**.
9. Anna välilehtisivulla uusi merkityksellinen nimi, kuten **Analytiikka**.
10. Valitse lomakkeen suunnittelutilassa **Analytiikka (välilehtisivu)**.
11. Määritä **Otsikko**-ominaisuudeksi **Analytiikka**.
12. Napsauta ohjausobjektia hiiren kakkospainikkeella ja lisää sitten uusi lomakeryhmän ohjausobjekti valitsemalla **Uusi** > **Ryhmä**.
13. Anna lomakeryhmälle uusi merkityksellinen nimi, kuten **powerBIReportGroup**.
14. Valitse lomakkeen suunnittelutilassa **PanoramaBody (välilehti)** ja vedä ohjausobjekti sitten **Työtila**-välilehteen.
15. Valitse suunnittelumäärityksessä ylin elementti, jonka nimi on **Rakenne | Kuvio: työtila toiminnassa**.
16. Napsauta hiiren kakkospainikkeella ja valitse sitten **Poista kuvio**.
17. Napsauta hiiren kakkospainikkeella uudelleen ja valitse sitten **Lisää kuvio** > **Välilehdellinen työtila**.
18. Tarkista muutokset luomalla koontiversio.
 
Seuraava kuva osoittaa, miltä rakenne näyttää muutosten jälkeen.

![FMClerkWorkspace muutosten jälkeen](media/analytical-workspace-definition-after.png)

Nyt kun työtilan raportin upottamiseen käytettävät lomakkeen ohjausobjektit on lisätty, pääohjausobjektin koko on määritettävä asetteluun sopivaksi. Oletusarvoisesti sekä **Suodatinruutu**-sivu että **Välilehti**-sivu näkyvät raportissa. Voit kuitenkin muuttaa näiden ohjausobjektien näkyvyyttä raportin kohdekäyttäjän mukaan.
 
> [!NOTE]
> Upotetuissa työtiloissa kannattaa käyttää laajennuksia, jotka piilottavat yhdenmukaisuuden vuoksi sekä **Suodatinruutu**- että **Välilehti**-sivut.
 
Olet nyt suorittanut sovelluksen lomakemäärityksen laajennustehtävän. Lisätietoja mukautusten tekemisestä laajennusten avulla on ohjeaiheessa [Mukauttaminen: lisäykset ja laajennukset](../extensibility/customization-overlayering-extensions.md).

# <a name="add-x-business-logic-to-embed-a-viewer-control"></a>Katseluohjausobjektin upottaminen lisäämällä X++-liiketoimintalogiikka
Lisää näiden ohjeiden mukaisesti liiketoimintalogiikka, joka käynnistää **Varausten hallinta** -työtilaan upotetun raportin katseluohjelman ohjausobjektin.

1. Laajenna suunnittelumääritys avaamalla **FMClerkWorkspace**-lomakkeen suunnittelutila.
2. Käytä koodimäärityksen taustalla olevaa koodia F7-näppäimellä.
3. Lisää seuraava X++-koodi.

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;     
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                FMPBIWorkspaceController controller = new FMPBIWorkspaceController();
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
    }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. Tarkista muutokset luomalla koontiversio.

Olet nyt suorittanut tehtävän, jolla upotetun raportin katseluohjelman ohjausobjektin käynnistävä liiketoimintalogiikka lisätään. Seuraava kuva osoittaa, miltä työtila näyttää muutosten jälkeen.

![Työtilaan upotettu raportti](media/analytical-workspace-final.png)

> [!NOTE]
> Voit käyttää aiemmin luotua toimintonäkymää käyttämällä sivun otsikkoon kuuluvia työtilan välilehtiä.

# <a name="reference"></a>Viite

## <a name="pbireporthelperinitializereportcontrol-method"></a>PBIReportHelper.initializeReportControl-menetelmä
Tässä osassa on tietoja aputoimintoluokasta, jolla Power BI -rapotti (.pbix-resurssi) upotetaan lomakeryhmän ohjausobjektiin.

### <a name="syntax"></a>Syntaksi
```
public static void initializeReportControl(
     str                 _resourceName,
     FormGroupControl    _formGroupControl,
     str                 _defaultPageName = '',
     boolean             _showFilterPane = false,
     boolean             _showNavPane = false,
     List                _defaultFilters = new List(Types::Class))
```

### <a name="parameters"></a>Parametrit

| Nimi | kuvaus |
|---|---|
| resourceName | .pbix-resurssin nimi. |
| formGroupControl | Lomakeryhmän ohjausobjekti, johon Power BI -raportin ohjausobjektia käytetään. |
| defaultPageName | Oletussivun nimi. |
| showFilterPane | Totuusarvo, joka ilmaisee, näytetäänkö suodatinruutu (**tosi**) vai piilotetaanko se (**epätosi**). |
| showNavPane | Totuusarvo, joka ilmaisee, näytetäänkö siirtymisruutu (**tosi**) vai piilotetaanko se (**epätosi**). |
| defaultFilters | Power BI -raportin oletussuodattimet. |
