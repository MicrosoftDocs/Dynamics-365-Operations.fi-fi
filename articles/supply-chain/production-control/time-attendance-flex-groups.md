---
title: Liukumaryhmät
description: Tässä ohjeaiheessa liukumaryhmien käyttöä työajan seurannassa.
author: johanhoffmann
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgFlexGroup, JmgFlexCorrection
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c71ebab0788b6c5d7466a5d71e3c72a7e86e41db
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427117"
---
# <a name="flex-groups"></a>Liukumaryhmät

[!include[banner](../includes/banner.md)]

Joustavan työajan ansiosta yritykset voivat vähentää ylityökorvauksien määrää antamalla työtekijöille ylimääräisiä vapaapäiviä silloin, kun työmäärä on vähäinen. Tällä ominaisuudella on käyttöä esimerkiksi niissä segmenteissä, joissa työmäärä vaihtelee kausittain.

Voit käyttää liukumaryhmiä seuraavien työntekijän joustavaa työntekijää koskevien sääntöjen ja periaatteiden määrittämiseen:

- Liukuvan työajan säännöt
- Työntekijän liukumasaldon laskentaperiaate

## <a name="set-up-flexible-working-hours-in-flex-groups"></a>Joustavan työnajan määrittäminen liukumaryhmissä

- Määritä joustavan työajan liukumaryhmät valitsemalla **Työajan seuranta** \> **Asetukset** \> **Ryhmät** \> **Liukumaryhmät**.

## <a name="associate-workers-with-flex-groups"></a>Työntekijöiden liittäminen liukumaryhmiin

- Valitse **Työajan seuranta** \> **Asetukset** \> **Aikarekisteröintityöntekijät**.

## <a name="rules-for-flex-regulations"></a>Liukuvan työajan säännöt

Voit määrittää liukuvan työajan sääntöjen avulla liukuvan työajan rajat tai pienimmän ja suurimman sallitun tuntimäärän työntekijän liukumatilillä. Liukuvan työajan rajat määritetään liukumaryhmässä. Kun liukuvan työajan rajat ylitetään, työntekijän liukumasaldoa ja palkkaa voidaan oikaista.

Jos työntekijän pienin sallittu liukuma ylittyy (eli liukumatilillä olevien tuntien määrä on alle määritetyn vähimmäismäärän), voit oikaista työtekijän liukumasaldon seuraavin keinoin luomalla liukuvan työajan säännön:

- Työntekijän liukumatili voidaan oikaista määritettyyn sallittuun vähimmäismäärään ilman, että työntekijän palkasta vähennetään se tuntimäärä, jolla liukumatili alittaa sallitun vähimmäismäärän.
- Työntekijän palkasta voidaan vähentää se tuntimäärä, jolla liukumatili alittaa sallitun vähimmäismäärän. Tämä vähennys tehdään luomalla maksutapahtuma sellaiselle maksulajille, jolla voi olla negatiivinen tai positiivinen palkkayksikkö.

Jos työntekijän suurin sallittu liukuma ylitetään, voit oikaista työntekijän liukumasaldon seuraavin keinoin luomalla liukuvan työajan säännön:

- Työntekijän liukumatili voidaan oikaista takaisin määritettyyn sallittuun enimmäismäärään ilman, että työntekijälle korvataan se tuntimäärä, jonka työntekijä työskenteli yli sallitun enimmäismäärän.
- Työntekijän sallitun enimmäismäärän ylittävä tuntimäärä voidaan muuntaa palkaksi. Tämä muunnos tehdään luomalla tietyn maksulajin maksutapahtumia.

Voit oikaista liukumasaldon seuraavissa tilanteissa:

- Kun palkanlaskentatietoihin perustuva maksutiedosto viedään **Siirrä maksu** -työn avulla. Palkanlaskentatiedot luodaan, kun siirrät työntekijän rekisteröinnin **Hyväksy**-sivulta.
- Kun **Oikaise liukumasaldot** -työ käsitellään.

> [!NOTE]
> Liukuvan työajan säännöt eivät esiinny **Hyväksy**-sivulla tapahtuvien päivittäisten työntekijän rekisteröintien hyväksymisten ja siirtojen aikana.

## <a name="principle-for-calculating-a-workers-flex-balance"></a>Työntekijän liukumasaldon laskentaperiaate

Periaate, jonka mukaan työtekijän liukumasaldon tuntien oikaisu lasketaan, määritetään liukumaryhmässä. Valitse **Työajan seuranta** \> **Asetukset** \> **Ryhmät** \> **Liukumaryhmät**. 

Käytettävissä on kaksi periaatetta:

