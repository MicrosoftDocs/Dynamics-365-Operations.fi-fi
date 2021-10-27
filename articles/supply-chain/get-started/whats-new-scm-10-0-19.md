---
title: Dynamics 365 Supply Chain Managementin version 10.0.19 uudet tai muuttuneet ominaisuudet (kesäkuu 2021)
description: Tässä ohjeaiheessa käsitellään Dynamics 365 Supply Chain Managementin version 10.0.19 uusia tai muuttuneita ominaisuuksia.
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0b39c3eee84a66082f1785f7f4d8a6d7dd96b63d
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2021
ms.locfileid: "7638467"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10019-june-2021"></a>Dynamics 365 Supply Chain Managementin version 10.0.19 uudet tai muuttuneet ominaisuudet (kesäkuu 2021)

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin version 10.0.19 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.837. Se on käytettävissä seuraavasti:

- **Julkaisun esiversio:** huhtikuu 2021
- **Julkaisun yleinen saatavuus (itsepäivitys):** kesäkuu 2021
- **Julkaisun yleinen saatavuus (automaattinen päivitys):** kesäkuu 2021

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Seuraavassa taulukossa on tämän julkaisun sisältämät toiminnot. *Ominaisuus*-sarakkeessa on linkki [julkaisusuunnitelmaan](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), jossa voit tarkastella kuinkin ominaisuuden virallisia julkaisupäiviä. *Lisätietoja*-sarakkeessa on lisätietoja ja/tai linkkejä liittyvään dokumentaatioon.

