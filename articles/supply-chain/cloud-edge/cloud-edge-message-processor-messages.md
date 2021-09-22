---
title: Sanoman käsittelijän sanomat
description: Tässä ohjeaiheessa on tietoja sanoman käsittelijän sanomaominaisuudesta scale unitin kuormitusta varten.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 685c8951b7c0d8524091cf06306388736d894f58
ms.sourcegitcommit: a21166da59675e37890786ebf7e0f198507f7c9b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/03/2021
ms.locfileid: "7471641"
---
# <a name="message-processor-messages"></a>Sanoman käsittelijän sanomat

[!include [banner](../includes/banner.md)]

Sanoman käsittelijän sanomia käytetään, kun suoritetaan pilvi- ja reunapalvelujen scale uniteja [valmistuksen kuormituksille](cloud-edge-workload-manufacturing.md) ja [varaston hallinnan kuormituksille](cloud-edge-workload-warehousing.md).

Keskuksen ja yksiköiden käyttöönottoympäristöjen välillä vaihdetaan paljon tietoja, jotta ne voidaan pitää synkronoituina, mutta *sanoman käsittelijä* käsittelee vain muutamia näistä tietojen vaihdoista. Voit tarkastella sanoman käsittelijän käsittelemiä sanomia valitsemalla **Järjestelmänvalvonta > Sanoman käsittelijä > Sanoman käsittelijän sanomat**.

## <a name="message-grid-columns-and-filters"></a>Sanomaruudukon sarakkeet ja suodattimet

**Sanoman käsittelijän sanomat** -sivun yläosan kenttien avulla voit etsiä haluamiasi sanomia. Useimmat näistä suodattimista vastaavat sanomaruudukon sarakeotsikoita. Käytettävissä ovat seuraavat suodattimet ja sarakeotsikot:

- **Sanomatyyppi** – Määrittää sanoman tyypin.
- **Sanomajono** – Määrittää sen jonon nimen, jossa sanoma käsitellään. Käytettävissä ovat seuraavat jonot:
  - *Skaalausyksiköstä keskukseen*
  - *Varastonohjausasteikon yksikkö*
  - *Tuotannonohjausasteikon yksikkö*
- **Sanoman tila** – Määrittää sanoman tilan. Käytössä ovat seuraavat tilat:
  - *Jonossa* – Sanoma on valmis sanoman käsittelijän käsiteltäväksi.
  - *Käsitelty* – Sanoman käsittely sanoman käsittelijän toimesta onnistui.
  - *Peruutettu* – Sanoma käsiteltiin, mutta käsittely epäonnistui.
- **Sanoman sisältö** – Tämän suodattimen avulla voit tehdä tekstihakuja sanoman sisällöstä. (Sanoman sisältöä ei näytetä ruudukossa.) Suodatin käsittelee useimmat erikoissymbolit (kuten ”-”) välilyönteinä ja käsittelee kaikkia välilyöntimerkkejä TAI-totuusarvo-operaattoreina. Tämä tarkoittaa esimerkiksi sitä, että jos haet tiettyä `journalid`-arvoa, joka on sama kuin "USMF-123456", järjestelmä etsii kaikki sanomat, joissa on "USMF" tai "123456", joka on todennäköisesti pitkä luettelo. Siksi olisi parempi syöttää vain "123456" siksi, että se palauttaa yksityiskohtaisia tuloksia.

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a>Sanoman tyypin esimerkki: Varasto-oikaisun taloudellisen päivityksen pyytäminen

Esimerkiksi **Sanoman tyyppi** *Varasto-oikaisun taloudellisen päivityksen pyytäminen* -kohdan avulla luodaan ja kirjataan keskukseen kirjauskansio, kun työntekijä [rekisteröi varaston oikaisun](cloud-edge-warehouse-inventory-adjustment.md) varastosovellusta käyttämällä scale unitin varastonhallinnan kuormitusta varten. Koska tämä prosessi on peräisin yksiköstä, **Sanomajono**-kenttä näyttää arvon *Scale unitista keskukseen*.

Tälle sanomatyypille scale unitin kuormitus kirjaa sanoman osana varastosovelluksen varasto-oikaisutoimintoa. Tämän jälkeen sanomatiedot siirretään keskukseen samassa prosessissa, kuin mitä käytetään [Commerce Data Exchange -arkkitehtuurissa](../../commerce/commerce-architecture.md). Sanoma päivitetään niin, että siinä näkyy **Sanoman tilana** *Jonossa*. Sanoman käsittelijä yrittää käsitellä sanomaa ja päivittää **Sanoman tilaksi** *Käsitelty*, jos käsittely onnistui, tai *Peruutettu*, jos epäonnistui.

## <a name="view-the-message-log-message-content-and-details"></a>Sanomalokin, sanomasisällön ja tietojen tarkasteleminen

Voit etsiä yksityiskohtaisia tietoja sanomasta valitsemalla sen ruudukosta ja avaamalla sitten **Loki**- tai **Sanoman sisältö** -välilehdet sanomaruudukosta, jossa näkyy kukin käsittelytapahtuma.

**Sanoman sisältö** riippuu **Sanoman tyypistä**, minkä takia sen tekstipituus vaihtelee. Yleensä sanoman sisältö alkaa **{** ja päättyy **}** ja välissä on kenttien nimet, kuten `journalId` ja sen jälkeen **:** sekä arvo, kuten *USMF-123456*.

**Loki**-välilehden työkalurivi sisältää seuraavat painikkeet:

