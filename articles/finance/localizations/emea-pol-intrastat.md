---
title: Puolan Intrastat
description: Tässä artikkelissa on tietoja Intrastat-raportoinnista Puolassa.
author: andosip
ms.date: 11/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.openlocfilehash: 45bd1d3c90d0a8a8ad5db6d0b80c5eed0aa489e8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871098"
---
# <a name="polish-intrastat"></a>Puolan Intrastat

[!include[banner](../includes/banner.md)]

**Intrastat**-sivun avulla voit luoda ja raportoida tietoja Euroopan unionin maiden/alueiden välisestä kaupasta. Puolan Intrastat-ilmoituksessa on raportoinnissa käytettäviä tietoja tavaroiden kaupasta.

Puolan Intrastat-ilmoituksessa on seuraavat kentät. Seuraavia lukuun ottamatta kaikki kentät koskevat sekä tuontia että vientiä: **RodzajTransportu** (kuljetustapa) ja **KrajPochodzenia** (alkuperämaa tai -alue) eivät koske vientiä, kun taas **IdKontrahenta** (asiakkaan ulkomainen ALV-tunnus) ei koske tuontia.

| Kentän nimi | Kuvaus |
|-------------------------|-------------------------|
| Deklaracja Data | Päivämäärä, jona tiedosto on luotu. |
| Miesiac | Ilmoituksen viitekuukausi. |
| Rok | Ilmoituksen viitevuosi. |
| Numer | Viitekauden ilmoitusnumero. |
| Wersja | Ilmoituksen versionumero. |
| NrWlasny | Ilmoituksen tunnus. Arvo luodaan automaattisesti. |
| Typ | Raportin suunta.</br><li>Tuonnin ollessa kyseessä tulostetaan kirjain P.</li><li>Viennin ollessa kyseessä tulostetaan kirjain W.</li> |
| Rodzaj | Ilmoituksen tyyppi. Arvo ilmaisee, onko raportti alkuperäinen ilmoitus vai muutosilmoitus. |
| UC | Sen yksikön koodi, johon Intrastat-ilmoitus on osoitettu. Arvo määritetään **Ulkomaankaupan parametrit** -sivun **Edustaja**-välilehden **Arvonlisävero**-osan **ALV-tunnus**-kentässä. |
| Nazwa | Yrityksen nimi. |
| Miejscowosc, UlicaNumer, KodPocztowy | Yrityksen koko osoite. |
| Nip | Puolan verovelvollisen tunnistenumero (arvonlisäverotunnus [ALV-tunnus]). |
| Regon | Puolan tilastollinen tunnistenumero (yrityksen numero). |
| LacznaWartoscFaktur | Laskun arvojen summa. |
| LacznaWartoscStatystyczna | Tilastoarvojen summa. |
| LacznaLiczbaPozycji | Tavaraerän kokonaismäärä. |
| PozId | Annetun tavaraerän juokseva numero. |
| OpisTowaru | Kauppatavaran kauppanimi. |
| KrajPochodzeniaWysylki | Vastapuolen maan tai alueen ISO (International Organization for Standardization) -koodi. |
| WarunkiDostawy | Toimitusehtojen Intrastat-koodi. |
| RodzajTransakcji | Tapahtuman luonteen ilmaiseva koodi. Puolan yrityksissä käytetään kaksinumeroisia tapahtumakoodeja. |
| KodTowarowy | Yhdistetyn nimikkeistön mukainen kahdeksannumeroinen kauppatavarakoodi. |
| RodzajTransportu | Kuljetustilan Intrastat-koodi. |
| KrajPochodzenia | Sen maan tai alueen ISO-koodi, jossa kauppatavarat tuotettiin tai valmistettiin. |
| MasaNetto | Nettopaino kilogrammoina. |
| IloscUzupelniajacaJm | Määrä lisämittayksikkönä, kokonaislukuina. |
| WartoscFaktury | Kaikkien yhden nimikkeen kattamien tapahtumien laskun arvo. |
| WartoscStatystyczna | Tilastollinen arvo. |
| Wypelniajacy: NazwiskoImie, Telefon, Faks, Email | Ilmoituksen lähettävän henkilön etu- ja sukunimi, puhelinnumero, faksinumero ja sähköpostiosoite. |
| IdKontrahenta | Asiakkaan ulkomainen ALV-tunnus EU-jäsenmaassa. |


## <a name="set-up-intrastat"></a>Määritä Intrastat

Tuo sähköisen raportoinnin (ER) määritysten uusin versio yleisestä säilöstä:

   - Intrastat-malli
   - Intrastat-raportti
   - Intrastat (PL)

