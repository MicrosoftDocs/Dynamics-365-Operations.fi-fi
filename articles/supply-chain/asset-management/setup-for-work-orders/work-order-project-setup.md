---
title: Työtilauksen projektiasetukset
description: Tässä ohjeaiheessa selitetään työtilausten projektin määritys käyttöomaisuuden hallinnassa.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjectSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bb897ca0a7e9c45ee55244189bb1b487fbddf0714ad3ea0cac26eb7bac36a07f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754080"
---
# <a name="work-order-project-setup"></a>Työtilauksen projektiasetukset

[!include [banner](../../includes/banner.md)]

 

**Resurssien hallinta** -moduulissa jokaiselle työtilaustyölle tarvitaan projektisuhde. Työtilaustyöhön liittyvän projektin avulla voit jäljittää eri projektien, jotka liittyvät omaisuuden hallintaan, kustannuksia, kuten sisäisiä ylläpitoprojekteja, huoltohallinnan projekteja ja investointiprojekteja. 

## <a name="project-setup-for-a-work-order-job"></a>Työtilaustyön projektiasetukset

Kun luot työtilaustyön työtilaukseen, **Projektinhallinta ja kirjanpito** -moduulin projektimääritykset **Resurssien hallinta** -moduulissa määräävät, miten projekteja voidaan käyttää kustannusseurantaan kyseisessä työtilaustyössä valitulle resurssille. Tässä osassa kuvataan seuraavat projektin asetusten osat, joita käytetään työtilauksessa: pääprojekti (projektin tunnus), projektityyppi, projektitehtävät ja taloushallinnon dimensiot:

- Kun luot työtilaustyön työtilaukseen, sille luodaan automaattisesti yksilöivä projektitunnus ja siihen liittyvä projektitehtävä. Jos työtilauksen useissa työtilaustöissä on kuitenkin sama resurssi, niitä varten käytetään samaa projektitunnusta. Toisin sanoen jokaiselle työtilauksen resurssille luodaan yksi projektitunnus.

    - Työtilaustyön pääprojekti (projektitunnus) löytyy pääprojektin asetuksista. (Lisätietoja pääprojektin asetuksista on seuraavassa osiossa.) Jos esimerkiksi liität asiakkaan tai toimintosijainnin tiettyyn pääprojektiin, pääprojektia käytetään aina, kun luot työtilauksia kyseiselle asiakkaalle tai kyseiselle toiminnalliselle sijainnille. Jos et liitä tiettyä projektitunnusta esimerkiksi toiminnalliseen sijaintiin, käytetään seuraavan asiaankuuluvaa pääprojektia työtilausprojektin asetuksissa.
    - Kaikki projektitunnukset edellyttävät projektityyppiä. Projektityyppi löytyy projektiryhmän asetusten asetuksista. (Lisätietoja projektiryhmän asetuksista on seuraavassa osiossa.) Jos projektiryhmän asetuksista ei löydy vastinetta, käytetään pääprojektin projektiryhmän asetuksia.
    - Projektin ennusteiden ja kirjauskansioiden projektitehtävien vaatimien projektitehtävien määrittäminen kopioidaan pääprojektista työtilausprojektiin. Jos pääprojektina käytettävän projektin **Tunti**-, **Kulu**- ja **Nimike**-asetuksiksi on määritetty **Kyllä**, projektitehtävä on pakollinen ennusteissa ja kirjauskansioissa. (Voit käyttää näitä asetuksia valitsemalla **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit** ja valitsemalla sitten projektin, jota käytetään pääprojektina. Vaihtoehdot ovat **Vaadi tehtävä kirjauskansioihin** -osassa **Asetukset** -pikavälilehdessä.)

- Taloushallinnon dimensiot kopioidaan käyttöomaisuuserästä ja yhdistetään pääprojektiin.

Seuraavassa osassa selitetään, kuinka pääprojektit ja projektiryhmät määritetään. Pääprojektia ja pääryhmiä käytetään työtilausten hallinnassa. Niitä käytetään myös työtilausten raportoinnissa.

## <a name="set-up-work-order-projects"></a>Työtilausprojektin asetukset

Ennen työtilausten luomista on määritettävä työtilausprojektit. **Työtilausprojektin asetukset** -sivu (**Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Projektin asetukset**) sisältää kaksi väli lehteä: **Pääprojekti** ja **Projektiryhmä**.

**Pääprojekti** -välilehdessä voit määrittää projektisuhteita, joita voidaan käyttää, jos työtilaustyössä valitulle käyttö omaisuudelle ei ole määritetty projektia. Pääprojektin asetuksia ei vaadita, jos yrityksessä käytetään resurssiprojekteja. Se on merkityksellinen vain, jos haluat käyttää työtilausprojekteja resurssiprojektien asemesta. Tällöin vähintään yksi pääprojekti on määritettävä.

**Projektiryhmä**-välilehdessä voit määrittää projektiryhmiä, jotka voidaan liittää työtilaustyyppeihin, resurssityyppeihin ja resursseihin.

Projektiryhmien avulla voidaan luoda tiettyjä kustannusvalvonnassa käytettäviä luokkia (ryhmiä). Esimerkiksi luomalla projektiryhmiä tietyille käyttöomaisuustyypeille tai työtilaustyypeille voit tehdä yksityiskohtaisen seurannan ylläpitokustannuksille tyypin mukaan.

Projektiryhmät eivät ole pakollisia. Jos et määritä projektiryhmiä, pääprojektin avulla määritetään projektiryhmä ja aliprojekti luodaan pääprojektin projektiryhmästä.

