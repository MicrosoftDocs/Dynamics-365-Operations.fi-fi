---
title: Projektiresurssien määrittäminen
description: Tässä aiheessa on tietoja projektin resurssien määrittämisestä ja pyytämisestä.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760538"
---
# <a name="set-up-project-resources"></a>Projektiresurssien määrittäminen

[!include [banner](../includes/banner.md)]

Sinun täytyy määrittää kalenteri ja liittää se työntekijään. Kalenterin avulla aikataulutetaan projekti ja siihen varattujen resurssien työaika. Kalenteria määrittäessään projektipäälliköt voivat suorittaa resurssien tasaamisen resurssien optimoinnin yhteydessä. Kalenterin aikataulun perusteella resursseille voidaan asettaa rajoituksia. Voit määrittää kalenterin **Kalenterit**-sivulla.

Työntekijän projektin resurssiksi määrittäessäsi voit valita sen yrityksen työntekijät, jolle resursseja määritetään. Voit vaihtoehtoisesti valita työntekijät muista organisaation yrityksistä. Nämä työntekijät ovat konsernin sisäisiä resursseja.

Seuraavissa ohjeissa selitetään, miten työntekijä määritetään yrityksen projektiin resurssiksi ja miten konsernin sisäinen projektin resurssi määritetään.

## <a name="set-up-a-worker-as-a-project-resource"></a>Työntekijän määrittäminen projektiresurssiksi

1. Valitse **Työntekijät**-sivun **Työntekijät**-luettelosta työntekijä, jonka haluat lisätä projektiin resurssiksi, ja avaa haluamasi työntekijätietue.
2. Valitse toimintoruudussa **Projekti** &gt; **Asetukset** &gt; **Projektiasetukset**.
3. Valitse kalenteri ja sulje sivu.

Voit myös määrittää resurssille oletusprojektit eräänlaisena esimäärityksenä. Esimäärityksiä voidaan käyttää, kun resurssi- tai projektipäällikkö tietää jo etukäteen, missä projekteissa resurssi työskentelee. Esimääritykset voivat perustua myös projektin sponsorin tai asiakkaan pyyntöön. Jos haluat esimäärittää projektin, valitse **Määritä projektit** -sivulta **Projektit**-välilehdestä **Jäljellä olevat projektit** -luettelosta haluamasi projekti.

## <a name="set-up-an-intercompany-resource"></a>Konsernin sisäisen resurssin määrittäminen

Kun määrität työntekijää konsernin sisäiseksi resurssiksi, määritä tiedot yrityksestä, joka antaa resurssin lainaksi ja yrityksestä, joka ottaa resurssin lainaksi.

### <a name="in-the-lending-company"></a>Yritys, joka antaa resurssin lainaksi

1. Varmista Financessa, että resurssin lainaava yritys on valittu. Tee sitten toimenpiteet, jotka on mainittu edellä olevassa kohdassa "Työntekijän määrittäminen projektiresurssiksi".
2. Valitse **Konsernin sisäinen kirjanpito** -sivulla **Uusi**.
3. **Yrityksen tunnus** -kenttään yritys, jolta resurssi lainataan. Anna tarvittavat tiedot muihin kenttiin ja valitse sitten **Tallenna**.
4. Valitse **Siirtohinta** -sivulla **Uusi**.
5. **Lainaava yritys** -kenttään asianmukainen yritys.
6. Jos haluat lainata lainaavalle yritykselle vain resurssin, jonka loit tämän osan alussa, valitse **Resurssi**-kentässä luomasi resurssin nimi. Jos haluat, että kaikki lainan antavan yrityksen resurssit ovat lainaavan yrityksen käytettävissä, jätä **Resurssi**-kenttä tyhjäksi.
7. Määritä **Projektinhallinnan ja kirjanpidon parametrit** -sivun **Konsernin sisäinen** -välilehden **Ota käyttöön konsernin sisäinen resurssien ajoitus ja aikaraportit** -asetuksen arvoksi **Kyllä**.

### <a name="in-the-borrowing-company"></a>Yritys, joka lainaa resurssin

- Syötä **Resurssiluettelo**-sivun hakusuodattimeen sille yritykselle luomasi resurssin nimi, jolta resurssi lainataan. Varmista, että nimi löytyy sen yrityksen resurssiluettelosta, jolle resurssi lainataan.

## <a name="request-project-resources"></a>Projektiresurssien pyytäminen
Projektiresurssin ajoitustoiminto tukee vain resurssipäälliköitä, jotka jakavat henkilöllisiä resursseja sitoumuksiin tai projekteihin. Tämä toiminto otetaan käyttöön suorittamalla seuraavat tehtävät valmiiksi tai varmistamalla, että ne on suoritettu:

- Määritä numerosarjat.
- Määritä projektinhallinnan ja kirjanpidon työnkulut.
- Ota resurssipyynnön työnkulut käyttöön.

Kun edeltävät tehtävät on suoritettu, voit suorittaa seuraavat tehtävät tarvittaessa:

- Luo resurssipyyntö alustavasti varatusta henkilöllisestä resurssista.
- Seuraa resurssipyyntöjä.
- Täytä resurssipyynnöt.
- Pyydä henkilöllistä resurssia työrakenteesta.
- Varaa projektin resurssit ilman henkilöllisen resurssin pyyntöä.
