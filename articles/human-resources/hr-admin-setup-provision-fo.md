---
title: Human Resourcesin valmistelu talous- ja toimintosovellusinfrastruktuurissa
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin uuden tuotantoympäristön valmistelua talous- ja toimintosovellusinfrastruktuurissa.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2fd8176d16178ecc4ba667e5937f2cec2e0af2c3
ms.sourcegitcommit: bd3b55e1af28e592c97b540de1e87cd8ba9c35a8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/03/2022
ms.locfileid: "9221589"
---
# <a name="provision-human-resources-in-the-finance-and-operations-infrastructure"></a>Human Resourcesin valmistelu talous- ja toimintosovellusinfrastruktuurissa

_**Kohde:** Human Resourcesin valmistelu talous- ja toimintosovellusinfrastruktuurissa_ 

> [!NOTE]
> Kesäkuusta 2022 alkaen uusia Human Resources -ympäristöjä ei voi valmistella erillisessä Human Resources -infrastruktuurissa, eikä siinä voi myöskään luoda uusia Microsoft Dynamics Lifecycle Services (LCS) -projekteja. Asiakkaat voiva ottaa Human Resources -ympäristöt voidaan käyttöön vain talous- ja toimintosovellusinfrastruktuurissa.

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin uuden tuotantoympäristön valmistelua talous- ja toimintosovellusinfrastruktuurissa.

## <a name="prerequisites"></a>Edellytykset

Ennen uuden ympäristön valmistelun aloittamista seuraavien edellytysten on toteuduttava:

