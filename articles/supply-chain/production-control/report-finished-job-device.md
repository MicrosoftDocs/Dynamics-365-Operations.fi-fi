---
title: Ilmoita valmiiksi työkorttilaitteesta
description: Tässä aiheessa kuvataan, miten järjestelmä konfiguroidaan niin, että työkorttilaitteen käyttäjät voivat raportoida valmiit tuotteet tuotantotilauksesta varastoon.
author: johanhoffmann
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 67fa97c938f091c23a41ddd5aaf34a32c5a13c93
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102807"
---
# <a name="report-as-finished-from-the-job-card-device"></a>Ilmoita valmiiksi työkorttilaitteesta

[!include [banner](../includes/banner.md)]

Työntekijät käyttävät työkorttilaitteen **Raportin edistyminen** -sivua tuotantotyötä varten valmistuneiden määrien raportoinnissa. Tässä ohjeaiheessa kuvataan, miten määritetään erilaisia asetuksia, jotka määrittävät, miten työntekijät voivat tehdä ilmoituksen valmistumisesta tämän sivun avulla. Ohjeaihe sisältää myös tietoja seuraavista toiminnoista. Vaihtoehtoja ovat:

- Määrittää, lisätäänkö valmiiksi ilmoitetut määrät varastoon ja miten ne lisätään.
- Määrittää, luodaanko eränumerot, niiden luontitavan sekä määrittää, käytetäänkö niitä valmiiksi-ilmoittamisen yhteydessä.
- Määrittää, luodaanko sarjanumerot, niiden luontitavan sekä määrittää, käytetäänkö niitä valmiiksi-ilmoittamisen yhteydessä.
- Määrittää, ilmoitetaanko valmistuneeksi rekisterikilpeen ja miten se tehdään.

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a>Määrittää, lisätäänkö valmiiksi ilmoitetut määrät varastoon

Seuraavien vaiheiden avulla voit määrittää, lisätäänkö viimeisen työvaiheen valmiiksi ilmoitetut määrät varastoon.

1. Valitse **Tuotannonhallinta \> Asetukset \> Tuotannonohjaus \> Tuotantotilauksen oletusarvot**.
1. Määritä **Ilmoita valmiiksi** -välilehdessä **Päivitä valmis raportti verkossa** -kenttään jokin seuraavista arvoista:

    - **Ei** – Varastoon ei lisätä määrää, kun viimeisestä työvaiheesta raportoidaan määriä. Tuotantotilauksen tila ei muutu koskaan.
    - **Tila + määrä** – Tuotantotilauksen tilaksi tulee *Ilmoitettu valmiiksi*, ja määrä ilmoitetaan valmiiksi varastoon.
    - **Määrä** – Määrän tilaksi tulee Ilmoitettu valmiiksi, mutta tuotantotilauksen tila ei muutu koskaan.
    - **Tila** – Vain tuotantotilauksen tila muuttuu. Varastoon ei lisätä määrää, kun viimeisestä työvaiheesta raportoidaan määriä.

> [!NOTE]
> Määriä ei seurata varastossa, jos ne työvaiheet, jotka ne on ilmoitettu valmiiksi, eivät ole määritelleet viimeistä työvaihetta. Näitä määriä voidaan kuitenkin käyttää edistymisen tarkastelemiseen. Ne voidaan myös sisällyttää sääntöihin, joissa määritetään, voivatko työntekijät aloittaa seuraavan työvaiheen, ennen kuin edellisessä työvaiheessa määritetty ilmoitettu määräraja saavutetaan. Voit määrittää nämä säännöt **Tuotantotilauksen oletusarvot** -sivun **Määrän oikeellisuustarkistus** -välilehdessä.

Lisätietoja **Tuotantotilauksen oletukset** -sivun käyttämisestä on kohdassa [Tuotantoparametrit tuotannon suorituksessa](production-parameters-manufacturing-execution.md).

## <a name="report-batch-controlled-items-as-finished"></a>Eräohjattujen nimikkeiden ilmoittaminen valmiiksi

Työkorttilaite tukee kolmea eränimikkeiden raportointiskenaariota. Nämä skenaariot koskevat sekä nimikkeitä, jotka on otettu käyttöön lisävarastoprosesseja varten, että nimikkeitä, jotka eivät ole käytössä lisävarastoprosesseissa.

