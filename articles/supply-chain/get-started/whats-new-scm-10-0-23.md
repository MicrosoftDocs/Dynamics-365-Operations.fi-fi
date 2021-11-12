---
title: Dynamics 365 Supply Chain Management 10.0.23:n esikatselu
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin version 10.0.23 uusia tai muuttuneita ominaisuuksia.
author: kamaybac
ms.date: 10/15/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 3cf30c203d936f171796d9dd8d766cbbb8c997e0
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647809"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10023"></a>Dynamics 365 Supply Chain Management 10.0.23:n esikatselu

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin esiversion 10.0.23 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.1037. Se on käytettävissä seuraavasti:

- **Esiversio:** lokakuu 2021
- **Version yleinen saatavuus (oma päivitys):** joulukuu 2021

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Seuraavassa taulukossa on tämän julkaisun sisältämät toiminnot. *Ominaisuus*-sarakkeessa on linkki [julkaisusuunnitelmaan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), jossa voit tarkastella kuinkin ominaisuuden virallisia julkaisupäiviä. *Lisätietoja*-sarakkeessa on lisätietoja ja/tai linkkejä liittyvään dokumentaatioon. Ominaisuuden käyttöönottotapa selviää *Mahdollistaja*-sarakkeesta. Lisätietoja ominaisuuksienhallinen käytöstä: [Ominaisuuksienhallinnan yleiskuvaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Tämän aiheen päivitys saattaa sisältää ominaisuuksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.

| Ominaisuusalue | Ominaisuus | Lisätietoja | Käyttöönottaja:   |
|---|---|---|---|
| Yleinen osoitekirja | Oletusarvoisen osavaltion/provinssin määrittäminen kullekin maalle/alueelle osoitemäärityksessä | Voit nyt määrittää kullekin maalle/alueelle oletusarvoisen osavaltion/provinssin yleisen osoitekirjan osoitemäärityksessä. Kun oletusarvoinen osavaltio/provinssi on määritetty, siitä tulee oletusarvo, joka täytetään osavaltio/provinssi-kenttiin, kun kulloisellekin maalle/alueelle luodaan uusi maa- tai paikkakuntatietue. Katso myös [Osoitemääritys](../../fin-ops-core/fin-ops/organization-administration/global-address-book-address-setup.md?toc=/dynamics365/supply-chain/toc.json) | Oletusarvoisesti käytössä. |
| Varasto&nbsp;ja&nbsp;logistiikka | [Tehtävien keskeyttäminen Warehouse Management ‑mobiilisovelluksessa](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/park-tasks-warehouse-management-mobile-app) | [Mobiililaitteen valikkokohteiden vaiheiden kiertämisen määrittäminen](../warehousing/warehouse-app-detours.md) | Ominaisuuksienhallinta (*Warehouse Management -sovelluksen kiertotiet*) |
| Varasto&nbsp;ja&nbsp;logistiikka | [Varastosovelluksen ylemmälle tasolle siirretyt kentät](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Laitteen vaiheiden ylennettyjen kenttien määrittäminen](../warehousing/warehouse-app-promoted-fields.md)| Ominaisuuksienhallinta (*Varastosovelluksen korotetut kentät*) |
| Tuotannonhallinta | [Raportti tuotannon käyttöliittymän rinnakkais- ja sivutuotteista](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | [Tuotannon käyttöliittymän käytön ohjeet työntekijöille](../production-control/production-floor-execution-use.md) | Ominaisuuksienhallinta (*Raportti tuotannon käyttöliittymän rinnakkais- ja sivutuotteista*) |

## <a name="feature-enhancements-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnon parannukset

Seuraavassa taulukossa on tämän julkaisun uudet ominaisuuksien parannukset. Jokainen näistä parannuksista parantaa aiemmin luotua toimintoa lisäysten avulla. Koska ne ovat vain parannuksia, niitä ei ole lueteltu [vapautussuunnitelmassa](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Jos kuitenkin haluat varmistaa, että nämä parannukset eivät ole ristiriidassa aiemmin luotujen mukautuksiesi tai asetuksesi kanssa, kaikki muutokset ovat oletusarvon mukaan pois käytöstä (ellei toisin ilmoiteta).

Jos haluat ottaa näitä ominaisuuksista käyttöön tai poistaa niitä käytöstä, se on tehtävä [ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), jossa ne luetellaan niitä nimiä käyttäen, jotka näkyvät seuraavan taulukon *Ominaisuuden nimi ominaisuuksienhallinnassa* -sarakkeessa.

| Moduuli | Ominaisuuden nimi ominaisuuksienhallinnassa | Lisätietoja |
|---|---|---|
| Resurssien hallinta | Kulujen vastatilit työtilauksen kirjauskansioissa | Tämän ominaisuuden avulla voit määrittää vastatilin jokaiselle työtilauksen kirjauskansiossa luetellulle kululle. Yleensä kuhunkin kuluun yhdistetään toimittajatili, mutta myös muita tilityyppejä tuetaan. Se lisää kaksi uutta saraketta (**Vastatilin tyyppi** ja **Vastatili**) **Kulu**-pikavälilehteen **Työtilauksen kirjauskansio** -sivulla.|
| Varastonhallinta | \[Venäjä\] Kirjaa Stornon taloushallinnon varastotapahtumat myyntitilausten taloushallinnon tositteen korjausmerkinnän mukaan | Tämä ominaisuus vaikuttaa hyvityslaskujen korjaustoimintoon Venäjän osalta. Se mahdollistaa varastotapahtumien kirjaamisen myyntilaskuille kirjanpidon korjausvaihtoehdon mukaisesti. Kun tämä ominaisuus on käytössä, varastotapahtuman tositteen **Korjaus**-merkinnän ja varastotapahtumien **Storno**-merkinnän välillä ei ole enää eroja. |
| Varastonhallinta | (Venäjä) Suorita Varastosaldon kiertonopeus -raportin laskelmat erätoimintona | Venäjänkielisten Supply Chain Managementin lokalisointien osalta tämän ominaisuuden avulla *Varastosaldon vaihtuvuus* -raportti voidaan suorittaa erätoimintona ja tallentaa. Myös aiemmin luotujen raporttien tarkasteleminen on mahdollista. |
| Varastonhallinta | (Venäjä) Käytä tapahtumia paikallisella kielellä maa- tai aluekohtaisissa ensisijaisissa lomakkeissa varastonhallinnassa | Venäjänkielisten Supply Chain Managementin lokalisointien osalta tämä ominaisuus ottaa käyttöön tuotteiden/nimikkeiden nimien ja mittayksiköiden venäjänkieliset käännökset seuraavissa venäjänkielisissä varaston tulosteissa: Inventointiluettelo (INV-3),Inventointiluettelo (INV-5) ja Inventointiluettelo (INV-6). |
| Hankinta | Tyhjennä ostotilauksen päivityshistoria | Tämän ominaisuuden avulla voit puhdistaa ostotilausten päivityksiin liittyvät väliaikaiset historiatietueet. Se lisää uuden **Puhdista ostopäivityshistoria** -painikkeen **Kaikki ostotilaukset** -sivun toimintoruutuun. Tämä ominaisuus on oletusarvoisesti käytössä. |
| Tuotannonhallinta | (Esiversio) Varastomateriaalien automaattinen keräily automaattisesti kirjattuja keräysluetteloita varten | Tämän ominaisuuden avulla voidaan tehdä keräily automaattisesti ja ratkaista varastodimensiot automaattisesti kirjattuja, jaettuja ja jälkikustannuslaskennassa olleita keräysluettelon kirjauskansioita varten. |
| Tuotannonhallinta | Raaka-aineiden vanhenemisen tarkistaminen suunnitellun käyttöpäivän perusteella | Tämä ominaisuus muuttaa sitä, miten erien vanhanemispäivät tarkistetaan, kun raaka-aine-erä varataan käytettäväksi tuotannossa. Kun tämä ominaisuus on käytössä, erän vanhenemispäivä tarkistetaan tuotannon tuoterakennerivillä tai erätilauksen kaavarivillä esitetyn suunnitellun käyttöpäivämäärän (eli raaka-ainepäivämäärään) perusteella. Kun tämä ominaisuus ei ole käytössä, erän vanhentumispäivä tarkistetaan tuotannon tai erätilauksen suunnitellun toimituspäivän perusteella (kuten aiemmin). |
| Myynti ja markkinointi | Tyhjennä myyntitilauksen päivityshistoria | Tämän ominaisuuden avulla voit puhdistaa myyntitilausten päivityksiin liittyvät väliaikaiset historiatietueet. Se lisää uuden **Puhdista myyntipäivityshistoria** -painikkeen myyntitilausten tieto- ja luettelosivujen toimintoruutuun. |
| Myynti ja markkinointi | Paranna 100 parasta -asiakasraportin suorituskykyä | Tämä ominaisuus parantaa **100 parasta** -asiakasraportin suorituskykyä siten, että se suoritetaan aina kaikille asiakkaille (niin kuin se on tarkoitettukin) mukautettujen kyselyjen sallimisen sijaan. Kun tämä ominaisuus on käytössä, kaikki **Sisällytettävät tietueet** -asetukset poistetaan käytöstä **100 parasta** -raporttivalintaikkunassa. |
| Varastonhallinta   | Lähtevien tilausten varastoon vapauttamisen asteikon yksikön tuki | Kun tämä ominaisuus on otettu käyttöön, lähtevät tilaukset voidaan vapauttaa suoraan keskuksesta scale unitiin, josta tilaukset täytetään. |

## <a name="new-and-updated-documentation-resources"></a>Uudet ja päivitetyt asiakirjaresurssit

Seuraavat ohjeaiheet on lisätty äskettäin tai niitä on päivitetty merkittävästi. Nämä ohjeaiheet eivät välttämättä liity tällä julkaisulla lisättyihin, edellisessä osassa lueteltuihin uusiin ominaisuuksiin. Niiden avulla saatat kuitenkin saada enemmän irti olemassa olevista ominaisuuksista.

| Ominaisuusalue | Uudet tai päivitetyt ohjeaiheet |
|---|---|
| Suunnittelun muutosten hallinta | [Suunnittelumääritteet ja suunnittelumääritteiden haku](../engineering-change-management/engineering-attributes-and-search.md) kuvaa nyt, miten suunnittelumääritteiden periminen toimii. |
| Pääsuunnittelu | [Pääsuunnittelu ja kysynnän ennusteet](../master-planning/planning-optimization/demand-forecast.md) ja [Ennusteen vähennysavaimet](../master-planning/reduction-keys.md) antavat nyt enemmän tietoja siitä, miten vähennysavaimia käytetään. |
| Pääsuunnittelu | [Nimikkeiden varmuusvaraston täyttäminen](../master-planning/safety-stock-replenishment.md) antaa nyt enemmän tietoja vähimmäis-/enimmäisavainten käytöstä. |
| Pääsuunnittelu | [Varastoennusteet](../master-planning/inventory-forecast.md) antaa nyt enemmän tietoja ennusteiden kohdistamisesta. |
| Pääsuunnittelu | [Toimitusaikataulu](../master-planning/supply-schedule.md) |
| Varastonhallinta   | [Yleiset mobiililaitteen parametrit](../warehousing/mobile-device-parameters.md) |
| Varastonhallinta   | [Ankkurointi](../warehousing/anchoring.md) |
| Myynti ja markkinointi | Konsernin sisäinen kaupankäynti on nyt kuvattu yksityiskohtaisesti alkaen aiheesta [Konsernin sisäisen kaupankäynnin määrittäminen](../sales-marketing/intercompany-trade-set-up.md) ja siihen liittyvistä aiheista. |
| Inventoinnin- ja varastonhallinta | Varaston näkyvyyden ohjeet on laajennettu ja päivitetty alkaen aiheesta [Varaston näkyvyyden apuohjelman yleiskatsaus](../inventory/inventory-visibility.md) ja siihen liittyvistä aiheista. |

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Ympäristön päivitykset Finance and Operations -sovelluksille

Microsoft Dynamics 365 Supply Chain Management 10.0.23 sisältää Platform updateja. Lisätietoja on kohdassa [Finance and Operations -sovellusten (marraskuu 2021) käyttöympäristön päivitysversio 10.0.23](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-23.md).

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.23 virheenkorjauksista päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=627874&dbType=3&qc=9b7e01944eb8b43f9c3aac4be26811c27be205847d6d2a240424f34f7e722910).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365:n ja toimialan pilvipalvelu: 2021 julkaisuaalto 2 -suunnitelma

Haluatko tietoja tulevien ja juuri julkaistujen yrityssovellustemme tai -ympäristöjemme ominaisuuksista?

Katso [Dynamics 365:n ja toimialan pilvipalvelu: 2021 julkaisuaalto 2 -suunnitelma](/dynamics365-release-plan/2021wave2/). Olemme koonneet kaikki tarvittavat tiedot yhteen asiakirjaan, jota voit käyttää suunnittelun apuna.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Poistetut ja vanhentuneet Supply Chain Management -toiminnot

[Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa kerrotaan toiminnoista, jotka on ajoitettu poistettaviksi tai vanhentuviksi tai jotka on poistettu Supply Chain Managementissa.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Ennen kuin toiminto poistetaan tuotteesta, siitä annetaan vanhentunisilmoitus [Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa 12 kuukautta ennen poistoa.

Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä toiminnalliset päivitykset on tehtävä kääntäjään.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
