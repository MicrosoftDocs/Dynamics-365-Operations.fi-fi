---
title: Esiversio – Dynamics 365 Supply Chain Management 10.0.28 (elokuu 2022)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin version 10.0.28 uusia tai muuttuneita ominaisuuksia.
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 306ff9be80c7a7a947b9132e3c9b4b9ec799b265
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813070"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10028-august-2022"></a>Esiversio – Dynamics 365 Supply Chain Management 10.0.28 (elokuu 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin esikatseluversion 10.0.28 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.1264. Se on käytettävissä seuraavan aikataulun mukaisesti:

- **Julkaisun esiversio:** Toukokuu 2022
- **Julkaisun yleinen saatavuus (itsepäivitys):** heinäkuu 2022
- **Julkaisun yleinen saatavuus (automaattinen päivitys):** heinäkuu 2022

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Seuraavassa taulukossa on tämän julkaisun sisältämät toiminnot. Tämän aiheen päivitys saattaa sisältää ominaisuuksia, jotka on lisätty koontiversioon tämän ohjeaiheen alkuperäisen julkaisun jälkeen.

| Ominaisuusalue | Ominaisuus | Lisätietoja | Käyttöönottaja:   |
|---|---|---|---|
| Varasto ja logistiikka | [Aiheutuneen kustannuksen integrointiyksiköt kolmannen osapuolen huolitsijoita varten](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [Aiheutuneet kustannukset -entiteettien yleiskuvaus](../landed-cost/landed-cost-entities-overview.md) | Oletusarvoisesti käytössä |
| Suunnittelu | [Säilyvyysajan tuki suunnittelun optimoinnissa](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | Tulossa pian <!-- KFM: Vendor is preparing this. Expected May 20. --> | Oletusarvoisesti käytössä |

<!-- KFM: Confirm status of this feature:
| Planning | [Demand Driven Material Requirements Planning (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | Coming soon | Feature management:<br>*(Preview) DDMRP for Planning Optimization* | -->

## <a name="feature-enhancements-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnon parannukset

Seuraavassa taulukossa on tämän julkaisun sisältämät ominaisuuksien parannukset. Jokainen näistä parannuksista parantaa aiemmin luotua toimintoa lisäysten avulla. Koska ne ovat vain parannuksia, niitä ei ole lueteltu [vapautussuunnitelmassa](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Jos kuitenkin haluat varmistaa, että nämä parannukset eivät ole ristiriidassa aiemmin luotujen mukautuksiesi tai asetuksesi kanssa, kaikki muutokset ovat oletusarvon mukaan pois käytöstä (ellei toisin ilmoiteta).

Jos haluat ottaa jonkin näistä ominaisuuksista käyttöön tai poistaa ne käytöstä, sinun on tehtävä se [ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moduuli | Ominaisuuden nimi ominaisuuksienhallinnassa | Lisätietoja |
|---|---|---|
| Varastonhallinta | Ota konsernin sisäiselle käytettävissä olevalle varastolle käyttöön vain nollasta poikkeavan varastomäärän näyttäminen | Tämän ominaisuuden avulla voit valita, sisällytetäänkö nimikkeet, joiden käytettävissä oleva määrä on nolla, konsernin sisäiseen varastoluetteloon. Voit ohjata tätä vaihtoehtoa käyttämällä **Älä näytä konsernin sisäisessä varastoluettelossa nimikkeitä, joiden käytettävissä oleva varastosaldo on nolla** -asetusta, jonka tämä ominaisuus lisää **Varasto ja varastonhallinnan parametrit** -sivulle. |
| Varastonhallinta | (Intia) Ohita siirron hintasäännöt sijainnille, kun Varastokoodista-asetuksen arvoksi on määritetty Kaikki | <p>Tämä toiminto koskee vain Intiaa. Tämä ominaisuus tekee siirtohintojen määrittämisestä varastosiirtoja varten intuitiivisempaa.</p><p>Määrität siirtohinnat määrittämällä kullekin nimikkeelle siirtohinnoittelusäännöt. Yksi tapa tehdä tämä konfigurointi on sisällyttää sääntörivi, jossa **Varastokoodista** -kenttä on määritetty arvoon *Kaikki*. Tämä asetus ilmaisee, että rivin määrittämää siirtohintaa tulee käyttää riippumatta siitä, mistä varastosta nimike kerätään. Kun tämä ominaisuus on käytössä, siirtohintasäännöt, joissa **Varastokoodista** -kenttä on määritetty arvoon *Kaikki*, ohittavat **Sijainti**-asetuksen. Näin ollen sääntö on voimassa riippumatta siirtotilauksessa määritetystä sijainnista. Tämä toiminta on odotettavissa, koska sijainti on varaston alapuolella varastodimensiohierarkiassa.</p><p>Jos tätä toimintoa ei ole, järjestelmä käyttää tämäntyyppisiä sääntöjä vain, kun siirtotilauksen sijainti vastaa täsmälleen säännölle määritettyä sijaintia. (Jos sääntöä varten on määritetty tyhjä sijainti, järjestelmä käyttää sääntöä vain siirtotilauksiin, joissa on myös tyhjä arvo sijainnille.)</p> |
| Varastonhallinta | Käytettävissä olevan varaston raportin tietojen siivous | Tämä ominaisuus tarjoaa tavan siivota tiedot, joita on käytetty *Käytettävissä olevan varaston raporttitallennus* -raporttien luomiseen. |
| Tuotannonhallinta | Määritä projektitoiminnot huoltosopimukselle ja huoltotilausriveille | Tämä ominaisuus lisää **Projektitehtävä**-kentän huoltosopimukselle ja huoltotilausriveille, jotta niille voi määrittää projektitehtävän. Tämä ominaisuus auttaa estämään estovirheet, kun kirjaat palvelunhallinnan kirjauskansioita, jotka vaativat projektitehtävän määrittämistä.  |
| Varastonhallinta   | Manuaalinen siirtorivin keräyspalvelu järjestelmänvalvojalle tai vastaaville luotettaville käyttäjille | Tämän ominaisuuden avulla järjestelmänvalvojat voivat poimia siirtoriveihin liittyvät varastotapahtumat manuaalisesti. Nämä rivit sisältävät rivit, jotka on jo vapautettu varastoon. Järjestelmänvalvojien on tehtävä tämä keräily vain poikkeustapauksissa, esimerkiksi silloin, kun järjestelmä on vioittunut. |

## <a name="new-and-updated-documentation-resources"></a>Uudet ja päivitetyt asiakirjaresurssit

Seuraavat ohjeaiheet on lisätty äskettäin tai niitä on päivitetty merkittävästi. Nämä ohjeaiheet eivät välttämättä liity tällä julkaisulla lisättyihin, edellisissä osissa lueteltuihin uusiin ominaisuuksiin. Niiden avulla saatat kuitenkin saada enemmän irti olemassa olevista ominaisuuksista.

| Ominaisuusalue | Uudet tai päivitetyt ohjeaiheet |
|---|---|
| Kustannushintojen hallinta | [Kiinteä vastaanottohinta](../cost-management/fixed-receipt-price.md) |
| Kustannushintojen hallinta | [Varaston kustannuslaskennan usein kysytyt kysymykset](../cost-management/inventory-costing-faq.md) |
| Kustannushintojen hallinta | [Kirjaa kirjanpidon periaatteen veloitustilille](../cost-management/post-to-charge-account-accounting-principle.md) |
| Inventoinnin- ja varastonhallinta | [Varastotapahtumatiedot](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Taloushallinnon ja toimintojen sovellusten ympäristöpäivitykset

Microsoft Dynamics 365 Supply Chain Management 10.0.28 sisältää Platform updateja. Lisätietoja on kohdassa [taloushallinnon ja toimintojen sovellusten (kesäkuu 2022) käyttöympäristön päivitysversio 10.0.28.](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md).<!-- KFM Confirm link -->

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.28 virheenkorjauksista päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 1 -suunnitelma

Haluatko tietoja tulevien ja juuri julkaistujen yrityssovellustemme tai -ympäristöjemme ominaisuuksista?

Katso [Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 1 -suunnitelma](/dynamics365-release-plan/2022wave1/). Olemme koonneet kaikki tarvittavat tiedot yhteen asiakirjaan, jota voit käyttää suunnittelun apuna.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Poistetut ja vanhentuneet Supply Chain Management -toiminnot

[Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa kerrotaan toiminnoista, jotka on ajoitettu poistettaviksi tai vanhentuviksi tai jotka on poistettu Supply Chain Managementissa.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Ennen kuin toiminto poistetaan tuotteesta, siitä annetaan vanhentunisilmoitus [Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa 12 kuukautta ennen poistoa.

Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä toiminnalliset päivitykset on tehtävä kääntäjään.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