- **Loki** – Näyttää käsittelytulokset. Tämä auttaa erityisesti ymmärtämään syitä, joiden vuoksi sanomien käsittely epäonnistui ja **Käsittelyn tulos** on *Epäonnistui*.
- **Myyntirakenne** – Useita sanomankäsittelytoimintoja voi suorittaa saman eräprosessin osana. Valitsemalla tämän painikkeen voit tarkastella näitä yksityiskohtaisia tietoja. Voit esimerkiksi nähdä, onko olemassa riippuvuuksia, jotka edellyttävät, että järjestelmä käsittelee tietyt sanomat tietyssä järjestyksessä.

## <a name="message-processor-batch-job"></a>Sanoman käsittelijän erätyö

Suoritettaessa jaettua hybriditopologiaa, jossa on scale uniteja *Sanoman käsittelijä* -erätyö käynnistyy automaattisesti, kun uusi sanoma luodaan käsittelyä varten, joten tätä työtä ei tarvitse ajoittaa manuaalisesti.

Voit tarvittaessa käyttää erätyötä valitsemalla **Järjestelmänvalvonta > Sanoman käsittelijä > Sanoman käsittelijä**.

## <a name="manually-process-or-cancel-a-message"></a>Sanoman käsitteleminen manuaalisesti tai sen peruuttaminen

Voit tarvittaessa käsitellä tai peruuttaa sanoman manuaalisesti sen nykyisen tilan mukaan. Voit tehdä tämän valitsemalla sanoman ruudukossa ja valitsemalla sitten toimintoruudusta **Käsittele** tai **Peruuta**.

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Liiketapahtumien määrittäminen hälytyksien toimitusta varten käsittelytulosten epäonnistumisen vuoksi

Se lisäksi, että voit suodattaa **Sanoman tila** -arvon *Peruutettu* epäonnistui-sanomien kyselemiseksi, voi määrittää [Liiketoimintatapahtumat](../../fin-ops-core/dev-itpro/business-events/home-page.md) keskuksessa ja saada ilmoituksen epäonnistuneista käsittelytuloksista. Voit tehdä tämän aktivoimalla yritystapahtuman nimeltä *Sanoman käsittelijän sanoma käsitelty* **Liiketoimintatapahtumien luettelo** -sivulla (**Järjestelmänvalvonta > Asetukset > Liiketoimintatapahtumat > Liiketoimintatapahtumien luettelo**).

Osana aktivointiprosessia sinua ohjataan määrittämään, koskeeko tapahtuma vain yhtä vai kaikkia yrityksiä sekä antamaan **Päätepisteen nimi**, on määritettävä ensin.

>[!NOTE]
> Jos **Kun liiketoimintatapahtuma ilmenee** -kohdan arvona on *Microsoft Power Automate* (eikä esimerkiksi *HTTPS*), **Päätepisteen nimi** luodaan automaattisesti Supply Chain Managementissa *Microsoft Power Automate* -määrityksen mukaisesti.

### <a name="microsoft-power-automate-example"></a>Microsoft Power Automate -esimerkki

Tässä esimerkissä **Kun liiketoimintatapahtuma ilmenee** -arvon käyttö *Microsoft Power Automate* n kanssa lähettää InfoLog-sanomia ja hyperlinkkejä sisältäviä sähköpostiviestejä **Sanoman käsittelijän sanomat** -sivun avaamiseksi tietylle epäonnistuneelle sivulle keskuksen käyttöönotossa. Tarvittaessa voit lisätä logiikkaa, jonka avulla ilmoitukset lähetetään rinnakkain eri kanavien avulla ja ohjata vastaanottajia tapahtumatietojen perusteella.

1. Kohdassa [Power Automate](https://preview.flow.microsoft.com) luo uusi automaattinen pilvityönkulku työnkulun käynnistimelle **Kun liiketoimintatapahtuma ilmenee - Fin & Ops App (Dynamics 365)** ja sen jälkeen **Jäsennä JSON**- ja **Lähetä sähköpostiviesti** -vaiheet seuraavassa kuvassa esitetyllä tavalla.

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automaten automaattinen pilvityönkulku.":::

1. **Kun liiketoimintatapahtuma ilmenee** -vaiheessa voit etsiä tai syöttää keskuksen **Esiintymä**-kohdan, sitten **Luokka** ja sitten **Liiketoimintatapahtuma** *Sanoman käsittelijän sanoma käsitelty* seuraavassa kuvassa esitetyllä tavalla.

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automaten Kun liiketoimintatapahtuma ilmenee -vaihe.":::

1. **Jäsennä JSON** -vaiheessa anna **Rakenne**, joka määrittää laajennetut kentät. Voit käyttää *Lataa rakenne*-vaihtoehtoa **Liiketoimintatapahtumien luettelo** -sivulla Supply Chain Managementissa tai aloittaa liittämällä esimerkkirakenteen tekstin. Tämä esimerkkiteksti annetaan seuraavan kuvan jälkeen.

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automaten Jäsennä JSON -vaihe.":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. Voit valita **Lähetä sähköpostiviesti** -kohdasta yksittäiset kentät tai aloittaa liittämällä sähköpostin perustekstiesimerkin **Perusteksti**-kenttään. Tämä esimerkki annetaan seuraavan kuvan jälkeen.

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automaten Lähetä sähköpostiviesti -vaihe.":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. Kun tallennat liiketoimintatapahtuman, se aktivoidaan automaattisesti ja sitä voidaan käyttää osana Supply Chain Managementia.
