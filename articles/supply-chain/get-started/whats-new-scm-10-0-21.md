---
title: Dynamics 365 Supply Chain Managementin version 10.0.21 uudet tai muuttuneet ominaisuudet (lokakuu 2021)
description: Tässä ohjeaiheessa käsitellään Dynamics 365 Supply Chain Managementin version 10.0.21 uusia tai muuttuneita ominaisuuksia.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 894686446436a390ec2d019672e3a2b8b0e5f5ef
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579733"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10021-october-2021"></a>Dynamics 365 Supply Chain Managementin version 10.0.21 uudet tai muuttuneet ominaisuudet (lokakuu 2021)

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin version 10.0.21 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.960. Se on käytettävissä seuraavasti:

- **Julkaisun esiversio:** Elokuu 2021
- **Version yleinen saatavuus (oma päivitys):** syyskuu 2021
- **Version yleinen saatavuus (automaattinen päivitys):** lokakuu 2021

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Seuraavassa taulukossa on tämän julkaisun sisältämät toiminnot. *Ominaisuus*-sarakkeessa on linkki [julkaisusuunnitelmaan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), jossa voit tarkastella kuinkin ominaisuuden virallisia julkaisupäiviä. *Lisätietoja*-sarakkeessa on lisätietoja ja/tai linkkejä liittyvään dokumentaatioon.

