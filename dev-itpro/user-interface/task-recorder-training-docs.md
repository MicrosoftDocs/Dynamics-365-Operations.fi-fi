---
title: "Dokumentaation tai koulutuksen luominen tehtävätallenteiden avulla"
description: "Tässä ohjeaiheessa kerrotaan, mitä tehtävien tallennustoiminto ja tehtäväoppaat ovat, miten tehtävätallenteita luodaan, ja miten Microsoftin tehtäväoppaita voi mukauttaa ja sisällyttää omiin ohjeisiisi."
author: josaw1
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 529751c09b8f99f986cad23a633bea661929d558
ms.openlocfilehash: d5e4857081134808b194d3248dd8739f83b57d6e
ms.contentlocale: fi-fi
ms.lasthandoff: 08/09/2017

---

# <a name="create-documentation-or-training-using-task-recordings"></a>Dokumentaation tai koulutuksen luominen tehtävätallenteiden avulla

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, mitä tehtävien tallennustoiminto ja tehtäväoppaat ovat, miten tehtävätallenteita luodaan, ja miten Microsoftin tehtäväoppaita voi mukauttaa ja sisällyttää omiin ohjeisiisi.

> [!IMPORTANT]
> Dynamics 365 for Talentissa ei voi myöskään luoda mukautettuja tehtäväoppaita. Talentin ohjejärjestelmä yhdistetään automaattisesti tuotteen tehtäväoppaisiin. 

<a name="learn-about-task-recorder"></a>Lisätietoja tehtävän tallennustoiminnosta
-------------------------

Tehtävän tallennustoiminto on työkalu, jolla voi tallentaa tuotteen käyttöliittymässä suoritetut toiminnot. Kun käytät tehtävän tallennustoimintoa, kaikki palvelimen avulla käyttöliittymässä suoritettavat tehtävät, kuten arvojen lisääminen, asetusten muuttaminen ja tietojen poistaminen, tallennetaan. Kaikkia tallennettuja vaiheita kutsutaan *tehtävätallenteeksi*. Tehtävätallenteita voidaan käyttää esimerkiksi seuraavilla tavoilla:

-   **Tehtävätallenteiden toistaminen tehtävän ohjauksina.** Tehtäväoppaat ovat keskeinen osa ohjeita. Tehtäväoppaissa käsitellään hallitusti, ohjatusti ja vuorovaikutteisesti liiketoimintaprosessin eri vaiheet. Käyttäjää ohjataan kunkin vaiheen suorittamisessa ponnahduskehotteen (eli kuplan) avulla. Se esiintyy kaikkialla käyttöliittymässä ja osoittaa käyttöliittymäelementin, johon käyttäjän tulee reagoida. "Kupla" sisältää myös tietoja siitä, miten elementtiä käytetään, kuten "Napsauta tätä" tai "Kirjoita tähän kenttään arvo". Tehtäväopas toimii käyttäjän nykyisen tietojoukon kanssa, ja syötetyt tiedot tallennetaan käyttäjän ympäristöön.
-   **Tehtävätallenteet voidaan näyttää menettelytapavaiheina ohjeruudussa.** Voit käyttää ohjeruutua tehtävätallenteiden hakemisessa ja näyttämisessä. Voit käyttää ohjeruutua valitsemalla siirtymispalkin yläosassa olevan **?**-painikkeen tai pikanäppäimet **Ctrl+Vaihto+?**. Tehtävätallenteen vaiheet näkyvät ohjeruudussa. Voit myös toistaa tallenteen tehtävän ohjauksena, jolloin se ohjaa sinut käyttöliittymän läpi.
-   **Tehtävätallenteet voidaan tallentaa liiketoimintaprosessien mallintajaan (BPM).** Voit tallentaa tehtävätallenteen liiketoimintaprosessien mallintajan (BPM) kirjaston hierarkian riville Lifecycle Services (LCS) -palveluissa. Tallenteesta luodaan vaiheluettelo ja liiketoimintaprosessikaavio. BPM-kirjastoon tallennetut tehtävätallenteet voidaan näyttää ohjeena.
-   **Tehtävätallenteet voidaan tallentaa Word-asiakirjoina.** Tämä mahdollistaa tulostettavien koulutusohjeiden luomisen.