- **Aika** – Työntekijän liukumatunnit lasketaan vain työntekijän päivälle rekisteröimästä ajasta. Kun työntekijän päivittäiset rekisteröinnit lasketaan, päivän ylijäämä- ja vajetuntien määrä lasketaan työntekijän aikaprofiilissa määritetyiltä ylijäämä- ja vajealueilta.
- **Maksulajit** – Työntekijän liukumatunnit lasketaan työntekijän maksusopimuksessa määritettyjen ylijäämä- ja vajemaksulajien ansioiden perusteella. Maksusopimus on liitetty aikarekisteröintityöntekijään. Liukumatilejä kannattaa hallita maksulajien avulla esimerkiksi silloin, kun haluat suurentaa työtekijän liukumatiliä tietyllä kertoimella vähintään yhdellä liukuma-alueella.

### <a name="scenario-1-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-minimum-is-exceeded"></a>Skenaario 1: Työntekijän palkan ja liukumatilin oikaisu, koska liukuman sallittu vähimmäismäärä on ylitetty

Työntekijällä, jolla on liukuva työaika, on negatiivinen liukumatili.

- **Liukumatili:** -4

Työntekijä on liitetty liukumaryhmään, jossa on seuraavat määritykset:

- **Liukuma vähintään:** -0,5
- **Vähimmäispalkan tyyppi:** 1302
- **Maksulajikerroin:** -1,00

Kuten työntekijän liukumatilin ja liukuman sallitun vähimmäismäärän erotus osoittaa, työntekijän sallittu vähimmäisliukuva ylittyy 3,5 tunnilla.

Kun palkanlaskennan järjestelmänvalvoja siirtää työntekijän palkkatiedot suorittamalla **Siirrä maksettavaksi**- tai **Liukumaoikaisu**-työn, tehdään seuraavat oikaisut:

- Työntekijän liukumatiliä oikaistaan 3,5 tunnilla. Näin ollen liukumasaldo -4,0 oikaistaan työntekijän liukuman sallittuun vähimmäismäärään -0,5 tuntia.
- Palkkatyypille 1302 luodaan maksukohde. Tällä maksukohteella on palkkayksikkö -3,5 tuntia, jotka vähennetään työntekijän palkasta. Tässä tapauksessa palkkayksikkö on negatiivinen luku, koska positiivinen oikaisu 3,5 on kerrottu liukumaryhmässä määritetyllä negatiivisella maksulajikertoimella -1,0. Tämä maksukohde on osa **Siirrä maksettavaksi** -työn luomaa maksutiedostoa.

### <a name="scenario-2-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-maximum-is-exceeded"></a>Skenaario 2: Työntekijän palkan ja liukumatilin oikaisu, koska liukuman sallittu enimmäismäärä on ylitetty

Työntekijällä, jolla on liukuva työaika, on positiivinen liukumatili.

- **Liukumatili:** 6

Työntekijä on liitetty liukumaryhmään, jossa on seuraavat määritykset:

- **Liukuma enintään:** 2,0
- **Vähimmäispalkan tyyppi:** 1302
- **Maksulajikerroin:** -1,0

Kuten työntekijän liukumatilin ja liukuman sallitun enimmäismäärän erotus osoittaa, työntekijän sallittu enimmäisliukuma ylittyy 4,0 tunnilla.

Kun palkanlaskennan järjestelmänvalvoja siirtää työntekijän palkkatiedot suorittamalla **Siirrä maksettavaksi**- tai **Liukumaoikaisu**-työn, tehdään seuraavat oikaisut:

- Työntekijän liukumatiliä oikaistaan -4,0 tunnilla. Näin ollen liukumasaldo 6,0 oikaistaan työntekijän liukuman sallittuun enimmäismäärään 2,0 tuntia.
- Palkkatyypille 1302 luodaan maksukohde. Tällä maksukohteella on palkkayksikkö 4,0 tuntia, jotka lisätään työntekijän palkkaan. Tässä tapauksessa palkkayksikkö on positiivinen luku, koska negatiivinen oikaisu 4,0 on kerrottu liukumaryhmässä määritetyllä negatiivisella maksulajikertoimella -1,0. Tämä maksukohde on osa **Siirrä maksettavaksi** -työn luomaa maksutiedostoa.

### <a name="scenario-3-managing-a-workers-flex-balance-based-on-pay-types"></a>Skenaario 3: Työntekijän palkkalajeihin perustuvan liukumasaldon hallinta

Kuten aiemmin on selitetty, liukumatilejä voi hallita joko työtekijän aikaprofiilissa määritetyillä ylijäämä- ja vajealueilla rekisteröidyn ajan perusteella tai työntekijän maksusopimuksissa määritettyjen palkkalajien perusteella. Jos käytössä palkkalajit, työntekijän liukumatiliä oikaistaan maksukohteilla, jotka luodaan, kun työtekijän rekisteröinti siirretään **Hyväksy**-sivulta. Liukumatilejä kannattaa hallita maksulajien avulla esimerkiksi silloin, kun haluat suurentaa työtekijän liukumatiliä tietyllä kertoimella vähintään yhdellä liukuma-alueella.

Tämä skenaario käyttää seuraavaa työpäivää edustavaa liukumaprofiilia.