Useimmat näistä toiminnoista on otettava käyttöön [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -kohdassa ennen niiden käyttämistä.

| Ominaisuusalue | Ominaisuus | Lisätietoja |
|---|---|---|
| Varasto&nbsp;ja&nbsp;logistiikka | [Yleinen varastokirjanpitoapuohjelma Dynamics 365 Supply Chain Managementille](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [Yleisen varastokirjanpidon aloitussivu](../global-inventory-accounting/global-inventory-accounting-home.md) |
| Varasto&nbsp;ja&nbsp;logistiikka | [Kirjaa käyttökelpoisia oikaisuja käyttäen vastatileihin liitettyjä syykoodeja](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [Varastoinventoinnin syykoodit](../warehousing/reason-codes-for-counting-journals.md) |
| Varasto&nbsp;ja&nbsp;logistiikka | [Myyntitarjouksen viitattujen tietojen vientikäytäntö](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | Valitse, aiheuttaako lainausten viittaamien tietojen muutokset kyseiset lainaukset (tai rivit) sisällytettäviksi seuraavaan lisävientitoimintaan. Lisäviennit suoritetaan nopeammin, jos tällaisia tarjouksia tai rivejä ei sisällytetä.<br><br>Tämä ominaisuus lisää asetuksen, jota kutsutaan **Ohita myyntitarjoukseen viitatut tiedot, kun muutoksia seurataan** **Myyntireskontra-parametrit** -sivulla. |
| Varasto&nbsp;ja&nbsp;logistiikka | Salattu tarjous <!-- KFM: Add RP link when available --> | [Sinetöidyt tarjoukset tarjouspyyntöihin](../procurement/sealed-bidding.md) |
| Varasto&nbsp;ja&nbsp;logistiikka | [Skannaa varaston viivakoodit GS1-muotostandardien avulla](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1-viivakoodit ja QR-koodit](../warehousing/gs1-barcodes.md) |
| Varasto&nbsp;ja&nbsp;logistiikka | [Varaston näkyvyyden apuohjelman alustava varaus](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [Varaston näkyvyyden varaukset](../inventory/inventory-visibility-reservations.md) |
| Varasto&nbsp;ja&nbsp;logistiikka | [Ostohyvityksen hallinnan vähennyksen ja todellisen painon parannukset](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Hallitse vähennyksiä käyttämällä vähennyksen työtilaa](../rebate-management/deduction-workbench.md )<br><br>[Ostohyvitysten käsitteleminen, tarkistaminen ja kirjaaminen](../rebate-management/process-review-post.md)<br><br>[Ostohyvitysten hallintasopimukset](../rebate-management/rebate-management-deals.md) |
| Varasto&nbsp;ja&nbsp;logistiikka | [Varastosovelluksen vaiheohjeet](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Warehouse Management ‑mobiilisovelluksen vaiheiden otsikoiden ja ohjeiden mukauttaminen](../warehousing/mobile-app-titles-instructions.md) |
| Varasto&nbsp;ja&nbsp;logistiikka | [Aiheutuneiden kustannusten päivitysten työtauot ja seurantapäivitykset](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Hyllytyksen päivitysseuranta](../landed-cost/update-tracking-putaway.md )<br><br>[Kuljetettavien tuotteiden käsittely](../landed-cost/in-transit-processing.md) |
| Pääsuunnittelu | [Negatiiviset päivät suunnittelun optimoinnissa](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Viivetoleranssi (negatiiviset päivät)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnon parannukset

Seuraavassa taulukossa on tämän julkaisun sisältämät toimintojen parannukset. Jokainen näistä parantaa aiemmin luotua toimintoa lisäysten avulla. Koska ne ovat vain parannuksia, niitä ei ole lueteltu [vapautussuunnitelmassa](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Jos kuitenkin haluat varmistaa, että nämä parannukset eivät ole ristiriidassa aiemmin luotujen mukautuksiesi tai asetuksesi kanssa, kaikki muutokset ovat oletusarvon mukaan pois käytöstä (ellei toisin ilmoiteta). Jos haluat käyttää mitä tahansa näistä ominaisuuksista, ne on nimenomaisesti otettava käyttöön [ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Ominaisuusalue | Ominaisuuden&nbsp;nimi&nbsp;ominaisuuksien&nbsp;hallinnassa | Lisätietoja |
|---|---|---|
| Kustannushintojen hallinta | Varaston sulkemisen edistymistiedot | Tämä esiversiotoiminto ottaa varaston sulkemisen edistymisen yksityiskohtaisen näkymän käyttöön. |
| Hankinta | Estä yleisten budjettivarausten ylikulutus, kun työnkulussa on useita ostoehdotuksia | Tämä esiversiotoiminto parantaa virheentarkistusta, kun käyttäjät lähettävät ja hyväksyvät ostoehdotuksia, jotka ylittävät yleisen budjetin varausrivin jäljellä olevan saldon. Tämä auttaa estämään yleisten budjettivarausten ylityönkulun, kun työnkulussa on useita ostoehdotuksia. |
| Tuotannonhallinta | Näytä täydet sarja-, erä- ja rekisterinumerot tuotannon käyttöliittymässä | Tämä ominaisuus tarjoaa paremman käyttökokemuksen sarja-, erä- ja lisenssinumeroiden tarkastelusta tuotannonohjausliittymässä. Näyttö muuttuu korttinäkymästä niin, että näkyvissä on rajallinen määrä merkkejä luettelonäkymään, jossa on tarpeeksi tilaa näyttää kaikki arvot. Luettelossa on myös mahdollisuus etsiä tiettyjä numeroita. |
| Myynti ja markkinointi | Rajoita kirjausta varten valittavien myyntitilausten määrää | Tällä ominaisuudella voidaan määrittää, kuinka monta myyntitilausta voidaan enintään valita, kun vahvistuksia, keräysluetteloita, pakkausluetteloita ja laskuja kirjataan myyntitilausten luettelosivulta. Se otetaan käyttöön automaattisesti. Ominaisuus lisää **Kirjattavien myyntitilausten enimmäismäärä** -asetuksen **Myyntireskontran parametrit** -sivulle. Uuden asetuksen oletusarvo on *100*. Ominaisuus auttaa parantamaan myyntitilausten luettelosivun suorituskykyä, kun merkittävä määrä myyntitilauksia valitaan. Se ei vaikuta myyntitilausten määrään, jotka voidaan käsitellä kausittaisen tehtävän perusteella. |
| Varastonhallinta   | Erota hyllytys lähetysilmoituksista (ASN) | Tätä toimintoa tarvitaan lähetettäessä ja vastaanottaessa ennakkoilmoitusta, kun varastonhallinnan kuormitusta suoritetaan skaalausyksikössä (osana jaettua hybriditopologiaa). Siihen lisätään uusi tietokantataulu, johon tallennetaan poispanotyön tiedot. Aiemmin nämä tiedot on tallennettu tauluihin, joita käytettiin myös ASN-tietoina. |
| Varastonhallinta   | Paikoita yhdistetyt yksiköt | Sallii järjestelmän käyttää nimikkeitä eri yksikköjen (kuten laatikoiden että koteloiden) sijainnissa. Tämän ominaisuuden avulla voit valita jokaisen korttipaikkamallin rivin eri yksikköjen tai yhden yksikön sijainnit. |
| Varastonhallinta   | Käytä nopeampaa ohjelmointirajapintaa konttien sulkemiseen/uudelleenavaamiseen pakkausasemalla | Kun tämä esiversiotoiminto on käytössä, konttiin liittyvät varastotapahtumat luodaan käyttämällä uutta valopainoprosessia, joka parantaa konttien sulkemista tai avaamista uudelleen manuaalisen pakkausluettelon käsittelyn aikana. |

## <a name="new-and-updated-documentation-resources"></a>Uudet ja päivitetyt asiakirjaresurssit

Seuraavat ohjeaiheet on lisätty äskettäin tai niitä on päivitetty merkittävästi. Ne eivät välttämättä liity tähän versioon liitettyihin uusiin ominaisuuksiin, jotka on mainittu edellisessä osassa, mutta ne voivat auttaa käyttämään nykyisiä ominaisuuksia tehokkaammin.

| Ominaisuusalue | Uudet tai päivitetyt ohjeaiheet |
|---|---|
| Pääsuunnittelu | [Varastoennusteet](../master-planning/inventory-forecast.md) |
| Pääsuunnittelu | [Parametrit, joita ei käytetä suunnittelun optimoinnissa](../master-planning/planning-optimization/not-used-parameters.md) |
| Pääsuunnittelu | [Täydennysmenetelmät ja määrän muokkaus](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| Pääsuunnittelu | [Ajoitus rajattoman kapasiteetin avulla](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Pääsuunnittelu | [Suunnitelman historia- ja suunnittelulokien tarkasteleminen](../master-planning/planning-optimization/plan-history-logs.md) |
| Varastonhallinta   | [Konttien pakkausstrategiat](../warehousing/container-packing-strategy-overview.md) |
| Varastonhallinta   | [Inventoinnin esimerkkiskenaariot](../warehousing/cycle-counting-scenarios.md) |
| Varastonhallinta   | [Tuo saapuvat ASN:t V2-tietoyksikön kautta](../warehousing/import-asn-v2-data-entity.md) |
| Varastonhallinta   | [Myyntitilausten ja siirtotilausten ylikeräily](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| Varastonhallinta   | [Etikettien tulostamisen ajoitus aallon aikana](../warehousing/configure-task-based-wave-label-printing.md) |
| Varastonhallinta   | [Warehouse Management -mobiilisovelluksen uudet ja muuttuneet ominaisuudet](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Ympäristön päivitykset Finance and Operations -sovelluksille

Microsoft Dynamics 365 Supply Chain Management 10.0.21 sisältää Platform updateja. Lisätietoja on kohdassa [Finance and Operations -sovellusten (lokakuu 2021) käyttöympäristön päivitysversio 10.0.21](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.21 virheenkorjauksista päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de).

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
