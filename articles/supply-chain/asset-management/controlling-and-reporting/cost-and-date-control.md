---
title: Kustannusten ja päivämäärien hallinta
description: Tässä artikkelissa kerrotaan kustannusten ja päivien hallinnasta resurssien hallinnassa.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 643e5afda7d3abaff926e81ff75186ca195a8cb1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861037"
---
# <a name="cost-and-date-control"></a>Kustannusten ja päivämäärien hallinta

[!include [banner](../../includes/banner.md)]

Käyttöomaisuuden hallinnassa voit laskea kustannuksia, jolloin saat yleiskuvan todellisista kustannuksista resurssien, toiminnallisten sijaintien tai työtilausten budjettikustannuksiin verrattuna. Todelliset kustannukset perustuvat kirjattuihin tapahtumiin.

Voit myös määrittää päivämäärän laskemisen, jos haluat verrata ajoitettuja alkamis- ja päättymispäiviä työtilausten todellisiin alkamis- ja päättymispäiviin.

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a>Käyttöomaisuuksien, toiminnallisten sijaintien ja työtilausten kustannusten hallinta

Käyttöomaisuudelle, toiminnallisille sijainneille ja työtilauksille tehdyt laskelmat ovat lähes identtiset. Ainoa ero on, että käyttöomaisuudelle ja toimipaikoille voidaan sisällyttää myös aliresursseja ja alisijainteja laskennassa. Päivämäärä on tapahtumapäivämäärä, jolloin rekisteröinti tallennettiin.

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssit** > **Resurssien kustannusten hallinta** tai **Toiminnallisen sijainnin kustannusten hallinta** tai **Resurssien hallinta** > **Kyselyt** > **Työtilaukset** > **Työtilauksen kustannusten hallinta**.

2. Valitse laskettava aikaväli **Resurssien kustannusten hallinta**- / **Toiminnallisen sijainnin kustannusten hallinta**- / **Työtilauksen kustannusten hallinta** -valintaikkunassa.

3. Valitse tarvittaessa taloushallinnon dimensioyhdistelmä, joka sisällytetään laskelmiin.

4. Valitse "kyllä" **Ohita nolla** -vaihtopainikkeessa, jos et halua näyttää tuloksia, joissa kustannus on nolla.

5. **Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia kustannushallinnan riveistä haluat liittyen toiminnallisiin sijainteihin. 

    Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintihierarkia, kaikki toimintosijainnin kustannusten hallinnan rivit näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista.

    Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki kustannusten hallinnan rivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.

6. Valitse **Näytä avoin sidottu kustannus** -vaihtopainikkeen arvoksi Kyllä, jos haluat sisällyttää kyseisen sarakkeen laskelmiin.

7. Valitse "kyllä" **Sisällytä aliresurssit** -vaihtopainikkeessa, jos haluat näyttää aliresursseihin liittyvät kustannukset erillisinä riveinä.

8. Jos haluat rajata haun, voit valita tietyt käyttöomaisuudet / toiminnalliset siajinnit/ työtilaukset **Sisällytettävät tietueet** -pikavälilehdessä.

9. Aloita laskenta valitsemalla **OK**.

    Alla olevassa kuvassa on esimerkki **Resurssien kustannusten hallinta** -valintaikkunasta.

    ![Resurssien kustannusten hallinta -valintaikkuna.](media/01-controlling-and-reporting.png)

10. Napsauta **Resurssien kustannusten hallinta** -sivulla **Ryhmittele**-painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason. Valitut **Ryhmittely...**-painikkeet on korostettu. Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.

## <a name="example-of-calculation-results-in-asset-cost-control"></a>Esimerkki resurssien kustannusten hallinnan laskutuloksista

Alla olevassa näyttökuvassa on esimerkki **Resurssien kustannusten hallinta** -laskennan tuloksista.

- **Alkuperäinen budjetti** -kenttä sisältää työtilausennusteen budjetoidut kustannukset. 
- **Sidottu kustannus** -kenttä näyttää kokonaiskustannukset, jonka yritys on sitoutunut maksamaan. 
- **Avoin sidottu kustannus** -kentässä näkyvät sitoumukset maksaa nimikkeistä, tunneista ja palveluista, jotka olet tilannut tai vastaanottanut mutta joita ei ole vielä maksettu. 
- **Toteutunut kustannus** -kentässä näkyvät asiaan liittyvät kulut, kun kaikki kulutusrekisteröinnit on kirjattu.

![Esimerkki resurssien kustannusten hallinnan laskutuloksista.](media/02-controlling-and-reporting.png)

Toinen tapa määrittää kustannuslaskennat on valita valita monta resurssia **Kaikki resurssit**- tai **Aktiiviset resurssit** -kohdassa. Valitse sitten **Yleiset**-välilehden **Kustannusten hallinta** -painike. **Resurssien kustannusten hallinta**-valintaikkunassa valitut käyttöomaisuudet lisätään automaattisesti **Sisällytettävät tietueet** -pikavälilehden **Resurssi**-kenttään. Valitse **OK**, niin valittujen käyttökohteiden kustannuslaskennat näytetään. Sama menettely voidaan tehdä toiminnallisille sijainneille kohdassa **Kaikki toiminnalliset sijainnit** tai **Aktiiviset toiminnalliset sijainnit** sekä kohdassa  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

## <a name="work-order-date-control"></a>Työtilausten päivämäärien hallinta

Tämän sivun avulla voit saada yleiskuvan suunnitelluista alkamis- ja päättymispäivistä verrattuna työtilausten todellisiin alkamis- ja päättymispäiviin.

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Työtilaukset** > **Työtilauksen päivämäärien hallinta**.

2. Valitse **Laske**.

3. Valitse toiminnallinen sijainti **Toiminnallinen sijainti** -kentässä.

4. Lisää aikaväli, jonka ajalta haluat tehdä laskennan (**Alkamispäivämäärä**- ja **Päättymispäivämäärä** -kentät). Kaikki työtilaukset, joiden oletettu aloituspäivä osuu aikavälillä, otetaan huomioon.

5. Valitse **OK**.

6. Valitse **Ryhmittely...**-painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason. Valitut **Ryhmittely...**-painikkeet on korostettu. Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.

## <a name="example-of-calculation-results-in-work-order-date-control"></a>Esimerkki työtilausten päivämäärien hallinnan laskutuloksista

Alla olevassa näyttökuvassa on esimerkki **Työtilauksen päivämäärien hallinta** -laskennan tuloksista.

- **Keskim. aloituksen viive** -kentässä näkyy työtilauksen suunnitellun alkamispäivän välinen ero suhteessa todelliseen alkamispäivämäärään. Jos todellinen alkamispäivä on esimerkiksi kaksi päivää ennen ajoitettua alkamispäivää, kentässä näkyy "-2".  
- **Keskim. lopetuksen viive** -kentässä näkyy työtilauksen suunnitellun lopetuspäivän välinen ero suhteessa todelliseen lopetuspäivämäärään. Jos todellinen lopetuspäivä on esimerkiksi kolme päivää ajoitetun lopetuspäivän jälkeen, kentässä näkyy "3".  
- **Esiintymiskerrat**-kentissä näkyy, kuinka monta kertaa poikkeama esiintyy suhteessa ajoitettuun ja todelliseen alkamispäivämäärään sekä työtilauksen ajoitettuun ja todelliseen päättymispäivämäärään.

![Esimerkki työtilausten päivämäärien hallinnan laskutuloksista.](media/03-controlling-and-reporting.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]