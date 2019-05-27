---
title: Varastotyön mobiililaitteiden määrittäminen
description: Tässä aiheessa kuvataan, kuinka valikkokohteet määritetään mobiililaitteella työskenteleville varaston työntekijöille.
author: MarkusFogelberg
manager: AnnBe
ms.date: 04/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 29941
ms.assetid: 6dff6313-dc6e-4f06-9c0c-dab24eefe4da
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b6555086d6c86c17b501af9d4d8155e9c08a447
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536546"
---
# <a name="set-up-mobile-devices-for-warehouse-work"></a>Varastotyön mobiililaitteiden määrittäminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka valikkokohteet määritetään mobiililaitteella työskenteleville varaston työntekijöille.

**Huomautus:** Tämä ohjeaihe koskee varastonhallintamoduulin ominaisuuksia. Se ei koske inventaariohallintamoduulin ominaisuuksia. Valikkovaihtoehdot, jotka näkyvät valikoissa varaston mobiililaitteessa, määritetään **Mobiililaitteen valikkovaihtoehdot** -sivulla. Koska samat valikkovaihtoehdot voivat olla eri valikoissa, on helppo määrittää valikkorakenteet niin, että vain tietyntyyppiset työt näkyvät tietyille käyttäjille. Voit määrittää valikkovaihtoehdot suorittamaan seuraavat tehtävät:

-   Käsittele kysely tai suorita tehtävä, kuten tarran tulostus, rekisterikilven numeroiden luonti, tuotantotilauksen aloitus tai toimipaikan nimikkeiden tietojen pikahaku.
-   Luo työ, joka suoritetaan toisen prosessin kautta. Esimerkiksi nimikkeen vastaanotto ostotilaukselle saattaa luoda hyllytystyön toiselle työntekijälle.
-   Suorita toisen prosessin (nykyisen työn) edellyttämä työ, kuten hyllytystyö, joka luotiin, kun ostotilaukselle vastaanotettiin nimike.

Jos haluat luoda kyselyn tai toiminnon valikkovaihtoehdon, määritä asetuksen **Tila** arvoksi **Epäsuora**. Luettelo **Toimintokoodi**-asetuksista tulee saataville siten, että voit valita kyselyn tai toiminnon tyypin, jota varten valikkokohde on. Voit luoda valikkovaihtoehdon fyysisen varastoinnin työn luomiseen, määritä **Tila**-kentän arvoksi **Työ**. Näkyviin tulee luettelo **Työn luontiprosessi** -vaihtoehdoista. Jos haluat luoda valikkovaihtoehdon nykyisen varastotyön käsittelyyn, määritä **Tila** kentän arvoksi **Työ** ja määritä **Käytä nykyistä työtä** -asetukseksi **Kyllä**. **Huomautus:** Valikkokohdalle on käytettävissä lisäkenttiä sille valitsemastasi tilasta riippuen, ja jos valikkokohtaa käytetään suorittamaan olemassa oleva työ. Lisätietoja lisäkenttien valinnasta on osiossa “Lisävalikkovaihtoehdot” myöhemmin tässä aiheessa.

## <a name="configure-menu-items-for-activities-and-inquiries"></a>Toimintojen ja kyselyjen valikkovaihtoehtojen määrittäminen
Jos valikkovaihtoehdon **Tila** kentän arvoksi määritetään **Epäsuora**, voit luoda valikkovaihtoehdon suorittamaan yleisen tehtävän tai kyselyn, joka ei luo työtä. Tällaisia tehtäviä ovat esimerkiksi rekisterikilpien uudelleentulostus tai toimipaikan nimikkeiden sijaintia koskeva kysely. Seuraavassa taulukossa näkyvät valittavina olevat vaihtoehdot.

