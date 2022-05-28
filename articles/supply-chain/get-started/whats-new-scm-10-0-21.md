---
title: Dynamics 365 Supply Chain Managementin version 10.0.21 uudet tai muuttuneet ominaisuudet (lokakuu 2021)
description: Tässä ohjeaiheessa käsitellään Dynamics 365 Supply Chain Managementin version 10.0.21 uusia tai muuttuneita ominaisuuksia.
author: kamaybac
ms.date: 10/28/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: cf38717ab3768249e3c9b988ee3893c5e539bcd0
ms.sourcegitcommit: 90ffd763d18f97654b9dbc9e3f71c998e6094c6b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2022
ms.locfileid: "8739384"
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
| Varasto&nbsp;ja&nbsp;logistiikka | [Salattu tarjous](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sealed-bidding) | [Sinetöidyt tarjoukset tarjouspyyntöihin](../procurement/sealed-bidding.md) |
| Varasto&nbsp;ja&nbsp;logistiikka | [Varaston näkyvyyden apuohjelman alustava varaus](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [Varaston näkyvyyden varaukset](../inventory/inventory-visibility-reservations.md) |
| Varasto&nbsp;ja&nbsp;logistiikka | [Ostohyvityksen hallinnan vähennyksen ja todellisen painon parannukset](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Hallitse vähennyksiä käyttämällä vähennyksen työtilaa](../rebate-management/deduction-workbench.md )<br><br>[Ostohyvitysten käsitteleminen, tarkistaminen ja kirjaaminen](../rebate-management/process-review-post.md)<br><br>[Ostohyvitysten hallintasopimukset](../rebate-management/rebate-management-deals.md) |
| Varasto&nbsp;ja&nbsp;logistiikka | [Varastosovelluksen vaiheohjeet](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Warehouse Management ‑mobiilisovelluksen vaiheiden otsikoiden ja ohjeiden mukauttaminen](../warehousing/mobile-app-titles-instructions.md) |
| Varasto&nbsp;ja&nbsp;logistiikka | [Aiheutuneiden kustannusten päivitysten työtauot ja seurantapäivitykset](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Hyllytyksen päivitysseuranta](../landed-cost/update-tracking-putaway.md )<br><br>[Kuljetettavien tuotteiden käsittely](../landed-cost/in-transit-processing.md) |
| Pääsuunnittelu | [Negatiiviset päivät suunnittelun optimoinnissa](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Viivetoleranssi (negatiiviset päivät)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnon parannukset

Seuraavassa taulukossa on tämän julkaisun sisältämät toimintojen parannukset. Jokainen näistä parantaa aiemmin luotua toimintoa lisäysten avulla. Koska ne ovat vain parannuksia, niitä ei ole lueteltu [vapautussuunnitelmassa](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Jos kuitenkin haluat varmistaa, että nämä parannukset eivät ole ristiriidassa aiemmin luotujen mukautuksiesi tai asetuksesi kanssa, kaikki muutokset ovat oletusarvon mukaan pois käytöstä (ellei toisin ilmoiteta). Jos haluat käyttää mitä tahansa näistä ominaisuuksista, ne on nimenomaisesti otettava käyttöön [ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moduuli | Ominaisuuden&nbsp;nimi&nbsp;ominaisuuksien&nbsp;hallinnassa | Lisätietoja |
|---|---|---|
| Kustannushintojen hallinta | Varaston sulkemisen edistymistiedot | Tämä esiversiotoiminto ottaa varaston sulkemisen edistymisen yksityiskohtaisen näkymän käyttöön. |
| Hankinta | Estä yleisten budjettivarausten ylikulutus, kun työnkulussa on useita ostoehdotuksia | Tämä esiversiotoiminto parantaa virheentarkistusta, kun käyttäjät lähettävät ja hyväksyvät ostoehdotuksia, jotka ylittävät yleisen budjetin varausrivin jäljellä olevan saldon. Tämä auttaa estämään yleisten budjettivarausten ylityönkulun, kun työnkulussa on useita ostoehdotuksia. |
| Tuotannonhallinta | Näytä täydet sarja-, erä- ja rekisterinumerot tuotannon käyttöliittymässä | Tämä ominaisuus tarjoaa paremman käyttökokemuksen sarja-, erä- ja lisenssinumeroiden tarkastelusta tuotannonohjausliittymässä. Näyttö muuttuu korttinäkymästä niin, että näkyvissä on rajallinen määrä merkkejä luettelonäkymään, jossa on tarpeeksi tilaa näyttää kaikki arvot. Luettelossa on myös mahdollisuus etsiä tiettyjä numeroita. |
| Myynti ja markkinointi | Rajoita kirjausta varten valittavien myyntitilausten määrää | Tällä ominaisuudella voidaan määrittää, kuinka monta myyntitilausta voidaan enintään valita, kun vahvistuksia, keräysluetteloita, pakkausluetteloita ja laskuja kirjataan myyntitilausten luettelosivulta. Se otetaan käyttöön automaattisesti. Ominaisuus lisää **Kirjattavien myyntitilausten enimmäismäärä** -asetuksen **Myyntireskontran parametrit** -sivulle. Uuden asetuksen oletusarvo on *100*. Ominaisuus auttaa parantamaan myyntitilausten luettelosivun suorituskykyä, kun merkittävä määrä myyntitilauksia valitaan. Se ei vaikuta myyntitilausten määrään, jotka voidaan käsitellä kausittaisen tehtävän perusteella. |
| Varastonhallinta   | Erota hyllytys lähetysilmoituksista (ASN) | Tätä toimintoa tarvitaan lähetettäessä ja vastaanottaessa ennakkoilmoitusta, kun varastonhallinnan kuormitusta suoritetaan skaalausyksikössä (osana jaettua hybriditopologiaa). Siihen lisätään uusi tietokantataulu, johon tallennetaan poispanotyön tiedot. Aiemmin nämä tiedot on tallennettu tauluihin, joita käytettiin myös ASN-tietoina. |
| Varastonhallinta   | Paikoita yhdistetyt yksiköt | Sallii järjestelmän käyttää nimikkeitä eri yksikköjen (kuten laatikoiden että koteloiden) sijainnissa. Tämän ominaisuuden avulla voit valita jokaisen korttipaikkamallin rivin eri yksikköjen tai yhden yksikön sijainnit. |
| Varastonhallinta   | Käytä nopeampaa ohjelmointirajapintaa konttien sulkemiseen/uudelleenavaamiseen pakkausasemalla | Kun tämä esiversiotoiminto on käytössä, konttiin liittyvät varastotapahtumat luodaan käyttämällä uutta valopainoprosessia, joka parantaa konttien sulkemista tai avaamista uudelleen manuaalisen pakkausluettelon käsittelyn aikana. |

## <a name="features-turned-on-by-default-in-this-release"></a>Tässä julkaisussa oletusarvoisesti käytössä olevat ominaisuudet

Seuraavassa taulukossa luetellaan ominaisuudet, jotka ovat oletusarvoisesti käytössä versiossa 10.0.21. Useimmat automaattisesti käyttöön otetut ominaisuudet voi ottaa käyttöön [ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Toiminnon nimi | Ota käyttöön päivämäärä | Toiminnon lisäysajankohta | Ominaisuuden tila | Moduuli |
| :--- | :--- | :--- | :--- | :--- |
| Käytettävissä olevan varaston raporttitallennus | 1.9.2021 | 1.4.2020 | Käytössä oletusarvoisesti | Varastonhallinta |
| Siirtotilauksen peruutus | 1.9.2021 | 13.7.2020 | Käytössä oletusarvoisesti | Varastonhallinta |
| Avaa varastokirjauskansion lukitus | 1.9.2021 | 17.8.2020 | Käytössä oletusarvoisesti | Varastonhallinta |
| Inventoinnin- ja varastonhallinnan tallennetut näkymät | 1.9.2021 | 30.9.2020 | Käytössä oletusarvoisesti | Varastonhallinta |
| Siirtyminen tuoterakenneriveiltä tuoterakenneversioon. | 1.9.2021 | 11.11.2019 | Käytössä oletusarvoisesti | Varastonhallinta |
| Käytetään mittayksikköä ja yksikkömäärää varastokirjauskansioissa | 1.9.2021 | 11.11.2019 | Käytössä oletusarvoisesti | Varastonhallinta |
| Salli tyhjät erämääritteiden arvot | 1.9.2021 | 11.11.2019 | Käytössä oletusarvoisesti | Varastonhallinta |
| Varaston siirtotilausrivien automaattinen rivinumeroiden lisäys | 1.9.2021 | 11.10.2019 | Käytössä oletusarvoisesti | Varastonhallinta |
| Varaston kirjauskansion hyväksynnän työnkulku | 1.9.2021 | 6.1.2020 | Käytössä oletusarvoisesti | Varastonhallinta |
| Ota käyttöön varaston laadunhallinnan parametrien varoitusominaisuus | 1.9.2021 | 7.10.2019 | Käytössä oletusarvoisesti | Varastonhallinta |
| Luo siirtotilaus myyntiriviltä | 1.9.2021 | 31.8.2019 | Käytössä oletusarvoisesti | Varastonhallinta |
| Ennustemallinvalinta kysynnän ennusteen tiedoissa | 1.9.2021 | 11.10.2019 | Käytössä oletusarvoisesti | Pääsuunnittelu |
| Pääsuunnittelun edistymisen visualisointi | 1.9.2021 | 7.10.2019 | Käytössä oletusarvoisesti | Pääsuunnittelu |
| Suunnittelun optimoinnin automaattinen vahvistus | 1.9.2021 | 11.10.2019 | Käytössä oletusarvoisesti | Pääsuunnittelu |
| Suunniteltujen tilausten rinnakkainen vahvistaminen | 1.9.2021 | 31.8.2019 | Käytössä oletusarvoisesti | Pääsuunnittelu |
| Tarjouksen lähettämisen onnistumissanoma | 1.9.2021 | 15.5.2019 | Käytössä oletusarvoisesti | Hankinta |
| Tarjouspyynnön viitelinkki lisätty ostotilaukseen | 1.9.2021 | 31.8.2019 | Käytössä oletusarvoisesti | Hankinta |
| Mahdollisuus vahvistaa hyväksytyt ostotilaukset toimittajayhteistyöstä erässä | 1.9.2021 | 10.9.2019 | Käytössä oletusarvoisesti | Hankinta |
| Ostojen cXML-parannukset | 1.9.2021 | 11.11.2019 | Käytössä oletusarvoisesti | Hankinta |
| Näytä &quot;Avaa julkaistut tarjouspyynnöt&quot; -linkki ruutuna | 1.9.2021 | 30.9.2020 | Käytössä oletusarvoisesti | Hankinta |
| Tarjouspyyntöjen kysymykset ja vastaukset | 1.9.2021 | 19.2.2020 | Käytössä oletusarvoisesti | Hankinta |
| Vaarallisten materiaalien tuotetiedot ja lähetysasiakirjat | 1.9.2021 | 14.6.2020 | Käytössä oletusarvoisesti | Tuotetietojen hallinta |
| Oletustilausmäärien tarkka vahvistus | 1.9.2021 | 24.6.2020 | Käytössä oletusarvoisesti | Tuotetietojen hallinta |
| Alkuperämaan/-alueen hallinnan ominaisuus | 1.9.2021 | 13.7.2020 | Käytössä oletusarvoisesti | Tuotetietojen hallinta |
| Julkaistujen tuotteiden tallennetut näkymät | 1.9.2021 | 30.9.2020 | Käytössä oletusarvoisesti | Tuotetietojen hallinta |
| Töiden hyväksynnän ja siirron valintaikkunoiden parannukset | 1.9.2021 | 11.10.2019 | Käytössä oletusarvoisesti | Tuotannonhallinta |
| Rekisterikilpi valmiiksi raportointia varten on lisätty työkorttilaitteeseen | 1.9.2021 | 31.8.2019 | Käytössä oletusarvoisesti | Tuotannonhallinta |
| Työkorttipääte-sivulle on lisätty uusi Lopeta tauko -painike | 1.9.2021 | 19.2.2020 | Käytössä oletusarvoisesti | Tuotannonhallinta |
| Ota käyttöön alihankintana hankittujen nimikkeiden osittainen vastaanotto ja korjaa Toimittaja-tyypin tuoterakennerivien hävikkilaskennan ongelma. | 1.9.2021 | 11.11.2019 | Käytössä oletusarvoisesti | Tuotannonhallinta |
| Tuotannonohjauksen tallennetut näkymät | 1.9.2021 | 17.8.2020 | Käytössä oletusarvoisesti | Tuotannonhallinta |
| Dynamics 365 Guides valmistukselle | 1.9.2021 | 13.7.2020 | Käytössä oletusarvoisesti | Tuotannonhallinta |
| Tuotannon suoritus | 1.9.2021 | 30.9.2020 | Käytössä oletusarvoisesti | Tuotannonhallinta |
| Ominaisuus, jolla voi lukita työkorttilaitteen ja työkorttipäätteen desinfiointia varten | 1.9.2021 | 10.5.2020 | Käytössä oletusarvoisesti | Tuotannonhallinta |
| Myyntitilauksen kulujen kohdistus | 1.9.2021 | 30.9.2020 | Käytössä oletusarvoisesti | Myynti ja markkinointi |
| Rajoita kirjausta varten valittavien myyntitilausten määrää | 1.9.2021 | 1.9.2021 | Käytössä oletusarvoisesti | Myynti ja markkinointi |
| Tyhjennä myyntitilauksen päivityshistoria | 1.9.2021 | 1.9.2021 | Käytössä oletusarvoisesti | Myynti ja markkinointi |
| Muuta inventointityön numerosarjaa | 1.9.2021 | 7.10.2019 | Käytössä oletusarvoisesti | Varastonhallinta   |
| Tehtävään perustuvan aallon kysynnän täydennys | 1.9.2021 | 7.10.2019 | Pakollinen | Varastonhallinta   |
| Piilota Kokonaisarvo-kenttä &quot;Kaikki kuormat&quot;- ja &quot;Kuorman tiedot&quot; -sivuilla | 1.9.2021 | 7.10.2019 | Käytössä oletusarvoisesti | Varastonhallinta   |
| Aallon etiketin tulostus | 1.9.2021 | 19.2.2020 | Pakollinen | Varastonhallinta   |
| Liitä ostotilauksen varastotapahtumat kuorman kanssa | 1.9.2021 | 6.1.2020 | Pakollinen | Varastonhallinta   |
| Laajennetut rekisterikilpien etikettien asettelut | 1.9.2021 | 19.2.2020 | Käytössä oletusarvoisesti | Varastonhallinta   |
| Organisaation laajuinen työn esto | 1.9.2021 | 19.2.2020 | Pakollinen | Varastonhallinta   |
| Työrivin tiedot | 1.9.2021 | 11.10.2019 | Käytössä oletusarvoisesti | Varastonhallinta   |
| Tee mobiililaitteen varastosiirron varaston tilan kentästä muokattava | 1.9.2021 | 16.10.2019 | Käytössä oletusarvoisesti | Varastonhallinta   |
| Vahvista lähtevät lähetykset erätöistä | 1.9.2021 | 13.7.2020 | Käytössä oletusarvoisesti | Varastonhallinta   |
| Määritä, näytetäänkö vastaanoton yhteenvetosivu mobiililaitteissa | 1.9.2021 | 1.4.2020 | Käytössä oletusarvoisesti | Varastonhallinta   |
| Moniselitteisten &#39;sijainnin ja rekisterikilven&#39; nimien ratkaisukehote | 1.9.2021 | 1.4.2020 | Käytössä oletusarvoisesti | Varastonhallinta   |
| Tallenna tuotevariantit ja seurantadimensiot varastointisovelluksessa kuormanimikkeen vastaanoton aikana | 1.9.2021 | 10.5.2020 | Käytössä oletusarvoisesti | Varastonhallinta   |
| Älä salli sellaisten kuormien luomista, jotka eivät täytä aallon kuormanrakennusmallin vaatimuksia. | 1.9.2021 | 17.8.2020 | Käytössä oletusarvoisesti | Varastonhallinta   |
| Arvioi kaikki useiden varastointiyksiköiden sijaintidirektiivien toiminnot | 1.9.2021 | 30.9.2020 | Käytössä oletusarvoisesti | Varastonhallinta   |

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
| Varastonhallinta   | [Tuo saapuvat ASN:t V3-tietoyksikön kautta](../warehousing/import-asn-data-entity.md) |
| Varastonhallinta   | [Myyntitilausten ja siirtotilausten ylikeräily](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| Varastonhallinta   | [Etikettien tulostamisen ajoitus aallon aikana](../warehousing/configure-task-based-wave-label-printing.md) |
| Varastonhallinta   | [Warehouse Management -mobiilisovelluksen uudet ja muuttuneet ominaisuudet](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Taloushallinnon ja toimintojen sovellusten ympäristöpäivitykset

Microsoft Dynamics 365 Supply Chain Management 10.0.21 sisältää Platform updateja. Lisätietoja on kohdassa [taloushallinnon ja toimintojen sovellusten (lokakuu 2021) käyttöympäristön päivitysversio 10.0.21.](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

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
