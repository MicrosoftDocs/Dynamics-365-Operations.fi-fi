---
title: "Yleistä Ohjeesta"
description: "Tämä artikkeli sisältää Microsoft Dynamics 365 for Operations -ohjejärjestelmän komponenttien yleiskatsauksen. Artikkelissa kerrotaan myös, miten voit luoda organisaatiosi mukautetun ohjeistuksen ja koulutuksen."
author: margoc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16381
ms.assetid: 018c148c-9cbd-41e0-8186-d75dbf66288f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 240060606c8a2955c3f0a0d47fb25b0cde64c187
ms.lasthandoff: 03/31/2017


---

# <a name="help-overview"></a>Yleistä Ohjeesta

Tämä artikkeli sisältää Microsoft Dynamics 365 for Operations -ohjejärjestelmän komponenttien yleiskatsauksen. Artikkelissa kerrotaan myös, miten voit luoda organisaatiosi mukautetun ohjeistuksen ja koulutuksen. 

Microsoft 365 for Operations -järjestelmässä on uudistettu ohjejärjestelmä, joka perustuu kahteen pääkomponenttiin:

-   Sivuston asiakirjat
-   tehtäväopastukseen

Pääsee sekä artikkeleita ja apuviivat tehtävän Dynamics 365 toimintojen Ohje-ruudun seuraavan näyttökuvan esitetyllä tavalla. [![Ohje-ruudun](./media/help-pane-ops-task-guides-1024x741.png)](./media/help-pane-ops-task-guides.png) tässä artikkelissa kuvataan ohjeen ja kerrotaan, kuinka voit luoda organisaatiolle mukautettuja dokumentaatio- ja koulutuksen resursseja.