| Vaihtoehto                      | Kuvaus                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ei mitään                        | Tämä oletusarvo ei ota käyttöön toimintoa tai kyselyä.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Tietoja                       | Näytä tietoja järjestelmästä, kuten versionumero, varaston tunniste ja parhaillaan kirjautuneena oleva työntekijä.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Vaihda varastoa            | Muuta varasto, johon työntekijä on kirjautunut.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Sijaintikysely            | Näytä kaikkia sijainnin nimikkeitä ja määriä koskevat tiedot.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Rekisterikilpikysely       | Näytä rekisterikilven nimikkeiden määrä ja rekisterikilven sijainti.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Käynnistä tuotantotilaus      | Käynnistä tuotantotilaus.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Tuotannon hävikki            | Syötä tuotannon aikana jokaiselle tuoterakenteen riville syntyneen hävikin määrä.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Tuotannon viimeinen kuormalava      | Määritä, että viimeinen nimikkeiden kuormalava on tuotettu tuotantotilaukselle ja että tuotantotilauksen tilaksi on päivitettävä **Ilmoitettu valmiiksi**. Niiden raaka-ainemateriaalien tila, joita ei kulutettu tuotannon aikana, palautetaan arvosta **Keräilty** arvoon **Tilauksessa**, ja nimikkeet voidaan palauttaa varastoon.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Nimikekysely                | Skannaa nimike määrittääksesi, missä se on varastossa. Kysely palauttaa kaikki skannatunnimikkeen sijainnit ja määrät.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Tulosta etiketti uudelleen               | Tulosta rekisterikilven etiketti uudelleen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Rekisterikilpikoonti         | Luo ylätason rekisterikilpi yhdistämällä useita saman toimipaikan rekisterikilpiä. Tästä vaihtoehdosta on hyötyä, jos siirrät useita rekisterikilpiä samanaikaisesti. Kun päärekisterikilpi on siirretty, sinun on suoritettava rekisterikilven tauko, ennen kuin voit poimia nimikkeitä kustakin rekisterikilvestä. **Vihje:** Jos haluat siirtää päärekisterikilven, sinun on käytettävä mobiililaitetta, joka on määritetty luomaan töitä siirroille.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Rekisterikilven tauko         | Jaa rekisterikilpikoonti siten, että voit kerätä rekisterikilvistä nimikkeet. jotka kuuluivat koontiin.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Kuljettajan sisäänkuittaus             | Jos käytät Kuljetustenhallintaa, rekisteröi kuljettajan saapuminen skannaamalla lähtevän kuorman tunnus, tapaamisen tunnus tai lähetyksen tunnus. Tämä vaihtoehto edellyttää, että tapaamiselle määritetään kuorma, ja kuorman tilan on oltava **Ladattu**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Kuljettajan uloskuittaus            | Rekisteröi, että kuljettaja on suorittanut tapaamisensa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Tyhjennä numerosarjojen välimuisti | Poista numerosarjan numerot numerosarjan välimuistista. Järjestelmänvalvoja suorittaa tavallisesti tämän toiminnon välimuistiin liittyvien ongelmien ratkaisemiseksi, kun käyttö tapahtuu mobiililaitteelta.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Muuta eräkäsittelyä    | Anna työntekijän määrittää erän käsittelykoodi nimikkeelle ja erälle. Tämä vaihtoehto päivittää eräkohtaisen käsittelykoodin.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Näytä avoin työluettelo      | Näyttää käyttäjäkohtaisen saatavilla olevien töiden luettelon. Käyttäjä voi valita suoritettavan työn, joka kohdistetaan hänelle. Luettelo on tarkoitettu katseltavaksi tablettilaitteissa, joiden näytön koko on 7 tuumaa tai enemmän. Kun valitset tämän vaihtoehdon, **Muokkaa kyselyä**- ja **Kenttäluettelo**-valikkovaihtoehdot ovat käytettävissä. **Muokkaa kyselyä** -sivulla voit määrittää ehtoja luettelossa näkyville töille. **Kenttäluettelo**-sivulla voit valita työluettelossa näkyvät kentät. Voit esimerkiksi rajoittaa näkyvissä olevien kenttien määrää, jotta käyttäjän on helpompi valita oikea työnimike. Voit myös valita **Yleiset**-välilehdessä **Tietueita sivulla** -kentässä, miten monta työtietuetta kullakin sivulla näytetään. Jos **Salli käyttäjien suodattaa työtä tapahtumatyypeittäin** -vaihtoehto on valittuna, työluettelossa on **Työn suodatus** -ohjausobjekti, jolla käyttäjä voi suodattaa luettelon tapahtumatyypin mukaan. Käyttäjä näkee työluettelossa vain työt, joiden käyttöoikeus hänellä on. Varmista, että käyttäjillä on oikeudet yhteen tai useampaan käyttäjäohjattuun valikkovaihtoehtoon, jotka tukevat tiettyä työluokkatyyppiä, jota heidän tulisi pystyä käyttämään. Käyttöoikeudet tarkistetaan myös, kun käyttäjä yrittää suorittaa työn luettelosta. |

## <a name="configure-menu-items-to-create-work-for-another-worker-or-process"></a>Valikkovaihtoehtojen määrittäminen työn luomiseksi toiselle työntekijälle tai prosessille
Voit määrittää valikkovaihtoehdon, joka luo työn toiselle työntekijälle, kun alustava toiminto on suoritettu mobiililaitteella. Jos esimerkiksi yksi työntekijä käyttää mobiililaitetta nimikkeen vastaanottamiseen, hyllytystyö luodaan toiselle työntekijälle. Määritä työn luova valikkovaihtoehto valitsemalla **Mobiililaitteen valikkovaihtoehdot** -sivulla **Tila**-kentässä **Työ**. Seuraavassa taulukossa **Työn luontiprosessi** -kentän vaihtoehdot on järjestetty tilaustyypin mukaan.