- Human Resources on ostettu pilvipalveluratkaisujen toimittajalta (CSP) tai yritysarkkitehtuurisopimuksen (EA) avulla. Jos käytössä on Dynamics 365 -käyttöoikeus, joka sisältää Human Resourcesin palvelusopimuksen, eikä tämän artikkelin vaiheiden suorittaminen onnistu, ota yhteys tukeen.
- Yleinen järjestelmänvalvoja on kirjautunut [Microsoft Dynamics Lifecycle Servicesiin (LCS)](https://lcs.dynamics.com) ja luonut uuden talous- ja toimintosovellusprojektin.

## <a name="provision-a-human-resources-trial-environment"></a>Henkilöstöhallinnon koeympäristön valmistelu

> [!NOTE]
> Human Resourcesin kokeiluympäristöt eivät ole käytettävissä itsenäisissä sovelluksissa huhtikuusta 2022 alkaen. Mahdolliset asiakkaat, jotka haluavat arvioida Human Resourcesin ominaisuuksia talous- ja toimintosovellusten avulla, voivat käyttää ilmaista 30 päivän kokeiluversiota yhdessä esittelytietojen kanssa Dynamics 365 Finance sisältää Human Resources -ominaisuudet, jotka tuodaan Finance-infrastruktuuriin yhdistämällä itsenäinen sovellus. Lisätietoja on kohdassa [HR-tuotteiden yhdistäminen tuo ominaisuudet samaan paikkaan asiakkaalle](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers). Lisätietoja Dynamics 365 Finance -kokeiluversioista on [vaiheittaisessa oppaassa](../fin-ops-core/fin-ops/get-started/before-you-buy.md).

## <a name="plan-human-resources-environments"></a>Human Resources -ympäristöjen suunnitteleminen

Ennen ensimmäisen Human Resources -ympäristön luontia sinun tulee suunnitella huolellisesti projektin ympäristötarpeet. Human Resourcesin perustilaus sisältää kaksi ympäristöä: tuotantoympäristön ja oletusarvoisen vakiomuotoisen hyväksyntätestiympäristön (eristysympäristön). Projektin monimutkaisuuden mukaan on mahdollistaa ostaa lisäympäristöjä tukemaan projektitoimintoja.

Valinnaisia lisäympäristöjä koskevia huomioita:

- **Tietojen siirto** – Tietojen siirtämisen avulla eristysympäristöä voidaan käyttää testaustarkoituksiin koko projektin ajan. Lisäympäristössä tietojen siirtotoiminnot voivat jatkua samalla, kun testaus- ja määritystoimintoja tapahtuu toisessa ympäristössä.
- **Integrointi** – integrointien määrittämien ja testaaminen voi tarkoittaa esimerkiksi alkuperäisiä integrointeja tai mukautettuja integrointeja, kuten palkanlaskenta-, hakijan seuranta- tai etuusjärjestelmiä ja -palveluja.
- **Koulutus** – koulutusta varten tarvitaan ehkä erillinen ympäristö, johon määritettyjen koulutustietojen avulla työntekijöitä voidaan kouluttaa käyttämään uutta järjestelmää. 
- **Monivaiheinen projekti** – lisäympäristö voidaan tarvita tukemaan määrityksiä, tietojen siirtoa, testausta tai muita toimintoja sellaisessa projektin vaiheessa, joka suunnitellaan projektin ensimmäisen julkaisun jälkeen tapahtuvaksi.
- **Kehitys** – Talous- ja toimintosovellusinfrastruktuurissa voidaan nyt laajentaa ratkaisua ja kehittää omia mukautuksia. Kunkin kehittäjän on käytettävä omaa kehitysympäristöä. Lisätietoja on kohdassa [Kehitysympäristöjen käyttöönottaminen ja käyttäminen](../fin-ops-core/dev-itpro/dev-tools/access-instances.md).
- **GOLD** – Uusissa käyttöönotoissa on tavallista käyttää erillistä GOLD-ympäristöä, joka pidetään muuttumattomana määrityksiä ja tietojen siirtoa varten. Tätä ympäristöä voi käyttää koko toteuttamisen ajan muiden ympäristöjen päivittämiseen. Sen avulla luodaan uusi tuotantoympäristö, jossa on perustason määritykset ja tietojen siirto. Tuotantoympäristöä ei voi ottaa talous- ja toimintosovellusinfrastruktuuriin, ennen kuin julkaisuvalmiusprosessi on suoritettu. Lisätietoja on kohdassa [Julkistamisen valmistelu](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

<!--NOTE: Need to come back and verify Tier-1 can be used and if a customer cannot purchase tier 3-5 need specific documentation about this.-->

> [!IMPORTANT]
> Ympäristöjä harkittaessa kannattaa toimia seuraavasti:
>
> - Ennen julkistamista kannattaa tehdä käyttöönottoharjoitus oletusarvoisessa vakiohyväksyntätestiympäristössä (eristysympäristössä) tai muussa ympäristössä.
> - Yksityiskohtaista käyttöönoton tarkistusluettelon käyttäminen. Tämä luettelo sisältää kaikki tietopaketit, joita tarvitaan lopullisten tietojen siirtämiseen tuotantoympäristöön julkistamisprosessin aikana. Tämä on erityisen tärkeää, jos määritysten tallennusta varten ei ole erillistä GOLD-ympäristöä.
> - Oletusarvoisen vakiohyväksyntätestiympäristön (entinen eristysympäristö) tai muun taso-2- tai sitä korkeamman ympäristön käyttäminen TEST-ympäristönä koko projektin ajan. Jos lisäympäristöjä tarvitaan, organisaatio voi ostaa niitä lisämaksusta.

## <a name="create-an-lcs-project"></a>LCS-projektin luominen

Luo ensin LCS-projekti, jotta voit hallinnoida Human Resources -ympäristöjä LCS:n avulla. Jos Human Resources -ympäristö ollaan siirtämässä talous- ja toimintosovellusinfrastruktuuriin, talous- ja toimintosovelluksille on luotava uusi LCS-projekti. Jos muita talous- ja toimintosovelluksia varten on jo LCS-projekti, Human Resources -ominaisuudet voidaan ottaa käyttöön **Ominaisuuksien hallinta** -työtilassa. Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Kun uusi asiakas tilaa Human Resourcesin, tilaus sisältää käyttöönottoprojektin työtilan. Kun asiakas on aktivoinut palvelun, vuokraajan järjestelmänvalvojan on rekisteröidyttävä osoitteessa <https://lcs.dynamics.com> käyttämällä vuokraajatiliä. Organisaatiolle luodaan automaattisesti projektityötila. Lisätietoja on kohdassa [Talous- ja toimintosovellusten asiakkaiden Lifecycle Services (LCS)i](../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md).

> [!NOTE]
> Valmistelun onnistuminen voidaan varmistaa, kun Human Resources -ympäristön valmisteluun käytetty tili on määritetty joko **Järjestelmänvalvoja**- tai **Järjestelmän mukauttaja** -rooliin siinä Power Apps -ympäristössä, joka on liitetty Human Resources -ympäristöön. Lisätietoja käyttöoikeusroolien määrittämisestä käyttäjille Microsoft Power Platformissa on kohdassa [Käyttöoikeuksien määrittäminen resursseille](/power-platform/admin/database-security).

LCS-projektin käyttöönottoprosessin on oltava valmis, ennen kuin ympäristöjen käyttöönotto voidaan aloittaa. Lisätietoja on kohdassa [Projektin käyttöönotto](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md). Lisätietoja LCS:n käyttämisestä on [Lifecycle Servicesin (LCS) käyttöoppaassa](../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md).

## <a name="deploy-human-resources-environments"></a>Human Resources -ympäristöjen käyttöönottaminen

Talous- ja toimintosovellusten, mukaan lukien Human Resourcesin, käyttöönotto pilvipalvelussa edellyttää, että käyttöönotettavaa ympäristöä ja tilausta ymmärretään sekä tiedetään, kuka tekee mitäkin. Lisäksi tiedetään, mitä tietoja ja mukauttamisia tarvitaan. Uusia ympäristöjä käyttöönotettaessa suositellaan palvelutilin käyttöä nimetyn käyttäjän sijaan. Lisätietoja ympäristöjen käyttöönottamisesta talous- ja toimintosovellusinfrastruktuurissa on kohdassa [Pilvikäyttöönoton yleiskatsaus](/fin-ops-core/dev-itpro/deployment/cloud-deployment-overview).

Human Resourcesin tuotantoympäristön käyttöönotto talous- ja toimintosovellusinfrastruktuurissa edellyttää, että julkaisuvalmiusprosessi on suoritettu. Lisätietoja on kohdassa [Julkistamisen valmistelu](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md). Tämä prosessi sisältää tilauksen arviointityökalun LCS:ssä. Lisätietoja on kohdassa [Tilauksen arviointityökalu](../fin-ops-core/dev-itpro/lifecycle-services/subscription-estimator.md).

## <a name="integrate-microsoft-power-platform-with-human-resources"></a>Microsoft Power Platformin ja Human Resourcesin integrointi

Microsoft Power Platform tuottaa Dynamics 365 -sovellusten ominaisuuspaketin Power Platform -hallintakeskuksen kautta. Human Resources -tiedot voidaan integroida ja niiden käyttöä voidaan laajentaa Microsoft Power Platformin avulla. Lisätietoja Human Resourcesin ja Microsoft Power Platformin integroinnissa on kohdassa [Microsoft Power Platformin sekä talous- ja toimintosovellusten integrointi](../fin-ops-core/dev-itpro/power-platform/overview.md).

## <a name="supported-geographies"></a>Tuetut maantieteelliset alueet

Lisätietoja Human Resourcesin tuetuista kielistä ja maantieteellisistä alueista on kohdassa [Suunniteltu maailmanlaajuisen käyttöön: tietoja tuetuista maista ja kielistä](https://dynamics.microsoft.com/availability-reports/).

## <a name="grant-access-to-the-environment"></a>Ympäristön käyttöoikeuksien myöntäminen

Oletusarvoisesti vain ympäristön luonut yleinen järjestelmänvalvoja voi käyttää sitä. Käyttöoikeus on myönnettävä sovelluksen muille käyttäjille erikseen. Sinun on lisättävä käyttäjiä ja määritettävä heille sopivat roolit henkilöstöhallintoympäristössä. Lisätietoja on kohdassa [Uusien käyttäjien luonti](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ja [Käyttäjien liittäminen käyttöoikeusrooleihin](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).

## <a name="additional-resources"></a>Lisäresurssit
Lisätietoja LCS:n projektin käytöstä ja hallinnasta talous- ja toimintosovellusinfrastruktuurissa on seuraavissa resursseissa:

- [Lifecycle Services -resurssit](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md)
- [Lifecycle Services (LCS) -käyttöopas](../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Käyttöönotto itsepalveluna – yleiskatsaus](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md)
- [Tietokannan siirtotoimintojen aloitussivu](../fin-ops-core/dev-itpro/database/dbmovement-operations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