## <a name="help-on-docsmicrosoftcom"></a>docs.microsoft.com Ohje
docs.microsoft.com-sivuston ([docs.microsoft.com/dynamics365/operations](https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations) on ensisijainen lähde Dynamics 365 toimintojen ohjeissa. Sivusto sisältää seuraavat ominaisuudet:

-   **Viimeisin sisältö pääsy** – sivusto antaa meille nopeampi ja joustavampi tapa luoda, toimita ja Päivitä tuotteen ohjeissa. Niinpä saatkin aina käyttöösi uusimmat tekniset tiedot.
-    **Sisältöä, joka on asiantuntijoiden kirjoittama** – sivusto tarjoaa tuotteen ohjeissa, jotka voidaan parantaa yhteisön jäsenten sekä sisä- että ulkopuolella Microsoft joukko lisälähteitä.
-   ** Erilaista sisältöä ** – sivuston käytön mahdollistaa nopean käyttää erityyppisiä sisältöä Dynamics 365 toimintoja, esimerkiksi Microsoft Office-Mix, tehtävän apuviivat, videot, esitykset ja wiki-artikkeleita.
-    **Sisältö, joka tukee liiketoimintaprosesseja** – sivusto sisältää business process suunnatusta sisältöä, joka hyödyntää Business Process Mallintaja (BPM) Microsoft Dynamics Lifecycle Services (LCS).

Olemme olet siirtää kaikki sisältö meidän edellisen ohjeen wiki-asiak. Olemme erittäin iloisia saadessamme meidän uusi sivusto ja toivoen, jotka ovat liian.

### <a name="when-can-we-use-it"></a>Milloin sitä voi käyttää?

Voit lukea asiakirjoja sisältö juuri nyt--vaatimatta sisään on täysin julkisia ja niitä voidaan etsiä. Voit etsiä sisältöä suosikkihakupalvelusi kautta. Sivuston artikkelit voivat kommentoida, jos valitset käyttämällä GitHub tilille.


## <a name="task-guides"></a>tehtäväopastukseen
Tehtävä opas on valvottu, Avustava, vuorovaikutteinen kokemus, joka opastaa käyttäjää tehtävän tai liiketoimintaprosessin vaiheita. Voit avata Ohje-ruudun (play) tehtävän opas. Kun klikkaat tehtävä-opas, Ohjeruutu näkyy tehtävän ohjeet. Lokalisoitu tehtävän oppaat ovat nyt saatavana. [![Tehtävä opas lukee näkymän](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png) Käynnistä ohjattu, vuorovaikutteisia kokemuksia, **tehtävän pikaopas** Ohje-ruudun alaosassa. Musta osoitin avautuu ja ilmaisee suoritettavan toiminnon. Noudata käyttöliittymän ohjeita ja anna tiedot ohjeiden mukaisesti. [![Tehtävän ohjeet opas vaihe](./media/task-guide-step-1-ops.png)](./media/task-guide-step-1-ops.png)**tärkeää:** tiedot, jotka kirjoitat kun toistat tehtävän opas on todellinen. Jos olet tuotantoympäristössä, tiedot annetaan käytössä olevassa yrityksessä.

### <a name="it-all-begins-with-task-recorder"></a>Tehtävän tallennustoiminto

Tehtävän ohjaukset luodaan tehtävän tallennustoiminnolla. Kun käytät tehtävätallennetta, kaikki Dynamics 365 for Operations -käyttöliittymässä tekemäsi toimet (kuten valikoiden napsauttaminen, asetusten muuttaminen ja tietojen antaminen) tallennetaan. Kaikkia tallennettuja vaiheita kutsutaan tehtävätallenteeksi. Kuten edellisessä osassa selitettiin, tehtävätallenteet voidaan näyttää Ohje-ruudussa ja ne voidaan toistaa tehtävän opastuksena. Tehtävätallenteita voi kuitenkin käyttää myös muilla tavoin:

-   **Tallenna tehtävätallenteet BPM:hen** – Voit tallentaa tehtävätallenteen BPM-kirjaston rivihierarkiaan LCS-palveluissa. Kun tallennat tehtävätallenteen BPM:hen, muodostettava vuokaavio voidaan näyttää yhdessä tallennevaiheiden kanssa. **Huomautus:** Jos haluat näyttää tehtävätallenteen Dynamics 365 for Operations -ohje-ruudussa ja toistaa sen tehtävän ohjauksena, tallenne on tallennettava BPM-kirjastoon.
-   **Tallenne tehtävätallenteet Word-asiakirjoina** – kun tallennat tehtävätallenteen Microsoft Word -asiakirjana, voit luoda helposti tulostettavia koulutusoppaita organisaation käyttöön;

Saat lisätietoja tehtävän tallennus [tehtävän tallennus-Dynamics 365 työvaiheiden](../user-interface/task-recorder.md).

### <a name="creating-customized-task-recordings"></a>Mukautettujen tehtävätallenteiden luominen

Voit luoda omia tehtävätallenteita tai ladata ja mukauttaa Microsoftin toimittamia tehtävätallenteita. Voitkin luoda organisaatiolle mukautetun ohjeen, joka vastaa juuri kyseistä Dynamics 365 for Operations -käyttöönottoa. Tehtävän merkitseminen Dynamics-365 toimintojen Ohje-ruudun ja apuna tehtävän toistumaan, sinun tulee tallentaa nauhoituksen BPM LCS-kirjastoon. Jos olet kumppani ja edistää yrityksen kirjastoon, kirjaston ja sisällyttää sen ratkaisun, se on saatavilla asiakkaille. Täydelliset ohjeet ovat kohdassa [tehtävän tallenteiden avulla asiakirjat tai koulutuksen](../user-interface/task-recorder.md).

## <a name="in-product-help"></a>Tuotteen sisäinen ohje
Voit käyttää Dynamics 365 toimintojen ohjeen sisältöön valitsemalla joko **Ohje** (**?**) kuvaketta ja valitse Ohje tai paina Ctrl + Vaihto +?. Kumpikin menetelmä avaa Ohje-ruudun. Ohje-ruudun voit käyttää artikkelit tai tehtävän apuviivat. [![](./media/help-pane-wiki-1024x684.png)](./media/help-pane-wiki.png)

### <a name="accessing-articles-from-the-help-pane"></a>Ohje-ruudun pääsyn artikkelit

Ohje-ruudun avulla voit käyttää artikkelit, jotka liittyvät toiminnot asiakkaan Dynamics-365. Kun ensin avata Ohje-ruudun ja valitsemalla **Wiki** -välilehden näet, jotka koskevat sivulle, jota olet parhaillaan operaatioille Dynamics 365 artikkeleita. Jos ei ole artikkeleita löytyy, voit kirjoittaa avainsanat, joilla Tarkennat hakua. Kun napsautat Ohje-ruudusta artikkelin, uuden välilehden selaimeen avautuu ja näyttää artikkelin. 

### <a name="accessing-task-guides-from-the-help-pane"></a>Tehtävän apuviivojen käyttäminen Ohje-ruudusta

Ennen kuin voit käyttää Ohje-ruudun tehtävän apuviivat, järjestelmänvalvojan on Go to **järjestelmäparametrit** toimintojen 365 Dynamics-sivu ja määrittää joitakin asetuksia. **Huomautuksia:**

-   Ohjeen määrittäminen edellyttää, että olet kirjautunut tilille sinä vuokraajana, jossa Dynamics 365 for Operations on otettu käyttöön.
-   LCS-kirjastoon ei voi muodostaa yhteyttä Dynamics 365 for Operations -esiintymästä, jota käytetään paikallisella virtuaalikiintolevyllä (VHD).

[![Järjestelmän parametrit-lomakkeen asetusten Ohje](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) käyttöön **järjestelmäparametrit** -sivulla seuraavasti:

1.  **Tärkeää: **Kun avaat Ohje-välilehden ensimmäisen kerran, sinun on muodostettava yhteys Lifecycle Services -palveluun. Muista linkkiä lomakkeen keskelle, odota yhteyden, sulje valintaikkuna ja valitsemalla Hae Parametrit-lomakkeesta OK. [![Muodostaa LCS](./media/connect-to-lcs-crop-1024x365.png)](./media/connect-to-lcs-crop.png)
2.  Valitse Lifecycle Services -projekti, johon yhteys muodostetaan.
3.  Valitse BPM-kirjastot (valitussa projektissa), josta tehtävätallenteet noudetaan.
4.  Määritä BPM-kirjastojen näyttöjärjestys. Tämä asetus määrittää, missä järjestyksessä kirjastojen tehtävätallenteet näkyvät Ohje-sivulla.

Kun järjestelmänvalvoja on suorittanut nämä vaiheet, voit avata Ohje-ruudun ja valita **Tehtävän ohjaukset** -välilehden. Nyt näet tehtävän apuviivat, jotka koskevat sivulle, jota olet parhaillaan Dynamics 365 operaatioille. Jos tehtävä ei ole apuviivat löytyy, voit syöttää avainsanat, joilla Tarkennat hakua. Kun valitset Ohje-tehtäväruudussa, tehtävä opas Ohjeruutu näkyy vaiheittaiset ohjeet ja voit pelata tehtävä opas. [![Tehtävä opas lukunäkymässä](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png)

### <a name="where-are-the-translated-task-guides"></a>Missä ovat käännetty tehtävän apuviivat?

Käännetty tehtävän apuviivat on julkaissut kirjastot "kaikki kielet-otsikossa. Dynamics 365 työvaiheissa Nähdäksesi lokalisoitu tehtävän opas auttaa Varmista, että olet muodostanut yhteyden apppropriate-kirjasto. Kieli, joka näkyy tehtävän opas ohjaa kunkin käyttäjän kieliasetusten **asetukset**&gt;**asetukset**. 
-   Jos tehtävä on Ohje on käännetty, kun avaat kyseisen tehtävän opas tehtävän oppaan teksti näkyy valitulla kielellä.
-   Jos tehtävän opas on ei ole vielä käännetty, kun se avataan, vain joitakin tekstin (teksti, ohjausobjektit) näkyvät valitulla kielellä.

## <a name="additional-resources"></a>Lisäresurssit
Seuraavassa taulussa on luettelo sivustoista, joissa on Microsoft Dynamics 365 for Operations -sisältöä. Sisältösivustomme on järjestetty tukemaan asiakkaan elinkaarta. Kullakin vaiheella on omat tukisivustot. Sivustot tähdellä merkittyjä (\*) vieressä edellyttää, että kirjaudut sisään käyttämällä tiliä, joka liittyy palvelun suunnitelma.

| Sivusto                                                                     | kuvaus                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Docs.microsoft.com](https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations) | Kaiken Dynamics 365 for Operations -tuoteohjeistuksen ylläpito tai linkitys.                                                                                                                                                               |
| [Lifecycle Services](http://lcs.dynamics.com/en/)\*                      | Pilvipalveluihin perustuva yhteinen työtila, jota asiakkaat ja heidän kumppaninsa voivat käyttää Dynamics 365 for Operations -projektien hallintaan ennen myyntiä, täytäntöönpanon aikana ja sen työvaiheissa. Sivustossa on apua käyttöönoton kaikissa vaiheissa. |
| [CustomerSource-sivustoon](http://www.customersource.com/)\*                       | Ylläpitää kattavia koulutusresursseja ja on Dynamics 365 for Operations -järjestelmän ensisijainen tukisivusto. Sivuston tiettyjen resurssien käyttö voi edellyttää kirjautumista.                                                                      |
| [Tuki blogi](http://aka.ms/AXSupportBlog)                              | Sisältää Dynamics 365 for Operations -tukiryhmän julkaisemia vinkkejä.                                                                                                                                                  |
| [MSDN](http://aka.ms/AXMSDN)                                             | Ylläpitää aiempien versioiden kehittäjille kirjoitettua sisältöä.                                                                                                                                                                       |
| [TechNet](http://aka.ms/TechNet)                                         | Ylläpitää aiempien versioiden sisältöä, joka on kirjoitettu IT-asiantuntijoille ja sovelluksen käyttäjille.                                                                                                                                           |
| [Dynamics-yhteisö](http://community.dynamics.com/en/)                  | Ylläpitää blogeja, keskustelupalstoja ja videoita.                                                                                                                                                                                                           |
| [Microsoft.com/Dynamics/](http://www.microsoft.com/dynamics/)                 | Sisältää arviointi- ja myyntitietoja.                                                                                                                                                                                                 |



<a name="see-also"></a>Lisätietoja
--------

[Työvaiheiden 365 Dynamics ohjeessa (ladattavat seikka arkkia)](https://mbs.microsoft.com/files/public/CS/AX2012R3/DynamicsAXHelpSystemFactSheet.pdf)

[Tehtävän tallennus Microsoft Dynamics 365 operaatioille](../user-interface/task-recorder.md)

[Dokumentaation tai koulutuksen luominen tehtävätallenteiden avulla](../user-interface/task-recorder.md)

[Uudet tai päivitetyt tehtävä auttaa (marraskuu-2016)](new-task-guides-november-2016.md)<ph id="t1">
</ph>[uusi tai päivitetty tehtävä auttaa (elokuuta 2016)](new-updated-task-guides-available-august-2016.md)<ph id="t2">
</ph>[uusi tai päivitetty tehtävä auttaa (toukokuussa 2016)](new-updated-task-guides-available-may-2016.md)<ph id="t3">
</ph>[uusi tehtävä auttaa (helmikuu 2016)](new-task-guides-available-february-2016.md)






