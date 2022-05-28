---
title: Työntekijätietojen hallinta työnkulkujen avulla
description: Tässä aiheessa käsitellään työntekijätietojen hallintaa työnkulkujen avulla.
author: twheeloc
ms.date: 11/03/2021
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
ms.openlocfilehash: 7c416a82976bc39464006325f02f1af4d2f32ea4
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691523"
---
# <a name="use-workflows-to-manage-employee-information"></a>Työntekijätietojen hallinta työnkulkujen avulla


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä ohjeaiheessa kerrotaan, henkilöstöhallinnon työnkulkuja käytetään työntekijätietojen hallintaan. Voit esimerkiksi liittää työnkulun toimeen ja määrittää hyväksynnän työnkulun, joka käynnistyy, kun työntekijät muuttavat tietuettaan.

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
Voit liittää työnkulun mihin tahansa määrittämääsi hierarkiaan. Jos toimeen liittyy esimerkiksi raportointihierarkian matriisi, voit määrittää työnkulun, joka reitittää kulut tietystä projektista projektin johtajalle toimeen liittyvän työntekijän esimiehen sijasta. Luo uusi työnkulku tai muokkaa aiemmin luotua työnkulkua valitsemalla **Henkilöstöhallinnan työnkulku** -sivulla **Uusi**. Avaa työnkulun suunnitteluohjelma valitsemalla työnkulku luettelossa. Voit käyttää suunnittelusovellusta uuden työnkulun luontiin tai muuttaa aiemmin luodun työnkulun vaiheita. Kun muutat aiemmin luotua työnkulkua, muutokset tallennetaan uuteen versioon. Tämän ansiosta voit tarvittaessa palata aiempaan versioon.

## <a name="configure-a-human-resources-workflow"></a>Henkilöstöhallinnon toimien määrittäminen
Seuraa näitä vaiheita määrittääksesi perustyönkulun, joka käynnistetään, kun työntekijät haluavat muuttaa henkilötietojaan.

1.  Valitse **Henkilöstöhallinnon työkulut** -sivulla **Uusi**.
2.  Valitse käytettävien työnkulkujen luettelosta **Tunnusnumerot**.
3.  Avaa työnkulun suunnitteluohjelma valitsemalla **Suorita** ja anna sitten käyttäjänimi ja salasana pyydettäessä.
4.  Vedä **Hyväksy tunnusnumero** -elementti työnkulun elementtien luettelosta suunnittelusovelluksen alustalle.
5.  Yhdistä hyväksyntäelementti **Alku**- ja **Loppu**-elementteihin.
6.  Valitse ensin kaksoisnapauttamalla (tai -napsauttamalla) **Hyväksy elementti**, pidä sitä sitten valittuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse lopuksi **Ominaisuudet**.
7.  Voit lisätä työkohteen ohjeita seuraavasti:

    1.  Valitse **Tehtävä** ja sitten **Hierarkia** tehtävätyyppi-kohdasta.
    2.  Valitse **Hierarkia**-vaihtoehdoista **Määritettävä hierarkia**.
    3.  Lisää pysäytysehto ja sulje sivu.

8.  Täytä lisäohjeet (muita varoituksia ei tule olla).
9.  Valitse **Tallenna ja sulje**. Aktivoi uusi työnkulku valitsemalla **Aktivoi** aukeavasta valintaikkunasta.
10. Siirry kohtaan **Henkilöstöhallinto** &gt; **Toimet** &gt; **Positiohierarkiatyypit**.
11. Valitse **Matriisi**.
12. Lisää **työntekijän tunnusnumero** -työnkulku luetteloon.

## <a name="additional-resources"></a>Lisäresurssit

[Osoitemuutosten tarkasteleminen ja hallinta](hr-personnel-view-address-changes.md) 





[!INCLUDE[footer-include](../includes/footer-banner.md)]
