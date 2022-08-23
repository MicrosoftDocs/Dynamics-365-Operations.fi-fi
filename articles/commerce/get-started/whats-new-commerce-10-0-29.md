---
title: Dynamics 365 Commerce 10.0.29:n esiversio (lokakuu 2022)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Commercein 10.0.29 uusia tai muuttuneita toimintoja.
author: josaw1
ms.date: 08/02/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: c1f85fcd8f79106a3af93489d3bef608b9840bf3
ms.sourcegitcommit: 91f58a9863f4e8f30ac787c2a9771c1ff6a05f72
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/03/2022
ms.locfileid: "9224235"
---
# <a name="preview-of-dynamics-365-commerce-10029-october-2022"></a>Dynamics 365 Commerce 10.0.29:n esiversio (lokakuu 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Commerce -esiversion 10.0.29 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.1326. Se on käytettävissä seuraavan aikataulun mukaisesti:

- **Julkaisun esiversio:** Elokuu 2022
- **Version yleinen saatavuus (oma päivitys):** syyskuu 2022
- **Version yleinen saatavuus (automaattinen päivitys):** lokakuu 2022

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Seuraavassa taulukossa on tämän julkaisun sisältämät toiminnot. Tämän artikkelin päivitys saattaa sisältää ominaisuuksia, jotka on lisätty koontiversioon tämän artikkelin alkuperäisen julkaisun jälkeen.

| Ominaisuusalue | Ominaisuus | Lisätietoja | Käyttöönottaja:   |
|---------|------------------|----------------|--------------| 
| Yritystenvälinen | [Myyntisopimusten tuen ottaminen käyttöön kanavien välille](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-b2b-sales-agreement-contract-based-pricing) | Tämän ominaisuuden avulla B2B-myyntiorganisaatiot voivat käyttää Commerce headquarters -sovelluksessa myyntisopimuksia määrittääkseen ostajilleen sopimuspohjaisen hinnoittelun. Kun B2B-ostaja tekee ostoksia verkkokaupassa, hänen organisaatiolleen määritettyä sopimuspohjaista hinnoittelua sovelletaan automaattisesti koko kokemukseen, aina tuotteiden löytämisestä ostamiseen ja maksamiseen. | Toimintojen hallinta<p>*Myyntisopimuksen tuki kaupankäyntikanavien välillä* |
| Customer Service | [Asiakaspalvelun ottaminen käyttöön Dynamics 365 Omnichannel for Customer Service -ratkaisulla](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/chat-dynamics-365-commerce-omnichannel-customer-service) | Ensiluokkainen asiakastukikokemus on välttämätöntä henkilökohtaisen ja miellyttävän kaupankäyntikokemuksen tarjoamiseksi kuluttajille. Kaupankäynnille on nykyään useita kosketuspisteitä, kuten fyysiset myymälät, online-kanavat ja sosiaaliset kanavat. Asiakkaat odottavat henkilökohtaista tukikokemusta kaikissa näissä kosketuspisteissä. Tämä ominaisuus auttaa sinua vauhdittamaan asiakkaiden ostopäätöksiä, lisäämään henkilökohtaista yhteydenpitoa asiakkaiden kanssa ja parantamaan asiakaspalvelua Dynamics 365 Omnichannel for Customer Service -ratkaisun integroinnilla. | Järjestelmänvalvoja/päättäjät ottavat käyttöön |
| Sähköinen kaupankäynti | Verkkokaupan tuotevertailun tuki | Salli ostajien vertailla tuotteita eri luokkien välillä, jotta he voivat tehdä oikean ostopäätöksen itse. Tämä ominaisuus on käytettävissä sekä B2C- että B2B-sivustoilla. | Sivuston luontiohjelma | 
| Lahjakortit | Vähittäismyynnin lahjakorttitaulujen tuki tietojen jakamiseksi yritysten välillä | Dynamics headquarters tukee tietojen jakamisen sallimista yritysten välillä tiettyjen taulujen osalta Dynamics-arkkitehtuurissa. Tässä ominaisuudessa Dynamics 365 Commerce sallii tietojen jakamisen yritysten välillä myös vähittäismyynnin lahjakorttitaulujen osalta. Näin ollen yhdessä yrityksessä olevan lahjakortin tiedot voidaan nyt kopioida toiseen samassa ympäristössä olevaan yritykseen. Alkuperäisen yrityksen lahjakorttitauluun tehdyt muutokset välitetään toisen yrityksen kopioituun lahjakorttitauluun. | Kehittäjät |
| Suorituskyky | RTS-riippuvuuden poistaminen "Muokkaa asiakasta" -skenaarioissa | Hyvä saatavuus ja korkea suorituskyky ovat normaaleja odotuksia myyntipisteiden (POS) ja sähköisen kaupankäynnin kanavissa. Näiden odotusten täyttämiseksi Dynamics 365 Commerce -kanavien ei tarvitse enää olla riippuvaisia reaaliaikaisesta kommunikoinnista Commerce headquarters -sovelluksen kanssa, kun asiakastietoja muokataan. Kyky muokata asynkronisten ja ei-asynkronisten asiakkaiden asiakastietoja asynkronisesti voi auttaa vähentämään reaaliaikaisia kutsuja Commerce headquarters -sovellukseen. | Järjestelmänvalvoja/päättäjät ottavat käyttöön |

