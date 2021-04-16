---
title: Määritä tytäryhtiö konsolidointia varten
description: Tässä ohjeaiheessa kerrotaan, miten konsolidointiyritysten tilikarttoja käsitellään.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 15050310f355ece683b00a00be9552d32aded17b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832847"
---
# <a name="set-up-a-subsidiary-legal-entity-for-consolidation"></a>Määritä tytäryhtiö konsolidointia varten

[!include [banner](../includes/banner.md)]

Menetelmä, jolla tytäryhtiön tilit valmistellaan konsolidointia varten, määräytyy osittain sen mukaan, miten paljon tytäryhtiön tilikartan rakenne vastaa konsolidointiyrityksen tilikarttaa.

Suorita ennen kauden sulkemiseen sisältyvän konsolidoinnin aloittamista kauden sulkemisen valmistelevat toimet, mutta älä sulje tytäryhtiön tilejä, ennen kuin konsolidointi on valmis. Lisätietoja kauden sulkemisesta on ohjeaiheissa [Kirjanpidon sulkeminen kauden lopussa](close-general-ledger-at-period-end.md) ja [Tilikauden sulkeminen](tasks/close-fiscal-year.md).

> [!NOTE]
>  On suositeltavaa käyttää Microsoft Dynamics 365 Financen Management Reporteria, kun haluat yhdistää useiden yrityksen taloudelliset tulokset konsolidointimuodossa. Management Reporterin avulla voit luoda konsolidointiraportteja eri yrityksille, tuoda konsolidointitietoja muista lähteistä Excelin avulla ja muuntaa summat miksi tahansa raportointivaluutaksi ilman, että konsolidointiprosessia tarvitsee suorittaa Dynamics 365 Financessa.

## <a name="map-subsidiary-main-accounts-to-consolidated-main-accounts"></a>Tytäryhtiön päätilien määrittäminen konsilidoituihin päätileihin

Jos tytäryhtiön tilikartta ei noudata konsolidointiyrityksen tilikarttaa, voit määrittää tytäryhtiön päätilit konsolidointiyrityksen päätileihin.

1. Siirry *tytäryhtiön yrityksessä* kohtaan **Kirjanpito \> Asetukset** \> **Tilikartta \> Tilikartta**.
2. Valitse tilikartta. Valitse **Päätilit**-pikavälilehdestä päätili ja valitse sitten **Muokkaa**.
3. Valitse kukin tytäryhtiön päätili, joka on määritettävä konsolidoituun päätiliin. Kirjoita **Yleiset**-pikavälilehden **Konsolidointitili**-kenttään se konsolidointiyrityksen tili, jonne tytäryhtiön valitun päätilin saldo tai tapahtumat on siirrettävä. Voit ilmoittaa saman konsolidoidun päätilin useille tytäryhtiöiden tilille.

    > [!NOTE]
    > Jos tytäryhtiön määritettyjen tilien päätilityypit eivät ole samoja kuin konsolidointiyrityksen tilien päätilityypit, niiden tilien arvot, joiden päätilityyppi on **Yhteensä**, korvataan konsolidoinnin aikana.

4. Valmistele taloushallinnon dimensioihin perustuvat konsolidointiyrityksen raportit ja tilinpäätökset. Seuraavien vaiheiden avulla voit yhdistää tytäryhtiön tileissä käytettävät taloushallinnon dimensiot konsolidointiyrityksen taloushallinnon dimensioihin:

    1. Siirry *tytäryhtiön yrityksessä* kohtaan **Kirjanpito \> Asetukset \> Taloushallinnon dimensiot \> Taloushallinnon dimensiot**, valitse taloushallinnon dimensio ja sitten **Taloushallinnon dimension arvot**.
    2. Valitse kondolisointiyrityksen eri taloushallinnon dimension arvoon määritettävä taloushallinnon dimension arvo.
    3. Ilmoita **Yleiset**-pikavälilehden **Ryhmädimensio**-kentässä konsolidointiyrityksen taloushallinnon dimensio. Tämä taloushallinnon dimensio määritetään konsolidoinnin aikana niihin tapahtumiin ja saldoihin, jotka käyttävät tytäryhtiössä valittua taloushallinnon dimensiota. Tässä ilmoitetun taloushallinnon dimension on oltava käytössä konsolidointiyrityksessä. Voit määrittää käytetyn taloushallinnon dimension ryhmän taloushallinnon dimensiona useisiin tytäryhtiön taloushallinnon dimensioihin.

