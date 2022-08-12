---
title: Dynamics 365 Supply Chain Management 10.0.27:n uudet ja muuttuneet ominaisuudet (Heinäkuu 2022)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Supply Chain Managementin 10.0.27 uusia tai muuttuneita toimintoja.
author: kamaybac
ms.date: 04/22/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: ff92e6904b8042232159a0aea095d7a91c17d4b7
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124097"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10027-july-2022"></a>Dynamics 365 Supply Chain Management 10.0.27:n uudet ja muuttuneet ominaisuudet (Heinäkuu 2022)

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Supply Chain Managementin version 10.0.27 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.1227. Se on käytettävissä seuraavan aikataulun mukaisesti:

- **Julkaisun esiversio:** huhtikuu 2022
- **Julkaisun yleinen saatavuus (itsepäivitys):** kesäkuu 2022
- **Julkaisun yleinen saatavuus (automaattinen päivitys):** heinäkuu 2022

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Seuraavassa taulukossa on tämän julkaisun sisältämät toiminnot. Tämän artikkelin päivitys saattaa sisältää ominaisuuksia, jotka on lisätty koontiversioon tämän artikkelin alkuperäisen julkaisun jälkeen.

| Ominaisuusalue | Ominaisuus | Lisätietoja | Käyttöönottaja:   |
|---|---|---|---|
| Varasto ja logistiikka | [Varaston näkyvyyden lisäosan varaston varaus](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-allocation-inventory-visibility-add-in) | [Varaston näkyvyyden varaston kohdistus](../inventory/inventory-visibility-allocation.md) | Oletusarvoisesti käytössä |
| Valmistus | Tuotannon käyttöliittymän Päivän tehtävät -näkymä | [Miten työntekijät käyttävät tuotannon käyttöliittymää](../production-control/production-floor-execution-use.md) ja [Lomasaldojen näyttäminen tuotannon käyttöliittymässä](../production-control/production-floor-execution-payroll-stats.md) | Toimintojen hallinta:<br>*Tuotannon käyttöliittymän Päivän tehtävät -näkymä* |
| Suunnittelu | [Alihankinnan tuki suunnittelun optimoinnissa](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-subcontracting) | [Tuotannon alihankintatyön hallinta](../production-control/manage-subcontract-work-production.md) | Oletusarvoisesti käytössä |

## <a name="feature-enhancements-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnon parannukset

