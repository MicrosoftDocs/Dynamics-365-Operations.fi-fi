---
title: Tuotantotilauksen kustannusanalyysi
description: Tässä artikkelissa tietoja kustannusanalyysista, jonka voi tehdä valmiille ja nykyisille tuotantotilauksille. Voit analysoida arvioidut kustannukset ja toteutuneet kustannukset käyttämällä Hinnan laskenta -sivua tai Ennakko- ja jälkilaskelmat -raporttia. Voit tarkastella komponenttinimikkeen, reititystyövaiheen ja epäsuoran kustannuksen tietoja arvioiduista ja todellisista kustannuksista (sekä määristä).
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage, ProdSetupHistoricalCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79634
ms.assetid: ded5da04-f787-49f7-b5e5-75c2a2b92930
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd303efb5aee53eec36fac7ec6329d28aacf96a1
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672287"
---
# <a name="production-order-cost-analysis"></a>Tuotantotilauksen kustannusanalyysi

[!include [banner](../includes/banner.md)]

Tässä artikkelissa tietoja kustannusanalyysista, jonka voi tehdä valmiille ja nykyisille tuotantotilauksille. Voit analysoida arvioidut kustannukset ja toteutuneet kustannukset käyttämällä Hinnan laskenta -sivua tai Ennakko- ja jälkilaskelmat -raporttia. Voit tarkastella komponenttinimikkeen, reititystyövaiheen ja epäsuoran kustannuksen tietoja arvioiduista ja todellisista kustannuksista (sekä määristä).

Tuotantotilauksen epäsuorat kustannukset perustuvat raportoituun materiaalinkulutukseen ja reititystyövaiheisiin. Ilmoitettua materiaalinkulutusta, reitityksen työvaiheita ja epäsuoria kustannuksia koskevat yksityiskohtaiset tapahtumat ovat tuotantotilauksen **Tuotannon kirjaus** -sivulla.

## <a name="variance-analysis-for-a-completed-production-order"></a>Valmiin tuotantotilauksen varianssianalyysi
Variansseissa näkyy tuotantonimikkeen ilmoitettujen tuotantotehtävien ja vakiokustannuslaskelmien ero. Suhde tuotantotilauksen arvioituihin kustannuksiin ei näy variansseissa. Ilmoitettuja tuotantotehtäviä ovat materiaalinkulutus ja reitityksen työvaiheet (ja niihin liittyvät epäsuorat kustannukset) sekä valmiiksi ilmoitettujen määrä. Seuraavat neljä varianssityyppiä lasketaan:

-   Eräkoon varianssi
-   Tuotannon määrävarianssi
-   Tuotantohintavarianssi
-   Tuotannon korvausvarianssi

Seuraavassa kaaviossa esitellään neljä varianssia, joissa näkyy tuotantotilauksen toteutuneiden kustannusten ja laskettujen kustannusten ero nimikkeen kustannustietueessa, kun tuotantotilaus on päätetty. 

![Valmiin tuotantotilauksen erot selittävä varianssi.](./media/control.jpg) 

Voit analysoida tuotannon variansseja **Varianssit**-sivulla tai **Tuotannon varianssi** -raportissa. Näyttöasetusten avulla voit tarkastella eriteltyjä varianssitietoja nimikkeen ja operatiivisen resurssin tai kustannusryhmän mukaan. Varastoparametrien kustannuserittelymenettely määrittää, seurataanko variansseja kustannusryhmän mukaan. Voit myös tarkastella varianssien yhteenvetoja **Yksittäinen**-, **Monitasoinen**- ja **Yhteensä** -näyttöasetusten avulla. Varianssin eritellyt tiedot auttavat ymmärtämään kunkin varianssin alkuperän. Jos haluat ennakoida varianssit ennen tuotantotilauksen päättämistä, analysoi **Ennakko- ja jälkilaskelmat** -raportin eritellyt tiedot.

## <a name="cost-analysis-for-current-production-orders"></a>Nykyisten tuotantotilausten kustannusanalyysi
Erillisissä raporteissa on tietoja kustakin tapahtumatyypistä. Näiden raporttien avulla voit analysoida ilmoitettujen tuotantotehtävien kustannuksia. Raporteissa on tietoja vain nykyisistä tuotantotilauksista, joiden tila on **Alkanut** tai **Ilmoitettu valmiiksi**.

-   **Keskeneräiset materiaalit**− Raportissa luetellaan keräysluettelotapahtumat, jotka on ilmoitettu nykyisiä tuotantotilauksia vasten määritetystä tapahtumapäivämäärästä alkaen. Raportissa ilmoitetaan komponentin otettu määrä sekä kunkin tapahtuman kustannussumma. Käytä yhden komponenttinimikkeen valintaehtoja. Voit esimerkiksi tulostaa tietoja komponentin otetusta määrästä sovellettavia tuotantotilauksia vasten. Otettua määrää ei päivitetä päänimikkeen valmiiksi ilmoitetuiksi määriksi. Tällöin prosessin raaka-aineiden todellinen määrä voidaan arvioida liian suureksi.
-   **Keskeneräinen työ**− Raportissa luetellaan reititystapahtumat (eli työt), jotka on ilmoitettu nykyisiä tuotantotilauksia vasten määritetystä tapahtumapäivämäärästä alkaen. Raportti sisältää jokaiselle tapahtumalle raportoidut tunnit, summan ja määrän (hyväksytyn ja virheellisen). Se sisältää myös tunnistustiedot, kuten työvaihenumeron, työvaihetunnuksen ja operatiivisen resurssin. Raportti näyttää myös kaikkien tuotantotilauksen ja valmiiksi ilmoitetun määrän tapahtumien kokonaisajan ja -summan.
-   **Keskeneräiset epäsuorat kustannukset**− Raportissa ilmoitetaan epäsuorat kustannukset, jotka on hankittu tuotantotilauksia vasten. Tiedot perustuvat reitityksen työvaiheiden ja komponenttien ilmoitettuun kulutukseen määritetystä tapahtumapäivämäärästä lähtien. Raportti ilmaisee epäsuoran kustannuksen tyypin (lisämaksu vai hinta), epäsuoran kustannuksen laskentalomakkeen koodin ja kunkin tapahtuman kustannussumman. Raportti ei sisällä tietoja epäsuoran kustannuksen luoneesta reitityskortti- tai keräysluettelotapahtumasta.
-   **Keskeneräisen tuotannon kustannuslaskenta**− Raportissa ilmoitetaan materiaalinkulutus, reitityksen työvaiheet ja epäsuorat kustannukset yhteensä nykyisiä tuotantotilauksia vasten määritetystä tapahtumapäivämäärästä alkaen.
-   **Keskeneräiset valmiit nimikkeet**− Raportissa ilmoitetaan nykyiset tuotantotilaukset sekä valmiiksi ilmoitetut tapahtumat määritetystä tapahtumapäivämäärästä alkaen.


## <a name="additional-resources"></a>Lisäresurssit

[Tuotannon varianssien yhteiset lähteet](common-sources-of-production-variances.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]