Useimmat näistä toiminnoista on otettava käyttöön [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -kohdassa ennen niiden käyttämistä.

| Ominaisuusalue | Ominaisuus | Lisätietoja |
|---|---|---|
| Varasto&nbsp;ja&nbsp;logistiikka | [Toimittajan lähettäneen pankin tietojen hyväksyminen ja tallentaminen](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/approve-save-vendor-submitted-bank-details) | [Toimittajan pankkitilin tietojen ylläpitäminen](../../finance/accounts-payable/maintain-vendor-bank-info.md) |
| Varasto ja logistiikka | [Yhteyshenkilön tietoyksikön viennin optimointi](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | Kun tämä on ominaisuus käytössä, viitattuihin tietoihin tehdyt muutokset eivät aiheuta siihen liittyvien kontaktien sisällyttämistä seuraavaan lisäävään vientiin. Kun tämä on ominaisuus poistettu käytöstä, viitattuihin tietoihin tehdyt muutokset aiheuttavat siihen liittyvien kontaktien sisällyttämistä seuraavaan lisäävään vientiin. |
| Varasto ja logistiikka | [Varastojen suoritustoimintojen asteittaiset parannukset scale uniteilla](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[Sanoman käsittelijän sanomat](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[Varasto-oikaisu](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[Varaston hallinnan kuormitukset pilven ja reunan asteikon yksiköitä varten](../cloud-edge/cloud-edge-workload-warehousing.md) |
| Varasto ja logistiikka | [Hakutoiminnot asiakirjan esittely- ja loppulausekentissä Myyntitarjous-sivulla](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Tämä ominaisuus lisää hakutoiminnon **asiakirjan esittely**- ja **loppulausekentissä** **Myyntitarjous**-sivulle.<br><br>Tämä ominaisuus on oletusarvoisesti käytössä. |
| Varasto ja logistiikka | [Varastonohjaus reunan scale uniteilla mukautetussa laitteistossa](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [Ota reunan scale unitit käyttöön mukautetussa laitteistossa LBD:n avulla](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Valmistus | [Tuotannonohjaus reunan scale uniteilla mukautetussa laitteistossa](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [Ota reunan scale unitit käyttöön mukautetussa laitteistossa LBD:n avulla](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Suunnittelu | Kyselypohjainen suunniteltujen tilausten vahvistaminen | [Vahvista suunnitellut tilaukset](../master-planning/planning-optimization/planned-order-firming.md) |
| Tuotetietojen hallinta | [Muuttujaehdotukset-sivun parannukset](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [Luo ennalta määriteltyjä tuotevariantteja](../pim/tasks/create-predefined-product-variants.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnon parannukset

Seuraavassa taulukossa on tämän julkaisun sisältämät toimintojen parannukset. Jokainen näistä parantaa aiemmin luotua toimintoa lisäysten avulla. Koska ne ovat vain parannuksia, niitä ei ole lueteltu [vapautussuunnitelmassa](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Jos kuitenkin haluat varmistaa, että nämä parannukset eivät ole ristiriidassa aiemmin luotujen mukautuksiesi tai asetuksesi kanssa, kaikki muutokset ovat oletusarvon mukaan pois käytöstä (ellei toisin ilmoiteta). Jos haluat käyttää mitä tahansa näistä ominaisuuksista, ne on nimenomaisesti otettava käyttöön [ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Ominaisuusalue | Ominaisuuden&nbsp;nimi&nbsp;ominaisuuksien&nbsp;hallinnassa | Lisätietoja |
|---|---|---|
| Myynti ja markkinointi | Myyntihistorian poistamisen suorituskyvyn parannukset | Myyntihistorian poistaminen voi kestää kauan, jos sitä ei suoriteta säännöllisesti ympäristöissä, joissa myyntipäivityksiä on paljon. Voit vähentää kestoa ja parantaa luotettavuutta ja jakaa sitten puhdistuserät, jotka suoritetaan rajoitetun keston ajan. Jos mahdollista, tietokantaominaisuudet suorituskykykertoimella voidaan vähentää lukitusta ja välttää tapahtumatauluihin liittyminen puhdistusta varten. Lisätietoja on kohdassa [Myyntihistorian tyhjennyksen suorituskyvyn parannukset](../sales-marketing/sales-update-history-cleanup-performance-improvements.md). |
| Myynti ja markkinointi | Päivitä pyydetty vastaanottopäivämäärä vahvistetulla päivämäärällä konsernin sisäisille tilauksille | Tämän ominaisuuden avulla voit ohjata, mitä tapahtuu myynti- ja ostopäivämäärän kenttien arvoille käytettäessä konsernin sisäistä suoraa toimitusta. Voit valita, päivittääkö järjestelmä pyydetyt päivämäärät vai jättääkö se ne päivittämättä. Jos ohitat päivityksen, pyydetyt päivämäärät edustavat sitä, mitä asiakas on pyytänyt. Jos otat päivityksen käyttöön, pyydetyt päivämäärät (kun käytetään toimituspäivämäärän hallintaa) edustavat vain aluksi sitä, mitä asiakas pyysi. Jos toimituspäivän ohjaus eroaa *Ei mitään* -päivästä, se ohita alun perin pyydetyn päivämäärän. Voit asettaa tämän vaihtoehdon käyttämällä **uutta päivityspyynnön vastaanottopäivää ja Vahvistettu päivämäärä** -asetusta yrityksen sisäisissä toimittajissa tai asiakasasetuksissa.<br><br>Jos toiminto ei ole käytössä, järjestelmä korvaa alkuperäisen myyntitilauksen pyydetyn vastaanottopäivämäärän toimituspäivän valvontasäännön perusteella, mutta pyydetty lähetyspäivämäärä säilyy ennallaan. |
| Varastonhallinta   | Pyöristä määrät alaspäin lähimpään myyntiyksikköön varastoon vapautuksen yhteydessä | Tämä ominaisuus lisää vaihtoehdon, joka voi rajoittaa vapautusten tilausmääriä varastoon. Kun avain on käytössä, tilausmäärät pyöristetään alaspäin lähimpään kokonaislukuun, ja tilaukset, joissa on vähemmän kuin yhden myyntiyksikön määriä, hylätään vapautusta varten. |
| Varastonhallinta   | Organisaation laajuinen Työn luonti -aikataulun aaltomenetelmä | Ottamalla tämän ominaisuuden käyttöön *Ajoita työn luonti* -aaltomenetelmä määritetään toimimaan rinnakkain kaikkien yritysten välillä. Tämä vaikuttaa myös useisiin lisäasetuksiin. Täydelliset tiedot ovat kohdassa [Työn luonnin aikatauluttaminen aallon aikana](../warehousing/configure-wave-schedule-work-creation.md). |

## <a name="new-and-updated-documentation-resources"></a>Uudet ja päivitetyt asiakirjaresurssit

Seuraavat ohjeaiheet on lisätty äskettäin tai niitä on päivitetty merkittävästi. Ne eivät välttämättä liity tähän versioon liitettyihin uusiin ominaisuuksiin, jotka on mainittu edellisessä osassa, mutta ne voivat auttaa käyttämään nykyisiä ominaisuuksia tehokkaammin.

| Ominaisuusalue | Uudet tai päivitetyt ohjeaiheet |
|---|---|
| Suunnittelun muutosten hallinta | [Suunnittelun muutosten hallinnan usein kysytyt kysymykset](../engineering-change-management/change-management-faq.md) |
| Hankinta | [Toimittajien luokkapyynnöt](../procurement/category-requests-from-vendors.md) |
| Tuotetietojen hallinta | [Mittayksikön hallinta](../pim/tasks/manage-unit-measure.md)<br><br>[Tuotekonfiguraatiomallin laskelmat](../pim/config-model-calculations.md) |
| Tuotannonhallinta | [Työtunnusten yhdistetty numerosarja](../production-control/unified-job-ids.md) |
| Kuljetustenhallinta | [LTL-luokat](../transportation/ltl-class.md)<br><br>[NMFC-koodit](../transportation/nmfc-codes.md) |
| Varastonhallinta, aallon luonti ja käsittely | [Aaltojen luominen ja käsittely](../warehousing/wave-processing.md)<br><br>[Varaston parametrit aaltokäsittelyä varten](../warehousing/wave-warehouse-parameters.md)<br><br>[Aaltomallit](../warehousing/wave-templates.md)<br><br>[Aallon kohdistus](../warehousing/wave-allocation-method.md)<br><br>[Työn luomisen ajoitus aallon aikana](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[Konttiinpakkaus](../warehousing/wave-containerization.md)<br><br>[Aallon suoritusilmoitukset](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Ympäristön päivitykset Finance and Operations -sovelluksille

Microsoft Dynamics 365 Supply Chain Management 10.0.19 sisältää Platform updateja. Lisätietoja on kohdassa [Finance and Operations -sovellusten (kesäkuu 2021) käyttöympäristön päivitysversio 10.0.19](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md).

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.19 virheenkorjauksista päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415).

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: vuoden 2021 julkaisuaallon 1 suunnitelma

Haluatko tietoja tulevien ja juuri julkaistujen yrityssovellustemme tai -ympäristöjemme ominaisuuksista?

Tutustu kohtaan [Dynamics 365: vuoden 2021 julkaisuaallon 1 suunnitelma](/dynamics365-release-plan/2021wave1/). Olemme koonneet kaikki tarvittavat tiedot yhteen asiakirjaan, jota voit käyttää suunnittelun apuna.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Poistetut ja vanhentuneet Supply Chain Management -toiminnot

[Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa kerrotaan toiminnoista, jotka on ajoitettu poistettaviksi tai vanhentuviksi tai jotka on poistettu Supply Chain Managementissa.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Ennen kuin toiminto poistetaan tuotteesta, siitä annetaan vanhentunisilmoitus [Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa 12 kuukautta ennen poistoa.

Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä toiminnalliset päivitykset on tehtävä kääntäjään.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
