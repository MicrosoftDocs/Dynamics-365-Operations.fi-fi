---
title: Dynamics 365 Supply Chain Managementin version 10.0.26 esikatselu (toukokuu 2022)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin version 10.0.26 uusia tai muuttuneita ominaisuuksia.
author: kamaybac
ms.date: 03/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 2b39eef816aaa383f0f8cbf1b2c308a6eafebd8f
ms.sourcegitcommit: a3b121a8c8daa601021fee275d41a95325d12e7a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8524434"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10026-may-2022"></a>Dynamics 365 Supply Chain Managementin version 10.0.26 esikatselu (toukokuu 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin esikatseluversion 10.0.26 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.1192. Se on käytettävissä seuraavasti:

- **Julkaisun esikatselu:** Maaliskuu 2022
- **Julkaisun yleinen saatavuus (itsepäivitys):** Huhtikuu 2022
- **Julkaisun yleinen saatavuus (automaattinen päivitys):** Toukokuu 2022

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Seuraavassa taulukossa on tämän julkaisun sisältämät toiminnot. Tämän aiheen päivitys saattaa sisältää ominaisuuksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.

| Ominaisuusalue | Ominaisuus | Lisätietoja | Käyttöönottaja:   |
|---|---|---|---|
| Varasto ja logistiikka | [Käytettävissä olevan varaston Varaston näkyvyys -kysely tukee varastonhallinnan lisänimikkeitä](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-visibility-support-advanced-warehouse-management) | Tulossa pian | Toimintojen hallinta:<br>*Ota varastonimikkeet käyttöön Varaston näkyvyys -kohdassa* |
| Varasto ja logistiikka | [Varaston näkyvyyden lisäosan luvattavissa oleva määrä](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/available-to-promise-inventory-visibility-add-in) | [Varaston näkyvyyden käytössä olevat muutosaikataulut ja luvattavissa olevat määrät](../inventory/inventory-visibility-available-to-promise.md) | Palvelumääritysten käyttöönottama |
| Valmistus | [Todellisen painon nimikkeet tuotannon työnohjausliittymälle](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/catch-weight-items-production-floor-execution-interface) | [Tuotannon käyttöliittymän käytön ohjeet työntekijöille](../production-control/production-floor-execution-use.md) | Toimintojen hallinta:<br>*(Esiversio) Todellisen painon nimikkeiden raportointi tuotannon käyttöliittymästä* |
| Valmistus | Omat työt -välilehti tuotannon käyttöliittymässä <!-- KFM: Add link to release plan when available --> | [Tuotannon käyttöliittymän käytön ohjeet työntekijöille](../production-control/production-floor-execution-use.md) | Toimintojen hallinta:<br>*Omat työt -välilehti tuotannon käyttöliittymässä* |

## <a name="feature-enhancements-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnon parannukset

Seuraavassa taulukossa on tämän julkaisun sisältämät ominaisuuksien parannukset. Jokainen näistä parannuksista parantaa aiemmin luotua toimintoa lisäysten avulla. Koska ne ovat vain parannuksia, niitä ei ole lueteltu [vapautussuunnitelmassa](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Jos kuitenkin haluat varmistaa, että nämä parannukset eivät ole ristiriidassa aiemmin luotujen mukautuksiesi tai asetuksesi kanssa, kaikki muutokset ovat oletusarvon mukaan pois käytöstä (ellei toisin ilmoiteta).

Jos haluat ottaa jonkin näistä ominaisuuksista käyttöön tai poistaa ne käytöstä, sinun on tehtävä se [ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moduuli | Ominaisuuden nimi ominaisuuksienhallinnassa | Lisätietoja |
|---|---|---|
| Hankinta | Kirjaa varastoitujen tuotteiden ja jäljellä olevien ei-varastoitavien tuotteiden rekisteröidyt määrät vastaanottoja ja toimittajan laskuja varten | Tämä ominaisuus muuttaa sitä, miten varastoimattoman tuotteen (kuten palveluiden) määrät kirjataan käsiteltäessä toimittajan laskuja ja saapuvia toimituksia ostotilauksiin verrattuna. Ominaisuus muuttaa *Rekisteröity määrä ja rekisteröidyt palvelut* -määrävaihtoehdon toimintatapaa vastaanottojen ja toimittajan laskujen kirjaamista varten. Se muuttaa sen vastaamaan *Rekisteröity määrä ja ei-varastoitavat tuotteet* -asetusta, joka on jo annettu myyntipakkausluetteloiden määrien kirjaamisen yhteydessä.<br><br>Kun kirjaat tuotteen vastaanoton tai toimittajan laskun käyttämällä *Rekisteröity määrä ja palvelut* -asetusta, järjestelmä kirjaa varastoitujen tuotteiden rekisteröidyn määrän mutta kirjaa ei-varastoitavien tuotteiden jäljellä olevan määrän (mukaan lukien sekä palvelut että muut kuin palvelut). Ilman tätä ominaisuutta järjestelmä kirjaa edelleen varastoitujen tuotteiden rekisteröidyn määrän (mukaan lukien varastoitaviksi nimikkeiksi määritetyt palvelut) mutta kirjaa aina ei-varastoitavien palvelutuotteiden täyden tilatun määrän (ja ohittaa ei-varastoitavat tuotteet, jotka eivät ole *Palvelu*-tyyppiä). |
| Hankinta | Synkronoi seurantadimensiot konsernin sisäisillä myynti- ja ostotilausriveillä | Tämän ominaisuuden avulla voit määrittää, synkronoidaanko sarja- ja eränumeroiden seurantadimensiot konsernin sisäisten myynti- ja ostotilausrivien välillä. Se lisää uusia asetuksia asiakkaiden ja toimittajien **Konsernin sisäinen** -määrityssivun **Ostotilauskäytännöt**- ja **Myyntitilauskäytännöt** -välilehdille. Se päivittää selvyyden vuoksi myös muutaman liittyvän asetuksen nimen.<br><br>Jos käytät edistynyttä varastonhallintaa (WMS), huomaa, että tämä ominaisuus synkronoi erä- ja sarjanumerot vain silloin, kun nämä dimensiot ovat sijainnin yläpuolella kohdevaraushierarkiassa. |
| Tuotetietojen hallinta | Tyhjennä tuotemääritearvot | Tämä ominaisuus lisää kausittaisen **Tyhjennä tuotemääritearvot** -nimisen tehtävän, joka tyhjentää tuotemääritteen arvotietueet, joita ei enää ole liitetty mihinkään tuotteeseen tuoteluokan kautta. |
| Varastonhallinta | (Venäjä) Estä ristiriidat, kun GTD-ilmoituksia käytetään ostotilauksissa, joissa on varastonhallintajärjestelmää käyttäviä nimikkeitä | Tämä ominaisuus on tarkoitettu vain Venäjän lokalisointiin. Se estää ristiriitoja, jotka tapahtuvat, kun myönnetään Venäjän tulli-ilmoitusnumeroita (GTD) tuontiostotilauksiin, joissa on varastonhallinnan lisätoiminnon (WMS) nimikkeitä. GTD:n myöntämisprosessi muuttaa mukautettuun kirjauskansioon sisältyvien laskujen liittyvien varastotapahtumien varastodimensioarvoja, mikä aiheuttaa ristiriidan ostotilauksen työtietueiden ja oston varastotapahtumien välillä. Kun tämä ominaisuus on käytössä, GTD-myöntämisprosessi luo oikaisutyöt, jotka eliminoivat tällaiset ristiriidat. |
| Varastonhallinta   | GS1-viivakoodien parannettu jäsennin | Tämä ominaisuus lisää GS1-symbolitietojen parannetun jäsentimen. Uusi jäsennin ottaa käyttöön GS1-yleismääritysalgoritmin GS1-symbolien jäsentämiseen ja antaa vahvempia tietojen oikeellisuustarkistuksia. |
| Varastonhallinta   | Uudet kuormasuunnittelun työtilan sivut | Lisää uudet kuormasuunnittelun työtilan sivut: **Saapuvan kuormasuunnittelun työtila** ja **Lähtevän kuormasuunnittelun työtila**. |
| Varastonhallinta   | Warehouse Management -sovellus – tyhjä GTD | Tämä ominaisuus on tarkoitettu vain Venäjän lokalisointiin. Warehouse Management -mobiilisovellusta käyttävät työntekijät voivat tarvittaessa jättää Venäjän tulli-ilmoitusnumerot (GTD) tyhjiksi. Jos GTD-seurantadimensio on määritetty sallimaan tyhjät arvot, järjestelmä hyväksyy GTD:n tyhjät arvot käytettävissä olevan varaston käytettävissä olevalle varastolle. |

## <a name="new-and-updated-documentation-resources"></a>Uudet ja päivitetyt asiakirjaresurssit

Seuraavat ohjeaiheet on lisätty äskettäin tai niitä on päivitetty merkittävästi. Nämä ohjeaiheet eivät välttämättä liity tällä julkaisulla lisättyihin, edellisissä osissa lueteltuihin uusiin ominaisuuksiin. Niiden avulla saatat kuitenkin saada enemmän irti olemassa olevista ominaisuuksista.

| Ominaisuusalue | Uudet tai päivitetyt ohjeaiheet |
|---|---|
| Kustannushintojen hallinta | Päivitettyjä esimerkkejä ja kaavioita on lisätty seuraaviin ohjeaiheisiin:<ul><li>[FIFO-merkintä ja fyysinen arvo](../cost-management/fifo-physical-value-marking.md)</li><li>[LIFO-merkintä ja fyysinen arvo](../cost-management/lifo-physical-value-marking.md)</li><li>[LIFO-päivämäärä, fyysinen arvo ja merkintä](../cost-management/lifo-date-physical-value-marking.md)</li><li>[Kustannushinnan käyttökeskiarvo](../cost-management/running-average-cost-price.md)</li><li>[Painotettu keskiarvo sekä fyysinen arvo ja merkintä](../cost-management/weighted-average-physical-value-marking.md)</li></ul> |
| Hankinta | [Ostotilausrivin tietoristiriidat](../troubleshooting/procurement/purchase-order-line-data-issues.md) |

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Taloushallinnon ja toimintojen sovellusten ympäristöpäivitykset

Microsoft Dynamics 365 Supply Chain Management 10.0.26 sisältää Platform updateja. Lisätietoja on kohdassa [taloushallinnon ja toimintojen sovellusten (toukokuu 2022) käyttöympäristön päivitysversio 10.0.26.](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-26.md).<!-- KFM Confirm link -->

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.26 virheenkorjauksista päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).

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