Voit luoda omia tehtävätallenteita, toistaa Microsoftin tehtävätallenteita tai muokata Microsoftin toimittamia tehtävätallenteita omaa konfiguraatiota vastaaviksi. Lisätietoja tehtävien tallennustoiminnosta on kohdassa [Tehtävien tallennustoiminto](task-recorder.md).

## <a name="plan-your-task-recording"></a>Tehtävätallenteen suunnitteleminen
Pidä seuraavat tiedot mielessäsi, kun olet luomassa uutta tehtävätallennetta tai muokkaamassa Microsoftin tehtävätallennetta.

-   Suunnittele tallenne samaan tapaan kuin video. Tee päätökset etukäteen.
-   Käy liiketoimintaläpi kerran tai kaksi ilman tallennusta, jotta vaiheet tulevat tutuiksi.
-   Kun käyt prosessin läpi ennen tallentamista, merkitse muistiin kohdat, joissa käytetään pikanäppäimiä tai **Enter**-näppäintä. Näin niitä ei tarvitse käyttää tallentamisen aikana.
-   Vastaa seuraaviin kysymyksiin:
    -   Haluatko ryhmitellä vaiheet alitehtäviksi? Alitehtävät erottelevat prosessin osat visuaalisesti. Jos olet luomassa esimerkiksi Tuotteen luominen ja vapauttaminen -tallennetta, haluat ehkä ryhmitellä yhteen tuotteen luomisessa ja toisaalta tuotteen vapauttamisessa tarvittavat vaiheet. Alitehtävien avulla pidemmistä prosesseista tulee myös helpommin luettavia.
    -   Haluatko lisätä huomautuksia? Jos haluat, minne ne lisätään? Lisätietoja on kohdassa Tietoja huomautustyypeistä.
    -   Mitä arvoja lisäät eri kenttiin liiketoimintaprosessin vaiheiden suorittamisen yhteydessä? Kannattaa päättää prosessin yhteydessä valittavat tai syötettävät arvot, jotta tallennuksen aikana ei tarvitse palata takaisin tai korjata virheitä.

**Kirjoita kuvaus ja huomautukset etukäteen**

-   Kunkin tehtävätallenteen alussa on kuvauskenttä, johon voi syöttää tallenteen kuvauksen. Kannattaa kirjoittaa ja tallentaa kuvaus etukäteen erilliseen asiakirjaan, jotta voit kopioida ja liittää sen tehtävätallenteeseen tallennuksen aikana. Näin voit hioa tekstiä ennen tallennusprosessia. Tallennusprosessista tulee nopeampi ja sujuvampi leikkaamisen ja liittämisen ansiosta.
-   Voit luoda huomautuksia missä tahansa tehtävätallenteen vaiheessa. Tehtävän ohjauksen toiston aikana huomautukset näkyvät kuplassa huomautuksina vaiheen tekstin ylä- tai alapuolella. Kun tekstiä tarkastellaan ohjeruudussa, huomautukset näkyvät vaiheessa tekstiin sidottuina. Huomautukset kannattaa kuvauksen tavoin kirjoittaa ja tallentaa erilliseen asiakirjaan. Kun olet tallentamassa tehtävätallennetta, voit leikata ja liittää huomautukset asiakirjan vaatimassa muodossa.

**Tietoja huomautustyypeistä** Kaikki huomautukset ovat valinnaisia. Lisää huomautuksia vain silloin, kun ne sisältävät käyttäjälle hyödyllisiä tietoja.

-   **Otsikko**: otsikon huomautus tulee näkyviin ennen tehtävän tallennustoiminnon automaattisesti luomaa vaihetekstiä. Otsikon huomautus näytetään tehtäväoppaassa automaattisesti luodun tekstin yläpuolella. Tämän tyyppisen huomautuksen avulla voit selittää, miksi käyttäjä suorittaa vaihetta. Voit myös antaa lisätietoja kontekstista.

