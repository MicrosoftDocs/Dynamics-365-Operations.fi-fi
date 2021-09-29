---
title: Varastoinventoinnin syykoodit
description: Tässä ohjeaiheessa käsitellään inventointitehtävin syykoodin määrittämistä ja käyttämistä.
author: perlynne
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 4c178ddf342b13a0ef8fee8b8b958554a9a31069
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500587"
---
# <a name="reason-codes-for-inventory-counting"></a>Varastoinventoinnin syykoodit

[!include [banner](../includes/banner.md)]

Syykoodien avulla voit analysoida inventointiprosessin tuloksia ja prosessin aikana mahdollisesti esiintyviä ristiriitoja. Voit määrittää inventoinnin syyn, kuten vioittuneen kuormalavan tai varasto-otantaan perustuvan varasto-oikaisun. Oikaisutoiminnon avulla voit samalla kirjata käytettävissä olevan varaston oikaisujen arvon asianmukaiselle vastatilille kunkin varasto-oikaisun syyn perusteella.

## <a name="recommendation"></a>Suositus

Ennen järjestelmän määrittämistä kannattaa määrittää syykoodien käyttöstrategia. Yritä vastata esimerkiksi seuraaviin kysymyksiin:

- Pitäisikö syykoodien olla pakollisia varastoissa?
- Pitäisikö syykoodien käytön olla pakollista vai valinnaista joidenkin nimikkeiden kanssa?
- Kuinka monta syykoodia tarvitaan?
- Onko oikaisuille ennalta valittava rajallinen syykoodien luettelo?
- Pitäisikö viivakoodinlukijoiden käyttäjien käyttää syykoodeja? Pitäisikö syykoodien olla ennalta valittuja, pakollisia tai ei-muokattavissa?
- Tarvitsevatko varastotyöntekijät syykoodin, jotka toimivat eri tavalla mobiililaitteissa? Jos vastaus on myönteinen, voit luoda lisää valikkokohteita ja määrittää ne eri henkilöille.
- Tuleeko syykoodien käyttää kirjanpidon vastatilikirjauksia?

## <a name="turn-on-reason-code-features-in-your-system"></a>Syykoodiominaisuuksien käyttöönottaminen järjestelmässä

Jos et näe kaikkia tässä aiheessa kuvattuja ominaisuuksia järjestelmässäsi, sinun on todennäköisesti otettava käyttöön *Kirjaa varastosta -oikaisut käyttämällä konfiguroitavissa olevia syykoodeja, jotka on liitetty vastatili* -toiminto. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Ominaisuuden nimi:** *Kirjaa käyttökelpoisia oikaisuja käyttäen vastatileihin liitettyjä konfiguroitavissa olevia syykoodeja*

## <a name="set-up-reason-codes"></a>Syykoodien määrittäminen

### <a name="set-up-reason-code-policies"></a>Syykoodikäytäntöjen määrittäminen

Voit luoda useita syykoodien käytäntöjä, jotka ohjaavat sitä, milloin ja miten inventoinnin syykoodit otetaan käyttöön. Jokaisella syykoodikäytännön syykoodityypillä voi olla kaksi eri inventoinnin syykoodityyppiä (*Valinnainen* tai *pakollinen*). Inventoinnin syykoodikäytäntöjä voidaan käyttää varasto- tai nimiketasolla.

Voit luoda syykoodikäytännön noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta** \> **Määritys** \> **Varasto** \> **Inventoinnin syykoodikäytännöt**.
1. Lisää ruudukkoon uusi käytäntö valitsemalla toimintoruudussa **Uusi**.
1. Määritä uuden käytännön **Nimi**-kenttä.
1. Valitse **Inventoinnin syykoodin tyyppi** -kentässä joko *Pakollinen* tai *Valinnainen*. Voit määrittää tällä tavoin, onko syykoodin valinta valinnaista vai pakollista jossakin seuraavista varastonoikaisuprosesseissa:

    - Inventointi (mobiililaite)
    - Pistoinventointi (mobiililaite)
    - Rajainventointi (mobiililaite)
    - Oikaisu sisään (mobiililaite)
    - Oikaisu ulos (mobiililaite)
    - Inventointikirjauskansio (raskas asiakas)
    - Määrän oikaisu/Online-inventointi (raskas asiakas)

Voit määrittää syykoodit sekä yksittäisille varastoille että tuotteille. Tuotteen syykoodiasetukset voivat ohittaa tuotteen varastoasetukset.

> [!NOTE]
> Varastoille ja tavaroille, joissa **laskentasyykoodin käytäntö** -kenttä on *Pakollinen*, laskentapäiväkirjaa ei voida täyttää ja sulkea ennen kuin syykoodi on annettu. Lisätietoja on seuraavassa osassa.