<table>
<tbody>
<tr>
<th>Työtilaustyyppi</th>
<th>Vaihtoehto</th>
<th>Kuvaus</th>
</tr>
<tr>
<td rowspan="8">Ostotilaus</td>
<td>Ostotilausrivin vastaanotto</td>
<td>Rekisteröi nimikkeen määrän vastaanotto käyttämällä ostotilausnumeroa ja ostotilauksen rivinumeroa ja luo hyllytystyö toiselle työntekijälle.</td>
</tr>
<tr>
<td>Ostotilausrivin vastaanotto ja poispano</td>
<td>Rekisteröi nimikkeen määrän vastaanotto käyttämällä ostotilausnumeroa ja ostotilauksen rivinumeroa ja pane nimikkeet pois. Sama työntekijä suorittaa molemmat toiminnot.</td>
</tr>
<tr>
<td>Ostotilausnimikkeen vastaanotto</td>
<td>Rekisteröi nimikkeen määrän vastaanotto ostotilaukselle rekisteröimällä ostotilauksen numero ja nimikkeen numero, ja luo hyllytystyö toiselle työntekijälle.</td>
</tr>
<tr>
<td>Ostotilausnimikkeen vastaanotto ja poispano</td>
<td>Rekisteröi nimikkeen määrän vastaanotto ostotilausta varten rekisteröimällä ostotilausnumero ja nimikenumero ja pane nimike pois. Sama työntekijä suorittaa molemmat toiminnot.</td>
</tr>
<tr>
<td>Rekisterikilven vastaanotto</td>
<td>Vastaanota saapuva kuormitus rekisterikilven tunnuksen avulla.</td>
</tr>
<tr>
<td>Rekisterikilven vastaanotto ja poispano</td>
<td>Vastaanota saapuva kuorma ja hyllytä se rekisterikilven tunnuksen avulla.</td>
</tr>
<tr>
<td>Kuorman nimikkeen vastaanotto</td>
<td>Rekisteröi kuorman nimikkeen määrä käyttämällä kuorman tunnusta ja luo hyllytystyö toiselle työntekijälle. Nimiketunnus ja tuotedimensiot täsmäyttävät vastaanoton ostotilausriveille.</td>
</tr>
<tr>
<td>Kuorman nimikkeen vastaanotto ja poispano</td>
<td>Rekisteröi kuormituksen vastaanotto käyttämällä kuormituksen tunnusta ja sijoita nimikkeet pois. Nimiketunnus ja tuotedimensiot täsmäyttävät vastaanoton ostotilausriveille. Sama työntekijä suorittaa molemmat toiminnot.</td>
</tr>
<tr>
<td>Palautustilaus</td>
<td>Palautustilauksen vastaanotto</td>
<td>Rekisteröi nimikkeen määrä rekisteröimällä RMA-numero ja luo hyllytystyö toiselle työntekijälle.</td>
</tr>
<tr>
<td>Palautustilauksen vastaanotto ja poispano</td>
<td>Rekisteröi nimikkeen määrä rekisteröimällä palautusnumero ja aseta nimikkeet pois. Sama työntekijä suorittaa molemmat toiminnot.</td>
</tr>
<tr>
<td>Siirtotilaus</td>
<td>Siirtotilausnimikkeen vastaanotto</td>
<td>Rekisteröi nimikkeen määrän vastaanotto ja luo hyllytystyö toiselle työntekijälle.

<strong>Huomautus:</strong> Käytä tätä vaihtoehtoa vain, jos nimikkeet on lähetetty varastosta, jolle ei ole aktivoitu varastonhallintaprosesseja.</td>
</tr>
<tr>
<td>Siirtotilausnimikkeen vastaanotto ja poispano</td>
<td>Rekisteröi nimikkeen määrän vastaanotto ja pane nimikkeet pois. Sama työntekijä suorittaa molemmat toiminnot.

<strong>Huomautus:</strong> Käytä tätä vaihtoehtoa vain, jos nimikkeet on lähetetty varastosta, jolle ei ole aktivoitu varastonhallintaprosesseja.</td>
</tr>
<tr>
<td>Siirtotilausrivin vastaanotto</td>
<td>Rekisteröi nimikkeen määrän vastaanotto ja luo hyllytystyö toiselle työntekijälle.</td>
</tr>
<tr>
<td>Siirtotilausrivin vastaanotto ja poispano</td>
<td>Rekisteröi nimikkeen määrän vastaanotto ja pane nimikkeet pois. Sama työntekijä suorittaa molemmat toiminnot.</td>
</tr>
<tr>
<td>Tuotanto</td>
<td>Ilmoita valmiiksi</td>
<td>Rekisteröi valmiin nimikkeen määrä, jonka tuotanto on valmistunut, ja luo hyllytystyö toiselle käyttäjälle. Määrä voi olla vähintään tuotantoon suunnitellun määrän osa tai koko määrä.</td>
</tr>
<tr>
<td>Ilmoita valmiiksi ja pane pois</td>
<td>Rekisteröi tuotantoon valmiin nimikkeen määrä ja siirrä nimikkeet pois. Määrä voi olla vähintään tuotantoon suunnitellun määrän osa tai koko määrä. Sama työntekijä suorittaa molemmat toiminnot.</td>
</tr>
<tr>
<td>Kanban</td>
<td>Määritä, että kanban on valmis, ja luo hyllytystyö toiselle työntekijälle.</td>
</tr>
<tr>
<td>Kanban-poispano</td>
<td>Määritä, että kanban on suoritettu, ja hyllytä nimikkeet. Sama työntekijä suorittaa molemmat toiminnot.</td>
</tr>
<tr>
<td>Varasto</td>
<td>Varastotapahtuma</td>
<td>Rekisteröi nimikkeet, jotka on siirretty paikasta toiseen. Työntekijä määrittää sijainnin, josta nimikkeet siirretään ja minne ne siirretään.</td>
</tr>
<tr>
<td>Karanteeni</td>
<td>Muuta käytettävissä olevien rekisterikilpien varaston tila tai sijainti tehdäksesi vioittuneet puuttuvat varastonimikkeet ei käytettävissä oleviksi.</td>
</tr>
<tr>
<td>Siirto mallin mukaan</td>
<td>Siirrä nimikkeet yhdestä toimipaikasta toiseen puoliautomaattisella tavalla. Työntekijä valitsee sijainnin, josta nimikkeet siirretään, ja Finance and Operations määrittää sijaintidirektiivin avulla, minne ne siirretään.</td>
</tr>
<tr>
<td>Varastosiirto</td>
<td>Rekisteröi nimikkeet, jotka on siirretty varastosta toiseen. Tämä vaihtoehto edellyttää, että työntekijällä on oikeus työskennellä molemmissa varastoissa.

