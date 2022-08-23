---
title: Sähköisen raportoinnin tietomallien parametrisoitujen kutsujen tukeminen
description: Tässä artikkelissa kerrotaan, miten sähköisen raportoinnin tietomallien parametrisoidut kutsut toteutetaan.
author: kfend
ms.date: 03/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: 10.0.15
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula, ERDataModelDesigner
ms.openlocfilehash: 5be189c19d963991ec012de189bbf7b721b88fef
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275985"
---
# <a name="support-parameterized-calls-of-er-data-models"></a>Sähköisen raportoinnin tietomallien parametrisoitujen kutsujen tukeminen

[!include [banner](../includes/banner.md)]

Voit luoda liikeasiakirjoja määrittämällä [Sähköisen raportoinnin (ER)](general-electronic-reporting.md) ratkaisun, joka sisältää seuraavat ER-komponentit:

- **[Muoto](er-overview-components.md#format-component)** – Tämä osa määrittää liiketoiminta-asiakirjan rakenteen.
- **Muotomääritys** – Tämä komponentti määrittää, miten liiketoimintatiedosto täytetään suorituksen aikana.
- **[Mallimääritys](er-overview-components.md#model-mapping-component)** – Tämä komponentti määrittää, mitä tietoja sovelluksesta tulee muotomääritykseen.
- **[Tietomalli](er-overview-components.md#data-model-component)** – Tämä komponentti siirtää tietoja yksittäisten komponenttien välillä.

Kun suoritat ER-muodon, jokainen muotoelementti suoritetaan alkumuotoelementistä. Aina kun suoritettava muotoelementti sisältää sidonnan [tietolähteeseen](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents), odotettujen tietojen toimitus suoritetaan tietolähteen avulla ja sen avulla täytetään muotoelementti. Kun *malli* tyypin tietolähdettä kutsutaan, sopivaa mallimääritystä kutsutaan tietojen vetämiseen sovelluksesta mallin määritysasetusten mukaan.

Aikaisemmin näitä mallikartoituskutsuja ei voitu parametrisoida, jotta ne olisivat riippuvaisia suoritettavan muodon logiikasta. Vain seuraavaa tietotyönkulkua tukittiin.

<table>
<tbody>
<tr align="center">
<td>
<b>Muoto</b><br>
Muoto&nbsp;elementti<br>
&nbsp;
</td>
<td>
<i>Sidonta</i><br>
&gt;&nbsp;pyyntö&nbsp;&gt;<br>
&lt;&nbsp;arvo&nbsp;&lt;
</td>
<td><b>Muodon&nbsp;yhdistäminen</b><br>
Tietolähde<br>
&nbsp;
</td>
<td>
<i>Tietomalli</i><br>
&gt;&nbsp;pyyntö&nbsp;&gt;<br>
&lt;&nbsp;arvo&nbsp;&lt;
</td>
<td>
<b>Mallin&nbsp;määritys</b><br>
Tietolähde<br>
&nbsp;
</td>
<td>
<i>Sidonta</i><br>
&gt;&nbsp;pyyntö&nbsp;&gt;<br>
&lt;&nbsp;arvo&nbsp;&lt;
</td>
<td>
<b>Taulu</b><br>
Tallenna<br>
Kenttä
</td>
</tr>
</tbody>
</table>

Versiossa 10.0.15 ja sitä myöhemmässä versiossa voit kuitenkin määrittää tietomallikenttiä, joita voidaan kutsua vain silloin, kun konfiguroitujen parametrien arvot on määritetty. Kun tällainen kenttä konfiguroidaan ja sitä kutsutaan muotokomponentista, pakolliset parametrit on määritettävä muodossa, joka on yhtä sitova kuin puhelun argumentit. Tällöin argumenttien arvot voidaan määrittää muotokohtaisten arvojen perusteella. Siksi voit käyttää tietomallien kutsuissa **dynaaminen suoritusajan parametrisointia**, joka tukee seuraavaa tietotyönkulkua.

<table>
<tbody>
<tr align="center">
<td>
<b>Muoto</b><br>
Muotoelementti&nbsp;1<br>
<br>
Muotoelementti&nbsp;2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Sidonta</i><br>
&gt;&nbsp;pyyntö&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;arvo&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;pyyntö&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;arvo&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Muodon&nbsp;yhdistäminen</b><br>
Tietolähde&nbsp;1<br>
&nbsp;<br>
<b>value2=Func(value1)</b><br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Tietomalli</i><br>
&gt;&nbsp;kenttä1&nbsp;&gt;<br>
&lt;&nbsp;arvo&nbsp;1&nbsp;&lt;<br>
<b>&gt;&nbsp;field2(value2)&nbsp;&gt;</b><br>
&lt;&nbsp;arvo&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Mallin&nbsp;määritys</b><br>
Tietolähde&nbsp;1<br>
<br>
Tietolähde&nbsp;2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Sidonta</i><br>
&gt;&nbsp;pyyntö&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;arvo&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;pyyntö&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;arvo&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Taulu&nbsp;1</b><br>
Tietue&nbsp;1<br>
Kenttä&nbsp;1<br>
<b>Taulu&nbsp;2</b><br>
Tietue&nbsp;2<br>
Kenttä&nbsp;2
</td>
</tr>
</tbody>
</table>

Uusien toimintojen avulla voit parametrisoida puhelun mihin tahansa [*tietue*](er-formula-supported-data-types-composite.md#record)- tai [*tietueluettelo*](er-formula-supported-data-types-composite.md#record-list)-tyypin tietomallikenttään. Tietomallikentän parametreissa tuetaan seuraavia tietotyyppejä:

- [Totuusarvo](er-formula-supported-data-types-primitive.md#boolean)
- [Säilö](er-formula-supported-data-types-composite.md#container)
- [Päivämäärä](er-formula-supported-data-types-primitive.md#date)
- [Päivämäärä ja aika](er-formula-supported-data-types-primitive.md#datetime)
- [GUID](er-formula-supported-data-types-primitive.md#guid)
- [Int64](er-formula-supported-data-types-primitive.md#int64)
- [Kokonaisluku](er-formula-supported-data-types-primitive.md#integer)
- [Reaaliluku](er-formula-supported-data-types-primitive.md#real)
- [Merkkijono](er-formula-supported-data-types-primitive.md#string)

Voit määrittää kaikki tietomallikentän parametrit, joille argumentti voidaan antaa yksittäisenä tietotyypin arvona, sekä näiden arvojen [*luettelon*](er-formula-supported-data-types-composite.md#record-list).

> [!NOTE]
> Tietomallikentän parametrin oletusarvoa ei tueta. Jos lisäät parametrin tietomallin kenttään ja kyseisen tietomallin versio on jo julkaistu ja julkaistu, sinun on [pohjustettava](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) kaikki vastaavat mallivastaukset ja -muodot tämän mallin uuteen versioon, koska tämä tietomallin muutos ei ole taaksepäin yhteensopiva.

Voit konfiguroida parametrisoituja tietomallikenttiä niin, että mallimäärityskutsut ovat muotokohtaisia. Tämän menetelmän avulla voit vähentää mallimääritysten määrää, joka on konfiguroitu useassa yksittäisessä tietomallissa. Tämän menetelmän avulla voit myös parantaa muotojen suoritustehoa ja lyhentää liiketoimintatiedostojen luomiseen tarvittavaa aikaa. Saat lisätietoja tästä toiminnosta suorittamalla tämän artikkelin esimerkin.

## <a name="example-use-parameterized-calls-of-er-data-models"></a>Esimerkki: Sähköisen raportoinnin tietomallien parametrisoitujen kutsujen käyttäminen

Seuraavissa vaiheissa selitetään, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin käyttäjä voi suunnitella tietomallin sisältävän ER-ratkaisun, mallimäärityksen sekä muodon ER-komponentin, joka on määritetty kutsumaan mallimääritystä muodosta, antamalla puhelun argumentin, jonka arvo on laskettu ajon aikana käyttämällä suoritusmuodon kaavaa. 

Nämä vaiheet voidaan suorittaa **DEMF**-yrityksessä. Koodimuutoksia ei tarvita. 

Tässä esimerkissä luodaan pakollisia ER-[konfiguraatioita](general-electronic-reporting.md#Configuration) malliyritykselle **Litware, Inc**. Tarkista, että malliyrityksen **Litware, Inc.** (`http://www.litware.com`) konfiguraatiopalvelu luetteloitu ER-kehyksessä ja merkitty tilaan **Aktiivinen**. Jos tämä määrityspalvelu ei ole luettelossa tai jos se ei ole merkittynä **aktiiviseksi**, noudata ohjeaiheen [Konfiguraatiopalvelun luominen ja sen merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) vaiheita.

### <a name="business-scenario"></a>Liiketoimintaskenaario

Sinulla on ER-ratkaisu, joka sisältää muodon, jonka voit suorittaa sähköisten tiedostojen kirjausta varten. Tämä muoto sisältää myynti- ja ostotilauksiin liittyviä verotapahtumia, joissa on tarvittavat tiedot, kuten tapahtuman päivämäärä ja veroarvo. Uuden tilikauden jälkeen tämän asiakirjan rakenne on muuttunut. Sinun on nyt lähetettävä laajennettu asiakirja, joka sisältää kaikkien niiden osapuolten (asiakkaiden ja toimittajien) lisätiedot, joiden tapahtumat esitetään luoduissa raporteissa. Siksi sinun on muokattava ER-ratkaisuasi niin, että se luo tämän uuden vaatimuksen noudattamia asiakirjoja.

### <a name="configure-the-er-framework"></a>Määritä ER-kehys

Seuraa vaiheita kohdassa [Määritä ER-kehys](er-quick-start2-customize-report.md#ConfigureFramework) luodaksesi ER-parametrien vähimmäisjoukon. Nämä asetukset on suoritettava, ennen kuin ER-kehystä käytetään uuden ER-ratkaisun suunnitteluun.

### <a name="design-a-domain-specific-data-model"></a>Toimialuekohtaisen tietomallin suunnitteleminen

Sinun on luotava uusi ER-konfiguraatio, joka sisältää vaaditun tietomallikomponentin. Tätä tietomallia käytetään myöhemmin tietolähteenä suunniteltaessa ER-muotoa tarkastusraportin luomiseksi.

Noudata näitä ohjeita, kun haluat tuoda vaaditun tietomallin Microsoftin toimittamasta XML-tiedostosta.

1. Lataa [Sample audit model.version.1.xml](https://download.microsoft.com/download/7/1/9/719b0132-fed7-4c73-8afa-90cac29c2fee/Sample-audit-model.version.1.xml) -tiedosto ja tallenna se paikalliseen tietokoneeseen.
2. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
3. Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**.
4. Valitse toimintoruudun **Konfiguroinnit**-välilehdessä **Vaihda**\>**Lataa XML-tiedostosta**.
5. Valitse **Selaa** ja etsi ja valitse **Sample audit model.version.1.xml** -tiedosto.
6. Tuo konfigurointi valitsemalla **OK**.

    ![Tuotu ER-tietomallin määritys Määritykset-sivulla.](./media/er-data-model-parameterized-calls-imported-model.png)

Seuraavassa kuvassa näkyy **tietomallin suunnittelu** -sivulla muokattava versio määritetystä tietomallista.

![ER-tietomallin rakenne Tietomallin suunnittelu -sivulla.](./media/er-data-model-parameterized-calls-model1.png)

Malli on suunniteltu siten, että se paljastaa vain ne verotapahtumat, joilla on tarvittavat tiedot.

### <a name="design-a-model-mapping-for-the-configured-data-model"></a>Mallin määrityksen suunnitteleminen konfiguroidulle tietomallille

Elektronisen raportoinnin kehittäjäroolin käyttäjänä sinun on luotava uusi ER-kokoonpano, joka sisältää mallin kartoituskomponentin näytetarkastustietomallille. Tämä komponentti toteuttaa Microsoft Dynamics 365 Financen konfiguroidun tietomallin, se liittyy nimenomaan kyseiseen sovellukseen. Mallikartoituskomponentti on konfiguroitava niin, että se määrittää sovellusobjektit, joita käytetään määritetyn tietomallin täyttämiseen sovellustiedoilla suorituksen aikana. Tämän tehtävän suorittaminen edellyttää, että olet tietoinen veroliiketoimialueen tietorakenteen toteutustavasta Financessa.

Noudata näitä ohjeita, kun haluat tuoda vaaditun tietojen yhdistämismäärityksen Microsoftin toimittamasta XML-tiedostosta.

1. Lataa [Sample audit model mapping.version.1.1.xml](https://download.microsoft.com/download/c/0/3/c03a4673-b1b1-4ef8-96d0-bf96518be6e0/Sample-audit-model-mapping.version.1.1.xml) -tiedosto ja tallenna se paikalliseen tietokoneeseen.
2. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
3. Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**.
4. Valitse toimintoruudun **Konfiguroinnit**-välilehdessä **Vaihda**\>**Lataa XML-tiedostosta**.
5. Valitse **Selaa** ja etsi ja valitse **Sample audit model mapping.version.1.1.xml** -tiedosto.
6. Tuo konfigurointi valitsemalla **OK**.

    ![Tuotu ER-tietomallin yhdistämismääritys Määritykset-sivulla.](./media/er-data-model-parameterized-calls-imported-mapping.png)

Seuraavassa kuvassa näkyy **mallikartoituksen suunnittelu** -sivulla määritetyn mallikartoituksen muokattava versio.

![ER-mallin yhdistämismäärityksen rakenne Mallin yhdistämismäärityksen suunnittelu -sivulla.](./media/er-data-model-parameterized-calls-mapping1.png)

Mallikartoitus on suunniteltu siten, että se paljastaa ne verotapahtumat, joilla on tarvittavat tiedot. Se hakee nämä tiedot `TaxTrans`-sovellustaulukosta käyttämällä konfiguroituja `TaxTrans`- ja `TaxTransFiltered` ER-tietolähteitä.

### <a name="design-a-new-format"></a>Uuden muodon suunnittelu

Sähköisen raportoinnin toiminnallinen konsultti -roolin käyttäjänä sinun on luotava uusi ER-konfiguraatio, joka sisältää muoto-komponentin. Muotokomponentti on määritettävä, jotta luotuihin raportteihin voidaan täyttää kaikki tarvittavat tiedot täyttävät verotapahtumat.

Noudata näitä ohjeita, kun haluat tuoda vaaditun muodon Microsoftin toimittamasta XML-tiedostosta.

1. Lataa [Sample audit format.version.1.1.xml](https://download.microsoft.com/download/e/b/7/eb7e126e-2bb3-4bbb-a735-ffd4c48920b1/Sample-audit-format.version.1.1.xml) -tiedosto ja tallenna se paikalliseen tietokoneeseen.
2. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
3. Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**.
4. Valitse toimintoruudun **Konfiguroinnit**-välilehdessä **Vaihda**\>**Lataa XML-tiedostosta**.
5. Valitse **Selaa** ja etsi ja valitse **Sample audit format.version.1.1.xml** -tiedosto.
6. Tuo konfigurointi valitsemalla **OK**.

    ![Tuotu ER-muodon määritys Määritykset-sivulla.](./media/er-data-model-parameterized-calls-imported-format.png)

Seuraavassa kuvassa näkyy **muodon suunnittelu** -sivulla määritetyn muodon muokattava versio.

![ER-muodon rakenne Muodon suunnittelu -sivulla.](./media/er-data-model-parameterized-calls-format1.png)

ER-muoto on määritetty luomaan raportti tekstitiedostona pilkuilla erotettuina (CSV) arvoina.

### <a name="run-the-imported-format"></a>Tuodun muodon suorittaminen

1. Valitse **Konfiguroinnit**-sivulla **Mallitarkastusmuoto**-määritys ja valitse sitten Toimintoruudusta **Suorita**.
2. Valitse **Sähköisen raportin parametrit** -valintaikkunan **Sisällytettävät tietueet** -välilehdessä **Suodata**.
3. Määritä ehdot **PIV-110000004** ja **INV-10000001** tositteiden verotapahtumien valitsemista varten.
4. Valitse **OK**.
5. Valitse **OK**.
6. Tarkista luotu tiedosto, joka sisältää valittujen tositteiden verotapahtumat.

    ![Luodun tiedoston esiversio ja verotapahtumat.](./media/er-data-model-parameterized-calls-output1.png)

### <a name="adjust-the-imported-er-solution"></a>Tuodun ER-ratkaisun muokkaaminen

Uuden vaatimuksen mukaan toimitettavan asiakirjan on sisällettävä niiden asiakkaiden ja toimittajien nimet, joiden tapahtumat sisältyvät siihen. Siksi sinun on muokattava tuotua ER-ratkaisua niin, että se luo asiakirjan, joka täyttää tämän uuden vaatimuksen.

Valitse, miten tuodut ER-komponentit on tarpeen muuttaa.

Ilmeinen lähestymistapa on toteuttaa seuraavat muutokset:

- Lisää `Transaction.Party.Name`-tietomalliin *merkkijono* tyypin uusi tietomallikenttä.
- Määritä mallimäärityksessä uuden tietomallikentän sidonta käyttämällä käytettävissä olevia taulusuhteita, jotta `DirPartyTable`-sovellustaulun tietue voidaan avata ja `Name`-kentän arvo haetaan siitä.

Vaikka tämä menetelmä toimii, se saattaa aiheuttaa SQL-tietokannan suorituskykyongelmia, koska `TaxTrans` on tapahtumataulu ja voi näin ollen sisältää suuria tietueita. Tässä tapauksessa `DirPartyTable`-kutsujen määrän on oltava sama kuin `TaxTrans`-taulun tietueiden määrä, joka voi aiheuttaa suorituskykyongelmia.

Voit vaihtoehtoisesti toteuttaa seuraavat muutokset:

- Lisää tietomalliin uusi `Party`-juuri ja uusi `Party.Name`-kenttä.
- Lisää mallimäärityksessä uusi tietolähde, joka liittää taulujen kaikki tietueet, joita käytetään taulusuhteissa `DirPartyTable`-sovellustaulun tietueen avaamiseen `TaxTrans`-taulusta alkaen.

Vaikka tämä lähestymistapa toimii, se saattaa aiheuttaa muistinkulutusongelmia. Tulos on haettava sovelluspalvelimen muistiin silloinkin, kun uusi [JOIN](er-join-data-sources.md)-tietolähde suoritetaan sovellustietokantaan yhtenä SQL-pyyntönä tietokannan suorituskyvyn estämiseksi. Koska tietueiden määrä ja kenttien määrä ovat hyvin suuret, tämä menetelmä saattaa aiheuttaa erittäin paljon muistin kulutusta. Muisti lopussa -suorituspalvelupoikkeus voidaan jopa esittää.

Voit toteuttaa muutokset, kun juokseva muoto kerää muistiin asiakkaiden ja toimittajien yksilöivät tunnuskoodit kaikille verotapahtumista, jotka esitetään luodussa raportissa. Koska vain yksilöivät koodit on pidettävä, lopullinen koodijoukko ei ole tarpeeksi suuri, jotta se vaikuttaa muistin kulutukseen. Koodijoukko välitetään sitten mallin määritykseen *malli* tyypin tietolähteen toisen kutsun argumenttina. Kutsun perusteella mallimääritys suorittaa uuden ER-tietolähteen, joka määrittää sovellustietokantaan yhden SQL-pyynnön, joka noutaa `DirPartyTable`-taulusta vain niiden osapuolten tietueet, joiden koodit on määritetty koodijoukkoon.

### <a name="adjust-the-imported-data-model"></a>Tuodun tietomallin muokkaaminen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta ja valitse **Mallitarkastusmalli**.
3. Valitse **Versiot**-pikavälilehdessä konfiguraatioversio **2**, jonka tila on **Luonnos**.
4. Valitse **Määrityksen osat** -pikavälilehti.
5. Valitse **Suunnittelutoiminto** avataksesi tietomallin muokkaamista varten.
6. Varmista **Tietomalli**-sivulla, että `Root`-kenttä on valittuna, ja valitse sitten **Uusi**.
7. Toimi avattavassa valintaikkunassa seuraavasti:

    1. Valitse **Uusi solmu** -kenttäryhmästä **aktiivisen solmun alisolmuasetus** -vaihtoehto.
    2. Kirjoita **Nimi**-kenttään **Osapuoli**.
    3. Valitse **Nimiketyyppi**-kentässä **Tietueluettelo**.
    4. Lopeta uuden kentän lisääminen valitsemalla **Lisää**.

8. Varmista, että `Root.Party`-kenttä on valittuna, ja valitse sitten **parametrit** **Node**-välilehdellä.
9. Toimi **Parametrit**-valintaikkunassa seuraavasti:

    1. Valitse **Parametrit**-välilehdessä **Uusi**.
    2. Kirjoita **Nimi**-kenttään **PartyRefRecId**.
    3. Valitse **Tyyppi**-kentästä **Int64**.
    4. Valitse **Luettelo**-valintaruutu.
    5. Viimeistele parametrien kirjoittaminen valitsemalla **OK**.

    > [!NOTE]
    > Olet juuri määrittänyt `Root.Party`-tietomallikentän kentälle, jota kutsutaan, kun **PartyRefRecId**-parametrissa annetaan arvo. Arvon on oltava niiden tietueiden luettelossa, joiden *Int64*-tietotyyppinä on `Value`-kenttä.

    ![Parametrit-valintaikkuna.](./media/er-data-model-parameterized-calls-model2a.png)

10. Varmista, että `Root.Party`-kenttä on yhä valittuna, ja valitse sitten **Uusi**.
11. Toimi avattavassa valintaikkunassa seuraavasti:

    1. Valitse **Uusi solmu** -kenttäryhmästä **aktiivisen solmun alisolmuasetus** -vaihtoehto.
    2. Kirjoita **Nimi**-kenttään **Nimi**.
    3. Valitse **Nimiketyyppi**-kentässä **Merkkijono**.
    4. Lopeta uuden kentän lisääminen valitsemalla **Lisää**.

12. Valitse **Tallenna** ja sulje sitten **Tietomalli**-sivu.

    ![Muokatun ER-tietomallin rakenne Tietomallin suunnittelu -sivulla.](./media/er-data-model-parameterized-calls-model2b.png)

13. Valitse **Versiot**-pikavälilehdessä versio **2**, valitse **Muuta tila** \> **Valmis**. Valitse sitten **OK**.

    > [!NOTE]
    > Tietomallisi muutokset tallennetaan **Mallitarkastusmalli** -tietomallikomponentin toiseen versioon, joka sijaitsee **Mallitarkastusmallin** ER -konfiguraation toisessa versiossa.

![Päivitetty ER-tietomallin määritys Määritykset-sivulla.](./media/er-data-model-parameterized-calls-updated-model.png)

### <a name="adjust-the-imported-model-mapping"></a>Tuodun tietomallimäärityksen muokkaaminen

1. Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta ja laajenna **Mallitarkastusmalli**.
2. Valitse **mallitarkastusmallin määritys** ja valitse sitten **Versiot**-pikavälilehdestä toinen määritysversio, joka perustuu ensimmäiseen tietomalliversioon (versio **1.2**) ja jonka tila on **Luonnos**.
3. Valitse **Pohjusta**.
4. Jätä **Kohdeversio**-kenttään **mallitarkastusmallin** perusmallin versio **2**.
5. Valitse **OK**, jos haluat kohdistaa mallimäärityksen uudelleen viimeaikaisten tietomallimuutosten kanssa.

    Huomaa, että muokattavissa olevan mallin määrityksen versionumero on muuttunut versiosta **1.2** versioon **2.2** sen merkiksi, että toista malliversiota käytetään tällä hetkellä pohjana.

6. Valitse **Suunnittelu**.
7. Valitse **Malli tietolähteen yhdistämismääritystä varten** -sivun nykyisen mallimäärityksen **Suunnittelija**.
8. Lisää `DirPartyTable`-sovellustauluun uusi tietolähde noudattamalla seuraavia ohjeita:

    1. Valitse **Tietolähdetyyppi**-ruudusta **Dynamics 365 for Operations \> Taulukkotiedot**.
    2. Valitse **Tietolähteet**-ruudussa **Lisää juuri**.
    3. Kirjoita **Nimi**-kenttään **PartyTable**.
    4. Kirjoita **Taulu**-kenttään **DirPartyTable**.
    5. Lopeta uuden tietolähteen lisääminen valitsemalla **OK**.

9. Noudata näitä ohjeita lisätäksesi uuden tietolähteen `DirPartyTable`-tietueiden pyytämiseen toimitetun tietuetunnistekoodiluettelon perusteella:

    1. Laajenna **Tietolähdetyypit** -ruudussa **Yleiset \> Tyhjä säilö**.
    2. Valitse **Tietolähteet**-ruudussa **Lisää juuri**.
    3. Kirjoita **Nimi**-kenttään **Data**.
    4. Lopeta uuden tietolähteen lisääminen valitsemalla **OK**.
    5. Valitse **Tietolähteet**-ruudussa **Data**-tietolähde.
    6. Valitse **Tietolähdetyyppi**-ruudusta **Toiminnot \> Laskettu kenttä**.
    7. Valitse **Tietolähteet**-ruudussa **Lisää**.
    8. Kirjoita **Nimi**-kenttään **DirParty**.
    9. Valitse **Muokkaa kaavaa**.
    10. Valitse **Kaavan suunnittelutoiminto** -sivulla **Parametrit**.
    11. Toimi **Parametrit**-valintaikkunassa seuraavasti:

        1. Valitse **Parametrit**-välilehdessä **Uusi**.
        2. Kirjoita **Nimi**-kenttään **DirPartyId**.
        3. Valitse **Tyyppi**-kentästä **Int64**.
        4. Valitse **Luettelo**-valintaruutu.
        5. Valitse **OK**.

        > [!NOTE]
        > Juuri konfiguroit tämän lasketun kentän niin, että se hyväksyy ajon aikana yhden sellaisen parametrin argumentin, joka on määritetty tietueluetteloksi, jossa on yksi *Int64*-tyypin `Value`-kenttä.

    12. Syötä **Kaava**-kenttään seuraava lauseke:

        `FILTER(PartyTable, VALUEINLARGE(PartyTable.RecId, DirPartyId, DirPartyId.Value))`

        > [!NOTE]
        > Olet juuri määrittänyt `DirParty`-lasketun kentän hakemaan vain `DirPartyTable`-tietueet, joissa tietueen tunnuskoodit sisältyvät `DirPartyId`-luetteloon, joka annetaan argumenttina, kun `DirParty`-kenttää kutsutaan.

        ![Resepti, jonka avulla osapuolen nimet noudetaan reseptien suunnittelusivun sovellustaulusta.](./media/er-data-model-parameterized-calls-formula1.png)

    13. Valitse **Tallenna** ja sulje **Kaavan suunnittelutoiminto** -sivu.
    14. Valitse **Tallenna** ja viimeistele uuden tietolähteen lisääminen valitsemalla **OK**.

10. Sido uusi tietolähde uuteen tietomallikenttään näiden ohjeiden avulla, jotta tietomallia käytetään osapuolien nimien paljastamiseen:

    1. Valitse **Tietomalli**-ruudussa `Root.Party`-tietomallikenttä.
    2. Valitse **Tietomalli**-ruudussa **Muokkaa**.
    3. Syötä **Kaavan suunnittelutoiminto** -sivun **Kaava**-kenttään lauseke `Data.DirParty(PartyRefRecId)`.
    4. Valitse **Tallenna** ja sulje **Kaavan suunnittelutoiminto** -sivu.

        > [!NOTE]
        > Olet juuri konfiguroinut sidonnaiset kutsumaan konfiguroitua `Data.DirParty`-tietolähdettä ja antamaan luettelon tietuetunnuskoodeista, jotka määritetään muodossa `Root.Party`-tietomallikenttää kutsuttaessa.

    5. Valitse **Tietomalli**-ruudussa `Root.Party.Name`-tietomallikenttä.
    6. Valitse **Tietomalli**-ruudussa **Muokkaa**.
    7. Valitse **Kaavan määrityksen suunnittelu** -sivun **Tietolähde**-ruudusta **Data \> DirParty** ja valitse **Nimi**.
    8. Valitse **Lisää tietolähde**.
    9. Valitse **Tallenna** ja sulje **Kaavan suunnittelutoiminto** -sivu.

    ![Muokatun ER-mallin yhdistämismäärityksen rakenne Mallin yhdistämismäärityksen suunnittelu -sivulla.](./media/er-data-model-parameterized-calls-mapping2.png)

11. Valitse **Tallenna** ja sulje **Mallin yhdistämismäärityksen suunnitteluohjelma** -sivu.
12. Sulje **Malli tietolähteen yhdistämismääritystä varten** -sivu.
13. Valitse **Versiot**-pikavälilehdessä versio **2.2**, valitse **Muuta tila \> Valmis**. Valitse sitten **OK**.

### <a name="adjust-the-imported-format"></a>Tuodun muodon muokkaaminen

1. Valitse **Konfiguroinnit**-sivulla **Mallitarkastuksen muoto**.
2. Valitse **Versiot**-pikavälilehdessä konfiguraatioversio **1.2**, jonka tila on **Luonnos**.
3. Valitse **Pohjusta**.
4. Jätä **Kohdeversio**-kenttään **mallitarkastusmallin** perusmallin versio **2**.
5. Valitse **OK**, jos haluat kohdistaa muodon uudelleen viimeaikaisten tietomallimuutosten kanssa.
6. Valitse **Suunnittelu**.
7. Valitse **Muodon suunnittelija** -sivun vasemman ruudun muodon rakennepuussa **Laajenna/Tiivistä**.
8. Näiden ohjeiden avulla voit lisätä uuden muotoelementin, jonka muodostamisraporteissa näytetään niiden osapuolten tietuetunnuskoodit, joiden tapahtumat näytetään.

    1. Valitse muodon rakennepuussa **Report.Row.Trans**-järjestyselementti.
    2. Valitse **Lisää**.
    3. Valitse **Lisää**-valintaikkunassa **Tietolähde \> Nimike**.
    4. Syötä **Komponentin ominaisuudet**-valintaikkunan **Nimi**-kenttään **Tunnus**.
    5. Valitse **Tietotyyppi**-kentässä **Int64**.
    6. Valitse **OK**.

    > [!NOTE]
    > **Tietolähde \> Nimike**-elementin avulla voi suorittaa sisäisiä laskelmia ja tietojen muunnosta vain suoritettavan muodon alueella. Tämän vuoksi et muuta luodun tiedoston sisältöä lisäämällä tämän muotoelementin.

9. Noudata näitä ohjeita lisätäksesi uusia muotoelementtejä osapuolien nimien syöttämiseksi luotuihin raportteihin:

    1. Valitse **Report.Row**-järjestyselementti.
    2. Valitse **Lisää**.
    3. Valitse **Lisää**-valintaikkunassa **Teksti \> Järjestys**.
    4. Syötä **Komponentin ominaisuudet**-valintaikkunan **Nimi**-kenttään **Osapuoli**.
    5. Valitse **OK**.
    6. Valitse **Report.Row.Party**-järjestyselementti.
    7. Valitse **Lisää**.
    8. Valitse **Lisää**-valintaikkunassa **Teksti \> Merkkijono**.
    9. Syötä **Komponentin ominaisuudet**-valintaikkunan **Nimi**-kenttään **Nimi**.
    10. Valitse **OK**.

10. Näiden ohjeiden avulla voit lisätä uuden tietolähteen, jonka muodostamisraporteissa näytetään niiden osapuolten tietuetunnuskoodit, joiden tapahtumat näytetään.

    1. Valitse **Yhdistämismääritys**-välilehdessä **Lisää juuri**.
    2. Valitse **Lisää tietolähde** -valintaikkunassa **Funktiot \> Tietojenkeruu**.
    3. Syötä **'Tietokokoelma' -tietolähteen ominaisuudet** -valintaikkunan **Nimi**-kenttään **PartyIds**.
    4. Valitse **Nimiketyyppi**-kentässä **Int64**.
    5. Valitse **OK**.

11. Näiden ohjeiden avulla voit lisätä uuden sidoksen, jonka muodostamisraporteissa näytetään niiden osapuolten tietuetunnuskoodit, joiden tapahtumat näytetään.

    1. Valitse muodon rakennepuussa **Report.Row.Trans.Id**-tietonimike-elementti.
    2. Valitse **Muokkaa kaavaa**.
    3. Syötä **kaavansuunnittelu**-sivulla lauseke `PartyIds.Collect(model.Transaction.Party.RecId)`.
    4. Valitse **Tallenna** ja sulje **Kaavan suunnittelutoiminto** -sivu.

12. Noudata näitä vaiheita lisätäksesi uusia sidoksia osapuolien nimien syöttämiseksi luotuihin raportteihin:

    1. Valitse muodon rakennepuussa **Report.Party**-järjestyselementti.
    2. Valitse **Muokkaa kaavaa**.
    3. Syötä **kaavansuunnittelu**-sivulla lauseke `model.Party(PartyIds.Result)`.
    4. Valitse **Tallenna** ja sulje **Kaavan suunnittelutoiminto** -sivu.
    5. Valitse muodon rakennepuussa **Report.Party.Name**-järjestyselementti.
    6. Valitse **Yhdistämismääritys**-välilehdestä `model.Party.Name`-tietomallikenttä.
    7. Valitse **Sido**.

    ![Muokattu ER-muodon rakenne Muodon suunnittelu -sivulla.](./media/er-data-model-parameterized-calls-format2.png)

13. Valitse **Tallenna** ja sulje **Muodon suunnittelutoiminto** -sivu.
14. Sulje **Malli tietolähteen yhdistämismääritystä varten** -sivu.
15. Valitse **Versiot**-pikavälilehdessä versio **2.2**, valitse **Muuta tila** \> **Valmis**. Valitse sitten **OK**.

### <a name="run-the-adjusted-format"></a>Muokatun muodon suorittaminen

1. Valitse **Konfiguroinnit**-sivulla **Mallitarkastusmuoto** ja valitse sitten Toimintoruudusta **Suorita**.
2. Valitse **Sähköisen raportin parametrit** -valintaikkunan **Sisällytettävät tietueet** -välilehdessä **Suodata**.
3. Määritä ehdot **PIV-110000004** ja **INV-10000001** tositteiden verotapahtumien valitsemista varten.
4. Valitse **OK**.
5. Valitse **OK**.
6. Tarkista luotu tiedosto, joka sisältää valittujen tositteiden verotapahtumat sekä vastaavan asiakkaan ja toimittajan nimet.

    ![Luodun tiedoston esiversio ja verotapahtumat ja osapuolten nimet.](./media/er-data-model-parameterized-calls-output2.png)

7. Siirry kohtaan **Ostoreskontra** \> **Toimittajat** \> **Kaikki toimittajat** ja tarkista valitun **PIV-110000004**-tositteen tiedot sekä toimittajan nimi.

    ![Ostotositteen tietojen tarkasteleminen Kaikki toimittajat- ja Laskukirjauskansio-sivuilla.](./media/er-data-model-parameterized-calls-review1.gif)

8. Siirry kohtaan **Myyntireskontra** \> **Asiakkaat** \> **Kaikki asiakkaat** ja tarkista valitun **INV-10000001**-tositteen tiedot sekä asiakkaan nimi.

    ![Myyntitositteen tietojen tarkasteleminen Kaikki asiakkaat ja Kirjatut arvonlisäverot -sivuilla.](./media/er-data-model-parameterized-calls-review2.gif)

Lisätietoja tästä ER-ratkaisun suorittamisesta saat käyttämällä ER:n sisäänrakennettua [suorituskyvyn jäljityksen](trace-execution-er-troubleshoot-perf.md) jäsennintä.

## <a name="additional-resources"></a>Lisäresurssit

- [Laskettu kenttä -tyyppisten ER-tietolähteiden parametrisoitujen kutsujen tuki](er-calculated-field-type.md)
- [Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi](trace-execution-er-troubleshoot-perf.md)
- [DATA COLLECTION -tietolähteiden käyttäminen sähköisissä raportointimuodoissa](er-data-collection-data-sources.md)
- [ValueInLarge ER -funktio](er-functions-logical-valueinlarge.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
