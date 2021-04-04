---
title: Hälytysten yleiskuvaus
description: Tämä ohjeaihe sisältää yleisiä tietoja hälytyksistä. Saat hälytysten avulla tietoja tapahtumista, joita haluat seurata työpäivän aikana.
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: e57b065dc1a2c0db593b38106f4391e281feb1e6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565035"
---
# <a name="alerts-overview"></a>Hälytysten yleiskuvaus

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a>Tietoja hälytyksistä
Hälytykset muodostavat kriittisten tapahtumien ilmoitusjärjestelmän järjestelmässä. Saat hälytysten avulla tietoja tapahtumista, joita haluat seurata työpäivän aikana. Voit luoda kätevästi oman hälytyssääntöjoukon, joilla saat hälytyksen myöhässä olevista lähetyksistä, poistetuista tilauksista, hintojen muutoksista ja muista reagointia vaativista tapahtumista.

Toiminnanohjausratkaisussa (ERP) on useita tyypillisiä skenaarioita, joissa hälytystoimintoa voi käyttää. Seuraavassa on muutamia esimerkkejä.

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a>Skenaario 1: Hälytyssäännön luonti uusia myyntitilauksia varten

1. Avaa **Kaikki myyntitilaukset** -sivu.
2. Valitse **Asetukset**-välilehden **Jaa**-ryhmän toimintoruudussa **Luo mukautettu hälytys**.
3. Valitse **Hälytä seuraavissa tilanteissa** -pikavälilehden **Luo hälytyssääntö** -valintaikkunan **Tapahtuma**-kentässä **Tietue on luotu**.

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a>Tilanne 2: Hälytyssäännön luonti toimituspäivän lykkäystä varten

1. Avaa **Kaikki ostotilaukset** -sivu.
2. Pääset käyttämään ostotilauksen tietoja valitsemalla ostotilauksen tunnuksen.
3. Laajenna **Ostotilauksen otsikko** -pikavälilehti.
4. Valitse **Asetukset**-välilehden **Jaa**-ryhmän toimintoruudussa **Luo mukautettu hälytys**.
5. Valitse **Hälytä seuraavissa tilanteissa** -pikavälilehden **Luo hälytyssääntö** -valintaikkunan **Kenttä**-kentässä **Toimituspäivämäärä**.
6. Valitse **Tapahtuma**-kentässä **on siirretty**.
    
Kun **Luo hälytyssääntö** -valintaikkuna suljetaan, sääntö näkyy **Ylläpidä hälytyssääntöjä** -sivulla. Voit päivittää aiemmin luotuja hälytyssääntöjä **Ylläpidä hälytyssääntöjä** -sivulla. Voit esimerkiksi muokata tapahtuman käynnistimiä, päivittää ilmoituksia ja päivittää voimassaolon päättymispäivät. Voit avata **Ylläpidä hälytyssääntöjä** -sivun toimintoruudun **Asetukset**-välilehden **Hälytys**-painiketta.

## <a name="what-occurs-when-an-alert-rule-is-created"></a>Mitä tapahtuu, kun luodaan hälytyssääntö?

Kun luot hälytyssääntöjä, voit liittää ennalta määritetyn tapahtuman tiettyyn kenttään. Esimerkiksi kentässä määritetty päivämäärä saavutetaan tai kentän sisältöä muutetaan. Vaihtoehtoisesti voit liittää tapahtuman tietyn sivun tietueisiin. Esimerkiksi tietue on luotu tai tietue on poistettu.

Kun valittu tapahtuma tapahtuu sivun kentässä tai tietueessa, sinulle lähetetään hälytys. Kun luot esimerkiksi säännön, jossa tietyn ostotilausrivin **Toimituspäivämäärä**-kenttä liitetään **erääntymisestä on aikaa** -tapahtumaan. Määritit aikavälin viideksi päiväksi. Tässä tapauksessa hälytys lähetetään viisi päivää ostotilausrivin toimituspäivän jälkeen.

Voit myös tarkentaa hälytyssääntöjä määrittämällä ehdot. Voit saada hälytyksiä esimerkiksi ostotilauksista, jotka luodaan tietyille toimittajatileille.

## <a name="preparing-for-an-alert"></a>Valmistellaan hälytystä

Ennen hälytyssäännön luomista on päätettävä, milloin ja missä tilanteissa haluat vastaanottaa hälytyksiä. Kun tiedät, mistä tapahtumasta haluat ilmoituksen, voit etsiä sivun, jossa kyseisen tapahtuman aiheuttavat tiedot näkyvät. Tapahtuma voi olla tietty päivämäärä tai tapahtuva muutos. Sinun onkin etsittävä sivu, jossa päivämäärä on määritetty tai jossa muuttuva kenttä tai luotu uusi tietue tulee näkyviin. Kun nämä tiedot ovat valmiina, voit luoda hälytyssäännön.

## <a name="components-of-an-alert-rule"></a>Hälytyssäännön osat

Hälytyssäännöllä on viisi osaa:

- **Tapahtuma** – Tapahtuma, joka käynnistää hälytyssäännön, voi olla tietty päivämäärä tai tapahtuva muutos. Voit määrittää tapahtumia **Luo hälytyssääntö** -valintaikkunan **Lähetä sähköpostihälytykset työn tilan muutoksista** -pikavälilehdessä.
- **Ehto** – Voit valita **Luo hälytyssääntö** -valintaikkunan **Hälytä seuraavasta:** -pikavälilehdessä ehtojen laajuuden. Näin voit määrittää, milloin saat tapahtumista hälytyksen. Voit käyttää sääntöä joko vain nykyisessä tietueessa tai kaikissa sivulla näkyvissä tietueissa. Jos sääntö koskee kaikkia yrityksiä, voit määrittää **Organisaationlaajuinen**-asetuksen arvoksi **Kyllä**.
- **Päättymissääntö** – **Luo hälytyssääntö** -valintaikkunan **Hälytä tähän asti** -pikavälilehdessä voit määrittää, miten kauan hälytyssääntö on aktiivinen.
- **Sisältö** – Voit määrittää **Luo hälytyssääntö** -valintaikkunan **Hälytystapa**-pikavälilehdessä hälytykselle aihe- ja sanomatekstin.
- **Käyttäjä** – Määritä **Luo hälytyssääntö** -valintaikkunan **Hälytys - kuka** -pikavälilehdessä käyttäjä, joka vastaanottaa hälytyssanoman. Käyttäjätunnus valitaan oletusarvoisesti.

    > [!NOTE]
    > Tämä asetus on rajoitettu organisaation järjestelmänvalvojien käyttöön.

## <a name="videos"></a>Videot

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a>Suodatettujen tietojen valvonta hälytysten avulla

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

[Suodatettujen tietojen valvonta hälytysten avulla](https://youtu.be/ZYKMcv6kl9s) -video (mainittu edellä) sisältyy [Finance and Operations -toistoluetteloon](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on katsottavissa YouTubessa.

### <a name="alert-rule-options"></a>Hälytyssääntövaihtoehdot

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

[Hälytyssääntövaihtoehdot](https://youtu.be/cpzimwOjicM) -video (edellä mainittu) sisältyy [Finance and Operations -toistoluetteloon](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on katsottavissa YouTubessa.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]