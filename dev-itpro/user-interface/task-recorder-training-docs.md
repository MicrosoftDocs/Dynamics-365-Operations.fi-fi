---
title: "Dokumentaation tai koulutuksen luominen tehtävätallenteiden avulla"
description: "Tässä ohjeaiheessa kerrotaan, mitä tehtävän tallennus ja tehtävä apuviivat ovat tallenteiden tehtävän luomisesta ja mukauttamisesta Microsoft tehtävä ohjaa ja sisällyttää ne ohjeet."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 38bce4a843f0db575c8d1ba08b7dc2ece8366663
ms.lasthandoff: 03/31/2017


---

# <a name="create-documentation-or-training-using-task-recordings"></a>Dokumentaation tai koulutuksen luominen tehtävätallenteiden avulla
Tässä ohjeaiheessa kerrotaan, mitä tehtävän tallennus ja tehtävä apuviivat ovat tallenteiden tehtävän luomisesta ja mukauttamisesta Microsoft tehtävä ohjaa ja sisällyttää ne ohjeet.

<a name="learn-about-task-recorder"></a>Lisätietoja tehtävän tallennustoiminnosta
-------------------------

Tehtävän tallennus on Microsoft Dynamics-365-toiminnot-työkalu, jonka avulla voit nauhoittaa toimia, jotka tuotteen käyttöliittymän (UI) kestää. Kun käytät tehtävän tallennustoimintoa, kaikki palvelimen avulla käyttöliittymässä suoritettavat tehtävät, kuten arvojen lisääminen, asetusten muuttaminen ja tietojen poistaminen, tallennetaan. Kaikkia tallennettuja vaiheita kutsutaan *tehtävätallenteeksi*. Tehtävätallenteita voidaan käyttää esimerkiksi seuraavilla tavoilla:

-   **Tehtävätallenteiden toistaminen tehtävän ohjauksina.** Tehtävän apuviivat ovat toimintojen avulla kokemusta Dynamics-365 erottamaton osa. Tehtävä opas on valvottu, Avustava, vuorovaikutteinen kokemus, liiketoiminnan prosessin vaiheet. Käyttäjää ohjataan kunkin vaiheen suorittamisessa ponnahduskehotteen (eli kuplan) avulla. Se esiintyy kaikkialla käyttöliittymässä ja osoittaa käyttöliittymäelementin, johon käyttäjän tulee reagoida. "Kuplan" sisältää myös tietoja vuorovaikutteisesti sivun osaan, kuten "Napsauta tätä" tai "Kirjoita tähän kenttään arvo." Tehtävä opas toimii käyttäjän tietojen joukkoa vastaan ja syötetyt tiedot on tallennettu käyttäjän ympäristössä.
-   **Tehtävän tallenteita voi näyttää ohjeruudun koskevia käsitteellisiä ohjeita.** Ohje-ruudun avulla voit etsiä ja tuoda näkyviin tehtävän tallenteita. Voit käyttää Ohje-ruudun napsauttamalla **?** Kuvaketta yläosan siirtymispalkista tai näppäinyhdistelmä, voit käyttää **Ctrl + Shift +?**. Voit lukea ohjeita tehtävän tallennus Ohje-ruudusta tai voit halutessasi asettaa pelata niin se opastaa Käyttöliittymän apuna tehtävän tallennus.
-   **Tehtävätallenteet voidaan tallentaa liiketoimintaprosessien mallintajaan (BPM).** Voit tallentaa tehtävätallenteen liiketoimintaprosessien mallintajan (BPM) kirjaston hierarkian riville Lifecycle Services (LCS) -palveluissa. Tallenteesta luodaan vaiheluettelo ja liiketoimintaprosessikaavio. Tehtävän tallenteita, jotka on tallennettu kirjastoon BPM nähdään Dynamics 365 toiminnoissa kuten ohjeessa.
-   **Tehtävätallenteet voidaan tallentaa Word-asiakirjoina.** Tämä mahdollistaa tulostettavien koulutusohjeiden luomisen.

Voit luoda tehtävän omia nauhoituksia, toistaa Microsoftin tehtävän tallenteita tai muokata Microsoftin toimittamia tehtävän tallenteiden määritysten mukaisiksi. Saat lisätietoja tehtävän tallennus [tehtävän tallennus-Dynamics 365 työvaiheiden](task-recorder.md).

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
-   Voit luoda huomautuksia missä tahansa tehtävätallenteen vaiheessa. Tehtävän ohjauksen toiston aikana huomautukset näkyvät kuplassa huomautuksina vaiheen tekstin ylä- tai alapuolella. Tarkasteltaessa on Ohje-ruudun teksti huomautukset näkyvät vaiheessa kirjoitetun tekstin. Huomautukset kannattaa kuvauksen tavoin kirjoittaa ja tallentaa erilliseen asiakirjaan. Kun olet tallentamassa tehtävätallennetta, voit leikata ja liittää huomautukset asiakirjan vaatimassa muodossa.

