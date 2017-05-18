---
title: "Työntekijätietojen hallinta työnkulkujen avulla"
description: "Tässä ohjeaiheessa kerrotaan, henkilöstöhallinnon työnkulkuja käytetään työntekijätietojen hallintaan. Voit esimerkiksi liittää työnkulun toimeen ja määrittää hyväksynnän työnkulun, joka käynnistyy, kun työntekijät muuttavat tietuettaan."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: a03b9aa61d754b47905d86114e0da29f1da64b81
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="use-workflows-to-manage-employee-information"></a>Työntekijätietojen hallinta työnkulkujen avulla

[!include[banner](includes/banner.md)]


Tässä ohjeaiheessa kerrotaan, henkilöstöhallinnon työnkulkuja käytetään työntekijätietojen hallintaan. Voit esimerkiksi liittää työnkulun toimeen ja määrittää hyväksynnän työnkulun, joka käynnistyy, kun työntekijät muuttavat tietuettaan.

Henkilöstöhallinnon työnkulut sisältävät useita työnkulkuja henkilöstönhallinnon tehtävien hallintaan. Käytettävissä on myös useita vaihtoehtoja tiettyjen työkulkujen muokkaamiseen ja niiden liittämiseen raportointihierarkiaan. Työnkulut auttavat muutosten tekemisessä useisiin, vakiomuotoisiin työntekijätietoihin. Voit liittää työnkulun toimeen. Jos työntekijä muuttaa nyt työntekijätietuettaan, käynnistyy työnkulku, joka edellyttää hyväksynnän ennen, kuin uudet tiedot voidaan tallentaa. Seuraaville tietotyypeille on määritetty työnkulut etukäteen, jotta työntekijätietojen tarkkuuden säilyttäminen ja muutosten hallinta olisi mahdollisimman tehokasta:

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
Voit liittää työnkulun mihin tahansa määrittämääsi hierarkiaan. Jos toimeen liittyy esimerkiksi raportointihierarkian matriisi, voit määrittää työnkulun, joka reitittää kulut tietystä projektista projektin johtajalle toimeen liittyvän työntekijän esimiehen sijasta. Luo uusi työnkulku tai muokkaa aiemmin luotua työnkulkua napsauttamalla **Henkilöstöhallinnan työnkulku** -sivulla **Uusi**. Käynnistä työnkulun suunnittelija valitsemalla luettelosta työnkulku. Voit käyttää suunnittelusovellusta uuden työnkulun luontiin tai muuttaa aiemmin luodun työnkulun vaiheita. Kun muutat aiemmin luotua työnkulkua, muutokset tallennetaan uuteen versioon. Tämän ansiosta voit tarvittaessa palata aiempaan versioon.

## <a name="configure-a-human-resources-workflow"></a>Henkilöstöhallinnon toimien määrittäminen
Seuraa näitä vaiheita määrittääksesi perustyönkulun, joka käynnistetään, kun työntekijät haluavat muuttaa henkilötietojaan.

1.  Valitse **Henkilöstöhallinnon työkulut** -sivulla **Uusi**.
2.  Valitse käytettävien työnkulkujen luettelosta **Tunnusnumerot**.
3.  Käynnistä työnkulun suunnittelusovellus valitsemalla **Suorita** ja kirjoita käyttäjänimesi ja salasanasi pyydettäessä.
4.  Vedä **Hyväksy tunnusnumero** -elementti työnkulun elementtien luettelosta suunnittelusovelluksen alustalle.
5.  Yhdistä hyväksyntäelementti **Alku**- ja **Loppu**-elementteihin.
6.  Kaksoisnapsauta **Hyväksy elementti** -kohtaa sitten valitse **Ominaisuudet**.
7.  Voit lisätä työkohteen ohjeita seuraavasti:
    1.  Valitse **Tehtävä** ja sitten **Hierarkia** tehtävätyyppi-kohdasta.
    2.  Valitse **Hierarkia**-vaihtoehdoista **Määritettävä hierarkia**.
    3.  Lisää pysäytysehto ja sulje sivu.

8.  Täytä lisäohjeet (muita varoituksia ei tule olla).
9.  Valitse **Tallenna ja sulje**. Aktivoi uusi työnkulku valitsemalla **Aktivoi** aukeavasta valintaikkunasta.
10. Siirry kohtaan **Henkilöstöhallinto** &gt; **Toimet** &gt; **Positiohierarkiatyypit**.
11. Valitse **Matriisi**.
12. Lisää **työntekijän tunnusnumero** -työnkulku luetteloon.