<strong>Huomautus:</strong> Tämä valikkovaihtoehto vaatii oletusarvoisen varaston siirtokirjauskansion, jossa <strong>Tositteen asetus</strong> -kentän arvona on <strong>Kirjaus</strong>.</td>
</tr>
<tr>
<td>Rekisterikilven lataus</td>
<td>Käytä tätä vaihtoehtoa, kun olet määrittämässä varastoa ensimmäistä kertaa. Tarkista kaikki rekisterikilvet kaikissa varaston sijainneissa. Sijaintien tulee olla rekisterikilpiohjattuja. Tätä vaihtoehtoa ei voi käyttää, jos <strong>Sarjanumero</strong> tai <strong>Eränumero</strong> sijaitsevat varaston varaushierarkiassa <strong>Sijainti</strong>-kohdan yläpuolella.</td>
</tr>
<tr>
<td>Inventointi</td>
<td>Oikaisu sisään</td>
<td>Kasvata nimikkeiden määrää varastossa. Määritä sijainti, rekisterikilpi, nimike, määrä, mittayksikkö ja tila.</td>
</tr>
<tr>
<td>Oikaisu ulos</td>
<td>Vähennä nimikkeiden määrää varastossa. Määritä varaston sijainti, rekisterikilpi, nimike, määrä, mittayksikkö ja tila.</td>
</tr>
<tr>
<td>Pistoinventointi</td>
<td>Käynnistä sijainnin laskenta. Työntekijän tulee laskea kaikki sijainnin nimikkeet. Jos inventoinnin tulos on pienempi kuin odotettu määrä, puuttuva määrä pidetään tappiona.</td>
</tr>
</tbody>
</table>

## <a name="configure-menu-items-to-process-existing-work"></a>Valikkovaihtoehdon määrittäminen käsittelemään olemassa olevat työt
Varastotöitä luovien valikkovaihtoehtojen lisäksi voit määrittää valikkovaihtoehdot käsittelemään työt, jotka on luotu aiemmin. Määritä **Tila**-kentän arvoksi **Työ** ja valitse **Käytä nykyistä työtä** -vaihtoehto. **Yleiset**-välilehteen tulee saataville joitakin lisävaihtoehtoja. Voit valvoa valikkovaihtoehdon käyttöä määrittämällä yhden tai useamman työluokan **Työluokka**-pikavälilehdessä. Työluokat määrittävät työn, jota valikkovaihtoehdolla voi käsitellä. Työluokan kautta voidaan myös myöntää käyttöoikeus tiettyihin käyttäjärooleihin tai erityyppisten työvaiheiden erilliskäsittelyyn. Seuraavassa taulukossa näkyvät valittavina olevat vaihtoehdot. Vaihtoehto voidaan valita **Ohjaaja**-kentässä **Mobiililaitteen valikkovaihtoehdot** -sivulla. 

<table>




