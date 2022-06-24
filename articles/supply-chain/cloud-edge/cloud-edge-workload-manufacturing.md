---
title: Valmistuksen suorituksen kuormitukset pilven ja reunan asteikon yksiköitä varten
description: Tässä artikkelissa käsitellään tuotannonohjauksen kuormitusten käyttöä pilvi- ja reunapalvelujen scale unitien kanssa.
author: johanhoffmann
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: johanho
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c73c2440d8807e965e5d2d89105c2a8a6971c849
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865321"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a>Valmistuksen suorituksen kuormitukset pilven ja reunan asteikon yksiköitä varten

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Valmistuksen suorittamisen kuormitus on tällä hetkellä käytettävissä vain esiversiona.
>
> Joitakin liiketoimintatoimintoja ei tueta kokonaisuudessaan julkisessa esiversiossa, kun kuormituksen scale uniteja käytetään.
>
> Et voi suorittaa valmistuksen suorituksen työkuorman esiversiota Scale Unitille, jos varaston suorituksen työkuorma on myös asennettu.

Tuotannon suorittamisessa asteikkoyksiköt toimittavat seuraavat toiminnot:

- Koneenkäyttäjät ja työnjohtajat voivat käyttää operatiivista tuotantosuunnitelmaa.
- Koneenkäyttäjät voivat pitää suunnitelman ajan tasalla suorittamalla erillisen valmistuksen ja prosessivalmistuksen töitä.
- Tuotannoin työnjohtaja voi muokata operatiivista suunnitelmaa.
- Työntekijät voivat käyttää reunapalvelujen työajanseurantaa kellokorttina ja varmistaa näin oikean palkanlaskennan.

Tässä artikkelissa käsitellään tuotannonohjauksen kuormitusten käyttöä pilvi- ja reunapalvelujen scale unitien kanssa.

## <a name="the-manufacturing-lifecycle"></a>Valmistuksen elinkaari

Valmistuksen elinkaari jaetaan seuraavan kuvan osoittamalla tavalla kolmeen osaan: *suunnittelu*, *toteutus* ja *viimeistely*.

[![Valmistuksen toteutusvaiheet, kun käytössä on yksi ympäristö](media/mes-phases.png "Valmistuksen toteutusvaiheet, kun käytössä on yksi ympäristö.")](media/mes-phases-large.png)

_Suunnittelu_-vaihe sisältää tuotannon määrittelyn, suunnittelun, tilauksen luonnin ja aikatauluttamisen sekä vapautuksen. Vapautusvaihe ilmaisee siirtymisen _Suunnittelu_-vaiheesta _Toteutus_-vaiheeseen. Kun tuotantotilaus vapautetaan, tuotantotilauksen työt tulevat näkyviin tuotannossa ja ovat valmiita toteuttamiseen.

Kun tuotantotyö merkitään valmiiksi, se siirtyy _Suorita_-vaiheesta _Viimeistely_-vaiheeseen. _Viimeistely_-vaiheessa *Toteutus*-vaiheet rekisteröinnit siirtyvät hyväksymistyönkulkuun, jossa ne lasketaan, hyväksytään ja siirretään. Tuotantotilaus on silloin valmis. Niinpä työntekijöiden palkkaperuste luodaan.

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a>Toteutusvaiheen jakaminen erillisiksi kuormituksiksi

Kuten seuraavassa kuvassa osoitetaan, scale uniteja käytettäessä _Toteutus_-vaihe jaetaan erilliseksi kuormitukseksi.

[![Valmistuksen toteutusvaiheet scale uniteja käytettäessä](media/mes-phases-workloads.png "Valmistuksen toteutusvaiheet, kun scale unitit ovat käytössä.")](media/mes-phases-workloads-large.png)

Malli siirtyy nyt yhden esiintymän asennuksesta keskukseen ja scale uniteihin perustuvaan mallin. _Suunnittelu_- ja _Viimeistely_-vaiheet suoritetaan taustatoimintoina keskuksessa ja tuotannonohjauksen kuormitus suoritetaan scale uniteina. Tietoja siirretään asynkronisesti keskuksen ja scale unitien välillä.

