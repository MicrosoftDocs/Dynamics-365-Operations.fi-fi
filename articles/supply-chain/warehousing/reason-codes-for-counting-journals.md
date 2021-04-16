---
title: Varastoinventoinnin syykoodit
description: Tässä ohjeaiheessa käsitellään inventointitehtävin syykoodin määrittämistä ja käyttämistä.
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: a6b8a686b6aee6b52b3f43caf8acae9f371f8804
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838199"
---
# <a name="reason-codes-for-inventory-counting"></a>Varastoinventoinnin syykoodit

[!include [banner](../includes/banner.md)]

Syykoodien avulla voit analysoida inventointiprosessin tuloksia ja prosessin aikana mahdollisesti esiintyviä ristiriitoja. Voit määrittää inventoinnin syyn, kuten vioittuneen kuormalavan tai varasto-otantaan perustuvan varasto-oikaisun.

## <a name="recommendation"></a>Suositus

Ennen järjestelmän määrittämistä kannattaa määrittää syykoodien käyttöstrategia. Yritä vastata esimerkiksi seuraaviin kysymyksiin:

- Pitäisikö syykoodien olla pakollisia varastoissa?
- Pitäisikö syykoodien käytön olla pakollista vai valinnaista joidenkin nimikkeiden kanssa?
- Kuinka monta syykoodia tarvitaan?
- Pitäisikö viivakoodinlukijoiden käyttäjien käyttää syykoodeja? Pitäisikö syykoodien olla ennalta valittuja, pakollisia tai ei-muokattavissa?
- Tarvitsevatko varastotyöntekijät syykoodin, jotka toimivat eri tavalla mobiililaitteissa? Jos vastaus on myönteinen, voit luoda lisää valikkokohteita ja määrittää ne eri henkilöille.

## <a name="where-reason-codes-apply"></a>Syykoodien käyttökohteet

Voit luoda useita syykoodikäytäntöjä. Kullakin syykoodikäytännöllä voi olla kaksi inventoinnin syykoodikäytäntöä. Inventoinnin syykoodikäytäntöjä voidaan käyttää varasto- tai nimiketasolla.

## <a name="set-up-reason-code-policies"></a>Syykoodikäytäntöjen määrittäminen

1. Valitse **Inventoinnin- ja varastonhallinta** \> **Asetukset** \> **Varasto** \> **Inventoinnin syykoodin käytännöt** ja luo uusi syykoodin käytäntö.
2. Valitse **Inventoinnin syykoodin tyyppi** -kentässä joko **Pakollinen** tai **Valinnainen**. Voit määrittää tällä tavoin, onko syykoodin valinta valinnaista vai pakollista jossakin seuraavista inventointikirjauskansioissa:

    - Inventointi (mobiililaite)
    - Pistoinventointi (mobiililaite)
    - Rajainventointi (mobiililaite)
    - Oikaisu sisään (mobiililaite)
    - Oikaisu ulos (mobiililaite)
    - Inventointikirjauskansio (raskas asiakas)

Voit määrittää syykoodit myös yksittäisille varastoille ja tuotteille. Tuotteiden syykoodiasetukset voivat ohittaa varastojen asetukset.

## <a name="mandatory-reason-codes"></a>Pakolliset syykoodit

Jos **Pakollinen**-parametri on määritetty varastojen tai nimikkeiden syykoodeissa, inventointikirjauskansiota ei voi viimeistellä ja sulkea, ennen kuin syykoodi on annettu.

### <a name="set-up-reason-codes-for-warehouses"></a>Varastojen syykoodien määrittäminen

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Varastoerittely** \> **Varastot**.
2. Valitse **Varasto**-välilehden **Inventoinnin syykoodin käytäntö** -kentässä jokin seuraavista vaihtoehdoista:

    - **Tyhjä** – nimikkeelle määritetty parametri määrittää, ovatko inventointikirjauskansiot pakollisia tuotteelle.
    - **Pakollinen** – varaston inventointikirjauskansiossa on aina käytettävä syykoodia.
    - **Valinnainen** – syykoodi ei ole pakollinen varaston inventointikirjauskansiossa.

### <a name="set-up-reason-codes-for-products"></a>Tuotteiden syykoodien määrittäminen

1. Valitse **Tuotetietojen hallinta** \> **Tuotteet** \> **Vapautetut tuotteet**.
2. Valitse ensin **Tuote**-välilehdessä **Inventoinnin syykoodin käytäntö** ja sitten jokin seuraavista vaihtoehdoista:

    - **Tyhjä** – varastolle määritetty parametri määrittää, ovatko inventointikirjauskansiot pakollisia tuotteelle.
    - **Pakollinen** – Tuotteen inventointikirjauskansiossa on aina käytettävä syykoodia. Tämä asetus ohittaa varastotason syykoodiasetuksen.
    - **Valinnainen** – syykoodi ei ole pakollinen tuotteen inventointikirjauskansiossa. Tämä asetus ohittaa varastotason syykoodiasetuksen.

### <a name="use-reason-codes-in-counting-journals"></a>Syykoodien käyttäminen inventointikirjauskansioissa