<thead>
<tr class="header">
<th>Vaihtoehto</th>
<th>kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ei mitään</td>
<td>Tämä oletusarvo ei käsittele työtä.</td>
</tr>
<tr class="even">
<td>Järjestelmäohjattu</td>
<td>Microsoft Dynamics 365 for Finance and Operations ohjaa työn tyyppiä, joka on määritetty työntekijälle ja järjestystä, jossa työntekijä suorittaa työn. Kun valitset tämän vaihtoehdon, voit valita toimintoruudussa <strong>Järjestelmäohjattu työ</strong> avataksesi <strong>Järjestelmäohjattu lajittelujärjestys</strong> -sivun, jossa voit määrittää työn lajittelukriteerit. Lajitteluehto hallitsee järjestystä, jossa työntekijä suorittaa työn. Voit luoda tarvitsemasi määrän kriteereitä.</td>
</tr>
<tr class="odd">
<td>Käyttäjäohjattu</td>
<td>Työntekijä valitsee suoritettavan työn ja sen suoritusjärjestyksen.</td>
</tr>
<tr class="even">
<td>Käyttäjien ryhmittely</td>
<td>Työntekijä ryhmittelee työn manuaalisesti. Tämä vaihtoehto on hyödyllinen esimerkiksi silloin, kun työntekijä voi kerätä sijainnissa useita nimikkeitä samaan aikaan. Kun työntekijä on saanut valmiiksi tarvittavien nimikkeiden keräilyn, hän voi hyllyttää nimikkeet.</td>
</tr>
<tr class="odd">
<td>Järjestelmän ryhmittely</td>
<td>Microsoft Dynamics 365 for Finance and Operations ryhmittelee työntekijän työn määritetyn kentän perusteella. Esimerkiksi keräilytyö ryhmitellään, kun työntekijä skannaa lähetyksen tunnuksen, kuorman tunnuksen tai minkä tahansa arvon, joka voi linkittää jokaisen työyksikön. Jos valitset tämän vaihtoehdon, seuraavat vaihtoehdot ovat käytettävissä:
<ul>
<li><strong>Järjestelmän ryhmittelykenttä</strong> – Valitse kenttä, jonka työntekijä skannaa työn ryhmittelemiseksi.</li>
<li><strong>Järjestelmän ryhmittelyotsikko</strong> – Anna teksti, joka opastaa työntekijää, mitä hänen pitää skannata työn ryhmittelemiseksi.</li>
</ul></td>
</tr>
<tr class="even">
<td>Tarkistettu ja käyttäjäohjattu</td>
<td>Työntekijä valitsee suoritettavan työn, kun työ liittyy suurempaan yksikköön, kuten kuormaan tai lähetykseen. Työntekijä määrittää nimikkeiden keräilyjärjestyksen. Jos valitset tämän vaihtoehdon, seuraavat vaihtoehdot ovat käytettävissä:
<ul>
<li><strong>Tarkistettu ja käyttäjäohjattu kenttä</strong> – Valitse kenttä, jonka työntekijä skannaa työn ryhmittelemiseksi.</li>
<li><strong>Tarkistettu ja käyttäjäohjattu etiketti</strong> – Kirjoita teksti, joka ilmoittaa työntekijälle tiedot siitä, mitä tulisi skannata, kun järjestelmä ryhmittelee keräilytyön.</li>
</ul>
Tämä on hyödyllinen vaihtoehto esimerkiksi silloin, kun useita kuormalavoja asetetaan väliaikaiseen sijaintiin kuormausta varten. Jos valitset <strong>Tarkistettu ja käyttäjäohjattu kenttä</strong> -kohdasta <strong>LoadId</strong>-vaihtoehdon, työntekijä voi valita minkä tahansa kuormalavan, joka liittyy kuormaan. Näkyviin tulee virhesanoma, jos työntekijä skannaa nimikkeen, joka ei liity kuormaan.</td>
</tr>
<tr class="odd">
<td>Klusterin keräily</td>
<td>Työntekijä ryhmittelee työn klustereihin. Klusterien avulla työntekijät voivat valita nimikkeitä samasta sijainnista useille työtilauksille samanaikaisesti.</td>
</tr>
<tr class="even">
<td>Inventoinnin ryhmittely</td>
<td>Työntekijä valitsee vyöhykkeen, työpoolin tai sijainnin ja Microsoft Dynamics 365 for Finance and Operations määrittää työn valinnan perusteella. Jos valitset tämän vaihtoehdon, voit valita toimintoruudusta myös <strong>Inventointi</strong>-vaihtoehdon määrittääksesi lisätiedot ja sen, kuinka monta kertaa työntekijän on toistettava laskenta, jos ero löydetään.</td>
</tr>
 <tr class="odd">
<td>Kuljetuksen kuormaus</td>
<td>Tämän toiminnon avulla useat varastotyöntekijät voivat ladata varaston samasta tai eri kuormasta samaan trukkiin. Koskee täysin tai osittain lähetettyjä kuormia.</td>
</tr>
</tbody>
</table>

## <a name="additional-menu-item-options"></a>Valikon lisävaihtoehdot
Lisätietoja valikkovaihtoehtojen asetuksia on **Mobiililaitteen valikkovaihtoehdot** -sivulla. Vaihtoehdot vaihtelevat sen prosessin mukaan, jolle määrität valikkovaihtoehtoa. 

Seuraavassa taulussa kuvataan nämä asetukset.

<table>




