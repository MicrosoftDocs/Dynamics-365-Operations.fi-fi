---
title: Resurssityypit
description: Tässä artikkelissa kerrotaan, kuinka resurssityypit luodaan resurssien hallinnassa. Siinä kuvataan myös resurssityyppeihin liittyvät elementit.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectJobType, EntAssetObjectType, EntAssetObjectTypeDefaultSparePart, EntAssetObjectTypeDefaultSparePartApprove, EntAssetObjectTypeDefaultCreateCombinations, EntAssetObjectTypeDefault, EntAssetObjectTypeDefaultCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d3a51fdb55e9158e88e89549e3d0049e699c233e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887628"
---
# <a name="asset-types"></a>Resurssityypit

[!include [banner](../../includes/banner.md)]



Tässä artikkelissa kerrotaan, miten voit luoda resurssityyppejä. Siinä kuvataan myös resurssityyppeihin liittyvät elementit. Resurssityypit ovat resurssien yleisiä luokkia. Esimerkkejä ovat CNC-koneet, mittauslaitteet ja kuorma-autojen moottorit. Resurssityyppien avulla hallitaan ylläpitotyötyyppejä (ylläpitotehtäviä), resurssin elinkaaritiloja, laskureita, resurssimääritteitä, kunnon arviointimalleja ja resurssimalleja, jotka voidaan valita resurssille. Resurssityyppi on määritettävä resurssin luomisen yhteydessä.

Kunkin resurssityypin osalta voidaan määrittää resurssityypin asetusten muunnoksia. Jos sinulla on esimerkiksi resurssityyppi, jonka nimi on **Kuorma-autot**, voit luoda kyseisen resurssityypin variaatioita resurssin eri valmistajille ja malleille. Kuhunkin resurssityypin määritykseen voidaan lisätä tarvittavat varaosat ja huoltosuunnitelmat.

Ensin määritetään tarvittavat resurssityypit. Seuraavaksi luodaan resurssimallit, jotka liittyvät resurssityyppeihin. **Resurssin oletustyypit** -sivulla voit luoda kaikki laitteessa tarvittavat resurssityyppien muutokset.

## <a name="create-an-asset-type"></a>Luo resurssityyppi

1. Valitse **Resurssien hallinta** > **Asetukset** > **Resurssityypit** > **Resurssityypit**.
2. Luo resurssityyppi valitsemalla **Uusi**.
3. Kirjoita **Resurssittyyppi** -kentässä resurssityypin tunnus.
4. Anna nimi **Nimi**-kenttään.
5. Valitse **Resurssin elinkaarimalli** -kentässä resurssin elinkaarimalli. Lisätietoja resurssin elinkaaritiloista ja resurssin elinkaarimalleista on kohdassa [Resurssin elinkaaren tilat](object-stages.md).
6. Määritä **Summa**-asetukseksi **Kyllä**, jos yhteenvetosuorituskykyilmaisimien (KPI) arvot lasketaan resursseille, joilla on kyseinen resurssityyppi.
7. Valitse **Tallenna**.
8. Valitse **Ylläpitotyön tyypit**-pikavälilehdessä ylläpitotyötyypit, jotka liittyvät resurssityyppiin:

    - Jos haluat valita työtyypin, valitse se **Jäljellä olevat ylläpitotyötyypit** -kentästä ja valitse sitten oikealle osoittava nuolipainike ![Oikealle osoittava nuolipainike.](media/29-setup-for-objects.png) siirtääksesi sen **Valitut työtyypit** -osioon.
    - Jos haluat valita kaikki käytettävissä olevat ylläpitotyötyypit, valitse ![Siirrä kaikki -nuolipainike](media/30-setup-for-objects.png) -painike. Kaikki ylläpitotyötyypit siirretään **Jäljellä olevat ylläpitotyötyypit** -kentästä **Valitut ylläpitotyötyypit** -kenttään.
    - Jos peruuttaa ylläpitotyötyypin valinnan, valitse se **Valitut ylläpitotyötyypit** -kentästä ja valitse sitten vasemmalle osoittava nuolipainike ![Vasemmalle osoittava nuolipainike.](media/31-setup-for-objects.png) siirtääksesi sen **Jäljellä olevat ylläpitotyötyypit** -kenttään.