Seuraavassa taulukossa on tämän julkaisun sisältämät ominaisuuksien parannukset. Jokainen näistä parannuksista parantaa aiemmin luotua toimintoa lisäysten avulla. Koska ne ovat vain parannuksia, niitä ei ole lueteltu [vapautussuunnitelmassa](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Jos kuitenkin haluat varmistaa, että nämä parannukset eivät ole ristiriidassa aiemmin luotujen mukautuksiesi tai asetuksesi kanssa, kaikki muutokset ovat oletusarvon mukaan pois käytöstä (ellei toisin ilmoiteta).

Jos haluat ottaa jonkin näistä ominaisuuksista käyttöön tai poistaa ne käytöstä, sinun on tehtävä se [ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moduuli | Ominaisuuden nimi ominaisuuksienhallinnassa | Lisätietoja |
|---|---|---|
| Pääsuunnittelu | Ota varaston läpimenoaika huomioon suunniteltua siirtotilausta luotaessa | Kun suunniteltu siirtotilaus luodaan, järjestelmä ottaa tämän ominaisuuden ansiosta huomioon nimikkeen oletustilausasetuksissa määritetyn varaston läpimenoajan laskettaessa suunnitellun siirtotilauksen vastaanottopäivämäärää, jos toimituspäivämäärän tarkistusasetuksena on *Ei mitään*- tai *Myynti*-tyypin läpimenoaika. Jos siirron läpimenoaika on määritetty, sen arvoa käytetään vastaanottopäivämäärän laskentaan ja kuljetuspäivät ohitetaan. |
| Hankinta | Oletusvälittäjän sopimuksen verotiedot toimittajan laskuriveillä | Tässä ominaisuudessa esitellään logiikka, jonka avulla määritetään oletusarvot välittäjäsopimuksen toimittajan laskurivien **Arvonlisävero**- ja **Nimikkeen arvonlisävero** -kentille. Tätä logiikkaa käytetään vain, kun välittäjän sopimusrivin veloitustyyppi on kirjanpito/kirjanpito. Nimikkeen arvonlisäveroryhmä ottaa oletusarvon joko välittäjän hankintaluokasta (jos se on määritetty) tai kulutyypistä. Arvonlisäveroryhmän ottaa oletusarvon toimittajan tililtä. |
| Hankinta | Rajoita ostotilausrivien määrää erätehtävää kohden | Tämän ominaisuuden avulla voit optimoida järjestelmän suorituskyvyn, kun vahvistukset ja tuotteiden vastaanotot kirjataan. Se lisää **hankintaparametrisivun** **Toimitus**-välilehteen uuden asetuksen, jonka nimi on **Tehtäväkohtaiset rivit**. Tämän uuden asetuksen avulla voit rajoittaa kunkin erätehtävän prosessien ostotilausrivien määrää. Siksi se voi estää suuria erätehtäviä hidastamasta järjestelmää. |
| Tuotetietojen hallinta | Täytä tuotemääritearvot | Tämä ominaisuus lisää kausittaisen tehtävän, jonka nimi on *Täytä tuotemääritteen arvot*. Tämä uusi kausittainen tehtävä luo puuttuvat tuotemääritteen arvotietueet määritteille, jotka on liitetty tuotteisiin tuoteluokan kautta. |
| Tuotannonhallinta | Lisämääritys tuotannon käyttöliittymässä | <p>Tämä ominaisuus lisää seuraavat asetukset **Määritä tuotannon suoritus** -sivulle:</p><ul><li>**Avaa aloitusikkuna automaattisesti hakua suoritettaessa** – Tätä asetusta käytettäessä **Aloita työ** -valintaikkuna avautuu automaattisesti, kun työntekijät etsivät työtä hakurivin avulla.</li><li>**Avaa Raportointi on meneillään -ikkuna automaattisesti hakua suoritettaessa** – Tätä asetusta käytettäessä työn **Raportointi on meneillään** -valintaikkuna avautuu automaattisesti, kun työntekijät etsivät työtä hakurivin avulla.</li><li>**Oletusarvoinen jäljellä oleva määrä Raportointi on meneillään -ikkunassa** – Kun tämä vaihtoehto on käytössä, **Raportointi on meneillään** -valintaikkunassa näkyy tuotantotyön jäljellä oleva jäljellä oleva määrä.</li></ul><p>Lisätietoja on kohdassa [Tuotannon käyttöliittymän määrittäminen](../production-control/production-floor-execution-configure.md).</p> |
| Tuotannonhallinta | Tuotantoryhmät tuotannon käyttöliittymässä | <p>Kun samaan tuotantotyöhön on liitetty useita työntekijöitä, he voivat nyt nimetä yhden työntekijän vetäjäksi. Jäljellä olevista työntekijöistä tulee tämän jälkeen automaattisesti tämän vetäjän avustajia. Tuloksena olevassa ryhmässä vain vetäjän on rekisteröitävä töiden tila, kun taas aikatietueet koskevat kaikkia ryhmän jäseniä. Tämä ominaisuus myös tukee skenaariota, jonka nimi on *apuresurssi*. Tässä skenaariossa työntekijä voi rekisteröityä avustajaksi toiselle työntekijälle, josta tulee juuri muodostetun ryhmän vetäjä.</p><p>Lisätietoja on kohdassa [Tuotannon käyttöliittymän käytön ohjeet työntekijöille](../production-control/production-floor-execution-use.md).</p> |
| Tuotannonhallinta | Suunnittelunimikkeitä koskeva raportti tuotannon käyttöliittymässä | Tämä ominaisuus yksinkertaistaa tuotantotyön käyttöliittymän nimikkeiden suunnittelussa olevien erätilausten raportointiprosessia. Kun erätilaus luodaan tuotteelle, jonka tuotantotyyppi on *Suunnittelunimike*, valmiiksi ilmoittaminen voidaan tehdä vain tämän erätilauksen osa- ja sivutuotteille. Suunnittelunimikkeiden erätilauksia käytetään yleensä hajotusprosessien tukea varten, jossa raaka-ainetuote puretaan useisiin eri tuotteisiin. Kun työntekijä raportoi suunnittelunimikkeen erätilauksen valmiiksi, **Raportointi on meneillään** -valintaikkunassa näkyvät nyt vain osa- ja sivutuotteet. Aiemmin se on myös näyttänyt suunnittelunimikkeen, ja tämä toiminta saattoi hämmentää työntekijöitä. |

## <a name="new-and-updated-documentation-resources"></a>Uudet ja päivitetyt asiakirjaresurssit

Seuraavat ohjeartikkelit on lisätty äskettäin tai niitä on päivitetty merkittävästi. Nämä artikkelit eivät välttämättä liity tällä julkaisulla lisättyihin, edellisissä osissa lueteltuihin uusiin ominaisuuksiin. Niiden avulla saatat kuitenkin saada enemmän irti olemassa olevista ominaisuuksista.

| Ominaisuusalue | Uudet tai päivitetyt artikkelit |
|---|---|
| Kustannushintojen hallinta | [Painotettu keskimääräinen päivämäärä sisältää fyysisen arvon ja merkinnän](../cost-management/weighted-average-date.md) |
| Jaettu hybriditopologia | [Kokeile Scale Uniteja jaetussa hybriditopologiassa](../cloud-edge/cloud-edge-try-out.md) |
| Kaksoiskirjoitus | [Synkronointi tarvittaessa Supply Chain Managementin hinnoittelumoduulin kanssa](../../fin-ops-core/dev-itpro/data-entities/dual-write/pricing-engine.md) |
| Varastonhallinta   | [Vapauta varastoon](../warehousing/release-to-warehouse-process.md) |

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Talous- ja toimintosovellusten ympäristöpäivitykset

Microsoft Dynamics 365 Supply Chain Management 10.0.27 sisältää Platform updateja. Lisätietoja on kohdassa [Talous- ja toimintosovellusten (kesäkuu 2022) käyttöympäristön päivitysversio 10.0.27](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-27.md).

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.27 virheenkorjauksista päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 1 -suunnitelma

Haluatko tietoja tulevien ja juuri julkaistujen yrityssovellustemme tai -ympäristöjemme ominaisuuksista?

Katso [Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 1 -suunnitelma](/dynamics365-release-plan/2022wave1/). Olemme koonneet kaikki tarvittavat tiedot yhteen asiakirjaan, jota voit käyttää suunnittelun apuna.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Poistetut ja vanhentuneet Supply Chain Management -toiminnot

[Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -artikkelissa kerrotaan toiminnoista, jotka on ajoitettu poistettaviksi tai vanhentuviksi tai jotka on poistettu Supply Chain Managementissa.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Ennen kuin toiminto poistetaan tuotteesta, siitä annetaan vanhentumisilmoitus [Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -artikkelissa 12 kuukautta ennen poistoa.

Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä toiminnalliset päivitykset on tehtävä kääntäjään.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

