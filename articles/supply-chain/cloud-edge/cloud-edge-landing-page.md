---
title: Asteikon yksiköt jaetussa hybriditopologiassa
description: Tässä aiheessa on lisätietoja valmistuksen ja varastoinnin hallinnan kuormitusten pilvi- ja reunapalvelujen Scale Uniteista.
author: cabeln
ms.date: 04/22/2021
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 30f455f37b5161878cf9c864b92966aa74da051f
ms.sourcegitcommit: b52ff5dfd32580121f74a5f262e5c2495e39d578
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376179"
---
# <a name="scale-units-in-a-distributed-hybrid-topology"></a>Asteikon yksiköt jaetussa hybriditopologiassa

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Microsoft Dynamics 365 Supply Chain Managementin skaalausyksikköominaisuudet ovat käytettävissäsi palvelun käyttöä säätelevillä ehdoilla. Lisätietoja on kohdassa [Microsoft Dynamicsin oikeudelliset tiedot](https://go.microsoft.com/fwlink/?LinkID=290927).
>
> Ottamalla pilvi- ja reunapalvelujen scale unitit käyttöön käyttäjältä pyydetään vahvistus, että hän ymmärtää, että joitakin pilvi- ja reunapalvelujen scale unitien määrityksiin ja käsittelyyn liittyviä tietoja voidaan tallentaa Yhdysvalloissa sijaitsevaan palvelinkeskukseen. Lisätietoja pilvipalvelun ja reunan skaalausyksiköiden tietojenkäsittelystä on [tietojenkäsittely skaalausyksiköiden hallinnan aikana](#data-processing-management) -osassa myöhemmin tässä aiheessa.

## <a name="core-value-proposition-for-a-distributed-hybrid-topology"></a>Jaetun hybriditopologian ydinarvoehdotus

Valmistuksessa ja jakelussa toimivien yritysten on voitava suorittaa keskeisiä liiketoimintaprosesseja ympärivuorokautisesti, ilman keskeytyksiä ja skaalautuvasti. Jaetun hybriditopologian avulla yritykset voivat suorittaa toiminnan kannalta välttämättömiä valmistus- ja varastoprosesseja ilman keskeytyksiä myös satunnaisten verkkoyhteyksiin tai viiveisiin liittyvien ongelmien yhteydessä.

Jaetussa hybriditopologiassa otetaan käyttöön *scale unitit*, jotka mahdollistavat tuotannon ja varaston toteutustyökuormien jakamisen eri ympäristöihin. Tämä toiminto voi auttaa parantamaan suorituskykyä, estämään palvelukatkoja ja maksimoimaan toiminta-ajan. Skaalausyksiköt tarjotaan Supply Chain Managementin ylläpitosopimukseen seuraavien apuohjelmien kautta:

- Dynamics 365 Supply Chain Managementin pilvipalvelujen Scale Unit -apuohjelma
- Dynamics 365 Supply Chain Managementin reunapalvelujen Scale Unit -apuohjelma

Kuormituksen ominaisuuksia vapautetaan jatkuvasti lisäparannusten avulla.

## <a name="scale-units-and-dedicated-workloads"></a>Scale unitit ja erilliset kuormitukset

Scale unitit laajentavat Supply Chain Management -keskusympäristöä lisäämällä erillisestä käsittelykapasiteettia. Scale unitit voidaan suorittaa pilvessä. Vaihtoehtoisesti ne voidaan suorittaa [reuna](cloud-edge-edge-scale-units-lbd.md)palveluna, paikallisena omissa tiloissa.

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 ja scale unitit.":::

Skaalausyksiköt tarjoavat määritetyn kuormituksen sietokykyä, luotettavuutta ja skaalaamista. Edge scale unitit voidaan väliaikaisesti irrottaa pilvikeskuksen ympäristöstä, ja työntekijät jatkavat työskentelyä reunalla määritetyissä kuormituksissa.

*Kuormitus* määritetään liiketoimintatoimintojen joukkona, joka voidaan jättää huomioimatta ja delegoida scale unitiin. Vaikka varastonhallinnan kuormitus on vapautettu, valmistuksen suorittamisen kuormitus on vielä esikatselussa.

Voit määrittää keskittimesi ympäristön ja cloud scale unitit valituille kuormituksille käyttämällä [Scale Unit -hallintaportaalia](https://sum.dynamics.com). Voit myös määrittää useita kuormituksia scale unitia kohti. Lisätietoja nykyisen version cloud scale unitien edellytyksistä ja rajoituksista on jäljempänä [cloud scale unitien edellytykset ja rajoitukset](#cloud-scale-unit-prerequisites) -osassa myöhemmin tässä ohjeaiheessaa.

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Scale unitin erillisen varastonhallinnan kuormituksen ominaisuudet

Varastonhallinnan kuormituksen avulla varastotyövaiheet voidaan skaalata ja suorittaa joustavassa ympäristössä käyttämällä yksittäisiä ylläpitoikkunoita. Varastonhallinnan kuormitus tukee useimpia yrityksen varastohallinnan prosesseja. Lisätietoja on kohdassa [Varaston hallinnan kuormitukset pilven ja reunan asteikon yksiköitä varten](cloud-edge-workload-warehousing.md).

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Scale unitin erillisen tuotannonohjauksen kuormituksen ominaisuudet

Valmistuksen kuormitukseen sisältyy seuraavat ominaisuudet:

- Koneenkäyttäjät ja työnjohtajat voivat käyttää operatiivista tuotantosuunnitelmaa.
- Koneenkäyttäjät voivat pitää suunnitelman ajan tasalla suorittamalla erillisen valmistuksen ja prosessivalmistuksen töitä.
- Tuotannoin työnjohtaja voi muokata operatiivista suunnitelmaa.
- Työntekijät voivat käyttää reunapalvelujen työajanseurantaa kellokorttina ja varmistaa näin oikean palkanlaskennan.

Lisätietoja on kohdassa [Pilvi- ja reunapalvelujen Scale Unitien tuotannonohjauksen kuormitukset](cloud-edge-workload-manufacturing.md).

## <a name="considerations-before-you-enable-the-distributed-hybrid-topology-for-supply-chain-management"></a>Huomioon otettavia seikkoja ennen jaetun hybriditopologian käyttöönottoa Supply Chain Managementissa

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

Microsoft on siirtämässä kaikki Supply Chain Managementin pilviympäristöt IaaS-mallista topologiaan, joka sijaitsee Service Fabricissa. Tämä siirto helpottaa skaalattavuutta ja helpottaa huoltohallintaa. Tämän vuoksi käyttöönotto- ja ylläpitotoiminnot ovat nopeampia. Samoin palvelukomponentteja siirretään mikropalveluiden käsitteeseen, ja palvelun isännöintimalli [siirtyy](/virtualization/windowscontainers/about/containers-vs-vm) näennäiskonemallista (VM) kevyeen säilöjä käyttävään arkkitehtuurimalliin.

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

Kun otat Dynamics 365 -ympäristösi käyttöön jaetussa hybriditopologiassa pilvipalveluissa ja reunan skaalausyksiköissä, joitakin hallintapalveluja ylläpidetään vain Yhdysvalloissa, kuten LCS:ssä. Tämä toiminta vaikuttaa joihinkin [Scale Unit Manager -portaalissa](https://sum.dynamics.com) käytettämiin hallinta- ja konfigurointitietojen siirtoon ja varastointiin. Seuraavassa on muutamia esimerkkejä:

- Vuokraajan nimet ja tunnukset
- LCS-projektin tunnukset
- Järjestelmänvalvojan ja projektin omistajan sähköpostiosoitteet, joita käytetään kirjautumisen yhteydessä
- Keskuksen ja Scale Unitien ympäristötunnukset
- Kuormituskonfiguraatiot sekä niiden nimet ja fyysiset osoitteet, jotta topologiasi voidaan näyttää maantieteellisessä kartassa
- Kerätyt mittarit (kuten viive ja siirtomäärä), jotka näkyvät kartta-analyysisivulla ja auttavat valitsemaan mahdollisimman suotuisan käyttötavan skaalausyksiköille

Yhdysvalloissa datakeskuksiin siirrettävät ja tallennetut tiedot poistetaan Microsoftin tietojen säilytyskäytäntöjen mukaisesti. Tietosuojasi on tärkeää Microsoftille. Lisätietoja on [tietosuojalausekkeessa](https://go.microsoft.com/fwlink/?LinkId=521839).

## <a name="onboard-to-the-distributed-hybrid-topology-for-supply-chain-management"></a>Ota käyttöön jaettu hybriditopologia Supply Chain Managementille

### <a name="try-out-the-distributed-hybrid-topology"></a>Kokeile jaettua hybriditopologiaa

Jaetun hybriditopologian käyttöönotossa on kaksi vaihetta. Ensimmäisen vaiheen aikana [kokeilet](cloud-edge-try-out.md) ratkaisua ja mukautukset on vahvistettava, jotta ne toimivat jaetussa topologiassa, jossa on skaalausyksiköitä. (Oikeellisuustarkistuksen voi tehdä olemassa olevien kehitysympäristöjen avulla.) Tämän jälkeen voit jatkaa toiseen vaiheeseen, jossa hankit tuotantoympäristöjä.

## <a name="select-your-lcs-project-tenant-and-the-detailed-onboarding-process"></a>LCS-projektin vuokraajan valitseminen ja yksityiskohtainen käyttöönottoprosessi

Skaalausyksiköitä on saatavilla useassa varastointiyksikössä (SKUs) ja hinnoitteluvaihtoehdoissa. Näin ollen voit valita vaihtoehdon, joka vastaa parhaiten suunniteltujen kuukausittaisten tapahtumien volyymia ja suorituskykyvaatimuksia.

> [!TIP]
> Tunnista tarpeisiisi parhaiten sopiva koko toimimalla toteutuskumppanisi ja Microsoftin kanssa ymmärtääksesi tarvitsemasi kuukausittainen tapahtumakoko.

Lähtötason SKU on *Perustaso* ja sitä suorituskykyisempää SKU:ta kutsutaan *vakiotasoksi*. Jokaiselle SKU:lle on esiladattu tietty määrä kuukausitapahtumia. Voit kuitenkin suurentaa kuukausittaista tapahtumabudjettia lisäämällä kullekin SKU:lle ylitysapuohjelmia.

:::image type="content" source="media/SKUs-highlevel.png" alt-text="Cloud Scale Unitin apuohjelmat.":::

> [!NOTE]
> Skaalausyksikköjen lisäosia ei ole määritetty rajoitetulle määrälle käyttäjiä. Ne ovat ylläpitosopimuksen kaikkien käyttäjien käytettävissä (edellyttäen, että järjestelmänvalvoja on määrittänyt tarvittavat käyttäjäroolit heille).

Kunkin skaalausyksikön lisäosan osto ei vain anna sinulle tapahtumien kuukausittaista määrää, vaan myös oikeuttaa tiettyyn määrään ympäristöpaikkoja LCS:ssä. Sinulla on oikeus jokaista Cloud Scale Unit -apuohjelmaa kohti uuteen tuotantopaikkaan ja uuteen eristysympäristöpaikkaan. Mukana on myös uusi LCS-projekti, joka sisältää nämä lisäprojektit. Paikkojen käyttöoikeudet on sidottu siten, että paikkoja on käytettävä skaalausyksikköinä, joissa on pilvikeskitin.

Ylitysten apuohjelmat eivät anna oikeutta uusiin ympäristöpaikkoihin.

Jos haluat hankkia lisää eristysympäristöjä, voit ostaa tavallisia eristysympäristöpaikkoja. Microsoft voi tämän jälkeen auttaa sinua mahdollistamaan näiden eristysympäristön skaalausyksiköiden käyttöönoton hybriditopologiassa.


Kun olet suunnitellut valmiiksi miten olet mukana Supply Chain Managementin jaetussa hybriditopologiassa, voit aloittaa käyttöönottoprosessin [Scale Unit Manager -portaalin](https://aka.ms/SCMSUM) avulla. Valitse portaalissa **Dynamics 365 -vuokralaiset** -välilehti. Välilehdellä on luettelo vuokraajista, joiden osa tili on ja joissa käyttäjä on LCS-projektin omistaja tai ympäristön järjestelmänvalvoja.

Jos toivottu vuokraaja ei ole luettelossa, siirry [LCS:hen](https://lcs.dynamics.com/v2) ja varmista, että olet joko kyseisen vuokraajan LCS-projektin ympäristön järjestelmänvalvoja tai projektin omistaja. Rekisteröityminen sallitaan vain valitun vuokraajan Azure Active Directory (Azure AD) -tileille.

> [!NOTE]
> Kun muutokset on tehty LCS:ssä, muutoksen päivittyminen vuokraajaluetteloon voi kestää 30 minuuttia.

Käyttöönoton tila näkyy kunkin luettelossa olevan vuokraajan kohdalla.

:::image type="content" source="media/cloud_edge-EnableHybrid1.png" alt-text="Vuokraajien luettelo Dynamics 365 -vuokraajat -välilehdessä.":::

Valitse **Napsauta tästä aloittaaksesi** pyytääksesi käyttöönoton LCS-vuokraajalle. Käyttöehdot on hyväksyttävä. Lisäksi on annetta yrityksen sähköpostiosoite, johon Microsoft voi lähettää käyttöönottoprosessiin liittyviä viestejä.

:::image type="content" source="media/cloud_edge-EnableHybrid2.png" alt-text="Vuokraajan rekisteröitymisen lähettäminen.":::

Microsoft tarkistaa pyynnön ja ilmoittaa seuraavista vaiheista lähettämällä sähköpostia rekisteröitymislomakkeessa annettuun osoitteeseen. Microsoft tekee tiivistä yhteistyötä, jotta skaalausyksiköt voidaan ottaa käyttöön hybriditopologiassa liiketoimintaskenaariossa.

Kun käyttöönottosi on valmis, voit konfiguroida skaalausyksiköt ja kuormituksen portin avulla.

### <a name="manage-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Scale unitien ja kuormitusten hallinta Scale Unit -hallintaportaalissa

Siirry [Scale Unit -hallintaportaaliin](https://aka.ms/SCMSUM) ja käytä kirjautumiseen vuokraajan tiliä. Voit lisätä keskusympäristön **Määritä scale unitit** -sivulla, jos se ei ole vielä luettelossa. Voit sitten valita keskuksen, johon haluat määrittää scale unitit ja kuormitukset.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Scale Unit -hallintaportaali, Määritä scale unitit -sivu":::

Jos haluat lisätä vähintään yhden tilauksessa olevan skaalausyksikön, valitse **Lisää skaalausyksiköitä**.

Lisää varastonhallinnan kuormitus yhteen scale unitiin valitsemalla **Määritetyt kuormitukset** -välilehdessä **Luo kuormitus** -painike. Kunkin kuormituksen osalta on määritettävä kuormituksen omistamien prosessien konteksti. Varastonhallinnan kuormituksissa konteksti on tietyn toimipaikan ja yrityksen tietty varasto.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Määritä kuormitukset -ikkuna":::

#### <a name="manage-workloads"></a><a name="manage-workloads"></a>Kuormitusten hallinta

Kun vähintään kuormitus on otettu käyttöön, alusta ja hallitse **Kuormitusten hallinta** -asetuksen avulla prosesseja, kuten seuraavassa taulukossa mainittuja prosesseja.

| Käsittele | Kuvaus |
|---|---|
| Scale unit -viestinnän keskeyttäminen | Keskuksen ja scale unitin välisten pipeline-sanomien keskeyttäminen. Tämä prosessi pysäyttää viestinnän ja tyhjentää keskuksen ja scale unitien välisen tietoputken. Tämä prosessi on suoritettava ennen Supply Chain Management -huoltotoiminnon suorittamista joko keskuksessa tai scale unitissa, mutta sitä voi käyttää myös muissa tilanteissa. |
| Scale unit -viestinnän jatkaminen | Keskuksen ja scale unitin välisten pipeline-sanomien jatkaminen. Tätä prosessia voi käyttää esimeriksi sen jälkeen, kun Supply Chain Management -huoltotoiminto on suoritettu joko keskuksessa tai scale unitissa. |
| Päivityksen kuormitukset | Uuden toiminnon keskuksen ja scale unitin kuormitusten synkronointi. Tätä prosessia on ehkä käytettävä, kun huolto on aiheuttanut tiedonsiirtokyselyjen muuttumisen ja/tai lisännyt uusia taulukoita tai kenttiä kuormitukseen. |
| Kuormituksen siirtäminen scale unitiin | Keskuksessa tällä hetkellä suoritettavan kuormituksen scale unitiin siirtämisen aikatauluttaminen. Kun tämä prosessi suoritetaan, tietojen synkronointi tapahtuu sujuvasti. Lisäksi keskus ja scale unit määritetään vaihtamaan kuormituksen omistus. |
| Scale unitin siirtäminen keskukseen | Scale unitissa tällä hetkellä suoritettavan kuormituksen keskukseen siirtämisen aikatauluttaminen. Kun tämä prosessi suoritetaan, tietojen synkronointi tapahtuu sujuvasti. Lisäksi keskus ja scale unit määritetään vaihtamaan kuormituksen omistus.
| Siirtäminen hätätilanteessa keskukseen | <p>Aiemmin luodun kuormituksen siirtäminen välittömästi keskukseen. *Tämä prosessi vaihtaa vain keskuksessa tällä hetkellä käytettävissä olevien tietojen omistuksen.*</p><p><strong>Varoitus:</strong> Tämä prosessi voi aiheuttaa synkronoimattomien tietojen menetyksen ja liiketoimintaprosessien käsittelyn epäonnistumisen. Tämän vuoksi prosessia pitäisi käyttää vain hätätilanteissa, joissa liiketoimintaprosessit on käsiteltävä keskuksessa sen vuoksi, että scale unitissa on käyttökatkos, jota ei voi korjata kohtuullisessa ajassa.</p> |
| Jaetun topologian käytön lopettaminen | Scale unitin käyttöönoton poistaminen ja suorittaminen vain keskuksessa ilman kuormituksen käsittelyä. |

:::image type="content" source="media/sum-manage-workloads.png" alt-text="Scale unitin ja kuormituksen hallintakokemus.":::

> [!TIP]
> Ajan mittaan skaalausyksikköjen hallintakokemukseen lisätään lisäparannuksia, jotka helpottavat elinkaarenhallinnan toimintoja. Nykyisen julkaisun erityisominaisuudet on dokumentoitu mukana olevassa käyttökirjassa, joka on niiden asiakkaiden käytettävissä, jotka ovat mukana jaetussa hybriditopologiassa Supply Chain Managementia varten. <!-- KFM: Add a link to the handbook when it is published -->

## <a name="feature-management-considerations-for-workloads"></a>Toimintojen hallinnan osalta työkuormissa huomioon otettavat asiat

Tässä osassa selitetään tärkeitä näkökohtia, jotka kannattaa ottaa huomioon, kun asennetaan työkuormia, lisätään toimintoja tai poistetaan toimintoja jaetussa hybriditopologiassa. Monet tekijät voivat vaikuttaa siihen, onko sinun suoritettava [työkuorman päivitys](#manage-workloads) muutosten tekemisen jälkeen. Sinun on kuitenkin yleensä tehtävä niin, kun päivität tiedonsiirtokyselyjä tai lisäät sellaisia ja/tai kun lisäät uusia taulukkoja tai kenttiä aiemmin asennettuun työkuormaan.

### <a name="mandatory-features-for-installing-a-workload"></a>Työkuorman asennuksen pakolliset toiminnot

Kun asennat työkuorman, asennusprosessi luo työkuormamäärityksen, joka sisältää tietoja kahden käyttöönoton välillä tietoja synkronoitaessa käytetyistä tietotaulukosta. Työkuormamäärityksen määritelmän luonti suoritetaan automaattisesti kulloinkin [Toimintojen hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) käytössä olevien toimintojen perusteella. Seuraava taulukko sisältää toiminnot, joiden on oltava käytössä varasto- tai valmistustyökuorman suorittamiseen vaadittavien työkuormamääritelmien luomista varten.

| Pakollinen toiminto | Kuormitus |
|---|---|
| Automaattinen GUID-tunnusten määrittäminen WHS-käyttäjän luonnissa | Varasto |
| Organisaation laajuinen työn esto | Varasto |
| Lähetysaallon etikettien tiedot | Varasto |
| Varastosovelluksen työluetteloiden yksikkötuki | Varasto |
| Tuotannon suoritus | Valmistus |

Kun otat kuormituksen käyttöön [skaalausyksikön käyttöönottotyökaluilla yhden ruudun kehitysympäristöissä](https://github.com/microsoft/SCMScaleUnitDevTools) tai [Scale Unitien hallintaportaalilla](https://sum.dynamics.com), kaikki pakolliset toiminnot ovat automaattisesti käytössä. Jos kuitenkin suoritat manuaalisen testikäyttöönoton, josta puuttuu vähintään yksi pakollinen toiminto, työkuorman asennus epäonnistuu ja saat puuttuvat toiminnot sisältävän sanoman. Tällöin sinun on otettava kyseiset toiminnot käyttöön manuaalisesti ja käynnistettävä työkuorman asennus uudelleen.

### <a name="enabling-or-disabling-features-that-have-data-synchronization-dependencies"></a>Sellaisten toimintojen käyttöönotto tai käytöstä poisto, joilla on tiedonsynkronointiriippuvaisuuksia

Keskuksen ja sen Scale Unitien välillä synkronoitavien tietojen valitsemiseen vaikuttavat toiminnot vaikuttavat myös siihen, miten työkuorman määritelmä luodaan. Siksi on tärkeää ottaa nämä toiminnot käyttöön ennen työkuorman asentamista. Jos otat tällaisen toiminnon käyttöön suorittaessasi työkuormaa, sinun on luotava työkuorman määritelmä uudelleen suorittamalla [työkuorman päivitys](#manage-workloads) toiminnon käyttöön ottamisen jälkeen. Myös jos otat pois käytöstä toiminnon, jolla on tietojensynkronointiriippuvuuksia, kun suoritat työkuormaa, sinun on suoritettava [työkuorman päivitys](#manage-workloads) poistaaksesi asianosaiset tiedonsynkronointitiedot työkuorman määritelmästä.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