- **Manuaalisesti määritellyt eränumerot** - Työntekijät voivat määrittää mukautetun eränumeron. Tämä eränumero voi olla peräisin ulkoisesta lähteestä, jota järjestelmä ei tunne.
- **Ennalta määritetyt eränumerot** - Työntekijät valitsevat eränumeron niiden eränumeroiden luettelosta, jotka järjestelmä luo automaattisesti, ennen kuin tuotantotilaus vapautetaan työkorttilaitteeseen.
- **Kiinteät eränumerot** - Työntekijät eivät voi syöttää tai valita eränumeroa. Sen sijaan järjestelmä liittää tuotantotilaukseen automaattisesti eränumeron ennen kuin se on vapautettu.


### <a name="enable-the-feature-on-your-system"></a>Ominaisuuden ottaminen käyttöön järjestelmässä

Jos haluat, että työkorttilaitteet hyväksyvät eränumeron valmiiksi ilmoittamisen aikana, sinun on otettava seuraavat ominaisuudet käyttöön (tässä järjestyksessä) [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) avulla:

1. Parannettu Raportointi on meneillään -valintaikkunan käyttäjäkokemus työkorttilaitteessa
1. Ota erä- ja sarjanumeroiden antaminen käyttöön, kun valmistuminen ilmoitetaan työkorttilaitteesta

### <a name="configure-products-that-require-batch-number-reporting"></a>Niiden tuotteiden määrittäminen, jotka edellyttävät eränumeroraportointia

Jos haluat, että tuote tukee jotain käytettävissä olevaa eräseurannassa olevaa skenaariota, tee näin:

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse määritettävä tuote.
1. Valitse **Hallitse varastoa** -pikavälilehden **Eränumeroryhmä**-kentässä skenaarion tueksi määritetty seurantanumeroryhmä.

> [!NOTE]
> Jos eräohjattavia tuotteita varten ei ole määritetty eränumeroryhmää, työkorttilaite antaa eränumerolle manuaalisen merkinnän valmiiksi ilmoittamisen aikana.

Seuraavissa osissa kuvataan, miten seurantanumeroryhmiä määritetään tukemaan kolmea eränimikkeiden raportointiskenaariota.

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a>Määritä seurantanumeroryhmä, jonka avulla työntekijät määrittävät eränumeron manuaalisesti

Voit sallia manuaalisesti määritetyt eränumerot asettamalla seuraavien vaiheiden ryhmän seuraavien ohjeiden mukaisesti.

1. Siirry kohtaan **Varaston hallinta \> Asetukset \> Dimensiot \> Seurantanumeroryhmät**.
1. Luo tai valitse määritettävä seurantanumeroryhmä.
1. Määritä **Yleinen**-pikavälilehden **Manuaalinen**-asetukseksi **Kyllä**.

    ![Manuaalisten eränumeroiden seurantanumeroryhmä.](media/tracking-number-group-manual.png "Manuaalisten eränumeroiden seurantanumeroryhmä")

1. Määritä muut arvot tarpeen mukaan ja valitse sitten tämä seurantanumeroryhmä vapautettujen tuotteiden eränumeroksi, jota varten haluat käyttää tätä skenaariota.

Kun käytät tätä skenaariota, työkorttilaitteen **Raportin edistyminen** -sivun **Eränumero**-kenttä on tekstiruutu, jossa työntekijät voivat syöttää minkä tahansa arvon.

![Raportin edistymissivu, jossa on kenttä manuaalisia eränumeroita varten.](media/job-card-device-batch-manual.png "Raportin edistymissivu, jossa on kenttä manuaalisia eränumeroita varten")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a>Määritä seurantanumeroryhmä, joka sisältää luettelon esimääritetyistä eränumeroista

Voit tarjota luettelon esimääritetyistä eränumeroista asettamalla seuraavien vaiheiden ryhmän seuraavien ohjeiden mukaisesti.

1. Siirry kohtaan **Varaston hallinta \> Asetukset > Dimensiot \> Seurantanumeroryhmät**.
1. Luo tai valitse määritettävä seurantanumeroryhmä.
1. Määritä **Yleinen**-pikavälilehden **Vain varastotransaktioille** -asetukseksi **Kyllä**.
1. Käytä **Per määrä** -kenttää, kun haluat jakaa eränumerot määrää kohden määrittämäsi arvon perusteella. Esimerkiksi tuotantotilaus on kymmenen kappaletta ja **Per määrä** -kentän arvoksi on määritetty *2*. Tässä tapauksessa tuotantotilaukseen liitetään viisi eränumeroa, kun se luodaan.

    ![Ennalta määritettyjen eränumeroiden seurantanumeroryhmä.](media/tracking-number-group-predefined.png "Ennalta määritettyjen eränumeroiden seurantanumeroryhmä")

