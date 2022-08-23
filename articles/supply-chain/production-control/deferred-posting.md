---
title: Tee valmiista tavaroista fyysisesti saatavilla olevia ennen kirjauskansioihin kirjaamista
description: Kun valmistettu nimike ilmoitetaan valmiiksi, se rekisteröidään jatkokäsittelyyn ja vähintään yksi kirjauskansio kirjataan. Tässä artikkelissa kuvaillaan, kuinka kirjauskansioiden kirjauksia voidaan lykätä ottamalla ne käyttöön erätyössä sanomajonossa.
author: johanhoffmann
ms.date: 08/02/2022
ms.topic: article
ms.search.form: ProdParameters, JmgProdParameters, InventLocation, JmgMES3PMessageProcessorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-08-02
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 7a8327552d9e6c38721fdac9ee1795e61f90f329
ms.sourcegitcommit: 8d072505f66f507aafbaae65bedf3b530eb6cb7b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9266482"
---
# <a name="make-finished-goods-physically-available-before-posting-to-journals"></a>Tee valmiista tavaroista fyysisesti saatavilla olevia ennen kirjauskansioihin kirjaamista

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Kun työntekijä ilmoittaa valmistetun nimikkeen valmiiksi, järjestelmä kirjaa sen fyysiseen jatkokäsittelyyn (kuten lähetykseen tai hyllytykseen). Tämän prosessin aikana kirjataan myös yksi tai useampia kirjauskansioita (kuten raportti valmiina kirjauskansiona, keräysluettelon kirjauskansiona ja reitityskorttikirjauskansiona). Jos haluat asettaa nimikkeet fyysisesti käyttöön ennen kaikkien kirjausten käsittelemistä, voit määrittää järjestelmän lykkäämään kirjauskansiokirjauksia. Lykätyt kirjaukset hallitaan tämän jälkeen erätyöllä, joka käsittelee kirjaukset järjestelmäresurssien sallimalla tavalla.

Seuraavassa kuvassa kerrotaan, miten kirjauskansioiden kirjausprosessit kutsutaan sekä lykätyillä kirjauksilla että ilman niitä.

![Ilmoita valmiiksi -prosessi lykätyillä kirjauskansiokirjauksilla ja ilman niitä.](media/deferred-posting-flowchart.png "Ilmoita valmiiksi -prosessi lykätyillä kirjauskansiokirjauksilla ja ilman niitä")

## <a name="turn-on-deferred-journal-posting-for-your-system"></a>Lykättyjen kirjauskansiokirjausten ottaminen käyttöön järjestelmässä

Ennen kuin lykättyjä kirjauskansiokirjauksia voidaan käyttää, se on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Tuotannonhallinta*
- **Toiminnon nimi::** *(Esiversio) Tee valmiista tavaroista fyysisesti saatavilla olevia ennen kirjauskansioihin kirjaamista*

## <a name="set-up-journal-posting-options-for-reporting-as-finished"></a>Kirjauskansion kirjausasetusten määrittäminen valmiiksi ilmoittamista varten

Työntekijät voivat raportoida nimikkeet valmiiksi seuraavia asiakkaita käyttäen:

- WWW-asiakasohjelma
- Warehouse Management -mobiilisovellus
- Tuotannon käyttöliittymä

Verkkoasiakasohjelma käyttää samaa kirjaustapaa kuin Warehouse Management -mobiilisovellus. Kirjaustapa, jota tuotannon käyttöliittymä käyttää, on kuitenkin määritettävä erikseen.

### <a name="set-journal-posting-options-for-the-web-client-and-the-warehouse-management-mobile-app"></a>Kirjauskansion kirjausasetusten määrittäminen verkkoasiakasohjelmalle ja Warehouse Management -mobiilisovellukselle

Mobiilisovelluksessa työntekijät raportoivat nimikkeet valmiiksi avaamalla mobiililaitteen valikkokohteen, jossa **Työn luontiprosessi** -arvo on *Ilmoita valmiiksi* tai *Ilmoita valmiiksi ja pane pois*. Verkkoasiakasohjelmassa työntekijät raportoivat nimikkeet valmiiksi **Kaikki tuotantotilaukset** -luettelosivulta tai **Tuotantotilaus (tiedot)** -sivulta. Voit konfiguroida yrityksen laajuisen oletusmenetelmän ja määrittää myös varastokohtaisia ohitusasetuksia tarpeen mukaan.

Seuraavaa menettelyä noudattamalla voit konfiguroida yrityksen laajuisen oletuskirjausmenetelmän, jota käytetään nimikkeiden ilmoittamisessa valmiiksi verkkoasiakkaasta tai Warehouse Management -mobiilisovelluksesta.

