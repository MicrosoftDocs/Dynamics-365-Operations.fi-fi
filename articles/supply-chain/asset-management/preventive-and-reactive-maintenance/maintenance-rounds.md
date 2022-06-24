---
title: Ylläpitokierrokset
description: Tässä artikkelissa kerrotaan ylläpitokierroksista resurssien hallinnassa.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRoundTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dfb75d69f20c68a40242bb1c0c25ca77f85e0c14
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852868"
---
# <a name="maintenance-rounds"></a>Ylläpitokierrokset

[!include [banner](../../includes/banner.md)]

 

**Resurssien hallinnassa** huoltokierroksia voidaan luoda eri resursseille, joihin on suoritettava samanlainen tehtävä säännöllisin väliajoin. Esimerkiksi voitelutyöt tai turvatarkastustyöt, jotka on suoritettava useilla koneilla samalla aikavälillä. Ensimmäinen vaihe on huoltokierroksen luominen, mukaan lukien käyttökohteet, jotka edellyttävät samaa kunnossapitotyötä. Seuraavaksi ajoitat huoltokierrokset. Kun kunnossapitokierrosten aikataulu on tehty, kaikki kierrokseen liittyvät työtietueet näkyvät kohdassa **Kaikki huoltoaikataulu** ja **Avoimet ylläpitoaikataulurivit**.

>[!NOTE]
>Kunnossapitokierroksia voidaan määrittää myös toiminnallisissa sijainneissa, jotka on tarkoitus suorittaa toiminnallisessa sijainnissa asennettuihin käyttöomaisuuksiin kierrospohjaista työtilausta luotaessa. Lisätietoja toiminnallisten sijaintien ylläpitohuoltokierrosten asetuksista toiminnallisissa sijainneissa on kohdassa [Luo toiminnalliset sijainnit](../functional-locations/create-functional-locations.md).

## <a name="set-up-a-maintenance-round"></a>Ylläpitokierroksen määritys

1. Valitse **Resurssien hallinta** > **Asetukset** > **Ennalta ehkäisevä ylläpito** > **Ylläpitokierrokset**.

2. Luo uusi ylläpitokierros valitsemalla **Uusi**.

3. Lisää tunniste **ylläpitokierros**-kentässä ja ylläpitokierroksen nimi **Nimi**-kentässä.

4. Valitse kierroksen aloituspäivä **Alkamispäivä**-kentässä.

5. Voit lisätä **Päättyminen päivän sisällä**- ja **Päättyminen tunnin sisällä** -kenttiin suunnitellun päätymishetken päivinä tai tunteina. Odotettu päättymispäivämäärä lasketaan suhteessa aloituspäivämäärään, joka lasketaan huoltoaikataulurivien luonnin yhteydessä. Voit esimerkiksi lisätä **Päättyminen päivän sisällä** -kenttään arvon 7, joka ilmaisee, että liittyvä tehtävä on suoritettava viikon kuluessa aloituspäivämäärästä.

6. Valitse "kyllä" **Luo automaattisesti** -vaihtopainikkeesta, jos työtilaukset luodaan automaattisesti ylläpitoaikatauluriveistä, jotka on luotu tästä huoltokierroksesta.

7. Valitse **Työtilauksen tyyppi** -kentässä työtilaustyyppi, jota käytetään tästä ylläpitokierroksesta luoduissa työtilauksissa.

8. Valitse **Palvelun taso** -kentässä työtilauksen palvelutaso, jota käytetään tästä ylläpitokierroksesta luoduissa työtilauksissa.

9. Lisää resurssi ylläpitokirrokseen valitsemalla **Resurssirivit**-pikavälilehdessä **Lisää**.

10. **Rivinumero**- kenttään lisätään automaattisesti rivinumero, joka ilmaisee kunnossapitokierroksen käyttöomaisuuksien järjestyksen.

11. Valitse resurssi **Resurssi**-kentässä.

12. Valitse käyttöomaisuuden kunnossapitotöiden tyyppi **Ylläpitotyön tyyppi** -kentässä.

13. Valitse tarvittaessa **Ylläpitotyön tyypin variantti** ja **Kauppa**, jotka liittyvät kunnossapitotyön tyyppiin.

14. Valitse **Kauden tyyppi** -kentässä toistuvuus (päivä, viikko jne.).

15. Lisää **Jakson frekvenssi** -kenttään ylläpitokierroksen toistumismäärä. Esimerkki: Jos **Kauden tyyppi** -kentässä on valittu "päivä" ja lisäät tähän kenttään numeron "7", uudet kunnossapitokierroksen rivit luodaan ennaltaehkäisevän huollon ajoituksessa kerran viikossa.

16. Valitse kunnossapitokierrokseen sisällytettävän käyttöomaisuuden alkamispäivämäärä **Alkamispäivämäärä**-kentässä. Tämä päivämäärä voi olla eri kuin ylläpitokierrokselle määritetty aloituspäivämäärä.

17. Lisää ylläpitokierrokseen lisää resursseja toistamalla vaiheita 9-16.

