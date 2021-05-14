---
title: Taloushallinnon raportoinnin usein kysytyt kysymykset
description: Tässä ohjeaiheessa käsitellään kysymyksiä, joita muilla käyttäjillä on ollut taloushallinnon raportoinnista.
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
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923022"
---
# <a name="financial-reporting-faq"></a>Taloushallinnon raportoinnin usein kysytyt kysymykset 

Tämä ohjeaihe sisältää vastauksia usein kysyttyihin talousraportoinnin kysymyksiin. 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Miten rajoitan raportin käyttöoikeuksia puurakenteen suojauksen avulla?

Seuraavassa esimerkissä kerrotaan, miten raportin käyttöoikeuksia rajoitetaan puurakenteen suojauksen avulla.

USFM-esittely-yrityksellä on taseraportti, johon kaikilla taloushallinnon raportoinnin käyttäjillä ei pitäisi olla käyttöoikeuksia. Voit rajoittaa käyttöoikeutta puurakenteen suojauksen avulla siten, että vain tietyt käyttäjät voivat käyttää raporttia. Rajoita käyttöoikeuksia noudattamalla seuraavia ohjeita: 

1. Kirjaudu Financial Reporter Report Designer.
2. Luo uusi puumääritys. Siirry kohtaan **Tiedosto > Uusi > Puumääritys**.
3. Kaksoisnapsauta **Yhteenveto**-riviä **Yksikkösuojaus**-sarakkeessa.
4. Valitse **Käyttäjät ja ryhmät**.  
5. Valitse käyttäjät tai ryhmät, joiden on voitava käyttää tätä raporttia. 
6. Valitse **Tallenna**.
7. Lisää uusi puumäärityksesi raportin määritykseen.
8. Valitse puumäärityksessä **Asetus**. Valitse **Raportointiyksikön valinta** -kohdassa **Sisällytä kaikki yksiköt**.

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a>Miten tunnistan tilit, jotka eivät täsmää saldojeni kanssa?

Jos sinulla on raportti, jossa ei ole täsmääviä saldoja, voit kokeilla seuraavia toimia tilien ja niiden varianssien tunnistamiseksi. 

**Financial Reporter Report Designer**
1. Luo uusi rivimääritys kohteessa Financial Reporter Report Designer. 
2. Valitse **Muokkaa > Lisää rivit dimensioista**.
3. Valitse **Päätili**.  
4. Valitse **OK**.
5. Tallenna rivimääritys.
6. Luo uusi sarakemääritys.
7. Luo uusi raportin määritys.
8. Valitse **Asetukset** ja poista tämän vaihtoehdon valinta.  
9. Luo raportti. 
10. Vie raportti Microsoft Exceliin.

**Dynamics 365 Finance** 
1. Valitse Dynamics 365 Financessa **Pääkirja > Kyselyt ja raportit > Pääkirja**.
2. Määritä seuraavat parametrit:
   - **Aloituspäivä** - syötä tilikauden alku.
   - **Aloituspäivä** - syötä päivämäärä, jolle raportti luodaan.
   - **Taloushallinnon dimensio** - aseta tämän kentän arvoksi **Asetettu päätili**.
 3. Valitse **Laske**.
 4. Vie raportti Microsoft Exceliin.

Nyt sinun pitäisi nyt pystyä kopioimaan tiedot Raporttien suunnitteluohjelman Excel-raportista Pääkirja-raporttiin, jotta voit verrata **Loppusaldo**-sarakkeita.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]