Tämä on muokkausruutu, joka näkyy, kun lisäät huomautuksen tallenteen luomisen yhteydessä. Syötä otsikkohuomautus **Otsikko**-ruutuun. 

[![screen1](./media/screen1.png)](./media/screen1.png) 

Otsikkohuomautus näyttää tältä tehtäväoppaan kuplassa. 

[![screen2](./media/screen2.png)](./media/screen2.png)

-   **Ilmoitukset:** Ilmoitusten huomautus tulee näkyviin tehtävän tallennustoiminnon automaattisesti luoman vaihetekstin jälkeen. Se näkyy tehtävän ohjauksessa vain, jos käyttäjä valitsee tehtävän ohjauksen kuplassa **Näytä lisää** -linkin. Voit käyttää tämän tyyppistä huomautusta kuvatessasi mitä tahansa tahansa käyttäjän vaiheen suorittamisessa tarvitsemia tietoja.

Tämä on muokkausruutu, joka näkyy, kun lisäät huomautuksen tallenteen luomisen yhteydessä. Syötä ilmoitusten huomautus **Ilmoitukset**-ruutuun. 

[![screen3](./media/screen3.png)](./media/screen3.png) 

Ilmoitusten huomautus näyttää tältä tehtäväoppaan kuplassa.

[![screen4](./media/screen4.png)](./media/screen4.png)

-   **Tiedot-vaihe**: Nämä huomautukset luodaan napsauttamalla ohjausobjektia tai jotain lomakkeen kohtaa hiiren kakkospainikkeella &lt; **Tehtävän tallennustoiminto** &lt; **Lisää Tiedot-vaihe. **Tiedot-vaiheet näkyvät numeroituina vaiheina paikassa, johon ne lisätään, vaikka toimintoa ei olisi tallennettu käyttöliittymässä. Voit lisätä lomaketason Tiedot-vaiheen tai ohjausobjektiin liitetyn Tiedot-vaiheen. Kun Tiedot-vaihe on liitetty lomakkeeseen, tehtävän ohjauksen kupla tulee näkyviin lomakkeeseen ilman osoitinta tehtävän ohjauksen toiston aikana. Kun Tiedot-vaihe on liitetty ohjausobjektiin, tehtävän ohjauksen kupla tulee osoittaa ohjausobjektiin tehtäväoppaan toiston aikana. Ohjeruudussa näkyy Tiedot-vaiheen huomautus numeroituna vaiheena. Huomautus sisältää syöttämäsi tekstin. Käytä Tiedot-vaiheita käyttäjän valmisteluun seuraavia vaiheita varten, Microsoft Dynamics 365 for Finance and Operations Enterprise editionin ulkopuolella tehtäviä vaiheita varten tai muihin tallenteisiin viittaamisessa (vaikka huomautuksiin ei voikaan luoda hyperlinkkejä).

**Määritä, miten pitkä tallenteesta tulee**

-   Käyttäjä lukee tai toistaa tallenteen yleensä alusta loppuun, joten älä yhdistele vaiheita tai tehtäviä, jotka on paras tehdä erikseen.
-   Älä yritä tallentaa pitkää useita aliprosesseja sisältävää skenaariota. Esimerkiksi Myymälän asiakaspalvelupisteen toiminnot on liian laaja aihe. Jaa se lyhyempiin tehtäviin, kuten Palautusten vastaanotto ja Lisää lahjakorttiin.
-   Jos tehtävä voidaan suorittaa useiden eri liiketoimintaprosessien osana, luo sille erillinen tallenne, johon voit viitata muissa tallenteissa.
-   Jos prosessi käsittää useita tehtäviä, jotka henkilö luultavasti tekee kerralla, voit sisällyttää ne yhteen tallenteeseen. Tällainen tallenne voi olla esimerkiksi Toiminnallisuusprofiilien määrittäminen ja liittäminen.
-   Jos käyttäjä suorittaa jonkin tehtävän kerralla (kuten konfiguroiminen) ja heti tämän jälkeen toisen itsenäisen tehtävän, joka saatetaan toistaa, jaa tehtävät kahteen erilliseen tallenteeseen.

