---
title: Työntekijän otsikon ohjausobjekti
description: Tässä artikkelissa on tietoja Henkilöt-keskittimen Työntekijän itsepalvelu -sivun ja Microsoft Dynamics 365 Human Resourcesin Työntekijä-sivun mukautetun otsikon ohjausobjektista.
author: twheeloc
ms.date: 09/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2867a952df79161aaee657dbc3df1f3298294dd5
ms.sourcegitcommit: 167f73a834629752c6b79c312d744e52df7f0927
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445945"
---
# <a name="worker-header-control"></a>Työntekijän otsikon ohjausobjekti

Microsoft Dynamics 365 Human Resources määrittää **Henkilöt**-keskittimen **Työntekijän itsepalvelu** -sivun ja tehostetun **Työntekijä**-sivun mukautettavan otsikon ohjausobjektin. Otsikko sisältää työntekijää koskevia tärkeitä tietoja ja myös yhdellä napsautuksella toimivia toimintoja, kuten sähköposti- ja muiden viestien lähettämisen ja puhelut. Otsikkoa voidaan muokata poistamalla kenttiä tai lisäämällä kenttiä, myös mukautettuja kenttiä. Kenttien avulla voidaan esittää lisätietoja. Jos haluat käyttää uutta otsikon ohjausobjektia, siirry **Ominaisuuksien hallinta** -kohtaan ja ota käyttöön **Työntekijän otsikon ohjausobjekti** -ominaisuus.

## <a name="personalization"></a>Mukauttaminen

Eräs työntekijän otsikon ohjausobjektin tärkeimpiä etuja on otsikkoon näkyviin tulevien tietojen mukauttaminen.

Otsikon oikeassa yläosassa on kolmen kentän ryhmä, jossa näkyy erilaisia tietoja työntekijän tilasta riippuen. Tätä kenttäryhmää kutsutaan otsikon Valokeila-osaksi. Voit mukauttaa otsikon Valokeila-osan poistamalla nykyisiä kenttiä tai lisäämällä kenttiä. Kentät, jotka voidaan lisätä otsikon ohjausobjektin Valokeila-osaan, ovat erilaisia **Työntekijän itsepalvelu** -sivulla, **Henkilöt**-keskittimessä ja **Työntekijä**-sivulla.

## <a name="employee-self-service"></a>Työntekijän itsepalvelu

**Työntekijän itsepalvelu** -sivun työntekijän otsikko sisältää seuraavat tiedot:

- Työntekijän nimi
- Henkilöstönumero
- Toimen nimike
- Osastot
- Työntekijätyyppi
- Työsuhteen yritys
- Palveluvuodet
- Esimies
- Toimityyppi

Otsikko sisältää myös yhdellä napsautuksella toimivan toiminnon henkilön henkilökohtaisten tietojen muokkaamista varten. Valitse **Muokkaa henkilökohtaisia tietoja**, jos haluat avata **Henkilökohtaiset tiedot** -sivun **Työntekijän itsepalvelu** -osassa.

## <a name="people-hub"></a>Ihmiset

Työntekijän otsikko **Henkilöt**-keskittimessä (**Henkilöiden työtila** -sivulla) sisältää seuraavat tiedot:

- Työntekijän nimi
- Henkilöstönumero
- Toimen nimike
- Osastot
- Työntekijätyyppi
- Työsuhteen yritys
- Palveluvuodet
- Esimies
- Toimityyppi

Otsikko sisältää myös yhdellä napsautuksella toimivia toimintoja, kuten sähköposti- ja muiden viestien lähettäminen ja puhelut. Jos käyttäjä tarkastelee omia tietojaan **Henkilön työtila** -sivulla, yhdellä napsautuksella toimivan toiminnon osa sisältää **Muokkaa henkilökohtaisia tietoja** -painikkeen. Käyttäjä voi valita tämän painikkeen avatakseen **Henkilökohtaiset tiedot** -sivun **Työntekijän itsepalvelu** -osassa.

## <a name="streamlined-worker-page"></a>Tehostettu Työntekijä-sivu

Tehostetun **Työntekijä**-sivun työntekijän otsikko sisältää seuraavat tiedot:

