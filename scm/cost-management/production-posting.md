---
title: Tuotannon kirjaus
description: "Tässä artikkelissa on tietoja tuotantoprosessin erityyppisistä kirjauksista."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventItemGroup, ProjCategory, WrkCtrResourceGroup, WrkCtrTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 54591
ms.assetid: 0917fe64-f643-46ae-98ff-5013b266a067
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4a400463c4b84ac8e3e5300bd710fb330458cafd
ms.lasthandoff: 03/31/2017


---

# <a name="production-posting"></a>Tuotannon kirjaus

Tässä artikkelissa on tietoja tuotantoprosessin erityyppisistä kirjauksista.

Tuotannon kirjaustoiminnot seuraavat tuotantoprosesseja, jotka kuvataan seuraavissa osissa.

## <a name="material-consumption"></a>Materiaalikulutus
Materiaalit kirjataan kulutetuiksi tuotannon aikana, kun tuotannon keräysluettelon kirjauskansio kirjataan. Tämä prosessi luo ottotapahtumia, jotka vähentävät käytettävissä olevaa varastoa. Tuotannon parametreja, voidaan määrittää, onko arvo raaka-aineista, jotka ovat meneillään (keskeneräinen työ \[KET\]) kirjataan kirjanpitoon. Keskeneräisissä töissä (KET) käytettävien raaka-aineiden arvo kirjataan sitten kohdistettuun Keräysluettelon tiliin sekä kohdistettuun Keräysluettelon vastatiliin.

## <a name="time-consumption"></a>käytetty aika.
Reitityskorttikirjauskansioon tai työkorttikirjauskansion kirjataan aika, jonka työntekijät käyttävät tuotantotöihin. Kun nämä kirjauskansiot kirjataan, järjestelmä suorittaa kirjauksen keskeneräisiin töihin (KET) kuuluvien resurssien kohdennetulle tilille. Tämä kirjaus edustaa tuotantotilaukseen kuluvalle ajalle kuuluvaa arvoa. Kun tuotantotilaus kirjataan päättyneeksi, KET-tilit täsmäytetään.

## <a name="reporting-finished-goods-and-error-quantities"></a>Valmiiden tuotteiden ja virheiden määrien raportointi
Kun tuotantotilaus ilmoitetaan valmiiksi, valmiiden tavaroiden määrä päivitetään Varastonhallintaan Ilmoitettu valmiiksi -kirjauskansion kautta. Jos käytät keskeneräisten töiden (KET) kirjanpitoa, jonka voit määrittää tuotannon parametreissä, kirjanpidon kirjauskansio tehdään vähentämään KET-tilejä ja lisäämään valmiiden tavaroiden varastoa. Kirjauskansio käyttää tuotteelle määritettyä vakiokustannusta.

## <a name="ending-the-production-order"></a>Tuotantotilauksen päättäminen
Ennen tuotantotilauksen lopettamista lasketaan tuotetun määrän toteutuneet kustannukset. Kaikki arvioidut materiaali-, työ- ja yleiskustannukset palautetaan ja korvataan toteutuneilla kustannuksilla. Valmiin nimikkeen kokonaiskustannukset veloitetaan varaston Vastaanotto-tililtä ja hyvitetään varaston Otot-tilille. Jos valitset **Lopeta työ** -valintaruudun suorittaessasi kustannuslaskennan, tuotantotilauksen tilaksi vaihdetaan **Päättynyt**. Tämä tila estää lisäkustannusten kirjaamisen vahingossa valmiiseen tuotantotilaukseen. Voit määrittää arvo, joka on valmiiksi raportoinnin aikana virheelliset määrät olisi jaettava hyvä määriin, jotka on ilmoitettu valmiiksi. Vaihtoehtoisesti voit määrittää, että virheelliset määrät kirjataan kohdistetulle hävikkitilille.

## <a name="controlling-the-level-of-ledger-posting"></a>Kirjanpitokirjausten tason hallinta
**Tuotannonhallinnan parametrit** -osassa on mahdollista käyttää **Kirjaus kirjanpitoon** -kenttää määrittämään tuotantoprosessien kirjanpitokirjausten taso. Käytettävissä ovat seuraavat arvot:

-   **Nimike ja resurssi** – Käytä kirjanpitotilejä, jotka on määritetty raaka-aineiden ja valmiiden tuotteiden nimikeryhmille. KET-ajan kulutus haetaan resurssin tai resurssiryhmän reititystyövaiheista.
-   **Nimike ja luokka** – Käytä kirjanpitotilejä, jotka on määritetty raaka-aineiden ja valmiiden tuotteiden nimikeryhmille. KET-ajan kulutus haetaan reitityksen työvaiheisiin liitetyistä kustannusluokista.
-   **Tuotantoryhmät** – Käytä kirjanpitotilejä, jotka on määritetty sekä materiaalien että ajan kulutuksen tuotantoryhmille. Tuotannon ryhmät liitetään julkaistuihin tuotteisiin ja kopioidaan tuotantotilauksiin, kun tilaukset luodaan. Tuotantotilausten kirjaus seuraa siten tuotantotilaukseen liitettyjä tuotantoryhmiä.

**Huomautus:** Jos on käytetty valmiin nimikkeen kustannuslaskennan vakiomenetelmää, se näkyy lopullisista tapahtumista. Jos todellisten kustannusten ja vakiomenetelmän avulla laskettujen kustannusten välillä on eroa, se kirjataan tilille tuottona tai tappiona.