**Päätä, missä kohtaa käyttöliittymää tallentaminen alkaa** Sivu, jolla olet tehtävätallenteen tallentamisen alkaessa, vaikuttaa siihen, millä sivulla tehtävän ohjaus näytetään. Jos haluat tehtävätallenteen olevan esimerkiksi ohjeruudussa, kun käyttäjä valitsee Kirjanpitoparametrit-sivun, sinun on aloitettava tallentaminen Kirjanpitoparametrit-sivulta. **Tallenna tallenteet .axtr-tiedostoina** Kun olet luonut tehtävätallenteen tai muokannut sitä, näkyviin tulee useita tallenteen lataus- tai tallennusvaihtoehtoja. Voit ladata tiedoston tehtävätallenteen pakettina (.axtr) tai käsittelemättömänä tallennetiedostona (.xml) tai Word-asiakirjana tai tallentaa tiedoston LCS-kirjastoon. Tehtävätallenne kannattaa aina tallentaa tehtävätallenteen pakettitiedostona (.axtr). Se helpottaa tiedoston ylläpitoa, jos menettelyitä tai huomautuksia on muutettava myöhemmin. Jos haluat noutaa tiedoston Word-asiakirjana, tallenna se myös silloin tehtävätallenteen pakettitiedostona.

## <a name="create-your-task-recording"></a>Tehtävätallenteen luominen
Yksityiskohtaiset vaiheet löytyvät kohdasta [Tehtävätallenteen luominen](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Microsoftin tehtävätallenteiden kopioiminen ja mukauttaminen
Voit ladata ja muokata Microsoftin tehtävätallenteita, kun haluat käyttää niitä omassa dokumentaatiossa tai koulutusmateriaaleissa. Lataa Microsoftin tehtävätallenteet seuraavien vaiheiden avulla:

1.  Avaa tehtävien tallennustoiminto Tehtävän tallennustoiminto sijaitsee **asetusvalikossa**.
2.  Valitse tehtävän tallennustoiminnon ruudussa **Ylläpidä tallennetta.**
3.  Valitse **Missä tallenne on** -kohdassa **Se on LCS-kirjastossa**.
4.  Valitse **Valitse LCS-kirjasto**.
5.  Valitse yleinen Microsoft-kirjasto.
6.  Valitse puussa se liiketoimintaprosessin solmu, johon tehtävätallenne on liitetty.
7.  Napsauta **OK**.
8.  Valitse **Käynnistä**.
9.  Käy tässä vaiheessa tallenne läpi ja muuta vaiheita uudelleentallennuksen yhteydessä. **Huomautus**: Jos haluat muuttaa vain tallenteen tekstiä, voit avata tallenteen **Muokkaa tallenteen huomautuksia** -tilassa ja tallentaa sen uudelleen.
10. Kun olet päässyt tallenteen toistossa loppuun, valitse näytön yläosassa olevan tehtävän tallennustoiminnon palkissa **Pysäytä**.
11. Määritä tehtävätallenteen tallennustapa.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Tehtävätallenteiden sisällyttäminen ohjeruutuun
Voit näyttää omat mukautetut tehtävätallenteen ohjeruudussa tehtävän ohjauksina toistettavina tai tekstinä tarkasteltavina. Tallenna tehtävätallenteet ensin omaan BPM-kirjastoon ja päivitä ohjejärjestelmän parametrit niin, että ne osoittavat BPM-kirjastoon. Lisätietoja on kohdassa [Yhteyden muodostaminen ohjejärjestelmään.](../get-started/help-connect.md)

<a name="see-also"></a>Lisätietoja
--------

[Ohjeen yleiskatsaus](..\get-started\help-overview.md)

[Yhdistämisen ohje](..\get-started\help-connect.md)

[Tehtävien tallennustoiminto](task-recorder.md)

[Monipuolisten ohjeaiheiden luominen tehtävien tallennustoiminnolla (ulkoinen linkki)](https://mbspartner.microsoft.com/AX/Videos/970)