- Työntekijän nimi
- Henkilöstönumero
- Toimen nimike
- Osastot
- Työntekijätyyppi
- Työsuhteen yritys

Otsikko sisältää erilaisia tietoja työntekijän tilasta riippuen. Jos esimerkiksi työntekijä on lopettanut työskentelyn yrityksessä, otsikon ohjausobjektissa on **Lopettanut**-merkki, työsuhteen päättymispäivä ja lopettamisen syy.

Alla olevassa taulukossa näkyvät tiedot, jotka näkyvät otsikossa, jossa on eri työntekijöiden tilat.

| Työntekijän tilanneraportti | Näytettävät tiedot | Muistiinpano |
|-----------------|--------------------|------|
| Odottava | <ul><li>Nimi</li><li>Henkilöstönumero</li><li>Toimen nimike</li><li>Osasto</li><li>Työntekijätyyppi</li><li>Yritys</li><li>Odottaa-merkki</li><li>Aloituspäivämäärä</li><li>Raportoi:</li><li>Toimityyppi</li></ul> | |
| Palkattu äskettäin | <ul><li>Nimi</li><li>Henkilöstönumero</li><li>Toimen nimike</li><li>Osasto</li><li>Työntekijätyyppi</li><li>Yritys</li><li>Palkattu äskettäin -merkki</li><li>Palveluvuodet</li><li>Raportoi:</li><li>Toimityyppi</li></ul> | Oletusarvoisesti **Palkattu äskettäin** -merkki näkyy työntekijöille, jotka on palkattu edellisten seitsemän päivän aikana. Jos haluat muuttaa tätä asetusta, määritä aikaväli **Äskettäin palkattujen päivämääräalue** -osaan **Henkilöstöhallinnon parametrit** -sivun **Yleiset**-välilehdessä. Jos haluat esimerkiksi nähdä edellisen 14 päivän aikana palkattujen työntekijöiden **Palkattu äskettäin** -merkin, määritä **Kausi**-kentän arvoksi **14** ja **Yksikkö**-kentän arvoksi **Päivät**. |
| Aktiivinen työntekijä | <ul><li>Nimi</li><li>Henkilöstönumero</li><li>Toimen nimike</li><li>Osasto</li><li>Työntekijätyyppi</li><li>Yritys</li><li>Aloituspäivämäärä</li><li>Raportoi:</li><li>Toimityyppi</li></ul> | |
| Lopettaa | <ul><li>Nimi</li><li>Henkilöstönumero</li><li>Toimen nimike</li><li>Osasto</li><li>Työntekijätyyppi</li><li>Yritys</li><li>Lopettaa-merkki</li><li>Palveluvuodet</li><li>Raportoi:</li><li>Toimityyppi</li></ul> | Oletusarvoisesti **Lopettaa**-merkki näkyy työntekijöillä, jotka lähtevät yrityksestä seitsemän päivän kuluessa. Jos haluat muuttaa tätä asetusta, määritä aikaväli **Lopettavien työntekijöiden päivämääräalue** -osaan **Henkilöstöhallinnon parametrit** -sivun **Yleiset**-välilehdessä. Jos haluat esimerkiksi nähdä seuraavien 14 päivän aikana lähtevien työntekijöiden **Lopettaa**-merkin, määritä **Kausi**-kentän arvoksi **14** ja **Yksikkö**-kentän arvoksi **Päivät**. |
| Lopettaneet | <ul><li>Lopettanut-merkki</li><li>Henkilöstönumero</li><li>Työsuhteen päättymispäivämäärä</li><li>Syykoodi</li></ul> | Oletusarvoisesti **Lopettanut**-merkki näkyy työntekijöillä, jotka ovat lähteneet yrityksestä edellisten päivän aikana. Jos haluat muuttaa tätä asetusta, määritä aikaväli **Lopettaneiden työntekijöiden päivämääräalue** -osaan **Henkilöstöhallinnon parametrit** -sivun **Yleiset**-välilehdessä. Jos haluat esimerkiksi nähdä edellisten 14 päivän aikana lähteneiden työntekijöiden **Lopettanut**-merkin, määritä **Kausi**-kentän arvoksi **14** ja **Yksikkö**-kentän arvoksi **Päivät**. |