18. Lisää toiminnallinen sijainti ylläpitokirrokseen valitsemalla **Toiminnallisen sijainnin rivit**-pikavälilehdessä **Lisää**. Lisätietoja on yllä olevien liittyvien kenttien kuvauksessa. Samat kentät ovat käytettävissä käyttöomaisuusrivin luomisessa, mutta voit tarvittaessa myös valita **valmistajan**- ja **mallin** toiminnalliselle sijainnille. Jos valitset vain rivin toiminnallisen sijainnin, mutta et tee valintoja **Resurssityyppi**, **Valmistaja**, **Malli**, **Ylläpitotyön tyyppi**, **Ylläpitotyön tyypin variantti** ja **Kauppa** -kohdissa, kaikki kyseiseen toiminnalliseen sijaintiin liittyvät käyttökohteet huoltoaikataulutuksen yhteydessä sisällytetään huoltokierrokseen.

19. Valitse huoltokierrokseen sisällytettävä työtilauspooli valitsemalla **Poolit**-pikavälilehdessä **Lisää**. Useita työtilauspooleja voidaan liittää yhteen huoltokierrokseen.

20. Tallenna asetukset.

>[!NOTE]
>**Resurssit**- ja **Rivit**-kentissä (**Otsikko**-pikavälilehden **Tiedot**-ryhmässä) näkyy valittuun huoltokierrokseen liittyvien käyttöomaisuuksien ja rivien kokonaismäärä.

Alla oleva kuva osoittaa esimerkin huoltokierroksesta, joka sisältää kolme käyttöomaisuuserää.

![Kuva 1.](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a>Ajoita ylläpitokierroksia

Kun olet määrittänyt kunnossapitokierroksen, voit ajoittaa kaikki huoltokierrokseen liittyvät työt suorittamalla ajoitustyön.

1. Valitse **Resurssien hallinta** > **Kausittainen** > **Ennalta ehkäisevä ylläpito** > **Ajoita ylläpitokierrokset** tai **Resurssien hallinta** > **Yhteiset** > **Ylläpitoaikataulu** > **Kaikki ylläpitoaikataulut** tai **Avoimet ylläpitoaikataulurivit** tai **Avoimet ylläpitoaikataulupoolit** > valitse ylläpitoaikataulurivi luettelosta > **Ylläpitokierrokset** -painike.

2. Valitse **Kausi**-kentässä kausityyppi, jota käytetään aikataulutuksessa.

3. Lisää **Jakson frekvenssi** -kenttään niiden kausien määrä, jotka sisällytetään ajoitustyöhön. Aikataulun alku on kuluva päivämäärä.

4. Valitse "kyllä" **Luo automaattisesti**- vaihtopainikkeesta, jos työtilaus luodaan automaattisesti huoltokierroksen perusteella.

>[!NOTE]
>Jos tämän vaihtopainikkeen arvoksi on määritetty "kyllä" ja **Luo automaattisesti** -vaihtopainikkeessa on Kyllä valittuna **Ylläpitokierrokset** -lomakkeessa, työtilaukset luodaan huoltokierrosrivien perusteella ja myös ylläpitosuunnitelmarivit, joiden tila on "Työtilaus luotu", luodaan. Jos vain yksi **Luo automaattisesti** -vaihtopainikkeista on määritetty Kyllä-arvoon, tässä avattavassa valikossa tai **Ylläpitokierrokset** -kohdassa luodaan vain huoltoaikataulurivit tilassa Luotu. Tässä tapauksessa työtilauksia ei luoda.

5. Voit tarvittaessa valita aikataulun työlle tietyt kierrokset tai toisen alkamispäivämäärän. Valitse **Suodata** ja lisää sisällytettävät kierrokset.

6. Valitse **OK**.

7. Näet nyt ylläpitokierroksen työt kohdassa **Resurssien hallinta** > **Yhteiset** > **Ylläpitoaikataulu** > **Kaikki ylläpitoaikataulut** tai **Avoimet ylläpitoaikataulurivit**. Jos ajoitetut kierrokset on liitetty työtilauspooliin, huoltoaikataulurivit näkyvät myös kohdassa **Avoimet ylläpitoaikataulupoolit**. Kierroksesta luoduilla ylläpitoaikatauluriveillä on viitetyyppi "Ylläpitokierrokset".

Alla olevat kaksi kuvitusta näyttävät työn aikataulutuksen **Ajoita ylläpitokierroksia** -valintaikkunassa ja huoltoaikataulu rivit, jotka on luotu **Kaikki ylläpitoaikataulut** -kohdassa kyseisen ajoitustyön perusteella.

![Kuva 2.](media/14-preventive-maintenance.png)

![Kuva 3.](media/15-preventive-maintenance.png)

- Kun työtilaukset luodaan manuaalisesti toimittajan takuun kattamille resursseille, näyttöön tulee valintaikkuna, jonka avulla käyttäjä saa tietää takuun. Työtilauksen luonti voidaan sitten peruuttaa. Takuusuhdetta koskeva tarkistus jätetään pois automaattisesti luoduissa työtilauksissa.  
- Voit määrittää eräajon **Suorita taustalla** -pikavälilehdessä, jolloin kierrokset ajoitetaan säännöllisin väliajoin.  
- Jos kierros sisältyy useisiin työtilauspooleihin (lisätietoja on kohdassa [Työtilauspoolit](../work-orders/work-order-pools.md)), kullekin poolille näytetään yksi tietue kohdassa **Avaa ylläpitoaikataulupoolit**. Tämä tehdään työtilauspoolien suodatusasetusten optimoimiseksi.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]