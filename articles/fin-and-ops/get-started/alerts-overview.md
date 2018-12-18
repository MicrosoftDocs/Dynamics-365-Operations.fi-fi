---
title: "Hälytykset"
description: "Tässä ohjeaiheessa on yleisiä tietoja Microsoft Dynamics 365 for Finance and Operationsin hälytyksistä. Saat hälytysten avulla tietoja tapahtumista, joita haluat seurata työpäivän aikana."
author: tjvass
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 38309e986c1d284ed63be760745b20a5415adb4c
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="alerts"></a>Hälytykset

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a>Tietoja hälytyksistä
Hälytykset muodostavat tärkeiden tapahtumien ilmoitusjärjestelmän Microsoft Dynamics 365 for Finance and Operations -sovelluksessa. Saat hälytysten avulla tietoja tapahtumista, joita haluat seurata työpäivän aikana. Voit luoda kätevästi oman hälytyssääntöjoukon, joilla saat hälytyksen myöhässä olevista lähetyksistä, poistetuista tilauksista, hintojen muutoksista ja muista reagointia vaativista tapahtumista.

Toiminnanohjausratkaisussa (ERP) on useita tyypillisiä skenaarioita, joissa Finance and Operations -sovelluksen hälytystoimintoa voi käyttää. Seuraavassa on muutamia esimerkkejä.

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

Ennen hälytyssäännön luomista on päätettävä, milloin ja missä tilanteissa haluat vastaanottaa hälytyksiä. Kun tiedät, mistä tapahtumasta haluat ilmoituksen, voit etsiä Finance and Operationsissa sivun, jossa kyseisen tapahtuman aikaansaavat tiedot näkyvät. Tapahtuma voi olla tietty päivämäärä tai tapahtuva muutos. Sinun onkin etsittävä sivu, jossa päivämäärä on määritetty tai jossa muuttuva kenttä tai luotu uusi tietue tulee näkyviin. Kun nämä tiedot ovat valmiina, voit luoda hälytyssäännön.

## <a name="components-of-an-alert-rule"></a>Hälytyssäännön osat

Hälytyssäännöllä on viisi osaa:

- **Tapahtuma** – Tapahtuma, joka käynnistää hälytyssäännön, voi olla tietty päivämäärä tai tapahtuva muutos. Voit määrittää tapahtumia **Luo hälytyssääntö** -valintaikkunan **Lähetä sähköpostihälytykset työn tilan muutoksista** -pikavälilehdessä.
- **Ehto** – Voit valita **Luo hälytyssääntö** -valintaikkunan **Hälytä seuraavasta:** -pikavälilehdessä ehtojen laajuuden. Näin voit määrittää, milloin saat tapahtumista hälytyksen. Voit käyttää sääntöä joko vain nykyisessä tietueessa tai kaikissa sivulla näkyvissä tietueissa. Jos sääntö koskee kaikkia yrityksiä, voit määrittää **Organisaationlaajuinen**-asetuksen arvoksi **Kyllä**.
- **Päättymissääntö** – **Luo hälytyssääntö** -valintaikkunan **Hälytä tähän asti** -pikavälilehdessä voit määrittää, miten kauan hälytyssääntö on aktiivinen.
- **Sisältö** – Voit määrittää **Luo hälytyssääntö** -valintaikkunan **Hälytystapa**-pikavälilehdessä hälytykselle aihe- ja sanomatekstin.
- **Käyttäjä** – Määritä **Luo hälytyssääntö** -valintaikkunan **Hälytys - kuka** -pikavälilehdessä käyttäjä, joka vastaanottaa hälytyssanoman. Käyttäjätunnus valitaan oletusarvoisesti.

    > [!NOTE]
    > Tämä asetus on rajoitettu organisaation järjestelmänvalvojien käyttöön.

## <a name="email-notifications-from-alerts"></a>Sähköposti-ilmoitukset hälytyksistä

Sähköposti-ilmoituksia hälytyksistä ei ole vielä otettu käyttöön. Se otetaan käyttöön myöhemmässä päivityksessä.

