---
title: Hälytyssääntöjen luominen
description: Tässä artikkelissa on tietoja hälytyksistä ja siitä, miten hälytyssääntö luodaan.
author: RichdiMSFT
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: f523680f3d71ffd75c6cd2df284d2fd3610cef96
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853614"
---
# <a name="create-alert-rules"></a>Hälytyssääntöjen luominen

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>Aloittaminen

Ennen hälytyssäännön luomista on päätettävä, milloin ja missä tilanteissa haluat vastaanottaa hälytyksiä. Kun tiedät, mistä tapahtumasta haluat ilmoituksen, voit etsiä sivun, jossa kyseisen tapahtuman aiheuttavat tiedot näkyvät. Tapahtuma voi olla tietty päivämäärä tai tapahtuva muutos. Sinun onkin etsittävä sivu, jossa päivämäärä on määritetty tai jossa muuttuva kenttä tai luotu uusi tietue tulee näkyviin. Kun nämä tiedot ovat valmiina, voit luoda hälytyssäännön.

Hälytyssääntöä luotaessa määritetään ehdot, joiden on toteuduttava ennen hälytyksen antamista. Ehdot tarkoittavat periaatteessa sitä, että tietty tapahtuma esiintyy ja tietyt ehdot täyttyvät samanaikaisesti. Tapahtuman esiintyessä järjestelmä suorittaa tarkistuksen määritettyjen ehtojen mukaisesti.

## <a name="ensure-the-alert-batch-jobs-are-running"></a>Hälytyksen erätöiden suorittamisen varmistaminen

Tietojen muuttamisen erätöiden ja eräpäivän hälytysten on oltava käynnissä, jotta hälytyksen ehdot voidaan käsitellä ja ilmoitukset lähettää. Jos haluat suorittaa erätyöt, siirry kohtaan **Järjestelmän hallinta** > **Kausittaiset tehtävät** > **Hälytykset** ja lisää uusi erätyö **Muutokseen perustuvat hälytykset** ja/tai **Eräpäivän hälytykset**. Jos tarvitaan pitkään ja usein suoritettava erätyö, valitse **Toistuvuus** ja määritä **Ei päättymispäivää** -kohdan **Toistumisen kuvio** -kohdan arvoksi **Minuutit** ja **Määrä**-kohdan arvoksi **1**.

## <a name="events"></a>Tapahtumat

Tapahtuma, joka käynnistää hälytyssäännön, voi olla tietty päivämäärä tai tapahtuva muutos. Käynnistää tapahtumat, jotka on määritetty **Luo hälytyssääntö** -valintaikkunan **Hälytä seuraavissa tilanteissa** -pikavälilehdessä. Tietyn kentän käytettävissä olevat tapahtumat määräytyvät valitun käynnistimen mukaan.

Jos esimerkiksi määrität hälytyssäännön **Alkamispäivä**-kenttään, eräpäivän tapahtumat soveltuvat. `is due in` -tapahtumatyyppi on tämän vuoksi käytettävissä kyseisessä kentässä. Eräpäivään perustuva tapahtuma ei kuitenkaan sovellu esimerkiksi **Kustannuspaikka**-kentälle. `is due in` -tapahtumatyyppi ei ole tämän vuoksi käytettävissä. Käytettävissä on sen sijaan `has changed` -tapahtumatyyppi.

## <a name="event-types"></a>Tapahtumatyypit

Mahdollisia tapahtumatyyppejä on kolme:

- **Luomis- ja poistamistyyppiset tapahtumat** – Nämä tapahtumat käynnistävät hälytyksen, kun tietue luodaan tai poistetaan.
- **Päivitystyypin tapahtumat** – Nämä tapahtumat käynnistävät hälytyksen, kun tietyn kentän tiedot muuttuvat.
- **Eräpäivätyypin tapahtumat** – Nämä tapahtumat käynnistävät hälytyksen tiettynä päivämääränä.
    
Käyttäjä voi käynnistää muutokset. Esimerkiksi käyttäjä muuttaa ostotilauksen toimituspäivää. Vaihtoehtoisest muutokset voivat tapahtua prosessin osana. Esimerkiksi sivun **Tila**-kenttä muuttuu niin, että se vastaa järjestelmän eri prosessien elinkaarta.

## <a name="conditions"></a>Olosuhteet

Voit käyttää **Luo hälytyssääntö** -valintaikkunan **Hälytä seuraavasta:** -pikavälilehden ehtoja tapahtumien hälytysten ohjauksessa.

Voit esimerkiksi määrittää, että järjestelmä lähettää hälytyksen ostotilausten tilojen muuttuessa vain silloin, kun tila vastaa tiettyjä ehtoja. Haluat ilmoituksen etenkin silloin, kun ostotilauksen tilaksi määritetään **Vastaanotettu**. Tilan muutos on hälytyksen laukaiseva tapahtuma.

Seuraavaksi päätetään, mistä ostotilauksista haluat saada hälytyksen. Voit esimerkiksi valita yhden seuraavista vaihtoehdoista. Nämä asetukset määrittävät hälytyssäännön ehdot.

