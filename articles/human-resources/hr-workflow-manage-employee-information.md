---
title: Työntekijätietojen hallinta työnkulkujen avulla
description: Tässä artikkelissa käsitellään työntekijätietojen hallintaa työnkulkujen avulla.
author: twheeloc
ms.date: 11/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: dbbbb0ee807cb65fa4f4f9a29cc4a2b6b045b08c
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750731"
---
# <a name="use-workflows-to-manage-employee-information"></a>Työntekijätietojen hallinta työnkulkujen avulla

[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kerrotaan, henkilöstöhallinnon työnkulkuja käytetään työntekijätietojen hallintaan. Voit esimerkiksi liittää työnkulun toimeen ja määrittää hyväksynnän työnkulun, joka käynnistyy, kun työntekijät muuttavat tietuettaan.

Henkilöstöhallinnon työnkulut sisältävät useita työnkulkuja henkilöstönhallinnon tehtävien hallintaan. Käytettävissä on myös useita vaihtoehtoja tiettyjen työkulkujen muokkaamiseen ja niiden liittämiseen raportointihierarkiaan. Työnkulut auttavat muutosten tekemisessä monen tyyppisiin työntekijätietoihin. Voit liittää työnkulun toimeen. Jos työntekijä muuttaa nyt työntekijätietuettaan, käynnistyy työnkulku, joka edellyttää hyväksynnän ennen, kuin uudet tiedot voidaan tallentaa. Seuraaville tietotyypeille on määritetty työnkulut etukäteen, jotta työntekijätietojen tarkkuuden säilyttäminen ja muutosten hallinta olisi mahdollisimman tehokasta:

-   Tunnusnumerot
-   Kurssit
-   Koulutus
-   Kuva
-   Lainatut nimikkeet
-   Ammattikokemus
-   Projektikokemus
-   Osaamisalueet
-   Luottamustoimet
-   Henkilöstöhallinnon toimet
-   Kurssin rekisteröinti

Työnkulkuun voi sisältyä arviointiprosessi, kun työntekijöitä palkataan, siirretään tai irtisanotaan. Tällä tavalla asiakirjan voi tarkistaa tai toiminnon ehdot määrittää osaksi työnkulkua. Kun tarkistus on valmis, asiakirja tai toiminto on valmis ja työnkulku siirtyy lopulliseen hyväksyntävaiheeseen.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Työnkulun liittäminen toimihierarkiaan

Voit liittää työnkulun mihin tahansa määrittämääsi toimihierarkiaan. Työnkulkujen reitityksessä käytetään kahta hierarkiatyyppiä: **Johtajahierarkia** ja **Määritettävä hierarkia**.

- **Johtajahierarkia** edustaa yrityksen tai organisaation raportointirakennetta. Lisätietoja tästä hierarkiatyypistä on kohdassa [Raportoi toimelle](hr-personnel-positions.md#reports-to-position).
- **Määritettävä hierarkia** edustaa matriisia tai mukautettua hierarkiaa. Lisätietoja tästä hierarkiatyypistä on kohdassa [Suhteet](hr-personnel-positions.md#relationships).

### <a name="managerial-hierarchy-example"></a>Esimerkki johtajahierarkiasta

Voit määrittää työnkulun siten, että kun työntekijä lähettää ostopyynnön uutta tietokonetta varten, se reititetään työntekijän esimiehelle ja tasoa ylemmälle esimiehelle. Kun määrität työnkulun vaihetta, määritä **Määrityksen tyyppi** -kentän arvoksi **Hierarkia**. **Hierarkiatyyppi**-välilehti tulee tällöin käyttöön. Valitse tässä esimerkissä **Johtajahierarkia**.

### <a name="configurable-hierarchy-example"></a>Esimerkki määritettävästä hierarkiasta

Jos toimi liittyy esimerkiksi matriisiraportointihierarkiaan, voit määrittää työnkulun, joka reitittää tietyn projektin kulut projektin johtajalle työntekijän esimiehen sijasta. Määritä tällöin **Määrityksen tyyppi** -kentän arvoksi **Hierarkia**. Valitse **Hierarkiatyyppi**-välilehdestä **Määritettävä hierarkia**. Kun työnkulku on määritetty, valitse **Työnkulkuasetus**-sivulta **Liitä**-hierarkia valitaksesi hierarkian, jota tulisi käyttää työnkulun reitityksessä.

> [!IMPORTANT]
> Kun työnkulun hyväksyntään lähetetään asiakirja, tapahtuma tai päätietue, lähettäjän ensisijaista toimea käytetään määrittämään, kenelle asiakirja tulisi reitittää seuraavaksi.

### <a name="hierarchy-setting-in-workflow-parameters"></a>Työnkulkuparametrien hierarkia-asetus

1. Siirry **Työnkulkuparametrit**-sivulla **Hierarkian reititys** -osioon.
2. **Käytä toimihierarkiaa** -vaihtoehdoksi on määritetty oletusarvoisesti **Ei**. Tällöin työnkulku käyttää työntekijän ensisijaista toimea hierarkiassa navigointiin. Määritä vaihtoehdoksi **Kyllä**, jos haluat työnkulun käyttävän toimen ylätasoa hierarkiassa navigointiin.

### <a name="additional-example"></a>Lisäesimerkki 

Työntekijä Grace Sturmanilla on kaksi toimea: konsultti ja kouluttaja. Gracen ensisijainen toimi on kouluttaja. Kun hän ei kouluta uusia työntekijöitä, hän voi toimia konsulttina. Grace raportoi ensisijaisessa toimessaan henkilöstöhallintojohtaja Clairelle. Claire raportoi Charlielle. Konsulttina toimiessaan Gracella on useita yhteyksiä projektista riippuen.

Gracen yritys luo työnkulun reitityssääntöjä, jotka perustuvat **Määritettävään hierarkiaan** (matriisihierarkiat / projektipohjaiset hierarkiat). Tässä hierarkiassa käytetään Gracen toimea konsulttina. Jos **Käytä toimihierarkiaa** -vaihtoehdoksi on määritetty **Ei** ja Gracelle reititetään asiakirja hyväksyntää varten, työnkulku tarkistaa hänen ensisijaisen toimensa (kouluttaja) määrittääkseen, minne asiakirja tulisi reitittää seuraavaksi. Tällöin se reititetään ensin Clairelle ja sitten Charlielle. Jos vaihtoehdoksi on määritetty **Kyllä** ja työnkulku käyttää **määritettävää hierarkiaa**, työnkulku tarkistaa Gracen konsulttitoimen ja raportointisuhteen määrittääkseen, minne asiakirja tulisi reitittää seuraavaksi.

### <a name="configure-a-human-resources-workflow"></a>Henkilöstöhallinnon toimien määrittäminen
Seuraa näitä vaiheita määrittääksesi perustyönkulun, joka käynnistetään, kun työntekijät haluavat muuttaa henkilötietojaan.

1.  Valitse **Henkilöstöhallinnon työkulut** -sivulla **Uusi**.
2.  Valitse käytettävien työnkulkujen luettelosta **Tunnusnumerot**.
3.  Avaa työnkulun suunnitteluohjelma valitsemalla **Suorita** ja anna sitten käyttäjänimesi ja salasanasi.
4.  Siirrä **Hyväksy tunnusnumero** -elementti työnkulun elementtien luettelosta suunnittelusovelluksen alustalle.
5.  Yhdistä hyväksyntäelementti **Alku**- ja **Loppu**-elementteihin.
6.  Valitse ensin kaksoisnapauttamalla (tai -napsauttamalla) **Hyväksy elementti**, pidä sitä sitten valittuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse lopuksi **Ominaisuudet**.
7.  Voit lisätä työkohteen ohjeita seuraavasti:

    1.  Valitse **Tehtävä** ja sitten **Hierarkia** tehtävätyyppi-kohdasta.
    2.  Valitse **Hierarkia**-vaihtoehdoista **Määritettävä hierarkia**.
    3.  Lisää pysäytysehto ja sulje sivu.

8.  Suorita muut mahdolliset lisäohjeet.
9.  Valitse **Tallenna ja sulje**. Aktivoi uusi työnkulku valitsemalla **Aktivoi** aukeavasta valintaikkunasta.
10. Siirry kohtaan **Henkilöstöhallinto** &gt; **Toimet** &gt; **Positiohierarkiatyypit**.
11. Valitse **Matriisi**.
12. Lisää **työntekijän tunnusnumero** -työnkulku luetteloon.

## <a name="additional-resources"></a>Lisäresurssit

[Osoitemuutosten tarkasteleminen ja hallinta](hr-personnel-view-address-changes.md) 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
