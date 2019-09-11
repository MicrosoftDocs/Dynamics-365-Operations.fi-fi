---
title: Kustannusten ja päivämäärien hallinta
description: Tässä ohjeaiheessa kerrotaan kustannusten ja päivien hallinnasta resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2bcd1584f6a858f7589387fbfe96267b7c16176a
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918392"
---
# <a name="cost-and-date-control"></a>Kustannusten ja päivämäärien hallinta

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Käyttöomaisuuden hallinnassa voit laskea kustannuksia, jolloin saat yleiskuvan todellisista kustannuksista resurssien, toiminnallisten sijaintien tai työtilausten budjettikustannuksiin verrattuna. Todelliset kustannukset perustuvat kirjattuihin tapahtumiin. Voit myös määrittää päivämäärän laskemisen, jos haluat verrata ajoitettuja alkamis- ja päättymispäiviä työtilausten todellisiin alkamis- ja päättymispäiviin.

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a>Käyttöomaisuuksien, toiminnallisten sijaintien ja työtilausten kustannusten hallinta

Käyttöomaisuudelle, toiminnallisille sijainneille ja työtilauksille tehdyt laskelmat ovat lähes identtiset. Ainoa ero on se, että käyttöomaisuudelle ja toimipaikoille voidaan sisällyttää myös aliresursseja ja alisijainteja laskennassa. Päivämäärä on tapahtumapäivämäärä, jolloin rekisteröinti tallennettiin.

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssit** > **Resurssien kustannusten hallinta** tai **Toiminnallisen sijainnin kustannusten hallinta** tai **Resurssien hallinta** > **Kyselyt** > **Työtilaukset** > **Työtilauksen kustannusten hallinta**.

2. Valitse laskettava kausi **Resurssien kustannusten hallinta**- / **Toiminnallisen sijainnin kustannusten hallinta**- / **Työtilauksen kustannusten hallinta** -valintaikkunassa.

3. Valitse tarvittaessa taloushallinnon dimensioyhdistelmä, joka sisällytetään laskelmiin.

4. Valitse "kyllä" **Ohita nolla** -vaihtopainikkeessa, jos et halua näyttää tuloksia, joissa kustannus on nolla.

5. **Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia kustannushallinnan riveistä haluat liittyen toiminnallisiin sijainteihin. Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintihierarkia, kaikki toimintosijainnin kustannusten hallinnan rivit näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista. Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki kustannusten hallinnan rivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.

6. Valitse **Näytä avoin sidottu kustannus** -vaihtopainikkeen arvoksi Kyllä, jos haluat sisällyttää kyseisen sarakkeen laskelmiin.

7. Valitse "kyllä" **Sisällytä aliresurssit** -vaihtopainikkeessa, jos haluat näyttää aliresursseihin liittyvät kustannukset erillisinä riveinä.

8. Jos haluat rajata haun, voit valita tietyt käyttöomaisuudet / toiminnalliset siajinnit/ työtilaukset **Sisällytettävät tietueet** -pikavälilehdessä.

9. Aloita laskenta valitsemalla **OK**.

Alla olevassa kuvassa on esimerkki **Resurssien kustannusten hallinta** -valintaikkunasta.

![Kuva 1](media/01-controlling-and-reporting.png)

10. Valitse **Resurssien kustannusten hallinta** -sivun toimintoruudun **Ryhmittely ...**  -ryhmissä asiaankuuluvia painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason. Valitut toimintoruudun painikkeet on korostettu. Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.

Alla olevassa kuvassa on esimerkki **Resurssien kustannusten hallinta** -laskennan tuloksista.

![Kuva 2](media/02-controlling-and-reporting.png)

Toinen tapa määrittää kustannuslaskennat on valita valita monta resurssia **Kaikki resurssit**- tai **Aktiiviset resurssit** -kohdassa. Valitse sitten **Yleiset**-välilehden **Kustannusten hallinta** -painike. **Resurssien kustannusten hallinta**-valintaikkunassa valitut käyttöomaisuudet lisätään automaattisesti **Sisällytettävät tietueet** -pikavälilehden **Resurssi**-kenttään. Valitse **OK**, niin valittujen käyttökohteiden kustannuslaskennat näytetään. Sama menettely voidaan tehdä toiminnallisille sijainneille kohdassa **Kaikki toiminnalliset sijainnit** tai **Aktiiviset toiminnalliset sijainnit** sekä kohdassa  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

>[!NOTE]
>**Alkuperäinen budjetti** -kenttä sisältää työtilausennusteen budjetoidut kustannukset. **Sidottu kustannus** -kenttä näyttää kokonaiskustannukset, jonka yritys on sitoutunut maksamaan. **Avoin sidottu kustannus** -kentässä näkyvät sitoumukset maksaa nimikkeistä, tunneista ja palveluista, jotka olet tilannut tai vastaanottanut mutta joita ei ole vielä maksettu. Kun kaikki kulutusrekisteröinnit on kirjattu, niihin liittyvät kustannukset sisältyvät **Toteutunut kustannus** -kenttään.

## <a name="work-order-date-control"></a>Työtilausten päivämäärien hallinta

Tämän sivun avulla voit saada yleiskuvan suunnitelluista alkamis- ja päättymispäivistä verrattuna työtilausten todellisiin alkamis- ja päättymispäiviin.

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Työtilaukset** > **Työtilauksen päivämäärien hallinta**.

2. Valitse **Laske**.

3. Valitse toiminnallinen sijainti **Toiminnallinen sijainti** -kentässä.

4. Lisää kausi, jonka ajalta haluat tehdä laskennan (**Alkamispäivämäärä**- ja **Päättymispäivämäärä** -kentät). Kaikki työtilaukset, joilla on odotettu aloitus kauden sisällä, sisällytetään.

5. Valitse **OK**.

6. Valitse toimintoruudun **Ryhmittely...** -ryhmissä asiaankuuluvia painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason. Valitut toimintoruudun painikkeet on korostettu. Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.

Alla olevassa kuvassa on esimerkki **työtilauksen päivämäärien hallinta** -laskennan tuloksista.

![Kuva 3](media/03-controlling-and-reporting.png)

- **Keskim. aloituksen viive** -kentässä näkyy työtilauksen suunnitellun alkamispäivän välinen ero suhteessa todelliseen alkamispäivämäärään. Jos todellinen alkamispäivä on esimerkiksi kaksi päivää ennen ajoitettua alkamispäivää, kentässä näkyy "-2".  
- **Keskim. lopetuksen viive** -kentässä näkyy työtilauksen suunnitellun lopetuspäivän välinen ero suhteessa todelliseen lopetuspäivämäärään. Jos todellinen lopetuspäivä on esimerkiksi kolme päivää ajoitetun lopetuspäivän jälkeen, kentässä näkyy "3".  
- **Esiintymiskerrat**-kentissä näkyy, kuinka monta kertaa poikkeama esiintyy suhteessa ajoitettuun ja todelliseen alkamispäivämäärään sekä työtilauksen ajoitettuun ja todelliseen päättymispäivämäärään.

