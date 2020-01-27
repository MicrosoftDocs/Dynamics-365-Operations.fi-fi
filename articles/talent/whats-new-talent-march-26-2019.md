---
title: Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (26. maaliskuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
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
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a9cd6fda0e6e0405163184327f954b66eb8c7612
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897554"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-26-2019"></a>Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (26. maaliskuuta 2019)

Tässä ohjeaiheessa käsitellään Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

### <a name="enhancements-to-interview-scheduling"></a>Parannukset haastattelujen aikataulutukseen
Seuraavat lisätoiminnot sisältyvät haastattelun ajoitukseen.

- Rekrytoijat tai työhön ottavat esimiehet tai voivat halutessaan käynnistää muistutuksen haastattelijalle palautteen antamiseksi. Muistutukseen liittyvä sähköpostimalli on myös määritettävissä.
- Jakaessaan haastattelun yhteenvedon ehdokkaan kanssa haastattelun aikatauluttaja voi halutessaan piilottaa haastattelijoiden nimet ja myös piilottaa rivejä haastattelun yhteenvedosta.

## <a name="changes-in-onboard"></a>Onboardin muutokset

### <a name="embedded-images-in-activities"></a>Sisällytetyt kuvat tehtävissä
Voit nyt upottaa kuvia suoraan tehtäviin. Sen lisäksi, että voit kopioida ja liittää kuvia Internetistä, voit ladata kuvat paikallisesta tiedostojärjestelmästä. Tehtävä voi olla enintään 1 Mt. Jos kuva on liian suuri, muokkaa kokoa ja yritä ladata se uudelleen.

[![Kartoitus](./media/embedimages.png)](./media/embedimages.png)

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset
**Koontiversio 8.1.2210**

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a>Mukautettu kenttätuki valituille kokonaisuuksille kohteessa Common Data Service 

Seuraavat Common Data Service -entiteetit tukevat nyt Talentissa luotuja asiakaskenttiä:

- Työntekijä
- Etninen tausta
- Sotaveteraanitila
- Kielikoodi
- Tehtävä
- Työlaji
- Työtehtävä
- Sijainti
- Toimityyppi
 
### <a name="employment-history-not-displayed-chronologically"></a>Työhistoriaa ei näytetä aikajärjestyksessä
Tämän muutoksen myötä työsuhdehistoria-sivulla näkyy nyt työsuhderekisterit kronologisesti, riippumatta yhtiöstä. Voit myös käyttää lajitteluvaihtoehtoja lajitellaksesi yrityksen mukaan.

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a>Kiinteät kompensaatiosuunnitelmat eivät näy, kun yritys rajoittaa käyttäjän turvallisuutta.
Tässä versiossa kiinteät korvaussuunnitelmat näkyvät nyt, kun käyttäjät rajoittavat käyttäjien turvallisuutta. Kaikkia tietoturva-asetuksia kunnioitetaan ja kiinteät suunnitelmat näkyvät niille yrityksille, joissa käyttäjällä on käyttöoikeudet. 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a>Työn tallenteita ei voi poistaa käyttämällä Talentin Open in Excel -vaihtoehtoa
Tässä versiossa voit nyt poistaa työtietueita käyttämällä **Avaa Excelissä** -asetusta Talentissa.

### <a name="upgrade-to-common-data-service"></a>Päivitä Common Data Serviceen
Common Data Service -versioon tapahtuvan päivityksen määräajat lähestyvät nopeasti. Kirjaudu sisään Power Apps-hallintakeskukseen ja tarkista, onko tietokantasi päivitettävä. Lisätietoja määräajoista ja päivityksen vaiheista on kohdassa [Päivittäminen Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>Esiversiossa

Lisätietoja esikatselutoimintojen käyttöönottamisesta on kohdasta [Esikatselutoimintojen käyttö Microsoft Dynamics 365 Talentissa](./access-preview-feature.md).

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Syykoodit on määritettävä lomatyyppien avulla.
Organisaatiot saattavat tarvita lisätietoja, jotka liittyvät aikakatkaisupyyntöihin. Näiden tietojen saamiseksi työntekijöiden täytyy sisällyttää syykoodi aikarajoituksiinsa. Tämän julkaisun avulla voit nyt määrittää tietyn lomalajin yhteydessä olevat syykoodit ja antaa työntekijöille mahdollisuuden valita syykoodin aikakatkaisupyynnöissään.

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a>Määritä syiden koodit, joita tarvitaan, kun lähetät aikaa pois tietyistä lomalajeista
Organisaatiot saattavat vaatia syykoodien asettamista tiettyihin lomalajeihin, kun työntekijät lähettävät aikaa. Tämä voi olla tarpeen maansa/alueensa tai yrityspolitiikan sääntelyvaatimuksen perusteella. Tämä julkaisu antaa HR:lle mahdollisuuden määrittää, mitkä lomalajit vaativat syykoodin. Tämä pannaan täytäntöön, kun työntekijät lähettävät aikarajoituksia, jos lomalla on syykoodi.

## <a name="coming-soon"></a>Tulossa pian

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Kompensaation lisäsuojaus (kiinteä ja muuttuva)
Monissa yrityksissä etuuspäälliköillä on ehkä vain määrättyjen kompensaatiotietueiden käyttöoikeus. Ne voivat olla johtajille tai alueellisille työntekijöille. Tämä muutoksen ansiosta henkilöstöhallinto voi hallita ja ylläpitää organisaation erilaisten työntekijäryhmien kompensaatiosuunnitelmia. Voit määrittää suojausrooleja kiinteille ja muuttuville suunnitelmille, jotka määrittelevät suunnitelmien ja suunnitelmiin liittyvien työntekijöiden tietojen, kuten palkan tai bonustietojen, käytön. Näille työntekijöille maksettavia korvauksia voi käsitellä vain pääsyllä myönnetyt roolit.

###  <a name="email-support-for-alerts"></a>Sähköpostituki hälytyksille
Finance and Operations -käyttöympäristöpäivitys 25:n avulla käyttäjät voivat luoda hälytyssääntöjä, jotka lähettävät automaattisesti sähköposti-ilmoituksia yhteyshenkilöille, kun tapahtuma käynnistyy. 

### <a name="duplicate-employee-checks-user-interface-changes"></a>Työntekijöiden kaksoiskontrollit: Käyttöliittymän muutokset
Tällä muutoksella tunnistetaan duplikaatit, kun syötät nimikenttiä, ja tila näyttää löytyneiden kopioiden määrän. Voit valita uuden sivun sisältävän linkin arvioidaksesi, käytetäänkö tunnistettua vastausta. Tietojen syöttämisen keskeyttämisen välttämiseksi kaksoiskappale ei avaudu automaattisesti.
