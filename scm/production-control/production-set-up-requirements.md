---
title: Tuotantoasetusten vaatimukset
description: "Tässä artikkelissa on tietoja asetuksista, jotka on tehtävä ennen tuotannonhallinnan aloittamista."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f34def96ea3b8fd6a8bd015cd120adf87d443285
ms.lasthandoff: 03/31/2017


---

# <a name="production-setup-requirements"></a>Tuotantoasetusten vaatimukset

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on tietoja asetuksista, jotka on tehtävä ennen tuotannonhallinnan aloittamista. 

Tuotannonhallinta on integroitu muiden moduulien ominaisuuksien kanssa. Siksi voit muuttaa tuotantotilauksia ja varmistaa, että ne päivitetään automaattisesti järjestelmän kaikissa muissa liittyvissä prosesseissa ja laskutoimituksissa. Seuraavat määritysprosessit käsitellään siinä järjestyksessä, missä ne on tehtävä.

## <a name="required-baseline-setup-in-other-modules"></a>Muiden moduulien pakolliset perusasetukset
Seuraavat tiedot on määritettävä muissa moduuleissa, ennen kuin voit käyttää tuotannonhallintaa. Nämä asetukset sisältävät seuraavat tehtävät:

-   Määritä yrityksen yleiset tiedot.
-   Määritä kirjanpito.
-   Määritä nimikeryhmät.
-   Määritä nimikeryhmien kirjanpitotilit.
-   Määritä varastonimikkeiden taulu inventoinnin- ja varastonhallinnassa.
-   Luo tuoterakenteet ja tuoterakenneversiot inventoinnin- ja varastonhallinnassa.

## <a name="required-calendar-and-resource-setup"></a>Kalenterin ja resurssin pakolliset asetukset
Avaa ennen tuotannonhallinnan käyttöä Organisaation hallinto. Luo ja määritä siellä kalenteri ja operatiiviset resurssit seuraavassa järjestyksessä:

1.  **Työaikamallit** – määritä tuotannon ajoituksessa käytettävissä olevat ajat määrittämällä työaikamallit.
2.  **Kalenterit** – määritä tuotannon ajoituksessa käytettävissä olevat päivät määrittämällä työaikakalenterit.
3.  **Resurssiryhmät** – Ryhmitä operatiiviset resurssit resurssiryhmiksi. Saat tällä tavoin yleiskuvan vapaasta kapasiteetista, kun suoritat aikataulutuksen. Resurssiryhmiä ei tarvitse määrittää ennen operatiivisten resurssien määrittämistä. Resurssien ryhmittäminen on kuitenkin hyvä osata tuotannonhallintaa määritettäessä.
4.  **Resurssit** – määritä tuotantoprosessin suorittamisessa ja kapasiteettisuunnittelussa käytettävät resurssit määrittämällä operatiiviset resurssit.

## <a name="required-production-parameters-setup"></a>Pakolliset tuotantoparametrien asetukset
**Tuotannonhallinnan parametrit** – Määritä tuotannon perusparametrit, joiden mukaisesti järjestelmä käsittelee tuotantotilaukset. Määritä, miten tuotantotilaukset luodaan, arvioidaan, ajoitetaan ja kulutetaan. Voit myös valita, millaista palautetta haluat ja miten kustannuslaskenta tehdään.

## <a name="required-journal-name-identification"></a>Pakollinen kirjauskansion nimen tunnus
**Tuotantokirjauskansioiden nimet** – Määritä tapahtumien kirjaamiseen käytettyjen tuotantokirjauskansioiden nimet.

## <a name="setup-if-you-use-operations"></a>Työvaiheita käytettäessä tarvittavat asetukset
Työvaiheet ilmaisevat tuotteen valmistuksessa suoritettavia tehtäviä. **Huomautus:** Sinun on tiedettävä nimekkeen tuottamisessa tarvittavat tehtävät ja kyseisten tehtävien prioriteetit. Lisäksi sinun tiedettävä, mitä resursseja käytetään ja kuinka paljon niitä käytetään.

1.  **Työvaiheet** – määritä työvaiheet, jotka ilmaisevat valmiin nimikkeen tuotannossa suoritettavat tehtävät.
2.  **Suhteet** – Muodosta omaisuudet määrittämällä työvaiheiden suhteet. Voit määrittää työvaiheiden suhteet valitsemalla **Työvaiheet**-sivulla **Suhteet**.

## <a name="setup-if-you-use-routes"></a>Reitityksiä käytettäessä tarvittavat asetukset
Jos käytät reitityksiä, jokaiselle tuotantoreititykselle on määritettävä työvaiheet. Reititys kuvaa, miten nimike etenee työvaiheesta toiseen tuotantoprosessin alusta loppuun.

1.  **Kustannusluokat** – määritä kustannusluokat, joiden mukaan määritettyjen prosessien tuntikustannukset ja asetusajat muodostuvat.
2.  **Kustannusryhmät** – luo ja ylläpidä eri kustannuslaskennan tyyppejä määrittämällä kustannusryhmiä.
3.  **Reititysryhmät** – Määritä reititysryhmien avulla reititysten ryhmiin liittyvät parametrit. Reititysryhmät on määritettävä ennen tuotantoreititysten luontia.
4.  **Reitit** – määritä ensin tuotantoreititykset ja reitityksen työvaiheiden oletusasetukset, joilla hallitaan ajoitusta, kustannuslaskentaa ja hinnoittelua sekä tilaraporttia.
5.  **Reitit** – ota tuotannon nimikevariaatiot käyttöön määrittämällä reititysversiot.

## <a name="optional-advanced-settings"></a>Valinnaiset lisäasetukset
1.  **Tuotantoryhmät** – Määritä tuotantoryhmät luomaan tuotetilausten ja kirjanpitotilien väliset suhteet. Kirjanpitotileillä tilaukset kirjataan tai ryhmitetään raportointia varten.
2.  **Tuotantopoolit** – luo tuotantopooleja, joilla tuotantotilauksia ryhmitellään kiireellisten tuotantotilausten käsittelyä varten tai tilausryhmien poistamista ja kirjaamista varten.
3.  **Ominaisuudet** – Määritä ominaisuudet luomaan erityismääritteet, jotka resursseille määritettyinä ohjaavat tuotantojen tilausta. Nämä määritteet on yhdistetty työaikamalliin.