**Tietoja huomautustyypeistä** Kaikki huomautukset ovat valinnaisia. Lisää huomautuksia vain silloin, kun ne sisältävät käyttäjälle hyödyllisiä tietoja.

-   **Otsikko**: otsikko Huomautus näkyy ennen vaiheen teksti, joka automaattisesti tehtävän tallennus Luo. Tehtävä opas otsikon huomautuksen tulee automaattisesti tekstin yläpuolelle. Tämän tyyppisen huomautuksen avulla voit selittää, miksi käyttäjä suorittaa vaihetta. Voit myös antaa lisätietoja kontekstista.

Tämä on muokkausruutu, joka näkyy, kun lisäät huomautuksen tallenteen luomisen yhteydessä. Syötä otsikkohuomautus **Otsikko**-ruutuun. 

[![screen1](./media/screen1.png)](./media/screen1.png) 

Otsikkohuomautus näyttää tältä tehtäväoppaan kuplassa. 

[![screen2](./media/screen2.png)](./media/screen2.png)

-   **Ilmoitukset:** Ilmoitusten huomautus tulee näkyviin tehtävän tallennustoiminnon automaattisesti luoman vaihetekstin jälkeen. Se näkyy tehtävän ohjauksessa vain, jos käyttäjä valitsee tehtävän ohjauksen kuplassa **Näytä lisää** -linkin. Voit käyttää tämän tyyppistä huomautusta kuvatessasi mitä tahansa tahansa käyttäjän vaiheen suorittamisessa tarvitsemia tietoja.

Tämä on muokkausruutu, joka näkyy, kun lisäät huomautuksen tallenteen luomisen yhteydessä. Syötä ilmoitusten huomautus **Ilmoitukset**-ruutuun. 

[![screen3](./media/screen3.png)](./media/screen3.png) 

Tämä on mitä huomautuksia Huomautus etsii opas tehtävän "kuplan".

[![screen4](./media/screen4.png)](./media/screen4.png)

-   **Info-vaihe**: nämä huomautukset luodaan napsauttamalla hiiren kakkospainikkeella ohjausobjektiin tai mihin tahansa lomakkeen &lt;**tehtävän tallennus**&lt; ** Lisää info vaihe. ** Info vaiheet näkyvät numeroitu vaiheessa vaiheessa riippumatta sen lisätä, vaikka mitään tallennettiin käyttöliittymässä. Voit lisätä lomaketason Tiedot-vaiheen tai ohjausobjektiin liitetyn Tiedot-vaiheen. Kun Tiedot-vaihe on liitetty lomakkeeseen, tehtävän ohjauksen kupla tulee näkyviin lomakkeeseen ilman osoitinta tehtävän ohjauksen toiston aikana. Info-vaiheeseen liittyy ohjausobjektiin, kun tehtävän "kuplan" opas osoittaa ohjausobjektin toistetut tehtävän opas. Ohje-ruudun vaihe info Huomautus näkyy numeroitu vaiheessa kirjoittamasi tekstin riippumatta. Info ohjeiden avulla voit valmistella käyttäjän kuvataan vaiheita, jotka voidaan tehdä työvaiheiden 365 Dynamics ulkopuolella tai muita tallenteita (vaikka ei voi luoda hyperinks huomautukset.) viittaavat seuraaviin vaiheisiin.

**Määritä, miten pitkä tallenteesta tulee**

-   Käyttäjä lukee tai toistaa tallenteen yleensä alusta loppuun, joten älä yhdistele vaiheita tai tehtäviä, jotka on paras tehdä erikseen.
-   Älä yritä tallentaa pitkää useita aliprosesseja sisältävää skenaariota. Esimerkiksi Myymälän asiakaspalvelupisteen toiminnot on liian laaja aihe. Jaa se lyhyempiin tehtäviin, kuten Palautusten vastaanotto ja Lisää lahjakorttiin.
-   Jos tehtävä voidaan suorittaa useiden eri liiketoimintaprosessien osana, luo sille erillinen tallenne, johon voit viitata muissa tallenteissa.
-   Jos prosessi käsittää useita tehtäviä, jotka henkilö luultavasti tekee kerralla, voit sisällyttää ne yhteen tallenteeseen. Tällainen tallenne voi olla esimerkiksi Toiminnallisuusprofiilien määrittäminen ja liittäminen.
-   Jos käyttäjä suorittaa jonkin tehtävän kerralla (kuten konfiguroiminen) ja heti tämän jälkeen toisen itsenäisen tehtävän, joka saatetaan toistaa, jaa tehtävät kahteen erilliseen tallenteeseen.

