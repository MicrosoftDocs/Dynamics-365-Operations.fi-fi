---
title: Valmistuksen ja varastoinnin hallinnan kuormitusten pilvi- ja reunapalvelujen Scale Unitit
description: Tässä aiheessa on lisätietoja valmistuksen ja varastoinnin hallinnan kuormitusten pilvi- ja reunapalvelujen Scale Uniteista.
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 3a23ee452535423684c6d210a448ee768379fa08
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516776"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>Valmistuksen ja varastoinnin hallinnan kuormitusten pilvi- ja reunapalvelujen Scale Unitit

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Pilvi- ja reunapalvelujen Scale Uniteilla voidaan jakaa tuotannon ja varaston ohjauksen kuormitukset eri ympäristöihin. Tämä toiminto voi auttaa parantamaan suorituskykyä, estämään palvelukatkoja ja maksimoimaan toiminta-ajan. Sen käyttö on mahdollista seuraavien apuohjelmien avulla:

- Dynamics 365 Supply Chain Managementin pilvipalvelujen Scale Unit -apuohjelma
- Dynamics 365 Supply Chain Managementin reunapalvelujen Scale Unit -apuohjelma

Valmistuksessa ja jakelussa toimivien yritysten on voitava suorittaa keskeisiä liiketoimintaprosesseja ympärivuorokautisesti, ilman keskeytyksiä ja skaalautuvasti. Pilvi- ja reunapalvelujen Scale Unitien avulla yritykset voivat suorittaa toiminnan kannalta välttämättömiä valmistus- ja varastoprosesseja ilman keskeytyksiä myös satunnaisten verkkoyhteyksiin tai viiveisiin liittyvien ongelmien yhteydessä.

## <a name="public-preview-information"></a>Julkisen esiversion tiedot

Esiversiossa on yksi ympäristö, joka toimii pilvipohjaisena Dynamics 365 Supply Chain Management -ympäristön keskuksena, ja yksi ympäristö, joka toimii pilvipalvelujen Scale Unitina.

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a>Esiversion saatavuus

Pilvi- ja reunapalvelujen Scale Unitien esiversio on Supply Chain Managementin nykyisten asiakkaiden saatavana lokakuussa 2020.