Nämä asetukset mahdollistavat täydellisen integroinnin **Projektinhallinta ja kirjanpito** -moduuliin. Näin voit jäljittää liittyvien projektien työtilauksiin liittyvät kustannukset. Seuraavassa menettelyssä kuvaillaan työtilausprojektien asetuksia.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Projektiasetukset**.
2. Valitse **Pääprojekti**-välilehdellä **Lisää**.
3. Valitse **Työtilauksen tyyppi**-, **Toiminnallinen sijainti**-, **Resurssityyppi**- ja **Resurssi**-kentistä haluamasi arvot. Voit määrittää kullekin lisäämällesi riville vain yhden kentän tai useita kenttiä. Määrittämäsi kenttien määrä määrittää yhdistelmän, jota käytetään, kun projektin tunnus valitaan käyttöomaisuuden hallinnassa. 

    Jos valitset toimintosijainnin, siihen liittyvät alatason sijainnit sisällytetään automaattisesti. Jos valitset käyttöomaisuuserän, voit luoda lisää työtilausprojektin asetusrivejä samalle käyttöomaisuuserälle, mutta voit valita eri projekteja kyseiselle käyttöomaisuudelle.

4. Valitse **Projektitunnus** -kentästä projekti, jonka tulisi liittyä vaiheessa 3 luomiisi asetuksiin.
5. Jos projektin asetusten tulisi olla voimassa vain rajoitetun ajan, valitse päättymispäivämäärä **Päättymispäivämäärä**-kentässä. Muussa tapauksessa valitse **Ei mikään**.

    Oletusarvon mukaan aloituspäivämäärä on päivämäärä, jolloin työtilausprojekti lisätään sivulle. Sen hallinnassa on **Voimassa alkaen** -kenttä, joka on oletusarvoisesti piilotettu. Jos haluat näyttää **Voimassa alkaen** -kentän, valitse **Näytä** \> **Kaikki**. Tämän jälkeen voit käyttää **Voimassa alkaen** -kenttää yhdessä **Päättymispäivämäärä**-kentän kanssa määrittämään rajoitetun voimassaoloajan työtilausprojektille.

    ![Työtilausten projektinmäärityssivu.](media/17-setup-for-work-orders.png)

6. Valitse **Projektiryhmä**-välilehdellä **Lisää**.
7. Valitse **Työtilaustyyppi**-kentässä työtilauksen tyyppi.
8. Jos haluat, että projektiryhmän liitos on tarkempi, valitse käyttöomaisuustyyppi **Resurssityyppi**-kentästä tai käyttöomaisuuserä **Resurssi**-kentästä.
9. Valitse **Projektiryhmä**-kentästä projektiryhmä, joka liittyy työtilaustyyppiin. Esimerkiksi **Ennalta ehkäisevä ylläpito** -niminen työtilaustyyppi voi liittyä projektiryhmään, jonka nimi **Enn. ylläp.** tai **Sisäinen.** Vaihtoehtoisesti **Investointi**-työtilaustyyppi, jota käytetään investointeihin ja käyttöomaisuuteen liittyviin työtilauksiin, voidaan liittää projektiryhmään, jonak nimi on **Investoi** tai **Investointi**.
10. Valitse **Tallenna**.

![Työtilausten projektinmäärityssivu, työtilauksen lisääminen.](media/18-setup-for-work-orders.png)

> [!NOTE]
> Aina, kun työtilausrivi luodaan, käyttöomaisuuden hallinta etsii projektiryhmää, joka liittyy työtilaustyön projektiin. Haku perustuu tässä ohjeaiheessa kuvattuihin asetuksiin. Jokaisella projektiryhmällä on siihen liittyvä projektityyppi. Projektiryhmät, joissa on **Aika ja materiaali**- tai **Kiinteähintainen** projektityyppi, ovat kelvollisia vain asiakastiliin liittyvissä resursseissa.
>
> Kun järjestelmä valitsee käytettävissä olevan työtilausprojektin tai projektiryhmän pääprojekteille ja projektiryhmille, valinta perustuu edellä kuvatun menetelmän avulla luomiisi tietueisiin. Käyttöomaisuuden hallinta käy läpi työtilausprojektiin liittyvät tietueet ja tarkistaa mahdolliset vastineet. Se tarkistaa aina kaikkein erikoisimman yhdistelmän ensin. Toisin sanoen resurssien hallinta tarkistaa työtilauksen pääprojektille ensin mahdollisen **Resurssi**-kentän vastaavuuden. Jos vastaavuutta ei löydy, se tarkistaa **Resurssityyppi**-kentän vastaavuuden. Jos vastaavuutta ei löydy, se tarkistaa **Toiminnallinen sijainti** -kentän vastaavuuden ja niin edelleen. Kuten näet **Työtilausprojektin asetukset** -sivun asettelussa, tämä tarkoittaa sitä, että jos haluat löytää erityisen yhdistelmän, resurssien hallinta tarkistaa kunkin tietueen oikealta vasemmalle, jotta se vastaa toisiaan. Jos vastinetta ei löydy, käytetään oletustietuetta, jossa valitaan vain projektitunnus. Liittyvän projektiryhmän hakuprosessi on samankaltainen. Käyttöomaisuuden hallinta tarkistaa ensin **Resurssi**-kentän mahdollisen vastaavuuden, sitten **Resurssityyppi** -kentän ja sitten **Työtilauksen tyyppi** -kentän vastaavuuden. Jos vastinetta ei löydy, käytetään oletustietuetta, jossa valitaan vain projektiryhmä.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]