9. Voit myös valita laskurit, jotka liittyvät kyseiseen resurssityyppiin. Tee valinnat **Laskurit**-pikavälilehdessä käyttämällä menetelmiä, jotka on kuvattu ylläpitotyötyypeille vaiheessa 8. Lisätietoja laskureiden määrityksestä esitetään kohdassa [Laskurit](counters.md).
10. Voit myös valita määritetyypit, jotka liittyvät kyseiseen resurssityyppiin. Tee valinnat **Määritetyypit** -pikavälilehdessä käyttämällä menetelmiä, jotka on kuvattu ylläpitotyötyypeille vaiheessa 8. Luo sitten haluamasi määritetyyppien järjestys valitsemalla määriteyyppi **Valitut määritetyypit** -kentässä ja siirrä sitä ylä- ja alanuolen avulla. Määritetyyppien järjestys näkyy resursseille, jotka käyttävät tätä resurssilajia. Lisä tietoja resurssimääritteistä on kohdassa [Ylläpidon määritetyypit](../setup-for-functional-locations/specification-types.md).

    > [!NOTE]
    > Kun lisäät uusia määritetyyppejä **Määritetyypit**-pikavälilehdessä, olemassa olevat resurssit päivitetään automaattisesti näillä tiedoilla.

11. Voit myös valita kunnon arviointimallit, jotka liittyvät kyseiseen resurssityyppiin. Tee valinnat **Kunnon arvioinnit** -pikavälilehdessä käyttämällä menetelmiä, jotka on kuvattu ylläpitotyötyypeille vaiheessa 8. Lisätietoja kunnon arviointimalleista ja rekisteröinneistä on kohdassa [Kunnon arviointi](../setup-for-objects/condition-assessment.md).
12. **Resurssimalli**-pikavälilehdessä näkyvät kaikki resurssin valmistajien ja mallien yhdistelmät, jotka on määritetty valittuun resurssityyppiin. Nähdäksesi valmistajan mukaan jaettuna olevat yhdistelmät valitse **Resurssimalli** avataksesi **Resurssimalli**-sivun.

    **Resurssimalli**-sivulla voit lisätä resurssimalli – resurssityyppi.suhteita. Lisäksi **Resurssityypit** -sivulla voit lisätä resurssin valmistaja – resurssin malli -suhteita suoraan resurssityyppiin. Lopuksi voit luoda uudet resurssin valmistaja – resurssin malli – resurssityyppi -suhteet **Resurssimalli**-sivulla (**Resurssien hallinta** \> **Asetukset** \> **Resurssit** \> **Resurssimalli**). Tämän vuoksi on olemassa kolme tapaa määrittää ja muokata resurssin valmistaja – resurssimalli – resurssityyppi -suhteita. Kaikki käytettävissä olevat yhdistelmät näkyvät eri näkökulmista, ja voit valita haluamasi kohdan määrityksen yhteydessä.

> [!NOTE]
> - Jos valitset laskurit resurssityypille, valinnat päivitetään automaattisesti **Laskurit**-sivulla (**Resurssienhallinta** > **Asetukset** > **Resurssit** > **Resurssityypit** > **Laskurit**).
> - **Yleiset**-pikavälilehden **Tiedot**-osan kentissä näkyy niiden ylläpitotyötyyppien, laskureiden ja määritteiden jne. määrä, jotka on määritetty valitulle resurssityypille.

Yleensä manuaalisesti luodut työtilaukset liittyvät korjaavaan kunnossapitoon, kun taas automaattisesti luodut työtilaukset liittyvät ennakoivan kunnossapidon ylläpitoon. Kun luot manuaalisesti työtilaukset, vain ylläpitotyötyypit, jotka on valittu **Resurssityypit**-sivun **Ylläpitotyötyypit**-pikavälilehdessä, voidaan käyttää. Automaattisesti luodut työtilaukset voivat kuitenkin käyttää kaikkia **Ylläpitotyötyypit**-sivulla luomiasi ylläpitotyötyyppejä (**Resurssien hallinta** \> **Asetukset** \> **Työt** \> **Ylläpitotyötyypit**).

## <a name="create-asset-type-setup-lines"></a>Luo resurssityypin asetusrivit

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Resurssit** \> **Resurssityypit** \> **Resurssityypin asetukset**. Valitse vaihtoehtoisesti **resurssien hallinta** \> **Asetukset** \> **resurssit** \> **resurssityypit** \> **resurssityypit**, valitse resurssityyppi ja sitten **resurssityypin asetukset**.
2. Kun käytät **Resurssityypin asetukset** -sivua ensimmäisen kerran, saatat löytää **Luo yhdistelmät** -painikkeen hyödylliseksi. Tämän painikkeen avulla voit luoda nopeasti kaikki resurssimallin yhdistelmät resurssityypille. Valitse **Luo yhdistelmät**, valitse resurssityyppi, jolle yhdistelmät luodaan, ja valitse sitten **OK**.

    > [!NOTE]
    > Jos et käytä kaikkia automaattisesti luotuja resurssityypin asetusyhdistelmiä, voit poistaa asetukset valitsemalla sen ja valitsemalla sitten **Poista**.