Lokakuun esiversion 10.0.15 tai Platform update 39:n käyttöönotto [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) -ympäristössä edellyttää, että käyttäjä on Supply Chain Managementin PEAP-ohjelman jäsen. PEAP-ohjelmaan voi liittyä, jos käyttäjä on jo laajan [Dynamics Insider Program](https://experience.dynamics.com/insider) -ohjelman jäsen. Valitse siinä tapauksessa Finance & Operations: Preview early access program (PEAP) -niminen ohjelma.

> [!IMPORTANT]
> Supply Chain Managementin Scale Unit -toiminnon käyttäminen edellyttää [Finance and Operationsin pilvi- ja reunapalvelun esiversio käyttöehtojen](https://Aka.ms/SCMCnETerms) hyväksymistä.

### <a name="data-processing-for-the-preview"></a>Tietojen käsittely esiversiossa

Julkisen version aikana joitakin hallintapalveluja isännöidään vain Yhdysvalloissa. Kun ominaisuus on yleisesti saatavana, nämä hallintapalvelut ovat kuitenkin saatavana kaikilla Supply Chain Managementin tukemilla maantieteellisillä alueilla. Tämä vaikuttaa kaikkiin Scale Unitin hallinnan käyttämien hallintatietojen siirtoon ja tallennukseen. Näitä tietoja ovat esimerkiksi seuraavat:

- Vuokraajan nimet ja tunnukset
- LCS-projektin tunnukset
- Kirjautumiseen käytetyt järjestelmänvalvojan sähköpostiviestit
- Keskuksen ja Scale Unitien ympäristötunnukset
- Kuormitusmääritykset
- Kartta-analyysisivulla näkyvät kerätyt mittarit (kuten viive ja siirtomäärä)

Yhdysvaltalaisiin palvelukeskuksiin siirretyt tiedot ja niissä tallennetut tiedot poistetaan, kun esiversioympäristöt sammutetaan.

### <a name="sign-up-for-the-preview"></a>Esiversion rekisteröiminen

Supply Chain Managementin pilvi- ja reunapalvelujen esiversioon rekisteröitymistä varten organisaatiolla on jo oltava julkaistu Supply Chain Management -pilviympäristö.

Scale Unit -ominaisuudet ovat tällä hetkellä julkisia esiversioita. Rekisteröitymiseen on käytettävä tietyn vuokraajan käyttäjätiliä. Käyttäjän on myös oltava kyseisessä vuokraajassa olevan aktiivisen Dynamics 365 LCS -projektin LCS:n projektin omistaja tai ympäristön järjestelmänvalvoja.

Esiversioon rekisteröidyttäessä valitaan vuokraaja ja noudatetaan rekisteröitymisen vaiheita. Heti kun Microsoft voi varata esiversiokapasiteettia, käyttäjälle lähetetään sähköpostiviesti, joka sisältää kahden ympäristön (keskus ja Scale Unit) valmistelutiedot ja kampanjakoodit soveltuvaa LCS-projektia varten. Kaksi ympäristö voidaan ottaa tämän jälkeen käyttöön tason 2 eristysympäristöinä. Kyseiset ympäristöt ovat voimassa 60 päivää kampanjakoodien luontipäivästä alkaen. Kahta ympäristöä ei pitäisi käyttää, ennen kuin seuraavassa kappaleessa oleva vaihe on suoritettu.

Kun olet vahvistanut Microsoftille, että kaksi ympäristöä on otettu käyttöön kampanjakoodien avulla, toinen ympäristöstä määritetään toimimaan keskuksena ja toinen Scale Unitina. Scale Unitit voidaan sitten määrittää ja ottaa käyttöön valituissa varastonhallinnan ja valmistuksen työkuormissa [Scale Unitin hallintaportaalin](https://aka.ms/SCMSUM) avulla.

Esiversioympäristöt poistetaan automaattisesti 60 päivän kuluttua. Ne voidaan kuitenkin poistaa myös aiemmin, jos vaikuttaa siltä, ettei niitä käytetä. Kun esiversioympäristöt on poistettu, käyttäjä voi rekisteröityä jonottamaan uuden esiversion käyttöönottoa.

Esiversioon voidaan rekisteröityä [Scale Unitin hallintaportaalissa](https://aka.ms/SCMSUM).

### <a name="limitations-that-apply-during-the-preview-period"></a>Esiversiojakson aikana käytössä olevat rajoitukset

> [!IMPORTANT]
> Tämän ominaisuuden esiversio-ohjelman ensimmäisessä vaiheessa Microsoft tukee vain keskuksia, joissa on pilvipalvelujen Scale Uniteja. Se ei siis tue keskuksia, joissa on reunapalvelujen Scale Uniteja. Reunapalvelun Scale Unitit asennetaan paikallisesti, ja niiden odotetaan oleva saatavana ohjelman tulevassa vaiheessa.

Koska pilvi- ja reunapalvelujen Scale Unitit ovat esiversion ominaisuus, niihin liittyvien palvelujen saatavuus on rajoitettu tiettyihin maihin ja tietyille alueille. Ottamalla pilvi- ja reunapalvelujen scale unitit käyttöön käyttäjä vahvistaa ymmärtävänsä, että joitakin pilvi- ja reunapalvelujen scale unitien määrityksiin ja käsittelyyn liittyviä tietoja voidaan tallentaa Yhdysvalloissa sijaitsevaan palvelinkeskukseen. Ottamalla pilvi- ja reunapalvelujen scale unitit käyttöön käyttäjä myös hyväksyy [Finance and Operationsin pilvi- ja reunapalvelujen esiversion käyttöehdot](https://Aka.ms/SCMCnETerms). Lisätietoja pilvi- ja reunapalvelujen scale uniteista on [dokumentaatiossa](https://aka.ms/scmcne).

Tietosuojasi on tärkeää Microsoftille. Lisätietoja on [tietosuojatiedoissa](https://aka.ms/privacy).

> [!IMPORTANT]
> Joitakin liiketoimintatoimintoja ei tueta kokonaisuudessaan julkisessa esiversiossa, kun kuormituksia käytetään scale uniteissa. Lisätietoja toiminnallisista kuormituksista on jäljempänä tässä aiheessa.

## <a name="scale-units-and-dedicated-workloads"></a>Scale unitit ja erilliset kuormitukset

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 ja scale unitit":::

Scale unitit laajentavat Supply Chain Management -keskusympäristöä lisäämällä erillisestä käsittelykapasiteettia. Scale unitit voidaan suorittaa pilvessä. Vaihtoehtoisesti ne voidaan suorittaa paikallisena reunapalveluna omissa tiloissa. Scale unitien yhteys keskusympäristöön voidaan katkaista tilapäisesti. Kun scale unitit on yhdistetty, ne vastaanottavat kaiken tiedot, jota tarvitaan määritettyjen kuormitusten erilliseen käsittelyyn.

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="Scale unit -vaihtoehdot julkisessa esiversiossa":::

Julkisessa esiversiossa keskusympäristöön voidaan määrittää pilvipalvelun scale unitin valitut kuormitukset Scale Unit -hallintaportaalissa. Jos esiversioon osallistuvalla on paikallisen ympäristön paikallisten liiketoimintatietojen käyttöoikeus, paikallisten liiketoimintatietojen ympäristö voidaan määrittää myös reunapalvelujen scale unitina.

Kuormitus määritetään liiketoimintatoimintojen joukkona, joka voidaan jättää huomioimatta ja delegoida scale unitiin. Esiversiossa on tällä hetkellä kahdenlaisia kuormituksia:

- Tuotannonohjaus
- Varastonhallinta  

Kuhunkin scale unitiin voidaan määrittää yksi kuormitus kutakin tyyppiä. 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Scale unitin erillisen tuotannonohjauksen kuormituksen ominaisuudet

Tuotannonohjauksessa pilvi- ja reunapalvelujen scale uniteissa on seuraavat ominaisuudet myös silloin, kun reunapalvelujen yksiköt eivät ole yhteydessä pilvipalveluun:

- Koneenkäyttäjät ja työnjohtajat voivat käyttää operatiivista tuotantosuunnitelmaa.
- Koneenkäyttäjät voivat pitää suunnitelman ajan tasalla suorittamalla erillisen valmistuksen ja prosessivalmistuksen töitä.
- Tuotannoin työnjohtaja voi muokata operatiivista suunnitelmaa.
- Työntekijät voivat käyttää reunapalvelujen työajanseurantaa kellokorttina ja varmistaa näin oikean palkanlaskennan.

Lisätietoja on kohdassa [Tuotannon scale unitin kuormitustiedot](cloud-edge-workload-manufacturing.md).

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Scale unitin erillisen varastonhallinnan kuormituksen ominaisuudet

Varastonhallinnan pilvi- ja reunapalvelujen scale uniteissa on seuraavat ominaisuudet myös silloin, kun reunapalvelujen yksiköt eivät ole yhteydessä pilvipalveluun:

- Valittujen aaltomenetelmien käsittely on otettu käyttöön myyntitilauksissa ja kysynnän täydennyksessä.
- Varastotyöntekijät voivat suorittaa myynnin ja kysynnän täydennyksen varastotyön käyttämällä varastosovellusta.
- Varastotyöntekijät voivat tehdä varastosovelluksella kyselyjä käytettävissä olevasta varastosta.
- Varastotyöntekijät voivat luoda ja suorittaa varastosiirtoja varastosovelluksella.
- Varastotyöntekijät voivat rekisteröidä ostotilauksia ja tehdä hyllytyksiä varastosovelluksella.

Lisätietoja on kohdassa [Varaston scale unitin kuormitustiedot](cloud-edge-workload-warehousing.md).

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a>Supply Chain Management -ympäristön scale unitien käyttöönottaminen

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a>Pilvi- ja reunapalvelujen scale unitien ottaminen käyttöön

Seuraavassa kuvassa on pilvipalvelujen scale unitien esiversion rekisteröitymisen ja valmistelun työnkulku.

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="Esiversion rekisteröitymisvaiheet":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a>LCS-projektin vuokraajan valitseminen ja yksityiskohtainen esiversioprosessi

Julkisessa esiversiossa [Scale Unit -hallintaportaalissa](https://aka.ms/SCMSUM) on luettelo vuokraajista, joiden osa tili on ja joissa käyttäjä on LCS-projektin omistaja tai ympäristön järjestelmänvalvoja.

Jos toivottu vuokraaja ei ole tässä luettelossa, siirry [LCS:hen](https://lcs.dynamics.com/v2) ja varmista, että olet joko kyseisen vuokraajan LCS-projektin ympäristön järjestelmänvalvoja tai projektin omistaja. Huomaa, että rekisteröityminen sallitaan vain valitun vuokraajan Azure Active Directory (Azure AD) -tileille.

> [!NOTE]
> Kun muutokset on tehty LCS:ssä, muutoksen päivittyminen vuokraajaluetteloon voi kestää 30 minuuttia.

Rekisteröitymisen tila näkyy kunkin luettelossa olevan vuokraajan kohdalla.

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="Vuokraajan rekisteröitymisasetus":::

Voit osallistua esiversioon rekisteröimällä LCS-vuokraajan valitsemalla **Rekisteröidy napsauttamalla tätä** -linkin. Käyttöehdot on hyväksyttävä. Lisäksi on annetta yrityksen sähköpostiosoite, johon Microsoft voi lähettää esiversioon rekisteröitymisprosessiin liittyviä viestejä.

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="Vuokraajan rekisteröitymisen lähettäminen":::

Microsoft tarkistaa pyynnön ja ilmoittaa seuraavista vaiheista lähettämällä sähköpostia rekisteröitymislomakkeessa annettuun osoitteeseen.

Sen jälkeen kun sinut on hyväksytty esiversio-ohjelmaan, saat kaksi kampanjakoodia LCS-projektia varten. Voit nyt ottaa kaksi ympäristöä käyttöön LCS:ssä näiden kampanjakoodien avulla. Ympäristöissä on oltava käytössä vähintään PEAP 10.0.15. Kun olet käyttänyt kampanjakoodit, ilmoita siitä Microsoftille (ohjeiden mukaisesti), jotta esiversiotoiminnot voidaan ottaa niissä käyttöön. Microsoft ilmoittaa, kun tämä määritysvaihe on valmis.

Voit nyt aloittaa scale unitien ja kuormitusten määrittäminen esiversioympäristössä.

> [!IMPORTANT]
> Pilvipalvelujen scale unit -määritysten [kaikki tarvittavat vaiheet voidaan tehdä Scale Unit -hallintaportaalissa](#scale-unit-manager-portal).
<!-- >
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Pilvipalvelun scale unitien ja kuormitusten hallinta Scale Unit -hallintaportaalissa

Siirry [Scale Unit -hallintaportaaliin](https://aka.ms/SCMSUM) ja käytä kirjautumiseen vuokraajan tiliä. Voit lisätä keskusympäristön **Määritä scale unitit** -sivulla, jos se ei ole vielä luettelossa. Voit sitten valita keskuksen, johon haluat määrittää scale unitit ja kuormitukset.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Scale unitin ja kuormituksen hallintakokemus":::

Jos haluat lisätä vähintään yhden topologiassa olevan scale unit, valitse **Lisää scale uniteja**. Esiversiossa pitäisi näkyä se pilvipalvelun scale unit, joka otettiin käyttöön toisella esiversio-ohjelman osana vastaanotetulla kampanjakoodilla.

<!-- > [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

Lisää varastonhallinnan tai tuotannonohjauksen kuormitus yhteen scale unitiin valitsemalla **Määritetyt kuormitukset** -välilehdessä **Luo kuormitus** -painike. Kunkin kuormituksen osalta on määritettävä kuormituksen omistamien prosessien konteksti. Varastonhallinnan kuormituksissa konteksti on tietyn toimipaikan ja yrityksen tietty varasto. Tuotannonohjauksen kuormituksissa konteksti on yrityksen tietty toimipaikka.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Kuormituksen luominen":::

> [!IMPORTANT]
> Esiversion Scale Unit -hallintaportaalissa ei voi poistaa kuormituksia scale uniteista eikä poistaa scale unitin määritystä keskukseen sen jälkeen, kun määritys on tehty. Jos määritys on poistettava, ota yhteys esiversio-ohjelman hallinnan yhteyshenkilöön.

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->


[!INCLUDE[footer-include](../../includes/footer-banner.md)]