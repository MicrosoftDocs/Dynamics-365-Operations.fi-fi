---
title: Power Appsin kaavasovellusten upottaminen
description: Tässä ohjeaiheessa käsitellään Microsoft Power Appsin kaaviosovellusten upottamista asiakasohjelmaan laajentamaan tuotteen toimintoja.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: c2f7b660d364be6e62d484e67908201027190a8a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065098"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Power Appsin kaavasovellusten upottaminen

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Microsoft Power Apps on palvelu, joka sallii kehittäjien ja muiden kuin teknisten käyttäjien muokata yrityssovelluksia mobiililaitteille, tableteille ja verkkoon ilman, että heidän tarvitsee kirjoittaa koodia. Taloushallinnon ja toimintojen sovellukset tukevat integrointia Power Appsin kanssa. Sinun, organisaatiosi tai laajemman ekosysteemin kehittämät kaaviosovellukset voidaan upottaa taloushallinnon ja toimintojen sovelluksiin laajentamaan tuotteen toimintoja. Voit esimerkiksi luoda Power Apps -kaaviosovelluksen, joka täydentää taloushallinnon ja toimintojen sovellusta toisesta järjestelmästä haetuilla tiedoilla.

Lisätietoja kaaviosovellusten upottamisesta on lyhyessä videossa [Kaaviosovellusten upottaminen](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Upotetun Power Apps -kaaviosovelluksen lisääminen sivulle

Ennen kuin Power Apps -kaaviosovellus voidaan upottaa asiakasohjelmaan, käyttäjän on ensin etsittävä tai luotava sovellus, jossa on toivotut visuaaliset elementit tai toiminnot. Tässä ohjeaiheessa ei ole yksityiskohtaista kuvausta sovellusten luontiprosessista. Jos Power Apps ei ole tuttu, tutustu [Power Apps -dokumentaatioon](/powerapps/).

Pohjaan perustuvan sovelluksen voi upottaa taloushallinnon ja toimintojen sovellukseen kolmella tavalla. Valinta voi siis perustua siihen, mikä tapa soveltuu parhaiten skenaarioon. 

- Pohjaan perustuvan sovelluksen upottaminen **Power Apps** -painikkeeseen sivun vakiotoimintoruudussa. Tällä tavoin lisätyt sovellukset näkyvät vaihtoehtoina **Power Apps** -valikkopainikkeessa, ja sovellukset avautuvat sivuruuduissa. 
- Pohjaan perustuvan sovelluksen upottaminen suoraan aiemmin luodulle sivulle uutena välilehtenä (pivot-välilehti, pikavälilehti, lehti tai työtilan osa).
- Pohjaan perustuvalle sovellukselle luodaan uusi koko sivun kokemus koontinäytössä.

Voit valita upotettua kaaviosovellusta määritettäessä yhden kentän, jonka haluat lähettää kontekstina sovellukseen. Tälölin sovellus voi reagoida tarkasteltavien tietojen perusteella.

> [!NOTE]
> Mallipohjaisia sovelluksia voi tällä hetkellä upottaa tällä tavoin.

### <a name="embedding-a-canvas-app-on-an-existing-page"></a>Pohjaan perustuvan sovelluksen upottaminen aiemmin luodulle sivulle

Seuraavassa menettelyssä näytetään, miten pohjaan perustuva sovellus upotetaan aiemmin luodulle sivulle Power Appsista.

1. Siirry sivulle, johon haluat upottaa kaaviosovelluksen. Tämä sivu sisältää tiedot, jotka on välitettävä sovellukseen syötteenä.
2. Avaa **Lisää Power Apps -sovellus** -ruutu:

    - Jos sovellus upotetaan suoraan sivulle, valitse **Asetukset** \> **Mukauta tämä sivu** \> **Lisää** ja tee sitten jokin seuraavista:

        - Jos **Koko sivun sovellukset** -ominaisuus on otettu käyttöön, valitse **Lisää sivu** ja valitse sitten alue, johon sovellus lisätään. Jos sovellus upotetaan **Power Apps** -valikkopainikkeeseen, valitse toimintoruutu. Jos sovellus upotetaan suoraan sivulle, valitse soveltuva välilehti, pikavälilehti, lehti tai osa (jos kyseessä on työtila). Valitse sitten **Lisää sovellus** -ruudussa **Power Apps**.
        - Jos **Koko sivun sovellukset** -ominaisuus on poistettu käytöstä, valitse **Lisää sovellus Power Appsista** ja valitse sitten alue, johon sovellus lisätään. Jos sovellus upotetaan **Power Apps** -valikkopainikkeeseen, valitse toimintoruutu. Jos sovellus upotetaan suoraan sivulle, valitse soveltuva välilehti, pikavälilehti, lehti tai osa (jos kyseessä on työtila).

    - Jos sovellusta käytetään **Power Apps** -valikkopainikkeella, **Power Apps** -valikkopainike voidaan valita vakiotoimintoruudussa, jonka jälkeen valitaan **Lisää sovellus**.

3. Määritä upotettu sovellus. Lisätietoja on myöhemmin tämän aiheen kohdassa [Pohjaan perustuvan sovelluksen määrittäminen](#configuring-a-canvas-app).
4. Valitse **Lisää** sen jälkeen, kun määrityksen oikeellisuus on tarkistettu.

    - Jos **Tallenna näkymät** -ominaisuus on poistettu käytöstä, upotettu sovellus näkyy sen jälkeen, selain on päivitetty.
    - Jos **Tallennetut näkymät** -ominaisuus on otettu käyttöön, näkymä on tallennettava, jotta muutos jää pysyväksi.

### <a name="embedding-a-canvas-app-as-a-full-page-experience-from-the-dashboard"></a>Pohjaan perustuvan sovelluksen upottaminen koko sivun kokemuksena koontinäytöstä

Pohjaan perustuvan sovelluksen upottamista koontinäytöstä kannattaa harkita, jos sovellus ei liity aiemmin luotuun sivuun tai jos sovelluksen halutaan näkyvän koko sivun kokemuksena taloushallinnon ja toimintojen sovelluksessa.

> [!NOTE]
> Tämä ominaisuus saadaan käyttöön ottamalla **Koko sivun sovellukset** -ominaisuus käyttöön ominaisuuksien hallinnassa. 

1. Avaa koontinäyttö.
2. Pidä sivua valittuna (tai napsauta sitä hiiren kakkospainikkeella), valitse **Mukauta** ja valitse sitten **Lisää sivu**.
3. Valitse **Lisää sivu** -ruudussa **Power Apps**.
4. Määritä upotettu sovellus. Lisätietoja on myöhemmin tämän aiheen kohdassa [Pohjaan perustuvan sovelluksen määrittäminen](#configuring-a-canvas-app).
5. Lisää sovellus koontinäyttöön uutena ruutuna valitsemalla **Tallenna**.
6. Valitse koontinäytössä uusi ruutu ja vahvista, että pohjaan perustuva sovellus näkyy odotetulla tavalla.

### <a name="configuring-a-canvas-app"></a>Pohjaan perustuvan sovelluksen määrittäminen

Seuraavat parametrit on määritettävä pohjaan perustuvaa sovellusta upotettaessa:

- **Nimi** – Kirjoita teksti, joka näkyy upotetun sovelluksen sisältävässä painikkeessa tai välilehdessä. Sovelluksen nimi kannattaa ehkä toistaa tässä kentässä.
- **Sovelluksen tunnus** – Määrittää upotettavan pohjaan perustuvan sovelluksen GUID-tunnuksen. Voit noutaa tämän arvon etsimällä sovelluksen sivustossa [make.powerapps.com](https://make.powerapps.com) ja siirtymällä sitten **Sovelluksen tunnus** -kenttään **Tiedot**-kohdassa.
- **Sovelluksen syötekonteksti** – Lisäksi voidaan valita kenttä, joka sisältää sovellukselle syötteenä välitettävät tiedot. Lisätietoja tavoista, joilla sovellus voi käyttää taloushallinnon ja toimintojen sovelluksista lähetettyjä tietoja, on jäljempänä tässä ohjeaiheessa kohdassa [Taloushallinnon ja toimintojen sovellusten tietoja hyödyntävän sovelluksen muodostaminen](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps).

    Versiosta 10.0.19 alkaen nykyinen yritys välitetään pohjaan perustuvaan sovellukseen myös kontekstina **cmp**-URL-parametrin kautta. Tämä toiminta ei vaikuta pohjaan perustuvaan kohdesovellukseen, ennen kuin kyseisen sovellus käyttää kyseisiä tietoja.

- **Sovelluksen koko** – Upotettavan sovelluksen tyypin valitseminen. Jos sovellus luodaan mobiililaitteille, valitse **Kapea**. Jos se luodaan tableteille, valitse **Leveä**. Tämä parametri varmistaa, että upotetulle sovellukselle on varattu riittävästi tilaa.
- **Yritykset** – Niiden yritysten valinta, joissa sovellus on käytettävissä. Sovellus on oletusarvoisesti käytettävissä kaikissa sovelluksissa. Tämä vaihtoehto on käytettävissä vain silloin, kun upotus tehdään suoraan aiemmin luodulle sivulle ja **[Tallennetut näkymät](saved-views.md)** -ominaisuus on poistettu käytöstä.

## <a name="sharing-an-embedded-app"></a>Upotetun sovelluksen jakaminen

Kun pohjaan perustuva sovellus on upotettu sivulle ja kun on vahvistettu, että se toimii oikein, upotettu sovellus on mahdollista jakaa järjestelmän muiden käyttäjien kanssa. Voit jakaa upotetun kaaviosovelluksen seuraavasti.

1. [Jaa pohjaan perustuva sovellus Power Appsissa](/powerapps/maker/canvas-apps/share-app) soveltuvien käyttäjien kanssa, jolloin he voivat käyttää sovellusta suoraan Power Appsissa.
2. Jaa upotettuihin sovelluksiin liitetyt mukauttamiset toivottujen käyttäjien kanssa. Voit käyttää kumpaa tahansa seuraavista menetelmistä:

    - **Julkaise näkymä (suositus):** Jos **[Tallennetut näkymät](saved-views.md)** -ominaisuus on otettu käyttöön, suositeltava ja ensisijainen menetelmä on luoda upotetun pohjaan perustuvan sovelluksen sisältävä näkymä ja julkaista kyseinen näkymä sitten toivotuille käyttäjille. Tämä menetelmä varmistaa, että kaikki käyttäjät, joilla on julkaistun näkymän kohteena olevat käyttöoikeusroolit, näkevät pohjaan perustuvan sovelluksen sivulla.

        Myös koko sivun kokemuksena koontinäytöstä upotettu pohjaan perustuva sovellus voidaan julkaista. Koontinäytössä valitse ja pidä valittuna (tai valitse hiiren kakkospainikkeella) sovellukseen liittyvä ruutu, valitse **Mukauta** valitse sitten **Julkaise sivu**. *Näkymien julkaiseminen* -kokemusta muistuttava kokemus näytetään, ja käyttöoikeudet, joihin julkaisu tehdään, voidaan valita. Jos päivityksestä 10.0.21 alkaen **Tallennettujen näkymien parannetut yritystuki** -ominaisuus on otettu käyttöön, sovellus voidaan julkaista myös toivottuihin yrityksiin.

    - Jos **Tallennetut näkymät** -ominaisuus on poistettu käytöstä, järjestelmänvalvoja voi antaa pohjaan perustuvan sovelluksen sisältävän mukautuksen soveltuvalle käyttäjäjoukolle **Mukauttaminen**-sivun kautta. Vaihtoehtoisesti sivun mukautukset voidaan viedä, jonka jälkeen ne lähetetään käyttäjille. Kukin kyseisistä käyttäjistä voi sitten tuoda mukautuksen. Mukauttamisen työkalurivillä on painikkeita, joilla viedä ja tuoda mukautuksia.

> [!NOTE]
> Jos kaaviosovellus on jaettu ulkoisten käyttäjien kanssa, kyseiset käyttäjät eivät voi käyttää upotettua sovellusta taloushallinnon ja toimintojen sovelluksissa. He voivat kuitenkin käyttää sovellusta suoraan Power Appsissa. Ulkoiset käyttäjät ovat vieraita ja käyttäjiä, jotka eivät kuulu siihen Microsoft 365:n Azure-hakemistoon, jossa taloushallinnon ja toimintojen sovellus on otettu käyttöön.

Lisätietoja tuotteen mukauttamistoiminnoista ja niiden käytöstä on kohdassa [Käyttökokemuksen mukauttaminen](personalize-user-experience.md).

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Taloushallinnon ja toimintojen sovelluksista lähetettyjä tietoja käyttävän kaaviosovelluksen luominen

Kun luot kaaviosovelluksen, joka upotetaan taloushallinnon ja toimintojen sovellukseen, tärkeä osa prosessia on käyttää kyseisen taloushallinnon ja toimintojen sovelluksen syöttötietoja. Power Apps -kehityskokemuksessa taloushallinnon ja toimintojen sovelluksesta välitettyjä tietoja voidaan käyttää käyttämällä muuttujaa **Param("EntityId")**. Lisäksi versiosta 10.0.19 alkaen nykyinen yritys välitetään myös kaaviosovellukselle **Param("cmp")**-muuttujan kautta. 

Esimerkiksi sovelluksen OnStart-toiminnolle voi määrittää syöttötiedot taloushallinnon ja toimintojen sovelluksista muuttujalle seuraavalla tavalla:

``` Power Apps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));

If(!IsBlank(Param("cmp")), Set(FinOpsLegalEntity, Param("cmp")), Set(FinOpsLegalEntity, ""));
```

## <a name="viewing-a-canvas-app"></a>Kaaviosovelluksen tarkasteleminen

Voit tarkastella taloushallinnon ja toimintojen sovelluksien sivulle upotettua kaaviosovellusta siirtymällä sivulle, jolla on upotettu sovellus. Muista, että sovelluksia voi käyttää vakiomuotoisen toimintoruudun **Power Apps** -painikkeen avulla. Vaihtoehtoisesti ne voivat tulla näkyviin suoraan sivulla uutena välilehtenä, pikavälilehtenä, lehtenä tai työtilan uutena osana. Kun käyttäjät yrittävät ladata sovelluksen sivulla ensimmäistä kertaa, heitä kehotetaan kirjautumaan sisään. Tällä vaiheella varmistetaan, että käyttäjillä on tarvittavat käyttöoikeudet sovelluksen käyttämiseen.

## <a name="editing-an-embedded-app"></a>Upotetun sovelluksen muokkaaminen

Sivulle upotettu sovellus saattaa vaatia muutoksia kyseisen sovelluksen määrityksiin. Voit esimerkiksi muokata upotettuun sovellukseen liitettyä otsikkoa. Jos on luotu uusi sovellus, sovelluksen tunnus on ehkä päivitettävä niin, että se osoittaa uusimpaan versioon.

Muokkaa upotetun sovelluksen konfiguraatiota näiden vaiheiden avulla:

1. Siirry **Muokkaa sovellusta** -ruutuun.

    - Jos upotettua sovellusta käytetään suoraan Power Apps -valikkopainikkeella, valitse ja pidä Power Apps -valikkopainiketta painettuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse **Mukauta**. Valitse määritettävä sovellus avattavasta **Valitse sovellus** -valikosta.
    - Jos upotettu sovellus näkyy suoraan sivulla, valitse ensin **Asetukset** ja sitten **Mukauta tämä sivu**. Napsauta upotettua sovellusta **Valinta**-työkalulla.
    - Jos upotettu sovellus lisättiin koontinäytöstä, avaa koontinäyttö, valitse ja pidä pohjaan perustuvaan sovellukseen liitettyä ruutua valittuna (tai napsauta sitä hiiren kakkospainikkeella), valitse **Mukauta** ja valitse lopuksi **Muokkaa sivua**.

2. Tee sovelluksen määritykseen tarvittavat muutokset ja valitse sitten **Tallenna**.

## <a name="removing-an-app"></a>Sovelluksen poistaminen

Upotetun sovelluksen poistamiseen sivulta tarvittaessa on muutamia tapoja:

- Siirry **Muokkaa sovellusta** -ruutuun tämän ohjeaiheen aiemmin käsitellyn osan [Upotetun sovelluksen muokkaaminen](#editing-an-embedded-app) ohjeiden avulla. Vahvista, että ruudussa on sen upotetun sovelluksen tiedot, jonka haluat poistaa, ja valitse sitten **Poista**-painike.
- Jos upotettu sovellus lisättiin koontinäytöstä, avaa koontinäyttö, valitse ja pidä pohjaan perustuvaan sovellukseen liitettyä ruutua valittuna (tai napsauta sitä hiiren kakkospainikkeella), valitse **Mukauta** ja valitse lopuksi **Poista sivu**. 
- Koska upotettu sovellus on tallennettu mukautuksen tietoina, sivun mukautuksen tyhjentäminen poistaa myös kaikki sivulle upotetut sovellukset. Huomaa, että sivun mukautukset tyhjennetään pysyvästi. Tyhjennystä ei voi peruuttaa. Voit poistaa sivun mukautukset valitsemalla ensin **Asetukset**, sitten **Mukauta tämä sivu** ja lopuksi **Tyhjennä**-painike. Kaikki tämän sivun edelliset mukautukset poistetaan, kun selain päivitetään. Lisätietoja sivujen optimoinnista mukauttamisen avulla on kohdassa [Käyttäjäkokemuksen mukauttaminen](personalize-user-experience.md).

## <a name="appendix"></a>Liite

### <a name="developer-modeling-a-canvas-app-on-a-form"></a>[Kehittäjä] Kaaviosovelluksen mallinnus lomakkeelle

Vaikka tämä ohjeaihe keskittyy kaaviosovelluksen upottamiseen räätälöinnin kautta, kehittäjillä on myös mahdollisuus lisätä kaaviosovellus lomakkeeseen Visual Studio -kehityskokemusta käyttäen. Voit tehdä tämän lisäämällä lomakkeeseen PowerAppsHostControlin. Ohjausobjektin käytettävissä olevat metatietojen ominaisuudet tarjoavat samat ominaisuudet kuin personointikokemuskin.

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[Kehittäjä] Määrittää, minne sovellus voidaan upottaa

Käyttäjät voivat upottaa sovellukset oletusarvoisesti mille tahansa sivulle joko Power Apps -valikkopainikkeeseen tai suoraan sivulle välilehtinä, pikavälilehtinä tai työtilan uutena osana. Kehittäjät voivat kuitenkin tarvittaessa määrittää tämän toiminnon niin, että se sallii sovellusten upottamisen vain tietyillä sivuilla. Se tehdään seuraavasti:

- **isPowerAppPersonalizationEnabled** – Jos tämä menetelmä palauttaa epätosi-arvon tietylle sivulle, Power Apps -valikkopainike ei ole näkyvissä. Tällöin käyttäjät eivät voi upottaa sovelluksia sivulle edes välilehtenä.
- **isPowerAppTabPersonalizationEnabled** – Jos tämä menetelmä palauttaa epätosi-arvon tietylle sivulle, käyttäjät eivät voi upottaa sovelluksia suoraan sivulle välilehtenä, pikavälilehtenä tai panoraamaosana. Käyttäjät voivat edelleen upottaa sovelluksia Power Apps -valikkopainikkeella, jos sivu sallii upottamisen.

Seuraavassa esimerkissä on uusi luokka ja kaksi menetelmää, jotka tarvitaan sovellusten upottamista varten.

```powerapps
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
