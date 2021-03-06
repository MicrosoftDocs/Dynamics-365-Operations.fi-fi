---
title: Taloushallinnon raportoinnin usein kysytyt kysymykset
description: Tämä ohjeaihe sisältää vastauksia eräisiin usein kysyttyihin talousraportoinnin kysymyksiin.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266630"
---
# <a name="financial-reporting-faq"></a>Taloushallinnon raportoinnin usein kysytyt kysymykset

Tämä ohjeaihe sisältää vastauksia usein kysyttyihin talousraportoinnin kysymyksiin.

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>Miten rajoitan raportin käyttöoikeuksia puurakenteen suojauksen avulla?

Seuraavassa esimerkissä kerrotaan, miten raportin käyttöoikeuksia rajoitetaan puurakenteen suojauksen avulla.

USMF-esittely-yrityksellä on **taseraportti**, johon kaikilla taloushallinnon raportoinnin käyttäjillä ei pitäisi olla käyttöoikeuksia. Voit rajoittaa yksittäisen raportin käyttöoikeutta puurakenteen suojauksen avulla siten, että vain tietyt käyttäjät voivat käyttää sitä.

1. Kirjaudu Financial Reporter Report Designer -palveluun.
2. Luo uusi puumääritys valitsemalla **Tiedosto \> Uusi \> Puumäritys**.
3. Kaksoisnapauta (tai kaksoisnapsauta) **Yhteenveto**-riviä **Yksikkösuojaus**-sarakkeessa.
4. Valitse **Käyttäjät ja ryhmät**.
5. Valitse käyttäjät tai ryhmät, joiden on voitava käyttää tätä raporttia.
6. Valitse **Tallenna**.
7. Lisää uusi puumäärityksesi raportin määritykseen.
8. Valitse puumäärityksessä **Asetus**. Valitse sitten **Raportointiyksikön valinta** -kohdassa **Sisällytä kaikki yksiköt**.

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>Miten tunnistan tilit, jotka eivät täsmää saldojeni kanssa?

Jos sinulla on raportti, jossa ei ole täsmääviä saldoja, käytä seuraavia toimia tilien ja niiden varianssien tunnistamiseksi.

### <a name="in-financial-reporter-report-designer"></a>Financial Reporter Report Designer -palvelussa

1. Luo uusi rivimääritys.
2. Valitse **Muokkaa \> Lisää rivit dimensioista**.
3. Valitse **MainAccount**.
4. Valitse **OK**.
5. Tallenna rivimääritys.
6. Luo uusi sarakemääritys.
7. Luo uusi raportin määritys.
8. Valitse **Asetukset** ja poista tämän vaihtoehdon valinta.
9. Luo raportti. 
10. Vie raportti Microsoft Exceliin.

### <a name="in-dynamics-365-finance"></a>Dynamics 365 Financessa

1. Mene kohtaan **Pääkirja \> Kyselyt ja raportit \> Pääkirja**.
2. Määritä seuraavat kentät:

    - **Aloituspäivä** – syötä tilikauden alkamispäivä.
    - **Päättymispäivämäärä** – syötä päivämäärä, jolle raportti luodaan.
    - **Taloushallinnon dimensio** – aseta tämän kentän arvoksi **Asetettu päätili**.

3. Valitse **Laske**.
4. Vie raportti Exceliin.

Nyt sinun pitäisi pystyä kopioimaan tiedot Financial Reporterin Excel-raportista **Pääkirja**-raporttiin, jotta voit verrata **Loppusaldo**-sarakkeita.

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Kun suunnittelen raportin Report Designerissa tai kun luon talousraportin, näyttöön tulee seuraava sanoma: "Työvaihetta ei voitu suorittaa loppuun tietopalvelun kehikossa olevan ongelman vuoksi." Miten reagoin?

Sanoma ilmaisee, että virhe tapahtui, kun järjestelmä yritti hakea taloushallinnon metatietoja tietovaraston osajoukosta käyttäessäsi talousraportointia. Tähän ongelmaan voi reagoida kahdella tavalla:

- Tarkista tietojen integroinnin tila menemällä Report Designerin kohtaan **Työkalut \> Integroinnin tila**. Jos integrointi on kesken, odota sen valmistumista. Yritä sen jälkeen uudelleen sitä, mitä teit saadessasi sanoman.
- Ota yhteyttä tukeen, jotta ongelma voidaan tunnistaa ja käsitellä. Järjestelmässä saattaa olla epäyhtenäisiä tietoja. Tuki-insinöörit auttavat palvelimella olevan ongelman tunnistamisessa ja etsivät erityiset tiedot, jotka saattavat vaatia päivittämistä.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