Kun tuotantotilaus vapautetaan keskukseen, kaikki tuotantotöiden käsittelyyn tarvittavat tiedot siirretään scale unitiin. Näitä tietoja ovat esimerkiksi tuotantotilaukset, tuotannon reititykset, tuoterakenteet ja tuotteet. Myös tiedot, jotka eivät liity tuotantotilaukseen (kuten epäsuorat tehtävät, poissaolokoodit ja tuotannon parametrit), siirretään keskuksesta scale unitiin. Pääsääntöisesti tiedot, jotka ovat peräisin keskuksesta ja jotka siirretään scale unitiin, voidaan luoda ja päivittää vain keskuksessa. Niinpä scale unitissa ei voi luoda uutta poissaolokoodia tai epäsuoraa tehtävää, vaan niitä voidaan käyttää vain rekisteröintiin. Toteutuksen aikana scale unitissa tehdyt rekisteröinnit siirretään sitten keskukseen, jossa työajanseurannan hyväksynnän, varaston ja taloushallinnon päivitykset käsitellään.

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a>Kuormituksissa suoritettavat tuotannonohjauksen tehtävät

Seuraavat tuotannonohjauksen tehtävät voidaan tällä hetkellä suorittaa kuormituksissa scale uniteja käytettäessä:

- Saapuminen, kirjautuminen, poistuminen ja poissaolo
- Aloita työ
- Töiden niputtaminen
- Raportointi on meneillään
- Ilmoita hävikki
- Epäsuora tehtävä
- Tauko
- Ilmoita valmiiksi ja hyllytettäväksi (vaatii, että suoritat myös Scale Unitin varaston suorituksen kuormituksen, katso myös kohta [Ilmoita valmiiksi ja hyllytettäväksi Scale Unitille](#RAF))

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a>Tuotannonohjauksen kuormitusten käyttäminen keskuksessa

Yleensä prosessit, joita tarvitaan tuotannonohjauksen kuormitusten suorittamiseen, suoritetaan automaattisesti, jotta keskus ja kaikki scale unitit pysyvät tarvittaessa synkronoituina. Ongelmatilanteessa voidaan kuitenkin käynnistää manuaalisesti kuormituksista vastaanotettavien lähtötietojen rekisteröintien käsitteleminen ja/tai rekisteröinnin käsittelylokin tarkistaminen.

### <a name="manually-process-raw-registrations"></a>Lähtötietojen rekisteröintien manuaalinen käsittely

Supply Chain Managementin erätyö suoritetaan automaattisesti, ja se käsittelee kaikki kuormituksista vastaanotetut rekisteröinnit. Tämä työ luo tarvittavat tuotantokirjauskansiot ja lokikirjaviennit, kun kuormituksen valmistuneen työn rekisteröinti käsitellään.

Vaikka työ suoritetaan yleensä automaattisesti, se voidaan suorittaa manuaalisesti koska tahansa kirjautumalla keskukseen ja valitsemalla **Tuotannonhallinta \> Kausittaiset tehtävät \> Taustatoimintojen kuormituksen hallinta \> Lähdetietojen rekisteröintien käsittely**.

### <a name="check-the-raw-registration-processing-log"></a>Lähdetietojen rekisteröinnin käsittelylokin tarkistaminen

Rekisteröinnin käsittelylokia voi tarkastella kirjautumalla keskukseen ja valitsemalla **Tuotannonhallinta \> Kausittaiset tehtävät \> Taustatoimintojen kuormituksen hallinta \> Lähdetietojen rekisteröinnin käsittelyloki**. **Lähdetietojen rekisteröinnin käsittelyloki** -sivulla on luettelo käsitellyistä lähdetietojen rekisteröinneistä ja kunkin rekisteröinnin tila.

![Lähdetietojen rekisteröinnin käsittelyloki -sivu.](media/mes-processing-log.png "Lähdetietojen rekisteröinnin käsittelyloki -sivu")

Luettelossa olevaa rekisteröintiä voi käsitellä valitsemalla ensin se ja sitten jompikumpi seuraavista painikkeista toimintoruudussa:

- **Käsittele** – Valittu rekisteröinti käsitellään manuaalisesti. Tämä toiminto voi olla kätevä, jos _Lähdetietojen rekisteröintien käsittely_ -työtä ei ole suoritettu tai se epäonnistui.
- **Peruuta** – valitun rekisteröinnin peruuttaminen.

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a>Tuotannonohjauksen kuormitusten käyttäminen scale unitissa

Yleensä prosessit, joita tarvitaan tuotannonohjauksen kuormitusten suorittamiseen, suoritetaan automaattisesti, jotta keskus ja kaikki scale unitit pysyvät tarvittaessa synkronoituina. Ongelmatilanteessa scale unitissa käsiteltyjen tilausten historia voidaan kuitenkin tarkistaa tai _Tuotannon keskuksesta scale unitiin viestikäsittely_ -työ voidaan suorittaa manuaalisesti.

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a>Scale unitissa käsiteltyjen valmistustöiden historian näyttäminen

Scale unitissa käsiteltyjen valmistustöiden historiaa voi tarkastella kirjautumalla scale unit -koneeseen ja valitsemalla **Tuotannon hallinta \> Kausittaiset tehtävät \> Taustatoimintojen kuormituksen hallinta \> Valmistustöiden käsittelyhistoria**. **Valmistustöiden käsittelyhistoria** -sivulla on tuotantotilausten käsittelyhistoria scale unitissa. Luettelossa olevaa tuotantotilausta voi käsitellä valitsemalla ensin se ja sitten jompikumpi seuraavista painikkeista toimintoruudussa:

- **Käsittele** – valittu tuotantotilaus käsitellään manuaalisesti.
- **Peruuta** – valittu tuotantotilaus peruutetaan.

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a>Tuotannon keskuksesta scale unitiin viestikäsittely -työ

_Tuotannon keskuksesta scale unitiin viestikäsittely_ -työ käsittelee tiedot keskuksesta scale unitiin. Tämä työ käynnistyy automaattisesti, kun tuotannonohjauksen kuormitus otetaan käyttöön. Se voidaan kuitenkin suorittaa myös manuaalisesti koska tahansa valitsemalla **Tuotannonhallinta \> Kausittaiset tehtävät \> Taustatoimintojen kuormituksen hallinta \> Tuotannon keskuksesta scale unitiin viestikäsittely**.

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a>Ilmoita valmiiksi ja hyllytettäväksi Scale Unitille

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

Nykyisessä versiossa [varaston suorittamisen kuormitus](cloud-edge-workload-warehousing.md) tukee ilmoittamista valmiiksi ja hyllytettäviksi (valmiit tuotteet, rinnakkaistuotteet ja sivutuotteet) (ei valmistuksen suorituksen kuormitus). Jos siis haluat käyttää tätä toimintoa Scale Unitin yhteydessä, toimi seuraavasti:

- Asenna Scale Unitiin sekä varaston suorituksen kuormitus että valmistuksen suorittamisen kuormitus.
- Warehouse Management -mobiilisovelluksen avulla voit ilmoittaa töitä valmiiksi ja hyllytettäväksi. Tuotannon käyttöliittymä ei tällä hetkellä tue näitä prosesseja.

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

## <a name="enable-and-use-the-start-operation-on-a-scale-unit"></a>Aloitustoiminnon käyttöönotto ja käyttö vaakayksikössä

Nykyisessä versiossa [varaston suorittamisen kuormitus](cloud-edge-workload-warehousing.md) tukee aloitustoimintoa tuotanto- ja erätilauksille (ei valmistuksen suorituksen kuormitus). Jos siis haluat käyttää tätä toimintoa Scale Unitin yhteydessä, toimi seuraavasti:

- Asenna Scale Unitiin sekä varaston suorituksen kuormitus että valmistuksen suorittamisen kuormitus.
- Ota käyttöön *Käynnistä tuotantotilaus varaston hallinnan kuormituksessa nykyisen pilven ja reunan skaalausyksiköitä varten* -toiminto [ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Aloita tuotanto- tai erätilaus Warehouse Management -mobiilisovelluksen avulla.

## <a name="enable-and-use-material-consumption-on-a-scale-unit"></a>Materiaalikulutuksen käyttöönotto ja käyttö vaakayksikössä

Nykyisessä versiossa Warehouse Management -mobiilisovelluksen materiaalinkulutuksen rekisteröimistä tukee [varaston suorittamisen kuormitus](cloud-edge-workload-warehousing.md) (ei valmistuksen suorittamisen kuormitus). Jos siis haluat käyttää tätä toimintoa Scale Unitin yhteydessä, toimi seuraavasti:

- Asenna Scale Unitiin sekä varaston suorituksen kuormitus että valmistuksen suorittamisen kuormitus.
- Ota käyttöön *Rekisteröi materiaalikulutus skaalausyksikön mobiilisovelluksessa* -toiminto [ominaisuudenhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Rekisteröi materiaalinkulutus Warehouse Management -mobiilisovelluksen avulla.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