### <a name="assign-counting-reason-code-policies-to-warehouses"></a>Määritä inventoinnin syykoodikäytännöt varastoille

Voit määrittää varastolle inventoinnin syykoodikäytännön noudattamalla seuraavia ohjeita.

1. Mene kohtaan **Varastonhallinta** \> **Asetukset** \> **Inventaarioanalyysi** \> **Varastot**.
1. Valitse luetteloruudusta varasto.
1. Valitse toimintoruudun **Varasto**-välilehden **Määritys**-ryhmässä **Inventoinnin syykoodikäytäntö**. Tee sitten jokin **Määritä Inventoinnin syykoodikäytäntö** -valintaikkunassa olevista vaihtoehdoista:

    - Määritä kunkin nimikkeen käytäntöasetusten avulla, ovatko inventointikirjauskansiot pakollisia, syöttäen ei arvoa (tai poistamalla olemassa olevaa arvoa).
    - Jos haluat vaatia varaston inventointikirjauskansioiden syykoodin, valitse syykäytäntö, jonka mukaan **Inventoinnin syykoodin tyyppi** -kentän arvoksi on määritetty *Pakollinen*.
    - Jos varaston inventointikirjauskansioiden syykoodi on valinnainen, valitse syykäytäntö, jonka mukaan **Inventoinnin syykoodin tyyppi** -kentän arvoksi on määritetty *Valinnainen*.

### <a name="assign-counting-reason-code-policies-to-products"></a>Määritä inventoinnin syykoodikäytännöt tuotteille

Voit määrittää tuotteelle inventoinnin syykoodikäytännön noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Tuotetietojen hallinta** \> **Tuotteet** \> **Vapautetut tuotteet**.
1. Valitse tuote ruudukossa.
1. Valitse toimintoruudun **Tuote**-välilehden **Määritys**-ryhmässä **Inventoinnin syykoodikäytäntö**. Tee sitten jokin **Määritä Inventoinnin syykoodikäytäntö** -valintaikkunassa olevista vaihtoehdoista:

    - Määritä varaston käytäntöasetusten avulla, ovatko inventointikirjauskansiot pakollisia tuotteelle, syöttäen ei arvoa (tai poistamalla olemassa olevaa arvoa).
    - Jos haluat vaatia tuotteen inventointikirjauskansioiden syykoodin, valitse syykäytäntö, jonka mukaan **Inventoinnin syykoodin tyyppi** -kentän arvoksi on määritetty *Pakollinen*. Tämä asetus ohittaa varastotason syykoodiasetuksen.
    - Jos tuotteen inventointikirjauskansioiden syykoodi on valinnainen, valitse syykäytäntö, jonka mukaan **Inventoinnin syykoodin tyyppi** -kentän arvoksi on määritetty *Valinnainen*. Tämä asetus ohittaa varastotason syykoodiasetuksen.

### <a name="set-up-counting-reason-codes"></a>Inventoinnin syykoodien määrittäminen

Voit määrittää inventoinnin syykoodit seuraavasti.

1. Siirry kohtaan **Varastonhallinta** \> **Määritys** \> **Varasto** \> **Inventoinnin syykoodit**.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.
1. Määritä uuden rivin **Inventoinnin syykoodi**- ja **Kuvaus**-kentät.
1. Voit määrittää vastatilin kirjoittamalla tai valitsemalla arvon **Vastatili**-kentässä.

    > [!NOTE]
    > Jos vastatili liitetään inventoinnin syykoodiin, inventointikirjauskansion käytössä on inventoinnin syykoodi, arvo kirjataan määritetylle vastatilille varaston kirjauksen oletusprofiilitilin asemesta.

### <a name="set-up-counting-reason-code-groups"></a><a name="reason-groups"></a>Inventoinnin syykoodiryhmien määrittäminen