<thead>
<tr class="header">
<th>Kenttä</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Salli työn jakaminen</td>
<td>Valitse tämä vaihtoehto, jos haluat antaa käyttäjien siirtää työtilauksen nimikkeitä useampaan kuin yhteen rekisterikilpeen. Tämä vaihtoehto on hyödyllinen esimerkiksi silloin, kun kohderekisterikilpi on täynnä ja työntekijän on lisättävä jäljellä olevat nimikkeet toiseen rekisterikilpeen. Työntekijä voi napsauttaa <strong>Koko</strong> määrittääkseen että rekisterikilpi on täynnä, ja että keräilytöiden vastaanotto lopetetaan. Tämän jälkeen näytetään keräiltyjen nimikkeiden laittosijainti ja valmiiksi suoritettu keräilytyö siirretään uuteen työtilaukseen. Jäljellä oleva keräilytyö kohteena olevalle rekisterikilvelle pysyy alkuperäisessä työtilauksessa.</td>
</tr>
<tr class="even">
<td>Ankkurointi</td>
<td>Valitse tämä vaihtoehto, jotta työntekijät voivat määrittää ehdotetun vaihe- tai lataamissijainnin korvaavan sijainnin. Kaikki jäljellä oleva hyllytystyö ohjataan uuteen sijaintiin. Tämä vaihtoehto on hyödyllinen esimerkiksi silloin, kun työntekijän on pantava nimikkeitä tilaukselle 1 laiturin 1 väliaikaisessa sijainnissa, mutta tämä ei ole mahdollista, koska edellinen kuorma ei ole poistunut sijainnista. Sen sijaan, että odottaisi väliaikaisen Dock 1 -sijainnin vapautumista, työntekijä voi päättää käyttää väliaikaista Dock 2 -sijaintia. Tässä tapauksessa työntekijä korvaa ehdotetun väliaikaisen sijainnin. Työtilauksen jäljellä olevien nimikkeiden laittosijainniksi päivittyy laiturin 2 väliaikainen sijainti. Jos valitset tämän vaihtoehdon, määritä <strong>Ankkuroi</strong>-kenttä.</td>
</tr>
<tr class="odd">
<td>Ankkuroi</td>
<td>Jos käytät ankkurointia, määritä, tehdäänkö ankkurointi lähetyksen vai kuorman mukaan.</td>
</tr>
<tr class="even">
<td>Tarkistusmallin tunnus</td>
<td>Valitse työjäljitysmalli, joka keskeyttää työprosessin valikkokohdan siten, että toinen toiminto voidaan suorittaa. Jos esimerkiksi valikkovaihtoehto on saapuvalle työlle, tarkistusmalli saattaa vaatia, että työntekijä tarkistaa toimituskontin lämpötilan. Prosessin keskeytymiskohta määritetään tarkistusmallissa. Se voi olla esimerkiksi ajankohta, jona työ aloitetaan tai valmistuu tai kun sen tila muuttuu.</td>
</tr>
<tr class="odd">
<td>Klusteriprofiilin tunnus</td>
<td>Valitse klusteriprofiili käytettäväksi klusterin keräysluettelossa. Klusterin profiili sisältää asetuksia, kuten luodaanko klusterit automaattisesti; toimien nimet ja työyksiköiden määrät, joihin ne voidaan määrittää; milloin klusterit jaetaan yksittäisiksi yksiköiksi ja milloin vaaditaan tarkistusta. Tämä kenttä on käytettävissä vain, jos <strong>Ohjaaja</strong>-kentässä on valittu <strong>Klusterin keräily</strong>.</td>
</tr>
<tr class="even">
<td>Laske ensin nimikkeen kokonaismäärä</td>
<td>Valitse tämä vaihtoehto, jos haluat työntekijöiden laskevan kokonaismäärän ensimmäiseksi inventoinnin aikana. Jos eroja on, työntekijän on annettava lisätietoja, kuten rekisterinumero, eränumero ja sarjanumerot.</td>
</tr>
<tr class="odd">
<td>Luo siirto</td>
<td>Valitse tämä valintaruutu, jos haluat antaa työntekijän luoda työn siirtoa varten niin, ettei työntekijän tarvitse suorittaa työtä heti. Tämä vaihtoehto on hyödyllinen esimerkiksi silloin, kun laatutarkastus on suoritettu ja tarkistaja haluaa, että nimike siirretään pois laatutarkastusalueelta.</td>
</tr>
<tr class="even">
<td>Direktiivikoodi</td>
<td>Kun haluat käyttää tiettyä sijaintidirektiiviä, valitse sijaintidirektiiville liitetty direktiivikoodi. Tämä kenttä on käytettävissä, kun luot työn ja työn luontiprosessi on <strong>Siirto mallin mukaan</strong>.</td>
</tr>
<tr class="odd">
<td>Poista inventointirajat käytöstä</td>
<td>Valitse tämä vaihtoehto, jos haluat ohittaa inventoinnin raja-arvot. Jos valitset tämän vaihtoehdon, inventointityötä ei luoda raja-arvojen ylittyessä.</td>
</tr>
<tr class="even">
<td>Näytä erän käsittelykoodi</td>
<td>Valitse tämä vaihtoehto, jos haluat näyttää eräkäsittelykoodit. Voit esimerkiksi näyttää erän käsittelykoodit, kun vastaanotat palautetun erän. Työntekijät voivat tällöin arvioida erän tilan tai laadun ja valita sopivan koodin. Erän käsittelykoodin säännöt määrittävät, onko erä muiden varastoprosessien käytettävissä. Jos et valitse tätä vaihtoehtoa, käytetään jotakin seuraavista eräkäsittelykoodeista:
<ul>
<li>Jos saat uuden eränumeron, nimikkeen malliryhmässä määritetty oletusarvoinen eräkäsittelykoodi</li>
<li>Eräkäsittelykoodi, joka on jo määritetty erään</li>
</ul></td>
</tr>
<tr class="odd">
<td>Näytä käsittelykoodi</td>
<td>Valitse tämä vaihtoehto, jos haluat näyttää eräkäsittelykoodit. Voit esimerkiksi näyttää käsittelykoodit, kun vastaanotat palautetut nimikkeet. Työntekijät voivat tällöin arvioida nimikkeiden tilan tai laadun ja valita sopivan koodin. Käsittelykoodin säännöt määrittävät, ovatko nimikkeet muiden varastoprosessien käytettävissä.</td>
</tr>
<tr class="even">
<td>Näytä varaston tila</td>
<td>Valitse tämä vaihtoehto, jos haluat näyttää varastossa olevien nimikkeiden tilan. Tämä vaihtoehto on käytettävissä kaikille valikkovaihtoehdoille, jotka käyttävät olemassa olevaa työtä, inventointia lukuun ottamatta.</td>
</tr>
<tr class="odd">
<td>Näytä keräilynäytön yhteenveto</td>
<td>Valitse tämä vaihtoehto, jos haluat näyttää yhteenvedon valitun työtilauksen keräilytyöstä. Yhteenveto on näkyvillä, kunnes ensimmäinen työtilauksen työrivi käsitellään.</td>
</tr>
<tr class="even">
<td>Muodosta rekisterikilpi</td>
<td>Valitsema tämä vaihtoehto, jos haluat luoda yksilöllisiä rekisterinumeroja numerosarjavalinnan perusteella. Voit esimerkiksi luoda rekisterinumeron ostotilauksille vastaanotetuille nimikkeille.</td>
</tr>
<tr class="odd">
<td>Ryhmä pantu pois</td>
<td>Valitse tämä vaihtoehto, jos haluat ryhmitellä hyllytystyöt. Tämä vaihtoehto on käytettävissä, kun joko työntekijä tai Microsoft Dynamics 365 for Finance and Operations ryhmitteli työn. Kun työntekijä on saanut ryhmän kaikki keräilytyöt valmiiksi, samaan ryhmään luodaan hyllytystyö.</td>
</tr>
<tr class="even">
<td>Varasto-oikaisutyypit</td>
<td>Valitse varaston oikaisutyyppi, joka määrittää varastoinventoinnin kirjauskansion, jota käytetään oikaisun kirjaamiseen, ja poistetaanko varauksia. Tämä kenttä on käytettävissä vain <strong>Oikaisu sisään</strong>- tai <strong>Oikaisu ulos</strong> -työnluontiprosessissa.</td>
</tr>
<tr class="odd">
<td>Ohita eränumero</td>
<td>Valitse tämä vaihtoehto, jos annat työntekijöiden, jotka raportoitavat tuotantotilauksen määrän valmistuneeksi, tallentaa eränumeron, joka eroaa tuotantotilaukseen liitetystä eränumerosta.</td>
</tr>
<tr class="even">
<td>Ohita kohderekisterikilpi</td>
<td>Valitse tämä vaihtoehto, jos annat työntekijöiden määrittää kohteen rekisterinumeron, joka eroaa ehdotetusta kohderekisterikilvestä. Käytä tätä vaihtoehtoa, kun työtilauksen ensimmäisen kerran keräily kohdistuu koko nimikkeen tai rekisterikilven määrään. Tämä vaihtoehto on hyödyllinen esimerkiksi silloin, kun kuormalavaa käytetään uudelleen.</td>
</tr>
<tr class="odd">
<td>Kerää ja pakkaa</td>
<td>Valitse tämä vaihtoehto, jos annat työntekijöiden yhdistää myyntitilauksen tai kuormauksen työt yhteen työyksikköön. Työntekijä voi suorittaa työn vain myyntitilaukselle tai kuormalle. Tämä vaihtoehto on hyödyllinen esimerkiksi silloin, kun myyntitilauksen määrää täytyy kasvattaa sen jälkeen, kun myyntitilaukselle on luotu kuorma, lähetys ja työ. Tämä vaihtoehto on käytettävissä vain, kun valikkokohde käyttää olemassa olevaa työtä ja käyttäjä tai järjestelmä ohjaa työtä.</td>
</tr>
<tr class="even">
<td>Valitse vanhin erä</td>
<td>Määritä, onko työntekijän kerättävä sijainnin vanhin erä ensin. Valittavissa ovat seuraavat vaihtoehdot:
<ul>
<li><strong>Ei mitään</strong> – Työntekijä voi valita minkä tahansa erän sijainnista. Työntekijä saa sanomaa.</li>
<li><strong>Varoitus</strong> – Työntekijä voi valita minkä tahansa erän sijainnissa, mutta näkyviin tulee varoitussanoma, jos erä ei ole vanhin.</li>
<li><strong>Pakota</strong> – Työntekijän on kerättävä sijainnin vanhin erä. Työntekijä saa virhesanoman, jos erä ei ole vanhin. <strong>Huomautus:</strong> Tällä vaihtoehdolla on merkitystä vain, jos <strong>Eränumero</strong> on <strong>Sijainti</strong>-arvoa alempana nimikkeelle määritetyssä varaushierarkiassa.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tulosta etiketti</td>
<td>Valitse tämä vaihtoehto, jos annat työntekijöiden tulostaa rekisterikilpitarroja.</td>
</tr>
<tr class="even">
<td>Järjestelmän ryhmittelykenttä</td>
<td>Valitse kenttä, joka määrittää, miten Microsoft Dynamics 365 for Finance and Operations ryhmittelee keräilytyön työntekijöille. Esimerkiksi jos valitset <strong>ShipmentId</strong>-kentän, työntekijä skannaa lähetystunnuksen keräilytyön ryhmittelemiseksi. Tämän jälkeen kaikki lähetyksen työt on määritetty työntekijälle. Tämä kenttä edellyttää, että luot valikkovaihtoehdon, jolla voi käyttää aiemmin luotua järjestelmän ryhmittelemää työtä. Kirjoita teksti myös <strong>Järjestelmän ryhmittelyotsikko</strong> -kenttään, jotta työntekijä tietää, mitä pitää skannata.</td>
</tr>
<tr class="odd">
<td>Järjestelmän ryhmittelyotsikko</td>
<td>Kirjoita teksti, jossa työntekijälle kerrotaan skannattavat tiedot, kun Microsoft Dynamics 365 for Finance and Operations ryhmittelee keräilytyön. Jos esimerkiksi käytät <strong>ShipmentId</strong>-kenttää keräilytöiden ryhmittelemiseen lähetyksen mukaan, voit kirjoittaa kenttään <strong>Lähetyksen tunnus</strong>. Tämä kenttä edellyttää, että luot valikkovaihtoehdon, jolla voi käyttää aiemmin luotua järjestelmän ryhmittelemää työtä. Sinun on myös valittava ryhmittelykenttä <strong>Järjestelmän ryhmittelykenttä</strong> -kentästä.</td>
</tr>
<tr class="even">
<td>Käytä oletustietoja</td>
<td>Valitse tämä vaihtoehto, jos haluat ottaa toimintoruudussa käyttöön <strong>Oletustiedot</strong>-painikkeen, jossa voit valita näytettäviksi työntekijän yleensä päivittäisessä työssään tarvitsemansa tiedot. Tämä vaihtoehto on hyödyllinen esimerkiksi silloin, kun työntekijä kerää nimikkeen usein samasta sijainnista. Voit valita <strong>Lähtösijainti</strong>-kentän näyttämään sijainnin oletusarvoisesti.</td>
</tr>
<tr class="odd">
<td>Tarkistettu ja käyttäjäohjattu kenttä</td>
<td>Valitse kenttä, jonka työntekijä skannaa työn ryhmittelemiseksi. Esimerkiksi jos valitset <strong>LoadId</strong>, työntekijä voit valita minkä tahansa työn, joka liittyy valittuun kuormaan. Kirjoita teksti myös <strong>Tarkistettu ja käyttäjäohjattu etiketti</strong> -kenttään, jotta työntekijä tietää, mitä pitää skannata.</td>
</tr>
<tr class="even">
<td>Tarkistettu ja käyttäjäohjattu etiketti</td>
<td>Kirjoita teksti, joka ilmoittaa työntekijälle tiedot siitä, mitä tulisi skannata, kun työn ryhmittelee Tarkistettu ja käyttäjäohjattu -kenttä. Esimerkiksi jos käytät <strong>LoadId</strong>-kenttää kuorman keräilytöiden ryhmittelemiseen, voit kirjoittaa kenttään <strong>Kuorman tunnus</strong>.</td>
</tr>
<tr class="odd">
<td>Työmallin koodi</td>
<td>Valitse työmalli, joka synnyttää prosessin työn. Esimerkiksi jos vastaanotat nimikkeen ostotilaukselle, hyllytystyö luodaan työmallin perusteella. Jos et valitse työmallia, Microsoft Dynamics 365 for Finance and Operations määrittää kyselyehtoperustaiset mallit. Katso lisätietoja työmalleista artikkelista <a href="control-warehouse-location-directives.md">Varastotyön hallinta työmalleilla ja sijaintidirektiiveillä</a>.</td>
</tr>
</tbody>
</table>