## <a name="feature-state-changes-in-this-release"></a>Tämän julkaisun toiminnon tilan muutokset

Seuraavassa taulukossa luetellaan ominaisuudet, jotka tulivat pakollisiksi tai oletusarvoisesti käyttöön versiossa 10.0.29. Kaikki nämä ominaisuudet otetaan automaattisesti käyttöön järjestelmässäsi heti, kun päivität versioon 10.0.29. Pakollisia ominaisuuksia ei voi poistaa käytöstä, mutta oletusarvoisesti käytössä olevia ominaisuuksia voi poistaa käytöstä [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilasta.

Taulukko sisältää myös ominaisuudet, jotka olivat aiemmin julkisen esiversion vaiheessa, mutta jotka ovat yleisesti saatavilla versiossa 10.0.29. Tämä muutos tarkoittaa sitä, että niitä suositellaan käytettäviksi tuotantoympäristöissä. Nämä ominaisuudet eivät ole oletusarvoisesti käytössä, ellei toisin ole mainittu. Jos haluat siis käyttää niitä, sinun täytyy ottaa ne käyttöön [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilasta.

| Ominaisuus | Nimi | Uuden ominaisuuden tila |
| --- | --- | --- |
| BrazilRetailLocalizationFeature_BR |(Brasilia) (Brasilia) Brasiliaan liittyvä Commerce-toiminto | Käytössä oletusarvoisesti |
| RetailAdvancedGTETaxAdjustmentFeature | (Intia) Käytä Retail POS:ssä vähittäismyyntitapahtumille laskettua GST-veroa vähittäismyynlaskemissa | Käytössä oletusarvoisesti |
| RetailChronologicalInvoicePostingFeature_IT | (Italia) Ota käyttöön vähittäismyyntilaskut, jotka on kirjattu ilman aikajärjestystä | Käytössä oletusarvoisesti |
| RetailDiscountWithoutTaxAdjustingFeature_MX | (Meksiko) Alennus, joka oikaisee vähittäismyynnin yleisen CFDI:n | Käytössä oletusarvoisesti |
| RetailFiscalIntegrationConfigurationEnhancementFeature | Tilikauden integroinnin teknisen profiilin ohitukset | Käytössä oletusarvoisesti |
| RetailFiscalIntegrationConnectorLocationFeature | Suora tilikauden integrointi myyntipisteen kassakoneista | Käytössä oletusarvoisesti |
| RetailFiscalIntegrationLocalStorageBackupEnableFeature | Verointegraation tietovaraston paikallinen varmuuskopio | Käytössä oletusarvoisesti |
| RetailFiscalIntegrationPostponeFiscalRegistrationFeature | Asiakirjojen rekisteröintiä on lykätty | Käytössä oletusarvoisesti |
| RetailFiscalIntegrationRegistrationProcessTerminalExceptionFeature | Myyntipisteen kassakoneiden tilikausirekisteröinnin tila | Käytössä oletusarvoisesti |
| RetailGSTInvoiceAddressTaxCalculationFeature_IN | (Intia) Laske GST-vero sähköisen kaupankäynnin tilausten laskutusosoitteen perusteella | Käytössä oletusarvoisesti |
| RetailInvoicesDefaultSalesDocumentStatusFeature_PL | (Puola) Myyntiasiakirjan oletustila vähittäismyynnin laskuille | Käytössä oletusarvoisesti |
| RetailRecalculateRoundingOfTaxBaseAmountsFeature_MX | (Meksiko) Retailin globaalin CFDI:n veroperusteen summien uudelleenlaskenta. | Käytössä oletusarvoisesti |
| RetailSupplementaryInvoiceFeature | Ota käyttöön vähittäismyymälöissä suoritettujen itsepalvelutukkutapahtumien täydentävät laskut | Käytössä oletusarvoisesti |
| RetailInventoryBufferAndInventoryLevelEnableFeature   |  Ota käyttöön varastopuskurit ja varastotasot    |  Käytössä oletusarvoisesti|
|RetailInboundOutboundInventoryValidationFeature|   Ota vahvistus käyttöön myyntipisteen saapuvissa ja lähtevissä varastotoiminnoissa   |   Käytössä oletusarvoisesti   |
|  RetailInventoryChannelCalculationConsolidationFeature    |  Parannettu sähköisen kaupankäynnin kanavapuolen varaston laskentalogiikka |   Käytössä oletusarvoisesti   |
|RetailInventoryAdjustmentsInPointOfSaleFeature|    Varaston oikaisut myyntipisteessä   |  Käytössä oletusarvoisesti  |
| RetailMultiplePickupDeliveryModeFeature |  Useiden noutotapojen tuki     |   Pakollinen    |
|  RetailProductAvailabilityOptimizationFeature |   Optimoitu tuotteen käytettävyyslaskenta  |  Pakollinen |
|   RetailPricingDataManagerV2Feature   |   Paranna Commercen hinnoittelumoduulin suorituskykyä |   Pakollinen |
|  RetailPricingPreventUnintendedRecalculationFeature   | Estä kaupankäynnin tilausten tahaton hintalaskelma    |  Pakollinen  |
| RetailTeamsIntegration    |   Ota Microsoft Teams-integraatio käyttöön| Pakollinen   |  
| ConsumerEFDSyncProcessFeature_BR | (Brasilia) NFC-e:n synkroninen käsittely | Käytössä oletusarvoisesti |
| RetailFiscalIntegrationInternalAndExternalServicesEnableFeature | Sisäisten ja ulkoisten yhdistimien tukeminen verotuksen integrointikehyksessä | Pakollinen |
| RetailTaxRegistrationIdEnableFeature_BR | (Brasilia) Etsi asiakkaita Retail POS-palvelussa verorekisteröintinumeroiden perusteella | Pakollinen |
| RetailTaxRegistrationIdEnableFeature_IN | (Intia) Etsi asiakkaita Retail POS-palvelussa verorekisteröintinumeroiden perusteella | Pakollinen |
| RetailTaxRegistrationIdEnableFeature_IT | (Italia) Asiakastietojen hallinta Retail POS -palvelussa | Pakollinen |
| RetailTaxRegistrationIdEnableFeature_PL | (Puola) Asiakastietojen hallinta Retail POS -myyntipisteessä | Pakollinen |
| RetailUpdateReturnOriginalTransactionIdGlobalEnableFeature_IN | (Intian vähittäismyynnin GST-vero) Päivitä hyvityslaskut viittauksilla alkuperäisiin laskuihin | Pakollinen |
| RetailUserDefinedCertificateProfileFeature | Käyttäjän määrittämät vähittäismyymälöiden varmenneprofiilit | Pakollinen |
  

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Taloushallinnon ja toimintojen sovellusten ympäristöpäivitykset

Microsoft Dynamics 365 Commerce 10.0.29 sisältää alustan päivitykset. Lisätietoja on kohdassa [taloushallinnon ja toimintojen sovellusten (lokakuu 2022) käyttöympäristön päivitysversio 10.0.29.](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md). 

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.29 virheenkorjauksista eri päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja lukemalla [Knowledge Base -artikkelin](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559&dbType=3&qc=ec3e3846199f5d3a27a0c4949e3902ffdbc87560f0cf928c4838b3bdd421633c). 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 2 -suunnitelma

Haluatko tietoja tulevien ja juuri julkaistujen yrityssovellustemme tai -ympäristöjemme ominaisuuksista?

Katso [Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 2 -suunnitelma](/dynamics365-release-plan/2022wave2/). Olemme koonneet kaikki tarvittavat tiedot yhteen asiakirjaan, jota voit käyttää suunnittelun apuna.

### <a name="removed-and-deprecated-features"></a>Poistetut ja vanhentuneet ominaisuudet

Poistetut ja vanhentuneet Commerce-ominaisuudet on kuvattu artikkelissa [Poistetut tai vanhentuneet Dynamics 365 Commerce -ominaisuudet](removed-deprecated-features-commerce.md).

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Ennen kuin toiminto poistetaan tuotteesta, siitä annetaan vanhentumisilmoitus [Dynamics 365 Commercein poistetut tai vanhentuneet toiminnot](removed-deprecated-features-commerce.md) -artikkelissa 12 kuukautta ennen poistoa.

Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä toiminnalliset päivitykset on tehtävä kääntäjään.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
