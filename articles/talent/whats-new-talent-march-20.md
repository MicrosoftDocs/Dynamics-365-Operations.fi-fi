---
title: Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (20. maaliskuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-20
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d69294b64c841c5486d694b129cf6c0f26fd93fd
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517910"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-20-2019"></a>Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (20. maaliskuuta 2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

### <a name="setting-the-audience-on-activities"></a>Toimintojen kohdeyleisön määrittäminen
Järjestelmän toiminnoille voi nyt määrittää kohdeyleisön. Prosessiin liittyvät toiminnot (kuten haastattelu, aikataulu, palaute ja EEO) voidaan määrittää kaikille ehdokkaille, sisäisille ehdokkaille ja ulkoisille ehdokkaille. Mukautetut toiminnot, kuten Microsoft Forms -kohteet, YouTube-videot ja WWW-sisältö, voidaan toimittaa kaikille ehdokkaille, sisäisille ehdokkaille, ulkoisille ehdokkaille tai työhönottoryhmälle.  

### <a name="improve-career-site-job-discoverability-search-engine-optimization"></a>Urasivuston töiden löydettävyyden parantaminen: Hakukoneoptimointi
Tämän toiminnon avulla hakukoneet löytävät Attractin urasivuston työilmoitukset ja indeksoivat ne. Tämä auttaa ehdokkaita löytämään Attractin urasivustoon lisätyt työt suosittujen hakukoneiden avulla.

### <a name="show-login-hint-to-candidates-who-forgot-their-credentials"></a>Näytä sisäänkirjautumisen vihje tunnistetiedot unohtaneille ehdokkaille
Jos ehdokas unohtaa sen yhteisöpalvelun tunnistiedot, jonka avulla hän haki työtä avaamalla tallennetun tai ehdokkaalle sähköpostitse lähetetyn linkin avulla, he näkevät nyt vihjeen. Vihje sisältää palveluntarjoajan nimen ja käyttäjänimen (peitetty). Näin ehdokkaat voivat käyttää työhakemusta oikeiden tunnistietojen avulla.

### <a name="help-internal-candidates-explore-internal-jobs"></a>Auta sisäisiä ehdokkaita tutustumaan sisäisiin töihin
Aiemmin ulkoiset ehdokkaat näkivät työhön ottavan esimiehen tai muun työhönottajan nimen. Tämä ongelma on korjattu. Nyt vain sisäiset ehdokkaat näkevät työn työhönottoryhmän jäsenet. Sisäisten ehdokkaiden on nyt myös helpompi tarkastella vain sisäisiä töitä ja hakea niitä. Kun ehdokas yrittää käyttää linkkiä ja tarkastella sisäistä työtä tai hakea sitä, heidän on tehtävä todennus Azure Active Directory -tunnistetietojen avulla. Sisäiset ehdokkaat voivat myös ottaa yhteyttä työhönottoryhmän jäseniin ja osoittaa kiinnostuksensa työtä kohtaan tai pyytää siitä lisätietoja. Tämä ominaisuus on käytettävissä kaikille vain sisäisille ehdokkaille tarkoitetuille töille. Lisätietoja on kohdassa [Attractin urasivuston toiminnot](./career-site.md).

### <a name="designate-silver-medalists-to-assign-high-value-applicants-for-future-positions"></a>Hopeamitalistien määrittäminen niin, että korkeamman arvon hakijat määritetään tulevia toimia varten
Työhön ottavat esimiehet ja muut työhönottajat pitävat usein listaa hakijoista, jotka ovat sopivia toimeen, mutta joita ei voi harkita työhön, koska toimi on jo täytetty. Tällaiset hakijat, joita kutsutaan hopeamitalisteiksi, ovat tärkeitä, koska heitä voidaan käyttää seuraavan kerran saman tyyppisen toimen avautuessa. Attractin avulla työhön ottavat esimiehet ja muut työhönottajat voivat nyt määrittää hopeamitalisteja hakijaluetteloihin, jos hakija on edennyt tarjousvaiheeseen. Hopeamitalistimääritys näkyy työn hakijaluettelossa sekä kykypoolinäkymässä, kun nämä hakijat ovat työhön ottavan esimiehen tai muun työhönottajan minkä tahansa poolin jäseniä. Lisäksi määritys näkyy työhistoriassa ehdokkaan kykypoolin profiilin osana. Voit esikatsella tätä toimintoa, jos järjestelmänvalvoja ottaa sen käyttöön [hallintakeskuksen ominaisuuksien hallinnan](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature) avulla.

### <a name="add-applicants-to-talent-pools"></a>Hakijoiden lisääminen kykypooleihin
Hakijoita on nyt aiempaa helpompi lisätä kykypooleihin, koska uusi toiminto näkyy hakijaluettelossa. Työhön ottava esimies tai muu työhönottaja voi valita kykypooliluettelosta valitsemalla **Lisää kykypooliin** -kuvakkeen. Tämän jälkeen hakijoiden lisääminen kykypooleihin on helppoa työn hakijaluettelosta.

### <a name="configure-whether-a-resume-is-required-to-apply-for-a-particular-job"></a>Määritä, onko ansioluettelo pakollinen tiettyä työtä haettaessa.
Asiakaspalautteen perusteella työhönottajat voivat nyt määrittää, onko ansioluettelo (ladattava tiedosto) pakollinen tiettyä työtä haettaessa. Tämä määritys on osa hakemuksen aktiviteettia. Se on käytettävissä työhönottoprosessissa. Kun tämä on käytettävissä, kaikki potentiaaliset hakijat saavat kehotteen ladata ansioluettelo, kun he hakevat tätä toimea. Hakemus ei ole valmis, jos ansioluetteloa ei ladata. Tämä vähentää hakijapoolin virheitä, koska tällöin jokainen hakija antaa tarpeeksi tietoja. Näin työhönottajat voivat lajitella hakijat.

### <a name="candidates-can-apply-to-a-job-using-their-linkedin-profile"></a>Ehdokkaat voivat hakea työtä LinkedIn-profiilin avulla.
Ehdokkaat, joilla on jo päivitetty profiili LinkedInissä, voivat hakea töitä vain yhdellä napsautuksella kyseisen profiilin kautta.

### <a name="track-how-a-candidate-profile-originated-in-the-system-and-where-your-applicants-discover-the-jobs-they-applied-for"></a>Seuraa, miten ehdokasprofiili on tullut järjestelmään ja mistä ehdokkaat löytävät työt, joihin he hakevat
Voit nyt katsoa, miten tietyn ehdokkaan profiili on saatu Attractiin, etsimällä profiilin lähteen ehdokkaan tiedoista hakemuksen tai kykypoolin profiilin **Profiili**-sivulla. Vastaavasti voit katsoa, miten hakija on löytänyt työn. Etsi hakemuksen lähde hakemuksen aktiviteettisyötteen **Hakemuksen aktiviteetti** -kohdasta. Nämä tiedot ovat käytettävissä myös kykypoolin profiilin työhistoriassa. Kun työnön ottavat esimiehet tai työhönottajat lisäävät ehdokkaita manuaalisesti, he näkevät kehotteen, jossa pyydetään määrittämään hakemuksen tai ehdokkaan profiilin lähde. Kun ehdokas hakee työtä ensimmäistä kertaa, hänen profiilin lähteensä on sama kuin hakemuksen lähde. Voit esikatsella tätä toimintoa, jos järjestelmänvalvoja ottaa sen käyttöön [hallintakeskuksen ominaisuuksien hallinnan](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature) avulla. Huomaa, että olemassa olevilla ehdokkailla ja hakijoilla ei ole lähtetietoja. Työnöhottajat voivat kuitenkin lisätä nämä tiedot manuaalisesti.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboardin ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2195

### <a name="attract-integration-throws-duplicate-record-error-for-applications"></a>Attract-integrointi aiheuttaa kahden saman tietueen virheen hakemuksille
Tässä päivityksessä kahden saman tietueen virhe on korjattu. Tämä ongelma esiintyy, kun **Henkilöstön hallinta** -työtila avataan.

### <a name="unable-to-close-form-when-editing-name-sequence"></a>Lomaketta ei voi sulkea, kun nimen järjestystä muokataan
Työntekijälomakkeen nimen järjestyksen muokkausta koskevat ongelmat on korjattu.

## <a name="coming-soon"></a>Tulossa pian

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Kompensaation lisäsuojaus (kiinteä ja muuttuva)
Monissa yrityksissä etuuspäälliköillä on ehkä vain määrättyjen kompensaatiotietueiden käyttöoikeus. Ne voivat olla johtajille tai alueellisille työntekijöille. Tämä muutoksen ansiosta henkilöstöhallinto voi hallita ja ylläpitää organisaation erilaisten työntekijäryhmien kompensaatiosuunnitelmia. Voit määrittää suojausrooleja kiinteille ja muuttuville suunnitelmille, jotka määrittelevät suunnitelmien ja suunnitelmiin liittyvien työntekijöiden tietojen, kuten palkan tai bonustietojen, käytön. Näille työntekijöille maksettavia korvauksia voi käsitellä vain roolit, joille on myönnetty käyttöoikeus.

###  <a name="email-support-for-alerts"></a>Sähköpostituki hälytyksille
Platform-päivityksen 24 avulla käyttäjät voivat luoda hälytyssääntöjä, jotka lähettävät automaattisesti sähköpostiviestejä yhteystietoihin, kun tapahtuma käynnistyy.

### <a name="duplicate-employee-check-interface-changes"></a>Työntekijätietojen kaksoiskappaleiden tarkistus: Käyttöliittymän muutokset
Tällä muutoksella tunnistetaan duplikaatit, kun syötät nimikenttiä, ja tila näyttää löytyneiden kopioiden määrän. Voit valita uuden sivun sisältävän linkin arvioidaksesi, käytetäänkö tunnistettua vastausta. Tietojen syöttämisen keskeyttämisen välttämiseksi kaksoiskappale ei avaudu automaattisesti.