## <a name="require-workers-to-confirm-the-product-location-or-quantity-when-they-pick-items"></a>Edellytä, että työntekijät vahvistavat tuotteen, sijainnin tai määrän nimikkeitä keräillessään.
Voit määrittää työn vahvistukset, jotka edellyttävät, että työntekijän käyttää mobiililaitetta sijainnin tai määrän rekisteröintiin suorittaessaan työtä varastossa. Työn vahvistusten avulla voidaan varmistaa, että työntekijä on oikeassa sijainnissa tai käsittelee oikeaa nimikkeiden määrää. Voit myös antaa Microsoft Dynamics 365 for Finance and Operationsin automaattisesti vahvistaa työntekijän rekisteröinnin. Jos otat käyttöön automaattisen vahvistuksen, et voi edellyttää vahvistuksia sijainnille tai määrälle. Työn vahvistukset sisältävät myös tuotteita ja tuotevariantteja. Voit myös rekisteröidä vahvistuksia lukemalla viivakoodin. Vahvistaaksesi tuotteita ja tuotevariantteja, sinun on syötettävä tuotteen tai tuotevariantin tunnus. Tunnus voi olla tuotetunnus, tuotehaun tunnus, ulkoinen tunnus, GTIN-koodi tai viivakoodi. Kun olet kirjoittanut tunnuksen tai skannannut viivakoodin, tuotevariantin dimensiot näkyvät mobiililaitteessa. 