Lisätietoja on kohdassa [ER-määritysten lataaminen määrityspalvelun yleisestä varastosta](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Yrityksen ALV-tunnuksen ja yrityksen numeron määrittäminen

### <a name="create-registration-types-for-company-codes"></a>Yrityskoodien rekisteröintityyppien luominen

Yrityskoodeille on luotava kaksi rekisteröintityyppiä: toinen koskee ALV-tunnusta (NIP-koodi) ja toinen yrityksen numero (Regon-koodi).

1. Valitse **Organisaation hallinto** > **Yleinen osoitekirja** > **Rekisteröintityypit** > **Rekisteröintityypit**.
2. Luo ALV-tunnuksen rekisteröintityyppi valitsemalla toimintoruudussa **Uusi**.
3. Anna uuden rekisteröintityypin nimi **Määritä rekisteröintityypin tiedot** -valintaikkunan **Nimi**-kenttään. Anna nimeksi esimerkiksi **NIP**.
4. Valitse **Maa tai alue**-kentässä **POL**.
5. Valitse **Luo**.
6. Luo yrityksen numeron rekisteröintityyppi valitsemalla toimintoruudussa **Uusi**.
7. Anna uuden rekisteröintityypin nimi **Määritä rekisteröintityypin tiedot** -valintaikkunan **Nimi**-kenttään. Anna kenttään esimerkiksi **Regon**.
8. Valitse **Maa tai alue**-kentässä **POL**.
9. Valitse **Luo**.

### <a name="match-the-registration-types-with-registration-categories"></a>Rekisteröintityyppien ja rekisteröintiluokkien kohdistaminen

1. Valitse **Organisaation hallinto** > **Yleinen osoitekirja** > **Rekisteröintityypit** > **Rekisteröintiluokat**.
2. Luo kunkin luodun rekisterityypin ja rekisteriluokan välille linkki valitsemalla toimintoruudussa **Uusi**.

    - Valitse ALV-tunnuksen (NIP-koodi) rekisteröintityypiksi **ALV-tunnus**-rekisteröintiluokka.
    - Valitse yrityksen numeron (Regon-koodi) rekisteröintityypiksi **Yrityksen tunnus (COID)** -rekisteröintiluokka.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Yrityksen ALV-tunnuksen ja yrityksen numeron määrittäminen

1. Valitse **Organisaation hallinto** > **Organisaatiot** > **Yritykset**.
2. Valitse ruudukossa yritys.
3. Valitse toimintoruudussa **Rekisteröintitunnukset**.
4. Valitse **Rekisteröintitunnus**-pikavälilehdessä **Lisää**.
5. Valitse **Rekisteröintityyppi**-kentässä yksi aiemmin luoduista rekisteröintityypeistä.
6. Anna yrityksen ALV-tunnus (NIP-koodi) tai yrityksen numero (Regon-koodi) aiemmassa vaiheessa valitun rekisterityypin perusteella.
7. Toista vaiheet 4–6 toisen aiemmin luodun rekisterityypin osalta.

## <a name="set-up-a-company-address"></a>Yrityksen osoitteen määrittäminen

1. Valitse **Organisaation hallinto** > **Organisaatiot** > **Yritykset**.
2. Valitse ruudukossa yritys.
3. Valitse **Osoitteet**-välilehdessä **Muokkaa**.
4. Valitse **Muokkaa osoitetta** -valintaikkunan **Postinumero**-kentässä yrityksen postinumero.
5. Anna osoite **Katuosoite**-kenttään.
6. Valitse paikkakunta **Paikkakunta**-kentässä.

## <a name="set-up-foreign-trade-parameters"></a>Määritä ulkomaankaupan parametrit

1. Valitse **Vero** > **Määritys** > **Ulkomaankaupan parametrit**.
2. Valitse **Intrastat**-välilehden **Sähköinen raportointi** -pikavälilehden **Tiedostomuodon määritys** -kentässä **Intrastat (PL)**.
3. Valitse **Raporttimuodon määritys** -kentässä **Intrastat-raportti**.
4. Valitse **Kauppatavarakoodihierarkia**-pikavälilehden **Luokkahierarkia**-kentästä **Intrastat**.
5. Valitse **Tapahtumakoodi**-kentässä ominaisuussiirtojen tapahtumakoodi. Tätä koodia käytetään tapahtumissa, jotka tuottavat toteutuneita tai suunniteltuja ominaisuussiirtoja (taloudellista tai muuta) kompensaatiota vastaan. Koodia käytetään myös korjauksiin. Puolan yrityksissä käytetään kaksinumeroisia tapahtumakoodeja.
6. Valitse **Hyvityslasku**-kentässä tapahtumakoodi tavaroiden palautusta varten.
7. Ilmoita **Maan tai alueen ominaisuudet** -välilehden **Maa tai alue** -kentässä kaikki maat tai alueet, joiden kanssa yritys käy kauppaa. Valitse kunkin EU-jäsenmaan kohdalla **Maa-/aluetyyppi**-kentässä **EU**, minkä jälkeen maa näkyy Intrastat-raportissa. Valitse Puolan osalta **Maa-/aluetyyppi**-kentässä **Kotimaa**.
8. Ilmaise sen yksikön koodi, johon Intrastat-ilmoitus on osoitettu, antamalla **Edustaja**-välilehden **Edustaja**-pikavälilehden **Arvonlisävero**-osan **ALV-tunnus**-kentässä **420000**.
9. Anna **Yhteyshenkilö**-välilehdessä ilmoituksen lähettävän henkilön etu- ja sukunimi, puhelinnumero, faksinumero ja sähköpostiosoite.
10. Määritä **Numerosarjat**-välilehden **XML-tiedoston numero** -viitteen **Numerosarjan koodi** -kentässä ei-jatkuva numerosarja, jossa on enintään yhdeksän merkkiä. Tätä kenttää käytetään luomaan automaattisesti **Ilmoituksen tunnus** -kentän arvo Intrastat-raportissa.

## <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Intrastat-ilmoituksen tuoteparametrien määrittäminen

1. Valitse **Tuotetietojen hallinta** > **Tuotteet** > **Vapautetut tuotteet**.
2. Valitse tuote ruudukossa.
3. Valitse **Ulkomaankauppa**-pikavälilehden **Intrastat**-osan **Kauppatavara**-kentässä kauppatavarakoodi. Kauppatavaran nimi tulostetaan **Kauppatavaroiden kuvaus** -kenttään Intrastat-raportissa.
4. Valitse tuotteen alkuperämaa tai -alue **Alkuperä**-osan **Maa tai alue** -kenttä.
5. Anna **Varastonhallinta**-pikavälilehden **Nettopaino**-kentässä tuotteen paino kilogrammoina.

## <a name="set-up-compression-of-intrastat"></a>Intrastatin tiivistysasetukset

-   Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Intrastatin pakkaus** ja valitse sitten kentät, joita on vertailtava, kun Intrastat-tiedoista tehdään yhteenveto. Valitse Puolan Intrastat-raporttiin seuraavat kentät:

    - Kauppatavara
    - Tapahtumakoodi
    - Alkuperämaa/-alue
    - Välitys
    - Toimitusehdot
    - Lähettäjän maa tai alue
    - Maa/alue
    - Korjaus
    - ALV-tunnus
    - Siirtosuunta
    - Lasku

## <a name="set-up-the-transport-method-and-delivery-terms"></a>Kuljetustavan ja toimitusehtojen määrittäminen

1.  Määritä kuljetuskoodit.

    1. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Kuljetustapa**.
    2. Valitse toimintoruudussa **Uusi**.
    3. Anna yksilöivä koodi **Kuljetus**-kentässä. Puolan yrityksissä käytetään yksinumeroisia kuljetuskoodeja.

2.  Määritä toimitustavan Intrastat-koodit.

    1. Valitse **Hankinta** > **Määritys** > **Jakelu** > **Toimitusehdot**.
    2. Valitse ruudukossa toimitusehdot.
    3. Anna **Yleinen**-pikavälilehden **Intrastat-koodi**-kentässä yksilöivä koodi.

## <a name="intrastat-transfer"></a>Intrastat-siirto

**Intrastat**-sivulla voit valita **Siirto**-kentässä automaattisesti siirrettäviksi yhteisön sisäistä kauppaa koskevat tiedot myyntitilauksesta, vapaatekstilaskuista, ostotilauksista, toimittajalaskuista, toimittajan tuotteen vastaanotoista, projektilaskuista ja siirtotilauksista. Vain ne asiakirjat siirretään, joissa on EU-maa on kohde- tai lähettäjämaa tai -alue, siirretään.

Tapahtuvat voidaan antaa myös manuaalisesti valitsemalla toimintoruudussa **Uusi**.

### <a name="generate-an-intrastat-report"></a>Luo Intrastat-raportti

1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
2. Valitse toimintoruudussa **Tuloste** &gt; **Raportti**.
3. Määritä seuraavat kentät **Intrastat-raportti**-valintaruudussa.

    | Kenttä | Kuvaus |
    |-------------------------|-------------------------|
    | Päivämäärästä | Valitse raportin aloituspäivä. |
    | Luo tiedosto | Luo Intrastat-raportin .xml-tiedosto valitsemalla tämän vaihtoehdon arvoksi **Kyllä**. |
    | Tiedostonimi | Anna xml-tiedoston nimi. |
    | Luo raportti | Luo Intrastat-raportin .xlsx-tiedosto valitsemalla tämän vaihtoehdon arvoksi **Kyllä**. |
    | Raporttitiedoston nimi | Anna .xlsx-tiedoston nimi. |
    | Siirtosuunta | Valitse **Saapumiset**, kun haluat raportin yhteisön sisäisistä saapumisista.</br>Valitse **Lähetykset**, kun haluat raportin yhteisön sisäisistä lähetyksistä. |
    | Ilmoituksen tunnus | Asiakirjatunnus luodaan automaattisesti, ja sen voi päivittää. |
    | Ilmoitustyyppi | Valitse alkuperäisen ilmoituksen **Ilmoitus**.</br>Valitse muutosilmoituksessa **Muutosilmoitus – korvaus**, jonka tarkoituksena on korvata täysin aiemmin luotu ja lähetetty alkuperäinen ilmoitus tai muutosilmoitus. |
    | Tiedoston luontipaikkakunta | Anna tulostettava arvo Intrastat-raportin **Miejscowosc**-kentässä. |
    | Asiakirjan luontipäivä | Anna tulostettava arvo Intrastat-raportin **Deklaracja Data** -kentässä. |
    | Tiedoston numero | Anna tulostettava arvo Intrastat-raportin **Numer**-kentässä. |
    | Asiakirjan versio | Anna tulostettava arvo Intrastat-raportin **Wersja**-kentässä. |

4. Valitse **OK** ja tarkista luodut raportit.

## <a name="example"></a>Esimerkki

Tässä esimerkissä näytetään **DEMF**-yrityksen avulla, miten tuonti ja vienti kirjataan Intrastat-raportointia varten.

### <a name="preliminary-setup"></a>Alustavat asetukset

Seuraavien ER-määritysten uusin versio on tuotava:

   - Intrastat-malli
   - Intrastat-raportti
   - Intrastat (PL)

### <a name="set-up-a-company-address"></a>Yrityksen osoitteen määrittäminen

1. Valitse **Organisaation hallinto** > **Yleinen osoitekirja** > **Osoitteet** > **Osoitemääritys**.
2. Valitse **Paikkakunta**-välilehdessä **Uusi**.
3. Valitse **Maa tai alue**-kentässä **POL**.
4. Anna **Paikkakunta**-kenttään **Varsova**.
5. Valitse **Postinumero**-välilehdessä **Uusi**.
6. Valitse **Maa tai alue**-kentässä **POL**.
7. Valitse **Paikkakunta**-kentässä **Varsova**.
8. Anna **Postinumero**-kenttään **00-844**.
9. Valitse **Organisaation hallinta** > **Organisaatio** > **Yritykset** ja valitse **DEMF**-yritys.
10. Valitse **Osoitteet**-pikavälilehdessä **Muokkaa**.
11. Valitse **Maa tai alue**-kentässä **POL**.
12. Valitse **Postinumero**-kentässä **31-111**.
13. Anna **Katuosoite**-kenttään **Statystyczna 22/1**.
14. Valitse **Paikkakunta**-kentässä **Varsova**.
15. Valitse **OK**.

## <a name="set-up-a-vat-id-and-an-enterprise-number-code-for-your-company"></a>Yrityksen ALV-tunnuksen ja yrityksen numerokoodin määrittäminen

### <a name="create-registration-types-for-company-codes"></a>Yrityskoodien rekisteröintityyppien luominen

1. Valitse **Organisaation hallinto** > **Yleinen osoitekirja** > **Rekisteröintityypit** > **Rekisteröintityypit**.
2. Luo ALV-tunnuksen (NIP-koodi) rekisteröintityyppi valitsemalla toimintoruudussa **Uusi**.
3. Anna **Määritä rekisteröintityypin tiedot** -valintaikkunan **Nimi**-kenttään **NIP**.
4. Valitse **Maa tai alue**-kentässä **POL**.
5. Valitse **Luo**.
6. Luo yrityksen numeron (Regon-koodi) rekisteröintityyppi valitsemalla toimintoruudussa **Uusi**.
7. Anna **Määritä rekisteröintityypin tiedot** -valintaikkunan **Nimi**-kenttään **Regon**.
8. Valitse **Maa tai alue**-kentässä **POL**.
9. Valitse **Luo**.

### <a name="match-the-registration-types-with-registration-categories"></a>Rekisteröintityyppien ja rekisteröintiluokkien kohdistaminen

1. Valitse **Organisaation hallinto** > **Yleinen osoitekirja** > **Rekisteröintityypit** > **Rekisteröintiluokat**.
2. Luo kunkin luodun rekisterityypin ja rekisteriluokan välille linkki valitsemalla toimintoruudussa **Uusi**.

    - Valitse **NIP**-rekisteröintityypiksi **ALV-tunnus**-rekisteröintiluokka.
    - Valitse **Regon**-rekisteröintityypiksi **Yrityksen tunnus (COID)** -rekisteröintiluokka.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Yrityksen ALV-tunnuksen ja yrityksen numeron määrittäminen

1. Valitse **Organisaation hallinto** > **Organisaatiot** > **Yritykset**.
2. Valitse ruudukossa **DEMF**.
3. Valitse toimintoruudussa **Rekisteröintitunnukset**.
4. Valitse **Rekisteröintitunnus**-pikavälilehdessä **Lisää**.
5. Valitse **Rekisteröintityyppi**-kentässä **NIP**.
6. Anna **Rekisteröintinumero**-kentässä **1234567890**.
7. Valitse **Lisää**.
8. Valitse **Rekisteröintityyppi**-kentässä **Regon**.
9. Anna **Rekisteröintinumero**-kentässä **12345678901234**.

### <a name="set-up-a-number-sequence-code"></a>Numerosarjan koodin määrittäminen

1. Valitse **Organisaation hallinta** > **Numerosarjat** > **Numerosarjat**.
2. Valitse toimintoruudun **Numerosarja**-välilehden **Uusi**-ryhmässä **Numerosarja**.
3. Anna **Tunnus**-pikavälilehden **Numerosarjan koodi** -kentässä **XML\_tiedosto**.
4. Valitse **Laajuuden parametrit** -pikavälilehden **Laajuus**-kentässä **Yritys**.
5. Valitse **Yritys**-kentässä **DEMF**.
6. Anna **Segmentit**-pikavälilehden **Aakkosnumeerinen**-segmentin **Pituus**-kentässä **4**.
7. Määritä **Jatkuva**-asetuksen arvoksi **Ei** **Määritys**-osan **Yleiset**-pikavälilehdessä.
8. Anna **Numeroiden kohdistus** -osan **Suurin**-kentässä **9999**.

### <a name="set-up-foreign-trade-parameters"></a>Määritä ulkomaankaupan parametrit

1. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Ulkomaankaupan parametrit**.
2. Valitse **Intrastat**-välilehden **Yleiset**-pikavälilehden **Tapahtumakoodi**-kentässä **11**.
3. Valitse **Sähköinen raportointi** -pikavälilehden **Tiedostomuodon määritys** -kentässä **Intrastat (PL)**.
4. Valitse **Raporttimuodon yhdistäminen** -kentässä **Intrastat-raportti**.
5. Varmista, että **Kauppatavarakoodihierarkia**-pikavälilehden **Luokkahierarkia**-kenttään on määritetty **Intrastat**.
6. Valitse **Maan tai alueen ominaisuudet** -välilehdessä **Uusi**.
7. Valitse **Osapuolen maa/alue**-kentässä **POL**. Valitse sitten **Maa-/aluetyyppi**-kentässä **Kotimaa**.
8. Valitse **Osapuolen maa/alue**-kentässä **DEU**. Valitse sitten **Maa-/aluetyyppi**-kentässä **EU**.
9. Anna **Edustaja**-välilehden **Edusta**-pikavälilehden **Arvonlisävero**-osan **Verovapausnumero**-kentässä **420000**.
10. Anna **Yhteyshenkilö**-välilehden **Nimi**-kentässä **Manish Chopra**.
11. Anna **Puhelin**-kenttään arvo **425-555-5068**.
12. Anna **Faksinumero**-kenttään arvo **425-555-5049**.
13. Anna **Sähköposti**-kenttään **manishc@contoso.com**.
14. Valitse **Numerosarjat**-välilehden **XML-tiedostonumero**-viitteen **Numerosarjan koodi** -kentässä **XML\_tiedosto**.

### <a name="set-up-product-information"></a>Tuotetietojen määrittäminen

1. Valitse **Tuotetietojen hallinta** > **Tuotteet** > **Vapautetut** **tuotteet**.
2. Valitse ruudukossa **D0001**.
3. Valitse **Ulkomaankauppa**-pikavälilehden **Intrastat**-osan **Kauppatavara**-kentässä **100 200 30**.
4. Anna **Nettopaino**-kentässä **2** **Varastonhallinta**-pikavälilehden **Painomitat**-osassa.
5. Valitse toimintoruudussa **Tallenna**.
6. Valitse ruudukossa **D0003**.
7. Valitse **Ulkomaankauppa**-pikavälilehden **Intrastat**-osan **Kauppatavara**-kentässä **100 200 30**.
8. Valitse **Alkuperä**-osan **Maa tai alue** -kentässä **DEU**.
9. Anna **Nettopaino**-kentässä **5** **Varastonhallinta**-pikavälilehden **Painomitat**-osassa.
10. Valitse toimintoruudussa **Tallenna**.

### <a name="change-the-site-address"></a>Toimipaikan osoitteen muuttaminen

1. Valitse **Varastonhallinta** > **Asetukset** > **Varasto** > **Toimipaikat**.
2. Valitse ruudukossa **1**.
3. Valitse **Osoitteet**-pikavälilehdessä **Muokkaa**.
4. Valitse **Muokkaa osoitetta** -valintaikkunan **Maa tai alue** -kentässä **POL**.
5. Valitse **OK**.

### <a name="set-up-a-transport-method"></a>Kuljetustavan määrittäminen

1. Luo kuljetustapa.

    1. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Kuljetustapa**.
    2. Valitse toimintoruudussa **Uusi**.
    3. Anna **Kuljetus**-kenttään arvo **3**.
    4. Anna **Kuvaus**-kenttään arvo **Maantiekuljetus**.

2. Määritä toimitustilalle uusi kuljetustapa. Tällä tavoin määritetään kuljetustavan oletusarvot, joita käytetään, kun vastaava toimitustapa valitaan.

    1. Valitse **Hankinta** > **Määritys** > **Jakelu** > **Toimitustavat**.
    2. Valitse ruudukossa **10**.
    3. Valitse **Ulkomaankauppa**-pikavälilehden **Kuljetus** -kentässä **3**.

3. Valitse asiakkaan oletustoimitustapa.

    1. Valitse **Myyntireskontra** > **Asiakkaat** > **Kaikki asiakkaat**.
    2. Valitse ruudukossa **DE-016**.
    3. Valitse **Lasku ja toimitus** -pikavälilehden **Toimitustapa**-kentässä **10**.

4. Valitse toimittajan oletustoimitustapa.

    1. Valitse **Ostoreskontra** > **Toimittajat** > **Kaikki toimittajat**.
    2. Valitse ruudukossa **DE-001**.
    3. Valitse **Lasku ja toimitus** -pikavälilehden **Toimitustapa**-kentässä **10**.

### <a name="set-up-codes-for-terms-of-delivery"></a>Toimitusehtojen koodien määrittäminen

1. Määritä toimitusehtojen Intrastat-koodi.

    1. Valitse **Hankinta** > **Määritys** > **Jakelu** > **Toimitusehdot**.
    2. Valitse ruudukossa **CIF**.
    3. Anna **Yleinen**-pikavälilehden **Intrastat-koodi**-kentässä **CIF**.

2. Valitse asiakkaan oletustoimitusehdot.

    1. Valitse **Myyntireskontra** > **Asiakkaat** > **Kaikki asiakkaat**.
    2. Valitse ruudukossa **DE-016**.
    3. Valitse **Lasku ja toimitus** -pikavälilehden **Toimitusehdot**-kentässä **CIF**.

3. Valitse toimittajan oletustoimitusehdot.

    1. Valitse **Ostoreskontra** > **Toimittajat** > **Kaikki toimittajat**.
    2. Valitse ruudukossa **DE-001**.
    3. Valitse **Lasku ja toimitus** -pikavälilehden **Toimitusehdot**-kentässä **CIF**.

### <a name="verify-an-eu-customers-tax-exempt-number-code"></a>EU-asiakkaan ALV-tunnuksen koodin tarkistaminen

1. Valitse **Myyntireskontra** > **Asiakkaat** > **Kaikki asiakkaat**.
2. Valitse ruudukossa **DE-016**.
3. Tarkista **Lasku ja toimitus** -pikavälilehden **Arvonlisävero**-osassa, että **ALV-tunnus**-kentän asetuksena on **DE9012**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>EU-asiakkaan myyntitilauksen luominen

1. Valitse **Myyntireskontra** > **Tilaukset** > **Kaikki myyntitilaukset**.
2. Valitse toimintoruudussa **Uusi**.
3. Valitse **Luo myynti tilaus** -valintaikkunan **Asiakas**-pikavälilehden **Asiakas**-osan **Asiakastili**-kentässä **DE-016**.
4. Valitse **Yleiset**-pikavälilehden **Varastodimensiot**-osan **Toimipaikka**-kentässä **1**.
5. Valitse **Varasto**-kentässä **11**.
6. Tarkista **Osoite**-välilehden **Osoite**-kentän asetuksena on **Teichgasse 12, Kiel, 24103, DEU**, koska asiakas on Saksasta.
7. Valitse **OK**.
8. Tarkista **Otsikko**-välilehden **Toimitus**-pikavälilehdessä, että **Toimitusehdot**-kentän asetuksena on **CIF** ja että **Toimitustapa**-kentän asetuksena on **10**.
9. Valitse **Rivit**-välilehden **Myyntitilauksen rivit** -pikavälilehden **Nimikkeen numero** -kentässä **D0001**. Anna sitten **Määrä**-kenttään **8**.
10. Tarkista **Ulkomaankauppa**-välilehden **Rivin erittely** -pikavälilehdessä, että **Tapahtumakoodi**-kentän asetuksena on **11**, **Kauppatavara**-kentän asetuksena on **100 200 30** ja **Alkuperämaa tai -alue** -kentän asetuksena on **POL**.
11. Valitse toimintoruudussa **Tallenna**.
12. Valitse Toimintoruudun **Laskutus**-välilehden **Luo**-ryhmässä **Lasku**.
13. Valitse **Laskun kirjaus**-valintaikkunan **Parametrit**-pikavälilehden **Parametri**-osan **Määrä**-kentästä **Kaikki**.
14. Valitse **Määritys**-pikavälilehden **Myyntipäivämäärä**-kentässä **18.10.2021** (18. lokakuuta 2021).
15. Kirjaa lasku valitsemalla **OK**.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Tapahtuman siirtäminen Intrastat-kirjauskansioon ja tuloksen tarkistaminen

1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
2. Valitse toimintoruudussa **Siirto**.
3. Määritä **Intrastat (Siirto)** -valintaikkunan **Parametrit**-osassa **Myyntilasku**-asetuksen arvoksi **Kyllä**.
4. Valitse **Suodata**.
5. Valitse **Intrastat-suodatin**-valintaikkunan **Alue**-välilehdessä ensimmäinen rivi ja tarkista, että **Kenttä**-kentän arvo on **Päivämäärä**.
6. Valitse **Ehdot**-kentässä kuluva päivä.
7. Sulje **Intrastat-suodatin**-valintaikkuna valitsemalla **OK**.
8. Sulje **Intrastat (siirto)** -valintaikkuna valitsemalla **OK** ja tarkista tulos. Rivi ilmaisee aiemmin luodun myyntitilauksen.

    ![Intrastat-sivulla olevan myyntitilauksen ilmaiseva rivi](media/intrastat_pl_1.png)

9. Saat lisätietoja valitsemalla ensin tapahtumarivin ja sitten **Yleiset**-välilehden.

    ![Myyntitilauksen tiedot Intrastat-sivun Yleiset-välilehdessä](media/intrastat_pl_2.png)

10. Valitse toimintoruudussa **Tuloste** > **Raportti**.
11. Valitse **Intrastat-raportti**-valintaikkunan **Parametrit**-pikavälilehden **Päivämäärä**-osan **Päivämäärästä**-kentässä kuluvan kuukauden ensimmäinen päivä.
12. Määritä **Vientiasetukset**-osassa **Muodosta** **tiedosto** -asetuksen arvoksi **Kyllä**. Anna sitten **Tiedostonimi**-kenttään tarvittava nimi.
13. Määritä **Luo raportti** -asetukseksi **Kyllä**. Anna sitten **Raporttitiedoston nimi** -kenttään tarvittava nimi.
14. Valitse **Suunta**-kentässä **Vienti**.
15. Tarkista **Tiedostomuodon määritys** -osassa, että **Ilmoitustyyppi**-kentän asetuksena on **Ilmoitus**.
16. Anna **Asiakirjan luonnin kaupunki** -kentässä **Krakova**.
17. Valitse **Asiakirjan luonnin kaupunki** -kentässä **19.10.2021** (19. lokakuuta 2021).
18. Anna **Asiakirjan numero** -kenttään **11**.
19. Anna **Asiakirjan versio** -kenttään **22**.
20. Valitse **OK** ja tarkista luotu XML-muotoinen raportti. Seuraavassa taulukossa on esimerkkiraportin arvot.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Kentän nimi</strong></p>
    </td>
    <td>
    <p><strong>Kentän kuvaus</strong></p>
    </td>
    <td>
    <p><strong>Arvo</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Tietoja asiakirjasta</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja Data</p>
    </td>
    <td>
    <p>Päivämäärä, jona tiedosto on luotu.</p>
    </td>
    <td>
    <p>19.10.2021</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>Paikkakunta, jossa asiakirja luotiin.</p>
    </td>
    <td>
    <p>Krakova</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Nimikkeiden kokonaismäärä.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Tilastollinen kokonaisarvo.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>Laskun kokonaisarvo.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Yksikkökoodi.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Ilmoituksen tyyppi.</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Asiakirjan versio.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numer</p>
    </td>
    <td>
    <p>Asiakirjan numero.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="330">
    <p>Viitekuukausi.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="330">
    <p>Viitevuosi.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="330">
    <p>Raportin suunta.</p>
    </td>
    <td>
    <p>K</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="330">
    <p>Ilmoituksen tunnus.</p>
    </td>
    <td>
    <p>21ISTDEMF-0001</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Tietoja yrityksestä</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="330">
    <p>Paikkakunta, jossa yritys sijaitsee.</p>
    </td>
    <td>
    <p>Varsova</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="330">
    <p>Yrityksen Regon-koodi.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>Yrityksen NIP-koodi.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>Yrityksen postinumero.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>Katuosoite, jossa yritys sijaitsee.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>Yrityksen nimi.</p>
    </td>
    <td>
    <p>Contoso Entertainment System Germany</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Tietoja tavarasta</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>Tilastollinen arvo.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>Laskun arvo.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Nettopaino.</p>
    </td>
    <td>
    <p>16</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>IdKontrahenta</p>
    </td>
    <td>
    <p>Asiakkaan ALV-numero.</p>
    </td>
    <td>
    <p>DE9012</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>Kauppatavarakoodi.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Tapahtumakoodi.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>Toimitustavan ehdot.</p>
    </td>
    <td>
    <p>CIF (Kulut, vakuutus ja rahti maksettuna)</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>Vienti- tai tuontimaan maa- tai aluekoodi.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>Kauppatavaroiden kuvaus.</p>
    </td>
    <td>
    <p>Laitteisto</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>Nimikkeen numero.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Yhteystiedot</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Sähköpostiosoite</p>
    </td>
    <td>
    <p>Lähettäjän sähköpostiosoite.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Lähettäjän faksin numero.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>Lähettäjän puhelinnumero.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>Lähettäjän nimi.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

21. Tarkista luotu Excel-muotoinen raportti.

    ![Viennin Intrastat-raportti](media/intrastat_pl_3.png)

### <a name="create-a-purchase-order"></a>Luo ostotilaus

1. Valitse **Ostoreskontra** > **Ostotilaukset** > **Kaikki ostotilaukset**.
2. Valitse toimintoruudussa **Uusi**.
3. Valitse **Luo ostotilaus** -valintaikkunan **Toimittajatili**-kentässä **DE-001**.
4. Valitse **Toimipaikka**-kentässä **1**.
5. Valitse **Varasto**-kentässä **11**.
6. Valitse **OK**.
7. Tarkista **Otsikko**-välilehden **Toimitus**-pikavälilehdessä, että **Toimitustapa**-kentän asetuksena on **10** ja että **Toimitusehdot**-kentän asetuksena on **CIF**.
8. Valitse **Rivit**-välilehden **Ostotilauksen rivit** -pikavälilehden **Nimikkeen numero** -kentässä **D0003**. Anna sitten **Määrä**-kenttään **6**.
9. Tarkista **Ulkomaankauppa**-välilehden **Rivin erittely** -pikavälilehdessä, että **Tapahtumakoodi**-kentän asetuksena on **11**, **Kuljetus**-kentän asetuksena on **3** ja **Kauppatavara**-kentän asetuksena on **100 200 30** ja **Alkuperämaa tai -alue** -kentän asetuksena on **DEU**.
10. Valitse toimintoruudun **Ostot**-välilehden **Toiminnot**-ryhmässä **Vahvista**.
11. Valitse Toimintoruudun **Laskutus**-välilehden **Luo**-ryhmässä **Lasku**.
12. Valitse toimitusruudussa **Oletuslomake** ja valitse sitten **Rivien oletusmäärä** -kentässä **Tilattu määrä**. Valitse sitten **OK**.
13. Anna **Toimittajan laskun otsikko** -pikavälilehden **Laskun tunnus** -osan **Numero**-kentässä **00010**.
14. Valitse **Laskujen päivämäärät** -osan **Laskun päivämäärä** -kentässä kuluva päivämäärä. Tätä päivämäärää käytetään Intrastat-siirrossa.
15. Valitse **Asiakirjan vastaanottopäivämäärä** -kentässä **18.10.2021** (18. lokakuuta 2021).
16. Kirjaa lasku valitsemalla toimintoruudussa **Kirjaa**.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Tuonnin Intrastat-ilmoituksen luominen

1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
2. Valitse toimintoruudussa **Siirto**.
3. Määritä **Intrastat (Siirto)** -valintaikkunan **Toimittajan lasku**-asetukseksi **Kyllä**.
4. Siirrä tapahtumat valitsemalla **OK** ja tarkista sitten Intrastat-kirjauskansio.

    ![Intrastat-sivulla olevan ostotilauksen ilmaiseva rivi](media/intrastat_pl_4.png)

5. Tarkastele ostotilauksen **Yleiset**-välilehden tietoja.

    ![Ostotilauksen tiedot Intrastat-sivun Yleiset-välilehdessä](media/intrastat_pl_5.png)

6. Valitse toimintoruudussa **Tuloste** > **Raportti**.
7. Valitse **Intrastat-raportti**-valintaikkunan **Parametrit**-pikavälilehden **Päivämäärä**-osan **Päivämäärästä**-kentässä kuluvan kuukauden ensimmäinen päivä.
8. Määritä **Vientiasetukset**-osassa **Muodosta** **tiedosto** -asetuksen arvoksi **Kyllä**. Anna sitten **Tiedostonimi**-kenttään tarvittava nimi.
9. Määritä **Luo raportti** -asetukseksi **Kyllä**. Anna sitten **Raporttitiedoston nimi** -kenttään tarvittava nimi.
10. Valitse **Suunta**-kentässä **Tuonti**.
11. Tarkista **Tiedostomuodon määritys** -osassa, että **Ilmoitustyyppi**-kentän asetuksena on **Ilmoitus**.
12. Anna **Asiakirjan luonnin kaupunki** -kentässä **Krakova**.
13. Valitse **Asiakirjan luonnin kaupunki** -kentässä **19.10.2021** (19. lokakuuta 2021).
14. Anna **Asiakirjan numero** -kenttään **11**.
15. Anna **Asiakirjan versio** -kenttään **22**.
16. Valitse **OK** ja tarkista luotu XML-muotoinen raportti. Seuraavassa taulukossa on esimerkkiraportin arvot.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Kentän nimi</strong></p>
    </td>
    <td>
    <p><strong>Kentän kuvaus</strong></p>
    </td>
    <td>
    <p><strong>Arvo</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Tietoja asiakirjasta</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja Data</p>
    </td>
    <td>
    <p>Päivämäärä, jona tiedosto on luotu.</p>
    </td>
    <td>
    <p>19.10.2021</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>Paikkakunta, jossa asiakirja luotiin.</p>
    </td>
    <td>
    <p>Krakova</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Nimikkeiden kokonaismäärä.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Tilastollinen kokonaisarvo.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>Laskun kokonaisarvo.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Yksikkökoodi.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Ilmoituksen tyyppi.</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Asiakirjan versio.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numer</p>
    </td>
    <td>
    <p>Asiakirjan numero.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="332">
    <p>Viitekuukausi.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="332">
    <p>Viitevuosi.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="332">
    <p>Raportin suunta.</p>
    </td>
    <td>
    <p>P</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="332">
    <p>Ilmoituksen tunnus.</p>
    </td>
    <td>
    <p>21ISTDEMF-0002</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Tietoja yrityksestä</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="332">
    <p>Paikkakunta, jossa yritys sijaitsee.</p>
    </td>
    <td>
    <p>Varsova</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="332">
    <p>Yrityksen Regon-koodi.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>Yrityksen NIP-koodi.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>Yrityksen postinumero.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>Katuosoite, jossa yritys sijaitsee.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>Yrityksen nimi.</p>
    </td>
    <td>
    <p>Contoso Entertainment System Germany</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Tietoja tavarasta</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>Tilastollinen arvo.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>Laskun arvo.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Nettopaino.</p>
    </td>
    <td>
    <p>30</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzenia</p>
    </td>
    <td>
    <p>Alkuperämaan tai -alueen koodi.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransportu</p>
    </td>
    <td>
    <p>Kuljetustavan koodi.</p>
    </td>
    <td>
    <p>3</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>Kauppatavarakoodi.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Tapahtumakoodi.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>Toimitustavan ehdot.</p>
    </td>
    <td>
    <p>CIF (Kulut, vakuutus ja rahti maksettuna)</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>Vienti- tai tuontimaan maa- tai aluekoodi.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>Kauppatavaroiden kuvaus.</p>
    </td>
    <td>
    <p>Laitteisto</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>Nimikkeen numero.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Yhteystiedot</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Sähköpostiosoite</p>
    </td>
    <td>
    <p>Lähettäjän sähköpostiosoite.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Lähettäjän faksin numero.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>Lähettäjän puhelinnumero.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>Lähettäjän nimi.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

17. Tarkista luotu Excel-muotoinen raportti.

    ![Tuonnin Intrastat-raportti](media/intrastat_pl_6.png)