1. Määritä muut arvot tarpeen mukaan ja valitse sitten tämä seurantanumeroryhmä vapautettujen tuotteiden eränumeroksi, jota varten haluat käyttää tätä skenaariota.

Kun käytät tätä skenaariota, työkorttilaitteen **Raportin edistyminen** -sivun **Eränumero**-kenttä on pudotusvalikko, josta työntekijöiden tulee valita esimääritetty arvo.

![Raportin edistymissivu, jossa on luettelo esimääritettyjä eränumeroita varten.](media/job-card-device-batch-predefined.png "Raportin edistymissivu, jossa on luettelo esimääritettyjä eränumeroita varten")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a>Määritä seurantanumeroryhmä, joka automaattisesti määrittää eränumerot

Jos eränumerot määritetään automaattisesti ilman työntekijän syöttöä, määritä seurantanumeroryhmä noudattamalla näitä ohjeita.

1. Siirry kohtaan **Varaston hallinta \> Asetukset \> Dimensiot \> Seurantanumeroryhmät**.
1. Luo tai valitse määritettävä seurantanumeroryhmä.
1. Määritä **Yleinen**-pikavälilehden **Vain varastotransaktioille** -asetukseksi **Ei**.
1. Määritä kohdan **Manuaalinen** asetukseksi **Ei**.

    ![Kiinteiden eränumeroiden seurantanumeroryhmä.](media/tracking-number-group-fixed.png "Kiinteiden eränumeroiden seurantanumeroryhmä")

1. Määritä muut arvot tarpeen mukaan ja valitse sitten tämä seurantanumeroryhmä vapautettujen tuotteiden eränumeroksi, jota varten haluat käyttää tätä skenaariota.

Kun käytät tätä skenaariota, työkorttilaitteen **Raportin edistyminen** -sivun **Eränumero**-kenttä näyttää arvon, mutta työntekijät eivät voi muokata sitä.

![Raportin edistymissivu, jossa on kiinteä eränumero.](media/job-card-device-batch-fixed.png "Raportin edistymissivu, jossa on kiinteä eränumero")

## <a name="report-serial-controlled-items-as-finished"></a>Sarjaohjattujen nimikkeiden ilmoittaminen valmiiksi

Työkorttilaite tukee kolmea sarjaohjattujen nimikkeiden raportointiskenaariota. Nämä skenaariot koskevat sekä nimikkeitä, jotka on otettu käyttöön lisävarastoprosesseja varten, että nimikkeitä, jotka eivät ole käytössä lisävarastoprosesseissa.

- **Manuaalisesti määritellyt sarjanumerot** - Työntekijät voivat määrittää mukautetun sarjanumeron. Tämä sarjanumero voi olla peräisin ulkoisesta lähteestä, jota järjestelmä ei tunne.
- **Ennalta määritetyt sarjanumerot** - Työntekijät valitsevat sarjanumerot niiden sarjanumeroiden luettelosta, jotka järjestelmä luo automaattisesti, ennen kuin tuotantotilaus vapautetaan työkorttilaitteeseen.
- **Kiinteät sarjanumerot** - Työntekijät eivät voi syöttää tai valita sarjanumeroa. Sen sijaan järjestelmä liittää tuotantotilaukseen automaattisesti sarjanumeron ennen kuin se on vapautettu.

### <a name="enable-the-feature-on-your-system"></a>Ominaisuuden ottaminen käyttöön järjestelmässä

Jos haluat, että työkorttilaitteet hyväksyvät sarjanumeron valmiiksi ilmoittamisen aikana, sinun on otettava seuraavat ominaisuudet käyttöön (tässä järjestyksessä) [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) avulla:

1. Parannettu Raportointi on meneillään -valintaikkunan käyttäjäkokemus työkorttilaitteessa
1. Ota erä- ja sarjanumeroiden antaminen käyttöön, kun valmistuminen ilmoitetaan työkorttilaitteesta

### <a name="configure-products-that-require-serial-number-reporting"></a>Niiden tuotteiden määrittäminen, jotka edellyttävät sarjanumeroraportointia