*Inventoinnin syykoodiryhmiä* voidaan käyttää Warehouse Management -mobiilisovelluksen *oikaisu*- ja *korjaus*-valikkojen nimikkeissä inventoinnin syykoodien luettelon rajoittamiseksi. (Lisätietoja inventoinnin syykoodiryhmistä on kohdassa [Määritä kannettavan laitteen valikkovaihtoehdot oikaisua ja korjausta varten](#setup-adjustment-in-out) jäljempänä tässä ohjeaiheessa.)

1. Siirry kohtaan **Varastonhallinta** \> **Määritys** \> **Varasto** \> **Inventoinnin syykoodiryhmät**.
1. Lisää ryhmä valitsemalla toimintoruudussa **Uusi**.
1. Määritä uuden ryhmän **Inventoinnin syyryhmä**- ja **Ryhmän kuvaus** -kentät.
1. Valitse toimintoruudussa **Tallenna**.
1. Valitse **Tiedot**-osassa työkaluriviltä **Uusi** lisätäksesi ruudukkoon rivin. Määritä sitten uuden rivin **Inventoinnin syykoodi** -kenttä. 
1. Lisää koodeja tarpeen mukaan toistamalla edellinen vaihe. Jos sinun on poistettava koodi ryhmästä, valitse koodi ja valitse sitten työkaluriviltä **Poista**.

### <a name="set-up-reason-codes-for-mobile-device-menu-items"></a>Mobiililaitteen valikkovaihtoehtojen syykoodien asettaminen

Syykoodit voidaan konfiguroida seuraaville varastojen oikaisutyypeille:

- Inventointi
- Pistoinventointi
- Rajainventointi
- Oikaisu sisään
- Oikaisu ulos

Useimmissa tapauksissa voit määrittää seuraavat tiedot kullekin asiaankuuluvalle kannettavan laitteen valikkokohteelle:

- Syykoodin mahdollinen näyttäminen mobiililaitteen käyttäjälle inventoinnin aikana.
- Mobiililaitteen valikkovaihtoehdossa näytettävä oletussyykoodi.
- Käyttäjän tekemä syykoodin mahdollinen muokkaus.

#### <a name="set-up-mobile-device-menu-items-for-a-counting-process"></a>Mobiililaitteen valikkovaihtoehtojen inventointiprosessin asettaminen

Määritä mobiililaitteen valikkovaihtoehto inventointiprosessia varten seuraavasti.

1. Siirry kohtaan **Warehouse management** \> **Asetukset** \> **Mobiililaite** \> **Mobiililaitteen valikkovaihtoehdot**.
1. Valitse haluamasi valikkokohde luetteloruudusta tai luo uusi valikkokohde.
1. Valitse toimintoruudussa **Inventointi**.
1. Määritä **Inventoinnin oletussyykoodi** -kentässä oletussyykoodi, joka on kirjattava, kun mobiililaitteen valikkokohdetta käytetään inventointiin.
1. Valitse **Näytä inventoinnin syykoodi** -kentästä jokin seuraavista arvoista:

    - *Rivi* – Näytä syykoodi kunkin varianssin kirjaamisen jälkeen.
    - *Piilota* – Älä näytä syykoodia.

1. Aseta **Muokkaa inventoinnin syykoodia** -asetukseksi *Kyllä*, jotta työntekijä voi muokata syykoodia, kun se näkyy mobiililaitteessa laskennan aikana. Määritä arvoksi *Ei*, jos haluat estää työntekijää muokkaamasta koodia.

> [!NOTE]
> **Inventointi**-painike voidaan ottaa käyttöön missä tahansa mobiililaitteen valikkovaihtoehdossa, jos inventointi voidaan tehdä. Esimerkeissä on pistoinventoinnin, käyttäjän ohjaaman työn ja järjestelmän ohjaaman työn valikkovaihtoehtoja.

#### <a name="set-up-mobile-device-menu-items-for-adjustment-in-and-adjustment-out"></a><a name="setup-adjustment-in-out"></a>Mobiililaitteen Oikaisu sisään- ja Oikaisu ulos -valikkovaihtoehdon määrittäminen

Määritä mobiililaitteen Oikaisu sisään- ja Oikaisu ulos -valikkovaihtoehto seuraavasti.

1. Siirry kohtaan **Warehouse management** \> **Asetukset** \> **Mobiililaite** \> **Mobiililaitteen valikkovaihtoehdot**.
1. Luo valikkonimike valitsemalla toimintoruudussa **Uusi**.
1. Määritä uuden valikkovaihtoehdon **Mobiilinimikkeen nimi**- ja **Otsikko**-kentät.
1. Määritä **Tila**-kentän arvoksi *Työ*.
1. Valitse **Käytä nykyistä työtä** -vaihtoehdossa *Ei*.
1. Valitse **Työn luontiprosessi** -kentässä *Oikaisu sisään* tai *Oikaisu ulos*.
1. Valitse **Yleiset**-pikavälilehdellä seuraavat lisäkentät. (Kaikki nämä kentät lisätään, kun valitset **Työn luontiprosessi** -kentässä *Oikaisu sisään* tai *Oikaisu ulos*.)

    - **Käytä prosessiopasta** – Jos olet luomassa *Oikaisu ulos*-prosessia, varmista, että määrität tämän asetuksen arvoksi *Kyllä*. Jos olet luomassa *Oikaisu ulos* -prosessia, tämän vaihtoehdon asetuksena on aina *Kyllä*.
    - **Inventoinnin oletussyykoodi** – Määritä kentässä oletussyykoodi, joka on kirjattava, kun mobiililaitteen valikkokohdetta käytetään inventointiin.
    - **Näytä inventoinnin syykoodi** – Valitse kentästä jokin seuraavista arvoista:

        - *Rivi* – Näytä syykoodi kunkin varianssin kirjaamisen jälkeen.
        - *Piilota* – Älä näytä syykoodia.

    - **Muokkaa inventoinnin syykoodia** – Aseta asetukseksi *Kyllä*, jotta työntekijä voi muokata syykoodia, kun se näkyy mobiililaitteessa laskennan aikana. Määritä arvoksi *Ei*, jos haluat estää työntekijää muokkaamasta koodia.
    - **Inventoinnin syykoodiryhmä** – Valitse syykoodiryhmä, jos haluat rajoittaa työntekijöille esiteltyjen asetusten luetteloa. Lisätietoja syykoodiryhmien määrittämisestä on tässä ohjeaiheessa aiemmin olevassa [Inventoinnin syykoodiryhmien määrittäminen](#reason-groups) -osassa. 

> [!NOTE]
> Kun liität inventoinnin syykoodiryhmän *Oikaisu sisään*- ja *Oikaisu ulos* -valikkokohteisiin, joissa **Käytä prosessiopasta** -asetus on *Kyllä*, voit saada rajoitetun luettelon inventoinnin syykoodeista osana käsittelyä Warehouse Management-mobiilisovelluksessa.
>
> **Käytä prosessiopasta** -vaihtoehdon avulla voit myös estää vahingossa tapahtuvien suurten oikaisujen määrän. (Työntekijä voi esimerkiksi skannata vahingossa nimiketunnuksen viivakoodin määräarvon asemesta.) Voit määrittää tämän toiminnon valitsemalla **Käytä prosessiopasta** -asetusta *Kyllä* jokaiselle asianmukaiselle valikkokohteelle. Siirry sitten kohtaan **Warehouse management \> Asennus \> Työntekijä** ja määritä kullekin asiaankuuluvalle varastotyöntekijälle **Oikaisumäärän raja** -kenttä, jonka työntekijä voi rekisteröidä.

## <a name="processing-that-uses-counting-reason-codes"></a>Inventoinnin syykoodeja käyttävä käsittely

Kun työntekijät käyttävät Warehouse Management -mobiilisovellusta, syykoodit tallennetaan. Jos inventoinnin hyväksymisprosessia ei ole määritetty, tallennettuja syykoodeja käytetään heti osana seuraavia inventointikirjauskansion kirjauksia.

### <a name="cycle-count-approvals"></a>Inventoinnin hyväksynnät

Työntekijä voi muuttaa inventointiin liitettyä syykoodia ennen inventoinnin hyväksymistä. Kun inventointi on hyväksytty, syykoodi annetaan inventointikirjauskansion riveille.

#### <a name="modify-reason-codes-for-cycle-count-approvals"></a>Syklin inventointihyväksyntöjen syykoodien muokkaaminen

Voit määrittää syklin inventointihyväksynnät seuraavasti.

1. Mene kohtaan **Varastonhallinta** \> **Inventointi** \> **Tarkistusta odottava inventointityö**.
1. Valitse inventointimäärä ruudukossa.
1. Valitse toimintoruudun **Työ**-välilehdessä **Inventointi**. Valitse uusi syykoodi **Syykoodi** -kentässä.

Syykoodit lisätään *Inventointikirjauskansio*-tyypin inventointikirjauskansioiden riveille.

1. Valitse **Varastonhallinta** \> **Kirjauskansioviennit** \> **Inventointi** \> **Inventointi**.
2. Valitse inventointikirjauskansion riviyksiköstä **Inventoinnin syykoodi** -kentässä syykoodi, joka vastaa nykyistä tilannetta.

### <a name="view-the-reason-codes-recorded-in-the-counting-history"></a>Näytä inventointihistoriassa tallennetut syykoodit

Voit tarkastella inventointihistoriaan tallennettuja syykoodeja noudattamalla seuraavia vaiheita.

1. Siirry kohtaan **Varastonhallinta** \> **Kyselyt ja raportit** \> **Inventointihistoria**.
1. Valitse luetteloruudusta nimikkeiden inventointitietue.
1. Näytä **Inventoinnin syykoodi** -kentässä inventointihistoria, joka on tallennettu syykoodin avulla.

### <a name="use-reason-codes-for-quantity-adjustment-or-online-counting"></a>Syykoodien käyttäminen määrän oikaisussa tai online-inventoinnissa

Jos haluat käyttää syykoodia määrän oikaisussa tai online-inventoinnissa, noudata seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Kyselyt ja raportit \> Käytettävissä olevien luettelo**.
1. Valitse toimintoruudussa **Määrän oikaisu**.
1. Valitse ensin **Määrän oikaisu** ja sitten **Inventoinnin syykoodi** -kentässä syykoodi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
