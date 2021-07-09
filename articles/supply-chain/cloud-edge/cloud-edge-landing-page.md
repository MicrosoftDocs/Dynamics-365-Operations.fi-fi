---
title: Valmistuksen ja varastoinnin hallinnan kuormitusten pilvi- ja reunapalvelujen Scale Unitit
description: Tässä aiheessa on lisätietoja valmistuksen ja varastoinnin hallinnan kuormitusten pilvi- ja reunapalvelujen Scale Uniteista.
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 24c322712edf1277eabfdd708f528d89bcf43640
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261743"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>Pilven ja reunan asteikon yksiköt valmistuksen ja varaston hallinnan kuormituksia varten

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Microsoft Dynamics 365 Supply Chain Managementin skaalausyksikköominaisuudet ovat käytettävissäsi palvelun käyttöä säätelevillä ehdoilla. Lisätietoja on kohdassa [Microsoft Dynamicsin oikeudelliset tiedot](https://go.microsoft.com/fwlink/?LinkID=290927).
>
> Ottamalla pilvi- ja reunapalvelujen scale unitit käyttöön käyttäjältä pyydetään vahvistus, että hän ymmärtää, että joitakin pilvi- ja reunapalvelujen scale unitien määrityksiin ja käsittelyyn liittyviä tietoja voidaan tallentaa Yhdysvalloissa sijaitsevaan palvelinkeskukseen. Lisätietoja pilvipalvelun ja reunan skaalausyksiköiden tietojenkäsittelystä on [tietojenkäsittely skaalausyksiköiden hallinnan aikana](#data-processing-management) -osassa myöhemmin tässä aiheessa.

## <a name="core-value-proposition-for-scale-units"></a>Skaalausyksiköiden ydinarvoehdotus

Valmistuksessa ja jakelussa toimivien yritysten on voitava suorittaa keskeisiä liiketoimintaprosesseja ympärivuorokautisesti, ilman keskeytyksiä ja skaalautuvasti. Pilvi- ja reunapalvelujen Scale Unitien avulla yritykset voivat suorittaa toiminnan kannalta välttämättömiä valmistus- ja varastoprosesseja ilman keskeytyksiä myös satunnaisten verkkoyhteyksiin tai viiveisiin liittyvien ongelmien yhteydessä.

Pilvi- ja reunapalvelujen Scale Uniteilla voidaan jakaa tuotannon ja varaston ohjauksen kuormitukset eri ympäristöihin. Tämä toiminto voi auttaa parantamaan suorituskykyä, estämään palvelukatkoja ja maksimoimaan toiminta-ajan. Skaalausyksiköt tarjotaan Supply Chain Managementin ylläpitosopimukseen seuraavien apuohjelmien kautta:

- Cloud Scale Unitin apuohjelma Dynamics 365 Supply Chain Managementille (*saatavana huhtikuussa 2021*)
- Edge Scale Unitin apuohjelma Dynamics 365 Supply Chain Managementille (*saatavana pian*)

Kuormituksen ominaisuuksia vapautetaan jatkuvasti lisäparannusten avulla.

## <a name="scale-units-and-dedicated-workloads"></a>Scale unitit ja erilliset kuormitukset

Scale unitit laajentavat Supply Chain Management -keskusympäristöä lisäämällä erillisestä käsittelykapasiteettia. Scale unitit voidaan suorittaa pilvessä. Vaihtoehtoisesti ne voidaan suorittaa reunapalveluna, paikallisena omissa tiloissa.

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 ja scale unitit":::

Skaalausyksiköt tarjoavat määritetyn kuormituksen sietokykyä, luotettavuutta ja skaalaamista. Edge scale unitit voidaan väliaikaisesti irrottaa pilvikeskuksen ympäristöstä, ja työntekijät jatkavat työskentelyä reunalla määritetyissä kuormituksissa.

*Kuormitus* määritetään liiketoimintatoimintojen joukkona, joka voidaan jättää huomioimatta ja delegoida scale unitiin. Vaikka varastonhallinnan kuormitus on vapautettu, valmistuksen suorittamisen kuormitus on vielä esikatselussa.

Voit määrittää keskittimesi ympäristön ja cloud scale unitit valituille kuormituksille käyttämällä [Scale Unit -hallintaportaalia](https://sum.dynamics.com). Voit myös määrittää useita kuormituksia scale unitia kohti. Lisätietoja nykyisen version cloud scale unitien edellytyksistä ja rajoituksista on jäljempänä [cloud scale unitien edellytykset ja rajoitukset](#cloud-scale-unit-prerequisites) -osassa myöhemmin tässä ohjeaiheessaa.

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Scale unitin erillisen varastonhallinnan kuormituksen ominaisuudet

Varastonhallinnan kuormitus on ensimmäinen skaalausyksiköiden jaettu kuormitus, joka on vapautettu yleiseen saatavuuteen.

Skaalausyksiköt toimittavat varastonhallinnassa seuraavat toiminnot:

- Järjestelmä voi käsitellä valittuja aaltomenetelmiä myyntitilauksissa ja kysynnän täydennyksessä.
- Varastotyöntekijät voivat suorittaa myynnin ja kysynnän täydennyksen varastotyön käyttämällä varastonhallinnan mobiilisovellusta.
- Varastotyöntekijät voivat tehdä varastonhallinnan mobiilisovelluksella kyselyjä käytettävissä olevasta varastosta.
- Varastotyöntekijät voivat luoda ja suorittaa varastosiirtoja varastonhallinnan mobiilisovelluksella.
- Varastotyöntekijät voivat rekisteröidä ostotilauksia ja tehdä hyllytyksiä varastonhallinnan mobiilisovelluksella.

Lisätietoja on kohdassa [Varaston hallinnan kuormitukset pilven ja reunan asteikon yksiköitä varten](cloud-edge-workload-warehousing.md).

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Scale unitin erillisen tuotannonohjauksen kuormituksen ominaisuudet

Valmistuksen kuormituksen ensimmäinen versio on esiversiona, ja se sisältää seuraavat toiminnot:

- Koneenkäyttäjät ja työnjohtajat voivat käyttää operatiivista tuotantosuunnitelmaa.
- Koneenkäyttäjät voivat pitää suunnitelman ajan tasalla suorittamalla erillisen valmistuksen ja prosessivalmistuksen töitä.
- Tuotannoin työnjohtaja voi muokata operatiivista suunnitelmaa.
- Työntekijät voivat käyttää reunapalvelujen työajanseurantaa kellokorttina ja varmistaa näin oikean palkanlaskennan.

Lisätietoja on kohdassa [Pilvi- ja reunapalvelujen Scale Unitien tuotannonohjauksen kuormitukset](cloud-edge-workload-manufacturing.md).

## <a name="considerations-before-you-enable-the-distributed-hybrid-topology-for-supply-chain-management"></a>Huomioon otettavia seikkoja ennen jakelun hybriditopologian käyttöönottoa Supply Chain Managementissa

Ottamalla jaetut hybriditopologiat käyttöön siirrät Supply Chain Managementin pilviympäristön niin, että se toimii keskuksena. Voit myös liittää muita ympäristöjä, jotka on määritetty skaalausyksiköiksi pilvipalvelussa tai reunalla.

### <a name="prerequisites-and-limitations-for-cloud-scale-units"></a><a name="cloud-scale-unit-prerequisites"></a>Cloud scale unitien edellytykset ja rajoitukset

Skaalausyksiköiden nykyisessä versiossa jotkin toiminnot eivät ole vielä käytettävissä, mutta ne voidaan lisätä asteittain.

#### <a name="you-must-be-a-licensed-customer-of-supply-chain-management"></a>Sinun on oltava Supply Chain Managementin lisensoitu asiakas

Jotta voit olla mukana jaetussa topologiassa, sinulla on oltava Supply Chain Managementin lisenssi. Aiemmin luodusta pilviympäristöstä tulee hybriditopologiassasi keskus. Voit ilmoittaa sekä eristysympäristöt että tuotantoympäristöt keskittimen ympäristöiksi ja voit lisätä yksiköitä saamiesi apuohjelmien mukaan.

#### <a name="your-existing-project-must-be-administered-via-the-global-commercial-version-of-lcs"></a>Aiemmin luotua projektia täytyy käyttää LCS:n yleisen kaupallisen version kautta

Aiemmin luodun Microsoft Dynamics Lifecyle Services (LCS) -projektin on täytettävä seuraavat versiovaatimukset:

- Projektia täytyy käyttää LCS:n yleisen kaupallisen version kautta osoitteessa [lcs.dynamics.com](https://lcs.dynamics.com).
- LCS:n paikallisia versioita (kuten [eu.lcs.dynamics.com](https://eu.lcs.dynamics.com) ja [fr.lcs.dynamics.com](https://fr.lcs.dynamics.com)) ei tueta.
- LCS:n viranomaispilvipalveluversioita ei tueta.
- LCS:n Mooncake-versiota ei tueta.

#### <a name="your-current-production-environment-must-be-of-the-self-service-type-in-lcs"></a>Nykyisen tuotantoympäristön tyypin on oltava itsepalvelutyyppi LCS:ssä

Nykyisen tuotantoympäristön on oltava merkitty **itsepalvelu**-tyyppiin LCS:ssä. Tämä tyyppi ilmaisee, että LCS-projektin vuokraaja on jo muunnettu niin, että se tukee Azure Service Fabric -isännöintimallia.

> [!IMPORTANT]
> Ympäristötyyppejä, jotka suorittavat infrastruktuurin palveluna (IaaS) ei tueta. Nämä ympäristöt on tyypillisesti merkitty **Microsoftin hallitsemiksi** tyypeiksi LCS:ssä. Jos käytössä on tämän tyyppisiä ympäristöjä, ota yhteys Microsoftin yhteyshenkilöön ja ota huomioon siirron aikajana **itsepalvelu**-tyypiksi.

Microsoft on siirtämässä kaikki Supply Chain Managementin pilviympäristöt IaaS-mallista topologiaan, joka sijaitsee Service Fabricissa. Tämä siirto helpottaa skaalattavuutta ja helpottaa huoltohallintaa. Tämän vuoksi käyttöönotto- ja ylläpitotoiminnot ovat nopeampia. Samoin palvelukomponentteja siirretään mikropalveluiden käsitteeseen, ja palvelun isännöintimalli [siirtyy](https://docs.microsoft.com/virtualization/windowscontainers/about/containers-vs-vm) näennäiskonemallista (VM) kevyeen säilöjä käyttävään arkkitehtuurimalliin.

Lopulta sama Service Fabriciin perustuva säilöjen käyttöön perustuva palveluinstanssi tehostaa sekä pilvipalvelu- että reunaesiintymiä riippumatta siitä, onko esiintymä pilvipalvelussa vai skaalausyksikössä vai reunalla.

Ennen kuin voit siirtyä hybriditopologiaan, joka tukee skaalausyksiköitä, projektin vuokraajan on siirryttävä Service Fabric –isännöityyn malliin. Lisäksi on muunnettava kaikki ympäristöt, jotka toimivat keskittimenä.

> [!TIP]
> Jos haluat tehdä kyselyn LCS-projektin vuokraajasta, etsi ympäristösi tyyppi [LCS:stä](https://lcs.dynamics.com/) tai ota yhteys yhteistyökumppaniisi tai Microsoftin yhteyshenkilöön.

#### <a name="local-business-data-on-premises-environments-arent-supported-as-hubs-for-scale-units"></a>Paikallisia liiketoimintatieto (paikalliset) -ympäristöjä ei tueta skaalausyksiköiden keskittiminä

Paikalliset ympäristöt eivät voi toimia skaalausyksiköiden keskittiminä. Keskitinympäristöt ovat aina pilvipalveluja.

#### <a name="scale-unit-management-capabilities-are-limited"></a>Skaalausyksikköjen hallintaominaisuudet ovat rajallisia

Hallintaominaisuudet, jotka voivat auttaa kuormitusten siirtoja, ovat rajoitettuja. Joitakin hallintatoimintoja ei tueta itsepalveluna, ja sinun on ehkä pyydettävä tukea yhteistyökumppanisi tai Microsoftin yhteyshenkilön kautta. Esimerkkejä tällaisista ovat esimerkiksi skaalausyksiköiden väliset siirrot ja tilapäiset ad-hoc-siirrot hätätilanteissa.

#### <a name="metrics-and-measurements-arent-yet-available"></a>Mittarit ja mittaukset eivät ole vielä käytettävissä

Mittareita ja mittauksia, jotka auttavat valitsemaan skaalausyksiköiden parhaan sovelluksen, ei ole vielä käytettävissä. Valitse tehokkain sovellus yhdessä Microsoftin yhteyshenkilön tai käyttöönottokumppanin kanssa.

### <a name="data-processing-during-management-of-scale-units"></a><a name="data-processing-management"></a>Tietojenkäsittely skaalausyksiköiden hallinnan aikana

Kun otat Dynamics 365 -ympäristösi käyttöön jaetussa, hybriditopologiassa pilvipalveluissa ja reunan skaalausyksiköissä, joitakin hallintapalveluja ylläpidetään vain Yhdysvalloissa, kuten LCS:ssä. Tämä toiminta vaikuttaa joihinkin [Scale Unit Manager -portaalissa](https://sum.dynamics.com) käytettämiin hallinta- ja konfigurointitietojen siirtoon ja varastointiin. Seuraavassa on muutamia esimerkkejä:

- Vuokraajan nimet ja tunnukset
- LCS-projektin tunnukset
- Järjestelmänvalvojan ja projektin omistajan sähköpostiosoitteet, joita käytetään kirjautumisen yhteydessä
- Keskuksen ja Scale Unitien ympäristötunnukset
- Kuormituskonfiguraatiot sekä niiden nimet ja fyysiset osoitteet, jotta topologiasi voidaan näyttää maantieteellisessä kartassa
- Kerätyt mittarit (kuten viive ja siirtomäärä), jotka näkyvät kartta-analyysisivulla ja auttavat valitsemaan mahdollisimman suotuisan käyttötavan skaalausyksiköille

Yhdysvalloissa datakeskuksiin siirrettävät ja tallennetut tiedot poistetaan Microsoftin tietojen säilytyskäytäntöjen mukaisesti. Tietosuojasi on tärkeää Microsoftille. Lisätietoja on [tietosuojatiedoissa](https://go.microsoft.com/fwlink/?LinkId=521839).

## <a name="onboarding-in-two-stages"></a>Mukana on kaksi vaihetta

Jakeluun jaetussa hybriditopologiassa on kaksi vaihetta. Ensimmäisen vaiheen aikana mukautukset on vahvistettava, jotta ne toimivat jaetussa topologiassa, jossa on skaalausyksiköitä. Sen vuoksi eristys- ja tuotantoympäristöt siirretään vain toisen vaiheen aikana.

### <a name="stage-1-evaluate-customizations-in-one-box-development-environments"></a>Vaihe 1: Mukautusten arvioiminen yhden ruudun kehitysympäristöissä

Ennen kuin aloitat eristys- tai tuotantoympäristön tuomisen, suosittelemme, että tutustut skaalausyksiköihin kehitysasetuksissa, kuten yhden laatikon ympäristössä (eli tier-1-ympäristössä), jotta voit vahvistaa prosessit, mukautukset ja ratkaisut. Tässä vaiheessa tietoja ja mukautuksia käytetään yksiruutuissa ympäristöissä. Yksi ympäristö ottaakeskittimen roolin ja toinen ottaa roolin skaalausyksikönä. Nämä asetukset ovat paras tapa tunnistaa ja korjata ongelmia. Myös viimeisintä ennakkokäyttökoontiversiota (PEAP) voi käyttää tämän vaiheen suorittamiseen.

Vaiheessa 1 on käytettävä [skaalausyksikön käyttöönottotyökaluja yhden ruudun kehitysympäristöissä](https://github.com/microsoft/SCMScaleUnitDevTools). Näiden työkalujen avulla voit konfiguroida skaalausyksiköt yhdessä tai kahdessa erillisessä yksiruutuisessa ympäristössä. Työkalut toimitetaan binaarijulkaisuna ja lähdekoodina GitHubissa. Tutki projektia, joka sisältää [vaiheittaiset käyttöoppaat](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide), jotka kuvaavat työkalujen käyttöä.

### <a name="stage-2-acquire-add-ins-and-deploy-in-your-sandbox-and-production-environments"></a>Vaihe 2: Apuohjelmien hankkiminen ja käyttöönotto eristys- ja tuotantoympäristöissäsi

Jos haluat siirtyä jostakin eristys- tai tuotantoympäristöstäsi uuteen topologiaan, sinun on hankittava lisäosat yhdelle tai useammalle cloud scale unitille (ja tulevaisuudessa edge scale unitille). Apuohjelmat myöntävät [LCS:ssä](https://lcs.dynamics.com/) vastaavat projekti- ja ympäristöpaikat, jotta skaalausyksikön ympäristöjä voidaan käyttää.

> [!NOTE]
> Skaalausyksikköjen apuohjelmia ei liitetä rajoitettuun käyttäjämäärään, vaan kuka tahansa olemassa olevan ylläpitosopimuksen käyttäjä voi käyttää niitä roolien perusteella, jotka järjestelmänvalvoja määrittää.

Skaalausyksiköitä on saatavilla useassa varastointiyksikössä (SKUs) ja hinnoitteluvaihtoehdoissa. Näin ollen voit valita vaihtoehdon, joka vastaa parhaiten suunniteltujen kuukausittaisten tapahtumien volyymia ja suorituskykyvaatimuksia.

Lähtötason SKU on *Perustaso* ja sitä suorituskykyisempää SKU:ta kutsutaan *vakiotasoksi*. Jokaiselle SKU:lle on esiladattu tietty määrä kuukausitapahtumia. Voit kuitenkin suurentaa kuukausittaista tapahtumabudjettia lisäämällä kullekin SKU:lle ylitysapuohjelmia.

:::image type="content" source="media/SKUs-highlevel.png" alt-text="Cloud Scale Unitin apuohjelmat":::

> [!TIP]
> Tunnista tarpeisiisi parhaiten sopiva koko toimimalla kumppanisi ja Microsoftin kanssa ymmärtääksesi tarvitsemasi kuukausittainen tapahtumakoko.

Kunkin skaalausyksikön lisäosan osto ei vain anna sinulle tapahtumien kuukausittaista määrää, vaan myös oikeuttaa tiettyyn määrään ympäristöpaikkoja LCS:ssä. Sinulla on oikeus jokaista Cloud Scale Unit -apuohjelmaa kohti uuteen tuotantopaikkaan ja uuteen eristysympäristöpaikkaan. Mukana on myös uusi LCS-projekti, joka sisältää nämä lisäprojektit. Paikkojen käyttöoikeudet on sidottu siten, että paikkoja on käytettävä skaalausyksikköinä, joissa on pilvikeskitin.

Ylitysten apuohjelmat eivät anna oikeutta uusiin ympäristöpaikkoihin.

Jos haluat hankkia lisää eristysympäristöjä, voit ostaa tavallisia eristysympäristöpaikkoja. Microsoft voi tämän jälkeen auttaa sinua mahdollistamaan näiden eristysympäristön skaalausyksiköiden käyttöönoton hybriditopologiassa.

## <a name="onboard-to-the-distributed-hybrid-topology-for-supply-chain-management"></a>Ota käyttöön jaettu hybriditopologia Supply Chain Managementille

### <a name="select-your-lcs-project-tenant-and-the-detailed-onboarding-process"></a>LCS-projektin vuokraajan valitseminen ja yksityiskohtainen käyttöönottoprosessi

Kun olet suunnitellut valmiiksi miten olet mukana Supply Chain Managementin jaetussa hybriditopologiassa, voit aloittaa käyttöönottoprosessin [Scale Unit Manager -portaalin](https://aka.ms/SCMSUM) avulla. Valitse portaalissa **Dynamics 365 -vuokralaiset** -välilehti. Välilehdellä on luettelo vuokraajista, joiden osa tili on ja joissa käyttäjä on LCS-projektin omistaja tai ympäristön järjestelmänvalvoja.

Jos toivottu vuokraaja ei ole luettelossa, siirry [LCS:hen](https://lcs.dynamics.com/v2) ja varmista, että olet joko kyseisen vuokraajan LCS-projektin ympäristön järjestelmänvalvoja tai projektin omistaja. Rekisteröityminen sallitaan vain valitun vuokraajan Azure Active Directory (Azure AD) -tileille.

> [!NOTE]
> Kun muutokset on tehty LCS:ssä, muutoksen päivittyminen vuokraajaluetteloon voi kestää 30 minuuttia.

Käyttöönoton tila näkyy kunkin luettelossa olevan vuokraajan kohdalla.

:::image type="content" source="media/cloud_edge-EnableHybrid1.png" alt-text="Vuokralaisten luettelo Dynamics 365 -vuokralaiset -välilehdessä":::

Valitse **Napsauta tästä aloittaaksesi** pyytääksesi käyttöönoton LCS-vuokraajalle. Käyttöehdot on hyväksyttävä. Lisäksi on annetta yrityksen sähköpostiosoite, johon Microsoft voi lähettää käyttöönottoprosessiin liittyviä viestejä.

:::image type="content" source="media/cloud_edge-EnableHybrid2.png" alt-text="Vuokraajan rekisteröitymisen lähettäminen":::

Microsoft tarkistaa pyynnön ja ilmoittaa seuraavista vaiheista lähettämällä sähköpostia rekisteröitymislomakkeessa annettuun osoitteeseen. Microsoft tekee tiivistä yhteistyötä, jotta skaalausyksiköt voidaan ottaa käyttöön hybriditopologiassa liiketoimintaskenaariossa.

Kun käyttöönottosi on valmis, voit konfiguroida skaalausyksiköt ja kuormituksen portin avulla.

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Pilvipalvelun scale unitien ja kuormitusten hallinta Scale Unit -hallintaportaalissa

Siirry [Scale Unit -hallintaportaaliin](https://aka.ms/SCMSUM) ja käytä kirjautumiseen vuokraajan tiliä. Voit lisätä keskusympäristön **Määritä scale unitit** -sivulla, jos se ei ole vielä luettelossa. Voit sitten valita keskuksen, johon haluat määrittää scale unitit ja kuormitukset.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Scale unitin ja kuormituksen hallintakokemus":::

Jos haluat lisätä vähintään yhden tilauksessa olevan skaalausyksikön, valitse **Lisää skaalausyksiköitä**.

Lisää varastonhallinnan kuormitus yhteen scale unitiin valitsemalla **Määritetyt kuormitukset** -välilehdessä **Luo kuormitus** -painike. Kunkin kuormituksen osalta on määritettävä kuormituksen omistamien prosessien konteksti. Varastonhallinnan kuormituksissa konteksti on tietyn toimipaikan ja yrityksen tietty varasto.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Kuormituksen luominen":::

> [!TIP]
> Ajan mittaan skaalausyksikköjen hallintakokemukseen lisätään lisäparannuksia, jotka helpottavat elinkaarenhallinnan toimintoja. Nykyisen julkaisun erityisominaisuudet on dokumentoitu mukana olevassa käyttökirjassa, joka on niiden asiakkaiden käytettävissä, jotka ovat mukana mukana jaetussa hybriditopologiassa Supply Chain Managementia varten. <!-- KFM: Add a link to the handbook when it is published -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