**Päättää, missä käyttöliittymän aloittamaan tallennus** sivu, joka olet kun käynnistät tehtävän tallennuksen tallennus vaikuttaa tehtävän opas näytetään sivu. Jos haluat, että tehtävän tallennus luetteloidaan Ohje-tehtäväruudussa, kun käyttäjä valitsee Ohje sivulla kirjanpidon parametrit, sinun on käynnistettävä nauhoituksen sivulla kirjanpidon parametrit. **Tallenna tallenteet .axtr-tiedostoina** Kun olet luonut tehtävätallenteen tai muokannut sitä, näkyviin tulee useita tallenteen lataus- tai tallennusvaihtoehtoja. Voit ladata tiedoston tehtävätallenteen pakettina (.axtr) tai käsittelemättömänä tallennetiedostona (.xml) tai Word-asiakirjana tai tallentaa tiedoston LCS-kirjastoon. Tehtävätallenne kannattaa aina tallentaa tehtävätallenteen pakettitiedostona (.axtr). Se helpottaa tiedoston ylläpitoa, jos menettelyitä tai huomautuksia on muutettava myöhemmin. Jos haluat noutaa tiedoston Word-asiakirjana, tallenna se myös silloin tehtävätallenteen pakettitiedostona.

## <a name="create-your-task-recording"></a>Tehtävätallenteen luominen
Lisätietoja yksityiskohtainen hallintapaketteihin, on [tehtävän tallennus luomisesta](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Microsoftin tehtävätallenteiden kopioiminen ja mukauttaminen
Voit ladata ja muokata Microsoftin tehtävän tallenteiden käyttämään omia ohjeisiin tai koulutusmateriaalia. Lataa Microsoftin tehtävätallenteet seuraavien vaiheiden avulla:

1.  Dynamics-365 operaatioille Avaa tehtävän tallennus. Tehtävän tallennustoiminto sijaitsee **asetusvalikossa**.
2.  Valitse tehtävän tallennustoiminnon ruudussa **Ylläpidä tallennetta.**
3.  Valitse **Missä tallenne on** -kohdassa **Se on LCS-kirjastossa**.
4.  Valitse **Valitse LCS-kirjasto**.
5.  Valitse Microsoft yleinen kirjasto.
6.  Valitse puussa se liiketoimintaprosessin solmu, johon tehtävätallenne on liitetty.
7.  Napsauta **OK**.
8.  Valitse **Käynnistä**.
9.  Tässä vaiheessa käydä läpi kaikki vaiheet muuttaminen saman tien uudelleen äänittää nauhoitus. **Huomautus**: Jos haluat vain muuttaa nauhoituksen, voit avata kirjaamiseksi **muokata tallennuksen ajastaminen huomautukset** -tilassa ja tallenna se.
10. Kun olet päässyt tallenteen toistossa loppuun, valitse näytön yläosassa olevan tehtävän tallennustoiminnon palkissa **Pysäytä**.
11. Määritä tehtävätallenteen tallennustapa.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Tallennukset on tehtävä sisällä Ohje-tehtäväruudussa
Näyttämään oman mukautetun tehtävän tallenteiden Ohje-tehtäväruudussa siten, että ne voidaan toistaa ohjauksina tehtävän tai tarkastella tekstinä tallennukset on tehtävä tallentaa BPM-kirjastoon ja päivittää oman ohjejärjestelmän parametrien osoittamaan BPM-kirjasto. Lisätietoja on ohjeaiheessa [muodostaa ohjeen.](../get-started/help-connect.md)

<a name="see-also"></a>Lisätietoja
--------

[Työvaiheiden 365 Dynamics-Ohje](..\get-started\help-overview.md)

[Yhdistää Ohje](..\get-started\help-connect.md)

[Tehtävän tallennus Dynamics 365 operaatioille](task-recorder.md)

[Viimeksi lisätyt tehtävän tallennus-ominaisuudet](\core\get-started\recently-added-editing-features-in-task-recorder)

[Uusi koulutus kirjastojen luomisesta Dynamics AX sisällä elinkaari-palveluja käyttämällä tehtävän tallennus (ulkoinen linkki)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)

[Luominen Rich ohjeaiheiden kanssa tehtävän tallennus (ulkoinen linkki)](https://mbspartner.microsoft.com/AX/Videos/970)