Voit lisätä inventointikirjauskansiossa syykoodit seuraaville inventointityypeille:

- Inventointi
- Pistoinventointi
- Rajainventointi
- Oikaisu sisään
- Oikaisu ulos

Syykoodit lisätään **Inventointikirjauskansio**-tyypin inventointikirjauskansioiden riveille.

1. Valitse **Inventoinnin- ja varastonhallinta** \> **Kirjauskansioviennit** \> **Inventointi** \> **Inventointi**.
2. Valitse vaihtoehto inventointikirjauskansion tietojen **Inventoinnin syykoodi** -kentässä.

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a>Inventointihistorian näyttäminen syykoodien mukaan kirjattuna

- Valitse ensin **Inventoinnin- ja varastonhallinta** \> **Kyselyt ja raportit** \> **Inventointihistoria** ja sitten tarkastele sitten **Inventoinnin syykoodi** -kentässä syykoodin kautta kirjattua inventointihistoriaa.

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a>Määrän muutoksen syykoodin käyttäminen

1. Valitse **Käytettävissä oleva varasto** -sivulla **Säädä määrää**. Voit avata **Käytettävissä oleva varasto** -sivu useilla eri tavoilla. Valitse esimerkiksi **Inventoinnin- ja varastonhallinta** \> **Kyselyt ja raportit** \> **Käytettävissä oleva varasto**.
2. Valitse ensin **Säädä määrää** ja sitten **Inventoinnin syykoodi** -kentässä syykoodi.

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a>Mobiililaitteen valikkovaihtoehtojen syykoodien määrittäminen

Voit määrittää syykoodit mille tahansa mobiililaitteen valikkoehdon inventointityypille. Mobiililaitteen valikkovaihtoehdon määritys sisältää seuraavat tiedot:

- Syykoodin mahdollinen näyttäminen mobiililaitteen käyttäjälle inventoinnin aikana.
- Mobiililaitteen valikkovaihtoehdossa näytettävä oletussyykoodi.
- Käyttäjän tekemä syykoodin mahdollinen muokkaus.

### <a name="set-up-reason-codes-on-a-mobile-device"></a>Syykoodien määrittäminen mobiililaitteessa

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Mobiililaite** \> **Mobiililaitteen valikkovaihtoehdot**.
2. Valitse **Inventointi**-välilehdessä **Inventointi**.
3. Määritä **Inventoinnin oletussyykoodi** -kentässä oletussyykoodi, joka on kirjattava, kun inventointi tehdään käyttämällä mobiililaitteen valikkovaihtoehtoa.
4. Valitse **Näytä inventoinnin syykoodi** -kentässä **Rivi** näyttämään syykoodi, kun kukin varianssi on kirjattu. Vaihtoehtoisesti voit valita **Piilota**, jos syykoodia ei näytetä.
5. Valitse **Muokkaa inventoinnin syykoodia** -asetukseksi joko **Kyllä** tai **Ei**. Jos valitse tässä asetuksessa **Kyllä**, työntekijä voi muokata syykoodia, kun se näytetään mobiililaitteessa inventoinnin aikana.

> [!NOTE]
> **Inventointi**-painike voidaan ottaa käyttöön missä tahansa mobiililaitteen valikkovaihtoehdossa, jos inventointi voidaan tehdä. Esimerkissä on pistoinventoinnin, käyttäjän ohjaaman työn ja järjestelmän ohjaaman työn valikkovaihtoehtoja.

## <a name="cycle-count-approvals"></a>Inventoinnin hyväksynnät

Käyttäjä voi muuttaa inventointiin liitettyä syykoodia ennen inventoinnin hyväksymistä. Kun inventointi on hyväksytty, syykoodi annetaan inventointikirjauskansion riveille.

### <a name="modify-cycle-count-approvals"></a>Inventoinnin hyväksymisten muokkaaminen

1. Valitse **Varastonhallinta** \> **Inventointi** \> **Tarkistusta odottava inventointityö**.
2. Valitse ensin **Inventointi** ja sitten **Syykoodi**-kentässä uusi syykoodi.

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a>Mobiililaitteen Oikaisu sisään- ja Oikaisu ulos -valikkovaihtoehdon muokkaaminen

1. Valitse ensin **Varastonhallinta** \> **Asetukset** \> **Mobiililaite** \> **Mobiililaitteen valikkovaihtoehdot** ja sitten **Oikaisu sisään ja ulos**.
2. Valitse **Käytä nykyistä työtä** -vaihtoehdossa **Ei**.
3. Valitse **Työn luontiprosessi** -kentässä **Oikaisu sisään**.

Seuraavat kentät lisätään mobiililaitteen valikkovaihtoehtoon, kun **Oikaisu sisään** tai **Oikaisu ulos** valitaan työn luontiprosessin aikana:

- Inventoinnin oletussyykoodi
- Näytä inventoinnin syykoodi
- Muokkaa inventoinnin syykoodia


[!INCLUDE[footer-include](../../includes/footer-banner.md)]