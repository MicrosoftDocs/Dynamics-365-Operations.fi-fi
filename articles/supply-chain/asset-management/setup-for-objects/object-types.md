---
title: Resurssityypit
description: Tässä ohjeaiheessa kerrotaan, kuinka resurssityypit luodaan resurssien hallinnassa. Siinä kuvataan myös resurssityyppeihin liittyvät elementit.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 288dac77f9d999012ec930ef2bca5c0921c2955f
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783242"
---
# <a name="asset-types"></a>Resurssityypit

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Tässä ohjeaiheessa kerrotaan, miten voit luoda resurssityyppejä. Siinä kuvataan myös resurssityyppeihin liittyvät elementit. Resurssityypit ovat resurssien yleisiä luokkia. Esimerkkejä ovat CNC-koneet, mittauslaitteet ja kuorma-autojen moottorit. Resurssityyppien avulla hallitaan työlajeja (ylläpitotehtäviä), resurssin elinkaaritiloja, resurssin mittauksia, resurssimääritteitä, kunnon arviointimalleja ja resurssimalleja, jotka voidaan valita resurssille. Resurssityyppi on määritettävä resurssin luomisen yhteydessä.

Kunkin resurssityypin osalta voidaan määrittää resurssityypin asetusten muunnoksia. Jos sinulla on esimerkiksi resurssityyppi, jonka nimi on **Kuorma-autot**, voit luoda kyseisen resurssityypin variaatioita resurssin eri valmistajille ja malleille. Kuhunkin resurssityypin määritykseen voidaan lisätä tarvittavat varaosat ja huoltosuunnitelmat.

Ensin määritetään tarvittavat resurssityypit. Seuraavaksi luodaan resurssimallit, jotka liittyvät resurssityyppeihin. **Resurssin oletustyypit** -sivulla voit luoda kaikki laitteessa tarvittavat resurssityyppien muutokset.

## <a name="create-an-asset-type"></a>Luo resurssityyppi

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Resurssityypit** \> **Resurssityypit**.
2. Luo resurssityyppi valitsemalla **Uusi**.
3. Kirjoita **Resurssittyyppi** -kentässä resurssityypin tunnus.
4. Anna nimi **Nimi**-kenttään.
5. Valitse **Resurssin elinkaarimalli** -kentässä resurssin elinkaarimalli. Lisätietoja resurssin elinkaaritiloista ja resurssin elinkaarimalleista on kohdassa [Resurssin elinkaaren tilat](object-stages.md).
6. Määritä **Summa**-asetukseksi **Kyllä**, jos yhteenvetosuorituskykyilmaisimien (KPI) arvot lasketaan resursseille, joilla on kyseinen resurssityyppi.
7. Valitse **Tallenna**.
8. Valitse **Työtyypit**-pikavälilehdessä työtyypit, jotka liittyvät resurssityyppiin:

    - Jos haluat valita työtyypin , valitse se **Jäljellä olevat työtyypit** -kentässä ja valitse sitten oikea nuolipainike ![Oikealle osoittava nuolipainike](media/29-setup-for-objects.png) siirtääksesi sen **Valitut työtyypit** -osioon.
    - Jos haluat valita kaikki käytettävissä olevat työlajit, valitse ![Siirrä kaikki -nuolipainike](media/30-setup-for-objects.png). Kaikki työlajit siirretään **Jäjlellä olevat työtyypit** -kentästä **Valitut työtyypit** -kenttään.
    - Jos peruuttaa työtyypin valinnan, valitse se **Valitut työtyypit** -kentässä ja valitse sitten vasen nuolipainike ![Vasemmalle osoittava nuolipainike](media/31-setup-for-objects.png) siirtääksesi sen **Jäljellä olevat työtyypit** -osioon.

9. Voit myös valita resurssimitat, jotka liittyvät kyseiseen resurssityyppiin. Tee valinnat **Resurssien mittarit** -pikavälilehdessä käyttämällä menetelmiä, jotka on kuvattu vaiheessa 8 työtyypeille. Lisä tietoja Resurssien mittaritmitan asetuksista on kohdassa [Ylläpidettävän resurssin mittaukset](counters.md).
10. Voit myös valita määritetyypit, jotka liittyvät kyseiseen resurssityyppiin. Tee valinnat **Määritetyypit** -pikavälilehdessä käyttämällä menetelmiä, jotka on kuvattu vaiheessa 8 työtyypeille. Luo sitten haluamasi määritetyyppien järjestys valitsemalla määriteyyppi **Valitut määritetyypit** -kentässä ja siirrä sitä ylä- ja alanuolen avulla. Määritetyyppien järjestys näkyy resursseille, jotka käyttävät tätä resurssilajia. Lisä tietoja resurssimääritteistä on kohdassa [Ylläpidon määritetyypit](../setup-for-functional-locations/specification-types.md).

    > [!NOTE]
    > Kun lisäät uusia määritetyyppejä **Määritetyypit**-pikavälilehdessä, olemassa olevat resurssit päivitetään automaattisesti näillä tiedoilla.