3. Luo resurssityypin asetus manuaalisesti valitsemalla **Uusi**.
4. Määritä **Resurssityyppi**-, **Valmistaja** -ja **Malli**-kentissä arvot sen mukaan, kuinka erityinen resurssityyppiasetus on.
5. Jos resurssityyppiin liittyy takuusopimus, valitse sopimus **Toimittajan takuu** -ja **Asiakkaan takuu** -kentissä. 
6. Valitse **Varaosat** -pikavälilehdellä **Lisää** lisätäksesi varaosia valittuun resurssityypin asetuksiin.
7. Voit hyväksyä varaosan valitsemalla varaosarivin ja valitsemalla sitten **Hyväksy**. Voit valita useita rivejä hyväksyttäväksi.
8. Jos haluat nähdä, käytetäänkö varaosaa jossakin muualla resurssien hallinnassa (esimerkiksi suhteessa resursseihin ja työtilauksiin), valitse varaosarivi ja valitse sitten **Nimike, missä käytetty** avataksesi **Nimike, missä käytetty** -sivun. Jos haluat nähdä luettelon kaikista aktiiviset varaosista, valitse **Aktiivinen** -valintaruutu. Jos haluat nähdä vain hyväksytyt varasat, valitse **Hyväksytty**-valintaruutu.
9. Valitse **Ylläpitosuunnitelmat**-pikavälilehdellä **Lisää** lisätäksesi ylläpitosuunnitelmia valittuun resurssityypin asetuksiin.
10. Jos haluat kopioida resurssityypin asetukset toiseen asetukseen, voit käyttää Kopioi-toimintoa. Valitse kopioitavat resurssityypin asetukset, valitse **Kopioi asetukset** ja valitse resurssityypin asetukset, josta asetukset kopioidaan. Eri asetusten asetukset määrittävät, kuinka paljon tietoa on mukana. Kun olet valmis, kopioi asetukset valitsemalla **OK**.

> [!NOTE]
> Jos sinulla on useita varaosarivejä ja huoltosuunnitelman rivejä, joita käytät uudelleen, Kopioi-toiminnolla voit nopeasti ja helposti määrittää useiden resurss tyypin asetusyhdistelmien tiedot.

## <a name="spare-parts-on-the-asset-type-setup"></a>Varaosat resurssityypin asetuksissa

Kuten kohdassa "Luo resurssityypin asetusrivit" on kuvattu, varaosat määritetään resurssimalleille **Resurssityypin asetukset** -sivulla. Tämän vuoksi, kun avaat **resurssityypin asetukset** -sivun, näet vain varaosat, jotka liittyvät valittuun resurssityypin, resurssin valmistajan ja resurssimallin yhdistelmään. Jos haluat nähdä luettelon kaikista varaosatietueista, avaa **Varaosat**- sivu **(Resurssien hallinta** \> **Kyselyt** \> **Varaosat**).

**Varaosat**-sivulla voit myös luoda uusia varaosia resurssityypin, resurssin valmistajan ja resurssimallin olemassa oleville yhdistelmille. Voit päättää, haluatko luoda varaosatietueita **Resurssityypin asetukset**- vai **Varasat**-sivulla. **Resurssityypin asetukset** -sivulla on yhteenveto valitun resurssityypin, resurssin valmistajan ja resurssimallin yhdistelmästä, kun taas **Varaosat**-sivulla on kattava yhteenveto kaikista resurssityypin asetusriveistä. Jos **Varaosat**-sivu sisältää useita tietueita, **Resurssityypin asetukset** -sivu saattaa antaa sinulle paremman yleiskuvan.

Jos haluat nähdä, käytetäänkö valitun rivin varaosaa jossakin muualla resurssien hallinnassa (esimerkiksi suhteessa resursseihin ja työtilauksiin), valitse varaosarivi ja valitse sitten **Nimike, missä käytetty** avataksesi **Nimike, missä käytetty** -sivun. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]