---
title: Aikataulutettujen BYOD-erätöiden optimointi
description: Tässä artikkelissa käsitellään suorituskyvyn optimointia käytettäessä oman tietokannan tuontitoimintoa (BYOD) Microsoft Dynamics 365 Human Resourcesissa.
author: twheeloc
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: 4df60a82e016ec8f3ba6ba0d70c261824961d221
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848310"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a>Aikataulutettujen BYOD-erätöiden optimointi


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa käsitellään suorituskyvyn optimointia käytettäessä oman tietokannan tuontitoimintoa (BYOD). Lisätietoja oman tietokannan tuonnista on kohdassa [Oman tietokannan tuonti (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

## <a name="performance-considerations-for-data-export"></a>Tietojen viennin suorituskykyyn liittyviä tietoja

Kun entiteetit on julkaistu kohdetietokantaan, tiedot voidaan siirtää **Tiedonhallinta**-työtilan vientitoiminnolla. Vientitoiminnolla voi määrittää vähintään yhden entiteetin sisältävän tietojen siirtotyön. Lisätietoja tietojen viennistä on kohdassa [Tietojen tuonti- ja vientitöiden yleiskatsaus](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

Voit viedä tietoja **Vie**-sivulla erilaisiin kohdetietomuotoihin, kuten CSV-tiedostoon. Tämä sivu tukee myös SQL-tietokantoja toisena kohteena.

Voit luoda tietoprojektin, jossa on useita entiteettejä, ja käyttää erätyötä aikatauluttamaan kyseisen tietoprojektin suorittamisen. Jos valitset **Vienti eräajona** -vaihtoehdon, voit aikatauluttaa tietojen vientityön säännöllisesti suoritettavaksi.

Voit parantaa oman tietokannan viennin luotettavuutta harkitsemalla huolellisesti useiden entiteettien lisäämistä vientiprojektiin. Seuraavat parametrit kannattaa ottaa huomioon, kun pohditaan samaan projektiin lisättävien entiteettien määrää:

- Entiteettien monimutkaisuus
- Odotettava entiteettikohtainen tietomäärä
- Kokonaisaika, joka tarvitaan viennin valmistumiseen työtasolla

Suorituskyky pysyy hyvänä, kun yhteen projektiin ei lisätä satoja entiteettejä. Onkin suositeltavaa luoda useita töitä, joissa missään ei ole runsaasti entiteettejä.

## <a name="scheduling-byod-batch-jobs"></a>BYOD-erätöiden aikatauluttaminen

Voit vähentää vaikutusta Microsoft Dynamics 365 Human Resourcesin käyttäjiin suorittamalla BYOD-erätyöt öisin ja työajan ulkopuolella. Muista tarkistaa toistuvien erätöiden aikavyöhyke. Jotkin erätyöt voivat käyttää Pacific Standard Time (PST) -aikaa.

Suorituskykyongelmia voidaan välttää, kun seuraavat otetaan huomioon BYOD-erätöiden aikataulutusvälejä määritettäessä:

- Kunkin erätyön suorittamiseen tarvittava aika
- Omassa tietokannassa tuotavien tietojen liiketoimintatarve

Määritä kunkin erätyön toistumisarvo siten, että se varmistaa työn valmistumisen selvästi ennen seuraavaa aikataulutettua ajoa. Vältä useiden töiden rinnakkaista suorittamista, sillä se voi heikentää Human Resourcesin suorituskykyä.

Suorituskyky pysyy hyvänä, kun BYOD-erätöiden aikataulutuksessa käytetään aina **Vienti**-sivun **Vienti eräajona** -vaihtoehtoa. Vältä toistuvien vientien aikatauluttamista kohdassa **Hallinta \> Toistuvien tietotöiden hallinta**.

## <a name="incremental-export"></a>Lisäävä vienti

Kun entiteetti lisätään tietojen vientiin, valittavana on joko lisäävä siirto (vienti) tai täydellinen siirto. Täydellinen siirto poistaa kaikki entiteetin tietueet BYOD-tietokannassa. Tämän jälkeen lisätään Human Resources -entiteetin nykyinen tietuejoukko.

Lisäävää siirtoa varten muutosten seuranta on otettava käyttöön jokaisessa entiteetissä **Entiteetit**-sivulla. Lisätietoja on kohdassa [Muutosten seurannan ottaminen käyttöön yksiköille](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

Jos valitset lisäävän siirron, ensimmäinen siirto on aina täydellinen siirto. SQL seuraa muutoksia tästä ensimmäisestä täydellisestä siirrosta alkaen. Kun uusi tietue lisätään tai kun tietue päivitetään tai poistetaan, muutos näkyy myös kohde-entiteetissä.

## <a name="time-outs"></a>Aikakatkaisut

BYOD-vientien oletusaikakatkaisut:

- Kymmenen minuuttia katkaisutoiminnoissa
- Yksi tunti joukkolisäystoiminnoissa

Jos määrät ovat suuria, nämä aikakatkaisuasetukset eivät ehkä riitä. Voit päivittää ne valitsemalla **Tiedonhallinta \> Kehikkoparametrit \> Tuo oma tietokanta**. Nämä aikakatkaisut ovat yrityskohtaisia ja ne on määrittävä erikseen kullekin yritykselle.

## <a name="known-limitations"></a>Tunnetut rajoitukset

Oman tietokannan tuontitoiminnolla on seuraavat rajoitukset:

- Tietokannassa ei saa olla aktiivisia lukituksia synkronoinnin aikana. Aktiiviset lukitukset voivat hidastaa kirjoittamista tai jopa estää tietojen viennin Azuren SQL-tietokantaan.
- Yhdistelmäentiteettejä ei voi viedä omaan tietokantaan. Yhdistelmäentiteettejä ei tueta tällä hetkellä. Sen sijaan on vietävä yksittäiset entiteetit, joista yhdistelmäentiteetti koostuu. Voit kuitenkin viedä molemmat entiteetit samassa tietoprojektissa.
- Lisäävällä siirrolla ei voi entiteettejä, joilla ei ole yksilöiviä avaimia. Tämä rajoitus voi esiintyä etenkin silloin, jos yritä tehdä tietueiden lisäävän viennin muutamista valmiista entiteeteistä. Koska nämä entiteetit suunniteltiin mahdollistamaan tietojen tuonti, niillä ei ole yksilöivää avainta.

## <a name="troubleshooting"></a>Vianmääritys

### <a name="incremental-push-doesnt-work-correctly"></a>Lisäävä siirto ei toimi oikein

**Ongelma:** Kun entiteetille tehdään täydellinen siirto, näkyvissä on suuri joukko tietueita omaa tietokantaa tuotaessa ja **select**-lauseketta käytettäessä. Lisäävää siirtoa tehtäessä omaa tietokantaa tuotaessa näkyvissä on vain muutama tietue. Vaikuttaa siltä, että lisäävä siirto poisti kaikki tietueet ja lisäsi vain muuttuneet tietueet omassa tuodussa tietokannassa.

**Ratkaisu:** SQL:n muutosten seurantataulukoiden tila ei ole ehkä odotettu. Näissä tilanteissa entiteetin muutosten seuranta kannattaa poistaa käytöstä ja ottaa sitten uudelleen käyttöön. Lisätietoja on kohdassa [Muutosten seurannan ottaminen käyttöön yksiköille](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="staging-tables-arent-clearing"></a>Valmistelutaulukot eivät tyhjene

**Ongelma:** Kun käytät projektin valmistelua, valmistelutaulukot eivät tyhjenny oikein. Taulukkojen tiedot kasvavat edelleen, mikä aiheuttaa suorituskykyongelmia.

**Ratkaisu:** Valmistelutaulukoissa ylläpidetään seitsemän päivää historiaa. **Tuonnin/viennin väliaikaisen tallennuksen tietojen puhdistus** -erätyö tyhjentää valmistelutaulukoiden yli seitsemän päivää vanhemmat historiatiedot automaattisesti. Jos tämä työ jumittuu, taulukot eivät tyhjenny oikein. Tämän erätyön käynnistäminen uudelleen jatkaa prosessia valmistelutaulukoiden tyhjentämiseksi automaattisesti.

## <a name="see-also"></a>Lisätietoja

[Tietojen hallinnan yleiskatsaus](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Oman tietokannan tuonti (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Tietojen tuonti- ja vientityöt – yleiskatsaus](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Muutosten seurannan ottaminen käyttöön yksiköille](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