5. Jos suoritat online-konsolidointia, varmista seuraavien vaiheiden avulla, että siirrot tapahtuvat haluamallasi tavalla:

    1. Siirry *konsolidoidussa yrityksessä* kohtaan **Kirjanpito** \> Kausittainen \> Konsolidoi \> Konsolidoi \[Vie kohteeseen\] avataksesi **Konsolidoi \[Online\]** -sivun.
    2. Valitse **Ehdot**-välilehden **Käytä konsolidointitiliä** -valintaruutu.
    3. Valitse sopivat taloushallinnon dimensiot **Taloushallinnon dimensiot** -välilehdestä.
    4. Kirjoita kunkin valitsemasi taloushallinnon dimension kohdalle numero **Segmenttien järjestys**-kenttään. Tämä numero osoittaa, missä järjestyksessä dimensiot pitäisi näyttää.

## <a name="maintain-the-same-chart-of-accounts-in-the-subsidiary-and-consolidated-legal-entities"></a>Saman tilikartan ylläpitäminen tytäryhtiössä ja konsolidointiyrityksessä

Tytäryhtiön päätileillä voi olla samat tilinumerot ja sama tilikartan rakenne kuin konsolidointiyrityksen päätileillä. Siinä tapauksessa tytäryhtiön päätilejä ei tarvitse määrittää manuaalisesti konsolidointitilien päätileihin.

Noudata seuraavia ohjeita ennen konsolidoinnin aloittamista.

1. Siirry *konsolidoidussa yrityksessä* kohtaan **Kirjanpito** \> Kausittainen \> Konsolidoi \> Konsolidoi \[Vie kohteeseen\] avataksesi **Konsolidoi \[Online\]** -sivun.
2. Valitse **Käytä konsolidointitiliä** -valintaruutu. Tapahtumat ja saldot siirtyvät oikealle tilille automaattisesti konsolidoinnin aikana.

> [!NOTE]
> Jos tilit eivät vastaa toisiaan, konsolidointi pysähtyy ja saat asiasta sanoman.

## <a name="create-a-chart-of-accounts-for-the-consolidated-legal-entity-based-on-an-existing-chart-of-accounts"></a>Konsolidointiyrityksen tilikartan luominen aiemmin luodun tilikartan perusteella

Voit tehdä konsolidoinnin, vaikka tilikartan tilejä ei ole vielä luotu konsolidointiyrityksessä.

- Jos olet suunnitellut konsolidointiyrityksessä käytettävän tilirakenteen, voit määrittää tytäryhtiön tilit tähän rakenteeseen.
- Jos et määritä tytäryhtiön tilejä, konsolidointiyrityksen tilit luodaan automaattisesti siirrettäessä tietoja konsolidointiyritykseen. Nämä tilit perustuvat päätiliin. Seuraavat tiedot lisätään konsolidointiyrityksen tileihin, joilla on sama tilinumero kuin tytäryhtiön tilillä.

Riippumatta siitä, oletko määrittänyt tilit, poista konsolidointiyrityksen **Konsolidoi**-sivun **Käytä konsolidointitiliä** -valintaruudun valinta ennen tämän tyyppisen konsolidoinnin suorittamista.

> [!NOTE]
> Voit käyttää tätä menetelmää konsolidointiyrityksen tilikartan luomiseen jostakin tytäryhtiön tilikartasta. (Lisätietoja on kohdassa [Konsolidointitiliryhmät ja lisäkonsolidointitilit](../budgeting/consolidation-account-groups-consolidation-accounts.md).) Liitä sitten asianmukainen konsolidoinnin muuntoperiaate jokaiseen konsolidoituun päätiliin ja suorita konsolidointi kaikille tytäryhtiön yrityksille.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]