11. Voit myös valita kunnon arviointimallit, jotka liittyvät kyseiseen resurssityyppiin. Tee valinnat **Kunnon arvioinnit** -pikavälilehdessä käyttämällä menetelmiä, jotka on kuvattu vaiheessa 8 työtyypeille. Lisätietoja kunnon arviointimalleista ja rekisteröinneistä on kohdassa [Kunnon arviointi](../setup-for-objects/condition-assessment.md).
12. **Resurssimalli**-pikavälilehdessä näkyvät kaikki resurssin valmistajien ja mallien yhdistelmät, jotka on määritetty valittuun resurssityyppiin. Nähdäksesi valmistajan mukaan jaettuna olevat yhdistelmät valitse **Resurssimalli** avataksesi **Resurssimalli**-sivun.

    **Resurssimalli**-sivulla voit lisätä resurssimalli – resurssityyppi.suhteita. Lisäksi **Resurssityypit** -sivulla voit lisätä resurssin valmistaja – resurssin malli -suhteita suoraan resurssityyppiin. Lopuksi voit luoda uudet resurssin valmistaja – resurssin malli – resurssityyppi -suhteet **Resurssimalli**-sivulla (**Resurssien hallinta** \> **Asetukset** \> **Resurssit** \> **Resurssimalli**). Tämän vuoksi on olemassa kolme tapaa määrittää ja muokata resurssin valmistaja – resurssimalli – resurssityyppi -suhteita. Kaikki käytettävissä olevat yhdistelmät näkyvät eri näkökulmista, ja voit valita haluamasi kohdan määrityksen yhteydessä.

> [!NOTE]
> - Jos valitset resurssityypille resurssin mitat, valinnat päivitetään automaattisesti **Resurssin mitat** -sivulle(**Resurssien hallinta** \> **Asetukset** \> **Resurssit** \> **Resurssityypit** \> **Resurssin mitat**).
> - **Yleiset**-pikavälilehden **Tiedot**-osan kentissä näkyy työtyyppien, resurssin mittojen ja määritteiden jne. määrä, jotka on määritetty valitulle resurssityypille.

Yleensä manuaalisesti luodut työtilaukset liittyvät korjaavaan kunnossapitoon, kun taas automaattisesti luodut työtilaukset liittyvät ennakoivan kunnossapidon ylläpitoon. Kun luot manuaalisesti työtilaukset, vain työlajit, jotka on valittu **Resurssityypit**-sivun **Työtyypit**-pikavälilehdessä, voidaan käyttää. Automaattisesti luodut työtilaukset voivat kuitenkin käyttää kaikkia **Työtyypit**-sivulla luomiasi työtyyppejä (**Resurssien hallinta** \> **Asetukset** \> **Työt** \> **Työtyypit**).

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
8. Jos haluat nähdä, käytetäänkö varaosaa jossakin muualla resurssien hallinnassa (esimerkiksi suhteessa resursseihin ja työtilauksiin), valitse varaosarivi ja valitse sitten **Nimike, missä käytetty** avataksesi**Nimike, missä käytetty** -sivun. Jos haluat nähdä luettelon kaikista aktiiviset varaosista, valitse **Aktiivinen** -valintaruutu. Jos haluat nähdä vain hyväksytyt varasat, valitse **Hyväksytty**-valintaruutu.
9. Valitse **Ylläpitosuunnitelmat**-pikavälilehdellä **Lisää** lisätäksesi ylläpitosuunnitelmia valittuun resurssityypin asetuksiin.
10. Jos haluat kopioida resurssityypin asetukset toiseen asetukseen, voit käyttää Kopioi-toimintoa. Valitse kopioitavat resurssityypin asetukset, valitse **Kopioi asetukset** ja valitse resurssityypin asetukset, josta asetukset kopioidaan. Eri asetusten asetukset määrittävät, kuinka paljon tietoa on mukana. Kun olet valmis, kopioi asetukset valitsemalla **OK**.

> [!NOTE]
> Jos sinulla on useita varaosarivejä ja huoltosuunnitelman rivejä, joita käytät uudelleen, Kopioi-toiminnolla voit nopeasti ja helposti määrittää useiden resurss tyypin asetusyhdistelmien tiedot.

## <a name="spare-parts-on-the-asset-type-setup"></a>Varaosat resurssityypin asetuksissa

Kuten kohdassa "Luo resurssityypin asetusrivit" on kuvattu, varaosat määritetään resurssimalleille **Resurssityypin asetukset** -sivulla. Tämän vuoksi, kun avaat **resurssityypin asetukset** -sivun, näet vain varaosat, jotka liittyvät valittuun resurssityypin, resurssin valmistajan ja resurssimallin yhdistelmään. Jos haluat nähdä luettelon kaikista varaosatietueista, avaa **Varaosat**- sivu **(Resurssien hallinta** \> **Kyselyt** \> **Varaosat**).

**Varaosat**-sivulla voit myös luoda uusia varaosia resurssityypin, resurssin valmistajan ja resurssimallin olemassa oleville yhdistelmille. Voit päättää, haluatko luoda varaosatietueita **Resurssityypin asetukset**- vai **Varasat**-sivulla. **Resurssityypin asetukset** -sivulla on yhteenveto valitun resurssityypin, resurssin valmistajan ja resurssimallin yhdistelmästä, kun taas **Varaosat**-sivulla on kattava yhteenveto kaikista resurssityypin asetusriveistä. Jos **Varaosat**-sivu sisältää useita tietueita, **Resurssityypin asetukset** -sivu saattaa antaa sinulle paremman yleiskuvan.

Jos haluat nähdä, käytetäänkö valitun rivin varaosaa jossakin muualla resurssien hallinnassa (esimerkiksi suhteessa resursseihin ja työtilauksiin), valitse varaosarivi ja valitse sitten **Nimike, missä käytetty** avataksesi**Nimike, missä käytetty** -sivun. 