Jos haluat, että tuote tukee jotain käytettävissä olevaa sarjanumeroseurannassa olevaa skenaariota, tee näin:

Kukin skenaario otetaan käyttöön seuraavasti.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse määritettävä tuote.
1. Valitse **Hallitse varastoa** -pikavälilehden **Sarjanumeroryhmä**-kentässä skenaarion tueksi määritetty seurantanumeroryhmä.

> [!NOTE]
> Jos sarjaohjattavia tuotteita varten ei ole määritetty sarjanumeroryhmää, työkorttilaite antaa sarjanumerolle manuaalisen merkinnän valmiiksi ilmoittamisen aikana.

Seuraavissa osissa kuvataan, miten seurantanumeroryhmiä määritetään tukemaan kolmea sarjaseurantanimikkeiden raportointiskenaariota.

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-serial-number"></a>Määritä seurantanumeroryhmä, jonka avulla työntekijät määrittävät sarjanumeron manuaalisesti

Voit sallia manuaalisesti määritetyt sarjanumerot asettamalla seuraavien vaiheiden ryhmän seuraavien ohjeiden mukaisesti.

1. Siirry kohtaan **Varaston hallinta \> Asetukset \> Dimensiot \> Seurantanumeroryhmät**.
1. Luo tai valitse määritettävä seurantanumeroryhmä.
1. Määritä **Yleinen**-pikavälilehden **Manuaalinen**-asetukseksi **Kyllä**.

    ![Seurantanumeroryhmät-sivu, sarjanumerot.](media/tracking-number-group-manual-serial.png "Seurantanumeroryhmät-sivu, sarjanumerot")

1. Määritä muut arvot tarpeen mukaan ja valitse sitten tämä seurantanumeroryhmä vapautettujen tuotteiden sarjanumeroksi, jota varten haluat käyttää tätä skenaariota.

Kun käytät tätä skenaariota, työkorttilaitteen **Raportin edistyminen** -sivun **Sarjanumero**-kenttä on tekstiruutu, jossa työntekijät voivat syöttää minkä tahansa sarjanumeron arvon. Arvon syöttämisen yhteydessä se lisätään sarjanumeroluetteloon. Tässä luettelossa työntekijät voivat tehdä seuraavia toimintoja:

- Jos haluat merkitä sarjanumeron hävikiksi, valitse **Hävikki**-painike soveltuvalla rivillä. Työntekijää pyydetään antamaan **virheen syy**.
- Jos haluat poistaa sarjanumeron, valitse **PÅoista**-painike soveltuvalla rivillä.

![Raportin edistymissivu, jossa on kenttä manuaalisia sarjanumeroita varten.](media/job-card-device-serial-manual.png "Raportin edistymissivu, jossa on kenttä manuaalisia sarjanumeroita varten")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-serial-numbers"></a>Määritä seurantanumeroryhmä, joka sisältää luettelon esimääritetyistä sarjanumeroista

Voit tarjota luettelon esimääritetyistä sarjanumeroista asettamalla seuraavien vaiheiden ryhmän seuraavien ohjeiden mukaisesti.

1. Siirry kohtaan **Varaston hallinta \> Asetukset \> Dimensiot \> Seurantanumeroryhmät**.
1. Luo tai valitse määritettävä seurantanumeroryhmä.
1. Määritä **Yleinen**-pikavälilehden **Vain varastotransaktioille** -asetukseksi **Kyllä**.
1. Käytä **Per määrä** -kenttää, kun haluat jakaa sarjanumerot määrälle, joka on yksi.

    ![Ennalta määritettyjen sarjanumeroiden seurantanumeroryhmä.](media/tracking-number-group-predefined-sn.png "Ennalta määritettyjen sarjanumeroiden seurantanumeroryhmä")

1. Määritä muut arvot tarpeen mukaan ja valitse sitten tämä seurantanumeroryhmä vapautettujen tuotteiden sarjanumeroksi, jota varten haluat käyttää tätä skenaariota.

Kun käytät tätä skenaariota, työkorttilaitteen **Raportin edistyminen** -sivun **Sarjanumero**-kenttä on pudotusvalikko, josta työntekijöiden tulee valita esimääritetty arvo.

![Raportin edistymissivu, jossa on luettelo esimääritettyjä sarjanumeroita varten.](media/job-card-device-serial-predefined.png "Raportin edistymissivu, jossa on luettelo esimääritettyjä sarjanumeroita varten")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-serial-numbers"></a>Määritä seurantanumeroryhmä, joka automaattisesti määrittää sarjanumerot