- **Nykyinen valittu tietue** – Saat hälytyksen, kun tietyn ostotilauksen tilaksi tulee **Vastaanotettu**.
- **Kaikki tietueet** – Saat hälytyksen, kun aktiivisen sivunäkymän nimikkeen ostotilauksen tila muuttuu. Voit luoda tietylle tietuejoukolle sääntöjä sivulla olevien suodatuksen lisäasetusten avulla. Voit esimerkiksi luoda hälytyksen, joka käynnistetään tietyn asiakasryhmän asiakkaiden kaikille ostotilauksille.
    
## <a name="expiry-of-rule"></a>Päättymissääntö

Määritä **Luo hälytyssääntö** -valintaikkunan **Hälytä tähän asti:** -pikavälilehdessä, miten kauan hälytyssääntö on aktiivinen.

## <a name="alert-contents"></a>Hälytyksen sisältö

Määritä **Luo hälytyssääntö** -valintaikkunan **Hälytystapa**-pikavälilehdessä hälytyksen sanomalle aihe- ja sanomateksti.

## <a name="user-id"></a>Käyttäjätunnus

Määritä **Luo hälytyssääntö** -valintaikkunan **Hälytystapa**-pikavälilehdessä käyttäjä, joka vastaanottaa hälytyssanomat. Käyttäjätunnus valitaan oletusarvoisesti. Vain organisaation järjestelmänvalvoja voi vaihtaa hälytyksen saavaa käyttäjää.

## <a name="alerts-as-business-events"></a>Hälytykset liiketoimintatapahtumina

Hälytyksiä voidaan lähettää ulkoisesti liiketoimintatapahtuman kehyksen avulla. Kun luot hälytyksen, määritä **Organisaation laajuinen** -kohdan arvoksi **Ei** ja **Lähetä ulkoisesti** -kohdan arvoksi **Kyllä**. Kun hälytys käynnistää liiketoimintatapahtuman, voit käynnistää Power Automaten luoman työnkulun käyttämällä **Kun liiketoimintatapahtuma ilmenee** -käynnistimen Finance and Operations -yhdistimessä tai lähettää tapahtuman liiketoimintatapahtumien päätepisteeseen **Liiketoimintatapahtumien luettelo** -kohdan avulla.

## <a name="create-an-alert-rule"></a>Luo hälytyssääntö

0. Hälytyksen erätöiden suorittamisen varmistaminen (katso yllä).
1. Avaa sivu, joka sisältää valvottavat tiedot.
2. Valitse **Asetukset**-välilehden **Jaa**-ryhmän toimintoruudussa **Luo hälytyssääntö**.
3. Valitse **Kenttä**-kentän **Luo hälytyssääntö** -valintaikkunassa seurattava kenttä.
4. Valitse **Tapahtuma**-kentässä tapahtuman tyyppi.
5. Valitse **Hälytä seuraavasta:** -pikavälilehdessä haluttu vaihtoehto. Jos haluat lähettää hälytyksen liiketoimintatapahtumana, määritä **Organisaation laajuinen** -arvoksi **Ei**.
6. Jos haluat hälytyssäännön poistuvan käytöstä tiettynä päivämääränä, valitse **Hälytä tähän asti** -pikavälilehdessä päättymispäivämäärä.
7. Hyväksy **Hälytystapa**-pikavälilehden **Aihe**-kentässä sähköpostiviestin aiheen oletusotsikko tai kirjoita uusi aihe. Tekstistä tulee otsikko sähköpostiviestissä jonka saat, kun hälytys laukaistaan. Jos haluat lähettää hälytyksen liiketoimintatapahtumana, määritä **Lähetä ulkoisesti** -kohdan arvoksi **Kyllä**.
8. Valitse **Sanoma**-kentässä valinnainen sanoma. Tekstistä tulee sanoma, jonka saat, kun hälytys käynnistyy.
9. Tallenna asetukset ja luo hälytyssääntö valitsemalla **OK**.

## <a name="limitations-and-workarounds"></a>Rajoitukset ja ratkaisuehdotukset

### <a name="workaround-for-creating-alerts-for-the-secondary-data-sources-of-a-form"></a>Ratkaisuehdotus lomakkeen toissijaisten tietolähteiden hälytysten luontia varten
Hälytyksiä ei voi luoda joillekin lomakkeiden toissijaisille tietolähteille. Kun esimerkiksi asiakkaan tai toimittajan kirjausprofiililomakkeessa luodaan hälytyksiä, käytettävissä on vain otsikon (CustLedger tai VendLedger) kentät eikä dimensiotilit. Tämän rajoituksen ratkaisuehdotus on avata kyseinen taulukko ensisijaisena tietolähteenä käyttämällä **SysTableBrowser**-lomaketta. 
1. Avaa taulukko **SysTableBrowser**-lomakkeessa.
    ```
        https://<EnvironmentURL>/?cmp=USMF&mi=SysTableBrowser&TableName=<TableName>
    ```
2. Luo hälytys SysTableBrowser-lomakkeesta.

### <a name="change-based-alerts-do-not-work-for-batch-status-changes"></a>Muutoksiin perustuvat hälytykset eivät toimi, jos erän tila muuttuu
Muutokseen perustuvat hälytykset eivät toimi erän tilan muutuessa, koska se on pois käytöstä suorituskykysyistä. Sen sijaan on määritettävä **Erähälytykset**-toiminto. Lisätietoja on kohdassa [Hälytysten määrittäminen eräkäsittelyn parannettuihin lomakkeisiin](../../dev-itpro/sysadmin/alerts.md#set-up-alerts-for-batch-enhanced-forms).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]