1. Valitse **Tuotannonhallinta \> Asetukset \> Tuotannonhallinnan parametrit**.
1. Määritä **Kirjauskansiot**-välilehdessä **Valmiiksi ilmoitettujen kirjauskansio** -osassa **Kirjausmenetelmä**-kenttään jokin seuraavista arvoista:

    - *Välitön* – Kun nimike raportoidaan valmiiksi, järjestelmä käsittelee kaikki liittyvät kirjauskansiokirjaukset, ennen kuin valmiin nimikkeen on ilmoitettu olevan fyysisesti käytettävissä.
    - *Lykätty* – Kun nimike raportoidaan valmiiksi, järjestelmä merkitsee valmiin nimikkeen olevan fyysisesti käytettävissä ja lisää kirjauskansiokirjaukset viestijonoon. Järjestelmä ei odota, kunnes kirjaukset on käsitelty kokonaan, ennen kuin se merkitsee valmiin nimikkeen fyysisesti käytettävissä olevaksi.

Seuraavia ohjeita noudattamalla voit määrittää varastokohtaiset ohitukset **Tuotannonhallinnan parametrit** -sivulla konfiguroitavalle oletuskirjausmenetelmälle.

1. Mene kohtaan **Varastonhallinta \> Asetukset \> Inventaarioanalyysi \> Varastot**.
1. Valitse varasto, jonka haluat määrittää.
1. Valitse toimintoruudussa **Muokkaa**.
1. Määritä **Varasto**-pikavälilehdessä **Tuotantotilaukset**-osassa **Kirjausmenetelmä**-kenttään jokin seuraavista arvoista:

    - *Peri* – Valittu varasto perii asetuksen **Tuotannonhallinnan parametrit** -sivulta.
    - *Välitön* – Kun nimike raportoidaan valmiiksi, järjestelmä käsittelee kaikki liittyvät kirjauskansiokirjaukset, ennen kuin valmiin nimikkeen on ilmoitettu olevan fyysisesti käytettävissä.
    - *Lykätty* – Kun nimike raportoidaan valmiiksi, järjestelmä merkitsee valmiin nimikkeen olevan fyysisesti käytettävissä ja lisää kirjauskansiokirjaukset viestijonoon. Järjestelmä ei odota, kunnes kirjaukset on käsitelty kokonaan, ennen kuin se merkitsee valmiin nimikkeen fyysisesti käytettävissä olevaksi.

### <a name="set-journal-posting-options-for-the-production-floor-execution-interface"></a>Määritä kirjauskansion kirjausasetukset tuotannon käyttöliittymälle

Seuraavaa menettelyä noudattamalla voit konfiguroida kirjaustavan, jota käytetään, kun nimikkeitä ilmoitetaan valmiiksi tuotannon käyttöliittymästä.

1. Valitse **Tuotannonhallinta \> Asetukset \> Tuotannonohjaus \> Tuotantotilauksen oletusarvot**.
1. Määritä **Ilmoita valmiiksi** -välilehdessä **Valmiiksi ilmoitettujen kirjauskansio** -osassa **Kirjausmenetelmä**-kenttään jokin seuraavista arvoista:

    - *Välitön* – Kun nimike raportoidaan valmiiksi, järjestelmä käsittelee kaikki liittyvät kirjauskansiokirjaukset, ennen kuin valmiin nimikkeen on ilmoitettu olevan fyysisesti käytettävissä.
    - *Lykätty* – Kun nimike raportoidaan valmiiksi, järjestelmä merkitsee valmiin nimikkeen olevan fyysisesti käytettävissä ja lisää kirjauskansiokirjaukset viestijonoon. Järjestelmä ei odota, kunnes kirjaukset on käsitelty kokonaan, ennen kuin se merkitsee valmiin nimikkeen fyysisesti käytettävissä olevaksi.

## <a name="schedule-the-message-processor-batch-job-to-process-deferred-postings"></a>Ajoita sanoman käsittelijän erätyö käsittelemään lykättyjä kirjauksia

Sanoman käsittelijän erätyö vastaa kirjauskansion kirjausten käsittelystä sen jälkeen, kun kirjauskansiot on asetettu jonoon. Tämä työ on määritettävä suoritettavaksi säännöllisin väliajoin, jotta kirjauskansion kirjausten käsittely voidaan varmistaa. Seuraavia ohjeita noudattamalla voit määrittää vaaditun erätyön.