Jos sarjanumerot määritetään automaattisesti ilman työntekijän syöttöä, määritä seurantanumeroryhmä noudattamalla näitä ohjeita.

1. Siirry kohtaan **Varaston hallinta \> Asetukset \> Dimensiot \> Seurantanumeroryhmät**.
1. Luo tai valitse määritettävä seurantanumeroryhmä.
1. Määritä **Yleinen**-pikavälilehden **Vain varastotransaktioille** -asetukseksi **Ei**.
1. Määritä kohdan **Manuaalinen** asetukseksi **Ei**.

    ![Kiinteiden sarjanumeroiden seurantanumeroryhmä.](media/tracking-number-group-fixed-sn.png "Kiinteiden sarjanumeroiden seurantanumeroryhmä")

1. Määritä muut arvot tarpeen mukaan ja valitse sitten tämä seurantanumeroryhmä vapautettujen tuotteiden sarjanumeroksi, jota varten haluat käyttää tätä skenaariota.

Kun käytät tätä skenaariota, työkorttilaitteen **Raportin edistyminen** -sivun **Sarjanumero**-kenttä näyttää arvon, mutta työntekijät eivät voi muokata sitä. Tämä skenaario on tarpeellinen vain, jos tuotantotilaus luodaan yhden kappaleen määrälle sarjanumeroseurannassa olevia nimikkeitä.

![Raportin edistymissivu, jossa on kiinteä sarjanumero.](media/job-card-device-serial-fixed.png "Raportin edistymissivu, jossa on kiinteät sarjanumerot")

## <a name="report-as-finished-to-a-license-plate"></a>Ilmoita valmistuneeksi rekisterikilpeen

Lisävarastoprosessit voivat käyttää käyttöoikeuskilpi-dimensiota tähän tarkoitukseen määritettyjen varastosijaintien varastonseurantaan. Tässä tapauksessa rekisterinumero on pakollinen, kun työntekijä ilmoittaa määrät valmiiksi.

### <a name="enable-license-plate-reporting-and-label-printing"></a>Rekisterikilven raportoinnin ja etiketin tulostuksen ottaminen käyttöön

Tässä osassa kuvattujen toimintojen käyttäminen edellyttää, että otat seuraavat ominaisuudet käyttöön [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) avulla (tässä järjestyksessä):

1. *Rekisterikilpi valmiiksi raportointia varten on lisätty työkorttilaitteeseen*<br>(Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on oletusarvoisesti käytössä. Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on pakollinen.)
1. *Ota käyttöön rekisterikilven numeron automaattinen luonti, kun työkorttilaitteessa raportoidaan valmiiksi*<br>(Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on pakollinen.)
1. *Tulosta etiketti työkorttilaitteesta*<br>(Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on pakollinen.)

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a>Aseta raportointi valmistuneeksi rekisterikilpeen

Noudattamalla seuraavia ohjeita voit määrittää, pitääkö työntekijöiden käyttää uudelleen aiemmin luotua rekisterikilpeä vai luoda uusi rekisterikilpi, kun he raportoivat määrät valmiiksi.

1. Valitse **Tuotannonhallinta \> Asetukset \> Tuotannonohjaus \> Konfiguroi työkortti laitteita varten**.
2. Aseta seuraavat asetukset kullekin laitteelle:

    - **Luo rekisterikilpi** – Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat luoda uuden rekisterikilven kullekin valmistuneelle raportille. Aseta arvoksi **Ei**, jos aiemmin luotua rekisterikilpeä käytetään jokaisen valmiiksi määritetyn raportin yhteydessä.
    - **Tulosta etiketti** – Määritä tämän asetuksen arvoksi **Kyllä**, jos työntekijän tulee tulostaa käyttöoikeuskilven otsikon kullekin valmiille raportille. Määritä arvoksi **Ei**, jos etikettiä ei tarvita. 

![Konfiguroi työkortti laitteita varten -sivu.](media/config-job-card-raf.png "Konfiguroi työkortti laitteita varten -sivu")

> [!NOTE]
> Määrittääksesi etiketin, siirry kohtaan **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Asiakirjan reititysasettelut**. Lisätietoja on kohdassa [Rekisterikilven tarratulostuksen ottaminen käyttöön](../warehousing/tasks/license-plate-label-printing.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]