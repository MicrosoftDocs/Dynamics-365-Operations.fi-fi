---
title: "Hälytyssääntöjen luominen"
description: "Tässä ohjeaiheessa on tietoja hälytyksistä. Siinä myös selitetään, miten luodaan sellainen hälytyssääntö, joka ilmoittaa tapahtumista, kuten saapuvasta päivämäärästä tai tapahtuvasta muutoksesta."
author: tjvass
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 78e1e6f7be04e1d4fecae080cbd4a285358590fb
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="create-alert-rules"></a>Hälytyssääntöjen luominen

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>Aloittaminen
Ennen hälytyssäännön luomista on päätettävä, milloin ja missä tilanteissa haluat vastaanottaa hälytyksiä. Kun tiedät, mistä tapahtumasta haluat ilmoituksen, voit etsiä Microsoft Dynamics 365 for Finance and Operationsissa sivun, jossa kyseisen tapahtuman aikaansaavat tiedot näkyvät. Tapahtuma voi olla tietty päivämäärä tai tapahtuva muutos. Sinun onkin etsittävä sivu, jossa päivämäärä on määritetty tai jossa muuttuva kenttä tai luotu uusi tietue tulee näkyviin. Kun nämä tiedot ovat valmiina, voit luoda hälytyssäännön.

Hälytyssääntöä luotaessa määritetään ehdot, joiden on toteuduttava ennen hälytyksen antamista. Tämä tarkoittaa, että tietty tapahtuma esiintyy ja tietyt ehdot täyttyvät samanaikaisesti. Tapahtuman esiintyessä järjestelmä aloittaa tarkistuksen Finance and Operationsissa määritettyjen ehtojen mukaisesti.

## <a name="events"></a>Tapahtumat
Tapahtuma, joka käynnistää hälytyssäännön, voi olla tietty päivämäärä tai tapahtuva muutos. Käynnistää tapahtumat, jotka on määritetty **Luo hälytyssääntö** -valintaikkunan **Hälytä seuraavissa tilanteissa** -pikavälilehdessä. Tietyn kentän käytettävissä olevat tapahtumat määräytyvät valitun käynnistimen mukaan.

Jos esimerkiksi määrität hälytyssäännön **Alkamispäivä**-kenttään, eräpäivän tapahtumat soveltuvat. **Erääntymisaika**-tapahtumatyyppi on tämän vuoksi käytettävissä kyseisessä kentässä. Eräpäivään perustuva tapahtuma ei kuitenkaan sovellu esimerkiksi **Kustannuspaikka**-kentälle. **Erääntymisaika**-tapahtumatyyppi ei ole tämän vuoksi käytettävissä. Sen sijaan käytettävissä on **on muuttunut** -tapahtumatyyppi.

## <a name="event-types"></a>Tapahtumatyypit
Mahdollisia tapahtumatyyppejä on kolme:

- **Luomis- ja poistamistyyppiset tapahtumat** – Nämä tapahtumat käynnistävät hälytyksen, kun tietue luodaan tai poistetaan.
- **Päivitystyypin tapahtumat** – Nämä tapahtumat käynnistävät hälytyksen, kun tietyn kentän tiedot muuttuvat.
- **Eräpäivätyypin tapahtumat** – Nämä tapahtumat käynnistävät hälytyksen tiettynä päivämääränä.
    
Käyttäjä voi käynnistää muutokset. Esimerkiksi käyttäjä muuttaa ostotilauksen toimituspäivää. Vaihtoehtoisest muutokset voivat tapahtua prosessin osana. Esimerkiksi sivun **Tila**-kenttä muuttuu niin, että se vastaa järjestelmän eri prosessien elinkaarta.

## <a name="conditions"></a>Ehdot
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
Määritä **Luo hälytyssääntö** -valintaikkunan **Hälytystapa**-pikavälilehdessä käyttäjä, joka vastaanottaa hälytyssanomat. Käyttäjätunnus valitaan oletusarvoisesti. Tämä asetus on rajoitettu organisaation järjestelmänvalvojien käyttöön.

## <a name="create-an-alert-rule"></a>Luo hälytyssääntö
1. Avaa sivu, joka sisältää valvottavat tiedot.
2. Valitse **Asetukset**-välilehden **Jaa**-ryhmän toimintoruudussa **Luo hälytyssääntö**.
3. Valitse **Kenttä**-kentän **Luo hälytyssääntö** -valintaikkunassa seurattava kenttä.
4. Valitse **Tapahtuma**-kentässä tapahtuman tyyppi.
5. Valitse **Hälytä seuraavasta:** -pikavälilehdessä vaihtoehto.
6. Jos haluat hälytyssäännön poistuvan käytöstä tiettynä päivämääränä, valitse **Hälytä tähän asti** -pikavälilehdessä päättymispäivämäärä.
7. Hyväksy **Hälytystapa**-pikavälilehden **Aihe**-kentässä sähköpostiviestin aiheen oletusotsikko tai kirjoita uusi aihe. Tekstiä käytetään otsikkona sähköpostiviestissä jonka saat, kun hälytys laukaistaan.
8. Valitse **Sanoma**-kentässä valinnainen sanoma. Tämä teksti on sanoma, jonka saat, kun hälytys laukaistaan.
9. Tallenna asetukset ja luo hälytyssääntö valitsemalla **OK**.