| Profiilin tyyppi  | Alku    | Loppu      |
|---------------|----------|----------|
| Ylijäämä         | 0.00 | 8.00 |
| Saapuminen      | 8.00 | 8.00 |
| Vaje-         | 8.00 | 9.00 |
| Vakioaika | 9.00 | 11.30 |
| Palkallinen tauko    | 11.30 | 12.00 |
| Vaje-         | 12.00 | 16.00 |
| Poistuminen     | 16.00 | 16.00 |
| Ylijäämä         | 16.00 | 00.00 |

Tässä tapauksessa haluat hallita työntekijän liukumasaldoa palkkalajien perusteella. Niinpä sinun on valittava työntekijän liukumaryhmässä **Perustuu palkkalajeihin** -asetukseksi **Kyllä**.

Liukumatuntien huomiointia varten on määritettävä myös uusi palkkalaji. Tässä skenaariossa palkkalajin nimi on **FlexCnt**.

| Maksulaji | kuvaus  |
|----------|--------------|
| FlexCnt  | Liukumalaskuri |

Määritä seuraavaksi palkkalaji seuraavasti ja lisää uuden tyypin rivit palkkaprofiiliin.

1. Valitse ensin **Työajan seuranta** \> **Asetukset** \> **Ryhmät** \> **Liukumaryhmät** ja sitten **Seuraava**.
2. Määritä sekä **Ylijäämä**- että **Vaje**-kentässä uudeksi palkkalajiksi **FlexCnt**.
3. Valitse ensin **Työajan seuranta** \> **Asetukset** \> **Maksusopimukset** ja sitten **Sopimusrivit**.
4. Lisää seuraavat kolme riviä **Ylijäämä**-profiilityypin kohtaan **Maanantai**.

    | Maksulaji | kuvaus  | Alkaen klo | Loppuen klo  | Minimi | Maksimi | Kerroin |
    |----------|--------------|-----------|----------|---------|---------|--------|
    | FlexCnt  | Liukumalaskuri | 0.00  | 18.00 | 00,00   | 00,00   | 1,00   |
    | FlexCnt  | Liukumalaskuri | 18.00  | 0.00 | 00,00   | 2,00   | 1.50   |
    | FlexCnt  | Liukumalaskuri | 18.00  | 0.00 | 2,00   | 6,00   | 2,00   |

    > [!NOTE]
    > Kutakin riviä käytetään eri aikavälille ja kullakin on erilainen kerroin. Työntekijän aikavälillä työskentelemät liukumatunnit kerrotaan kyseisen rivin kertoimella. Jos työtä tehtiin esimerkiksi kello 18.00–20.00, nämä tunnit kerrotaan kertoimella 1,50. Tämä kerroin määritetään **Maksusopimusrivit**-sivun **Yleiset**-välilehden **Kerroin**-kentässä.

Työntekijä antaa seuraavat päivää koskevat rekisteröinnit.

| Kirjauskansion rekisteröintityyppi | Alku    | Loppu      |
|---------------------------|----------|----------|
| Saapuminen                  | 7.00 | 7.00 |
| Tuotannon työ            | 7.00 | 21.00 |
| Poistuminen                 | 21.00 | 21.00 |

Maksettava summa lasketaan **Hyväksy**-sivulla työntekijän rekisteröinnin perusteella. Voit tarkastella tulosta rekisteröinnin laskennan jälkeen **Ajat**-välilehdessä. Tässä skenaariossa kiinnostavia ovat seuraavat kentät:

| Liukuman lisäys | Liukuman vähennys | Aika  | Maksetaan ajasta |
|--------|--------|-------|----------|
| 6,00   | 0,00   | 13,50 | 8,00    |

Ylijäämäajan määrä on kuusi tuntia ja laskenta perustuu aikaprofiilin liukuma-alueeseen. Tämä summa sisältää tunnin ylijäämäaikaa 7.00–8.00 ja viisi tuntia ylijäämäaikaa 16.00–21.00.

Kun siirrät rekisteröinnit, havaitset, että ylijäämäaika on muuttunut 6,0 tunnista 8,0 tunniksi.

| Liukuman lisäys | Liukuman vähennys | Aika  | Maksetaan ajasta |
|--------|--------|-------|----------|
| 8,00   | 0,00   | 13,50 | 8,00    |

Tämä muutos tapahtuu siirron jälkeen, koska liukumatunnit on laskettu palkkalajin eikä ajan perusteella. Seuraavassa taulukossa näytetään, miten kahdeksan tuntia lasketaan.

| Kohteesta     | Asti       | Aika | Kerroin    | Liukumatili |
|----------|----------|------|-----------|--------------|
| 7.00 | 8.00 | 1    | 1         | 1            |
| 16.00 | 18.00 | 2    | 1         | 2            |
| 18.00 | 20.00 | 2    | 1.5       | 3            |
| 20.00 | 21.00 | 1    | 2         | 2            |
|          |          |      | **Yhteensä** | **8**        |