Seuraavassa taulukossa on kuvattu eri työtyypit, joiden kanssa työn vahvistuksia voi käyttää.

| Vaihtoehto                 | Kuvaus                                                                |
|------------------------|----------------------------------------------------------------------------|
| Keräilyt                   | Pyydä vahvistus keräiltäessä nimikkeitä.                                |
| Määritä                    | Vaadi vahvistus, kun nimikkeet viedään sijaintiin.                     |
| Inventointi               | Pyydä vahvistus inventoinnin aikana.                                |
| Oikaisut            | Vaadi vahvistus varastomääriä muokattaessa.               |
| Mukautettu                 | Pyydä vahvistus mukautetuille töille.                                      |
| Karanteeni             | Vaadi vahvistus, kun nimikkeitä siirretään karanteeniin.                   |
| Rekisterikilpikoonti | Vaadi vahvistus, kun nimikkeitä yhdistellään rekisterikilven luontia varten. |
| Tulosta                  | Vaadi vahvistus, kun rekisterikilpiä tulostetaan.                |
| Tilan muutos          | Vaadi vahvistus, kun varaston tilaa muutetaan.              |

**Huomautus:** Voit vaatia tuotteen vahvistusta ainoastaan keräily- ja laitto-työtyypeille.

<a name="additional-resources"></a>Lisäresurssit
--------

[Määritä mobiililaitteen valikkovaihtoehto työn valmistumista varten Ostotilaus-tyypissä (tehtäväopas)](tasks/set-up-mobile-device-menu.md)

[Määritä mobiililaitteen valikkovaihtoehto vastaanotettujen nimikkeiden rekisteröinnille (tehtäväopas)](tasks/set-up-mobile-device-menu-item-register-received-items.md)
[Varastotilojen käytön hyödyt](../inventory/inventory-statuses.md)