1. Valitse **Järjestelmänvalvoja \> Sanoman käsittelijä \> Sanoman käsittelijä**.
1. Määritä **Parametrit**-pikavälilehdessä **Sanomajono**-kentän arvoksi *Tuotanto*.
1. Määritä **Suorita taustalla** -pikavälilehdessä **Erän käsittely** -kohdan arvoksi *Kyllä*. Määritä sitten toistuva aikataulu ja konfiguroi muut asetukset tarpeen mukaan. Asetukset toimivat samalla tavalla kuin muissakin [taustatöissä](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Microsoft Dynamics 365 Supply Chain Managementissa.

## <a name="track-the-progress-of-your-deferred-postings"></a>Lykättyjen kirjausten etenemisen seuraaminen

Lykätyt kirjauskansion kirjaukset asetetaan jonoon *sanoman käsittelijän sanomina*, jotka odottavat, kunnes *sanoman käsittelijä* käsittelee ne. Sanoman käsittelijä on määritettävä suoritettavaksi ajoitettuna erätyönä. Jos haluat tarkastella sanomien käsittelijän käsittelemiä lykättyjä kirjaussanomia, valitse **Tuotannonohjaus \> Tuotantotilaukset \> Lykätty tuotantotilauksen kirjaaminen**.

### <a name="message-grid-columns-and-filters"></a>Sanomaruudukon sarakkeet ja suodattimet

**Lykätty tuotantotilauksen kirjaaminen** -sivun yläosan kenttien avulla voit etsiä haluamiasi sanomia.

Seuraavat suodattimet ovat käytettävissä:

- **Sanomatyyppi** – Määritä ruudukossa näkyvien sanomien tyyppi.
- **Sanoman tila** – Määritä ruudukossa näkyvien sanomien tila. Käytössä ovat seuraavat tilat:

    - *Jonossa* – Sanoma on valmis sanoman käsittelijän käsiteltäväksi.
    - *Käsitelty* – Sanoman käsittely sanoman käsittelijän toimesta onnistui.
    - *Peruutettu* – Sanoman käsittely ei onnistunut lopullisessa yrityksessä. Tämän jälkeen käyttäjä peruutti sen.
    - *Epäonnistui* – Sanoman käsittely ei onnistunut lopullisessa yrityksessä. Järjestelmä yrittää epäonnistuneita sanomia uudelleen kolme kertaa. Sen jälkeen se antaa periksi ja jättää sanoman *Epäonnistunut*-tilaan. Huomaa, että et voi peruuttaa tai muokata sanomaa manuaalisesti ennen viimeistä näistä kolmesta yrityksestä.

- **Sanoman sisältö** – Tämän suodattimen avulla voit tehdä tekstihakuja sanoman sisällöstä. (Sanoman sisältöä ei näytetä ruudukossa.) Suodatin käsittelee useimmat erikoissymbolit (kuten väliviivat) välilyönteinä ja käsittelee kaikkia välilyöntimerkkejä TAI-totuusarvo-operaattoreina. Jos etsit esimerkiksi tiettyä `journalid`-arvoa, joka on sama kuin *USMF-123456*, järjestelmä löytää kaikki sanomat, jotka sisältävät joko arvon "USMF" tai "123456". Tällöin tulosluettelo on todennäköisesti pitkä. Siksi olisi parempi syöttää vain *123456* siksi, että se palauttaa yksityiskohtaisia tuloksia.

Voit myös lajitella ja suodattaa luettelon valitsemalla haluamasi sarakeotsikot ja kirjoittamalla ehdot avattavaan valintaikkunaan.

### <a name="view-the-message-log-message-content-and-details"></a>Sanomalokin, sanomasisällön ja tietojen tarkasteleminen

Voit etsiä yksityiskohtaisia tietoja sanomasta valitsemalla sen ruudukosta ja valitsemalla sitten **Loki**- tai **Raakasisältö**-välilehden sanomaruudukosta, jossa näkyy kukin käsittelytapahtuma.

**Loki**-välilehden työkalurivi sisältää seuraavat painikkeet:

- **Loki** – Valitsemalla tämän painikkeen voit näyttää käsittelytulokset. Tämä painike on erityisen hyödyllinen, kun sanomien **käsittelytuloksen** arvona on *Epäonnistui* ja haluat tietää, miksi käsittely epäonnistuu.
- **Myyntirakenne** – Useita sanomankäsittelytoimintoja voi suorittaa saman eräprosessin osana. Valitsemalla tämän painikkeen voit tarkastella näitä yksityiskohtaisia tietoja. Voit esimerkiksi nähdä, onko olemassa riippuvuuksia, jotka edellyttävät, että jotkut sanomat käsitellään tietyssä järjestyksessä.

### <a name="manually-process-or-cancel-a-message"></a>Sanoman käsitteleminen manuaalisesti tai sen peruuttaminen

Voit tarvittaessa käsitellä tai peruuttaa sanoman manuaalisesti sen nykyisen tilan mukaan. Valitse sanoma ruudukossa ja valitse sitten toimintoruudusta **Käsittele** tai **Peruuta**.

### <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Liiketapahtumien määrittäminen hälytyksien toimitusta varten käsittelytulosten epäonnistumisen vuoksi

Voit määrittää [liiketapahtumia](../../fin-ops-core/dev-itpro/business-events/home-page.md) hälytyksien toimitusta varten käsittelytulosten epäonnistumisen vuoksi. Valitse **Järjestelmän hallinta \> Asetukset \> Liiketoimintatapahtumat \> Liiketoimintatapahtumien luettelo** ja aktivoi liiketoimintatapahtuma, jonka nimi on *Sanoman käsittelijä - sanoma käsitelty*.

Osana aktivointiprosessia järjestelmä pyytää määrittämään, koskeeko tapahtuma vain yhtä yritystä vai kaikkia yrityksiä. Näyttöön tule myös kehote määrittää **Päätepisteen nimi** -arvo. Tämä arvo on määritettävä ensin.

> [!NOTE]
> Jos **Kun liiketoimintatapahtuma ilmenee** -kentän arvona on *Microsoft Power Automate* (eikä esimerkiksi *HTTPS*), **Päätepisteen nimi** -arvo luodaan automaattisesti Supply Chain Managementissa *Microsoft Power Automate* -määrityksen mukaisesti.
